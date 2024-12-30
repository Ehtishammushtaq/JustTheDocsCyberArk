---
layout: default
title: Failover
parent: CyberArk Vault
nav_order: 5
---

# Failover

Failover ensures continuous access to the Vault by switching operations from the primary to the DR Vault or another node in the cluster.

## Initiating Failover
- **Standalone Setup:** Stop the Vault Server service on the primary Vault.
- **Cluster Setup:** Use the CVM interface to trigger a failover.
- **DR Vault:** Monitors the primary Vault and becomes active when the primary Vault goes offline.

### Services Monitored for Failover
- PrivateArk Server Service
- PrivateArk Database Service
- Logic Container Service