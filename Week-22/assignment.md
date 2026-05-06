# Week 22 Assignment: Capstone — Risk Management & Policy Library

## Capstone Overview

| Field | Detail |
|-------|--------|
| **Client** | NovaTech Corp |
| **Your Role** | Lead GRC Consultant |
| **Estimated Time** | 14–18 hours |
| **Difficulty** | 🌟🌟🌟🌟🌟 |
| **Frameworks** | ISO 27001:2022, NIST CSF 2.0, FAIR, PCI-DSS v4.0, UK GDPR |

---

## Capstone Context

Building on your Week 21 governance foundation, this week you execute two of the most critical GRC programme components: a comprehensive risk register and a complete 15-policy library. Together, these deliverables form the analytical and governance backbone of NovaTech's GRC programme.

**Critical continuity requirements with Week 21:**
- Your risk register must use the risk appetite statement from Week 21's governance framework
- Your 15 policies must align to the RACI matrix from Week 21 (correct policy owners)
- Your risk register must use the risk categories referenced in Week 21's GRC Strategy
- The top risks in your register will be referenced in Week 24's board presentation

---

## Deliverable 1: Enterprise Risk Register (30+ Risks)

**What It Is:** NovaTech Corp's complete enterprise information security risk register, serving as the primary risk management tool for monthly Security Steering Group reviews and quarterly board reporting.

**Required risk domains and targets:**

| Domain | Target # Risks | Example Risks |
|--------|---------------|---------------|
| Technology/Cyber | 8 | Ransomware, DDoS, API breach, AWS misconfiguration, AI model attack |
| Third-Party/Supply Chain | 5 | Payment processor breach, AWS outage, supply chain software attack |
| Compliance/Regulatory | 5 | FCA enforcement, PCI-DSS non-compliance, ICO investigation |
| Operational | 4 | Manual processing errors, key person dependency, fraud detection failure |
| Strategic | 3 | Competitive landscape, investor confidence, talent attrition |
| Physical | 2 | Office fire/flood, laptop theft |
| Emerging | 3 | Quantum computing threat to encryption, AI misuse, CBDC transition risk |

**For each risk:**
Risk ID | Risk Title | Risk Category | Risk Description (2–3 sentences, NovaTech-specific) | Threat Source | Asset at Risk | Risk Owner | Likelihood (1–5) | Impact (1–5) | Inherent Score | Inherent Rating | Current Controls | Residual Likelihood | Residual Impact | Residual Score | Residual Rating | FAIR ALE (top 5 only) | Treatment Option | Treatment Actions (specific — name tools/vendors) | Treatment Owner | Target Date | Status

**Required Risk Owners from NovaTech's org:**
- CISO (Raj Singh): Technology and cyber risks
- CFO: Financial and strategic risks
- Head of Legal/DPO: Compliance and regulatory risks
- CTO: Technology infrastructure risks
- Head of Operations: Operational risks

**FAIR Analysis for Top 3 Risks** (build into the register; detail in a separate analysis):

**Risk 1 — Ransomware Attack on NovaTech Payment Processing Platform:**
- Context: UK fintech processing £2.8B annual payment volume; ransomware encrypts payment processing servers; operations halted
- TEF: 12–20 targeted ransomware attempts/year (UK financial sector NCSC data)
- Vulnerability: 8–15% success rate (no PAM; some network segmentation gaps)
- LEF: (16 avg × 11.5% avg) = 1.84 events/year
- Primary Loss: Revenue loss during estimated 5-day outage (£85,000/hour × 120 hours) + incident response (£450K) + restoration (£800K) = £10.4M–£14.2M
- Secondary Loss: FCA enforcement (£8M–£40M), reputational damage/customer attrition (£5M–£25M), litigation (£1M–£5M)
- PLM: £24M–£79M (median £42M)
- ALE: 1.84 × £42M = £77M annualised expected loss
- Control investment case: PAM (£80K investment) reduces vulnerability to 3% → new ALE = 0.48 × £42M = £20M → risk reduction of £57M → ROI 712:1

**Risk 2 — PCI-DSS Cardholder Data Breach via API Vulnerability:**
Complete FAIR analysis following same structure. TEF: 8–15 attempts/year. Vulnerability: 12–20% (API security gaps known from pen test). Primary Loss: PCI-DSS forensics + card replacement costs + revenue loss. Secondary Loss: PCI-DSS fine (up to £500K + card scheme fines), ICO fine (GDPR Art. 33 violation if personal data), reputational.

**Risk 3 — FCA Enforcement for Operational Resilience Failures:**
Unique risk — the threat is regulatory, not a cyberattack. Current state: 3 open FCA findings, no operational resilience programme. Likelihood of FCA enforcement escalation if findings not remediated: 30–60%. Loss if FCA formal notice issued: £5M–£25M fine + reputational damage + potential licence suspension. ALE = 0.45 × £15M = £6.75M.

---

## Deliverable 2: Risk Heatmap

**What It Is:** Visual 5×5 heatmap showing all 30+ risks plotted by residual likelihood × residual impact, colour-coded Critical/High/Medium/Low.

Create in Excel. Plot all risks by Risk ID. Add a heatmap narrative (3–4 sentences): "NovaTech's heatmap shows [X] Critical and [Y] High residual risks. The highest-concentration risk area is [Technology/Cyber] — reflecting the combination of sophisticated threat actors targeting UK fintechs and current control gaps. Priority risk reduction focus: PAM implementation and API security hardening, which address [X] Critical risks simultaneously."

---

## Deliverable 3: Risk Treatment Plan (Top 10 Risks)

**What It Is:** Detailed treatment plans for NovaTech's 10 highest residual risk scores.

For each of the top 10 risks:
- Risk title and current residual score / FAIR ALE
- Treatment option: Mitigate (most will be Mitigate)
- Specific controls: Name 3–5 specific controls with tools, vendors, and estimated costs
- Expected residual risk score after treatment
- Cost-benefit: Investment vs ALE reduction
- Owner and target completion date
- Dependencies (which controls must be in place first)

Priority the 10 treatments in recommended implementation order. Include a budget summary: Total investment in top 10 risk treatments = £[X].

---

## Deliverable 4: Security Policy Library (15 Policies)

**Write all 15 policies in full.** Each policy must be complete — no placeholder text.

**The 15 NovaTech Security Policies:**

**POL-001: Information Security Policy** (MASTER POLICY)
- Scope: All NovaTech employees, contractors, third parties with system access
- Must reference: ISO 27001 Clause 5.2 | PCI-DSS Req 12.1 | UK GDPR Art. 32
- Signed by: CEO Kemi Adeyemi
- Special NovaTech content: Payment data protection commitment, FCA regulatory commitment, ISO 27001 certification commitment

**POL-002: Acceptable Use Policy**
- Must address: company device use, personal software installation prohibition, social media use, cardholder data handling on personal devices (PCI-DSS Req 12.4)
- ISO ref: A.5.10, A.6.2, A.8.1 | PCI-DSS: Req 12

**POL-003: Access Control Policy**
- Must address: least privilege, MFA requirements, privileged access management, quarterly access reviews, PCI-DSS cardholder data access restrictions
- ISO ref: A.5.15–5.22 | PCI-DSS: Req 7, 8 | UK GDPR: Art. 32

**POL-004: Password and Authentication Policy**
- Must specify: minimum 14 characters for standard, 20 characters for admin, MFA mandatory for all system access, PAM requirements for privileged accounts
- ISO ref: A.8.5 | PCI-DSS: Req 8

**POL-005: Incident Response Policy**
- Must include: P1–P4 severity table with payment disruption as P1, GDPR 72-hour breach notification trigger, FCA operational resilience incident reporting, PCI-DSS incident reporting requirements
- ISO ref: A.5.24–5.28 | PCI-DSS: Req 12.10 | UK GDPR: Art. 33–34

**POL-006: Data Classification Policy**
- Must include: 4 levels — Public, Internal, Confidential, Restricted (Cardholder Data is Restricted; patient data if applicable is Restricted)
- PCI-DSS cardholder data specifically addressed as highest classification
- ISO ref: A.5.12–5.13 | PCI-DSS: Req 3

**POL-007: Remote Working Policy**
- Must address: VPN mandatory for all remote access, MFA, home Wi-Fi security requirements, prohibition on accessing cardholder data from public Wi-Fi
- ISO ref: A.6.7 | PCI-DSS: Req 12.5

**POL-008: Vendor Management Policy**
- Must address: vendor tiering, due diligence requirements, DPA requirements (GDPR Art. 28), PCI-DSS service provider requirements (Req 12.8)
- ISO ref: A.5.19–5.22 | PCI-DSS: Req 12.8 | UK GDPR: Art. 28

**POL-009: Business Continuity Policy**
- Must address: FCA PS21/3 operational resilience requirements (important business services, tolerance for disruption), RTO/RPO for payment processing
- ISO ref: A.5.29–5.30 | FCA PS21/3

**POL-010: Cryptography Policy**
- Must address: TLS 1.2+ minimum for cardholder data in transit, AES-256 for cardholder data at rest, key management, prohibition on weak ciphers
- ISO ref: A.8.24–8.25 | PCI-DSS: Req 3, 4

**POL-011: Patch Management Policy**
- Must specify: Critical patches within 48 hours, High within 7 days, Medium within 30 days — applies to all payment processing systems
- ISO ref: A.8.8 | PCI-DSS: Req 6

**POL-012: Change Management Policy**
- Must address: CAB process, emergency change process, testing requirements before production deployment, PCI-DSS change management controls
- ISO ref: A.8.32 | PCI-DSS: Req 6.3

**POL-013: Data Retention and Deletion Policy**
- Must specify: retention periods by data category (PCI-DSS: cardholder data minimum retention 12 months, maximum as required by law; UK GDPR: storage limitation principle)
- ISO ref: A.5.9, A.5.33–5.34 | PCI-DSS: Req 3.1 | UK GDPR: Art. 5(1)(e)

**POL-014: Physical Security Policy**
- Must address: London HQ access controls, data centre access, clean desk policy, secure disposal of payment terminals and devices containing cardholder data
- ISO ref: A.7 | PCI-DSS: Req 9

**POL-015: AI Use Policy**
- Must address: NovaTech's fraud detection AI governance, GDPR Art. 22 automated decision-making requirements, employee use of third-party AI tools (ChatGPT, Copilot), prohibited uses of AI with cardholder data, AI system register requirement
- ISO ref: A.5.1 (policy framework) | UK GDPR: Art. 22 | NIST AI RMF

---

## Deliverable 5: Policy Register

**Create a comprehensive Policy Register spreadsheet:**

Policy ID | Policy Name | Version | Status | Owner (Role) | Approved By | Effective Date | Next Review Date | ISO 27001 Controls Mapped | NIST CSF Functions | PCI-DSS Requirements | GDPR Articles | Training Required | Classification

Complete one row per policy. Ensure consistency with Week 21 RACI (policy owner roles must match).

---

## Deliverable 6: Risk-to-Policy Alignment Matrix

**Create a matrix showing how NovaTech's policies map to risks:**

For each risk (rows), list which policies (columns) contain controls that treat the risk. Mark the primary policy (P) and secondary policies (S).

Include summary statistics: Average policies per risk | Risks with no policy coverage (gaps) | Policies with no risk coverage (orphaned policies)

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Risk Register Completeness | 20% | 30+ risks across all domains; NovaTech-specific |
| FAIR Analysis Quality | 25% | 3 FAIR analyses complete; secondary losses included; calibration cited |
| Policy Library Completeness | 30% | All 15 policies written in full; NovaTech-specific; correct ISO/PCI refs |
| Programme Integration | 25% | Consistent with Week 21 (risk appetite, RACI, org structure); risk-to-policy matrix logical |

---

## Week-Specific Resources

- [FCA Enforcement Actions](https://www.fca.org.uk/news/news-stories/enforcement-action-financial-services) — FAIR calibration for regulatory fines
- [PCI-DSS v4.0 Requirements Document](https://www.pcisecuritystandards.org/document_library/) — Policy alignment requirement detail
- [FAIR Institute: Fintech Risk Examples](https://www.fairinstitute.org/blog) — Calibration for payment sector
- [SANS Policy Templates](https://www.sans.org/information-security-policy/) — Reference for policy structure
- [UK GDPR Art. 5 — Storage Limitation](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/) — Data retention policy context

---

## Submission

```
Capstone-NovaTech/02-Risk-Management/
├── NovaTech-Enterprise-Risk-Register-30Risks-v1.0.xlsx
├── NovaTech-Risk-Heatmap-v1.0.xlsx
├── NovaTech-FAIR-Analysis-Top3-Risks-v1.0.xlsx
└── NovaTech-Risk-Treatment-Plan-Top10-v1.0.xlsx

Capstone-NovaTech/03-Policy-Library/
├── NovaTech-POL-001-Information-Security-Policy-v1.0.md
├── NovaTech-POL-002-Acceptable-Use-Policy-v1.0.md
├── NovaTech-POL-003-Access-Control-Policy-v1.0.md
├── NovaTech-POL-004-Password-Authentication-Policy-v1.0.md
├── NovaTech-POL-005-Incident-Response-Policy-v1.0.md
├── NovaTech-POL-006-Data-Classification-Policy-v1.0.md
├── NovaTech-POL-007-Remote-Working-Policy-v1.0.md
├── NovaTech-POL-008-Vendor-Management-Policy-v1.0.md
├── NovaTech-POL-009-Business-Continuity-Policy-v1.0.md
├── NovaTech-POL-010-Cryptography-Policy-v1.0.md
├── NovaTech-POL-011-Patch-Management-Policy-v1.0.md
├── NovaTech-POL-012-Change-Management-Policy-v1.0.md
├── NovaTech-POL-013-Data-Retention-Deletion-Policy-v1.0.md
├── NovaTech-POL-014-Physical-Security-Policy-v1.0.md
├── NovaTech-POL-015-AI-Use-Policy-v1.0.md
├── NovaTech-Policy-Register-v1.0.xlsx
└── NovaTech-Risk-to-Policy-Alignment-Matrix-v1.0.xlsx
```
