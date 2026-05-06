# Week 23 Assignment: Capstone — Compliance, Audit & Vendor Programs

## Capstone Overview

| Field | Detail |
|-------|--------|
| **Client** | NovaTech Corp |
| **Your Role** | Lead GRC Consultant |
| **Estimated Time** | 14–18 hours |
| **Difficulty** | 🌟🌟🌟🌟🌟 |
| **Frameworks** | ISO 27001:2022, PCI-DSS v4.0, GDPR/UK GDPR, ISO 19011 |

---

## Capstone Context

This week delivers three critical programme components: multi-framework compliance mapping, the internal audit programme, and the vendor risk programme. These components must be internally consistent with Weeks 21–22 deliverables.

**Critical continuity requirements:**
- Compliance matrix must reference NovaTech's 15 policies from Week 22
- Audit programme priority must be based on Week 22 risk register (highest-risk domains audited first)
- Vendor register must use the Vendor Management Policy from Week 22 (POL-008)
- All GDPR findings must connect to the regulatory obligations from Week 21

---

## Deliverable 1: Unified Compliance Matrix (ISO 27001 + PCI-DSS + GDPR)

**What It Is:** NovaTech's master compliance control mapping, showing where each control satisfies ISO 27001, PCI-DSS, and/or GDPR requirements simultaneously.

**Create a comprehensive spreadsheet:**

| Control ID | Control Name | Control Description | ISO 27001 Ref | PCI-DSS Ref | GDPR Ref | Control Owner | Evidence Required | Evidence Source | Status | Gap? |

**Required coverage (minimum 50 controls):**

Ensure coverage of these key mapping areas:

**Access Control block:**
- Quarterly access reviews → ISO A.5.18 | PCI-DSS Req 7.2.4 | GDPR Art. 32
- MFA enforcement → ISO A.8.5 | PCI-DSS Req 8.4 | GDPR Art. 32
- Privileged account management → ISO A.8.2 | PCI-DSS Req 8.2 | —
- Termination access removal → ISO A.6.5 | PCI-DSS Req 8.6 | GDPR Art. 32

**Data Protection block:**
- Encryption at rest (cardholder data) → ISO A.8.24 | PCI-DSS Req 3.5 | GDPR Art. 32
- Encryption in transit → ISO A.8.24 | PCI-DSS Req 4.2 | GDPR Art. 32
- Data classification → ISO A.5.12 | PCI-DSS Req 3.1 | GDPR Art. 5(1)(b)
- Data retention → ISO A.5.33 | PCI-DSS Req 3.2 | GDPR Art. 5(1)(e)

**Incident Management block:**
- IR plan and procedure → ISO A.5.24 | PCI-DSS Req 12.10 | GDPR Art. 33
- Breach detection → ISO A.5.25 | PCI-DSS Req 10.7 | GDPR Art. 33
- Breach notification to regulator → ISO A.5.26 | PCI-DSS Req 12.10.5 | GDPR Art. 33 (72hr)
- Post-incident review → ISO A.5.27 | PCI-DSS Req 12.10.7 | —

**Monitoring and Logging block:**
- Logging enabled for all systems → ISO A.8.15 | PCI-DSS Req 10.2 | GDPR Art. 32
- Log review → ISO A.8.16 | PCI-DSS Req 10.4 | —
- Alerting on anomalies → ISO A.8.16 | PCI-DSS Req 10.7 | —

**Vendor Management block:**
- Vendor security assessment → ISO A.5.19 | PCI-DSS Req 12.8 | GDPR Art. 28
- DPA with processors → ISO A.5.20 | — | GDPR Art. 28
- Vendor monitoring → ISO A.5.22 | PCI-DSS Req 12.8.4 | GDPR Art. 28(3)(h)

**Add a summary dashboard tab:**
- Total controls in matrix
- % satisfying all 3 frameworks
- % satisfying 2 frameworks
- % single-framework only
- Efficiency ratio: Controls addressing all 3 frameworks / total controls
- Framework coverage: ISO 27001 % Annex A covered | PCI-DSS % requirements covered | GDPR % key articles covered

---

## Deliverable 2: ISO 27001 Gap Assessment (Full 93 Controls)

**What It Is:** NovaTech's formal ISO 27001:2022 gap assessment covering all 93 Annex A controls, scored 0–5 maturity, forming the basis for the ISO 27001 certification roadmap.

**Critical requirement:** NovaTech is immature — most controls should be scored 0–2 given the scenario context. Be honest. An inflated gap assessment will not match a credible certification roadmap.

**Apply these realities to your scoring:**
- A.5.1 (IS Policies): Score 2 — policies exist (from Week 22) but just written; not yet communicated or trained
- A.5.9 (Asset inventory): Score 1 — no formal inventory; partial spreadsheets
- A.5.18 (Access rights): Score 1 — no formal access reviews; no PAM
- A.5.24–5.28 (Incident management): Score 1 — no formal IR programme
- A.8.2 (Privileged access): Score 0 — no PAM; unrestricted admin access
- A.8.8 (Vulnerability management): Score 2 — some patching; no formal programme
- A.8.15 (Logging): Score 2 — AWS CloudTrail; not reviewed
- A.7 (Physical controls): Score 3 — office access controls reasonable; no visitor log
- A.6.3 (Security awareness training): Score 1 — annual training; not documented

**For each control:**
Control Ref | Control Name | Domain | Maturity Score (0–5) | Current State | Gap Description | Priority (Critical/High/Medium/Low) | Effort to Remediate | Owner | Target Date | ISO 27001 Certification Impact

**Summary dashboard:**
- Average maturity by domain (Organizational, People, Physical, Technological)
- % at Level 0, 1, 2, 3, 4, 5
- Priority distribution: Critical/High/Medium/Low gap count
- Top 10 critical gaps (automatically calculated)
- Minimum maturity required for ISO 27001 Stage 1: describe what readiness looks like

---

## Deliverable 3: Audit Charter and Annual Audit Programme

**Audit Charter:**
Write NovaTech's Internal Security Audit Charter (co-sourced with KPMG). Must include: purpose, authority (Board Risk & Audit Committee signatory), independence (KPMG team independent of NovaTech CISO), scope, responsibilities, methodology (ISO 19011), reporting line, and annual programme approval process.

**Annual Audit Programme (12-Month Plan for 2025):**

Create a structured 12-month audit calendar showing 6 planned audits:

| Audit # | Domain | Scope | ISO 27001 Criteria | Planned Month | Duration | Auditor | Risk Basis |
|---------|--------|-------|-------------------|---------------|----------|---------|------------|
| AU-2025-01 | Access Control and Identity Management | All corporate systems (AD, Azure, Salesforce) | A.5.15–5.22, A.8.2, A.8.5 | Q1 Month 2 | 5 days | KPMG | Highest risk per register: 4 Critical access risks |
| AU-2025-02 | Patch and Vulnerability Management | All in-scope systems | A.8.8, A.8.20 | Q2 Month 1 | 3 days | Internal + KPMG | PCI-DSS Req 6 requirement |
| AU-2025-03 | Incident Response Programme | IR Plan, playbooks, training | A.5.24–5.28 | Q2 Month 3 | 4 days | KPMG | FCA finding: no IR programme |
| AU-2025-04 | Vendor Management | Top 5 Tier 1 vendors | A.5.19–5.22 | Q3 Month 1 | 5 days | Internal | Vendor risk concentration |
| AU-2025-05 | ISO 27001 Pre-Certification Audit | Full ISMS | ISO 27001 Clauses 4–10 + Annex A | Q3 Month 3 | 10 days | KPMG | Pre-Stage 2 readiness |
| AU-2025-06 | Data Protection (GDPR) | All processing activities | ISO A.5.34 + GDPR | Q4 Month 1 | 4 days | KPMG | ICO compliance requirement |

For each audit: detailed audit objectives, evidence to be collected, sample sizes, reporting timeline, escalation path for critical findings.

---

## Deliverable 4: Vendor Risk Register (NovaTech Full Vendor Landscape)

**Create NovaTech's complete vendor risk register:**

| Vendor ID | Vendor Name | Service | Data Accessed | Tier | Country | DPA Signed? | Last Assessment | Current Risk Rating | Assessment Due |
|-----------|-------------|---------|--------------|------|---------|-------------|-----------------|---------------------|---------------|

**Include at minimum 15 vendors:**
- CloudPay Ltd. (Tier 1 — payment processor; never assessed)
- Microsoft Azure/M365 (Tier 1 — identity/cloud; SOC 2 review)
- DataInsights Analytics (Tier 1 — customer data analytics; US-based; HIGH risk)
- LegalEagle LLP (Tier 2 — legal counsel)
- TalentBridge HR (Tier 2 — HR SaaS; 2,000 employee records)
- AWS (Tier 1 — cloud infrastructure; review published SOC 2)
- Salesforce (Tier 2 — CRM; customer contact data)
- GitHub (Tier 2 — source code; NovaTech IP)
- Slack (Tier 3 — internal comms; limited sensitive data)
- KnowBe4 (Tier 3 — security training; employee emails)
- Vanta (Tier 2 — GRC platform; compliance data)
- KPMG (Tier 2 — internal audit co-source; significant access to internal docs)
- BSI (Tier 2 — ISO 27001 certification body; access to ISMS documentation)
- PenTest Partners (Tier 1 — penetration testing firm; significant network/system access)
- Emergency Recovery Inc. (Tier 3 — off-site backup media storage)

**Risk rate each vendor:** Critical/High/Medium/Low based on data processed, tier, assessment age, and known gaps.

---

## Deliverable 5: Five Completed Vendor Risk Assessment Questionnaires

**Complete VRAQs for these 5 vendors** using the Vendor-Risk-Assessment-Questionnaire-Template.md from /Templates/:

**1. CloudPay Ltd.** (Payment Processor — Tier 1, Critical)
VRAQ completed as if CloudPay responded. Findings to incorporate:
- SOC 2 Type II certified: YES (include report date)
- PCI-DSS Level 1 Service Provider: YES
- Breach notification SLA: 72 hours to NovaTech
- Penetration test: Annual; last test 14 months ago (FINDING: approaching 18-month threshold)
- Sub-processors: 2 undisclosed sub-processors handling card tokenisation (FINDING: NovaTech must approve sub-processors per GDPR Art. 28)
- Overall: APPROVE WITH CONDITIONS (sub-processor disclosure required within 30 days)

**2. DataInsights Analytics** (US Analytics — Tier 1, High Risk)
Findings to incorporate:
- No ISO 27001 or SOC 2 certification (CRITICAL FINDING)
- Data processed in US-East-1 (CRITICAL FINDING: international transfer; no SCCs in current contract)
- Penetration test: Last conducted 22 months ago (FINDING: past annual requirement)
- Encryption: at rest confirmed (AES-256); in transit confirmed (TLS 1.3)
- Breach notification: 5 business days (FINDING: GDPR requires prompt notification to enable 72-hr ICO deadline)
- Sub-processors: Not disclosed
- Overall: DO NOT APPROVE — halt data transfer pending SCC execution and remediation plan

**3. LegalEagle LLP** (Legal Counsel — Tier 2)
Limited VRAQ (law firm — professional privilege limits what can be asked):
- ISO 27001: Not certified; Cyber Essentials Plus certified
- Data handled: Privileged legal correspondence only; no customer personal data
- Risk: Medium — data sensitivity is high but limited scope
- Overall: APPROVE with annual Cyber Essentials Plus renewal requirement

**4. TalentBridge HR** (HR SaaS — Tier 2)
Findings:
- ISO 27001 certified (current certificate)
- SOC 2 Type II: In progress (expected Q3 this year)
- Penetration test: 8 months ago; findings remediated
- MFA: Enforced for all admin access
- GDPR: DPA in place; UK data centre only (eu-west-1)
- Data retention: 7-year employee data retention (aligned to UK employment law)
- Overall: APPROVE

**5. PenTest Partners** (Penetration Testing — Tier 1)
Special consideration: pen testers have deep network/system access during testing
- CREST certified penetration testing firm
- ISO 27001 certified
- Background checks on all testers
- All work under NDA and rules of engagement
- Penetration test scope documented before engagement starts
- Overall: APPROVE with enhanced controls during test windows (CISO monitoring)

---

## Deliverable 6: Compliance Evidence Tracker

**What It Is:** A master tracker for all compliance evidence NovaTech must collect and maintain across ISO 27001, PCI-DSS, and GDPR.

**Create a spreadsheet:**

Evidence ID | Framework | Requirement Reference | Evidence Description | Evidence Type (Document/Screenshot/Log/Certificate) | Collection Frequency | Collection Owner | Storage Location (Vanta) | Last Collected | Next Due | Status

**Include minimum 40 evidence items** covering:
- ISO 27001 mandatory evidence (Clause 7.5 documented information requirements)
- PCI-DSS Req 10 (log monitoring evidence), Req 11 (scan results, pen test reports), Req 12 (policy review records)
- GDPR evidence (RoPA, DPIA register, SAR log, DPA register, consent records)

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Unified Compliance Matrix | 25% | 50+ controls; accurate ISO/PCI/GDPR mappings; gaps identified |
| ISO 27001 Gap Assessment | 25% | 93 controls assessed; realistic maturity scores; NovaTech-specific |
| Audit Programme | 20% | 6 audits planned; risk-sequenced; resourced; consistent with governance |
| Vendor Assessments | 30% | All 5 VRAQs completed; realistic findings; DataInsights flagged as high risk |

---

## Week-Specific Resources

- [PCI-DSS v4.0 Full Requirements](https://www.pcisecuritystandards.org/document_library/) — Mapping source
- [ISO 27001 Annex A Controls List](https://www.iso.org/standard/27001) — Gap assessment reference
- [GDPR Article 28 — ICO Guidance](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/accountability-and-governance/accountability-framework/using-processors/)
- [ISO 19011:2018 Audit Guidelines](https://www.iso.org/standard/70017.html) — Audit programme standards
- [NCSC: Supply Chain Security](https://www.ncsc.gov.uk/collection/supply-chain-security)
- [Microsoft Trust Center — Azure Compliance](https://www.microsoft.com/en-us/trust-center/compliance/compliance-overview)

---

## Submission

```
Capstone-NovaTech/04-Compliance-Mapping/
├── NovaTech-Unified-Compliance-Matrix-ISO-PCI-GDPR-v1.0.xlsx
├── NovaTech-ISO27001-Gap-Assessment-93Controls-v1.0.xlsx
└── NovaTech-Compliance-Evidence-Tracker-v1.0.xlsx

Capstone-NovaTech/05-Audit-Program/
├── NovaTech-Internal-Audit-Charter-v1.0.md
└── NovaTech-Annual-Audit-Programme-2025-v1.0.xlsx

Capstone-NovaTech/06-Vendor-Risk/
├── NovaTech-Vendor-Risk-Register-v1.0.xlsx
├── NovaTech-VRAQ-CloudPay-v1.0.xlsx
├── NovaTech-VRAQ-DataInsights-Analytics-v1.0.xlsx
├── NovaTech-VRAQ-LegalEagle-LLP-v1.0.xlsx
├── NovaTech-VRAQ-TalentBridge-HR-v1.0.xlsx
└── NovaTech-VRAQ-PenTest-Partners-v1.0.xlsx
```
