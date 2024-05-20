---
layout: default
title: CPM
nav_order: 3
has_children: true
---
# CPM

The Central Policy Manager is responsible for automatically managing (rotating), changing, and verifying passwords for privileged accounts across an organization's network and devices. It ensures that the access to privileged accounts is secure and compliant with the organization's policy by enforcing password complexity, rotation, and access control policies. This reduces the risk of unauthorized access to critical systems and data, enhancing the overall security posture of an organization. CPM has to be assigned to a SAFE. CPM also has account discovery. CPM configs are done through PVWA.

**Password Verification**: This verifies password content on remote devices to ensure that they are synchronized with corresponding passwords in the Password Vault and are valid and up to date. CyberArk tries to login to the system and if successful, then verified.

**Password Change**: On this option, CyberArk will login to the system and then if successful, will update the target with a temp password. Then it will update the password on the CyberArk side.

**Password Reconciliation**: When CyberArk is not able to login to the target system with the stored credentials, it will use Recon Account to reconcile and sync the passwords between Vault and Target machine.

**Password Rotation**: Password rotation refers to the practice of automatically changing passwords at regular intervals or under certain conditions.

On a separate note, when the password on the target system is changed bypassing CyberArk, the password goes out of sync. Verify button is used to check if the hashes match. If the passwords are not matching, we can do password reconciliation, which basically changes the password on the target machine and stores it in CyberArk. Reconcile accounts are needed as we need access to the target system.

Reconcile accounts are a type of Create linked accounts. You can define a reconciliation account password that will be used to reset the unsynchronized password at the account level. You can store this account in a separate Safe, where it is only accessible to Privilege Cloud for reconciliation purposes. For details, see Define a reconciliation account password. The reconcile account can be defined on the target account level or on the platform level, making it available to all accounts associated with the platform. CPM is installed as a separate component and can be installed on the same server as your PVWA. But considering the load and other security vulnerabilities that come with co-located installation, it is often advisable to install it on a separate server.

