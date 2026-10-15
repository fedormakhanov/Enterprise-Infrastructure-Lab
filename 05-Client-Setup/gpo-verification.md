# GPO Verification

## Objective
Verify that Group Policy Objects apply correctly to domain-joined clients.

## Commands

Run on client:
gpupdate /force

Check applied policies:
gpresult /r

## Expected Results

- Password Policy: Domain-level settings visible
- Desktop Policy: Wallpaper enforced, Control Panel disabled
- Security Baseline: Firewall enabled

## Purpose

Ensures that the domain controller successfully manages workstation configuration.
