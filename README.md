# Zabbix-templates-for-Active-Directory
This repository contains zabbix templates for Active Directory(AD) and PowerShell(PS) script for AD replication monitoring
# Requirements
PowerShell 3.00+ version
# Installation
Add userparameter in your zabbix_agentd.conf by analogy with userparameter.conf
Import the template ADReplication.xml and the template ADAudit.xml in your zabbix installation
# Description
1). LLD finds a active directory replication partners
2). Zabbix server obtains replication metrics:
  - Failure count
  - Failure type
  - First failure time
  - Last replication error
  - some metadata metrics
3). Each trigger of last error contains the url to support.microsoft.com page of the troubleshooting for error by she's id.
