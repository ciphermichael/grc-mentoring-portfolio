# Week 13 Assignment: Business Impact Analysis

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | GlobalLogistics Ltd. |
| **Your Role** | GRC Analyst — Business Continuity |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟🌟 |
| **Frameworks** | ISO 22301:2019, ISO 27001 (A.5.29, A.5.30) |

---

## Scenario Brief — Read This Carefully

**GlobalLogistics Ltd.** is a 24/7 UK logistics and supply chain management company employing 3,500 people. They operate logistics services for 180 corporate clients including major retailers (Next, Marks & Spencer) and pharmaceutical distributors. Their operations run continuously — 24 hours a day, 7 days a week, 365 days a year. Any system downtime has immediate financial consequences including £85,000 per hour in lost revenue and contractual penalties.

GlobalLogistics manages 8 regional distribution centres across the UK, a fleet management platform tracking 2,400 vehicles in real-time, a customer order management system processing 45,000 shipments per day, and a temperature monitoring system for pharmaceutical shipments (critical for regulatory compliance with MHRA).

Their CEO, Kevin Obi, has commissioned a Business Continuity Programme following two incidents in the last 18 months: a 7-hour AWS outage that disrupted order processing (£595,000 in losses and customer penalties), and a ransomware attack that encrypted their fleet management database (recovered in 11 days with significant manual process costs).

GlobalLogistics has no formal Business Continuity Management System (BCMS). They have no documented BIA, no formal RTOs or RPOs, no tested Business Continuity Plans. You have been engaged as their Business Continuity GRC Consultant to conduct GlobalLogistics' first BIA and produce the business continuity strategy inputs.

**Key systems and their current backup arrangements:**
- Order Management System (OMS) — AWS hosted; daily backup (24-hour RPO); no DR environment
- Fleet Management Platform — On-premise; weekly backup (7-day RPO!!); no DR
- Temperature Monitoring (Pharmaceutical) — IoT/cloud; 15-minute data snapshots; regulatory requirement to maintain records
- Warehouse Management System (WMS) — On-premise at 8 distribution centres; site-by-site backups; no central DR
- Finance System (SAP) — AWS hosted; 4-hourly backup; no tested recovery plan
- HR System (Workday) — SaaS; provider-managed backup; Workday SLA = 99.9% uptime
- Communication Platform (Microsoft Teams + Exchange) — M365; Microsoft SLA; 30-day recycle bin
- Customer Portal — AWS hosted; daily backup

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 13 — especially the RTO/RPO/MTD/MBCO definitions
- [ ] Read ISO 22301:2019 Clause 8.2 overview
- [ ] Read the BCI Good Practice Guidelines BIA chapter
- [ ] Understand the formula: RTO must always be < MTD

### Questions to Answer Before Starting
1. GlobalLogistics' Fleet Management Platform has a 7-day RPO (weekly backup). Is this acceptable for a 24/7 logistics company? What does 7 days of data loss mean in practice?
2. If GlobalLogistics loses the Order Management System for 4 hours (4 × £85K/hr), what is the financial impact?
3. The temperature monitoring system tracks pharmaceutical shipments. If it goes offline for 8 hours, what regulatory body might investigate?
4. What is the minimum viable operation GlobalLogistics could maintain if the OMS was offline?
5. Why must the RTO be less than the MTD?

---

## Deliverables

### Deliverable 1: BIA Methodology Document

**What It Is:** A document explaining how the BIA was conducted — scope, data collection approach, scoring methodology, and definitions.

**Must include:**
- BIA scope: Which business processes are in scope
- Data collection approach: How information was gathered (stakeholder interviews, system documentation review, workshops)
- Impact categories and scoring: Define each impact category and how impact is scored at each time interval
- Recovery metrics definitions: RTO, RPO, MTD, MBCO — definitions with examples specific to GlobalLogistics
- Priority classification: How processes are classified as Critical, High, Medium, Low
- ISO 22301 reference: How this BIA meets the Clause 8.2 requirements

---

### Deliverable 2: BIA Data Collection Questionnaire

**What It Is:** The structured questionnaire used to collect BIA data from each business process owner.

**Questionnaire sections:**

1. **Process Overview**: Process name, business unit, process owner, brief description, typical volume (daily/weekly)

2. **Dependency Mapping**: IT systems required, personnel required (minimum to operate), facilities required, third-party services required, data inputs required

3. **Impact Assessment over time**: For each time interval (0–4hr, 4–8hr, 8–24hr, 24–48hr, 48–72hr, 72hr–1wk), rate impact 1–5 across:
   - Financial: What revenue loss or cost occurs?
   - Operational: What service degradation occurs?
   - Regulatory: Are any reporting or SLA obligations breached?
   - Reputational: What customer or media impact?
   - Legal: Any contractual penalties?

4. **Recovery Requirements**: Maximum Tolerable Downtime, target RTO, data sensitivity and RPO requirement, minimum staff needed to resume operations (MBCO)

5. **Workaround Procedures**: Can the process operate manually? For how long? At what capacity?

6. **Current Recovery Arrangements**: Existing backups, DR environment (if any), documented recovery procedures (if any)

---

### Deliverable 3: Completed BIA for 8 Business Processes

**What It Is:** The completed BIA data for each of GlobalLogistics' 8 identified critical processes.

**Create a structured spreadsheet with one sheet per process, covering:**
- Process description and normal operating volume
- System and resource dependencies
- Impact assessment table (6 time intervals × 5 impact categories = 30 scored cells per process)
- Accumulated impact score over time (shows the "pain curve" as downtime extends)
- MTD determination (the point at which impact becomes mission-threatening)
- RTO recommendation
- RPO requirement
- MBCO definition (minimum viable operation level)
- Current gap: Current backup/DR capability vs required RPO and RTO

**Process-specific BIA guidance:**

**Process 1: Customer Order Management (OMS)**
- Volume: 45,000 shipments/day
- Financial impact: £85,000/hour revenue loss + £15,000/hour penalty exposure
- MTD: 4 hours (after 4 hours, major retailers activate penalty clauses)
- Recommended RTO: 2 hours | RPO: 15 minutes
- Current state: 24-hour RPO, no DR → CRITICAL GAP

**Process 2: Fleet Management Platform**
- 2,400 vehicles; if offline, vehicles cannot be dispatched efficiently
- Financial: £40,000/hour operational cost + delivery delays
- MTD: 6 hours (manual dispatch feasible short-term)
- Recommended RTO: 4 hours | RPO: 1 hour
- Current state: 7-day RPO → CRITICAL GAP

**Process 3: Temperature Monitoring (Pharmaceutical)**
- MHRA requires continuous temperature records for pharmaceutical shipments
- If offline, all pharmaceutical shipments must halt (regulatory requirement)
- Financial: £120,000/hour (pharmaceutical shipments highest-value)
- MTD: 2 hours (regulatory requirement to halt if monitoring fails)
- Recommended RTO: 30 minutes | RPO: 5 minutes
- Current state: 15-minute snapshots → RPO acceptable; no tested recovery plan → GAP

**Processes 4–8:** Complete the BIA for Finance System, WMS, HR System, Communication Platform, Customer Portal — use the scenario data to determine realistic impacts and recovery targets.

---

### Deliverable 4: RTO / RPO / MTD / MBCO Summary Table

**What It Is:** A single-page executive summary table showing all 8 processes with their recovery metrics.

| Process | Criticality | MTD | Recommended RTO | Recommended RPO | MBCO | Current RPO | Current RTO | Gap? |
|---------|-------------|-----|-----------------|-----------------|------|-------------|-------------|------|
| Order Management | Critical | 4hr | 2hr | 15min | 30% of volume via manual process | 24hr | No DR | YES — Critical |
| Fleet Management | Critical | 6hr | 4hr | 1hr | Manual dispatch for <200 vehicles | 7 days | No DR | YES — Critical |
| Temp Monitoring | Critical | 2hr | 30min | 5min | Minimum viable monitoring for pharma | 15min | Unknown | PARTIAL — needs test |
[Continue for all 8 processes]

**Below the table**: A prioritised recovery sequence — the order in which processes should be recovered in a disaster. (Temp Monitoring first due to 2hr MTD, then OMS, then Fleet.)

---

### Deliverable 5: Business Continuity Strategy Options

**What It Is:** A document presenting 3 strategy options for achieving the recommended RTOs and RPOs, with cost estimates for each.

**For each option:**
- Strategy name and description
- Which processes it covers
- Technical approach (e.g., Active-Active AWS architecture, warm standby DR site, cold standby)
- Estimated one-time implementation cost
- Estimated annual recurring cost
- RPO/RTO achievable under this strategy
- Advantages and disadvantages

**Minimum 3 options:**
1. **Minimal DR (Quick Win)** — Improve backup frequency for highest-priority systems; implement pilot DR environment for OMS only. Cost: ~£150K. Partial risk reduction.
2. **Full Cloud DR** — Implement AWS active-passive DR for all cloud-hosted systems; migrate Fleet Management to cloud. Cost: ~£450K. Achieves most RTOs.
3. **Full Active-Active** — Multi-region AWS deployment; real-time replication. Cost: ~£1.2M. Meets all RTOs including 30-minute temp monitoring target.

**Recommendation**: Recommend Option 2 with a phased approach — Option 1 immediately (30-day quick wins), full Option 2 within 12 months.

---

### Deliverable 6: BIA Executive Summary (2 pages)

**What It Is:** A board-ready 2-page summary of the BIA findings for Kevin Obi (CEO) to present to the board.

Write in business language: no acronyms without explanation. Focus on: £ impact of current gaps, investment required, risk of inaction.

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| BIA Completeness | 30% | All 8 processes completed; all metrics defined |
| RTO/RPO/MTD Accuracy | 30% | Metrics correctly defined and justified; RTO < MTD for all processes |
| Strategy Options | 20% | 3 realistic options with cost estimates |
| Professional Quality | 20% | Executive summary board-ready; BIA report audit-ready |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **ISO 22301:2019 Clause 8.2** | BIA methodology and requirements |
| **ISO 27001:2022 A.5.29** | Information security during disruption |
| **ISO 27001:2022 A.5.30** | ICT readiness for business continuity |

---

## Week-Specific Resources

- [ISO 22301:2019 Overview — iso.org](https://www.iso.org/standard/75106.html) — BCMS standard
- [BCI Good Practice Guidelines — BIA Chapter](https://www.thebci.org/knowledge/good-practice-guidelines.html) — Free from BCI
- [CISA: Business Continuity Planning](https://www.cisa.gov/business-continuity-planning) — US guidance with BIA methodology
- [NCSC: Incident Management Guidance](https://www.ncsc.gov.uk/guidance/incident-management) — UK BC guidance
- [AWS Disaster Recovery Guide](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-workloads-on-aws.html) — Technical DR options (relevant to strategy options)
- [MHRA: Cold Chain Management](https://www.gov.uk/guidance/good-distribution-practice) — Pharmaceutical temperature monitoring context

---

## Submission

```
Week-13/Deliverables/
├── GlobalLogistics-BIA-Methodology-v1.0.md
├── GlobalLogistics-BIA-Data-Collection-Questionnaire-v1.0.xlsx
├── GlobalLogistics-BIA-Completed-8-Processes-v1.0.xlsx
├── GlobalLogistics-RTO-RPO-MTD-Summary-Table-v1.0.xlsx
├── GlobalLogistics-BC-Strategy-Options-v1.0.md
└── GlobalLogistics-BIA-Executive-Summary-v1.0.md
```
