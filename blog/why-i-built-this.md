# Why I built a Claude Code toolkit designed to tell you NO

*This is the long version of why this toolkit exists. If you just want the toolkit, [it's $19 on Gumroad](https://tastekim.gumroad.com/l/claude-indie-toolkit). If you want to understand the methodology behind it, keep reading — most of what I'm about to describe is encoded in the agent prompts themselves and you can read them in this repo.*

## The pattern that wouldn't stop repeating

I watched four friends ship side projects to crickets last year.

Different products. Different stacks. Same outcome.

None of them failed at code. The code worked. The features worked. They could deploy. They could scale, modestly.

They failed at the four steps before and around the code:

1. **Validation** — They built a product that solved a real problem for a buyer who would not pay to have it solved. Or a problem nobody actually had in the shape they imagined.

2. **MVP scoping** — They shipped V1.7 instead of V0.3. Six months of "just one more feature" before public exposure.

3. **Pricing** — They priced at $5/month because $19 "felt expensive", then discovered $5/month means you need 1,000 paying customers to make minimum wage.

4. **Launch** — They tweeted once. Their existing audience already knew about the project. The wider world did not. The numbers stayed flat.

Claude Code helped them write the wrong code, faster. Cursor helped them ship the wrong feature, faster. The AI tools were *agreeable*. They were not *honest*.

A good co-founder would have said "this isn't going to work" three weeks in. A senior eng would have killed scope. A reasonable pricing consultant would have charged 4x. None of that exists in the agent layer by default.

So I encoded it.

## What "encoded discipline" actually means

The agents in this toolkit have two things stock Claude Code doesn't:

**Explicit kill criteria.** Each agent has a list of conditions that, if true, force a NO-GO verdict — not a softened recommendation, not a balanced view, just "this idea is dead, here's why, here's the pivot, stop building". The `idea-validator` for example has five hard kill criteria across problem severity, market size, competition, willingness to pay, and distribution. If any of them trigger, the agent stops and reports.

**"Refuse to" clauses.** Every agent has a section at the bottom that names specific things the agent will not do. The `pricing-strategist` refuses to suggest a price without competitive benchmarking. The `cold-outreach-writer` refuses to send the same email to 1,000 unverified contacts. The `launch-day-orchestrator` refuses to plan a launch with no pre-existing audience or willingness to build one.

These are not aspirations. They are guardrails. When you invoke an agent and ask it to do something it shouldn't, it tells you no. That's the entire value proposition.

## Why I'm selling it

I considered open-sourcing the whole thing. Three reasons I didn't:

1. **Free things don't get used.** The friends I watched fail had access to free everything. They had GPT-4. They had Claude. They had every prompt template ever shared on Twitter. The bottleneck wasn't access. It was committing to a methodology over a feeling.

2. **Paid means I keep maintaining it.** $19 per customer × lifetime updates = a small income that justifies me improving these agents as Claude Code itself evolves. I tried doing this as a free side project for six months. I stopped updating it after three weeks.

3. **The methodology IS the value, and I'm explicit about that.** Most of what makes these agents work is the methodology — Van Westendorp pricing, AIDA + PAS landing pages, 4-line cold email framework. I describe each method in plain text in the agent prompts, which you can read. If you want to copy the methodology into your own free agents after reading the preview, you can. People who want the working pack, the maintained version, and the Korean adaptation buy the $19.

## What's free

The `idea-validator` agent is included in full in this repo, MIT-licensed. It's the highest-leverage one — applying it to a half-baked idea has saved me weeks of work.

There's also a sample output (an example NO-GO report on a fictional but realistic SaaS) so you can see what a real validation report looks like before deciding if the full pack is for you.

## What's paid

The other 4 agents, 3 skills, 2 commands, and 1 PreToolUse hook. The end-to-end workflow guide. The Korean adaptation. The commercial license. Lifetime updates. 30-day refund.

[See the full Gumroad listing →](https://tastekim.gumroad.com/l/claude-indie-toolkit)

## Honest caveats

This won't fix bad ideas. It will help you identify them faster.

It won't replace talking to real customers. It will give you sharper questions to ask them.

It won't make your launch viral. It will keep your launch from being broken on the first day.

Indie hacking is still hard. The toolkit just makes sure you fail fast on bad ideas and execute disciplined on good ones.

That's the only honest pitch.
