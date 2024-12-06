![image](https://github.com/user-attachments/assets/f566da4a-b154-4a06-a735-262bb9232939)


# SYSADM1 -- Managing Services in Windows

# Requirement: 

-   A virtual machine running Linux and Windows OS

    **Services** are background processes that run independently of user
    interactions in Windows. They provide essential system functions,
    such as network connectivity, printing, and time synchronization.
    This lab will guide you through the process of managing services
    using the Services app.

# Instructions:  {#instructions .list-paragraph}

1.  Open the Start menu and search for \"Services\"

2.  Familiarize yourself with the columns, including Service Name,
    Display Name, Status, and Startup type.

3.  Right-click on a service and select \"Start\", \"Stop\", or
    \"Restart\". Fill out the table below

> Windows:

![image](https://github.com/user-attachments/assets/d7952e2d-a98a-4e29-8032-ab11e66e1e49)

![image](https://github.com/user-attachments/assets/0c071998-6c56-4602-935d-1b37a22e41cb)



4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

![image](https://github.com/user-attachments/assets/263b8634-4884-456c-a6bf-7fd1ae495bda)


![image](https://github.com/user-attachments/assets/86689df2-97d9-4a67-9326-ff4aa660c4ad)


![image](https://github.com/user-attachments/assets/4bb0a0b5-722b-4046-8a0c-ca03093abdc5)


![image](https://github.com/user-attachments/assets/927c19e2-8187-49fa-8374-bf732f5c7e9b)


![image](https://github.com/user-attachments/assets/3fa66b68-4333-44b3-97c4-07051e962ed3)

![image](https://github.com/user-attachments/assets/d797af4d-2289-4c5a-aac3-d870dcf09f8d)


5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

![image](https://github.com/user-attachments/assets/80c066a2-fb83-45ac-9e66-2b95669b6f0e)

7.Save the batch file in Z:\lastname_timer.bat

![image](https://github.com/user-attachments/assets/91dae0ae-6f78-47ce-91ba-b8e2476680e5)


8.  Use the sc command to add timer.bat service in the command line
    interface.

> *sc create BatchTimerService binPath= \"path_to_your_batch_file.bat\"
> start= auto*
>
> *net start BatchTimerService*
>
> **Replace path_to_your_batch_file.bat with the actual path to your
> batch file.**

-   **sc create BatchTimerSservice binPath=Z:\\Domisiw_timer.bat
    start=auto**

9.  Verify that BatchTimerService has been added to the services.

![image](https://github.com/user-attachments/assets/91715098-2dc6-4d47-8ae5-84dfb937fc3e)


10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

![image](https://github.com/user-attachments/assets/14d26585-9c26-4559-a0d9-0b22f8483828)




![image](https://github.com/user-attachments/assets/0134b5b5-9bf7-4006-8509-cc355dfff1fa)
