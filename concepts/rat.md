# Riskiest Assumption Test (RAT)

> Source: Rik Higham, "The MVP is dead. Long live the RAT" (2016). Critique and refinement of the [MVP](lean-startup.md) concept. Closely related to [assumption mapping](assumption-mapping.md), more pointed.

## The critique of MVP

Eric Ries's [MVP](lean-startup.md) was meant to be tiny. In practice, the term became a fig leaf for "minimum viable *product*", which most teams interpret as:

> "A version 1 with all the core features, just less polished."

Result: 6 months of engineering before the riskiest assumption ever gets tested. The original Lean Startup spirit (test the existential question first, cheap) gets lost.

## The RAT reframe

> Don't build a Minimum Viable Product. Build the smallest thing that **tests your riskiest assumption**.

That "thing" might not even be a product:
- Landing page
- Spreadsheet
- Manual concierge
- Slack bot
- Phone call
- Wizard-of-Oz email service

The output isn't a product. It's a **test result**.

## Worked examples

### MVP thinking
"We're building an AI legal assistant. Let's MVP a simplified version with one feature."

→ 4 months engineering. Ship. Discover users don't trust AI for legal. Pivot.

### RAT thinking
"We're building an AI legal assistant. Riskiest assumption: lawyers will *trust* AI-generated drafts enough to use them."

→ 1 day: post in 3 lawyer Slack groups asking "would you review a draft I'm generating with GPT?" Track responses.

→ 2 weeks: manually GPT-generate drafts for 5 willing lawyers. Have them edit. Measure: do they actually use the drafts? Do they pay?

→ Riskiest assumption tested in 2 weeks for ~$0.

The RAT might fail (lawyers won't trust). That's the point — fail fast and cheap, not slow and expensive.

## Picking the RAT

For any product idea:

1. List all assumptions ([assumption mapping](assumption-mapping.md))
2. For each assumption, ask:
   - **What if this is wrong?** (Existential or minor?)
   - **What evidence do we have?** (Lots? None?)
3. The most-existential, least-evidenced assumption = your RAT.

The RAT is a single point of failure. Test that first. Other assumptions can wait.

## Common riskiest-assumption types

| Type | Example | Cheap test |
|---|---|---|
| **Demand** | "Users want this enough to pay" | Landing page + signup form |
| **Behavior** | "Users will do X workflow" | Concierge MVP |
| **Trust** | "Users will trust an AI for high-stakes decisions" | Wizard-of-Oz with humans |
| **Value perception** | "$50/mo is acceptable" | Pre-order with payment |
| **Channel** | "We can reach this segment via Reddit" | Run 3 Reddit posts; measure clicks |
| **Feasibility** | "Model can produce 95% accuracy on Y" | Engineering spike |

## RAT vs MVP — strict definitions

| MVP | RAT |
|---|---|
| Smallest product that produces value | Smallest test of the riskiest assumption |
| Code-shaped by default | Often non-code |
| 1–6 months typical | Days to 2 weeks typical |
| Result: a working product | Result: a yes/no answer |
| Learnings come from usage data | Learnings come from a designed test |

## When to use RAT framing

- **Pre-PMF startups** — every assumption is unvalidated; pick the existential one
- **New features in mature products** — when stakes are high
- **Any time you hear "let's build an MVP"** — push back: "what's the actual riskiest assumption? can we test it without building?"

## When MVP framing is fine

- **Validation already done on demand/behavior** — you know users want it; now build a basic version
- **Product is the test** — some products require usage to validate (e.g. social products with network effects)
- **Mature product line** — extending an existing product where most assumptions are validated

## Common failure modes

- **"RAT" used as buzzword** — same MVP, renamed
- **Multiple "RATs" in parallel** — defeats the point; one assumption at a time
- **RAT that doesn't actually test the riskiest** — easy to pick a comfortable assumption to test
- **Confirmation-bias RAT** — designed to validate, not to falsify
- **Skipping the RAT step** — straight to building because building feels like progress

## The Falsifiability Test

Before running any RAT, ask:

> "What result would falsify our hypothesis?"

If you can't answer — your test is unfalsifiable. Common case: a test where any signup, any positive comment, any click counts as "validation." The team will *find* validation regardless of whether the hypothesis is true.

A real RAT has a pre-committed kill criterion: "If fewer than X people do Y by date Z, we kill this idea."

## See also

- [Assumption mapping](concepts/assumption-mapping.md) — the practice of finding the RAT
- [Lean Startup](concepts/lean-startup.md) — the parent framework (RAT critiques the MVP within it)
- [Prototyping](concepts/prototyping.md) — different prototype types are RAT vehicles
- [Five-second test](concepts/five-second-test.md) — one specific kind of cheap test
- [Mom Test](concepts/mom-test.md) — interviews are often the cheapest RAT
