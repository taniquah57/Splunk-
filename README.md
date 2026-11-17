 # Splunk – Log Analysis & Security Monitoring Lab
 
Developed a foundational understanding of how security analysts use Splunk to search log data, investigate account activity, identify potentially suspicious behavior, and support security monitoring and incident investigations.

## Project Overview

This hands-on lab explored the fundamentals of Splunk, focusing on data ingestion, indexing, searching, and analyzing system logs for security monitoring and investigation.

- Explored how to add data into Splunk from different sources.
- Learned how indexes organize collected log data and how to search across all accessible indexes.
- Examined fields to identify important information within log events, such as usernames, IP addresses, timestamps, and activity types.
- Explored authentication logs to identify account login activity and investigate successful and failed login attempts.
- Reviewed system and PowerShell logs to understand how Splunk can help identify commands executed on a system.
- Practiced using Search Processing Language (SPL) to retrieve and filter log data.
- Security Event Investigation

1. Add Data
- Allows you to bring data into Splunk.
- Data can come from log files, servers, applications, network devices, and other sources.
- Splunk indexes the data so you can search and investigate it.
2. Search Index
- An index is where Splunk stores and organizes incoming data.
- Searching index=* allows you to search across all indexes you have permission to access.
- Searching a specific index limits your results to that index.
Example:
index=*


3. Fields
Think of fields like chapters or labels in a book. They help organize information so you can find specific details within a log.

Examples:
- user – Who performed an action?
- src_ip – What IP address did the activity come from?
- action – What action occurred?
- host – Which device generated the event?
4. Login Activity
To investigate who logged into an account, you can search authentication logs.

<img width="975" height="901" alt="image" src="https://github.com/user-attachments/assets/daf24cc7-c891-4697-ad61-4a08765ca9ab" />

Example:
index=* "login"


You can look for:
- Username
- Login time
- Source IP address
- Successful logins
- Failed login attempts

  <img width="975" height="532" alt="image" src="https://github.com/user-attachments/assets/91eb2af1-0766-430d-bd9a-98d0a68e133c" />

5. Commands and Code Activity
Splunk can help you investigate commands executed on a system.

For example, PowerShell logs may show what commands were executed and when.

Example:
index=* powershell


You can investigate:
- Commands executed
- User accounts associated with activity
- Timestamps
- Systems where commands were executed
Note: The exact information available depends on which logs and data sources have been configured.

<img width="975" height="540" alt="image" src="https://github.com/user-attachments/assets/1b21e091-5bce-4c93-9938-63992fd92835" />
