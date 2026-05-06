# Week 09 Learning Guide: SOC 2 and Cloud Compliance

## What You Will Learn This Week

SOC 2 is the dominant security assurance framework for SaaS companies selling to enterprise customers — especially in the United States. Any SaaS company pursuing enterprise sales will eventually face the question: "Do you have a SOC 2 report?" This week you learn the full SOC 2 framework, conduct a readiness assessment, and build a path from zero to Type II. You will also learn how cloud-native architectures affect the compliance picture — a critical skill as nearly every modern application runs in AWS, Azure, or GCP.

---

## Section 1: Core Concept Explained

### What Is SOC 2?

SOC 2 (System and Organization Controls 2) is an **auditing standard** published by the American Institute of Certified Public Accountants (AICPA). Unlike ISO 27001 (a certification), SOC 2 produces an **attestation report** — an independent auditor's opinion on whether a service organisation's controls meet the Trust Services Criteria (TSC).

**Who conducts SOC 2 audits?** Certified Public Accounting (CPA) firms — accounting firms like Deloitte, PwC, EY, or specialist firms like Prescient Assurance, Schellman, and A-LIGN. The auditor must be a licensed CPA firm.

**What are the 5 Trust Services Criteria (TSC)?**
1. **Security (CC)** — Mandatory in every SOC 2 report. Protection against unauthorised access.
2. **Availability (A)** — System is available for operation as committed.
3. **Confidentiality (C)** — Information designated as confidential is protected.
4. **Processing Integrity (PI)** — System processing is complete, accurate, timely, and authorised.
5. **Privacy (P)** — Personal information is collected, used, and retained per the privacy notice.

Most SaaS companies include Security (mandatory) + Availability. Companies handling sensitive data add Confidentiality. Healthcare or financial companies may add Processing Integrity or Privacy.

**Type I vs Type II:**
- **SOC 2 Type I**: Point-in-time report. The auditor assesses whether controls are *designed* suitably as of a specific date. Typically takes 2–4 months to achieve from a standing start. Useful as an initial milestone but not sufficient for most enterprise requirements.
- **SOC 2 Type II**: Period-of-time report. The auditor assesses whether controls *operated effectively* over an observation period (typically 6–12 months). This is the gold standard and what most enterprise procurement teams require.

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **SOC 2** | Attestation of security controls against AICPA Trust Services Criteria | "We have a SOC 2 Type II report" |
| **Trust Services Criteria (TSC)** | The 5 categories of controls assessed | Security, Availability, Confidentiality, PI, Privacy |
| **Common Criteria (CC1–CC9)** | The control points within the Security TSC | CC6 = Logical and Physical Access |
| **Type I** | Point-in-time design assessment | "Controls are suitably designed as of Dec 31" |
| **Type II** | Period-of-time operating effectiveness | "Controls operated effectively for 6 months" |
| **CPA Firm** | The accounting firm conducting the audit | Schellman, Deloitte, A-LIGN |
| **Control Exception** | Finding where a control didn't operate as intended | "In 3 of 25 instances, access reviews were not completed" |
| **Scope** | Which systems/services are included | "The XYZ SaaS platform hosted on AWS us-east-1" |
| **Sub-service Organisation** | A vendor your organisation relies on | AWS is a sub-service organisation for most SaaS companies |
| **User Entity Controls** | Controls that must be performed by the customer | Customer must manage their own user access |
| **Complementary Controls** | Controls at the sub-service organisation level | AWS SOC 2 report covers infrastructure-layer controls |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Real-World SOC 2 Process

1. **Decision to pursue SOC 2** — Typically triggered by an enterprise prospect requirement or a sales process blocker. Involves CEO/CFO buy-in for the investment (typically £20,000–£60,000 for Type I, £40,000–£100,000+ for Type II depending on auditor and scope).

2. **Define scope** — Determine which services, systems, and TSC to include. Most companies start with Security + Availability only. Too broad a scope increases cost and complexity.

3. **Select an auditor** — Research CPA firms specialising in SOC 2. Get quotes from 2–3 firms. Consider: cost, timing, experience in your industry, their reputation with enterprise customers.

4. **Gap assessment** — Assess current controls against the Common Criteria. Identify gaps. This is typically conducted by an internal GRC team or a readiness consultant.

5. **Remediate gaps** — Implement missing controls before the Type I observation period. For Type II, controls must operate during the observation period.

6. **Evidence collection** — Collect documentation of control implementation: access review records, log review evidence, policy approvals, change management approvals, vendor assessment records.

7. **Type I audit** — Auditor reviews documentation and tests design. Typically 2–4 weeks on-site or remote.

8. **Type II observation period** — Controls operate under auditor observation for 6–12 months. Auditor selects samples throughout the period.

9. **Type II report** — Auditor issues the report. Any control exceptions (instances where a control didn't operate as designed) are documented. Too many exceptions result in a qualified opinion.

10. **Annual renewal** — SOC 2 Type II reports cover a specific period. Enterprise customers will want annual reports. The ongoing programme requires continuous evidence collection.

---

## Section 3: Framework Deep Dive

### SOC 2 Common Criteria (CC1–CC9) — Security TSC

**CC1 — Control Environment**
The organisation's control environment — management's commitment to security, integrity and ethical values, oversight by the board, accountability of individuals.

**CC2 — Communication and Information**
How security information is communicated internally and externally — policies communicated, security responsibilities defined, external communications about security commitments.

**CC3 — Risk Assessment**
Formal risk assessment process — identification of objectives, risks that threaten objectives, risk analysis, fraud risk consideration.

**CC4 — Monitoring**
Monitoring activities — separate evaluations, ongoing monitoring, internal audit, remediation of deficiencies.

**CC5 — Control Activities**
Control activities — policies and procedures to achieve security objectives, including technology controls.

**CC6 — Logical and Physical Access Controls** (Most heavily tested)
- CC6.1: Logical access security measures to prevent unauthorised access
- CC6.2: Authentication — new user provisioning, MFA
- CC6.3: Role-based access — least privilege
- CC6.4: Physical access controls
- CC6.5: Logical access removal upon termination
- CC6.6: Network segmentation, boundary protection
- CC6.7: Transmission controls — encryption in transit
- CC6.8: Malicious software protection

**CC7 — System Operations**
- CC7.1: Threat and vulnerability detection
- CC7.2: Anomaly detection and monitoring
- CC7.3: Threat and vulnerability evaluation and response
- CC7.4: Security incident response
- CC7.5: Security incidents causing disclosure

**CC8 — Change Management**
Authorisation and testing of changes to infrastructure, data, software, and procedures.

**CC9 — Risk Mitigation**
Vendor/third-party risk identification and management; business disruption risk mitigation.

---

## Section 4: Common Mistakes Beginners Make

1. **Pursuing SOC 2 without a readiness assessment first.** Diving into a SOC 2 audit without knowing your gaps wastes money (auditors bill by the hour; finding gaps in the audit itself is expensive) and produces a qualified report with exceptions.

2. **Underestimating the evidence burden.** SOC 2 requires evidence of control *operation* over time. This means: access review records from each quarter, change approval records for each change, log review records weekly, incident response test documentation. Evidence collection must start from Day 1 of the observation period.

3. **Confusing SOC 2 with ISO 27001.** SOC 2 is an attestation (auditor opinion on your controls). ISO 27001 is a certification (you comply with a management system standard). They have different criteria, different auditors, and different outputs. Both can be required — many enterprise companies want both.

4. **Not properly scoping sub-service organisations.** AWS, GCP, Azure, and other cloud providers produce their own SOC 2 reports. Your auditor will want to understand how your SOC 2 scope interacts with cloud provider controls. Learn the "carve-out" vs "inclusive" method.

5. **Expecting Type I to satisfy enterprise requirements.** Most enterprise procurement teams require Type II. Type I is a milestone, not the end goal. Set expectations accordingly.

6. **Not tracking exceptions throughout the observation period.** Any control failure during the Type II observation period must be tracked, investigated, and remediated. Auditors will look for exception trends.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Use a compliance automation platform** — Vanta, Drata, Secureframe, or TrustCloud dramatically reduce the evidence collection burden. They integrate with AWS, GitHub, Google Workspace, etc. to auto-collect evidence.
- **Start with Security TSC only** — adding Availability, Confidentiality, or Processing Integrity increases scope, cost, and complexity. Add them in Year 2 when the programme is mature.
- **Read AWS's SOC 2 report** — AWS publishes their SOC 2 report for customers on AWS Artifact. Understanding what AWS covers helps you scope your own controls correctly.
- **The observation period start date matters** — don't start the clock on your Type II observation period until all controls are implemented. A Type I audit buys you time to get controls operational.
- **Treat the readiness assessment as a gap assessment** — use it to identify exactly which CC criteria you fail, then prioritise remediation by CC criterion criticality.
- **SOC 2 and ISO 27001 overlap significantly** — if you're pursuing both, plan the audit schedule to minimise duplication of effort.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [AICPA SOC 2 Overview](https://us.aicpa.org/interestareas/frc/assuranceadvisoryservices/sorhome) — Official TSC description
- [AICPA Trust Services Criteria 2017](https://www.aicpa.org/resources/download/2017-trust-services-criteria-with-2022-points-of-focus-updates) — Full criteria document (free PDF)
- [AWS SOC 2 Compliance](https://aws.amazon.com/compliance/soc-faqs/) — How AWS handles SOC 2
- [Vanta: SOC 2 Academy](https://www.vanta.com/resources/soc-2) — Excellent free guides
- [Secureframe: SOC 2 Guide](https://secureframe.com/hub/soc-2/what-is-soc-2) — Practical implementation guidance
- [CSA Cloud Controls Matrix](https://cloudsecurityalliance.org/research/cloud-controls-matrix/) — Cloud security reference

### Books

- *SOC 2 Examination Basics* by Sonu Nair — Foundational SOC 2 reference
- *Building Security into DevSecOps* by Dan Cornell — Relevant for cloud-native SOC 2 environments

### Online Courses

- [ISACA: SOC for Service Organizations](https://www.isaca.org/) — Professional SOC 2 training
- [Coursera: Cloud Security Basics](https://www.coursera.org/learn/cloud-security-basics) — Cloud fundamentals relevant to SOC 2
- [YouTube: SOC 2 Explained — Simply Cyber](https://www.youtube.com/@SimplyCyber) — Free accessible explanations

### Tools to Explore

- **Vanta** (vanta.com) — Industry-leading SOC 2 automation; free trial available
- **Drata** (drata.com) — Compliance automation with SOC 2 support
- **Secureframe** (secureframe.com) — SOC 2 readiness and automation platform

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (90 min)

- 20 min: SOC 2 framework overview — 5 TSC, Type I vs Type II, who the auditors are
- 20 min: CC6 deep dive — the most critical criteria; what evidence is needed for each CC6 sub-criterion
- 20 min: Cloud-native controls — how AWS services satisfy SOC 2 requirements; what customers must still control
- 15 min: Demonstrate a compliance automation platform (Vanta or Drata) — show how evidence is auto-collected
- 15 min: Introduce StartupStack scenario; identify the most critical SOC 2 gaps from the scenario

### Session B Focus (60 min)

- Review readiness assessment: Are all CC criteria assessed? Are gaps specific and linked to StartupStack's known issues?
- Check evidence checklist: Is evidence realistic (not too easy or too hard to collect)?
- Review 90-day roadmap: Is CC6 addressed early (most critical)? Is CC8 change management realistic for a 50-person startup?

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "What are the 5 SOC 2 Trust Services Criteria?"
2. "What is the difference between SOC 2 Type I and Type II?"
3. "Why do enterprise companies require SOC 2 Type II and not Type I?"
4. "What does CC6 cover?"
5. "How does AWS factor into a SaaS company's SOC 2 report?"
6. "What is a SOC 2 control exception?"
7. "How long does a SOC 2 Type II audit take?"
8. "What's the difference between SOC 2 and ISO 27001?"
9. "What compliance automation tools have you worked with?"
10. "Walk me through how you would prepare a company for their first SOC 2 Type I audit."

### Keywords to Use

- Trust Services Criteria (TSC) — Security, Availability, Confidentiality, PI, Privacy
- Common Criteria CC1–CC9
- Type I (design) vs Type II (operating effectiveness)
- Observation period
- CPA firm / auditor
- Control exception
- Compliance automation — Vanta, Drata, Secureframe
- Sub-service organisation (AWS)
- Evidence collection
- Carve-out vs inclusive method
