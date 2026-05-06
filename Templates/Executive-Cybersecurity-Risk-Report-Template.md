# Executive Cybersecurity Risk Report Template

| Field | Value |
|-------|-------|
| **Document ID** | EXEC-RISK-Q3-2025 |
| **Organisation** | [Company Name] |
| **Report Period** | Q3 2025 (July – September 2025) |
| **Version** | 1.0 |
| **Prepared By** | [CISO Name] |
| **Reviewed By** | [CRO / Head of Legal] |
| **Audience** | Board Risk and Audit Committee |
| **Classification** | Confidential — Board Only |
| **Distribution** | Board members only — not for further distribution |

---

> **Presenter's Note:** This report is intended for board-level consumption. All technical concepts are explained in business terms. Risks are expressed as financial exposures where possible. No section should require cybersecurity expertise to understand.

---

## 1. Executive Summary

### Security Posture: **AMBER** — Improving

Overall, [Company Name]'s cybersecurity posture has improved materially in Q3 2025. Following investment in [SIEM / EDR / PAM], our ability to detect and respond to threats has strengthened significantly. However, two areas remain elevated risk: [describe top 2 concerns in plain language].

**Q3 Headline Metrics:**

| Metric | Q2 | Q3 | Target | Status |
|--------|----|----|--------|--------|
| Mean Time to Detect threats | 14.2 hours | 9.2 hours | < 8 hours | Amber ↑ |
| Patch compliance (Critical CVEs) | 78% | 88% | 95% | Amber ↑ |
| Phishing simulation failure rate | 22% | 14% | < 10% | Amber ↑ |
| Security incidents (P1) | 1 | 0 | 0 | Green ✓ |
| Open Critical vulnerabilities >90 days | 21 | 12 | 0 | Amber ↑ |

> **↑** = Improving | **↓** = Declining | **→** = Stable

**Board Action Required:** The board is asked to note the Q3 security performance and approve the Year 2 GRC programme budget request of £[X]K (see Section 7).

---

## 2. Top 5 Cybersecurity Risks

*Risks are expressed as expected financial impact to enable comparison with other business risks.*

| Rank | Risk | Likelihood | Impact | ALE (Annualised Expected Loss) | Trend | Treatment Status |
|------|------|-----------|--------|-------------------------------|-------|-----------------|
| 1 | Ransomware attack on core systems | 4/5 (Likely) | 5/5 (Catastrophic) | £[X]M per year | → Stable | In treatment — PAM deployment Q4 |
| 2 | Regulatory enforcement for operational resilience failures | 3/5 (Possible) | 4/5 (Major) | £[X]M exposure | ↓ Improving (FCA finding 1 closed) | 1 of 3 FCA findings closed |
| 3 | Third-party data breach via critical vendor | 3/5 (Possible) | 4/5 (Major) | £[X]M | → Stable | Vendor assessment programme launched |
| 4 | Insider data theft by privileged user | 2/5 (Unlikely) | 5/5 (Catastrophic) | £[X]M | → Stable | DLP evaluation in progress |
| 5 | DDoS attack on customer-facing services | 3/5 (Possible) | 3/5 (Moderate) | £[X]M | → Stable | AWS Shield Advanced approved |

> **Note on methodology:** Likelihood and impact are scored 1–5. Financial estimates use the FAIR (Factor Analysis of Information Risk) quantitative model, calibrated against NCSC threat intelligence and industry breach data (Verizon DBIR 2025). These are expected value estimates — actual losses in any given incident may be higher or lower.

---

## 3. Risk Deep Dives

### Risk 1: Ransomware Attack

**Business Context:** Ransomware attacks against UK companies in our sector increased 40% in 2024 (NCSC Annual Review). A successful attack encrypting our [core system] would halt operations for an estimated 5–7 days, costing approximately £[X]M in direct revenue loss plus regulatory penalties.

**What we have done:** Deployed EDR (endpoint detection and response) on all Windows endpoints (completed August 2025). CloudTrail logging centralised into SIEM (completed September 2025). Patch compliance improved from 78% to 88%.

**What we still need:** Privileged Access Management (PAM) tooling — the single biggest gap. Without PAM, an attacker who compromises any IT admin credential gains full system access. PAM deployment (CyberArk) is approved and in delivery for Q4 2025.

**Investment:** £80,000 (PAM). Expected risk reduction: ~65% reduction in ALE from ransomware (£[X]M annual reduction).

---

### Risk 2: FCA Operational Resilience

**Business Context:** The FCA raised 3 findings in their March 2025 supervisory review: (1) insufficient board oversight of cyber risk; (2) no operational resilience programme; (3) informal risk management. Failure to remediate risks formal enforcement action.

**What we have done:** Finding 1 closed — quarterly board security reporting established (this report); Security Steering Committee launched. Finding 2 in progress — operational resilience programme design complete; implementation ongoing.

**Finding 3 status:** Risk management methodology approved by CISO; risk register reviewed; Risk Appetite Statement drafted for board approval.

**Board action:** The board is asked to approve the Risk Appetite Statement (attached as Annex A).

---

## 4. Compliance Status

### ISO 27001 Certification Progress

| Activity | Status | Milestone Date |
|----------|--------|---------------|
| Gap assessment | Complete | June 2025 |
| Policy library (15 policies) | Complete | July 2025 |
| Risk assessment | Complete | August 2025 |
| Internal audit (Access Control) | Complete — 3 findings | September 2025 |
| Internal audit findings remediated | 2 of 3 complete | October 2025 (target) |
| Stage 1 Audit (BSI) | Scheduled | November 2025 |
| Stage 2 Audit (BSI) | Planned | February 2026 |
| **ISO 27001 Certificate** | **On track** | **Q1 2026** |

> **Business impact:** ISO 27001 certification unlocks [X] enterprise deals currently in "pending security approval" status in our pipeline, with estimated combined ARR of £[X]M.

### GDPR Compliance

| Area | Status |
|------|--------|
| Record of Processing Activities (RoPA) | Updated — complete |
| DPA with all processors | 14 of 15 complete; DataInsights DPA in negotiation |
| Subject Access Requests — Q3 response rate | 100% within 30-day deadline (3 SARs received) |
| Data breach notifications | None required in Q3 |
| ICO enforcement actions | None |

### PCI-DSS v4.0

| Area | Status |
|------|--------|
| QSA Audit scheduled | Q4 2025 |
| Open findings from last QSA | 3 of 5 remediated; 2 in progress |
| Patch compliance (cardholder systems) | 92% — on track for QSA |

---

## 5. Security Operations Metrics

*A full metrics dashboard is available from the GRC team on request. Key highlights:*

**Improving significantly:**
- **Phishing simulation failure rate:** 31% (Q1) → 22% (Q2) → 14% (Q3). Target: <10% by Q4. Driven by quarterly phishing simulations and security awareness training refresh. **Estimated risk reduction: ~45% fewer successful phishing attacks.**
- **Mean Time to Detect (MTTD):** 19.3hr → 14.2hr → 9.2hr. Target: <8hr. Driven by SIEM deployment in Q3. At current improvement rate, target achievable by Q4.
- **Patch compliance (Critical CVEs):** 62% → 78% → 88%. Target: 95%. 3 legacy systems remain — patch schedule confirmed.

**Stable (no change):**
- **Open Critical CVEs >90 days:** 34 → 21 → 12. Improving but not yet at target (0). Root cause: 12 remaining CVEs on legacy systems awaiting upgrade in Q4 planned maintenance window.

---

## 6. Incident Report

### Q3 2025 Incidents

| Severity | Count | Notable Incidents |
|---------|-------|------------------|
| P1 (Critical) | 0 | None |
| P2 (High) | 1 | See below |
| P3 (Medium) | 4 | Minor phishing; no data loss |
| P4 (Low) | 12 | Routine operational |

**P2 Incident — August 12, 2025:**
*What happened:* A developer account was compromised via a spear-phishing email. The attacker accessed the developer's GitHub account but did not access production systems. Detected by SIEM alert on unusual login location (non-UK IP). Account suspended within 2 hours.
*Data affected:* No customer data accessed. Source code repository access (non-production). No GDPR breach.
*Actions taken:* MFA enforced on GitHub; phishing awareness session for development team.
*Lessons learned:* GitHub not covered by previous MFA enforcement — now corrected.

---

## 7. Investment Summary and Year 2 Request

### Year 1 Expenditure (Vs £650,000 Budget)

| Category | Budget | Actual Q3 | Forecast Q4 |
|----------|--------|-----------|-------------|
| External consultancy (GRC programme) | £200,000 | £145,000 | £195,000 |
| ISO 27001 certification (BSI) | £35,000 | £0 | £35,000 |
| GRC Platform (Vanta) | £45,000 | £45,000 | £45,000 |
| PAM tooling (CyberArk) | £80,000 | £15,000 | £80,000 |
| SIEM implementation | £120,000 | £118,000 | £120,000 |
| EDR (CrowdStrike) | £75,000 | £75,000 | £75,000 |
| Security awareness (KnowBe4) | £15,000 | £15,000 | £15,000 |
| Penetration testing | £25,000 | £25,000 | £25,000 |
| Internal GRC hire | £48,000 | £36,000 | £48,000 |
| Contingency | £7,000 | £0 | £7,000 |
| **TOTAL** | **£650,000** | **£474,000** | **£645,000** |

**ROI achieved (Year 1):**
- ALE reduction (top 3 risks): £[X]M expected annual loss reduction
- Enterprise pipeline unlocked (ISO 27001): £[X]M ARR potential
- FCA enforcement risk mitigated: £[X]M estimated fine avoided

### Year 2 Budget Request: £420,000

| Investment | Amount | Justification |
|-----------|--------|---------------|
| SOC 2 Type II audit | £80,000 | US enterprise expansion requirement |
| ISO 27001 surveillance audit | £25,000 | Mandatory to maintain certification |
| FAIR quantitative risk programme | £50,000 | Regulatory expectation (DORA); investor due diligence |
| Permanent GRC Lead (salary + benefits) | £65,000 | Replace consultant; build internal capability |
| GRC Analyst (additional hire) | £48,000 | Programme growth requires additional resource |
| Security tooling (ongoing + new) | £120,000 | Vanta, KnowBe4, CrowdStrike, threat intel feeds |
| Penetration testing (annual) | £25,000 | ISO 27001 requirement; annual test |
| Training and professional development | £7,000 | Staff certifications (CompTIA, ISACA) |
| **TOTAL** | **£420,000** | |

---

## 8. Looking Ahead — Q4 Priorities

| Priority | Action | Timeline | Owner |
|----------|--------|----------|-------|
| 1 | Complete PAM deployment (CyberArk — all admin accounts) | November 2025 | CISO |
| 2 | ISO 27001 Stage 1 audit (BSI) | November 2025 | GRC Lead |
| 3 | PCI-DSS QSA annual assessment | December 2025 | GRC Lead |
| 4 | Patch remaining 12 legacy CVEs (planned maintenance) | October 2025 | Head of IT |
| 5 | Board Risk Appetite Statement approval | This meeting | Board |

---

## 9. Board Resolutions

**Resolution 1:** The Board notes the Q3 2025 cybersecurity report and the progress against the GRC programme.

**Resolution 2:** The Board approves the Year 2 GRC programme budget of £420,000.

**Resolution 3:** The Board approves the Risk Appetite Statement for Information Security (Annex A).

---

## Annex A: Risk Appetite Statement (For Approval)

[Organisation] maintains a **Low** appetite for information security risks that could result in:
- Disclosure of customer personal data
- Disruption to core business services exceeding [RTO hours]
- Regulatory enforcement action

Quantified risk tolerance: The Board sets a maximum acceptable annualised expected loss (ALE) from information security risks of £[X]M. Individual risks exceeding £[X]M ALE are escalated to the Board Risk Committee for acceptance or mandatory treatment.

---

## Annex B: Glossary of Terms

| Term | Plain English Definition |
|------|--------------------------|
| **Annualised Expected Loss (ALE)** | The average annual financial loss expected from a risk based on probability and magnitude |
| **MTTD (Mean Time to Detect)** | Average time between when an attacker enters our systems and when we identify the intrusion |
| **Patch compliance** | The percentage of our systems that have security updates applied within the required timeframe |
| **SOC 2** | An independent audit report confirming our security controls meet industry standards — required by many enterprise customers |
| **ISO 27001** | An internationally recognised security management certification — required by UK enterprise procurement teams |
| **SIEM** | Security monitoring system that collects and analyses log data to detect threats |
| **PAM** | Privileged Access Management — controls that restrict what IT administrators can access and do |
| **EDR** | Endpoint Detection and Response — advanced anti-malware that detects and responds to sophisticated attacks |
| **CVE** | Common Vulnerabilities and Exposures — publicly disclosed software vulnerability |
| **P1 Incident** | A critical security incident causing or likely to cause significant business impact |

---

*Executive Cybersecurity Risk Report | Q3 2025 | Board Risk & Audit Committee | Version 1.0*
