# Week 16 Learning Guide: CIS Controls and Cross-Framework Mapping

## What You Will Learn This Week

The CIS Critical Security Controls (CIS Controls v8) are a prioritised set of 18 proven defensive actions designed by practitioners, for practitioners. Unlike ISO 27001 (certification-focused) or NIST CSF (strategy-focused), CIS Controls are operational — they tell you exactly what to implement, in what order, to most effectively reduce your risk of the most common attacks. This week you also develop the critical GRC skill of cross-framework mapping — the ability to translate between ISO 27001, NIST CSF, and CIS Controls, which is essential when managing multi-framework compliance programmes.

---

## Section 1: Core Concept Explained

### What Are the CIS Critical Security Controls?

The CIS Controls (now v8) are published by the Center for Internet Security (CIS), a non-profit community of cybersecurity practitioners. They represent the consensus best practices of the global security community — distilled from real-world incident data, threat intelligence, and practitioner experience. The key principle: implement these controls in priority order to eliminate the vast majority of the attack surface.

**Version 8 (2021) organisation**: 18 Control Groups | 153 Safeguards | 3 Implementation Groups

**The 18 CIS Control Groups:**
1. Inventory and Control of Enterprise Assets
2. Inventory and Control of Software Assets
3. Data Protection
4. Secure Configuration of Enterprise Assets and Software
5. Account Management
6. Access Control Management
7. Continuous Vulnerability Management
8. Audit Log Management
9. Email and Web Browser Protections
10. Malware Defenses
11. Data Recovery
12. Network Infrastructure Management
13. Network Monitoring and Defense
14. Security Awareness and Skills Training
15. Service Provider Management
16. Application Software Security
17. Incident Response Management
18. Penetration Testing

**Implementation Groups (IGs)**: The 153 safeguards are grouped into 3 priority levels:
- **IG1 (56 safeguards)**: Basic cyber hygiene — the minimum every organisation should implement. Designed for SMBs with limited security budgets and expertise.
- **IG2 (74 additional safeguards)**: For organisations with moderate security resources. Addresses more complex threats.
- **IG3 (23 additional safeguards)**: For organisations with mature security programmes facing sophisticated, targeted attacks.

**The IG1 "essential controls"** address the most common attack vectors. Studies show that implementing IG1 alone eliminates the risk from approximately 85% of common cyberattacks.

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **CIS Controls** | 18 prioritised control groups | CIS Control 7: Continuous Vulnerability Management |
| **CIS Safeguard** | Specific action within a control group | 7.1: Establish and Maintain a Vulnerability Management Process |
| **IG1** | Implementation Group 1 — basic hygiene (56 safeguards) | All organisations should implement IG1 |
| **IG2** | Implementation Group 2 — moderate security (74 additional) | Companies with dedicated IT/security teams |
| **IG3** | Implementation Group 3 — advanced (23 additional) | Sophisticated/regulated organisations |
| **Cross-Framework Mapping** | Connecting equivalent controls across frameworks | CIS 5 (Account Management) maps to ISO A.5.15–5.18 |
| **CIS Benchmark** | Configuration hardening guide for specific technologies | CIS AWS Foundations Benchmark, CIS Windows 10 |
| **CCTHQ** | CIS Controls online tool | Used to assess and track control implementation |
| **Cyber Insurance** | Insurance covering cybersecurity incident costs | Underwriters use CIS IG1 compliance as a rating factor |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Real-World CIS Controls Assessment Process

1. **Determine the appropriate IG level** — Small businesses with no dedicated security staff should implement IG1. Organisations with dedicated IT security teams should implement IG1 + IG2. Highly regulated or targeted organisations should implement all three.

2. **Obtain the CIS Controls v8 document** — Free download from cisecurity.org. Review all 18 controls and their safeguards.

3. **Conduct a self-assessment** — For each safeguard, assess: Not Implemented / Partially Implemented / Fully Implemented. This is typically done through staff interviews and evidence review.

4. **Prioritise by IG level** — All IG1 safeguards must be implemented before IG2; all IG2 before IG3.

5. **Build an implementation roadmap** — Assign owners to each safeguard gap. Sequence implementation by risk priority within IG1 first.

6. **Map to existing frameworks** — If the organisation also has ISO 27001 or NIST CSF, map CIS controls to those frameworks to identify overlaps and avoid duplicate work.

7. **Track implementation progress** — Use a tracker (spreadsheet or CIS CSAT tool) to monitor progress across all safeguards.

8. **Use CIS Benchmarks for technical hardening** — CIS publishes detailed configuration hardening benchmarks for hundreds of technologies (Windows, Linux, AWS, Azure, M365, Docker, Kubernetes). These are the "how to implement" guides for the control framework.

### Real Company Example

SMBTech is a 75-person manufacturing company that has just applied for cyber insurance. Their insurer, CyberGuard, has declined their application citing "insufficient basic security hygiene." The policy requires at minimum: asset inventory, MFA on all accounts, regular patching, email filtering, and working backups — all of which correspond to CIS IG1 safeguards.

GRC Consultant Amy Chen conducts a CIS IG1 assessment of SMBTech. Out of 56 IG1 safeguards, she finds:
- 22 fully implemented
- 18 partially implemented
- 16 not implemented

Critical gaps: No formal asset inventory (CIS 1) — 3 servers were completely unknown to IT. No MFA on email (CIS 5.6). Email filtering missing (CIS 9). No tested backup process (CIS 11.2).

Amy builds a 90-day remediation plan focusing on the 16 not-implemented safeguards. After 90 days of implementation, SMBTech reapplies for cyber insurance with a 34% reduction in premium compared to their first application. The insurer is satisfied with IG1 compliance evidence.

---

## Section 3: Framework Deep Dive

### Cross-Framework Mapping: CIS v8 ↔ ISO 27001 ↔ NIST CSF

CIS publishes official cross-framework mappings on cisecurity.org. Key mappings:

| CIS Control | CIS Safeguard (example) | ISO 27001 Mapping | NIST CSF Mapping |
|-------------|------------------------|-------------------|------------------|
| CIS 1 (Asset Management) | 1.1: Establish asset inventory | A.5.9 (Asset inventory) | ID.AM-01 |
| CIS 5 (Account Management) | 5.3: Disable dormant accounts | A.5.18 (Access rights) | PR.AA-01 |
| CIS 6 (Access Control) | 6.4: Require MFA | A.8.5 (Secure auth) | PR.AA-01 |
| CIS 7 (Vulnerability Management) | 7.4: Perform automated patch management | A.8.8 (Vuln management) | ID.RA-01 |
| CIS 8 (Audit Log Management) | 8.2: Collect audit logs | A.8.15 (Logging) | DE.AE-03 |
| CIS 10 (Malware Defenses) | 10.1: Deploy anti-malware | A.8.7 (Malware protection) | PR.DS-01 |
| CIS 11 (Data Recovery) | 11.1: Establish and maintain data recovery | A.5.30 (ICT readiness) | RC.RP-01 |
| CIS 17 (Incident Response) | 17.1: Designate personnel to manage incidents | A.5.24 (IR planning) | RS.MA-01 |

**The value of cross-framework mapping:** An organisation implementing CIS IG1 addresses approximately 60% of ISO 27001 Annex A controls and approximately 70% of NIST CSF IG1 subcategories simultaneously. Mapping prevents organisations from treating frameworks as separate compliance exercises when they can be unified.

---

## Section 4: Common Mistakes Beginners Make

1. **Treating CIS Controls as optional for small companies.** CIS IG1 is described as "essential cyber hygiene" — 56 safeguards that every organisation regardless of size should implement. The consequences of not implementing them (ransomware, phishing, supply chain attacks) don't scale with company size.

2. **Starting with IG3 before completing IG1.** The implementation group sequencing is intentional. IG1 provides the foundational hygiene that makes IG2 and IG3 effective. Skipping ahead wastes effort.

3. **Confusing CIS Controls with CIS Benchmarks.** CIS Controls are the what (what controls to implement). CIS Benchmarks are the how (specific configuration settings for specific technologies). Both are needed for a complete implementation.

4. **Mapping frameworks incorrectly.** Mappings are rarely 1:1. CIS Control 7 (Vulnerability Management) maps to multiple ISO 27001 controls (A.8.8, A.8.20, A.8.29) and multiple NIST CSF subcategories. Understand the mapping nuances.

5. **Not using CIS Benchmarks for technical hardening.** The CIS Controls describe what to do. The CIS Benchmarks tell you exactly how to configure each technology (exact registry settings, service configurations). Ignoring the benchmarks leaves significant gaps.

6. **Not tracking implementation with evidence.** "We implemented MFA" without a screenshot of Azure AD conditional access policy enforcing MFA is not verifiable. Evidence is required for audit and insurance purposes.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Use the CIS CSAT (CIS Controls Self Assessment Tool)** — free tool that tracks implementation status against all 153 safeguards.
- **CIS Benchmarks are gold for hardening projects** — if you're hardening AWS, Windows Server, or M365, the CIS Benchmark is the authoritative guide.
- **Cyber insurance companies love CIS IG1** — many insurers use CIS IG1 compliance as a standard in their security questionnaires. If you're helping a client with cyber insurance, map their controls to CIS IG1.
- **Cross-framework mapping saves enormous effort** — an organisation implementing ISO 27001 who also needs NIST CSF alignment: use the cross-framework mapping to show how ISO 27001 controls satisfy NIST CSF subcategories.
- **CIS Controls v8 is publicly free** — download it, study it, reference it in your portfolio work.
- **Know which CIS controls address the most common attack vectors** — ransomware is primarily addressed by CIS 1 (asset visibility), CIS 7 (patching), CIS 10 (malware defenses), and CIS 11 (backup). Phishing is primarily addressed by CIS 9 (email filtering) and CIS 14 (awareness training).

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [CIS Controls v8 — Full Document](https://www.cisecurity.org/controls/v8) — Free download; essential reading
- [CIS Controls v8 Mapping to ISO 27001](https://www.cisecurity.org/cybersecurity-tools) — Official cross-framework mapping
- [CIS Controls v8 Mapping to NIST CSF](https://www.cisecurity.org/cybersecurity-tools) — Official mapping
- [CIS Benchmarks Directory](https://www.cisecurity.org/cis-benchmarks/) — Free hardening guides for 100+ technologies
- [CIS CSAT Tool](https://csat.cisecurity.org/) — Free CIS Controls self-assessment tool
- [NCSC Cyber Essentials to CIS Mapping](https://www.ncsc.gov.uk/cyberessentials/overview) — UK baseline aligned to CIS IG1

### Books

- *CIS Controls v8 Implementation Guide* — CIS — Free download from cisecurity.org
- *Cybersecurity First Principles* by Roger Grimes — Covers CIS Controls in practical context

### Online Courses

- [SANS: Implementing and Auditing CIS Controls (SEC566)](https://www.sans.org/cyber-security-courses/implementing-auditing-security-frameworks-controls/) — Professional-level course
- [CIS: Online CIS Controls Training](https://www.cisecurity.org/cis-controls-academy) — Official CIS training
- [YouTube: CIS Controls v8 Explained — Simply Cyber](https://www.youtube.com/@SimplyCyber) — Free accessible explanations

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (90 min)

- 20 min: CIS Controls v8 overview — all 18 control groups; IG1/IG2/IG3 explained
- 20 min: IG1 deep dive — walk through the 56 IG1 safeguards; discuss which are most commonly missing in SMBs
- 25 min: Cross-framework mapping exercise — for CIS Controls 1, 5, 6, 7, map to ISO 27001 and NIST CSF together
- 15 min: Introduce SMBTech scenario; discuss cyber insurance context and why CIS IG1 matters for insurability
- 10 min: Show the CIS CSAT tool; demonstrate how to track implementation

### Session B Focus (60 min)

- Review CIS IG1 assessment: Are implementation statuses honest? Are the critical gaps identified?
- Check cross-framework mapping: Are mappings accurate? Nuanced (not 1:1 assumptions)?
- Review implementation roadmap: Prioritised by IG1 first? Quick wins identified?
- Ask: "SMBTech's insurer requires MFA on all accounts. Which CIS safeguard(s) address this and which ISO 27001 control does it map to?"

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "Walk me through the CIS Critical Security Controls."
2. "What are the three Implementation Groups?"
3. "What does IG1 cover and why is it important for SMBs?"
4. "How does CIS Controls v8 map to ISO 27001?"
5. "Why would a company use CIS Controls rather than ISO 27001?"
6. "What is a CIS Benchmark and how is it different from CIS Controls?"
7. "How do you assess an organisation's CIS Controls compliance?"
8. "Which CIS controls specifically address ransomware prevention?"
9. "What is cross-framework mapping and why is it valuable?"
10. "How does CIS IG1 relate to cyber insurance requirements?"

### Keywords to Use

- CIS Controls v8 — 18 control groups, 153 safeguards
- Implementation Groups — IG1 (basic hygiene), IG2 (moderate), IG3 (advanced)
- CIS Benchmarks — technology-specific hardening guides
- Cross-framework mapping — CIS to ISO 27001 to NIST CSF
- CIS CSAT tool
- Cyber insurance readiness
- Asset inventory (CIS 1) — foundational control
- Multi-factor authentication (CIS 5.6, 6.4)
- Vulnerability management (CIS 7)
- Backup and recovery (CIS 11)
