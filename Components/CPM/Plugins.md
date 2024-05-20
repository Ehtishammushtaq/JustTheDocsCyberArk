---
layout: default
title: Plugins
parent: CPM
nav_order: 1
---
# Plugins

### CPM Installation and Platform Differences
- While CPM is installed as a separate component, each platform is different in the sense that changing passwords for a Windows machine is different than changing passwords on a Linux machine.
- Different systems types have different plugins. For example, the way you log in and change a password on a Windows server is different than how you do the same thing on a Unix server.
- Each plugin is associated with the relevant platform that manages the password policy setting for the specific target machine.
- There are a couple of out-of-the-box plugins for target accounts. For some specific use cases that don’t fit the out-of-the-box criteria, you can download or create your own plugin.
  - For downloads, go to CyberArk Marketplace.
  - To build your own, CyberArk has an Integrations and tools tab on their website.
- Plugins are attached at the Platform level. To meet specific needs, you might need to create a new platform for those specific devices to be able to use CPM.

### Execution
- For each password change request, the CPM uses a specific plugin tailored to interact with the target system or application where the account resides.
- This plugin knows how to log into the system, navigate its interface or API, and execute the password change operation according to the system's requirements and constraints.
- Regardless of what account is stored in the safe, the platform level configuration will take care of it.


### Custom Plugin

- IDRAC and ILO
- Install custom plugins from MarketPlace
- Move the files to the bin folder
- Import the platform in CyberArk
- Assign it to accounts

### What report do you run to see all accounts that are failing

- Compliance report and filter to see the failed account


<br>
<img src="{{ site.baseurl }}/assets/Images/cpm1.png" alt="Infrastructure" style="width: 100%; height: auto; margin: auto; display: block;">
<br>
<img src="{{ site.baseurl }}/assets/Images/cpm2.png" alt="Infrastructure" style="width: 100%; height: auto; margin: auto; display: block;">
<br>
<img src="{{ site.baseurl }}/assets/Images/cpm3.png" alt="Infrastructure" style="width: 100%; height: auto; margin: auto; display: block;">
<br>
<img src="{{ site.baseurl }}/assets/Images/cpm4.png" alt="Infrastructure" style="width: 100%; height: auto; margin: auto; display: block;">
<br>
