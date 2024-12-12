# AWS Solutions Architect Certification - Session 1

*Note: The following essay is in English. Official AWS certification names and certain cloud terminology are provided in parentheses with their Spanish official or widely-used translations when it adds value for Spanish-speaking learners. This approach helps readers who are familiar with Spanish IT/cloud terms to better understand concepts without losing the English context.*

---

## Introduction

Welcome to the first session of the AWS Solutions Architect training course. Today, we will begin with a broad overview of cloud computing and fundamental AWS concepts. This session sets the stage for your journey towards AWS certifications, focusing on the foundational knowledge you will need to progress through the AWS Certified Cloud Practitioner (*AWS Certificado Cloud Practitioner (Fundamentos)*), AWS Certified Solutions Architect – Associate (*AWS Certificado Arquitecto de Soluciones – Asociado*), and eventually the AWS Certified Solutions Architect – Professional (*AWS Certificado Arquitecto de Soluciones – Profesional*).

We have a structured learning environment, including a WhatsApp group and a Google Classroom, where you will register attendance and provide feedback (retroalimentación) after each session. The sessions are recorded and made available the following day, so you can review them at your convenience.

Your instructor, José, is an experienced IT professional (profesional de TI) with a background in data engineering, big data (datos masivos), analytics (análisis) and visualization, pipelines, and multiple cloud certifications (certificaciones en la nube). Throughout this course, participants were asked to introduce themselves, share their experience with AWS and other clouds, their roles, hobbies, and what they hope to gain from the course. This collaborative approach ensures we understand the group’s background and goals, making the learning experience more effective.

---

## The AWS Certification Landscape

AWS certifications are categorized by difficulty and specialization:

1. **Foundational (Fundacional)**:
   - **AWS Certified Cloud Practitioner (AWS Certificado Cloud Practitioner (Fundamentos))**:  
     A starting point for learners new to the AWS Cloud, covering basic terminology, global infrastructure, pricing, and fundamental services.

2. **Associate (Asociado)**:
   - **AWS Certified Solutions Architect – Associate (AWS Certificado Arquitecto de Soluciones – Asociado)**:  
     Validates the ability to design secure, cost-optimized, and highly available architectures on AWS.
   - **AWS Certified Developer – Associate (AWS Certificado Desarrollador – Asociado)**:  
     Focuses on development and maintenance of applications on AWS.
   - **AWS Certified SysOps Administrator – Associate (AWS Certificado Administrador SysOps – Asociado)**:  
     Concentrates on managing and operating AWS workloads.

3. **Professional (Profesional)**:
   - **AWS Certified Solutions Architect – Professional (AWS Certificado Arquitecto de Soluciones – Profesional)**:
     Validates advanced technical skills and experience in designing distributed systems and complex architectures on AWS.
   - **AWS Certified DevOps Engineer – Professional (AWS Certificado Ingeniero DevOps – Profesional)**:
     Emphasizes continuous integration/continuous delivery (CI/CD), infrastructure as code (infraestructura como código), and efficient operations at scale.

4. **Specialty (Especialidad)**:
   - Examples include Security, Networking, Databases, Analytics, and Machine Learning.
   - For instance, **AWS Certified Security – Specialty (AWS Certificado en Seguridad – Especialidad)**.
   
No prior certification is strictly required before moving to a more advanced level. However, foundational and associate-level certifications build essential skills and context, making advanced certifications more approachable.

**Certification Maintenance:**  
Certifications are valid for three years. Achieving a higher-level certification (for example, obtaining the Professional level after the Associate) automatically renews the lower-level ones. Exam questions typically involve scenario-based problem-solving, not just theoretical knowledge, so gaining hands-on practice and using practice tests is crucial.

---

## Cloud Computing Fundamentals

### From Traditional IT to the Cloud

In a traditional IT environment (entorno de TI tradicional), organizations maintain their own data centers (centros de datos), incurring large capital expenses (CAPEX) for servers, storage, networking, physical security, and staff. Upgrades and scaling require extensive planning and provisioning times, and disaster recovery (recuperación ante desastres) can be expensive and complex.

**Cloud computing (informática en la nube)** shifts this model to on-demand, pay-as-you-go (pago por uso) operational expenses (OPEX). Instead of guessing capacity and paying upfront, you scale elastically as needed. AWS handles the undifferentiated heavy lifting of data center operations, freeing you to focus on adding business value.

### Characteristics and Benefits

**Key Characteristics:**
- On-Demand Self-Service (autoservicio bajo demanda)
- Broad Network Access (acceso a la red amplio)
- Resource Pooling (agrupación de recursos)
- Rapid Elasticity (elasticidad rápida)
- Measured Service (servicio medido)

**Key Benefits:**
- Convert CAPEX to OPEX.
- Benefit from economies of scale.
- Scale on demand, no need to overprovision.
- Increase speed, deploy resources in minutes.
- Reduce costs by removing the overhead of maintaining data centers.
- Achieve global reach easily by deploying applications in multiple AWS Regions (Regiones).

---

## Cloud Service Models and Deployment Models

**Service Models:**
- **Infrastructure as a Service (IaaS)**: Example – Amazon EC2  
  You manage OS and applications; AWS manages the underlying hardware.
- **Platform as a Service (PaaS)**: Example – AWS Elastic Beanstalk  
  Focus on code; AWS handles infrastructure provisioning and management.
- **Software as a Service (SaaS)**: Example – Salesforce  
  Fully managed application accessible over the internet.

**Deployment Models:**
- **Public Cloud (Nube Pública)**: Shared infrastructure, hosted by providers like AWS.
- **Private Cloud (Nube Privada)**: Dedicated infrastructure for a single organization.
- **Hybrid Cloud (Nube Híbrida)**: Combination of public and private for greater flexibility.

---

## Why AWS?

AWS leads the cloud market with a global footprint of Regions and Availability Zones (Zonas de Disponibilidad), offering unmatched breadth and depth of services. Customers choose AWS for:

- **Cost Efficiency:** Pay only for what you use.
- **Elasticity & Agility:** Scale quickly as demand changes.
- **Global Infrastructure (Infraestructura Global):** Lower latency, better fault tolerance, regional compliance.
- **Security & Compliance:** Broad security features, certifications, and encryption.

---

## AWS Global Infrastructure

AWS Regions are geographically separate areas, each containing multiple Availability Zones. Distributing applications across multiple AZs enhances high availability (alta disponibilidad) and fault tolerance (tolerancia a fallos). Edge locations (puntos de presencia) improve latency for content delivery.

When choosing a Region, consider compliance requirements, service availability, cost differences, and latency.

---

## Getting Started: AWS Account and Free Tier

**Creating an AWS Account:**
1. Visit the [AWS Free Tier](https://aws.amazon.com/free/) page.
2. Provide an email, password, and billing details.
3. Verify identity with a phone number.
4. Select a support plan; basic (básico) support is free.
5. Access the console and start exploring AWS services.

The AWS Free Tier offers limited free usage of popular services for 12 months, making it easier to practice and avoid unexpected costs. Always monitor usage to stay within free limits.

---

## Cost Management: AWS Pricing, Cost Explorer, and Budgets

**AWS Pricing Model:**
- Compute, storage, and data transfer costs vary by usage.
- Inbound data transfer is usually free; outbound data costs apply.

**Tools:**
- **AWS Pricing Calculator:** Estimate costs before deployment.
- **AWS Cost Explorer:** Visualize spending over time, identify trends, and drill down by service, region, or tag.
- **AWS Budgets (Presupuestos de AWS):**  
  Set spending limits, receive alerts when you approach or exceed thresholds, and even automate actions if overspending is forecasted.

**Tagging Resources (Etiquetado de Recursos):**
Tags help organize resources by project, department, or environment (entorno). They also simplify cost allocation in Cost Explorer.

---
