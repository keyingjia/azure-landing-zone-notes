Azure Basics: Concepts and Architecture

This document summarizes the foundational knowledge I’ve learned about Microsoft Azure, focusing on core services, resource hierarchy, identity and access management, and governance tools like policies and blueprints. It serves as both a study note and a reference for future Azure-related work.

1. Azure Core Services

Azure provides a wide range of cloud services that fall into several major categories. Understanding these categories helps with designing scalable and efficient cloud solutions.

1.1 Compute
Virtual Machines (VMs): On-demand Windows or Linux machines.
App Services: PaaS offering for hosting web applications.
Functions: Serverless compute service for event-driven applications.
Container Instances / AKS: Run containers or orchestrate them with Kubernetes.

1.2 Storage
Blob Storage: Object storage for unstructured data like images or videos.
Azure Files: Managed file shares accessible via SMB.
Disk Storage: Block storage for use with VMs.
Tables & Queues: NoSQL storage and message queues.

1.3 Networking
Virtual Network (VNet): Fundamental building block for private communication.
Network Security Groups (NSGs): Control inbound/outbound traffic to resources.
Azure Firewall / Application Gateway / Load Balancer: Advanced traffic routing and filtering.
VPN Gateway / ExpressRoute: Secure connection between on-prem and Azure.

1.4 Security
Azure Active Directory (AAD): Identity service for users and apps.
Microsoft Defender for Cloud: Security posture management and threat detection.
Key Vault: Securely store and manage secrets, keys, and certificates.
Azure DDoS Protection: Prevent distributed denial-of-service attacks.


2. Resource Hierarchy: Subscription, Resource Group, and Resources

Azure uses a hierarchical structure to manage cloud assets efficiently:

Subscription
- A billing container for deployed resources.
- Represents an isolated boundary for services, policies, and RBAC.

Resource Group (RG)
- A logical container that holds related resources.
- Resources in a group share the same lifecycle, permissions, and policies.

Resources
- Individual services like VMs, storage accounts, databases, etc.
- Deployed and managed within a Resource Group.



3. Identity and Access Control (RBAC)

Azure uses Role-Based Access Control (RBAC) to manage permissions.

Key Concepts
- Principal: The user, group, or app requiring access.
- Role Definition: A collection of permissions (e.g., Reader, Contributor, Owner).
- Scope: The level at which access is applied — subscription, RG, or resource.

Examples
| Role        | Description                        |
|-------------|------------------------------------|
| Owner       | Full access to all resources       |
| Contributor | Can manage resources but not RBAC  |
| Reader      | View only access                   |



4. Azure Governance: Policy & Blueprints

Azure Policy
- Enforces organizational standards and compliance.
- Example: Require that all VMs use managed disks or tag resources with `cost-center`.

Components:
- Policy Definition: Describes what to evaluate and what action to take.
- Initiative: A collection of related policy definitions.
- Assignment: Applies policy/initiative to a scope.

Azure Blueprints
- Packages resources, policies, and RBAC into a reusable template for environment setup.
- Ideal for deploying consistent environments across multiple subscriptions.

Blueprint Components:
- ARM templates (infrastructure)
- Policies (governance)
- RBAC assignments (access)
- Resource Groups

Summary

| Concept        | Purpose                                  |
|----------------|------------------------------------------|
| Core Services  | Provide cloud capabilities (compute, storage, etc.) |
| Resource Model | Organize and manage cloud assets         |
| RBAC           | Control who can access what              |
| Policy         | Enforce rules and compliance             |
| Blueprint      | Deploy repeatable, governed environments |


References

- [Azure Documentation](https://docs.microsoft.com/en-us/azure/)
- [Azure Policy Overview](https://learn.microsoft.com/en-us/azure/governance/policy/overview)
- [Azure Blueprints Overview](https://learn.microsoft.com/en-us/azure/governance/blueprints/overview)
- [RBAC in Azure](https://learn.microsoft.com/en-us/azure/role-based-access-control/overview)

