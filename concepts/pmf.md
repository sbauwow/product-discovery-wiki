# Product-Market Fit (PMF)

> Sources: Marc Andreessen ("The only thing that matters", 2007), Sean Ellis (PMF survey, ~2010), Rachleff, Reichheld. The single most-discussed and least-precisely-defined concept in startup product.

## The Andreessen definition

> Product/market fit means being in a good market with a product that can satisfy that market.

Vague but useful. Andreessen continues:

> When a great team meets a lousy market, market wins.
> When a lousy team meets a great market, market wins.
> When a great team meets a great market, something special happens.

Implication: the market is the dominant factor. Great teams in bad markets fail; mediocre teams in great markets succeed. PMF means *being in the right market*.

## How to know you have PMF

### 1. The Sean Ellis test

Survey existing users:

> "How would you feel if you could no longer use [product]?"

Options:
- Very disappointed
- Somewhat disappointed
- Not disappointed
- N/A — I no longer use it

**Threshold: 40%+ "very disappointed"** = PMF. Below 40% = not yet.

Why it works: "very disappointed" is a behavioral proxy for *would they actively miss it?*. Users who'd be very disappointed are users who've integrated the product into their lives.

The 40% threshold comes from Ellis's data across hundreds of startups — products above 40% reliably grew; products below struggled.

### 2. Retention curve flattening

```
Pre-PMF: retention curve goes to zero
  100% │●
       │ \
       │  ●
       │   \
       │    ●
       │     ●─────●
       │            ──●─────●  ← still decaying
       └───────────────────────→

PMF: retention curve flattens at non-trivial level
  100% │●
       │ \
       │  ●
       │   \
       │    ●─────●─────●─────●  ← levels off at, say, 30%+
       │
       └───────────────────────→
```

A flat retention curve means *some users genuinely use the product as part of their lives*. The asymptotic level is your PMF audience.

Benchmarks (Lenny Rachitsky / Mixpanel data):
- Consumer: 25%+ at month 12 = solid PMF
- B2B SaaS: 70%+ at month 12 = solid PMF
- Mobile apps: 5%+ at day-30 = strong (rare)

### 3. Organic growth

Pre-PMF, growth is paid (you're pushing). Post-PMF, growth is organic (users pull others in). Word-of-mouth, referral, search-driven traffic dominates.

### 4. The Andreessen "smell test"

> You can always feel when product/market fit isn't happening. The customers aren't quite getting value out of the product, word of mouth isn't spreading, usage isn't growing fast, press reviews are kind of "blah", the sales cycle takes too long, and lots of deals never close.
>
> And you can always feel product/market fit when it's happening. The customers are buying as fast as you can make it, money is piling up, you're hiring sales and customer support staff as fast as you can.

A team that has PMF *knows*. A team that asks "do we have PMF?" usually doesn't.

## What PMF is NOT

- ❌ Lots of signups (could be vanity acquisition)
- ❌ Positive press (press is decoupled from usage)
- ❌ Investor enthusiasm (investors fund pre-PMF too)
- ❌ Beta users saying nice things ([Mom Test](mom-test.md) violation)
- ❌ A working product (working ≠ wanted)

## Stages of PMF (Rachleff / Andreessen lineage)

```
Stage 1: Idea            ── you have a thesis
Stage 2: Prototype       ── you've built something
Stage 3: Initial users   ── some users use it
Stage 4: Pre-PMF growth  ── usage grows, but not exponentially
Stage 5: PMF             ── exponential pull from users
Stage 6: Scale           ── now it's an execution problem
```

Most "scaling" failures are actually pre-PMF startups attempting to scale prematurely. The fix is to keep iterating on the product/market until PMF appears, *then* scale.

## Achieving PMF

### Path 1: Iterate the product (most common)
Same market, change product. Keep the segment, refine the value prop, sharpen the offering. Standard [Lean Startup](lean-startup.md) play.

### Path 2: Pivot the market
Same product, change segment. Sometimes the product is fine but you're selling to the wrong people. Common SaaS pattern.

### Path 3: Pivot both
Recognize the entire premise was wrong. Drastic; usually team change too.

## The "Single Most Important Metric" question

When testing PMF, every team should be able to answer:

> What's the *one* metric that, if it improves, indicates we're approaching PMF?

For a B2B SaaS: Day-30 retention.
For a consumer social app: DAU/MAU + day-1 retention.
For a marketplace: GMV per active user, both sides.

If you can't pick one, you don't have a clear PMF hypothesis to test.

## Common PMF anti-patterns

### 1. Vanity acquisition
1M signups, 5% retention. Looks like PMF; isn't. Cohort analysis exposes it.

### 2. PMF for one segment, scale to wrong segment
Achieve PMF with prosumers; raise money; scale to enterprise; lose PMF (different needs). Common SaaS pattern.

### 3. Feature creep masking PMF loss
PMF erodes; team adds features hoping to recover. Each new feature dilutes the original value prop further.

### 4. Pseudo-PMF
A few extremely active users mask a long tail of churn. Average looks ok; deeper analysis shows you have product/segment-of-1 fit.

### 5. PMF treated as binary endpoint
PMF can be **lost**. A pivot, market shift, or feature creep can erode it. Mature teams continuously re-validate.

## See also

- [Lean Startup](concepts/lean-startup.md) — the iteration framework toward PMF
- [Customer Development](concepts/customer-development.md) — Blank's structured PMF process
- [Cohort analysis](concepts/cohort-analysis.md) — the mathematical signal
- [Aha moment / Activation](concepts/aha-moment.md) — leading indicator of retention → PMF
- [Innovation Accounting](concepts/innovation-accounting.md) — how to measure progress toward PMF
- [North Star Framework](concepts/north-star.md) — the post-PMF scaling metric
