# Week 14 Learning Guide: Incident Response and GRC Oversight

## What You Will Learn This Week

Cybersecurity incidents are inevitable — how an organisation responds determines the difference between a manageable disruption and a catastrophic breach. This week you learn the full incident response lifecycle from a GRC perspective: not just the technical containment, but the governance oversight, GDPR notification obligations, regulatory reporting, board communication, and lessons-learned processes that GRC professionals own. When an incident occurs, the GRC team coordinates across legal, IT, communications, and management — this week you will learn how.

---

## Section 1: Core Concept Explained

### What Is Incident Response from a GRC Perspective?

An Information Security Incident is any event that has or could have an adverse effect on the confidentiality, integrity, or availability of an organisation's information assets. From a GRC perspective, incident response is not just technical remediation — it is a compliance, legal, and governance challenge.

**Why GRC leads on incident response:**
- **GDPR obligations**: A breach involving personal data triggers mandatory ICO notification within 72 hours (Art. 33). GRC/Legal determines if the threshold is met.
- **Regulatory obligations**: FCA, PRA, MHRA, and other regulators have specific incident reporting requirements. Missing a deadline is itself a compliance failure.
- **Board communication**: The board must be informed of material incidents. GRC translates technical details into business risk language.
- **Evidence preservation**: GRC ensures forensic evidence is preserved (for legal proceedings, insurance claims, and regulatory investigations).
- **Lessons learned**: After containment, GRC leads the post-incident review to identify root causes and drive control improvements.
- **ISO 27001 requirements**: ISO 27001 Annex A controls A.5.24–5.28 cover incident management planning, response, evidence collection, and lessons learned.

**NIST CSF 2.0 — RESPOND and RECOVER functions** define the expected capabilities for incident response:
- **RS.MA**: Incident Management — execute and communicate the response
- **RS.AN**: Incident Analysis — investigate root cause
- **RS.CO**: Reporting and Communication — notify stakeholders
- **RS.MI**: Incident Mitigation — contain and eradicate
- **RC.RP**: Recovery Execution — restore operations
- **RC.CO**: Recovery Communication — communicate recovery status

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **Security Incident** | Any event adversely affecting CIA of information assets | Ransomware attack, data breach, DDoS |
| **Incident Response Plan** | Documented procedures for handling incidents | 40-page IR plan covering P1–P4 incidents |
| **IR Playbook** | Step-by-step procedure for a specific incident type | Ransomware Playbook — isolation, investigation, restoration |
| **Incident Severity** | Classification of incident by business impact | P1 (Critical), P2 (High), P3 (Medium), P4 (Low) |
| **GDPR Breach** | Incident involving personal data | Customer records leaked = GDPR breach |
| **Art. 33 Notification** | 72-hour ICO notification for GDPR breaches | Must report if risk to individuals |
| **IOC** | Indicator of Compromise | Malicious IP address, hash of malware file |
| **Containment** | Isolating affected systems to prevent spread | Taking an infected server offline |
| **Eradication** | Removing the threat from the environment | Deleting ransomware, closing the attack vector |
| **Post-Incident Review** | Formal lessons-learned exercise | Conducted 2 weeks after incident resolution |
| **Lessons Learned** | Actions identified from post-incident review | Implement email filtering to prevent phishing |
| **Tabletop Exercise** | Simulated incident discussion (no live systems) | Practice the IR plan without real impact |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The GRC Role in the Incident Response Lifecycle

**Phase 1 — Preparation**
GRC responsibilities:
- Draft and maintain the Incident Response Policy and Plan
- Define incident classification severity levels (P1–P4) with examples and SLAs
- Build IR playbooks for high-probability incident types (ransomware, phishing, data breach, DDoS)
- Establish the IR team: IR Lead, GRC/Legal, IT/Security, Communications, Senior Management
- Define the GDPR breach assessment decision tree (when does an incident become a notifiable GDPR breach?)
- Maintain regulatory reporting obligations register (which regulator requires what, by when)
- Schedule annual IR tabletop exercises

**Phase 2 — Detection and Analysis**
GRC responsibilities:
- Receive escalation from IT/Security team
- Begin GDPR breach assessment: Does this incident involve personal data? If so — classify, assess risk to individuals
- Advise on evidence preservation requirements (for regulatory investigation, insurance, litigation)
- Begin the incident log (timestamped record of all actions and decisions)
- Assess regulatory reporting obligations: FCA? PRA? ICO? What is the deadline?

**Phase 3 — Containment and Eradication**
GRC responsibilities:
- Ensure legal counsel is notified for all P1/P2 incidents
- Advise on notification obligations as investigation reveals scope
- Coordinate board/senior management notification for material incidents
- Track the 72-hour GDPR clock — document time-to-detection and work backward
- Manage external communications (if required): press statement, client notifications

**Phase 4 — Recovery**
GRC responsibilities:
- Confirm ICO notification has been made (if required)
- Confirm individual notifications have been made (if high risk — GDPR Art. 34)
- Advise on insurance claim process
- Ensure all regulatory correspondence is documented

**Phase 5 — Post-Incident Review**
GRC responsibilities:
- Lead the post-incident review (PIR)
- Document root causes, contributing factors, timeline
- Identify control failures
- Produce the lessons-learned report
- Track control improvements to implementation
- Update IR plan and playbooks based on learning
- Report PIR findings to board/Audit Committee

---

## Section 3: Framework Deep Dive

### ISO 27001:2022 — Incident Management Controls

| Control | Requirement |
|---------|-------------|
| A.5.24 | Planning and preparation — IR roles, responsibilities, procedures |
| A.5.25 | Assessment and decision on information security events — triage process |
| A.5.26 | Response to information security incidents — documented response procedures |
| A.5.27 | Learning from incidents — lessons learned; control improvements |
| A.5.28 | Collection of evidence — forensic procedures for evidence preservation |

### GDPR Breach Notification (Articles 33 and 34)

**Article 33 — Notify supervisory authority (ICO):**
- When: Breach that is likely to result in a risk to the rights and freedoms of individuals
- Deadline: **Without undue delay and, where feasible, not later than 72 hours** after becoming aware
- Content: Nature of breach, categories/numbers of individuals, categories/numbers of records, contact details of DPO, consequences, measures taken or proposed

**Article 34 — Notify individuals:**
- When: Breach is likely to result in a **high risk** to the rights and freedoms of individuals
- Deadline: Without undue delay
- Content: Nature of breach, contact details of DPO, consequences, measures taken

**GDPR Breach Decision Tree:**
1. Is there a personal data breach? (Unauthorised access, disclosure, destruction, loss, alteration)
2. Is there a risk to individuals' rights and freedoms? → If yes: Notify ICO (Art. 33)
3. Is there a HIGH risk to individuals' rights and freedoms? → If yes: Also notify individuals (Art. 34)
4. Are there mitigating factors (encryption rendering data unreadable)? → May reduce obligation

**The 72-hour clock starts when the organisation BECOMES AWARE** — not when the breach occurred. A breach discovered 10 days after it happened still triggers the 72-hour clock from discovery.

---

## Section 4: Common Mistakes Beginners Make

1. **Confusing the 72-hour ICO notification with Art. 34 individual notification.** They have different triggers. ICO notification (Art. 33) = risk to individuals. Individual notification (Art. 34) = HIGH risk to individuals.

2. **Not preserving forensic evidence before containment actions.** The instinct is to immediately isolate and clean systems. But wiping systems destroys evidence needed for regulatory investigation, insurance claims, and legal proceedings. Preserve first, then eradicate.

3. **Forgetting the incident log.** The ICO expects a timestamped log showing when the breach was discovered, what decisions were made, and when notifications were made. Without this, regulatory defence is much harder.

4. **Not having an IR plan before the incident.** Creating an IR plan in the middle of a ransomware attack is impossible. The plan must exist and be tested before it's needed.

5. **Under-estimating ransomware recovery time.** Most organisations assume 1–2 days to recover from ransomware. The average recovery time is 21 days. BCPs and RTOs must reflect reality.

6. **Not practising the IR plan.** A plan that has never been tested is a plan that will fail under pressure. Annual tabletop exercises are mandatory good practice.

7. **Failing to communicate with the board during an incident.** A material incident that the board doesn't know about — because the CISO didn't escalate — creates serious governance failures.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Know your regulatory reporting obligations cold** — maintain a "regulatory reporting register" that lists: regulator, reporting trigger, deadline, required content, who notifies.
- **The 72-hour GDPR clock starts at discovery** — document exactly when you became aware. Notify early; you can always update. A late notification is always worse than an early one.
- **Never clean a system without forensic imaging first** — work with IT/forensics to preserve evidence before eradication.
- **Have pre-agreed templates** — pre-drafted ICO notification templates and client notification templates speed up the response dramatically.
- **Run tabletop exercises at least annually** — use a ransomware scenario; test the IR plan; identify gaps before an incident does.
- **Build relationships with external IR firms in advance** — retaining a cyber incident response firm (CrowdStrike, Mandiant) before you need them means faster response times.
- **The post-incident review is as important as the incident response** — the PIR is how organisations improve. Treat it as seriously as the response itself.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [NIST SP 800-61 Rev 2 — Computer Security Incident Handling Guide](https://csrc.nist.gov/publications/detail/sp/800-61/rev-2/final) — Definitive IR reference
- [GDPR Article 33 — ico.org.uk breach notification guidance](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/security/guide-to-security/data-breaches/) — ICO breach notification
- [ISO 27001:2022 A.5.24–5.28](https://www.iso.org/standard/27001) — IS incident management controls
- [NCSC: Incident Management Guidance](https://www.ncsc.gov.uk/guidance/incident-management) — UK IR guidance
- [CISA: Ransomware Guide](https://www.cisa.gov/stopransomware/ransomware-guide) — Comprehensive ransomware IR guidance
- [EDPB: Breach Notification Guidelines](https://edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-092022-personal-data-breach-notification_en)

### Books

- *The Practice of Network Security Monitoring* by Richard Bejtlich — Detection and IR fundamentals
- *Cybersecurity Incident Response* by Eric C. Thompson — GRC-focused IR guide

### Online Courses

- [SANS: SEC504 Hacker Tools, Techniques, Exploits and Incident Handling](https://www.sans.org/cyber-security-courses/hacker-techniques-exploits-incident-handling/) — Advanced IR
- [CISA: Introduction to Incident Response](https://www.cisa.gov/resources-tools/training) — Free government training

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (90 min)

- 20 min: IR lifecycle — walk through all phases with GRC roles highlighted at each stage
- 20 min: GDPR breach decision tree — work through 3 scenarios together: "Does this trigger Art. 33? Art. 34?"
- 20 min: Ransomware tabletop — run a 20-minute mini tabletop: "It's 9am Monday; your monitoring tool alerts to unusual encryption activity on file servers. Walk me through the first 4 hours."
- 15 min: ISO 27001 A.5.24–5.28 requirements explained with practical examples
- 15 min: Introduce BioMed scenario — ransomware hitting a healthcare company; what makes this especially high-stakes?

### Session B Focus (60 min)

- Review IR Policy: Does it include P1–P4 classification? GDPR notification decision tree?
- Check Ransomware Playbook: Is the GDPR clock addressed? Is evidence preservation step before eradication?
- Ask: "BioMed discovers the ransomware at 10am Thursday. They become aware that patient data was exfiltrated at 2pm Thursday. When does the 72-hour clock start and when is the ICO notification deadline?"

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "Walk me through the incident response lifecycle."
2. "What are the GDPR obligations when a data breach occurs?"
3. "What is the 72-hour GDPR notification deadline and when does it start?"
4. "What's the difference between GDPR Article 33 and Article 34?"
5. "What GRC deliverables are required for ISO 27001 incident management?"
6. "How do you classify incident severity?"
7. "What is a tabletop exercise and why is it important?"
8. "What is a post-incident review and what should it produce?"
9. "Tell me about an incident response scenario you've worked through."
10. "What is an IR playbook and what should a ransomware playbook contain?"

### Keywords to Use

- Incident Response lifecycle (Prepare, Detect, Contain, Eradicate, Recover, Review)
- GDPR Article 33 (72-hour ICO notification)
- GDPR Article 34 (individual notification — high risk)
- Incident severity classification (P1–P4)
- IR playbook (ransomware, phishing, data breach)
- Post-incident review / lessons learned
- ISO 27001 A.5.24–5.28
- NIST CSF RESPOND function
- Forensic evidence preservation
- Tabletop exercise
