# Week 04 Assignment: Introduction to Compliance Programs

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | PaySafe Corp |
| **Your Role** | Compliance Analyst |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟 |
| **Frameworks** | PCI-DSS v4.0, GDPR / UK GDPR |

---

## Scenario Brief — Read This Carefully

**PaySafe Corp** is a UK-based payment processing company, processing approximately £3.2 billion in payment card transactions annually on behalf of 50,000 UK retailers. They are headquartered in Leeds with 320 employees. Their systems include: a web-based merchant portal, a payment gateway API that retailers integrate into their websites, two primary databases storing transaction records, and a data analytics platform that processes historical transaction data for merchant reporting.

PaySafe handles **cardholder data** (Primary Account Numbers, expiry dates) and processes **personal data** for both merchant contacts and their end-customer payment records. Their merchant customers range from independent retailers to mid-sized e-commerce businesses.

PaySafe's annual external QSA (Qualified Security Assessor) audit is in **5 months**. Their last PCI-DSS assessment (v3.2.1) flagged 12 non-conformances. The QSA has notified them that this assessment will be conducted against PCI-DSS v4.0 — and several requirements have changed. Additionally, the ICO (Information Commissioner's Office) has sent PaySafe a formal questionnaire following a third-party complaint about their data retention practices. PaySafe's Head of Compliance has resigned unexpectedly. You have been brought in as an interim Compliance Analyst to stabilise the programme.

**Immediate context:**
- 5 months until PCI-DSS v4.0 QSA audit
- ICO questionnaire must be responded to within 30 days
- 12 open PCI-DSS non-conformances from the last assessment
- Data retention practices flagged by ICO — unclear if a retention policy exists
- No Record of Processing Activities (RoPA) documented
- DPO appointed but part-time and has limited capacity
- Customer Subject Access Request (SAR) response process is informal

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 4 — especially the GDPR articles and PCI-DSS requirements sections
- [ ] Download PCI-DSS v4.0 Quick Reference Guide from pcisecuritystandards.org
- [ ] Read the ICO's "What is a RoPA?" guide at ico.org.uk
- [ ] Read GDPR Articles 5, 6, 30, 33, 34, and 35 at gdpr-info.eu

### Questions to Answer Before Starting
1. Does PaySafe need to comply with PCI-DSS? Under which merchant level?
2. PaySafe stores PAN (Primary Account Numbers) in their database. Under PCI-DSS, what encryption requirements apply?
3. Under GDPR Article 30, who is required to maintain a Record of Processing Activities?
4. The ICO questionnaire arrives about data retention. What GDPR principle governs how long data can be kept?
5. A merchant calls PaySafe asking for all personal data PaySafe holds about them under GDPR Article 15. What is the deadline for responding?

---

## Deliverables

### Deliverable 1: PCI-DSS v4.0 Gap Assessment

**What It Is:** A structured assessment of PaySafe's current compliance with all 12 PCI-DSS v4.0 requirements, identifying gaps, risk ratings, and remediation priorities before the QSA audit.

**Step-by-Step Instructions:**

1. Create a spreadsheet with tabs: PCI-DSS Gap Assessment | Summary Dashboard | Remediation Plan

2. For each of the 12 PCI-DSS requirements, create a row with:
   - Requirement number and name
   - Key sub-requirements (select 3–5 key sub-requirements to assess per main requirement)
   - Current compliance status: Compliant | Partial | Non-Compliant | Not Applicable
   - Evidence available (Yes/No/Partial)
   - Gap description (if non-compliant or partial)
   - Risk rating (Critical/High/Medium/Low)
   - Remediation action required
   - Owner
   - Target date

3. Incorporate PaySafe's known issues:
   - Req 3 (Protect stored account data): Are PAN stored? If yes, is encryption (AES-256) confirmed? Mark as partial with "Encryption implemented but key management process undocumented"
   - Req 10 (Log and monitor): Daily log review required by v4.0 — mark as Non-Compliant based on scenario context (no evidence of daily review)
   - Req 11 (Test security): Internal vulnerability scans must be quarterly — clarify if this has occurred
   - Req 12 (Security policy): 12-month policy review cycle required — check against PaySafe's outdated policies

4. Summary Dashboard tab: Total requirements assessed, % Compliant, % Partial, % Non-Compliant, Critical gaps count, High gaps count, 5-month audit readiness rating (RAG).

5. Remediation Plan tab: Prioritised list of all non-compliant items sorted by criticality, with 5-month remediation timeline mapped against the QSA audit date.

**Quality Bar:** Sub-requirements are specific (not just "Requirement 3 — compliant"). Gap descriptions explain what exactly is missing or insufficient. Remediation actions are specific (not "implement controls").

---

### Deliverable 2: GDPR Compliance Checklist and Gap Analysis

**What It Is:** A structured assessment of PaySafe's GDPR compliance status across the key GDPR obligations applicable to a payment processing company.

**Step-by-Step Instructions:**

1. Create a GDPR compliance checklist covering:

   **Data Governance (Articles 5, 6, 9)**
   - [ ] All processing activities identified and lawful basis documented
   - [ ] Special category data: Does PaySafe process any? If no, document why not applicable
   - [ ] Data minimisation reviewed — only necessary data collected

   **Record of Processing Activities (Article 30)**
   - [ ] RoPA documented for all processing activities
   - [ ] RoPA includes: name/contact of controller, purpose, categories of data, recipients, transfers, retention periods, security measures

   **Data Retention (Article 5(1)(e) — Storage Limitation)**
   - [ ] Data retention policy exists and is enforced
   - [ ] Retention periods defined for each data category
   - [ ] Automated deletion or review process in place

   **Individual Rights (Articles 15–22)**
   - [ ] Subject Access Request (SAR) procedure exists (30-day deadline)
   - [ ] Right to erasure procedure exists
   - [ ] Right to restriction/objection procedure exists
   - [ ] Privacy notice meets Articles 13/14 requirements

   **Data Breach Response (Articles 33, 34)**
   - [ ] Breach detection and reporting procedure exists
   - [ ] 72-hour ICO notification process documented
   - [ ] Individual notification criteria and process defined

   **Data Protection Impact Assessment (Article 35)**
   - [ ] DPIA trigger criteria defined
   - [ ] DPIA process documented
   - [ ] DPO engaged in high-risk processing decisions

   **International Transfers (Articles 44–49)**
   - [ ] All international data transfers identified (does payment data go to non-UK/EU processors?)
   - [ ] Transfer mechanism for each: Standard Contractual Clauses (SCCs), adequacy decision, etc.

2. For each item: Status (Compliant/Partial/Non-Compliant/Not Applicable) | Evidence | Gap Description | Priority | Action | Owner

3. Write a 1-page gap summary highlighting the top 5 GDPR gaps and recommended priority actions.

---

### Deliverable 3: Compliance Calendar (12-Month)

**What It Is:** A 12-month compliance calendar showing all PCI-DSS and GDPR compliance deadlines, review dates, and recurring activities — with named owners for each.

**Step-by-Step Instructions:**

1. Create a calendar (Excel/Google Sheets) with months as columns and compliance activities as rows.

2. Include PCI-DSS activities:
   - Quarterly internal vulnerability scans (Req 11.3.1)
   - Quarterly external vulnerability scans by ASV (Req 11.3.2)
   - Annual penetration test (Req 11.4)
   - Annual security awareness training (Req 12.6)
   - Annual policy review (Req 12.3.1)
   - QSA audit (5 months from now — mark as fixed deadline)
   - SAQ (Self-Assessment Questionnaire) if applicable

3. Include GDPR activities:
   - Annual RoPA review
   - Annual privacy notice review
   - Annual DPIA review for high-risk processing
   - Annual data retention schedule review
   - SAR response SLA monitoring (monthly check)
   - DPO annual report

4. Mark the ICO questionnaire deadline (30 days — immediate priority).

5. Assign a named role owner to every activity.

6. Highlight any upcoming deadlines in the next 60 days in red.

---

### Deliverable 4: Compliance Obligations Register

**What It Is:** A master register of all legal, regulatory, and contractual compliance obligations applicable to PaySafe — the single source of truth for all compliance requirements.

**Step-by-Step Instructions:**

1. Create a structured table with columns: Obligation ID | Regulation/Standard | Specific Requirement | Article/Section Reference | Mandatory/Voluntary | Who Enforces | Applicable to PaySafe (Y/N/Partial) | Justification if NA | Current Status | Evidence Required | Owner | Last Reviewed

2. Include at minimum:
   - UK GDPR — 15 key articles
   - PCI-DSS v4.0 — 12 requirements (high level)
   - ICO Registration requirement
   - Companies Act (relevant data/record obligations)
   - FCA requirements if PaySafe has any regulated activities (research and document)
   - Any contractual requirements (merchant agreements requiring data security)

3. Sort by: Mandatory first, then by risk level.

4. Add a summary tab: Total obligations, % currently compliant, % partial, % non-compliant.

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| PCI-DSS Assessment Quality | 30% | Sub-requirements assessed; gaps specific; remediation actions actionable |
| GDPR Coverage | 30% | All key GDPR articles addressed; gap analysis specific to PaySafe context |
| Completeness | 20% | All 4 deliverables submitted |
| Professional Quality | 20% | Regulatory-grade language; evidence-based assessment |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **PCI-DSS v4.0** | Full 12-requirement gap assessment for a payment processor |
| **GDPR / UK GDPR** | Compliance checklist covering Articles 5, 6, 30, 33, 35 |
| **ISO 27001 (partial)** | Referenced for security controls supporting PCI-DSS Req 3, 8, 10 |

---

## Week-Specific Resources

- [PCI-DSS v4.0 Standard — pcisecuritystandards.org](https://www.pcisecuritystandards.org/document_library/) — Free download
- [PCI-DSS v4.0 Quick Reference Guide](https://www.pcisecuritystandards.org/documents/PCI-DSS-v4-0-Quick-Reference-Guide.pdf) — 2-page summary
- [ICO Guide to UK GDPR — ico.org.uk](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/) — Complete guidance
- [GDPR Full Text — gdpr-info.eu](https://gdpr-info.eu/) — Searchable; focus on Articles 5, 6, 30, 33, 35
- [ICO Enforcement Actions](https://ico.org.uk/action-weve-taken/enforcement/) — Real cases; see what gaps lead to fines
- [EDPB Breach Notification Guidelines](https://edpb.europa.eu/our-work-tools/documents/public-consultations/2021/guidelines-012021-examples-regarding-data-breach_en) — GDPR Art 33/34 detail
- [ICO Right of Access Guidance](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/individual-rights/right-of-access/) — SAR process
- [PCI SSC: What Changed in v4.0](https://blog.pcisecuritystandards.org/whats-new-in-pci-dss-v40) — Key changes from v3.2.1

---

## Submission

```
Week-04/Deliverables/
├── PaySafe-PCIDSS-Gap-Assessment-v1.0.xlsx
├── PaySafe-GDPR-Compliance-Checklist-v1.0.xlsx
├── PaySafe-Compliance-Calendar-12Month-v1.0.xlsx
└── PaySafe-Compliance-Obligations-Register-v1.0.xlsx
```
