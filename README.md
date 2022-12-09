# TMS-Migration-Tool

Tool to migrate all TMS and external server booked meetings to hybrid calendar services.

**TMT Configuration Document**

**What is the purpose of the TMT Application?**

As TMS (Telepresence Management Suite) is phasing out, all meeting scheduled via TMS, or external servers must be moved to hybrid calendar services.
TMT is the application which is built to carry out this task.

**Pre-requisites:**

o  Key Value Pairs 

o	Configuration Steps

o	Known issues

o	Getting help

o	Credits

o	Demo

**Pre-requisites:**

1.	TMT application (TMT.exe)
2.	TMS server username and password.
3.	Name of the server where Microsoft Exchange is installed (either online or on premise or both, whichever is applicable).
4.	On Premise / Online Username (or both Usernames)
5.	On Premise / Online Password (or both Passwords)
6.	MonitoredMailboxCalendarProperties.csv file to be copied in the folder of TMT application from the customers deployment.
7.	Date (dd-mm-yyyy hh:mm:ss) from when you want the tool to move future meetings.

Note: The TMT application needs to be saved and run on the same machine where TMS is installed.

**Key Value Pairs:**

**TMSServerUsername**
- Username of the server where TMS is installed.

**TMSServerPassword**
- Password of the server where TMS is installed.

**IsExchangeHybrid**
- a boolean flag
- set to true, if customer is using both Exchanges, on premise and online.
- set to false, if only one Exchange is used.

If IsExchangeHybrid= “false”, fill one of the below Exchange information that is applicable (OnPremise or Online)
Else fill both.

**ExchangeOnPremise**
- name of the server where Microsoft Exchange is installed (empty, if not applicable)

**OnPremiseUserName**
- Username to access the Outlook mailbox (empty, if not applicable)

**OnPremisePassword**
- Password to access the Outlook mailbox (empty, if not applicable)

**ExchangeOnline**
- Outlook office 365 (empty, if not applicable)

**OnlineUserName**
- Username to access the Outlook mailbox (empty, if not applicable)

**OnlinePassword**
- Password to access the Outlook mailbox (empty, if not applicable)

**IsPilotRun**
- A boolean flag to determine if it is a trial run or a full run. Set to true for trial run, else false (or empty).

**PilotUsers**
- Incase the above flag is set to true, provide usernames separated by semicolon in this parameter.

**StartDate**
- Date value that would determine the conferences to be considered for updating from this input date
- Date should be in the format of "dd-mm-yyyy hh:mm:ss"

**Configuration steps:**

![Image](https://user-images.githubusercontent.com/119580730/206635046-4a47fc51-534c-4ae0-a066-a4a0c7a2b8f4.png)

1.	In TMT tool, redirect yourself to TMT.exe config file and fill in these Key Value pairs wherever applicable.
            
Note: 
The TMT application needs to be saved and run on the same machine where TMS is installed.
MonitoredMailboxCalendarProperties.csv file should be copied in the folder of TMT application from the customers deployment.

2. Save and run the TMT application.
3. Please refer log file generated to determine which meetings were successfully migrated and those which couldn't.

**Known issues**
•	This tool is not tested against Online-Exchange or O365.

**Credits:**
1.	Vinay Naik
2.	Shruthi PV
3.	Prasad Pavuluri


