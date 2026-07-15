# Active Directory Lab (Azure)

A hands-on lab where I built Active Directory from scratch using real infrastructure — 
not a tutorial sandbox. I deployed a Windows Server VM in Azure, promoted it to a 
domain controller, built a basic AD structure, created users and groups, and tested 
authentication from a domain-joined client — using both the GUI and PowerShell.

## Why I built this

I'm working toward an entry-level IT support role and wanted practical, hands-on 
experience with the tools most helpdesk and support teams use daily — Active Directory, 
DNS, user/group management, and basic troubleshooting — rather than just studying 
theory.

## What I did

1. **Deployed a Windows Server VM in Azure** — set up a virtual network, network 
   interface, and public IP for the domain controller.
2. **Installed Active Directory Domain Services (AD DS)** and promoted the server to 
   a domain controller, creating a new forest and domain. This also installed DNS, 
   since AD depends on it to locate domain controllers and services.
3. **Designed a simple OU structure** to logically organize users, groups, and future 
   Group Policy targets (e.g. separating staff, IT, and service accounts).
4. **Created users and security groups**, and assigned users to groups to control 
   access — testing how group membership affects permissions.
5. **Deployed a second Windows Server VM as a client**, joined it to the domain, and 
   tested logging in with a domain user account to confirm authentication worked 
   end-to-end.
6. **Performed common AD administration tasks** both through the GUI (Server Manager, 
   Active Directory Users and Computers) and PowerShell, to get comfortable with both 
   approaches.
7. **Troubleshot issues** that came up during setup (see below).
8. **Cleaned up all Azure resources** after the lab to avoid ongoing charges — 
   deallocated VMs, then deleted the resource group and confirmed all associated 
   disks, IPs, and network interfaces were removed.

## Tools & technologies used

Azure (VMs, VNet, resource groups), Windows Server, Active Directory Domain Services 
(AD DS), DNS, Active Directory Users and Computers (ADUC), PowerShell

## Screenshots


- Azure resource group with VMs deployed
- AD DS installation / DCPROMO wizard
- Active Directory Users and Computers showing OU structure
- Users and groups created
- Successful domain login from the client VM
- A PowerShell command being used for an AD task (e.g. `Get-ADUser` or `New-ADUser`)




## Scripts

PowerShell scripts used during the lab are in the [`/scripts`](./scripts) folder, 
covering tasks like creating users, creating groups, and adding users to groups.

## What I'd do next

- Add Group Policy Objects (GPOs) to enforce settings like password policy or 
  restrict access to Control Panel
- Automate the OU/user/group creation with a single PowerShell script instead of 
  doing it manually
- Add a basic file share with NTFS permissions tied to security groups

## Cost & cleanup

This lab used Azure VMs, which incur cost while running. All resources (VMs, disks, 
public IPs, network interfaces, and the resource group itself) were deleted after 
completing the lab to avoid ongoing charges.
