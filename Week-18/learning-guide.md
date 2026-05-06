# Week 18 Learning Guide: GRC Program Management

## What You Will Learn This Week

Managing a single compliance framework is challenging. Managing three simultaneously — ISO 27001, SOC 2, and GDPR — while keeping the business moving is where GRC professionals earn their seniority. This week you learn multi-framework GRC programme management: building a programme charter, creating a unified compliance calendar, mapping overlapping controls across frameworks, selecting and using GRC technology platforms, and communicating with the diverse stakeholder groups that every mature GRC programme must serve.

---

## Section 1: Core Concept Explained

### What Is GRC Programme Management?

A GRC Programme is the organised, managed collection of governance, risk management, and compliance activities across an organisation. Programme management refers to the planning, coordination, resourcing, and execution of all these activities in an integrated, efficient way.

The key challenge of GRC programme management is **efficiency across multiple frameworks**. Most large organisations must comply with multiple frameworks simultaneously:
- A UK insurer might need: ISO 27001 + SOC 2 + GDPR + FCA/PRA requirements + Solvency II + DORA
- A UK SaaS company might need: ISO 27001 + SOC 2 + GDPR + Cyber Essentials

Without programme management, each compliance requirement becomes a separate project — creating duplicate work, inconsistent documentation, confused stakeholders, and unsustainable resource demands.

With programme management, overlapping requirements across frameworks are identified and addressed once, evidence is collected once and mapped to multiple frameworks, and stakeholders receive consistent, coordinated communications.

**The unified control framework approach**: Most experienced GRC professionals build a **unified control library** — a single list of controls that maps to all applicable frameworks. One access review procedure satisfies: ISO 27001 A.5.18, SOC 2 CC6.3, NIST CSF PR.AA-03, and CIS Control 5.3 simultaneously. This is the core efficiency of mature GRC programme management.

### Key Terminology

| Term | Definition | Example |
|------|------------|---------|
| **GRC Programme** | Organised collection of all GRC activities | ISO 27001 + SOC 2 + GDPR programme |
| **Programme Charter** | Formal document authorising and defining the programme | Board-approved; defines scope, governance, budget |
| **Unified Control Library** | Single control list mapped to multiple frameworks | "Quarterly access review" maps to ISO A.5.18, SOC 2 CC6.3, NIST PR.AA |
| **Compliance Calendar** | Annual schedule of all compliance activities | SOC 2 observation period, ISO 27001 internal audit, GDPR DPIA reviews |
| **Control Overlap** | Where two frameworks require the same or similar control | ISO A.8.5 (MFA) maps to SOC 2 CC6.1 maps to NIST CSF PR.AA-03 |
| **GRC Platform** | Technology tool managing compliance activities | Vanta, Drata, ServiceNow GRC, RSA Archer |
| **Compliance Automation** | Technology automatically collecting evidence | Vanta auto-collects MFA status from Azure AD |
| **Programme Health** | Overall status of the GRC programme | Green = on track; Amber = at risk; Red = in crisis |
| **Stakeholder Map** | Document identifying all stakeholders and their needs | CISO (risk), CFO (cost), Legal (regulatory), IT (implementation) |

---

## Section 2: How GRC Professionals Apply This in Real Companies

### Building a Multi-Framework GRC Programme

1. **Start with a Programme Charter** — Get board-level approval before doing anything else. The charter defines: programme scope (which frameworks, which entities), governance (who makes decisions), budget, timeline, and success criteria. Without a charter, the programme lacks authority.

2. **Map all compliance obligations** — For each framework, document all requirements. Then map overlaps: where does ISO 27001 A.9 (access control) overlap with SOC 2 CC6? Where does GDPR Article 32 overlap with ISO 27001 A.5 (organizational controls)?

3. **Build a unified control library** — Create a single list of controls that satisfies all framework requirements. Each control entry includes: control description, what it satisfies (ISO ref, SOC 2 criteria, NIST subcategory, GDPR article), who owns it, how it's evidenced.

4. **Design the compliance calendar** — Map all compliance activities across the year: internal audits, external audits, SOC 2 observation period start/end, ISO 27001 surveillance audit, GDPR DPIA reviews, risk assessment updates, policy reviews.

5. **Select and implement GRC technology** — For a company managing multiple frameworks, a GRC platform (Vanta, Drata, Secureframe, ServiceNow GRC) dramatically reduces manual effort. The platform automates evidence collection, tracks control status, manages audits, and produces compliance reports.

6. **Establish stakeholder communication cadence** — Different stakeholders need different information: Board (quarterly — risk posture, compliance status, budget); CISO/Management (monthly — control effectiveness, open gaps, upcoming deadlines); IT/Operational Teams (weekly — specific tasks, evidence requests, upcoming audits); External Auditors (scheduled — evidence provision, audit support).

7. **Track programme health** — Build a programme health dashboard: How many controls are implemented? How many evidence items are collected? How many gaps are open? When is the next external audit? Is the programme on track?

8. **Manage audit logistics** — External auditors (ISO 27001 certification bodies, SOC 2 CPA firms) need organised, consistent evidence. Poor audit management (late evidence, inconsistent formats, disorganised documentation) is a significant cause of audit delays and failures.

### Real Company Example

InsureCo, a 1,500-person insurer, was managing ISO 27001, SOC 2, and GDPR as three completely separate programmes. They had three separate teams, three separate policy libraries (with inconsistent and sometimes contradictory policies), and three separate audit processes. Annual compliance cost: £1.8M.

Their new Head of GRC, David Santos, was tasked with unifying the programmes. He started by mapping all three frameworks against each other and identified:
- 78% of ISO 27001 controls had direct SOC 2 equivalents
- 42 of 93 ISO 27001 Annex A controls were also addressed by GDPR requirements
- The existing 3 policy libraries had 12 duplicate policies covering the same topics with slightly different wording

David built a unified control library with 140 controls covering all three frameworks. He consolidated 3 policy libraries into 1 (18 policies, each mapped to ISO, SOC 2, and GDPR references). He implemented Vanta as the compliance automation platform, which automatically collected 60% of the evidence previously collected manually.

Results: Annual compliance cost reduced by 35% to £1.17M. Audit preparation time reduced from 12 weeks to 4 weeks. No more contradictory policy requirements. The CISO could present one consolidated compliance dashboard to the board rather than three separate reports.

---

## Section 3: Framework Deep Dive

### GRC Technology Platforms

**Tier 1 — Compliance Automation (SMB to Mid-Market):**
- **Vanta**: Best for companies pursuing SOC 2, ISO 27001, GDPR simultaneously. Auto-collects evidence via integrations (AWS, GitHub, Google Workspace, M365). Monitoring, policy management, vendor risk.
- **Drata**: Similar to Vanta; strong SOC 2 and ISO 27001 support; real-time control monitoring.
- **Secureframe**: Compliance automation with strong reporting; good SOC 2 support.
- **TrustCloud**: Newer entrant; strong for multi-framework; built-in AI assistance.

**Tier 2 — Enterprise GRC Platforms:**
- **ServiceNow GRC**: Enterprise-grade; integrates with ServiceNow ITSM; expensive; high configurability.
- **RSA Archer**: Legacy enterprise GRC; extensive; complex; requires significant configuration.
- **MetricStream**: Enterprise GRC with strong risk and audit modules.
- **IBM OpenPages**: Enterprise risk and compliance management.

**Tier 3 — Audit Management:**
- **AuditBoard**: Purpose-built audit management; strong reporting; used by internal audit teams.
- **TeamMate+**: Audit management for internal audit departments.
- **Galvanize**: Risk and compliance with audit workflow.

---

## Section 4: Common Mistakes Beginners Make

1. **Running multiple frameworks as separate programmes.** The most common and most expensive mistake. Unified programme management is the fundamental efficiency gain.

2. **Not getting a Programme Charter approved first.** Without board/executive authority, the GRC programme cannot mandate controls from business units. Authority flows from the charter.

3. **Over-investing in technology before defining processes.** A GRC platform automates processes. If the processes aren't defined first, the platform will automate chaos.

4. **Under-investing in stakeholder management.** GRC programmes fail when business units see GRC as a police function rather than a value-add. Communication, partnership, and education are as important as technical controls.

5. **Not managing the compliance calendar.** Missing an internal audit, letting a certification expire, or being unprepared for an external audit all have serious consequences. The compliance calendar is the GRC team's operational heartbeat.

6. **Building a unified framework that doesn't accurately reflect the requirements.** Mapping ISO A.8.5 to SOC 2 CC6.1 and assuming one "MFA control" satisfies both requires validating that the MFA control genuinely satisfies both frameworks' requirements. Lazy mapping creates audit findings.

---

## Section 5: Professional Tips From Experienced GRC Analysts

- **The unified control library is your programme's backbone** — invest the time to build it properly. It will save months of duplicate work.
- **Use a compliance automation platform from Day 1** — Vanta and Drata trial periods are often generous. The time saved in evidence collection pays for the platform within weeks.
- **Build relationships with IT and DevOps** — they are your evidence providers. A good relationship means faster evidence collection; a bad one means audit delays.
- **The compliance calendar is a management tool, not just a schedule** — share it with all stakeholders; use it to drive accountability.
- **Stakeholder mapping is underrated** — knowing which stakeholders need what information, in what format, at what cadence, makes communication massively more effective.
- **Track GRC programme ROI** — compare the cost of running the programme to the value delivered (audit fees avoided, revenue unlocked from certification, fines avoided). This justifies budget.

---

## Section 6: Recommended Learning Resources

### Must-Read Documentation (Free)

- [OCEG GRC Capability Model (Red Book)](https://www.oceg.org/resources/grc-capability-model-red-book/) — The definitive GRC programme model
- [ISACA: GRC Programme Design](https://www.isaca.org/resources/grc) — ISACA GRC resources
- [ISO 27001 + SOC 2 Unified Approach](https://www.vanta.com/resources/iso-27001-vs-soc-2) — Comparison and unification approaches
- [ServiceNow GRC Documentation](https://docs.servicenow.com/bundle/washingtondc-it-service-management/page/product/governance-risk-compliance/concept/c_GovernanceRiskAndCompliance.html) — Enterprise GRC platform overview

### Online Courses

- [ISACA: GRC Management](https://www.isaca.org/training-and-events/online-courses) — GRC programme management
- [Coursera: Cybersecurity Risk Management](https://www.coursera.org/learn/cybersecurity-risk-management) — Risk and programme management
- [Vanta Academy](https://www.vanta.com/resources/vanta-academy) — Compliance automation platform training

---

## Section 7: Instructor Mentorship Guidance

### Session A Focus (90 min)

- 20 min: Multi-framework GRC — show side-by-side ISO 27001 vs SOC 2 vs GDPR; identify overlaps
- 20 min: Unified control library exercise — take 5 controls and map them across 3 frameworks together
- 20 min: GRC technology demo — show Vanta or Drata live; discuss what it automates
- 15 min: Stakeholder mapping exercise — identify all stakeholders for InsureCo's GRC programme; what does each need?
- 15 min: Compliance calendar design — map InsureCo's activities across 12 months

### Session B Focus (60 min)

- Review Programme Charter: Does it have board-level authority? Budget? Clear scope?
- Check unified compliance matrix: Are mappings accurate? Is it clear one control satisfies multiple frameworks?
- Review GRC tool selection: Is the recommendation justified for InsureCo's size and complexity?

---

## Section 8: Interview Preparation

### Common Interview Questions

1. "How do you manage compliance across multiple frameworks simultaneously?"
2. "What is a unified control framework?"
3. "What GRC technology platforms have you worked with?"
4. "How do you build a compliance calendar?"
5. "What is a GRC programme charter?"
6. "How do you demonstrate GRC programme ROI?"
7. "Tell me about a time you streamlined a compliance programme."
8. "What stakeholders does a GRC programme need to engage?"
9. "How do you choose between Vanta and ServiceNow GRC for a client?"
10. "What is a unified compliance matrix?"

### Keywords to Use

- Unified control framework / control library
- Multi-framework compliance management
- Compliance automation — Vanta, Drata, Secureframe
- GRC programme charter
- Compliance calendar
- Control overlap and efficiency
- Stakeholder management
- Programme health dashboard
- ISO 27001 + SOC 2 + GDPR unified approach
- ServiceNow GRC, RSA Archer (enterprise platforms)
