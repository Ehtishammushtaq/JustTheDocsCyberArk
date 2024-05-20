---
layout: default
title: Accounts and Services
parent: PVWA
nav_order: 6
---
# Accounts and Services

### Service Accounts

A service account is a special type of user account that is intended for non-human users such as applications, services, or automated processes to interact with the operating system or software applications. Unlike regular user accounts, which are typically associated with individual people, service accounts are used by software services and applications to control access to network resources, execute processes, and perform tasks that require specific user rights.

### PVWA Predefined Users (Service Accounts)

These are the service accounts that the PVWA application uses to interact with other components.

- **PVWA APP USER**: Handles batch jobs, background jobs, mostly internal tasks.
- **PVWA GW USER**: This user connects PVWA to the Vault. This is the user who will access the Vault for the Password Vault Web Access.

### PVWA Services

- **IIS**: This service connects PVWA to the internet.
- **Schedule Task Service**: Responsible for generating reports, background jobs.

