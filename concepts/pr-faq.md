# PR/FAQ (Working Backwards)

> Source: Amazon's "Working Backwards" practice, popularized by Colin Bryar & Bill Carr (*Working Backwards*, 2021). Write the press release **before** building the product. Forces clarity on customer benefit and distinctiveness.

## The artifact

A PR/FAQ is a 6-page document, two parts:

```
PART 1: PRESS RELEASE (1 page)
├── Headline
├── Subheadline
├── Summary paragraph
├── Customer problem paragraph
├── Solution paragraph
├── Quote from internal exec
├── Customer testimonial quote
└── Call to action

PART 2: FAQ (4-5 pages)
├── External FAQ (customer questions)
└── Internal FAQ (stakeholder questions)
```

Total: ~6 pages. The constraint is the point.

## Why "press release first"

Amazon's reasoning: most product specs are written *to engineers*, in feature/implementation language. By the time the team builds it, they've never articulated *why a customer would care*.

Writing the press release first forces:
1. **Customer-language framing** — what would a journalist write about this?
2. **Distinctiveness clarity** — why is this newsworthy vs incremental?
3. **Outcome focus** — what changes for the customer?
4. **Honesty test** — would this actually be press-release-worthy? If not, why are we building it?

The same idea writ large is **working backwards**: start from the desired customer outcome, then derive what to build.

## The press-release section

Standard 1-page structure. ~250-400 words.

### Headline
What the product does, in customer-benefit terms.
- ✅ "Spotify launches AI playlists that adapt to your mood in real time"
- ❌ "Spotify launches new ML-powered recommendation engine v3.2"

### Subheadline
Specific, concrete benefit + target audience.
- ✅ "Now music listeners can describe how they feel and Spotify generates a 50-song playlist that matches and evolves through the day"

### Summary paragraph
Lede: who benefits, what's launching, why it matters.

### Customer problem paragraph
What sucks today. From the customer's POV, in their language.

### Solution paragraph
How the product solves the problem. Still customer-language. Concrete examples.

### Internal exec quote
"We built X because we believe Y about customer Z." Not corporate fluff.

### Customer testimonial quote
A *fictional* customer reaction, but one that should ring true to the target. Forces you to imagine a real person reacting to this.

### Call to action
What can a reader do? Sign up, download, learn more, etc.

## The FAQ section

5–10 pages of pre-answered questions. Two halves:

### External FAQ (customer-facing)

> Q: What's different about this from [competitor]?
> Q: How much does it cost?
> Q: Will it work on my device?
> Q: Is my data secure?
> Q: How do I get started?

These are the questions the press release will trigger. Pre-answer them.

### Internal FAQ (stakeholder-facing)

> Q: What's the business case? What's the projected revenue?
> Q: What's the engineering cost?
> Q: What are we *not* building, and why?
> Q: What's the riskiest assumption? How will we test it?
> Q: What if competitor ships first?
> Q: What's the failure mode?
> Q: How is success measured? When?

These are what execs and engineers will ask. Pre-answer them.

## The 6-page rule

Bezos famously banned PowerPoint at Amazon. Meetings open with 20 minutes of silent reading of the 6-page memo, then discussion.

Why:
- **Forces written precision** — handwave-able slides become specific paragraphs
- **Gets everyone aligned upfront** — no "wait, what does X mean?" mid-meeting
- **Surfaces gaps** — anything unclear in writing gets challenged

The discipline is hard. A team that can't write a tight 6-page PR/FAQ has not yet thought clearly about what they're building.

## Worked example skeleton

```
HEADLINE: "Acme launches AI legal assistant that drafts contracts in 30 seconds"

SUBHEADLINE: "Now solo lawyers can draft routine contracts instantly,
focusing their time on judgment, not boilerplate"

SUMMARY: ...

PROBLEM: "Solo and small-firm attorneys spend 40% of their billable hours
on routine contract work — work clients won't pay full rate for. AI tools
exist but require legal expertise to use safely; non-AI tools are templates
that don't adapt to client specifics..."

SOLUTION: "Acme integrates with the lawyer's case management system.
Given a client's intake form, it generates a complete contract draft
with citations to relevant statutes and prior firm contracts. Lawyer
reviews and edits in their existing workflow..."

EXEC QUOTE: "We built Acme because we saw small firms losing market
share to AI-savvy larger firms. Our goal is to give them parity..."

CUSTOMER QUOTE: "I used to spend 4 hours per contract. Now I spend
20 minutes reviewing Acme's draft. It's transformed my practice."
— Sarah K., solo practitioner, NYC

CTA: "Start a free 30-day trial at acmelegal.com"

[FAQ section follows...]
```

## When to write a PR/FAQ

- **Net-new product launch** — clarifies whether this is real
- **Major feature with strategic implications** — separates marquee work from incremental
- **Cross-functional alignment** — gives sales/marketing/eng a common frame
- **Strategic kill decisions** — if you can't write a believable press release, don't build

## When less useful

- **Incremental features** — small UI tweaks don't need PR/FAQs
- **Engineering-internal projects** — refactors, migrations
- **Already-validated products in iteration mode** — overhead exceeds value

## Common failure modes

- **Aspirational PR** — describes a product the team can't actually build
- **Customer quote that wouldn't ring true** — if you can't imagine a real customer saying this, the value isn't real
- **FAQ that dodges hard questions** — most useful FAQ items are uncomfortable ones
- **Written after the fact** — used as marketing copy, not as discovery tool. Defeats the point.
- **6-page sprawl** — without word constraint, goes to 30 pages and no one reads

## How it fits with [discovery](continuous-discovery.md)

PR/FAQ is **upstream** of discovery. Before launching an [OST](opportunity-solution-tree.md) or running interviews, ask: would this — if successful — be worth a press release?

If no → kill or rescope.
If yes → that's the *target*. Now do discovery to figure out *how* to deliver it.

## See also

- [Outcomes vs outputs](concepts/outcomes-vs-outputs.md) — PR/FAQ is the customer-facing outcome statement
- [Opportunity Solution Tree](concepts/opportunity-solution-tree.md) — runs *under* the PR/FAQ; finds the path
- [Strong PM](concepts/strong-pm.md) — the writing skill required for good PR/FAQs
- [Product strategy](concepts/product-strategy.md) — PR/FAQ implicitly assumes strategic clarity
- [Mom Test](concepts/mom-test.md) — the customer-quote in PR/FAQ should feel like a real interview, not a slogan
