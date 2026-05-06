# Week 08 Learning Guide: Vendor Risk Management

## What You Will Learn This Week

Your organisation is only as secure as its weakest vendor. The SolarWinds attack, the Kaseya VSA breach, and numerous third-party data breaches have made vendor risk management one of the most scrutinised areas of GRC. This week you will build a complete vendor risk management programme — including a tiering model, vendor risk assessments, and a vendor risk register. You will also learn the GDPR obligations that make vendor due diligence legally required (not just good practice) for any company processing personal data.

---

## Section 1: Core Concept Explained

### What Is Vendor Risk Management?

Vendor Risk Management (VRM) — also called Third-Party Risk Management (TPRM) or Supply Chain Risk Management — is the structured process of identifying, assessing, and managing the cybersecurity risks posed by third parties who have access to your systems, data, or infrastructure.

In modern organisations, vendors are everywhere. A typical mid-sized UK company might use: cloud providers (AWS, Azure), SaaS applications (Salesforce, Microsoft 365, Slack), specialist software vendors, managed service providers, outsourced IT support, legal firms, payroll providers, and recruitment platforms. Each of these vendors has some level of access to your data or systems — and each is a potential attack vector.

The regulatory mandate for VRM is clear under **GDPR Article 28**: if you are a data controller and you engage a data processor (any vendor who processes personal data on your behalf), you must: have a Data Processing Agreement (DPA) in place, only use processors that provide sufficient guarantees, conduct due diligence on their security, and have the right to audit them.

Beyond regulatory obligation, VRM is a strategic business requirement. Enterprise customers increasingly demand evidence of vendor security programmes. SOC 2 CC9 requires assessment of vendor risk. ISO 27001 A.5.19–5.22 requires formal supplier security management.

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **Vendor / Third Party** | External entity with access to your systems or data | Cloud provider, payroll service, IT support |
| **Data Processor** | Vendor processing personal data on your behalf | Payroll SaaS processing employee salary data |
| **Sub-Processor** | Vendor used by your processor | AWS is a sub-processor of your SaaS payroll vendor |
| **Data Processing Agreement (DPA)** | GDPR-required contract with processors (Art. 28) | Contract specifying security obligations |
| **VRAQ** | Vendor Risk Assessment Questionnaire | Sent to vendors to assess their security posture |
| **Vendor Tiering** | Categorising vendors by criticality and risk | Tier 1 = Critical; Tier 4 = Low risk |
| **Fourth-Party Risk** | Risk from vendors of your vendors (sub-processors) | Your payroll vendor uses an insecure cloud provider |
| **Right to Audit** | Contractual right to audit vendor security | Annual audit right in DPA |
| **Inherent Vendor Risk** | Risk before assessing vendor's security controls | A vendor processing health data = inherent high risk |
| **Residual Vendor Risk** | Risk after considering vendor's security controls | SOC 2 certified vendor = lower residual risk |
| **SLA (Service Level Agreement)** | Agreed service performance commitments | 99.9% uptime; breach notification within 24 hours |
| **Supply Chain Attack** | Attack via a trusted vendor (e.g., SolarWinds) | Malicious code inserted into software update |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Real-World Vendor Risk Management Process

1. **Build a vendor inventory** — Before you can manage vendor risk, you need to know who your vendors are. Create a complete list of all third parties with access to company systems, data, or networks. Most organisations are surprised how many vendors they have.

2. **Tier vendors by inherent risk** — Not all vendors need the same level of assessment. A vendor providing monthly office plant maintenance needs different scrutiny than a vendor processing millions of customer records. Develop a tiering model:
   - **Tier 1 (Critical)**: Vendors with access to sensitive personal data, core business systems, or critical infrastructure. Full assessment required.
   - **Tier 2 (High)**: Vendors with significant but less sensitive access. Questionnaire + review of certifications.
   - **Tier 3 (Standard)**: Vendors with limited data access. Lighter-touch assessment.
   - **Tier 4 (Low)**: Vendors with no meaningful data access (e.g., office supplies, catering). Contract terms only.

3. **Conduct vendor risk assessments** — For Tier 1 and Tier 2 vendors, send a Vendor Risk Assessment Questionnaire (VRAQ). Review their security certifications (ISO 27001, SOC 2, Cyber Essentials). Request penetration test evidence. Review their incident response procedures.

4. **Review vendor contractual terms** — Check contracts for: security obligations, data processing terms, breach notification obligations, right to audit, liability and insurance requirements, sub-processor disclosure requirements.

5. **Sign Data Processing Agreements (DPAs)** — For any vendor processing personal data, a GDPR-compliant DPA is legally required. This must include all elements of GDPR Article 28(3).

6. **Conduct ongoing monitoring** — Vendor risk doesn't end at initial assessment. Monitor vendors continuously: track news about vendor security incidents, conduct annual reassessments of Tier 1 vendors, check for changes in certification status.

7. **Vendor offboarding** — When a vendor relationship ends, ensure all access is revoked, all data is returned or securely destroyed, and all contractual obligations are fulfilled.

### Real Company Example

When Meridian Insurance Group (a 5,000-person UK insurer) conducted their first systematic vendor inventory, they identified 340 third-party applications and services — far more than the 80 their IT team were aware of. This "shadow IT" problem is extremely common.

Their VRM programme, led by GRC Analyst Priya Mehta, started by categorising all 340 vendors using a tiering model. 12 vendors were Tier 1 (including their core policy management system, their cloud data warehouse provider, and their outsourced call centre). 45 were Tier 2. The remaining 283 were Tier 3 or 4.

Priya then sent full VRAQs to all 12 Tier 1 vendors. Four were unable to produce a SOC 2 report or ISO 27001 certificate. Two failed specific VRAQ questions around encryption and access control. One vendor (their data warehouse provider) had been breached 18 months earlier but had not notified Meridian. This was a material finding requiring immediate escalation.

The VRM programme resulted in: 4 vendors required to remediate gaps within 90 days; 1 vendor replaced; 1 vendor breach incident reported to ICO (as it involved personal data); significant security improvements across the supplier ecosystem.

---

## Section 3: Framework Deep Dive

### ISO 27001:2022 — Supplier Security Controls

**A.5.19 — Information security in supplier relationships**: Processes and procedures defined for managing security risks associated with suppliers.

**A.5.20 — Addressing information security within supplier agreements**: Information security requirements included in agreements with each supplier.

**A.5.21 — Managing information security in the ICT supply chain**: Supplier ICT products and services security requirements defined and applied.

**A.5.22 — Monitoring, review and change management of supplier services**: Regular monitoring and review of supplier service delivery including security aspects.

### GDPR Article 28 — Processor Requirements

The DPA between controller and processor MUST include (Art. 28(3)):
- Processing only on documented controller instructions
- Confidentiality obligations on persons processing the data
- Security measures (Article 32)
- Sub-processor requirements (prior written authorisation)
- Assistance with data subject rights requests
- Assistance with breach notification and DPIAs
- Deletion or return of data at end of service
- Provision of all information necessary to demonstrate compliance (right to audit)

### SOC 2 CC9 — Risk Mitigation

SOC 2 CC9 requires organisations to: identify, select, and develop risk mitigation activities (including vendor/supply chain risk); evaluate changes in vendor relationships; include appropriate vendor risk management practices.

---

## Section 4: Common Mistakes Beginners Make

1. **Only assessing new vendors and ignoring existing ones.** Vendor risk changes over time. A vendor who was secure 3 years ago may not be secure today. Annual reassessment of Tier 1 vendors is essential.

2. **Relying solely on vendor self-assessment.** VRAQs are self-reported. Verify claims by requesting certifications (SOC 2 reports, ISO 27001 certificates), penetration test evidence, or third-party assessment reports.

3. **Treating a DPA as optional.** GDPR requires DPAs with all data processors. This is a legal requirement, not a nice-to-have. Missing DPAs can result in ICO enforcement.

4. **Ignoring fourth-party risk.** Your vendor uses sub-vendors. If your payroll vendor hosts their software on an insecure cloud provider, your data is at risk. Ask vendors to disclose their sub-processors.

5. **No vendor offboarding process.** When vendors are terminated, access must be revoked and data returned/destroyed. Many organisations leave terminated vendors with lingering access to systems.

6. **Treating vendor tiering as set-and-forget.** A vendor's tier can change. A vendor who previously had no data access may acquire it as the business relationship grows. Review tiers annually.

7. **Not including security obligations in contracts.** Many organisations sign vendor contracts without negotiating security clauses. Once signed, it's very difficult to add security obligations.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Start your VRM programme with a vendor inventory** — you can't manage what you don't know about.
- **Use third-party risk assessment services** — BitSight, SecurityScorecard, and RiskRecon provide automated external vendor risk ratings based on passive scanning.
- **Always request and read SOC 2 reports** (not just the certificate) — the report details the controls tested and any exceptions found.
- **Build vendor risk into procurement** — VRM works best when security assessment happens before signing contracts, not after.
- **The GDPR DPA is a negotiation** — vendors may present their own DPA template; review it carefully against Article 28 requirements.
- **Track sub-processors explicitly** — require vendors to notify you of sub-processor changes; this is your GDPR right.
- **Breach notification SLA in contracts** — require vendors to notify you within 24 hours of a breach involving your data (so you have time to meet your own 72-hour ICO obligation).

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [GDPR Article 28 — gdpr-info.eu](https://gdpr-info.eu/art-28-gdpr/) — Processor obligations in full
- [ICO: Using Processors](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/accountability-and-governance/accountability-framework/using-processors/) — UK GDPR guidance
- [ISO 27001 A.5.19–5.22 Overview](https://www.iso.org/standard/27001) — Supplier security controls
- [NCSC: Supply Chain Security Guidance](https://www.ncsc.gov.uk/collection/supply-chain-security) — UK government supply chain security
- [CISA: ICT Supply Chain Risk Management](https://www.cisa.gov/supply-chain-risk-management) — US government guidance applicable to US vendors
- [SolarWinds Post-Breach Analysis — NCSC](https://www.ncsc.gov.uk/news/joint-advisory-on-sunburst-malware) — Why vendor risk matters

### Books

- *Third-Party Risk Management* by N. Eric Weiss — Comprehensive TPRM guide
- *Vendor Risk Management* by Gregory C. Rasner — Practical VRM implementation

### Online Courses

- [ISACA: Third-Party Risk Management Course](https://www.isaca.org/training-and-events) — Professional training
- [Coursera: Cybersecurity and Supply Chain Risk](https://www.coursera.org/learn/cybersecurity-supply-chain-risk) — Supply chain risk fundamentals
- [YouTube: Vendor Risk Management Explained — RSA Conference](https://www.youtube.com/@RSAConference) — Conference presentations on VRM

### Tools to Explore

- **BitSight** (bitsight.com) — External vendor risk ratings; request a demo
- **SecurityScorecard** (securityscorecard.com) — Alternative vendor risk rating platform
- **OneTrust Vendor Risk** — Privacy and vendor risk management

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (Teaching Session — 90 min)

- 20 min: Why vendor risk matters — SolarWinds, Kaseya, and third-party breach statistics
- 15 min: GDPR Article 28 walkthrough — what must be in a DPA; consequences of missing DPAs
- 20 min: Vendor tiering model design — work through a tiering exercise together for 10 fictional vendors
- 20 min: VRAQ walkthrough — review the template; discuss what makes a vendor's answer high-risk vs low-risk
- 15 min: Introduce DataBridge scenario; identify the risk with TechSupport Pro's 3-year gap

### Session B Focus (Assignment Review — 60 min)

- Review vendor register: Are vendors correctly tiered? Are GDPR Art. 28 considerations reflected?
- Spot-check one VRAQ: Is it realistically completed? Are gaps identified?
- Review vendor risk matrix: Does it correctly reflect risk vs security posture?
- Ask: "TechSupport Pro has had remote access to client environments for 3 years without assessment. What is DataBridge's immediate obligation?"

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "Walk me through how you would build a vendor risk management programme from scratch."
2. "What is the difference between a data controller and a data processor?"
3. "What does GDPR Article 28 require in a Data Processing Agreement?"
4. "How do you tier vendors by risk?"
5. "What is a Vendor Risk Assessment Questionnaire and what does it cover?"
6. "How do you conduct ongoing monitoring of vendor risk?"
7. "What is fourth-party risk?"
8. "What is a supply chain attack? Give an example."
9. "What ISO 27001 controls relate to vendor risk?"
10. "What happens when a vendor suffers a data breach involving your data?"

### Keywords to Use

- Third-Party Risk Management (TPRM)
- Vendor tiering model (Tier 1–4)
- GDPR Article 28 — Data Processing Agreement
- Vendor Risk Assessment Questionnaire (VRAQ)
- Sub-processors and fourth-party risk
- Right to audit
- SOC 2 Type II report review
- Ongoing monitoring — BitSight, SecurityScorecard
- Supply chain attack — SolarWinds reference
- Breach notification SLA
- ISO 27001 A.5.19–5.22
