# NIST Cybersecurity Framework 2.0 — Maturity Assessment Template

| Field | Value |
|-------|-------|
| **Document ID** | NIST-CSF-001 |
| **Organisation** | [Company Name] |
| **Version** | 1.0 |
| **Assessment Date** | DD-MMM-YYYY |
| **Assessor** | [Name / Role] |
| **Framework Version** | NIST CSF 2.0 (Published February 2024) |
| **Classification** | Confidential — Internal |

---

## Purpose

This assessment evaluates the organisation's cybersecurity posture against the NIST Cybersecurity Framework version 2.0. It establishes a Current Profile, defines a Target Profile, and identifies gaps for remediation. Results inform the cybersecurity strategy and investment prioritisation.

---

## NIST CSF 2.0 Implementation Tiers

| Tier | Name | Description |
|------|------|-------------|
| **Tier 1** | Partial | Cybersecurity risk management is not formalised. Reactive approach. No risk awareness at organisational level. |
| **Tier 2** | Risk Informed | Risk management practices approved but not organisation-wide. Some awareness of risk. |
| **Tier 3** | Repeatable | Formal, documented, consistent practices. Organisation-wide adoption. Risk-informed decisions. |
| **Tier 4** | Adaptive | Cybersecurity practices continuously improved. Predictive, proactive. Active information sharing. |

---

## Assessment Summary

### Current Profile vs Target Profile

| Function | Current Tier | Target Tier | Gap | Priority |
|----------|-------------|-------------|-----|----------|
| GOVERN (GV) | 1 | 3 | 2 | Critical |
| IDENTIFY (ID) | 2 | 3 | 1 | High |
| PROTECT (PR) | 2 | 3 | 1 | High |
| DETECT (DE) | 1 | 3 | 2 | Critical |
| RESPOND (RS) | 1 | 3 | 2 | Critical |
| RECOVER (RC) | 1 | 3 | 2 | High |
| **Overall Average** | **1.3** | **3.0** | **1.7** | |

> **Visual:** Insert radar/spider chart here showing 6 axes with current (dotted) and target (solid) tier lines

---

## Detailed Assessment — GOVERN (GV)

### GV.OC — Organisational Context

| Subcategory | ID | Description | Current Tier | Evidence | Gap | Recommended Action |
|-------------|-----|-------------|-------------|---------|-----|-------------------|
| Organisational mission is understood | GV.OC-01 | The organisational mission, objectives, stakeholders, and activities are understood and inform cyber risk management decisions | 1 | No documented security strategy | No alignment between business strategy and cybersecurity | Develop GRC Strategy document |
| Legal requirements are identified | GV.OC-02 | Legal, regulatory, contractual requirements regarding cybersecurity — including privacy and civil liberties obligations — are understood and managed | 2 | GDPR obligations known; FCA requirements not formally documented | Regulatory obligations not comprehensively documented | Build compliance obligations register |
| Information security strategy is aligned | GV.OC-03 | Organisational cybersecurity risk strategy risk tolerances and assumptions are established, communicated, and used to make decisions | 1 | No formal risk strategy or risk appetite statement | No risk appetite defined | Define risk appetite; communicate to all risk owners |

### GV.RM — Risk Management Strategy

| Subcategory | ID | Description | Current Tier | Evidence | Gap | Recommended Action |
|-------------|-----|-------------|-------------|---------|-----|-------------------|
| Risk management objectives established | GV.RM-01 | Risk management objectives are established and agreed to by organisational stakeholders | 1 | No formal risk management programme | Risk management objectives not defined | Establish enterprise risk management programme |
| Risk appetite established | GV.RM-02 | Risk tolerance statements are established, communicated, and maintained | 1 | No risk appetite statement exists | Risk appetite not defined or communicated | Draft and approve risk appetite statement |
| Risk management process established | GV.RM-03 | Cybersecurity risk management activities and outcomes are included in enterprise risk management processes | 1 | Risk managed ad hoc by IT team | No formal risk management methodology | Implement ISO 27005-aligned risk methodology |

### GV.SC — Cybersecurity Supply Chain Risk Management

| Subcategory | ID | Description | Current Tier | Evidence | Gap | Recommended Action |
|-------------|-----|-------------|-------------|---------|-----|-------------------|
| Supply chain risk strategy established | GV.SC-01 | A cybersecurity supply chain risk management program, strategy, objectives, policies, and processes are established and agreed to | 1 | No vendor risk management programme | No supply chain risk governance | Establish VRM programme; write vendor management policy |
| Supplier contracts include security requirements | GV.SC-05 | Requirements to address cybersecurity risks in supply chains are established, prioritised, and integrated into contracts | 1 | Some contracts have basic T&Cs; no security clauses | No security requirements in vendor contracts | Update standard vendor contract template; require DPAs |

---

## Detailed Assessment — IDENTIFY (ID)

### ID.AM — Asset Management

| Subcategory | ID | Description | Current Tier | Evidence | Gap | Recommended Action |
|-------------|-----|-------------|-------------|---------|-----|-------------------|
| Hardware assets inventoried | ID.AM-01 | Inventories of hardware managed by the organisation are maintained | 2 | Partial spreadsheet inventory; 3 unregistered servers | Incomplete; not automated | Implement automated asset discovery (CrowdStrike Falcon or AWS Config) |
| Software assets inventoried | ID.AM-02 | Inventories of software, services, and systems managed by the organisation are maintained | 2 | SCCM deployed for Windows; cloud services not inventoried | Cloud and SaaS not covered | Add cloud asset discovery; shadow IT detection |
| Network flows documented | ID.AM-03 | Representations of the organisation's authorised network communication and internal and external network data flows are maintained | 1 | No data flow maps exist | No network documentation | Commission network mapping exercise |
| External systems catalogued | ID.AM-07 | Inventories of services provided by suppliers, components, and third parties are maintained | 1 | No vendor inventory | No supplier inventory | Build vendor register (all third parties) |

### ID.RA — Risk Assessment

| Subcategory | ID | Description | Current Tier | Evidence | Gap | Recommended Action |
|-------------|-----|-------------|-------------|---------|-----|-------------------|
| Threats identified | ID.RA-01 | Vulnerabilities in assets are identified, validated, and recorded | 2 | Qualys scanner deployed; results not actioned systematically | Scanning without systematic remediation | Implement vulnerability management SLA |
| Cyber threat intelligence gathered | ID.RA-02 | Cyber threat intelligence is received from information sharing forums and sources | 1 | No formal threat intel programme | No threat intelligence process | Subscribe to NCSC feeds; ISAC membership |
| Risk assessment conducted | ID.RA-05 | Threats, vulnerabilities, likelihoods, and impacts are used to understand inherent risk and inform risk response priorities | 1 | Risk register exists but 11 months old | Risk assessment not maintained | Conduct formal risk assessment; monthly updates |

---

## Detailed Assessment — PROTECT (PR)

### PR.AA — Identity Management, Authentication, and Access Control

| Subcategory | ID | Description | Current Tier | Evidence | Gap | Recommended Action |
|-------------|-----|-------------|-------------|---------|-----|-------------------|
| Identities managed | PR.AA-01 | Identities and credentials for authorised users, services, and hardware are managed by the organisation | 2 | AD managed; service accounts undocumented | Service account inventory missing | Audit and document all service accounts |
| MFA implemented | PR.AA-03 | Users, services, and hardware are authenticated | 2 | MFA for O365; not for VPN or on-premise systems | MFA not universal | Enforce MFA for all remote access and privileged access |
| Access reviews conducted | PR.AA-05 | Access permissions, entitlements, and authorisations are defined in a policy, managed, enforced, and reviewed | 1 | No access reviews conducted | No formal access review process | Implement quarterly access reviews |

### PR.AT — Awareness and Training

| Subcategory | ID | Description | Current Tier | Evidence | Gap | Recommended Action |
|-------------|-----|-------------|-------------|---------|-----|-------------------|
| Security awareness training | PR.AT-01 | Personnel are provided with awareness and training so that they possess the knowledge and skills to perform general tasks with cybersecurity risks in mind | 2 | Annual training; completion rate 67% | Training not universal; no phishing simulation | Improve to 95% completion; add quarterly phishing simulations |
| Privileged user training | PR.AT-02 | Individuals in specialised roles are provided with awareness and training so that they possess the knowledge and skills to perform relevant cybersecurity tasks | 1 | No role-specific training for IT admins | No privileged user-specific training | Implement role-based security training programme |

---

## Detailed Assessment — DETECT (DE)

### DE.CM — Continuous Monitoring

| Subcategory | ID | Description | Current Tier | Evidence | Gap | Recommended Action |
|-------------|-----|-------------|-------------|---------|-----|-------------------|
| Networks monitored | DE.CM-01 | Networks and network services are monitored to find potentially adverse events | 1 | No SIEM; CloudTrail enabled but not reviewed | No active monitoring | Implement SIEM; establish log review process |
| Computing environment monitored | DE.CM-09 | Computing hardware and software, runtime environments, and their data are monitored to find potentially adverse events | 1 | Basic AV on endpoints; no EDR | No behavioural detection | Deploy EDR (CrowdStrike or SentinelOne) |

### DE.AE — Adverse Event Analysis

| Subcategory | ID | Description | Current Tier | Evidence | Gap | Recommended Action |
|-------------|-----|-------------|-------------|---------|-----|-------------------|
| Event thresholds established | DE.AE-03 | Information is correlated from multiple sources | 1 | Events in silos; no correlation | No event correlation | SIEM implementation with correlation rules |
| Impact estimated | DE.AE-07 | Cyber threat intelligence and other contextual information are integrated into the analysis of adverse events | 1 | No threat intelligence integration | No threat-informed detection | Integrate threat intel feeds with SIEM |

---

## Detailed Assessment — RESPOND (RS)

### RS.MA — Incident Management

| Subcategory | ID | Description | Current Tier | Evidence | Gap | Recommended Action |
|-------------|-----|-------------|-------------|---------|-----|-------------------|
| Incident response plan executed | RS.MA-01 | The incident response plan is executed in coordination with relevant third parties once an incident is declared | 1 | No formal IR plan | No IR programme | Develop IR Policy, IR Plan, and 3 playbooks |
| Incidents categorised | RS.MA-02 | Incidents are categorised and prioritised | 1 | IT handles incidents informally; no severity classification | No incident classification | Implement P1–P4 severity classification |

---

## Detailed Assessment — RECOVER (RC)

### RC.RP — Incident Recovery Plan Execution

| Subcategory | ID | Description | Current Tier | Evidence | Gap | Recommended Action |
|-------------|-----|-------------|-------------|---------|-----|-------------------|
| Recovery plan executed | RC.RP-01 | The recovery portion of the incident response plan is executed once initiated from the incident response process | 1 | No documented recovery plan | No recovery planning | Develop DR plan; define RTOs/RPOs |
| Recovery actions communicated | RC.RP-04 | The timing of restoration of affected systems or services and the status of the organisation's recovery activities are communicated to stakeholders | 1 | No communication templates | No recovery communication plan | Add communication procedures to DR plan |

---

## Gap Analysis Summary

| Priority | Action | CSF Category | Timeline | Estimated Cost |
|---------|--------|-------------|---------|---------------|
| Critical | Implement SIEM | DE.CM | Q1 | £80–150K |
| Critical | Develop IR Programme | RS.MA | Q1 | £20K (staff time) |
| Critical | Define risk appetite | GV.RM | Q1 | £5K (staff time) |
| High | Enforce MFA universally | PR.AA | Q1 | £0–£5K (M365 licence) |
| High | Deploy EDR | DE.CM | Q2 | £50–80K |
| High | Implement access reviews | PR.AA | Q2 | £0 (process change) |
| High | Establish vendor risk programme | GV.SC | Q2 | £20K (staff time) |
| Medium | Complete asset inventory | ID.AM | Q2 | £15K |
| Medium | Implement DR plan | RC.RP | Q3 | £50K |

---

## Recommended Implementation Roadmap

**Quarter 1 (Months 1–3) — Critical Foundations:**
Address all Critical-priority gaps. Total estimated investment: £105–175K

**Quarter 2 (Months 4–6) — Controls Improvement:**
Address all High-priority gaps. Total estimated investment: £90–110K

**Quarter 3–4 (Months 7–12) — Optimisation and Monitoring:**
Address Medium-priority gaps; implement continuous monitoring. Total estimated investment: £65K

**Total Year 1 investment: £260–350K**
**Expected outcome: Move from average Tier 1.3 to Tier 3.0 by Month 12**

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | YYYY-MM-DD | [Name] | Initial assessment |

---

*NIST CSF 2.0 Maturity Assessment Template | v1.0 | Aligned to NIST CSF 2.0 (February 2024)*
