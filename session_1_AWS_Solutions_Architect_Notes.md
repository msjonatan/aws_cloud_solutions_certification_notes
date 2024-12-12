# Session 1 - AWS Solutions Architect Certification (Certificación de Arquitectura de Soluciones en AWS)

## Certifications (Certificaciones)

- **Cloud Practitioner (Básico)**
- **Solutions Architect - Associate (Associate)**
  - 65 questions: 50 affect the score, 15 do not.
- **Solutions Architect - Professional (Professional)**
  - 75 questions: 60 affect the score, 15 do not.

---

## Cloud Computing Overview (Descripción General de la Informática en la Nube)

### Traditional IT Model (Modelo Informático Tradicional)

- **Resources as Capital Expenses (CAPEX):**
  - Planning
  - Space
  - Installation
  - Personnel
  - Physical Security
  - Resource capacity prediction
  - Maintenance
- **Challenges:**
  - High cost of renting data centers.
  - Power, cooling, and maintenance expenses.
  - Hardware upgrades are time-consuming.
  - Limited scalability.
  - 24/7 monitoring team required.
  - Disaster recovery complexities.

### Cloud Computing Model (Modelo Informático en la Nube)

- **Resources as Operational Expenses (OPEX):**
  - Flexibility
  - Low initial costs
  - Pay only for what you use
  - Scale resources in minutes
  - Agility
- **Five Characteristics of Cloud Computing:**
  1. **On-Demand Self-Service (Auto servicio bajo demanda):**
     - Users can provision resources without human interaction.
  2. **Broad Network Access (Amplio acceso a la red):**
     - Accessible via multiple client platforms.
  3. **Multi-Tenancy & Resource Pooling (Multiinquilino y agrupación de recursos):**
     - Shared infrastructure with privacy and security.
  4. **Rapid Elasticity (Elasticidad rápida):**
     - Automatic scaling based on demand.
  5. **Measured Service (Servicio medido):**
     - Pay-as-you-go model with accurate metering.

### What is Cloud Computing? (¿Qué es Cloud Computing?)

**Cloud Computing** is the on-demand delivery of computing power, databases, storage, applications, and other IT resources via the internet, using a **pay-as-you-go pricing model**. It enables viewing and using infrastructure as software rather than hardware.

### Benefits (Beneficios):

1. **CAPEX to OPEX:**
   - Avoid owning hardware.
   - Reduce Total Cost of Ownership (TCO).
2. **Economies of Scale:**
   - Lower costs due to AWS's efficiency and scale.
3. **Stop Guessing Capacity:**
   - Scale up or down based on demand.
4. **Increase Speed and Agility:**
   - Deploy resources in minutes.
5. **Global Reach:**
   - Utilize AWS's global infrastructure.
6. **Focus on Business Growth:**
   - Stop spending on data center management.

---

## Cloud Service Models (Modelos de Servicio Cloud)

### IaaS (Infrastructure as a Service)
- Example: **Amazon EC2 (Elastic Compute Cloud)**
- Provides:
  - Virtual servers (VMs)
  - Storage and network components
  - Full control over infrastructure

### PaaS (Platform as a Service)
- Example: **AWS Elastic Beanstalk**
- Provides:
  - Runtime environments for applications.
  - Automatic scaling, load balancing, and health monitoring.

### SaaS (Software as a Service)
- Examples:
  - Google Workspace
  - Salesforce
  - Dropbox

---

## Cloud Deployment Models (Modelos de Despliegue en la Nube)

1. **Public Cloud (Nube Pública):**
   - Resources shared among multiple clients.
   - Fully managed by a third-party provider (e.g., AWS).
2. **Private Cloud (Nube Privada):**
   - Exclusive to one organization.
   - Managed internally or by a third party.
3. **Hybrid Cloud (Nube Híbrida):**
   - Combines public and private clouds.
   - Allows for data sharing and scalability.

---

## Why AWS? (¿Por qué AWS?)

### AWS Overview (Visión General de AWS):

- **World's most widely adopted cloud platform**.
- Over 200 fully featured services.
- **Benefits:**
  - Low cost
  - Elastic and agile
  - Secure
  - Global reach
  - Open and flexible

### Pricing Model (Modelo de Precios):

1. **Compute:** Pay for the compute time.
2. **Storage:** Pay for the amount of data stored.
3. **Data Transfer:** Inbound is free; outbound has associated costs.

---

## AWS Global Infrastructure (Infraestructura Global de AWS)

### Key Components:

1. **Regions:** Geographical areas with multiple Availability Zones.
2. **Availability Zones (AZs):** Physically separate data centers within a region.
3. **Edge Locations:** CDN endpoints for low-latency content delivery.
4. **Regional Edge Caches:** Enhance performance for frequently accessed content.

### Benefits:
- Low latency
- High fault tolerance
- Legal compliance and data residency options

---

## Setting Up an AWS Account (Creación de Cuenta)

### Steps:

1. Visit [AWS Signup Page](https://aws.amazon.com/free/).
2. Provide email and billing information.
3. Select a support plan (Free Tier recommended for starters).

---

## AWS Pricing Calculator and Cost Explorer (Calculadora de Precios y Explorador de Costos)

- **AWS Pricing Calculator (Calculadora de Precios):**
  - Tool to estimate the costs of AWS services.
  - URL: [AWS Pricing Calculator](https://calculator.aws/#/).
- **AWS Cost Explorer (Explorador de Costos):**
  - Analyzes and tracks usage and spending.

---

## Setting Budgets (Configuración de Presupuesto)

### AWS Budgets:

- Allows you to:
  - Set custom usage and cost limits.
  - Receive alerts when thresholds are exceeded.

### Steps:

1. Go to the **Budgets Dashboard** in the AWS Management Console.
2. Create a new budget by specifying:
   - **Type:** Cost, Usage, or Reservation.
   - **Thresholds:** Define alert limits.
   - **Recipients:** Who receives alerts.
3. Monitor your budget in real-time.

---

### Notes:
- These notes align with the AWS Solutions Architect Certification syllabus and session objectives.
- Terminology is provided in both English and Spanish for clarity and exam preparation.
