# Week 14 Assignment: Incident Response and GRC Oversight

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | BioMed Ltd. |
| **Your Role** | GRC Lead / Incident Response Coordinator |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟🌟🌟 |
| **Frameworks** | ISO 27001 (A.5.24–5.28), NIST CSF 2.0 (RESPOND/RECOVER), GDPR Arts. 33–34 |

---

## Scenario Brief — Read This Carefully

**BioMed Ltd.** is a 600-person UK pharmaceutical manufacturer and distributor based in Cambridge. They manufacture diagnostic equipment and supply to NHS trusts, private hospitals, and export to 8 EU countries. They hold ISO 13485 (medical device quality management) and are regulated by the MHRA. Their systems process: employee personal data (600 staff), patient data received from NHS clients for diagnostic processing, and commercially sensitive formula data for their proprietary diagnostic reagents.

**The Incident (Timeline):**

- **Day 1, 07:30**: BioMed's IT Manager notices unusual disk encryption activity on the production file server. He investigates. By 08:30, it is confirmed: ransomware has been deployed across 23 Windows servers and 180 workstations. The file server holding patient diagnostic records, HR data, and manufacturing protocols is encrypted.

- **Day 1, 09:00**: The CEO is notified. BioMed has no formal Incident Response Plan. The IT Manager begins attempts to restore from backup — but discovers the last successful backup was 3 days ago, and the backup server has also been encrypted.

- **Day 1, 11:00**: The CISO (newly appointed, 6 weeks in role) calls you, the GRC Lead, to coordinate the response. You determine: (a) patient diagnostic records for 3,400 individuals are on the encrypted server; (b) HR records for all 600 employees are on the encrypted server; (c) the attacker may have exfiltrated data before encrypting (network logs show large outbound transfer 36 hours earlier).

- **Day 1, 14:00**: Based on the network logs, your forensics team confirms data exfiltration occurred 36 hours ago — approximately 1.5GB of files were transferred to an external IP address. This now confirms a personal data breach (both patient data and employee data potentially exfiltrated).

- **Day 1, 14:30**: The 72-hour GDPR clock for ICO notification starts from the moment you became aware of the breach (14:00). Deadline: **Day 4, 14:00**.

- **Day 4**: Ransomware partially contained; some systems restored from clean backups. GDPR notification decision must be made.

- **Day 14**: Full system restoration. Post-incident review begins.

**Your task:** Build BioMed's incident response programme (what should have been in place) and coordinate the response to this specific incident.

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 14 — especially GDPR Art. 33/34 and the IR lifecycle
- [ ] Read NIST SP 800-61 Rev 2 (incident handling guide) — Sections 1–3
- [ ] Read the ICO's breach notification guidance at ico.org.uk
- [ ] Read NCSC's Ransomware guidance

### Questions to Answer Before Starting
1. BioMed's data exfiltration occurred 36 hours before discovery. When does the 72-hour GDPR clock start?
2. Does this incident require ICO notification under GDPR Art. 33? Why?
3. Does this incident require notification to individuals (Art. 34)? For which groups (patients? employees? both?)?
4. What makes ransomware + data exfiltration worse than ransomware alone from a GDPR perspective?
5. BioMed is an NHS supplier. Does the NHS have its own incident reporting requirements?

---

## Deliverables

### Deliverable 1: Incident Response Policy

**What It Is:** BioMed's formal Incident Response Policy — the governance document that should have existed before this incident.

**Must include:**
- Purpose and scope (all information security incidents)
- Incident definitions and examples (what constitutes an incident vs a security event vs a vulnerability)
- Incident severity classification table:
  - **P1 (Critical)**: Active ransomware, data breach affecting >1,000 individuals, regulatory impact, business operations halted. Response: 24/7 response; CEO notified immediately; external IR firm engaged
  - **P2 (High)**: Significant data breach <1,000 individuals, major system compromise, significant business impact. Response: Same-day response; CISO notified within 1 hour
  - **P3 (Medium)**: Limited incident, contained quickly, minimal data impact. Response: Next business day
  - **P4 (Low)**: Minor events, no data impact, quickly resolved. Response: Normal operational response
- IR Team roles and responsibilities: CISO (IR Lead), GRC Lead (compliance coordinator), IT Security, Legal Counsel, Communications Lead, CEO (for P1/P2)
- Response procedures: escalation paths, communication requirements, GDPR notification decision tree
- Evidence preservation requirements (before containment)
- Regulatory notification obligations (ICO 72 hours; NHS DSP Toolkit; MHRA if devices affected)
- Lessons learned requirements
- Plan testing: annual tabletop exercise minimum
- Policy owner: CISO | Review: annual | ISO refs: A.5.24–5.28

---

### Deliverable 2: Incident Response Plan (Full Lifecycle)

**What It Is:** A complete, actionable IR Plan covering all phases of incident response at BioMed.

**Structure:**

**Section 1 — Preparation**
- IR team contact list (RACI for incident response)
- External contacts: cyber insurance provider, external IR firm, legal counsel, ICO contact details, NHS DSPT team contact
- Evidence preservation requirements and tools
- Communication templates (internal, board, regulator, affected individuals)

**Section 2 — Detection and Triage**
- How incidents are reported (SIEM alert, user report, vendor notification)
- Initial triage checklist: What questions to ask in the first 30 minutes?
- Severity assessment tool: series of yes/no questions leading to P1/P2/P3/P4 classification
- GDPR breach assessment decision tree:
  1. Is personal data involved? → Yes: Continue assessment
  2. Has confidentiality/integrity/availability been compromised? → Yes: This is a personal data breach
  3. Is there a risk to individuals' rights and freedoms? → Yes: Notify ICO (Art. 33)
  4. Is there a HIGH risk to individuals' rights and freedoms? → Yes: Notify individuals (Art. 34)

**Section 3 — Containment**
- Network isolation procedures (when and how to isolate affected systems)
- Forensic evidence preservation: memory capture, disk imaging, log extraction — BEFORE any eradication
- Notification escalation: Who must be told? When? In what format?
- Communication holding statement: approved template for use while investigation is ongoing

**Section 4 — Eradication and Recovery**
- Eradication steps: malware removal, vulnerability patching, credential resets
- Validation: how to verify the threat is removed before reconnecting
- Recovery sequencing: which systems are restored first (based on business criticality)
- Recovery communication: keeping stakeholders informed of progress

**Section 5 — Post-Incident Review**
- PIR trigger: mandatory for all P1/P2 incidents; within 14 days
- PIR participants: CISO, GRC Lead, IT, Legal, affected Business Units
- PIR output: root cause analysis, lessons learned, corrective actions with owners and dates

---

### Deliverable 3: Three IR Playbooks

**Playbook 1 — Ransomware Response**
Hour-by-hour playbook for the first 72 hours:
- 0–1hr: Detection, initial assessment, severity classification
- 1–2hr: Escalation (CISO, CEO), external IR firm engaged, insurance notified
- 2–4hr: **Evidence preservation** (memory dump, log export) BEFORE isolation
- 4–8hr: Isolation of affected systems, network segmentation, backup assessment
- 8–24hr: GDPR assessment — is personal data affected? Start ICO 72-hour clock
- 24–48hr: Forensic investigation, scope confirmation, regulatory notification decisions
- 48–72hr: ICO notification (if required), recovery planning, board update
- 72hr+: Recovery execution, clean backups identified, system restoration

Include a "GDPR clock tracker" table: When breach discovered | 72-hour deadline | Art. 33 notification submitted | Art. 34 notification requirement assessed

**Playbook 2 — Data Breach (Unauthorised Disclosure)**
- Detection scenarios (email to wrong recipient, misconfigured cloud storage, insider exfiltration)
- Initial severity assessment: How many individuals? What data categories? What is the risk?
- GDPR notification decision tree
- Individual notification template
- ICO notification steps (what information to include per Art. 33(3))

**Playbook 3 — Phishing / Business Email Compromise**
- Initial indicators: user reports suspicious email, finance team receives CEO fraud attempt
- Response steps: reset compromised credentials, check mail rules, check forwarding rules
- Scope assessment: Were any credentials compromised? Was any data accessed?
- If credentials compromised: treat as potential data breach; begin GDPR assessment
- Prevention: report to NCSC (suspicious email reporting service), phishing awareness update

---

### Deliverable 4: GDPR Breach Notification Procedure

**What It Is:** BioMed's specific procedure for assessing and notifying the ICO of personal data breaches.

**Must include:**
1. GDPR breach definition and BioMed-specific examples
2. 72-hour clock: how to calculate the deadline; documentation requirements
3. ICO notification form walkthrough: what information is required (Art. 33(3))
4. Individual notification: when required; template; delivery method
5. GDPR breach register template: record all incidents including those not requiring notification
6. Evidence requirements for ICO investigation (what to preserve)
7. Applies to BioMed incident: draft the ICO notification for the BioMed ransomware incident as an exercise, including all Art. 33(3) required fields

---

### Deliverable 5: Post-Incident Review Template + BioMed Lessons Learned Report

**Template must include:**
- Incident overview (what happened, timeline)
- Root cause analysis (technical root cause + governance root cause)
- Detection gap analysis (why wasn't this detected sooner?)
- Response effectiveness review (what worked well; what failed)
- Control failure identification (which controls failed or were absent?)
- Lessons learned (specific, actionable improvements)
- Corrective actions (specific action, owner, deadline, control reference)
- Management sign-off

**Apply template to BioMed incident:**
Write a 2-page Lessons Learned Report based on the BioMed scenario. Root causes to identify:
- No IR Plan (primary governance failure)
- Backup not tested; backup server on same network (technical failure)
- No network segmentation — ransomware spread to 23 servers (technical failure)
- No EDR — attack not detected for 36 hours (detection gap)
- No PAM — ransomware used compromised admin credentials (access control failure)

Corrective actions: IR plan developed, backup hardening, network segmentation, EDR deployment, PAM implementation. Each with owner and 90-day deadline.

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| IR Policy Quality | 20% | Professional; severity classification clear; regulatory refs included |
| IR Plan Completeness | 25% | All phases covered; GRC roles explicit; GDPR decision tree |
| Playbook Quality | 30% | Specific hour-by-hour steps; GDPR clock addressed; forensic preservation step present |
| Lessons Learned | 25% | Root causes identified; specific corrective actions; ISO 27001 refs |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **ISO 27001:2022 A.5.24–5.28** | IS incident management controls |
| **NIST SP 800-61 Rev 2** | Incident handling methodology |
| **NIST CSF 2.0 — RESPOND/RECOVER** | RS.MA, RS.AN, RS.CO, RS.MI, RC.RP |
| **GDPR Articles 33–34** | Breach notification obligations |

---

## Week-Specific Resources

- [NIST SP 800-61 Rev 2 Full Text](https://csrc.nist.gov/publications/detail/sp/800-61/rev-2/final) — Computer Security Incident Handling Guide
- [ICO: Reporting a Breach](https://ico.org.uk/for-organisations/report-a-breach/) — ICO breach notification portal
- [ICO: Guide to Data Breach Notification](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/security/guide-to-security/data-breaches/) — Detailed guidance
- [NCSC: Ransomware Response Guide](https://www.ncsc.gov.uk/guidance/mitigating-malware-and-ransomware-attacks) — UK ransomware guidance
- [CISA: Ransomware Guide](https://www.cisa.gov/stopransomware/ransomware-guide) — Comprehensive response steps
- [SANS: Incident Handler's Handbook](https://www.sans.org/reading-room/whitepapers/incident/) — Free IR reference

---

## Submission

```
Week-14/Deliverables/
├── BioMed-Incident-Response-Policy-v1.0.md
├── BioMed-Incident-Response-Plan-v1.0.md
├── BioMed-Ransomware-Playbook-v1.0.md
├── BioMed-Data-Breach-Playbook-v1.0.md
├── BioMed-Phishing-BEC-Playbook-v1.0.md
├── BioMed-GDPR-Breach-Notification-Procedure-v1.0.md
└── BioMed-Lessons-Learned-Report-v1.0.md
```
