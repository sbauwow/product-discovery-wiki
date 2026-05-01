# Growth Loops

> Source: Brian Balfour (Reforge, ex-HubSpot), ~2017. Reframes growth from **funnels** (linear, leak-prone) to **loops** (closed, compounding). The defining frame for modern growth practice.

## The thesis

A funnel runs out:

```
Acquisition → Activation → Retention → Revenue → END
```

Each stage leaks. Once revenue happens, the funnel ends. To grow, you re-fill the top — usually by spending more on acquisition. The funnel is a leaky bucket; growth = pouring water in.

A loop *closes back* on itself:

```
Acquisition → Activation → Retention → Revenue ──┐
       ↑                                          │
       └──────  output reinvested as input ──────┘
```

The output of one cycle becomes the input of the next. Growth compounds without external spend.

## Why loops compound

Math:

```
Funnel: each cycle independent. New users / month = constant input.
Loop:   each cycle's output feeds the next. New users / month = (k * users from prior cycle).
        If k > 1, grows exponentially.
        If k = 1, steady state.
        If k < 1, decays.
```

The "k" is the **loop coefficient**: how many new users does one user generate? A loop with k = 1.2 doubles every ~3.8 cycles. A funnel with the same conversion never compounds.

## The five major loop types (Reforge taxonomy)

### 1. Viral / Word-of-mouth loop
User gets value → tells others → others sign up → ...

Examples: Dropbox referral ("invite friends, get more space"), WhatsApp (need to invite to message), early Hotmail ("Sent from Hotmail" footer).

Variables: invitation rate, conversion rate, time-to-invite.

### 2. Paid acquisition loop
User signs up → pays → revenue → re-invested in ads → more signups → ...

Examples: most consumer SaaS, e-commerce, mobile games.

Variable that matters: LTV / CAC. If LTV/CAC > 3, the loop sustains. If < 1, it collapses.

### 3. Content loop
User creates content → content indexed by search → drives organic traffic → new users sign up → create more content → ...

Examples: Pinterest, Reddit, Quora, Glassdoor, Yelp, Stack Overflow.

Critical: user-generated content (UGC) compounds search visibility for free.

### 4. Sales loop
User signs up → expands inside org → sales team upsells → revenue → fund more sales reps → land more accounts → ...

Examples: Salesforce, Datadog, Snowflake.

The "land and expand" pattern. Revenue from one customer funds acquisition of the next.

### 5. UGC / Network density loop
User joins → invites colleagues / consumes others' content → network gets denser → product more valuable → users invite more → ...

Examples: Slack, Notion, Figma, LinkedIn.

This blends with [network effects](network-effects.md). The loop drives the network; the network makes the loop more efficient.

## Worked example: Pinterest content loop

```
1. New user joins (acquisition: paid + organic)
2. User pins images (creation)
3. Pinterest indexes pins; Google surfaces them
4. Searcher lands on Pinterest from Google (organic acquisition)
5. Searcher signs up to save / repin (activation)
6. New user pins more images
7. → Step 3 (compounds)
```

Each user-action expands the searchable inventory, which drives more SEO traffic, which produces more new users. Pinterest's growth came primarily from this loop, not paid acquisition.

## Loops vs [funnels](funnel-analysis.md): when each fits

| Funnel thinking | Loop thinking |
|---|---|
| Optimize stage-by-stage conversion | Optimize the *loop coefficient* |
| Linear, finite | Cyclical, compounding |
| Activity ends after Revenue | Activity restarts each cycle |
| Useful for analyzing existing journey | Useful for designing growth mechanism |
| Tactical | Strategic |

Both are useful. The error is using only one. Funnel diagnoses leaks; loops diagnose whether your growth mechanism is structurally compounding or fundamentally leaking.

## Designing a loop

For any product, ask:

1. **What action does a user take that produces an output others can use as input?**
2. **How does that output reach others?** (Search? Social? In-product? Sales rep?)
3. **What converts a recipient into a new user?**
4. **What re-engages the original user to act again?**

If you can't answer all four, you have a funnel, not a loop.

## Loop coefficient (k)

Roughly:

```
k = (avg outputs per user) × (rate of output → new user conversion)
```

Example for a viral loop:
- Avg invites sent per user = 4
- Invitation acceptance rate = 25%
- → k = 4 × 0.25 = 1.0 (steady state, not compounding)

To compound: increase invites OR conversion. A 4-invite loop with 30% conversion (k=1.2) is dramatically better than 4-invite with 25% (k=1.0). Small differences compound.

## Multi-loop products

The strongest companies run *multiple* loops simultaneously:

| Pinterest | Slack | LinkedIn |
|---|---|---|
| SEO content loop (primary) | Viral within team (primary) | Viral connection loop (primary) |
| Paid acquisition (secondary) | Sales loop (mid-market+) | Content loop (jobs, articles, SEO) |
| Email re-engagement loop | Notification loop | Sales loop (recruiting, premium) |

Each loop reinforces others. Multi-loop products are more defensible than single-loop ones.

## Common failure modes

- **Treating funnel as loop** — describing AARRR stages as a "loop" without identifying the input-output reinvestment
- **Loop without compounding** — k < 1 means the loop is just a slow funnel
- **Imagined loops** — "users will refer friends" without measuring whether they actually do
- **Single-loop dependency** — paid-only loops collapse when ad costs rise; viral-only loops collapse when channel saturates
- **Confusing engagement metrics with loop metrics** — DAU growing isn't proof of a working loop; could be paid spend masking churn

## See also

- [Pirate Metrics (AARRR)](concepts/pirate-metrics.md) — funnel framework; loops are the cyclical complement
- [RARRA](concepts/rarra.md) — retention-first ordering, a step toward loop thinking
- [Network effects](concepts/network-effects.md) — UGC/density loops directly produce network effects
- [Cold-start problem](concepts/cold-start-problem.md) — the hardest part is starting any growth loop from zero
- [Funnel analysis](concepts/funnel-analysis.md) — analytical method that complements loop design
- [PMF](concepts/pmf.md) — without PMF, no loop has positive k
