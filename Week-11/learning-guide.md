# Week 11 Learning Guide: Internal Security Audit Fundamentals

## What You Will Learn This Week

Internal audit is the third line of defence in every governance framework — and it is one of the most valued GRC skills in the job market. This week you will learn the complete audit lifecycle, from planning through fieldwork through reporting. You will conduct a realistic access control audit using professional audit methodology (ISO 19011). Understanding how to design audit programmes, write audit plans, collect evidence, and draft findings is a skill that opens doors to GRC Analyst, IS Auditor, and Compliance Analyst roles.

---

## Section 1: Core Concept Explained

### What Is an Internal Security Audit?

An internal security audit is an independent, systematic, evidence-based examination of an organisation's information security controls to determine whether they are implemented and operating effectively. Unlike external audits (conducted by certification bodies or regulators), internal audits are conducted by the organisation's own team or by an internal audit function reporting independently to the board.

The purpose of an internal audit is to:
- Provide assurance that controls are working as intended
- Identify control deficiencies before external auditors or regulators do
- Drive continuous improvement in the security programme
- Meet regulatory and standard requirements (ISO 27001 Clause 9.2 mandates internal audits at planned intervals)

**ISO 19011:2018** — Guidelines for Auditing Management Systems — is the international standard that defines audit principles, audit programme management, and the audit process. It applies to all management system audits including ISO 27001 ISMS audits.

**ISO 19011 Audit Principles:**
1. Integrity — the foundation of professionalism
2. Fair presentation — truthful and accurate reporting
3. Due professional care — diligence and judgment
4. Confidentiality — discretion with audit information
5. Independence — basis for impartiality
6. Evidence-based approach — rational basis for conclusions
7. Risk-based approach — focus on highest-risk areas

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **Audit Charter** | Document defining the purpose, authority, and responsibility of the audit function | Board-approved; defines auditor independence |
| **Audit Programme** | Annual plan of all audits to be conducted | 6 audits planned for 2025 covering different domains |
| **Audit Plan** | Detailed plan for a specific audit | "Access Control Audit — MegaRetail — March 2025" |
| **Audit Scope** | What the audit covers | ISO 27001 A.5.15–5.22; user access management |
| **Audit Criteria** | Standards against which to audit | ISO 27001:2022 Annex A controls |
| **Fieldwork** | The actual evidence-gathering phase | Interviews, document review, technical testing |
| **Audit Finding** | A conclusion supported by evidence | "14% of user accounts not deprovisioned within SLA" |
| **Non-Conformance** | Failure to meet a required criterion | ISO 27001 control not implemented |
| **Observation** | Risk area not yet a non-conformance | "Access reviews conducted but not documented" |
| **Audit Report** | Formal output documenting findings | Management-facing report with findings and recommendations |
| **Corrective Action** | Remediation of a finding | "Implement automated deprovisioning process by Q2" |
| **Finding Severity** | Critical / High / Medium / Low / Informational | Critical = immediate risk; Informational = best practice |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Internal Audit Lifecycle (5 Phases)

**Phase 1 — Planning**
- Define the audit scope, objectives, and criteria
- Review prior audit findings and any known risk areas
- Build the audit plan: schedule, resource allocation, stakeholder communication
- Develop the fieldwork programme: what tests will be run, what evidence will be requested
- Send an opening communication to auditees

**Phase 2 — Fieldwork**
- Conduct opening meeting with auditees to explain the process
- Gather evidence: document review, staff interviews, technical testing, system screenshots
- Test controls: inquiry (ask), observation (watch), inspection (examine documents), re-performance (re-do the control yourself to verify)
- Document all evidence with references and dates
- Begin identifying potential findings

**Phase 3 — Evidence Analysis**
- Analyse evidence gathered against the audit criteria
- Identify non-conformances, observations, and positive findings
- Validate findings with auditees (avoid surprises in the final report)
- Assess the severity of each finding

**Phase 4 — Reporting**
- Write the audit report: executive summary, scope, methodology, findings, recommendations
- Present to CISO and management for review (factual accuracy, not to change findings)
- Issue formal audit report to management and Board/Audit Committee
- Agree corrective action plans and deadlines with management

**Phase 5 — Follow-Up**
- Track corrective action implementation
- Re-test remediated controls
- Update audit programme based on findings
- Report status to management and Board

### Real Company Example

The Head of Internal Audit at MegaRetail Ltd., David Chen, conducts a planned access control audit. MegaRetail has 2,000 employees across 85 stores and an HQ. They use Active Directory for user account management and a proprietary retail POS system.

David selects 30 user accounts as his sample for testing (statistical sampling: 10 from HQ, 10 from store managers, 10 from IT staff). He tests:
1. Are terminated users deprovisioned within 24 hours? (ISO 27001 A.5.18, A.6.5)
2. Are access rights reviewed quarterly? (ISO 27001 A.5.18)
3. Do privileged accounts have separate admin accounts from regular accounts? (A.8.2)
4. Is MFA enforced for all remote access? (A.8.5)

His findings: 4 of 30 accounts (13%) still active for terminated employees — the latest was 47 days post-termination. Access reviews documented for HQ but not for store systems. 3 IT administrators using their regular accounts for admin tasks (no PAM). MFA enforced for Office 365 but not for VPN.

These findings are rated: High (active terminated accounts), Medium (missing store access reviews), High (no PAM for admin accounts), High (MFA gap on VPN).

The audit report includes specific corrective actions: automated deprovisioning workflow implementation within 60 days; extension of access review programme to store systems within 90 days; PAM deployment within 120 days.

---

## Section 3: Framework Deep Dive

### ISO 27001:2022 — Internal Audit Requirements (Clause 9.2)

ISO 27001 Clause 9.2 requires:
- Internal audits conducted at planned intervals
- Audit programme considers importance of processes and results of previous audits
- Auditors must be objective and impartial (cannot audit their own work)
- Results reported to relevant management
- Documented information retained as evidence

**ISO 27001 Clause 10.2** — Non-conformity and corrective action:
When a non-conformance is found: react to control/correct it, evaluate cause, determine if similar non-conformances could exist, take action to address the cause, review effectiveness of action taken.

### ISO 19011 — Audit Process

The ISO 19011 audit process defines:
- **Audit types**: First-party (internal audit), Second-party (customer audit of supplier), Third-party (certification body audit)
- **Competence requirements**: Auditors must have appropriate knowledge, skills, and personal attributes
- **Evidence types**: Observable, demonstrable, documented
- **Sampling**: Risk-based sampling; sufficient coverage to support conclusions

### Control Testing Methods

| Method | Description | Example |
|--------|-------------|---------|
| **Inquiry** | Ask people about controls | "How do you handle terminated user access?" |
| **Observation** | Watch a control being performed | Watch an IT admin create a user account |
| **Inspection** | Examine a document or record | Review access review completion records |
| **Re-performance** | Independently re-execute the control | Run the same access review query the team uses |

---

## Section 4: Common Mistakes Beginners Make

1. **Auditing based on what management tells you, not what evidence shows.** The classic auditor error is accepting verbal assurances without evidence. "We review access monthly" requires access review records as evidence, not just the manager's statement.

2. **Over-scoping the audit.** Trying to audit everything in one audit is ineffective. Focus: one domain, one system, one risk area per audit. Depth over breadth.

3. **Not being specific in findings.** "Access control is weak" is not an audit finding. "3 of 10 sampled terminated accounts remained active beyond the 24-hour SLA, including one account active for 47 days post-termination" is an audit finding.

4. **Surprising management with findings in the report.** Good auditors validate findings with auditees before the final report. Surprises in the report damage relationships and reduce credibility.

5. **Not rating finding severity.** Every finding should be rated for severity. Without ratings, management cannot prioritise remediation. "Everything is High" is as useless as "everything is Low."

6. **Not following up on corrective actions.** An audit report that collects dust provides zero value. Follow up relentlessly. Track corrective actions monthly. Escalate overdue actions.

7. **Conflating audit role with management role.** Auditors provide independent assurance — they do not implement controls or take corrective actions themselves. Maintaining independence is critical.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Sample strategically, not randomly** — focus your sample on the highest-risk areas. For access control: focus on privileged accounts, IT/admin accounts, and recent joiners/leavers.
- **The opening meeting sets the tone** — explain the audit purpose, methodology, and what you'll need from auditees. A collaborative tone gets better cooperation and more candid responses.
- **Maintain an audit evidence log** — every piece of evidence referenced in findings must be traceable. Document source, date collected, and format.
- **Use a finding template** — consistent finding format (Condition, Criteria, Cause, Effect, Recommendation) makes reports professional and auditor-ready.
- **Positive findings matter too** — always acknowledge well-controlled areas. "The quarterly access review process for cloud systems was found to be effective and well-documented" is valuable feedback.
- **Risk-rate your findings honestly** — use your organisation's severity definitions consistently. A Critical finding that turns out to be Low after management review damages credibility.
- **Build relationships with IT and operations** — internal auditors who are seen as adversaries get cooperation; those seen as partners get information.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [ISO 27001:2022 Clause 9.2](https://www.iso.org/standard/27001) — Internal audit requirements
- [ISO 19011:2018 Guidelines](https://www.iso.org/standard/70017.html) — Audit management standard overview
- [IIA: International Standards for the Professional Practice of Internal Auditing](https://www.theiia.org/en/standards/) — Free access to IIA standards
- [ISACA IS Audit and Assurance Standards](https://www.isaca.org/resources/isaca-journal/issues/2016/volume-1/is-audit-and-assurance-standards-and-guidelines) — IS audit standards
- [NCSC: Internal Audit of Cyber Risk](https://www.ncsc.gov.uk/guidance/board-toolkit) — Practical guidance
- [CISA Review Manual Chapter 1 — IS Audit Process](https://www.isaca.org/credentialing/cisa) — Foundational IS audit process

### Books

- *CISA Review Manual* by ISACA — The definitive IS audit reference; Chapters 1–3
- *Internal Auditing Handbook* by K.H. Spencer Pickett — Comprehensive audit methodology
- *IT Audit Handbook* by Chris Davis — IT-specific audit guidance

### Online Courses

- [ISACA: CISA Exam Preparation](https://www.isaca.org/credentialing/cisa) — Covers audit process in depth
- [IIA: Internal Audit Fundamentals](https://www.theiia.org/en/learning/) — Foundation-level internal audit
- [SANS: Auditing Networks, Perimeters, and Systems (AUD507)](https://www.sans.org/cyber-security-courses/auditing-networks-perimeters-and-systems/) — Technical audit skills

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (90 min)

- 20 min: Audit lifecycle — walk through all 5 phases with a real example; what happens in each
- 20 min: Control testing methods — inquiry, observation, inspection, re-performance with examples
- 20 min: Finding writing exercise — give student a "bad" finding and work together to rewrite it using Condition, Criteria, Cause, Effect, Recommendation format
- 15 min: Audit sampling — explain risk-based sampling; how many accounts to sample for a 2,000-person company
- 15 min: Introduce MegaRetail scenario; identify what a focused access control audit scope looks like

### Session B Focus (60 min)

- Review audit plan: Is scope clear? Are tests specific? Is sampling methodology explained?
- Check findings: Are they evidence-based? Specific? Correctly severity-rated?
- Review audit report: Is it written in business language? Does the executive summary convey the key risk?
- Ask: "Walk me through your most critical finding and how you would present it to the MegaRetail CISO."

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "Walk me through the internal audit lifecycle."
2. "What are the 4 types of audit evidence?"
3. "What is ISO 27001 Clause 9.2?"
4. "What makes a good audit finding?"
5. "How do you stay independent as an internal auditor?"
6. "What is the difference between a finding and an observation?"
7. "How do you determine the scope of an internal audit?"
8. "What is an audit charter?"
9. "How do you prioritise audit findings for remediation?"
10. "Tell me about an audit you conducted — what did you find?"
11. "What is risk-based auditing?"

### Keywords to Use

- ISO 19011 audit principles
- ISO 27001 Clause 9.2 (internal audit)
- Audit lifecycle: Planning, Fieldwork, Analysis, Reporting, Follow-up
- Control testing: inquiry, observation, inspection, re-performance
- Audit finding: Condition, Criteria, Cause, Effect, Recommendation
- Finding severity: Critical, High, Medium, Low, Informational
- Independence and objectivity
- Risk-based sampling
- Corrective action tracking
- Three Lines of Defense (Third Line = Internal Audit)
