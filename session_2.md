# AWS Solutions Architect Certification – Session 2

*(Note: Text is in English, as the exam is in English. Key AWS/cloud terms are provided in Spanish (in parentheses) where helpful to those familiar with Spanish terminology.)*

---

## Introduction

In this second session, we focus on identity management, access control, governance, and multi-account strategies in AWS. These concepts are critical for building secure, compliant, and easily managed cloud architectures. We will cover the Shared Responsibility Model, methods of accessing AWS, the Identity and Access Management (IAM) service, AWS support plans, and multi-account strategies via AWS Organizations.

**Topics Covered:**
1. Shared Responsibility Model (Modelo de Responsabilidad Compartida)
2. How to Access AWS (¿Cómo acceder a AWS?)
3. Identity and Access Management (IAM - Gestión de Identidad y Acceso)
4. AWS Support Plans (Planes de Soporte)
5. Multi-Account Strategies (Estrategias Multi Cuenta)

---

## Shared Responsibility Model (Modelo de Responsabilidad Compartida)

**AWS Responsibilities (Seguridad de la Nube):**
- Physical security of data centers (centros de datos).
- Maintaining and securing the underlying global infrastructure: Compute, Storage, Networking, Databases.
- Managing host operating systems, virtualization, and hardware components.

**Customer Responsibilities (Seguridad en la Nube):**
- Configuring and securing systems, applications, and data.
- Encrypting data (encriptación de datos) in transit and at rest.
- Managing IAM policies, firewall rules (grupos de seguridad), and network traffic protection.
- Ensuring the principle of least privilege (principio de privilegios mínimos) for all identities.

The level of responsibility varies depending on the service category:

- **Infrastructure Services (e.g., Amazon EC2):**  
  Customers manage OS patches, firewall rules, and application-level security.
- **Container Services (e.g., Amazon RDS):**  
  AWS patches and manages the database engine, customers handle data, users, and encryption.
- **Abstracted Services (e.g., Amazon S3):**  
  AWS manages most infrastructure, customers secure their data and control access policies.

[Learn more about Shared Responsibility](https://aws.amazon.com/compliance/shared-responsibility-model/)

---

## How to Access AWS (¿Cómo acceder a AWS?)

**Access Methods:**
1. **AWS Management Console (Consola de Administración):**  
   - Web interface using username/password and optional MFA (Multi-Factor Authentication - Autenticación Multifactor).
   - Ideal for initial setup, administrative tasks, and manual configuration.

2. **Command Line Interface (CLI - Interfaz de Línea de Comandos):**  
   - Uses Access Keys (Claves de Acceso) for authentication.
   - Enables scripting, automation, and DevOps workflows.
   - Directly calls AWS APIs.

3. **Software Development Kits (SDKs - Kits de Desarrollo de Software):**  
   - Programmatically interact with AWS services using your preferred programming language.
   - Requires Access Keys.
   - Integrates AWS into applications, CI/CD pipelines, and custom tools.

**Best Practices:**
- Enable MFA for root and privileged users.
- Do not store Access Keys in source code or on EC2 instances directly.
- Consider using IAM Roles for AWS services to avoid embedding credentials.

---

## Identity and Access Management (IAM - Gestión de Identidad y Acceso)

**IAM** is a global AWS service that governs authentication, authorization, and auditing across your AWS account.

1. **Authenticate (Autenticar):**
   - Use usernames, passwords, Access Keys, and optionally MFA.
   - Federation (Federación) can allow external identities (e.g., Active Directory, social logins).

2. **Authorize (Autorizar):**
   - IAM Policies (Políticas IAM) define which actions (Acciones) and resources (Recursos) a user, group, or role can access.
   - Policies are JSON documents specifying Effect (Allow/Deny), Actions, Resources, and optional Conditions.
   - Apply the principle of least privilege.

3. **Audit (Auditar):**
   - AWS CloudTrail logs all API calls for transparency and investigation.
   - IAM Credential Reports and Access Advisor help review current permissions and usage.

**IAM Key Concepts:**
- **Root Account (Cuenta Raíz):**  
  Created when you first sign up. Has unrestricted access.  
  Do not use for daily tasks; secure it with MFA.

- **IAM Users (Usuarios IAM):**  
  Represent individuals or applications. Can belong to groups.

- **IAM Groups (Grupos IAM):**  
  Collections of users sharing common permissions. Easier to manage at scale.

- **IAM Roles (Roles IAM):**  
  Used for granting temporary access to services (e.g., EC2 instances, Lambda functions) or external identities, without sharing Access Keys.

**Best Practices:**
- Do not use the Root account for routine operations.
- Use IAM users and groups for organization-wide roles and permissions.
- Enforce MFA, strong password policies, and least privilege.
- Use IAM Roles for AWS services instead of Access Keys.
- Regularly audit permissions using Credential Reports and Access Advisor.

---

## AWS Support Plans (Planes de Soporte de AWS)

AWS offers multiple support plans to cater to different needs:

1. **Basic (Básico):**  
   - Free; includes AWS documentation, whitepapers, community forums.
   - Basic Trusted Advisor checks (limited set).
   - AWS Personal Health Dashboard for personalized alerts.

2. **Developer (Desarrollador):**  
   - Starts at $29/month.
   - Email support during business hours.
   - General guidance <24h, system impaired <12h response times.

3. **Business (Negocios):**  
   - 24/7 phone, chat, and email support.
   - Full Trusted Advisor checks.
   - Production system down <1h response time.

4. **Enterprise (Empresarial) & Enterprise on-Ramp:**  
   - Designated Technical Account Manager (TAM).
   - Comprehensive architectural reviews and proactive guidance.
   - Critical issues <15m response time (Enterprise).

---

## Multi-Account Strategies (Estrategias Multi Cuenta)

As organizations grow, they often require multiple AWS accounts. Using **AWS Organizations** helps centralize governance, security, and cost management across accounts:

**Key Benefits:**
- **Consolidated Billing (Facturación Consolidada):**  
  Aggregate charges for all accounts into a single bill.

- **Volume Discounts (Descuentos por volumen):**  
  Combine usage from multiple accounts to reach higher-volume discounts (e.g., S3 tiered pricing).

- **Separation of Environments and Workloads:**  
  Create separate accounts for Dev, Test, and Prod, or by department, cost center, or compliance requirements.

- **Central Governance:**  
  Apply Service Control Policies (SCPs) at an organizational level to limit capabilities across all child accounts, even restricting root users in those accounts.

**AWS Organizations:**
- **Root Organizational Unit (Unidad Organizativa Root):**  
  The top-level container for all your AWS accounts and OUs.
  
- **Master Account (Cuenta Maestra):**  
  The primary account that creates the organization. It pays the bills and can control other accounts’ policies.
  
- **Member Accounts (Cuentas Miembro):**  
  Additional accounts invited or created within the organization.
  
- **Organizational Units (Unidades Organizativas - OUs):**  
  Group accounts logically (by business unit, environment, or compliance).  
  Apply SCPs for fine-grained control.

**Best Practices:**
- Use one master account for billing and governance.
- Create OUs for different teams, projects, or environments.
- Enable AWS CloudTrail in all accounts and centralize logs for auditing.
- Tag resources consistently for cost allocation and reporting.
- Use SCPs to enforce organization-wide rules.

---

## Summary

**Key Takeaways:**
- The Shared Responsibility Model clarifies what AWS and customers each secure.
- Access AWS via Console, CLI, or SDKs; secure credentials and prefer IAM Roles over Access Keys.
- IAM manages users, groups, policies, and roles—fundamental for secure and least-privilege architectures.
- AWS Support Plans range from Basic to Enterprise, offering increasing support and guidance.
- Multi-account strategies with AWS Organizations provide centralized governance, cost optimization, and security at scale.

---
