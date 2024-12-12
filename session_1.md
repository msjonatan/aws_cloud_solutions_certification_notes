# AWS Solutions Architect Certification - Session 1

*(Note: The text is in English since the certification exam is in English. Key AWS/cloud terms are provided in Spanish (in parentheses) where it adds value for Spanish-speaking learners.)*

---

## Introduction to AWS Certifications

AWS certifications validate your cloud expertise and help you demonstrate in-demand skills. They are grouped into four categories:

1. **Foundational (Fundacional):**  
   - **AWS Certified Cloud Practitioner:** Provides fundamental AWS Cloud knowledge (conocimientos fundamentales de la nube AWS).

2. **Associate (Asociado):**  
   - **AWS Certified Solutions Architect – Associate:** Core architectural best practices on AWS.
   - **AWS Certified Developer – Associate:** Building, deploying, and maintaining AWS-based applications.
   - **AWS Certified SysOps Administrator – Associate:** Operating and managing workloads in AWS.

3. **Professional (Profesional):**  
   - **AWS Certified Solutions Architect – Professional:** Advanced skills for designing large-scale, complex architectures.
   - **AWS Certified DevOps Engineer – Professional:** Expertise in CI/CD, automation, and operations on AWS.

4. **Specialty (Especialidad):**  
   - Focused on domains such as Security (Seguridad), Analytics (Analítica), Machine Learning (Aprendizaje Automático), Databases (Bases de Datos), and Networking (Redes).

For more details, visit the [AWS Certification Official Page](https://aws.amazon.com/certification/).

### AWS Certification Paths

Two common certification paths include:

- **Architectural Path:**
  - Begin with Cloud Practitioner (Fundacional) for core cloud concepts.
  - Progress to Solutions Architect – Associate (Asociado) to learn well-architected frameworks.
  - Advance to Solutions Architect – Professional (Profesional) for complex, enterprise-scale solutions.
  - Consider a Security Specialty (Especialidad de Seguridad) to deepen secure architecture expertise.

- **Application Architecture Path:**
  - Start with Cloud Practitioner (Fundacional).
  - Move on to Developer Associate (Asociado) for application-focused development on AWS.
  - Elevate to DevOps Engineer – Professional (Profesional) for CI/CD and operational excellence.
  - Explore Database or Machine Learning Specialty (Especialidad) to specialize further.

See the [AWS Certification Paths PDF](https://d1.awsstatic.com/training-and-certification/docs/AWS_certification_paths.pdf) for more information.

---

## Session Agenda

In this first session, we cover the foundational concepts of AWS and cloud computing:

1. **Cloud Computing Overview (Descripción general de la informática en la nube)**
2. **Benefits of the Cloud (Beneficios de la nube)**
3. **Cloud Service Models: IaaS (Infraestructura como servicio), PaaS (Plataforma como servicio), SaaS (Software como servicio)**
4. **Cloud Deployment Models: Public (Nube Pública), Private (Nube Privada), Hybrid (Nube Híbrida)**
5. **Why Choose AWS? (¿Por qué AWS?)**
6. **AWS Global Infrastructure (Infraestructura global de AWS)**
7. **Setting Up an AWS Account (Creación de una cuenta AWS)**
8. **AWS Pricing Calculator and Cost Explorer (Calculadora de Precios y Explorador de Costos)**
9. **Budget Configuration (Configuración de Presupuesto)**

---

## Understanding Cloud Computing

### Traditional IT Model (Modelo Informático Tradicional)

Traditional on-premises infrastructure requires significant Capital Expenditures (CAPEX - Gastos de capital) for hardware, data center space, cooling, power, and staffing. Scaling is slow, upgrades are costly, and disaster recovery is complex.

### What is Cloud Computing?

Cloud computing is the on-demand delivery of IT resources—compute (cómputo), storage (almacenamiento), databases (bases de datos), and more—over the internet with pay-as-you-go pricing. Instead of owning physical infrastructure, you rent resources from a provider like AWS. This shifts spending from CAPEX to Operational Expenses (OPEX - Gastos operativos), improving agility and cost efficiency.

### Five Essential Characteristics of Cloud Computing

1. **On-Demand Self-Service (Auto servicio bajo demanda):** Provision resources as needed without provider intervention.
2. **Broad Network Access (Amplio acceso a la red):** Access services from anywhere, using various devices.
3. **Resource Pooling (Agrupación de recursos):** Multi-tenant architecture ensures multiple customers share resources securely.
4. **Rapid Elasticity (Elasticidad rápida):** Instantly scale resources to handle workload changes.
5. **Measured Service (Servicio medido):** Pay only for what you use, with monitored and controlled usage.

---

## Benefits of Cloud Computing (Beneficios del Cloud Computing)

1. **Trade CAPEX for OPEX:** Reduce upfront costs; pay only for what you consume.
2. **Massive Economies of Scale:** AWS’s scale lowers costs.
3. **Eliminate Guessing on Capacity:** Scale dynamically to meet demand.
4. **Speed & Agility:** Launch resources in minutes, accelerating innovation.
5. **Global Reach (Alcance global):** Deploy workloads worldwide using AWS’s global infrastructure.
6. **Focus on Business:** Let AWS handle infrastructure management, freeing you to focus on value-added activities.

---

## Cloud Service Models

1. **Infrastructure as a Service (IaaS - Infraestructura como servicio):**  
   - Example: Amazon EC2.  
   - AWS manages the underlying hardware; you control the OS, middleware, and applications.

2. **Platform as a Service (PaaS - Plataforma como servicio):**  
   - Example: AWS Elastic Beanstalk.  
   - AWS manages OS and runtime; you focus on application code deployment and management.

3. **Software as a Service (SaaS - Software como servicio):**  
   - Example: Salesforce, Dropbox.  
   - Fully managed applications delivered via the internet; no infrastructure management required.

---

## Cloud Deployment Models

1. **Public Cloud (Nube Pública):**  
   - Shared infrastructure managed by a third-party provider like AWS.
   - Pay-as-you-go pricing, high scalability, and minimal management overhead.

2. **Private Cloud (Nube Privada):**  
   - Exclusive to a single organization.  
   - Greater control and customization but higher costs and complexity.

3. **Hybrid Cloud (Nube Híbrida):**  
   - Combination of on-premises and public cloud.  
   - Ideal for phased migrations, disaster recovery, or compliance requirements.

---

## Why Choose AWS? (¿Por qué AWS?)

- **Comprehensive Services:** Over 200 fully featured services, from compute and storage to machine learning and analytics.
- **Cost Efficiency:** Economies of scale pass savings to customers.
- **Elasticity & Agility (Elasticidad y agilidad):** Scale resources instantly to meet changing demands.
- **Global Infrastructure (Infraestructura global):** Regions, Availability Zones (Zonas de disponibilidad), and Edge Locations for low latency and fault tolerance.
- **Security (Seguridad):** Mature security frameworks, encryption options, and numerous compliance certifications.
- **Openness & Flexibility:** Supports multiple programming languages, operating systems, and architectures.

---

## AWS Global Infrastructure (Infraestructura Global de AWS)

1. **Regions (Regiones):**  
   - Geographically isolated areas with multiple Availability Zones.
   - Choose regions based on latency, compliance, and service availability.

2. **Availability Zones (Zonas de disponibilidad):**  
   - Separate data centers within a region.  
   - Provide redundancy and fault tolerance.

3. **Edge Locations (Puntos de presencia):**  
   - Improve content delivery performance via AWS CloudFront.
   - Bring content closer to end users for low-latency access.

---

## Setting Up an AWS Account (Creación de una cuenta AWS)

1. **Sign Up at AWS Free Tier:** Access free allowances for various services.  
2. **Provide Billing Information:** A credit/debit card is required.  
3. **Identity Verification:** Confirm via phone.  
4. **Select Support Plan:** Basic (Básico) is free and suitable for beginners.  
5. **Launch Your First Resources:** Use the AWS Management Console to start.

---

## AWS Pricing & Cost Management

**Pricing Model:**  
- **Compute:** Pay per hour/second of usage.  
- **Storage:** Pay per GB/month.  
- **Data Transfer:** Inbound often free, outbound billed per GB.

### AWS Pricing Calculator (Calculadora de Precios AWS)
- Estimate monthly costs before deployment to avoid surprises.

### AWS Cost Explorer (Explorador de Costos)
- Visualize historical costs and usage trends.
- Filter by service, region, or tags to understand spending patterns.

### AWS Budgets (Presupuestos de AWS)
- Set cost or usage thresholds.
- Receive alerts as you approach or exceed your budget.
- Automate cost controls and plan for future spending.

### Tagging (Etiquetado)
- Assign key-value pairs to resources.
- Categorize costs by project, department, or environment.

---

## Summary

**Key Takeaways:**
- Cloud computing shifts from on-premises CAPEX investments to a flexible OPEX model, fostering agility and innovation.
- AWS certifications (Fundacional, Asociado, Profesional, Especialidad) guide you along a learning path tailored to your career goals.
- AWS’s global infrastructure (Regiones, Zonas de disponibilidad) ensures reliable, low-latency service delivery.
- Understand IaaS, PaaS, SaaS service models and Public, Private, Hybrid deployment models to choose the right architecture.
- Leverage AWS tools like the Pricing Calculator, Cost Explorer, and Budgets to manage and optimize costs.
- By embracing AWS, focus on business outcomes rather than maintaining physical infrastructure, accelerating time-to-value in the cloud.

---
