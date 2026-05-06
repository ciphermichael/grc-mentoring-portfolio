# Week 15 Assignment: Security Metrics and Executive Reporting

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | TechCorp |
| **Your Role** | GRC Analyst |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟🌟 |
| **Frameworks** | ISO 27001 (Clause 9.1), NIST CSF 2.0, CIS Controls v8 |

---

## Scenario Brief — Read This Carefully

**TechCorp** is a 1,200-person UK technology services company providing managed IT services to 85 corporate clients across financial services, healthcare, and retail sectors. They have an annual security budget of £2.8M. Their CISO, Dr. James Nkosi, was appointed 4 months ago from a FTSE 100 company.

Dr. Nkosi's primary mandate from the CEO is to "professionalise security reporting" — the previous security updates to the board were ad hoc, technical, and provided no basis for decision-making. The CEO, Sarah Williams, has explicitly asked for: "One page every quarter that tells me whether security is getting better or worse, and what we need to invest in."

The CFO has separately asked the CISO: "Can you quantify the return on our security investment? How do we know the £2.8M is having an impact?"

**Current security data you have been given:**

- Patch compliance rate (Q1): 78% | (Q2): 82% | (Q3): 86% | Target: ≥ 95% [Amber — improving]
- Mean Time to Detect (MTTD): Q1: 19.3hr | Q2: 14.2hr | Q3: 11.8hr | Target: < 8hr [Amber — improving]
- Phishing simulation failure rate: Q1: 28% | Q2: 19% | Q3: 14% | Target: < 10% [Amber — improving]
- Open critical vulnerabilities >90 days: Q1: 34 | Q2: 21 | Q3: 12 | Target: 0 [Amber — improving]
- Security awareness training completion: Q1: 88% | Q2: 91% | Q3: 94% | Target: ≥ 95% [Amber — near target]
- Policy review compliance (within review date): Q3: 76% | Target: 100% [Red — no improvement trend data]
- Vendor assessments completed (Tier 1, annual): 18 of 25 = 72% | Target: 100% [Red]
- ISO 27001 gap closure rate: Q1: 8 gaps | Q2: 6 gaps | Q3: 9 gaps closed | Total remaining: 41 gaps [Amber]
- Security incidents this quarter: P1=0, P2=2, P3=8, P4=19 | Q3 MTTR average: 6.8 hours [Green — P1=0]
- Penetration test: Last conducted: 18 months ago | Target: Annual [Red — overdue]

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 15 — KPI/KRI definitions and dashboard design principles
- [ ] Read ISO 27001:2022 Clause 9.1 (monitoring and measurement requirements)
- [ ] Study one example security dashboard (search "CISO security dashboard template" for visual inspiration)
- [ ] Understand what questions a board member would ask when viewing this data

### Questions to Answer Before Starting
1. Looking at TechCorp's data, which metrics are most concerning to you and why?
2. Phishing failure rate has dropped from 28% to 14% — how would you communicate this improvement to the board in one sentence?
3. The penetration test is 18 months overdue. What business risk does this create? How do you explain this to the CFO?
4. What is the difference between MTTD and MTTR?
5. The CEO wants to know if security is getting better or worse. Based on the data, what would you say?

---

## Deliverables

### Deliverable 1: Executive Risk Dashboard (RAG Status)

**What It Is:** A professional one-page dashboard showing TechCorp's 10 security KPIs with RAG status, trends, and summary narrative. This is the dashboard Dr. Nkosi presents to the board quarterly.

**Step-by-Step Instructions:**

1. Create a visual dashboard (Excel, Google Sheets, or PowerPoint) with:
   - Dashboard title: TechCorp | Q3 2025 Security Metrics Dashboard | Prepared by: [Your Name] | Classification: Confidential
   - 10 metric rows, each showing: Metric Name | Q1 | Q2 | Q3 | Target | RAG | Trend Arrow (↑↓→)

2. Apply RAG thresholds:
   - Patch Compliance: Green ≥ 95%, Amber 85–94%, Red < 85%
   - MTTD: Green < 8hr, Amber 8–24hr, Red > 24hr
   - Phishing Failure: Green < 10%, Amber 10–20%, Red > 20%
   - Open Critical Vulns: Green = 0, Amber 1–10, Red > 10
   - Training Completion: Green ≥ 95%, Amber 85–94%, Red < 85%
   - Policy Review: Green 100%, Amber 90–99%, Red < 90%
   - Vendor Assessments: Green 100%, Amber 80–99%, Red < 80%
   - ISO 27001 Gaps: Green ≥ 8 closed/quarter, Amber 4–7, Red < 4
   - Incidents P1 count: Green = 0, Amber = 1, Red ≥ 2
   - Pen Test: Green = within 12 months, Red = overdue

3. Apply correct RAG to each Q3 metric using the data provided.

4. Add trend arrows: ↑ (improving), ↓ (declining), → (stable)

5. Overall RAG Summary: Total Green/Amber/Red count; overall programme RAG

6. Dashboard narrative (max 150 words): "Q3 2025 shows continued improvement across 7 of 10 metrics. Key areas of concern are [X] and [Y]. The positive trend in [phishing / MTTD] demonstrates the impact of [training programme / SIEM investment]. Recommended actions for Q4: [2–3 specific actions]."

**Quality Bar:** Dashboard is visually clear; RAG correctly applied; trend arrows accurately reflect direction; narrative is written for a non-technical board member.

---

### Deliverable 2: 10 Cybersecurity KPIs with Targets and Baselines

**What It Is:** A formal KPI definition document establishing TechCorp's 10 security metrics, including precise definitions, data sources, and thresholds.

**For each KPI, document:**
- KPI Name
- Definition (exactly what is measured)
- Measurement formula (e.g., "Number of critical patches applied within 48 hours ÷ Total critical patches released × 100")
- Data Source (which system/team produces this data)
- Measurement frequency
- Baseline (starting value or Q1 value)
- Target value
- Green/Amber/Red thresholds
- Responsible owner (who is accountable for this metric)
- Why this metric matters (1 sentence linking to business risk)

Complete for all 10 metrics using the TechCorp data.

---

### Deliverable 3: Risk Trend Analysis (3-Quarter)

**What It Is:** A 2-page trend analysis report covering TechCorp's security performance across Q1–Q3, identifying patterns, improvements, and concerns.

**Structure:**
1. **Overall Trend Summary**: Is TechCorp's security posture improving, stable, or deteriorating? Support with data.
2. **Positive Trends**: Which metrics are improving and why? Link to specific investments or programme changes.
   - Phishing failure rate: 28% → 14% — likely impact of security awareness training programme
   - MTTD: 19.3hr → 11.8hr — likely impact of SIEM implementation
3. **Concerning Trends / Static Metrics**: Which metrics are not improving? Root cause analysis.
   - Policy review: No trend data; still Red at 76%
   - Pen test: Overdue; no recent data point
4. **Investments Made vs Outcomes**: What was invested in Q1–Q3 (training programme, SIEM)? What metrics improved as a result?
5. **Q4 Predictions**: If current trends continue, where will each metric be by Q4? Which will be Green?

---

### Deliverable 4: Compliance Posture Summary

**What It Is:** A 1-page summary of TechCorp's current compliance posture across their active compliance programmes.

**Include:**
- ISO 27001 gap closure progress: 41 gaps remaining; at 8 gaps/quarter, certification in 5 quarters
- Policy review compliance: 76% — which policies are overdue? (Identify top 3 by risk)
- Vendor assessment status: 7 of 25 Tier 1 vendors unassessed — name them if possible (use fictional names)
- Penetration test: 18 months overdue — risk statement
- SOC 2 status (if applicable): Not applicable currently — TechCorp does not have SOC 2 in scope
- Regulatory status: No open regulatory investigations; no ICO complaints this quarter

---

### Deliverable 5: Board Briefing Pack (5 Slides)

**What It Is:** A 5-slide PowerPoint presentation for Dr. Nkosi to present to TechCorp's board at the quarterly security update.

**Slide 1 — Security Posture at a Glance**
The 10-KPI dashboard on one slide. Overall RAG. "Is security improving?"

**Slide 2 — Key Risks**
Top 3 risks requiring board attention:
1. Penetration test overdue (18 months) — what's the risk; what's the plan; cost to remediate
2. Open critical vulnerabilities (12 remaining >90 days) — what's the risk; timeline to Zero
3. 7 Tier 1 vendors unassessed — what's the risk; 90-day assessment plan

**Slide 3 — Programme Progress and ROI**
Show the improvement story: 6 metrics improving. Investment made (training, SIEM). Outcomes (phishing drop, MTTD improvement). "Our £2.8M security investment is delivering measurable improvement."

**Slide 4 — ISO 27001 Certification Roadmap**
Progress toward certification: gaps remaining, rate of closure, projected certification date.

**Slide 5 — Q4 Priorities and Investment Requests**
What will the security team focus on in Q4?
- Complete Tier 1 vendor assessments (no additional budget required)
- Conduct penetration test (£35,000 cost — request board approval)
- Policy review catch-up programme (10 policies to review in Q4)
Budget request: £35,000 for pen test.

---

### Deliverable 6: Narrative Executive Report (3 pages)

**What It Is:** A written executive risk report (the complement to the slide deck) for TechCorp's CISO to distribute to board members in advance of the quarterly board meeting.

**Structure:**
1. Executive Summary (half page): Overall security posture, headline metrics, top 3 risks, budget ask
2. Security Performance Review (1 page): Narrative covering all 10 KPIs with trend context
3. Compliance Status (half page): ISO 27001, policies, vendors, pen test
4. Risk Section (half page): 3 current risks with business impact statements in £ terms
5. Q4 Plan and Investment Request (half page): What happens next; what budget is needed

**Tone:** Written for a board that is engaged but not technical. No acronyms without explanation. Focus on business risk and business impact.

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Dashboard Quality | 25% | RAG correct; visually clear; trend arrows accurate |
| KPI Definitions | 20% | All 10 defined with data sources, thresholds, owners |
| Trend Analysis | 20% | Patterns identified; improvement linked to investment |
| Board Materials | 35% | Slides and report are board-ready; business language; "so what" explained |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **ISO 27001:2022 Clause 9.1** | Monitoring and measurement requirements |
| **NIST CSF 2.0 — GOVERN.OV** | Oversight — results reviewed and used to inform strategy |
| **CIS Controls v8** | Metrics framework for specific controls |

---

## Week-Specific Resources

- [NIST IR 8286 — Cybersecurity Measures](https://nvlpubs.nist.gov/nistpubs/ir/2021/NIST.IR.8286.pdf) — Metrics framework
- [NCSC Board Toolkit — Security Metrics](https://www.ncsc.gov.uk/collection/board-toolkit) — What boards need to see
- [CISA: Cyber Performance Goals](https://www.cisa.gov/cross-sector-cybersecurity-performance-goals) — CPG metrics framework
- [Security Metrics by Andrew Jaquith](https://www.pearson.com/en-gb/subject-catalog/p/security-metrics/P200000009568) — The definitive book on security measurement
- [CIS Controls v8 — Metrics per Control](https://www.cisecurity.org/controls/v8) — Control-specific measurement
- [ISO 27001:2022 Clause 9.1 Explained — Advisera](https://advisera.com/27001academy/blog/2022/06/27/how-to-monitor-measure-analyse-evaluate-your-isms/) — Performance evaluation guidance

---

## Submission

```
Week-15/Deliverables/
├── TechCorp-Security-Dashboard-Q3-2025-v1.0.xlsx
├── TechCorp-KPI-Framework-v1.0.xlsx
├── TechCorp-Risk-Trend-Analysis-Q1-Q3-2025-v1.0.md
├── TechCorp-Compliance-Posture-Summary-Q3-2025-v1.0.md
├── TechCorp-Board-Briefing-Pack-Q3-2025-v1.0.pptx
└── TechCorp-Executive-Risk-Report-Q3-2025-v1.0.md
```
