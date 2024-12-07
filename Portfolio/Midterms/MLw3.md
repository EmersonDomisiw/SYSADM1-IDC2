![image](https://github.com/user-attachments/assets/92917fe9-cc96-436c-9b6b-fe8a81fc6cd6)


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

![image](https://github.com/user-attachments/assets/3e185ee5-542a-4bf7-b5e1-890898530fd4)


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

![image](https://github.com/user-attachments/assets/d0482837-7f01-4c0b-af61-7de6a7aad8c8)

![image](https://github.com/user-attachments/assets/02253590-1ba2-43e2-9202-170cd9ef3f1b)


![image](https://github.com/user-attachments/assets/81b3a281-54b8-4b9a-94b2-e0b3ead87cc9)

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

![image](https://github.com/user-attachments/assets/935244d1-f4e6-4d16-b066-2a909370f973)


**Part 4: Reflection Questions**

1.  What are the most common causes of a **503 Service Unavailable**
    error?

![image](https://github.com/user-attachments/assets/a6cf04a0-ebe0-44ff-b67e-0bb20e06a7cf)


2.  How would you **monitor login attempts** to detect potential
    security threats?

![image](https://github.com/user-attachments/assets/578f6bb3-c591-4be6-ba13-68bff5a91ec0)


3.  Why is **monitoring logs** in Event Viewer important for
    administrators?

![image](https://github.com/user-attachments/assets/1c15229b-6b98-4b0b-a2b1-50479866ac13)
![image](https://github.com/user-attachments/assets/4aa8f810-ff79-4684-804d-8b8ca14aa82f)



Grading Rubric

 ![image](https://github.com/user-attachments/assets/90f596a2-c8c0-4168-9313-bc5e3aa2cdf9)

