SERADM1

  ----------------------------------- -----------------------------------
  Name: Domisiw, Emerson P.           Date: 04/12/24

  Section: IDB1                       Title of Activity: LW2 Deploying a
                                      Network Printer
  ----------------------------------- -----------------------------------

This activity will guide you through deploying a printer on a Windows
Server 2019 machine.

Preparation:

1\. Working server-client virtual machines.

2\. Create **Z:\\lastnameF** folder

3\. Transfer FLW1 in this folder

4\. Record a video-output FLW2 and save it in the drive specified in the
previous instruction. The video should have a maximum duration of 2
minutes.

*Domain: Domisiw.org*

Instructions:

A. Install Print Server Role:

1\. Open Server Manager.

2\. Click Add roles and features.

3\. Select Role-based or feature-based installation and click Next.

4\. Choose the destination server and click Next.

5\. Expand Print and Document Services, click Add Features (if
prompted), and click Next twice.

6\. In Role services, select Print Server and click Next twice.

7\. Review the selections and click Install.

B. Add and Configure Printer:

1\. Open Print Management (search for it in the Start Menu).

2\. In the Actions pane, click Add Printer.

3\. Select Create a new port and choose Standard TCP/IP Port.

4\. Enter the printer's IP address (hypothetical scenario) and click
Next.

5\. Windows will search for drivers. If found, select the appropriate
driver and click Next.

6\. Give the printer a recognizable name (e.g., Student Printer 1) and
optionally set it as the default printer.

7\. Check the Share this printer box and click Finish.

C. Deploying with Group Policy:

1\. Create a group policy that will allow two users to access the
network printer you deployed and one user that cannot access it.

![](vertopal_1e094e0c7b26499199a17d02c2e1a7c3/media/image1.png){width="6.483333333333333in"
height="3.5083333333333333in"}
