---
layout: default
title: Stand Alone
parent: CyberArk Vault
nav_order: 5
---

# Stand Alone

In a stand-alone configuration, the Vault consists of a primary Vault and a Disaster Recovery (DR) Vault without clustering.

## Characteristics
- **Primary Vault:** Active node handling all operations.
- **DR Vault:** Passive node that becomes active during failover.
- **Replication:** Managed by the DR service with full and smart replication modes.

## Switching Roles
- Use the **PrivateArk Server Service** to manually switch between the primary and DR Vaults.
- Click the **red button** in the PrivateArk interface to simulate a DR scenario.