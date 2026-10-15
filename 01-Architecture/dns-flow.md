```
                         ┌───────────────────────────┐
                         │        CLIENT-01          │
                         │   user1@corp.local        │
                         │   IP: 192.168.10.20       │
                         └─────────────┬─────────────┘
                                       │
                                       │ 1. DNS Query
                                       │    "SRV-DC01.corp.local?"
                                       │
                         ┌─────────────▼─────────────┐
                         │   DNS Server / DC         │
                         │       SRV-DC01            │
                         │     192.168.10.10         │
                         └─────────────┬─────────────┘
                                       │
                                       │ 2. Local Zone Lookup
                                       │    corp.local zone
                                       │
                         ┌─────────────▼─────────────┐
                         │   AD-Integrated DNS Zone  │
                         │     corp.local            │
                         │  (A, SRV, CNAME records)  │
                         └─────────────┬─────────────┘
                                       │
                                       │ 3. Response
                                       │    "SRV-DC01 = 192.168.10.10"
                                       │
                         ┌─────────────▼─────────────┐
                         │        CLIENT-01          │
                         │   DNS Cache Updated       │
                         └─────────────┬─────────────┘
                                       │
                                       │ 4. If domain not found:
                                       │    Forwarder Query →
                                       │
                         ┌─────────────▼─────────────┐
                         │     DNS Forwarders        │
                         │   8.8.8.8 / 1.1.1.1       │
                         └─────────────┬─────────────┘
                                       │
                                       │ 5. External DNS Resolution
                                       │
                         ┌─────────────▼─────────────┐
                         │        Internet DNS       │
                         └───────────────────────────┘
```

CLIENT → SRV-DC01: DNS query
SRV-DC01 → AD DNS Zone: Lookup corp.local records
SRV-DC01 → CLIENT: Response (A, SRV, CNAME)
If record not found → Forwarders → Internet DNS
