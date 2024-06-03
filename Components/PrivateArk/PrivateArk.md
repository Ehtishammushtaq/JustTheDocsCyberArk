---
layout: default
title: PrivateArk
nav_order: 5
has_children: true
---
# PrivateArk

The PrivateArk Client is a Windows-based application that allows for direct interaction with 
the CyberArk Vault Server. It's designed for performing administrative activities within the 
Enterprise Password Vault. Administrators typically use the PrivateArk Client to manage the 
CyberArk Vault, including tasks such as managing safes, users, and policies.
The PrivateArk Client can be installed on the same machine as the Enterprise Password 
Vault, but it can also be deployed on users' workstations to perform administrative tasks 
remotely. This flexibility allows administrators to securely manage the Vault without 
needing to be directly on the server where the Vault is installed. PVWA couldn’t do 
EVERYTHING PrivateArk client could. Some configuration options aren’t available in the 
PVWA so the PAClient needs installed in order to perform some low-level actions like 
editing directory mapping’s, resetting credential files and transferring files to and from your 
Vault


## Installing the PrivateArk Client

1. **Gather Information**: During the installation, you will need the following information about the vault:
   - Vault’s Server Name
   - Server Address (IP)
   - Default Username
   - The port used to talk to the vault is 1858.
   - You will need to be a member of the POC Admin group to perform this installation.

2. **Advanced Settings**:
   - Go to **Advanced Settings** -> **Authentication Method** -> and choose the appropriate authentication method, such as LDAP or Radius.

3. **Restart the Server**: After the installation, restart the server you installed the PrivateArk client on.