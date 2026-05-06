# Week 01 Assignment: Introduction to Cybersecurity GRC

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | TechStart Inc. |
| **Your Role** | GRC Analyst (first engagement) |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟 (Foundational) |
| **Frameworks** | ISO 27001, NIST CSF 2.0, SOC 2, GDPR, PCI-DSS |

---

## Scenario Brief — Read This Carefully

**TechStart Inc.** is a 200-person SaaS company founded in 2019, headquartered in Manchester with a remote-first workforce. They provide project management software to small and medium businesses across the UK and EU. Their platform is hosted on AWS (us-east-1 and eu-west-1 regions) and handles personal data for approximately 85,000 end users, including names, email addresses, and business activity data.

TechStart has just closed a Series B funding round of £18M and is now pursuing enterprise deals with larger clients. Their first enterprise prospect — a 3,000-person financial services company — has requested evidence of a formal security programme and asked specifically: "Are you ISO 27001 certified or pursuing certification? Do you have a SOC 2 report? How do you comply with GDPR?" TechStart's CEO, Jamie Brooks, has no answers.

The company currently has no dedicated GRC function. Their CTO, Sarah Chen, handles all security decisions informally. There is one partially written Information Security Policy from 2021 that no one has reviewed since. There is no risk register, no vendor management process, no formal compliance programme, and no security awareness training.

The CEO has brought you in as their first GRC Analyst. Your immediate mandate is to **assess the compliance landscape and recommend a compliance strategy** that will enable TechStart to respond to enterprise customers and build a defensible security programme. The CISO role does not exist yet — you report directly to the CEO and will be the primary author of TechStart's GRC strategy.

**Key stakeholders you will work with:**
- Jamie Brooks (CEO) — business-focused, wants to close the enterprise deal
- Sarah Chen (CTO) — technically skilled but unfamiliar with GRC frameworks
- Rachel Davies (Head of Legal) — needs GDPR compliance; has flagged personal data concerns
- Marcus Webb (Head of Sales) — frustrated that deals are being lost due to lack of security credentials

---

## Before You Start

### Pre-Work Checklist

- [ ] Read the full `learning-guide.md` for Week 1 — especially Sections 1, 2, and 3
- [ ] Visit NIST CSF 2.0 website and read the function overview
- [ ] Read the ISO 27001 overview page on iso.org
- [ ] Read the AICPA SOC 2 overview page
- [ ] Read the ICO's "What is UK GDPR?" guide at ico.org.uk
- [ ] Browse one real GRC job description on LinkedIn to understand required skills

### Questions to Answer Before Starting

1. What industry is TechStart in and what regulations apply to them as a UK SaaS company processing EU personal data?
2. TechStart's enterprise prospect is a financial services company. What compliance credential would that type of customer typically demand from a software vendor?
3. What is the difference between ISO 27001 (which is a certification) and SOC 2 (which is an attestation)?
4. Does a 200-person SaaS company need to comply with GDPR? Why?
5. What does "Series B" mean and why would funding events trigger compliance needs?

---

## Deliverables

### Deliverable 1: GRC Landscape Analysis Report (3–5 pages)

**What It Is:** A professional report presenting TechStart's compliance landscape — which regulations apply, which frameworks are relevant, what their current state looks like, and what the priority recommendations are. This is the document you would hand the CEO in your first week.

**Why This Deliverable Matters:** This report is what enables leadership to make an informed investment decision about compliance. Without it, the CEO doesn't know which frameworks matter or where to start.

**Step-by-Step Instructions:**

1. Open a new document with a professional cover page: TechStart Inc. GRC Landscape Analysis | Date | Prepared by: [Your Name] | Version: 1.0 | Classification: Confidential
2. Write an Executive Summary (max 1 page): What is TechStart's current compliance risk? What are the top 3 recommendations? What happens if they don't act?
3. Write a Business Context section: Describe TechStart's business model, data types processed, geographic scope, and growth trajectory (200 employees, £18M Series B, enterprise sales pursuit).
4. Write a Regulatory Obligations section: List every mandatory requirement that applies to TechStart as a UK SaaS company. Include: UK GDPR (processing EU user personal data), the ICO registration requirement, and any FCA-adjacent requirements if they touch financial services customer data.
5. Write a Framework Analysis section: Describe each of the 4 key frameworks (ISO 27001, NIST CSF 2.0, SOC 2, GDPR) in 1–2 paragraphs each. Explain: What is it? Who demands it? What does it require? Is it mandatory or voluntary for TechStart?
6. Write a Current State Assessment section: Based on the scenario, document TechStart's current security posture honestly. What exists? What is missing? Use a traffic light (RAG) table.
7. Write a Recommended Priority section: Based on TechStart's enterprise sales goal, what should they pursue first? Justify your recommendation. (Hint: SOC 2 or ISO 27001 is the likely answer — explain which and why.)
8. Write a 12-Month High-Level Roadmap section: Quarter-by-quarter activities (Q1: Foundation building, Q2: Controls implementation, Q3: Internal audit, Q4: Certification/attestation).
9. Add a signature block and version history table.
10. Save as: `TechStart-GRC-Landscape-Report-v1.0.pdf` or `.md`

**Template to Use:** No specific template — create this as a professional document from scratch.

**Quality Bar — What "Distinction" Looks Like:**
- Written in business language (not academic or overly technical)
- Executive Summary is self-contained — a busy CEO can read it in 3 minutes and understand the situation
- Current state assessment is honest about gaps (not a copy of what a perfect company would have)
- Framework recommendations are justified against TechStart's specific context (enterprise sales to financial services, UK SaaS, EU user data)
- Roadmap is realistic for a 200-person startup with a small GRC team

**Common Mistakes:**
- Writing in academic style ("ISO 27001 is an international standard published by...") rather than client advisory style
- Recommending all 4 frameworks simultaneously without prioritising
- Not tailoring the analysis to TechStart's specific business context (enterprise sales, EU data, etc.)

**Example Content — Executive Summary:**

> TechStart Inc. operates in a compliance environment with both mandatory obligations (UK GDPR, ICO registration) and market-driven requirements (ISO 27001 or SOC 2 demanded by enterprise customers). The current security programme is informal — no risk register, no vendor management, one outdated policy. This creates immediate risk: the enterprise sales pipeline is directly blocked by the absence of a compliance credential, and a data breach under current conditions would expose TechStart to ICO enforcement action. **Immediate priority:** Begin ISO 27001 implementation and appoint a CISO or Senior GRC Analyst within 30 days.

---

### Deliverable 2: Framework Comparison Table

**What It Is:** A professional comparison table showing ISO 27001, NIST CSF 2.0, SOC 2, and GDPR side-by-side across key dimensions.

**Step-by-Step Instructions:**

1. Create a table with these rows: Framework Name | Publisher | Type (mandatory/voluntary) | Primary Purpose | Who Requires It | Scope | Key Components | Certification/Attestation? | Typical Cost | Time to Achieve | Best For | Overlap With
2. Complete the table for all 4 frameworks accurately.
3. Add a fifth row for PCI-DSS with a note on whether it applies to TechStart.
4. Below the table, write a 1-paragraph synthesis: "For TechStart, the most strategically valuable framework is [X] because [3 reasons]."

**Quality Bar:**
- All table cells completed accurately (no vague entries)
- PCI-DSS correctly identified as not applicable to TechStart (they don't process payment cards)
- Synthesis paragraph references TechStart's specific situation

---

### Deliverable 3: Recommended Framework Priority with Justification

**What It Is:** A 1-2 page document making a formal recommendation on which compliance framework TechStart should pursue first, second, and third — with clear business justification.

**Step-by-Step Instructions:**

1. Use a structured format: Priority 1 | Priority 2 | Priority 3
2. For each priority, include: Framework name | Business justification | Timeline | Estimated cost | Dependencies
3. Write a "Key Risks of Inaction" section: What happens to TechStart's business if they don't act in the next 90 days?
4. Address the specific enterprise prospect question: "Are you ISO 27001 certified or pursuing certification?"
5. Consider: ISO 27001 is globally recognised and covers more ground; SOC 2 is preferred by US enterprise customers; GDPR is mandatory now. Structure your recommendation accordingly.

**Example Recommendation Structure:**

> **Priority 1 (Start Now): ISO 27001:2022 Implementation** — Justification: The enterprise prospect is a UK financial services company. ISO 27001 is the most commonly required security certification in UK enterprise procurement. It provides a foundation that also advances GDPR compliance and can map to SOC 2 criteria. Timeline: 12 months to certification. Estimated cost: £60–100K (staff time + tooling + audit fees).

---

### Deliverable 4: GRC Team Structure Recommendation

**What It Is:** A brief document recommending the GRC function structure TechStart should build over the next 12 months.

**Step-by-Step Instructions:**

1. Define the immediate hire: What role does TechStart need most urgently? (CISO? GRC Manager? Privacy Officer?)
2. Build a 12-month hiring roadmap: What roles are needed by Q1, Q2, Q3, Q4?
3. Define reporting lines: Who does the CISO report to? Who does the GRC team report to?
4. Draw a simple org chart (text-based is acceptable): Show CISO → GRC Analyst → Compliance Analyst → DPO (Data Protection Officer)
5. Define the three lines of defense for TechStart at its current size.
6. Write a RACI for the top 5 GRC activities at TechStart (risk assessment, policy development, GDPR compliance, vendor risk, internal audit).

---

### Deliverable 5: Professional GitHub Portfolio Setup

**What It Is:** A public GitHub repository set up as your professional GRC portfolio.

**Step-by-Step Instructions:**

1. Create a new public GitHub repository named: `grc-analyst-portfolio` or `cybersecurity-grc-portfolio`
2. Write a professional README.md with: Your name and GRC specialisation | About this portfolio (what it contains) | Table of projects | Skills demonstrated | Certifications pursuing | Contact information
3. Create the folder structure matching the programme's repository structure
4. Upload your Week 1 deliverables (landscape report, framework comparison table, team structure recommendation)
5. Write a project-specific README for Week 1 explaining: the scenario, your role, the deliverables, and frameworks applied
6. Set up your GitHub profile: professional photo, bio mentioning "GRC Analyst | Cybersecurity Governance, Risk and Compliance", link to this repository

**Quality Bar:**
- README is written in professional English — no "Lorem ipsum" placeholder text
- Repository structure is clean and navigable
- Week 1 project README clearly explains what the work is and why it matters

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Completeness | 25% | All 5 deliverables submitted |
| Professional Quality | 30% | Reads like a real client-facing document; no academic language |
| Framework Accuracy | 25% | Frameworks correctly described; recommendations are appropriate to context |
| Business Relevance | 20% | Analysis is specific to TechStart's situation, not generic |

---

## Frameworks Applied This Week

| Framework | How Applied |
|-----------|------------|
| **ISO 27001:2022** | Included in landscape analysis as primary recommended framework; described in comparison table |
| **NIST CSF 2.0** | Included in landscape analysis; useful reference for US customers |
| **SOC 2 (AICPA)** | Described as alternative/complementary to ISO 27001 for enterprise SaaS |
| **GDPR / UK GDPR** | Identified as mandatory for TechStart; GDPR compliance recommended as parallel track |
| **PCI-DSS v4.0** | Assessed and determined not applicable (TechStart doesn't process payment cards) |

---

## Week-Specific Resources

- [ISO 27001 Overview — iso.org](https://www.iso.org/standard/27001) — Public standard overview
- [NIST CSF 2.0 — Official Website](https://www.nist.gov/cyberframework) — Full framework document and quick start guides
- [AICPA SOC 2 Overview](https://us.aicpa.org/interestareas/frc/assuranceadvisoryservices/sorhome) — Official SOC 2 description
- [ICO: What is UK GDPR?](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/what-is-uk-gdpr/) — UK regulator guidance
- [ICO Registration Check](https://ico.org.uk/for-organisations/register/) — Does TechStart need to register with the ICO?
- [CIS Controls v8 Overview](https://www.cisecurity.org/controls/v8) — Alternative foundational framework
- [NCSC Cyber Essentials](https://www.ncsc.gov.uk/cyberessentials/overview) — UK baseline; consider for TechStart
- [Vanta Blog: ISO 27001 vs SOC 2](https://www.vanta.com/resources/iso-27001-vs-soc-2) — Practical comparison for SaaS companies
- [UpGuard: GRC Explained](https://www.upguard.com/blog/grc) — Good overview of GRC for beginners
- [GitHub Profile Setup Guide](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/about-your-profile) — Official GitHub profile documentation

---

## Submission

Upload your completed deliverables to:

```
Week-01/Deliverables/
├── TechStart-GRC-Landscape-Report-v1.0.md
├── Framework-Comparison-Table.md
├── Framework-Priority-Recommendation.md
├── GRC-Team-Structure-Recommendation.md
└── [Link to your GitHub portfolio in README.md]
```

Then update your `README.md` completion status table and tag your mentor for review.
