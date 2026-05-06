# Week 03 Assignment: Security Governance Frameworks

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | Apex Financial Services |
| **Your Role** | GRC Consultant |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟 |
| **Frameworks** | ISO 27001 (Clause 5), COBIT 2019, Three Lines of Defense |

---

## Scenario Brief — Read This Carefully

**Apex Financial Services** is a 500-person UK financial advisory firm regulated by the Financial Conduct Authority (FCA). They manage approximately £4.2 billion in client assets and employ 500 staff across offices in London (HQ, 350 staff) and Edinburgh (150 staff). Their business processes financial data, client investment portfolios, and personal data for approximately 12,000 individual clients.

Three months ago, the FCA conducted a supervisory review of Apex's cybersecurity governance arrangements. Their assessment identified three significant findings: (1) The board has no visibility of cyber risk — the CISO reports to the CTO who reports to the COO, and cyber risk never reaches board level; (2) There is no formal security committee structure — security decisions are made ad hoc by the CISO; (3) Security policies exist but are not board-approved, not linked to a formal governance structure, and 40% are past their review date.

The FCA has given Apex 6 months to remediate these findings or face potential enforcement action. The CEO, Helena Marsh, has engaged you as the lead GRC Consultant to design and implement a formal security governance framework.

**Key stakeholders:**
- Helena Marsh (CEO) — sponsor; needs to personally present the governance improvement plan to FCA
- Raj Patel (CISO) — currently reports to CTO; wants board access but hasn't been able to achieve it
- David Thompson (CFO) — willing to chair a Security Steering Committee; risk-aware
- Sarah Okonkwo (CTO) — currently Raj's line manager; technically focused; not engaged in governance
- Laura Chen (Head of Internal Audit) — Third Line; wants independence from CISO

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 3 — especially the Three Lines of Defense explanation
- [ ] Read the NCSC Board Toolkit for cyber governance guidance
- [ ] Read the FCA's operational resilience policy statement (PS21/3)
- [ ] Review the IIA's updated Three Lines Model (2020) from theiia.org

### Questions to Answer Before Starting
1. Why is it a governance risk that Apex's CISO reports to the CTO rather than directly to the CEO or board?
2. What are the three lines of defense and which teams at Apex sit in each line?
3. What is the difference between "Responsible" and "Accountable" in a RACI matrix?
4. What should be in a Security Committee Charter?
5. The FCA is a "supervisory" regulator. What does this mean for Apex's compliance obligations?

---

## Deliverables

### Deliverable 1: Security Governance Framework Document (5–8 pages)

**What It Is:** The definitive governance document for Apex's information security programme — defining structure, accountability, roles, and reporting. This is the document Helena will present to the FCA.

**Step-by-Step Instructions:**

1. **Cover page and version control**: Apex Financial Services | Security Governance Framework | Version 1.0 | Owner: CISO | Approved by: Board Risk Committee | Classification: Confidential | Review Date: Annual

2. **Section 1 — Purpose and Scope**: Why does Apex need this framework? What does it govern? Reference the FCA findings and the regulatory obligation to demonstrate adequate oversight.

3. **Section 2 — Governance Principles** (8 principles): Write 8 clear principles that will guide Apex's security governance. Examples: "Security is a business risk, not an IT problem." | "Board-level accountability for cyber risk is non-negotiable." | "All security decisions are risk-based and documented." Customise to reflect FCA regulated environment.

4. **Section 3 — Three Lines of Defense Model**:
   - First Line (Business and IT Operations): Define which teams own and operate controls; their responsibilities
   - Second Line (GRC, Risk, Compliance): Define the CISO, GRC team, and DPO roles; oversight and advisory functions
   - Third Line (Internal Audit): Define Internal Audit's role; reinforce independence from CISO

5. **Section 4 — Security Committee Structure**: Design three committees:
   - Board Risk and Audit Committee (quarterly): membership, mandate, agenda topics, quorum
   - Cyber Risk Steering Committee (monthly): chaired by CFO; membership includes CISO, CTO, Legal, HR; mandate; agenda
   - Security Operations Forum (bi-weekly): operational level; CISO chairs; IT security, DevOps, IT Ops; agenda

6. **Section 5 — Roles and Responsibilities**: Define specific security responsibilities for: Board | CEO | CFO | CISO | CTO | DPO | Business Unit Heads | All Employees

7. **Section 6 — Policy Framework Architecture**: Draw the hierarchy:
   - Level 1: Board-Approved Policies (e.g., Information Security Policy)
   - Level 2: Management-Approved Standards (e.g., Password Standard)
   - Level 3: Operational Procedures (e.g., User Access Provisioning Procedure)
   - Level 4: Guidelines and Best Practices

8. **Section 7 — Governance Reporting Cadence**: Define what gets reported, to whom, how often:
   - Monthly: CISO metrics report to CFO and Cyber Risk Steering Committee
   - Quarterly: CISO board report to Board Risk and Audit Committee
   - Annual: External audit report; ISMS management review

9. **Section 8 — Governance KPIs** (minimum 8): Define measurable KPIs with targets:
   - Policy review compliance rate (target: 100% reviewed within review date)
   - Risk register review frequency (monthly)
   - Security awareness training completion (target: 95% within 30 days of hire)
   - Audit finding closure rate (80% closed within agreed SLA)
   - Board reporting cadence (100% — no missed quarterly reports)
   - Incident response plan test completion (annually)
   - Vendor risk assessment completion rate (100% of Tier 1 vendors annually)
   - Third-party audit finding remediation rate (75% within SLA)

**Quality Bar:** Document reads as a real governance framework, not a textbook. FCA-specific context woven throughout. Three Lines of Defense clearly applied to Apex's actual team structure. KPIs are measurable with specific targets.

---

### Deliverable 2: RACI Matrix for GRC Activities

**What It Is:** A responsibility assignment matrix covering 15 major GRC activities at Apex, defining who is Responsible, Accountable, Consulted, and Informed for each.

**Step-by-Step Instructions:**

1. Create a matrix with GRC activities as rows and key roles as columns: CEO | CFO | CISO | CTO | DPO | Head of IT | Head of Legal | Head of Internal Audit | Business Unit Heads | All Staff

2. Cover these 15 activities:
   1. Information Security Policy approval and review
   2. Information security risk assessment
   3. Risk appetite setting
   4. Security awareness training programme
   5. GDPR/data protection compliance
   6. Vendor risk assessments
   7. Security incident response
   8. Internal security audit programme
   9. Business continuity planning
   10. CISO board reporting
   11. New system/project security review
   12. Penetration testing programme
   13. Compliance gap assessment
   14. Security budget allocation
   15. Regulatory (FCA) reporting on cyber matters

3. Apply RACI rigorously: Only ONE Accountable per activity. Multiple Responsible is fine. Consulted means they provide input. Informed means they receive output.

4. Add a brief legend explaining RACI definitions.

5. Highlight in a different colour any activities where the current state is problematic (e.g., "Board currently listed as Informed for risk assessment but should be Accountable for risk appetite").

---

### Deliverable 3: Security Committee Charters (3 charters)

**What It Is:** Formal charter documents for each of the three committees in Apex's new governance structure.

**For each charter, include:**
1. Committee name and classification
2. Purpose and mandate (why does this committee exist?)
3. Membership (role titles, not names; note who chairs)
4. Meeting frequency and quorum requirements
5. Standing agenda template
6. Decision authority (what can this committee decide? What must it escalate?)
7. Reporting line (who does this committee report to?)
8. Review date for the charter itself

**Charter 1: Board Risk and Audit Committee**
- Membership: 3 Board NEDs + Chair, CEO (attendee), CFO (attendee), CISO (attendee), External Auditor (periodic)
- Frequency: Quarterly
- Key mandate: Approve risk appetite; receive quarterly CISO report; oversee internal audit programme; escalate critical cyber risks to full board

**Charter 2: Cyber Risk Steering Committee**
- Membership: CFO (Chair), CISO, CTO, Head of Legal, DPO, Head of HR, Head of Internal Audit (observer)
- Frequency: Monthly
- Key mandate: Review monthly security metrics; approve risk treatments above CISO authority; approve new policies; receive compliance updates

**Charter 3: Security Operations Forum**
- Membership: CISO (Chair), Head of IT, Security Operations Lead, DevOps Lead, IT Infrastructure Manager
- Frequency: Bi-weekly
- Key mandate: Review operational security metrics; discuss open vulnerabilities and patches; review incident status; plan security initiatives

---

### Deliverable 4: Governance KPI Framework

**What It Is:** A professional KPI framework document defining 10+ governance metrics, targets, measurement methods, and reporting owners.

**Step-by-Step Instructions:**

1. For each KPI, define:
   - KPI Name
   - Definition (exactly what is measured)
   - Calculation method
   - Data source (where the data comes from)
   - Target
   - Reporting frequency
   - RAG thresholds (Green/Amber/Red values)
   - Reporting owner

2. Include at least 10 KPIs covering: policies, training, risk, audits, incidents, vendors, and board reporting.

3. Present as a table — this will be included in the CISO's monthly board pack.

---

### Deliverable 5: Security Governance Framework — Diagram

**What It Is:** A visual diagram (created in Lucidchart, Draw.io, or PowerPoint) showing Apex's governance structure — committees, reporting lines, and Three Lines of Defense.

**Instructions:**
- Show the Three Lines of Defense as horizontal bands
- Show committee hierarchy with reporting arrows
- Show CISO reporting line (recommended: CISO → CEO, with dotted line to Board Risk Committee)
- Use Apex branding colours if possible

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Framework Quality | 30% | Comprehensive, FCA-appropriate, Three Lines of Defense correctly applied |
| RACI Accuracy | 25% | RACI rules followed; one Accountable per activity; realistic for Apex |
| Professional Quality | 25% | Board and regulator-ready documents |
| Completeness | 20% | All 5 deliverables submitted |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **ISO 27001:2022 Clause 5** | Leadership requirements — roles, policy, top management commitment |
| **COBIT 2019** | IT governance principles applied to Apex's governance design |
| **IIA Three Lines Model** | Applied to define First, Second, and Third Lines at Apex |
| **FCA Operational Resilience (PS21/3)** | Regulatory context for governance requirements |

---

## Week-Specific Resources

- [IIA Three Lines Model (2020)](https://www.theiia.org/en/standards/the-iias-three-lines-model/) — Updated model from the Institute of Internal Auditors
- [NCSC Board Toolkit](https://www.ncsc.gov.uk/collection/board-toolkit) — Cyber governance guidance for boards
- [FCA Operational Resilience — PS21/3](https://www.fca.org.uk/publications/policy-statements/ps21-3-operational-resilience-financial-sector) — FCA regulatory context
- [ISACA COBIT 2019 Framework Overview](https://www.isaca.org/resources/cobit) — Governance framework reference
- [ISO 27001:2022 Clause 5 Requirements](https://www.iso.org/standard/27001) — Leadership and governance requirements
- [NCSC: 10 Steps to Cyber Security — Governance](https://www.ncsc.gov.uk/collection/10-steps/governance) — Practical governance guidance
- [Lucidchart — Free Org Chart Tool](https://www.lucidchart.com/) — For governance diagrams
- [Draw.io — Free Diagram Tool](https://app.diagrams.net/) — Alternative diagram tool

---

## Submission

```
Week-03/Deliverables/
├── Apex-Security-Governance-Framework-v1.0.md
├── Apex-RACI-Matrix-v1.0.xlsx
├── Apex-Committee-Charters-v1.0.md
├── Apex-Governance-KPI-Framework-v1.0.xlsx
└── Apex-Governance-Structure-Diagram-v1.0.png
```
