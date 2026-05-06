# Week 08 Assignment: Vendor Risk Management

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | DataBridge Corp |
| **Your Role** | GRC Analyst — Vendor Risk |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟🌟 |
| **Frameworks** | ISO 27001 (A.5.19–5.22), SOC 2 (CC9), GDPR (Art. 28) |

---

## Scenario Brief — Read This Carefully

**DataBridge Corp** is a 400-person UK data analytics company that helps FTSE 100 clients extract insights from their business data. DataBridge processes highly sensitive commercial and personal data on behalf of its clients — market research, customer behaviour analytics, and financial modelling. As a data processor under GDPR, DataBridge must ensure that its own sub-processors (vendors) meet adequate security standards.

DataBridge is currently onboarding three new critical vendors:
1. **CloudMatrix Analytics** — A US-based AI analytics platform that will process DataBridge's client data to generate ML insights. High risk: processes personal data; data leaves the UK to US servers.
2. **SecureVault Ltd.** — A UK cloud backup provider that will store encrypted backups of DataBridge's production data. Medium-high risk: stores sensitive data but doesn't process or access it.
3. **TalentSphere HR** — A SaaS HR platform managing DataBridge's 400 employee records including salary, performance reviews, and personal data. Medium risk: employee data only.

Additionally, an existing vendor — **TechSupport Pro** — provides 24/7 remote desktop support to DataBridge's clients. This vendor has not been assessed in 3 years despite having access to client environments.

The Head of Legal has flagged that DataBridge's GDPR obligations as a data processor require formal due diligence on all sub-processors (GDPR Art. 28). The CISO has flagged that several previous incidents (SolarWinds, Kaseya) demonstrate the extreme risk of trusted vendor access to client environments. You are tasked with building DataBridge's vendor risk management programme and conducting the first four vendor assessments.

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 8 — vendor risk framework and GDPR Art. 28
- [ ] Read ISO 27001 controls A.5.19, A.5.20, A.5.21, A.5.22 (Supplier relationships)
- [ ] Review the Vendor Risk Assessment Questionnaire Template in `/Templates/`
- [ ] Read GDPR Article 28 at gdpr-info.eu — Data Processor obligations

### Questions to Answer Before Starting
1. Under GDPR Art. 28, what contractual obligations must DataBridge place on sub-processors?
2. How would you tier CloudMatrix Analytics (US AI platform processing EU personal data) vs TalentSphere HR (employee SaaS)?
3. What is a "right to audit" clause and why does DataBridge need it in its vendor contracts?
4. TechSupport Pro has remote access to DataBridge client environments. What makes this vendor particularly high-risk?
5. What ISO 27001 controls specifically address supplier and third-party risk?

---

## Deliverables

### Deliverable 1: Vendor Risk Management Policy

**What It Is:** A formal policy governing how DataBridge manages security risk in its vendor relationships.

**Must include:**
- Purpose and scope (all third parties with access to DataBridge systems or data)
- Vendor tiering model: Tier 1 (Critical — process/access personal data, critical systems access), Tier 2 (High — significant data access), Tier 3 (Standard — limited access), Tier 4 (Low — no data access)
- Due diligence requirements by tier (Tier 1: full VRAQ + right to audit + annual review; Tier 4: contract terms only)
- Minimum security requirements for all vendors
- Contractual requirements (DPA requirements under GDPR Art. 28; security clauses; breach notification requirements)
- Ongoing monitoring requirements
- Vendor offboarding requirements
- Policy owner: Head of Legal/CISO (joint); review: annual

---

### Deliverable 2: Vendor Risk Register (All Vendors Including New)

**What It Is:** A structured register of all DataBridge vendors with risk tiering and assessment status.

**Create a spreadsheet with:**
- Vendor Name | Service Description | Data Accessed | Data Classified (Personal/Confidential/Commercial) | Tier (1–4) | Countries of Operation | Last Assessment Date | Assessment Due Date | Current Risk Rating | Remediation Status | Contract Expiry | DPA Signed? | Right to Audit? | Contact

**Populate with:**
- CloudMatrix Analytics (US AI platform) — Tier 1
- SecureVault Ltd. (UK backup) — Tier 2
- TalentSphere HR (HR SaaS) — Tier 2
- TechSupport Pro (remote support, 3yr no assessment) — Tier 1
- Add 4 additional fictional vendors to reach 8 total (e.g., Microsoft 365, AWS, legal firm, office supplies — tier appropriately)

**Risk rate each vendor:** Critical/High/Medium/Low based on data accessed, tier, assessment age, and known gaps.

---

### Deliverable 3: Completed Vendor Risk Assessment Questionnaires (3 of 4 vendors)

**What It Is:** Completed VRAQs for CloudMatrix Analytics, SecureVault Ltd., and TalentSphere HR using the template in `/Templates/Vendor-Risk-Assessment-Questionnaire-Template.md`.

**For each VRAQ:**
1. Complete all sections of the VRAQ template as if you had received their responses (fabricate realistic answers — some should show gaps)
2. Calculate a risk score for each section and overall
3. Identify top 3 findings/gaps per vendor
4. Make a recommendation: Approve to onboard / Approve with conditions / Do not approve

**Specific scenarios to incorporate:**
- **CloudMatrix Analytics**: Their VRAQ reveals they are SOC 2 Type II certified but have no specific controls for UK data residency. They process data in US-East-1 only. GDPR international transfer risk (no SCCs in contract yet). Score: High overall.
- **SecureVault Ltd.**: ISO 27001 certified; good security posture; gap found in their incident notification SLA (they commit to 72 hours but GDPR requires they notify DataBridge promptly enough for DataBridge to meet their own 72hr ICO obligation). Score: Medium.
- **TalentSphere HR**: No ISO 27001 or SOC 2; they provide a security questionnaire self-assessment only; encryption at rest unconfirmed; penetration test last conducted 18 months ago. Score: High with conditions.

---

### Deliverable 4: Vendor Risk Matrix

**What It Is:** A visual risk matrix showing all 8 vendors plotted by: data criticality (Y-axis) and security posture (X-axis), colour-coded by risk rating.

**Instructions:**
1. Plot all 8 vendors on a 3×3 or 4×4 matrix
2. X-axis: Vendor Security Posture (Weak / Moderate / Strong)
3. Y-axis: Data/Access Criticality (Low / Medium / High / Critical)
4. Colour code: High criticality + Weak posture = Red (immediate action); Low criticality + Strong posture = Green
5. Write a 1-paragraph narrative identifying which vendors require immediate attention

---

### Deliverable 5: Vendor Remediation Tracker

**What It Is:** A structured tracker for following up on gaps identified in vendor assessments.

**For each gap found across all vendors:**
- Vendor name | Gap description | Risk level | Required remediation | Vendor-committed deadline | DataBridge escalation option if not remediated | Status

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| VRAQ Completeness | 30% | VRAQs fully completed; realistic gaps incorporated |
| Policy Quality | 25% | GDPR Art. 28 correctly reflected; tiering model practical |
| Risk Register Accuracy | 25% | Vendors correctly tiered; risk ratings justified |
| Professional Quality | 20% | Board-ready documents; correct terminology |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **ISO 27001:2022 A.5.19–5.22** | Supplier relationship controls |
| **SOC 2 CC9** | Vendor and supply chain risk criteria |
| **GDPR Article 28** | Data Processor obligations and DPA requirements |

---

## Week-Specific Resources

- [GDPR Article 28 Full Text — gdpr-info.eu](https://gdpr-info.eu/art-28-gdpr/) — Data processor obligations
- [ICO: Using Processors](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/accountability-and-governance/accountability-framework/using-processors/) — UK GDPR guidance on sub-processors
- [ISO 27001:2022 A.5.19–5.22 Overview](https://www.iso.org/standard/27001) — Supplier security controls
- [NCSC: Supply Chain Security](https://www.ncsc.gov.uk/collection/supply-chain-security) — UK supply chain guidance
- [CISA: Supply Chain Risk Management](https://www.cisa.gov/supply-chain-risk-management) — US guidance relevant to US vendor (CloudMatrix)
- [SolarWinds Incident Post-Mortem](https://www.ncsc.gov.uk/news/joint-advisory-on-sunburst-malware) — Why vendor risk matters in practice

---

## Submission

```
Week-08/Deliverables/
├── DataBridge-Vendor-Risk-Management-Policy-v1.0.md
├── DataBridge-Vendor-Risk-Register-v1.0.xlsx
├── DataBridge-VRAQ-CloudMatrix-Analytics-v1.0.xlsx
├── DataBridge-VRAQ-SecureVault-Ltd-v1.0.xlsx
├── DataBridge-VRAQ-TalentSphere-HR-v1.0.xlsx
├── DataBridge-Vendor-Risk-Matrix-v1.0.xlsx
└── DataBridge-Vendor-Remediation-Tracker-v1.0.xlsx
```
