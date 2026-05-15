# Claude Code Indie Hacker Toolkit

> **Ship side projects that make money. Without the 6-month "build trap".**

A production-ready Claude Code toolkit for solo founders. Built around one belief: **most indie products fail at validation and positioning, not at code.**

🛒 **[Get the full toolkit on Gumroad — $19 ($14 with code `LAUNCH`)](https://tastekim.gumroad.com/l/claude-indie-toolkit)**

[![Cover](https://i.imgur.com/RBVJ1kL.png)](https://tastekim.gumroad.com/l/claude-indie-toolkit)

---

## 🎯 Three products, one toolkit family

The Indie Hacker Toolkit is the flagship. If you need just the parts, two focused mini-packs exist:

| Product | Price (LAUNCH) | For |
|---|---|---|
| **[Claude Code Indie Hacker Toolkit](https://tastekim.gumroad.com/l/claude-indie-toolkit)** | $19 ($14) | Solo founders building & shipping side projects end-to-end |
| **[Claude Code Cold Email Pack](https://tastekim.gumroad.com/l/cold-email-pack)** | $9 ($6) | Anyone doing B2B outreach, SDR, fundraising, partnerships |
| **[MVP Spec Templates for Claude Code](https://tastekim.gumroad.com/l/mvp-spec-templates)** | $14 ($10) | Founders who keep starting MVPs that take 6 months instead of 4 weeks |

**Each `LAUNCH` code is valid only for the first 72 hours of launch (until midnight, May 18, 2026).** After that, full price.

---

## What's in the full toolkit

| Component | What it does |
|---|---|
| **5 agents** | `idea-validator`, `landing-page-architect`, `pricing-strategist`, `cold-outreach-writer`, `launch-day-orchestrator` |
| **3 skills** | `mvp-spec-writer` (constraint-driven MVP spec), `competitor-deep-dive`, `revenue-modeler` |
| **2 commands** | `/validate-idea`, `/launch-checklist` |
| **1 guardrail hook** | `scope-creep-guard` — blocks Claude from writing files outside your MVP spec |
| **Docs** | End-to-end workflow guide, install instructions, **🇰🇷 한국어 가이드**, examples |
| **Blog series** | [Why I built this](./blog/why-i-built-this.md) · [5-pillar validation framework](./blog/the-5-pillar-idea-validation-framework.md) · [Agents that refuse](./blog/agents-that-refuse.md) |

Every agent has explicit **kill criteria** and **"refuse to" rules**. They're designed to **tell you NO** before you build the wrong thing.

---

## Free preview agent

This repo ships with **one full agent** as a free preview: `idea-validator`.

Try it. If it pushes back on your half-baked idea the way a senior co-founder would, the full toolkit is yours for $19 (or $14 with code `LAUNCH` during launch week).

```bash
# Install the preview agent
mkdir -p ~/.claude/agents
curl -L https://raw.githubusercontent.com/tastekim/claude-indie-toolkit/main/agents/idea-validator.md \
  -o ~/.claude/agents/idea-validator.md
```

Then in any Claude Code session:
> Use the `idea-validator` agent to evaluate this idea: [your idea]

You'll get a 5-pillar GO/NO-GO report with kill criteria, weighted scores, evidence requirements, and a recommended pivot if NO-GO.

See `examples/sample-validation-report.md` for what the output looks like.

---

## Why this exists

Open-source Claude Code skill libraries have 1,000+ generic prompts. Most assume **the founder already knows what to build**.

But the hard part isn't writing code with Claude Code. It's:

1. Picking an idea that has a market (most don't)
2. Cutting the MVP in half so you ship before quitting
3. Pricing it so the math works
4. Reaching the first 10 buyers
5. Launching without embarrassing yourself

This toolkit codifies the discipline for those five problems.

---

## Real example (from `docs/WORKFLOW.md` in the paid pack)

A founder's idea: "Chrome extension that auto-fills cold email personalization from LinkedIn."

The `idea-validator` agent verdict: **PIVOT NEEDED** (score 6.4/10).
The Chrome extension was a feature, not a product. AI personalization is being matched for free by every existing outreach tool. Her unfair advantage — 18 months of refined manual outreach experience — was the missing wedge.

Renamed product: **Brief.** Repositioned as a research tool (3-bullet briefs), not a generator. Built MVP in 3.5 weeks. Launched. **18 paying customers in 7 days = $342 MRR.**

She didn't quit her job, but she had options.

The full case study walks through every agent's output along the way.

---

## What's in the paid pack vs. this preview

| | This preview repo | Full paid pack ($19) |
|---|---|---|
| `idea-validator` agent | ✅ | ✅ |
| `landing-page-architect` agent | — | ✅ |
| `pricing-strategist` agent | — | ✅ |
| `cold-outreach-writer` agent | — | ✅ (also in [Cold Email Pack](https://tastekim.gumroad.com/l/cold-email-pack)) |
| `launch-day-orchestrator` agent | — | ✅ |
| `mvp-spec-writer` skill | — | ✅ (also in [MVP Spec Templates](https://tastekim.gumroad.com/l/mvp-spec-templates)) |
| `competitor-deep-dive` skill | — | ✅ |
| `revenue-modeler` skill | — | ✅ |
| `/validate-idea` command | — | ✅ |
| `/launch-checklist` command | — | ✅ |
| `scope-creep-guard` hook | — | ✅ |
| End-to-end workflow guide | — | ✅ |
| 한국어 가이드 (Korean adaptation) | — | ✅ |
| 12 cold email templates | — | (in Cold Email Pack) |
| 5 MVP-SPEC templates (SaaS / Extension / AI / Marketplace / Newsletter) | — | (in MVP Spec Templates) |
| Sample outputs and examples | partial | ✅ |
| Commercial license | — | ✅ |
| Lifetime updates | — | ✅ |
| 30-day refund | — | ✅ |

**[Get the full toolkit — $19 (`LAUNCH` → $14, ends May 18, 2026)](https://tastekim.gumroad.com/l/claude-indie-toolkit)**

---

## Star this repo

If the preview agent saves you from building the wrong thing, ⭐ the repo. It helps other solo founders find it.

## License

The preview content in this repo is MIT-licensed for evaluation use.
The full paid toolkit is under a commercial license — see Gumroad listing.

---

Built by [@tastekim](https://github.com/tastekim) — Seoul-based developer who got tired of watching peers spend 6 months building products no one wanted.
