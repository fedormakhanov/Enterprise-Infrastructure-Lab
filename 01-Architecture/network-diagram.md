# Network Diagram (ASCII)
```
Internet
   |
   |  (ISP)
   |
[Router / Gateway]
   IP: 192.168.10.1
   |
   |  LAN 192.168.10.0/24
   |
[Switch]
   |
   |-----------------------------+
   |                             |
[SRV-DC01]                       [CLIENT-01]
Domain Controller                Workstation
corp.local                       Joined to corp.local
IP: 192.168.10.10                IP: 192.168.10.20
DNS: 192.168.10.10               DNS: 192.168.10.10
```

Flow:
- CLIENT-01 → SRV-DC01: Kerberos / LDAP / DNS / GPO
- SRV-DC01 → Router: DNS forwarders (Internet resolution)
