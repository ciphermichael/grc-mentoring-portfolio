# Week 12 Learning Guide: Control Testing and Evidence Management

## What You Will Learn This Week

Control testing is the rigorous process of determining whether security controls actually work — not just whether they exist. This is a critical distinction. A policy that says "access reviews occur quarterly" is a control. Evidence that the access review was conducted, completed by the right people, and resulted in access removals is control operating effectiveness. This week you will build a professional control testing workbook and learn the evidence standards required for SOC 2 and ISO 27001 audits.

---

## Section 1: Core Concept Explained

### What Is Control Testing?

Control testing is the systematic process of gathering evidence to determine whether security controls are: (1) suitably designed to achieve their objective, and (2) operating effectively in practice. It is the engine of compliance assurance — you are not just checking that a control exists, but that it works.

There are two dimensions of control assessment:
- **Design effectiveness**: Is the control designed in a way that, if it operates as intended, it would prevent or detect the specified risk? (This is what SOC 2 Type I assesses)
- **Operating effectiveness**: Does the control actually function as designed over time? Is there evidence of consistent operation? (This is what SOC 2 Type II assesses)

**Types of control deficiencies:**
- **Control Gap**: The control doesn't exist at all
- **Control Design Deficiency**: The control exists but is not designed to address the risk (e.g., a lock on an internal door but no lock on the external server room door)
- **Control Operating Deficiency**: The control is designed correctly but not operated consistently (e.g., access reviews scheduled quarterly but only conducted once in the past year)
- **Significant Deficiency**: A material weakness in the control that could lead to material misstatement of financial statements or security failure
- **Material Weakness**: The most severe classification; indicates controls are so deficient that material harm is likely

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **Control Testing** | Systematic evidence gathering to assess control effectiveness | Testing access review process for 15 controls |
| **Design Effectiveness** | Control designed to achieve its objective | MFA policy correctly designed to prevent unauthorised access |
| **Operating Effectiveness** | Control consistently functioning as designed | MFA enforced on all 500 user accounts, evidenced |
| **Control Exception** | A single instance where a control didn't operate | 1 account found without MFA in a 100-account sample |
| **Population** | All items that could potentially be selected for testing | All 3,000 user accounts in Active Directory |
| **Sample** | Subset selected for testing | 25 accounts selected for MFA testing |
| **Evidence** | Documentation proving a control is operating | Access review sign-off record; screenshot of MFA status |
| **Deficiency** | Failure to meet the control requirement | 3 accounts lacking MFA enforcement |
| **Remediation** | Corrective action to fix a deficiency | Enable MFA for the 3 accounts within 48 hours |
| **Control Testing Workbook** | Structured document recording all tests | Excel with 15 controls tested with evidence |
| **Evidence Tag** | Reference linking evidence to its control | EV-001 = "AD user export dated 2025-01-15" |
| **Assertion** | What the control claims to achieve | "All privileged accounts use MFA" |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Control Testing Process

1. **Define the control population** — For each control to be tested, define the complete population. "MFA for all admin accounts" — the population is all accounts in the "Admin" AD security group.

2. **Determine sample size** — Use a risk-based or statistical approach. Higher-risk controls and larger populations require larger samples. Common guidance:
   - Population 1–25: Test all items
   - Population 26–60: Sample 25
   - Population 61–100: Sample 30
   - Population 101–250: Sample 40
   - Population 251+: Sample 60

3. **Define the test approach** — For each control, determine the testing method:
   - **Inquiry**: Interview the control owner about the process
   - **Observation**: Watch the control being performed
   - **Inspection**: Review documentary evidence (policies, records, logs)
   - **Re-performance**: Independently execute the control yourself to verify

4. **Request evidence** — Submit a formal evidence request list to control owners. Be specific about what evidence is needed, in what format, for what time period.

5. **Test the evidence** — Compare evidence against the control assertion. For "quarterly access reviews": Was the review conducted in each quarter? Did it cover all in-scope systems? Did it result in access removals where appropriate? Were exceptions documented?

6. **Document test results** — For each control: test approach, sample size, evidence examined, exceptions found, test conclusion (Effective / Deficient).

7. **Escalate deficiencies** — Exceptions and deficiencies must be reported. Determine severity: is this an isolated exception or a systemic control failure?

8. **Track remediation** — Deficiencies must be remediated and re-tested. Track in a deficiency log with target dates and owners.

### Real Company Example

FinancePro Ltd.'s GRC team, led by GRC Manager Sophie Andrews, conducts quarterly control testing across their SOC 2 and ISO 27001 in-scope systems. Their Q1 testing covers 15 controls across access control, change management, and vulnerability management.

Testing control CC6.3 (Role-based access — least privilege): Sophie requests an export of all user accounts from the Azure AD admin portal, plus the last quarterly access review completion records. Population: 280 user accounts. Sample size: 40 accounts. Test approach: Inspection of account permissions vs approved job role matrix.

Findings: 4 of 40 sampled accounts (10%) have permissions above their job role level. 2 accounts belong to employees who changed roles 3 months ago — their old permissions were never removed. 2 accounts are "super user" accounts with no business justification. Exception rate: 10%.

Assessment: Control Design — Effective (the quarterly access review process is correctly designed). Control Operating — Deficient (the review didn't identify and remove these excess permissions). Severity: High.

Remediation: Remove excess permissions within 5 business days; update the access review checklist to explicitly include role-change review; re-test in Q2.

---

## Section 3: Framework Deep Dive

### Control Testing in ISO 27001 Audits

ISO 27001 internal auditors test controls against Annex A requirements. Key access control tests for ISO 27001:

| Control | Assertion | Evidence Required |
|---------|-----------|------------------|
| A.5.18 — Access rights | Access rights only assigned based on need | Access review records; role matrix; provisioning requests |
| A.8.2 — Privileged access | Privileged accounts separate from regular accounts | AD export showing admin accounts; PAM tool logs |
| A.8.5 — Secure authentication | MFA enforced for all remote access | Azure AD conditional access policy; MFA status export |
| A.6.5 — Termination | Access removed promptly on termination | Offboarding checklist; HR termination records vs AD deactivation date |
| A.8.8 — Vulnerability management | Critical patches applied within SLA | Vulnerability scan reports; patch deployment records |

### SOC 2 Control Testing

SOC 2 auditors test against Trust Services Criteria. For CC6 (Logical and Physical Access), key tests include:

- **CC6.1**: Review access control policy; interview control owner; inspect access review records
- **CC6.2**: Select sample of new users; verify provisioning went through approval workflow
- **CC6.3**: Select sample of users; verify permissions match approved job role
- **CC6.5**: Select sample of terminated employees; verify access removed within SLA
- **CC6.6**: Review network segmentation architecture; test firewall rules; verify VPN configuration

---

## Section 4: Common Mistakes Beginners Make

1. **Testing control existence rather than operating effectiveness.** Finding a policy document says "access reviews occur quarterly" is not evidence that access reviews actually happened. You need the access review completion records, the accounts reviewed, and the actions taken.

2. **Using samples that are too small.** A 3-item sample from a 500-item population cannot support a conclusion about the full population. Use risk-based sample sizes.

3. **Not dating evidence.** Evidence must be from the right period. A screenshot dated from 2022 cannot prove a control operated in 2025. Always check and record evidence dates.

4. **Not documenting the test methodology.** If another auditor cannot reproduce your test from your workbook, your testing is inadequate. Document: what you tested, how you selected the sample, what evidence you reviewed, what you concluded.

5. **Conflating control exceptions with control failures.** A single exception (1 account missed in 500 reviewed) may be an isolated lapse rather than a systemic failure. Context matters. A 20% exception rate is a systemic failure.

6. **Not distinguishing design from operating deficiencies.** These are different problems with different remediation paths. A design deficiency requires redesigning the control; an operating deficiency requires improving how the existing control is executed.

7. **Skipping the remediation follow-up.** Testing that finds deficiencies but doesn't track their remediation provides limited assurance value. Always close the loop.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Use a standardised control testing workbook** — consistent structure allows comparison across quarters and makes review by auditors straightforward.
- **Agree your evidence request list in advance** — don't surprise control owners with evidence requests on the day. Give 5–10 business days notice.
- **Photograph or screenshot everything** — oral evidence ("the IT team told me") is the weakest form. Documentary evidence (screenshots, logs, signed records) is the strongest.
- **Test your top-risk controls more frequently** — access control and privileged access should be tested quarterly; lower-risk controls annually.
- **Build an evidence tag system** — every piece of evidence gets a unique reference (EV-001, EV-002) that links it to the control and test. This makes auditor review much cleaner.
- **The control testing workbook is a key portfolio artefact** — a completed, professional workbook with real test conclusions is one of the most impressive things you can show a GRC hiring manager.
- **Know the difference between a control exception and a control deficiency** — a single exception in 100 tests may be acceptable (1%); consistent exceptions indicate a systemic problem.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [PCAOB AS 2201: Auditing Internal Controls](https://pcaobus.org/Standards/Auditing/Pages/AS2201.aspx) — Professional standard for control testing
- [AICPA: Considering Internal Control](https://www.aicpa.org/resources/article/guide-to-understanding-soc-2-trust-services-criteria) — SOC 2 control considerations
- [ISACA: CISA Review Manual — Control Testing Chapter](https://www.isaca.org/credentialing/cisa) — IS control testing methodology
- [ISO 27001 Clause 9 — Performance Evaluation](https://www.iso.org/standard/27001) — Monitoring and measurement requirements
- [SANS: How to Use Evidence to Support Audit Findings](https://www.sans.org/reading-room/whitepapers/auditing/) — Evidence standards

### Books

- *CISA Review Manual* by ISACA — Chapters 3–4: Control testing and audit evidence
- *IT Audit Handbook* by Chris Davis — Practical control testing methodology

### Online Courses

- [ISACA: Auditing IT Governance](https://www.isaca.org/training-and-events/online-courses) — Control testing in practice
- [SANS: Security Audit Essentials](https://www.sans.org/cyber-security-courses/) — Practical auditing skills
- [LinkedIn Learning: Internal Audit Basics](https://www.linkedin.com/learning/) — Search "internal audit" for free trial access

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (90 min)

- 20 min: Design vs operating effectiveness — use the MFA example to show the difference clearly
- 15 min: Control testing methods — which method for which control type?
- 20 min: Evidence quality — show 3 examples of evidence (weak to strong); discuss what makes each stronger
- 20 min: Sample size guidance — work through 3 sample size decisions together using the population table
- 15 min: Control deficiency rating — when is an exception a deficiency? When is it a systemic failure?

### Session B Focus (60 min)

- Review control testing workbook: Are test approaches documented? Are sample sizes appropriate?
- Check evidence inventory: Are evidence items tagged? Dated? From the correct period?
- Review deficiency register: Are severities consistently applied?
- Ask: "You found that 10% of sampled accounts have excessive permissions. How do you determine if this is a critical finding or a minor observation?"

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "What is the difference between design effectiveness and operating effectiveness?"
2. "Walk me through how you test an access control."
3. "What are the 4 types of control testing evidence?"
4. "How do you determine sample size for control testing?"
5. "What is a control exception vs a control deficiency?"
6. "What is a material weakness?"
7. "What evidence would you collect to test that quarterly access reviews are occurring?"
8. "How do you document control testing for an auditor review?"
9. "What is the difference between an internal control review and an audit?"
10. "Tell me about a control deficiency you identified and how it was remediated."

### Keywords to Use

- Design effectiveness vs operating effectiveness
- Inquiry, observation, inspection, re-performance
- Population and sample size
- Control exception rate
- Evidence tag / evidence inventory
- Deficiency severity: material weakness, significant deficiency, minor deficiency
- SOC 2 Common Criteria (CC6 for access control)
- ISO 27001 Clause 9.1 (monitoring and measurement)
- Corrective action tracking
- Control testing workbook
