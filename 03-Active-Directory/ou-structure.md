# Organizational Unit Structure (corp.local)

This OU architecture follows enterprise standards and separates users, computers, servers, 
administrators, and service accounts for proper Group Policy and access control management.
```
corp.local
└── Corp
    ├── Corp Users          - Standard domain users
    ├── Corp Computers      - Domain-joined workstations
    ├── Admins              - Administrative accounts (Domain Admins)
    ├── Servers             - Server objects (future expansion)
    └── Service Accounts    - Non-human accounts for services and automation
```

## Purpose

- Simplifies GPO targeting
- Improves security and access control
- Matches real corporate AD design
