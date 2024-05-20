---
layout: default
title: Basic Operations
parent: PVWA
nav_order: 4
---
# Basic Operations

### How to Bulk Onboard Accounts

- **PVWA -> Add Accounts (drop down) -> Upload CSV** (correct formatting) limit 10,000 accounts. Some prerequisites are Username, PlatformID, and SafeName.

### How to Onboard Accounts

- **Some prerequisites to know:**
  - Select the system type [Unix, Windows, etc.]. After clicking this, the platform will be filtered for this type of system.
  - Platform to be used or a fresh instance of one.
  - Naming conventions.
  - Safe that it is going to be onboarded in.
  - After these steps, it depends on the organization for other particulars like rotation policy, password strength, etc.

### Additional Security on Accounts

- Initiate check-in/check-out, one-time passwords, dual control.

### How to See All Reports in CyberArk

- Run an Inventory report.

### Change the Deletion Time of Logs

- Go to master policy and create an exception -> Change the audit period to x days from the default 90 days.
