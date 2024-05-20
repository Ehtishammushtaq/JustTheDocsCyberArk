---
layout: default
title: Troubleshooting
parent: PVWA
nav_order: 7
---
# Troubleshooting

### Error: Authentication failed

- **Check if the user is using the correct Authentication Method**
  - Private Ark -> Tools -> Admin tools -> Users and groups -> Find the user -> Properties -> Authentication they should be using.
- **Check if the user is using the right credentials**
  - Go to PVWA and look for the account and password.
- **Check if the user has access to CyberArk**
  - Check the AD group for CyberArk and see if the user is a member of the group.
- **Check if the user’s account is not locked in AD**

### Users getting Kicked out

- **Check web.config logs, Trace logs, and console logs to see if anything seems odd.**
- **This seems to be a typical case of load balancing issue.**
  - Contact the F5 team and have them fix the load balancer.

### Error generating report

- **Check if the schedule task service is running as it is responsible for background jobs and reports.**

### User Suspended Error

- **The user is locked in PrivateArk**
  - PrivateArk -> Tools -> Admin tools -> Users and groups -> Trusted net area -> Find the user -> Activate the user.

### Communication Error / The interface is not loading

- **Check the main services, Scheduled task service, and the ISS service.**
- **Restart the ISS service as it connects PVWA to the web.**
- **Check web.config logs for any anomaly**

### Issue – web.config got corrupted

- **Usually happens when the installation path was pointing to the wrong drive**
- **Create a web.config file with the right path**
  - Locate the file: The web.config file for PVWA is typically located in the root directory of the PVWA application on the IIS server where PVWA is hosted. `C:\inetpub\wwwroot\PVWA\`
  - Edit or Create the New web.config File: If you are creating a new web.config file from scratch (which is unusual, as you would normally edit the existing one), you can open a text editor like Notepad or any code editor of your choice.
  - Add PVWA-Specific Settings: Within the web.config file, you will need to configure settings specific to your PVWA installation. This might include database connection strings, session timeout settings, authentication settings, and other application-specific settings as per CyberArk's documentation or your organization's requirements.
  - Apply the New Configuration: Once the new web.config file is ready, place it in the root directory of the PVWA application on the IIS server, replacing the old one.
  - Restart IIS: After updating the web.config file, you may need to restart IIS for the changes to take effect. This can be done through the IIS Manager or by using the `iisreset` command in the command prompt.
- **Restart the ISS service.**
