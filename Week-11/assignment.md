# Week 11 Assignment: Internal Security Audit Fundamentals

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | MegaRetail Ltd. |
| **Your Role** | Internal Security Auditor |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟🌟🌟 |
| **Frameworks** | ISO 27001:2022 (Clause 9.2), ISO 19011, IIA IPPF |

---

## Scenario Brief — Read This Carefully

**MegaRetail Ltd.** is a 2,000-person UK retail chain with 85 stores and a Birmingham headquarters. They operate a POS (Point of Sale) system across all stores connected via a corporate WAN, Microsoft Active Directory for user management, a cloud-hosted e-commerce platform (Azure), and Microsoft 365 for all office staff.

MegaRetail is currently preparing for an ISO 27001 Stage 2 certification audit in 6 months. As part of their ISO 27001 programme (Clause 9.2 — Internal Audit), the CISO, James Okafor, must demonstrate that internal audits have been conducted at planned intervals. The access control domain has been identified as a high-risk area: a recent penetration test found multiple accounts with excessive privileges, and 6 accounts belonging to terminated employees were still active.

You are MegaRetail's Internal Audit Lead (engaged as a GRC Consultant). Your first audit is a focused **Access Control Audit** covering ISO 27001 Annex A controls A.5.15, A.5.16, A.5.17, A.5.18, A.6.5, A.8.2, A.8.3, and A.8.5. The audit scope is: all user account management processes for MegaRetail's corporate systems (Active Directory, Azure, Microsoft 365). POS system access is out of scope for this audit (covered in a separate scheduled audit).

**Key information:**
- 2,000 user accounts in Active Directory
- 45 IT administrators with elevated privileges
- Last access review: 9 months ago (review should be quarterly per policy)
- Termination process: HR sends email to IT; IT manually disables account (no automation)
- MFA: Enforced for Microsoft 365 but not for VPN or Azure console access
- Privileged Access Management (PAM): No PAM tool; admin accounts not separated from regular accounts for most IT staff
- Password policy: 8-character minimum (below the 12-character ISO 27001 best practice)

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 11 — especially the audit lifecycle and evidence types
- [ ] Read ISO 27001:2022 controls A.5.15 through A.5.18 and A.6.5
- [ ] Read ISO 19011:2018 audit principles
- [ ] Review the Internal Audit Checklist Template in `/Templates/`

### Questions to Answer Before Starting
1. What does ISO 27001 Clause 9.2 require about internal audits?
2. What are the 4 control testing methods? Which would you use to test whether terminated user accounts are removed promptly?
3. MegaRetail has 45 IT admin accounts. How many should you sample for testing?
4. An access review was completed 9 months ago against a quarterly requirement. Is this a finding? What severity?
5. What makes an auditor "independent"? Can James Okafor (CISO) audit his own access control programme?

---

## Deliverables

### Deliverable 1: Audit Charter

**What It Is:** The formal document authorising the internal audit function at MegaRetail and defining its scope, independence, and authority.

**Must include:**
- Purpose: Why an internal audit function exists (assurance, governance, ISO 27001 compliance)
- Authority: Signed by the board or Audit Committee; grants the auditor access to all systems, records, and personnel
- Independence: The audit function reports to the Board Audit Committee, NOT to the CISO (to maintain independence)
- Scope: What the audit function covers (all information security controls within the ISO 27001 ISMS)
- Responsibilities: What auditors are required to do; what they are NOT responsible for (they don't implement controls)
- Confidentiality: How audit findings are protected
- Standards: ISO 19011, IIA IPPF, ISO 27001 Clause 9.2

---

### Deliverable 2: Annual Audit Programme (12-Month Plan)

**What It Is:** MegaRetail's full 12-month internal audit plan for the ISO 27001 programme, covering all major control domains across the year.

**Create a calendar showing:**
- 6 audits planned across the year covering: Access Control (this engagement), Cryptography and Data Protection, Vendor Management, Change Management and Patch Management, Incident Response and BCP, Supplier Audit (one critical third party)
- For each audit: audit title, scope, planned month, estimated duration, auditor, criteria
- Resource plan: How many person-days per audit?
- Risk basis: Why is each domain being audited and why in this sequence? (Higher-risk domains first)
- Coverage: Together, the 6 audits should cover all major Annex A control domains

---

### Deliverable 3: Access Control Audit Plan

**What It Is:** The detailed plan for this specific access control audit.

**Must include:**
1. Audit Objectives: What is the audit trying to determine? (Are access control controls effectively preventing unauthorised access?)
2. Audit Scope: Corporate systems (AD, Azure, M365). POS systems out of scope. Users in scope: all 2,000.
3. Audit Criteria: ISO 27001 Annex A controls: A.5.15, A.5.16, A.5.17, A.5.18, A.6.5, A.8.2, A.8.3, A.8.5
4. Fieldwork Tests: List every specific test to be performed:
   - Test 1: Sample 40 user accounts; verify account status matches HR records (active employees only)
   - Test 2: Sample 45 IT admin accounts; verify each has a separate admin account (A.8.2)
   - Test 3: Review last access review completion records; verify quarterly cadence (A.5.18)
   - Test 4: Test MFA enforcement — select 20 accounts; verify MFA status (A.8.5)
   - Test 5: Sample 10 termination events from last 6 months; verify access removed within 24hr SLA (A.6.5)
   - Test 6: Review password policy settings; verify minimum requirements met (A.8.5)
5. Evidence to Request: Complete list of evidence required (AD user export, HR termination records, access review sign-offs, MFA status report, password policy configuration)
6. Schedule: Opening meeting date, fieldwork dates, draft report date, final report date

---

### Deliverable 4: Audit Fieldwork Workbook (15 Control Tests)

**What It Is:** The structured document recording all 15 control tests, evidence examined, and conclusions.

**Create a spreadsheet with one row per test:**
Test ID | Control Ref | Control Assertion | Population | Sample Size | Testing Method | Evidence Reviewed | Evidence Reference | Test Result (Effective/Deficient) | Exceptions Found | Exception Rate | Finding (if any) | Severity

**Complete all 15 tests using MegaRetail's scenario data:**

Apply these findings from the scenario:
- Test 1 (Terminated accounts): Of 40 sampled accounts, 4 active for terminated employees. One active for 47 days. [HIGH finding]
- Test 2 (Privileged access separation): 32 of 45 IT admins use same account for regular and admin tasks. No PAM. [HIGH finding]
- Test 3 (Access review cadence): Last review 9 months ago; should be quarterly. Missing 2 reviews. [MEDIUM finding]
- Test 4 (MFA enforcement): Of 20 accounts tested, all have M365 MFA. 3 VPN accounts lack MFA. [HIGH finding]
- Test 5 (Termination SLA): 7 of 10 terminations met 24hr SLA. 3 were 48–72 hours. [LOW finding]
- Test 6 (Password policy): AD password policy: 8 chars; no complexity requirement. [MEDIUM finding]
- Create 9 additional tests (inquiries, document reviews) that find some positive results

---

### Deliverable 5: Audit Findings Register

**What It Is:** A structured register of all findings from the audit, rated by severity, with corrective action recommendations.

**For each finding (minimum 6 findings):**
- Finding ID (F-001, F-002, etc.)
- Finding Title (short, descriptive)
- ISO 27001 Control Reference
- Severity: Critical / High / Medium / Low / Informational
- Condition: What was found (factual, evidence-based)
- Criteria: What is required (the ISO 27001 control or policy requirement)
- Cause: Why the gap exists (root cause)
- Effect/Risk: What harm could result if not remediated
- Recommendation: Specific corrective action
- Management Response: (Leave blank — management fills in)
- Target Date: Recommended remediation deadline
- Owner: Recommended owner

---

### Deliverable 6: Draft Audit Report (4–6 pages)

**What It Is:** The formal audit report presenting findings to the CISO and Board Audit Committee.

**Structure:**
1. Cover page: MegaRetail Internal Audit — Access Control Audit | Audit Ref | Date | Auditors
2. Executive Summary (1 page): Overall audit conclusion, number of findings by severity, top 3 findings, overall risk rating
3. Audit Background: Scope, objectives, criteria, methodology, sample sizes used
4. Findings Summary Table: All findings with severity, control ref, and one-line description
5. Detailed Findings (3–4 pages): For each High/Critical finding: full condition, criteria, cause, effect, recommendation
6. Positive Observations: What was found to be well-controlled (at least 2 positive observations)
7. Conclusion and Next Steps: Follow-up plan; next scheduled review

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Audit Plan Quality | 20% | Scope clear; tests specific; evidence requests precise |
| Fieldwork Workbook | 30% | All 15 tests documented; evidence-based; correctly concluded |
| Findings Quality | 30% | Specific condition/criteria/cause/effect/recommendation format; severity appropriate |
| Audit Report Quality | 20% | Board-ready; executive summary compelling; recommendations actionable |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **ISO 27001:2022 Clause 9.2** | Internal audit mandate and requirements |
| **ISO 27001:2022 Annex A** | Audit criteria — A.5.15–5.18, A.6.5, A.8.2, A.8.3, A.8.5 |
| **ISO 19011:2018** | Audit principles and process |
| **IIA IPPF** | Internal audit professional standards |

---

## Week-Specific Resources

- [ISO 27001:2022 Clause 9.2 Requirements](https://www.iso.org/standard/27001) — Internal audit clause
- [ISO 19011:2018 Audit Guidelines Overview](https://www.iso.org/standard/70017.html) — Audit standards
- [IIA: International Standards for Professional Practice](https://www.theiia.org/en/standards/) — Free IIA standards access
- [ISACA IS Audit Guidelines](https://www.isaca.org/resources/isaca-journal/issues/2016/volume-1/is-audit-and-assurance-standards-and-guidelines) — IS audit standards
- [SANS: Auditing Active Directory](https://www.sans.org/reading-room/whitepapers/auditing/) — Technical audit guidance
- [PCAOB AS 2201 — Internal Control Auditing](https://pcaobus.org/Standards/Auditing/Pages/AS2201.aspx) — Professional audit standards

---

## Submission

```
Week-11/Deliverables/
├── MegaRetail-Audit-Charter-v1.0.md
├── MegaRetail-Annual-Audit-Programme-2025-v1.0.xlsx
├── MegaRetail-Access-Control-Audit-Plan-v1.0.md
├── MegaRetail-Fieldwork-Workbook-v1.0.xlsx
├── MegaRetail-Audit-Findings-Register-v1.0.xlsx
└── MegaRetail-Access-Control-Audit-Report-v1.0.md
```
