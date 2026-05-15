# Sample Output: idea-validator agent

> Real example of what the `idea-validator` agent produces. Idea details fictionalized; the structure and rigor are exactly what you get.

---

## Validation Report: TaskFlow AI

### Verdict: **NO-GO**

Weighted score: **3.8 / 10**
Confidence: **HIGH**

### Scores

- **Problem Severity: 5/10** — Task management is a real but well-served need. Users have many existing workarounds and most are reasonably satisfied. No vocal complaints about current tools rising to the top of public discussion.
- **Market Size: 7/10** — TAM is large ($5B+ annual SaaS task management spend). However, this works against you — incumbents have already captured the customers most willing to pay.
- **Competition: 2/10** — The category is owned by Notion, Linear, Asana, Todoist, ClickUp, and Monday — all with significant funding, ML/AI investment, and switching costs (data lock-in). No clear positioning gap.
- **Willingness to Pay: 4/10** — Buyers already have a tool. New AI features are being added FOR FREE to every incumbent. To displace, you must be 10x better at something specific. "AI-powered" is not 10x.
- **Distribution: 3/10** — Founder has no existing audience in this space. Productivity / task management is a saturated SEO/ad space (Notion spends millions). No clear unfair-distribution wedge.

### Kill Criteria Status

- ❌ **Problem has existing workaround AND public complaints exist** — workarounds exist, but the volume of public complaints is low. Most users tolerate their current tool.
- ✅ SOM × price ≥ $50K ARR realistic — at scale, yes.
- ❌ **Competitive landscape has signal AND a clear wedge** — landscape is dense; the proposed wedge ("AI-powered") is being matched for free by every incumbent.
- ⚠️ Buyer has pre-approved budget category — yes, but already spent on existing tools.
- ❌ **Distribution plan has at least one scalable channel** — founder's only plan is "post on Product Hunt and Twitter". Not scalable; not differentiated.

### Evidence Found

- Notion released "Notion AI" pricing at $10/seat in 2023, now bundled with Plus tier. Source: notion.so/pricing.
- Linear's "Asks", "Magic", and "Initiatives" features added AI-powered task generation in 2024-2025. Source: linear.app/changelog.
- Recent Show HN posts for AI task managers (2025): 30-50 upvotes average, 1-3 sign-ups per upvote, < 5% conversion to paid. Source: HN archive search.
- ProductHunt search for "AI todo": 40+ products launched in last 24 months, with average #15-30 placement. No #1 of the month in this category.

### What I Would Build Instead

If you have skill in this area, the wedge is NOT "AI for tasks". It's one of:

1. **Vertical specialization** — task management for a specific underserved profession (e.g., field service techs, freelance attorneys). Specialize the data model, not just the UI.
2. **Adjacent jobs** — task SYNTHESIS, not task management. E.g., "I dumped 200 voice notes into this app and it produced my Q3 OKRs" — different category, less competition.
3. **A workflow plugin** instead of a standalone app — be the AI layer ON TOP of an incumbent (Notion plugin, Linear app, Slack bot).

### The 3 Questions the Founder Must Answer

1. Name 10 people who would pay $19/month for this specifically, today. Not "people like X" — actual names, with reasoning why they wouldn't just stay on their current tool.
2. What is your unfair advantage that Linear, with $400M in funding and dozens of engineers, cannot copy in 6 months?
3. If you build this for 3 months and 0 customers pay, what specific evidence would convince you to stop? (If you can't answer, you'll never stop.)

---

## Why This Agent Is Different From "Just Asking Claude"

Notice what the agent did:

1. **Pulled specific competitor evidence** instead of saying "the market is competitive".
2. **Quantified the kill criteria** instead of saying "it might be hard".
3. **Refused to validate the idea** despite Total Addressable Market looking attractive.
4. **Offered structural pivots**, not "you could add more features".
5. **Closed with action-forcing questions** the founder cannot bluff their way past.

This is the value of a structured methodology encoded into the agent prompt — and it's the same rigor every agent in this toolkit brings.
