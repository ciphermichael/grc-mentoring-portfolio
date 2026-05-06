# Week 03 Learning Guide: Security Governance Frameworks

## What You Will Learn This Week

Governance is the skeleton of any security programme. Without it, security becomes reactive, underfunded, and unaccountable. This week you will design a complete security governance structure — defining who owns security, how decisions are made, how accountability flows, and how security performance is measured. You will produce the documents that senior GRC professionals and CISOs use to run enterprise security programmes: a governance framework, a RACI matrix, a committee charter, and a set of governance KPIs.

---

## Section 1: Core Concept Explained

### What Is Security Governance?

Security governance is the system by which an organisation **directs, controls, and accounts for** its information security programme. It defines who is responsible for security decisions, how those decisions are made, how accountability is structured, and how performance is measured and reported.

Think of governance as the constitutional framework of a country. The constitution defines who has what power, how laws are made, and who is accountable to whom. Security governance does the same for information security — it defines the CISO's authority, the board's oversight role, how policies are created and approved, how risks are escalated, and how security performance is reported.

Poor governance is the root cause of most security programme failures. When the CISO has no board access, when there are no clear security policies, when risk decisions are made ad-hoc, and when accountability is diffused across teams — the result is a fragmented, reactive, and underfunded security programme. Strong governance prevents this.

**The Three Lines of Defense** model is the most widely used governance framework in regulated industries. It separates the roles of those who own risk (First Line), those who manage and oversee risk (Second Line), and those who provide independent assurance (Third Line):
- **First Line**: Business operations and IT — they own and operate controls
- **Second Line**: GRC, Risk Management, Compliance — they set frameworks, monitor, and advise
- **Third Line**: Internal Audit, External Audit — they provide independent assurance

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **Governance** | System of direction, control, and accountability for security | Board approving the Information Security Policy |
| **Three Lines of Defense** | Governance model separating operations, oversight, and assurance | IT (1st), GRC (2nd), Internal Audit (3rd) |
| **RACI Matrix** | Responsibility Assignment Matrix: Responsible, Accountable, Consulted, Informed | CISO is Accountable for security strategy |
| **Security Committee** | Formal body that makes security governance decisions | Security Steering Committee meeting monthly |
| **Committee Charter** | Document defining a committee's mandate, membership, and operating rules | Board Risk Committee Charter |
| **Governance KPI** | Metric measuring the effectiveness of governance activities | % of policies reviewed on time |
| **Policy Hierarchy** | Structured levels of governance documents | Policies → Standards → Procedures → Guidelines |
| **CISO** | Chief Information Security Officer — executive responsible for security | Reports to CRO or CEO; presents to board |
| **DPO** | Data Protection Officer — required under GDPR for certain organisations | Responsible for GDPR compliance oversight |
| **Accountability** | Being answerable for outcomes, not just activities | CISO is accountable for security posture |
| **COBIT** | Control Objectives for Information and Related Technologies — IT governance framework | Used by auditors and IT governance professionals |
| **Board Risk Committee** | Board-level committee overseeing enterprise risk including cyber | Receives quarterly CISO reports |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Real-World Process

1. **Assess the current governance state** — Review existing committee structures, reporting lines, policy ownership, and accountability arrangements. Interview the CISO, CFO, and Legal Counsel to understand current gaps.
2. **Define the governance model** — Choose the appropriate governance structure for the organisation's size and complexity. A 50-person startup needs lightweight governance; a 5,000-person regulated firm needs formal committee structures.
3. **Apply the Three Lines of Defense** — Define which teams sit in each line and document their responsibilities clearly.
4. **Design the committee structure** — Most enterprises need at minimum: a Board Risk Committee (or Board Audit Committee), a Security Steering Committee (senior management), and an Operational Risk Forum (practitioners).
5. **Build the RACI matrix** — For every major GRC activity (policy development, risk assessment, vendor assessment, internal audit, incident response), assign who is Responsible, Accountable, Consulted, and Informed.
6. **Draft the committee charters** — Each committee needs a formal charter documenting: purpose, membership, quorum, meeting frequency, agenda, and decision authority.
7. **Define the reporting cadence** — How often does the CISO report to the board? What format? What metrics? Typically: monthly metrics to management, quarterly report to board, annual risk review.
8. **Establish governance KPIs** — Define measurable indicators of governance health: policy review compliance rate, risk review frequency, training completion rate, audit finding closure rate.
9. **Document the policy framework architecture** — Establish the hierarchy: Policies (board-approved, principles-based) → Standards (management-approved, specific requirements) → Procedures (operational instructions) → Guidelines (best practice advice).
10. **Socialise and get buy-in** — Governance only works if people know about it and accept it. Run awareness sessions with each Line of Defense.

### Real Company Example

Apex Financial Services is a 500-person UK financial advisory firm regulated by the FCA. Their new Head of GRC, Priya Sharma, is tasked with establishing a formal security governance structure following an FCA review that cited "inadequate board oversight of cyber risk."

Priya designs a three-tier committee structure: a Board Risk and Audit Committee (meeting quarterly, receiving CISO reports), a Cyber Risk Steering Committee (meeting monthly, chaired by CFO, attended by CISO, CTO, Head of Compliance, Legal Counsel), and a Security Operations Forum (meeting bi-weekly, operational practitioners).

She drafts a RACI matrix covering 18 GRC activities. Key accountability decisions: the CISO is Accountable for all security policies; the Board Risk Committee is Accountable for setting risk appetite; business line heads are Accountable for their own data and systems (First Line).

She also designs 8 governance KPIs: policy review compliance (target: 100% of policies reviewed within review date), risk register review frequency (monthly), training completion rate (target: 95% within 30 days of hire), audit finding closure rate (target: 80% of findings closed within agreed SLA), and board reporting cadence (quarterly). Within 6 months, the FCA's follow-up review notes "significant improvement in board oversight of cyber risk."

### What This Looks Like Day-to-Day

- Preparing the monthly Security Steering Committee pack (agenda, metrics, risk updates)
- Drafting and maintaining committee charters and terms of reference
- Tracking policy review schedules and chasing owners for overdue reviews
- Running quarterly governance maturity self-assessments
- Maintaining the RACI matrix as the organisation changes
- Writing the quarterly CISO board report
- Facilitating risk escalation discussions between business units and the CISO

---

## Section 3: Framework Deep Dive

### ISO 27001:2022 Clause 5 — Leadership

ISO 27001 requires demonstrable leadership and commitment from top management:

- **5.1 Leadership and commitment**: Top management must demonstrate commitment to the ISMS — not just sign a policy, but actively support, resource, and review the security programme.
- **5.2 Policy**: Management must establish an Information Security Policy that is appropriate to the organisation's purpose, includes security objectives, commits to continual improvement, and is communicated to all staff.
- **5.3 Organizational roles, responsibilities, and authorities**: Management must assign and communicate security roles. This is where the RACI matrix is used.

**Key ISO 27001 governance requirements**: Board-approved Information Security Policy; defined roles (CISO, Risk Owner, Asset Owner); management review at planned intervals (Clause 9.3).

### COBIT 2019 — IT Governance Framework

COBIT (Control Objectives for Information and Related Technologies) is an IT governance framework published by ISACA. Key concepts:
- **Governance vs Management**: COBIT distinguishes between governance (setting direction, evaluating, monitoring) and management (planning, building, running, monitoring).
- **5 Governance Principles**: Meeting stakeholder needs, covering the enterprise end-to-end, applying a single integrated framework, enabling a holistic approach, separating governance from management.
- **Governance and Management Objectives**: 5 governance objectives (EDM01–05) covering Ensured Governance Framework Setting, Benefits Delivery, Risk Optimization, Resource Optimization, Stakeholder Engagement.

COBIT is used heavily by IT auditors (CISA) and is worth understanding as it underpins many internal audit programmes.

---

## Section 4: Common Mistakes Beginners Make

1. **Creating governance structures that exist on paper only.** The most common governance failure is a beautiful framework document that nobody follows. Governance only works if committees meet regularly, reports are produced, and decisions are documented.

2. **Placing governance too deep in the organisation.** Security governance must have board-level visibility. If the CISO only reports to the CTO, cyber risk never reaches the board — and budgets reflect that.

3. **Confusing Responsible and Accountable in RACI.** Only ONE person can be Accountable (the one who answers for the outcome). Multiple people can be Responsible (those doing the work). This distinction is critical.

4. **Building a governance structure that doesn't match the organisation's size.** A 50-person startup doesn't need 5 committees. Start with the minimum viable governance structure and scale as the organisation grows.

5. **Writing committee charters that are too vague.** A charter that says "the committee will address security issues" is useless. It must specify: meeting frequency, quorum, decision authority, agenda template, and escalation paths.

6. **Treating the policy hierarchy as optional.** Without a clear policy hierarchy (Policy → Standard → Procedure), policies overlap, conflict, and become unenforceable.

7. **Not defining what "Informed" means in RACI.** If 50 people are listed as "Informed" on every activity, the governance structure becomes noise. Be selective — only those who genuinely need information to do their job.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **The Three Lines of Defense model is your interview answer for any question about governance structure** — learn it cold.
- **Always build a RACI matrix before writing policies** — you'll know who to consult, who to get approval from, and who needs to be trained.
- **Governance must be visible to be effective** — committee meetings should have minutes published, decisions communicated, and actions tracked.
- **Tailor governance to the organisation's culture** — a bureaucratic governance structure in a startup will be ignored; a minimal governance structure in a bank will fail regulatory review.
- **KPIs are the proof your governance works** — without measurable indicators, you can't demonstrate effectiveness to auditors or boards.
- **The CISO's reporting line matters** — a CISO who reports to the CIO has less board visibility and budget influence than one who reports to the CEO or CFO.
- **Get the Information Security Policy signed by the CEO or board** — it demonstrates top management commitment (required by ISO 27001 Clause 5.1).
- **Governance documentation ages quickly** — build review dates into every governance document from day one.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [ISO 27001:2022 Clause 5 — Leadership](https://www.iso.org/standard/27001) — Read the publicly available requirements
- [COBIT 2019 Framework](https://www.isaca.org/resources/cobit) — Free overview from ISACA
- [NCSC Cyber Governance Guidance](https://www.ncsc.gov.uk/guidance/board-toolkit) — Board Toolkit for cyber governance
- [FCA: Operational Resilience Governance](https://www.fca.org.uk/firms/operational-resilience) — Regulatory governance expectations
- [IIA Three Lines Model (2020)](https://www.theiia.org/en/standards/the-iias-three-lines-model/) — Updated Three Lines of Defense from the IIA
- [ISACA: IT Governance](https://www.isaca.org/resources/it-governance) — Free governance resources
- [UK Government Cyber Governance Code of Practice](https://www.ncsc.gov.uk/collection/board-toolkit) — NCSC Board Toolkit

### Books

- *COBIT 2019 Framework* by ISACA — Definitive IT governance reference
- *IT Governance* by Alan Calder & Steve Watkins — Practical governance implementation
- *The Security Leader's Communication Playbook* by Jeffrey Brown — How to communicate security to boards
- *CISA Review Manual* by ISACA — Comprehensive coverage of IT governance and control

### Online Courses

- [ISACA: COBIT Foundation](https://www.isaca.org/training-and-events/online-courses) — Foundational COBIT governance course
- [Coursera: IT Governance — University of California](https://www.coursera.org/learn/it-governance) — IT governance fundamentals
- [SANS: Security Policy and Governance (MGT514)](https://www.sans.org/cyber-security-courses/security-strategic-planning-policy-leadership/) — Advanced but excellent
- [YouTube: Three Lines of Defense Model Explained](https://www.youtube.com/results?search_query=three+lines+of+defense+governance) — Multiple free explanations

### Tools to Explore

- **Lucidchart / Draw.io** — For drawing governance structure diagrams and RACI matrices
- **Confluence / Notion** — Document governance frameworks, policies, and committee minutes
- **MetricStream** — Enterprise GRC platform; watch demo videos to see governance modules

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (Teaching Session — 90 min)

**Agenda:**
- 20 min: Lecture — What is security governance? Why does it matter? Show the Three Lines of Defense model with examples from real organisations.
- 20 min: Committee structures — Show a governance diagram for a financial services firm. Discuss who sits on what committee and why.
- 15 min: RACI exercise — Give students 5 GRC activities and ask them to assign RACI roles live. Discuss the differences.
- 15 min: Introduce the Apex Financial Services scenario; discuss what governance problems the FCA identified.
- 10 min: Show example CISO board report format and discuss what boards need to see.
- 10 min: Policy hierarchy explanation — walk through Policy → Standard → Procedure with a real example.

### Session B Focus (Assignment Review — 60 min)

- Review governance framework: Is it structured around the Three Lines of Defense? Are roles clearly defined?
- Check RACI matrix: Is there exactly ONE Accountable per activity? Are Responsible and Accountable correctly distinguished?
- Review committee charter: Does it include mandate, membership, quorum, frequency, agenda, and decision authority?
- Check governance KPIs: Are they measurable? Are there targets?
- Discuss: "Which governance decision in your framework has the most impact on overall security effectiveness?"

### Mentor Discussion Questions

1. "If the Apex CISO currently reports to the CTO, what governance risk does that create and how would you address it?"
2. "Why is the Three Lines of Defense model particularly important in a regulated financial services firm?"
3. "What's the difference between a Security Steering Committee and a Board Risk Committee in terms of purpose and membership?"
4. "How do you measure whether your governance structure is actually working?"
5. "What would you change about the governance structure if Apex doubled in size to 1,000 employees?"

### Red Flags to Watch For

- RACI matrix has multiple people listed as Accountable for a single activity
- Governance structure shows no board-level committee
- Committee charter has no quorum, meeting frequency, or decision authority defined
- KPIs are not measurable (e.g., "improve security awareness" rather than "training completion rate ≥ 95%")
- Framework exists only as a document with no implementation or monitoring mechanism described

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "Describe the Three Lines of Defense model and give an example of each line."
2. "What does a RACI matrix show and how do you build one?"
3. "What committees would you expect to see in a well-governed financial services company?"
4. "What should a CISO include in a quarterly board report?"
5. "What's the difference between a policy, a standard, a procedure, and a guideline?"
6. "How do you measure whether a security governance programme is effective?"
7. "What ISO 27001 clauses relate to governance and leadership?"
8. "If a CISO has no board access, what governance risks does that create?"
9. "What is the CISO's relationship to the board in a well-governed organisation?"
10. "Tell me about a governance structure you've designed or worked with."

### Keywords to Use

- Three Lines of Defense
- RACI matrix — Responsible, Accountable, Consulted, Informed
- Committee charter
- Policy hierarchy — policies, standards, procedures, guidelines
- Governance KPIs
- Board Risk Committee
- Security Steering Committee
- ISO 27001 Clause 5 (Leadership)
- COBIT 2019
- Top management commitment
- Reporting cadence
- Accountability vs responsibility
