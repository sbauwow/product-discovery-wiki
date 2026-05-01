# Lean Startup

> Source: Eric Ries, *The Lean Startup* (2011). Roots in Steve Blank's customer development and Toyota lean manufacturing.

## Core loop

```
        ┌──────────┐
        │  IDEAS   │
        └────┬─────┘
             │ build
             ▼
        ┌──────────┐
        │ PRODUCT  │ ──┐
        └──────────┘   │ measure
                       ▼
                  ┌─────────┐
                  │  DATA   │
                  └────┬────┘
                       │ learn
                       ▼
                  ┌─────────┐
                  │  IDEAS  │
                  └─────────┘
```

Build → Measure → Learn. **Minimize total time through the loop.** That's the only optimization target.

## Key concepts

### MVP (Minimum Viable Product)

> The smallest thing you can build that lets you start the learning loop.

NOT "version 1 with fewer features". An MVP is defined by the *riskiest assumption* you're testing, not by feature scope. If the riskiest assumption is "do users want this at all?", a landing page with a signup form is an MVP. No code required.

Common MVP types:
- **Landing page MVP** — describe the product, measure signups
- **Concierge MVP** — deliver the service manually before automating
- **Wizard of Oz MVP** — fake the backend with humans
- **Single-feature MVP** — one feature, real users, narrow audience

### Validated learning

The output of the loop. Not "we shipped X". Rather: "we learned Y about user behavior, with N users, over T time, and the data was Z."

A feature shipped without learning is waste.

### Pivot or persevere

After each loop iteration, decide:
- **Persevere** — keep going, the hypothesis is holding
- **Pivot** — change one core element of the strategy while keeping others

Pivot types (Ries lists ~10):
- **Zoom-in** — a single feature becomes the whole product
- **Zoom-out** — the whole product becomes one feature of a bigger one
- **Customer segment** — same product, different buyer
- **Customer need** — same buyer, different need
- **Platform** — app → platform, or vice versa
- **Engine of growth** — viral → paid → sticky

## Engines of growth

Three self-reinforcing growth loops:

1. **Sticky** — high retention, low churn (compounds via cohort retention)
2. **Viral** — each user brings >1 new user (compounds via viral coefficient k)
3. **Paid** — LTV > CAC, reinvest profit into acquisition

A startup picks one and optimizes it. Trying all three diffuses focus.

## Innovation accounting

Three levels of metrics:
1. **Vanity metrics** — total signups, page views (always go up, don't tell you anything)
2. **Actionable metrics** — cohort retention, conversion rates (causally linked to actions)
3. **Innovation accounting** — track learning, not just numbers

## Where it fits

Lean Startup is upstream of [continuous discovery](continuous-discovery.md). It's the philosophical move ("we are running experiments, not executing plans"). Continuous discovery is the *operationalized* version with weekly cadence and the [opportunity tree](opportunity-solution-tree.md) as artifact.

## Critiques

- **Over-rotation on MVPs** — some products (medical, infrastructure, brand-led) can't ship a half-baked MVP. Apple didn't lean-startup the iPhone.
- **Local optima** — A/B test culture optimizes the current product, doesn't find the next one
- **Vague pivots** — "we pivoted" became a fig leaf for "we changed direction without learning anything"

Ries's later book *The Startup Way* attempts to address these in enterprise contexts.

## See also

- [Assumption mapping](assumption-mapping.md) — picking what to test
- [Prototyping](prototyping.md) — MVP types in detail
- [North Star Framework](north-star.md) — actionable metrics at scale
