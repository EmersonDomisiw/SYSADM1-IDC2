![image](https://github.com/user-attachments/assets/e0689427-af1c-4669-ac18-892388c664df)



# SYSADM1 -- Kerberos Lab Activity: A step-by-step Guide

> **Objective:**
>
> Set up a basic Kerberos authentication system to understand how
> Kerberos manages secure logins through ticket-based access.
>
> **Setup Requirements:**

-   Two VMs in Oracle VM, both running a Linux distribution like Ubuntu
    > or CentOS.

-   VM1: Kerberos Server

-   VM2: Kerberos Client

> **Step 1: Initial Setup and Package Installation**

1.  **Update Packages on Both VMs:**

    -   Open a terminal on each VM and run:

> *bash*
>
> *sudo apt update && sudo apt upgrade --y*
>
![image](https://github.com/user-attachments/assets/5c3a4ccf-267f-4c66-b15a-1d9d83f2a899)

![image](https://github.com/user-attachments/assets/3adb7d66-1805-4d4a-9552-c016c29ed706)



2.  **Install Kerberos Server Packages on VM1 (Kerberos Server):**

    -   In VM1, install the Kerberos Key Distribution Center (KDC) and
        > admin server:

> *bash*
>
> *sudo apt install krb5-kdc krb5-admin-server --y*
>
![image](https://github.com/user-attachments/assets/30db0f1b-bc3e-4734-bc08-20f84fe37864)


3.  **Install Kerberos Client Package on VM2 (Kerberos Client):**

    -   In VM2, install the Kerberos client software:

> *bash*
>
> *sudo apt install krb5-user -y*

-   During installation, when prompted, enter the Kerberos realm you
    > plan to set up, e.g., MYLAB.LOCAL.

![image](https://github.com/user-attachments/assets/ee77c62d-488c-4439-a2c0-252f9ad994f5)


> **Step 2: Configure the Kerberos Server (VM1)**

1.  **Edit the Kerberos Configuration File:**

    -   Open /etc/krb5.conf for editing:

> *bash*
>
> *sudo nano /etc/krb5.conf*

-   Set the realm as MYLAB.LOCAL. You should also specify the KDC and
    > admin server as VM1's hostname or IP address:

> ini
>
> \[libdefaults\]
>
> default_realm = MYLAB.LOCAL
>
> \[realms\]
>
> MYLAB.LOCAL = {
>
> kdc = \<VM1_IP_or_hostname\>
>
> admin_server = \<VM1_IP_or_hostname\>
>
> }
>


-   Save and close the file (Ctrl+X, then Y, and Enter to confirm).

  
> ![image](https://github.com/user-attachments/assets/31f0eb05-bbdd-45be-b513-034577785a20)

2.  **Initialize the Kerberos Database:**

    -   Create the database for the Kerberos realm:

> *bash*
>
> *sudo krb5_newrealm*

-   You will be prompted to set a password for the Kerberos database.

![image](https://github.com/user-attachments/assets/b5be4095-6974-462e-8dac-502846191fe4)


3.  **Start and Enable the Kerberos Services:**

    -   Start the KDC and admin server, and ensure they start
        > automatically on boot:

> *bash*
>
> *sudo systemctl start krb5-kdc*
>
> *sudo systemctl start krb5-admin-server*
>
> *sudo systemctl enable krb5-kdc*
>
> *sudo systemctl enable krb5-admin-server*
>
![image](https://github.com/user-attachments/assets/aad01c54-e501-43bf-ae49-e4eb6c7b4bbe)

>
> **Step 3: Set Up a Kerberos User Principal**

1.  **Create a New User Principal:**

    -   Run the following command to create a test user in the Kerberos
        > realm:

> *bash*
>
> *sudo kadmin.local -q \"addprinc testuser@MYLAB.LOCAL\"*

-   Set a password for testuser.

![image](https://github.com/user-attachments/assets/bf554609-2d76-4768-bdbd-f0e86701c929)


2.  **Verify the User Principal:**

    -   To confirm the principal is created, list all principals:

> *bash*
>
> *sudo kadmin.local -q \"listprincs\"*
>
![image](https://github.com/user-attachments/assets/69bae4a6-d9ff-4961-aaef-b8599ef760b0)

>
> **Step 4: Configure the Kerberos Client (VM2)**

1.  **Edit the Kerberos Configuration File on VM2:**

    -   Open /etc/krb5.conf for editing on VM2:

> *bash*
>
> *sudo nano /etc/krb5.conf*

-   Set the default realm to MYLAB.LOCAL and point to the KDC and admin
    > server on VM1. The configuration should match what you set on VM1.

![image](https://github.com/user-attachments/assets/ea8d18d2-8222-48d6-864a-b657d0cdfa2e)

>
> **Step 5: Test Kerberos Authentication**

1.  **Request a Kerberos Ticket for the User on VM2:**

    -   In the terminal on VM2, request a ticket for testuser:

> *bash*
>
> *kinit testuser@MYLAB.LOCAL*

-   Enter the password you set for testuser.

![image](https://github.com/user-attachments/assets/d14d906d-6e2e-43ce-af35-04a9f2da5982)


2.  **Verify the Ticket:**

    -   Check if the ticket was issued by listing active Kerberos
        > tickets:

> *bash*
>
> *list*

-   You should see details about the ticket, such as the principal and
    > expiration time, confirming successful Kerberos authentication.

![image](https://github.com/user-attachments/assets/6a94944d-6b71-4ffc-b518-cb2fb739df30)

