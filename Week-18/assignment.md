# Week 18 Assignment: GRC Program Management

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | InsureCo |
| **Your Role** | Head of GRC / Senior GRC Consultant |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟🌟🌟 |
| **Frameworks** | ISO 27001, SOC 2, GDPR (multi-framework management) |

---

## Scenario Brief — Read This Carefully

**InsureCo** is a 1,500-person UK general insurance company regulated by the FCA and PRA. They provide home, motor, and business insurance through direct and broker channels. Annual gross written premium: £320M. Their IT environment includes: an on-premise core insurance platform (policy management, claims, underwriting), Microsoft 365, Salesforce CRM, Guidewire (claims management, cloud-hosted on AWS), and a data warehouse on Azure.

InsureCo processes personal data for approximately 2 million policyholders (financial, motor, property, health-related data). They are currently managing three separate compliance programmes: ISO 27001 (certified since 2021), SOC 2 Type II (required by one large US broker partner), and GDPR. Each programme is managed by a different team member with minimal coordination.

**Current state problems:**
- 3 separate policy libraries with 12 duplicate and 3 contradictory policies
- ISO 27001 internal audit and SOC 2 control testing conducted separately — same controls tested twice
- Compliance calendar is 3 separate spreadsheets; stakeholders receive inconsistent information
- GRC team: 4 people (Head of GRC, 2 GRC Analysts, 1 DPO) — unsustainable with 3 separate programmes
- No GRC technology platform — all evidence collected manually in SharePoint folders
- ISO 27001 surveillance audit is in 5 months; SOC 2 observation period ends in 3 months
- Budget for next year: £850,000 (reduced 20% from current year) — efficiency is mandatory

**The CFO, Jennifer Park, has asked you to produce:** "A plan to run ISO 27001, SOC 2, and GDPR as one integrated programme — reducing team overhead by 30% while maintaining compliance quality."

---

## Deliverables

### Deliverable 1: GRC Programme Charter

**What It Is:** The formal document authorising and defining InsureCo's integrated GRC programme.

**Must include:**
1. **Programme Purpose**: Why does this integrated GRC programme exist? What problems does it solve?
2. **Programme Scope**: ISO 27001 + SOC 2 Type II + GDPR; all InsureCo entities; all UK offices; AWS and Azure environments; all 1,500 employees
3. **Programme Governance**: Who makes decisions?
   - Programme Sponsor: Chief Risk Officer (accountable for programme success)
   - Programme Lead: Head of GRC (day-to-day management)
   - Programme Board: Monthly meeting — CRO, CISO, CFO, Head of Legal, DPO
4. **Budget**: £850,000 for Year 1 (breakdown: staff, tooling, external auditors, certification fees)
5. **Success Criteria**: How do we know the programme is working?
   - ISO 27001 surveillance audit passed with 0 major non-conformances
   - SOC 2 Type II report issued with clean opinion
   - GDPR compliance maintained (0 ICO enforcement actions)
   - Team overhead reduced by 30% vs prior year (quantified)
   - GRC platform implemented within 90 days
6. **Timeline**: 12-month programme plan milestones
7. **Risks**: Top 5 programme risks with mitigations

---

### Deliverable 2: Multi-Framework Compliance Calendar (12 Months)

**What It Is:** A single, integrated 12-month compliance calendar covering all ISO 27001, SOC 2, and GDPR activities.

**Create a visual calendar (Excel or spreadsheet) showing by month:**

**ISO 27001 activities:**
- Internal audits (6 planned across the year)
- Management review (Clause 9.3 — quarterly)
- Surveillance audit (Month 5 — fixed deadline)
- Policy review schedule (which policies in which month)
- Risk assessment update (bi-annual)

**SOC 2 activities:**
- SOC 2 observation period end (Month 3 — fixed)
- Evidence collection deadlines (monthly)
- Auditor evidence submission (Month 4)
- SOC 2 report issuance (Month 5)
- New observation period start (Month 5)

**GDPR activities:**
- Annual RoPA review (Month 2)
- DPIA review schedule (by process — spread across year)
- Privacy notice annual review (Month 3)
- Data retention schedule review (Month 6)
- DPO annual report (Month 12)
- SAR SLA monitoring (monthly)

**Cross-framework activities:**
- Quarterly board compliance report (every 3 months)
- Annual penetration test (Month 9)
- Annual vendor risk assessment reviews (Tier 1 — quarterly; Tier 2 — bi-annual)
- Security awareness training (quarterly refresh)

For each activity: Framework | Activity | Owner | Duration | Dependencies | Output

---

### Deliverable 3: Unified Compliance Matrix (ISO + SOC 2 + GDPR Control Mapping)

**What It Is:** A single spreadsheet mapping all InsureCo controls to ISO 27001, SOC 2, and GDPR requirements — demonstrating where one control satisfies multiple frameworks.

**Create a master control library with:**
- Control ID (CTRL-001 etc.)
- Control Name
- Control Description (what the control does and how it's evidenced)
- ISO 27001 mapping (Annex A reference)
- SOC 2 mapping (Common Criteria reference CC1–CC9)
- GDPR mapping (Article reference where applicable)
- Control Owner (role)
- Evidence Type
- Evidence Collection Method
- Frequency
- Implementation Status (Implemented / Partial / Gap)

**Complete for at minimum 30 controls, ensuring comprehensive coverage of:**
- Access control (maps to ISO A.5.15–5.22 + SOC 2 CC6 + GDPR Art. 32)
- Logging and monitoring (maps to ISO A.8.15 + SOC 2 CC7 + GDPR Art. 32)
- Incident response (maps to ISO A.5.24–5.28 + SOC 2 CC7.4 + GDPR Art. 33)
- Vendor management (maps to ISO A.5.19–5.22 + SOC 2 CC9 + GDPR Art. 28)
- Cryptography (maps to ISO A.8.24 + SOC 2 CC6.7 + GDPR Art. 32)
- Awareness training (maps to ISO A.6.3 + SOC 2 CC2.2 + GDPR Art. 32 implicitly)

**Summary tab:** Total controls | % satisfying all 3 frameworks | % satisfying 2 frameworks | unique single-framework controls | efficiency ratio

---

### Deliverable 4: GRC Tool Selection Analysis

**What It Is:** A professional tool selection analysis comparing 3 GRC platforms and recommending one for InsureCo.

**Evaluate these 3 options:**

**Option 1: Vanta**
- Best for: SMB to mid-market; ISO 27001 + SOC 2 + GDPR
- Key features: Automated evidence collection via integrations; real-time control monitoring; policy management; vendor risk
- Integrations: AWS, Azure, M365, GitHub, Salesforce, Jira (all relevant to InsureCo)
- Pricing: ~£30K–£60K/year (estimate for 1,500-person company)
- Limitations: Less suitable for large enterprise complexity; limited insurance-specific templates

**Option 2: ServiceNow GRC**
- Best for: Large enterprise; complex multi-framework; ITSM integration
- Key features: Policy management, risk management, audit management, vendor risk; integrates with ServiceNow ITSM
- Pricing: ~£150K–£300K/year (enterprise)
- Limitations: High cost; significant implementation effort (6–12 months); requires ServiceNow ITSM already in place

**Option 3: AuditBoard**
- Best for: Internal audit management + compliance
- Key features: Audit management, compliance workflows, risk management; excellent reporting
- Pricing: ~£60K–£100K/year
- Limitations: Less automation than Vanta; stronger on audit management than compliance automation

**Evaluation criteria:**
| Criterion | Weight | Vanta | ServiceNow | AuditBoard |
|-----------|--------|-------|------------|------------|
| ISO 27001 support | 25% | | | |
| SOC 2 support | 20% | | | |
| GDPR support | 15% | | | |
| Evidence automation | 20% | | | |
| Implementation time | 10% | | | |
| Total cost (3-year) | 10% | | | |
| **Total** | 100% | | | |

**Recommendation**: Which platform should InsureCo select? Justify with specific reasons referencing InsureCo's context.

---

### Deliverable 5: Programme Health Dashboard

**What It Is:** A monthly GRC programme health dashboard showing the integrated status of all three compliance programmes.

**Dashboard sections:**
1. **Overall Programme Status**: Red/Amber/Green; key alerts; upcoming critical deadlines
2. **ISO 27001 Status**: Internal audit completion rate; open non-conformances; surveillance audit readiness (%)
3. **SOC 2 Status**: Observation period progress; control effectiveness (% tested and effective); days to evidence submission deadline
4. **GDPR Status**: Open SARs and deadline status; overdue DPIA reviews; RoPA last updated; open findings from DPO review
5. **Cross-Programme Controls**: % of unified controls implemented; % with current evidence; outstanding evidence requests
6. **Key Deadlines (Next 30 Days)**: List all compliance deadlines with owner and days remaining

---

### Deliverable 6: Stakeholder Communication Plan

**What It Is:** A structured plan defining how the GRC programme communicates with each stakeholder group.

| Stakeholder | Frequency | Format | Content | Owner |
|-------------|-----------|--------|---------|-------|
| Board/Risk Committee | Quarterly | PowerPoint presentation | Compliance status, top risks, budget status, regulatory changes | Head of GRC |
| CISO | Monthly | 1-page dashboard | Programme health, control gaps, upcoming audits | GRC Analyst |
| IT/Engineering | Weekly | Email update | Evidence requests, upcoming control tests, remediation deadlines | GRC Analyst |
| DPO | Monthly | Meeting + report | GDPR compliance status, SARs, DPIA schedule | GRC Analyst (GDPR) |
| External Auditors (ISO/SOC 2) | As needed | Evidence portal / email | Audit evidence, responses to queries | Head of GRC |
| All staff | Quarterly | Intranet update | Security awareness, policy updates, training reminders | GRC Analyst |

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Programme Charter | 20% | Board-quality; authority clear; success criteria measurable |
| Unified Matrix | 30% | 30+ controls; accurate cross-framework mappings; efficiency demonstrated |
| Compliance Calendar | 20% | All 3 frameworks covered; integrated; owners assigned |
| Tool Selection | 15% | Objective criteria; InsureCo-specific recommendation justified |
| Stakeholder Communication | 15% | All stakeholders addressed; frequency and format appropriate |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **ISO 27001:2022** | Integrated into unified control library and programme calendar |
| **SOC 2 (AICPA TSC)** | Mapped to ISO controls; observation period managed |
| **GDPR** | Integrated into unified calendar and control matrix (Art. 32 security) |

---

## Week-Specific Resources

- [OCEG GRC Capability Model](https://www.oceg.org/resources/grc-capability-model-red-book/) — Definitive GRC programme design framework
- [Vanta Platform Overview](https://www.vanta.com/resources) — Compliance automation documentation
- [ServiceNow GRC](https://www.servicenow.com/products/security/governance-risk-compliance.html) — Enterprise GRC platform
- [ISO 27001 + SOC 2 Unified Approach — Secureframe](https://secureframe.com/blog/iso-27001-vs-soc-2) — Unification guidance
- [ISACA: GRC Programme Management](https://www.isaca.org/resources/grc) — Professional GRC resources

---

## Submission

```
Week-18/Deliverables/
├── InsureCo-GRC-Programme-Charter-v1.0.md
├── InsureCo-Compliance-Calendar-12Month-v1.0.xlsx
├── InsureCo-Unified-Compliance-Matrix-v1.0.xlsx
├── InsureCo-GRC-Tool-Selection-Analysis-v1.0.md
├── InsureCo-Programme-Health-Dashboard-v1.0.xlsx
└── InsureCo-Stakeholder-Communication-Plan-v1.0.xlsx
```
