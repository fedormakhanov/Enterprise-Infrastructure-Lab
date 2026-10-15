# DNS Configuration

## Objective
Configure DNS to support AD DS and domain operations.

## Settings

- Primary DNS: 192.168.10.10
- Forwarders: (optional) 8.8.8.8, 1.1.1.1

## Verification

Run:
nslookup corp.local

Expected output:
Name: corp.local
Address: 192.168.10.10

## Result
DNS is fully functional and supports domain resolution.
