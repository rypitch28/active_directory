#Active Directory Setup

-Installed Windows Server 2022 as a virtual machine (VMware Workstation)
-Installed Windows 11 as a Virtual Machine Client


*Installing the Domain Controller
1. use `sconfig` to:
	-Change Hostname
	-Change IP to Static
	-Change DNS to own IP Address

2. Install Active directory windows feature

```````shell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools

Import-Module ADDSDeployment
Install-ADDSForest
```````
-Setting up PSSession From Client Manager to Server
1. Start WinRM
2. Set TrustedHosts
3. Create New PSSession
4. Enter Session
```````shell
Start-Servie WinRm

Set-Item wsman:\localhost\Client\TrustedHosts -value 192.168.135.138

New-PSSession -ComputerName 192.168.135.138 -Credential (Get-Credential)

Enter-PSSession 1  

```````


