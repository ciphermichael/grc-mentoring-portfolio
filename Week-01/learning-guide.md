# Week 01 Learning Guide: Introduction to Cybersecurity GRC

## What You Will Learn This Week

This week you are building the conceptual foundation for your entire GRC career. You will understand what GRC is, why it exists, how it sits within a business, and how to survey the major frameworks that govern cybersecurity compliance globally. By the end of the week you will be able to explain GRC fluently to both technical and non-technical audiences — a skill that will serve you in every interview and every client engagement.

---

## Section 1: Core Concept Explained

### What Is GRC?

GRC stands for **Governance, Risk, and Compliance** — three interconnected disciplines that together ensure an organisation manages its information security responsibly, consistently, and in line with legal and regulatory obligations.

**Governance** is the system by which an organisation makes decisions about security. It answers: *Who is responsible for security? What policies exist? How are security decisions made?* Governance creates the structure — the board committees, the CISO role, the security steering group, the policy hierarchy.

**Risk** is the disciplined process of identifying, assessing, and treating threats to the organisation's information assets. Risk management answers: *What could go wrong? How likely is it? How bad would it be? What do we do about it?* Risk is the analytical engine of GRC — it helps organisations prioritise where to spend limited security budget.

**Compliance** is the process of meeting obligations — whether mandatory (laws like GDPR, regulations like PCI-DSS) or voluntary (standards like ISO 27001, SOC 2). Compliance answers: *Are we meeting the rules that apply to us?* It involves gap assessments, evidence collection, audits, and remediation.

The three are inseparable. Governance sets direction and accountability. Risk identifies what threatens the organisation. Compliance ensures the organisation meets its commitments. A GRC Analyst sits at the intersection of all three, producing the documentation, frameworks, assessments, and reports that keep the organisation secure and legally sound.

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **GRC** | Governance, Risk, and Compliance — the integrated discipline managing information security decision-making | Building an ISO 27001 ISMS |
| **Framework** | A structured set of guidelines or controls that helps organisations manage security | ISO 27001, NIST CSF, SOC 2 |
| **Control** | A safeguard or countermeasure implemented to reduce risk | Multi-factor authentication, access reviews |
| **Policy** | A formal document stating management's intent and direction | Information Security Policy |
| **Standard** | A mandatory internal requirement specifying how a policy is implemented | Password length must be minimum 12 characters |
| **Governance** | Structures and processes for decision-making, accountability, and oversight | CISO reporting to Board Risk Committee |
| **Risk** | The potential that a threat will exploit a vulnerability and cause harm | Ransomware encrypting customer data |
| **Compliance** | Demonstrating adherence to a law, regulation, or standard | Passing a PCI-DSS audit |
| **CISO** | Chief Information Security Officer — senior executive responsible for security | "The CISO presents quarterly to the board" |
| **ISMS** | Information Security Management System — the organised approach to managing information security | ISO 27001 requires a documented ISMS |
| **Residual Risk** | Risk that remains after controls have been applied | MFA reduces login risk but residual risk remains |
| **Due Diligence** | Thorough investigation and verification before taking action | Assessing a vendor's security before signing a contract |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Real-World Process: Scoping and Mapping the GRC Landscape

When a GRC Analyst joins a new company or engagement, the first task is always a **landscape survey** — understanding what the organisation does, what data it holds, what regulations apply, and what its current security maturity looks like. Here is how that process works in practice:

1. **Understand the business model** — What does the company do? What data does it process? Who are its customers? A healthcare company handles special category data under GDPR. A payment processor must comply with PCI-DSS. A SaaS company selling to enterprises will face SOC 2 demands.
2. **Identify applicable regulations** — Research which laws and regulations apply based on geography, industry, and data types. UK companies processing EU data need UK GDPR and EU GDPR. Financial services firms need FCA rules. US companies in healthcare need HIPAA.
3. **Identify applicable standards** — Which frameworks are strategically important? ISO 27001 is globally recognised. SOC 2 is expected by US enterprise customers. NIST CSF is used heavily in the US public sector and regulated industries.
4. **Map the current state** — Interview stakeholders. Review existing policies, procedures, and technical controls. Identify what exists and what is missing.
5. **Prioritise gaps** — Not every gap is equal. A missing patch management process is more critical than a missing asset classification procedure. Prioritise by risk.
6. **Build a compliance roadmap** — Sequence remediation activities across a 6–12 month roadmap, assigning owners and deadlines.
7. **Present findings to leadership** — The GRC Analyst translates technical gaps into business risk language for the CISO and board.

### Real Company Example

Consider SecureFlow Ltd., a 180-person UK SaaS company providing workflow automation software to NHS trusts. Their new GRC Analyst, James Chen, joins to help them prepare for an ISO 27001 audit requirement from a key NHS client.

James starts by reviewing their existing documentation — he finds an outdated Acceptable Use Policy from 2019, no formal risk register, no vendor management process, and no security awareness training records. He then maps their regulatory obligations: UK GDPR (they process NHS staff personal data), NHS Data Security and Protection Toolkit (mandatory for NHS suppliers), and ISO 27001 (required contractually).

He creates a one-page landscape report for the CISO showing the three compliance tracks, a heat map of critical gaps, and a recommended 9-month roadmap prioritising the ISO 27001 certification. The board approves a budget for remediation based on James's report — this is the GRC Analyst's first major deliverable.

### What This Looks Like Day-to-Day

- Attending a kick-off meeting with a new client to understand their compliance objectives
- Drafting a GRC landscape report comparing applicable frameworks
- Creating a compliance obligations register for all relevant regulations
- Writing a presentation for the CISO explaining why ISO 27001 matters for enterprise sales
- Setting up a GitHub repository to document and track all GRC deliverables
- Researching a new regulation to assess if it applies to the business

---

## Section 3: Framework Deep Dive

### The Major Frameworks You Must Know

**ISO/IEC 27001:2022** — The international standard for information security management systems. Published by ISO, it specifies requirements for establishing, implementing, maintaining, and continually improving an ISMS. The 2022 version has 93 Annex A controls across 4 domains. Organisations can achieve UKAS-accredited certification by passing external audits (Stage 1 + Stage 2). Used globally across all industries.

**NIST Cybersecurity Framework (CSF) 2.0** — A voluntary framework published by the US National Institute of Standards and Technology. Version 2.0 (2024) introduced the GOVERN function, making 6 total functions: GOVERN, IDENTIFY, PROTECT, DETECT, RESPOND, RECOVER. Each function contains categories and subcategories. Widely used in US regulated industries and increasingly globally.

**SOC 2** — Published by the AICPA (American Institute of Certified Public Accountants). SOC 2 audits assess a service organisation's controls against 5 Trust Services Criteria: Security (mandatory), Availability, Confidentiality, Processing Integrity, Privacy. Type I = point-in-time assessment. Type II = over a 6-12 month observation period. Essential for US enterprise SaaS sales.

**GDPR / UK GDPR** — The General Data Protection Regulation. EU GDPR applies to organisations processing EU residents' data. UK GDPR (post-Brexit) applies to UK-based processing. Key principles: lawfulness, fairness, transparency; purpose limitation; data minimisation; accuracy; storage limitation; integrity and confidentiality; accountability. Fines up to 4% global annual turnover or €20M (whichever higher).

**PCI-DSS v4.0** — Payment Card Industry Data Security Standard. Mandatory for any organisation that stores, processes, or transmits cardholder data. 12 requirements organised around: build and maintain secure networks, protect cardholder data, maintain a vulnerability management program, implement strong access control, monitor and test networks, maintain an information security policy.

---

## Section 4: Common Mistakes Beginners Make

1. **Treating GRC as a checklist exercise.** Beginners often think GRC is just ticking boxes. In reality, GRC is about reducing real business risk. Every control should be linked to a threat. Every gap should be quantified by potential impact.

2. **Confusing governance, risk, and compliance.** Beginners often use these interchangeably. Governance = who decides and is accountable. Risk = what could go wrong. Compliance = are we meeting obligations. They are related but distinct.

3. **Not understanding the business context.** A GDPR gap assessment for a healthcare company is completely different from one for a retailer. Always understand the business model, data types, and customer base before applying any framework.

4. **Recommending the wrong framework.** Not every company needs ISO 27001. A startup with 15 employees selling to US enterprises probably needs SOC 2 first. Know which framework fits the business context.

5. **Writing policies without linking them to controls.** A policy that says "we encrypt data" is useless unless linked to a specific control (e.g., ISO 27001 A.8.24) and verified by evidence (e.g., encryption configuration screenshots).

6. **Underestimating stakeholder communication.** GRC work is only valuable if it influences decisions. Reports that sit unread are worthless. Learn to communicate risk in business terms — cost, revenue impact, reputational risk.

7. **Ignoring the overlap between frameworks.** ISO 27001 access control requirements largely map to SOC 2 CC6. Understanding these overlaps prevents duplicating work across compliance programs.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Always start with the business context** — before opening any framework document, understand what the company does, what data it holds, and what regulations apply to it.
- **Build a compliance obligations register** in your first week on any engagement — it prevents missing regulatory requirements.
- **Learn to speak "business risk" not "technical risk"** — say "a data breach could cost £2M in ICO fines and 3 months of reputational damage" not "we have a SQL injection vulnerability".
- **Use the overlap between frameworks** — ISO 27001 A.9 (Access Control) maps closely to NIST CSF PR.AC and SOC 2 CC6. Doing one assessment well can inform three frameworks.
- **Document everything in real-time** — GRC work is only as good as its documentation. If it's not written down, it didn't happen.
- **GitHub is your credibility** — maintaining a professional, well-documented GitHub portfolio demonstrates organisational skill and technical literacy to hiring managers.
- **Read actual job descriptions weekly** — they tell you what frameworks, tools, and skills employers currently value.
- **Join ISACA and IIA** — they publish free resources, run events, and the community is excellent for career development.
- **Frameworks are living documents** — NIST CSF updated to 2.0 in 2024. ISO 27001 updated in 2022. Stay current.
- **The best GRC professionals are curious** — they read breach reports, regulatory enforcement actions, and industry news to understand real-world threats.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [NIST CSF 2.0 Official Document](https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf) — Read the executive summary and function descriptions
- [ISO 27001:2022 Overview](https://www.iso.org/standard/27001) — Read the publicly available overview
- [GDPR Full Text — GDPR-info.eu](https://gdpr-info.eu/) — Bookmark and reference Articles 5, 6, 32, 33, 34, 83
- [NCSC Cyber Essentials Guidance](https://www.ncsc.gov.uk/cyberessentials/overview) — UK baseline controls framework
- [ICO Guide to UK GDPR](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/) — The UK regulator's own guidance
- [CIS Controls v8 Overview](https://www.cisecurity.org/controls/v8) — Free download of the 18 control groups
- [PCI-DSS v4.0 Quick Reference Guide](https://www.pcisecuritystandards.org/documents/PCI-DSS-v4-0-Quick-Reference-Guide.pdf) — 2-page summary of all 12 requirements
- [AICPA SOC 2 Overview](https://us.aicpa.org/interestareas/frc/assuranceadvisoryservices/sorhome) — Trust Services Criteria explained

### Books

- *The GRC Capability Model* — OCEG — The definitive GRC reference (free PDF from oceg.org)
- *CISA Review Manual* — ISACA — Excellent for understanding IS governance, risk, and audit fundamentals
- *Security Risk Management* by Evan Wheeler — Practical risk management in plain English
- *ISO 27001:2022 — A Pocket Guide* by Alan Calder — Concise, practical ISO 27001 reference

### Online Courses (Free / Low Cost)

- [ISACA's FREE Cybersecurity Fundamentals Certificate](https://www.isaca.org/credentialing/cybersecurity-fundamentals) — Foundational GRC concepts
- [Coursera: IBM Cybersecurity Analyst](https://www.coursera.org/professional-certificates/ibm-cybersecurity-analyst) — Covers GRC topics, audit for free
- [SANS Cyber Aces Online](https://www.cyberaces.org/) — Free foundational security knowledge
- [YouTube: Professor Messer Security+](https://www.youtube.com/professormesser) — Free security fundamentals that underpin GRC
- [LinkedIn Learning: ISO 27001 Foundation](https://www.linkedin.com/learning/) — Search "ISO 27001" — multiple free with trial

### Tools to Explore

- **Vanta** (vanta.com) — Request a demo to see how SOC 2/ISO 27001 compliance automation works
- **Drata** (drata.com) — Another compliance automation platform; see how evidence is collected
- **OneTrust** (onetrust.com) — Privacy and risk management platform; watch their demo videos

### Community and Podcasts

- **r/cybersecurity and r/netsec** — Reddit communities for security news and career advice
- **ISACA Online Community** — isaca.org/community — Forums, study groups, events
- **Risky Business Podcast** (risky.biz) — Industry news and interviews
- **Darknet Diaries** (darknetdiaries.com) — Real breach stories that contextualise why GRC matters

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (Teaching Session — 90 min)

**Agenda:**
- 20 min: Lecture — What is GRC and why does it matter to businesses? Use the Three Pillars model.
- 15 min: Framework walkthrough — Show ISO 27001, NIST CSF, SOC 2, GDPR side-by-side on a slide. Discuss when each applies.
- 15 min: GRC job roles exercise — What does a GRC Analyst do day-to-day? Show a real job description and discuss.
- 20 min: Live demo — Browse the NIST CSF 2.0 document together; show students where to find the functions and categories.
- 10 min: Introduce the TechStart assignment scenario; answer questions.
- 10 min: Demonstrate professional GitHub portfolio setup.

### Session B Focus (Assignment Review — 60 min)

- Review the GRC Landscape Report together — is the writing professional? Is it in business language, not academic?
- Check framework comparison table for accuracy — are the frameworks correctly described?
- Review recommended framework priority — is the justification sound and business-context-aware?
- Discuss GRC team structure recommendation — does it include CISO, DPO, and risk management roles?
- GitHub review — does the repository look professional? Clear README? Correct folder structure?

### Mentor Discussion Questions

1. "If TechStart were processing healthcare data instead of SaaS, which frameworks would change in priority and why?"
2. "What's the difference between governance and compliance — can you give me an example of each from a real company?"
3. "A CISO asks you: 'Do we need ISO 27001 or SOC 2?' How do you answer that question?"
4. "What is the business case for investing in a GRC program? Give me three business reasons."
5. "If a company only has budget for one certification this year, how would you decide which one?"

### Red Flags to Watch For

- Student describes GRC purely in technical terms rather than business/risk terms
- Framework comparison is copy-pasted from Wikipedia rather than synthesised
- GRC team structure shows only IT roles (no Legal, HR, Business representatives)
- Report reads like an essay rather than a professional business document
- GitHub repository is empty or has no structure

---

## Section 8: Interview Preparation

### Common Interview Questions for This Topic

1. "What does GRC stand for and what do each of the three components mean?"
2. "Walk me through the major cybersecurity frameworks and when you'd recommend each."
3. "What's the difference between a policy, a standard, and a procedure?"
4. "Why does a SaaS company need SOC 2? Why does a UK company need ISO 27001?"
5. "How do you stay current with changes in regulations and frameworks?"
6. "What is the role of a GRC Analyst vs a Security Engineer?"
7. "How would you explain GRC to a non-technical CEO?"
8. "What is the relationship between risk management and compliance?"
9. "If a company is subject to both GDPR and PCI-DSS, how do you manage both simultaneously?"
10. "What does 'residual risk' mean and how is it calculated?"
11. "Tell me about a time you had to learn a new regulation or framework quickly."
12. "What GRC tools have you worked with or do you have knowledge of?"

### How to Answer Key Questions

**Q: "What does GRC stand for and why does it matter?"**

*STAR Answer:* "GRC stands for Governance, Risk, and Compliance. Governance is the framework of accountability and decision-making around security — who's responsible, what policies exist, how decisions are made. Risk is the process of identifying threats, assessing their likelihood and impact, and deciding how to treat them. Compliance is ensuring the organisation meets its legal, regulatory, and contractual obligations. The reason GRC matters to business is that without it, organisations make ad-hoc security decisions, miss regulatory requirements, and can't demonstrate their security posture to customers or auditors. A mature GRC programme reduces the cost of compliance, reduces the likelihood of incidents, and enables enterprise sales by demonstrating security assurance."

**Q: "Which framework would you recommend for a UK SaaS startup?"**

*Answer:* "It depends on who their customers are. If they're selling to UK/EU enterprises, ISO 27001 is typically the first priority because it's globally recognised and often required contractually. If they have US enterprise customers or are processing data on behalf of clients, SOC 2 becomes essential. If they process personal data — which almost every SaaS company does — UK GDPR compliance is mandatory, not optional. I'd start by doing a compliance obligations assessment to map all mandatory and contractually required frameworks, then build a prioritised roadmap."

### Keywords to Use in Answers

- Information Security Management System (ISMS)
- Risk appetite and risk tolerance
- Three Lines of Defense
- Regulatory obligations
- Framework maturity assessment
- Compliance obligations register
- Residual risk
- Control effectiveness
- Stakeholder communication
- Governance structure
- CISO accountability
- Continuous monitoring
