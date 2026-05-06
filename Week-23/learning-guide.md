# Week 23 Learning Guide: Capstone — Compliance, Audit & Vendor Programs

## What You Will Build This Week

Week 23 delivers three integrated components: a unified multi-framework compliance mapping (ISO 27001 + PCI-DSS + GDPR), NovaTech's internal audit programme, and a complete vendor risk programme with 5 assessed vendors. These are the third-line assurance and supply chain components of the enterprise GRC programme — the infrastructure that proves controls are working and that third parties meet NovaTech's security standards.

---

## Section 1: Multi-Framework Compliance Mapping

### The Unified Compliance Matrix at Enterprise Scale

By Week 18 (InsureCo), you built a unified compliance matrix for ISO 27001 + SOC 2 + GDPR. NovaTech's matrix is more complex: ISO 27001 + PCI-DSS v4.0 + GDPR. The regulatory pressure from all three simultaneously is the lived reality of a regulated UK fintech.

**Why this matrix is so valuable:**
1. **Audit efficiency**: One access review procedure satisfies ISO 27001 A.5.18, PCI-DSS Req 7.2 (access control), and GDPR Art. 32 simultaneously. The matrix proves this overlap to auditors.
2. **Gap prioritisation**: A gap that appears in all 3 frameworks is 3× as urgent as one that appears in only one. The matrix surfaces these compound gaps.
3. **Evidence reuse**: One piece of evidence (e.g., quarterly access review completion records) can be cited for ISO 27001 Stage 2 audit, SOC 2 evidence package, and PCI-DSS QSA review. The matrix documents this.

### The ISO 27001 Gap Assessment at Capstone Quality

NovaTech's ISO 27001 gap assessment is different from Week 5's (Xown Solutions) in several ways:
- **NovaTech has 2,000 employees across 3 offices**: scope complexity is higher
- **PCI-DSS in scope**: Annex A Technological Controls must reflect payment card data handling requirements
- **FCA operational resilience**: A.5.29–5.30 are particularly important for NovaTech's FCA findings
- **Maturity scoring must reflect current state honestly**: The point is to identify the real gaps for the roadmap, not to inflate scores

---

## Section 2: Internal Audit Programme at Enterprise Scale

### What Makes NovaTech's Audit Programme Enterprise-Grade

NovaTech's internal audit programme, once established, will run permanently — it's the ongoing assurance mechanism that confirms controls are working year after year. The difference from a one-off audit:

**Annual programme design**: 6–8 planned audits per year covering all major ISO 27001 domains. The annual programme is risk-prioritised — higher-risk domains get audited more frequently or with wider scope.

**Audit independence**: NovaTech's internal audit function (co-sourced with KPMG as recommended in Week 21's operating model) must be genuinely independent. Internal auditors do not implement controls or make operational decisions — they test and report.

**Audit methodology documentation**: The audit charter, methodology, and reporting templates must be consistent across all audits, enabling comparison of findings across quarters and years.

**Escalation to Board Audit Committee**: Material audit findings escalate to the Board Risk & Audit Committee — this is the governance link that ensures board oversight of control effectiveness.

---

## Section 3: Vendor Risk Programme at Enterprise Scale

### NovaTech's 5 Critical Vendors

In Week 8 (DataBridge), you assessed 3 vendors. NovaTech's vendor programme is larger and more complex, reflecting its position as a regulated payment processor:

**The 5 assigned vendors:**

1. **CloudPay Ltd.** — NovaTech's primary payment processor. Processes all cardholder transactions. Tier 1 (Critical). PCI-DSS L1 service provider. Access: direct cardholder data. Previous assessment: never formally assessed. Risk: Any CloudPay compromise directly exposes NovaTech cardholder data — maximum PCI-DSS and reputational risk.

2. **Microsoft Azure** — Identity (Azure AD) and Office 365. Tier 1 (Critical). ISO 27001 certified; SOC 2 Type II; FedRAMP. Access: NovaTech employee credentials and corporate email. Assessment approach: Review Azure's published compliance reports (SOC 2, ISO 27001) rather than VRAQ (sub-service organisation approach).

3. **DataInsights Analytics** — Third-party analytics company processing NovaTech customer behavioural data for marketing analytics. Tier 1 (Critical). EU-US data transfer involved (DPA required; SCCs needed). No published certifications. This is the high-risk vendor.

4. **LegalEagle LLP** — NovaTech's external legal counsel. Holds privileged legal communications including regulatory correspondence. Tier 2 (High). Law firm — cannot receive a full VRAQ (professional privilege); assess via limited questionnaire.

5. **TalentBridge HR** — HR SaaS platform managing all 2,000 employee records including salary, performance reviews, sensitive personal data. Tier 2 (High). ISO 27001 certified. Penetration test conducted 8 months ago.

---

## Section 4: Integration with Prior Weeks

**Compliance matrix must reference:**
- Week 21 regulatory obligations register (all obligations should appear in the compliance matrix)
- Week 22 risk register (compliance gaps should link to regulatory risks identified)
- Week 22 policy library (policies referenced as controls in the compliance matrix)

**Audit programme must reference:**
- Week 21 governance framework (audit charter aligns to committee structure; findings escalate to Board Risk & Audit Committee)
- Week 22 risk register (highest-risk domains get highest audit priority)

**Vendor assessments must reference:**
- Week 21 vendor management policy (assessments follow the policy's tiering and due diligence requirements)
- Week 22 risk register (vendor risks should match vendor register findings)

---

## Section 5: Common Mistakes in Capstone Week 23

1. **Compliance matrix that's too shallow**: "ISO A.5.18 maps to PCI-DSS Req 7" is correct but incomplete. The matrix should show: exactly which sub-requirement of PCI-DSS, whether there's a gap, what evidence satisfies both, and who owns the control.

2. **Audit programme without risk basis**: The sequencing of audits across the year must be explained — why Access Control first? Because Week 22's risk register shows it as the highest-concentration risk area.

3. **Vendor assessments too lenient**: The whole point of vendor assessment is to find real gaps. CloudPay has never been formally assessed — realistically, there will be gaps. DataInsights Analytics (no certifications, US-based) will have gaps. Write realistic findings.

4. **Missing GDPR Art. 28 DPA status**: Every vendor in the register that processes personal data must have their DPA status documented. This is an ICO audit expectation.

5. **Audit programme that's aspirational but not resourced**: Who conducts the audits? What are their qualifications? How many person-days per audit? An audit programme without resource planning isn't credible.

---

## Section 6: Resources for Week 23

- [PCI-DSS v4.0 Control Objectives](https://www.pcisecuritystandards.org/document_library/) — Detailed requirements for compliance mapping
- [ISO 27001:2022 Annex A — Full control list](https://www.iso.org/standard/27001) — Gap assessment reference
- [GDPR Article 28 — ico.org.uk](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/accountability-and-governance/accountability-framework/using-processors/) — DPA requirements
- [NCSC: Supply Chain Security](https://www.ncsc.gov.uk/collection/supply-chain-security) — Vendor risk context
- [ISO 19011:2018](https://www.iso.org/standard/70017.html) — Audit programme standards
- [Microsoft Trust Center](https://www.microsoft.com/en-us/trust-center/compliance/compliance-overview) — Azure compliance documentation model

---

## Section 7: Instructor Guidance

**Capstone Week 23 quality markers:**
1. Unified compliance matrix covers all 3 frameworks with specific references (not generic)
2. ISO 27001 gap assessment maturity scores are realistic (NovaTech is immature — most should be 0–2)
3. Annual audit programme is risk-sequenced with resource plan
4. All 5 vendor assessments are completed with NovaTech-specific context
5. DataInsights Analytics VRAQ shows HIGH risk finding (international transfer, no certification)
6. Compliance evidence tracker has specific evidence items (not "evidence collected")
7. All deliverables reference NovaTech's specific regulatory obligations

**Discussion questions:**
1. "DataInsights Analytics processes NovaTech customer data in the US with no SCCs. What is the immediate action?"
2. "Your ISO 27001 gap assessment shows A.8.2 (Privileged Access) at maturity 1. How does this connect to your Week 22 risk register?"
3. "Your annual audit programme has 6 audits. Which audit domain has the highest priority and why?"
