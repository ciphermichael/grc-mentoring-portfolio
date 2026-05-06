# Business Impact Analysis (BIA) Template

| Field | Value |
|-------|-------|
| **Document ID** | BIA-001 |
| **Organisation** | [Company Name] |
| **Version** | 1.0 |
| **Assessment Date** | DD-MMM-YYYY |
| **BIA Lead** | [Name / Role] |
| **Reviewed By** | [Name / Role] |
| **Classification** | Confidential — Internal |
| **Framework Refs** | ISO 22301:2019 Clause 8.2 | ISO 27001:2022 A.5.29, A.5.30 |

---

## Purpose

This Business Impact Analysis (BIA) identifies critical business processes, assesses the impact of their disruption over time, and defines recovery objectives. Results inform the Business Continuity Strategy, Business Continuity Plans, and IT Disaster Recovery Plans.

---

## Key Definitions

| Metric | Definition | Example |
|--------|------------|---------|
| **RTO** | Recovery Time Objective — the maximum acceptable time to restore a process or system following disruption | Order Management: RTO = 2 hours |
| **RPO** | Recovery Point Objective — the maximum acceptable amount of data loss measured in time | Database: RPO = 15 minutes (last backup to failure) |
| **MTD** | Maximum Tolerable Downtime — the maximum period the organisation can survive without the process before business failure | Payment processing: MTD = 4 hours |
| **MBCO** | Minimum Business Continuity Objective — the minimum level of service required during disruption | Process 30% of orders manually during outage |
| **RTO < MTD** | Recovery must always be achievable before the business fails — **RTO must always be less than MTD** | If MTD = 4hr, RTO must be ≤ 3hr |

---

## Impact Severity Scale

### Financial Impact

| Level | Rating | Financial Loss |
|-------|--------|---------------|
| 1 | Negligible | < £1,000 |
| 2 | Minor | £1,000 – £10,000 |
| 3 | Moderate | £10,000 – £100,000 |
| 4 | Major | £100,000 – £1,000,000 |
| 5 | Catastrophic | > £1,000,000 |

### Operational Impact

| Level | Rating | Service Impact |
|-------|--------|---------------|
| 1 | Negligible | Minor degradation; workaround available |
| 2 | Minor | Noticeable degradation; most services available |
| 3 | Moderate | Significant degradation; key services unavailable |
| 4 | Major | Critical services unavailable |
| 5 | Catastrophic | Complete service failure; business operations halted |

---

## Process Impact Escalation Table

*For each time interval, rate the combined impact (1–5) across all impact categories*

| Impact Category | 0–4 Hours | 4–8 Hours | 8–24 Hours | 24–48 Hours | 48–72 Hours | 72hr–1 Week |
|----------------|-----------|-----------|------------|-------------|-------------|-------------|
| Financial | | | | | | |
| Operational | | | | | | |
| Regulatory | | | | | | |
| Reputational | | | | | | |
| Legal/Contractual | | | | | | |
| **Overall Score** | | | | | | |

---

## Business Process BIA

### Process 1: Customer Order Management

**Process Overview:**
| Field | Detail |
|-------|--------|
| Process Name | Customer Order Management |
| Process Owner | Head of Operations |
| Business Unit | Operations |
| Process Description | Manages end-to-end customer order processing from receipt to fulfilment confirmation |
| Daily Transaction Volume | 2,500 orders/day; £850,000 daily revenue |
| Operating Hours | 24/7 |
| Process Criticality | Critical |

**Dependencies:**
| Dependency Type | Dependency | If Unavailable? |
|----------------|-----------|----------------|
| IT Systems | Order Management System (OMS), Customer Database, Payment Gateway | Orders cannot be processed |
| Personnel | Operations Team (minimum: 3 staff) | Manual order processing at 15% capacity |
| Facilities | Operations Centre (Birmingham) | Can partially operate remotely |
| Third Parties | Payment Processor (CloudPay), Courier API | Cannot fulfil orders without both |
| Data Inputs | Customer master data, product catalogue, inventory levels | Cannot validate or process orders |

**Impact Assessment:**

| Impact Category | 0–4 Hours | 4–8 Hours | 8–24 Hours | 24–48 Hours | 72hr–1 Week |
|----------------|-----------|-----------|------------|-------------|-------------|
| Financial (£/hour) | £35,000 | £35,000 | £35,000 | £35,000 + penalties | £35,000 + SLA breach + £50K/day penalties |
| Financial Score (1–5) | 3 | 3 | 4 | 5 | 5 |
| Operational Score (1–5) | 3 | 4 | 5 | 5 | 5 |
| Regulatory Score (1–5) | 1 | 2 | 3 | 4 | 5 |
| Reputational Score (1–5) | 1 | 2 | 3 | 4 | 5 |
| Legal/Contractual (1–5) | 1 | 2 | 3 | 5 | 5 |
| **Overall Score** | **2** | **3** | **4** | **5** | **5** |

**Recovery Metrics:**
| Metric | Value | Basis |
|--------|-------|-------|
| **MTD** | 4 hours | SLA breach triggers at 4hr; customer contracts include penalty clauses |
| **RTO** | 2 hours | Must recover before MTD; 2hr allows time for validation |
| **RPO** | 15 minutes | Maximum acceptable transaction data loss based on revenue at £35,000/hour |
| **MBCO** | 30% of normal order volume via manual process | Minimum to prevent contract breach |

**Current Recovery Capability:**
| Item | Current State | Gap vs Target |
|------|--------------|---------------|
| Backup | Daily backup to S3 (24-hour RPO) | RPO GAP — 15 min required vs 24hr available |
| DR Environment | None | RTO GAP — no failover; restoration from backup takes est. 8hr |
| Workaround Procedure | Not documented | MBCO GAP — no documented manual process |

---

### Process 2: Payment Processing

**Process Overview:**
| Field | Detail |
|-------|--------|
| Process Name | Payment Processing |
| Process Owner | Head of Finance |
| Process Description | Processing customer payment card transactions via integrated payment gateway |
| Daily Volume | £850,000 in daily transactions |
| Criticality | Critical |

**Dependencies:** Payment Gateway (CloudPay API), Payment Server, Banking APIs, Card Scheme connectivity

**Impact Assessment:**

| Impact Category | 0–4 Hours | 4–8 Hours | 8–24 Hours |
|----------------|-----------|-----------|------------|
| Financial | £212,500/hr revenue halt | £212,500/hr | £212,500/hr |
| Regulatory | PCI-DSS breach of processing SLA | FCA operational resilience trigger | FCA formal notification required |
| Operational | Cannot accept new payments | Cannot accept payments; backlog builds | Major operational crisis |
| **Overall Score** | 4 | 5 | 5 |

**Recovery Metrics:**
| Metric | Value |
|--------|-------|
| **MTD** | 2 hours (FCA PS21/3 important business service) |
| **RTO** | 1 hour |
| **RPO** | 0 minutes (real-time replication required — no transaction loss acceptable) |
| **MBCO** | Accept payments via manual card imprint or alternative payment method |

---

### Process 3: Human Resources and Payroll

**Process Overview:**
| Field | Detail |
|-------|--------|
| Process Name | HR and Payroll Processing |
| Process Owner | Head of HR |
| Process Description | Employee data management; monthly payroll processing; HR record keeping |
| Criticality | High |

**Impact Assessment:**

| Impact Category | 0–4 Hours | 24 Hours | 5 Days |
|----------------|-----------|----------|--------|
| Financial | Minimal | Minimal | Payroll delay: staff morale/legal risk |
| Regulatory | None | None | Employment law if payroll missed |
| Operational | Minimal | Minimal | Major if payroll date affected |
| **Overall Score** | 1 | 1 | 4 |

**Recovery Metrics:**
| Metric | Value |
|--------|-------|
| **MTD** | 5 days (payroll deadline-driven) |
| **RTO** | 3 days |
| **RPO** | 24 hours (daily backup acceptable) |
| **MBCO** | Manual payroll calculations possible with 3 HR staff |

---

### Process 4: IT Infrastructure and Network Operations

**Process Overview:**
| Field | Detail |
|-------|--------|
| Process Name | Core IT Infrastructure |
| Process Owner | Head of IT |
| Process Description | Network, servers, storage, cloud infrastructure underpinning all business operations |
| Criticality | Critical (enabler for all other processes) |

**Recovery Metrics:**
| Metric | Value |
|--------|-------|
| **MTD** | Dependent on processes supported; overall 2 hours |
| **RTO** | 1 hour for core infrastructure |
| **RPO** | 15 minutes for production database systems |
| **MBCO** | Core network and key application servers available |

---

## BIA Summary — All Processes

| Process | Criticality | MTD | RTO | RPO | MBCO | Current RPO | Current RTO | Gap? |
|---------|-------------|-----|-----|-----|------|------------|------------|------|
| Customer Order Management | Critical | 4hr | 2hr | 15min | 30% volume via manual | 24hr | No DR (est. 8hr) | YES — Critical |
| Payment Processing | Critical | 2hr | 1hr | 0min | Manual card method | Real-time | No tested DR | YES — Critical |
| HR and Payroll | High | 5 days | 3 days | 24hr | Manual payroll calc | 24hr | 3 days restore | Acceptable |
| Core IT Infrastructure | Critical | 2hr | 1hr | 15min | Core network/servers | 15min (RDS) | No tested DR | YES — High |
| Customer Support | Medium | 24hr | 8hr | 24hr | Email-only support | 24hr | Cloud-based (low risk) | Acceptable |
| Finance and Accounting | High | 72hr | 48hr | 24hr | Manual transaction logging | 24hr | 48hr restore | Acceptable |

---

## Recovery Priority Ranking

Based on MTD analysis, the recovery sequence during a major disaster event:

1. **Payment Processing** (MTD: 2hr) — Restore first
2. **Core IT Infrastructure** (MTD: 2hr, enables all others) — Restore simultaneously
3. **Customer Order Management** (MTD: 4hr) — Restore third
4. **Finance/Accounting** (MTD: 72hr)
5. **HR/Payroll** (MTD: 5 days)
6. **Customer Support** (MTD: 24hr — note: earlier than Finance but less severe impact)

---

## Business Continuity Strategy Recommendations

Based on this BIA, the following investments are recommended to close critical gaps:

| Gap | Strategy Option | Estimated Cost | Expected Recovery Improvement |
|-----|----------------|---------------|------------------------------|
| OMS no DR | Warm standby DR environment (AWS second region) | £120K setup + £30K/yr | RTO: 8hr → 2hr; RPO: 24hr → 15min |
| Payment no DR | Active-active AWS multi-region deployment | £200K setup + £50K/yr | RTO: Unknown → 30min; RPO: 0min |
| Untested recovery | Annual DR test programme | £25K/yr | Validates all RTOs |

---

## BIA Review Schedule

This BIA must be reviewed:
- Annually as part of the business continuity management review
- When significant business changes occur (new products, systems, or markets)
- After any business disruption event
- When critical process dependencies change

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | YYYY-MM-DD | [Name] | Initial BIA |

---

*Business Impact Analysis Template | v1.0 | ISO 22301:2019 Clause 8.2 | ISO 27001:2022 A.5.29, A.5.30*
