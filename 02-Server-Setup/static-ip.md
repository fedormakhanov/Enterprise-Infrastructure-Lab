# Static IP Configuration

## Objective
Assign a static IP address to SRV-DC01 for domain controller stability.

## Configuration

- IP Address: 192.168.10.10
- Subnet Mask: 255.255.255.0
- Gateway: 192.168.10.1
- DNS Server: 192.168.10.10 (self)

## Steps

1. Open Network & Internet Settings
2. Change adapter options
3. Right-click Ethernet → Properties
4. Select IPv4 → Properties
5. Enter the static IP configuration

## Result
The server is reachable consistently and ready for AD DS installation.
