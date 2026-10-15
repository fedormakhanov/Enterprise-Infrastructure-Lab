# Active Directory Domain Services Installation

## Objective
Install AD DS and promote SRV-DC01 to a domain controller for corp.local.

## Steps

1. Open Server Manager → Add Roles and Features
2. Select "Active Directory Domain Services"
3. Complete installation
4. Click "Promote this server to a domain controller"
5. Create a new forest:
   - Domain: corp.local
6. Restart after promotion

## Result
SRV-DC01 is now the primary domain controller for corp.local.

- Server renamed to SRV-DC01
- Static IP: 192.168.10.10
- DNS: 192.168.10.10
- Domain: corp.local
- Role installed: AD DS
- Promoted to Domain Controller
