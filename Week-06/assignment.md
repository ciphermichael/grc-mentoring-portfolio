# Week 06 Assignment: NIST Cybersecurity Framework 2.0

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | CloudFirst Inc. |
| **Your Role** | GRC Analyst |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟🌟 |
| **Frameworks** | NIST CSF 2.0, ISO 27001 (cross-mapping), CIS Controls v8 |

---

## Scenario Brief — Read This Carefully

**CloudFirst Inc.** is a 300-person cloud services company based in Edinburgh, providing managed cloud infrastructure (compute, storage, networking) to UK businesses. They primarily serve mid-market companies (50–500 employees) that do not have the internal capability to manage their own cloud infrastructure. CloudFirst manages approximately 150 client environments across AWS and Azure.

As a managed cloud services provider, CloudFirst has significant responsibility for their clients' security posture — but until now, they have operated without a formal cybersecurity framework. Their new CISO, Dr. Rachel Kim (hired 60 days ago from a FTSE 100 company), has mandated a comprehensive baseline assessment as her first major initiative.

Dr. Kim has chosen NIST CSF 2.0 as the assessment framework for three reasons: (1) CloudFirst has several US multinational clients who require NIST alignment; (2) NIST CSF 2.0 provides excellent coverage of supply chain and third-party risk (critical for a managed services provider); (3) it provides a clear path toward ISO 27001 implementation (planned for next year).

**Current known security gaps:**
- No formal risk management strategy or risk appetite statement
- No complete IT asset inventory (systems are tracked in multiple spreadsheets)
- Multi-factor authentication not enforced for all staff (30% of accounts lack MFA)
- No SIEM or centralised logging; monitoring is ad hoc
- No documented incident response plan (incidents handled reactively)
- No DR plan; backups exist but recovery has never been tested
- Developer direct access to client production environments (no formal PAM)
- No formal vendor/supply chain security programme despite managing 150+ client environments

**Target:** NIST CSF 2.0 Tier 3 (Repeatable) across all functions within 12 months.

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 6 — especially the 6-function breakdown
- [ ] Download NIST CSF 2.0 document from nist.gov and read the function descriptions
- [ ] Use the NIST CSF 2.0 Reference Tool at csrc.nist.gov to browse subcategories
- [ ] Understand what "Tier 3 — Repeatable" means for each function

### Questions to Answer Before Starting
1. What is the difference between NIST CSF 2.0 Tier 2 and Tier 3?
2. CloudFirst manages client environments. Which CSF function most directly addresses supply chain and third-party risk?
3. If CloudFirst has no incident response plan, what tier would you assign to the RESPOND function?
4. How does NIST CSF 2.0 map to ISO 27001 Annex A controls?
5. What does "GV.RM" mean and why is it the most important GV subcategory for CloudFirst?

---

## Deliverables

### Deliverable 1: NIST CSF 2.0 Maturity Assessment (All 6 Functions)

**What It Is:** A comprehensive assessment scoring CloudFirst's current tier across all 6 CSF functions, with evidence and gap narrative for each.

**Step-by-Step Instructions:**

1. Create a spreadsheet with tabs: Summary Dashboard | GOVERN | IDENTIFY | PROTECT | DETECT | RESPOND | RECOVER

2. **Summary Dashboard tab**: Function | Current Tier | Target Tier | Gap | Priority | Key Actions

3. For each function tab, list all categories and key subcategories. For each subcategory:
   - Subcategory ID and description (e.g., GV.RM-01: Risk management objectives are established)
   - Current Tier (1–4)
   - Evidence of current state (what exists today)
   - Gap description (what's missing for the target tier)
   - Priority (Critical/High/Medium/Low)
   - Recommended action

4. Apply CloudFirst's known gaps consistently:
   - GOVERN: Tier 1 across most categories (no risk strategy, no formal roles, no supply chain programme)
   - IDENTIFY.AM: Tier 2 (some inventory in spreadsheets; incomplete)
   - PROTECT.AA: Tier 2 (MFA partial; access control inconsistent)
   - DETECT.CM: Tier 1 (no SIEM; monitoring ad hoc)
   - RESPOND.MA: Tier 1 (no IR plan)
   - RECOVER.RP: Tier 1 (backups untested; no DR plan)

5. For each category, write a 2–3 sentence gap narrative explaining what Tier 3 requires and what CloudFirst is missing.

**Quality Bar:** All 6 functions assessed; tier scores calibrated to reflect CloudFirst's actual gaps (GOVERN should be lower than PROTECT since governance is the biggest gap); gap narratives are specific.

---

### Deliverable 2: Current vs Target CSF Profile (Gap Analysis)

**What It Is:** A side-by-side comparison document showing CloudFirst's current profile vs 12-month target profile, with a visual radar chart.

**Step-by-Step Instructions:**

1. Create a 2-column table: Current Tier per function | Target Tier per function | Gap (Target − Current) | Priority

2. Create a radar chart (spider diagram) with 6 axes (one per function): Show current tier as dotted line, target tier as solid line. This is the most impactful visual for executive presentation.

3. Write a 1-page narrative: "The gap analysis shows CloudFirst currently operates at an average of Tier [X] across all functions. The most significant gaps are in [functions]. Achieving Tier 3 across all functions within 12 months is [achievable/challenging] given [specific reasons]."

4. Include a "Quick Wins" section: Which 5 improvements can be made in the first 30 days with low cost/effort?

---

### Deliverable 3: CSF Profile Document for CloudFirst

**What It Is:** A formal CSF Profile document — the deliverable CloudFirst would use to communicate their security posture to US clients and regulators.

**Step-by-Step Instructions:**

1. Write a professional document with:
   - Cover page: CloudFirst Inc. | NIST CSF 2.0 Profile | Version 1.0 | Date | Classification
   - Executive Summary: Business context, assessment approach, overall findings
   - Organisational Context: What CloudFirst does, who they serve, key risks
   - Current Profile Summary: Tier per function with narrative
   - Target Profile: Desired tier per function with business justification
   - Gap Analysis Summary: Top 10 gaps prioritised by risk
   - Cross-Framework Mapping: Show how CSF functions map to ISO 27001 controls (minimum 10 examples)

---

### Deliverable 4: 12-Month CSF Implementation Roadmap

**What It Is:** A prioritised roadmap showing how CloudFirst will achieve Tier 3 across all functions within 12 months.

**Step-by-Step Instructions:**

1. Structure the roadmap by quarter (Q1–Q4) and by CSF function priority.

2. Q1 priorities (months 1–3) should address GOVERN first: risk appetite statement, formal roles/responsibilities, asset inventory completion.

3. Q2 priorities: PROTECT improvements (MFA enforcement, access control formalisation, patch management).

4. Q3 priorities: DETECT (SIEM implementation, log review process, alerting).

5. Q4 priorities: RESPOND (IR plan and tabletop exercise), RECOVER (DR test, RTO/RPO definition).

6. For each initiative: CSF subcategory addressed | Responsible owner | Resource requirement (person-days) | Tool/cost estimate | Success criteria | Dependencies

7. Include a budget summary: Estimated total investment to reach Tier 3. Breakdown: tooling, staff time, external advisory.

---

### Deliverable 5: Executive Summary (2 pages)

**What It Is:** A board-ready 2-page summary of the NIST CSF assessment findings for Dr. Kim to present to the CloudFirst board.

**Instructions:** Write in plain business language. No acronyms without explanation. Focus on: business risk exposure, investment required, business benefit of improvement. Include the radar chart visual.

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Assessment Accuracy | 30% | Tier scores calibrated and evidence-based |
| Gap Analysis Quality | 25% | Specific gaps identified; priorities justified |
| Roadmap Realism | 25% | Sequenced correctly; resources estimated; achievable |
| Professional Quality | 20% | Board-ready documents; correct NIST terminology |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **NIST CSF 2.0** | Full 6-function maturity assessment; CSF Profile development |
| **ISO 27001:2022** | Cross-mapping to show dual-framework value |
| **CIS Controls v8** | Referenced as informative resource for control recommendations |

---

## Week-Specific Resources

- [NIST CSF 2.0 Full Document](https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf) — Free PDF
- [NIST CSF 2.0 Reference Tool](https://csrc.nist.gov/projects/cybersecurity-framework/filters#/csf/filters) — Interactive subcategory browser
- [NIST: Getting Started with CSF 2.0](https://www.nist.gov/cyberframework/getting-started) — Enterprise quick start guide
- [NIST CSF 2.0 FAQ — What Changed from 1.1](https://www.nist.gov/cyberframework/csf-20-faqs) — Official change summary
- [Axio360 Free CSF Assessment](https://axio.com/cyber-risk-assessment/) — Online CSF assessment tool
- [Verizon DBIR 2024](https://www.verizon.com/business/resources/reports/dbir/) — For DETECT/RESPOND context
- [AWS Security Hub — NIST CSF Compliance Checks](https://docs.aws.amazon.com/securityhub/latest/userguide/nist-standard.html) — Cloud-specific CSF implementation

---

## Submission

```
Week-06/Deliverables/
├── CloudFirst-NIST-CSF-Assessment-v1.0.xlsx
├── CloudFirst-CSF-Profile-Document-v1.0.md
├── CloudFirst-Current-vs-Target-Radar-Chart.png
├── CloudFirst-CSF-Implementation-Roadmap-v1.0.xlsx
└── CloudFirst-Executive-Summary-v1.0.md
```
