# Agents that refuse: a small pattern that changes everything

Most agent prompts I read have one thing in common: they're trying to help. The instructions tell the agent to be useful, supportive, thorough, and clear. Some prompts go further and add personality ("be friendly", "be concise", "be a senior engineer").

Few prompts contain the most important instruction:

> **Refuse to do these specific things.**

This post is about that pattern, why it matters, and how I use it across the agents in this toolkit.

## The problem with helpful-only agents

When you ask Claude (or any frontier model) to help you with a task, the model tries hard to deliver on the task as stated. That's the entire training signal: "the user asked for X, give them X".

This works beautifully for well-specified tasks. It fails for ambiguous decisions and bad inputs.

If you ask the model to "validate my SaaS idea", a helpful-by-default agent will validate it. The model will find ways to argue both sides, but the bias is toward yes — because yes is more help-shaped.

If you ask the model to "price my product at $9/month", a helpful-by-default agent will help you justify $9/month. It will not say "you should probably charge $39 based on the competitive data" unless you specifically open that door.

The missing instruction is the explicit list of things the agent should *not* do regardless of what you ask.

## What "refuse to" looks like in practice

Here's the literal section from the `pricing-strategist` agent in this toolkit:

```
## Refuse to

- Pull pricing out of thin air without competitive benchmarking
- Recommend "free forever" without a clear monetization path
- Suggest gimmicky pricing (random odd numbers, fake "sale" prices)
```

And from `cold-outreach-writer`:

```
## When to refuse

If the founder wants to send the same email to 1,000+ unverified contacts → refuse. 
That's spam, it doesn't work, and it gets domains blacklisted.

If the founder has no clear ICP (Ideal Customer Profile) → refuse. 
Cold outreach without targeting is theater. Send them to the `idea-validator` agent first.
```

These are not safety filters. They're domain-specific refusals based on what makes the underlying task succeed or fail in the real world.

## Why this works

LLMs follow instructions in context. If you say "refuse to X" the model will refuse X — at least the obvious cases of X. The behavior change is large and reliable for prompts that explicitly enumerate refusal cases.

The value of doing this is that the agent's outputs become genuinely useful rather than just superficially compliant. You ask it for a quick pricing recommendation; it pushes back if you haven't done the homework. You ask it to draft a cold email; it asks for an ICP first.

That "push back" is the entire reason this toolkit exists. It's the senior co-founder behavior I want from my agents when I'm tempted to skip the disciplined work.

## Cost of the pattern

Three friction points worth naming:

1. **The agent gets argumentative.** You sometimes know better than the agent does about your specific context. The refusal triggers anyway. You have to either (a) provide the context that bypasses the refusal or (b) override the agent.

2. **Refusals can be wrong.** A blanket "refuse to do X" rule will misfire on edge cases. The agent should have an escape clause ("unless the founder explicitly justifies why this edge case is different").

3. **Token cost.** Refusal sections take 50-200 tokens per agent. Across a multi-agent workflow this adds up. The improvement in output quality more than compensates, but it's worth being aware.

## The hook variant

For the most important refusal — "don't write code outside the MVP spec" — I went one step further and implemented it as a PreToolUse hook (`scope-creep-guard`). The hook intercepts every `Write` or `Edit` operation, checks the project's `MVP-SPEC.md`, and prompts the user if the file path doesn't appear to be in scope.

The difference between a refusal in the prompt and a refusal in the hook is who has the last word. Prompt refusals can be argued past in conversation. Hook refusals require an explicit override action — slow enough that you actually think about it.

For things that should always be slow (touching production, writing code outside scope, deleting data), use hooks. For things that should be carefully reasoned (pricing, scope, positioning), prompt refusals are enough.

## Try it

The full toolkit, including the `pricing-strategist`, `cold-outreach-writer`, `mvp-spec-writer`, and the `scope-creep-guard` hook, is **$19** on Gumroad with the LAUNCH coupon (normally $19, $14 with code).

[Get the toolkit →](https://tastekim.gumroad.com/l/claude-indie-toolkit)

Or just steal the pattern. Add a `## Refuse to` section to your own agent prompts. List 3-5 things the agent should not do under any circumstances. Watch the output quality improve immediately.
