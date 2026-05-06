# Week 02 Learning Guide: Risk Management Fundamentals

## What You Will Learn This Week

Risk management is the analytical engine of GRC — the process that converts vague security concerns into prioritised, quantified, business-relevant decisions. This week you will build and populate a professional risk register, construct a 5×5 risk matrix, and write a risk assessment report — the three artefacts that GRC professionals produce more often than anything else. By the end of this week you will think in terms of threats, vulnerabilities, likelihood, and impact in every situation.

---

## Section 1: Core Concept Explained

### What Is Cybersecurity Risk Management?

Risk is the **potential for loss or harm** resulting from a threat exploiting a vulnerability. Risk management is the structured process of identifying, assessing, prioritising, and treating these risks so the organisation can make informed decisions about where to invest in security controls.

The core equation every GRC professional must memorise is:

> **Risk = Threat × Vulnerability × Impact**

Or in simpler terms: a risk only materialises when a **threat** (something that can cause harm — a hacker, a fire, a disgruntled employee) exploits a **vulnerability** (a weakness in your defences — unpatched software, no MFA, lack of access reviews) and causes an **impact** (financial loss, data breach, operational disruption).

Risk management matters because no organisation can eliminate all risk — it would be prohibitively expensive. Instead, GRC professionals help organisations understand their **risk appetite** (how much risk the board is willing to accept) and **risk tolerance** (the acceptable deviation from the appetite), then prioritise controls to bring risk within those boundaries.

**ISO 27001 Clause 6.1.2** requires organisations to establish and maintain an information security risk assessment process. **ISO 27005:2022** provides the specific guidance on how to conduct that process. **NIST SP 800-30** is the US equivalent for conducting risk assessments.

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **Threat** | Any circumstance or event with potential to cause harm | Ransomware actor, insider threat, power outage |
| **Vulnerability** | A weakness that could be exploited by a threat | No MFA, unpatched CVE, poor access management |
| **Likelihood** | Probability that a threat will exploit a vulnerability | Rated 1 (rare) to 5 (almost certain) |
| **Impact** | Severity of harm if the risk materialises | Financial loss, data breach, reputational damage |
| **Inherent Risk** | Risk level before any controls are applied | Raw exposure |
| **Residual Risk** | Risk level after controls have been applied | Acceptable or needs further treatment |
| **Risk Appetite** | Amount of risk the board is willing to accept | "We accept low and medium risks; escalate high/critical" |
| **Risk Tolerance** | Acceptable deviation above the risk appetite threshold | "Up to 3 high risks in active remediation" |
| **Risk Treatment** | The chosen response to a risk | Mitigate, Accept, Transfer, Avoid |
| **Risk Register** | The documented record of all identified risks | Spreadsheet with 20+ enterprise risks |
| **Risk Owner** | The individual accountable for managing a specific risk | Head of IT is owner of Ransomware risk |
| **Risk Heatmap** | Visual representation of risks by likelihood × impact | 5×5 matrix with colour-coded zones |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Real-World Process

1. **Define scope and methodology** — Agree with stakeholders which systems, processes, and data assets are in scope. Choose the scoring methodology (typically a 5×5 qualitative matrix for most organisations, or quantitative FAIR model for mature/financial organisations).
2. **Asset identification** — List all information assets: data (customer data, financial records), systems (CRM, ERP, cloud infrastructure), processes (payment processing, onboarding), and people.
3. **Threat identification** — For each asset, identify realistic threats. Use sources like NCSC Threat Intelligence, ENISA Threat Landscape, and industry-specific threat reports.
4. **Vulnerability identification** — Identify weaknesses that each threat could exploit. Sources: penetration test findings, vulnerability scans, audit findings, staff interviews.
5. **Likelihood scoring** — Rate likelihood 1–5: 1=Rare (less than once in 5 years), 2=Unlikely (once in 3–5 years), 3=Possible (once per year), 4=Likely (multiple times per year), 5=Almost Certain (frequent).
6. **Impact scoring** — Rate impact 1–5 across dimensions: Financial, Operational, Reputational, Regulatory. Score is the highest dimension. 1=Negligible, 2=Minor, 3=Moderate, 4=Major, 5=Catastrophic.
7. **Calculate inherent risk score** — Likelihood × Impact = score (1–25). Map to rating: 1–4=Low, 5–9=Medium, 10–16=High, 17–25=Critical.
8. **Identify current controls** — Document controls already in place that reduce likelihood or impact.
9. **Calculate residual risk** — Re-score after applying current controls.
10. **Determine risk treatment** — For each risk: Mitigate (add controls), Accept (document and monitor), Transfer (insurance/outsource), Avoid (stop the activity).
11. **Assign risk owners** — Every risk must have a named owner accountable for treatment.
12. **Build risk register** — Compile everything into a structured, professional spreadsheet or document.

### Real Company Example

Sarah Mitchell joined CloudSafe Ltd. as their first GRC Analyst. CloudSafe is a UK cloud storage company with 150 employees, holding data for 3,000 business customers. They had no formal risk management programme.

Sarah started by running a two-day risk workshop with the CISO, IT Manager, Head of Operations, and Legal Counsel. She used a structured questionnaire to identify threats relevant to a cloud storage company: ransomware, insider data theft, third-party cloud provider failure (they used AWS), accidental data deletion by customers, and GDPR non-compliance.

She then produced a 5×5 risk matrix showing 22 risks. The top 3 (Critical): Ransomware encryption of customer data (Likelihood 4 × Impact 5 = 20), Third-party AWS outage (Likelihood 3 × Impact 5 = 15), Customer data leaked by misconfigured storage bucket (Likelihood 4 × Impact 4 = 16).

The CISO used the risk register to secure a £140,000 budget for endpoint detection and response (EDR), privileged access management (PAM), and backup hardening — exactly the controls Sarah recommended to mitigate the top 3 risks.

### What This Looks Like Day-to-Day

- Running risk workshops with business stakeholders (1–2 hours each)
- Populating and updating the risk register monthly
- Reviewing new CVEs and assessing if they introduce new risks
- Writing risk treatment recommendations with cost-benefit analysis
- Presenting the risk register update to the Security Committee
- Tracking remediation actions against risk treatment plans
- Reviewing third-party risk assessments and adding vendor risks to the register

---

## Section 3: Framework Deep Dive

### ISO 27001:2022 Risk Management Requirements

**Clause 6.1 — Actions to address risks and opportunities**
- 6.1.1: General — organisations must consider what risks and opportunities need to be addressed
- 6.1.2: Information security risk assessment — must include: define risk acceptance criteria, ensure repeatable assessments, identify risks, analyse risks (likelihood × impact), evaluate risks against risk acceptance criteria
- 6.1.3: Information security risk treatment — select appropriate treatment options, determine controls required, produce Statement of Applicability (SoA)

**Clause 8.2** — Perform information security risk assessments at planned intervals or when significant changes occur.

### NIST CSF 2.0 — Risk Management Functions

- **GOVERN (GV)**: GV.RM — Establish and communicate risk management strategy, appetite, and tolerance
- **IDENTIFY (ID)**: ID.RA — Risk Assessment — Identify threats, vulnerabilities, likelihood, impact
- **PROTECT (PR)**: Controls implemented based on risk assessment findings
- **DETECT/RESPOND/RECOVER**: Assume breach — detect incidents, respond, and recover

### Risk Treatment Options (ISO 27001 Terminology)

| Treatment | Description | When to Use |
|-----------|-------------|-------------|
| **Mitigate** | Implement controls to reduce likelihood or impact | When risk exceeds appetite and cost of control is justified |
| **Accept** | Document and accept the risk | When cost of mitigation exceeds benefit or risk is within appetite |
| **Transfer** | Use insurance or outsourcing to shift financial burden | Cyber insurance, outsourcing high-risk functions |
| **Avoid** | Stop the activity that creates the risk | When risk is unacceptably high and no cost-effective mitigation exists |

---

## Section 4: Common Mistakes Beginners Make

1. **Copying risks from the internet.** Generic risks ("data breach", "malware") without tailoring to the specific organisation are useless. Every risk must be specific: "Ransomware encrypting the AWS production database due to lack of EDR on EC2 instances."

2. **Mixing up inherent and residual risk.** Inherent risk is the raw exposure. Residual risk is what remains after controls. Many beginners only calculate one or conflate them.

3. **Scoring everything as High.** Risk registers where every risk is rated "High" are useless for prioritisation. Learn to apply the scoring methodology consistently — not everything is catastrophic.

4. **No risk owners.** A risk with no named owner will never be treated. Every risk must have a specific person accountable, not a team or role.

5. **Treating risk management as a one-time exercise.** Risk registers must be maintained. Risks change as the threat landscape evolves, as new systems are introduced, and as controls are implemented.

6. **Ignoring the risk appetite.** Risk treatment recommendations must be framed against the organisation's stated risk appetite. If the board accepts "Low" risks, you don't need to remediate every Low-rated risk.

7. **Not linking risks to assets.** Every risk must be traceable to a specific information asset or business process. "Risk: ransomware" with no linked asset is incomplete.

8. **Forgetting to document evidence.** When risks are treated (controls implemented), evidence must be documented. Without evidence, auditors cannot verify the control works.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Run risk workshops, don't work in isolation** — The best risks are identified collaboratively with IT, Legal, Finance, and Operations. Each business unit sees different threats.
- **Use the NCSC Threat Intelligence publications** for threat context relevant to UK organisations.
- **Reference ENISA Threat Landscape** for EU threat intelligence and annual reports on top threats.
- **Always score impact across multiple dimensions** — financial, operational, reputational, and regulatory. A data breach might be Low financial impact but Critical reputational impact.
- **The risk register is a living document** — review it monthly, update when new threats emerge, and re-score when controls are implemented.
- **Quantify where possible** — even in qualitative risk programmes, try to attach a £ value to the impact. "£500K potential fine + £200K incident response cost" is more compelling to boards than "Critical".
- **Use the FAIR model for top risks** — even if you use qualitative scoring for most risks, apply Factor Analysis of Information Risk (FAIR) to your top 3 risks to quantify them in monetary terms.
- **Risk heatmaps are powerful communication tools** — a 5×5 colour-coded matrix shows the risk landscape at a glance. Always produce one.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [ISO 27005:2022 Overview](https://www.iso.org/standard/80585.html) — Information security risk management standard
- [NIST SP 800-30 Rev 1 — Guide for Conducting Risk Assessments](https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final) — Full text free download
- [NCSC Cyber Threat Intelligence](https://www.ncsc.gov.uk/section/keep-up-to-date/threat-reports) — Real UK threat landscape data
- [ENISA Threat Landscape 2024](https://www.enisa.europa.eu/topics/cyber-threats/enisa-threat-landscape) — Annual EU threat report
- [FAIR Institute — Introduction to FAIR](https://www.fairinstitute.org/what-is-fair) — Quantitative risk methodology
- [NCSC Risk Management Guidance](https://www.ncsc.gov.uk/collection/risk-management) — Practical UK government guidance
- [CISA Risk Assessment Guidance](https://www.cisa.gov/rrp) — US Government risk resources

### Books

- *How to Measure Anything in Cybersecurity Risk* by Douglas Hubbard & Richard Seiersen — The definitive book on quantitative cyber risk
- *Cybersecurity Risk Management* by Cynthia Irvine — Academic but practical framework
- *The CISA Prep Guide* by ISACA — Covers risk assessment in depth for CISA exam
- *Measuring and Managing Information Risk: A FAIR Approach* by Jack Freund & Jack Jones — The FAIR model bible

### Online Courses (Free / Low Cost)

- [ISACA: Risk and Information Systems Control (CRISC) Overview](https://www.isaca.org/credentialing/crisc) — Free overview content
- [Coursera: Introduction to Cyber Security Specialization — NYU](https://www.coursera.org/specializations/intro-cyber-security) — Covers risk fundamentals
- [SANS Reading Room: Risk Assessment Papers](https://www.sans.org/white-papers/risk-assessment/) — Free white papers
- [YouTube: FAIR Model Explained — FAIR Institute](https://www.youtube.com/@FAIRInstitute) — Free FAIR methodology videos
- [LinkedIn Learning: Cybersecurity Risk Management Fundamentals](https://www.linkedin.com/learning/)

### Tools to Explore

- **RiskLens** (risklens.com) — FAIR-based quantitative risk platform; watch demo videos
- **SimpleRisk** (simplerisk.com) — Open source risk management tool; free to self-host
- **Microsoft Excel / Google Sheets** — Build a risk register and heatmap from scratch (core GRC skill)

### Community and Podcasts

- **FAIR Institute Community** (fairinstitute.org/community) — Quantitative risk professionals
- **Risky Business Podcast** (risky.biz) — Weekly security news with risk context
- **CISO Series Podcast** (cisoseries.com) — Risk conversations with CISOs
- **r/cybersecurity** — Discussion of risk management approaches

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (Teaching Session — 90 min)

**Agenda:**
- 20 min: Lecture — Risk, threat, vulnerability, likelihood, impact definitions with real examples from recent breaches.
- 20 min: Live demo — Build a 5×5 risk matrix together on screen; score 3 sample risks as a class exercise.
- 15 min: Walk through the CloudSafe scenario — identify threats specific to a cloud storage company together.
- 20 min: Student workshop — identify 5 risks for CloudSafe from scratch and score them.
- 15 min: Risk treatment discussion — when to mitigate vs accept vs transfer; cost-benefit analysis examples.

### Session B Focus (Assignment Review — 60 min)

- Review risk register: Are risks specific (named threats, named assets)? Are scores calibrated (not everything High)?
- Review risk matrix: Is colour coding correct? Does it match the register?
- Check risk treatment recommendations: Are they specific controls, not vague suggestions?
- Review executive report: Is risk communicated in business language?
- Discuss: Which risk did the student find most interesting and why?

### Mentor Discussion Questions

1. "Walk me through how you scored the ransomware risk — what data or assumptions did you use?"
2. "If CloudSafe's CISO said they could only fix 3 risks this quarter, which 3 would you recommend and why?"
3. "What's the difference between transferring risk to cyber insurance vs mitigating it with controls?"
4. "How would the risk register change if CloudSafe started handling financial data instead of business documents?"
5. "What information would you need to calculate the inherent risk of a third-party cloud provider failure?"

### Red Flags to Watch For

- All risks scored at the same level (no differentiation between critical and low risks)
- Risk descriptions are generic ("data breach") without linking to specific assets or attack vectors
- No residual risk calculated — only inherent risk provided
- Risk owners listed as "IT Team" rather than named individuals
- Risk treatment is vague: "implement security controls" rather than specific recommendations

---

## Section 8: Interview Preparation

### Common Interview Questions for This Topic

1. "Walk me through how you conduct a risk assessment from start to finish."
2. "What's the difference between inherent risk and residual risk?"
3. "How do you score likelihood and impact in a risk matrix?"
4. "What are the four risk treatment options and when do you use each?"
5. "What is risk appetite and how does it influence risk treatment decisions?"
6. "Tell me about a risk register you've built or worked with."
7. "How do you identify risks — what sources do you use?"
8. "What is the difference between a quantitative and qualitative risk assessment?"
9. "What is the FAIR model and how does it differ from qualitative risk assessment?"
10. "How do you present risk findings to a board that doesn't have a technical background?"
11. "What's a risk you identified that surprised your stakeholders?"
12. "How often should a risk register be reviewed and updated?"

### How to Answer Key Questions

**Q: "Walk me through how you conduct a risk assessment."**

*Answer:* "I start by defining the scope — which systems, processes, or data assets we're assessing — and agreeing the methodology with stakeholders. Then I run risk identification workshops with business owners, IT, and Legal to identify threats relevant to those assets. For each threat I identify the vulnerability it could exploit and score likelihood and impact on a 1–5 scale. I calculate inherent risk as Likelihood × Impact, identify current controls, and recalculate residual risk. Then I prioritise risks against the organisation's risk appetite and recommend treatment — mitigate, accept, transfer, or avoid — with specific control recommendations and cost estimates. Everything goes into a risk register which I review and update monthly."

### Keywords to Use

- Inherent vs residual risk
- Risk appetite and tolerance
- Threat identification
- Vulnerability assessment
- Qualitative vs quantitative
- FAIR methodology
- Risk treatment options (mitigate, accept, transfer, avoid)
- 5×5 risk matrix
- ISO 27005
- NIST SP 800-30
- Risk owner accountability
- Risk register maintenance
