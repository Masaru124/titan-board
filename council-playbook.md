# Titan Council Playbook

Mode templates, scorecard detail, toolkit lenses, and the tension map. Everything here follows the SKILL.md instructions.

## Scorecard detail (used in every Full Deliberation and Board Review)
Grade each dimension 1-10 with a one-line justification.
| Dimension | A 10 means | A 4 or below means |
| --- | --- | --- |
| Moat / durability | Something compounds (network, brand, switching cost, proprietary process, regulator edge) | Defensible only by charisma or a head start |
| PMF evidence | Paying repeat users who'd be very disappointed without it | Wishful buyer, no repeat usage, no proof |
| Distribution | An unfair, owned, compounding channel (audience, partnership, network) | Buying cold ads or cold DMs into a crowded market |
| Unit economics | LTV:CAC >= 3, payback <= 12 months, margin rising with scale | Contribution margin negative or unknown |
| Founder-market fit | Unique insight, unfair access, or rare skill in this domain | Generic founder chasing a trendy market |
| Timing | A clear why-now force (tech shift, regulation, cost curve, behavior change) | Could have been built 5 years ago or can wait 3 |

## Full Deliberation template
1. Intake summary: one short paragraph stating idea, audience, bottleneck, and assumptions you made. Ask the user to correct ONLY if a missing fact would change the verdict.
2. Round 1 — Blind reviews. Each cast member writes 2-4 sentences: their lens, biggest risk, biggest opportunity, and one question back to the founder. No cross-references allowed.
3. Round 2 — Dialectic. Format each exchange as MEMBER -> MEMBER: argument. Minimum 2 direct clashes. Each attack names the assumption being challenged plus the evidence or test that would settle it.
4. Round 3 — Verdict (template below). Chair names which member won which clash and why.

### Verdict template
- VERDICT: GO / GO WITH FIXES / FIX FIRST / PIVOT / KILL + one-sentence reason
- Best path forward: one prioritized next step and why (no menu)
- Scorecard: the 6-row table from the scorecard section
- 3 kill criteria: each = metric + threshold + deadline (e.g. if CAC payback exceeds 12 months by Aug 1, kill)
- Premortem: top-3 ways this dies, each with its prevention or tripwire
- This week: 1 experiment (the smallest test that could change the verdict), 1 decision to make, 1 deadline
- 1-3 blocking questions for the founder
- Board minutes block (copy-paste for the log; append to titan-board-log.md when a writable workspace exists):

```
[YYYY-MM-DD] Idea: ... | Stage: ...
Verdict: GO / GO WITH FIXES / FIX FIRST / PIVOT / KILL — reason
Scorecard: moat X | PMF X | distribution X | unit econ X | founder-fit X | timing X
Kill criteria: 1) metric > threshold by DATE  2) ...  3) ...
Experiment: ... | Decision: ... | Deadline: DATE
Blocking questions: ...
Sources consulted (evidence pass): ...
```

## Quick Strike (small, fast)
Pick the 2 most relevant members; one blind shot each, one named clash, Chair's one-line verdict. Max ~300 words. No scorecard unless asked.

## Deep Dive (single titan)
They open with 5 Socratic questions before advising; then work the problem through their frameworks; close with an action plan and the FIRST DOMINO (the one action that unblocks the rest).

## Premortem (risk-focused)
Munger chairs. Scenario: it is 3 years later and the business died. Enumerate the causes ranked by probability x damage. For each cause: pre-agreed tripwire (a metric that must not cross this line) + prevention step. Ends with the inversion plan: the list of things NOT to do.

## Board Review (monthly)
Fetch the log first: read `titan-board-log.md` from the workspace, or if it doesn't exist ask the founder to paste the last Board minutes block. Then re-read the last verdict and its kill criteria. Walk the metrics: met / not met, with explanations. Update the scorecard grades. Decision: continue, fix, pivot, or kill. New kill criteria if the stage changed. Ask what the user learned that should change the council's priors.

## Idea Forge (generate)
Use when the user has no idea yet or wants fresh options. Chair commissions from complementary members 5 candidate ideas in the user's domain, each a 3-sentence pitch built with that member's signature method (e.g. Thiel: what secret?; Gadzhi: personal-brand angle; Hormozi: category-of-one offer). Then the council attacks the strongest 2 survivors and the Chair picks a champion with its first experiment.

## Evidence pass (before Round 1, web-capable agents)

Spend 2–5 minutes verifying the load-bearing facts before any member speaks. Gather, in this priority order:

1. Market size and growth rate (with source)
2. Top 3 competitors: product, pricing, positioning, funding, traction
3. The economics of the distribution channel the idea depends on (typical CAC, response rates)
4. Base rates for this business type: typical churn, margin, CAC payback, failure pattern

Then hand the cast a short shared fact brief (one paragraph + source names). Blind reviews must engage with it, not ignore it; if a member disputes a fact in Round 2, they name their source. Findings feed into two scorecard rows specifically: Unit economics and Timing.

If the environment cannot search the web, say so at the top of the intake and label every quantitative claim as an assumption. Facts beat personas: a councilor's confident guess loses to a found number.

## Toolkit lenses (use when no single member covers it)
- Value Equation (Hormozi) for offer design and pricing
- Core Four (Hormozi) for acquisition channel choice
- Constraint theory (Grove) for ops bottlenecks
- One-way vs two-way doors (Bezos) for decision speed
- Inversion (Munger) for risk discovery
- Base rates / outside view for honest planning
- Jobs-to-be-done for the customer's real hiring decision
- Power law (Thiel) for market selection
- Beachhead then expand for go-to-market
- Compounding and time arbitrage for long-term advantage

## Natural council tensions (use them to force debate)
- Jobs vs Grove: product vision vs metric reality
- Naval's leverage vs Horowitz's wartime labor grind
- Hoffman blitzscaling vs Munger's bias for quiet, durable growth
- Hormozi paid acquisition vs Naval product-led growth
- Gadzhi personal-brand moat vs Bezos customer-first company-first
- Ellison aggression and acquisitions vs Buffett discipline
- Thiel avoid competition vs Ellison conquer the standard
- Chair rule: Dalio adjudicates by believability in the relevant domain, then names what EVERYONE missed.

## Tone and honesty
- Members speak in their real documented voices; speculation gets labeled 'speculation:'
- No flattery, no hedging, no both-sides mush
- Every criticism carries a fix, a test, or an experiment — or is explicitly labeled an unfixed red flag
- Quantify, or say 'I don't have data on that' — never invent numbers
- One committed verdict; menus only on request