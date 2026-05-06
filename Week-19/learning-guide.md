# Week 19 Learning Guide: Cloud and AI Security Governance

## What You Will Learn This Week

The cloud has fundamentally changed GRC. Controls that once meant physical servers in a locked data centre now mean IAM policies, security groups, and compliance configurations in AWS, Azure, or GCP. And AI is creating an entirely new risk category — algorithmic bias, AI hallucination in critical systems, data poisoning, and regulatory uncertainty around automated decision-making. This week you learn to apply GRC to cloud-native environments and build governance frameworks for AI — two skills that are in explosive demand and represent the cutting edge of the GRC profession.

---

## Section 1: Core Concept Explained

### What Is Cloud GRC?

Cloud GRC is the application of governance, risk management, and compliance disciplines to cloud infrastructure and services. The fundamental difference from traditional GRC is the **shared responsibility model** — the division of security responsibilities between the cloud provider and the customer.

**The AWS Shared Responsibility Model:**
- **AWS is responsible FOR the cloud**: Security of the physical data centres, hardware, hypervisor, networking infrastructure, managed service software.
- **The customer is responsible IN the cloud**: Operating system security, application security, data encryption, IAM configuration, network security groups, compliance configuration.

This means a GRC professional assessing a cloud-hosted company cannot just review ISO 27001 A.7 (Physical Security) and conclude it's covered by AWS. They must understand: what does AWS cover? What must the customer configure themselves? What evidence does AWS provide (via their SOC 2 reports, ISO 27001 certificates) and what evidence must the customer produce?

**Cloud GRC key domains:**
- **Identity and Access Management (IAM)**: Cloud IAM is the primary access control mechanism. Overly permissive IAM policies are the leading cause of cloud security incidents.
- **Data Security**: Encryption at rest and in transit; key management; data classification in cloud storage.
- **Network Security**: VPC design, security groups, NACLs, WAF configuration.
- **Compliance Configuration**: AWS Config, Azure Policy, GCP Security Command Center — automated compliance checks.
- **Cloud Security Posture Management (CSPM)**: Tools (Wiz, Prisma Cloud, Orca) that continuously scan cloud environments for misconfigurations.
- **Supply Chain**: Third-party integrations; serverless dependencies; container image security.

### What Is AI Governance?

AI Governance is the framework of policies, processes, and controls that organisations implement to ensure AI systems are developed, deployed, and operated in ways that are ethical, accountable, transparent, and legally compliant.

The need for AI governance is driven by:
- **GDPR/UK GDPR**: Article 22 restricts automated decision-making that significantly affects individuals
- **EU AI Act** (2024): Classifies AI systems by risk (Minimal, Limited, High, Unacceptable) with different governance requirements
- **NIST AI RMF** (2023): A framework for managing AI risk — GOVERN, MAP, MEASURE, MANAGE
- **Business risk**: AI hallucinations, bias, data poisoning, and model opacity can cause significant harm

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **Shared Responsibility Model** | Division of security between cloud provider and customer | AWS secures hardware; customer secures OS |
| **IAM** | Identity and Access Management | AWS IAM roles; Azure RBAC |
| **CSPM** | Cloud Security Posture Management | Wiz, Prisma Cloud scanning for misconfigurations |
| **CIS Benchmark** | Configuration hardening guide for cloud platforms | CIS AWS Foundations Benchmark Level 1 |
| **AWS Config** | AWS service monitoring resource configurations | Checks if MFA is enabled on all IAM users |
| **AI RMF** | NIST AI Risk Management Framework (2023) | GOVERN, MAP, MEASURE, MANAGE functions |
| **EU AI Act** | EU regulation classifying and regulating AI systems | High-risk AI requires conformity assessment |
| **GDPR Art. 22** | Restrictions on automated decision-making | Credit scoring AI must allow human review |
| **AI Risk** | Risks specific to AI systems | Hallucination, bias, data poisoning, opacity |
| **Algorithmic Bias** | AI producing systematically unfair outcomes | Loan rejection AI disproportionately rejecting minorities |
| **Model Card** | Documentation of an AI model's purpose, training, and limitations | Required by some AI governance frameworks |
| **IaC Security** | Infrastructure-as-Code security | Scanning Terraform/CloudFormation for misconfigurations |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Cloud GRC Assessment Process

1. **Map the cloud environment** — Understand what cloud services are in use: AWS, Azure, GCP, multi-cloud. What services (EC2, S3, RDS, Lambda, etc.)? Who has access?

2. **Review the shared responsibility model** — For each cloud service used, document what the provider is responsible for and what the customer must configure. Use the cloud provider's shared responsibility documentation.

3. **Obtain cloud provider compliance documentation** — AWS, Azure, and GCP all publish SOC 2 reports, ISO 27001 certificates, and compliance documentation via their compliance portals (AWS Artifact, Microsoft Trust Center, GCP Compliance Reports).

4. **Assess cloud configuration against CIS Benchmarks** — The CIS Benchmark for AWS (Level 1 and Level 2) provides specific configuration requirements for 497 AWS services. Use AWS Security Hub or a CSPM tool to score current compliance.

5. **Review IAM configuration** — IAM is the most common source of cloud security failures. Check: Are all IAM users using MFA? Are there any users/roles with AdministratorAccess policy? Are root account credentials protected? Is least privilege applied?

6. **Assess encryption posture** — Are all S3 buckets encrypted? Are RDS databases encrypted? Are EBS volumes encrypted? Is CloudTrail logging encrypted?

7. **Review network security** — Are security groups overly permissive? Are any S3 buckets publicly accessible? Is VPC flow logging enabled?

8. **CSPM implementation** — Implement a CSPM tool (AWS Security Hub + native compliance checks, or third-party tools like Wiz or Prisma Cloud) that continuously monitors for misconfigurations.

### The AI Governance Process

1. **AI system inventory** — Catalogue all AI/ML systems in use: what they do, what data they use, what decisions they inform, who built them, what controls are in place.

2. **AI risk classification** — Apply the EU AI Act risk classification or NIST AI RMF mapping to categorise each AI system by risk level.

3. **Apply NIST AI RMF:**
   - **GOVERN**: Establish AI governance structure; AI use policy; AI ethics principles; roles and responsibilities
   - **MAP**: Identify AI risks (bias, accuracy, security, privacy, regulatory)
   - **MEASURE**: Assess and monitor AI risk using quantitative and qualitative metrics
   - **MANAGE**: Respond to identified AI risks; implement controls; document

4. **GDPR Article 22 compliance** — If AI makes or significantly influences decisions about individuals (credit, insurance, employment), ensure: legal basis (Art. 6); right to explanation; human review available.

5. **AI security controls** — Protect AI systems against adversarial attacks (prompt injection, data poisoning, model extraction); implement input validation; monitor model behaviour.

6. **AI governance policy** — Write a formal AI Use Policy defining: what AI the organisation can use; what it cannot use; data governance requirements for AI; human oversight requirements.

---

## Section 3: Framework Deep Dive

### NIST AI RMF 2.0 (2024)

**GOVERN (GV)**: Cross-cutting function — policies, processes, plans, and procedures for organisational AI risk management
- GV.1: Organisational policies and practices are in place to govern the organisation's AI
- GV.4: Organisational teams are committed to transparent, responsible AI development and use

**MAP (MP)**: Risk identification and classification
- MP.1: AI risk is identified and prioritised
- MP.2: Scientific and technological knowledge relevant to AI risks is identified

**MEASURE (ME)**: Risk analysis and monitoring
- ME.1: AI risk is analysed using quantitative and qualitative methods
- ME.3: AI system performance is monitored for degradation, risks, and biases

**MANAGE (MG)**: Risk response and recovery
- MG.1: Risks based on assessments are prioritised and addressed
- MG.4: Identified risks in AI systems are managed

### CIS AWS Foundations Benchmark (Level 1 key controls)

| Check | Control | Risk if Fails |
|-------|---------|---------------|
| 1.1 | Avoid root account usage | Root compromise = total account takeover |
| 1.4 | MFA enabled for root account | Root without MFA = critical vulnerability |
| 1.10 | MFA enabled for all IAM users | Account takeover risk |
| 2.1.1 | S3 buckets not publicly accessible | Data exposure to internet |
| 3.1 | CloudTrail enabled in all regions | Audit trail gap |
| 4.1 | No unrestricted inbound access on SSH | Exposed attack surface |

---

## Section 4: Common Mistakes Beginners Make

1. **Assuming cloud providers handle all security.** The most dangerous misconception. AWS secures the infrastructure. The customer must configure IAM, encryption, network security, and application security.

2. **Ignoring IaC (Infrastructure-as-Code) security.** If your company uses Terraform or CloudFormation to provision cloud resources, misconfigurations in the IaC code become production vulnerabilities. IaC security scanning (Checkov, tfsec) is a critical GRC control.

3. **Treating AI governance as optional.** The EU AI Act is law in the EU (affecting UK companies selling to EU). GDPR Article 22 is already in force. AI governance is not aspirational — it is a regulatory requirement.

4. **Applying traditional GRC controls to AI systems without adaptation.** A security policy that requires "all data to be encrypted at rest" needs to address whether training data for AI models meets this requirement.

5. **Not inventorying shadow AI.** Staff use AI tools (ChatGPT, Copilot, Gemini) that may process company data. Without an AI inventory and policy, data classification controls break down.

6. **Confusing cloud provider compliance with customer compliance.** AWS being ISO 27001 certified does not mean your applications running on AWS are ISO 27001 compliant. The customer must separately certify their own implementations.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **AWS Security Hub is your cloud GRC friend** — it aggregates findings from AWS Config, GuardDuty, and Inspector against NIST CSF, CIS AWS Benchmark, and other standards. It's the starting point for cloud GRC assessment.
- **Request cloud provider compliance documentation** — AWS Artifact, Microsoft Trust Center, and GCP Compliance Reports provide provider-side SOC 2 reports and ISO 27001 certificates. Use them as your provider attestation.
- **The CIS AWS Benchmark Level 1 is achievable for most companies** — 80% of Level 1 checks can be automated using AWS Config rules and AWS Security Hub.
- **NIST AI RMF is the framework to use for AI governance** — it aligns with the EU AI Act risk categories and is increasingly required by regulators.
- **Build an AI register before you need it** — catalogue all AI systems in use now. In 2 years, regulators will expect it.
- **AI hallucination is a GRC risk** — if your company uses AI for any customer-facing or regulated decision, "the AI said so" is not a valid explanation to a regulator. Human oversight controls are essential.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [AWS Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/) — Essential foundational document
- [CIS AWS Foundations Benchmark](https://www.cisecurity.org/cis-benchmarks/) — Free; Level 1 controls for AWS
- [NIST AI RMF 1.0](https://airc.nist.gov/RMF_Overview) — Full framework document
- [EU AI Act Summary](https://www.europarl.europa.eu/topics/en/article/20230601STO93804/eu-ai-act-first-regulation-on-artificial-intelligence) — Overview of EU AI Act risk categories
- [AWS Security Hub Overview](https://aws.amazon.com/security-hub/) — Cloud compliance monitoring
- [ICO: AI and Data Protection](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/artificial-intelligence/) — UK GDPR + AI guidance
- [NCSC: Cloud Security Guidance](https://www.ncsc.gov.uk/collection/cloud/understanding-cloud-security) — UK cloud security

### Books

- *Cloud Security: A Comprehensive Guide to Secure Cloud Computing* by Ronald L. Krutz — Cloud security reference
- *Trustworthy AI* by Beena Ammanath — AI ethics and governance

### Online Courses

- [AWS Security Fundamentals (Free)](https://aws.amazon.com/training/digital/aws-security-fundamentals/) — Free AWS security training
- [SANS: Cloud Security Architecture](https://www.sans.org/cyber-security-courses/cloud-security-architecture-operations/) — Advanced cloud GRC
- [NIST AI RMF Workshop Videos](https://www.nist.gov/artificial-intelligence) — Free NIST AI training

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (90 min)

- 20 min: Shared responsibility model — use AWS diagram; work through 5 services (EC2, S3, RDS, Lambda, IAM) and identify what's provider vs customer responsibility for each
- 20 min: CIS AWS Benchmark — walk through the top 10 Level 1 controls together; discuss what each requires technically
- 20 min: NIST AI RMF — walk through all 4 functions; for each, give a TechVenture AI use case example
- 15 min: GDPR Article 22 — work through: "TechVenture uses AI to score customer support tickets as 'urgent/not urgent'. Does this trigger Article 22?"
- 15 min: AI risk register exercise — identify 5 AI risks together for TechVenture

### Session B Focus (60 min)

- Review cloud governance framework: Is shared responsibility clearly articulated?
- Check CIS AWS assessment: Are findings specific (not generic)?
- Review AI risk register: Are AI-specific risks identified (not just generic IT risks)?
- Ask: "TechVenture's AI customer support assistant sometimes gives incorrect advice to customers. What GRC controls address this risk?"

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "Explain the AWS Shared Responsibility Model."
2. "What is CSPM and why is it important?"
3. "What is the CIS AWS Foundations Benchmark?"
4. "What are the key cloud IAM security risks?"
5. "What is the NIST AI RMF?"
6. "What does GDPR Article 22 say about AI?"
7. "What is the EU AI Act and how does it classify AI risk?"
8. "How do you assess a cloud-native company for ISO 27001 compliance?"
9. "What cloud security tools have you worked with?"
10. "What is IaC security?"

### Keywords to Use

- Shared Responsibility Model — AWS secures OF the cloud; customer secures IN the cloud
- Cloud Security Posture Management (CSPM)
- CIS AWS Benchmark Level 1/2
- AWS IAM least privilege
- AWS Security Hub / Microsoft Defender for Cloud
- NIST AI RMF — GOVERN, MAP, MEASURE, MANAGE
- EU AI Act — risk classification
- GDPR Article 22 — automated decision-making
- AI governance policy
- IaC security (Terraform, CloudFormation)
