# Enterprise Infrastructure Lab (Windows Server 2022 + Active Directory)

This project demonstrates a full enterprise-grade Windows Server 2022 domain deployment.  
It includes Active Directory Domain Services, DNS, OU architecture, Group Policy Objects,  
security baselines, and workstation management — replicating a real corporate environment  
for IT Support / Junior SysAdmin roles.

---

## Domain Architecture

- Domain Controller: **SRV-DC01**
- Domain: **corp.local**
- IP: **192.168.10.10**
- DNS: **192.168.10.10**
- Gateway: **192.168.10.1**
- OS: Windows Server 2022

---

## Organizational Unit Structure

"""corp.local
└── Corp
    ├── Corp Users
    ├── Corp Computers
    ├── Admins
    ├── Servers
    └── Service Accounts"""

---

## Users & Groups

### Standard User
- **user1**
- OU: Corp Users

### Administrator
- **admin1**
- OU: Admins
- Group: Domain Admins

---

## Group Policy Objects

### 1. Password Policy (Domain Level)
- Minimum length: 12
- Complexity: Enabled
- Max age: 90 days
- Lockout threshold: 5 attempts

### 2. Desktop Policy (Corp Users)
- Control Panel: Disabled
- Wallpaper: Enforced

### 3. Security Baseline (Corp Computers)
- Windows Firewall: Enabled
- SMBv1: Disabled (Server 2022 default)
- SMB Compression: Disabled
- Cipher Suite Order: Enforced

---

## Client Configuration

- Domain join
- GPO application verification
- Security baseline enforcement

---

## Purpose of the Project

This lab simulates a real corporate Windows environment and demonstrates skills in:

- Windows Server administration  
- Active Directory  
- DNS  
- Group Policy  
- Security hardening  
- Enterprise documentation  

Suitable for IT Support, Junior SysAdmin, and Infrastructure roles.

---

## Author

**Fedor Makhanov** — Aspiring IT Support / Junior SysAdmin  
Building enterprise-grade infrastructure labs and preparing for corporate IT roles.
