---
layout: default
title: PSM
nav_order: 4
has_children: true
---
# PSM

CyberArk Privileged Session Manager (PSM) is a component of the CyberArk Privileged Access Security Solution. The PSM aims to secure, control, and monitor privileged access to critical systems and data. It does so by isolating, controlling, and monitoring the sessions that privileged users, such as system administrators, have with systems that hold sensitive data or are critical to business operations. Recordings are kept for 90 days. Recordings are kept in PSMrecording safe. Some reports worthy of note are Activity report and Activity log.

<br>
<img src="{{ site.baseurl }}/assets/Images/psm1.png" alt="Infrastructure" style="width: 100%; height: auto; margin: auto; display: block;">
<br>
<img src="{{ site.baseurl }}/assets/Images/psm2.png" alt="Infrastructure" style="width: 100%; height: auto; margin: auto; display: block;">
<br>
<br>

PSM for Windows directly enables us to connect to a target system from the desktop using the RDP client. Once you have your PSM correctly installed and configured with the appropriate groups added to the safe, you will need to onboard the account to the safe with the appropriate platform, and then you will be able to see a connect button in the accounts tab. They will be given access to the “connect” button because the account they are using is a privileged account stored in the safe.

### How to Configure for Special Types of Connectors Besides RDP and SSH (Out of the Box)

1. Go to platform management and click **Marketplace** -> Download the required platform, for example, Facebook platform.
2. Then click **Import Platform** from the same platform management window.
3. After importing, you will see a new platform in the platform management window.
4. Go to platform management and click the three-dotted menu on the newly imported platform -> **Manage Connectors**.
5. Select the PSM server that will manage the session.
6. Go to the general CyberArk Marketplace and download the connector.

<br>
<img src="{{ site.baseurl }}/assets/Images/psm3.png" alt="Infrastructure" style="width: 100%; height: auto; margin: auto; display: block;">
<br>


- Drag and drop the new connector to the platform. Then just onboard the account normally using this platform and an appropriate safe. Put the username and password for the Facebook account in the account properties. You are good to connect using PSM.

### For Other Custom Connectors Follow These Steps:

1. Go to the Admin Section and select **Config Options** -> **Connection Components**.
2. Duplicate an existing connector and change the ID to the connector you want.
3. Change the webform field and put the XPath copied from the inspect element from the required website.
4. Associate this connector with a new or existing platform.
