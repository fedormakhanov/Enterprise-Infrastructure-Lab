# Enterprise Infrastructure Architecture

This document describes the architecture of the Windows Server 2022 domain environment
implemented in the Enterprise Infrastructure Lab.

## Domain Overview

- Domain: corp.local
- Domain Controller: SRV-DC01
- IP Address: 192.168.10.10
- DNS Server: 192.168.10.10
- Gateway: 192.168.10.1
- OS: Windows Server 2022 Standard

## Core Services

- Active Directory Domain Services (AD DS)
- DNS Server
- Group Policy Management
- Windows Firewall
- Security Baseline (SMB hardening, cipher suite enforcement)

## Logical Architecture
```
corp.local  
└── Corp  
    ├── Corp Users  
    ├── Corp Computers  
    ├── Admins  
    ├── Servers  
    └── Service Accounts
```

## Purpose

This architecture simulates a real corporate Windows domain environment suitable for
IT Support and Junior SysAdmin training, documentation, and portfolio demonstration.

