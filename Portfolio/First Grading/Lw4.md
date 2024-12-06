+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 418037ccb2504c81b17cb64bdcef7907 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: Domisiw, Emerson P.        | DATE PERFORMED:        |          |
|                                  | 09-12-24               |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 09-12-24               |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Managing Services in Linux

# Requirement: 

-   A virtual machine running Linux

![](vertopal_418037ccb2504c81b17cb64bdcef7907/media/image2.png){width="4.135416666666667in"
height="1.8020833333333333in"}

Complete this lab as follows:

1.  Use the service --status-all command to list all active and inactive
    services.

List down active and inactive services in the table below. Provide five
(5) services for each column.

  -----------------------------------------------------------------------
  **Active**                             **Inactive**
  -------------------------------------- --------------------------------
  alsa-utils                             bluetooth

  apparmor                               grub-common

  cron                                   console-setup.sh

  cups                                   plymouth

  dbus                                   Keyboard-setup.sh
  -----------------------------------------------------------------------

**SS:**

![](vertopal_418037ccb2504c81b17cb64bdcef7907/media/image3.png){width="5.827585301837271in"
height="2.499673009623797in"}

2.  Start the Bluetooth service using the systemctl command.

Ex. sudo systemctl start httpd

![](vertopal_418037ccb2504c81b17cb64bdcef7907/media/image4.png){width="4.359946412948381in"
height="1.1875in"}

**SS:**

![](vertopal_418037ccb2504c81b17cb64bdcef7907/media/image5.png){width="7.027083333333334in"
height="0.26944444444444443in"}

3.  Check the status of the Bluetooth service. What is its status?

**SS:**

![](vertopal_418037ccb2504c81b17cb64bdcef7907/media/image6.png){width="7.027083333333334in"
height="0.9076388888888889in"}

4.  Check the status of the cups services. Since when was it running?

**SS:**

![](vertopal_418037ccb2504c81b17cb64bdcef7907/media/image7.png){width="7.027083333333334in"
height="3.8444444444444446in"}

5.  Stop cups services.

**SS:**
![](vertopal_418037ccb2504c81b17cb64bdcef7907/media/image8.png){width="7.027083333333334in"
height="0.78125in"}

![](vertopal_418037ccb2504c81b17cb64bdcef7907/media/image9.png){width="7.027083333333334in"
height="1.3854166666666667in"}

6.  Verify if the service was stopped.

**SS:**

![](vertopal_418037ccb2504c81b17cb64bdcef7907/media/image10.png){width="7.027083333333334in"
height="1.273611111111111in"}

7.  Restart the cups services

**SS:**

![](vertopal_418037ccb2504c81b17cb64bdcef7907/media/image11.png){width="7.027083333333334in"
height="0.21736111111111112in"}

8.  Verify if the service was restarted.

**SS:**

![](vertopal_418037ccb2504c81b17cb64bdcef7907/media/image12.png){width="6.462411417322834in"
height="2.3681474190726157in"}
