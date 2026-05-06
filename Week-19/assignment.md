# Week 19 Assignment: Cloud and AI Security Governance

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | TechVenture Ltd. |
| **Your Role** | GRC Analyst — Cloud and AI |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟🌟🌟 |
| **Frameworks** | NIST CSF 2.0, CIS AWS Benchmark, NIST AI RMF, ISO 27001, GDPR Art. 22 |

---

## Scenario Brief — Read This Carefully

**TechVenture Ltd.** is a 120-person cloud-native UK SaaS startup that has grown from 15 to 120 employees in 2 years. They provide a B2B customer engagement platform used by 450 companies. Their platform is entirely cloud-native on AWS (eu-west-1, Ireland). Key AWS services in use: EC2, ECS (containers), RDS (PostgreSQL), S3, Lambda, API Gateway, CloudFront, SQS, and Cognito for user authentication.

TechVenture has also integrated AI extensively into their platform:
1. **Customer Sentiment AI**: An ML model that analyses customer interaction transcripts to score customer satisfaction (1–10). Used by clients to prioritise support follow-ups.
2. **Churn Prediction AI**: An ML model predicting which customers are likely to churn, trained on 18 months of customer data. Used by TechVenture's sales team to trigger retention campaigns.
3. **AI Support Assistant**: A GPT-4-based chatbot integrated into their platform that answers customer questions about TechVenture's product. Occasionally gives incorrect product information.
4. **Automated Content Moderation**: An AI model that reviews user-generated content in the platform for policy violations. Automatically removes content flagged as violating.

TechVenture has no formal cloud governance framework and no AI governance programme. They are growing rapidly and have recently signed their first enterprise contracts with two FTSE 250 companies that have asked for evidence of cloud security governance. They are also receiving questions from their DPO about the AI systems' GDPR Article 22 implications.

**Known cloud security issues (from a recent informal security review):**
- AWS root account has no MFA enabled
- 12 IAM users have Administrator-level access (should be 3)
- 3 S3 buckets containing customer data are publicly accessible (misconfiguration)
- No AWS CloudTrail logging in all regions (only us-east-1 — wrong region for eu-west-1 workloads)
- No AWS Security Hub or GuardDuty enabled
- EC2 security groups: 5 have port 22 (SSH) open to 0.0.0.0/0 (internet)
- RDS: 2 databases not encrypted at rest
- Lambda functions: No least-privilege IAM roles (all using same overly-permissive role)

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 19 — especially the Shared Responsibility Model and AI RMF
- [ ] Read the AWS Shared Responsibility Model documentation at aws.amazon.com
- [ ] Download or access the CIS AWS Foundations Benchmark Level 1 checklist
- [ ] Read NIST AI RMF at airc.nist.gov
- [ ] Read ICO's guidance on AI and automated decision-making

### Questions to Answer Before Starting
1. TechVenture has 3 S3 buckets publicly accessible. Under the AWS Shared Responsibility Model, whose responsibility is this — AWS or TechVenture?
2. Does the Churn Prediction AI trigger GDPR Article 22? (Does it make decisions that significantly affect individuals?)
3. What AWS native service would you enable first to improve TechVenture's cloud security posture monitoring?
4. The AI Support Assistant sometimes gives incorrect product information. What is the GRC risk category and what controls address it?
5. TechVenture's root account has no MFA. This is a CIS AWS Benchmark Level 1 finding. What is the severity rating?

---

## Deliverables

### Deliverable 1: Cloud Security Governance Framework

**What It Is:** TechVenture's formal cloud security governance framework — the document that defines how cloud security is governed, who is responsible for what, and what the baseline security requirements are.

**Must include:**
1. **Cloud governance scope**: AWS eu-west-1 environment; all AWS accounts; all TechVenture engineering teams
2. **Shared Responsibility Model applied to TechVenture**: A table showing for each AWS service TechVenture uses (EC2, ECS, RDS, S3, Lambda, etc.): what AWS is responsible for vs what TechVenture is responsible for
3. **Cloud governance principles** (6 principles): e.g., "Least privilege for all IAM access", "Encryption at rest for all data in S3 and RDS", "No production access from development accounts"
4. **Cloud security roles**: Cloud Security Owner (CTO), Cloud Security Analyst (DevOps Lead), GRC oversight
5. **Baseline security requirements** (the non-negotiable configuration standards): Root MFA, no public S3 buckets, CloudTrail enabled in all regions, security groups restrict SSH, RDS encryption enabled
6. **IaC security policy**: All AWS infrastructure provisioned via Terraform; all Terraform code scanned by Checkov before deployment
7. **Compliance monitoring**: AWS Security Hub enabled; weekly compliance review; quarterly CSPM review
8. **Cloud access policy**: Who can access production AWS? How is access provisioned and reviewed?

---

### Deliverable 2: CIS AWS Benchmark Assessment (Level 1)

**What It Is:** A formal assessment of TechVenture's AWS environment against the CIS AWS Foundations Benchmark Level 1, documenting all findings with remediation actions.

**Create a spreadsheet covering CIS AWS Level 1 key domains:**

**Identity and Access Management (CIS 1.x):**
- 1.1: Avoid root account use — Status: NON-COMPLIANT (root account has no MFA; active sessions detected) — CRITICAL
- 1.4: Ensure MFA on root account — NON-COMPLIANT — CRITICAL
- 1.10: Ensure MFA for all IAM users — NON-COMPLIANT (12 IAM users without MFA) — HIGH
- 1.16: Ensure IAM policies attached directly to users — assess — MEDIUM
- 1.20: Ensure a support role has been created — assess

**Storage (CIS 2.1.x):**
- 2.1.1: Ensure S3 public access block — NON-COMPLIANT (3 public buckets) — CRITICAL
- 2.1.5: Ensure S3 bucket logging enabled — assess

**Logging (CIS 3.x):**
- 3.1: Ensure CloudTrail enabled in all regions — NON-COMPLIANT (only enabled in us-east-1) — HIGH
- 3.2: Ensure log validation enabled — assess
- 3.3: Ensure CloudTrail integrated with CloudWatch Logs — assess

**Monitoring (CIS 4.x):**
- 4.1: Ensure no unrestricted SSH (port 22) — NON-COMPLIANT (5 security groups) — CRITICAL
- 4.2: Ensure no unrestricted RDP (port 3389) — assess
- 4.14: Ensure GuardDuty enabled — NON-COMPLIANT — HIGH

**For each finding:**
- Check ID and description
- Status: Compliant / Non-Compliant / Not Applicable
- Evidence/current state
- Risk if not remediated
- Severity: Critical / High / Medium / Low
- Remediation steps (specific AWS console or CLI actions)
- Owner
- Target date

**Summary tab:** % Compliant by domain; total Critical/High/Medium/Low findings; estimated remediation effort

---

### Deliverable 3: AI Risk Register (10+ AI-Specific Risks)

**What It Is:** A risk register specifically for TechVenture's 4 AI systems, identifying AI-specific risks not covered by traditional security risk registers.

**For each AI system, identify 2–3 specific risks:**

**Customer Sentiment AI:**
1. **AI bias risk**: Model may produce systematically different sentiment scores for different customer demographics if training data reflects historical bias. Risk: Discriminatory customer support prioritisation. GDPR Art. 22 consideration.
2. **Model accuracy degradation**: Sentiment model trained 18 months ago may no longer accurately reflect current language patterns. Risk: Incorrect customer priority scoring leading to lost accounts.

**Churn Prediction AI:**
3. **GDPR Art. 22 automated decision-making**: Churn model triggers automated retention campaign actions (discounts, outreach) based on scores. This may constitute "automated decision-making producing significant effects" on individuals. Risk: ICO enforcement if no human oversight mechanism. CRITICAL.
4. **Training data quality**: 18 months of training data may include COVID-era anomalies that don't reflect current churn patterns. Risk: Inaccurate predictions leading to wasted retention spend.
5. **Data minimisation breach**: Is all data used to train the churn model necessary? Has a DPIA been conducted? Risk: GDPR violation.

**AI Support Assistant:**
6. **Hallucination risk**: GPT-4 may provide confident but incorrect product information to customers. Risk: Customer reliance on incorrect advice; regulatory issues if advice involves regulated activity.
7. **Prompt injection**: Malicious user could inject instructions that cause the AI to reveal confidential information or act outside intended scope. Risk: Data breach; reputational damage.
8. **Data retention**: Are customer support conversations with the AI retained? For how long? Risk: GDPR storage limitation principle.

**Automated Content Moderation:**
9. **False positive removals**: AI incorrectly removes legitimate user content. Risk: Customer complaints; potential contractual liability.
10. **Lack of human review**: Automated removals with no human appeals process. Risk: Regulatory risk under EU AI Act (automated decisions affecting users); GDPR Art. 22 consideration.

**For each risk:** Risk ID | AI System | Risk Title | Risk Description | Risk Category (Accuracy/Bias/Privacy/Security/Regulatory) | Likelihood | Impact | Risk Score | GDPR/Regulatory Implication | Controls in Place | Control Gap | Recommended Action | Owner

---

### Deliverable 4: AI Governance Policy

**What It Is:** TechVenture's formal AI Use Policy governing how AI is developed, deployed, and used within the organisation.

**Must include:**
1. **Purpose**: Why TechVenture needs an AI governance policy (regulatory requirements: GDPR Art. 22, EU AI Act; business risk)
2. **Scope**: All AI/ML systems developed by TechVenture + all third-party AI tools used by employees (including ChatGPT, Microsoft Copilot)
3. **AI principles** (6 principles): Transparency, Accountability, Fairness, Privacy, Security, Human Oversight
4. **AI system classification**: High-risk (automated decisions affecting individuals) vs Standard vs Low-risk
5. **Requirements by classification**:
   - High-risk: GDPR Art. 22 compliance; DPIA required; human review mechanism; regular bias testing; model card documentation
   - Standard: Data governance review; security review; performance monitoring
   - Low-risk: Standard security controls; monitoring
6. **Third-party AI tool policy**: What employees can and cannot use; which data can be entered into AI tools; approved vs prohibited tools list
7. **AI incident response**: What happens if an AI system causes harm or produces materially incorrect outputs?
8. **AI register requirement**: All AI systems must be registered in TechVenture's AI inventory
9. **GDPR Art. 22 compliance**: Right to human review for churn prediction AI; privacy notice update requirement

---

### Deliverable 5: Cloud GRC Roadmap (90 Days)

**What It Is:** A prioritised 90-day remediation plan addressing TechVenture's critical cloud security gaps.

**Week 1–2 (Critical — No Cost):**
- Enable MFA on root account (immediate; zero cost)
- Block public access on 3 S3 buckets (immediate; zero cost; requires data classification review first)
- Review and reduce IAM Administrator-level access from 12 to 3 users
- Enable CloudTrail in all regions including eu-west-1

**Month 1 (High — Low Cost):**
- Enable AWS Security Hub and enable CIS AWS Benchmark standard checks
- Enable GuardDuty in eu-west-1 (cost: ~£50/month)
- Remediate 5 security groups with SSH open to 0.0.0.0/0
- Encrypt 2 unencrypted RDS databases (requires maintenance window; plan carefully)
- Enable Lambda least-privilege IAM roles (engineer effort: 2 days)

**Month 2 (Medium):**
- Implement Terraform IaC scanning with Checkov in CI/CD pipeline
- Enable CloudWatch Logs integration with CloudTrail
- Conduct IAM access review and document findings
- Implement AWS Config rules for ongoing compliance monitoring

**Month 3 (AI Governance):**
- Conduct DPIA for Churn Prediction AI
- Implement human review mechanism for churn prediction automated actions
- Update privacy notice to disclose AI use
- Complete AI register for all 4 systems
- Publish AI Governance Policy

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| CIS AWS Assessment | 25% | Critical findings identified; remediation steps specific; severity correctly applied |
| AI Risk Register | 30% | AI-specific risks (not generic IT risks); GDPR Art. 22 implications addressed |
| AI Governance Policy | 25% | Comprehensive; GDPR Art. 22 addressed; employee AI tools covered |
| Cloud GRC Framework | 20% | Shared responsibility correctly applied; TechVenture-specific |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **CIS AWS Foundations Benchmark Level 1** | Full cloud security assessment |
| **NIST AI RMF (2023)** | AI risk identification and governance structure |
| **GDPR Articles 22, 25, 35** | AI automated decision-making; privacy by design; DPIA |
| **ISO 27001 A.8** | Technological controls mapping to cloud security |
| **EU AI Act** | AI system risk classification |

---

## Week-Specific Resources

- [AWS Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/) — Essential
- [CIS AWS Foundations Benchmark](https://www.cisecurity.org/cis-benchmarks/) — Free download (register at CIS)
- [AWS Security Hub](https://aws.amazon.com/security-hub/) — Compliance monitoring documentation
- [NIST AI RMF 1.0](https://airc.nist.gov/RMF_Overview) — Full AI governance framework
- [ICO: AI and Automated Decision-Making](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/artificial-intelligence/) — GDPR + AI guidance
- [AWS Well-Architected Framework — Security Pillar](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html) — AWS security best practices

---

## Submission

```
Week-19/Deliverables/
├── TechVenture-Cloud-Security-Governance-Framework-v1.0.md
├── TechVenture-CIS-AWS-Benchmark-Assessment-v1.0.xlsx
├── TechVenture-AI-Risk-Register-v1.0.xlsx
├── TechVenture-AI-Governance-Policy-v1.0.md
└── TechVenture-Cloud-GRC-Roadmap-90Day-v1.0.xlsx
```
