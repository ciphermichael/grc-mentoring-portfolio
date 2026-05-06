# Week 21 Learning Guide: Capstone — Enterprise GRC Strategy & Governance

## What You Will Build This Week

This is the beginning of your capstone project — the flagship of your portfolio. Over Weeks 21–24 you will build a complete enterprise GRC programme for NovaTech Corp, a 2,000-person UK fintech company. This week you design the strategic foundation: the GRC strategy, governance framework, operating model, and 12-month roadmap that will direct everything that follows. This is the work of a senior GRC professional — the kind of deliverable that a GRC Director or CISO would present to a board.

---

## Section 1: The Enterprise Perspective

### Building GRC Programmes at Scale

Building an enterprise GRC programme from scratch is different in kind, not just scale, from individual compliance projects. The key differences:

**Strategic alignment**: At enterprise scale, the GRC programme must align explicitly to business strategy. NovaTech is pursuing enterprise sales, ISO 27001 certification, and FCA compliance. Every GRC decision — what to prioritise, what to resource, what to measure — must be traceable to those business objectives.

**Governance infrastructure**: An enterprise programme requires formal committee structures, defined reporting lines, explicit accountability matrices, and documented decision-making processes. Informal approaches that work for a 50-person startup collapse at 2,000 people.

**Operating model design**: Who does what in GRC? Which roles are internal? Which are outsourced? How does the GRC team interact with IT, Legal, Finance, and Business? The operating model answers these questions explicitly.

**Long-horizon planning**: A startup might plan 90 days ahead. An enterprise GRC programme plans 12–18 months ahead, with a view toward 3-year strategic objectives. Certification timelines, regulatory cycles, and budget cycles all operate on annual rhythms.

### What Makes Enterprise GRC Strategy "Enterprise-Grade"

When an assessor looks at your capstone, they are evaluating whether your GRC Strategy document looks like something a real CISO would present to a real board. The markers of enterprise-grade work:

1. **Board language**: The strategy is written for non-technical executives. Business risk, not technical detail. Financial impact, not vulnerability counts.
2. **Specific and measurable**: "Reduce our risk exposure" is not a strategic objective. "Achieve ISO 27001 certification by Q4 2025 and SOC 2 Type II readiness by Q2 2026" is.
3. **Financially grounded**: All recommendations include estimated investment, resource requirements, and expected business benefit.
4. **Regulatory aware**: The strategy explicitly addresses NovaTech's regulatory environment (FCA, UK GDPR, PCI-DSS) rather than treating compliance generically.
5. **Internally consistent**: The governance structure supports the strategy; the operating model resources the governance; the roadmap delivers the strategy.

---

## Section 2: Deep Dive on This Week's Capstone Deliverables

### GRC Strategy Document

**What makes it enterprise-grade:**
- A clear vision statement for the GRC programme (what does "excellent GRC" look like at NovaTech in 3 years?)
- 5 strategic objectives, each with a measurable target and a named owner
- Explicit alignment to NovaTech's business strategy (enterprise sales, FCA compliance, PCI-DSS certification, Series C funding)
- A "current state vs target state" narrative that tells the story of the maturity journey
- An investment summary: total programme cost Year 1 vs expected risk reduction and revenue unlock

**Common weaknesses to avoid:**
- Strategy that reads like a list of activities (activity list ≠ strategy)
- No connection between GRC objectives and business outcomes
- Missing regulatory context (NovaTech is a regulated UK fintech — FCA obligations are central)
- No financial dimension

### Security Governance Framework

**What makes it enterprise-grade:**
- Three Lines of Defense explicitly applied to NovaTech's org structure (name the specific NovaTech teams in each line)
- Committee structure with real operating cadences: Board Risk Committee (quarterly), Security Steering Group (monthly), Security Operations Forum (bi-weekly)
- Reporting lines that give the CISO appropriate authority and board access
- RACI matrix covering 15+ specific GRC activities
- Policy hierarchy architecture

**Common weaknesses to avoid:**
- Generic Three Lines of Defense without naming NovaTech-specific roles
- Committee structure without operating rules (quorum, decision authority, agenda template)
- RACI with multiple "Accountable" entries (only one per activity)
- Governance framework that mirrors a GDPR blog post rather than NovaTech's actual context

### GRC Operating Model

**What makes it enterprise-grade:**
- Specific team structure: How many FTEs in GRC? What are their roles? Who reports to whom?
- Build vs Buy decisions: Which GRC capabilities are in-house? Which are outsourced (external auditors, IR firm, penetration testers)?
- GRC technology: Which platform will NovaTech use (Vanta, ServiceNow GRC) and why?
- Interaction model: How does GRC interact with each business function?

### Regulatory Obligations Register

**What makes it enterprise-grade:**
- Every specific regulation mapped: FCA PS21/3 (operational resilience), UK GDPR, PCI-DSS v4.0, Companies Act 2006 cyber provisions, DORA (if applicable)
- For each obligation: Specific requirement, enforcement body, deadline, current compliance status, gap, owner
- Not a general list of frameworks — specific regulatory requirements with specific deadlines

---

## Section 3: Integration and Cohesion — Making the Capstone Tell One Story

The capstone across Weeks 21–24 must tell a coherent story about NovaTech's security journey. Your Week 21 strategy must be consistent with:
- The risks identified in Week 22's risk register
- The gaps found in Week 23's compliance assessment
- The metrics chosen in Week 24's dashboard

**Test of internal consistency:**
- If your strategy says "achieve ISO 27001 certification by Q4," your Week 23 compliance matrix should show the gap assessment informing the roadmap, and your Week 24 dashboard should track certification progress as a KPI
- If your governance framework says "CISO reports to CEO," your Week 22 risk register should show CISO as the top-level risk owner
- If your operating model says "implement Vanta as GRC platform," your Week 23 evidence tracker should reference Vanta as the evidence source

---

## Section 4: Common Mistakes in Capstone Projects

1. **Treating the capstone as 4 independent weeks rather than one integrated programme.** Week 22's risk register must reference Week 21's risk appetite. Week 23's compliance gaps must inform Week 21's roadmap. The capstone is a single coherent programme, not 4 separate assignments.

2. **Writing at the wrong level of detail.** Strategy documents need breadth (covering all major areas) and appropriate depth (enough detail to be credible) but not operational minutiae (leave that for standards and procedures).

3. **Copying real company information or templates verbatim.** Your NovaTech deliverables should be written as if NovaTech is a real company. Don't use generic blog post content — populate it with NovaTech-specific context (2,000 employees, £180M ARR, London fintech, FCA-regulated, 5M customers, PCI-DSS scope).

4. **Weak financial grounding.** Enterprise GRC strategies must include investment estimates. Look up approximate costs for: ISO 27001 certification (£30–80K), SIEM implementation (£50–150K), PAM tooling (£40–100K), GRC platform (£30–60K/year), penetration testing (£10–30K). Use realistic ranges.

5. **Governance without enforcement.** A committee structure that exists on paper but has no described enforcement mechanism (what happens when the business ignores the CISO?) is incomplete.

6. **Not naming the NovaTech regulatory environment.** Generic references to "compliance with applicable regulations" are not acceptable. Name the FCA, the ICO, the PCI SSC, and their specific requirements.

---

## Section 5: Professional Presentation Skills

### Presenting GRC Strategy to the NovaTech Board

The Week 24 board presentation will require you to distill the entire capstone into a 30-minute board briefing. Principles:

**Structure your board presentation around questions boards care about:**
1. What is our current risk exposure? (Use financial terms: £X in potential regulatory fines, £Y in potential incident costs)
2. What are we doing about it? (Your programme — concise, confident)
3. What will it cost? (Investment summary — clear, justified)
4. What is the business benefit? (Revenue unlocked by ISO 27001 certification, fines avoided, competitive differentiation)
5. What do you need from us? (Budget approval, governance decisions, executive sponsorship)

**Board communication principles:**
- Every slide has a headline that states the key message (not just the topic)
- No slide has more than 5 bullets
- Every risk is expressed in £ terms where possible
- Use visuals: heatmap, radar chart, timeline — not just text
- Practice the 30-minute presentation until it is smooth

---

## Section 6: Recommended Learning Resources

### Must-Read for Capstone

- [OCEG GRC Capability Model](https://www.oceg.org/resources/grc-capability-model-red-book/) — The definitive enterprise GRC programme model
- [FCA: Operational Resilience PS21/3](https://www.fca.org.uk/publications/policy-statements/ps21-3-operational-resilience-financial-sector) — NovaTech's primary regulatory context
- [NCSC: Board Toolkit for Cyber Governance](https://www.ncsc.gov.uk/collection/board-toolkit) — What board-level GRC looks like
- [PCI SSC: PCI-DSS v4.0 for Fintechs](https://www.pcisecuritystandards.org/) — NovaTech's payment compliance context
- [UK FCA: Cybersecurity Guidance](https://www.fca.org.uk/firms/cyber-security) — UK fintech regulatory expectations

### Books for Senior GRC Thinking

- *The CISO Handbook* by Michael Gentile — How CISOs build enterprise programmes
- *CISA Review Manual* — Enterprise IS governance and risk chapters
- *Security Risk Management* by Evan Wheeler — Enterprise risk programme design

---

## Section 7: Instructor Mentorship Guidance

### Capstone Week 21 Review Focus

**Quality markers for distinction-level Week 21 work:**
1. GRC Strategy contains a genuine financial investment analysis (costs vs business benefit)
2. Governance framework names specific NovaTech roles (not generic "CISO" — name the reporting line to CEO)
3. Operating model includes build vs buy analysis for at least 3 GRC capabilities
4. Regulatory obligations register includes specific FCA PS21/3, PCI-DSS v4.0, and UK GDPR requirements with specific deadlines
5. 12-month roadmap is sequenced logically (governance before controls; controls before audit; audit before certification)
6. All documents use consistent NovaTech branding (company name, scenario details)
7. Documents are at board-presentation quality — formatted, version-controlled, professionally written

**Questions to ask the student:**
1. "Walk me through your GRC Strategy document — what are NovaTech's top 3 strategic GRC objectives?"
2. "Your governance framework shows a Security Steering Committee. Who chairs it and what decision authority does it have?"
3. "How does your 12-month roadmap connect to NovaTech's ISO 27001 certification target?"
4. "What is the total investment required for Year 1 of NovaTech's GRC programme?"
5. "The FCA has reviewed NovaTech's cyber governance as part of an inspection. What documentation would you pull from your Week 21 deliverables?"

---

## Section 8: Interview and Career Preparation

### How to Discuss Your Capstone in Interviews

The NovaTech capstone is your most impressive portfolio piece. Practice describing it in under 90 seconds:

**The 90-second capstone pitch:**
"My capstone project involved building a complete enterprise GRC programme for NovaTech Corp, a fictional 2,000-person UK fintech with £180M ARR, 5 million customers, and significant FCA and PCI-DSS regulatory obligations. I produced: a GRC strategy and governance framework, a 30-risk enterprise risk register with FAIR quantitative analysis, a 15-policy library, compliance mapping across ISO 27001, NIST CSF, and GDPR, an internal audit programme with 6 planned audits, a 10-vendor risk programme, a 12-metric security dashboard, and a 20-slide board presentation. The full programme is documented on my GitHub portfolio."

### What Hiring Managers Want to See in Your Capstone

1. **Completeness**: All 8 programme components delivered
2. **NovaTech consistency**: All documents reference NovaTech-specific context, not generic templates
3. **Framework accuracy**: ISO 27001 controls correctly identified; GDPR articles correctly referenced; NIST CSF functions correctly named
4. **Professional quality**: Board-ready formatting; version control; no placeholder text
5. **Business language**: Risk expressed in £; investment justified with ROI; regulatory context named explicitly
