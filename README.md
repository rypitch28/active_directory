#Active Directory Setup

*Installed Windows Server 2022 as a virtual machine (VMware Workstation)
*Installed Windows 11 as a Virtual Machine Client


*Installing the Domain Controller
1. use `sconfig` to:
	-Change Hostname
	-Change IP to Static
	-Change DNS to own IP Address

2. Install Active directory windows feature

```````shell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```````

