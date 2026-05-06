# Week 17 Assignment: Enterprise Risk Assessment Program

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | GlobalBank PLC |
| **Your Role** | Senior GRC Analyst / Risk Specialist |
| **Estimated Time** | 10–14 hours |
| **Difficulty** | 🌟🌟🌟🌟🌟 |
| **Frameworks** | ISO 27005:2022, FAIR Model, ISO 27001:2022 |

---

## Scenario Brief — Read This Carefully

**GlobalBank PLC** is a major UK retail and commercial bank regulated by both the FCA (Financial Conduct Authority) and the PRA (Prudential Regulation Authority). They have 8,000 employees, 400 branches, 9 million personal banking customers, and £85 billion in assets under management. Their technology estate includes: a mainframe core banking system (IBM z/OS), a cloud-hosted digital banking platform (AWS eu-west-2), 8,000 Windows endpoints, Office 365, Salesforce, and a complex network of 3rd party integrations including SWIFT for international payments.

The Bank's new Chief Risk Officer (CRO), Helen Nakamura, has commissioned a complete overhaul of their Enterprise Information Security Risk Assessment Programme. The FCA's DORA (Digital Operational Resilience Act) requirements have increased the regulatory bar for operational risk quantification. The PRA has also requested that GlobalBank provide quantified estimates of their top 5 cyber risks as part of the annual ICAAP (Internal Capital Adequacy Assessment Process) — meaning cyber risks must be expressed in financial terms that feed into capital adequacy calculations.

Helen has tasked you with: (1) designing the enterprise risk methodology, (2) applying the FAIR model to GlobalBank's top 3 cyber risks, (3) producing a risk appetite and tolerance statement, and (4) building a risk register with 25+ risks.

**GlobalBank's known risk context:**
- Ransomware targeting financial institutions increasing 40% year-over-year (NCSC data)
- Core banking mainframe: last security assessment 18 months ago; privileged access unmanaged
- SWIFT integration: nation-state actor targeting of SWIFT system has been published by NCSC
- 3rd party risk: 15 critical vendors, 3 of which have not been assessed in over 2 years
- Insider threat: 3 suspicious access anomalies flagged by SIEM in the last 6 months; all investigated and closed
- Cloud security: AWS Security Hub score 73% (NIST CSF benchmark); 47 High findings open
- GDPR: 9 million customer records; data retention practices under ICO review

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 17 — especially the FAIR model calculation
- [ ] Download and read the FAIR Institute's FAIR introduction at fairinstitute.org
- [ ] Read ISO 27005:2022 overview
- [ ] Review Verizon DBIR 2024 financial sector section for threat frequency calibration

### Questions to Answer Before Starting
1. What is the difference between Annual Loss Expectancy (ALE) and Probable Loss Magnitude (PLM)?
2. GlobalBank has 9 million customers whose data could be breached. At GDPR maximum fine (4% of global annual turnover), what is the theoretical maximum regulatory fine if a material breach occurred?
3. DORA (Digital Operational Resilience Act) requires what from financial institutions regarding ICT risk quantification?
4. What is a risk appetite statement and who at GlobalBank should approve it?
5. Why must GlobalBank include secondary losses (regulatory fines, litigation) in their FAIR analysis?

---

## Deliverables

### Deliverable 1: Enterprise Risk Methodology Document

**What It Is:** GlobalBank's formal methodology for conducting information security risk assessments — the document that standardises how all risk assessments are conducted across the bank.

**Must include:**
1. **Purpose and scope**: Enterprise-wide; all IS risks to GlobalBank's information assets, technology systems, and operations
2. **Risk assessment approach**: Hybrid — qualitative for full risk register (ISO 27005 aligned); quantitative FAIR for top 10 risks (ICAAP and board reporting)
3. **Risk identification process**: Sources (threat intelligence, penetration tests, audit findings, industry reports, incident data), stakeholder interviews, threat library
4. **Qualitative scoring methodology**: 5×5 likelihood × impact matrix with detailed definitions for each level:
   - Likelihood 1–5 definitions customised for a major bank (Tier 1 bank faces different probabilities than an SMB)
   - Impact 1–5 across 5 dimensions: Financial, Operational, Reputational, Regulatory, Customer Impact
5. **Quantitative FAIR methodology**: When applied, data sources for calibration, who conducts analysis, tools used (RiskLens or manual FAIR)
6. **Risk categorisation**: IS, Operational, Compliance, Third-Party, Technology, Regulatory, Physical
7. **Risk appetite integration**: How risk register ratings map to GlobalBank's risk appetite
8. **Risk treatment options**: Mitigate (with specific control recommendations), Accept (documentation requirements), Transfer (cyber insurance parameters), Avoid
9. **Review cadence**: Monthly risk committee; quarterly CISO board report; annual full reassessment; triggered reviews on incidents/changes
10. **Roles**: CRO (approve methodology), CISO (IS risk lead), Risk Owners (business line heads), Internal Audit (3rd line review)

---

### Deliverable 2: FAIR Analysis for Top 3 Risks

**What It Is:** Quantitative FAIR analysis for GlobalBank's 3 highest-priority risks, expressed in financial terms suitable for ICAAP submission.

**Risk 1 — Ransomware Targeting Core Banking Systems**

*Step through the full FAIR calculation:*

**Context**: Ransomware group targets GlobalBank's core banking mainframe (IBM z/OS). Successful attack encrypts production systems, halting banking operations.

**Threat Event Frequency (TEF)**: Based on NCSC data for major UK financial institutions, ~15–25 ransomware targeting attempts per year. Use range: 15–25 attempts/year.

**Vulnerability (V)**: Given GlobalBank's current controls (no PAM on mainframe, some network segmentation, EDR on Windows but not mainframe), estimate: 6–12% of attempts succeed.

**Loss Event Frequency (LEF)**: TEF × V = (15–25) × (6–12%) = 0.9–3.0 events/year. Median: ~1.8 events/year.

**Primary Loss Magnitude**:
- Revenue loss during estimated 7-day core banking outage: 8M customers × average daily transaction fee revenue × 7 days
- Customer compensation costs
- Incident response and forensics: £500K–£2M
- Restoration costs: £1M–£4M
- Ransom demand (if applicable): £1M–£10M

**Secondary Loss Magnitude**:
- FCA/PRA regulatory fine for operational resilience failure under DORA: £5M–£50M (historical FCA fines as calibration)
- PRA capital requirement increase
- Reputational damage: customer attrition (estimate: 2–5% of 9M customers close accounts at average £150 lifetime value)
- Litigation from affected customers
- SWIFT network suspension costs

**Probable Loss Magnitude (PLM)**: £18M–£65M (median: ~£32M)

**Annual Loss Expectancy (ALE)**: LEF × PLM = 1.8 × £32M = £57.6M annualised expected loss

**Control investment evaluation**: PAM for mainframe at £2.5M reduces vulnerability from 9% to 2%. New LEF = 0.45. New ALE = 0.45 × £32M = £14.4M. Risk reduction: £43.2M. ROI: 17:1.

**Write up all 3 FAIR analyses** (Risk 2 = SWIFT system compromise by nation-state actor; Risk 3 = Insider data theft by authorised user) using the same structured format as Risk 1. Calibrate using appropriate threat data for each scenario.

---

### Deliverable 3: Risk Appetite and Risk Tolerance Statement

**What It Is:** GlobalBank's formal risk appetite statement — the document approved by the Board Risk Committee that defines how much cybersecurity risk GlobalBank is willing to accept.

**Must include:**
1. **Risk appetite statement** (board-level, qualitative + quantitative):
   "GlobalBank maintains a LOW appetite for information security risks that could result in loss of customer data, disruption to core banking services, or regulatory non-compliance. The Board sets a maximum tolerable information security risk exposure of [£X]M in annualised expected loss terms. Individual risks exceeding [£Y]M ALE require Board Risk Committee approval before acceptance."

2. **Risk tolerance bands by category**:
   - Customer data confidentiality risks: Zero tolerance for GDPR-notifiable breaches
   - Core banking availability: Maximum acceptable downtime of 2 hours in any rolling 12-month period
   - Regulatory compliance: Zero tolerance for regulatory enforcement actions
   - Financial loss from cyber incidents: Maximum tolerable ALE of [define an appropriate figure]

3. **Risk escalation thresholds**: At what ALE does a risk escalate from CISO to CRO to Board?

4. **Approved by**: Board Risk Committee (signatory block)

---

### Deliverable 4: Enterprise Risk Register (25+ Risks)

**What It Is:** GlobalBank's enterprise IS risk register with 25+ risks across all domains, with both qualitative scoring and FAIR-based ALE for the top 5 risks.

**Columns:**
Risk ID | Risk Title | Risk Category | Threat Source | Asset at Risk | Current Controls | Likelihood (1–5) | Impact (1–5) | Inherent Score | Inherent Rating | Residual Likelihood | Residual Impact | Residual Score | Residual Rating | FAIR ALE (top 5 only) | Treatment | Treatment Actions | Risk Owner | Review Date | Status

**Risk categories to cover (aim for 4–5 risks per category):**
- Technology/Cyber: Ransomware, SWIFT compromise, DDoS, cloud misconfiguration, zero-day exploitation
- Third-Party: Critical vendor breach, vendor access misuse, software supply chain attack
- Insider: Privileged user data theft, accidental data exposure, rogue IT administrator
- Compliance: GDPR enforcement action, FCA operational resilience investigation, PCI-DSS non-compliance
- Physical: Data centre fire, physical security breach at branch, device theft
- Emerging: AI model poisoning (if GlobalBank uses AI for fraud detection), quantum computing threat to encryption

Include the 3 FAIR-analysed risks in the register with their quantified ALE values.

---

### Deliverable 5: Risk Treatment Plan with Cost-Benefit Analysis

**What It Is:** A detailed treatment plan for GlobalBank's top 5 risks, with cost-benefit analysis justifying investment decisions.

For each top 5 risk:
- Risk title and current residual score / ALE
- Selected treatment: Mitigate
- Specific controls to implement (name tools, vendors, technologies)
- Implementation cost
- Expected reduction in vulnerability
- New estimated ALE after controls
- ALE reduction (benefit)
- Cost-benefit ratio (ALE reduction ÷ investment cost)
- Recommendation: Proceed / Consider / Do not proceed

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Methodology Quality | 20% | Comprehensive; FAIR integrated; roles defined |
| FAIR Analysis Accuracy | 35% | Calculations correct; estimates calibrated with data sources; secondary losses included |
| Risk Register | 25% | 25+ risks; correctly scored; FAIR ALE for top 5 |
| Risk Appetite Statement | 20% | Specific; quantified; appropriate for a major bank |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **FAIR Model** | Quantitative risk analysis for top 3 risks |
| **ISO 27005:2022** | Risk assessment methodology framework |
| **ISO 27001:2022** | Risk treatment and risk register format |
| **FCA/PRA DORA** | Regulatory context requiring operational risk quantification |

---

## Week-Specific Resources

- [FAIR Institute: Introduction to FAIR](https://www.fairinstitute.org/what-is-fair) — Free methodology overview
- [Open FAIR Body of Knowledge](https://www.opengroup.org/forum/open-fair-forum) — Open standard FAIR documentation
- [ISO 27005:2022 Overview](https://www.iso.org/standard/80585.html) — Risk management standard
- [Verizon DBIR 2024 — Financial Sector](https://www.verizon.com/business/resources/reports/dbir/) — Threat frequency calibration
- [FCA: Operational Resilience Guidance](https://www.fca.org.uk/firms/operational-resilience) — DORA context
- [NCSC: UK Financial Sector Threat Intelligence](https://www.ncsc.gov.uk/sector/finance) — UK financial sector threats
- [RiskLens: FAIR Analysis Examples](https://www.risklens.com/resources) — FAIR calculation examples

---

## Submission

```
Week-17/Deliverables/
├── GlobalBank-Enterprise-Risk-Methodology-v1.0.md
├── GlobalBank-FAIR-Analysis-Top3-Risks-v1.0.xlsx
├── GlobalBank-Risk-Appetite-Statement-v1.0.md
├── GlobalBank-Enterprise-Risk-Register-25Risks-v1.0.xlsx
└── GlobalBank-Risk-Treatment-Cost-Benefit-Analysis-v1.0.xlsx
```
