---
layout: default
title: CCP
parent: Credential Providers
nav_order: 2
---

# Central Credential Provider (CCP)

The **Central Credential Provider (CCP)** is installed on a separate Windows server and enables applications to leverage the capabilities of the CyberArk Credential Provider (CP) without requiring the installation of CP on each end-user machine. CCP operates remotely and serves as a centralized service, allowing applications to securely retrieve credentials from the CyberArk Vault during runtime.

## Key Features
- **Centralized Credential Management:** Applications call a centralized service to retrieve credentials, reducing the need for local agents.
- **RESTful API Interface:** Provides a RESTful interface for seamless integration with various applications.
- **Load Balancing:** Can be load-balanced for enhanced availability and performance.
- **Deployment Flexibility:** Suitable for non-mission-critical applications or environments where deploying agents on each server is challenging.
- **Platform Requirements:** Runs on any Windows server capable of hosting IIS services, with considerations for load and availability.

---

## Architecture of CCP Agent

The CCP architecture is designed to provide secure and efficient credential retrieval:

- **CP Backend:** Relies on the Credential Provider backend for secure interactions with the Vault.
- **Source Cache:** Refreshes every 15 minutes to ensure up-to-date credentials.
- **RESTful Frontend:** Offers a standardized API interface for applications.
- **Windows IIS Service:** Runs on a Windows server capable of hosting IIS (Internet Information Services).
- **Application Authentication:** Implements additional application authentication methods for enhanced security.

---

## Authentication Process

The CCP ensures secure credential retrieval using the following authentication parameters:

1. **Application ID (App ID):** A unique identifier for each application.
2. **Allowed Machines:** Validates the IP address or hostname of allowed machines.
3. **OS Username:** Authenticates based on the operating system user under which the application runs.
4. **Certificate:** A signed certificate installed on the client-side provides additional client-side authentication.

---

## Installation of CCP Agent

To install and configure the CCP agent, follow these steps:

### Steps:
1. **Download the Installer:**
   - Obtain the CCP agent executable (`.exe`) from the CyberArk Marketplace.
   - Transfer the installer to the designated server and run the setup.

2. **Vault Configuration:**
   - Provide the Vault’s **IP address** and **port number** (default: `1858`).
   - Enter the **Admin credentials** for the Vault during setup.

3. **Application Registration:**
   - Navigate to **Applications -> Application List** in the CyberArk PVWA interface.
   - Add a new application named `AIMWebService` (specific to the CCP server).
   - Configure the application to allow the IP address of the CCP server.

4. **Allowed Machines:**
   - In the application settings, add the IP address of the server where CCP is installed.

---

## Configuring an Application to Use CCP

To allow an application to retrieve credentials via CCP, perform the following steps:

1. **Add the Application:**
   - In the **Applications** section of the PVWA, create a new application named `MYAPP`.
   - Add the IP address of the machine where the application is hosted (e.g., a MacBook).

2. **Access Control:**
   - Navigate to **Policy -> Access Control** and locate the safe where the credentials are stored.
   - Edit the safe permissions to include the following users:
     - `AIMWebService`
     - `MYAPP`
     - `Prov_<Hostname>`

3. **Test the Configuration:**
   - Verify that the application can successfully retrieve credentials from the Vault through CCP.

---

## Benefits of Using CCP
- **Simplified Deployment:** Eliminates the need to install agents on every server.
- **High Availability:** Supports load balancing for better performance and fault tolerance.
- **Scalable Integration:** Ideal for environments with diverse applications requiring credential access.

---

## Additional Resources
- [Central Credential Provider Installation Guide](https://docs.cyberark.com/)
- [CCP API Reference](https://docs.cyberark.com/)
- [Best Practices for Central Credential Provider](https://docs.cyberark.com/)
