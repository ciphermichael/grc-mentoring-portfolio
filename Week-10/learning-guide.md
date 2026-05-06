# Week 10 Learning Guide: GDPR and Data Privacy Compliance

## What You Will Learn This Week

GDPR is one of the most consequential privacy regulations globally, with fines reaching hundreds of millions of euros. Any GRC professional working in Europe — or for any company serving European customers — must have deep GDPR knowledge. This week you will go beyond the basics and into the real operational elements: conducting a DPIA, building a RoPA, navigating international data transfers, and responding to a data breach. These skills are in high demand and directly translate to job performance.

---

## Section 1: Core Concept Explained

### What Is GDPR?

The General Data Protection Regulation (GDPR) entered into force on 25 May 2018 across the EU. Post-Brexit, the UK implemented the **UK GDPR** (largely mirroring EU GDPR) through the Data Protection Act 2018. Both apply to organisations that:
- Are established in the UK/EU, or
- Process personal data of individuals in the UK/EU (regardless of where the organisation is based)

**Personal data** is any information relating to an identified or identifiable natural person — names, email addresses, location data, IP addresses, health records, employment data, purchase histories.

**Special category data** (Article 9) requires extra protection: health data, biometric data, genetic data, racial or ethnic origin, political opinions, religious beliefs, trade union membership, sexual orientation. Processing special category data requires one of the conditions in Art. 9(2) — most commonly explicit consent or a medical necessity basis.

**The 7 Data Protection Principles (Article 5):**
1. **Lawfulness, fairness and transparency** — processing must have a valid lawful basis and be transparent to data subjects
2. **Purpose limitation** — data collected for one purpose cannot be used for incompatible purposes
3. **Data minimisation** — only collect data that is necessary
4. **Accuracy** — keep data accurate and up to date
5. **Storage limitation** — don't keep data longer than necessary
6. **Integrity and confidentiality** — process data securely (this is where ISO 27001 aligns)
7. **Accountability** — the controller must be able to demonstrate compliance

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **Data Controller** | Decides why and how personal data is processed | The company itself |
| **Data Processor** | Processes data on behalf of the controller | SaaS payroll vendor |
| **Data Subject** | The individual whose data is being processed | The customer or employee |
| **Lawful Basis** | One of 6 legal grounds permitting processing | Consent, contract, legal obligation |
| **RoPA** | Record of Processing Activities (Art. 30) | Mandatory documentation of all processing |
| **DPIA** | Data Protection Impact Assessment (Art. 35) | Required for high-risk processing |
| **SAR** | Subject Access Request (Art. 15) — 30-day deadline | Customer requesting their data |
| **ICO** | Information Commissioner's Office — UK GDPR regulator | Enforces fines, investigates complaints |
| **DPO** | Data Protection Officer — required in some cases | Mandatory for public bodies and some processors |
| **SCC** | Standard Contractual Clauses — international transfer mechanism | Used to transfer data to US companies |
| **Art. 33** | GDPR breach notification to supervisory authority | 72-hour ICO notification |
| **Art. 34** | Notification to individuals if high risk | "We had a breach; your data may be affected" |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Real-World GDPR Compliance Process

1. **Data mapping** — Before you can comply with GDPR, you need to know what personal data you process. Conduct a data mapping exercise: interview each department, identify all data flows (collection, processing, storage, sharing, deletion), and document in a data flow diagram.

2. **Build the Record of Processing Activities (RoPA)** — GDPR Article 30 requires organisations with 250+ employees (or processing high-risk/large-scale data) to maintain a RoPA. For each processing activity: purpose, data categories, data subjects, recipients, retention period, security measures, international transfers.

3. **Identify and document lawful bases** — For each processing activity in the RoPA, identify the lawful basis. For employee data: Contract (employment contract). For marketing emails: Consent. For fraud prevention: Legitimate interests. Legitimate interests requires a balancing test.

4. **Conduct DPIAs for high-risk processing** — GDPR Article 35 requires a DPIA before starting high-risk processing. Triggers include: large-scale processing of special category data, systematic profiling, systematic monitoring of public areas. The DPIA assesses necessity, proportionality, risks, and mitigating measures.

5. **Implement individual rights procedures** — Organisations must have documented procedures for: Subject Access Requests (30-day deadline), Right to Erasure, Right to Restriction, Right to Portability. Without documented procedures, staff don't know what to do when a SAR arrives.

6. **Manage international transfers** — UK GDPR restricts transfers of personal data to countries without a UK adequacy decision. For transfers to the US or most other countries, you need a transfer mechanism: Standard Contractual Clauses (SCCs), Binding Corporate Rules (BCRs), or the UK International Data Transfer Agreement (IDTA).

7. **Build data breach response procedures** — GDPR Article 33 requires notification to the ICO within 72 hours of discovering a breach (if it poses a risk to individuals). Article 34 requires notification to individuals if the breach is high risk to them.

8. **Maintain ongoing compliance** — GDPR compliance is not static. New processing activities need RoPA updates. New vendors need DPAs. New regulations (EDPB guidelines) update requirements. Annual reviews are essential.

### Real Company Example

A UK fintech startup, PayNow Ltd., was referred to the ICO after a customer complained their account data was still visible 2 years after account deletion. The ICO investigation revealed: no data retention policy, no RoPA for customer data, no process for enforcing account deletion in backup systems.

Their newly appointed DPO, Marcus Brown, led a 90-day remediation programme. He started with a full data mapping exercise across all 8 business systems. He built a RoPA with 12 processing activities. He wrote a Data Retention Policy with specific retention periods: 7 years for financial records (legal obligation), 2 years for marketing data, 30 days for deleted accounts (customer data then purged from live systems and removed from backups within 90 days of next backup cycle).

He also implemented a SAR response procedure with a named SAR coordinator, a 30-day tracker, and a template response. The ICO closed the investigation with a reprimand (no fine) after seeing evidence of the remediation programme — demonstrating that a documented, implemented compliance programme can influence regulatory outcomes.

---

## Section 3: Framework Deep Dive

### Critical GDPR Articles for GRC Professionals

**Article 5** — 7 Principles of Data Protection (know all 7 by heart)

**Article 6** — Lawful Bases for Processing:
- (a) Consent — freely given, specific, informed, unambiguous. Must be withdrawable.
- (b) Contract — processing necessary to perform a contract with the data subject
- (c) Legal obligation — processing required by law
- (d) Vital interests — to protect someone's life
- (e) Public task — public authority carrying out a public task
- (f) Legitimate interests — controller's legitimate interests, balanced against data subject rights

**Article 9** — Special Category Data: requires explicit consent OR one of 10 specific conditions (medical necessity, employment law, etc.)

**Article 13/14** — Right to Information: transparency requirements; what must be in a privacy notice

**Article 15** — Right of Access: 30-day SAR response; what must be included in the response

**Article 17** — Right to Erasure ("Right to be Forgotten"): conditions for erasure; exceptions

**Article 25** — Data Protection by Design and Default: privacy built into product design

**Article 28** — Data Processors: DPA requirements (see Week 8)

**Article 30** — Records of Processing Activities: required content; who must maintain

**Article 32** — Security of Processing: "appropriate technical and organisational measures"; risk-based approach to security (this is where ISO 27001 directly supports GDPR)

**Article 33** — Notification of Breach to Supervisory Authority: **72-hour deadline**; required content (nature, categories/numbers of individuals, categories/numbers of records, contact details, consequences, measures taken)

**Article 34** — Communication to Data Subject: when required (high risk to rights and freedoms); what to include

**Article 35** — Data Protection Impact Assessment: when mandatory; required content; DPO consultation

**Articles 44–49** — International Transfers: adequacy decisions, SCCs, binding corporate rules, derogations

**Articles 83–84** — Fines: Upper tier (Art. 83(5)): 4% global annual turnover or €20M. Lower tier (Art. 83(4)): 2% or €10M.

---

## Section 4: Common Mistakes Beginners Make

1. **Treating GDPR as a one-time project.** GDPR compliance is ongoing. The RoPA must be updated every time a new processing activity begins. DPIAs must be reviewed when processing changes.

2. **Not conducting DPIAs before high-risk processing begins.** The DPIA must be conducted *before* the processing starts, not after. Starting high-risk processing without a DPIA is itself a violation.

3. **Confusing the 72-hour ICO notification with the notification to individuals.** Art. 33 = notify ICO within 72 hours (if risk to individuals). Art. 34 = notify individuals without undue delay if *high risk*. These are two separate obligations with different triggers.

4. **Failing to maintain SAR deadline tracking.** The 30-day SAR clock starts from receipt, regardless of whether the organisation acknowledges it promptly. Without a tracking system, deadlines are missed.

5. **Over-relying on consent.** Consent is the weakest lawful basis — it can be withdrawn at any time, voiding future processing. Where another lawful basis (contract, legitimate interests) applies, it's often more appropriate.

6. **Not understanding the UK-specific requirements.** Post-Brexit, UK GDPR has diverged from EU GDPR in some areas (international transfer mechanisms, the UK IDTA replacing EU SCCs). Don't assume EU and UK requirements are identical.

7. **Using GDPR as a compliance exercise rather than a culture change.** True data protection requires privacy by design — embedding privacy considerations into product development, not just adding a cookie banner.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Know your lawful bases by heart** — the 6 bases under Art. 6 and the conditions under Art. 9(2) are essential knowledge for any GRC professional.
- **The ICO publishes all enforcement actions** — read them. They show you exactly what triggers investigations and fines.
- **Build a SAR response procedure before you need it** — the worst time to design a process is when you have an active 30-day deadline.
- **The RoPA is your GDPR baseline document** — keep it current; it's the first thing the ICO will request in an investigation.
- **International transfers are a high-risk area** — Standard Contractual Clauses (SCCs) require a Transfer Impact Assessment (TIA) for high-risk destinations.
- **DPO independence is critical** — the DPO (where required) must be able to operate independently. A DPO who is also the Head of Marketing has a conflict of interest.
- **Article 32 bridges GDPR and ISO 27001** — use ISO 27001 implementation as evidence of GDPR Art. 32 compliance ("appropriate technical and organisational measures").

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [GDPR Full Text — gdpr-info.eu](https://gdpr-info.eu/) — Searchable; focus on Arts. 5, 6, 9, 30, 33, 35
- [ICO: UK GDPR Guidance](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/) — UK regulator's complete guidance
- [ICO: DPIA Guidance](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/accountability-and-governance/data-protection-impact-assessments-dpias/) — Step-by-step DPIA process
- [ICO: Enforcement Decisions](https://ico.org.uk/action-weve-taken/enforcement/) — Real cases with fine amounts
- [EDPB: Breach Notification Guidelines](https://edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-092022-personal-data-breach-notification_en) — Art. 33/34 detail
- [ICO: International Transfers](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/international-transfers/) — UK IDTA and SCCs
- [ICO: Subject Access Requests](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/individual-rights/right-of-access/) — SAR guidance

### Books

- *EU GDPR: A Practical Guide* by IT Governance Privacy Team — Concise, practical GDPR reference
- *Understanding GDPR* by Rupert Lees — Accessible explanation for practitioners
- *Privacy by Design* by Ann Cavoukian — Foundational text for privacy-by-design thinking

### Online Courses

- [IAPP: Foundation of Privacy Law](https://iapp.org/train/online-training/) — Industry-recognised privacy training
- [ICO: E-Learning](https://ico.org.uk/for-organisations/advice-for-small-organisations/e-learning/) — Free ICO e-learning modules
- [Coursera: Data Privacy Fundamentals — Northeastern](https://www.coursera.org/learn/data-privacy-fundamentals) — Free with audit

### Tools to Explore

- **OneTrust** (onetrust.com) — GDPR compliance management platform; watch demo
- **TrustArc** (trustarc.com) — Privacy management platform
- **ICO Data Protection Fee Calculator** — Check registration obligations

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (90 min)

- 20 min: GDPR principles — walk through all 7 Art. 5 principles with HealthTrack examples
- 15 min: Lawful bases — quiz the student: "HealthTrack collects blood glucose readings. What's the lawful basis under Art. 6? Art. 9?"
- 20 min: DPIA walkthrough — step through a DPIA for the HealthMetrics partnership together
- 20 min: Breach notification drill — simulate: "HealthTrack discovers a breach today at 9am. Walk me through the next 72 hours."
- 15 min: International transfers — explain SCCs and Transfer Impact Assessment for the US transfer

### Session B Focus (60 min)

- Review RoPA: Are all 6 Art. 30 fields present? Does the HealthMetrics entry correctly document the US transfer?
- Review DPIA: Is the risk to re-identification properly addressed? Is ICO consultation recommendation justified?
- Check gap assessment: Is the missed SAR deadline flagged as Critical (it is — ICO can open investigations on this alone)?

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "Walk me through the 7 GDPR data protection principles."
2. "What are the 6 lawful bases for processing under GDPR Article 6?"
3. "What is a DPIA and when is one required?"
4. "What does GDPR Article 33 require and what is the deadline?"
5. "What must a Record of Processing Activities contain?"
6. "What is the difference between a data controller and a data processor?"
7. "How do you handle a Subject Access Request?"
8. "What are special category data and what makes them different?"
9. "What transfer mechanisms are available for sending data from the UK to the US?"
10. "What are the maximum GDPR fines?"
11. "What is the ICO and what are its enforcement powers?"
12. "How does ISO 27001 support GDPR Article 32 compliance?"

### Keywords to Use

- 7 Data Protection Principles (Art. 5)
- 6 Lawful Bases (Art. 6) — consent, contract, legal obligation, vital interests, public task, legitimate interests
- Special category data (Art. 9)
- Record of Processing Activities (RoPA) — Art. 30
- Data Protection Impact Assessment (DPIA) — Art. 35
- 72-hour breach notification — Art. 33
- Subject Access Request (SAR) — 30-day deadline — Art. 15
- Standard Contractual Clauses (SCCs)
- ICO — Information Commissioner's Office
- Data Controller vs Data Processor
- Privacy by Design — Art. 25
- Transfer Impact Assessment
