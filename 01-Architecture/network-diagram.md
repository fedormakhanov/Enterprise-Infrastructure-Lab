# Network Diagram
```
                         ┌──────────────────────────┐
                         │        Internet          │
                         └─────────────┬────────────┘
                                       │
                                       │
                         ┌─────────────▼────────────┐
                         │     Router / Gateway     │
                         │       192.168.10.1       │
                         └─────────────┬────────────┘
                                       │
                                       │ LAN 192.168.10.0/24
                                       │
                         ┌─────────────▼────────────┐
                         │          Switch          │
                         └─────────────┬────────────┘
                                       │
             ┌─────────────────────────┼─────────────────────────┐
             │                         │                         │
┌────────────▼────────────┐  ┌────────▼─────────────┐   ┌─────────▼────────────┐
│       SRV-DC01          │  │      CLIENT-01       │   │      CLIENT-02       │
│  Windows Server 2022    │  │  Windows 10/11       │   │  Windows 10/11       │
│  Domain Controller      │  │  Domain Joined       │   │  Domain Joined       │
│  corp.local             │  │  IP: 192.168.10.20   │   │  IP: 192.168.10.21   │
│  IP: 192.168.10.10      │  │  DNS: 192.168.10.10  │   │  DNS: 192.168.10.10  │
└─────────────────────────┘  └──────────────────────┘   └──────────────────────┘
```
Communication Flow:
- CLIENT → SRV-DC01: DNS, LDAP, Kerberos, GPO
- SRV-DC01 → Router: DNS Forwarders (Internet)


# Active Directory Logical Structure
```
corp.local
└── Corp
    ├── Corp Users
    ├── Corp Computers
    ├── Admins
    ├── Servers
    └── Service Accounts
```
