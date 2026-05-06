# Week 13 Learning Guide: Business Impact Analysis

## What You Will Learn This Week

When a cyberattack, system failure, or disaster strikes, the organisation's survival depends on how well it planned for recovery. Business Impact Analysis (BIA) is the analytical foundation of business continuity — it determines which processes are most critical, how long the business can survive without them, and what recovery targets must be met. This week you learn to conduct a professional BIA, define recovery metrics (RTO, RPO, MTD, MBCO), and produce the business continuity strategy inputs that protect organisations from catastrophic disruption.

---

## Section 1: Core Concept Explained

### What Is a Business Impact Analysis?

A Business Impact Analysis (BIA) is a systematic process for identifying and evaluating the potential effects of an interruption to critical business processes. It quantifies the consequences of disruption over time — starting at the moment of failure and progressing through hours, days, and weeks of downtime.

The BIA answers 4 critical questions for each business process:
1. **What would happen** if this process were unavailable for 1 hour? 1 day? 1 week?
2. **How much loss** (financial, operational, reputational, regulatory) would accumulate over time?
3. **How quickly must this process be recovered** (RTO — Recovery Time Objective)?
4. **How much data loss is acceptable** (RPO — Recovery Point Objective)?

**ISO 22301:2019** is the international standard for Business Continuity Management Systems (BCMS). It is to business continuity what ISO 27001 is to information security — a requirements-based standard that organisations can be certified against. ISO 22301 Clause 8.2 explicitly requires a BIA as part of the BCMS.

The BIA is the input to the business continuity strategy. Without a BIA, business continuity planning is guesswork — you don't know which systems to protect most, which processes to recover first, or what your recovery infrastructure must be capable of.

### Key Terminology

| Term | Full Name | Definition | Example |
|------|-----------|------------|---------|
| **RTO** | Recovery Time Objective | Maximum acceptable time to restore a process | "Payment processing: RTO = 2 hours" |
| **RPO** | Recovery Point Objective | Maximum acceptable data loss (time between backup and failure) | "Database: RPO = 15 minutes" |
| **MTD** | Maximum Tolerable Downtime | Maximum time the organisation can survive without the process before business failure | "Payroll processing: MTD = 5 days" |
| **MBCO** | Minimum Business Continuity Objective | Minimum level of service needed to satisfy business obligations during disruption | "Process 50% of orders with manual workaround" |
| **BIA** | Business Impact Analysis | The assessment process itself | Conducted annually or when significant changes occur |
| **Critical Process** | A process whose failure has severe impact | Payment processing, customer authentication |
| **Dependency** | What a process relies on | "Order processing depends on the ERP system and internet connectivity" |
| **Workaround** | Manual or alternative method during recovery | "Process orders via phone during system outage" |
| **BCMS** | Business Continuity Management System | ISO 22301 management system framework | "GlobalLogistics' BCMS covers 8 critical processes" |
| **Impact Category** | Types of impact assessed | Financial, Operational, Reputational, Regulatory, Legal, Health & Safety |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Real-World BIA Process

1. **Scope the BIA** — Identify which business units and processes are in scope. For a large organisation, scope all business units; for a focused BIA, scope only the highest-risk areas.

2. **Build the business process inventory** — Identify all significant business processes. Not individual tasks — processes. "Process customer orders" is a process. "Click 'Submit' on the order form" is a task.

3. **Conduct BIA workshops** — Meet with business unit leaders and process owners. Use a structured questionnaire to capture: what does this process do? What does it depend on? What happens if it fails?

4. **Assess impacts over time** — For each process, assess the impact at defined time intervals: 0–4 hours, 4–8 hours, 8–24 hours, 24–48 hours, 48–72 hours, 72–168 hours (1 week). Impact categories: Financial (£ loss per hour), Operational (degraded service levels), Reputational (customer complaints, NPS), Regulatory (SLA breaches, regulatory reporting failures), Legal (contractual penalties).

5. **Determine MTD** — The point at which the accumulated impact becomes "mission-threatening" or "business failure" level.

6. **Determine RTO** — The RTO must always be less than the MTD. If the business can't survive more than 4 hours without payment processing, the RTO for payment processing must be less than 4 hours.

7. **Determine RPO** — Based on data criticality and backup infrastructure. For financial transaction systems, RPO is often near-zero (real-time replication). For less critical data, RPO might be 24 hours.

8. **Determine MBCO** — What minimum service level must be maintained? Some processes can operate in a degraded mode (manual workaround, reduced throughput) while full recovery occurs.

9. **Rank processes by criticality** — Produce a priority ranking for recovery. The process with the lowest RTO is recovered first.

10. **Document findings** — Produce a formal BIA report with methodology, findings, process priority ranking, and recovery target recommendations.

---

## Section 3: Framework Deep Dive

### ISO 22301:2019 — Business Continuity Management Systems

**Clause 8.2 — Business Impact Analysis and Risk Assessment:**
- 8.2.1: Business impact analysis — determine and document critical processes, their dependencies, recovery requirements (RTO, RPO, MBCO), and required resources
- 8.2.2: Risk assessment — identify threats to critical processes; assess likelihood and impact

**Key ISO 22301 concepts:**
- The BIA informs the **Business Continuity Strategy** (how to achieve RTOs and RPOs)
- The Strategy informs **Business Continuity Plans** (the actual procedures followed during disruption)
- Plans are **tested** through exercises (tabletop, walkthrough, simulation, full-scale)
- The BCMS is **reviewed** and **improved** continuously

### Impact Assessment Framework

| Impact Category | Example Metrics |
|-----------------|----------------|
| **Financial** | Revenue loss per hour, cost of manual workaround, regulatory fine if SLA breached |
| **Operational** | % of service degraded, number of customer transactions affected per hour |
| **Reputational** | Social media mentions, press coverage risk, Net Promoter Score impact |
| **Regulatory** | SLA compliance breach (FCA, Ofcom), reporting obligation missed |
| **Legal** | Contractual penalty per hour (SLA), litigation risk |
| **Health & Safety** | Risk to life (relevant for manufacturing, healthcare, infrastructure) |

---

## Section 4: Common Mistakes Beginners Make

1. **Confusing RTO with RPO.** RTO = how long to recover the system. RPO = how much data loss is acceptable. These are independent. A system might have a short RTO (2 hours) but a longer RPO (24 hours — daily backup) if the data changes slowly.

2. **Setting RTO greater than MTD.** This is a fatal error. If the business can only survive 4 hours without the process (MTD = 4hr) but the recovery target is 8 hours (RTO = 8hr), the business will fail before recovery completes. RTO must always be < MTD.

3. **Treating all processes as equally critical.** Not everything is critical. A BIA that rates every process as "Critical with 0-hour RTO" provides no useful prioritisation for recovery planning.

4. **Conducting the BIA in isolation without business unit input.** IT cannot determine business impact without talking to business owners. The IT team knows how long it takes to restore systems; business owners know how much revenue is lost per hour.

5. **Not updating the BIA when the business changes.** A BIA from 3 years ago is often dangerously out of date. New products, new systems, new customer obligations — all change the business impact profile.

6. **Confusing the BIA with a risk assessment.** They are related but different. The BIA focuses on impact (consequences of disruption). The risk assessment focuses on probability and threat. Both are inputs to business continuity planning.

7. **Building BCPs without conducting a BIA first.** The BIA determines which processes need BCPs and what the recovery targets are. BCPs without BIA inputs are typically wrong priorities.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Use structured BIA questionnaires** — send questionnaires to business unit leaders 2 weeks before BIA workshops; workshops then validate and fill gaps rather than starting from scratch.
- **Quantify financial impacts where possible** — "£X revenue loss per hour" is far more compelling to a board than "significant operational disruption."
- **RTO must be technically achievable** — validate RTOs with IT/infrastructure teams. A business may want a 1-hour RTO but the backup restore process takes 4 hours. The gap must be addressed in the strategy.
- **The MTD is your planning horizon** — everything in the BCP must be designed to restore the process within the MTD.
- **Consider dependencies carefully** — if Process A depends on System B, Process A's RTO cannot be shorter than System B's recovery time.
- **Run BIA workshops, not just questionnaires** — workshops surface the dependencies and impacts that questionnaires miss because participants don't know what information is important.
- **The BIA is an annual exercise** — schedule it every year and whenever significant changes occur (new products, system changes, mergers, regulatory changes).

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [ISO 22301:2019 Overview](https://www.iso.org/standard/75106.html) — BCMS standard overview
- [BCI: Good Practice Guidelines](https://www.thebci.org/knowledge/good-practice-guidelines.html) — Free BCI BIA guidance
- [NCSC: Incident Management and Business Continuity](https://www.ncsc.gov.uk/guidance/incident-management) — UK government BC guidance
- [CISA: Business Continuity Planning](https://www.cisa.gov/business-continuity-planning) — US guidance with BIA methodology
- [BSI: Business Continuity Management](https://www.bsigroup.com/en-GB/ISO-22301-Business-Continuity/) — ISO 22301 resources
- [ISO 22317: BIA Guidelines](https://www.iso.org/standard/50066.html) — Specific BIA standard

### Books

- *Business Continuity Management* by Andrew Hiles — Comprehensive BC reference
- *Effective Business Continuity Management* by Michael Gallagher — Practical BIA methodology
- *ISO 22301:2019 — A Pocket Guide* by Alan Calder — Concise implementation guide

### Online Courses

- [BCI: Certificate of the BCI (CBCI)](https://www.thebci.org/training-qualifications/cbci.html) — Entry-level BC certification
- [ISACA: Business Continuity](https://www.isaca.org/resources/business-continuity) — BC resources
- [Coursera: Business Continuity Management](https://www.coursera.org/learn/business-continuity-management) — Foundational BC course

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (90 min)

- 20 min: BIA concepts — RTO, RPO, MTD, MBCO explained with real examples; common confusions resolved
- 20 min: Impact assessment exercise — for a fictional e-commerce company, assess financial impact at 0, 4, 24, 72 hours of downtime
- 20 min: BIA questionnaire walkthrough — review a BIA questionnaire template and practice completing it for one process
- 15 min: Dependency mapping exercise — map dependencies for "process online orders" together
- 15 min: Introduce GlobalLogistics scenario; discuss what makes a 24/7 logistics platform particularly high-stakes

### Session B Focus (60 min)

- Review BIA: Are impacts quantified (£ values)? Are RTOs less than MTDs? Are dependencies captured?
- Check process prioritisation: Does the priority ranking make business sense?
- Ask: "GlobalLogistics' order management system has an RTO of 4 hours but their backup restore takes 6 hours. What do you recommend?"

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "What is a Business Impact Analysis and when is one required?"
2. "What is the difference between RTO and RPO?"
3. "What does MTD mean and how does it relate to RTO?"
4. "What is MBCO?"
5. "Walk me through how you would conduct a BIA."
6. "What ISO standard governs business continuity?"
7. "What impact categories should a BIA assess?"
8. "How do dependencies affect recovery time objectives?"
9. "How often should a BIA be updated?"
10. "What is the relationship between the BIA and the Business Continuity Plan?"

### Keywords to Use

- RTO — Recovery Time Objective (must be < MTD)
- RPO — Recovery Point Objective
- MTD — Maximum Tolerable Downtime
- MBCO — Minimum Business Continuity Objective
- ISO 22301 — BCMS standard
- Dependency mapping
- Impact categories (Financial, Operational, Reputational, Regulatory)
- Business process criticality ranking
- Business continuity strategy
- Annual BIA review cycle
