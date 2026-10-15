# Enterprise Infrastructure Lab (Windows Server 2022 + Active Directory)

This project demonstrates a full enterprise-grade Windows Server 2022 domain deployment.
It includes Active Directory Domain Services, DNS, OU architecture, Group Policy Objects,
security baselines, and workstation management — replicating a real corporate environment
for IT Support / Junior SysAdmin roles.

## Domain Architecture

- Domain: corp.local
- Domain Controller: SRV-DC01
- IP: 192.168.10.10
- DNS: 192.168.10.10

## OU Structure
```
corp.local
└── Corp
    ├── Corp Users
    ├── Corp Computers
    ├── Admins
    ├── Servers
    └── Service Accounts
```

## GPO Overview

### Password Policy
- Length 12, complexity enabled, lockout threshold 5

### Desktop Policy
- Control Panel disabled, wallpaper enforced

### Security Baseline
- Firewall enabled, SMB hardened, cipher suite order enforced

## Purpose

This lab simulates a real corporate Windows environment and demonstrates skills in:

- Windows Server administration
- Active Directory
- DNS
- Group Policy
- Security hardening
- Enterprise documentation

## Author

**Fedor Makhanov** — Aspiring IT Support / Junior SysAdmin
