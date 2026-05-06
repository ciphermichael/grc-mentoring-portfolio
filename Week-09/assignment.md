# Week 09 Assignment: SOC 2 and Cloud Compliance

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | StartupStack |
| **Your Role** | GRC Consultant — SOC 2 Readiness |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟🌟 |
| **Frameworks** | SOC 2 (AICPA Trust Services Criteria), CSA CCM, ISO 27001 (cross-mapping) |

---

## Scenario Brief — Read This Carefully

**StartupStack** is a 50-person UK SaaS company providing project management and team collaboration software. Their platform has 8,000 active business users (teams from small businesses to mid-market companies). The platform is entirely cloud-native, hosted on AWS (eu-west-1, Ireland). They process personal data (user names, email addresses, project content, file attachments) under GDPR as a data controller.

StartupStack has received a compelling enterprise lead — **Meridian Insurance Group**, a 5,000-person insurance company whose procurement team has stated: "We require a SOC 2 Type II report dated within the last 12 months before we can proceed. We also need evidence of appropriate cloud security controls." This would be StartupStack's largest contract at £380,000 ARR.

The CEO, Jamie Santos, has asked you to conduct a SOC 2 readiness assessment and build a 90-day plan to achieve readiness for a Type I audit (the first milestone toward a Type II report). StartupStack has never been through a SOC 2 audit. Their Head of Engineering, Alex Park, manages all security controls informally.

**Current cloud security state:**
- AWS hosted; uses S3, RDS, EC2, Lambda, CloudFront
- No formal change management process for infrastructure changes
- Logging: CloudTrail enabled; logs not reviewed; no alerting
- Access control: AWS IAM used; some overly permissive IAM roles; no PAM
- Data encryption: RDS encryption enabled; S3 encryption enabled; key management informal
- Incident response: No documented process; Alex "handles issues as they come up"
- Vendor management: Uses Stripe (payment processing), Intercom (customer support), GitHub (code hosting), Sendgrid (email) — none formally assessed
- Availability: AWS multi-AZ for RDS; no formal RTO/RPO defined

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 9 — especially the 5 Trust Services Criteria
- [ ] Read the AICPA SOC 2 overview at aicpa.org
- [ ] Review the SOC 2 common criteria codes: CC1–CC9 (Common Criteria) and the additional criteria
- [ ] Understand the difference between Type I and Type II reports

### Questions to Answer Before Starting
1. What are the 5 SOC 2 Trust Services Criteria? Which one is mandatory in every SOC 2 report?
2. What is the difference between a SOC 2 Type I and Type II report?
3. Meridian Insurance requires a Type II report. Why is a Type I report not sufficient for them?
4. Which SOC 2 Common Criterion (CC code) covers logical and physical access controls?
5. StartupStack uses Stripe for payment processing. Under SOC 2, how is a sub-service organisation like Stripe treated?

---

## Deliverables

### Deliverable 1: SOC 2 Readiness Assessment (All 5 TSC)

**What It Is:** A structured assessment of StartupStack's current controls against all 5 SOC 2 Trust Services Criteria, identifying gaps before the Type I audit.

**Step-by-Step Instructions:**

1. Create a spreadsheet with a tab per TSC: Security (mandatory) | Availability | Confidentiality | Processing Integrity | Privacy

2. For the **Security TSC (CC1–CC9)**, assess all Common Criteria. Key criteria for StartupStack:
   - **CC1 — Control Environment**: Does management demonstrate commitment to security? (Risk: StartupStack has no CISO; controls are informal)
   - **CC2 — Communication and Information**: Are security responsibilities communicated? (Risk: No formal security roles or policies)
   - **CC3 — Risk Assessment**: Is there a formal risk assessment? (Risk: None conducted)
   - **CC4 — Monitoring**: Is the control environment monitored? (Risk: No logging review; no alerting)
   - **CC5 — Control Activities**: Logical and physical controls in place? (Risk: IAM roles overly permissive)
   - **CC6 — Logical and Physical Access**: Is access restricted and reviewed? (Risk: No formal access reviews; no PAM)
   - **CC7 — System Operations**: Are operations monitored for anomalies? (Risk: No SIEM; CloudTrail not reviewed)
   - **CC8 — Change Management**: Are changes controlled? (Risk: No formal change management)
   - **CC9 — Risk Mitigation**: Are vendor and supply chain risks managed? (Risk: Key vendors not assessed)

3. For each criterion: Assessment (In Place / Partial / Not In Place) | Evidence Available | Gap Description | Severity | Remediation Required

4. **Availability TSC (A1)**: Assess: Is there a formal uptime/availability commitment? SLA? BCP? DR plan? (Risk: None defined)

5. **Confidentiality TSC (C1)**: Assess: How is confidential data identified and protected? (StartupStack stores project content — is this confidential?)

6. Provide a summary: % criteria In Place, % Partial, % Not In Place; overall SOC 2 readiness rating.

---

### Deliverable 2: Type I vs Type II Gap Analysis

**What It Is:** A clear document explaining the difference between Type I and Type II, what StartupStack needs for each, and a realistic timeline.

**Structure:**
1. What is a SOC 2 Type I report? (Point-in-time; documents that controls are designed suitably)
2. What is a SOC 2 Type II report? (6–12 month observation period; tests control effectiveness over time)
3. Why does Meridian Insurance require Type II? (One paragraph)
4. What must StartupStack achieve before a Type I audit? (Based on your readiness assessment findings)
5. Realistic timeline: Type I target date | Type II target date (Type II = Type I + at least 6 months observation)
6. Table: Control gaps that must be remediated before Type I | Controls that can be in remediation during Type II observation period

---

### Deliverable 3: SOC 2 Control Mapping to StartupStack AWS Environment

**What It Is:** A mapping showing how specific SOC 2 Common Criteria are satisfied by AWS services and StartupStack's own controls.

**Create a table:**
SOC 2 Criterion | StartupStack Control | AWS Service Supporting It | Evidence Required | Gap?

**Cover at minimum:**
- CC6.1 (Logical access) → IAM roles + MFA enforcement → AWS IAM | Evidence: IAM role configurations
- CC6.6 (Boundary protection) → VPC security groups → AWS VPC | Evidence: Security group configs
- CC7.1 (Detection of threats) → CloudTrail + CloudWatch alerts → AWS CloudTrail, CloudWatch | Evidence: Log review records
- CC8.1 (Change management) → [Currently no formal CM] → AWS CloudFormation could support | Gap: Formal change process needed
- A1.1 (Availability commitments) → Multi-AZ RDS → AWS RDS | Evidence: Architecture diagram

---

### Deliverable 4: 90-Day SOC 2 Readiness Roadmap

**What It Is:** A realistic 90-day plan to prepare StartupStack for a SOC 2 Type I audit.

**Structure by month:**

**Month 1 — Governance Foundation:**
- Appoint a SOC 2 programme lead (who within StartupStack owns this?)
- Define in-scope services (which StartupStack services are in the SOC 2 scope?)
- Select a SOC 2 auditor (research and select an accounting firm qualified to conduct SOC 2 audits)
- Establish CC1: Write an Information Security Policy; assign security responsibilities
- Begin CC3: Conduct first formal risk assessment

**Month 2 — Control Implementation:**
- CC6: Enforce MFA for all AWS console access; review and tighten IAM roles; implement quarterly access reviews
- CC8: Implement formal change management process (change request → approval → testing → deployment → review)
- CC7: Set up CloudWatch alerts for security events; implement log review process
- CC9: Conduct vendor assessment for Stripe, Intercom, GitHub, Sendgrid

**Month 3 — Evidence and Pre-Audit:**
- Collect evidence for all implemented controls (screenshots, logs, policy documents, access review records)
- Conduct internal SOC 2 readiness review
- Address any remaining gaps
- Engage auditor for Type I audit scheduling

For each initiative: SOC 2 criteria addressed | Owner | Effort | Evidence to produce | Success criteria

---

### Deliverable 5: SOC 2 Evidence Collection Checklist

**What It Is:** A practical checklist of all evidence StartupStack must collect before the Type I audit.

**Organised by TSC criteria:**
- For each Common Criterion: List 2–4 specific evidence items (e.g., "CC6.1: IAM role configurations export, MFA enforcement screenshot, access review records Q1, offboarding checklist")
- Evidence format: Document, screenshot, log extract, certificate, interview memo
- Evidence owner: Who produces each piece of evidence?
- Collection deadline: When must evidence be collected by?

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Readiness Assessment Quality | 30% | All 5 TSC assessed; specific gaps identified; SOC 2 terminology correct |
| Type I vs II Analysis | 20% | Clear distinction; realistic timeline |
| Control Mapping | 20% | AWS services correctly mapped to SOC 2 criteria |
| Roadmap Realism | 30% | 90-day plan achievable; criteria addressed in correct sequence |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **SOC 2 — AICPA Trust Services Criteria** | Full readiness assessment against all 5 criteria |
| **CSA Cloud Controls Matrix (CCM)** | Referenced for cloud-specific control implementation |
| **ISO 27001:2022** | Cross-mapping to show path from SOC 2 to ISO 27001 certification |

---

## Week-Specific Resources

- [AICPA SOC 2 Overview](https://us.aicpa.org/interestareas/frc/assuranceadvisoryservices/sorhome) — Official SOC 2 description
- [AICPA Trust Services Criteria (2017 updated)](https://www.aicpa.org/resources/download/2017-trust-services-criteria-with-2022-points-of-focus-updates) — Official TSC document
- [SOC 2 Academy by Laika](https://heylaika.com/resources/) — Excellent free SOC 2 guides
- [Secureframe SOC 2 Guide](https://secureframe.com/hub/soc-2/what-is-soc-2) — Practical implementation guide
- [AWS SOC 2 Compliance](https://aws.amazon.com/compliance/soc-faqs/) — AWS's own SOC 2 compliance documentation
- [Vanta SOC 2 Checklist](https://www.vanta.com/resources/soc-2-checklist) — Practical readiness checklist
- [CSA Cloud Controls Matrix](https://cloudsecurityalliance.org/research/cloud-controls-matrix/) — Cloud security control reference

---

## Submission

```
Week-09/Deliverables/
├── StartupStack-SOC2-Readiness-Assessment-v1.0.xlsx
├── StartupStack-TypeI-vs-TypeII-Analysis-v1.0.md
├── StartupStack-SOC2-AWS-Control-Mapping-v1.0.xlsx
├── StartupStack-SOC2-90Day-Roadmap-v1.0.xlsx
└── StartupStack-SOC2-Evidence-Checklist-v1.0.xlsx
```
