```
                ┌──────────────────────────────┐
                │        CLIENT-01             │
                │  User logs in (user1)        │
                └───────────────┬──────────────┘
                                │
                                │ 1. Request TGT
                                │    (Kerberos AS-REQ)
                                │
                ┌───────────────▼──────────────┐
                │      SRV-DC01 (KDC)          │
                │  Kerberos Authentication     │
                └───────────────┬──────────────┘
                                │
                                │ 2. Issue TGT
                                │    (AS-REP)
                                │
                ┌───────────────▼──────────────┐
                │        CLIENT-01             │
                │  Stores TGT locally          │
                └───────────────┬──────────────┘
                                │
                                │ 3. Request Service Ticket
                                │    (TGS-REQ)
                                │
                ┌───────────────▼──────────────┐
                │      SRV-DC01 (KDC)          │
                │  Issues ST for LDAP/GPO      │
                └───────────────┬──────────────┘
                                │
                                │ 4. LDAP Bind
                                │    (Directory Query)
                                │
                ┌───────────────▼──────────────┐
                │   Active Directory (LDAP)    │
                │   OU, Groups, Policies       │
                └───────────────┬──────────────┘
                                │
                                │ 5. GPO Retrieval
                                │    (SYSVOL + LDAP)
                                │
                ┌───────────────▼──────────────┐
                │        CLIENT-01             │
                │  Applies GPO + Auth Success  │
                └──────────────────────────────┘
```
