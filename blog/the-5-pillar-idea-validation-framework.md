# The 5-pillar idea validation framework, with examples

This is the methodology behind the `idea-validator` agent in this repo. It's the most-used agent in the toolkit. I'm writing it up in plain English here so you can apply it manually even if you don't use the agent.

## The premise

Most product validation is theater. Founders ask leading questions to friendly contacts, get encouraging answers, and convince themselves the market is real. Six months later, the product launches to crickets.

The job of a real validation framework is to push back hard enough that bad ideas die in 30 minutes instead of 6 months. The cost of saying no to a good idea is one conversation. The cost of saying yes to a bad one is half a year.

## The 5 pillars

Each pillar is scored 1-10, weighted, and aggregated. Any one pillar can trigger a kill criterion that overrides the aggregate.

### Pillar 1: Problem Severity (weight: 25%)

Is this a **painkiller** (must have) or a **vitamin** (nice to have)?

Ask:
- How often does the user hit this problem? (Daily > weekly > monthly > yearly)
- What is the user doing TODAY to solve it? No workaround = no real pain.
- Can you find people complaining about this in public (Reddit, Twitter, forums)?

**Kill criterion**: If users have no existing workaround AND aren't complaining publicly → the problem doesn't exist for them in the way you imagine. Score ≤ 3.

### Pillar 2: Market Size (weight: 20%)

Calculate TAM (total spend on the category), SAM (the slice you can reach), and SOM (what you can capture year 1). Use WebSearch to find industry reports and adjacent product revenue as proxies.

**Kill criterion**: If SOM × realistic price < $50K ARR potential year 1 → too small for a solo founder to justify. Score ≤ 4.

### Pillar 3: Competition (weight: 20%)

Map direct competitors (same problem, same approach), indirect competitors (same problem, different approach), and DIY alternatives (spreadsheet, free tool, manual process).

Counter-intuitive truth: competition is GOOD. It validates the market. The death zone is "no competition" — usually means no market.

**Kill criteria**:
- Zero competitors AND zero indirect solutions → market doesn't exist. Score ≤ 2.
- One dominant competitor with 80%+ market share AND no clear differentiation angle → too late. Score ≤ 3.

### Pillar 4: Willingness to Pay (weight: 25%)

Apply the Mom Test lens:
- Has anyone PAID for a similar solution? Competitor pricing pages = proof.
- Is this B2B or B2C? B2B SaaS converts ~10x easier than B2C.
- Is the budget pre-approved (existing line item) or net-new spend?

**Kill criterion**: If the buyer needs to "create a new budget category" to pay you → 3x harder sale. Score ≤ 5 unless differentiation is overwhelming.

### Pillar 5: Distribution (weight: 10%)

Answer ruthlessly:
- How does the founder reach the first 100 paying customers?
- Does the founder have an unfair distribution advantage (audience, community, employer)?
- Is the channel scalable (paid ads, SEO) or one-time (manual outreach plateaus)?

**Kill criterion**: If the only distribution plan is "I'll post on Twitter and hope" → score ≤ 2.

## A worked example

Idea: "AI task management for solo developers."

- **Problem Severity: 5/10** — Real but well-served. No vocal complaints about current tools.
- **Market Size: 7/10** — Large TAM, but incumbents have captured most willing buyers.
- **Competition: 2/10** — Notion, Linear, Asana, ClickUp, Todoist — all funded, all adding AI features for free. ❌ Kill criterion: dominant competitors with no clear differentiation angle.
- **Willingness to Pay: 4/10** — Buyers already pay for an existing tool. Switching cost high.
- **Distribution: 3/10** — No clear unfair advantage. Paid acquisition in this space is saturated (Notion spends millions).

Weighted score: 4.4/10 + multiple kill criteria triggered.

Verdict: **NO-GO**. Recommended pivot: vertical specialization, workflow plugin on top of an existing tool, or task synthesis (different category) rather than task management.

## Why most validation skips this

The pillars look obvious. The discipline is in actually answering them with evidence rather than vibes. The `idea-validator` agent demands WebSearch evidence for every claim about market size, competitors, and customer complaints. If you can't find evidence, the agent says "unknown" — it never invents numbers.

That single rule kills the majority of false-positive validations.

## Use the agent

The agent is included for free in this repo (MIT-licensed). It implements this framework with explicit kill criteria, evidence requirements, and three action-forcing questions at the end of every report.

```bash
mkdir -p ~/.claude/agents
curl -L https://raw.githubusercontent.com/tastekim/claude-indie-toolkit/main/agents/idea-validator.md \
  -o ~/.claude/agents/idea-validator.md
```

Then in any Claude Code session:

> Use the `idea-validator` agent to evaluate this idea: [your idea].

If the report verdict is NO-GO, accept it. If it's GO, the [full pack](https://tastekim.gumroad.com/l/claude-indie-toolkit) handles the next steps — MVP scoping, pricing, landing page, cold outreach, and launch coordination.
