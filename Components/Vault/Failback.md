---
layout: default
title: Failback
parent: CyberArk Vault
nav_order: 5
---
# Failback

Failback is the process of restoring the primary Vault after a failover to the DR Vault.

## Steps for Failback
1. Set **Auto Failover Mode** to "No."
2. Delete the last two entries in the `padr.ini` file:
   - `NextBinaryLogNumberToStartAt`
   - `LastDataReplicationTimeStamp`
3. Restart the DR service to reestablish the primary Vault as the active node.