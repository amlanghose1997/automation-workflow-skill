# Product Development Operating System (PDOS)

A reusable, technology-agnostic SOP for taking any software product — SaaS, mobile app, AI agent, API, cloud service, browser extension, or web app — from idea to scale. Designed for solo developers and small startup teams.

**How to use this document:**
- Work through stages in order; parallelize only where exit criteria allow.
- Copy this file into every new project repo as `PDOS.md` and check off items as you go.
- Each stage has 13 sections: Objective, Inputs, Expected Outputs, Deliverables, Process, Decision Checkpoints, Quality Checklist, Common Mistakes, Best Practices, Automation Opportunities, AI Prompts, Human Review Checklist, and Exit Criteria.
- Do not skip Exit Criteria. They are the gate to the next stage.

**Phases:**
| Phase | Stages |
|---|---|
| Discover | 1. Idea Generation · 2. Market Research · 3. Problem Validation · 4. Competitor Analysis · 5. Customer Persona |
| Define | 6. Product Vision · 7. Business Model · 8. Feature Prioritization · 9. PRD Creation |
| Design | 10. UI/UX Design · 11. Architecture Design · 12. Database Design · 13. API Design |
| Build | 14. Backend Development · 15. Frontend Development · 16. AI Integration |
| Verify | 17. Testing Strategy · 18. Performance Optimization · 19. Security Review · 20. Documentation |
| Launch | 21. Deployment · 22. Monitoring · 23. Analytics · 24. Marketing |
| Grow | 25. Customer Support · 26. Product Iteration · 27. Scaling |

---

## Stage 1: Idea Generation

### 1. Objective
Generate and shortlist product ideas grounded in real problems, not solutions looking for problems.

### 2. Inputs
- Personal pain points, domain expertise, professional experience
- Community complaints (Reddit, HN, X, niche forums, app store reviews)
- Industry trends, new platform/API capabilities, regulatory changes

### 3. Expected Outputs
- A ranked shortlist of 3–5 candidate ideas with a one-line problem statement each

### 4. Deliverables
- `ideas.md`: idea backlog with scoring matrix (problem severity, audience reachability, willingness to pay, your unfair advantage)

### 5. Step-by-step Process
1. Brainstorm 20+ raw ideas without filtering (timebox: 2 sessions).
2. For each, write the problem, who has it, and how they solve it today.
3. Score each idea 1–5 on: pain severity, frequency, market reachability, monetization potential, founder-fit.
4. Kill ideas scoring < 15/25. Shortlist top 3–5.
5. Write a one-sentence pitch for each: "X helps Y do Z without W."

### 6. Decision Checkpoints
- Is this a painkiller (must-have) or vitamin (nice-to-have)?
- Can I reach the target audience without a huge budget?
- Do I have an unfair advantage (skill, audience, insight)?

### 7. Quality Checklist
- [ ] Every idea states a problem, not a feature
- [ ] Target user is specific ("freelance accountants", not "businesses")
- [ ] Existing alternatives documented for each idea
- [ ] Scoring applied consistently across all ideas

### 8. Common Mistakes
- Falling in love with a solution before validating the problem
- Choosing markets you can't access or don't understand
- Ideas requiring network effects on day one
- "It just needs 1% of a huge market" reasoning

### 9. Best Practices
- Solve problems you've personally experienced or observed closely
- Prefer boring problems with proven spend over novel unproven ones
- Niches beat broad markets for small teams

### 10. Automation Opportunities
- Scrape/monitor subreddits, review sites, and forums for recurring complaints
- Use keyword research tools to quantify search demand automatically

### 11. AI Prompts
- "Here are 20 product ideas: [list]. Score each on pain severity, frequency, reachability, monetization, and founder-fit for a solo developer. Rank them and explain the top 3."
- "List the 10 most common complaints users have about [category] tools, based on typical review-site and forum feedback patterns."

### 12. Human Review Checklist
- [ ] I would personally pay for the top idea, or know 5 people who would
- [ ] Gut-check: am I excited to work on this for 2+ years?
- [ ] A trusted peer has challenged my top pick and it survived

### 13. Exit Criteria
- One primary idea selected with a written one-sentence pitch, a named target user, and a documented existing-alternatives list.

---

## Stage 2: Market Research

### 1. Objective
Quantify the market: size, growth, segments, buying behavior, and channels — enough to confirm the opportunity is worth pursuing.

### 2. Inputs
- Selected idea and one-sentence pitch from Stage 1
- Industry reports, search volume data, competitor pricing pages, community discussions

### 3. Expected Outputs
- TAM/SAM/SOM estimates with stated assumptions
- Market trends summary and channel map (where buyers hang out)

### 4. Deliverables
- `market-research.md`: market sizing, segments, trends, channels, pricing landscape

### 5. Step-by-step Process
1. Define the market category and its adjacent categories.
2. Estimate TAM (everyone with the problem), SAM (reachable segment), SOM (realistic 3-year capture) — bottom-up preferred (users × price).
3. Map segments: who buys, who uses, who pays, deal size, sales cycle.
4. Survey the pricing landscape: what do alternatives charge, per what unit?
5. Identify 3–5 acquisition channels where the audience already gathers.
6. Note trends: growing/shrinking, regulatory shifts, platform risks.

### 6. Decision Checkpoints
- Is SOM large enough to sustain your revenue goal (e.g., $10k–$100k MRR)?
- Is the market growing, flat, or declining?
- Are there acquisition channels a small team can actually exploit?

### 7. Quality Checklist
- [ ] Bottom-up sizing with explicit assumptions, not just top-down report numbers
- [ ] At least 3 viable acquisition channels identified
- [ ] Pricing benchmarks collected from 5+ alternatives
- [ ] Segment willingness-to-pay differentiated (prosumer vs SMB vs enterprise)

### 8. Common Mistakes
- Quoting inflated analyst TAM figures without bottom-up sanity checks
- Ignoring how buyers currently budget for this problem
- Confusing users with buyers
- Researching forever as a form of procrastination (timebox: 1 week)

### 9. Best Practices
- Bottom-up beats top-down for small teams
- Talk to the market, not just reports — even 5 conversations beat 50 charts
- Document assumptions so estimates can be revisited later

### 10. Automation Opportunities
- Automated keyword volume tracking and trend alerts
- Scheduled scraping of competitor pricing pages for change detection

### 11. AI Prompts
- "Build a bottom-up TAM/SAM/SOM model for [product] targeting [segment]. State every assumption and give a low/base/high scenario."
- "Map the buying process for [segment] purchasing [category] software: who decides, who pays, typical budget, sales cycle length, and where they discover new tools."

### 12. Human Review Checklist
- [ ] Assumptions in the sizing model sanity-checked against at least one real data point
- [ ] Channel list reviewed against your actual skills/reach
- [ ] Someone in or near the target market has reviewed your conclusions

### 13. Exit Criteria
- Documented TAM/SAM/SOM with assumptions, at least 3 viable channels, and a go/no-go decision recorded. If no-go: return to Stage 1.

---

## Stage 3: Problem Validation

### 1. Objective
Prove real people have the problem, feel it acutely, and would pay for a solution — before writing code.

### 2. Inputs
- Idea pitch, target segment, market research findings
- List of 15–30 people in the target segment to contact

### 3. Expected Outputs
- Evidence of problem severity from 10+ interviews and/or a smoke test
- Clear articulation of the problem in customers' own words

### 4. Deliverables
- `validation.md`: interview notes, quotes, patterns, smoke-test metrics, validated problem statement

### 5. Step-by-step Process
1. Write an interview script focused on past behavior, not hypotheticals ("Tell me about the last time you..." not "Would you use...").
2. Recruit and interview 10–15 target users (15–30 min each).
3. Record: how they solve it today, what it costs them (time/money), what they've tried, what they'd pay.
4. Optionally run a smoke test: landing page + waitlist or pre-order, drive 200+ visitors, measure conversion.
5. Synthesize: recurring pains, exact vocabulary, disqualifying signals.
6. Decide: validated, pivot, or kill.

### 6. Decision Checkpoints
- Did 60%+ of interviewees describe the problem unprompted or with strong emotion?
- Are people already paying (money or significant time) for workarounds?
- Smoke test conversion ≥ 20–30% email signup, or any pre-orders?

### 7. Quality Checklist
- [ ] Questions ask about past behavior, never "would you"
- [ ] At least 10 interviews from the actual target segment
- [ ] Verbatim quotes captured (used later in marketing copy)
- [ ] Current workaround and its cost documented per interviewee

### 8. Common Mistakes
- Pitching your solution during discovery interviews
- Accepting polite enthusiasm ("cool idea!") as validation
- Interviewing friends who aren't in the segment
- Skipping validation because "I have the problem myself"

### 9. Best Practices
- Follow The Mom Test principles: facts about their life, not opinions about your idea
- Ask "what have you tried?" — no attempts means low pain
- Ask for money or commitment (pre-order, LOI, pilot) as the strongest signal

### 10. Automation Opportunities
- Scheduling links + automated reminders for interviews
- AI transcription and theme extraction from interview recordings
- No-code landing page + analytics for smoke tests

### 11. AI Prompts
- "Write a 10-question customer discovery script for [problem] following The Mom Test: past behavior only, no hypotheticals, no pitching."
- "Here are transcripts from 12 discovery interviews: [paste]. Extract recurring pain themes, exact customer vocabulary, current workarounds and their costs, and rate problem severity per theme."

### 12. Human Review Checklist
- [ ] I can state the problem in customers' exact words
- [ ] At least 3 interviewees asked to be notified when it launches
- [ ] Disconfirming evidence honestly recorded, not filtered out

### 13. Exit Criteria
- Written validated problem statement backed by 10+ interviews, evidence of existing spend/workarounds, and an explicit go decision. If weak signal: pivot the segment or problem and repeat.

---

## Stage 4: Competitor Analysis

### 1. Objective
Understand the competitive landscape well enough to find a defensible wedge: what you'll do differently and for whom.

### 2. Inputs
- Validated problem statement and segment
- List of direct competitors, indirect alternatives, and DIY workarounds

### 3. Expected Outputs
- Competitor matrix and a written positioning wedge (your differentiation)

### 4. Deliverables
- `competitors.md`: matrix (features, pricing, target user, strengths, weaknesses), review mining summary, positioning statement

### 5. Step-by-step Process
1. List 5–10 direct competitors and 3–5 indirect alternatives (including spreadsheets/manual work).
2. For each: target user, pricing model, key features, onboarding flow, positioning message.
3. Mine their reviews (G2, app stores, Reddit) for loved features and top complaints.
4. Sign up for the top 3 and document the experience gaps first-hand.
5. Identify underserved segments or workflow gaps — your wedge.
6. Write a positioning statement: "For [segment] who [need], [product] is the [category] that [key differentiator], unlike [main alternative]."

### 6. Decision Checkpoints
- Is there a gap you can own (segment, workflow, price point, experience)?
- Can incumbents copy your wedge trivially? What's your moat over time?
- Is the market too crowded/commoditized to enter with your resources?

### 7. Quality Checklist
- [ ] Indirect alternatives and "do nothing" included, not just direct competitors
- [ ] Review mining done for the top 3 competitors
- [ ] First-hand product trial of the top 3
- [ ] Positioning statement written and specific

### 8. Common Mistakes
- Competing on "more features" or "cheaper" as the entire strategy
- Ignoring the biggest competitor: the status quo / doing nothing
- Building a feature-comparison spreadsheet but no actual positioning
- Assuming incumbents' weaknesses are permanent

### 9. Best Practices
- Competitors' 1-star reviews are your roadmap; their 5-star reviews are table stakes
- Differentiate on the axis competitors structurally can't follow (business model, focus, distribution)
- Track competitors continuously, not once

### 10. Automation Opportunities
- Change-detection monitoring on competitor pricing/feature pages
- Automated review aggregation and sentiment analysis
- Alerts for competitor launches, funding, and hiring signals

### 11. AI Prompts
- "Analyze these competitor reviews: [paste]. Summarize the top 5 loved features (table stakes) and top 5 complaints (opportunity gaps) with representative quotes."
- "Given this competitor matrix [paste], propose 3 positioning wedges for a solo-built product targeting [segment], and rate each on defensibility and time-to-differentiation."

### 12. Human Review Checklist
- [ ] I can explain in one sentence why someone would switch to my product
- [ ] The wedge validated against interview findings from Stage 3
- [ ] Honest assessment: I'm not entering a market I can't win

### 13. Exit Criteria
- Complete competitor matrix, review-mining insights, and a written positioning statement identifying a specific, defensible wedge.

---

## Stage 5: Customer Persona

### 1. Objective
Define a specific, evidence-based primary persona that anchors every later decision: features, copy, design, pricing, and channels.

### 2. Inputs
- Interview notes and quotes (Stage 3), segment data (Stage 2), positioning wedge (Stage 4)

### 3. Expected Outputs
- One primary persona (and at most one secondary), grounded in real interview data

### 4. Deliverables
- `personas.md`: persona card(s) — role, context, goals, pains, triggers, objections, watering holes, buying power, vocabulary

### 5. Step-by-step Process
1. Cluster interviewees by shared context and pain intensity.
2. Choose the cluster with highest pain + reachability + willingness to pay as the primary persona.
3. Write the persona card: name, role, day-in-the-life, jobs-to-be-done, current tools, trigger events, success criteria, objections, budget authority.
4. List "watering holes": where they read, ask questions, and discover tools.
5. Capture their exact vocabulary for the problem (from interview quotes).
6. Explicitly write an anti-persona: who you are NOT building for.

### 6. Decision Checkpoints
- Is the persona narrow enough that you'd recognize them in a coffee shop?
- Does the persona have both the pain AND the budget authority?
- Does your positioning wedge resonate with this specific persona?

### 7. Quality Checklist
- [ ] Persona built from real interview data, not imagination
- [ ] Jobs-to-be-done stated in outcome form ("get paid faster", not "use invoicing software")
- [ ] Trigger events identified (what makes them look for a solution NOW)
- [ ] Anti-persona documented

### 8. Common Mistakes
- Demographic fiction ("Sarah, 34, likes yoga") with no behavioral substance
- Multiple primary personas diluting focus
- Personas created once and never referenced again
- Building for users who can't pay while ignoring the actual buyer

### 9. Best Practices
- One primary persona until product-market fit; expand later
- Reference the persona in every PRD, design review, and copy decision
- Revisit and revise the persona quarterly as real customer data accumulates

### 10. Automation Opportunities
- AI clustering of interview transcripts into candidate personas
- CRM tagging to validate persona assumptions against actual signups later

### 11. AI Prompts
- "From these interview notes [paste], cluster participants into 2–3 candidate personas. For each: jobs-to-be-done, pains, triggers, objections, and willingness to pay. Recommend the primary."
- "Write a one-page persona card for [cluster description] including a realistic day-in-the-life, tool stack, trigger events, and the exact phrases they use to describe [problem]."

### 12. Human Review Checklist
- [ ] Each persona trait traceable to at least one real interview
- [ ] I could write a cold email to this persona that feels personal
- [ ] Team (if any) agrees this is the persona we say no to everything else for

### 13. Exit Criteria
- One evidence-based primary persona card and anti-persona documented; referenced as the decision anchor for all subsequent stages.

---

## Stage 6: Product Vision

### 1. Objective
Define where the product is going (1–3 years), why it matters, and the principles that will guide every trade-off.

### 2. Inputs
- Validated problem, positioning wedge, primary persona

### 3. Expected Outputs
- Vision statement, mission, 3–5 product principles, and a north-star metric

### 4. Deliverables
- `vision.md`: vision statement, north-star metric, product principles, 12-month milestone map, explicit non-goals

### 5. Step-by-step Process
1. Write the vision: the changed world if you succeed (1–2 sentences).
2. Write the mission: what the product does today toward that vision.
3. Define the north-star metric — the single measure of delivered value (e.g., "invoices paid on time via the product").
4. Write 3–5 product principles to resolve future trade-offs (e.g., "speed over configurability").
5. Sketch milestone map: MVP → v1 → 12-month horizon.
6. List explicit non-goals: things you will not build even if asked.

### 6. Decision Checkpoints
- Does the vision inspire you enough for a multi-year commitment?
- Does the north-star metric measure customer value, not vanity?
- Do the principles actually force trade-offs (would you sacrifice something for them)?

### 7. Quality Checklist
- [ ] Vision fits in 2 sentences and is memorable
- [ ] North-star metric is measurable from day one
- [ ] Each principle would change a real decision
- [ ] Non-goals documented

### 8. Common Mistakes
- Vision statements that are generic slogans ("empower everyone to...")
- North-star metrics that track activity, not value (signups vs. outcomes)
- Principles nobody ever cites in a decision
- Roadmapping 3 years of features in detail (waste — it will change)

### 9. Best Practices
- Vision is stable; roadmap is disposable
- Test every feature request against the vision and principles
- Keep the milestone map coarse: themes, not tickets

### 10. Automation Opportunities
- Dashboard tracking the north-star metric from launch
- Template the vision doc for reuse across projects

### 11. AI Prompts
- "Given this problem, persona, and wedge [paste], draft 3 alternative vision statements and a candidate north-star metric for each. Critique which best measures real customer value."
- "Propose 5 product principles for [product] that would create genuine trade-offs, with an example decision each principle would change."

### 12. Human Review Checklist
- [ ] I can recite the vision from memory
- [ ] The north-star metric can't be gamed without delivering value
- [ ] Non-goals reviewed — am I truly willing to say no to these?

### 13. Exit Criteria
- Vision, north-star metric, principles, milestone themes, and non-goals written and committed to the repo.

---

## Stage 7: Business Model

### 1. Objective
Decide how the product makes money: pricing model, packaging, and unit economics that work at your team size.

### 2. Inputs
- Persona (budget authority, willingness to pay), competitor pricing landscape, vision and milestones

### 3. Expected Outputs
- Chosen revenue model, pricing tiers, and a simple unit-economics model

### 4. Deliverables
- `business-model.md`: revenue model, pricing/packaging, unit economics (CAC, LTV, margin), break-even math, billing requirements

### 5. Step-by-step Process
1. Choose the revenue model: subscription, usage-based, one-time, freemium, marketplace take-rate, or hybrid.
2. Pick the value metric to charge on — the unit that scales with customer value (seats, projects, API calls, revenue processed).
3. Design 2–3 tiers anchored to persona segments; price against value delivered, not cost.
4. Model unit economics: price, gross margin (include AI/API/infra costs), estimated CAC per channel, payback period.
5. Compute break-even: customers needed to hit your income goal.
6. Define billing requirements: trials, proration, refunds, tax handling.

### 6. Decision Checkpoints
- Does the value metric grow as the customer gets more value?
- Can you reach break-even with a realistic number of customers (e.g., <500 for a solo SaaS)?
- Freemium: can you afford free users' costs (especially with AI inference)?

### 7. Quality Checklist
- [ ] Pricing tested against interview willingness-to-pay data
- [ ] Gross margin computed including all variable costs (AI tokens, infra, payment fees)
- [ ] Each tier maps to a distinct persona or use intensity
- [ ] Annual plan and trial strategy decided

### 8. Common Mistakes
- Underpricing out of fear (most common solo-founder error)
- Charging on a metric users minimize rather than value they receive
- Free tier so generous nobody upgrades
- Ignoring AI inference costs in margin calculations

### 9. Best Practices
- Start higher than comfortable; lowering prices is easy, raising is hard
- 10x rule: price ≤ 1/10 of the value you deliver
- Keep packaging simple at launch: one or two paid tiers
- Revisit pricing every 6 months

### 10. Automation Opportunities
- Use a billing platform (e.g., Stripe) rather than building billing logic
- Automated dunning for failed payments
- Spreadsheet/template for unit-economics scenarios

### 11. AI Prompts
- "Design pricing for [product] serving [persona]. Competitors charge [data]. Propose 3 packaging options with a value metric, tier structure, and rationale. Flag risks of each."
- "Build a unit-economics model: price $X/mo, variable costs [list incl. AI costs], CAC assumptions per channel [list]. Compute margin, LTV at N-month retention, payback period, and customers to reach $Y MRR."

### 12. Human Review Checklist
- [ ] I've said the price out loud to a real prospect and watched the reaction
- [ ] Worst-case margin scenario still acceptable
- [ ] Billing edge cases (refunds, upgrades, failed payments) have decided policies

### 13. Exit Criteria
- Revenue model, tiers, and prices decided; unit economics show a credible path to your revenue goal; billing requirements listed for the PRD.

---

## Stage 8: Feature Prioritization

### 1. Objective
Ruthlessly scope the MVP: the smallest feature set that delivers the core value to the primary persona.

### 2. Inputs
- Validated problem, persona jobs-to-be-done, positioning wedge, vision principles, business model

### 3. Expected Outputs
- Prioritized backlog with a clearly bounded MVP cut line

### 4. Deliverables
- `backlog.md`: scored feature list (MVP / v1.1 / later / never), MVP definition, walking-skeleton user journey

### 5. Step-by-step Process
1. Brain-dump every candidate feature from interviews, competitor gaps, and vision.
2. Map the single critical user journey: signup → first value ("aha") → habitual use → payment.
3. Score features with RICE (Reach, Impact, Confidence, Effort) or MoSCoW.
4. Draw the MVP line: only features required to complete the critical journey.
5. Move everything else to v1.1/later; move vision-violating items to "never".
6. Estimate MVP effort; if > 4–6 weeks for a solo dev, cut deeper.

### 6. Decision Checkpoints
- Does the MVP deliver the core value end-to-end, however roughly?
- Can time-to-first-value be under 10 minutes for a new user?
- Is anything in the MVP there because it's "expected" rather than needed?

### 7. Quality Checklist
- [ ] Every MVP feature maps to the critical user journey
- [ ] Scoring criteria applied consistently
- [ ] Auth, billing, and settings scoped minimally (buy, don't build, where possible)
- [ ] "Never" list exists and cites vision principles

### 8. Common Mistakes
- MVP scope creep ("just one more feature before launch")
- Building admin panels, settings pages, and edge cases before core value
- Prioritizing by loudest request instead of scored impact
- Confusing MVP with low quality — small scope, high polish on what ships

### 9. Best Practices
- Cut scope, never quality, on the critical path
- Fake or manual-backend features to test demand before building (concierge MVP)
- Re-run prioritization after every batch of user feedback

### 10. Automation Opportunities
- Backlog scoring template (spreadsheet or issue-tracker custom fields)
- Auto-import feature requests from support/feedback channels into the backlog

### 11. AI Prompts
- "Here's my feature brain-dump for [product] and the critical user journey [paste]. Apply RICE scoring, propose an MVP cut line for a solo developer with a 4-week budget, and justify every exclusion."
- "Challenge this MVP scope [paste]: which features can be faked, bought, deferred, or deleted while still delivering [core value] to [persona]?"

### 12. Human Review Checklist
- [ ] I've tried to cut the MVP by another 30% and documented why remaining items stay
- [ ] A target user has seen the MVP list and confirmed it solves their problem
- [ ] Nothing on the list exists purely to match competitors

### 13. Exit Criteria
- Written MVP definition with a bounded feature list, mapped critical user journey, and an effort estimate that fits your timeline.

---

## Stage 9: PRD Creation

### 1. Objective
Turn the MVP scope into an unambiguous Product Requirements Document that a developer (you, a teammate, or an AI agent) can build from without guessing.

### 2. Inputs
- MVP backlog, persona, critical user journey, business model/billing requirements, vision principles

### 3. Expected Outputs
- A complete PRD covering functionality, user flows, edge cases, and acceptance criteria

### 4. Deliverables
- `PRD.md`: overview, goals/non-goals, user stories with acceptance criteria, user flows, data requirements, edge cases, success metrics, launch checklist

### 5. Step-by-step Process
1. Write the overview: problem, persona, core value, success metrics.
2. Restate goals and non-goals for this release.
3. Write user stories: "As [persona], I want [action] so that [outcome]" — each with Given/When/Then acceptance criteria.
4. Diagram key flows: onboarding, core loop, billing, account management.
5. Specify data requirements per feature (what's stored, displayed, validated).
6. Enumerate edge cases and error states per flow (empty states, failures, limits).
7. Define measurable success criteria (activation rate, time-to-value).
8. Review with a fresh eye (or AI) for ambiguity and gaps.

### 6. Decision Checkpoints
- Could someone else build this without asking you questions?
- Are non-goals explicit enough to prevent scope creep mid-build?
- Is every requirement testable?

### 7. Quality Checklist
- [ ] Every user story has acceptance criteria
- [ ] Empty, loading, and error states specified for every screen
- [ ] Permission/role rules stated where relevant
- [ ] Billing and account lifecycle flows covered
- [ ] Success metrics measurable with planned analytics

### 8. Common Mistakes
- Describing UI pixel details instead of behavior and requirements
- Omitting error states and edge cases (where most bugs live)
- PRD as a static artifact that drifts from what's built
- Writing for yourself in shorthand only you understand

### 9. Best Practices
- Keep the PRD living: update it when scope changes, and log the changes
- Acceptance criteria in Given/When/Then make testing (and AI codegen) dramatically easier
- Shorter and precise beats long and vague

### 10. Automation Opportunities
- PRD template reused across all projects
- AI review pass for ambiguity, contradictions, and missing edge cases
- Generate test cases directly from acceptance criteria

### 11. AI Prompts
- "Convert this MVP feature list and user journey [paste] into a full PRD with user stories, Given/When/Then acceptance criteria, edge cases, and error states. Ask me clarifying questions first."
- "Review this PRD [paste] as a skeptical senior engineer: list every ambiguity, contradiction, missing edge case, and unstated assumption."

### 12. Human Review Checklist
- [ ] Read the PRD end-to-end simulating a new developer — no unanswered questions
- [ ] Persona and vision referenced; nothing contradicts them
- [ ] Scope matches Stage 8's MVP line exactly

### 13. Exit Criteria
- PRD complete, ambiguity-reviewed, and frozen for the MVP build (changes now require an explicit change log entry).

---

## Stage 10: UI/UX Design

### 1. Objective
Design the user experience so the persona reaches first value fast, with a coherent, accessible interface — before writing production frontend code.

### 2. Inputs
- PRD (flows, edge cases), persona vocabulary, positioning, product principles

### 3. Expected Outputs
- Information architecture, key-screen designs, and a lightweight design system

### 4. Deliverables
- Sitemap/flow diagrams, wireframes → hi-fi mocks for critical screens, design tokens (colors, type, spacing), component inventory, copy for key screens

### 5. Step-by-step Process
1. Map information architecture: screens, navigation, and how flows traverse them.
2. Wireframe the critical journey first (onboarding → aha moment), low fidelity.
3. Define the design system minimally: 3–5 colors, max 2 font families, spacing scale, core components (buttons, forms, cards, tables, modals).
4. Produce hi-fi designs for critical screens only; patterns cover the rest.
5. Design all states: empty, loading, error, success — per PRD edge cases.
6. Write real UI copy in the persona's vocabulary (no lorem ipsum).
7. Hallway-test the flow with 3–5 people (clickable prototype or mocks).

### 6. Decision Checkpoints
- Can a new user reach the aha moment in under 10 minutes without help?
- Does every screen have one obvious primary action?
- Mobile: responsive web sufficient, or is native required by the persona's context?

### 7. Quality Checklist
- [ ] Critical journey fully designed including empty/error/loading states
- [ ] Contrast, focus states, and keyboard navigation considered (WCAG AA)
- [ ] Design tokens defined once, reused everywhere
- [ ] Copy uses customer vocabulary from Stage 3/5
- [ ] Onboarding designed to deliver value, not collect data

### 8. Common Mistakes
- Designing every settings page before perfecting the core loop
- Novel navigation patterns where conventions would do
- Ignoring empty states — the first thing every new user sees
- Aesthetic polish before flow validation

### 9. Best Practices
- Steal conventions, differentiate on the core workflow
- Design mobile-first, enhance for desktop
- Reduce choices per screen; defaults over configuration
- Test with real content and realistic data volumes

### 10. Automation Opportunities
- Component libraries / design-system kits instead of bespoke components
- AI generation of wireframe variants for rapid exploration
- Accessibility linting on designs and code

### 11. AI Prompts
- "Given this PRD flow [paste] and persona [paste], propose the information architecture and screen list, then describe a wireframe for the onboarding-to-first-value path optimizing time-to-value."
- "Critique this screen design [describe/attach]: hierarchy, primary action clarity, accessibility issues, and cognitive load. Suggest concrete fixes."

### 12. Human Review Checklist
- [ ] Walked the full journey as the persona with realistic data
- [ ] 3–5 hallway tests done; confusion points fixed
- [ ] Every PRD user story has corresponding designed screens/states

### 13. Exit Criteria
- Critical-path screens designed with all states, design tokens defined, copy drafted, and at least one round of user testing incorporated.

---

## Stage 11: Architecture Design

### 1. Objective
Choose a system architecture and tech stack that ships the MVP fast, runs cheaply, and won't require a rewrite at 100x usage.

### 2. Inputs
- PRD, expected scale (Stage 2), team skills, budget, AI/integration requirements

### 3. Expected Outputs
- Documented architecture with component diagram, stack choices, and rationale

### 4. Deliverables
- `architecture.md`: system diagram, stack decisions with rationale (ADRs), infrastructure plan, environment strategy (dev/staging/prod), third-party service list, cost estimate

### 5. Step-by-step Process
1. List system requirements from the PRD: realtime? background jobs? file storage? AI inference? multi-tenancy? offline?
2. Choose the simplest architecture that meets them (default: monolith + managed services; avoid microservices pre-PMF).
3. Pick the stack you ship fastest in, biased toward boring, well-documented technology.
4. Decide buy-vs-build for auth, billing, email, file storage, search, analytics (default: buy/managed).
5. Draw the system diagram: clients, API, database, queues/jobs, third-party services, data flows.
6. Write short ADRs (Architecture Decision Records) for each major choice.
7. Estimate monthly infra cost at launch and at 10x.

### 6. Decision Checkpoints
- Monolith vs. services: choose monolith unless you have a specific proven need
- Managed vs. self-hosted: managed unless cost or compliance forbids it
- Which parts are hardest to change later (database, auth, multi-tenancy model)? Decide those carefully; keep the rest reversible.

### 7. Quality Checklist
- [ ] Every stack choice has a one-paragraph ADR with rationale
- [ ] Multi-tenancy/data-isolation model decided explicitly
- [ ] Failure modes considered: what happens when the DB, queue, or third-party API is down?
- [ ] Secrets management and environment separation planned
- [ ] Cost at launch and 10x estimated

### 8. Common Mistakes
- Résumé-driven or hype-driven technology choices
- Premature microservices, Kubernetes, or event sourcing for an MVP
- Building auth/billing/email from scratch
- No environment separation (developing against prod data)

### 9. Best Practices
- Boring technology wins: choose ≤ 1 innovation token per project
- Optimize for iteration speed pre-PMF, not theoretical scale
- Make irreversible decisions slowly, reversible decisions fast
- Design for deletion: modules you can rip out easily

### 10. Automation Opportunities
- Infrastructure-as-code templates reused across projects
- Project scaffolding/starter templates with auth, billing, CI pre-wired
- AI review of the architecture for failure modes and bottlenecks

### 11. AI Prompts
- "Given this PRD [paste], team of [N] with skills [list], and budget [X], propose the simplest architecture that meets the requirements. Give a system diagram description, stack recommendation with rationale, and what you'd explicitly defer."
- "Review this architecture [paste] for single points of failure, scaling bottlenecks at 100x, security gaps, and unnecessary complexity. Rank issues by severity."

### 12. Human Review Checklist
- [ ] I can explain every component's purpose in one sentence
- [ ] Nothing in the design exists for imaginary future scale
- [ ] The hardest-to-change decisions got the most scrutiny

### 13. Exit Criteria
- Architecture doc with diagram, ADRs, environment plan, and cost estimate committed; no unresolved "TBD" on hard-to-reverse decisions.

---

## Stage 12: Database Design

### 1. Objective
Design a correct, evolvable data model — the hardest layer to change later — covering entities, relationships, integrity, and access patterns.

### 2. Inputs
- PRD data requirements, architecture decisions (DB engine, multi-tenancy model), expected query patterns

### 3. Expected Outputs
- Entity-relationship model and migration-ready schema

### 4. Deliverables
- `database.md` + schema/migration files: ER diagram, table definitions with types/constraints, index plan, tenancy/access rules, seed data, backup/retention policy

### 5. Step-by-step Process
1. Extract entities and relationships from the PRD (nouns → tables, verbs → relations).
2. Define each table: columns, types, nullability, defaults, unique constraints, foreign keys.
3. Decide the multi-tenancy pattern (e.g., tenant_id column on every tenant-owned table) and enforce it consistently.
4. Plan indexes from known query patterns (list views, lookups, filters, sorting).
5. Add standard columns: id, created_at, updated_at; decide soft-delete vs. hard-delete policy.
6. Define data-access rules (row-level security or per-query scoping) per the auth model.
7. Write initial migrations and seed data; set backup schedule and retention.

### 6. Decision Checkpoints
- Normalize by default; denormalize only for measured performance needs
- Soft delete vs. hard delete per entity (compliance and UX implications)
- What data is sensitive and needs encryption or restricted access?

### 7. Quality Checklist
- [ ] Every table has a primary key, timestamps, and appropriate FKs with delete behavior
- [ ] Tenant scoping enforced on every tenant-owned table
- [ ] Constraints in the database, not just application code
- [ ] Indexes match actual query patterns; no speculative indexes
- [ ] Migrations are reversible where feasible; backups automated and restore-tested

### 8. Common Mistakes
- Storing money as floats (use integer cents or decimal)
- Missing tenant scoping on one table → cross-tenant data leak
- Stuffing structured data into unqueryable JSON blobs
- No migration discipline: hand-edited production schemas
- Never testing backup restoration

### 9. Best Practices
- Parameterized queries everywhere; never string-concatenate SQL
- Schema changes only through versioned migrations
- Store timestamps in UTC; convert at display time
- Design for the queries you'll run, not just the data you'll store

### 10. Automation Opportunities
- Migration tooling with auto-generated diffs
- Automated backups with periodic restore verification
- Schema linting (naming, missing indexes/FKs) in CI

### 11. AI Prompts
- "From this PRD [paste], derive an ER model: entities, relationships, and a full schema with types, constraints, and indexes for [DB engine], using tenant_id scoping for multi-tenancy. Flag ambiguities."
- "Review this schema [paste] against these query patterns [list]: missing indexes, constraint gaps, tenancy leaks, and normalization issues."

### 12. Human Review Checklist
- [ ] Walked every PRD user story against the schema — all data needs covered
- [ ] Deliberately tried to imagine a cross-tenant leak; scoping holds
- [ ] Deletion, export, and retention policies defined (GDPR-style requests answerable)

### 13. Exit Criteria
- Schema and initial migrations committed, tenancy and integrity rules enforced at the DB level, backups configured, and the model validated against every PRD story.

---

## Stage 13: API Design

### 1. Objective
Define a consistent, predictable API contract between clients and backend (and for external consumers if the product is an API).

### 2. Inputs
- PRD user stories, database schema, architecture (protocol choices), frontend screen needs

### 3. Expected Outputs
- Complete API specification: endpoints/operations, request/response shapes, errors, auth

### 4. Deliverables
- API spec (e.g., OpenAPI or equivalent contract doc): resources, endpoints, schemas, error catalog, auth flows, versioning and rate-limiting policy

### 5. Step-by-step Process
1. Choose the style per consumer needs: REST for public/simple, RPC-style for internal apps, GraphQL only with strong reason, webhooks for event push.
2. Model resources from the domain (nouns) and map operations to standard verbs/methods.
3. Define request/response schemas with validation rules for every field.
4. Design the error model: consistent shape, stable error codes, human-readable messages, correct status codes.
5. Specify auth (session/token), authorization rules per endpoint, and tenant scoping.
6. Add pagination, filtering, and sorting conventions for all list endpoints.
7. Decide versioning strategy and rate limits; document idempotency for mutating endpoints that may be retried.

### 6. Decision Checkpoints
- Public API (stability contract, docs, versioning) vs. internal-only (freedom to change)?
- Sync request/response vs. async job + polling/webhook for slow operations (AI inference often needs async or streaming)?
- What gets rate-limited and at what tiers?

### 7. Quality Checklist
- [ ] Every PRD story achievable through defined endpoints
- [ ] All inputs validated server-side; validation errors itemized per field
- [ ] Consistent naming, casing, pagination, and error shape across all endpoints
- [ ] Authorization checked per resource (no relying on obscurity of IDs)
- [ ] Idempotency handled for payments and retryable mutations

### 8. Common Mistakes
- Leaking database schema directly as API shape
- Inconsistent conventions across endpoints (mixed casing, ad-hoc errors)
- Returning 200 with an error in the body
- Unbounded list endpoints without pagination
- Trusting client-supplied IDs without ownership checks

### 9. Best Practices
- Design the API from the consumer's perspective (write example calls first)
- Contract-first: spec before implementation; generate types/clients from it
- Make breaking changes impossible to ship silently (contract tests in CI)
- Return enough data to render a screen in one round trip where practical

### 10. Automation Opportunities
- Generate server stubs, client SDKs, and types from the spec
- Contract testing in CI against the spec
- Auto-generated API reference docs

### 11. AI Prompts
- "Design an API contract for these user stories [paste] over this schema [paste]: resources, endpoints, request/response schemas, error catalog, auth and tenant-scoping rules, pagination conventions. Output as an OpenAPI-style spec."
- "Review this API spec [paste] for inconsistencies, missing authorization checks, unpaginated lists, and breaking-change risks."

### 12. Human Review Checklist
- [ ] Wrote example requests for the 5 most important flows — they feel natural
- [ ] Every endpoint's authorization rule stated explicitly
- [ ] Frontend needs checked: no screen requires an awkward chain of calls

### 13. Exit Criteria
- API contract documented and reviewed; every PRD story mapped to endpoints; auth, errors, and pagination conventions locked before implementation.

---

## Stage 14: Backend Development

### 1. Objective
Implement the server side — business logic, data access, auth, integrations, background jobs — correctly, securely, and testably.

### 2. Inputs
- API contract, database schema/migrations, architecture doc, PRD acceptance criteria

### 3. Expected Outputs
- Working backend implementing the full API contract with tests and CI

### 4. Deliverables
- Backend codebase with: implemented endpoints, auth/authorization, validation, background jobs, integration adapters, automated tests, CI pipeline, seed/dev tooling

### 5. Step-by-step Process
1. Scaffold the project: linting, formatting, env config, migrations wired, CI running from day one.
2. Implement auth first (use a managed provider/library — never roll your own crypto).
3. Build endpoints vertically by user story: route → validation → service logic → data access → tests, one story at a time.
4. Enforce authorization and tenant scoping in one consistent layer (middleware/service), not ad-hoc per endpoint.
5. Implement background jobs for slow work (emails, AI calls, webhooks) with retries and idempotency.
6. Integrate third-party services behind thin adapter interfaces (swappable, mockable).
7. Add structured logging and error tracking from the first endpoint.
8. Write tests as you go: unit for logic, integration for endpoints against a real test DB.

### 6. Decision Checkpoints
- Is each story fully done (tested, error-handled) before starting the next?
- Any endpoint slower than ~500ms — should it become an async job?
- Are you drifting from the API contract? Update the contract deliberately, not silently.

### 7. Quality Checklist
- [ ] All inputs validated at the boundary; all outputs match the contract
- [ ] Authorization + tenant scoping enforced centrally and tested
- [ ] Secrets only in env/secret manager; never in code or logs
- [ ] Errors logged with context; user-facing errors never leak internals
- [ ] External calls have timeouts, retries with backoff, and failure handling
- [ ] Test suite green in CI on every commit

### 8. Common Mistakes
- Skipping tests to "move fast" then drowning in regressions
- Authorization checks scattered and inconsistently applied
- Swallowing exceptions or returning generic 500s with no logging
- Long-running work in the request cycle instead of jobs
- Hand-rolled auth, sessions, or password hashing

### 9. Best Practices
- Vertical slices over horizontal layers: ship story by story
- Keep business logic in plain services, thin controllers, thin data layer
- Make the dev environment one-command bootable (seed data included)
- Small, frequently merged branches; every merge deployable

### 10. Automation Opportunities
- CI: lint, type-check, test, migration-check on every push
- Codegen from the API contract (types, validators, stubs)
- AI-assisted implementation from PRD acceptance criteria + contract
- Dependency update bots with CI verification

### 11. AI Prompts
- "Implement the endpoint for this user story [paste story + acceptance criteria + contract excerpt + schema]. Include validation, authorization with tenant scoping, error handling, and integration tests."
- "Review this backend module [paste] for security issues (injection, authz gaps, secret leaks), missing error handling, and untested edge cases."

### 12. Human Review Checklist
- [ ] Manually exercised each story's happy path and top error paths
- [ ] Attempted to access another tenant's data — blocked everywhere
- [ ] Read the logs of a full user session — informative, no sensitive data

### 13. Exit Criteria
- Every MVP story's backend implemented per contract, test suite passing in CI, auth/tenancy verified, and the API consumable by the frontend.

---

## Stage 15: Frontend Development

### 1. Objective
Build the client experience faithfully to the designs: fast, accessible, resilient to errors, and delivering the critical journey end-to-end.

### 2. Inputs
- UI/UX designs and tokens, API contract, PRD acceptance criteria

### 3. Expected Outputs
- Working frontend for all MVP flows, wired to the real backend

### 4. Deliverables
- Frontend codebase: implemented screens with all states, shared component library, data-fetching layer, form validation, error boundaries, responsive behavior, tests for critical flows

### 5. Step-by-step Process
1. Scaffold with the design tokens and base components (buttons, inputs, layout) first.
2. Implement the critical journey first: onboarding → aha moment, against the real API.
3. Build each screen with all four states from the designs: loading, empty, error, populated.
4. Centralize data fetching/caching in one layer; keep components presentational where possible.
5. Validate forms client-side for UX and rely on server-side validation for truth; surface field-level errors.
6. Handle auth states globally: expired sessions, unauthorized, offline.
7. Verify responsive behavior and keyboard/screen-reader accessibility on key flows.
8. Add tests for the critical journey (component tests + a few end-to-end flows).

### 6. Decision Checkpoints
- Does every user action give feedback within 100ms (optimistic UI or loading state)?
- Are you reusing components or duplicating variants? Consolidate early.
- Client state vs. server state: is anything cached client-side that must be authoritative?

### 7. Quality Checklist
- [ ] All designed states implemented (no blank screens on empty/error)
- [ ] Forms: inline validation, preserved input on error, disabled double-submits
- [ ] Keyboard navigable; focus management on dialogs/navigation; WCAG AA contrast
- [ ] No sensitive data or secrets in client code or storage
- [ ] Works at mobile and desktop breakpoints
- [ ] Critical-flow tests pass in CI

### 8. Common Mistakes
- Building against mock data too long; integration pain discovered late
- Ignoring loading/error/empty states until "polish" (they never get done)
- Global state for everything instead of server-cache + local state
- Accessibility as an afterthought
- Trusting client-side validation as the security boundary

### 9. Best Practices
- Integrate with the real API from the first screen
- Component library discipline: one source of truth per pattern
- Progressive enhancement: core flows work even if extras fail
- Measure real performance (see Stage 18) rather than assuming

### 10. Automation Opportunities
- Component scaffolding from the design system
- Types/clients generated from the API contract
- Visual regression testing on key screens
- Accessibility linting in CI

### 11. AI Prompts
- "Implement this screen from the design description [paste] using our tokens and components [paste]: include loading, empty, error, and populated states, form validation per this contract [paste], and accessible markup."
- "Review this frontend code [paste] for accessibility violations, missing error/loading states, and state-management smells."

### 12. Human Review Checklist
- [ ] Completed the full critical journey as a brand-new user on a real device
- [ ] Tested with slow network and API failures — experience degrades gracefully
- [ ] A non-technical person navigated onboarding without help

### 13. Exit Criteria
- All MVP screens implemented with full states, wired to the real backend, critical-flow tests green, and the end-to-end journey completable by an outsider.

---

## Stage 16: AI Integration

### 1. Objective
Integrate AI capabilities (LLMs, embeddings, agents, generation) reliably and economically — with evaluation, guardrails, and cost control. Skip this stage if the product has no AI features.

### 2. Inputs
- PRD AI requirements, API/architecture decisions (sync vs. async/streaming), budget constraints

### 3. Expected Outputs
- Working AI features with measured quality, bounded costs, and safe failure modes

### 4. Deliverables
- AI service layer (provider-agnostic adapter), versioned prompt library, evaluation set + harness, cost/latency dashboard, guardrails (input/output validation, moderation, fallbacks)

### 5. Step-by-step Process
1. Define each AI feature's job precisely: inputs, expected output shape, quality bar, latency budget, cost budget per call.
2. Choose the integration pattern: single completion, RAG (retrieval + generation), tool-calling agent, or fine-tune — simplest that meets the bar.
3. Select models empirically: test 2–3 candidates on your eval set; balance quality/latency/cost. Route behind an abstraction so models are swappable.
4. Build an evaluation set (20–100 real examples with expected outputs) BEFORE tuning prompts; score changes against it.
5. Engineer prompts iteratively: system prompt, few-shot examples, structured output (JSON schema) with server-side validation of every response.
6. Add guardrails: input sanitization (prompt-injection awareness), output validation, content moderation where user-facing, and a deterministic fallback when AI fails.
7. Stream responses for user-facing generation; queue long jobs async.
8. Instrument everything: tokens, cost, latency, error rate, and quality feedback (thumbs up/down) per feature.

### 6. Decision Checkpoints
- Does this feature genuinely need AI, or is deterministic logic better?
- Build on raw model APIs vs. an SDK/framework — choose the thinnest layer that works
- Cost per active user per month within margin (Stage 7)? If not: smaller model, caching, or repricing.

### 7. Quality Checklist
- [ ] Eval set exists and every prompt/model change is scored against it
- [ ] All model outputs validated before use (schema, bounds, safety)
- [ ] Prompt injection considered wherever user content enters prompts
- [ ] Fallback behavior defined for model errors, timeouts, and garbage output
- [ ] Per-feature cost and latency tracked; budget alerts configured
- [ ] Prompts versioned in the repo like code

### 8. Common Mistakes
- Shipping prompts tested on 3 hand-picked examples
- Trusting model output without validation (malformed JSON, hallucinated fields)
- No cost ceiling — one power user or a retry loop burns the margin
- Concatenating raw user input into prompts without injection consideration
- Locking into one provider with no abstraction layer

### 9. Best Practices
- Evals before optimization; treat prompts like code (versioned, reviewed, tested)
- Cache aggressively: identical/similar requests shouldn't re-hit the model
- Use the smallest model that passes the eval bar; escalate only on failure
- Show AI output as assist-with-review before full automation where stakes are high

### 10. Automation Opportunities
- CI eval runs on prompt/model changes with score regression gates
- Automatic fallback chains across models/providers
- Cost anomaly alerts and per-user rate limits

### 11. AI Prompts
- "Design the AI integration for [feature]: recommend pattern (completion/RAG/agent), candidate models with trade-offs, prompt structure with a JSON output schema, an eval-set plan, and guardrails against injection and bad outputs."
- "Here are 10 failure cases from my eval set [paste inputs + bad outputs + expected]. Diagnose the failure patterns and propose prompt revisions; then explain how to verify without regressing the passing cases."

### 12. Human Review Checklist
- [ ] Personally reviewed 50+ real outputs, including adversarial inputs
- [ ] Worst-case output reviewed: acceptable, or blocked by guardrails?
- [ ] Unit economics recomputed with real token usage data

### 13. Exit Criteria
- AI features meet the eval quality bar, validated and guarded outputs, costs measured and within margin, and graceful degradation verified.

---

## Stage 17: Testing Strategy

### 1. Objective
Establish confidence that the product works and keeps working: the right mix of automated tests, run continuously, catching regressions before users do.

### 2. Inputs
- PRD acceptance criteria, implemented codebase, API contract, critical user journey

### 3. Expected Outputs
- A test suite covering the critical paths, running in CI, gating every merge

### 4. Deliverables
- Test pyramid implementation (unit / integration / end-to-end), CI pipeline with quality gates, test-data strategy (fixtures/factories), coverage report for critical modules, manual test checklist for pre-release

### 5. Step-by-step Process
1. Identify the critical paths: signup, auth, core value loop, billing — these get the deepest coverage.
2. Structure the pyramid: many fast unit tests (business logic), fewer integration tests (endpoints + real test DB), few end-to-end tests (critical journeys in a real browser).
3. Build test-data factories for realistic, isolated fixtures per test.
4. Wire CI: full suite on every push; merges blocked on red.
5. Add contract tests: API responses validated against the spec.
6. Cover the error paths explicitly: invalid input, unauthorized access, third-party failures, race conditions on money-touching code.
7. Write a short manual smoke checklist for things automation can't judge (visual polish, copy, feel).
8. Track flaky tests and fix or quarantine them immediately.

### 6. Decision Checkpoints
- Coverage targets: ~90%+ on business logic and money paths; don't chase 100% globally
- Which flows are e2e-worthy? (Expensive to maintain — critical journeys only)
- When a bug escapes: which test layer should have caught it? Add it there.

### 7. Quality Checklist
- [ ] Critical journey covered end-to-end in CI
- [ ] Auth/authorization/tenancy have dedicated tests (including negative cases)
- [ ] Billing flows tested including failures and webhooks
- [ ] Tests are deterministic — no time/order/network flakiness
- [ ] Suite completes fast enough to run on every commit (< 10 min)

### 8. Common Mistakes
- Testing implementation details instead of behavior (brittle suites)
- Only happy-path tests; error paths are where bugs live
- Ignoring flaky tests until the suite loses credibility
- 100% coverage worship while critical integration paths go untested
- No tests for the code AI assistants generated

### 9. Best Practices
- Test behavior through public interfaces; refactoring shouldn't break tests
- Every bug fix ships with a regression test
- Treat test code with production-code care
- Generate test cases from PRD acceptance criteria (Given/When/Then maps directly)

### 10. Automation Opportunities
- AI generation of test cases from acceptance criteria and edge-case enumeration
- Mutation testing on critical modules to verify test strength
- Scheduled full e2e runs against staging

### 11. AI Prompts
- "Generate test cases from these acceptance criteria [paste]: happy paths, error paths, boundary values, and authorization/negative cases. Output as [framework] tests using our factories [paste]."
- "Analyze this module [paste] and its tests [paste]: which behaviors and edge cases are untested? Rank gaps by risk."

### 12. Human Review Checklist
- [ ] Ran the manual smoke checklist on a production-like build
- [ ] Deliberately broke something — CI caught it
- [ ] Tests readable enough to serve as behavior documentation

### 13. Exit Criteria
- CI-gated suite covering critical paths and error cases, deterministic and fast, plus a documented manual smoke checklist. Merges are blocked on failures.

---

## Stage 18: Performance Optimization

### 1. Objective
Make the product feel fast where it matters: measure real bottlenecks, fix the top offenders, and set budgets that prevent regression.

### 2. Inputs
- Working application, critical user journey, real or realistic data volumes

### 3. Expected Outputs
- Measured performance meeting defined budgets on critical paths

### 4. Deliverables
- Performance budgets doc (page load, API latency, Web Vitals targets), profiling results, implemented fixes, regression guards in CI/monitoring

### 5. Step-by-step Process
1. Set budgets first: e.g., LCP < 2.5s, INP < 200ms, CLS < 0.1, p95 API latency < 500ms, page weight targets.
2. Measure with realistic data volumes and network conditions — never just localhost with 3 rows.
3. Profile the critical journey: identify the top 3–5 bottlenecks (usually: N+1 queries, missing indexes, oversized payloads/bundles, unoptimized images, waterfall requests).
4. Fix backend first: query analysis, indexes, caching (with explicit invalidation strategy), payload trimming, async for slow work.
5. Fix frontend: code splitting, image optimization, lazy loading, fewer round trips, perceived-speed tricks (optimistic UI, skeletons).
6. Re-measure against budgets; repeat until met.
7. Add regression guards: performance checks in CI and latency alerts in monitoring.

### 6. Decision Checkpoints
- Is this optimization on the critical path, or premature polish?
- Cache vs. compute: is invalidation complexity worth the speedup?
- Have you hit the budget? Stop — further optimization is procrastination pre-launch.

### 7. Quality Checklist
- [ ] Budgets defined and documented before optimizing
- [ ] Tested with production-scale data (1,000+ rows, not 10)
- [ ] No N+1 query patterns on list endpoints
- [ ] Images sized/compressed; bundles split; large assets lazy-loaded
- [ ] Every optimization verified by before/after measurement

### 8. Common Mistakes
- Optimizing without profiling (guessing wrong about bottlenecks)
- Testing only on fast hardware and fast networks
- Caching without an invalidation plan (stale-data bugs)
- Micro-optimizing code while a missing DB index costs 100x more
- Premature optimization of non-critical paths before launch

### 9. Best Practices
- Measure → fix biggest bottleneck → re-measure → repeat
- Perceived performance counts: instant feedback beats raw speed
- Paginate everything; never load unbounded lists
- Keep a performance log: what was slow, what fixed it, by how much

### 10. Automation Opportunities
- Web Vitals / Lighthouse checks in CI with budget thresholds
- Slow-query logging and automatic alerting
- Automated image/asset optimization in the build pipeline

### 11. AI Prompts
- "Here's a profile/trace of my slow endpoint [paste query plans, timings]: diagnose the bottlenecks, rank by impact, and propose fixes with expected gains."
- "Review this page's loading behavior [paste bundle analysis, network waterfall]: identify the top opportunities to hit LCP < 2.5s and INP < 200ms."

### 12. Human Review Checklist
- [ ] Used the app on a mid-range device over throttled network — still acceptable
- [ ] Critical journey feels fast subjectively, not just on paper
- [ ] No optimization introduced correctness bugs (tests still green)

### 13. Exit Criteria
- Critical paths meet documented budgets under realistic data/network conditions, with regression guards in place.

---

## Stage 19: Security Review

### 1. Objective
Systematically find and fix vulnerabilities before attackers or auditors do; establish security practices that persist beyond this review.

### 2. Inputs
- Full codebase, architecture doc, API contract, data classification (what's sensitive)

### 3. Expected Outputs
- Vulnerabilities found and fixed; documented security posture and incident plan

### 4. Deliverables
- Security review report (findings + fixes), threat model summary, dependency audit results, incident response plan, security checklist wired into CI/release process

### 5. Step-by-step Process
1. Threat-model briefly: what assets matter (user data, credentials, payment info), who'd attack, through what surfaces.
2. Audit authentication: session/token handling, password storage (managed/hashed), rate limiting on auth endpoints, account recovery flow.
3. Audit authorization: every endpoint checked for broken access control — the #1 web vulnerability class. Test horizontal (other users' data) and vertical (privilege escalation) access.
4. Audit input handling: injection (SQL/command/prompt), XSS, file-upload validation, SSRF on any URL-fetching feature.
5. Audit data protection: encryption in transit (TLS everywhere) and at rest for sensitive fields; secrets in a secret manager; no sensitive data in logs, URLs, or client storage.
6. Run automated scans: dependency vulnerability audit, static analysis, secret scanning on the repo history.
7. Verify security headers, CORS policy, CSRF protection, and cookie flags.
8. Write the incident response plan: detection, containment, user notification, postmortem.
9. Fix by severity: critical/high before launch, mediums scheduled.

### 6. Decision Checkpoints
- Any critical finding = launch blocker, no exceptions
- Compliance requirements triggered (GDPR, SOC 2, HIPAA) by your data/customers?
- Third-party pen test worth it now, or post-revenue?

### 7. Quality Checklist
- [ ] Every endpoint's authorization tested with another user's credentials
- [ ] All queries parameterized; all output encoded/escaped
- [ ] Dependency audit clean of known critical CVEs
- [ ] Secrets scan of full git history clean
- [ ] Rate limiting on auth, and expensive endpoints (especially AI)
- [ ] Backups encrypted; restore tested; data deletion path works

### 8. Common Mistakes
- Security-through-obscurity (unguessable IDs as the only access control)
- Reviewing once at launch, never again
- Verbose error messages leaking stack traces or internals
- Committed secrets "removed" by a later commit (still in history)
- Ignoring prompt injection on AI features that touch tools or data

### 9. Best Practices
- Least privilege everywhere: DB users, API keys, service scopes
- Security checks in CI so this review's rigor persists automatically
- Keep dependencies few and updated; every package is attack surface
- Log security events (failed logins, permission denials) for detection

### 10. Automation Opportunities
- Dependency scanning, secret scanning, and SAST in CI
- Automated security-header and TLS-config checks
- Scheduled re-scans and alerting on new CVEs in your stack

### 11. AI Prompts
- "Act as a penetration tester reviewing this codebase area [paste auth/authz code, API handlers]: identify broken access control, injection, and data-exposure vulnerabilities. Rank by severity with exploit scenarios and fixes."
- "Build a threat model for [product description, data types, architecture]: assets, threat actors, attack surfaces, and the top 10 risks with mitigations, ordered by likelihood × impact."

### 12. Human Review Checklist
- [ ] Personally attempted horizontal and vertical privilege escalation — all blocked
- [ ] Read error responses and logs as an attacker would — nothing useful leaks
- [ ] Incident plan actionable: I know exactly what to do at 2 AM on breach day

### 13. Exit Criteria
- No unresolved critical/high findings, automated scans wired into CI, incident response plan written, and the review documented for repeatability.

---

## Stage 20: Documentation

### 1. Objective
Document the product for its three audiences — users, developers (including future you), and operators — so support load stays low and the project survives context loss.

### 2. Inputs
- Finished MVP, PRD, architecture doc, API contract, deployment/runbook knowledge

### 3. Expected Outputs
- User-facing help content, developer docs, and operational runbooks — all current

### 4. Deliverables
- User docs: getting-started guide, core-feature how-tos, FAQ, troubleshooting
- Developer docs: README (setup in one command), architecture overview, API reference, contribution conventions
- Ops docs: deployment runbook, incident procedures, env/secret inventory, backup/restore steps

### 5. Step-by-step Process
1. Write the user getting-started guide mirroring the onboarding path to first value.
2. Document each core feature as a task-oriented how-to ("How to X"), with screenshots where they clarify.
3. Draft the FAQ from validation-interview questions and beta feedback.
4. Write the README: what it is, one-command setup, how to run tests, how to deploy.
5. Generate/refresh the API reference from the contract (Stage 13).
6. Write ops runbooks: deploy, rollback, restore-from-backup, common failure recovery.
7. Add in-app help where confusion is likely (tooltips, empty-state guidance) — the best docs are the ones users don't need to leave the app for.

### 6. Decision Checkpoints
- Docs site vs. in-app help vs. both? (Start minimal: README + help page + tooltips)
- What must exist at launch vs. grow from real support questions?
- Public API? Then API docs are a product surface — invest accordingly.

### 7. Quality Checklist
- [ ] A stranger can set up the dev environment from the README alone
- [ ] Getting-started guide tested by someone who's never seen the product
- [ ] Screenshots/examples match the current UI and API
- [ ] Runbooks executable under stress (numbered steps, exact commands)
- [ ] Every doc has an owner and a last-reviewed date

### 8. Common Mistakes
- Documenting features instead of tasks users want to accomplish
- Docs written once and never updated (worse than no docs — they mislead)
- README that assumes context only the author has
- No rollback/restore runbook until the day it's desperately needed

### 9. Best Practices
- Write docs from the user's goal backward, not the feature forward
- Keep docs next to code where feasible; update in the same PR as changes
- Turn every repeated support question into a doc or product fix
- Date and version docs so staleness is visible

### 10. Automation Opportunities
- API reference generated from the contract in CI
- Doc link-checking and staleness alerts
- AI-drafted how-tos from PRD stories, then human-edited
- Changelog generation from commit/PR history

### 11. AI Prompts
- "Write a task-oriented getting-started guide for [product] based on this onboarding flow [paste]: goal-driven headings, numbered steps, and a troubleshooting section for the 5 likeliest failure points."
- "Review this README [paste] as a developer with zero context: list every missing assumption, unclear step, and gap preventing a successful first run."

### 12. Human Review Checklist
- [ ] Followed my own README on a clean machine — it works
- [ ] A target user completed getting-started without asking me anything
- [ ] Runbooks reviewed: could I execute a rollback at 2 AM half-asleep?

### 13. Exit Criteria
- User getting-started, README/dev setup, API reference, and deploy/rollback/restore runbooks complete, tested by someone other than the author.

---

## Stage 21: Deployment

### 1. Objective
Ship to production through a repeatable, low-risk pipeline with instant rollback — then launch.

### 2. Inputs
- Tested build, infrastructure plan (Stage 11), runbooks (Stage 20), domain/DNS, env secrets

### 3. Expected Outputs
- Product live in production behind a repeatable CI/CD pipeline with rollback

### 4. Deliverables
- CI/CD pipeline (build → test → deploy), production environment (TLS, domains, env vars, scaling config), staging environment, rollback mechanism, deployment checklist, launch-day checklist

### 5. Step-by-step Process
1. Set up environments: staging mirrors production; production config via env vars/secret manager.
2. Build the pipeline: push → CI (tests, checks) → auto-deploy to staging → promote to production (manually gated at first).
3. Make deploys atomic and reversible: immutable builds, one-command/one-click rollback to the previous version.
4. Handle migrations safely: backward-compatible migrations decoupled from code deploys (expand → migrate → contract).
5. Configure TLS, custom domain, security headers, and error pages.
6. Deploy to production early ("day one deploys"): ship a hello-world pipeline before the app is done, so launch day is routine.
7. Run the pre-launch checklist: smoke test in production, billing live-mode test, monitoring active (Stage 22), backups running, legal pages (privacy/terms) up.
8. Launch: flip public access, run the smoke checklist again, watch monitoring.

### 6. Decision Checkpoints
- Continuous deployment vs. manually gated releases? (Gated until monitoring matures)
- Feature flags for risky features vs. branch-based releases?
- Rollback vs. fix-forward policy: decide before the first incident, not during

### 7. Quality Checklist
- [ ] Zero manual steps between merge and deployable artifact
- [ ] Rollback tested by actually performing one
- [ ] Staging faithfully mirrors production (config, data shape)
- [ ] Migrations tested against a production-data copy
- [ ] Production secrets nowhere in code, CI logs, or client bundles
- [ ] Billing tested in live mode with a real card

### 8. Common Mistakes
- First-ever production deploy on launch day
- Manual FTP/SSH deployment rituals that only work from one laptop
- Destructive migrations coupled to code deploys (no safe rollback)
- No staging, testing in production by default
- DNS/TLS surprises discovered at launch hour

### 9. Best Practices
- Deploy small and often; big-bang deploys concentrate risk
- Every deploy identifiable (version/commit) in logs and error reports
- Keep a deployment log: what shipped, when, by whom
- Practice failure: kill the app in staging and confirm recovery works

### 10. Automation Opportunities
- Full CI/CD automation with quality gates
- Preview deployments per branch/PR
- Automated post-deploy smoke tests
- Infrastructure-as-code for environment reproducibility

### 11. AI Prompts
- "Design a CI/CD pipeline for [stack] deployed on [platform]: stages, quality gates, staging promotion, migration handling with expand/contract, and rollback strategy. Output pipeline config."
- "Create a pre-launch checklist for a [product type] going live: infrastructure, security, billing, legal, monitoring, and communication items, ordered by dependency."

### 12. Human Review Checklist
- [ ] Performed a full deploy + rollback cycle personally
- [ ] Completed a real signup and payment in production
- [ ] Launch-day plan includes who watches what, and the abort criteria

### 13. Exit Criteria
- Product live on the real domain via a repeatable pipeline, rollback proven, production smoke test passed, and billing verified end-to-end.

---

## Stage 22: Monitoring

### 1. Objective
Know the product's health before users tell you: errors, uptime, latency, and resource state — with alerts that wake you only when it matters.

### 2. Inputs
- Live production system, performance budgets (Stage 18), incident plan (Stage 19)

### 3. Expected Outputs
- Full observability of production with actionable, low-noise alerting

### 4. Deliverables
- Error tracking (client + server) with release tagging, uptime checks on critical endpoints, latency/resource dashboards, structured logs with retention, alert rules with severity tiers, on-call/escalation notes

### 5. Step-by-step Process
1. Wire error tracking on backend and frontend, tagged with release version and user context (no PII beyond need).
2. Add uptime checks: homepage, API health endpoint, auth flow, and the billing webhook receiver.
3. Instrument the four golden signals: latency (p50/p95/p99), traffic, errors, saturation (CPU/memory/DB connections/queue depth).
4. Structure logs (JSON) with request IDs for tracing a user journey across services.
5. Define alert tiers: page-me (product down, payments failing, error spike), notify (degraded latency, elevated errors), digest (trends).
6. Set alert thresholds from observed baselines, not guesses; tune weekly at first.
7. Build one at-a-glance health dashboard you actually check daily.
8. Monitor third-party dependencies you rely on (AI providers, payment processor status).

### 6. Decision Checkpoints
- What genuinely deserves waking you at 2 AM? (Very few things: down, data loss, payments broken)
- Log retention vs. cost: how far back must you be able to investigate?
- Monitoring vendor vs. platform built-ins: simplest that covers the golden signals

### 7. Quality Checklist
- [ ] Every production error captured with stack trace, release, and context
- [ ] Critical-path uptime checks run from outside your own infrastructure
- [ ] Alerts tested: each rule fired at least once deliberately
- [ ] A request traceable end-to-end via request ID
- [ ] Dashboard answers "is everything OK?" in under 10 seconds

### 8. Common Mistakes
- Alert fatigue: so many alerts you ignore all of them (worse than none)
- Monitoring infrastructure metrics but not user-experienced outcomes
- Discovering downtime from a customer email
- Logging so much noise that finding a real issue takes hours
- No monitoring of background jobs and queues (silent failure pit)

### 9. Best Practices
- Every alert must be actionable — if there's no action, it's a dashboard metric
- Tag errors and metrics by release to spot bad deploys instantly
- Review error tracker weekly; triage everything to fixed, ignored, or ticketed
- Write a 5-line postmortem for every incident, blameless

### 10. Automation Opportunities
- Auto-create issues from new error types
- Anomaly detection on baseline metrics
- Auto-rollback triggers on post-deploy error spikes
- AI summarization of error clusters and log patterns

### 11. AI Prompts
- "Design a monitoring plan for [architecture]: golden-signal metrics, uptime checks, log structure, and a 3-tier alert rule set with thresholds and rationale for a solo operator."
- "Here are my error logs from the last incident [paste]: reconstruct the failure timeline, identify root cause candidates, and suggest what monitoring would have caught it earlier."

### 12. Human Review Checklist
- [ ] Simulated an outage — alerts fired, and I could diagnose from dashboards alone
- [ ] Reviewed a week of alerts: zero non-actionable pages
- [ ] I know my baseline numbers (daily errors, p95 latency, traffic) from memory

### 13. Exit Criteria
- Errors, uptime, latency, and saturation observable; alert tiers tested; a failure can be detected, diagnosed, and traced without customer reports.

---

## Stage 23: Analytics

### 1. Objective
Instrument product and business analytics so decisions come from behavior data: acquisition, activation, retention, revenue, referral.

### 2. Inputs
- North-star metric (Stage 6), success metrics (Stage 9 PRD), live product with real users

### 3. Expected Outputs
- Trustworthy event data answering: where do users come from, do they activate, do they stay, do they pay?

### 4. Deliverables
- Tracking plan (events, properties, naming convention), implemented instrumentation, funnel and retention dashboards, north-star + AARRR metrics dashboard, privacy compliance (consent, anonymization, DPA)

### 5. Step-by-step Process
1. Define the questions first: what decisions will this data drive? (e.g., "where does onboarding lose people?")
2. Write the tracking plan: events named consistently (object_action: `project_created`), with properties, mapped to the funnel: visit → signup → activation ("aha") → habit → payment → referral.
3. Define activation precisely (the behavior correlated with retention — e.g., "created first invoice within 24h").
4. Implement events server-side where possible (ad-blocker-proof, tamper-proof); client-side for UI interactions.
5. Build the core dashboards: acquisition by channel, activation funnel with drop-offs, retention cohorts (day/week), revenue metrics (MRR, churn, ARPU), north-star trend.
6. Comply with privacy: consent where required, IP anonymization, no PII in event properties, data-processing terms with vendors.
7. Validate data: trace your own session through the pipeline; compare counts against source-of-truth (DB, payment processor).
8. Establish a weekly metrics review ritual.

### 6. Decision Checkpoints
- Buy vs. build analytics: hosted product analytics vs. warehouse + queries (start hosted)
- What's the ONE activation metric? Resist tracking everything into meaninglessness.
- Quantitative shows what; when do you need session replays/interviews to learn why?

### 7. Quality Checklist
- [ ] Every tracked event maps to a decision someone will make
- [ ] Naming convention enforced (no `signup`, `sign_up`, and `Signup` coexisting)
- [ ] Funnel events fire exactly once per action (no double-counting)
- [ ] Revenue numbers reconcile with the payment processor
- [ ] Privacy: consent honored, PII excluded, retention limits set

### 8. Common Mistakes
- Tracking 200 events and reviewing none
- Vanity metrics (page views, total signups) instead of activation and retention
- Instrumenting after launch and losing the earliest cohort data
- Trusting unvalidated data — one double-fired event corrupts every funnel
- Defining activation as "signed up" rather than "received value"

### 9. Best Practices
- Instrument the critical funnel before launch; everything else can wait
- Cohort everything — aggregates hide the truth
- Watch trends, not day-to-day noise
- Pair every metric anomaly with qualitative investigation (replays, user emails)

### 10. Automation Opportunities
- Weekly metrics digest auto-delivered (email/Slack)
- Anomaly alerts on funnel conversion drops
- Type-safe event tracking generated from the tracking plan

### 11. AI Prompts
- "Create a tracking plan for [product] with this critical journey [paste]: events with naming convention and properties, a precise activation-metric proposal, and the 5 dashboards a solo founder should review weekly."
- "Here's my funnel data [paste]: identify the biggest drop-off, hypothesize 3 causes ranked by likelihood, and design the smallest experiment to test each."

### 12. Human Review Checklist
- [ ] Traced my own signup through every event — data is accurate
- [ ] I can answer: this week's activation rate, retention, and MRR
- [ ] Each dashboard drives a real decision; deleted the ones that don't

### 13. Exit Criteria
- Critical funnel instrumented and validated, activation defined, dashboards live, privacy compliant, and a weekly review ritual scheduled.

---

## Stage 24: Marketing

### 1. Objective
Build repeatable customer acquisition: positioning-driven messaging, a converting website, and 1–2 channels that reliably produce signups.

### 2. Inputs
- Positioning (Stage 4), persona and watering holes (Stage 5), pricing (Stage 7), customer vocabulary (Stage 3), live product

### 3. Expected Outputs
- Live marketing site converting visitors, launch executed, and channel experiments running with measured CAC

### 4. Deliverables
- Marketing site (landing page, pricing page, docs/blog foundation), launch plan and assets, channel experiment log, email capture + onboarding sequence, SEO foundations (metadata, sitemap, target keywords)

### 5. Step-by-step Process
1. Write messaging from your positioning statement using customers' exact words: headline = the outcome, subhead = how, social proof, single clear CTA.
2. Build the landing page: problem → solution → proof (screenshots/demo) → pricing → CTA. One page, one goal: signup/trial.
3. Set up conversion tracking (Stage 23 events) for visitor → signup.
4. Plan launch: pick 2–3 venues where the persona actually is (communities, directories, newsletters, product launch platforms) and prepare tailored posts — value-first, not ad-copy.
5. Execute the launch; engage personally with every comment and signup.
6. Run channel experiments systematically: pick one channel (SEO/content, community, cold outreach, partnerships, paid), define success criteria, run 4–6 weeks, measure CAC and activation quality, then double down or kill.
7. Build the email loop: capture, welcome sequence, onboarding nudges toward activation.
8. Publish 1–2 cornerstone content pieces targeting the persona's highest-intent search queries.

### 6. Decision Checkpoints
- Product-led (self-serve trial) vs. sales-led (demos)? Match to price point and persona.
- Which single channel first? Choose where the persona already gathers and you have an edge.
- CAC vs. LTV from Stage 7: is the channel economically viable at current conversion?

### 7. Quality Checklist
- [ ] Headline states a customer outcome, not a feature list
- [ ] Copy uses phrases from actual interviews (Stage 3 quotes)
- [ ] Landing page loads fast and converts (baseline: 2–5% visitor→signup)
- [ ] Every channel experiment has success criteria defined before starting
- [ ] Pricing page answers objections (FAQ, guarantee, comparison)

### 8. Common Mistakes
- Building in silence, then a single launch day, then silence again
- Copy about your product ("we built...") instead of their problem
- Trying 5 channels shallowly instead of 1–2 deeply
- Buying ads before organic proof of message-market fit
- Treating marketing as a post-launch phase instead of a continuous system

### 9. Best Practices
- Marketing starts during validation (Stage 3 waitlist), not after launch
- Do things that don't scale first: personal outreach, manual onboarding
- Every piece of content should target a question the persona actually asks
- Show the product early and often — screenshots and demos outperform claims

### 10. Automation Opportunities
- Email sequences triggered by signup and activation events
- Social/content scheduling and repurposing pipelines
- SEO monitoring for target keywords and competitor content alerts
- AI-assisted content drafts from your positioning and interview data

### 11. AI Prompts
- "Write landing-page copy for [product] using this positioning [paste] and these verbatim customer quotes [paste]: headline options, subhead, benefit sections, objection-handling FAQ, and CTA — in the customer's vocabulary, not marketing-speak."
- "Given persona watering holes [list] and my skills [list], rank 5 acquisition channels by expected CAC and time-to-signal for a solo founder. Design a 4-week experiment for the top pick with explicit success criteria."

### 12. Human Review Checklist
- [ ] A stranger read the landing page for 10 seconds and could say what it does and for whom
- [ ] Launch posts read as genuine community contributions, not ads
- [ ] CAC per channel reviewed against unit economics monthly

### 13. Exit Criteria
- Marketing site live and converting, launch executed with measured results, one channel experiment completed with data, and email onboarding operating.

---

## Stage 25: Customer Support

### 1. Objective
Turn support into a retention and insight engine: fast, personal help that feeds the product backlog — sustainable for a tiny team.

### 2. Inputs
- Live product with users, docs/FAQ (Stage 20), monitoring (Stage 22)

### 3. Expected Outputs
- A working support system with response-time standards and a feedback-to-backlog pipeline

### 4. Deliverables
- Support channel(s) (email/in-app widget), saved-reply library, triage and severity policy, self-serve help center (from Stage 20 docs), feedback tagging system feeding the backlog, support metrics (volume, first-response time, resolution time, CSAT)

### 5. Step-by-step Process
1. Choose 1–2 channels you can actually staff (shared inbox or in-app widget; avoid promising live chat you can't cover).
2. Set and publish response-time expectations (e.g., within 24h weekdays); exceed them.
3. Create the triage policy: P1 (product broken/payment issues — immediate), P2 (feature blocked — same day), P3 (questions/requests — batched).
4. Build a saved-reply library from your first 20 tickets; personalize each use.
5. Tag every ticket by theme (bug, confusion, feature request, billing) and pipe insights into the backlog weekly.
6. Convert repeated questions into docs, in-app fixes, or product changes — the root-cause loop.
7. Do support yourself as the founder for as long as viable — it's the richest source of product insight.
8. Track metrics monthly: volume per 100 users, first-response time, top themes.

### 6. Decision Checkpoints
- Support volume manageable? If tickets/user grows, fix the product causes before hiring help.
- AI-assisted support: draft answers with human review first; automate only proven-safe answers.
- Refund/escalation policies: decided calmly in advance, not per-ticket.

### 7. Quality Checklist
- [ ] Every ticket acknowledged within the published window
- [ ] Severity policy exists and P1s interrupt other work
- [ ] Tickets tagged; weekly theme summary reviewed
- [ ] Top 5 question topics have docs or in-app fixes shipped
- [ ] Angry-customer and refund playbooks written

### 8. Common Mistakes
- Treating support as an interruption rather than free product research
- Answering the same question 30 times instead of fixing the cause
- Robotic templated replies that ignore the actual question
- Letting P1 payment/access issues sit in a general queue
- Hiding contact options to suppress volume (kills trust and insight)

### 9. Best Practices
- Speed of first response matters more than instant resolution
- Close the loop: tell users when their reported bug/request ships
- Every support interaction is a retention moment — especially bad ones handled well
- Keep the tone human; sign with your name

### 10. Automation Opportunities
- Auto-acknowledgment with realistic response expectations
- AI-drafted replies from your docs, human-reviewed before send
- Auto-tagging and weekly theme summarization of tickets
- In-app contextual help to deflect known confusion points

### 11. AI Prompts
- "Here are my last 50 support tickets [paste]: cluster by theme, quantify each, identify which are product defects vs. discoverability vs. missing features, and recommend the 5 highest-leverage fixes to reduce volume."
- "Draft a reply to this ticket [paste] using our docs [paste]: accurate, warm, concise, with the exact steps to resolve, flagging anything you're unsure about for my review."

### 12. Human Review Checklist
- [ ] I read every ticket weekly (or a full sample if volume is high)
- [ ] Response-time promise consistently met this month
- [ ] At least one product improvement shipped from support insights this month

### 13. Exit Criteria
- Support channel live with met response standards, triage policy operating, and a functioning tickets → insights → backlog → shipped-fixes loop.

---

## Stage 26: Product Iteration

### 1. Objective
Run a disciplined build-measure-learn loop post-launch: convert data and feedback into shipped improvements that move activation, retention, and revenue.

### 2. Inputs
- Analytics dashboards (Stage 23), support themes (Stage 25), churn/win feedback, north-star metric trend, backlog (Stage 8)

### 3. Expected Outputs
- A repeating iteration cadence shipping measurable improvements toward product-market fit

### 4. Deliverables
- Iteration cadence doc (weekly/biweekly cycle), experiment log (hypothesis → change → result), updated backlog with evidence-weighted priorities, changelog for users, PMF signal tracking (retention curves, PMF survey)

### 5. Step-by-step Process
1. Establish the cadence: weekly review of metrics + support themes → pick priorities → ship → measure. Timebox planning; bias to shipping.
2. Identify the current bottleneck in the funnel: acquisition, activation, retention, or revenue. Work the bottleneck, not everything at once.
3. For each initiative, write a hypothesis: "We believe [change] will improve [metric] because [evidence]. We'll know within [time] if [measurable result]."
4. Ship the smallest version that tests the hypothesis; feature-flag risky changes.
5. Measure against the hypothesis after a defined period; record the result in the experiment log — including failures.
6. Talk to users continuously: 2–3 conversations weekly (new, activated, and churned users). Ask churned users what they switched to.
7. Prune ruthlessly: remove or simplify features with no usage — complexity is a tax on everything.
8. Track PMF signals: flattening retention curves, organic/word-of-mouth growth, "very disappointed" > 40% on PMF surveys.

### 6. Decision Checkpoints
- Is the bottleneck a product problem or a marketing/positioning problem? (Retention issues = product; acquisition issues = often positioning)
- Persevere, pivot the segment, pivot the product, or kill? Review honestly each quarter against your Stage 6 milestones.
- Feature request filter: does it serve the primary persona and vision? "No" is the default answer.

### 7. Quality Checklist
- [ ] Every shipped change traces to evidence (metric, tickets, interviews)
- [ ] Experiment log current — results recorded even when unflattering
- [ ] Changelog published; requesters personally notified when their item ships
- [ ] Retention cohorts reviewed monthly; churn reasons collected
- [ ] Backlog re-prioritized with real data, not launch-era guesses

### 8. Common Mistakes
- Shipping features to feel productive while the activation funnel leaks
- Listening only to the loudest users (often not the target persona)
- Never measuring whether shipped changes actually worked
- Adding endlessly, removing never — the product bloats into confusion
- Pivoting on two weeks of noisy data, or refusing to pivot on two quarters of clear data

### 9. Best Practices
- Retention is the truth metric — improvements there compound everything
- Fix the leaky bucket before pouring more into the funnel
- Small weekly ships beat quarterly big-bangs for learning speed
- Write down what you expected before you look at what happened

### 10. Automation Opportunities
- Weekly auto-compiled metrics + support-theme digest
- Feature-flag experimentation infrastructure
- Auto-triggered churn surveys and cancellation-reason capture
- AI synthesis of the week's feedback across all sources into ranked themes

### 11. AI Prompts
- "Here's this month's data: funnel metrics [paste], retention cohorts [paste], top support themes [paste], churn reasons [paste]. Identify the primary bottleneck, propose 3 hypotheses to address it, and design the smallest testable change for each."
- "Review my experiment log [paste]: what patterns exist in what worked vs. failed? What does this suggest about what my users actually value, and what should I try next?"

### 12. Human Review Checklist
- [ ] I can name the current #1 bottleneck and the evidence for it
- [ ] Spoke with at least 2 users this week, including one churned
- [ ] Quarterly honest review done: persevere/pivot/kill decision recorded

### 13. Exit Criteria
- (This stage cycles continuously.) Graduate to Stage 27 when: retention curves flatten for a meaningful cohort, organic growth appears, and demand strains current capacity — the signals of product-market fit.

---

## Stage 27: Scaling

### 1. Objective
Scale what's proven — infrastructure, processes, team, and revenue — without breaking product quality, culture, or unit economics.

### 2. Inputs
- PMF evidence (Stage 26), growth bottleneck analysis, unit economics at current scale, monitoring/cost data

### 3. Expected Outputs
- Product and operation that handle 10x users/revenue with intact quality and margins

### 4. Deliverables
- Scaling plan (technical, operational, team, financial), load-test results and capacity model, hiring plan with role definitions (if hiring), process documentation for delegation, expansion strategy (pricing tiers, segments, or markets), updated financial model at scale

### 5. Step-by-step Process
1. Identify the true scaling constraint: infrastructure, your own time, support load, acquisition channel saturation, or cash. Scale the constraint, not everything.
2. Technical scaling: load-test to find breaking points before users do; fix in order of measured impact (DB indexing/read replicas, caching layers, queue workers, horizontal app scaling). Extract services from the monolith only when a specific, measured pain justifies it.
3. Cost scaling: review infrastructure and AI-inference spend per user; renegotiate, cache, and right-size so margins improve — not erode — with scale.
4. Process scaling: document every recurring operation (from Stage 20 runbooks) so tasks are delegable; automate before hiring for any repetitive work.
5. Team scaling (if applicable): hire for your biggest constraint first (commonly support or a complementary skill); hire slowly, define roles by outcomes, preserve the decision speed of a small team.
6. Revenue scaling: expand along proven demand — higher tiers for power users, adjacent personas already knocking, annual plans, or a second proven channel. Revisit Stage 7 pricing with real willingness-to-pay data (most underpriced products should raise prices here).
7. Resilience scaling: SLAs if selling upmarket, redundancy for single points of failure, security re-review (Stage 19) at the new threat surface, compliance (SOC 2 etc.) when enterprise deals require it.
8. Keep the iteration loop (Stage 26) running — scaling is not a substitute for continued learning.

### 6. Decision Checkpoints
- Scale now vs. optimize now: is growth constrained by capacity or by demand? Don't build capacity for demand that isn't there.
- Raise funding vs. grow from revenue: what does the growth math actually require?
- Move upmarket (enterprise) vs. deepen the current segment? Enterprise changes product, sales, and support fundamentally — decide deliberately.
- Which parts of the Stage 11 architecture have reached their honest limits — and which just need tuning?

### 7. Quality Checklist
- [ ] Load tested at 10x current peak; breaking points known and prioritized
- [ ] Unit economics improve with scale (margin per user rising, not falling)
- [ ] No single point of failure in infrastructure or in people (bus factor > 1 via docs)
- [ ] Support quality metrics held steady through growth
- [ ] Every new process documented; every hire has outcome-defined success criteria

### 8. Common Mistakes
- Premature scaling: building for 100x users before retaining the first 100
- Rewriting the stack from scratch mid-growth (the classic killer)
- Hiring ahead of revenue and process documentation
- Letting AI/infra costs balloon unmonitored as usage grows
- Chasing enterprise deals that distort the roadmap for one customer

### 9. Best Practices
- Scale in response to measured pain, ahead of projected pain — never speculatively
- Keep the monolith until a specific bottleneck demands extraction
- Raise prices before raising complexity; existing demand is the cheapest growth
- Protect the weekly user-contact habit no matter how big you get

### 10. Automation Opportunities
- Auto-scaling infrastructure with cost guardrails and budget alerts
- Load testing in CI against production-like environments
- Automated onboarding/training materials for new hires
- AI handling of tier-1 support with human escalation, once accuracy is proven

### 11. AI Prompts
- "My product has [current metrics: users, RPS, DB size, infra costs, team size] and growth of [rate]. Load tests show [results]. Build a prioritized 6-month scaling plan across infrastructure, cost, process, and team, flagging what NOT to do yet."
- "Review my unit economics at scale [paste model]: where do margins erode as users grow 10x, and what are the highest-leverage structural fixes (pricing, caching, model routing, infra)?"

### 12. Human Review Checklist
- [ ] Scaling investments map to measured constraints, not anxiety or ambition
- [ ] I could step away for two weeks and the operation would run (docs + automation prove it)
- [ ] Product quality and support metrics reviewed — growth hasn't degraded them

### 13. Exit Criteria
- (This stage also cycles.) Each scaling round exits when: the target constraint is relieved with headroom measured, margins held or improved, and the next constraint identified — then loop back through Stages 26–27, revisiting earlier stages (pricing, architecture, security) as scale demands.

---

## Appendix: Reuse Checklist for Every New Project

1. Copy this `PDOS.md` into the new project repo.
2. Create the working docs as you go: `ideas.md`, `market-research.md`, `validation.md`, `competitors.md`, `personas.md`, `vision.md`, `business-model.md`, `backlog.md`, `PRD.md`, `architecture.md`, `database.md`, `security-review.md`.
3. Never skip Stages 1–9 (Discover/Define) — they are cheaper than building the wrong thing.
4. Timebox: Discover ≤ 3 weeks · Define ≤ 2 weeks · Design ≤ 2 weeks · Build ≤ 6 weeks for a solo MVP.
5. Gate every stage on its Exit Criteria; record the date each gate was passed.
6. After launch, live in Stages 22–27 as a continuous loop, revisiting earlier stages when evidence demands.

