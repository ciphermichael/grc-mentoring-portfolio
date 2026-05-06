# Week 07 Assignment: Security Policy Development

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | RetailMax Ltd. |
| **Your Role** | GRC Analyst / Policy Author |
| **Estimated Time** | 10–14 hours |
| **Difficulty** | 🌟🌟🌟 |
| **Frameworks** | ISO 27001:2022 (Annex A), NIST CSF 2.0 (PROTECT function) |

---

## Scenario Brief — Read This Carefully

**RetailMax Ltd.** is a 1,000-person UK retail chain operating 85 stores across England and Wales, with a headquarters in Birmingham and an e-commerce platform generating £45M annual online revenue. Their IT environment includes: a POS (Point of Sale) system across all 85 stores, a WAN connecting stores to HQ, a cloud-hosted e-commerce platform (AWS), Microsoft 365 for all 1,000 employees, and a corporate device fleet of 800 laptops and 1,200 store tablets.

Three months ago, RetailMax suffered a data breach. An employee in the Manchester store installed an unauthorised file-sharing application on their company tablet to transfer work files to their personal device. The application contained spyware. The spyware captured credentials and allowed an attacker to access the customer database, exposing 40,000 customer records including names, email addresses, and purchase histories. The ICO has been notified and is currently investigating.

The post-incident Root Cause Analysis identified: (1) No Acceptable Use Policy governing personal software installation; (2) No Data Classification Policy defining how sensitive data must be handled; (3) No formal Patch Management Policy — the tablet OS was unpatched for 8 months; (4) No Security Awareness training delivered in the past 18 months.

The new CISO, James Okafor, has been brought in to build a complete security policy library. You are his GRC Analyst. You have 6 weeks to produce a 10-policy library ready for board approval. The ICO investigation means this work is also urgent from a regulatory response perspective — the ICO will expect to see that policies are now in place.

**Key constraints:**
- Policies must work for both store (non-technical) employees and IT/technology employees
- Language must be understandable without security expertise
- Policies must be aligned to ISO 27001 Annex A controls (RetailMax is beginning ISO 27001 planning)
- All policies must be approved by the CEO and board before publication

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 7 — especially the policy hierarchy and template sections
- [ ] Read the Security Policy Template in `/Templates/Security-Policy-Template.md`
- [ ] Review SANS free policy templates at sans.org/information-security-policy
- [ ] Read ISO 27001:2022 Clause 5.2 (Policy requirements)

### Questions to Answer Before Starting
1. What is the difference between a "policy" and a "procedure"? Give an example of each for RetailMax.
2. Who should approve RetailMax's Information Security Policy — the CISO, the CEO, or the board?
3. What ISO 27001 Annex A control requires a formal Acceptable Use Policy?
4. The ICO is investigating RetailMax. How does the existence of a Data Classification Policy affect their regulatory defence?
5. A store employee asks: "What's the difference between company data and personal data?" — Which policy answers this question?

---

## Deliverables

### Deliverable 1: 10 Complete Security Policies

Write all 10 policies using the Security Policy Template in `/Templates/`. Each policy must be complete — no placeholder text.

**Policies to write:**

**POL-001: Information Security Policy**
- The apex document; signed by the CEO
- Must state: management commitment, security objectives, ISMS scope, consequences of non-compliance
- ISO ref: ISO 27001 Clause 5.2, A.5.1
- 2–3 pages

**POL-002: Acceptable Use Policy (AUP)**
- Governs employee use of all company IT assets: devices, email, internet, social media
- Must explicitly address: personal software installation (the breach root cause), personal use of company devices, company data on personal devices, BYOD rules
- ISO ref: A.5.10, A.6.2, A.8.1
- 3–4 pages

**POL-003: Access Control Policy**
- Governs user account creation, access rights assignment, privileged access, and access reviews
- Must address: least privilege, need-to-know, MFA requirements, quarterly access reviews
- ISO ref: A.5.15, A.5.16, A.5.17, A.5.18, A.8.2, A.8.3
- 3 pages

**POL-004: Password and Authentication Policy**
- Minimum password length (12+ characters), complexity requirements, MFA requirements, password manager use, prohibited practices (sharing passwords, default passwords)
- ISO ref: A.8.5
- 2 pages

**POL-005: Incident Response Policy**
- Incident classification (P1–P4), reporting procedures, IR team roles, GDPR breach notification requirements (72-hour ICO notification trigger)
- ISO ref: A.5.24, A.5.25, A.5.26, A.5.27
- 3 pages

**POL-006: Data Classification Policy**
- Define 4 classification levels: Public | Internal | Confidential | Restricted
- For each level: description, examples, handling requirements (storage, transmission, disposal, access)
- Apply to RetailMax context: customer purchase data = Confidential; employee HR data = Restricted; store promotional material = Public
- ISO ref: A.5.12, A.5.13
- 3 pages

**POL-007: Remote Working Policy**
- Rules for working from non-office locations; VPN requirements; screen privacy; home Wi-Fi security; device lock; prohibition on working from public Wi-Fi without VPN
- Applies to RetailMax's 200 office/remote employees (not store staff)
- ISO ref: A.6.7, A.8.1
- 2 pages

**POL-008: Patch Management Policy**
- Defines patching cadence by severity (Critical: 24hr, High: 7 days, Medium: 30 days, Low: 90 days)
- Applies to all 800 laptops and 1,200 store tablets (this is the gap that enabled the breach)
- Exception process for legacy systems
- ISO ref: A.8.8
- 2 pages

**POL-009: Physical Security Policy**
- Governs physical access to all 85 stores and HQ; visitor management; clear desk; device security in stores; secure disposal of equipment
- ISO ref: A.7.1, A.7.2, A.7.4, A.7.7, A.7.14
- 2 pages

**POL-010: Security Awareness and Training Policy**
- Mandatory training at onboarding and annually; phishing simulation programme; specific training for privileged users
- Applies to all 1,000 employees including store staff (simplified training for store employees)
- Completion tracking and reporting requirements
- ISO ref: A.6.3
- 2 pages

**For each policy, the template must include:**
- Document header (Document ID, Version 1.0, Status, Owner, Approved By, Review Date, ISO ref, NIST CSF ref)
- Purpose
- Scope (who it applies to)
- Policy Statements (the actual requirements — written in "must" language)
- Roles and Responsibilities
- Enforcement
- Review History

---

### Deliverable 2: Policy Register / Index

**What It Is:** A master index of all 10 policies showing their status, ownership, and review schedule.

**Create a spreadsheet with columns:**
Policy ID | Policy Name | Version | Status | Owner (Role) | Approved By | Effective Date | Next Review Date | ISO 27001 Controls Mapped | NIST CSF Functions | Regulatory Relevance | Training Required

Complete one row per policy. Set all Next Review Dates to 12 months from today.

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Policy Completeness | 30% | All 10 policies fully written; no placeholder text |
| Policy Quality | 35% | Uses "must" language; specific requirements; correct ISO refs |
| Coverage | 20% | All required topics covered; breach root causes addressed |
| Professional Format | 15% | Consistent template; version control; board-ready presentation |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **ISO 27001:2022 Annex A** | Each policy maps to specific Annex A control references |
| **ISO 27001:2022 Clause 5.2** | Information Security Policy requirements |
| **NIST CSF 2.0 — PROTECT** | PR.AT (awareness training), PR.AA (access control) subcategories |
| **GDPR Art. 32** | Security measures — referenced in InfoSec Policy and Incident Response Policy |

---

## Week-Specific Resources

- [SANS Free Security Policy Templates](https://www.sans.org/information-security-policy/) — 27 free professional templates
- [ISO 27001:2022 Clause 5.2](https://www.iso.org/standard/27001) — Policy requirements
- [NCSC: Policies and Procedures](https://www.ncsc.gov.uk/guidance/setting-up-two-factor-authentication) — UK guidance
- [ICO: Technical and Organisational Measures](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/security/encryption/) — Policy requirements under GDPR Art 32
- [Advisera: Policy Writing Guide for ISO 27001](https://advisera.com/27001academy/blog/2015/03/16/how-to-write-iso-27001-policies-procedures-and-work-instructions/)
- [CIS: Security Policy Best Practices](https://www.cisecurity.org/insights/white-papers/cis-controls-policy-cheat-sheet) — CIS policy guidance

---

## Submission

```
Week-07/Deliverables/
├── RetailMax-POL-001-Information-Security-Policy-v1.0.md
├── RetailMax-POL-002-Acceptable-Use-Policy-v1.0.md
├── RetailMax-POL-003-Access-Control-Policy-v1.0.md
├── RetailMax-POL-004-Password-Authentication-Policy-v1.0.md
├── RetailMax-POL-005-Incident-Response-Policy-v1.0.md
├── RetailMax-POL-006-Data-Classification-Policy-v1.0.md
├── RetailMax-POL-007-Remote-Working-Policy-v1.0.md
├── RetailMax-POL-008-Patch-Management-Policy-v1.0.md
├── RetailMax-POL-009-Physical-Security-Policy-v1.0.md
├── RetailMax-POL-010-Security-Awareness-Training-Policy-v1.0.md
└── RetailMax-Policy-Register-v1.0.xlsx
```
