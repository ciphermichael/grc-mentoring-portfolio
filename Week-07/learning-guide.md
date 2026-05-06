# Week 07 Learning Guide: Security Policy Development

## What You Will Learn This Week

Every mature security programme is built on a foundation of well-written, enforced policies. This week you will write professional, audit-ready security policies — the actual documents that govern how an organisation's employees, contractors, and partners must behave with respect to information security. Policy writing is one of the most common daily tasks for GRC analysts, and doing it well — clearly, specifically, and with proper governance structure — is a skill that directly demonstrates professional competence to employers.

---

## Section 1: Core Concept Explained

### What Is a Security Policy?

A security policy is a **formal, board-approved document** that states management's intent, direction, and commitment on a specific security topic. Policies are:
- **Mandatory** — employees must comply; non-compliance has consequences
- **High-level** — they state *what* must happen, not *how* (that's for standards and procedures)
- **Board or senior management approved** — demonstrating top-down commitment
- **Reviewed regularly** — typically annually or when significant changes occur

The policy hierarchy works like this:

> **Policy** (Board-approved, principles-based) → **Standard** (Management-approved, specific requirements) → **Procedure** (Operational instructions, step-by-step) → **Guideline** (Best practice advice, recommended but not mandatory)

For example: The **Access Control Policy** (what) states "All access to information systems must be based on least privilege." The **Access Control Standard** (how) specifies "User accounts must be reviewed quarterly; privileged accounts must use PAM tooling; MFA is mandatory for all admin accounts." The **User Provisioning Procedure** (steps) details the exact steps to create a user account, assign roles, and request manager approval.

**ISO 27001 requirement:** Clause 5.2 requires a board-approved Information Security Policy. Annex A controls require policies for specific domains: A.5.1 (IS policies), A.6.2 (acceptable use for personal devices), A.8.5 (secure authentication).

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **Policy** | Board-approved statement of management intent | Information Security Policy |
| **Standard** | Specific, measurable requirement derived from policy | Password minimum 12 characters, MFA required |
| **Procedure** | Step-by-step operational instructions | User onboarding procedure |
| **Guideline** | Recommended best practice (not mandatory) | Email writing best practice guide |
| **Policy Owner** | Role accountable for maintaining the policy | CISO owns Information Security Policy |
| **Policy Approver** | Authority that approves the policy | CEO or Board |
| **Policy Scope** | Who and what the policy applies to | All employees, contractors, third parties with access |
| **Enforcement** | Consequences of non-compliance | Disciplinary action, contract termination |
| **Review Cycle** | How often the policy is formally reviewed | Annual minimum; triggered by significant change |
| **Version Control** | Document management tracking changes | Version 1.2 | Updated 2025-01-01 | Author: CISO |
| **Policy Library** | Collection of all security policies | 15 policies in the formal library |
| **Acceptable Use Policy** | Policy governing use of company IT assets | No personal downloads on company devices |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### The Real-World Policy Development Process

1. **Identify required policies** — Start by mapping your organisation's risks and regulatory requirements to identify which policies are needed. ISO 27001, SOC 2, and GDPR all require specific policies.

2. **Identify the policy owner** — Every policy needs a named owner (a role, not a person) who is accountable for its content, accuracy, and maintenance.

3. **Research the regulatory requirements** — For each policy, identify the specific ISO 27001 Annex A controls, GDPR articles, or industry regulations that the policy must address.

4. **Draft the policy** — Use a consistent template (same header, same section structure) across all policies. Write in clear, specific language — avoid vague statements like "we take security seriously."

5. **Consult relevant stakeholders** — Before finalising, consult with HR (for employment law implications), Legal (for regulatory requirements), IT (for technical feasibility), and Business units (for operational impact).

6. **Get formal approval** — The policy must be formally approved by the appropriate authority — typically the board for the Information Security Policy, and senior management for individual policies.

7. **Communicate and train** — Policies only work if people know about them. All staff must be trained on relevant policies at onboarding and annually.

8. **Maintain and review** — Build a policy review calendar. All policies should be reviewed at minimum annually; major changes (new regulation, new technology, incident) should trigger an unscheduled review.

9. **Track compliance** — Maintain evidence that policies have been reviewed, approved, communicated, and that staff have acknowledged them.

### Real Company Example

RetailMax Ltd. suffered a significant data breach when an employee installed unauthorised file-sharing software on their work laptop, inadvertently exposing 40,000 customer records. The post-incident review identified root causes: no Acceptable Use Policy governing personal software installation, no Data Classification Policy defining how sensitive data must be handled, and no formal Patch Management Policy ensuring device security.

The new CISO, Priya Singh, was tasked with building a complete policy library from scratch. She started by inventorying the risks and ISO 27001 controls relevant to RetailMax: a 1,000-person retail chain with POS systems, an e-commerce platform, and 300 store-based employees who all use company-issued tablets.

Priya identified 12 required policies, assigned owners (CISO for security policies, HR Director for personnel policies, IT Manager for technical policies), built a 3-month writing schedule, and established a review cadence (all policies to board by month 4 for approval).

The resulting policy library was presented to the board. The CEO signed the master Information Security Policy, making RetailMax's security obligations explicit for the first time. The board approved the policies with minor amendments. The library became a key exhibit in RetailMax's subsequent ISO 27001 gap assessment — showing "Defined" maturity (Level 3) for policy-related controls.

---

## Section 3: Framework Deep Dive

### ISO 27001 Annex A — Policy-Related Controls

| Control Ref | Control Name | What Policy It Requires |
|-------------|--------------|------------------------|
| A.5.1 | Policies for information security | Master Information Security Policy |
| A.6.2 | Information security responsibilities | Roles and responsibilities policy/RACI |
| A.6.3 | Security awareness, education, and training | Training and Awareness Policy |
| A.6.4 | Disciplinary process | Acceptable Use Policy (enforcement section) |
| A.6.5 | Responsibilities after termination | HR Security Policy (offboarding section) |
| A.8.1 | User endpoint devices | Acceptable Use Policy (device section) |
| A.8.2 | Privileged access rights | Access Control Policy (privileged access section) |
| A.8.5 | Secure authentication | Password and Authentication Policy |
| A.8.7 | Protection against malware | Patch Management and Anti-Malware Policy |
| A.8.8 | Management of technical vulnerabilities | Vulnerability Management Policy |
| A.8.24 | Use of cryptography | Cryptography Policy |
| A.5.9 | Inventory of information assets | Asset Management Policy |
| A.5.10 | Acceptable use of information assets | Acceptable Use Policy |
| A.5.14 | Information transfer | Data Transfer and Classification Policy |

---

## Section 4: Common Mistakes Beginners Make

1. **Writing policies that are too vague.** "We protect our data" is not a policy statement. "All personally identifiable information must be encrypted at rest using AES-256 and in transit using TLS 1.2 or higher" is a policy statement.

2. **Confusing policies with procedures.** A policy states what must be achieved. It should not contain step-by-step instructions (that's a procedure). Keeping them separate makes policies more stable over time.

3. **Not getting formal approval.** A policy that hasn't been formally approved by the appropriate authority is not a policy — it's a draft. The approval process is as important as the content.

4. **Writing policies that are technically impossible to comply with.** Always validate technical feasibility with IT before finalising. "MFA must be enforced for all systems" is aspirational if many systems don't support MFA yet — write it as a requirement with a transition timeline.

5. **Not including scope.** Every policy must clearly state who it applies to. "All employees" is a start, but many policies also apply to contractors, third parties, and sometimes customers.

6. **Using policy language that creates legal risk.** "We will never share your data" is a dangerous policy statement if data is legally required to be shared with regulators. Work with Legal before finalising.

7. **Forgetting version control.** Every policy version must be numbered, dated, and the author identified. Without this, it's impossible to track what changed between versions.

8. **Not communicating policies to staff.** A policy library that only the CISO reads provides zero security value. Staff must be trained on relevant policies and acknowledge them.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **Use a consistent policy template across all policies** — same header, same section structure. Consistency makes the library professional and easier to audit.
- **Map every policy to its ISO 27001 or NIST CSF control references** in the header — this is extremely useful during gap assessments and audits.
- **Write policy statements in the imperative** — "Must", "Shall", "Is required to" — not "should consider" or "it is recommended that".
- **The Information Security Policy is the apex document** — it sets the tone and must be signed by the CEO or board, not just the CISO.
- **Build a policy exception process** — sometimes operational reality requires a temporary exception to a policy. Document this: who can grant exceptions, what evidence is required, how long exceptions last, and how they're tracked.
- **Use the policy to set minimum standards, not aspirational targets** — policies describe the floor (minimum acceptable behaviour), not the ceiling.
- **Annual review is the minimum** — review whenever: a regulation changes, a significant incident occurs, the organisation's business model changes, or a new technology is adopted.
- **Track policy acknowledgements** — LMS (Learning Management System) records, email confirmations, or signed forms all serve as evidence that staff are aware of policies.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [ISO 27001:2022 Clause 5.2 — Policy Requirements](https://www.iso.org/standard/27001) — What ISO requires in a policy
- [SANS Institute: Information Security Policy Templates](https://www.sans.org/information-security-policy/) — Free professional policy templates
- [NCSC: Security Policy Guidance](https://www.ncsc.gov.uk/guidance/introduction-logging-small-and-medium-organisations) — UK guidance on policy content
- [ISO 27001 Academy: Policy Library Guide](https://advisera.com/27001academy/blog/2015/03/16/how-to-write-iso-27001-policies-procedures-and-work-instructions/) — Step-by-step policy writing
- [NIST SP 800-100: Information Security Handbook for Managers](https://csrc.nist.gov/publications/detail/sp/800-100/final) — Policy development chapter

### Books

- *Writing Information Security Policies* by Scott Barman — The definitive guide to security policy writing
- *ISO 27001 Controls: A Guide to Implementing and Auditing* by Bridget Kenyon — Covers policy requirements per control
- *The CISO Handbook* by Michael Gentile — Practical security programme management including policies

### Online Courses

- [SANS: Security Policy Development](https://www.sans.org/cyber-security-courses/security-policy-development/) — Professional policy writing course
- [LinkedIn Learning: Writing Security Policies](https://www.linkedin.com/learning/) — Search "information security policies"
- [Coursera: IT Security: Defense against the digital dark arts (Google)](https://www.coursera.org/learn/it-security) — Covers policy and controls

### Tools to Explore

- **ConvergePoint** — Policy management platform; watch demo
- **PolicyTech** — NAVEX Global's policy management tool
- **Notion / Confluence** — Free tools for policy library management in smaller organisations

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (Teaching Session — 90 min)

- 20 min: Policy vs Standard vs Procedure — use 3 real examples to show the difference clearly
- 15 min: Policy template walkthrough — review the Security Policy Template in /Templates/ together
- 25 min: Live policy writing exercise — write an Acceptable Use Policy for RetailMax together; discuss each section
- 15 min: Policy library architecture — what 10 policies does every organisation need?
- 15 min: Introduce RetailMax scenario; discuss why the breach happened and how a policy library would have prevented it

### Session B Focus (Assignment Review — 60 min)

- Spot-check 3 policies: Are they specific enough? Do they use "must" not "should"?
- Check ISO 27001 control mappings in each policy header
- Review policy register: Are review dates set? Are owners assigned?
- Discuss: "Which of your 10 policies is most critical for RetailMax and why?"

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "What's the difference between a policy, a standard, and a procedure?"
2. "Walk me through how you would develop a new security policy."
3. "What makes a security policy 'audit-ready'?"
4. "How many policies does a typical security programme need?"
5. "How do you get staff to actually follow security policies?"
6. "What ISO 27001 clause requires a board-approved Information Security Policy?"
7. "What should an Acceptable Use Policy cover?"
8. "How do you handle a policy exception request?"
9. "How often should policies be reviewed?"
10. "What are the consequences of having no security policies?"

### Keywords to Use

- Policy hierarchy (policy, standard, procedure, guideline)
- ISO 27001 Clause 5.2 (Information Security Policy)
- Board-approved / top management commitment
- Policy owner and approver
- Scope — all employees, contractors, third parties
- Version control and review cycle
- Policy exception process
- Staff acknowledgement and training
- Mandatory enforcement
- Control mapping (ISO 27001 Annex A references)
