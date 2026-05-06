# Week 05 Learning Guide: ISO 27001:2022 Deep Dive

## What You Will Learn This Week

ISO 27001 is the most globally recognised cybersecurity certification. If you master one framework in GRC, this is the one. This week you will go deep — understanding every clause, mapping all 93 Annex A controls, conducting a formal gap assessment with maturity scoring, and building an implementation roadmap. By the end of this week you will be able to have an expert-level conversation about ISO 27001 with CISOs, auditors, and certification bodies. This is one of the most heavily weighted topics in every GRC interview.

---

## Section 1: Core Concept Explained

### What Is ISO 27001:2022?

ISO/IEC 27001:2022 is an international standard published by the International Organization for Standardization (ISO) and the International Electrotechnical Commission (IEC). It specifies the requirements for establishing, implementing, maintaining, and continually improving an **Information Security Management System (ISMS)**.

The key word is "management system" — ISO 27001 is not just a checklist of technical controls. It requires organisations to build a **systematic, documented, risk-based approach** to managing information security. This means: defining scope, assessing risks, selecting controls based on those risks, implementing them, monitoring their effectiveness, and continually improving.

**Why ISO 27001 matters:** Increasingly, enterprises require ISO 27001 certification from their technology vendors before signing contracts. It is the trusted signal that an organisation has a mature, audited security programme. UK and EU government contracts, NHS supplier requirements, major enterprise SaaS deals — all increasingly require it. A UKAS-accredited ISO 27001 certificate from a recognised certification body (BSI, LRQA, DNV) carries global credibility.

**ISO 27001:2022 vs 2013:** The 2022 revision made significant changes:
- Control count changed from 114 (14 domains) to **93 controls (4 domains)**
- 4 new domains: Organizational, People, Physical, Technological
- 11 new controls added (including A.8.25 Secure Development Lifecycle, A.8.16 Monitoring Activities)
- Control attributes added (cybersecurity concepts, operational capabilities, information security properties)
- Stronger emphasis on threat intelligence and information security in projects

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **ISMS** | Information Security Management System — the documented, risk-based approach to managing security | ISO 27001 requires a documented ISMS |
| **Statement of Applicability (SoA)** | Document declaring which of the 93 controls apply and why | Mandatory ISO 27001 deliverable |
| **Gap Assessment** | Analysis of current state vs ISO 27001 requirements | Scored 0–5 maturity for each control |
| **Maturity Score** | Rating (0–5) of how well a control is implemented | 0=Not Exist, 3=Defined, 5=Optimised |
| **Certification Audit** | Two-stage audit by accredited certification body | Stage 1 (document review) + Stage 2 (implementation audit) |
| **UKAS** | United Kingdom Accreditation Service — accredits certification bodies | BSI, LRQA, DNV are UKAS-accredited |
| **Annex A** | The 93 controls referenced in ISO 27001 | Grouped in 4 domains |
| **Clause 6.1.2** | Risk assessment requirements within ISO 27001 | Must identify, analyse, and evaluate risks |
| **Clause 9.2** | Internal audit requirement | Must conduct at planned intervals |
| **Clause 9.3** | Management review requirement | Top management must review the ISMS |
| **Non-Conformance** | Failure to meet ISO 27001 requirement | Found during audit; must be corrected |
| **Continual Improvement** | Ongoing enhancement of ISMS effectiveness | Required by Clause 10 |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Real-World ISO 27001 Implementation Process

1. **Secure management commitment** — ISO 27001 fails without top management buy-in. Get the CEO or board to formally support the project, allocate budget, and approve an implementation project.

2. **Define ISMS scope** — The scope statement defines what is inside the ISMS. It covers: the organisation's activities and locations, the information assets included, the boundaries of the ISMS. A SaaS company might scope to "all systems used to deliver the [ProductName] SaaS platform, including cloud infrastructure, internal development systems, and support tools."

3. **Conduct gap assessment** — Assess current state against all Clauses (4–10) and all 93 Annex A controls. Score each control on a 0–5 maturity scale. This produces the roadmap inputs.

4. **Conduct information security risk assessment** — Per Clause 6.1.2, identify threats, assess likelihood and impact, score risks, identify treatment options.

5. **Produce Statement of Applicability (SoA)** — For every one of the 93 Annex A controls: Is it applicable (Yes/No)? If yes, what is the implementation status? If no, justification for exclusion. This is a mandatory deliverable.

6. **Implement controls** — Based on the SoA and risk treatment decisions, implement the required controls. Write policies, configure technical controls, establish processes, run awareness training.

7. **Run internal audits** — Clause 9.2 requires internal audits at planned intervals. The internal audit tests whether the ISMS is implemented and effective.

8. **Management review** — Clause 9.3 requires top management to formally review the ISMS. Inputs: audit findings, risk assessment results, non-conformances, KPI performance. Output: decisions on improvements.

9. **Stage 1 Audit (Certification body)** — The certification body (e.g., BSI) reviews all ISMS documentation. They check: Does the scope make sense? Is the SoA complete? Are the mandatory clauses documented? They issue a Stage 1 audit report identifying readiness for Stage 2.

10. **Stage 2 Audit (Certification body)** — The auditor visits (on-site or remotely) to test implementation. They select a sample of controls and test them against evidence. They interview staff. If no major non-conformances, they issue the ISO 27001 certificate.

11. **Surveillance audits** — Certificate is valid for 3 years, subject to annual surveillance audits checking continued compliance.

### Real Company Example

Xown Solutions Limited is a UK SaaS company providing financial reporting software to mid-sized businesses. They have 120 employees. Their biggest potential client — a FTSE 250 company — requires ISO 27001 certification before signing a £2M contract.

Their GRC Manager, Rachel Thompson, leads the ISO 27001 project. She starts by defining the ISMS scope: "The development, hosting, and support of the Xown financial reporting SaaS platform, hosted on Microsoft Azure, with offices in Birmingham and London."

She conducts a 4-week gap assessment covering all 93 controls. Key findings:
- Organizational controls: 60% compliant — most policies exist but are outdated
- People controls: 40% compliant — no formal security awareness training programme
- Physical controls: 75% compliant — office security is good; remote working procedures weak
- Technological controls: 45% compliant — patch management inconsistent; no privileged access management; monitoring and logging incomplete

Rachel identifies 23 High-priority gaps requiring remediation before Stage 1 audit. She builds a 6-month implementation roadmap, assigns owners to each gap, and secures £85,000 budget for PAM tooling, SIEM implementation, and training programme development. The FTSE 250 client signs a letter of intent pending certification.

---

## Section 3: Framework Deep Dive

### ISO 27001:2022 Clause Structure (Clauses 4–10)

**Clause 4 — Context of the Organisation**
- 4.1: Understanding the organisation and its context (internal/external issues)
- 4.2: Understanding the needs and expectations of interested parties (stakeholders)
- 4.3: Determining the scope of the ISMS
- 4.4: Information security management system (ISMS)

**Clause 5 — Leadership**
- 5.1: Leadership and commitment
- 5.2: Policy (Information Security Policy)
- 5.3: Organizational roles, responsibilities, and authorities

**Clause 6 — Planning**
- 6.1.1: Actions to address risks and opportunities
- 6.1.2: Information security risk assessment
- 6.1.3: Information security risk treatment (includes SoA requirement)
- 6.2: Information security objectives

**Clause 7 — Support**
- 7.1: Resources | 7.2: Competence | 7.3: Awareness | 7.4: Communication | 7.5: Documented information

**Clause 8 — Operation**
- 8.1: Operational planning and control
- 8.2: Information security risk assessment (perform)
- 8.3: Information security risk treatment (implement)

**Clause 9 — Performance Evaluation**
- 9.1: Monitoring, measurement, analysis, and evaluation
- 9.2: Internal audit
- 9.3: Management review

**Clause 10 — Improvement**
- 10.1: Continual improvement
- 10.2: Non-conformity and corrective action

### Annex A — 93 Controls in 4 Domains

**Organizational Controls (A.5) — 37 controls**
Key controls: A.5.1 Policies, A.5.2 Roles and responsibilities, A.5.14 Information transfer, A.5.23 Information security for cloud services, A.5.24 IS incident management planning, A.5.30 ICT readiness for business continuity

**People Controls (A.6) — 8 controls**
Key controls: A.6.1 Screening, A.6.3 Security awareness training, A.6.5 Responsibilities after termination, A.6.8 Information security event reporting

**Physical Controls (A.7) — 14 controls**
Key controls: A.7.1 Physical security perimeters, A.7.3 Securing offices, A.7.9 Security of assets off-premises, A.7.14 Secure disposal/reuse of equipment

**Technological Controls (A.8) — 34 controls**
Key controls: A.8.2 Privileged access rights, A.8.5 Secure authentication, A.8.7 Protection against malware, A.8.8 Management of technical vulnerabilities, A.8.16 Monitoring activities, A.8.24 Use of cryptography, A.8.25 Secure development lifecycle

---

## Section 4: Common Mistakes Beginners Make

1. **Scoping the entire organisation when a tighter scope is more manageable.** Beginners often try to scope everything. Starting with a defined product or system reduces complexity, cost, and time to certification.

2. **Treating the SoA as a form to fill in rather than a risk-based decision document.** Every "Not Applicable" needs a clear justification. Every "Applicable" needs implementation evidence. Auditors scrutinise the SoA carefully.

3. **Underestimating the evidence burden.** ISO 27001 requires documented evidence for most controls. "We do it but haven't written it down" fails an audit. Everything must be documented.

4. **Ignoring the mandatory Clauses (4–10) and focusing only on Annex A.** Many beginners think ISO 27001 is just 93 controls. In reality, the mandatory clauses (risk assessment, management review, internal audit, objectives) are equally important and heavily audited.

5. **Not conducting an internal audit before the Stage 2.** An internal audit (Clause 9.2) is mandatory and must happen before the certification audit. It identifies non-conformances that would fail the Stage 2 audit.

6. **Forgetting Clause 9.3 — Management Review.** Top management must formally review the ISMS. This must be documented with inputs (audit results, risk assessment, KPIs) and outputs (decisions, action items). Many organisations skip this.

7. **Letting scope creep during implementation.** Once scope is defined and approved, resist adding new systems mid-project. Each addition restarts parts of the process.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Know the 2022 vs 2013 differences cold** — this is an extremely common interview question. 93 controls (4 domains) vs 114 controls (14 domains); 11 new controls; new attribute framework.
- **The SoA is the most important document in an ISO 27001 programme** — treat it like the programme's constitution; keep it current.
- **Use a maturity model for gap assessments** — 0-5 scoring is more useful than binary yes/no because it shows progress over time and prioritises investment.
- **Start with the high-risk controls** — when building a remediation roadmap, prioritise controls that address the organisation's top risks, not alphabetical order.
- **Certification body choice matters** — BSI, LRQA, DNV, and Bureau Veritas are major UKAS-accredited certification bodies. Costs and styles vary; get quotes from 2–3.
- **An internal audit before Stage 2 is not optional** — use it to find your own non-conformances before the external auditor does.
- **The surveillance audit is as important as certification** — non-conformances found in annual surveillance audits can suspend or withdraw the certificate.
- **Build ISO 27001 into the business culture** — organisations that treat it as a project (not a programme) typically fail their surveillance audits.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [ISO 27001:2022 — Official Standard Overview](https://www.iso.org/standard/27001) — Public overview and structure
- [ISO 27002:2022 — Controls Guidance](https://www.iso.org/standard/75652.html) — Companion standard explaining how to implement each of the 93 controls
- [NCSC Cyber Security Framework — Mapping to ISO 27001](https://www.ncsc.gov.uk/section/products-services/ncsc-for-startups) — NCSC resources for implementation
- [UKAS Accreditation Directory](https://www.ukas.com/find-an-organisation/) — Find UKAS-accredited ISO 27001 certification bodies in the UK
- [ISO 27001 Academy — Free Resources](https://advisera.com/27001academy/iso-27001-resources/) — Free templates and guides from Advisera
- [IT Governance: ISO 27001 Gap Analysis Tool](https://www.itgovernance.co.uk/iso27001) — Free gap analysis tools
- [BSI Knowledge Centre — ISO 27001](https://www.bsigroup.com/en-GB/ISO-27001-Information-Security/) — Resources from a major certification body

### Books

- *ISO 27001:2022 — A Pocket Guide* by Alan Calder — Concise, practical, essential reading
- *Nine Steps to Success: An ISO 27001 Implementation Overview* by Alan Calder — Step-by-step implementation guide
- *ISO 27001 Controls: A Guide to Implementing and Auditing* by Bridget Kenyon — Comprehensive control implementation guide
- *The CISA Exam Guide* by ISACA — Covers information security management systems in depth

### Online Courses

- [Udemy: ISO 27001 Lead Implementer Preparation](https://www.udemy.com/course/iso-iec-27001-information-security-management/) — Highly rated; covers implementation in detail
- [Coursera: Introduction to Information Security](https://www.coursera.org/learn/intro-cyber-security) — Foundational security concepts
- [PECB: ISO 27001 Foundation](https://pecb.com/en/education-and-certification-for-individuals/iso-iec-27001) — Official PECB foundation training
- [YouTube: ISO 27001 Explained — The GRC Channel](https://www.youtube.com/results?search_query=iso+27001+explained) — Multiple free explainer videos
- [IT Governance Online Training](https://www.itgovernance.co.uk/online-courses/iso27001) — UK-focused ISO 27001 training

### Tools to Explore

- **Vanta** — Automates ISO 27001 evidence collection and control monitoring; request a demo
- **Drata** — Similar compliance automation with ISO 27001 support
- **Microsoft Purview Compliance Manager** — Includes ISO 27001 assessment template for Microsoft 365 environments

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (Teaching Session — 90 min)

**Agenda:**
- 25 min: ISO 27001 structure walkthrough — Clauses 4–10 explained with examples. Show where auditors focus.
- 20 min: Annex A domains — walk through the 4 domains and key controls. Emphasise the new 2022 controls.
- 15 min: SoA exercise — for 10 sample controls, decide together: applicable? Implementation status? Evidence needed?
- 15 min: Maturity scoring exercise — score 5 controls using the 0–5 scale for a fictional company.
- 15 min: Introduce Xown Solutions scenario; discuss what a realistic scope statement looks like.

### Session B Focus (Assignment Review — 60 min)

- Review ISMS scope statement — is it specific? Does it define boundaries clearly? Is it the right scope for the business?
- Check SoA — are all 93 controls addressed? Are "Not Applicable" exclusions justified? Are implementation statuses realistic?
- Review gap assessment — is maturity scoring consistent? Are High-priority gaps correctly identified?
- Check implementation roadmap — is sequencing logical? Are owners assigned? Are timelines realistic?
- Ask: "Walk me through your top 3 gaps and why you prioritised them."

### Mentor Discussion Questions

1. "Xown Solutions wants to scope only their development systems. What are the risks of scoping too narrowly?"
2. "A control is marked 'Not Applicable' in the SoA because 'we don't have physical servers'. Is this justification sufficient for A.7.8 Clear Desk?"
3. "What's the difference between a Stage 1 and Stage 2 audit? What happens if you fail Stage 1?"
4. "Your gap assessment shows that Technological Controls are only 45% compliant. Which 5 controls would you fix first and why?"
5. "The CEO asks why ISO 27001 certification is worth £80,000. How do you justify the investment?"

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "Walk me through the structure of ISO 27001:2022."
2. "What changed between ISO 27001:2013 and ISO 27001:2022?"
3. "What is a Statement of Applicability and why is it important?"
4. "How do you define ISMS scope?"
5. "What are the mandatory clauses of ISO 27001?"
6. "What is the difference between a Stage 1 and Stage 2 audit?"
7. "What are the 4 domains of Annex A in ISO 27001:2022?"
8. "Name 5 controls from Annex A and explain what they require."
9. "What is a non-conformance and what happens when one is found?"
10. "How long does ISO 27001 certification take and what does it cost?"
11. "What is the difference between ISO 27001 and ISO 27002?"
12. "What are surveillance audits?"

### How to Answer Key Questions

**Q: "What changed from ISO 27001:2013 to 2022?"**

*Answer:* "The 2022 revision consolidated the control set from 114 controls across 14 Annex A domains to 93 controls across 4 domains — Organizational, People, Physical, and Technological. 11 new controls were added, including A.5.23 for cloud services security, A.5.30 for ICT readiness for business continuity, A.8.16 for monitoring activities, and A.8.25 for secure development lifecycle. Controls also now have an attribute framework covering cybersecurity concepts, operational capabilities, and information security properties. The core clause structure (Clauses 4–10) remained broadly the same, with enhanced emphasis on risk management and threat intelligence."

### Keywords to Use

- ISMS — Information Security Management System
- Statement of Applicability (SoA)
- Maturity scoring (0–5 scale)
- Annex A — 4 domains, 93 controls
- Mandatory clauses (4–10)
- UKAS accreditation
- Stage 1 and Stage 2 audit
- Non-conformance / corrective action
- Continual improvement (Clause 10)
- Risk-based approach (Clause 6.1.2)
- Internal audit (Clause 9.2)
- Management review (Clause 9.3)
