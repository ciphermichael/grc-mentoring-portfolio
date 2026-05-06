# Week 24 Learning Guide: Capstone — Metrics Dashboard & Final Presentation

## What You Will Build This Week

This is your final week. You will complete NovaTech's GRC programme by building a professional security metrics dashboard and delivering a 30-minute board presentation — the capstone's climax. This week you demonstrate the most advanced GRC skill: synthesising a complex, multi-month programme into a compelling, board-ready narrative that drives decision-making. You will also perform a final polish of your entire GitHub portfolio, ensuring it is genuinely job-ready.

---

## Section 1: The Security Metrics Dashboard at Capstone Level

### What Makes NovaTech's Dashboard Different

By Week 15 (TechCorp), you built a 10-KPI operational dashboard for a relatively stable company. NovaTech's dashboard is a programme dashboard — it must show not just how current controls are performing, but how the entire 12-month GRC programme is progressing toward strategic objectives.

**Two dashboard layers:**

**Layer 1 — Programme Progress Dashboard** (for board quarterly reporting):
- ISO 27001 certification progress: Gaps closed / total gaps; milestone status
- PCI-DSS compliance progress: Requirements met / total; QSA audit readiness
- FCA findings remediation: 3/3 findings closed?
- Risk treatment progress: High/Critical risks with treatment in progress
- Vendor programme progress: Tier 1 vendors assessed / total

**Layer 2 — Security Operations Dashboard** (for monthly CISO/management reporting):
- Standard 10 KPIs (patch compliance, MTTD, phishing rate, etc.)
- RAG status, trend arrows, 3-quarter trend data
- Monthly narrative

### Designing Metrics That Matter to NovaTech's Board

NovaTech's board cares specifically about:
1. **ISO 27001 certification timeline** — Series D investors require it; the CEO has committed to it
2. **FCA operational resilience** — 3 open findings; the FCA is watching
3. **PCI-DSS compliance** — Payment processor status affects transaction volume limits
4. **Ransomware exposure** — Board has been briefed on the £77M ALE; wants to see treatment progress

Every metric presented to the NovaTech board must link to one of these four priorities.

---

## Section 2: The Board Presentation

### The 30-Minute Board Presentation — Structure

NovaTech's board receives the final GRC programme report. Format: 30 minutes presentation + 15 minutes Q&A. Audience: 7 board members (3 NEDs, CEO, CFO, CTO, Head of Legal). Moderately technical but primarily business-focused. Series C investors on the board are primarily focused on certification timeline and regulatory risk.

**20-slide deck structure:**

**Slides 1–4: Executive Summary and Programme Overview**
- Slide 1: Title slide — "NovaTech Corp — Enterprise GRC Programme: Year 1 Report" | Date | Presented by Lead GRC Consultant
- Slide 2: Executive Summary — Programme in numbers: 30+ risks documented; 15 policies published; ISO 27001 Stage 1 audit in Month 10; 5 vendors assessed; 6 audits planned
- Slide 3: Current Security Posture — "Where are we now?" — Radar chart showing GRC maturity at programme start vs Month 12 target
- Slide 4: Programme Health — Overall RAG status; 3 strategic objectives Green, 2 Amber; key message

**Slides 5–8: Risk Landscape**
- Slide 5: Enterprise Risk Heatmap — Visual from Week 22; key message: "X Critical risks; Y High risks; top 3 require immediate investment"
- Slide 6: Top 3 Risk Deep Dive — Risk 1 (Ransomware, £77M ALE) | Risk 2 (PCI-DSS breach) | Risk 3 (FCA enforcement) — 1 slide, 3 columns
- Slide 7: Risk Treatment Progress — Investment made vs ALE reduction achieved (show ROI narrative)
- Slide 8: Risk Trend — Are risks increasing or decreasing vs Q1 baseline?

**Slides 9–12: Compliance and Certification**
- Slide 9: ISO 27001 Progress — Gaps remaining; stage 1 audit date; projected certification date; "on track / at risk"
- Slide 10: PCI-DSS Status — QSA audit date; key requirements status; Level 2 recertification outcome
- Slide 11: FCA Operational Resilience — All 3 findings closed? Evidence summary
- Slide 12: GDPR Compliance — RoPA updated; DPAs in place; DataInsights Analytics remediated?

**Slides 13–15: Programme Results**
- Slide 13: Audit Programme — 6 audits completed; findings by severity; critical findings remediated
- Slide 14: Vendor Risk — 5 Tier 1 vendors assessed; DataInsights issue resolved; vendor risk reduced
- Slide 15: Security Awareness and Culture — Training completion rate; phishing improvement

**Slides 16–18: Investment and ROI**
- Slide 16: Investment Summary — £650K invested vs £15M+ risk reduction (ALE reduction for top 3 risks)
- Slide 17: Business Value Delivered — ISO 27001 certification unlocks £2.5M ARR; FCA risk mitigated; Series D condition met
- Slide 18: Year 2 Investment Request — £420K budget request with specific breakdown and ROI case

**Slides 19–20: Looking Forward**
- Slide 19: Year 2 Priorities — SOC 2 Type II (if required), ISO 27001 surveillance audit, FAIR quantification programme, advanced threat detection
- Slide 20: Board Resolution Required — Approve Year 2 budget | Approve GRC programme continuation | Note achievement of ISO 27001 certification

---

## Section 3: Handling Tough Board Questions

### The 10 Questions You Must Prepare For

1. **"Why are we still at High/Amber on the ISO 27001 certification timeline?"**
Answer: Be specific — which gaps remain, what's the plan, what's the revised timeline.

2. **"The £77M ransomware exposure — has this reduced with the controls we've implemented?"**
Answer: Show the FAIR re-analysis — PAM implementation has reduced ALE from £77M to £X. Control investment is clearly justified.

3. **"We invested £650,000. What did we get for it?"**
Answer: ROI narrative — quantify risk reduction (ALE), revenue unlocked (ISO 27001 certification), regulatory risk mitigated (FCA findings), investor condition met.

4. **"DataInsights Analytics — is this issue resolved?"**
Answer: Clear yes/no. If SCCs are not signed, this is a GDPR violation. Be honest.

5. **"Why should we invest another £420,000 in Year 2?"**
Answer: Business case — what Year 2 delivers that Year 1 hasn't. SOC 2 unlocks US market. FAIR programme improves capital allocation. Surveillance audit maintains ISO 27001.

6. **"How do we know the programme is actually working?"**
Answer: Metrics — show the trend data. Phishing failure down from 28% to 12%. Patch compliance up from 65% to 92%. MTTD reduced from 19 hours to 8 hours.

7. **"If we got hit by ransomware today, what happens?"**
Answer: Your IR plan is in place; PAM is deployed; backups are hardened; SIEM is monitoring. But be honest about what's not yet complete.

8. **"What's the FCA's view of our programme?"**
Answer: 3 findings closed. No current enforcement action. Annual supervisory meeting planned for Q1 Year 2 where you'll present the programme.

9. **"Should we pursue SOC 2 next year?"**
Answer: Recommend based on business need — if US enterprise sales are a priority, yes. Budget for it is in the Year 2 request.

10. **"How does your programme compare to other fintechs our size?"**
Answer: Reference industry benchmarks — NCSC data on UK fintech security maturity; note that ISO 27001 certification puts NovaTech ahead of 65% of comparable UK fintechs.

---

## Section 4: Final GitHub Portfolio Polish

### The Portfolio Review Checklist for Job Market

This is your last chance to ensure your portfolio is genuinely job-ready before you enter the market.

**Overall Portfolio:**
- 15+ projects with complete deliverables
- Capstone NovaTech project is the flagship — most complete, most polished
- Each project README explains: scenario, your role, frameworks applied, deliverables, skills demonstrated
- GitHub profile README published with GRC specialisation summary
- 6 best repositories pinned

**Professional Standards Across All Projects:**
- No placeholder text: "Lorem ipsum", "[Your name]", "TBD", "Insert here"
- Version control: all documents have version numbers, dates, and classification labels
- Consistent file naming: Company-Deliverable-Version.md
- Framework references accurate: ISO 27001 Annex A control numbers correct; NIST CSF function codes correct; GDPR articles cited correctly

**NovaTech Capstone (the flagship):**
- All 8 sections (01-Governance through 08-Executive-Reports) populated
- GRC Programme is internally consistent (risk appetite flows through to risk register; policies cross-referenced in compliance matrix)
- Board presentation is visual, professional, non-technical
- Before/after maturity assessment shows GRC programme impact clearly

---

## Section 5: Professional Reflection

### What You Have Demonstrated Over 24 Weeks

By completing this programme, you have demonstrated competence in:

- **ISO 27001:2022** — Full standard, gap assessment, SoA, implementation roadmap, internal audit
- **NIST CSF 2.0** — All 6 functions, maturity assessment, CSF Profile, cross-framework mapping
- **SOC 2** — All 5 Trust Services Criteria, readiness assessment, evidence collection
- **GDPR/UK GDPR** — Full compliance assessment, RoPA, DPIA, breach notification, international transfers
- **PCI-DSS v4.0** — Gap assessment, QSA preparation, cardholder data protection
- **CIS Controls v8** — IG1/IG2 assessment, cross-framework mapping, cyber insurance readiness
- **FAIR quantitative risk** — ALE calculation, Monte Carlo concepts, board ROI presentation
- **Internal audit** — ISO 19011 methodology, audit lifecycle, finding writing, report quality
- **Control testing** — SOC 2 common criteria, evidence standards, deficiency classification
- **Vendor risk management** — Tiering, VRAQ, GDPR Art. 28, ongoing monitoring
- **Business Impact Analysis** — RTO/RPO/MTD/MBCO, ISO 22301 methodology
- **Incident response** — NIST SP 800-61, GDPR Art. 33/34, post-incident review
- **Security metrics** — KPI/KRI design, RAG dashboards, executive reporting
- **Cloud GRC** — AWS shared responsibility, CIS AWS Benchmark, CSPM
- **AI governance** — NIST AI RMF, EU AI Act, GDPR Art. 22
- **GRC programme management** — Unified control frameworks, multi-framework compliance, GRC platforms
- **Executive communication** — Board-level reporting, risk quantification in business terms

This is an extraordinary breadth of demonstrable GRC competence. Your GitHub portfolio proves it. Now go get the job.

---

## Section 6: Instructor Guidance

### Capstone Week 24 — Final Review Criteria

**Distinction-level capstone (across all 4 weeks):**
1. All 8 NovaTech GRC programme components delivered with complete, non-placeholder content
2. Full internal consistency: Week 21 governance drives Week 22 risk register drives Week 23 compliance matrix drives Week 24 metrics
3. FAIR analyses present realistic financial estimates with calibration sources cited
4. Board presentation is 20 slides, visually professional, written for a non-technical audience
5. GitHub portfolio is genuinely job-ready: all 15 projects complete; no placeholder text; consistent professional formatting
6. Before/after GRC maturity assessment shows measurable programme impact

**The mock board Q&A:** Run this as a genuine pressure test. The student must field 10 tough board questions without notes in 15 minutes. This is the closest thing to a real board presentation they'll face before their first job.
