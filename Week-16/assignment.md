# Week 16 Assignment: CIS Controls and Cross-Framework Mapping

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | SMBTech |
| **Your Role** | GRC Consultant |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟🌟 |
| **Frameworks** | CIS Controls v8 (IG1 + IG2), ISO 27001:2022, NIST CSF 2.0 |

---

## Scenario Brief — Read This Carefully

**SMBTech** is a 75-person UK software development company based in Leeds, providing custom software solutions to the retail sector. They employ 35 developers, 15 project managers, 15 sales and account staff, and 10 in admin/finance. Their IT environment includes: 75 Windows 11 laptops, Microsoft 365 (Teams, SharePoint, Exchange), a self-managed Azure development environment (5 virtual machines), GitHub Enterprise for source code, Jira for project management, and a 3rd party payroll provider.

SMBTech processes limited personal data: employee HR records, client contact information, and occasional contractor data. They do not process payment card data or health data.

SMBTech has applied for a cyber liability insurance policy. Their insurer, CyberArmour, has declined to offer coverage until SMBTech demonstrates "basic cyber hygiene aligned to an industry standard security framework." The account manager from CyberArmour specifically mentioned CIS Controls v8 IG1 as the minimum acceptable standard.

Additionally, SMBTech's largest client — SupplyChain Global (a FTSE 250 retailer) — has sent a security questionnaire asking: "Do you comply with any recognised cybersecurity framework? If so, which controls are in place?" The CTO, Marcus Green, has asked you to assess their CIS Controls compliance and produce both a cyber insurance readiness report and a response to SupplyChain Global's questionnaire.

**Known current state:**
- Asset inventory: Managed via spreadsheet; last updated 8 months ago; likely incomplete (3 Azure VMs may be unlisted)
- Patch management: Windows Update set to automatic; Azure VMs patched manually; no formal process
- MFA: Enabled for Microsoft 365 admin accounts; not enabled for regular employee accounts
- Email filtering: Basic spam filter in Microsoft 365; no advanced anti-phishing
- Backups: Microsoft 365 data in Recycle Bin / 30-day retention; Azure VMs: no backup configured
- Security awareness training: No formal programme; phishing training was done "about 2 years ago"
- Endpoint detection: Microsoft Defender enabled (basic); no EDR
- Privileged access: No separation of admin and regular accounts; 8 people have Microsoft 365 admin access
- Logging: No centralised logging; Azure Activity Log enabled but not reviewed

---

## Before You Start

### Pre-Work Checklist
- [ ] Read `learning-guide.md` for Week 16 — especially the 18 control groups and IG1/IG2 definitions
- [ ] Download CIS Controls v8 from cisecurity.org (free)
- [ ] Read the CIS Controls v8 mapping to ISO 27001 (also free at cisecurity.org)
- [ ] Understand what CIS IG1 specifically requires for account management and MFA

### Questions to Answer Before Starting
1. CIS Control 5 (Account Management) Safeguard 5.6 requires: "Use dedicated workstations for all administrative tasks, or administrative users who need standard user access and administrative access should have two separate accounts." Does SMBTech meet this? What's the gap?
2. SMBTech has no formal backup for Azure VMs. Which CIS Control and safeguard covers backup? Is this an IG1 requirement?
3. CIS IG1 Safeguard 6.4 requires MFA for all user access. SMBTech has MFA only for Microsoft 365 admin accounts. What is the gap?
4. SMBTech's email filtering is basic. Which CIS Control addresses email security?
5. SMBTech has 8 Microsoft 365 admin accounts. CIS Control 5 suggests minimum admin accounts. What should the target number be?

---

## Deliverables

### Deliverable 1: CIS Controls v8 Assessment (IG1 and IG2)

**What It Is:** A comprehensive assessment of SMBTech's current implementation of all CIS IG1 safeguards (56) and selected IG2 safeguards most relevant to their environment.

**Step-by-Step Instructions:**

1. Create a spreadsheet with tabs: IG1 Assessment | IG2 Assessment | Summary Dashboard

2. **IG1 Assessment tab** — list all 56 IG1 safeguards. For each:
   - CIS Control number (1–18)
   - Safeguard ID (e.g., 1.1, 5.6)
   - Safeguard description
   - Implementation Status: Not Implemented / Partially Implemented / Fully Implemented
   - Evidence / Current State (what SMBTech does or doesn't do)
   - Gap Description (what is missing)
   - Priority (Critical/High/Medium/Low based on SMBTech's risk context)
   - Recommended Action (specific and actionable)
   - Owner (role responsible)
   - Effort (Low/Medium/High)
   - Estimated cost

3. Apply SMBTech's known gaps. Key assessments:
   - CIS 1.1 (Establish and maintain enterprise asset inventory): Partially — spreadsheet exists but outdated; 3 Azure VMs potentially unlisted → HIGH gap
   - CIS 5.6 (Centralise Account Management): Not Implemented — 8 M365 admins with no separation; no PAM → HIGH
   - CIS 6.4 (Require MFA): Partially — M365 admin only; 75 regular users without MFA → CRITICAL
   - CIS 9.2 (Use DNS filtering services): Not Implemented — basic spam filter only → HIGH
   - CIS 11.1 (Establish and maintain a data recovery practice): Not Implemented — Azure VMs have no backup → CRITICAL
   - CIS 14.2 (Train workforce members to recognise social engineering): Partially — training done 2 years ago; not annual → HIGH
   - CIS 8.2 (Collect audit logs): Partially — Azure Activity Log enabled but not reviewed → MEDIUM

4. **Summary Dashboard tab**: IG1 completion: X of 56 safeguards fully implemented (X%). Top 10 critical gaps. Traffic light overview by CIS Control group.

---

### Deliverable 2: Cross-Framework Mapping (CIS to ISO 27001 to NIST CSF)

**What It Is:** A mapping document showing how CIS Controls v8 safeguards map to ISO 27001 Annex A controls and NIST CSF 2.0 subcategories.

**Instructions:**

1. Create a mapping table covering all 18 CIS Control groups, showing the primary ISO 27001 and NIST CSF equivalents.

2. **Detailed mapping for SMBTech's 10 most critical gaps** — for each gap:
   - CIS safeguard reference
   - What the CIS safeguard requires
   - ISO 27001 equivalent control (with Annex A reference)
   - NIST CSF 2.0 subcategory equivalent
   - Whether addressing the CIS gap also closes the ISO/NIST gap

3. Write a 1-page narrative: "For SMBTech, implementing the 10 critical CIS IG1 gaps will simultaneously address [X] ISO 27001 Annex A controls and [Y] NIST CSF subcategories. This creates significant efficiency — rather than treating CIS compliance as a separate exercise, remediation of CIS gaps advances all three frameworks simultaneously."

---

### Deliverable 3: Implementation Priority List (Top 15 Controls)

**What It Is:** A prioritised remediation list for SMBTech, ordering the 15 most critical IG1 gaps in recommended implementation sequence.

**For each item:**
- Priority rank (1 = most urgent)
- CIS safeguard reference and description
- Why this rank? (risk justification)
- Specific implementation action (tool or process to implement)
- Estimated cost (free/low-cost solutions prioritised for SMBTech)
- Estimated time to implement
- Owner

**Priority guidance:**
- P1 (Implement within 2 weeks): MFA for all accounts, Azure VM backups, reduce M365 admin accounts
- P2 (Implement within 30 days): Advanced email filtering, asset inventory cleanup, Azure Activity Log review process
- P3 (Implement within 90 days): Formal security awareness training, EDR upgrade, centralised logging

---

### Deliverable 4: Cyber Insurance Readiness Checklist

**What It Is:** A checklist demonstrating SMBTech's CIS IG1 readiness for CyberArmour's insurance assessment, showing current state, gap, and remediation status.

**Format:**
| Control Area | CyberArmour Requirement | CIS Ref | Current Status | Gap | Remediation Plan | Target Date |
|---|---|---|---|---|---|---|
| MFA | MFA on all accounts | 6.4 | Admin only | 75 user accounts without MFA | Enable M365 MFA for all users | [30 days] |

Cover the standard cyber insurance control areas: MFA, email filtering, EDR, backup and recovery, vulnerability patching, privileged access management, security awareness training, incident response plan.

---

### Deliverable 5: Implementation Roadmap (with Cost Estimates)

**What It Is:** A 90-day roadmap for implementing the top 15 CIS IG1 gaps, with free and low-cost solutions appropriate for a 75-person company.

**Structure:**
- Week 1–2: Quick wins (zero cost)
  - Enable MFA for all 75 M365 users (free — already licensed)
  - Reduce M365 admin accounts from 8 to 3 (free)
  - Review and update asset inventory (free — 4 person-hours)
  - Enable Azure VM backups (Azure Backup: ~£50/month for 5 VMs)

- Month 1: High-impact, low-cost
  - Implement Microsoft Defender for Business (EDR upgrade) — ~£3/user/month = £225/month
  - Enable Microsoft Defender anti-phishing and safe links — included in M365 Business Premium (~£20/user/month)
  - Establish formal security awareness training — KnowBe4 or Proofpoint ~£10/user/year = £750/year

- Month 2–3: Process improvements
  - Implement formal patch management procedure (free — documented process)
  - Set up Azure Monitor and Log Analytics for centralised logging (~£100/month)
  - Implement quarterly access reviews for Azure and M365 (free — process change)
  - Create Incident Response plan (free — document-based)

**Total estimated investment**: Year 1: ~£8,400 | Ongoing: ~£5,400/year

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| IG1 Assessment Quality | 30% | All 56 safeguards assessed; gaps specific to SMBTech; realistic status |
| Cross-Framework Mapping | 25% | Accurate mappings; efficiency of combined approach demonstrated |
| Implementation Roadmap | 25% | Realistic for SMBTech's size/budget; quick wins identified; cost estimates |
| Professional Quality | 20% | Board-ready documents; correct CIS/ISO/NIST terminology |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **CIS Controls v8 (IG1 + IG2)** | Full IG1 assessment; IG2 selected safeguards assessed |
| **ISO 27001:2022 Annex A** | Cross-mapped to CIS safeguards |
| **NIST CSF 2.0** | Cross-mapped to CIS safeguards |

---

## Week-Specific Resources

- [CIS Controls v8 Free Download](https://www.cisecurity.org/controls/v8) — Essential; download and reference throughout
- [CIS CSAT Tool](https://csat.cisecurity.org/) — Free self-assessment tool; use to structure assessment
- [CIS Controls v8 to ISO 27001 Mapping](https://www.cisecurity.org/cybersecurity-tools) — Official mapping document
- [CIS Controls v8 to NIST CSF Mapping](https://www.cisecurity.org/cybersecurity-tools) — Official mapping document
- [CIS Microsoft 365 Benchmark](https://www.cisecurity.org/cis-benchmarks/) — M365 hardening guide relevant to SMBTech
- [NCSC Cyber Essentials](https://www.ncsc.gov.uk/cyberessentials/overview) — UK baseline aligned to CIS IG1

---

## Submission

```
Week-16/Deliverables/
├── SMBTech-CIS-Controls-Assessment-IG1-IG2-v1.0.xlsx
├── SMBTech-Cross-Framework-Mapping-CIS-ISO-NIST-v1.0.xlsx
├── SMBTech-Top15-Implementation-Priority-v1.0.md
├── SMBTech-Cyber-Insurance-Readiness-Checklist-v1.0.xlsx
└── SMBTech-CIS-Implementation-Roadmap-90Day-v1.0.xlsx
```
