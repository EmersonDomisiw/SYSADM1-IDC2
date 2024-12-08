+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 841c422378184c808e07fe043178786e |                        |          |
| /media/image6.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+==================================+========================+==========+
| NAME: Lara Mae Laruta            | DATE                   | /50      |
|                                  | PERFORMED:11/13/2024   |          |
+----------------------------------+------------------------+----------+
| Section:IDC1                     | DATE                   |          |
|                                  | SUBMITTED:11/13/204    |          |
+----------------------------------+------------------------+----------+

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
> ![](vertopal_841c422378184c808e07fe043178786e/media/image13.png){width="6.125295275590551in"
> height="2.1483027121609797in"}
>
> *SERVER*
>
> ![](vertopal_841c422378184c808e07fe043178786e/media/image8.png){width="7.142697944006999in"
> height="2.7514818460192476in"}
>
> *CLIENT*

2.  **Install Kerberos Server Packages on VM1 (Kerberos Server):**

    -   In VM1, install the Kerberos Key Distribution Center (KDC) and
        > admin server:

> *bash*
>
> *sudo apt install krb5-kdc krb5-admin-server --y*
>
> ![](vertopal_841c422378184c808e07fe043178786e/media/image5.png){width="7.027083333333334in"
> height="4.351388888888889in"}

3.  **Install Kerberos Client Package on VM2 (Kerberos Client):**

    -   In VM2, install the Kerberos client software:

> *bash*
>
> *sudo apt install krb5-user -y*

-   During installation, when prompted, enter the Kerberos realm you
    > plan to set up, e.g., MYLAB.LOCAL.

> ![](vertopal_841c422378184c808e07fe043178786e/media/image3.png){width="7.027083333333334in"
> height="5.50625in"}
>
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
> ![](vertopal_841c422378184c808e07fe043178786e/media/image11.png){width="7.027083333333334in"
> height="5.830555555555556in"}

-   Save and close the file (Ctrl+X, then Y, and Enter to confirm).

2.  **Initialize the Kerberos Database:**

    -   Create the database for the Kerberos realm:

> *bash*
>
> *sudo krb5_newrealm*

-   You will be prompted to set a password for the Kerberos database.

> ![](vertopal_841c422378184c808e07fe043178786e/media/image10.png){width="7.027083333333334in"
> height="6.043055555555555in"}

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
> ![](vertopal_841c422378184c808e07fe043178786e/media/image2.png){width="6.6800120297462815in"
> height="2.0464512248468942in"}
>
> **Step 3: Set Up a Kerberos User Principal**

1.  **Create a New User Principal:**

    -   Run the following command to create a test user in the Kerberos
        > realm:

> *bash*
>
> *sudo kadmin.local -q \"addprinc testuser@MYLAB.LOCAL\"*

-   Set a password for testuser.

> ![](vertopal_841c422378184c808e07fe043178786e/media/image9.png){width="7.027083333333334in"
> height="1.525in"}

2.  **Verify the User Principal:**

    -   To confirm the principal is created, list all principals:

> *bash*
>
> *sudo kadmin.local -q \"listprincs\"*
>
> ![](vertopal_841c422378184c808e07fe043178786e/media/image7.png){width="6.844704724409449in"
> height="1.5627176290463691in"}
>
> **Step 4: Configure the Kerberos Client (VM2)**

1.  **Edit the Kerberos Configuration File on VM2:**

    -   Open /etc/krb5.conf for editing on VM2:

> *bash*
>
> *sudo nano /etc/krb5.conf*

-   Set the default realm to MYLAB.LOCAL and point to the KDC and admin
    > server on VM1. The configuration should match what you set on VM1.

> ![](vertopal_841c422378184c808e07fe043178786e/media/image1.png){width="7.027083333333334in"
> height="4.788194444444445in"}
>
> **Step 5: Test Kerberos Authentication**

1.  **Request a Kerberos Ticket for the User on VM2:**

    -   In the terminal on VM2, request a ticket for testuser:

> *bash*
>
> *kinit testuser@MYLAB.LOCAL*

-   Enter the password you set for testuser.

> ![](vertopal_841c422378184c808e07fe043178786e/media/image4.png){width="5.511185476815398in"
> height="0.8021948818897637in"}

2.  **Verify the Ticket:**

    -   Check if the ticket was issued by listing active Kerberos
        > tickets:

> *bash*
>
> *list*

-   You should see details about the ticket, such as the principal and
    > expiration time, confirming successful Kerberos authentication.

> ![](vertopal_841c422378184c808e07fe043178786e/media/image12.png){width="7.027083333333334in"
> height="1.8576388888888888in"}
