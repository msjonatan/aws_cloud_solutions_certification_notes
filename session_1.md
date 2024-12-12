# AWS Solutions Architect Certification - Session 1

*(Note: The text is in English since the certification exam is in English. However, key cloud and AWS terms will include their Spanish equivalents in parentheses where it adds value, especially if you are familiar with Spanish IT/cloud terminology.)*

---

## Introduction to AWS Certifications

AWS certifications validate your cloud expertise, enabling you to highlight in-demand skills. They are categorized into four levels:

1. **Foundational (Fundacional):**  
   - **AWS Certified Cloud Practitioner:** Establishes fundamental AWS Cloud knowledge (conocimientos fundamentales de la nube AWS).

2. **Associate (Asociado):**  
   - **AWS Certified Solutions Architect – Associate:** Core architectural best practices on AWS.
   - **AWS Certified Developer – Associate:** Building and maintaining AWS-based applications.
   - **AWS Certified SysOps Administrator – Associate:** Operating and managing AWS workloads.

3. **Professional (Profesional):**  
   - **AWS Certified Solutions Architect – Professional:** Advanced skills for complex, large-scale AWS architectures.
   - **AWS Certified DevOps Engineer – Professional:** Expert in CI/CD, automation, and operations in the cloud.

4. **Specialty (Especialidad):**  
   - Certifications focus on areas like Security (Seguridad), Analytics (Analítica), Machine Learning (Aprendizaje Automático), Databases (Bases de Datos), Networking (Redes).

For more details, visit the [AWS Certification Official Page](https://aws.amazon.com/certification/).

---

## AWS Certification Paths

Two common paths include:

1. **Architectural Path:**
   - Start with Cloud Practitioner (Fundacional) for core cloud knowledge.
   - Move on to Solutions Architect – Associate (Asociado) to design well-architected systems.
   - Progress to Solutions Architect – Professional (Profesional) for advanced architectures.
   - Add a Security Specialty (Especialidad de Seguridad) for deeper expertise in secure architectures.

2. **Application Architecture Path:**
   - Begin with Cloud Practitioner (Fundacional).
   - Advance to Developer Associate (Asociado) for application-centric AWS usage.
   - Move to DevOps Engineer – Professional (Profesional) to master CI/CD, deployment, and operations.
   - Consider Database or Machine Learning Specialty (Especialidad) certifications for domain-specific expertise.

See the [AWS Certification Paths PDF](https://d1.awsstatic.com/training-and-certification/docs/AWS_certification_paths.pdf) for more information.

---

## Session Agenda

Today’s session covers:

1. Cloud Computing Overview (Descripción general de la informática en la nube)
2. Benefits of the Cloud (Beneficios de la nube)
3. Cloud Service Models: IaaS (Infraestructura como servicio), PaaS (Plataforma como servicio), SaaS (Software como servicio)
4. Cloud Deployment Models: Public (Nube pública), Private (Nube privada), Hybrid (Nube híbrida)
5. Why Choose AWS? (¿Por qué AWS?)
6. AWS Global Infrastructure (Infraestructura global de AWS)
7. Setting Up an AWS Account (Creación de una cuenta AWS)
8. AWS Pricing Calculator and Cost Explorer (Calculadora de precios y Explorador de costos)
9. Budget Configuration (Configuración de presupuesto)

---

## Understanding Cloud Computing

### Traditional IT Model (Modelo Informático Tradicional)

On-premises (en las instalaciones) infrastructure involves high Capital Expenditures (CAPEX - Gastos de capital) for servers, networking, cooling, power, and security. Scaling is slow, upgrades are costly, and disaster recovery planning is complex.

### What is Cloud Computing?

Cloud computing provides on-demand delivery of compute (cómputo), storage (almacenamiento), databases (bases de datos), and other IT resources over the internet, paying only for what you use. It transforms infrastructure from a CAPEX model to an Operational Expense (OPEX - Gastos operativos) model, enhancing agility and cost efficiency.

### Five Essential Characteristics of Cloud Computing

1. **On-Demand Self-Service (Auto servicio bajo demanda):** Provision resources as needed without manual intervention.
2. **Broad Network Access (Amplio acceso a la red):** Access services from anywhere, via various devices.
3. **Resource Pooling (Agrupación de recursos):** Multi-tenant environment with secure isolation.
4. **Rapid Elasticity (Elasticidad rápida):** Scale resources up or down quickly based on demand.
5. **Measured Service (Servicio medido):** Pay only for your actual resource usage.

---

## Benefits of Cloud Computing (Beneficios del Cloud Computing)

1. **From CAPEX to OPEX:** Lower upfront costs and pay as you go.
2. **Economies of Scale:** AWS’s large scale reduces costs.
3. **Stop Guessing Capacity:** Scale according to actual usage.
4. **Speed & Agility:** Launch servers within minutes.
5. **Global Reach (Alcance global):** Deploy worldwide instantly.
6. **Focus on Business:** Let AWS handle data center maintenance.

---

## Cloud Service Models

- **IaaS (Infraestructura como servicio):** e.g., Amazon EC2. You manage the OS and above; AWS manages the underlying hardware.
- **PaaS (Plataforma como servicio):** e.g., AWS Elastic Beanstalk. AWS manages OS and runtime; you focus on your application code.
- **SaaS (Software como servicio):** e.g., Salesforce, Dropbox. Fully managed software delivered over the internet.

---

## Cloud Deployment Models

- **Public Cloud (Nube Pública):** Shared infrastructure, hosted by a provider like AWS.
- **Private Cloud (Nube Privada):** Dedicated environment for a single organization.
- **Hybrid Cloud (Nube Híbrida):** Mix of public and private, balancing control and flexibility.

---

## Why Choose AWS? (¿Por qué AWS?)

- **Comprehensive Services:** 200+ fully featured services.
- **Cost-Efficiency:** Benefit from AWS’s scale.
- **Elasticity & Agility (Elasticidad y agilidad):** Scale instantly.
- **Global Infrastructure (Infraestructura global):** Regions, Availability Zones (Zonas de disponibilidad), and Edge Locations.
- **Security (Seguridad):** Strong compliance frameworks.
- **Openness & Flexibility:** Choose languages, frameworks, and architectures.

---

## AWS Global Infrastructure (Infraestructura Global de AWS)

- **Regions (Regiones):** Geographically isolated locations, each with multiple Availability Zones (Zonas de disponibilidad).
- **Availability Zones (Zonas de disponibilidad):** Discrete data centers with redundant power and networking.
- **Edge Locations (Puntos de presencia):** Improve content delivery latency using services like Amazon CloudFront.

**Considerations:**  
Choose a region based on latency, compliance, and services needed. Deploy across multiple AZs for fault tolerance. Use Edge Locations to lower latency for end-users.

---

## Setting Up an AWS Account (Creación de una cuenta AWS)

1. **Sign Up at AWS Free Tier:** Access services with free allowances.
2. **Provide Billing Information:** Credit/debit card required.
3. **Identity Verification:** Enter a phone number for confirmation.
4. **Select Support Plan:** Basic (Básico) is free and sufficient for learning.
5. **Get Started:** Launch your first services via the AWS Management Console.

---

## AWS Pricing & Cost Management

**Pricing Model:**  
- Compute: Pay per CPU time.  
- Storage: Pay per GB/month.  
- Data Transfer: Inbound often free, outbound billed per GB.

### AWS Pricing Calculator (Calculadora de Precios AWS)
- Estimate monthly costs before deployment.

### AWS Cost Explorer (Explorador de Costos)
- Track and visualize costs over time.
- Identify trends, filter by service, region, or tags.

### AWS Budgets (Presupuestos de AWS)
- Set spending or usage thresholds.
- Receive alerts when approaching or exceeding budgets.
- Forecast future usage and automate cost-control actions.

### Tagging (Etiquetado)
- Assign key-value pairs to resources.
- Filter costs by tags to understand spending at project or department level.

---

## Summary

**Key Takeaways:**
- Cloud computing shifts from costly, inflexible on-premises infrastructures to scalable, pay-as-you-go models.
- AWS certifications (Fundacional, Asociado, Profesional, Especialidad) guide your learning path.
- AWS provides global infrastructure (Regiones, Zonas de disponibilidad) ensuring low latency and high availability.
- Service models (IaaS, PaaS, SaaS) and deployment models (Nube Pública, Nube Privada, Nube Híbrida) address diverse needs.
- Manage costs using tools like the AWS Pricing Calculator, Cost Explorer, and Budgets.

---
