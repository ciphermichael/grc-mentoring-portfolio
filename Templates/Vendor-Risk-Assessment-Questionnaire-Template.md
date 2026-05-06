# Vendor Risk Assessment Questionnaire (VRAQ)

| Field | Value |
|-------|-------|
| **Document ID** | VRAQ-[XXX] |
| **Vendor Name** | [Vendor Organisation Name] |
| **Assessment Date** | DD-MMM-YYYY |
| **Assessed By** | [GRC Analyst Name] |
| **Vendor Contact** | [Name, Role, Email] |
| **Services Provided** | [Brief description of services] |
| **Contract Value** | £[X] annually |
| **Data Accessed** | [Type of data: personal data, financial data, cardholder data, etc.] |
| **Vendor Tier** | Tier 1 (Critical) / Tier 2 (High) / Tier 3 (Standard) / Tier 4 (Low) |
| **Framework Refs** | ISO 27001 A.5.19–5.22 | GDPR Art. 28 | SOC 2 CC9 | PCI-DSS Req 12.8 |
| **Classification** | Confidential — Internal |

---

## Purpose

This Vendor Risk Assessment Questionnaire assesses the information security posture of [Vendor Name] as a third-party provider to [Our Organisation]. The assessment determines whether the vendor meets our minimum security standards and whether they can be approved as a supplier.

---

## Vendor Tiering

| Tier | Definition | Due Diligence Required |
|------|------------|----------------------|
| **Tier 1 — Critical** | Processes sensitive personal data, cardholder data, or has critical system access | Full VRAQ + certification review + right to audit + annual reassessment |
| **Tier 2 — High** | Significant data access or important system integration | VRAQ + certification review + bi-annual reassessment |
| **Tier 3 — Standard** | Limited data access, non-critical systems | Abbreviated VRAQ + annual review |
| **Tier 4 — Low** | No data access, no system access | Contract terms only |

---

## Section 1: Information Security Governance

*Assesses whether the vendor has appropriate security leadership, policies, and programme maturity.*

| # | Question | Response | Evidence Required | Score (1–5) | Notes |
|---|----------|----------|-------------------|-------------|-------|
| 1.1 | Does the organisation have a dedicated CISO or Head of Security? | Yes / No / Shared role | Name and contact details | | |
| 1.2 | Is there a documented Information Security Policy, approved by executive leadership? | Yes / No | Copy of IS Policy (current version) | | |
| 1.3 | When was the Information Security Policy last reviewed? | Date | Policy document version date | | |
| 1.4 | Does the organisation hold ISO 27001 certification? | Yes / No | Certificate + scope statement | | |
| 1.5 | Does the organisation hold SOC 2 Type II attestation? | Yes / No | Most recent SOC 2 report | | |
| 1.6 | Does the organisation hold Cyber Essentials or Cyber Essentials Plus certification? | Yes / No | Certificate copy | | |
| 1.7 | Is there a formal security awareness training programme for all staff? | Yes / No | Training completion records | | |
| 1.8 | How frequently is security awareness training conducted? | Annually / Quarterly / On-hire / — | Training programme schedule | | |

**Section 1 Score: __ / 40** | **Section RAG: Green / Amber / Red**

---

## Section 2: Access Control and Authentication

*Assesses whether the vendor restricts access to your organisation's data appropriately.*

| # | Question | Response | Evidence Required | Score (1–5) | Notes |
|---|----------|----------|-------------------|-------------|-------|
| 2.1 | Is multi-factor authentication (MFA) enforced for all staff accounts accessing our data? | Yes / No / Partial | Screenshot of MFA policy configuration | | |
| 2.2 | Is MFA enforced for privileged/administrator accounts? | Yes / No | PAM tool configuration or IAM policy | | |
| 2.3 | Are access rights granted on a least-privilege, need-to-know basis? | Yes / No | Access control policy document | | |
| 2.4 | How frequently are access reviews conducted? | Monthly / Quarterly / Annually / Never | Most recent access review records | | |
| 2.5 | Is there a Privileged Access Management (PAM) solution in place? | Yes / No — [Tool name if yes] | PAM tool vendor documentation | | |
| 2.6 | Is user access terminated within 24 hours of employee departure? | Yes / No | Sample offboarding records (anonymised) | | |
| 2.7 | Are vendor's staff who access our systems subject to background screening? | Yes / No | Background check policy | | |
| 2.8 | Is a separate account required for privileged vs standard tasks? | Yes / No | AD/IAM configuration screenshot | | |

**Section 2 Score: __ / 40** | **Section RAG: Green / Amber / Red**

---

## Section 3: Data Protection and Encryption

*Assesses how the vendor protects data, particularly your organisation's data.*

| # | Question | Response | Evidence Required | Score (1–5) | Notes |
|---|----------|----------|-------------------|-------------|-------|
| 3.1 | Is all data at rest encrypted? What encryption standard is used? | Yes / No / Standard: [AES-256/other] | Encryption configuration documentation | | |
| 3.2 | Is all data in transit encrypted? What TLS version is required? | Yes / No / TLS version: | SSL/TLS configuration documentation | | |
| 3.3 | Does the organisation have a Data Classification Policy? | Yes / No | Policy document | | |
| 3.4 | How is your organisation's data segmented from other customers' data? | Logical / Physical / — | Architecture diagram (can be redacted) | | |
| 3.5 | Does the vendor have a formal key management procedure? | Yes / No | Key management policy | | |
| 3.6 | Does the organisation conduct regular Data Protection Impact Assessments (DPIAs) for high-risk processing? | Yes / No | DPIA register or sample DPIA | | |
| 3.7 | Is your organisation's data retained only for the contractually agreed period? | Yes / No | Data retention policy | | |
| 3.8 | What is the data return/deletion process at contract termination? | Description | Data destruction procedure document | | |

**Section 3 Score: __ / 40** | **Section RAG: Green / Amber / Red**

---

## Section 4: Third-Party and Supply Chain Risk

*Assesses whether the vendor manages risk from its own sub-suppliers.*

| # | Question | Response | Evidence Required | Score (1–5) | Notes |
|---|----------|----------|-------------------|-------------|-------|
| 4.1 | Does the vendor use sub-processors or sub-contractors who will access our data? | Yes / No | List of sub-processors (names, countries) | | |
| 4.2 | If yes, have these sub-processors been formally assessed for security? | Yes / No | Sub-processor assessment records | | |
| 4.3 | Are sub-processors contractually required to meet the same security standards as the vendor? | Yes / No | Sub-processor contract terms | | |
| 4.4 | Will our organisation be notified if a sub-processor changes? | Yes / No | Contract clause or process document | | |
| 4.5 | Does the vendor maintain a software bill of materials (SBOM) for software supplied? | Yes / No / Not applicable | SBOM or dependency management process | | |

**Section 4 Score: __ / 25** | **Section RAG: Green / Amber / Red**

---

## Section 5: Vulnerability Management

*Assesses how the vendor identifies and remediates security vulnerabilities.*

| # | Question | Response | Evidence Required | Score (1–5) | Notes |
|---|----------|----------|-------------------|-------------|-------|
| 5.1 | Is there a formal vulnerability management programme? | Yes / No | Policy document | | |
| 5.2 | How frequently are vulnerability scans conducted? | Weekly / Monthly / Quarterly / — | Most recent scan report summary | | |
| 5.3 | What is the SLA for remediating Critical vulnerabilities? | [X] hours/days | Vulnerability management SLA document | | |
| 5.4 | Is a penetration test conducted at least annually? | Yes / No | Most recent pen test executive summary | | |
| 5.5 | When was the most recent penetration test conducted? | Date | Pen test completion certificate | | |
| 5.6 | Are penetration test findings tracked to remediation? | Yes / No | Remediation tracking records | | |
| 5.7 | Does the organisation have a bug bounty or responsible disclosure programme? | Yes / No | Policy URL or description | | |

**Section 5 Score: __ / 35** | **Section RAG: Green / Amber / Red**

---

## Section 6: Incident Response

*Assesses the vendor's ability to detect, respond to, and notify you of security incidents.*

| # | Question | Response | Evidence Required | Score (1–5) | Notes |
|---|----------|----------|-------------------|-------------|-------|
| 6.1 | Is there a documented Incident Response Plan? | Yes / No | IR Policy document (or summary) | | |
| 6.2 | What is the notification SLA for notifying your organisation of a security incident affecting your data? | [X] hours | Contractual notification SLA | | |
| 6.3 | Is the incident response plan tested at least annually (tabletop or simulation)? | Yes / No | Most recent IR test record | | |
| 6.4 | Has the vendor experienced a data breach or security incident affecting customer data in the last 3 years? | Yes / No | If yes: description and remediation taken | | |
| 6.5 | Does the vendor maintain a 24/7 security operations capability? | Yes / No / Business hours only | SOC coverage documentation | | |
| 6.6 | Is there a dedicated security incident response team or retainer with an IR firm? | Yes / No | Team composition or retainer contract | | |

**Section 6 Score: __ / 30** | **Section RAG: Green / Amber / Red**

---

## Section 7: Business Continuity and Disaster Recovery

*Assesses whether the vendor can maintain service continuity during disruptions.*

| # | Question | Response | Evidence Required | Score (1–5) | Notes |
|---|----------|----------|-------------------|-------------|-------|
| 7.1 | Is there a documented Business Continuity Plan? | Yes / No | BCP document (or summary) | | |
| 7.2 | What is the vendor's Recovery Time Objective (RTO) for your services? | [X] hours | SLA documentation | | |
| 7.3 | What is the vendor's Recovery Point Objective (RPO)? | [X] hours | SLA documentation | | |
| 7.4 | Is the BCP/DR plan tested at least annually? | Yes / No | Most recent DR test results | | |
| 7.5 | What is the vendor's uptime SLA? | [X]% | SLA documentation | | |
| 7.6 | Is there geographic redundancy for critical systems? | Yes / No | Architecture description | | |

**Section 7 Score: __ / 30** | **Section RAG: Green / Amber / Red**

---

## Section 8: Compliance and Certifications

*Assesses the vendor's regulatory compliance posture.*

| # | Question | Response | Evidence Required | Score (1–5) | Notes |
|---|----------|----------|-------------------|-------------|-------|
| 8.1 | Is the vendor GDPR compliant (if processing EU/UK personal data)? | Yes / No | Privacy policy; DPA terms |  | |
| 8.2 | Has the vendor appointed a Data Protection Officer (DPO)? | Yes / No | DPO name and contact | | |
| 8.3 | Where is personal data stored and processed? | Country/region | Data location map or contract clause | | |
| 8.4 | If data is transferred outside the UK/EU, what transfer mechanism is used? | SCCs / Adequacy decision / BCRs / None | Transfer mechanism documentation | | |
| 8.5 | Is the vendor PCI-DSS compliant (if applicable)? | Yes / No / NA | QSA attestation or SAQ | | |
| 8.6 | Does the vendor carry cyber liability insurance? | Yes / No | Insurance certificate summary | | |
| 8.7 | Has the vendor been subject to any regulatory enforcement actions in the last 3 years? | Yes / No | If yes: description | | |

**Section 8 Score: __ / 35** | **Section RAG: Green / Amber / Red**

---

## Overall Risk Assessment

| Section | Score | Max | % | RAG |
|---------|-------|-----|---|-----|
| 1. Information Security Governance | | 40 | | |
| 2. Access Control and Authentication | | 40 | | |
| 3. Data Protection and Encryption | | 40 | | |
| 4. Third-Party and Supply Chain | | 25 | | |
| 5. Vulnerability Management | | 35 | | |
| 6. Incident Response | | 30 | | |
| 7. Business Continuity and DR | | 30 | | |
| 8. Compliance and Certifications | | 35 | | |
| **TOTAL** | | **275** | | |

### Overall Risk Rating

| Score | Risk Rating | Recommendation |
|-------|------------|---------------|
| 248–275 (90%+) | Low Risk | Approve — annual reassessment |
| 193–247 (70–89%) | Medium Risk | Approve with conditions — track conditions to closure |
| 138–192 (50–69%) | High Risk | Conditional approval pending remediation of critical gaps |
| <138 (<50%) | Critical Risk | Do not approve — significant remediation required |

---

## Findings Summary

### Critical Findings (Must Remediate Before Approval)

| # | Finding | Section | Risk | Required Action | Vendor Commitment Date |
|---|---------|---------|------|-----------------|----------------------|
| 1 | | | | | |
| 2 | | | | | |

### High Findings (Remediate Within 90 Days)

| # | Finding | Section | Risk | Required Action | Vendor Commitment Date |
|---|---------|---------|------|-----------------|----------------------|
| 1 | | | | | |

### Medium Findings (Remediate Within 180 Days)

| # | Finding | Section | Risk | Required Action | Vendor Commitment Date |
|---|---------|---------|------|-----------------|----------------------|
| 1 | | | | | |

---

## Assessment Outcome

**Recommendation:** ☐ Approve | ☐ Approve with Conditions | ☐ Do Not Approve

**Conditions (if applicable):**
1.
2.
3.

**Next Assessment Due:** DD-MMM-YYYY

**Assessed by:** [Name] | [Role] | [Date]

**Approved by:** [Name] | [Role] | [Date]

---

## GDPR Data Processing Agreement Status

| Requirement | Status |
|-------------|--------|
| DPA in place | Yes / No / In progress |
| DPA references GDPR Art. 28(3) requirements | Yes / No |
| DPA includes right to audit clause | Yes / No |
| Sub-processor disclosure requirement included | Yes / No |
| 72-hour (or faster) breach notification SLA included | Yes / No |

---

*Vendor Risk Assessment Questionnaire | ISO 27001 A.5.19–5.22 | GDPR Art. 28 | SOC 2 CC9 | PCI-DSS Req 12.8*
