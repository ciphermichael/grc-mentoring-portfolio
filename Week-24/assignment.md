# Week 24 Assignment: Capstone — Metrics Dashboard & Final Presentation

## Capstone Overview

| Field | Detail |
|-------|--------|
| **Client** | NovaTech Corp |
| **Your Role** | Lead GRC Consultant |
| **Estimated Time** | 14–18 hours |
| **Difficulty** | 🌟🌟🌟🌟🌟 |
| **Frameworks** | ISO 27001:2022, NIST CSF 2.0, GDPR, PCI-DSS v4.0, CIS Controls v8 |

---

## Capstone Context

This is the final week of the programme. You will complete NovaTech's GRC programme with a comprehensive security metrics dashboard, executive reports, and a 30-minute board presentation. You will also polish your complete GitHub portfolio to job-market standard. This is the climax of 6 months of work — produce your best.

**Critical continuity requirements:**
- Dashboard KPIs must be consistent with metrics mentioned in Week 21 GRC Strategy
- Board presentation narrative must reference deliverables from all 4 capstone weeks
- Maturity assessment must show "before" state (Week 21 initial assessment) vs "after" (current programme state)
- Risks in the board pack must come from Week 22 risk register (top 5 risks with FAIR ALE values)

---

## Deliverable 1: Security Metrics Dashboard (12-Month KPIs)

**What It Is:** NovaTech's primary security operations dashboard tracking 12 KPIs across the programme period, presented in a board-ready format.

**Create two dashboard views:**

### View 1 — Security Operations Dashboard (Monthly to Management)

12 KPIs with 3-quarter trend data. For each KPI, fabricate realistic data showing the improvement expected over a 12-month programme:

| KPI | Q1 (Baseline) | Q2 | Q3 | Q4 (Target) | RAG | Trend |
|-----|--------------|----|----|-------------|-----|-------|
| Critical patch compliance rate | 62% | 74% | 88% | ≥95% | Amber ↑ |
| High patch compliance rate | 71% | 81% | 90% | ≥95% | Amber ↑ |
| Mean Time to Detect (MTTD) | 19.3hr | 14.7hr | 9.2hr | <8hr | Amber ↑ |
| Phishing simulation failure rate | 31% | 22% | 14% | <10% | Amber ↑ |
| Open Critical CVEs >90 days | 47 | 29 | 12 | 0 | Amber ↑ |
| Security awareness training completion | 67% | 78% | 91% | ≥95% | Amber ↑ |
| Tier 1 vendor assessments completed | 0 of 5 | 2 of 5 | 4 of 5 | 5 of 5 | Amber ↑ |
| Policy review compliance | 24% | 58% | 82% | 100% | Amber ↑ |
| P1 security incidents | 0 | 1 | 0 | 0 | Green (1 in Q2 recovered well) |
| ISO 27001 gap closure rate | — | 18 gaps closed | 34 gaps closed | ≥60 total | Amber ↑ |
| MTTD: Ransomware detection (SIEM) | N/A | N/A | 8.2hr (SIEM live Q3) | <4hr | Amber (new metric) |
| FCA findings remediated | 0 of 3 | 1 of 3 | 3 of 3 | 3 of 3 | Green ✓ |

**For each KPI define:**
- KPI Name
- Definition and measurement methodology
- Data source (Vanta, AWS Security Hub, SIEM, HR system, etc.)
- RAG thresholds (Green/Amber/Red specific values)
- Q1 baseline → Q4 current value → Target
- Responsible owner
- "So what?" narrative (1 sentence explaining the business significance)

**Overall Security Posture Indicator:** Calculate a weighted composite score. Give each KPI a weight (more strategic KPIs weighted higher). Current score vs target score. Present as a headline "security posture score."

### View 2 — Programme Progress Dashboard (Quarterly to Board)

5 strategic programme KPIs:

| Programme KPI | Status | Progress | Target |
|---------------|--------|----------|--------|
| ISO 27001 Certification | On track | Stage 1 complete; Stage 2 scheduled Month 11 | Certified by Month 12 |
| FCA Findings | Complete | 3/3 remediated | 3/3 by Month 6 ✓ |
| PCI-DSS Level 2 | On track | QSA engaged; audit Month 10 | Recertified by Month 10 |
| Risk Treatment Progress | On track | Top 10 risks: 7 treated, 3 in progress | All 10 treated by Month 12 |
| GRC Programme Budget | On track | £580K of £650K spent; Q4 on plan | Within £650K budget |

---

## Deliverable 2: Executive Cybersecurity Risk Report (Quarterly Board Report)

**What It Is:** The formal written board report accompanying the dashboard — the document board members read before the presentation.

**Structure (8–10 pages):**

**1. Executive Summary** (1 page):
Written for the board. 3 sections:
- Current State: "NovaTech's security posture has improved materially in Year 1. [Headline metric: e.g., 'MTTD reduced from 19.3 hours to 9.2 hours']."
- Key Achievements: 5 bullet points (ISO 27001 Stage 1 complete, FCA findings closed, etc.)
- Immediate Attention: 2 items requiring board awareness

**2. Risk Landscape** (2 pages):
- Top 5 risks with FAIR ALE values (from Week 22)
- Treatment progress for each
- Risk trend: Are risks increasing or decreasing?
- Risk heatmap (insert from Week 22)

**3. Compliance Status** (2 pages):
- ISO 27001 progress: Gaps remaining, Stage 2 schedule, expected certification date
- PCI-DSS status: QSA findings summary, recertification timeline
- FCA operational resilience: All 3 findings closed — evidence summary
- GDPR: DataInsights Analytics remediation status; ICO registration current; no enforcement actions

**4. Programme Investment and ROI** (1 page):
- Investment to date: £[X] of £650K budget (with breakdown)
- Risk reduction achieved: ALE reduced by £[X] for top 5 risks
- Business value: ISO 27001 opens £2.5M ARR opportunity; FCA risk mitigated

**5. Year 2 Plan and Investment Request** (1 page):
- Year 2 objectives
- Budget request: £420,000
- Itemised breakdown: SOC 2 Type II (£80K), surveillance audit (£25K), FAIR programme (£50K), staff (£180K), ongoing tooling (£85K)
- ROI case for Year 2 investment

**6. Board Resolutions Required** (half page):
- Resolution 1: Approve Year 2 GRC programme budget (£420,000)
- Resolution 2: Note Year 1 GRC programme achievements
- Resolution 3: Ratify appointment of permanent GRC Lead (internal hire replacing consultant)

---

## Deliverable 3: Board Presentation Pack (20 Slides)

**What It Is:** The full 20-slide board presentation delivered in the Week 24 mock board meeting.

**20-slide structure:**

**Slides 1–4: Opening**
- Slide 1: Title slide with NovaTech branding, date, presenter
- Slide 2: Agenda (5 sections)
- Slide 3: Executive Summary — programme in 5 numbers
- Slide 4: Programme Timeline — milestones achieved (visual Gantt or timeline)

**Slides 5–7: Security Posture**
- Slide 5: GRC Maturity — Before vs After radar chart (8 domains)
- Slide 6: Security Operations Dashboard — 12 KPIs with RAG and trends
- Slide 7: Overall security posture improvement narrative — "are we safer?"

**Slides 8–11: Risk**
- Slide 8: Enterprise Risk Heatmap (from Week 22)
- Slide 9: Top 5 Risks — FAIR ALE with treatment progress
- Slide 10: Ransomware Risk — Deep dive on largest risk; ALE before (£77M) vs ALE after PAM/controls (£[X])
- Slide 11: Risk Treatment Investment ROI — £650K invested; £[X]M ALE reduced

**Slides 12–15: Compliance**
- Slide 12: ISO 27001 Journey — Gap closure timeline; Stage 1 complete; Stage 2 countdown
- Slide 13: FCA Operational Resilience — 3/3 findings closed; evidence summary
- Slide 14: PCI-DSS — Status; QSA audit result
- Slide 15: GDPR — No enforcement actions; DataInsights remediated

**Slides 16–17: Programme Results**
- Slide 16: Audit Programme — 6 audits; findings by severity; improvements made
- Slide 17: Vendor Programme — 5 assessed; one issue found and resolved; ongoing programme

**Slides 18–20: Investment and Forward Plan**
- Slide 18: Business Value Delivered — ROI narrative; Series D condition met
- Slide 19: Year 2 Roadmap — SOC 2, FAIR programme, advanced detection
- Slide 20: Board Resolutions — 3 resolutions for approval

**Design principles:**
- Maximum 5 bullets per slide
- Every slide headline is a key message (not just a topic title)
- Use visuals: heatmaps, radar charts, trend lines, RAG tables
- Written for non-technical executives — no unexplained acronyms

---

## Deliverable 4: GRC Programme Maturity Assessment (Before/After)

**What It Is:** A formal assessment comparing NovaTech's GRC maturity at programme start (Month 0, from Week 21 initial assessment) vs current state (Month 12), demonstrating programme impact.

**Create a structured assessment across 8 GRC domains:**

| Domain | Month 0 Maturity | Month 12 Maturity | Improvement | Evidence |
|--------|-----------------|-------------------|-------------|----------|
| Governance and Oversight | 0.5 / 5.0 | 3.2 / 5.0 | +2.7 | Board committee established; CISO board access; quarterly reporting |
| Risk Management | 0.8 / 5.0 | 3.5 / 5.0 | +2.7 | 30-risk register; FAIR analysis; risk appetite set |
| Policy Framework | 0.5 / 5.0 | 3.8 / 5.0 | +3.3 | 15 policies published; policy register maintained |
| Compliance Management | 0.5 / 5.0 | 3.2 / 5.0 | +2.7 | ISO 27001 Stage 1 passed; PCI-DSS recertified; FCA findings closed |
| Audit and Assurance | 0.0 / 5.0 | 3.0 / 5.0 | +3.0 | Audit charter; 6 audits conducted; findings tracked |
| Vendor Risk | 0.5 / 5.0 | 3.5 / 5.0 | +3.0 | 5 Tier 1 vendors assessed; vendor register operational |
| Incident Response | 0.5 / 5.0 | 3.2 / 5.0 | +2.7 | IR plan and 3 playbooks; SIEM live; tabletop conducted |
| Security Metrics/Reporting | 0.0 / 5.0 | 3.5 / 5.0 | +3.5 | 12-KPI dashboard; quarterly board reports; executive pack |

**Overall programme maturity:**
- Month 0: 0.4 / 5.0 (Nascent/Initial)
- Month 12: 3.3 / 5.0 (Defined/Managed)
- Improvement: +2.9 maturity points in 12 months

Include radar charts (before and after) and a narrative explanation of what drove improvement in each domain.

---

## Deliverable 5: Complete NovaTech GRC Programme Binder

**What It Is:** A README or index document for the complete NovaTech capstone — the "cover page" of the entire 4-week capstone project.

**Create `Capstone-NovaTech/README.md`:**
```markdown
# NovaTech Corp — Enterprise GRC Programme

## Programme Overview
[3-paragraph summary of NovaTech, the engagement, and what was built]

## Deliverables Index
[Table of all deliverables across all 4 weeks with links to files]

## Frameworks Applied
[Table: Framework | How Applied | Key Deliverables]

## Your Role
[What you did as Lead GRC Consultant — specific responsibilities]

## Programme Impact
[Before/After maturity table]
[Business value: ISO 27001 unlocked £2.5M ARR; FCA findings closed; Series D condition met]

## Skills Demonstrated
[List 20+ specific GRC skills with examples from the NovaTech programme]
```

---

## Deliverable 6: GitHub Portfolio Final Polish

**What It Is:** A documented review and polish of your complete GitHub portfolio, with attestation that it meets job-market quality standards.

**Complete this final checklist:**

**Root Portfolio README:**
- [ ] Professional summary of your GRC specialisation
- [ ] Table of all 15 projects with one-line descriptions and links
- [ ] Frameworks mastered listed clearly
- [ ] Certifications (actual + pursuing)
- [ ] Contact information and LinkedIn link

**NovaTech Capstone:**
- [ ] 8-section folder structure present (01-Governance through 08-Executive-Reports)
- [ ] All deliverables populated (no empty folders or placeholder files)
- [ ] README.md complete with overview, frameworks, skills demonstrated
- [ ] Maturity before/after prominently displayed

**All 15 Projects (verify each):**
- [ ] README.md: Scenario, role, frameworks, deliverables, skills
- [ ] All deliverables files present and complete (no "Coming Soon")
- [ ] No placeholder text in any file
- [ ] Professional file naming (Company-Deliverable-v1.0.md not "final_doc.xlsx")
- [ ] Version control headers in all documents

**Profile-Level:**
- [ ] Profile README published with GRC bio
- [ ] 6 best repos pinned (include NovaTech capstone as Pin 1)
- [ ] Profile bio updated
- [ ] Contribution graph shows recent activity

**Produce a written attestation:** "I have reviewed all 15 portfolio projects against the quality checklist. The following issues were found and corrected: [list]. The portfolio is now job-market ready."

---

## Capstone Final Evaluation

### What Makes This Capstone Distinction Grade

**Across all 4 capstone weeks (21–24):**

1. **Completeness** — All 8 NovaTech programme sections delivered; all deliverables complete
2. **Internal consistency** — Week 21 strategy drives Week 22 risk appetite which governs Week 23 compliance gaps which informs Week 24 KPI targets. One coherent programme.
3. **NovaTech specificity** — All documents populated with NovaTech-specific context (£180M ARR, 2,000 employees, FCA regulation, 5M customers, £650K budget). No generic templates.
4. **Financial grounding** — FAIR analyses with realistic £ values; investment summaries with specific cost breakdowns; ROI calculations
5. **Board-ready quality** — All documents formatted professionally; no placeholder text; version controlled; classification labels applied
6. **Framework accuracy** — ISO 27001 control references correct; NIST CSF function codes correct; GDPR articles correctly cited; PCI-DSS requirements numbered correctly
7. **Programme impact demonstrated** — Before/after maturity assessment shows quantified improvement; business value articulated in £ terms

---

## Week-Specific Resources

- [NCSC: Board Toolkit — Cyber Reporting](https://www.ncsc.gov.uk/collection/board-toolkit) — Board-level reporting standards
- [FCA: Good Practices in Operational Resilience](https://www.fca.org.uk/publications/multi-firm-reviews/good-and-poor-practices-in-operational-resilience) — FCA expectations
- [ISACA: Cybersecurity Audit Programme](https://www.isaca.org/resources) — Professional audit guidance
- [GitHub: Creating a Profile README](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)
- [CyberSeek: GRC Career Pathways](https://www.cyberseek.org/) — Job market context for board ROI narrative

---

## Submission

```
Capstone-NovaTech/07-Metrics-Dashboard/
├── NovaTech-Security-Metrics-Dashboard-12Month-v1.0.xlsx
└── NovaTech-Programme-Progress-Dashboard-v1.0.xlsx

Capstone-NovaTech/08-Executive-Reports/
├── NovaTech-Executive-Risk-Report-Q4-Year1-v1.0.md
├── NovaTech-Board-Presentation-20Slides-v1.0.pptx
├── NovaTech-GRC-Maturity-Before-After-Assessment-v1.0.xlsx
└── NovaTech-Programme-Binder-Index-v1.0.md

[Your Portfolio Root]/
└── README.md (final polished version)
└── [GitHub Portfolio Final Polish Checklist].md
```

---

## Final Word

You have spent 24 weeks building something genuinely impressive. The NovaTech programme is a complete, enterprise-grade GRC engagement that demonstrates skills most GRC Analysts develop over 2–3 years of real-world experience. Your portfolio proves what you can do — not what you say you can do.

Present it with confidence. You earned it.
