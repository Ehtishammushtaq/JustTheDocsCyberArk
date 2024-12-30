---
layout: default
title: CP
parent: Credential Providers
nav_order: 1
---
#  Credential Provider (CP)


The **Credential Provider (CP)** is installed directly on servers running applications and is designed to securely retrieve credentials for these applications. It provides tools for retrieving passwords using a single function call in a **command-line interface (CLI)** or a native API for **Java**, **C/C++**, and **.NET** across various platforms. 

## Key Features
- **Application Authentication:** CP authenticates applications at runtime and during password requests to prevent credential theft.
- **High Performance & Availability:** Includes a secure caching mechanism for credentials, ensuring high performance and availability even during network disruptions to the Vault.
- **Platform Support:** Supports various platforms and programming languages, making it versatile for diverse environments.
- **Mission-Critical Applications:** Ideal for business-critical applications due to its reliable and secure architecture.

---

## Architecture of CP Agent

The Credential Provider follows a simple yet robust architecture:

- **Installation Location:** Installed on the client machine where the application requiring the password is hosted.
- **Vault Communication:** Requires a direct link or communication with the CyberArk Vault to retrieve credentials.
- **Secure Cache:** Configured to securely cache credentials locally, providing continued functionality even if the Vault is temporarily inaccessible.

---

## Authentication Process

The CP authenticates applications based on multiple parameters to ensure security and legitimacy. The authentication process includes:

1. **Application Name:** Each application is assigned a unique **APP ID**.
2. **Allowed Machine:** Authentication is based on IP address, DNS name, or hostname.
3. **OS Username:** Validates the operating system user under which the application runs.
4. **Path:** Verifies the valid file path for each application.
5. **Hash:** Ensures integrity using a list of hash keys/values specific to the application.

---

## Installation of CP Agent

To install and configure the CP agent, follow these steps:

### Steps:
1. **Download the Installer:**
   - Obtain the CP agent executable (`.exe`) from the CyberArk Marketplace and transfer it to the client server.
   - Run the setup to install the agent.

2. **Vault User Creation:**
   - During installation, a user named `Prov_<serverHostname>` is automatically created in the CyberArk Vault.

3. **CyberArk Prerequisites:**
   - **Provisioning Details:** Ensure the following are prepared in CyberArk:
     - `Prov_<serverHostname>` user
     - Safe name
     - Machine name
     - IP address
   - **Authentication Setup:** Add OS username, application path, or hash to the authentication settings.

4. **Safe Permissions:**
   - Add the `Prov_<serverHostname>` user to the relevant safe in the Vault.

5. **Configuration:**
   - Configure the CP agent using a YAML file or a list of commands.
   - Applications can use this configuration to retrieve credentials and enable auto-login functionality.

---

## Benefits of Using CP
- **Enhanced Security:** Prevents hard-coded credentials and enforces strict application authentication mechanisms.
- **Reliability:** Ensures credentials remain accessible through secure caching during network issues.
- **Versatility:** Compatible with a wide range of applications and platforms.
- **Efficiency:** Optimized for business-critical operations requiring low latency and high availability.

---

## Additional Resources
- [Credential Provider Installation Guide](https://docs.cyberark.com/)
- [CP API Reference](https://docs.cyberark.com/)
- [Best Practices for Secure Application Authentication](https://docs.cyberark.com/)

