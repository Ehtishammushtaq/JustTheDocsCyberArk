---
layout: default
title: High Availability
parent: CyberArk Vault
nav_order: 5
---
# High Availability


CyberArk supports high availability (HA) configurations to ensure continuous access to the Vault. This is achieved through the deployment of clustered nodes and shared resources, monitored by the **CyberArk Cluster Vault Manager (CVM)**.

## Components of High Availability
- **Cluster Vault Node:** A single Vault server paired with another node in a cluster.
- **Cluster Vault Manager (CVM):** Monitors Vault services and resources, triggering failovers when necessary.
- **Shared Storage:** A fiber-channel SAN accessible to all cluster nodes, hosting metadata and Vault data.
- **Shared Address (Virtual IP):** Represents the Vault in the public network and is allocated to the active node during startup.
- **Quorum Disk:** Prevents split-brain scenarios through a voting mechanism.
- **Cluster Private Network:** An isolated network for cluster heartbeat communication.

## Key Features
- **Automatic Failover:** Triggers in case of service or resource failure.
- **Scalability:** Supports two-node clusters with shared storage.
- **Redundancy:** Ensures data consistency and availability during failover scenarios.
