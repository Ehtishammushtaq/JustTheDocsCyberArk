---
layout: default
title: Troubleshooting
parent: CPM
nav_order: 4
---
# Troubleshooting

### Error - Account is failing to reconcile

- Check if the correct recon account is associated.
- See if the CPM is assigned to the safe.
- See if the recon account is locked in AD.

### Error - Name does not exist

- Means the account does not exist in AD.

### Error - CPM disabled the account

- Check if the recon account is locked.
- Check if the recon account has access to the domain of the account.

### How to set Head Start Interval

- Set it at the platform level. If rotation is set for 30 days, you can set the head start interval to 5 days so CPM rotates the password 5 days earlier (used to take load off the CPM).
