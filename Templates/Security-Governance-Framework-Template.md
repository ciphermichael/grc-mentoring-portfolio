# Security Governance Framework Template

| Field | Value |
|-------|-------|
| **Document ID** | SGF-001 |
| **Organisation** | [Company Name] |
| **Version** | 1.0 |
| **Owner** | CISO |
| **Approved By** | Board Risk and Audit Committee |
| **Effective Date** | DD-MMM-YYYY |
| **Next Review Date** | DD-MMM-YYYY (Annual) |
| **Classification** | Internal |
| **Framework Refs** | ISO 27001:2022 Clause 5 | COBIT 2019 | IIA Three Lines Model 2020 |

---

## 1. Purpose and Scope

### 1.1 Purpose

This Security Governance Framework defines the structure, accountability, roles, processes, and reporting mechanisms through which [Company Name] manages its information security responsibilities. It establishes clear lines of accountability for cybersecurity decisions, sets the minimum expectations for governance maturity, and provides the foundation for all security policies, standards, and procedures.

### 1.2 Scope

This framework applies to:
- All employees, contractors, and third-party personnel accessing [Company Name] systems or data
- All information assets owned or managed by [Company Name]
- All locations, including [Company Name] offices, remote working, and cloud-hosted environments
- All information systems and data processing activities

### 1.3 Relationship to Other Documents

This framework is the governance tier document that directs:
- The Information Security Policy (POL-001) — management's intent and commitment
- The Risk Management Framework — how risks are identified and managed
- The Compliance Management Framework — how regulatory obligations are met
- All supporting security standards, procedures, and guidelines

---

## 2. Governance Principles

The following 8 principles guide all information security governance decisions at [Company Name]:

1. **Security as a Business Enabler** — Security protects business value; it is not merely a technical function. Every governance decision considers both risk reduction and business objectives.

2. **Board Accountability** — The Board is ultimately accountable for [Company Name]'s cybersecurity risk posture. The CISO reports regularly to the Board to provide the visibility required for informed oversight.

3. **Risk-Based Decision Making** — All security investment and control decisions are based on documented risk assessments. Resources are allocated to highest-risk areas first.

4. **Proportionality** — Security controls are proportionate to the sensitivity of the information, the nature of the risk, and the size and nature of the organisation.

5. **Clear Accountability** — Every security function, risk, policy, and asset has a named accountable owner. Accountability cannot be shared — it must be assigned to one individual.

6. **Compliance as a Minimum Standard** — Regulatory and contractual obligations define the minimum security floor. [Company Name]'s security programme strives to exceed minimum standards.

7. **Continual Improvement** — The security programme is continually reviewed and improved based on audit findings, incident learnings, threat intelligence, and regulatory changes.

8. **Transparency and Trust** — The organisation communicates openly with customers, regulators, and staff about its security programme, within the bounds of confidentiality.

---

## 3. Three Lines of Defense Model

[Company Name] adopts the IIA Three Lines Model (2020) to structure accountability for risk and security:

### First Line — Business Operations and IT (Risk Owners)

**Responsible for:** Owning and operating security controls within their area of business.

**Who is in the First Line:**
- Technology Engineering and Development teams
- IT Operations and Infrastructure
- Product and Data teams
- Finance, HR, Legal, and Sales functions

**First Line responsibilities:**
- Implementing and adhering to security policies and controls
- Identifying security risks within their business area
- Reporting security incidents and events
- Completing mandatory security awareness training
- Maintaining accurate records of their assets and data processing

### Second Line — GRC, Risk Management, and Compliance (Risk Oversight)

**Responsible for:** Setting the framework, monitoring risk, advising the business, and providing oversight of First Line activities.

**Who is in the Second Line:**
- CISO and GRC Team
- Risk Manager / Head of Risk
- Data Protection Officer (DPO)
- Compliance Manager / Legal Counsel

**Second Line responsibilities:**
- Developing and maintaining the Security Governance Framework, policies, and standards
- Conducting risk assessments and maintaining the risk register
- Monitoring compliance with security policies and regulatory requirements
- Advising the First Line on security controls and risk management
- Reporting to the Board on security risk posture
- Overseeing vendor risk management

### Third Line — Internal Audit (Independent Assurance)

**Responsible for:** Providing independent assurance to the Board that the First and Second Lines are operating effectively.

**Who is in the Third Line:**
- Head of Internal Audit (or co-sourced audit partner)
- External Auditors (ISO 27001 certification body, SOC 2 CPA firm)
- Regulatory Reviewers (FCA, ICO inspectors)

**Third Line responsibilities:**
- Conducting independent audits against ISO 27001, regulatory requirements, and internal policies
- Reporting audit findings to the Board Audit Committee (not to the CISO)
- Tracking corrective action implementation
- Providing assurance on control effectiveness

> **Critical governance principle:** The Third Line (Internal Audit) must be independent from the Second Line (GRC/CISO). The Head of Internal Audit reports to the Board, not to the CISO. This independence is required by ISO 27001 Clause 9.2 and the IIA IPPF.

---

## 4. Security Committee Structure

### 4.1 Board Risk and Audit Committee

| Element | Detail |
|---------|--------|
| **Purpose** | Provides board-level oversight of cybersecurity risk, compliance, and the internal audit programme |
| **Chair** | Independent Non-Executive Director (NED) |
| **Membership** | 3 NEDs (including Chair) | CEO (attendee) | CFO (attendee) | CISO (presenter) | Head of Internal Audit (presenter) |
| **Quorum** | 3 members (minimum 2 NEDs) |
| **Frequency** | Quarterly |
| **Key Agenda Items** | CISO quarterly risk report | Internal audit findings | Risk appetite review | Compliance status | Major incidents |
| **Decision Authority** | Sets risk appetite | Approves ISMS scope | Receives internal audit reports | Approves GRC programme budget |
| **Reporting Line** | Reports to full Board |

### 4.2 Security Steering Committee (Management Level)

| Element | Detail |
|---------|--------|
| **Purpose** | Provides executive management oversight of the day-to-day security programme, risk management, and compliance |
| **Chair** | CISO or CFO (as agreed) |
| **Membership** | CISO (Chair) | CFO | CTO | Head of Legal | DPO | Head of HR | Head of Product | CISO's GRC Lead |
| **Quorum** | 4 members |
| **Frequency** | Monthly |
| **Key Agenda Items** | Monthly security metrics dashboard | Open risks and treatment progress | Policy approvals | Vendor risk updates | Upcoming compliance deadlines |
| **Decision Authority** | Approves policies | Approves risk treatment plans within budget authority | Escalates to Board |
| **Reporting Line** | Reports to CEO; provides materials to Board Risk Committee |

### 4.3 Security Operations Forum (Operational Level)

| Element | Detail |
|---------|--------|
| **Purpose** | Operational coordination of security activities; tactical decision-making |
| **Chair** | CISO or GRC Lead |
| **Membership** | CISO | Head of IT | Security Operations Lead | DevOps Lead | IT Infrastructure Manager | GRC Analyst |
| **Frequency** | Bi-weekly |
| **Key Agenda Items** | Open vulnerabilities and patches | Incidents in progress | Control testing results | Evidence requests | Upcoming audit preparations |
| **Decision Authority** | Operational security decisions within policy bounds |

---

## 5. Roles and Responsibilities

### CISO (Chief Information Security Officer)

**Accountable for:** The overall information security posture and GRC programme effectiveness.

Key responsibilities:
- Sets the security strategy and direction (within board-approved framework)
- Presents quarterly to the Board Risk and Audit Committee
- Owns the information security risk register
- Approves security policies (below board level)
- Manages the GRC team and programme budget
- Acts as the Responsible Officer for ISO 27001 ISMS
- Manages relationships with external auditors and regulators

### DPO (Data Protection Officer)

**Accountable for:** GDPR / UK GDPR compliance and data subject rights.

Key responsibilities:
- Maintains the Record of Processing Activities (RoPA)
- Provides guidance on DPIAs
- Acts as the point of contact for the ICO
- Manages Subject Access Requests oversight

### Head of Internal Audit

**Accountable for:** Independent assurance on control effectiveness.

Key responsibilities:
- Develops and executes the annual audit programme
- Reports directly to Board Audit Committee (not CISO)
- Issues audit findings and tracks corrective actions
- Provides assurance opinion on ISMS effectiveness

### Business Unit Heads (First Line Risk Owners)

**Accountable for:** Information security within their business area.

Key responsibilities:
- Ensuring their teams adhere to security policies
- Reporting security incidents and near-misses
- Owning the data and systems within their remit
- Completing security awareness training

### All Employees

**Responsible for:**
- Compliance with all security policies
- Reporting suspected security incidents
- Completing mandatory security training
- Maintaining the security of assets entrusted to them

---

## 6. Policy Framework Architecture

[Company Name]'s policy hierarchy:

```
LEVEL 1: BOARD-APPROVED POLICIES
(High-level; principles-based; CEO/Board signature)
└── Information Security Policy (POL-001)
└── Risk Management Policy (POL-RMF-001)
└── Data Protection Policy (POL-DP-001)

LEVEL 2: MANAGEMENT-APPROVED STANDARDS
(Specific requirements; CISO approval)
└── Access Control Standard
└── Password Standard
└── Cryptography Standard
└── Patch Management Standard
└── [Domain-specific standards]

LEVEL 3: OPERATIONAL PROCEDURES
(Step-by-step; IT/Operations teams)
└── User Provisioning Procedure
└── Incident Response Procedures
└── Backup and Recovery Procedures
└── [Operational procedures]

LEVEL 4: GUIDELINES AND BEST PRACTICES
(Advisory; recommended but not mandatory)
└── Secure Coding Guide
└── Password Manager Guidance
└── Remote Working Best Practices
```

**Policy lifecycle:** Draft → Legal/DPO Review → CISO Approval → Publication → Annual Review

---

## 7. Governance Reporting Cadence

| Report | Frequency | Audience | Author | Key Content |
|--------|-----------|----------|--------|------------|
| Security Weekly Update | Weekly | CISO | Security Operations Team | Incidents, vulnerabilities, patches, operational status |
| GRC Programme Update | Monthly | Security Steering Committee | GRC Lead | Programme progress, KPIs, open risks, compliance status |
| Security Metrics Dashboard | Monthly | CISO + CFO | GRC Lead | 10 KPIs with RAG status, trend data |
| Board Cyber Risk Report | Quarterly | Board Risk & Audit Committee | CISO | Top risks (£ ALE), compliance status, audit findings, investment update |
| Annual ISMS Report | Annual | Board | CISO | Full ISMS review, programme maturity, Year+1 plan |

---

## 8. Governance KPIs

The following 8 KPIs measure the effectiveness of the security governance programme:

| KPI | Description | Target | Measurement Source | Owner |
|-----|-------------|--------|-------------------|-------|
| Policy review compliance | % of policies reviewed within review date | 100% | Policy register | GRC Lead |
| Risk register review frequency | Risk register reviewed monthly by CISO | 12 reviews/year | Risk register version history | CISO |
| Security awareness training completion | % staff completing annual training | ≥ 95% | LMS completion report | HR/GRC |
| Internal audit completion rate | % of planned audits completed on schedule | 100% | Audit programme tracker | Head of Internal Audit |
| Audit finding closure SLA | % of high/critical audit findings closed within agreed SLA | ≥ 80% within SLA | Audit tracking system | GRC Lead |
| Board reporting cadence | Quarterly board security report delivered on time | 4 of 4 per year | Board meeting minutes | CISO |
| Tier 1 vendor assessment completion | % of Tier 1 vendors assessed annually | 100% | Vendor risk register | GRC Lead |
| Management review conducted | Quarterly ISMS management review completed | 4 per year | Management review minutes | CISO |

---

## 9. Governance Compliance Calendar

| Activity | Owner | Frequency | Month(s) |
|----------|-------|-----------|---------|
| Board Risk & Audit Committee | CISO | Quarterly | Jan, Apr, Jul, Oct |
| Security Steering Committee | CISO | Monthly | All months |
| Security Operations Forum | GRC Lead | Bi-weekly | All months |
| ISMS Management Review | CISO | Quarterly | Mar, Jun, Sep, Dec |
| Annual risk assessment | GRC Lead | Annual | Q1 |
| Internal audit programme | Head of Internal Audit | As planned | Per audit schedule |
| Annual policy reviews | GRC Lead | Annual | Q4 |
| Annual penetration test | GRC Lead | Annual | Q3 |
| Vendor Tier 1 assessments | GRC Lead | Annual | Q2 |

---

## 10. RACI Matrix — Security Governance Activities

| Activity | Board | CEO | CISO | CFO | DPO | GRC Lead | Head of IT | BU Heads | All Staff |
|----------|-------|-----|------|-----|-----|---------|-----------|---------|---------|
| Set risk appetite | A | C | R | C | I | C | I | I | I |
| Approve IS Policy | A | R | C | I | C | C | I | I | I |
| Manage risk register | I | I | A | I | C | R | C | C | I |
| Internal security audit | I | I | A | I | I | R | C | C | I |
| GDPR compliance | I | I | C | I | A | C | C | C | R |
| Vendor risk assessments | I | I | A | I | C | R | C | C | I |
| Security awareness training | I | I | A | C | I | R | I | C | R |
| Incident response | I | C | A | C | C | C | R | R | R |
| Board security reporting | A | C | R | C | I | C | I | I | I |
| Policy compliance monitoring | I | I | A | I | C | R | C | C | I |

*A = Accountable | R = Responsible | C = Consulted | I = Informed*

---

## 11. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | YYYY-MM-DD | [Name] | Initial framework |

---

*Security Governance Framework | v1.0 | ISO 27001:2022 Clause 5 | COBIT 2019 | IIA Three Lines Model 2020*
