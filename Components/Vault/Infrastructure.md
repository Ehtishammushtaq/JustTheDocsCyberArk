---
layout: default
title: Infrastructure
parent: CyberArk Vault
nav_order: 5
---

# Infrastructure

The CyberArk Vault infrastructure includes the Primary Vault, Disaster Recovery (DR) Vault, and clustered configurations for high availability.

## Disaster Recovery (DR)
- **DR Service Features:**
  - **Failover Check:** Sends heartbeat messages using ICMP protocol.
  - **Replication Modes:**
    - **Full Replication:** Initial complete data copy.
    - **Smart Replication:** Incremental replication of changes.

- **Failover Process:**
  - Automatically switches between primary and DR Vault when a failure is detected.
  - Configured through the **padr.ini** file.

## Stand-Alone Configuration
- **Primary and DR Vaults:** A basic setup with an active primary and passive DR Vault.
- **Switching Roles:** Triggered by stopping the Vault Server service on the primary Vault.

## High Availability Configuration
- Two nodes in each environment:
  - Monitored by **CVM**.
  - Connected to shared storage and a shared virtual IP.