# Pirate Metrics (AARRR)

> Source: Dave McClure (500 Startups), 2007. Five-stage funnel for SaaS / consumer products. Acronym pronounced "AARRR" (pirate noise).

## The funnel

```
ACQUISITION  →  ACTIVATION  →  RETENTION  →  REVENUE  →  REFERRAL
   │              │                │             │            │
   visit          first             come          pay          tell
   sign up        success           back                       others
```

| Stage | Question | Example metric |
|---|---|---|
| **Acquisition** | Where do users come from? | Visitors, signups, channel CAC |
| **Activation** | Do they have a great first experience? | % completing onboarding, time-to-first-value |
| **Retention** | Do they come back? | Day 1/7/30 retention, weekly active rate |
| **Revenue** | Do they pay? | Conversion rate, LTV, MRR |
| **Referral** | Do they bring others? | Viral coefficient (k), NPS, referrals/user |

## Why this order matters

McClure's insight: most startups optimize **acquisition first** (ads, SEO, growth hacks). Wrong order. Acquisition into a bucket with holes (poor activation, retention) just wastes spend.

```
Right priority order:
  1. Activation works → users get value → retention possible
  2. Retention works → cohorts stick → revenue/referral compound
  3. Revenue works → LTV > CAC → acquisition becomes profitable
  4. Referral works → growth becomes self-sustaining
  5. Acquisition: now you know what to scale

Wrong order (most startups):
  1. Acquisition first → fills bucket
  2. Bucket has holes → CAC > LTV → die
```

Fix retention before pouring acquisition money in. Common mantra: "Retention is the only metric that matters."

## The funnel chart

```
       100 visitors
       ────────────────  Acquisition: 10% sign up
                ↓
        10 signups
        ──────────       Activation: 40% reach value
                ↓
         4 activated
         ──────         Retention: 50% return week 2
                ↓
          2 retained
          ──             Revenue: 50% convert paid
                ↓
           1 paying
                          Referral: 30% refer 1 user
                ↓
           0.3 referrals
```

End-to-end: 100 visitors → ~1 paid → 0.3 referrals. Each stage's % is a lever.

## Improving each stage

### Acquisition
- Channel mix (paid, organic, content, partnerships)
- Landing page conversion
- Ad creative / SEO

### Activation
- Onboarding flow
- Time-to-first-value ([aha moment](aha-moment.md))
- Empty-state design

### Retention
- Habit loops ([Hooked](hooked.md))
- Re-engagement (email, push)
- Core loop frequency

### Revenue
- Pricing model
- Conversion CTAs
- Free-to-paid trigger

### Referral
- In-product sharing
- Incentive structure (refer-and-get)
- NPS-driven word-of-mouth

## Variants

- **AAARRR** — adds **Awareness** at the top (people knowing you exist)
- **HEART** ([Google's](heart-framework.md)) — UX-focused, partial overlap
- **RARRA** — Reichheld/some advocates argue *Retention* should be first stage talked about, since it gates everything

## Common mistakes

- **Vanity at top of funnel** — 1M visits, 0.01% activation = useless. See [vanity metrics](vanity-metrics.md).
- **No cohort analysis** — averaging across all users hides retention curves. See [cohort analysis](cohort-analysis.md).
- **Optimizing wrong stage first** — see ordering above
- **Same funnel for every segment** — power users and casual users have different funnels; aggregate hides the difference

## When AARRR fits

✅ Consumer / SaaS products with linear user lifecycle
✅ B2B SaaS (with adapted definitions)
✅ Marketplaces (per side: buyers & sellers each have an AARRR)

## When it doesn't fit

❌ Enterprise sales (long, multi-stakeholder, no "activation" moment)
❌ Hardware (different lifecycle entirely)
❌ Internal tools (no "revenue" stage)

## See also

- [North Star Framework](north-star.md) — North Star usually comes from Activation or Retention stage
- [Aha moment / Activation](aha-moment.md) — the most important stage for most products
- [Cohort analysis](cohort-analysis.md) — how to measure retention honestly
- [Vanity metrics](vanity-metrics.md) — what to avoid
