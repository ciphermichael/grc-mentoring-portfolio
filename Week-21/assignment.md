# Week 21 Assignment: Capstone — Enterprise GRC Strategy & Governance

## Capstone Overview

| Field | Detail |
|-------|--------|
| **Client** | NovaTech Corp |
| **Your Role** | Lead GRC Consultant |
| **Estimated Time** | 12–16 hours |
| **Difficulty** | 🌟🌟🌟🌟🌟 |
| **Frameworks** | ISO 27001:2022, NIST CSF 2.0, GDPR/UK GDPR, PCI-DSS v4.0, FCA PS21/3 |

---

## NovaTech Corp — Full Client Profile

**Company:** NovaTech Corp
**Industry:** UK Fintech — Consumer Payment Processing
**Size:** 2,000 employees (London HQ 1,200; Manchester office 500; Edinburgh office 300)
**Founded:** 2016
**Revenue:** £180M ARR (growing 35% YoY)
**Customers:** 5 million retail payment customers
**Investors:** Series C funded (£85M, closed 6 months ago)
**Technology Stack:** AWS (eu-west-2), Azure AD for identity, custom payment processing platform, Salesforce CRM, Jira, GitHub, Slack, Microsoft 365

**Regulatory Environment:**
- Regulated by FCA as a Payment Institution (Authorisation No. 12345678)
- PRA oversight for systemic risk requirements (as they grow)
- UK GDPR obligations (ICO registered; DPO appointed part-time)
- PCI-DSS v4.0 — processes cardholder data; currently QSA-assessed as Level 2 merchant
- FCA PS21/3 (Operational Resilience) — important business services must be identified; tolerance for disruption set by March 2025

**Current Security State (from your initial assessment):**
- No ISO 27001 or SOC 2 certification
- FCA cyber governance review raised 3 findings (board oversight inadequate; no operational resilience programme; risk management informal)
- No formal internal security audit programme
- Risk register exists as a spreadsheet but has not been reviewed in 11 months
- GDPR DPO appointed but part-time; programme immature
- Vendor management: no formal programme; 15 critical vendors including payment processor, cloud hosting, data analytics partner
- Security team: 8 people (CISO + 7 engineers); no dedicated GRC resource
- Board: 7 members including 3 NEDs; cybersecurity briefing last occurred 18 months ago
- Series C investors have mandated ISO 27001 certification as a condition for Series D consideration

**Your engagement:** NovaTech's CEO, Kemi Adeyemi, has engaged your firm as Lead GRC Consultants to build their enterprise GRC programme from the ground up. You have a 12-month mandate and a Year 1 budget of £650,000. Your engagement lead within NovaTech is Raj Singh, the CISO.

---

## This Week's Capstone Deliverables

### Deliverable 1: GRC Strategy Document (Vision, Mission, Objectives)

**Strategic importance:** This is the governing document for the entire 12-month engagement. Every subsequent deliverable (risk register, policies, compliance matrix) must align to the strategy. The CEO will sign this document, and the investors will review it.

**Required content:**

**Executive Summary** (1 page, written for the CEO):
- Current state assessment: NovaTech's GRC maturity today in 3 bullets
- The case for investment: What are the business risks of the status quo? (FCA enforcement risk, ISO 27001 certification blocking enterprise sales, investor requirement)
- The programme summary: What you will build in 12 months
- Total investment: Year 1 programme cost summary
- Expected outcomes: What NovaTech achieves by the end of the programme

**1. GRC Vision Statement**:
Write NovaTech's GRC vision — where do they want to be in 3 years? Example structure: "NovaTech Corp will be recognised as a leader in financial technology governance, operating with ISO 27001-certified security management, PCI-DSS Level 1 compliance, and mature risk management practices that enable confident growth into new markets."

**2. GRC Mission Statement**:
The day-to-day purpose of the GRC function. 2 sentences.

**3. Strategic Objectives** (5 objectives, each with a measurable target):
- Objective 1: Achieve ISO 27001:2022 certification by Q4 2025
- Objective 2: Achieve PCI-DSS Level 2 recertification with 0 Level 1 findings by Q3 2025
- Objective 3: Remediate 3 FCA operational resilience findings by Q2 2025
- Objective 4: Establish formal enterprise risk management programme with monthly board reporting by Q1 2025
- Objective 5: Achieve GRC programme maturity score of 3.5/5.0 (CMMI Level 3) by Q4 2025

For each objective: Measurable target | Business justification | Key dependencies | Owner | Budget allocation

**4. Current State vs Target State Assessment**:
Use a radar chart or table showing maturity (0–5) across 8 GRC domains in current state vs target state:
- Governance and Oversight
- Risk Management
- Policy Framework
- Compliance Management
- Audit and Assurance
- Vendor Risk Management
- Incident Response
- Security Metrics and Reporting

**5. Programme Investment Summary** (Year 1):
| Category | Estimated Cost |
|----------|---------------|
| External consultancy (this engagement) | £200,000 |
| ISO 27001 certification audit (BSI) | £35,000 |
| GRC technology platform (Vanta) | £45,000/yr |
| Penetration testing programme | £25,000 |
| Internal GRC headcount (1 GRC Analyst hire) | £48,000/yr |
| Security awareness training platform | £15,000/yr |
| PAM tooling (CyberArk) | £80,000 |
| SIEM implementation | £120,000 |
| Miscellaneous (training, subscriptions, tools) | £82,000 |
| **Total Year 1** | **£650,000** |

**6. Expected Business Value**:
- Enterprise sales unlocked by ISO 27001: Estimated £2.5M ARR from 3 enterprise opportunities currently blocked
- FCA enforcement risk mitigated: Estimated £15–50M fine risk (based on comparable FCA enforcement actions)
- Series D investor requirement met: Condition for Series D consideration (investor mandate)
- PCI-DSS Level 1 compliance enables higher transaction limits: Additional revenue opportunity

---

### Deliverable 2: Security Governance Framework

**Required content:**

1. **Three Lines of Defense at NovaTech** (name the actual NovaTech teams/roles in each line):
   - First Line: Technology Engineering, Product, Operations, Finance, HR
   - Second Line: GRC Team (CISO leads), DPO, Risk Management function (new)
   - Third Line: Internal Audit (new function), External Auditors, FCA Supervisory Review

2. **Security Committee Structure** (3 committees with charters):
   - Board Risk & Audit Committee (quarterly; 3 NEDs + CEO attend; CISO presents)
   - Security Steering Group (monthly; CISO chairs; CFO, CTO, Head of Legal, DPO, Head of Product)
   - Security Operations Forum (bi-weekly; CISO chairs; IT Security leads, Engineering leads)

3. **Governance Reporting Cadence**:
   | Report | Frequency | Audience | Author | Contents |
   |--------|-----------|----------|--------|---------|
   | Security Operations Update | Weekly | CISO | Security Team | Incidents, vulnerabilities, patch status |
   | GRC Programme Update | Monthly | Security Steering Group | GRC Lead | Programme progress, open risks, compliance status |
   | Security Metrics Dashboard | Monthly | CISO + CFO | GRC Lead | 10 KPIs with RAG status |
   | Board Security Report | Quarterly | Board Risk Committee | CISO | Top 5 risks, compliance status, investment update |

4. **RACI Matrix** (15+ GRC activities):
   Roles: CEO | CISO | CFO | CTO | Head of Legal | DPO | GRC Lead | Business Unit Heads | All Staff
   Activities: IS Policy approval, Risk assessment, Risk appetite setting, GDPR compliance, Vendor risk, Internal audit, Board reporting, FCA correspondence, PCI-DSS compliance, Incident response, Business continuity, Security awareness training, New system security review, Penetration testing oversight, ISO 27001 programme management

5. **Policy Hierarchy Architecture** for NovaTech:
   Level 1 (Board-approved): Information Security Policy, Data Protection Policy, Risk Management Policy
   Level 2 (CISO-approved): 15 security standards (one per domain)
   Level 3 (IT Management-approved): Operational procedures
   Level 4: Guidelines and best practices

---

### Deliverable 3: GRC Operating Model

**Required content:**

1. **GRC Team Structure** (Year 1):
   - CISO: Raj Singh (existing; your primary stakeholder)
   - GRC Lead / Programme Manager: New hire (you are filling this role during the engagement, then transitioning to a permanent hire)
   - GRC Analyst: New hire (£48,000; responsible for day-to-day compliance tracking, evidence collection, policy maintenance)
   - DPO: Upgrade from part-time to full-time (£55,000)
   - Security Awareness Lead: Shared with HR (20% FTE)

2. **Build vs Buy Analysis** for key GRC capabilities:
   | Capability | Build (Internal) | Buy (External/Outsourced) | Recommendation |
   |------------|-----------------|--------------------------|----------------|
   | Internal Audit | Option: hire Internal Auditor | Option: co-source with Big 4 firm | Buy: co-source with KPMG for Year 1 |
   | Penetration Testing | Option: build team | Option: annual external firm | Buy: external firm annually |
   | GRC Technology | Option: build in Excel | Option: Vanta/ServiceNow | Buy: Vanta (recommended) |
   | ISO 27001 Audit | N/A | External only (BSI/LRQA) | Buy: BSI |
   | Security Awareness | Option: build content | Option: KnowBe4 platform | Buy: KnowBe4 |

3. **GRC Platform Recommendation**: Recommend Vanta with justification (NovaTech's size, multi-framework need: ISO 27001 + GDPR + PCI-DSS, AWS/Azure integration, 90-day implementation timeline).

4. **GRC Team Interaction Model**: How does GRC interact with Engineering, Product, Finance, Legal, HR? Define the "GRC Business Partner" model where each GRC team member has assigned business unit relationships.

---

### Deliverable 4: Regulatory Obligations Register

**Required content:**

| Regulation | Specific Requirement | Enforcement Body | Compliance Deadline | Current Status | Gap | Owner | Priority |
|------------|---------------------|-----------------|--------------------|--------------|----|-------|----------|
| FCA PS21/3 | Identify important business services; set impact tolerances | FCA | March 2025 | Not started — FCA finding | CRITICAL GAP | CISO | P1 |
| UK GDPR Art. 30 | Maintain up-to-date RoPA | ICO | Ongoing | RoPA exists but outdated | GAP | DPO | P1 |
| PCI-DSS v4.0 Req 12.3.1 | Annual security policy review | PCI SSC | Annual | Policies not reviewed in 2 years | GAP | GRC Lead | P2 |
| ISO 27001:2022 Clause 9.2 | Internal audits at planned intervals | BSI (certification) | Pre-Stage 1 audit | No audit programme | GAP | GRC Lead | P1 |
| UK Companies Act 2006 | Directors' duties re information security | HMRC/Courts | Ongoing | Informal | — | CEO/Legal | P3 |

Complete for minimum 15 specific regulatory requirements across all applicable regulations.

---

### Deliverable 5: 12-Month GRC Roadmap

**Required content:**

A detailed Gantt-style plan showing the complete 12-month programme:

**Q1 (Months 1–3) — Foundation:**
- Month 1: GRC strategy approved by board; RACI signed; governance committees established; Vanta onboarded; GRC Analyst hired
- Month 2: IS Risk Assessment conducted (30+ risks); Risk Register v1.0; Risk Appetite Statement drafted; FCA finding 1 remediated (board cyber briefing conducted)
- Month 3: Policy Library v1.0 (15 policies written); Policy Register established; FCA finding 2 remediated (risk management process documented)

**Q2 (Months 4–6) — Controls Implementation:**
- Month 4: PAM tooling deployed for privileged accounts; Patch Management SLA enforced; Vendor Risk Register established (15 vendors tiered)
- Month 5: ISO 27001 Gap Assessment complete; SoA v1.0; ISO 27001 remediation roadmap; PCI-DSS gap assessment
- Month 6: SIEM implementation complete; incident response programme launched; FCA finding 3 remediated (operational resilience programme)

**Q3 (Months 7–9) — Audit and Assurance:**
- Month 7: Internal audit programme launched (co-sourced with KPMG); Access Control Audit 1 complete
- Month 8: ISO 27001 internal audit complete; non-conformances remediated
- Month 9: ISO 27001 pre-audit readiness check; annual penetration test; PCI-DSS QSA prep

**Q4 (Months 10–12) — Certification:**
- Month 10: ISO 27001 Stage 1 audit; Stage 1 findings remediated
- Month 11: ISO 27001 Stage 2 audit
- Month 12: ISO 27001 certificate received; PCI-DSS Level 2 recertification; GRC maturity assessment; board year-end review; Year 2 plan presented

---

### Deliverable 6: Security Committee Charter (Security Steering Group)

**Required content:** Write the full charter for the Security Steering Group as described in Deliverable 2. Include: purpose, membership (named roles), quorum, meeting frequency and format, standing agenda, decision authority, escalation paths, reporting line, review date. 1–2 pages.

---

## Capstone Quality Standards

### What Makes This Capstone Distinction-Grade?

1. All NovaTech scenario details used consistently (2,000 employees, £180M ARR, £650K budget, Series C investors, 5M customers, FCA regulatory findings)
2. GRC Strategy includes financial analysis (costs, expected business value, investment ROI)
3. Governance framework includes operating rules for all 3 committees (not just membership lists)
4. Regulatory obligations register covers FCA PS21/3, PCI-DSS v4.0, UK GDPR, ISO 27001 with specific requirements
5. 12-month roadmap is correctly sequenced (governance before controls; internal audit before external certification)
6. All documents are board-ready: professional format, version control, no placeholder text
7. Week 21 deliverables are internally consistent with each other (strategy supports governance; operating model resources governance; roadmap delivers strategy)

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **ISO 27001:2022** | Certification target; governance framework reference; SoA and gap assessment planned |
| **NIST CSF 2.0** | GOVERN function applied to governance framework design |
| **FCA PS21/3** | Operational resilience findings remediation in roadmap |
| **UK GDPR** | DPO role in operating model; GDPR obligations in regulatory register |
| **PCI-DSS v4.0** | Compliance obligations in regulatory register; certification roadmap |

---

## Week-Specific Resources

- [FCA: Operational Resilience PS21/3](https://www.fca.org.uk/publications/policy-statements/ps21-3-operational-resilience-financial-sector) — NovaTech's primary regulatory gap
- [NCSC: Board Toolkit](https://www.ncsc.gov.uk/collection/board-toolkit) — Board-level governance reference
- [OCEG GRC Capability Model](https://www.oceg.org/resources/grc-capability-model-red-book/) — Enterprise GRC programme design
- [ISO 27001:2022 Clause 5 — Leadership](https://www.iso.org/standard/27001) — Governance requirements
- [Vanta Platform](https://www.vanta.com/) — Recommended GRC platform for NovaTech
- [BSI: ISO 27001 Certification Process](https://www.bsigroup.com/en-GB/iso-27001-information-security/) — Understanding the Stage 1/2 audit process for roadmap

---

## Submission

```
Capstone-NovaTech/01-Governance/
├── NovaTech-GRC-Strategy-v1.0.md
├── NovaTech-Security-Governance-Framework-v1.0.md
├── NovaTech-GRC-Operating-Model-v1.0.md
├── NovaTech-Regulatory-Obligations-Register-v1.0.xlsx
├── NovaTech-GRC-Roadmap-12Month-v1.0.xlsx
└── NovaTech-Security-Steering-Group-Charter-v1.0.md
```
