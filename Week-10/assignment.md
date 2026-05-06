# Week 10 Assignment: GDPR and Data Privacy Compliance

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | HealthTrack Ltd. |
| **Your Role** | Data Protection Analyst / GRC Analyst |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟🌟 |
| **Frameworks** | GDPR / UK GDPR, ICO Guidance, ISO 27001 (Art. 32 alignment) |

---

## Scenario Brief — Read This Carefully

**HealthTrack Ltd.** is a UK health-tech startup founded in 2021, with 45 employees based in London. They provide a digital health monitoring application used by 120,000 UK individuals to track chronic conditions (diabetes, hypertension, asthma). The app collects: name, email, date of birth, NHS number, GPS location (for medication reminders), blood glucose readings, blood pressure readings, and medication schedules.

This data constitutes **special category personal data under GDPR Article 9** (health data) — the highest-risk data category, subject to the most stringent protection requirements and the most significant ICO enforcement risk.

HealthTrack recently signed a commercial analytics partnership with **HealthMetrics Inc.**, a US data analytics company, to analyse anonymised patient data to improve their AI recommendation engine. This partnership involves **transferring UK health data to the United States** — a jurisdiction without a UK adequacy decision for this type of transfer. Their DPO, Sarah Nkosi, has flagged this as a potential GDPR violation.

Additionally, HealthTrack received 3 Subject Access Requests (SARs) last month — all from the same solicitor representing a group of users. The solicitor has indicated the group is considering legal action over HealthTrack's data retention practices (users claim their data was retained for years after account deletion).

**Current data protection problems:**
- Record of Processing Activities (RoPA) last updated in 2022; does not include the HealthMetrics partnership
- Data Protection Impact Assessment (DPIA) not conducted for the HealthMetrics analytics partnership
- Data retention schedule exists but is not enforced — deleted accounts retain data in backup systems
- No Standard Contractual Clauses (SCCs) in place with HealthMetrics for international transfer
- Privacy notice does not mention the analytics partnership
- SAR response process: informal; first two SARs missed the 30-day deadline

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 10 — especially the GDPR articles section
- [ ] Read GDPR Articles 9 (special categories), 28, 30, 33, 35, 44–49 at gdpr-info.eu
- [ ] Read the ICO's DPIA guidance at ico.org.uk
- [ ] Read the ICO's guidance on international data transfers post-Brexit

### Questions to Answer Before Starting
1. HealthTrack processes health data. Under GDPR Art. 9, what lawful basis can they use for this processing?
2. The HealthMetrics transfer goes from UK to US. What UK GDPR transfer mechanism is appropriate?
3. A SAR was received yesterday. What is the deadline for responding and what must the response include?
4. What triggers a mandatory DPIA under GDPR Article 35? Does the HealthMetrics analytics partnership trigger one?
5. HealthTrack deleted a user account but their data remains in backups. Is this a GDPR violation?

---

## Deliverables

### Deliverable 1: GDPR Compliance Gap Assessment

**What It Is:** A comprehensive assessment of HealthTrack's GDPR compliance status across all major obligations.

**Step-by-Step Instructions:**

1. Create a spreadsheet with a row for each GDPR obligation. Use these sections:

   **Part 1 — Lawful Basis and Consent (Articles 5–7, 9)**
   - Lawful basis documented for each processing activity?
   - For health data (Art. 9): explicit consent obtained? Or other Art. 9(2) condition?
   - Consent records maintained? Withdrawal mechanism in place?

   **Part 2 — Data Governance (Articles 5, 25)**
   - Data minimisation: Only necessary data collected?
   - Purpose limitation: Data used only for disclosed purposes?
   - Privacy by Design implemented in product development?

   **Part 3 — Record of Processing Activities (Article 30)**
   - RoPA exists and is current? (HealthMetrics partnership must be included)
   - All required fields present: purposes, categories, recipients, retention, transfers, security measures?

   **Part 4 — Individual Rights (Articles 15–22)**
   - SAR response process defined? 30-day deadline met? (Flag: 2 missed deadlines)
   - Right to erasure process? (Flag: deleted accounts retain data in backups)
   - Right to data portability? (Users can export their health data?)

   **Part 5 — Data Breach Response (Articles 33–34)**
   - Breach detection procedure exists?
   - 72-hour ICO notification process documented?
   - Individual notification criteria and template exists?

   **Part 6 — International Transfers (Articles 44–49)**
   - HealthMetrics US transfer: Is adequate mechanism in place? (Flag: No SCCs)
   - Transfer Impact Assessment conducted?

   **Part 7 — Third Party (Article 28)**
   - DPA in place with HealthMetrics? With cloud providers? With app stores (Apple/Google)?
   - Sub-processor list maintained?

2. For each item: Status (Compliant/Partial/Non-Compliant/Not Applicable) | Evidence | Gap | Risk Level (Critical/High/Medium/Low) | Action | Owner | Priority

3. Summary dashboard: Overall compliance %, by section, top 5 critical gaps.

---

### Deliverable 2: Record of Processing Activities (RoPA)

**What It Is:** HealthTrack's formal Record of Processing Activities as required by GDPR Article 30.

**Required fields per processing activity (Article 30(1)):**
- Name and contact details of the controller (HealthTrack Ltd.)
- Purposes of processing
- Categories of data subjects
- Categories of personal data
- Categories of recipients
- Transfers to third countries and the mechanism used
- Envisaged retention periods
- General description of technical and organisational security measures

**Processing activities to document (minimum 6):**
1. User health monitoring data collection and storage (core product — includes health data Art. 9)
2. User account management (names, emails, login data)
3. Analytics partnership — HealthMetrics Inc. (new; must include US transfer details)
4. Marketing communications (if any)
5. Employee HR data
6. Customer support records (support tickets containing health queries)

**For the HealthMetrics processing activity, document:**
- Controller: HealthTrack Ltd.
- Processor: HealthMetrics Inc. (US)
- Purposes: Statistical analysis of anonymised health data to improve AI model
- Categories of data: Anonymised health metrics (note: if re-identification risk exists, this may still be personal data)
- Transfer mechanism: To be determined — document as "SCCs to be implemented"

---

### Deliverable 3: Data Protection Impact Assessment (DPIA) — HealthMetrics Partnership

**What It Is:** A formal DPIA for the HealthMetrics analytics partnership as required by GDPR Article 35.

**Why a DPIA is required here:** GDPR Art. 35(3) mandates a DPIA for: (a) systematic and extensive profiling; (b) large-scale processing of special category data; (c) systematic monitoring. The HealthMetrics partnership involves large-scale processing of health data (120,000 individuals) AND profiling — both triggers apply.

**DPIA structure (following ICO template):**

1. **Description of the processing**: What data, what processing, what technology, who does what
2. **Necessity and proportionality**: Why is this processing necessary? Is a less privacy-intrusive alternative available?
3. **Assess necessity**: What is the lawful basis? For health data — which Art. 9(2) condition applies?
4. **Identify and assess risks**:
   - Risk 1: Re-identification of "anonymised" health data by HealthMetrics
   - Risk 2: US law (FISA/CLOUD Act) potentially requiring HealthMetrics to disclose UK health data to US authorities
   - Risk 3: Data breach at HealthMetrics exposing UK patient health data
   - Risk 4: HealthMetrics using data beyond the agreed purposes
5. **Identify measures to address risks**:
   - For re-identification: Contractual prohibition; technical de-identification standards; right to audit
   - For US law risk: Transfer Impact Assessment; SCCs with supplementary measures; assess if processing can occur in EU/UK
   - For data breach: Breach notification SLA in contract; data minimisation
6. **DPO sign-off**: Sarah Nkosi (DPO) must review and sign off
7. **ICO consultation**: If residual risk remains high, must consult ICO before proceeding (Art. 36)

**Outcome recommendation**: Based on your DPIA, should HealthTrack proceed with the HealthMetrics partnership? Under what conditions? Recommend whether ICO consultation is required.

---

### Deliverable 4: GDPR Compliance Roadmap

**What It Is:** A prioritised 90-day action plan to remediate HealthTrack's critical GDPR gaps.

**Structure:**

**Immediate (0–30 days) — Critical/ICO-visible:**
- Complete DPIA for HealthMetrics partnership (mandatory before continuing data flows)
- Halt HealthMetrics data transfer until SCCs are signed
- Update RoPA to include HealthMetrics
- Fix SAR response process — assign a named owner, set up a 30-day tracking system
- Notify the 3 affected SAR requestors of delay with apology and revised timeline

**Short-term (31–60 days):**
- Negotiate and sign SCCs with HealthMetrics
- Update Privacy Notice to disclose HealthMetrics partnership and US transfer
- Implement data retention enforcement for deleted accounts in backup systems
- Conduct staff training on SAR handling

**Medium-term (61–90 days):**
- Annual RoPA review process established
- DPIA review schedule set
- Annual GDPR compliance review schedule established
- DPO capacity review — part-time DPO sufficient for current scale?

For each action: GDPR article addressed | Risk if not completed | Owner | Success criteria

---

### Deliverable 5: Data Breach Response Procedure

**What It Is:** A documented procedure for detecting, assessing, and reporting data breaches under GDPR Articles 33 and 34.

**Must include:**
- Breach definition and examples (what constitutes a personal data breach at HealthTrack)
- Breach severity assessment: low risk (no notification needed), medium risk (notify ICO), high risk (notify ICO + individuals)
- Step-by-step breach response timeline (Hour 0–72 against the ICO notification deadline)
- ICO notification: What information to provide (Art. 33(3))
- Individual notification: When required, what to include (Art. 34)
- Breach register: Template for recording all incidents (including those not requiring ICO notification)
- Roles: Who identifies breaches? Who assesses? Who notifies the ICO?

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Gap Assessment Quality | 25% | All major GDPR obligations assessed; specific gaps identified |
| RoPA Completeness | 20% | All Art. 30 fields completed; HealthMetrics transfer documented |
| DPIA Quality | 30% | Risks identified; measures proportionate; ICO consultation recommendation justified |
| Roadmap Priority | 25% | Critical items correctly identified and prioritised |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **GDPR / UK GDPR** | Full compliance assessment; RoPA, DPIA, breach notification |
| **ICO Guidance** | DPIA methodology; international transfer guidance |
| **ISO 27001 A.5.34** | Privacy and protection of personal information |

---

## Week-Specific Resources

- [GDPR Full Text — gdpr-info.eu](https://gdpr-info.eu/) — Arts. 9, 28, 30, 33, 35, 44–49
- [ICO: Data Protection Impact Assessments](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/accountability-and-governance/data-protection-impact-assessments-dpias/) — Full DPIA guidance
- [ICO: International Transfers Post-Brexit](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/international-transfers/) — SCCs and adequacy
- [ICO: Record of Processing Activities](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/accountability-and-governance/documentation/record-of-processing-activities/) — RoPA guidance
- [ICO: Subject Access Requests](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/individual-rights/right-of-access/) — SAR guidance
- [EDPB: DPIA Guidelines](https://edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-092022-personal-data-breach-notification_en) — Breach notification guidelines
- [NHS DSPT — Data Security and Protection Toolkit](https://www.dsptoolkit.nhs.uk/) — NHS health data requirements

---

## Submission

```
Week-10/Deliverables/
├── HealthTrack-GDPR-Gap-Assessment-v1.0.xlsx
├── HealthTrack-Record-of-Processing-Activities-v1.0.xlsx
├── HealthTrack-DPIA-HealthMetrics-Partnership-v1.0.md
├── HealthTrack-GDPR-Compliance-Roadmap-v1.0.xlsx
└── HealthTrack-Data-Breach-Response-Procedure-v1.0.md
```
