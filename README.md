# Sysmon
Installing &amp; Setting up Sysmon in windows Machine.

# What is a Sysmon
System Monitor (Sysmon) is a Windows system service and device driver that, once installed on a
system, remains resident across system reboots to monitor and log system activity to the Windows
event log.


# Prerequisites
Windows Host machine with admin rights
7 zip or winrar

# How to install Sysmon

- Click on the link attached below and scroll down.   ( https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)

- This will go directly to your download folder. Since its zipped, we will need to unzip it using the 7 zip app.

- After Unzipping, Open PowerShell in admin mode and navigate to the folder where you stored the unzipped files of sysmon.

- Now that you are in the Symon directory, you will be able to install the app, to do this, run the
following command:

<img width="484" alt="image" src="https://github.com/user-attachments/assets/2f0e7a14-6de1-4eda-906b-63f77267b8eb">

- Once this command has finished executing, Sysmon is now installed and you should be able to see the service running if you open the Services application.

- Sysmon being installed as is, doesn’t really do much. To truly leverage this tool, we are going to need to use a config file. There are many config files for Sysmon available online, but for this tutorial I am going to use SwiftOnSecurity’s config file from GitHub (GitHub - SwiftOnSecurity/sysmon-config: Sysmon configuration file template with default high-quality event tracing) as it is recommended by multiple
cyber security companies. Head to that link and download the files as a zip file.

- Click on the github link and download the files. ( https://github.com/SwiftOnSecurity/sysmon-config )

- Once the download has finished, extract the zip file.THe folder will be named Sysmon-config-master. Open that folder and moved the file named “sysmonconfig-export.xml” to the Sysmon file folder.

- We should have the following files in the Sysmon folder:

- <img width="462" alt="image" src="https://github.com/user-attachments/assets/50fd8524-0ac2-4d8f-8ff8-1d95f313c031">

- Now, head back to your PowerShell terminal and enter the following command:

- <img width="458" alt="image" src="https://github.com/user-attachments/assets/fe33a5af-891b-49bc-9850-6495f6d9795e">

- The final step is to ensure that the config file has been applied. We are going to run the following command:

- <img width="458" alt="image" src="https://github.com/user-attachments/assets/cc9a04f4-26d5-4664-91d9-e0ac60f7023f">


Assuming the output of this command was a huge list of query names and target objects, the configuration has been applied and the setup is complete. Sysmon can now be used for System
Information and Events management including with the use of a SIEM tool.


