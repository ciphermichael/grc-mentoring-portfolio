# Week 12 Assignment: Control Testing and Evidence Management

## Assignment Overview

| Field | Detail |
|-------|--------|
| **Client** | FinancePro Ltd. |
| **Your Role** | GRC Analyst / Controls Assessor |
| **Estimated Time** | 8–12 hours |
| **Difficulty** | 🌟🌟🌟🌟 |
| **Frameworks** | ISO 27001:2022, SOC 2 (Common Criteria), NIST CSF 2.0 |

---

## Scenario Brief — Read This Carefully

**FinancePro Ltd.** is a 800-person UK financial services company providing investment management software to regulated wealth management firms. They are CREST-certified, ISO 27001 certified (certification due for renewal in 8 months), and currently preparing for their first SOC 2 Type II audit (their largest US client — Meridian Capital — has required one).

Their quarterly internal control testing programme is managed by the GRC Team. This quarter's control testing covers 15 controls across Access Control, Change Management, and Vulnerability Management. The GRC team has requested your assistance in completing the Q1 control testing workbook for this quarter.

**Known context:**
- Last access review: Conducted 3 months ago; some accounts flagged but not all actioned
- Change management: Formal process exists; CAB (Change Advisory Board) meets weekly
- Vulnerability management: Qualys scanner in use; patches applied but cadence not always within SLA
- MFA: Enforced for all M365 accounts; inconsistent for legacy applications
- Privileged access: CyberArk PAM deployed for network infrastructure; not yet for application servers

---

## Deliverables

### Deliverable 1: Control Testing Workbook (15 Controls Tested)

**What It Is:** A professional testing workbook documenting all 15 control tests with methodology, sample, evidence, and conclusions.

**15 Controls to Test:**

**Access Control (Controls 1–6):**
1. CC6.2 / A.5.16: User provisioning — new accounts created only with manager approval
2. CC6.3 / A.5.18: Access rights — access based on least privilege; role matrix exists and is followed
3. CC6.5 / A.6.5: Offboarding — access removed within 24 hours of termination
4. CC6.2 / A.8.5: MFA — all M365 accounts enforce MFA
5. A.8.2: Privileged access — admin accounts separated from regular accounts (PAM used for network infra)
6. A.5.18: Access reviews — quarterly access reviews completed for all in-scope systems

**Change Management (Controls 7–10):**
7. CC8.1 / A.8.32: Change authorisation — all production changes have CAB approval
8. CC8.1: Emergency changes — emergency changes documented and retrospectively approved
9. CC8.1: Testing — all changes tested in non-production before production deployment
10. A.8.32: Post-implementation review — changes reviewed within 5 days of deployment

**Vulnerability Management (Controls 11–15):**
11. A.8.8: Scanning — internal vulnerability scans conducted weekly
12. A.8.8: Critical patch SLA — Critical CVEs patched within 48 hours of release
13. A.8.8: High patch SLA — High CVEs patched within 7 days
14. CC7.1: Penetration testing — annual penetration test conducted and findings tracked
15. A.8.8: Remediation tracking — all open vulnerabilities tracked in a remediation register

**For each control, document:**
- Control ID | Framework Ref | Control Assertion | Population | Sample Size | Testing Method (Inquiry/Observation/Inspection/Re-performance) | Evidence Examined | Evidence Reference | Exceptions Found | Exception Rate | Test Conclusion (Effective/Deficient) | Deficiency Severity (if applicable)

**Introduce realistic exceptions in the workbook:**
- Control 3 (Offboarding): 2 of 30 sampled terminations — access removed in 72 hours, not 24. [Deficiency: Low]
- Control 5 (PAM): Application servers not yet in PAM scope despite being in SOC 2 scope. [Deficiency: High]
- Control 12 (Critical patch SLA): 1 of 5 Critical CVEs patched in 5 days (exceeded 48hr SLA). [Deficiency: Medium]
- Control 6 (Access reviews): Legacy application quarterly review not completed this quarter. [Deficiency: High]
- All other controls: Effective

---

### Deliverable 2: Evidence Inventory and Tagging System

**What It Is:** A complete inventory of all evidence collected for the 15 controls, with a tagging system that links evidence to specific controls.

**Create a structured spreadsheet:**
Evidence Tag | Control Tested | Evidence Description | Evidence Type (Document/Screenshot/Log/Interview Record) | Date Collected | Source System | Covers Period | Collected By | Storage Location

**Complete with at least 30 evidence items (2+ per control):**

Example rows:
- EV-001 | Control 1 (User Provisioning) | ServiceNow new user request tickets — Q1 2025 sample of 25 | Document | 2025-01-15 | ServiceNow | Jan–Mar 2025 | [Your Name] | GRC-Evidence/Q1-2025/Access-Control/
- EV-002 | Control 1 | AD user creation date export showing accounts created Jan–Mar 2025 | Screenshot | 2025-01-15 | Active Directory | Jan–Mar 2025 | [Your Name] | GRC-Evidence/Q1-2025/Access-Control/
- EV-003 | Control 3 (Offboarding) | HR termination records Q1 2025 — 30 terminations | Document | 2025-01-16 | Workday HR | Jan–Mar 2025 | [Your Name] | GRC-Evidence/Q1-2025/Access-Control/

---

### Deliverable 3: Control Deficiency Register

**What It Is:** A register of all deficiencies found, with root cause analysis, severity, and remediation tracking.

**For each of the 4 deficiencies found:**
- Deficiency ID | Control Reference | Deficiency Title | Deficiency Description (specific, factual) | Root Cause | Risk (what harm could result) | Severity | Owner | Remediation Required | Target Date | Status

**Severity definitions to apply:**
- **Critical**: Material weakness; likely to result in audit qualification or regulatory breach
- **High**: Significant control gap; risk of material harm if not remediated quickly
- **Medium**: Control operating below required standard; risk manageable in short term
- **Low**: Minor gap; low likelihood of harm; best practice improvement needed

---

### Deliverable 4: Control Effectiveness Dashboard

**What It Is:** A visual summary dashboard showing control testing results across all 15 controls this quarter.

**Create a dashboard showing:**
- Summary: Total controls tested | Effective | Deficient | Deficiency by severity (Critical/High/Medium/Low)
- Control effectiveness rate: X of 15 controls effective = X%
- Bar chart or table: Effective vs Deficient by domain (Access Control / Change Management / Vulnerability Management)
- Trend vs last quarter: Are controls improving, stable, or deteriorating?
- Top risks: The 2 highest-severity deficiencies highlighted
- RAG status per control domain: Red (multiple High/Critical deficiencies) / Amber (1 High deficiency) / Green (effective or Low deficiencies only)

---

### Deliverable 5: Remediation Recommendations Report (2 pages)

**What It Is:** A concise management report presenting control test results and prioritised remediation recommendations.

**Structure:**
1. Executive Summary: Q1 testing results; overall control effectiveness rating; top 3 recommendations
2. Findings Overview: Summary table of all 4 deficiencies with severity and deadline
3. Detailed Recommendations (for High/Critical deficiencies):
   - Deficiency description
   - Root cause
   - Recommended remediation (specific: tool, process change, or policy update)
   - Resource required
   - Target date
   - Risk if not remediated
4. Positive Findings: What is working well (at least 3 effective controls to highlight)
5. Q2 Testing Priorities: What the next quarter's testing should focus on based on this quarter's findings

---

## Grading Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Testing Workbook Quality | 35% | All 15 controls tested; correct methodology; exception rates calculated |
| Evidence Inventory | 20% | Evidence correctly tagged, described, and dated |
| Deficiency Register | 25% | Root causes analysed; severities calibrated; remediations specific |
| Reporting Quality | 20% | Dashboard visual and clear; report board-ready |

---

## Frameworks Applied

| Framework | How Applied |
|-----------|------------|
| **ISO 27001:2022** | Controls tested against Annex A: A.5.16, A.5.18, A.6.5, A.8.2, A.8.5, A.8.8, A.8.32 |
| **SOC 2 Common Criteria** | Controls mapped to CC6 (access), CC7 (operations), CC8 (change management) |
| **NIST CSF 2.0** | PROTECT and DETECT functions alignment |

---

## Week-Specific Resources

- [AICPA: SOC 2 Common Criteria](https://us.aicpa.org/interestareas/frc/assuranceadvisoryservices/sorhome) — CC1–CC9 descriptions
- [PCAOB AS 2201: Internal Control Testing](https://pcaobus.org/Standards/Auditing/Pages/AS2201.aspx) — Professional testing standards
- [ISACA: CISA Manual — Control Testing](https://www.isaca.org/credentialing/cisa) — IS control testing methodology
- [CyberArk PAM Overview](https://www.cyberark.com/what-is/privileged-access-management/) — PAM context for Control 5
- [Qualys Vulnerability Management](https://www.qualys.com/apps/vulnerability-management/) — Context for vulnerability management testing
- [SANS: Evidence Collection for Auditors](https://www.sans.org/reading-room/whitepapers/auditing/) — Audit evidence standards

---

## Submission

```
Week-12/Deliverables/
├── FinancePro-Control-Testing-Workbook-Q1-2025-v1.0.xlsx
├── FinancePro-Evidence-Inventory-Q1-2025-v1.0.xlsx
├── FinancePro-Control-Deficiency-Register-Q1-2025-v1.0.xlsx
├── FinancePro-Control-Effectiveness-Dashboard-Q1-2025.xlsx
└── FinancePro-Remediation-Recommendations-Q1-2025-v1.0.md
```
