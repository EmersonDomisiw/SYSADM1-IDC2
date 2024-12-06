+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 075bae183d274caabad3dfe242229eb8 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: Domisiw, Emerson P.        | DATE PERFORMED:        | /50      |
|                                  | 09-26-24               |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 09-26-24               |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Monitoring Print Services in Windows Server 2019

# Requirement: 

-   A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1.  Install and configure **print.srv** domain

  --------------------------------------------------------------------------------------------
  ![](vertopal_075bae183d274caabad3dfe242229eb8/media/image2.png){width="4.11515748031496in"
  height="2.542020997375328in"}
  --------------------------------------------------------------------------------------------

  --------------------------------------------------------------------------------------------

2.  Connect one client to the recently created domain

+-----------------------------------------------------------------------+
| ![](vertopal_075bae183                                                |
| d274caabad3dfe242229eb8/media/image3.png){width="2.614948600174978in" |
| height="1.5731364829396326in"}                                        |
|                                                                       |
| ![](vertopal_075bae183                                                |
| d274caabad3dfe242229eb8/media/image4.png){width="4.322521872265967in" |
| height="1.8563713910761155in"}                                        |
|                                                                       |
| ![](vertopal_075bae183d                                               |
| 274caabad3dfe242229eb8/media/image5.png){width="4.2816316710411195in" |
| height="2.270003280839895in"}                                         |
|                                                                       |
| ![](vertopal_075bae183                                                |
| d274caabad3dfe242229eb8/media/image6.png){width="4.289636920384952in" |
| height="1.9912849956255467in"}                                        |
+=======================================================================+
+-----------------------------------------------------------------------+

3.  Install Print Services Role:

  ---------------------------------------------------------------------------------------------
  ![](vertopal_075bae183d274caabad3dfe242229eb8/media/image7.png){width="4.781917104111986in"
  height="1.791917104111986in"}
  ---------------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------------------

4.  Search the internet for any printer installer and convert it to iso

+-----------------------------------------------------------------------+
| ![](vertopal_075bae18                                                 |
| 3d274caabad3dfe242229eb8/media/image8.png){width="4.69621062992126in" |
| height="2.361796806649169in"}                                         |
|                                                                       |
| ![](vertopal_075bae183                                                |
| d274caabad3dfe242229eb8/media/image9.png){width="6.261290463692038in" |
| height="0.39588910761154855in"}                                       |
+=======================================================================+
+-----------------------------------------------------------------------+

5.  Install and deploy it as network printer

  -----------------------------------------------------------------------------------------------
  ![](vertopal_075bae183d274caabad3dfe242229eb8/media/image10.png){width="1.8208530183727034in"
  height="2.0788035870516186in"}
  -----------------------------------------------------------------------------------------------

  -----------------------------------------------------------------------------------------------

Part 2: Monitoring Print Services

Objective: Familiarize yourself with monitoring tools available in
Windows Server 2019.

1.  Event Viewer:

    -   Open Event Viewer (run eventvwr.msc).

    -   Navigate to Applications and Services Logs \> Microsoft \>
        Windows \> PrintService.

    -   Review logs for print jobs, errors, and warnings.

  ----------------------------------------------------------------------------------------------
  ![](vertopal_075bae183d274caabad3dfe242229eb8/media/image11.png){width="5.933818897637796in"
  height="2.253548775153106in"}
  ----------------------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------------------

2.  Performance Monitor:

    -   Open Performance Monitor (run perfmon).

    -   In the left pane, expand Data Collector Sets \> System.

    -   Right-click System Performance and select Start.

    -   Monitor performance metrics related to print services.

  ----------------------------------------------------------------------------------------------
  ![](vertopal_075bae183d274caabad3dfe242229eb8/media/image12.png){width="5.905240594925634in"
  height="2.0331911636045494in"}
  ----------------------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------------------

3.  Using Print Management Console:

    -   Open Print Management from Server Manager.

    -   View active print jobs and their status.

    -   Use the Printers node to check the status of all printers.

  ----------------------------------------------------------------------------------------------
  ![](vertopal_075bae183d274caabad3dfe242229eb8/media/image13.png){width="5.950287620297463in"
  height="1.6206135170603675in"}
  ----------------------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------------------

Part 3: Exploring Third-Party Monitoring Tools

1.  Research at least two third-party print monitoring tools

    -   Consider factors such as features, pricing, and compatibility
        with Windows Server 2019.

  ----------------------------------------------------------------------------------------------
  ![](vertopal_075bae183d274caabad3dfe242229eb8/media/image14.png){width="6.250872703412074in"
  height="0.3125437445319335in"}
  ----------------------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------------------

2.  Install and Configure:

    -   Choose one of the tools to install in your environment.

    -   Follow the installation instructions provided by the tool\'s
        documentation.

    -   Configure it to monitor your print services.

3.  Test and Report Findings:

    -   Generate a report or dashboard from the tool.

    -   Analyze the collected data (e.g., print volume, errors, user
        activity).

Rubric

  --------------------------------------------------------------------------------------------------------------
  **Criteria**   **1                  **2 (Needs       **3                **4        **5             **Score**
                 (Unsatisfactory)**   Improvement)**   (Satisfactory)**   (Good)**   (Excellent)**   
  -------------- -------------------- ---------------- ------------------ ---------- --------------- -----------

  --------------------------------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 1: Setting Up Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Domain         No domain Domain     Domain      Domain       Domain           
  Installation**   created   created    created     configured   configured and   
                             with       correctly   well         documented       
                             errors                              thoroughly       
  ---------------- --------- ---------- ----------- ------------ ---------------- --

  ----------------------------------------------------------------------------------

  --------------------------------------------------------------------------------
  **Client       Client not  Connection   Client      Client      Client        
  Connection**   connected   attempt      connected   connected   connected and 
                             failed       but with    correctly   documented    
                                          issues                  well          
  -------------- ----------- ------------ ----------- ----------- ------------- --

  --------------------------------------------------------------------------------

  ------------------------------------------------------------------------------------
  **Print Services Role not    Role        Role        Role         Role installed, 
  Role             installed   installed   installed   installed    configured, and 
  Installation**               with issues correctly   and          documented      
                                                       configured   thoroughly      
  ---------------- ----------- ----------- ----------- ------------ --------------- --

  ------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Printer      No          Installer    Installer   Installer   Installer      
  Installer      installer   conversion   converted   converted   converted,     
  Conversion**   found       attempted    but not     and used    used, and      
                             but failed   used                    documented     
                                                                  well           
  -------------- ----------- ------------ ----------- ----------- -------------- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Network      Printer    Deployment   Printer      Printer     Printer        
  Printer        not        failed       deployed but deployed    deployed,      
  Deployment**   deployed                not          correctly   tested, and    
                                         functional               documented     
                                                                  well           
  -------------- ---------- ------------ ------------ ----------- -------------- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 2: Monitoring Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ------------------------------------------------------------------------------
  **Event   Event     Opened but  Logs reviewed Logs        Logs reviewed     
  Viewer    Viewer    no logs     but           reviewed    with thorough     
  Usage**   not       reviewed    superficial   with some   analysis and      
            opened                              analysis    documentation     
  --------- --------- ----------- ------------- ----------- ----------------- --

  ------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Performance   Performance   Opened but  Metrics     Metrics     Metrics       
  Monitor Usage** Monitor not   no metrics  monitored   monitored   monitored,    
                  opened        monitored   but not     with some   analyzed, and 
                                            analyzed    analysis    documented    
                                                                    thoroughly    
  --------------- ------------- ----------- ----------- ----------- ------------- --

  ----------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Print       Console   Opened but      Active jobs     Active    Active jobs   
  Management    not       functionality   viewed          jobs      viewed and    
  Console       opened    not used        superficially   viewed    documented    
  Usage**                                                 with some thoroughly    
                                                          detail                  
  ------------- --------- --------------- --------------- --------- ------------- --

  ----------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 3: Exploring Third-Party Tools**                                        
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Research   No tools     Research     Research on Research on  Research on    
  on Tools**   researched   incomplete   one tool    two tools    two tools,     
                                         completed   with some    detailed       
                                                     analysis     analysis, and  
                                                                  comparison     
  ------------ ------------ ------------ ----------- ------------ -------------- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------------
  **Installation    Tool not    Installation   Tool         Tool         Tool           
  and               installed   failed         installed    installed    installed,     
  Configuration**                              but not      and          configured,    
                                               configured   configured   and documented 
                                                            with issues  thoroughly     
  ----------------- ----------- -------------- ------------ ------------ -------------- --

  ----------------------------------------------------------------------------------------

  -------------------------------------------------------------------------------
  **Reporting   No report   Report   Report      Report      Comprehensive     
  Findings**    generated   lacks    generated   generated   report with       
                            detail   but lacks   with some   thorough analysis 
                                     analysis    analysis    and documentation 
  ------------- ----------- -------- ----------- ----------- ----------------- --

  -------------------------------------------------------------------------------

![](vertopal_075bae183d274caabad3dfe242229eb8/media/image15.png){width="4.875680227471566in"
height="3.27128937007874in"}

![](vertopal_075bae183d274caabad3dfe242229eb8/media/image16.png){width="4.8027537182852145in"
height="2.3024048556430445in"}
