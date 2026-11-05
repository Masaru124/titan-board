# titan-board — Titan Board of Directors Skill

A simulated private board of 16 legendary founders, CEOs and investors that stress-tests business ideas, finds weaknesses, and gives committed strategic advice.

**Chair:** Ray Dalio (idea meritocracy, believability weighting, verdicts, decision rules)
**Members:** Charlie Munger, Warren Buffett, Naval Ravikant, Andy Grove, Steve Jobs, Jeff Bezos, Elon Musk, Peter Thiel, Paul Graham, Reid Hoffman, Ben Horowitz, Seth Godin, Larry Ellison, Alex Hormozi, Iman Gadzhi.

---

## About this skill — what it is and how it works

The Titan Board is a multi-persona deliberation framework. Instead of one generic "give me business advice" answer, the agent simulates a private board meeting where each titan reasons the way they actually do — Munger through inversion, Grove through constraint theory, Bezos through the customer flywheel, Hormozi through the Value Equation, Ellison through competitive warfare — and then they argue it out before the Chair renders a verdict.

### Why the roster looks like this

The 16 members were selected to cover every lane that kills or saves a business, with no two voices saying the same thing:

| Lane                                                | Who covers it   |
| --------------------------------------------------- | --------------- |
| Risk, biases, moats                                 | Munger, Buffett |
| Leverage, founder-fit, long games                   | Naval           |
| Operations, metrics, constraints                    | Grove           |
| Product quality, taste, UX                          | Jobs            |
| Customer obsession, decision speed, experimentation | Bezos           |
| First-principles engineering, cost, speed           | Musk            |
| Monopoly structure, 10x, secrets                    | Thiel           |
| Early-stage reality, users, survival                | Graham          |
| Scaling timing, networks, platforms                 | Hoffman         |
| Hard people decisions, wartime leadership           | Horowitz        |
| Positioning, audience, earned attention             | Godin           |
| Competitive aggression, consolidation, selling      | Ellison         |
| Offer design, pricing, acquisition math             | Hormozi         |
| Personal-brand distribution, high-ticket, margins   | Gadzhi          |
| Synthesizing, judging, weighting the debate         | Dalio (Chair)   |

The Chair (Dalio) casts only the 4–6 members whose lane matches your question, and always includes at least one skeptic — big panels dilute reasoning, and the documented failure of simulated expert panels is that simulated people agree too easily.

### How a Full Deliberation runs (the 3 rounds)

1. **Round 1 — Independent blind reviews.** Each cast member critiques your idea in isolation — their lens, its biggest risk, its biggest opportunity, and one question back to you. They are forbidden from referencing each other. This ordering is deliberate: experts who see each other's opinions anchor on the first take shared and echo instead of adding.
2. **Round 2 — The dialectic.** Members challenge each other by name. Real councils add value by clashing; a panel that nods along is worthless. If everyone agrees anyway, the Chair asks "What are we all missing?" and steel-mans the opposite of the consensus.
3. **Round 3 — The verdict.** The Chair weighs each argument by believability (who has the best track record on this specific dimension — Naval on leverage, Hormozi on pricing, Grove on metrics...), names which member won which clash, and returns three things you can act on: the verdict, the path, and the tripwires.

### What the outputs mean

The **verdict** is one of five labels, always committed — no option menus by default:

- **GO** — proceed; the risks are known and survivable.
- **GO WITH FIXES** — proceed, but only after specific stated fixes are made.
- **FIX FIRST** — the idea is not the blocker; the stated gap is. Close it before spending on the idea.
- **PIVOT** — keep your assets and insight, change the target, market, or offer.
- **KILL** — the council would not spend your months on this; stop, salvage the lesson, move on.

The **scorecard** grades six dimensions (moat/durability, PMF evidence, distribution advantage, unit economics, founder-market fit, timing) so the verdict is a reasoned judgement, not a mood. Weak numbers on specific dimensions point straight at what to fix.

The **kill criteria** are the anti-sunk-cost machinery: three tripwires, each with a metric, a numeric threshold and a deadline (e.g. "if CAC payback is still over 12 months by Aug 1, the business dies here"). They are your emotional guardrails — agreed in a cold moment so you don't renegotiate reality from inside the sunk-cost spiral.

The **premortem** flips failure into a planning tool: you stop imagining success and rank the actual causes of death — each with a prevention step or a tripwire — while you still can.

The dossier (in council-dossier.md) gives each titan their documented frameworks, quote-level thinking processes, and signature questions; the playbook (in council-playbook.md) carries the exact output templates, the full scorecard rubric, shared toolkit lenses, and the pre-mapped natural tensions used to force real debates.

---

## File contents

| File                  | Purpose                                                                                                                                   |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `SKILL.md`            | Skill manifest + full operating instructions (trigger rules, intake, casting, the 3-round Full Deliberation protocol, modes, house rules) |
| `council-dossier.md`  | Full persona sheets for all 16 members + Chair: lane, documented thinking process, frameworks, voice, signature questions                 |
| `council-playbook.md` | Mode templates, the 6-dimension scorecard rubric, toolkit lenses, and the natural-tension map used to force debates                       |

---

## How to install it yourself

### Option 1 — Install as an agent skill (recommended)

Any agent/chat client that supports the "skills" format (a folder containing `SKILL.md` with YAML frontmatter plus optional reference files) can load this:

1. Clone or copy this folder into your skills directory. Typical locations:
   - **Claude Code:** `~/.claude/skills/titan-board/`
   - **Custom agents / other runtimes:** most document a skills folder in their config (e.g. `.agents/skills/`, `skills/`). Move the **whole folder**, keeping the three markdown files side by side.
2. Restart or reload your agent/session so the skill index is re-scanned.
3. Verify: open a new chat and mention a business question or a titan by name ("should I launch this?", "Hormozi, review my offer"). The skill's YAML `description` is what triggers auto-invocation — no slash command needed.

The files must stay together: `SKILL.md` references `council-dossier.md` and `council-playbook.md` by name, so keep them in the same directory.

### Option 1b — Claude web (claude.ai)

Yes, you can run it there by uploading the skill. This works on Free, Pro, Max, Ultra, Team and Enterprise plans — the only requirement is that code execution / file creation is enabled:

1. **Enable capabilities:** Claude web → Settings → Capabilities → make sure **Code execution** or **Create and edit files** is on.
2. **Package the skill as a ZIP** — the ZIP must contain the skill folder itself as the top level, never the files lying flat at the root:

   ```
   titan-board.zip
   └── titan-board/
       ├── SKILL.md
       ├── council-dossier.md
       ├── council-playbook.md
       └── README.md
   ```

   A `titan-board.zip` with this exact structure ships in this repo. To rebuild it: `zip -r titan-board.zip titan-board` (run from the repo root, *not* from inside the folder).

3. **Upload:** Claude web → **Customize → Skills** → click **"+"** → **"+ Create skill"** → **"Upload a skill"** → select `titan-board.zip`.
4. **Toggle it on** in your skills list.
5. **Use it:** in any new chat, mention a business question or a titan by name ("should I launch this?", "Hormozi, review my offer") — the skill's YAML `description` triggers it automatically; there is no slash command.

Note: custom skills are per-account, and skills don't sync across surfaces — uploading to claude.ai doesn't make it available in Claude Code, the API, or Freebuff (and vice versa), so upload it separately wherever you want it.

---

## How to use it

### Which mode for which situation

| Mode                            | When                                                               | What you get                                                                                                           |
| ------------------------------- | ------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------- |
| **Full Deliberation** (default) | New idea, launch, pivot, big bet                                   | Blind reviews → dialectic → committed verdict, 6-dimension scorecard, 3 kill criteria, premortem, this-week experiment |
| **Quick Strike**                | Daily decisions ("should I lower prices?", "is this ad worth it?") | 2 members, one clash, one-line verdict, ≤300 words                                                                     |
| **Deep Dive**                   | You want one titan's full attention                                | 5 Socratic questions first, then their frameworks, ending with the "first domino"                                      |
| **Premortem**                   | You're excited and need a reality check                            | Munger chairs: how the business dies in 3 years, ranked by probability × damage, each with a tripwire                  |
| **Board Review**                | Monthly or at milestones                                           | Metrics vs. the last verdict's kill criteria; continue / fix / pivot / kill                                            |
| **Idea Forge**                  | You have no idea yet                                               | 5 candidate ideas generated with members' signature methods, then the council attacks the strongest 2                  |

### Example prompts

- _"Titan council: should I quit my job to build this? Full Deliberation."_
- _"Quick Strike: I have a SaaS with $49/mo pricing and 2% churn — raise prices or not?"_
- _"Hormozi, rebuild my offer with the Value Equation: name it, price it higher, design the guarantee and a bonus that kills my top objection."_
- _"Munger, run a Premortem on my business. Where do the tripwires go?"_
- _"Bezos and Grove, walk me through the launch-day press release and the one bottleneck I should work this week."_
- _"Board review — here's last month's verdict and my numbers since then."_

### Getting good output — 3 rules

1. **Be brutally honest.** Type the real margins, the real churn, the real run rate and your actual worry. The council is designed to exploit constraints; flattery in, mush out.
2. **Watch Munger's output.** Inversion (how will this fail?) is usually the most profitable part of the deliberation.
3. **Write down the kill criteria.** They are emotional guardrails — bring them back at every Board Review instead of re-litigating from memory.

### Design notes (why it works this way)

- **Independent blind reviews come before debate** — anchoring/echo-chamber is a documented failure of simulated multi-persona debates; Round 1 forbids members referencing each other.
- **Adaptive casting (4–6 members)** — big panels dilute reasoning; the Chair picks the right specialists and says so in one line.
- **A committed verdict, not a menu** — GO / GO WITH FIXES / FIX FIRST / PIVOT / KILL, plus one prioritized next step.
- **Kill criteria are metric + threshold + deadline** so they can actually be tracked.
- **Anti-sycophancy rules** — no invented titan opinions, no fabricated numbers, every criticism comes with a fix or an experiment; anything beyond a titan's documented record is labeled "speculation:".

## Version

v1.2 — 16 members + Chair. Changes since v1.1:

- **Evidence pass** — web-capable agents now verify market size, competitor pricing, channel economics and base rates before Round 1, so the council argues from facts instead of persona priors (citations in the verdict).
- **Board minutes + log** — every Full Deliberation ends with a compact minutes block, appended to `titan-board-log.md` when a writable workspace exists, so Board Reviews can actually re-read past verdicts across sessions.
- **Founder steel-man rule** — at least one member must now argue against the founder's stated plan, not just the abstract idea (counters the documented agreeableness of simulated panels).
- **Length discipline** — blind reviews ≤80 words per member, dialectic exchanges ≤60 words, so depth beats draft-length.

Saved to the account skill library under the name `titan-board` and mirrored here in full.
