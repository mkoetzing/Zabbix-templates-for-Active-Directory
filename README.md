# Zabbix-templates-for-Active-Directory
This repository contains zabbix templates for Active Directory(AD) and PowerShell(PS) script for AD replication monitoring
# Requirements
PowerShell 3.00+ version
# Installation
1. Add userparameter in your zabbix_agentd.conf by analogy with userparameter.conf
2. Create dir "C:\Program Files\Zabbix Agent\scripts" and Copy ADReplication.ps1
3. Import the template ADReplication.xml and the template ADAudit.xml in your zabbix installation
 
# Description
1). LLD finds a active directory replication partners

2). Zabbix server obtains replication metrics:
  - Failure count
  - Failure type
  - First failure time
  - Last replication error
  - some metadata metrics

3). Each trigger of last error contains the url to support.microsoft.com page of the troubleshooting for error by her id.
![problem](https://user-images.githubusercontent.com/39965096/51258163-62942c00-19ba-11e9-88ac-33c31647c8be.PNG)
![last data](https://user-images.githubusercontent.com/39965096/51258208-7c357380-19ba-11e9-8627-3d819134a1a3.PNG)
4) Audit template triggers (the name of the triggers in Russian language):
User profile has been blocked

  - Delete secure local group
  - User name has been modify
  - Modify secure local group
  - Log in successfully
  - Modify user profile
  - Delete member local secure group
  - Add member local secure group
  - User profile has been created
  - Log in denied
  - Attempt to reset the account password
  - User profile disabled
  - Secure local group has been created
  - User profile deleted
  - Clear audit journal

![audit](https://user-images.githubusercontent.com/39965096/51258362-d9c9c000-19ba-11e9-932e-fc90228cd6a2.PNG)


# Troubleshoot

If you have error "Timeout while executing a shell script"
please edit in your zabbix_agentd.conf parameter Timeout=30, default 10 sec.

Tested on windows servers 2008r2 2012r2 2016
