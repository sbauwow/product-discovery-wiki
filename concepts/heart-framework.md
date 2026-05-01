# HEART Framework

> Source: Kerry Rodden et al., Google UX Research (2010 paper). UX-specific metric system, complement to product/business metrics.

## Five dimensions

| Letter | Dimension | What it measures |
|---|---|---|
| **H** | **Happiness** | Subjective satisfaction (NPS, CSAT, ratings, sentiment) |
| **E** | **Engagement** | Depth and frequency of use |
| **A** | **Adoption** | New users / new feature uptake |
| **R** | **Retention** | Existing users still using over time |
| **T** | **Task success** | Can users complete their tasks? (efficiency, error rate, completion %) |

## Goals / Signals / Metrics matrix

For each HEART dimension, define:

| Step | Question | Output |
|---|---|---|
| **Goal** | What does success look like for this dimension? | Plain-English statement |
| **Signal** | What user behavior would indicate that goal is met? | Observable behavior |
| **Metric** | How do we count it? | Specific tracked metric |

### Worked example: search feature

| Dimension | Goal | Signal | Metric |
|---|---|---|---|
| Happiness | Users feel search works | Positive sentiment | CSAT after search session |
| Engagement | Users search regularly | Frequent searches | Searches per active user / week |
| Adoption | New users find search | First-week search use | % new users who search in week 1 |
| Retention | Search keeps users | Repeat usage | % users who searched last month, returned this month |
| Task success | Users find what they want | Click on result | Click-through rate, query reformulation rate |

## When to use HEART

- Designing UX for a specific feature or product area
- Setting OKRs for a UX-focused team
- Justifying UX investment with metrics

## When NOT to use it

- As a top-level company strategy framework (use [North Star](north-star.md) for that)
- For non-UX work (infrastructure, B2B sales motion, etc.)
- When you only need 1–2 metrics — HEART encourages 5+, which can over-instrument

## HEART vs North Star

| HEART | North Star |
|---|---|
| 5 dimensions | 1 metric |
| Feature/product-area scoped | Company-wide |
| UX-specific | Business + user value |
| Tactical instrumentation | Strategic anchor |

They complement. North Star sets the top-level outcome. HEART instruments specific UX surfaces under it.

## Common pitfalls

- **All five filled in mechanically** — sometimes a feature genuinely doesn't have a meaningful happiness or retention dimension; don't force it
- **Signal ≠ metric** — teams skip "signal" and jump to numbers. Defining the signal *before* the metric prevents tracking the wrong thing.
- **No baseline** — H/E/A/R/T metrics need cohort baselines to be meaningful

## See also

- [North Star Framework](north-star.md) — strategic-level metric
- [Outcomes vs outputs](outcomes-vs-outputs.md) — HEART metrics are outcomes
