# Week 04 Learning Guide: Introduction to Compliance Programs

## What You Will Learn This Week

Compliance is the legal and contractual obligation dimension of GRC. This week you shift from theory to regulatory reality — understanding how organisations navigate mandatory requirements like GDPR and PCI-DSS, how to conduct a compliance gap assessment, and how to build the compliance infrastructure (calendar, obligations register, remediation tracker) that keeps organisations on the right side of regulators. These skills are in high demand because regulators are increasingly aggressive and fines are rising.

---

## Section 1: Core Concept Explained

### What Is a Compliance Programme?

A compliance programme is the **organised, documented, and monitored system** by which an organisation ensures it meets all applicable legal, regulatory, and contractual requirements. It answers: *What obligations do we have? Are we meeting them? What do we need to fix?*

The key distinction in compliance is between **mandatory** requirements (laws and regulations — you must comply or face fines, criminal liability, loss of licences) and **voluntary** standards (ISO 27001, SOC 2 — you choose to comply for business reasons like customer trust and enterprise sales).

**Why compliance matters to business:** The ICO fined British Airways £20M for a GDPR breach involving 500,000 customers. Marriott was fined £18.4M. Amazon was fined €746M by Luxembourg under GDPR. These are not abstract risks — regulators have shown they will pursue and penalise organisations that fail to meet compliance obligations. Beyond fines, non-compliance creates reputational damage, customer loss, and in some regulated industries, loss of operating licences.

The GRC Analyst's role in compliance is to: identify all applicable obligations → assess current compliance → identify gaps → prioritise remediation → track evidence → maintain ongoing monitoring → manage regulator relationships.

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **Mandatory Compliance** | Legal or regulatory requirement — must comply | GDPR, PCI-DSS, FCA regulations |
| **Voluntary Standard** | Framework adopted for business reasons | ISO 27001, SOC 2, Cyber Essentials |
| **Gap Assessment** | Analysis of current compliance vs required state | "We meet 65 of 90 GDPR requirements" |
| **Compliance Calendar** | Schedule of compliance deadlines and review dates | GDPR annual DPIA review, PCI-DSS quarterly scan |
| **Obligations Register** | Document listing all applicable requirements | Laws, regulations, contractual clauses |
| **Evidence** | Documentation proving a control or requirement is met | Policy document, screenshot, log file, certificate |
| **Remediation** | Actions taken to close compliance gaps | Implementing a data retention policy |
| **Regulator** | Government body enforcing compliance | ICO (UK GDPR), FCA (financial services), PCI SSC |
| **Audit Trail** | Chronological record of activities and evidence | Access logs showing who accessed what data |
| **Data Controller** | Entity determining the purposes of processing personal data | The company itself in most cases |
| **Data Processor** | Entity processing data on behalf of a controller | Cloud provider, payroll service |
| **Cardholder Data** | Payment card information protected by PCI-DSS | Primary Account Number (PAN), CVV, expiry date |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Real-World Process

1. **Build a compliance obligations register** — The first step is identifying ALL applicable requirements. Sources: legal counsel, industry association guidance, regulatory websites, contract review. For each requirement: regulation name, relevant articles/requirements, applicability to the organisation, current status (compliant/partial/non-compliant), evidence required.

2. **Scope the compliance assessment** — Determine which systems, processes, and data are in scope for each regulation. PCI-DSS scope depends on the Cardholder Data Environment (CDE). GDPR scope depends on what personal data is processed and where.

3. **Conduct gap assessment** — For each requirement, assess current state against what is required. Rate compliance: Compliant (evidence exists and is current), Partial (controls exist but gaps remain), Non-Compliant (no controls), Not Applicable (document why).

4. **Prioritise gaps by risk** — Not all compliance gaps are equal. A missing data breach notification procedure (GDPR Art. 33) is higher risk than a missing privacy notice on an internal system.

5. **Build a remediation plan** — For each gap: specific action required, responsible owner, target date, cost estimate, dependencies.

6. **Build a compliance calendar** — Document all compliance deadlines: regulatory submission dates, annual review cycles, external audit dates, certification renewal dates, penetration test requirements.

7. **Establish evidence management** — Create a system for collecting, organising, and retaining evidence. Use a compliance evidence tracker. Evidence must be retrievable in an audit.

8. **Monitor compliance continuously** — Compliance is not a one-time exercise. New regulations emerge. Existing requirements are updated. Internal changes can create new compliance obligations.

9. **Manage regulator relationships** — Know your regulators: ICO for data protection in the UK, FCA for financial services, CQC for healthcare. Respond to regulator inquiries professionally and promptly.

### Real Company Example

PaySafe Corp processes £2 billion in payment card transactions annually, serving 50,000 retailers across the UK. Their Head of Compliance, David Okafor, is tasked with a PCI-DSS v4.0 gap assessment before their annual Qualified Security Assessor (QSA) audit.

David starts by scoping the Cardholder Data Environment (CDE) — the systems that store, process, or transmit cardholder data. At PaySafe, this includes 3 web servers, 2 databases, a payment gateway integration, and the network segment hosting them.

He then assesses compliance against all 12 PCI-DSS requirements. Key gaps found: Requirement 5 (anti-malware on all in-scope systems — 2 legacy servers have no endpoint protection), Requirement 10 (logging and monitoring — logs not being reviewed daily as required), Requirement 11 (internal vulnerability scans not being run quarterly).

Simultaneously, David identifies GDPR obligations: PaySafe processes transaction records containing personal data (name, card number, purchase history). Key GDPR gaps: no formal Record of Processing Activities (RoPA), no Data Retention Policy, no formal procedure for responding to Subject Access Requests (SARs).

David produces a two-page compliance gap matrix showing 8 PCI-DSS gaps and 5 GDPR gaps, a 90-day remediation plan, and a compliance calendar with all key dates. The QSA audit is in 4 months — the remediation plan gets board approval within a week.

---

## Section 3: Framework Deep Dive

### GDPR / UK GDPR Key Requirements

**6 Principles (Article 5)**: Lawfulness, fairness, transparency | Purpose limitation | Data minimisation | Accuracy | Storage limitation | Integrity and confidentiality (security) | Accountability

**Lawful Bases for Processing (Article 6)**: Consent | Contract | Legal obligation | Vital interests | Public task | Legitimate interests

**Individual Rights**: Right to access (Art. 15) | Right to erasure (Art. 17) | Right to data portability (Art. 20) | Right to restrict processing (Art. 18) | Right to object (Art. 21)

**Key Requirements for GRC**: Record of Processing Activities (Art. 30) | DPIA for high-risk processing (Art. 35) | Data breach notification to ICO within 72 hours (Art. 33) | Security measures appropriate to risk (Art. 32) | Data Protection Officer where required (Art. 37)

**Fines**: Up to 4% of global annual turnover or €20M (higher tier); up to 2% or €10M (lower tier)

### PCI-DSS v4.0 — 12 Requirements

1. Install and maintain network security controls
2. Apply secure configurations to all system components
3. Protect stored account data
4. Protect cardholder data with strong cryptography during transmission over open, public networks
5. Protect all systems and networks from malicious software
6. Develop and maintain secure systems and software
7. Restrict access to system components and cardholder data by business need to know
8. Identify users and authenticate access to system components
9. Restrict physical access to cardholder data
10. Log and monitor all access to system components and cardholder data
11. Test security of systems and networks regularly
12. Support information security with organisational policies and programmes

---

## Section 4: Common Mistakes Beginners Make

1. **Treating a gap assessment as a one-time exercise.** Compliance changes constantly — regulations are updated, the organisation's systems change, new processing activities begin. The gap assessment must be repeated at least annually.

2. **Scoping too broadly or too narrowly for PCI-DSS.** Too broad: including systems that don't touch cardholder data, increasing audit cost and complexity. Too narrow: excluding in-scope systems, which creates material compliance failures.

3. **Confusing mandatory and voluntary compliance.** A company doesn't "choose" whether to comply with GDPR — it's mandatory. The consequences of treating mandatory requirements as optional are severe.

4. **Not capturing evidence at the time.** Evidence must be collected and retained contemporaneously. You cannot reconstruct evidence after the fact for a regulator. Build evidence collection into operational processes.

5. **Building a compliance calendar without owners.** A calendar of dates is useless without someone accountable for each date. Every compliance deadline needs an owner.

6. **Underestimating the GDPR special categories.** Processing health data, biometric data, racial/ethnic origin, or political opinions carries significantly higher GDPR obligations and risk. Many beginners treat all personal data the same.

7. **Not documenting why certain requirements are not applicable.** For PCI-DSS and ISO 27001, auditors expect justification for any requirement marked "Not Applicable". "We don't store cardholder data because we use a tokenisation service" is acceptable if documented.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Map your obligations register to specific regulatory articles** — not just regulation names. "GDPR Art. 30 — Record of Processing Activities" is more actionable than "GDPR compliance".
- **Use a Red/Amber/Green (RAG) status in your compliance matrix** — instantly communicates priority to leadership.
- **PCI-DSS scope reduction is a strategic skill** — the less cardholder data your systems touch, the smaller your compliance burden. Recommend tokenisation and point-to-point encryption where possible.
- **Know the ICO's enforcement actions** — the ICO publishes all enforcement notices. Read them. They show you exactly what gaps lead to fines.
- **GDPR Subject Access Requests (SARs) are a common interview topic** — know the 30-day deadline and the process.
- **Build automated compliance monitoring where possible** — manual compliance tracking does not scale. Tools like Vanta, Drata, and Secureframe automate evidence collection for SOC 2 and ISO 27001.
- **Understand your organisation's regulatory relationship** — some industries have "supervisory" regulators (FCA, PRA) that conduct regular reviews. Others are self-declared. The relationship changes your compliance programme design.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [ICO Guide to UK GDPR](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/) — The definitive UK GDPR compliance guide
- [GDPR Full Text — gdpr-info.eu](https://gdpr-info.eu/) — Searchable full text; bookmark Articles 5, 6, 17, 30, 33, 35
- [ICO Enforcement Decisions](https://ico.org.uk/action-weve-taken/enforcement/) — Real cases showing what gaps lead to fines
- [PCI-DSS v4.0 Standard](https://www.pcisecuritystandards.org/document_library/) — Free download from PCI SSC
- [PCI DSS Quick Reference Guide v4.0](https://www.pcisecuritystandards.org/documents/PCI-DSS-v4-0-Quick-Reference-Guide.pdf) — 2-page summary
- [NCSC: Cyber Essentials — Compliance Guidance](https://www.ncsc.gov.uk/cyberessentials/overview) — UK baseline compliance
- [EDPB Guidelines on Data Breach Notification](https://edpb.europa.eu/our-work-tools/documents/public-consultations/2021/guidelines-012021-examples-regarding-data-breach_en) — Essential for understanding Art. 33/34 obligations

### Books

- *EU GDPR — A Practical Guide* by IT Governance Privacy Team — Concise, practical GDPR reference
- *PCI-DSS: A Practical Guide to Implementing and Maintaining Compliance* by Steve Wright — Detailed PCI guidance
- *Data Protection: A Practical Guide to UK and EU Law* by Peter Carey — Comprehensive UK/EU privacy law reference
- *IT Compliance Controls* by Susan Snedaker — Broad compliance programme management

### Online Courses

- [IAPP Foundation of Privacy Law](https://iapp.org/train/online-training/) — Data privacy fundamentals
- [Coursera: Data Privacy Fundamentals — Northeastern University](https://www.coursera.org/learn/data-privacy-fundamentals) — Free with audit
- [PCI Security Standards Council Training](https://www.pcisecuritystandards.org/training-courses/) — Official PCI training
- [SANS SEC566: Implementing and Auditing CIS Controls](https://www.sans.org/cyber-security-courses/implementing-auditing-security-frameworks-controls/) — Compliance control implementation

### Tools to Explore

- **ICO Data Protection Fee Calculator** — Check if your organisation needs to register with the ICO
- **Secureframe** (secureframe.com) — Compliance automation; request demo to see compliance tracking
- **TrustCloud** (trustcloud.ai) — See how compliance evidence is collected and organised

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (Teaching Session — 90 min)

**Agenda:**
- 15 min: Mandatory vs voluntary compliance — discuss real GDPR enforcement actions. What did organisations do wrong?
- 20 min: GDPR deep dive — walk through Articles 5, 6, 30, 33, 35 with examples. What does each require in practice?
- 20 min: PCI-DSS overview — walk through the 12 requirements. What is "scope" and why does it matter?
- 20 min: Compliance gap assessment exercise — give students 3 GDPR requirements and a fictional scenario; assess compliance together.
- 15 min: Introduce PaySafe Corp scenario; build compliance calendar together for first 90 days.

### Session B Focus (Assignment Review — 60 min)

- Review gap assessment: Is each requirement assessed against specific evidence? Is the RAG status clearly applied?
- Check compliance calendar: Are all key PCI-DSS and GDPR dates included? Do all dates have owners?
- Review obligations register: Are specific GDPR articles and PCI-DSS requirements cited (not just the regulation name)?
- Discuss: "Which gap in PaySafe's compliance programme carries the highest regulatory risk and why?"

### Mentor Discussion Questions

1. "PaySafe processes payment cards. If they use Stripe for payment processing and never touch raw card numbers, do they still need PCI-DSS compliance?"
2. "A customer emails PaySafe saying 'I want all my data deleted.' Walk me through the GDPR process."
3. "PaySafe discovers their database was breached 10 days ago. What are their GDPR obligations and what's the deadline?"
4. "What's the difference between a data controller and a data processor? Is PaySafe one or both?"
5. "How would you prioritise the 8 PCI-DSS gaps and 5 GDPR gaps if you could only fix 5 items in the next 30 days?"

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "What is the difference between mandatory compliance and voluntary standards?"
2. "Walk me through GDPR's key principles."
3. "What is the GDPR breach notification deadline and what does it require?"
4. "What is PCI-DSS and who needs to comply with it?"
5. "What is 'scope' in PCI-DSS and why does it matter?"
6. "How do you build a compliance gap assessment?"
7. "What is a Record of Processing Activities (RoPA)?"
8. "What is a Data Protection Impact Assessment (DPIA) and when is it required?"
9. "How do you handle a Subject Access Request (SAR) under GDPR?"
10. "What is the ICO and what powers does it have?"
11. "How do you manage compliance across multiple regulatory frameworks simultaneously?"

### Keywords to Use

- GDPR Articles 5, 6, 30, 33, 35
- Lawful basis for processing
- Record of Processing Activities (RoPA)
- Data Protection Impact Assessment (DPIA)
- Subject Access Request (SAR) — 30-day deadline
- Breach notification — 72-hour ICO notification
- PCI-DSS Cardholder Data Environment (CDE)
- Scope reduction / tokenisation
- Compliance obligations register
- Evidence management
- Regulatory enforcement
- ICO (Information Commissioner's Office)
