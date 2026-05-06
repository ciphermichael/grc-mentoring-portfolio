# Week 17 Learning Guide: Enterprise Risk Assessment Program

## What You Will Learn This Week

Most organisations assess risk qualitatively — scoring threats on a 1–5 scale and colour-coding them red, amber, or green. But boards and CFOs increasingly demand quantitative risk analysis: "Don't tell me this risk is 'High' — tell me it costs us £2.3M in expected annual loss." This week you study the FAIR (Factor Analysis of Information Risk) model — the premier quantitative cyber risk methodology — alongside enterprise-scale risk programme design. This is Phase 4 Advanced GRC content, reflecting the skills of senior GRC professionals and risk managers.

---

## Section 1: Core Concept Explained

### What Is Quantitative Risk Analysis?

Qualitative risk analysis (the 5×5 matrix you built in Week 2) is excellent for communication and prioritisation. But it has a critical limitation: it cannot answer "how much should we invest to mitigate this risk?" because you can't calculate return on a colour.

Quantitative risk analysis replaces subjective ratings with financial estimates expressed in currency (£/$). The key metric is:

**Annual Loss Expectancy (ALE) = Annual Rate of Occurrence (ARO) × Single Loss Expectancy (SLE)**

Or more sophisticatedly, using the **FAIR model:**

**Loss Event Frequency (LEF) = Threat Event Frequency (TEF) × Vulnerability (V)**

**Probable Loss Magnitude (PLM) = Primary Loss Magnitude + Secondary Loss Magnitude**

**Risk = LEF × PLM**

This produces a risk expressed as: "We expect X% probability of this loss event occurring once per year, with an expected loss of £Y if it does occur. Our annualised expected loss is therefore £Z."

**Why quantitative risk matters:**
- A CISO who says "ransomware is a Critical risk" gets a nodded head. A CISO who says "our FAIR analysis shows ransomware carries an annualised expected loss of £3.8M against which our £280,000 EDR investment reduces expected loss by 62% — a 14:1 ROI" gets budget approved.

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **FAIR** | Factor Analysis of Information Risk — quantitative risk methodology | Industry standard for cyber risk quantification |
| **ALE** | Annual Loss Expectancy | £450,000/year expected loss from ransomware |
| **LEF** | Loss Event Frequency — how often a loss event occurs | 30% chance of ransomware per year (LEF = 0.3) |
| **TEF** | Threat Event Frequency — how often a threat actor acts | Ransomware groups target companies like ours ~5x/year |
| **Vulnerability** | Probability that an action leads to a loss | 10% of attacks succeed given current controls |
| **PLM** | Probable Loss Magnitude — how much a loss costs | £1.5M average ransomware cost |
| **SLE** | Single Loss Expectancy | £1.5M per successful ransomware attack |
| **ARO** | Annual Rate of Occurrence | 0.3 (30% probability in a given year) |
| **ISO 27005** | IS risk management standard | Formal methodology framework |
| **Risk Appetite** | Maximum tolerable risk level | "Accept up to £500K annualised expected loss per risk" |
| **Risk Tolerance** | Acceptable deviation above appetite | "Up to 3 risks within 20% above appetite" |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The FAIR Methodology Step-by-Step

1. **Identify the risk scenario** — "What is the probability and magnitude of ransomware encrypting GlobalBank's core banking database?"

2. **Identify the asset and impact** — The core banking database contains transaction records for 8 million customers. A successful attack interrupts core banking for an estimated 5 days.

3. **Estimate Threat Event Frequency (TEF)** — How often do ransomware actors attempt to compromise organisations like GlobalBank? Use threat intelligence: industry breach reports, NCSC data, Verizon DBIR. For a major UK bank: approximately 10–15 targeted ransomware attempts per year.

4. **Estimate Vulnerability** — Given GlobalBank's current controls (EDR on endpoints but no PAM, some network segmentation gaps), what percentage of ransomware attempts succeed? Reference similar organisations' data. Estimate: 8–12% of attempts succeed.

5. **Calculate Loss Event Frequency (LEF)** — LEF = TEF × Vulnerability = 12 attempts × 10% success rate = 1.2 expected events/year.

6. **Estimate Primary Loss Magnitude** — Direct financial losses:
   - Revenue loss during 5-day outage: £8M
   - Incident response and forensics: £450K
   - Restoration costs (backups, recovery): £800K
   - Ransom payment (if paid): £600K–£5M
   - Primary total: ~£10–14M

7. **Estimate Secondary Loss Magnitude** — Indirect losses:
   - Regulatory fine (FCA enforcement for operational resilience failure): £5–20M
   - Reputational damage (customer attrition, share price): £15–50M
   - Litigation from affected customers: £2–8M

8. **Calculate Probable Loss Magnitude (PLM)** — Based on calibrated estimates, the median PLM is approximately £18M.

9. **Calculate Annualised Expected Loss** — LEF × PLM = 1.2 events/year × £18M = £21.6M annualised expected loss.

10. **Evaluate control investment ROI** — GlobalBank is considering a £2M PAM implementation. Analysis shows PAM reduces vulnerability from 10% to 3%. New LEF = 0.36. New ALE = 0.36 × £18M = £6.5M. Risk reduction: £15.1M. ROI: £15.1M reduction for £2M investment = 7.5:1 ROI. The investment is clearly justified.

### What This Looks Like Day-to-Day at Enterprise Level

- Running quarterly risk workshops with business unit risk owners
- Maintaining the enterprise risk register with 30+ risks
- Applying FAIR analysis to top 5 risks quarterly for board reporting
- Writing the CISO's quantitative risk report for the Board Risk Committee
- Setting and communicating the risk appetite statement
- Managing risk treatment tracker and escalation processes

---

## Section 3: Framework Deep Dive

### ISO 27005:2022 — Information Security Risk Management

ISO 27005 provides guidance on information security risk management that satisfies ISO 27001's risk assessment requirements (Clause 6.1.2). Key process:

1. Context establishment (scope, risk criteria, risk appetite)
2. Risk identification (threats, vulnerabilities, assets, impacts)
3. Risk analysis (likelihood × impact)
4. Risk evaluation (compare against risk criteria)
5. Risk treatment (select treatment options, implement controls)
6. Communication and consultation (engage stakeholders)
7. Monitoring and review (update risk register)

ISO 27005 supports both qualitative and quantitative approaches. FAIR is the most widely adopted quantitative methodology aligned with ISO 27005.

### FAIR Model Components

**Tier 1: Risk (frequency of loss × magnitude of loss)**

**Tier 2: Loss Event Frequency** = Threat Event Frequency × Vulnerability
**Tier 2: Loss Magnitude** = Primary Loss + Secondary Loss

**Tier 3 — TEF decomposition**: Contact Frequency × Probability of Action
**Tier 3 — Vulnerability decomposition**: Threat Capability > Control Strength → loss occurs

**FAIR uses Monte Carlo simulation** — instead of point estimates (e.g., "probability = 30%"), FAIR uses ranges (e.g., "30–80% probability") and runs 10,000+ simulations to produce a probability distribution of losses.

---

## Section 4: Common Mistakes Beginners Make

1. **Using false precision.** Quantitative risk analysis produces numbers, not certainty. "£3,847,291 annual loss" implies more precision than exists. Always present as ranges: "£2.5M–£6.5M expected annual loss, median £3.8M."

2. **Ignoring secondary losses.** Most analysts calculate primary losses (direct costs) but miss secondary losses (regulatory fines, reputational damage, litigation). Secondary losses typically dwarf primary losses for major breaches.

3. **Confusing probability with frequency.** "30% probability of ransomware" could mean "30% chance at least once this year" (probability) or "0.3 events per year on average" (frequency). FAIR uses frequency; be precise.

4. **Not using calibrated estimates.** Random guesses produce useless outputs. Base estimates on: industry breach data (Verizon DBIR), NCSC/ENISA threat intelligence, insurance actuarial data, vendor threat reports.

5. **Treating qualitative and quantitative as mutually exclusive.** Both have value. Use qualitative for the full risk register (quick, communicative); use quantitative FAIR analysis for the top 5–10 risks (deeper, more decision-useful).

6. **Not linking quantitative risk to control investment decisions.** The whole point of quantitative risk is to calculate ROI on controls. "This £500K control investment reduces ALE by £2.3M" is the output executives want.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Use the FAIR framework from Open FAIR (opengroup.org)** — the FAIR model is documented as an open standard; the FAIR Institute (fairinstitute.org) has excellent free resources.
- **Use RiskLens for FAIR analysis** — it's the leading FAIR-based software; request a demo to understand the methodology.
- **Reference Verizon DBIR for threat frequency calibration** — the annual DBIR provides industry-specific breach frequency data that calibrates FAIR's TEF estimates.
- **FAIR is not a replacement for qualitative risk management** — use qualitative for breadth (full risk register), FAIR for depth (top risks with investment decisions).
- **The CISO board report should include at least 2 FAIR-quantified risks** — it demonstrates programme maturity and enables board-level financial decision-making.
- **ISO 27005 is the standard; FAIR is the methodology** — know the relationship.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [FAIR Institute: Introduction to FAIR](https://www.fairinstitute.org/what-is-fair) — Free FAIR methodology overview
- [Open FAIR Body of Knowledge](https://www.opengroup.org/forum/open-fair-forum) — Open standard FAIR documentation
- [ISO 27005:2022 Overview](https://www.iso.org/standard/80585.html) — Risk management standard
- [Verizon DBIR 2024](https://www.verizon.com/business/resources/reports/dbir/) — Breach frequency calibration data
- [NCSC: Threat Intelligence — Annual Review](https://www.ncsc.gov.uk/section/keep-up-to-date/threat-reports) — UK threat data
- [FAIR Institute: FAIR Analysis Examples](https://www.fairinstitute.org/blog) — Case study examples

### Books

- *Measuring and Managing Information Risk: A FAIR Approach* by Jack Freund & Jack Jones — The FAIR bible
- *How to Measure Anything in Cybersecurity Risk* by Douglas Hubbard — Quantitative risk methodology

### Online Courses

- [FAIR Institute: FAIR Training](https://www.fairinstitute.org/academy) — Official FAIR training
- [CRISC Exam Preparation — ISACA](https://www.isaca.org/credentialing/crisc) — Enterprise risk management at professional level
- [RiskLens: FAIR Analysis Demo](https://www.risklens.com/) — Product demos with FAIR methodology explanation

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (90 min)

- 25 min: FAIR model deep dive — walk through all tiers with GlobalBank as the example; calculate ALE together
- 20 min: Qualitative vs quantitative comparison — same risk assessed both ways; discuss what each adds
- 20 min: Control investment ROI calculation — show how to calculate ROI of a £500K control against £3M ALE reduction
- 15 min: Risk appetite setting exercise — help student draft a risk appetite statement for GlobalBank
- 10 min: Monte Carlo introduction — what it is and why ranges are more honest than point estimates

### Session B Focus (60 min)

- Review FAIR analysis: Are estimates calibrated (not random)? Are secondary losses included?
- Check risk register: 25+ risks; are they genuinely enterprise-level risks (not just IT risks)?
- Review risk appetite statement: Is it specific and quantified?
- Ask: "Your FAIR analysis shows PAM investment has a 7.5:1 ROI. A board member asks: 'Aren't all security controls worthwhile then?' How do you respond?"

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "What is the FAIR model?"
2. "What is Annual Loss Expectancy?"
3. "How do you calculate Loss Event Frequency?"
4. "What is the difference between qualitative and quantitative risk assessment?"
5. "What is Secondary Loss Magnitude and why does it matter?"
6. "How do you calculate ROI on a security control?"
7. "What is ISO 27005?"
8. "What data do you use to calibrate threat frequency estimates?"
9. "What is a risk appetite statement?"
10. "When would you use FAIR vs a qualitative risk matrix?"
11. "What is Monte Carlo simulation?"

### Keywords to Use

- FAIR model — Factor Analysis of Information Risk
- Annual Loss Expectancy (ALE = ARO × SLE)
- Loss Event Frequency (LEF = TEF × Vulnerability)
- Probable Loss Magnitude (PLM = Primary + Secondary)
- Secondary loss magnitude — regulatory fines, reputational damage
- Risk appetite and risk tolerance
- Calibrated estimates — DBIR, NCSC data
- Monte Carlo simulation
- ISO 27005 — risk management standard
- Control investment ROI
- Quantitative vs qualitative — when to use each
