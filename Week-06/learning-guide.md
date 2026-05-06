# Week 06 Learning Guide: NIST Cybersecurity Framework 2.0

## What You Will Learn This Week

NIST CSF 2.0 is the most widely used cybersecurity framework in the United States and is growing rapidly in global adoption. Released in February 2024, version 2.0 introduced a critical new function — GOVERN — making it a 6-function framework. This week you will conduct a full maturity assessment against all 6 functions, produce a CSF Profile for CloudFirst Inc., and build an implementation roadmap. NIST CSF knowledge is essential for working with US companies, federal contractors, and any organisation wanting a risk-based security programme language.

---

## Section 1: Core Concept Explained

### What Is NIST CSF 2.0?

The NIST Cybersecurity Framework (CSF) is a voluntary framework published by the US National Institute of Standards and Technology. Version 2.0 (published February 2024) is a significant evolution from version 1.1. While ISO 27001 is a requirements-based standard that organisations get certified against, NIST CSF is a **descriptive framework** — it describes what good security looks like, at what maturity levels, across the full security lifecycle. Organisations use it to assess their current state, define their target state, and identify the gap.

The framework is structured around **6 Core Functions**, 22 Categories, and approximately 106 Subcategories. The 6 functions (using their acronyms) are:

- **GOVERN (GV)** — NEW in v2.0: Establishes and monitors the cybersecurity risk management strategy, policies, roles, responsibilities, and organisational context. This is the "meta-function" that directs all others.
- **IDENTIFY (ID)** — Understand the organisation's cybersecurity risks to systems, assets, data, and capabilities.
- **PROTECT (PR)** — Implement safeguards to ensure delivery of critical services.
- **DETECT (DE)** — Identify the occurrence of a cybersecurity event.
- **RESPOND (RS)** — Take action regarding a detected cybersecurity incident.
- **RECOVER (RC)** — Maintain resilience and restore capabilities impaired by an incident.

**What makes CSF 2.0 different from 1.1:** The addition of GOVERN (GV) is the most significant change. It elevates governance, risk management strategy, supply chain risk, and roles/responsibilities to a first-class function — reflecting the industry recognition that good governance is the foundation of effective cybersecurity. Other changes include expanded supply chain risk guidance and clearer tier definitions.

**CSF Tiers (1–4):** The framework uses 4 maturity tiers:
- **Tier 1 — Partial**: Ad hoc, reactive. No formal risk management practices.
- **Tier 2 — Risk Informed**: Risk management practices are approved but not organisation-wide.
- **Tier 3 — Repeatable**: Formal, documented, consistent practices. Organisation-wide adoption.
- **Tier 4 — Adaptive**: Continuously improving. Uses lessons learned and predictive indicators.

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **CSF Function** | The 6 high-level cybersecurity outcomes | GOVERN, IDENTIFY, PROTECT, DETECT, RESPOND, RECOVER |
| **CSF Category** | Subdivisions within each function | ID.AM (Asset Management), PR.AC (Access Control) |
| **CSF Subcategory** | Specific outcomes within each category | ID.AM-01: Inventories of hardware maintained |
| **CSF Profile** | The desired or current state of the framework | "Current Profile" = Tier 2 across most functions |
| **CSF Tier** | Maturity level of implementation (1–4) | Tier 3 = Repeatable |
| **Target Profile** | Where the organisation wants to be | Target: Tier 3 across all functions in 12 months |
| **Gap Analysis** | Comparison of current vs target profile | 14 subcategories at Tier 1 needing improvement |
| **GOVERN (GV)** | New in CSF 2.0 — governance and strategy function | GV.RM = Risk Management Strategy |
| **Informative Reference** | Mapping of CSF outcomes to other frameworks | CSF ID.AM-01 maps to ISO 27001 A.5.9 |
| **Supply Chain Risk** | Risk from third-party and supplier dependencies | GV.SC = Supply Chain Risk Management |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Real-World NIST CSF Assessment Process

1. **Understand organisational context** — Before scoring anything, understand the business: what sector, what assets, what regulations, what customer expectations. A Tier 1 target is appropriate for a small startup; a Tier 3 or 4 target is appropriate for critical infrastructure or regulated industries.

2. **Define the scope** — Which business units, systems, and processes are in scope? For most SMB engagements, the scope is the entire organisation.

3. **Collect information** — Interview stakeholders from IT, Security, Legal, and Business. Review existing documentation (policies, procedures, architecture diagrams). Request evidence of control implementation.

4. **Score current state using tiers (1–4)** — For each of the 6 functions and their categories/subcategories, assign a current tier based on the evidence collected. This is the Current Profile.

5. **Define the target profile** — Work with leadership to define the desired tier for each function. The target profile is risk-informed — areas with higher risk exposure get higher target tiers.

6. **Calculate the gap** — Compare Current Profile to Target Profile. Identify which categories/subcategories need the most improvement.

7. **Prioritise improvements** — Based on risk priority, resource availability, and quick wins, build a prioritised roadmap.

8. **Build the implementation roadmap** — Assign improvements to time periods (immediate, short-term, medium-term, long-term) with owners, resource estimates, and success criteria.

9. **Document as a CSF Profile** — Produce a formal CSF Profile document showing current state, target state, and gap narrative for each function.

10. **Present to leadership** — The executive-friendly output is typically a spider/radar chart showing current vs target tiers across the 6 functions.

### Real Company Example

Marcus Tan, GRC Lead at CloudFirst Inc. (a 300-person cloud services company), was asked by the new CISO to establish a cybersecurity baseline. CloudFirst had no prior formal assessment. Using NIST CSF 2.0, Marcus spent 3 weeks conducting interviews and reviewing documentation.

His Current Profile showed:
- GOVERN: Tier 1 (no formal risk management strategy, no documented roles)
- IDENTIFY: Tier 2 (some asset inventory, but incomplete; risk assessment ad hoc)
- PROTECT: Tier 2 (MFA implemented for some systems; not all; patch management inconsistent)
- DETECT: Tier 1 (no SIEM; limited monitoring)
- RESPOND: Tier 1 (no incident response plan)
- RECOVER: Tier 1 (backups exist; no tested recovery plan)

Target Profile (12 months): Tier 3 across all functions.

The gap analysis identified 32 subcategories requiring improvement. Marcus prioritised by risk: GOVERN.RM (risk management strategy), DE.CM (monitoring and detection), and RS.MA (incident management) as the top priorities.

The resulting roadmap was approved by the board with a £220,000 investment in SIEM tooling, an IR programme, and a GRC platform.

### What This Looks Like Day-to-Day

- Interviewing IT, security operations, and business teams to collect evidence
- Scoring CSF subcategories against the 4-tier scale
- Producing radar charts comparing current vs target profiles
- Writing CSF Profile documents for CISO or board reporting
- Mapping CSF improvements to ISO 27001 controls (frequently required for dual-framework organisations)
- Tracking implementation progress against the CSF roadmap quarterly

---

## Section 3: Framework Deep Dive

### NIST CSF 2.0 — All 6 Functions and Key Categories

**GOVERN (GV)**
- GV.OC: Organisational Context — Understanding priorities, legal requirements, stakeholder expectations
- GV.RM: Risk Management Strategy — Establishing and communicating risk appetite and tolerance
- GV.RR: Roles, Responsibilities, and Authorities — Defining accountability for cybersecurity
- GV.PO: Policy — Cybersecurity policies established and communicated
- GV.OV: Oversight — Results of risk management reviewed and used to inform improvements
- GV.SC: Cybersecurity Supply Chain Risk Management — Managing third-party and supplier risk

**IDENTIFY (ID)**
- ID.AM: Asset Management — Inventory of hardware, software, data, and services
- ID.RA: Risk Assessment — Identifying and assessing cybersecurity risks
- ID.IM: Improvement — Identifying improvements to existing plans and processes

**PROTECT (PR)**
- PR.AA: Identity Management, Authentication, and Access Control — MFA, least privilege
- PR.AT: Awareness and Training — Security awareness programmes
- PR.DS: Data Security — Data protection at rest and in transit
- PR.PS: Platform Security — Configuration management, patch management
- PR.IR: Technology Infrastructure Resilience — Backup and recovery capabilities

**DETECT (DE)**
- DE.CM: Continuous Monitoring — Network, user, and event monitoring
- DE.AE: Adverse Event Analysis — Analysing detected events for potential incidents

**RESPOND (RS)**
- RS.MA: Incident Management — Executing and communicating response activities
- RS.AN: Incident Analysis — Investigating incidents to understand root cause
- RS.CO: Incident Response Reporting and Communication — Notifying stakeholders
- RS.MI: Incident Mitigation — Containing and eradicating threats

**RECOVER (RC)**
- RC.RP: Incident Recovery Plan Execution — Restoring capabilities
- RC.CO: Incident Recovery Communication — Communicating recovery status

---

## Section 4: Common Mistakes Beginners Make

1. **Assigning the same tier to all subcategories within a function.** Reality: within PROTECT, an organisation might be Tier 3 on access control but Tier 1 on monitoring. Score at subcategory level for accuracy.

2. **Treating NIST CSF as a compliance checklist.** CSF is a risk-based framework. Tier targets should reflect risk — not every function needs to be Tier 4. Tier 3 is often the appropriate target for most commercial organisations.

3. **Ignoring the GOVERN function.** Many practitioners still use v1.1 thinking and undervalue GOVERN. In v2.0, GOVERN is the foundation — if governance is weak, all other functions are less effective.

4. **Not defining a Target Profile before scoring.** Without a target, the gap analysis is meaningless. Always define targets before scoring current state.

5. **Conflating CSF Tiers with ISO 27001 certification stages.** They are different scales. Tier 3 CSF does not equal ISO 27001 certification. They have different criteria.

6. **Not using Informative References.** CSF subcategories map to ISO 27001 controls, NIST SP 800-53 controls, CIS Controls, and other frameworks. Using these mappings prevents duplicate assessment work.

7. **Scoring aspirationally rather than honestly.** The Current Profile must reflect actual, evidenced implementation — not what the organisation intends to do. Inflated scores undermine the value of the assessment.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Use NIST's own CSF 2.0 reference tool at csrc.nist.gov** — it includes all subcategories with informative references to ISO 27001, NIST 800-53, and CIS Controls.
- **Produce a radar/spider chart** — six axes, one per function, showing current (dotted) vs target (solid) tiers. This is the most compelling executive communication tool for CSF.
- **CSF maps beautifully to ISO 27001** — most dual-framework organisations use CSF to communicate internally and ISO 27001 for external certification; learn to translate between them.
- **GOVERN is your entry point for strategy conversations** — use GV.RM (risk management strategy) and GV.RR (roles and responsibilities) to start discussions about governance structure.
- **v2.0's supply chain function (GV.SC) is increasingly important** — vendor risk and supply chain questions appear in nearly every GRC role assessment.
- **Document your evidence sources** for each tier score — auditors may challenge your assessment if scores are not backed by evidence.
- **The NIST CSF website has excellent quick start guides** for different organisation types — use them when tailoring assessments.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [NIST CSF 2.0 Full Framework Document](https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf) — Free PDF; read core and all functions
- [NIST CSF 2.0 Reference Tool](https://csrc.nist.gov/projects/cybersecurity-framework/filters#/csf/filters) — Interactive subcategory browser with framework mappings
- [NIST CSF 2.0 Quick Start Guides](https://www.nist.gov/cyberframework/getting-started) — SMB, enterprise, and sector-specific guides
- [NIST CSF 2.0 vs 1.1 Changes Summary](https://www.nist.gov/cyberframework/csf-20-faqs) — Official FAQ explaining what changed
- [NIST SP 800-53 Rev 5](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) — Controls catalogue that CSF maps to
- [CIS Controls v8 to NIST CSF Mapping](https://www.cisecurity.org/cybersecurity-tools) — Cross-framework mapping

### Books

- *NIST CSF 2.0 Implementation Guide* — Various practitioner guides available on Amazon
- *Cybersecurity Framework — NIST SP 1271* — Official NIST small business guide
- *Managing Cybersecurity Risk* by David Sutton — Covers NIST CSF and risk management

### Online Courses

- [Coursera: Cybersecurity Specialization — University of Maryland](https://www.coursera.org/specializations/cybersecurity) — Covers NIST frameworks
- [ISACA: CSX Cybersecurity Fundamentals](https://www.isaca.org/credentialing/cybersecurity-fundamentals) — NIST CSF covered in detail
- [YouTube: NIST CSF 2.0 Deep Dive — Gerald Auger](https://www.youtube.com/@SimplyCyber) — Free detailed explanations
- [SANS: NIST CSF Implementation Course](https://www.sans.org/cyber-security-courses/nist-csf-implementing-framework/) — Professional-level training

### Tools to Explore

- **NIST CSF Assessment Tool** — Available at nist.gov; Excel-based self-assessment
- **Axio360** (axio.com) — NIST CSF online assessment platform; free tier available
- **Vanta** — Maps controls to NIST CSF alongside ISO 27001 and SOC 2

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (Teaching Session — 90 min)

**Agenda:**
- 25 min: Walk through all 6 CSF 2.0 functions — what each covers, what Tier 1 vs Tier 3 looks like
- 15 min: GOVERN deep dive — why it's new and why it matters; show GV.RM and GV.SC in detail
- 20 min: Live scoring exercise — pick 3 subcategories and score them together for a fictional company; discuss evidence needed for each tier
- 15 min: Radar chart demo — create a basic radar chart together in Excel showing current vs target
- 15 min: Introduce CloudFirst scenario; discuss what Tier 3 means as a target for a cloud services company

### Session B Focus (Assignment Review — 60 min)

- Review tier scores for each function: Are they calibrated (not all Tier 1 or all Tier 3)?
- Check GOVERN function scoring — is it lower than PROTECT (common for companies without formal governance)?
- Review radar chart: Does it clearly show the gap?
- Check roadmap: Are the highest-gap areas prioritised first?
- Ask: "Walk me through your DETECT tier score — what evidence would you need to justify moving from Tier 1 to Tier 3?"

### Mentor Discussion Questions

1. "Why did NIST add the GOVERN function in version 2.0? What problem was it solving?"
2. "CloudFirst scored Tier 1 on DETECT. What does Tier 3 on DETECT require and how long would it take to get there?"
3. "If CloudFirst is also working towards ISO 27001, how would you use the NIST CSF assessment to accelerate the ISO gap assessment?"
4. "A board member asks: 'We're Tier 2 overall — is that good or bad?' How do you answer?"
5. "What's the difference between a CSF Profile and a CSF Tier?"

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "Walk me through the 6 functions of NIST CSF 2.0."
2. "What is new in NIST CSF 2.0 compared to 1.1?"
3. "What are the 4 CSF implementation tiers?"
4. "How do you conduct a NIST CSF maturity assessment?"
5. "What is a CSF Profile?"
6. "How does NIST CSF map to ISO 27001?"
7. "What does the GOVERN function cover?"
8. "Why would a UK company use NIST CSF if they're pursuing ISO 27001?"
9. "What is the difference between NIST CSF and NIST SP 800-53?"
10. "How do you present NIST CSF assessment results to a board?"

### Keywords to Use

- 6 Functions: GOVERN, IDENTIFY, PROTECT, DETECT, RESPOND, RECOVER
- Implementation Tiers 1–4 (Partial, Risk Informed, Repeatable, Adaptive)
- CSF Profile (Current and Target)
- Subcategories and informative references
- Supply chain risk management (GV.SC)
- Risk management strategy (GV.RM)
- Gap analysis and roadmap
- Cross-framework mapping (CSF to ISO 27001 to CIS)
