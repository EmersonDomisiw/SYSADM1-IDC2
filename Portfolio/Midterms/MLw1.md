![image](https://github.com/user-attachments/assets/f6314fc0-7549-427b-a1f6-28fe89133df1)


# SYSADM1 -- Monitoring Print Services in Windows Server 2019

# Requirement: 

-   A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1.  Install and configure **print.srv** domain

![image](https://github.com/user-attachments/assets/530c1747-2420-4025-a20f-4612d611d148)


2.  Connect one client to the recently created domain

![image](https://github.com/user-attachments/assets/5aa0c10a-d63b-4f6a-a845-751f77e23b2c)
![image](https://github.com/user-attachments/assets/084fd682-f961-4387-940e-eea860c719ab)


3.  Install Print Services Role:

![image](https://github.com/user-attachments/assets/a9701e3c-4212-4450-bc3f-49d493520242)


4.  Search the internet for any printer installer and convert it to iso

![image](https://github.com/user-attachments/assets/ab933310-b76b-484e-82b4-fcf013a1e4ee)


5.  Install and deploy it as network printer

![image](https://github.com/user-attachments/assets/22f0b74d-f739-40ab-b46f-36ee7967f97e)

Part 2: Monitoring Print Services

Objective: Familiarize yourself with monitoring tools available in
Windows Server 2019.

1.  Event Viewer:

    -   Open Event Viewer (run eventvwr.msc).

    -   Navigate to Applications and Services Logs \> Microsoft \>
        Windows \> PrintService.

    -   Review logs for print jobs, errors, and warnings.

![image](https://github.com/user-attachments/assets/e33cf393-ae2e-4faa-8061-84a773d706d2)


2.  Performance Monitor:

    -   Open Performance Monitor (run perfmon).

    -   In the left pane, expand Data Collector Sets \> System.

    -   Right-click System Performance and select Start.

    -   Monitor performance metrics related to print services.

![image](https://github.com/user-attachments/assets/200c490f-f2c5-4a9e-a960-4e59e25de86a)


3.  Using Print Management Console:

    -   Open Print Management from Server Manager.

    -   View active print jobs and their status.

    -   Use the Printers node to check the status of all printers.

![image](https://github.com/user-attachments/assets/7f04dc3c-56a9-4fa5-bdf6-decd2a9bdb98)


Part 3: Exploring Third-Party Monitoring Tools

1.  Research at least two third-party print monitoring tools

    -   Consider factors such as features, pricing, and compatibility
        with Windows Server 2019.

![image](https://github.com/user-attachments/assets/935f9c50-26cf-4186-8dd4-d55405f769dc)


2.  Install and Configure:

    -   Choose one of the tools to install in your environment.

    -   Follow the installation instructions provided by the tool\'s
        documentation.

    -   Configure it to monitor your print services.

3.  Test and Report Findings:

    -   Generate a report or dashboard from the tool.

    -   Analyze the collected data (e.g., print volume, errors, user
        activity).

![image](https://github.com/user-attachments/assets/a823f7cd-3fe8-49b5-a302-db81684e7cb8)

![image](https://github.com/user-attachments/assets/3901c696-e1b5-4a48-ad6c-94a71b0a4a73)

![image](https://github.com/user-attachments/assets/e9f65dbb-b7fe-425e-b874-cf6aba5853aa)


