# Week 05 Assignment: ISO 27001:2022 Deep Dive

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | Xown Solutions Limited |
| **Your Role** | ISO 27001 Lead Implementer / GRC Consultant |
| **Estimated Time** | 10–14 hours |
| **Difficulty** | 🌟🌟🌟 |
| **Frameworks** | ISO 27001:2022 (full), ISO 27002:2022 |

---

## Scenario Brief — Read This Carefully

**Xown Solutions Limited** is a UK SaaS company based in Birmingham. They develop and host financial reporting software used by 180 mid-sized businesses across the UK and EU. Their platform handles highly sensitive financial data — balance sheets, profit and loss accounts, shareholder data, and payroll information — for clients with an average annual revenue of £25M. Xown has 120 employees: 45 developers, 20 in operations/support, 30 in sales and account management, and 25 in finance, HR, and admin.

Their largest prospective client — Henderson Financial Group, a FTSE 250 investment management company — has issued a procurement requirement: all technology vendors handling financial data must provide ISO 27001 certification from a UKAS-accredited certification body, or a confirmed certification roadmap with target date, within 60 days. This is a £2.4M annual contract. Xown's CEO, Caroline Marsh, has made ISO 27001 certification the company's top strategic priority for the year.

**Current Security State (from a preliminary review):**
- Information Security Policy: Exists but last reviewed in 2021; not board-approved
- Risk Assessment: No formal risk assessment has ever been conducted
- Access Control: Some controls in place; no Privileged Access Management; developers have direct production database access
- Vendor Management: No vendor security assessments conducted; 3 critical SaaS vendors (AWS, Salesforce, Zendesk) have never been reviewed
- Security Awareness Training: Annual training conducted but not documented; completion records do not exist
- Patch Management: Informal — developers apply patches when they notice CVEs
- Monitoring and Logging: AWS CloudTrail enabled; logs not reviewed regularly; no SIEM
- Physical Security: Birmingham office has keycard access; no visitor log; no clear desk policy enforced
- Business Continuity: AWS backups configured; no documented DR plan; no BIA ever conducted

**Your engagement:** Caroline has engaged you as the ISO 27001 Lead Implementer. You will spend the first 6 weeks conducting the gap assessment and building the implementation roadmap. The target is Stage 2 certification within 12 months. BSI (British Standards Institution) has been selected as the certification body.

**Key stakeholders:**
- Caroline Marsh (CEO) — sponsor; wants the Henderson contract; understands this is a 12-month programme
- David Osei (Head of IT) — technically skilled; will own most control implementation
- Emma Collins (Head of Legal) — concerned about data protection; wants GDPR alignment
- Mark Hassan (CISO — newly appointed) — your primary counterpart; has ISO 27001 awareness from a previous role but has never led an implementation

---

## Before You Start

### Pre-Work Checklist

- [ ] Read the full `learning-guide.md` for Week 5 — especially Section 3 (full Clause and Annex A breakdown)
- [ ] Download or bookmark ISO 27001:2022 free overview from iso.org
- [ ] Review ISO 27002:2022 control descriptions for the 4 domains
- [ ] Read BSI's guide to ISO 27001 certification stages
- [ ] Review the Sample ISO 27001 Gap Assessment in `/Example-Evidence/`

### Questions to Answer Before Starting

1. Xown stores financial data for 180 businesses. Is this data personal data under GDPR? Does it require special treatment?
2. What is the difference between ISO 27001 (requirements) and ISO 27002 (guidance)?
3. Xown uses AWS as their cloud provider. Under the AWS Shared Responsibility Model, which ISO 27001 controls does AWS satisfy on Xown's behalf, and which remain Xown's responsibility?
4. What does UKAS accreditation mean for a certification body, and why does it matter?
5. The Stage 1 audit is 4 months away. Which ISO 27001 mandatory documents must exist before Stage 1?

---

## Deliverables

### Deliverable 1: ISMS Scope Statement

**What It Is:** The formal document defining what is included within Xown's Information Security Management System. This is one of the first mandatory documents BSI will review in the Stage 1 audit.

**Why This Deliverable Matters:** Scope defines the boundaries of ISO 27001 certification. Too narrow and you exclude important assets; too broad and implementation becomes unmanageable and expensive.

**Step-by-Step Instructions:**

1. Create a professional document with header: Xown Solutions Limited | ISMS Scope Statement | Document ID: ISMS-SCO-001 | Version: 1.0 | Owner: CISO | Classification: Internal

2. Write the Organisation Context section (Clause 4.1): Describe Xown's purpose, the nature of the data processed, geographic locations, and key stakeholders.

3. Write the ISMS Boundary Definition: Define exactly what is in scope. For Xown, this should include:
   - The Xown financial reporting SaaS platform and all underlying systems
   - AWS infrastructure (eu-west-2 region) hosting the platform
   - Birmingham headquarters (all IT systems within the building)
   - Remote working infrastructure (VPN, endpoint devices)
   - All Xown employees, contractors, and third parties with access to in-scope systems

4. Write the ISMS Exclusions section: What is excluded and why? (Example: The Birmingham car park CCTV system may be excluded as it doesn't interface with information assets.)

5. Write the Interested Parties section (Clause 4.2): List all parties interested in Xown's information security:
   - Henderson Financial Group (requiring ISO 27001)
   - ICO (GDPR regulator)
   - Xown clients (relying on data confidentiality)
   - Xown employees (relying on employment data protection)
   - Shareholders
   - BSI (certification body)

6. Write the Legal and Regulatory Requirements section: UK GDPR, UK GDPR (controller obligations for employee data + processor obligations for client data), Companies Act, PCI-DSS assessment (not applicable — confirm why).

7. Add a sign-off block: Approved by CEO, CISO, Head of Legal.

**Quality Bar:**
- Scope is specific to Xown's actual business (not a generic template)
- All interested parties are identified and their security expectations noted
- Exclusions are explicitly justified
- Document is board-presentable

---

### Deliverable 2: Statement of Applicability (All 93 Controls)

**What It Is:** The cornerstone ISO 27001 document declaring which of the 93 Annex A controls are applicable to Xown, the implementation status of each, and justification for any exclusions.

**Why This Deliverable Matters:** The SoA is mandatory (required by Clause 6.1.3d). BSI auditors will scrutinise it closely. Every excluded control needs documented justification.

**Step-by-Step Instructions:**

1. Create a spreadsheet with columns: Control Reference | Control Name | Applicable (Yes/No) | Inclusion/Exclusion Justification | Implementation Status (Not Implemented/Partially Implemented/Fully Implemented) | Evidence Reference | ISO 27002 Guidance Reference

2. Complete all 93 controls across 4 domains:
   - **A.5 Organizational Controls** (37 controls): A.5.1 through A.5.37
   - **A.6 People Controls** (8 controls): A.6.1 through A.6.8
   - **A.7 Physical Controls** (14 controls): A.7.1 through A.7.14
   - **A.8 Technological Controls** (34 controls): A.8.1 through A.8.34

3. For each control, determine applicability based on Xown's scope. Most controls will be Applicable. Some legitimate exclusions for Xown: A.7.5 (Protecting against physical and environmental threats — only applicable to Birmingham office, not AWS managed facilities) may be partially applicable.

4. Assess implementation status honestly based on the scenario's current state. Do not overstate implementation.

5. Add a summary tab: Total controls applicable, % fully implemented, % partially, % not implemented, % not applicable.

**Distinction criteria:** At least 70 controls marked as applicable; implementation status reflects the scenario's known gaps (e.g., A.8.2 Privileged access rights = Not Implemented given developers have production access); all exclusions have documented justification.

---

### Deliverable 3: Gap Assessment with Maturity Scoring (0–5)

**What It Is:** A detailed assessment of Xown's current compliance with all ISO 27001 requirements (Clauses 4–10 and Annex A controls), scored using a 0–5 maturity scale.

**Maturity Scale:**
- 0 — Not Existent: No controls or processes in place
- 1 — Initial: Ad hoc; no documented process
- 2 — Developing: Some controls exist but inconsistently applied
- 3 — Defined: Documented processes; consistently applied
- 4 — Managed: Measured, monitored, and reported
- 5 — Optimised: Continuously improved based on data

**Step-by-Step Instructions:**

1. Create a gap assessment covering all mandatory Clauses (4–10): For each clause, assess current maturity (0–5), document evidence of current state, identify gap description, recommend action.

2. Create a control-level gap assessment for all 93 Annex A controls: Current maturity (0–5) | Gap description | Priority (Critical/High/Medium/Low) | Recommended action | Owner | Effort (High/Med/Low)

3. Apply Xown's known gaps consistently:
   - A.6.3 (Security awareness training): Score 1 — training occurs but undocumented; no records
   - A.8.2 (Privileged access rights): Score 1 — developers have unconstrained production access
   - A.8.8 (Management of technical vulnerabilities): Score 2 — informal patching exists
   - A.8.16 (Monitoring activities): Score 2 — CloudTrail enabled but logs not reviewed
   - A.9.3 (Management review — Clause): Score 0 — no formal management review has occurred

4. Produce a summary dashboard: Average maturity score per domain, total gaps by priority, overall programme maturity.

---

### Deliverable 4: Top 10 Critical Gaps with Detailed Recommendations

**What It Is:** A board-ready report identifying the 10 most critical gaps discovered in the gap assessment, with specific remediation recommendations.

**Step-by-Step Instructions:**

1. Select the 10 gaps rated Critical or High priority from your gap assessment.
2. For each gap:
   - Control reference and name
   - Current state (what exists today)
   - Required state (what ISO 27001 requires)
   - Risk created by the gap (what could go wrong without this control)
   - Specific remediation action (not vague — name specific tools, processes, policies)
   - Responsible owner
   - Estimated effort (hours or weeks)
   - Estimated cost
   - Dependencies (what must happen first)

3. Present in priority order. Your top 3 should include: privileged access management (A.8.2), management review establishment (Clause 9.3), and formal risk assessment (Clause 6.1.2) — these are the foundation without which Stage 1 audit will fail.

---

### Deliverable 5: ISO 27001 Implementation Roadmap (12-Month Plan)

**What It Is:** A detailed Gantt-style plan showing how Xown will achieve ISO 27001 certification within 12 months, broken into phases with milestones and owners.

**Step-by-Step Instructions:**

1. Structure the roadmap around these phases:
   - **Month 1–2 (Foundation)**: ISMS scope, risk assessment methodology, management commitment, SoA v1.0
   - **Month 3–4 (Policy & Governance)**: Policy library (10+ policies), committee charter, RACI, awareness training launch
   - **Month 5–6 (Controls Implementation — Part 1)**: Access management (PAM), vulnerability management programme, patch management procedure
   - **Month 7–8 (Controls Implementation — Part 2)**: Monitoring and SIEM setup, vendor management programme, incident response plan
   - **Month 9 (Internal Audit)**: ISO 27001 internal audit, non-conformance remediation
   - **Month 10 (Management Review + Pre-Audit)**: Clause 9.3 management review, external gap assessment by BSI pre-audit team
   - **Month 11 (Stage 1 Audit)**: BSI Stage 1 documentation review; resolve any Stage 1 findings
   - **Month 12 (Stage 2 Audit)**: BSI Stage 2 implementation audit; certificate issued

2. For each phase, list: Key activities | Deliverables | Responsible owner | Dependencies | Milestone/go-no-go criteria

3. Include a resource plan: What headcount and budget is required for each phase?

4. Include key risks to the roadmap: What could delay certification and what are the mitigations?

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| SoA Completeness | 25% | All 93 controls addressed; exclusions justified; implementation status realistic |
| Gap Assessment Accuracy | 30% | Maturity scores calibrated; consistent with scenario's known gaps |
| Recommendations Quality | 25% | Specific, actionable, owner-assigned, costed |
| Roadmap Realism | 20% | Timeline feasible; phases sequenced correctly; resources identified |

---

## Frameworks Applied This Week

| Framework | How Applied |
|-----------|------------|
| **ISO 27001:2022 — Full Standard** | Gap assessment against all Clauses 4–10 and all 93 Annex A controls |
| **ISO 27002:2022** | Control guidance used to understand implementation requirements for each Annex A control |
| **ISO 27005:2022** | Referenced in methodology for risk-based control selection |

---

## Week-Specific Resources

- [ISO 27001:2022 Standard — Overview](https://www.iso.org/standard/27001) — Free structural overview
- [ISO 27002:2022 — Controls Guidance Overview](https://www.iso.org/standard/75652.html) — Companion control guidance
- [BSI Guide to ISO 27001 Certification](https://www.bsigroup.com/en-GB/iso-27001-information-security/) — Stage 1/2 process explained by a major certification body
- [Advisera ISO 27001 Academy Free Resources](https://advisera.com/27001academy/iso-27001-resources/) — Templates, guides, documentation list
- [UKAS Accredited Certification Bodies](https://www.ukas.com/find-an-organisation/) — Search for ISO 27001 certification bodies
- [AWS Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/) — Defines which controls AWS owns
- [Vanta: ISO 27001 Checklist](https://www.vanta.com/resources/iso-27001-checklist) — Practical implementation checklist
- [IT Governance: ISO 27001 SoA Template](https://www.itgovernance.co.uk/iso27001) — Sample SoA format
- [SANS: ISO 27001 Implementation Paper](https://www.sans.org/reading-room/) — Search "ISO 27001 implementation" for practitioner papers

---

## Submission

Upload your completed deliverables to:

```
Week-05/Deliverables/
├── Xown-ISMS-Scope-Statement-v1.0.md
├── Xown-Statement-of-Applicability-v1.0.xlsx
├── Xown-ISO27001-Gap-Assessment-v1.0.xlsx
├── Xown-Top10-Critical-Gaps-Report-v1.0.md
└── Xown-ISO27001-Implementation-Roadmap-v1.0.xlsx
```

Then update your `README.md` completion status table and tag your mentor for review.
