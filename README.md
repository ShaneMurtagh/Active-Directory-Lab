# Active Directory Lab (Azure)

Built a Windows Server domain controller from scratch on Azure — installed AD DS, 
created an OU structure, added users/groups, and tested login from a client VM.

## What I did
- Deployed a Windows Server VM on Azure
- Installed Active Directory Domain Services and promoted it to a domain controller
- Created OUs, users, and security groups
- Joined a client VM to the domain and tested authentication
- Ran common AD tasks through both GUI (Server Manager, ADUC) and PowerShell

## Tools used
Azure, Windows Server, Active Directory Domain Services, DNS, PowerShell

## Screenshots
(add a few images from `/screenshots` here, e.g. AD Users and Computers, 
a successful domain login, the DCPROMO wizard)

## A problem I hit
(one short paragraph — e.g. "client couldn't join the domain because DNS was pointing 
to Azure's default resolver instead of the DC — fixed by updating the VM's DNS setting")

## Scripts
See `/scripts` for the PowerShell used to create users and groups.
