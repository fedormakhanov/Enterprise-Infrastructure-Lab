                     ┌───────────────────────────┐
                     │      Domain Controller    │
                     │         SRV-DC01          │
                     │       corp.local          │
                     └─────────────┬─────────────┘
                                   │
                                   │  GPO Replication
                                   │  (SYSVOL + AD DS)
                                   │
                     ┌─────────────▼─────────────┐
                     │     SYSVOL Share          │
                     │  \\SRV-DC01\SYSVOL        │
                     └─────────────┬─────────────┘
                                   │
                                   │  GPO Download
                                   │  (Client → DC)
                                   │
                     ┌─────────────▼─────────────┐
                     │     CLIENT-01             │
                     │  Windows 10/11            │
                     │  Domain Joined            │
                     └─────────────┬─────────────┘
                                   │
                                   │  gpupdate /force
                                   │  gpresult /r
                                   │
                     ┌─────────────▼─────────────┐
                     │   GPO Processing Engine   │
                     │   (User + Computer Mode)  │
                     └─────────────┬─────────────┘
                                   │
                                   │  Applies:
                                   │  - Password Policy
                                   │  - Desktop Policy
                                   │  - Security Baseline
                                   │
                     ┌─────────────▼─────────────┐
                     │   Final Configuration     │
                     │  (Firewall, Wallpaper,    │
                     │   Control Panel, etc.)    │
                     └───────────────────────────┘
