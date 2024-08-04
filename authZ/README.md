### Authorization (AuthZ) Overview

**Definition**: Authorization is the process of determining what an authenticated user or system is allowed to do. It follows authentication, which verifies the identity of the user or system.

**Purpose**: To control access to resources and ensure that users or systems can only perform actions they are permitted to. Authorization ensures that users or systems have the right permissions based on their roles, attributes, or policies.

### Key Concepts

1. **Access Control**: 
   - **Definition**: Mechanisms used to enforce who can access or modify resources. This includes permissions, roles, and policies.
   - **Types**: 
     - **Discretionary Access Control (DAC)**: Resource owners set access permissions.
     - **Mandatory Access Control (MAC)**: Access is controlled by the system based on policies.
     - **Role-Based Access Control (RBAC)**: Access is granted based on roles assigned to users.
     - **Attribute-Based Access Control (ABAC)**: Access is based on user attributes, resource attributes, and environmental conditions.

2. **Roles and Permissions**:
   - **Roles**: Define a set of permissions grouped together, often reflecting job functions or responsibilities (e.g., Admin, Editor, Viewer).
   - **Permissions**: Specific rights granted to roles or users, such as read, write, delete, or execute.

3. **Policies**:
   - **Definition**: Rules that define access controls and permissions. Policies can be set based on various criteria such as user attributes, resource types, or contextual factors.
   - **Examples**: Access policies that specify conditions under which access is granted, such as time of day or location.

4. **Access Control Lists (ACLs)**:
   - **Definition**: Lists attached to resources that specify which users or systems are allowed or denied access and what actions they can perform.

5. **Contextual Factors**:
   - **Definition**: Factors such as time, location, device security, or current risk level that can influence access decisions.
   - **Examples**: Requiring higher access permissions for sensitive operations only if the user is accessing from a secure network.

### TL;DR

Authorization determines **what** authenticated users or systems are allowed to do within a system or resource. It involves managing roles, permissions, and policies to ensure that only authorized entities can access or modify resources. Authorization mechanisms help enforce security and ensure proper access control across various systems and applications.

```mermaid
graph TD
    A[Authenticated User/Application] --> B[Azure Active Directory]
    B --> C[Authorization Mechanisms]
    
    C --> D[Role-Based Access Control]
    C --> E[Azure AD Conditional Access]
    C --> F[Azure Policy]
    C --> G[Access Control Lists]
    C --> H[Managed Identities]
    
    D --> I[Resource Access]
    E --> I
    F --> I
    G --> I
    H --> I
    
    I --> J[Azure Resource]

