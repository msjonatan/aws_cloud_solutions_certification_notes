# AWS Solutions Architect Certification – Session 2

*(Note: Text is in English, as the exam is in English. Key AWS/cloud terms are provided in Spanish (in parentheses) where helpful.)*

---

## Introduction

Welcome to Session 2 of the AWS Solutions Architect course. In this session, we delve into identity, access, governance, and multi-account strategies. Understanding these concepts is critical for architecting secure, compliant, and scalable cloud environments. We will discuss the Shared Responsibility Model, how to access AWS, Identity and Access Management (IAM), AWS Support Plans, and multi-account strategies using AWS Organizations.

**Topics Covered:**
1. Shared Responsibility Model (Modelo de Responsabilidad Compartida)
2. How to Access AWS (¿Cómo acceder a AWS?)
3. Identity and Access Management (IAM - Gestión de Identidad y Acceso)
4. AWS Support Plans (Planes de Soporte)
5. Multi-Account Strategies (Estrategias Multi Cuenta)

---

## Shared Responsibility Model (Modelo de Responsabilidad Compartida)

AWS and customers share security responsibilities:

**AWS Responsibilities (Seguridad de la Nube):**
- Physical security of data centers (centros de datos), global infrastructure, and hardware.
- Managing the virtualization layer, patching the hypervisor.
- Ensuring the security **of** the cloud.

**Customer Responsibilities (Seguridad en la Nube):**
- Configuring operating systems (sistemas operativos invitados), databases, and applications.
- Encrypting data (encriptación de datos) at rest and in transit.
- Managing identity and access via IAM and applying firewall rules (Security Groups) and network protections.
- Ensuring the security **in** the cloud through proper configuration and least privilege (principio de privilegios mínimos).

**Service Categories and Responsibilities:**
- **IaaS (e.g., EC2):** Customers manage guest OS patches, firewall rules, and app security.
- **Container/Managed Services (e.g., RDS):** AWS handles database engine patching; customers handle data, backups, and access.
- **Abstracted Services (e.g., S3):** AWS manages most infrastructure; customers configure policies, encryption, and data access controls.

[Learn More](https://aws.amazon.com/compliance/shared-responsibility-model/)

---

## How to Access AWS (¿Cómo acceder a AWS?)

**Three Methods of Access:**
1. **AWS Management Console (Consola de Administración):**
   - GUI via browser, user/password + optional MFA.
   - Ideal for initial setup, administrative and manual tasks.

2. **Command Line Interface (CLI - Interfaz de Línea de Comandos):**
   - Requires Access Keys (Claves de Acceso).
   - Enables scripting, automation, and DevOps workflows.
   - Do not embed keys in code or store on EC2. Use IAM Roles instead.

3. **Software Development Kits (SDKs - Kits de Desarrollo de Software):**
   - Integrate AWS into applications using programming languages.
   - Requires Access Keys.
   - Perfect for CI/CD pipelines and programmatic control.

**Best Practices:**
- Enable MFA for Root and privileged users.
- Rotate and audit Access Keys regularly.
- Use IAM Roles for EC2 and other services to avoid exposing credentials.

---

## Identity and Access Management (IAM - Gestión de Identidad y Acceso)

IAM is a global service that governs who can do what in your AWS account:

**Key IAM Elements:**
- **Root Account (Cuenta Raíz):**
  - Created at account setup with full privileges.
  - Do not use for daily tasks; protect with MFA.

- **IAM Users (Usuarios IAM):**
  - Represent individuals or applications.
  - Can be grouped for easier permission management.

- **IAM Groups (Grupos IAM):**
  - Collections of users sharing common permissions.
  - Attach policies at the group level to simplify administration.

- **IAM Roles (Roles IAM):**
  - Provide temporary credentials for AWS services or external identities.
  - Avoid placing Access Keys in code or on instances.

**IAM Policies:**
- JSON documents specifying Effect (Allow/Deny), Actions, Resources, and Conditions.
- Follow least privilege principles.
- Types: AWS Managed, Customer Managed, Inline policies.

**Auditing & Security Tools:**
- **AWS CloudTrail:** Logs all API activity for auditing.
- **Credential Reports & Access Advisor:** Identify unused credentials and unnecessary permissions.

**Best Practices:**
- Avoid using Root account for routine operations.
- Implement MFA, strong password policies, and rotate keys.
- Assign permissions via Groups; use IAM Roles for services.
- Regularly audit permissions and remove unused privileges.

---

## AWS Support Plans (Planes de Soporte)

Choose a support plan based on your operational needs:

1. **Basic (Básico):**
   - Free, includes documentation, whitepapers, forums.
   - Limited Trusted Advisor checks (7 checks).

2. **Developer (Desarrollador):**
   - From $29/month, email support in business hours.
   - General guidance <24h, system impaired <12h.

3. **Business (Negocios):**
   - 24/7 phone, chat, email support.
   - Full Trusted Advisor checks.
   - Production down <1h response time.

4. **Enterprise On-Ramp & Enterprise (Empresarial):**
   - Technical Account Manager (TAM) included.
   - Proactive guidance, Well-Architected reviews.
   - Critical issues <15m response (Enterprise).
   
---

## Multi-Account Strategies (Estrategias Multi Cuenta)

**AWS Organizations** centralizes governance, security, and cost management for multiple accounts:

**Key Benefits:**
- **Consolidated Billing (Facturación Consolidada):** Single invoice, volume discounts.
- **Security & Compliance:** Apply Service Control Policies (SCPs) to enforce rules and restrictions.
- **Workload Isolation:** Separate accounts for Dev, Test, Prod, or compliance requirements.
- **Cost Management:** Tag resources, align costs to projects or departments.

**Core Concepts:**
- **Master Account (Cuenta Maestra):** Central billing and governance.
- **Member Accounts (Cuentas Miembro):** Individual AWS accounts under the organization.
- **Organizational Units (OUs - Unidades Organizativas):** Group accounts logically (by team, environment).
- **SCPs:** Restrict or allow certain services or actions at the organizational level.

**Best Practices:**
- Use OUs to group accounts by function or lifecycle (e.g., Dev, Test, Prod).
- Enable CloudTrail across all accounts for centralized auditing.
- Apply SCPs for consistent compliance.
- Use multi-account strategies for isolation, scalability, and simplified billing.

---

## Summary

**Key Takeaways:**
- The Shared Responsibility Model defines who secures what: AWS secures the cloud, customers secure their configurations and data.
- Access AWS via Console, CLI, or SDKs; follow best practices like MFA and IAM Roles.
- IAM ensures fine-grained control over identity and access; implement least privilege, rotate keys, and audit permissions.
- AWS Support Plans range from Basic to Enterprise, offering increasing support and faster response times as operational complexity grows.
- Multi-account strategies with AWS Organizations streamline governance, cost management, and security controls at scale.

---
