---
layout: default
title: Credential Providers
nav_order: 6
has_children: true
---

# Credential Providers

Credential Providers are critical components of CyberArk’s suite of solutions, designed to securely manage and retrieve application credentials. The three main credential providers are:

- **CyberArk Credential Provider (CP)**
- **CyberArk Central Credential Provider (CCP)**
- **Conjur**

These tools work to eliminate hard-coded credentials in applications, scripts, and configuration files, while securely managing and retrieving credentials from the CyberArk Vault.

---

## Overview of Credential Providers

### CyberArk Credential Provider (CP)
The **CyberArk Credential Provider** operates as an agent installed on servers or workstations, directly interacting with the CyberArk Vault to retrieve credentials. It is commonly used in environments where applications can directly interface with the provider.

#### Key Features
- **Agent-Based Interaction:** Credentials are retrieved directly from the CyberArk Vault using an installed agent.
- **Application Integration:** Works seamlessly with traditional and legacy applications requiring credentials at runtime.
- **Offline Credential Access:** Supports caching credentials locally for use during network outages.

#### Use Case
CP is ideal for on-premises environments with applications that can integrate directly with an installed agent.

---

### CyberArk Central Credential Provider (CCP)
The **Central Credential Provider** adds an additional layer by providing a RESTful API service in front of the CP agent. This makes it more versatile for applications that need a standardized interface for credential retrieval.

#### Key Features
- **RESTful API Interface:** Applications can use standard HTTP calls to retrieve credentials.
- **Centralized Service:** Acts as a centralized service for managing multiple applications and credential requests.
- **High Compatibility:** Supports a wide range of applications, including web services and third-party integrations.

#### Use Case
CCP is best suited for distributed environments where applications need a centralized service for secure credential retrieval.

---

### Conjur
**Conjur** is a cloud-native credential provider designed to integrate with modern DevOps workflows, containerized applications, and cloud-native environments.

#### Key Features
- **Cloud-Native Design:** Built for containerized and dynamic environments.
- **DevOps Integration:** Works seamlessly with CI/CD pipelines and tools like Kubernetes, Jenkins, and Ansible.
- **APIs and CLI:** Provides APIs and command-line tools for easy integration and management.

#### Use Case
Conjur is ideal for dynamic, containerized, or cloud-native environments where automation and scalability are crucial.

---

## Comparison: CP, CCP, and Conjur

| **Aspect**             | **CP**                                            | **CCP**                                           | **Conjur**                                       |
|-------------------------|--------------------------------------------------|--------------------------------------------------|-------------------------------------------------|
| **Interface**          | Direct interaction with CyberArk Vault via agent | RESTful API service in front of CP agent         | API and CLI                                     |
| **Architecture**       | Agent-based                                      | Agent with centralized RESTful service          | Cloud-native                                    |
| **Application Support**| Traditional and legacy applications              | Broad compatibility, including modern web apps  | DevOps tools, CI/CD pipelines, containerized apps |
| **Use Case**           | On-premises environments                         | Distributed environments needing centralized service | Cloud-native and dynamic environments           |

---

## Benefits of Using Credential Providers
- **Eliminate Hard-Coded Credentials:** Prevent sensitive information from being exposed in scripts or applications.
- **Secure Credential Management:** Store and retrieve credentials securely within the CyberArk Vault.
- **Scalable Solutions:** Designed to handle a variety of applications and environments, from legacy systems to cloud-native architectures.

---

## Additional Resources
- [CyberArk CP Documentation](https://docs.cyberark.com/Product-Doc/OnlineHelp/CP/Latest/en/Content/CP/CredentialProviders.htm)
- [CyberArk CCP Documentation](https://docs.cyberark.com/Product-Doc/OnlineHelp/CP/Latest/en/Content/CP/CCP.htm)
- [Conjur Overview](https://www.cyberark.com/products/conjur/)
- [Best Practices for Credential Management](https://docs.cyberark.com/)

---

## Next Steps
- Learn how to [install and configure CP](#).
- Explore [REST API integration with CCP](#).
- Get started with [Conjur setup and DevOps workflows](#).





