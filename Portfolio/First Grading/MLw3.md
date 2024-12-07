+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| ac9354636ccb4c399b6a4b1e4275bdfb |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: Domisiw, Emerson P.        | DATE PERFORMED:        | /50      |
|                                  | 10-17-24               |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 10-17-24               |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Platform Services

# Requirement: 

-   A virtual machine running Windows Server

    **Objective/s:**

    To analyze IIS logs in the Event Viewer to identify critical web
    service metrics, understand common error codes, and learn how to
    monitor the health of web applications.

**Instructions**

**Part 1: Opening Event Viewer and Loading Logs**

1.  Access the event viewer in the server.

2.  From the event viewer, explore the windows log and list down its
    major categories

+-----------------------------------------------------------------------+
| **Application**                                                       |
|                                                                       |
| **Security**                                                          |
|                                                                       |
| **Setup**                                                             |
|                                                                       |
| **System**                                                            |
|                                                                       |
| **Forwarded Events**                                                  |
+=======================================================================+
+-----------------------------------------------------------------------+

**Part 2: Filtering and Analyzing IIS Events**

1.  Apply filter to the windows log categories to display errors for the
    past 12 hours.

2.  **Identify Critical Events** or recurring events.

3.  **Analyze the Events**:

    -   For each critical or recurring event, **record the following
        details**:

        -   **Event ID**

        -   **Source**

        -   **Timestamp**

        -   **Description**

+--------------+-------------------------------------------------------+
| **Events**   | **Screenshots**                                       |
+==============+=======================================================+
| Application  | ![](vertopal_ac9354636ccb4c399b6a4b1e4                |
|              | 275bdfb/media/image2.png){width="4.481359361329834in" |
|              | height="3.354491469816273in"}                         |
|              |                                                       |
|              | **Description:** License Activation(slui.exe) failed  |
|              |                                                       |
|              | **Description:** Acquisition of End User License      |
|              | failed.                                               |
|              |                                                       |
|              | **Description:** License acquisition failure          |
+--------------+-------------------------------------------------------+
| Security     | ![](vertopal_ac9354636ccb4c399b6a4b1e4                |
|              | 275bdfb/media/image3.png){width="4.405187007874016in" |
|              | height="2.10657261592301in"}                          |
+--------------+-------------------------------------------------------+
| Setup        | ![](vertopal_ac9354636ccb4c399b6a4b1e4                |
|              | 275bdfb/media/image4.png){width="4.716973972003499in" |
|              | height="1.650100612423447in"}                         |
+--------------+-------------------------------------------------------+
| System       | ![](vertopal_ac9354636ccb4c399b6a4b1e4                |
|              | 275bdfb/media/image5.png){width="4.787461723534558in" |
|              | height="2.5726990376202976in"}                        |
|              |                                                       |
|              | **Description:** 4199-The system detected an address  |
|              | conflict for IP address 10.20.30.40.                  |
|              |                                                       |
|              | **Description:** 7030-The Printer Extensions and      |
|              | Notifications is marked as an interactive service.    |
|              |                                                       |
|              | **Description:** 46- The time service encountered an  |
|              | error and was forced to shut down.                    |
+--------------+-------------------------------------------------------+
| Forwarded    | ![](vertopal_ac9354636ccb4c399b6a4b1e4                |
| Events       | 275bdfb/media/image6.png){width="5.085450568678915in" |
|              | height="2.5670341207349083in"}                        |
+--------------+-------------------------------------------------------+

**Part 3: Troubleshooting and Solution Development**

1.  Review the logs and check for recurring errors.

2.  Is there a specific time or pattern to these errors?

3.  Draft a Troubleshooting Report:

    -   Based on the events found, create a short report with the
        following sections:

**Report Structure**

**1.** Overview

-   A brief summary of the issue and scope of your analysis.

  -----------------------------------------------------------------------
  Based on the issue that I encountered in the troubleshooting, it
  indicates failures in the application installations and configurations
  that's why it causes some issues while I am doing the troubleshooting
  process.
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

**2.** Key Findings

-   List the critical events you found. Example:

    -   **Event ID 503**: Application pool stopped at 10:05 AM.

    -   **Event ID 404**: Page not found error at 11:15 AM.

**3.** Root Causes and Solutions

-   Describe the likely cause of each error and how you would fix it.

+-----------------------------------------------------------------------+
| -   Event ID 8198: My windows installer service failed to start which |
|     had hinder the application installations.                         |
|                                                                       |
| Solution: Restart the Windows Installer                               |
|                                                                       |
| -   Event ID 4199: Missing installation files.                        |
|                                                                       |
| Solution: Verify the integrity of the installation files and          |
| re-download if necessary                                              |
+=======================================================================+
+-----------------------------------------------------------------------+

**Part 4: Reflection Questions**

1.  What are the most common causes of a **503 Service Unavailable**
    error?

+-----------------------------------------------------------------------+
| The most common causes of 503 Service Unavailable are:                |
|                                                                       |
| -Maintenance or downtime of the server                                |
|                                                                       |
| -Resource limitations(CPU memory)                                     |
|                                                                       |
| -High traffic in the server                                           |
+=======================================================================+
+-----------------------------------------------------------------------+

2.  How would you **monitor login attempts** to detect potential
    security threats?

+-----------------------------------------------------------------------+
| -Setting up an alerts for multiple failed logins                      |
|                                                                       |
| -Enabling auditing for login events in Windows server                 |
|                                                                       |
| -Review the security logins to monitor in the Event Viewer to see the |
| failed attempts that is created                                       |
+=======================================================================+
+-----------------------------------------------------------------------+

3.  Why is **monitoring logs** in Event Viewer important for
    administrators?

+-----------------------------------------------------------------------+
| -For the reason that it identifies errors and application issues.     |
|                                                                       |
| -It tracks security events and potential breaches that is happening.  |
|                                                                       |
| -It helps the network engineers to be updated about errors,           |
| unauthorized activities and system failures so that it will be safe   |
| and secured when using any applications and avoid threats and         |
| vulnerabilities from happening.                                       |
+=======================================================================+
+-----------------------------------------------------------------------+

Grading Rubric

  ---------------------------------------------------------------------------------------------------------------------------------------
  **Criteria**        **Excellent**     **Good**          **Needs                           **Poor**                         **Points**
                                                          Improvement**                                                      
  ------------------- ----------------- ----------------- --------------- ----------------- ------------- ------------------ ------------
  **Log Analysis**    Identifies all    Identifies most   Identifies some                   Fails to                         /10
                      key events (503,  key events with   events, but                       identify key                     
                      404, 500, etc.)   minor errors in   with incomplete                   events or                        
                      with accurate     details.          or incorrect                      provides                         
                      event details.                      details.                          incorrect                        
                                                                                            details.                         

  **Troubleshooting   Proposes logical, Solutions are     Solutions are                     Solutions are                    /10
  Solutions**         effective         mostly correct    somewhat vague                    unclear or                       
                      solutions to all  but miss some key or incomplete.                    incorrect.                       
                      identified        points.                                                                              
                      issues.                                                                                                

  **Report Structure  Well-organized    Report is mostly  Report is                         Report is                        /10
  & Clarity**         report with all   organized with    disorganized or                   unclear or                       
                      sections clearly  minor formatting  missing                           incomplete.                      
                      completed.        issues.           sections.                                                          

  **Recommendations   Provides          Recommendations                   Recommendations                 Fails to provide   /10
  for Monitoring**    thoughtful,       are relevant but                  are vague or                    relevant           
                      proactive         lack depth.                       incomplete.                     recommendations.   
                      recommendations                                                                                        
                      to prevent future                                                                                      
                      issues.                                                                                                

  **Participation &   Actively engaged  Participated but                  Minimal                         Did not            /10
  Effort**            in the activity,  required some                     participation,                  participate        
                      followed          guidance.                         needed                          meaningfully.      
                      instructions                                        significant help.                                  
                      thoroughly.                                                                                            

  **Score**                                                                                                                  **/50**
  ---------------------------------------------------------------------------------------------------------------------------------------
