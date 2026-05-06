# Week 02 Assignment: Risk Management Fundamentals

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | CloudSafe Ltd. |
| **Your Role** | GRC Analyst |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟 |
| **Frameworks** | ISO 27001 (Clause 6.1.2), ISO 27005, NIST CSF 2.0 (GOVERN, IDENTIFY) |

---

## Scenario Brief — Read This Carefully

**CloudSafe Ltd.** is a 150-person UK cloud storage company, founded in 2017, headquartered in Bristol. They provide secure cloud storage and file-sharing services to 3,000 UK business clients including law firms, accountancies, and manufacturing companies. Their platform stores approximately 2 petabytes of data including sensitive client documents — legal files, financial records, and personal data.

CloudSafe is both a data controller (employee data) and a data processor (client business data) under GDPR. Their infrastructure runs entirely on AWS (eu-west-2, London region). Three months ago, CloudSafe lost a £400,000 contract renewal when a client's security team asked to see their risk register and received no response. The CEO, Marcus Lowe, has hired you as their first GRC Analyst to build a formal risk management programme.

**Known control gaps:** No EDR on all endpoints, no Privileged Access Management for AWS console, developers have direct production database access, no formal vendor management, no patch management programme, no security awareness training in 2 years.

**Client mix:** Legal (25%), financial advisory (30%), healthcare (10%), other professional services (35%).

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 2 — especially the risk scoring methodology
- [ ] Review NIST SP 800-30 Rev 1 introduction and threat tables
- [ ] Read the NCSC Annual Review for current UK threat context
- [ ] Study the AWS Shared Responsibility Model

### Questions to Answer Before Starting
1. Under the AWS Shared Responsibility Model, who patches the EC2 operating system — CloudSafe or AWS?
2. A developer has production database access. What risk category does this fall into?
3. If likelihood = 3 and impact = 4, what is the risk score and rating?
4. CloudSafe stores healthcare client data. Does this change their GDPR obligations?
5. What are the 4 risk treatment options and when would you choose each?

---

## Deliverables

### Deliverable 1: Enterprise Risk Register (20 risks minimum)

**What It Is:** A structured spreadsheet documenting all identified risks with assessment scores, current controls, and treatment decisions — CloudSafe's primary risk management tool.

**Step-by-Step Instructions:**

1. Create a spreadsheet with these columns: Risk ID | Risk Title | Risk Category | Risk Description | Threat Source | Vulnerability | Asset Affected | Risk Owner | Likelihood (1–5) | Impact (1–5) | Inherent Risk Score | Inherent Rating | Current Controls | Residual Likelihood | Residual Impact | Residual Score | Residual Rating | Treatment | Treatment Actions | Owner | Target Date | Status

2. Define scoring scales clearly in a separate tab:
   - Likelihood: 1=Rare, 2=Unlikely, 3=Possible, 4=Likely, 5=Almost Certain
   - Impact: 1=Negligible (<£1K), 2=Minor (£1–10K), 3=Moderate (£10–100K), 4=Major (£100K–£1M), 5=Catastrophic (>£1M)
   - Ratings: 1–4=Low (Green), 5–9=Medium (Yellow), 10–16=High (Orange), 17–25=Critical (Red)

3. Identify risks across these categories — aim for 3–5 risks per category:
   - **Technology Risks**: Ransomware attack on S3 storage, unpatched EC2 vulnerabilities, S3 misconfiguration exposing client data, DDoS against the platform
   - **Third-Party Risks**: AWS region outage, critical SaaS vendor compromise (Salesforce/Zendesk), supply chain attack on development dependencies
   - **Insider Threats**: Developer misuse of production database access, accidental mass data deletion, disgruntled employee exfiltrating client files
   - **Compliance Risks**: GDPR data breach fine (ICO enforcement), failure to respond to Subject Access Request, DPIA not conducted for high-risk processing
   - **Physical/Operational Risks**: Bristol office fire destroying endpoint devices, key person dependency (only 1 AWS admin)

4. For each risk, document current controls honestly. If none exist, write "No controls identified."

5. Calculate residual risk after considering current controls. Residual score should be lower than inherent score only when effective controls exist.

6. Assign named role owners: Head of IT (technology risks), Head of Legal (compliance risks), CEO (strategic risks).

**Example Row:**
| CSR-001 | Ransomware encryption of AWS S3 production storage | Technology | Financially motivated ransomware group encrypts client file storage via compromised developer credentials | External attacker | No PAM; developer AWS admin access not restricted | AWS S3 platform; client data | Head of IT | 4 | 5 | 20 (Critical) | AWS versioning enabled; no EDR; no network segmentation | 3 | 5 | 15 (High) | Mitigate: Deploy EDR on all endpoints; implement AWS IAM least privilege; enable S3 Object Lock | Head of IT | Q1 | Open |

**Quality Bar:** Risks are specific to CloudSafe (not generic); likelihood/impact scores are calibrated (not all 4s and 5s); current controls honestly assessed; treatment actions name specific tools/technologies.

---

### Deliverable 2: 5×5 Risk Heatmap

**What It Is:** A colour-coded visual matrix plotting all 20+ risks by likelihood (Y-axis) and impact (X-axis), giving CloudSafe's CEO an instant visual of risk concentration.

**Step-by-Step Instructions:**

1. Create a 5×5 grid in Excel/Google Sheets: Likelihood (1–5) on Y-axis, Impact (1–5) on X-axis.
2. Colour code cells: Score 1–4=Green, 5–9=Yellow, 10–16=Orange, 17–25=Red.
3. Plot each risk ID in its inherent position, then show residual position with an arrow or asterisk.
4. Add a legend explaining the colour coding and risk rating definitions.
5. Write a 1-paragraph heatmap narrative in business language: "CloudSafe's heatmap shows [X] Critical and [Y] High risks. The most significant risk cluster is [category]. Three risks remain High or Critical even after applying current controls, requiring priority treatment..."

---

### Deliverable 3: Risk Assessment Report (3–4 pages)

**What It Is:** A professional report presenting findings to CloudSafe's CEO and Head of IT — the document you would present in your first board briefing.

**Step-by-Step Instructions:**

1. **Executive Summary** (half page): Overall posture, top 3 risks with residual scores, immediate actions recommended, budget estimate for top 5 mitigations.

2. **Methodology** (1 page): How risks were identified (stakeholder interviews, documentation review, threat intelligence sources). Reference ISO 27005 and NIST SP 800-30 as methodology foundations. Explain the 5×5 qualitative scoring approach.

3. **Key Findings** (1–2 pages): Top 5 risks in detail — current state, residual score, recommended treatment with specific controls, estimated cost, priority.

4. **Risk Appetite Recommendation**: Recommend a formal risk appetite for CloudSafe's board. Example: "Accept residual risks scored 1–6 with quarterly monitoring. Mandate treatment for all risks scored 7+ within 90 days. Escalate Critical risks (17+) to board within 30 days of identification."

5. **Next Steps**: Monthly register review, quarterly risk committee, 6-month reassessment schedule.

---

### Deliverable 4: Risk Treatment Plan for Top 5 Risks

**What It Is:** A detailed treatment plan for CloudSafe's 5 highest residual risks, including specific controls, estimated cost, and cost-benefit analysis.

**Step-by-Step Instructions:**

1. Select your 5 highest residual-risk-scored items from the register.
2. For each, provide:
   - Risk title and current residual score
   - Treatment option (Mitigate/Accept/Transfer/Avoid) with justification
   - 3–5 specific controls to implement (name tools: CrowdStrike EDR, CyberArk PAM, AWS GuardDuty, etc.)
   - Estimated implementation cost (one-time + annual)
   - Expected residual risk score after treatment
   - Risk reduction calculation: (Inherent Score − Post-Treatment Score) / Inherent Score × 100 = % risk reduction
3. Prioritise treatments in recommended implementation order with a rationale.

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Risk Register Quality | 35% | Specific, calibrated, owned, treated |
| Completeness | 25% | All 4 deliverables submitted |
| Professional Quality | 20% | Board-ready language and formatting |
| Framework Accuracy | 20% | ISO 27005/NIST SP 800-30 methodology applied |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **ISO 27001:2022 Clause 6.1.2** | Risk assessment requirements and process |
| **ISO 27005:2022** | Risk identification, analysis, and evaluation methodology |
| **NIST SP 800-30 Rev 1** | Threat source and threat event identification |
| **NIST CSF 2.0 — GV.RM** | Risk appetite and tolerance statement |
| **NIST CSF 2.0 — ID.RA** | Risk assessment process |

---

## Week-Specific Resources

- [NIST SP 800-30 Rev 1 Full Text](https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final) — Free; read Sections 2–3
- [ISO 27005:2022 Overview](https://www.iso.org/standard/80585.html) — Risk management standard
- [NCSC Cyber Threat Reports](https://www.ncsc.gov.uk/section/keep-up-to-date/threat-reports) — UK threat intelligence
- [ENISA Threat Landscape 2024](https://www.enisa.europa.eu/topics/cyber-threats/enisa-threat-landscape) — Annual EU threat report
- [Verizon DBIR](https://www.verizon.com/business/resources/reports/dbir/) — Annual breach data for probability calibration
- [FAIR Institute: What is FAIR?](https://www.fairinstitute.org/what-is-fair) — Quantitative risk alternative
- [AWS Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/) — Cloud risk scoping
- [NCSC: Cloud Security Guidance](https://www.ncsc.gov.uk/collection/cloud/understanding-cloud-security) — UK guidance for cloud risk

---

## Submission

```
Week-02/Deliverables/
├── CloudSafe-Risk-Register-v1.0.xlsx
├── CloudSafe-Risk-Heatmap-v1.0.xlsx
├── CloudSafe-Risk-Assessment-Report-v1.0.md
└── CloudSafe-Top5-Risk-Treatment-Plan-v1.0.md
```
