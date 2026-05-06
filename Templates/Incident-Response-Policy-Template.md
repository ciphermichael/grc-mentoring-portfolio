# Incident Response Policy Template

| Field | Value |
|-------|-------|
| **Document ID** | POL-IR-001 |
| **Version** | 1.0 |
| **Status** | Approved |
| **Owner** | CISO |
| **Approved By** | CEO / Security Steering Committee |
| **Effective Date** | DD-MMM-YYYY |
| **Review Date** | DD-MMM-YYYY (Annual) |
| **Classification** | Internal |
| **ISO 27001 Ref** | A.5.24, A.5.25, A.5.26, A.5.27, A.5.28 |
| **NIST CSF Ref** | RS.MA, RS.AN, RS.CO, RS.MI, RC.RP |
| **GDPR Ref** | Art. 33 (ICO notification), Art. 34 (individual notification) |

---

## 1. Purpose

This Incident Response Policy establishes [Company Name]'s framework for identifying, managing, containing, and recovering from information security incidents. It ensures that all incidents are handled promptly, consistently, and in compliance with applicable regulatory obligations including GDPR Article 33 (72-hour ICO breach notification) and PCI-DSS Requirement 12.10.

---

## 2. Scope

This policy applies to:
- All information security incidents affecting [Company Name]'s systems, data, or operations
- All employees, contractors, and third parties involved in incident response
- All systems, applications, and data under [Company Name]'s control, including cloud-hosted environments

---

## 3. Definitions

| Term | Definition |
|------|------------|
| **Security Event** | Any observable occurrence in a system or network that may indicate a security concern (e.g., failed login attempt, IDS alert) |
| **Security Incident** | One or more related security events that threaten information confidentiality, integrity, or availability — or create risk of harm |
| **Personal Data Breach** | A breach of security leading to the accidental or unlawful destruction, loss, alteration, unauthorised disclosure of, or access to, personal data (GDPR Art. 4(12)) |
| **P1 — Critical** | Active threat causing significant business disruption, data breach, or regulatory breach |
| **P2 — High** | Confirmed incident with significant security impact; immediate response required |
| **P3 — Medium** | Contained incident with limited impact; same-business-day response |
| **P4 — Low** | Minor incident; no data impact; routine response |

---

## 4. Incident Classification

### Severity Levels and Response Times

| Severity | Description | Examples | Initial Response | Escalation |
|---------|-------------|---------|-----------------|------------|
| **P1 — Critical** | Major incident: active system compromise, confirmed data breach, ransomware deployment, critical system unavailability | Ransomware encrypting systems; confirmed customer data exfiltration; payment processing halted | Within 15 minutes; 24/7 response | CISO immediately; CEO within 30 minutes; Board Chair for data breach |
| **P2 — High** | Significant incident: potential data breach, malware detected, critical vulnerability exploitation | Malware detected on endpoint; suspected insider data theft; DDoS causing degraded service | Within 1 hour (business hours); 4 hours (out-of-hours) | CISO within 1 hour; Head of Legal for potential GDPR breach |
| **P3 — Medium** | Moderate incident: suspicious activity, policy violation, contained security event | Phishing email identified (no click); policy violation (USB usage); suspicious login alert | Within 4 business hours | CISO if escalates to P2 |
| **P4 — Low** | Minor incident: no security impact; administrative | Password reset request; spam; low-risk user error | Within 2 business days | Escalate if evidence of broader compromise |

---

## 5. Incident Response Team

| Role | Responsibility | Primary | Backup |
|------|---------------|---------|--------|
| **Incident Response Lead** | Coordinates overall response; makes containment decisions; manages communications | CISO | GRC Lead |
| **Technical Lead** | Technical containment, investigation, and eradication | Head of IT | Senior IT Engineer |
| **Legal and Compliance** | Regulatory notification decisions; legal privilege; evidence preservation | Head of Legal | External Legal Counsel |
| **Communications Lead** | External communications; customer and press notifications | Head of Communications / CEO | CISO |
| **DPO** | GDPR breach assessment; ICO notification decision and execution | DPO | Head of Legal |
| **Forensic Investigator** | Evidence preservation and forensic analysis | External IR Firm (retainer) | Head of IT |

**24/7 IR Escalation Contact:**
- CISO: [Phone] | [Mobile]
- Backup (GRC Lead): [Phone] | [Mobile]
- External IR Firm (retained): [Company] | [Phone]

---

## 6. Incident Response Lifecycle

### Phase 1 — Preparation

The IR Lead ensures the following are maintained and tested:

- [ ] This IR Policy reviewed and approved annually
- [ ] IR Playbooks available for: Ransomware | Data Breach | Phishing/BEC | DDoS | Insider Threat
- [ ] IR Team trained on this policy and their responsibilities (annual)
- [ ] Tabletop exercise conducted (at minimum annual; P1 scenario)
- [ ] External IR firm retainer agreement in place
- [ ] Cyber liability insurance policy reviewed and current
- [ ] Regulatory notification contacts documented: ICO [contact] | FCA [contact] | PCI DSS [PFI contact]
- [ ] Pre-approved communication templates drafted: ICO notification | Customer notification | Press statement holding notice

### Phase 2 — Detection and Identification

**Incident sources:** SIEM alerts | User reports | Third-party notification | Regulatory notification | Threat intelligence

**Initial triage — must be completed within 15 minutes of notification:**
1. Confirm whether this is a security event or confirmed incident
2. If incident: classify severity (P1/P2/P3/P4) using definitions above
3. Notify IR Lead immediately for P1/P2 incidents
4. Begin incident log (timestamp all actions from this point)
5. If personal data may be involved: notify DPO immediately — GDPR 72-hour clock may start from this point

**GDPR Breach Assessment — Initial Decision:**

```
Is personal data involved? → No → Standard IR process
                         ↓ Yes
Is the personal data compromised (access / disclosure / destruction / loss / alteration)?
                         → No → Monitor; reassess if situation changes
                         ↓ Yes → THIS IS A PERSONAL DATA BREACH
Is there risk to individuals' rights and freedoms?
                         → No → No ICO notification required; document in breach register
                         ↓ Yes → NOTIFY ICO WITHIN 72 HOURS (Art. 33)
Is there HIGH risk to individuals' rights and freedoms?
                         → No → ICO notification sufficient
                         ↓ Yes → NOTIFY INDIVIDUALS WITHOUT UNDUE DELAY (Art. 34)
```

**72-hour ICO clock:** Starts at the moment of becoming aware of the breach — not when it occurred. Document the exact time of awareness.

### Phase 3 — Containment

**Critical rule:** Before any containment action, **preserve forensic evidence** — memory dump, disk image, network logs, system logs. Failure to preserve evidence before containment can destroy the ability to prosecute or recover.

**Forensic preservation checklist (P1/P2):**
- [ ] Memory capture of affected systems (before reboot)
- [ ] Log export: SIEM, firewall, endpoint logs (last 72 hours minimum)
- [ ] Network traffic capture if active exfiltration suspected
- [ ] Email logs if phishing/BEC involved
- [ ] Preserve all evidence in tamper-evident, read-only format

**Containment actions (after evidence preservation):**
- Network isolation: Segment affected systems from rest of network
- Account suspension: Disable compromised accounts immediately
- Block malicious indicators: Update firewall rules, EDR blocks for identified IOCs
- Escalate external parties: Notify cloud provider (AWS/Azure) if cloud systems affected; notify payment processor if cardholder data potentially exposed

### Phase 4 — Eradication

**Eradication requirements:**
- Identify the root cause of the incident
- Remove malware, malicious access, or misconfiguration
- Patch the vulnerability that enabled the breach
- Reset all potentially compromised credentials
- Validate that the threat has been fully removed before proceeding to recovery

**Do not proceed to Recovery until the Technical Lead confirms the threat is fully eradicated.**

### Phase 5 — Recovery

- Restore systems from clean backups (verify backup integrity before use)
- Restore service in priority order per the Business Impact Analysis (RTO sequence)
- Monitor restored systems closely for 72 hours for re-infection indicators
- Communicate recovery status to stakeholders at defined intervals

### Phase 6 — Post-Incident Review

A Post-Incident Review (PIR) **must** be conducted for all P1 and P2 incidents:
- **Timing:** Within 14 days of incident resolution
- **Participants:** CISO, IR Lead, Technical Lead, DPO (if data breach), Head of Legal
- **Output:** Written PIR report including:
  - Incident timeline
  - Root cause analysis
  - What worked well in the response
  - What failed or could be improved
  - Control gaps identified
  - Corrective actions with owners and dates
  - Update to IR playbooks if applicable

---

## 7. GDPR Breach Notification Procedures

### ICO Notification (Article 33)

**Deadline:** Not later than 72 hours after becoming aware of the breach.

**ICO notification must include (Art. 33(3)):**
- Nature of the breach (what happened)
- Categories and approximate number of individuals affected
- Categories and approximate number of personal data records affected
- Name and contact details of the DPO
- Description of likely consequences
- Description of measures taken or proposed

**How to notify:** ICO online self-reporting tool at ico.org.uk/report-a-breach/

**If 72-hour deadline cannot be met:** Notify within 72 hours with reason for delay; provide remaining information as soon as possible.

### Individual Notification (Article 34)

**When required:** If breach is likely to result in high risk to individuals' rights and freedoms.

**High-risk indicators:** Health data | financial data | location data | data enabling identity theft | data affecting vulnerable individuals

**Individual notification must include:**
- Clear description of the breach in plain language
- DPO contact details
- Likely consequences
- Measures taken to address the breach

**Exceptions to individual notification:** If data is encrypted and key is not compromised; if subsequent measures eliminate the high risk.

---

## 8. Evidence Collection and Preservation

All evidence collected during incident response must be:
- **Documented:** Chain of custody record for each evidence item
- **Preserved:** Read-only copies; hash values recorded (SHA-256)
- **Retained:** For minimum 3 years or until legal proceedings concluded (whichever is longer)
- **Secured:** Evidence stored in access-restricted, tamper-evident storage

**Evidence types to collect:**
- System logs (application, security, event logs)
- Network traffic captures
- Memory dumps (RAM)
- Disk images of affected systems
- Email headers and message bodies (if phishing/BEC)
- Access logs (authentication, database, cloud platform)
- Physical evidence (if physical breach involved)

---

## 9. Communication Protocols

### Internal Communications

| Audience | When | Who Notifies | Method |
|---------|------|-------------|--------|
| CISO | Immediately (P1/P2) | First responder | Phone |
| CEO | Within 30 min (P1); 2hr (P2) | CISO | Phone + email |
| Head of Legal | When personal data potentially affected | CISO | Phone |
| CFO | When financial impact possible (P1/P2) | CISO | Phone + email |
| Board Chair | For P1 involving data breach or regulatory breach | CEO | Phone |
| All staff | When operational impact affects them | Communications Lead | Email |

### External Communications

| Audience | When | Who | Approval Required |
|---------|------|-----|-----------------|
| ICO | Within 72 hours (if GDPR breach) | DPO | Head of Legal |
| FCA | Per FCA operational resilience requirements | CISO + Head of Legal | CEO |
| Individuals affected | If high risk (GDPR Art. 34) | DPO / Communications | CEO + Head of Legal |
| Customers (non-GDPR) | When service affected | Communications Lead | CEO |
| Press | Only when media contact made | Communications Lead | CEO |
| PCI DSS (PFI) | If cardholder data potentially compromised | Head of Legal | CEO |

**Rule:** No external communications are made without approval from the CEO (or designated substitute) except where regulatory obligation creates a deadline (ICO 72 hours).

---

## 10. Incident Register

All incidents must be recorded in the Incident Register, regardless of severity. The register includes:

| Field | Description |
|-------|-------------|
| Incident ID | Unique identifier (INC-2025-001) |
| Date/Time Detected | When the incident was first identified |
| Date/Time Aware | When [Company Name] formally became aware |
| Severity | P1/P2/P3/P4 |
| Incident Type | Ransomware / Data Breach / Phishing / DDoS / Insider / Other |
| Summary | 2–3 sentence description |
| Systems Affected | List of affected systems |
| Personal Data Affected | Yes/No; if yes: categories and numbers |
| GDPR Notifiable? | Yes/No; if yes: ICO notification date |
| ICO Reference | ICO case reference number if applicable |
| Resolution Date | When incident was resolved |
| PIR Completed | Yes/No; link to PIR report |
| Lessons Learned | Key improvements identified |

---

## 11. Enforcement

Failure to comply with this policy may result in:
- Disciplinary action up to and including dismissal (for employees)
- Contract termination (for contractors and third parties)
- Regulatory reporting of the non-compliance (where legally required)

---

## 12. Review History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | YYYY-MM-DD | [Name] | Initial policy |

---

*Incident Response Policy | v1.0 | ISO 27001:2022 A.5.24–5.28 | NIST SP 800-61 | GDPR Arts. 33–34*
