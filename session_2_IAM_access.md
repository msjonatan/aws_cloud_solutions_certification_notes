# AWS Solutions Architect Certification – Session 2

*(Note: The text is in English, as the certification exam is in English. Key AWS/cloud terms are provided in Spanish (in parentheses) where helpful for those familiar with Spanish terminology.)*

---

## Introduction

In this second session, we focus on identity, access, and governance in the AWS Cloud. We will explore the Shared Responsibility Model, methods of accessing AWS, Identity and Access Management (IAM), AWS support plans, and multi-account strategies. Understanding these concepts is critical for designing secure, compliant, and well-governed architectures on AWS.

**Topics Covered:**
1. Shared Responsibility Model (Modelo de Responsabilidad Compartida)
2. How to Access AWS
3. Identity and Access Management (Gestión de Identidad y Acceso - IAM)
4. AWS Support Plans (Planes de Soporte AWS)
5. Multi-Account Strategies (Estrategias Multi Cuenta)

---

## Shared Responsibility Model (Modelo de Responsabilidad Compartida)

AWS cloud security is a shared responsibility between AWS and the customer. This model delineates which components are managed by AWS and which remain the customer’s responsibility.

- **AWS Responsibilities:**  
  AWS is responsible for the security **of** the cloud. This includes:
  - Physical security of data centers (centros de datos).
  - Underlying infrastructure: Compute, storage, database, and networking resources.
  - Global and regional infrastructure, hardware, and managed services.

- **Customer Responsibilities:**  
  Customers are responsible for security **in** the cloud. This includes:
  - Configuring services securely (secure configurations).
  - Managing data, user access, encryption keys (claves de cifrado), and application-level security.
  - Ensuring that IAM policies and firewall rules meet organizational requirements.
  - Implementing data encryption and securing network traffic.

**Service Categories and Responsibilities:**
- **Infrastructure Services:** (e.g., Amazon EC2)  
  Customers manage operating systems, patches, application code, and security groups.
- **Container Services:** (e.g., Amazon RDS)  
  AWS manages the underlying platform, while customers handle application logic, data, and user access.
- **Abstracted Services:** (e.g., Amazon S3)  
  AWS handles most infrastructure tasks; customers focus on data protection, access policies, and compliance settings.

[Learn more about the Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)

---

## How to Access AWS

There are three primary ways to interact with AWS services:

1. **AWS Management Console (Consola de Administración de AWS):**  
   A web-based graphical interface.  
   - Authenticate with a username, password, and optionally MFA (Autenticación Multifactor).
   - Ideal for manual operations, initial set-up, and administrative tasks.

2. **Command Line Interface (CLI - Interfaz de Línea de Comandos):**  
   Text-based commands to manage and script operations on AWS.  
   - Requires Access Keys (Claves de Acceso) and secret keys.
   - Useful for automation, scripting, DevOps workflows.

3. **Software Development Kits (SDKs - Kits de Desarrollo de Software):**  
   Integrate AWS directly into applications using programming languages.  
   - Requires Access Keys.
   - Enables programmatic control of AWS resources.

**Security Guidelines for Access:**
- Never embed Access Keys in code repositories.
- Rotate keys regularly.
- Use MFA for the AWS root account and privileged users.

---

## Identity and Access Management (IAM)

**IAM (Gestión de Identidad y Acceso)** is a global AWS service that controls who can access what:

1. **Authenticate (Autenticar):**  
   Credentials such as user/password, Access Keys, or MFA devices ensure the right person logs in.
   
2. **Authorize (Autorizar):**  
   IAM Policies (Políticas IAM) define which AWS actions and resources a user, group, or role can access.
   - Policies are JSON documents specifying `Effect`, `Action`, `Resource`, and `Condition`.
   - Follow the principle of least privilege (principio de privilegios mínimos).

3. **Audit (Auditar):**  
   Use AWS CloudTrail to record and track all API calls, changes, and activities in your AWS environment.
   This provides transparency and traceability for compliance and security investigations.

**Key IAM Concepts:**
- **Root Account (Cuenta root):**  
  The account owner’s initial credentials with unrestricted access.  
  - Should not be used for day-to-day operations; secure it with MFA.
  
- **IAM Users (Usuarios IAM):**  
  Individual named entities that represent people or applications.
  - Can belong to zero or multiple IAM groups.

- **IAM Groups (Grupos IAM):**  
  Collections of users sharing common permissions.  
  - Groups cannot contain other groups, just users.

- **IAM Roles (Roles IAM):**  
  Similar to users but for AWS services or external entities.  
  - Assigned temporary credentials, enabling services like EC2 instances or Lambda functions to interact with other AWS resources without embedding keys.

**IAM Security Tools:**
- **IAM Credentials Report (Informe de Credenciales IAM):** Account-level report listing all users, status of their credentials.
- **IAM Access Advisor (Asesor de Acceso):** Shows which services a user has accessed and when.

**Best Practices:**
- Activate MFA (Multi-Factor Authentication) on the root account.
- Grant least privilege: give only the permissions users need.
- Use Roles for services and applications.
- Regularly rotate keys and review policies.

---

## AWS Support Plans (Planes de Soporte AWS)

AWS offers different support tiers to meet varying customer needs:

1. **Basic (Básico):**  
   Free, includes documentation, whitepapers, and access to community forums.  
   Basic Trusted Advisor checks for security and performance recommendations.

2. **Developer (Desarrollador):**  
   Starting at $29/month, provides email support during business hours.  
   Ideal for testing or early-stage development.

3. **Business (Negocios):**  
   24/7 email, chat, and phone support from AWS support engineers.  
   Full Trusted Advisor checks and a response time as low as 1 hour for critical issues.

4. **Enterprise (Empresarial):**  
   Dedicated Technical Account Manager (TAM) and solutions architect guidance.  
   15-minute response time for critical issues.  
   Ideal for large enterprises with mission-critical workloads.

---

## Multi-Account Strategies (Estrategias Multi Cuenta)

As organizations grow, managing multiple AWS accounts under a single umbrella improves security, governance, and cost optimization.

**Benefits:**
- **Consolidated Billing (Facturación Consolidada):**  
  Combine charges across accounts for a single bill.
  
- **Security and Isolation:**  
  Separate sensitive workloads into distinct accounts, reducing blast radius and simplifying compliance.

- **Organizational Units (OUs - Unidades Organizativas):**  
  Group accounts by function, department, or environment (dev, test, prod).

- **AWS Organizations:**  
  A global service that helps manage multiple AWS accounts centrally.  
  - Control policies, apply service control policies (SCPs) to enforce organizational governance.
  - Consolidate billing and gain volume discounts.

- **Cost Allocation Tags (Etiquetas de asignación de costos):**
  Tag resources and accounts for granular cost tracking and reporting.

**Best Practices:**
- Use AWS Organizations for centralized governance.
- Align accounts and OUs with operational or compliance requirements.
- Enable AWS CloudTrail in all accounts and centralize logs for auditing.
- Use cross-account roles and least-privilege access to maintain security boundaries.

---

## Summary

**Key Takeaways:**
- The Shared Responsibility Model clarifies that AWS secures the underlying infrastructure, while customers secure their data and applications.
- Multiple access methods (Console, CLI, SDK) provide flexibility in managing AWS resources, but must be secured properly.
- IAM is crucial for controlling access, enforcing least privilege, and auditing activity via CloudTrail.
- AWS Support Plans range from Basic (Básico) to Enterprise (Empresarial), offering different levels of assistance and guidance.
- Multi-account strategies and AWS Organizations improve security, compliance, cost management, and operational efficiency at scale.

---
