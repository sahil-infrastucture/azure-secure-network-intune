# Azure Secure Network with Intune

A learning-focused infrastructure project demonstrating how **identity**, **device trust**, and **network security** work together in a modern Azure environment.

This project is intentionally designed as a **hands-on lab**, built step by step to understand real-world cloud access patterns rather than production-scale complexity.

---

## Project Overview

Modern cloud security no longer relies only on firewalls or VPNs.  
Access decisions are increasingly based on:

- **Who the user is**
- **Which device they are using**
- **Whether the device is compliant**
- **How the network is secured**

This project demonstrates how secure access to Azure resources can be designed using:

- Microsoft Entra ID (Azure AD) for identity
- Microsoft Intune for device compliance
- Azure networking components for traffic control

Together, these layers form a **Zero Trust–aligned access model**.

---

## Why This Project Exists

In modern enterprise environments:

- Users may authenticate successfully, but their devices may be unmanaged
- Network access alone cannot guarantee secure access
- Infrastructure decisions increasingly depend on identity and device trust

This project exists to explore how:

- **Microsoft Entra ID** controls user identity
- **Microsoft Intune** evaluates device compliance
- **Azure networking** enforces network boundaries
- **Conditional Access** ties identity and device trust together

---

## High-Level Access Flow (Conceptual)

1. A user signs in using Microsoft Entra ID  
2. The device is evaluated for compliance using Microsoft Intune  
3. Conditional Access policies allow or deny access  
4. Approved devices connect securely to Azure resources  
5. Network Security Groups control traffic inside the virtual network  

This layered approach ensures access is granted **only when identity, device, and network conditions are satisfied**.

---

## Architecture Components

### Identity Layer
- **Microsoft Entra ID**
  - User authentication
  - Group-based access control

### Device Management Layer
- **Microsoft Intune**
  - Device enrollment
  - Compliance evaluation
  - Device trust signaling

### Network Layer
- **Azure Virtual Network (VNet)**
  - Private cloud networking

### Security Controls
- **Network Security Groups (NSGs)**
  - Inbound and outbound traffic filtering

### Connectivity
- **Secure access mechanisms**
  - Designed to be expanded in later phases

Each component solves a specific problem and contributes to a complete infrastructure design.

---

## Scope of the Project

### Included
- Azure identity fundamentals
- Group-based access control
- Device trust using Microsoft Intune
- Zero Trust access concepts
- Realistic troubleshooting scenarios
- Clear documentation and reasoning

### Intentionally Excluded
- Enterprise-scale high availability
- Advanced firewall appliances
- Large-scale automation or CI/CD pipelines

The focus is **understanding**, not production complexity.

```
## Repository Structure

azure-secure-network-intune/
├── README.md
├── architecture/ # Architecture explanations and diagrams
├── networking/ # VNet, NSG, and networking concepts
├── intune/ # Device enrollment and compliance
├── troubleshooting/ # Failure scenarios and resolutions
└── notes/ # Design decisions and lessons learned

```

## Learning Goals

This project was built to:

- Understand how identity affects network access
- Learn how Microsoft Intune integrates with infrastructure security
- Explore how device compliance influences Conditional Access
- Practice troubleshooting real infrastructure failures
- Improve documentation and architectural thinking

---

## Troubleshooting Mindset

Infrastructure is defined by **how failures are handled**, not just successful setups.

This project intentionally includes scenarios such as:

- Device marked non-compliant
- Access blocked by Conditional Access
- Network traffic denied by NSGs

Each issue is documented with:
- Symptoms
- Root cause
- Resolution steps

---

## Security and Cost Considerations

- All work is performed in a **personal lab tenant**
- No production environments are used
- No secrets, credentials, or tenant IDs are stored
- Only free or trial-based services are used
- Resources are shut down or removed when not needed

---

## Lessons Learned

This is a living section that evolves as the project grows.  
It captures:

- What was initially confusing
- What became clear through hands-on work
- Design decisions that would change in future iterations

---

## How to Use This Repository

1. Read the Project Overview and Architecture sections
2. Follow the phases documented in the `notes/` directory
3. Review troubleshooting scenarios to understand failure handling
4. Use this project as a reference for learning or interview discussion

---

## Disclaimer

This repository represents a **learning lab**, not a production deployment.  
Design choices prioritize clarity and understanding over enterprise scale.
