# Authentication (AuthN)

Authentication (AuthN) is the process of verifying the identity of a user or system to ensure they are who they claim to be. In Azure, authentication is primarily handled through Azure Active Directory (Entra), which supports various methods to validate identities:

- **Username/Password**: Basic method where users enter their credentials.
- **Multi-Factor Authentication (MFA)**: Adds an extra layer of security by requiring additional verification factors, such as a code sent to a phone.
- **Managed Identities**: Provides an identity for applications to authenticate to Azure resources without needing to manage credentials manually.
- **OAuth 2.0 and OpenID Connect**: Protocols used for securing API access and enabling single sign-on by handling authorization and authentication.

```mermaid
graph TD
    A[User/Application] --> B[Entra/Azure Active Directory]
    B --> C{Authentication Method}
    C --> D[Username/Password]
    C --> E[MFA]
    C --> F[Certificates]
    C --> G[Managed Identities]
    D --> H[Access Granted]
    E --> H
    F --> H
    G --> H
    B --> I[Azure Resource]
    H --> I
    I --> J[Access to Resource]

