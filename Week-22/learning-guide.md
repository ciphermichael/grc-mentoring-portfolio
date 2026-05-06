# Week 22 Learning Guide: Capstone — Risk Management & Policy Library

## What You Will Build This Week

This week you execute the two foundational GRC pillars for NovaTech: a 30+ risk enterprise risk register with FAIR analysis for the top risks, and a complete 15-policy security policy library. These two deliverables represent the analytical backbone (risk) and the governance backbone (policy) of any mature GRC programme. By the end of this week, NovaTech will have documented its risk landscape and the rules that govern how it manages information security.

---

## Section 1: Enterprise Risk Register at Scale

### Building a 30+ Risk Register for a Fintech

A risk register for a 2,000-person regulated UK fintech is categorically different from the 20-risk register you built in Week 2. The differences:

**Domain breadth**: An enterprise risk register must cover all risk domains — technology, third-party, compliance, operational, physical, strategic, and emerging. A fintech also has payment fraud risk, regulatory licence risk, and competitive risk in the technology landscape.

**Risk owner sophistication**: Risk owners at enterprise level are senior executives — CISO, CFO, CTO, Head of Legal, Chief Risk Officer. Each risk must be owned at the appropriate level of accountability.

**FAIR integration**: For the board and FCA, qualitative risk ratings are insufficient. NovaTech needs FAIR quantification for its top 5 risks to present to investors and regulators.

**Regulatory risk prominence**: Risks with regulatory consequences (FCA, PCI-DSS, ICO) must be prominent and specifically named — not buried in generic "compliance risk" categories.

**Risk treatment specificity**: Treatment plans for enterprise risks name specific vendors, tools, timelines, and costs — not vague recommendations.

### The 15-Policy Library Architecture

By Week 7 you built 10 policies for RetailMax. NovaTech requires all 15 named policies from the capstone spec. The additional 5 policies (Cryptography, Patch Management, Change Management, Data Retention, Physical Security, AI Use) add important coverage.

**What makes a fintech policy library different:**
- Payment-specific language: PCI-DSS cardholder data handling, payment card credentials
- FCA references: FCA operational resilience requirements baked into the BCP policy
- Higher stakes: NovaTech processes payments for 5M customers — the consequences of policy failures are more severe
- Board visibility: The full policy library is an FCA exhibit — it must be board-approved and audit-ready

---

## Section 2: Deep Dive on Key Deliverables

### Enterprise Risk Register (30+ Risks)

**Risk categories for NovaTech:**
- **Technology/Cyber** (6–8 risks): Ransomware, DDoS on payment platform, AWS misconfiguration, API security breach, insider data theft, AI model poisoning, zero-day exploitation
- **Third-Party/Supply Chain** (4–5 risks): Payment processor breach, AWS outage, critical SaaS vendor compromise, software supply chain attack
- **Compliance/Regulatory** (4–5 risks): PCI-DSS non-compliance, FCA enforcement, ICO investigation, GDPR Art. 33 notification failure, PSD2 compliance gap
- **Operational** (4 risks): Key person dependency (CISO), manual process errors in payment processing, fraud detection failure, customer data accuracy
- **Strategic** (3 risks): Competitor breach damaging fintech industry trust, talent attrition in security team, Series D investor withdrawal
- **Physical** (2 risks): London HQ fire/flood, device theft (laptop with unencrypted data)
- **Emerging** (2 risks): AI/ML model attack on fraud detection, quantum computing threat to payment encryption

**FAIR analysis for top 3–5 risks**: Apply the FAIR model (as learned in Week 17) to at least 3 risks:
- Risk 1: Ransomware attack on payment processing platform
- Risk 2: PCI-DSS cardholder data breach via API vulnerability
- Risk 3: FCA enforcement action for operational resilience failures

For each FAIR analysis, include: TEF, Vulnerability estimate, LEF, Primary Loss Magnitude, Secondary Loss Magnitude (regulatory fines, litigation, reputational damage), PLM, and Annual Loss Expectancy. Calibrate using industry data (Verizon DBIR, FCA enforcement history, ICO penalty register).

### The 15-Policy Library

**For each policy, the quality bar:**
- 2–4 pages of complete content (no placeholder text)
- Uses "must", "shall", "is required to" language throughout
- Includes NovaTech-specific context (2,000 employees, fintech, FCA-regulated, payment processing)
- Maps to ISO 27001 Annex A controls, PCI-DSS requirements, and GDPR articles where relevant
- Signed by CEO (Information Security Policy) or CISO (domain policies)
- Version 1.0, dated, classification: Internal

---

## Section 3: Risk-to-Policy Alignment Matrix

The risk-to-policy alignment matrix demonstrates that NovaTech's policy library is risk-driven — each policy exists because it mitigates specific identified risks. This is a sophisticated GRC deliverable that demonstrates programme integration.

**How to build it:**
For each risk in the register, identify which policy (or policies) governs the controls that treat that risk. Then for each policy, confirm it addresses the risks you've identified.

Example:
| Risk | Risk Score | Primary Treatment Policy | Secondary Policies |
|------|------------|--------------------------|-------------------|
| Ransomware on payment servers | Critical (20) | POL-011 Patch Management | POL-003 Access Control, POL-005 IR Policy |
| Developer data exfiltration | High (16) | POL-003 Access Control | POL-001 InfoSec Policy, POL-002 AUP |
| PCI-DSS cardholder data breach | Critical (20) | POL-001 InfoSec Policy | POL-003 Access Control, POL-010 Cryptography |

---

## Section 4: Common Capstone Week 22 Mistakes

1. **Risk register lacks calibration**: Risks calibrated to NovaTech's specific threat environment (UK fintech, FCA-regulated, 5M customers) rather than generic. Ransomware targeting financial services is specific and well-documented.

2. **Policies reused from Week 7 without NovaTech customisation**: The Week 7 policies were for RetailMax. NovaTech needs its own policies — different company, different regulatory context, different risk profile. Don't copy/paste.

3. **FAIR analysis missing secondary losses**: The most significant losses for a fintech breach are regulatory fines (FCA up to 10% of annual turnover for some violations) and reputational damage. These must be included.

4. **Policy library missing fintech-specific requirements**: NovaTech processes payments — policies must reference cardholder data, PCI-DSS requirements, and payment security specifically.

5. **Risk-to-policy matrix is superficial**: Every policy linking to every risk means no meaningful analysis. The matrix should show specific, justified connections.

---

## Section 5: Professional Tips for Capstone Week 22

- **FAIR calibration for fintechs**: The FCA publishes enforcement notices with fine amounts. Use these to calibrate secondary loss estimates for regulatory risk scenarios.
- **Policy library architecture**: Use a consistent document numbering scheme (POL-001 through POL-015) and ensure all 15 policies use identical formatting.
- **Risk register density**: 30+ risks sounds like a lot, but a fintech with 2,000 employees, 5M customers, and FCA/PCI-DSS obligations genuinely has this many material risks. Don't compress — be thorough.
- **The Policy Register is as important as the policies**: A clean Policy Register showing owner, version, review date, approval status, and ISO/NIST/PCI-DSS cross-references demonstrates programme maturity.

---

## Section 6: Resources Specific to Week 22

- [FCA Enforcement Actions](https://www.fca.org.uk/news/news-stories/enforcement-action-financial-services) — Use for FAIR secondary loss calibration
- [ICO Penalty Register](https://ico.org.uk/action-weve-taken/enforcement/) — GDPR fine amounts for calibration
- [Verizon DBIR — Financial Sector](https://www.verizon.com/business/resources/reports/dbir/) — Threat frequency calibration
- [PCI-DSS v4.0 Requirements](https://www.pcisecuritystandards.org/document_library/) — Policy alignment requirements
- [FAIR Institute Blog](https://www.fairinstitute.org/blog) — FAIR analysis examples for financial sector

---

## Section 7: Instructor Mentorship Guidance

### Capstone Week 22 Review Focus

**Quality markers:**
1. Risk register has 30+ risks across all 7 categories; scores are calibrated (not all High/Critical)
2. FAIR analysis for at least 3 risks includes secondary losses with calibration evidence cited
3. All 15 policies are complete (no placeholders); use "must" language; include NovaTech-specific context
4. Risk-to-policy matrix demonstrates genuine analytical connections (not every policy linked to every risk)
5. Risk owner names are consistent with NovaTech's org structure from Week 21

**Discussion questions:**
1. "Walk me through your top risk — why did you score it Critical and what FAIR ALE did you calculate?"
2. "Your AI Use Policy — how did you handle NovaTech's fraud detection AI?"
3. "The Access Control Policy — which PCI-DSS requirement does it satisfy?"
4. "How many of your 30 risks have no current controls? What does that tell you about NovaTech's GRC maturity?"
