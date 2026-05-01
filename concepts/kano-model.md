# Kano Model

> Source: Noriaki Kano, 1984. Categorizes features by how they affect customer satisfaction.

## The five categories

```
SATISFACTION
       ↑
       │           Excitement (delighters)
       │              ↗ unexpected, asymptotic
       │            ↗
       │          ↗     Performance (linear)
       │        ↗      ↗  more is better
       │      ↗      ↗
   ────┼────●──────●──────────────→ FUNCTIONALITY
       │             ↘            (level provided)
       │              ↘
       │               Basic (must-haves)
       │                  ↘ presence: 0 satisfaction
       │                     absence: huge dissatisfaction
       │
   DISSATISFACTION
```

| Category | Behavior | Example |
|---|---|---|
| **Basic / Must-have** | Absence = anger; presence = no credit | "App opens when I tap it" |
| **Performance / Linear** | More is proportionally better | Battery life, speed, storage |
| **Excitement / Delighter** | Unexpected; absence not missed; presence delights | First face unlock, AirDrop |
| **Indifferent** | Users don't care either way | Internal architecture, brand of toothpaste cap |
| **Reverse** | More is *worse* for some users | Notification frequency, marketing emails |

## How features migrate

A delighter today is a basic in 5 years. The model is *time-dependent*:

```
2010: front-facing camera = excitement (iPhone 4)
2015: front-facing camera = performance (megapixels matter)
2020: front-facing camera = basic (absence is failure)
```

Implication: investing in current-day delighters is a treadmill. Yesterday's wow becomes today's table stakes.

## How to apply

Survey users with a paired question for each candidate feature:

| Question | Possible answers |
|---|---|
| *Functional:* How would you feel if the product had X? | Like / Expect / Neutral / Tolerate / Dislike |
| *Dysfunctional:* How would you feel if it didn't have X? | Like / Expect / Neutral / Tolerate / Dislike |

The pair maps to a category via the Kano table.

## Strategy implications

| Category | Investment strategy |
|---|---|
| Basic | Must do; no competitive advantage from doing well, huge cost from doing badly |
| Performance | Compete on these; track competitors' levels |
| Excitement | Differentiate here; high-leverage if novel |
| Indifferent | Stop doing these |
| Reverse | Make optional or remove |

## Why it's useful

- Forces categorization of features by *type* of value, not raw priority
- Distinguishes "table stakes" from "differentiator" — different investment logic
- Surfaces "delight" as a deliberate design move, not luck

## Critiques

- **Survey-based** — relies on stated preference, which lies
- **Static snapshot** — doesn't capture migration over time without re-running
- **Hard to action** — categorization doesn't tell you *what* delighter to invest in
- **Cultural variance** — what delights varies by segment

## When to use

- Mature product with feature set to triage
- Competitive analysis (which features are basics vs differentiators in this market?)
- Onboarding redesigns (what are the must-haves the user can't navigate without?)

## When not to use

- Early product with no feature set yet (use [JTBD](jobs-to-be-done.md))
- Net-new categories (no comparable products to survey against)

## See also

- [RICE / ICE](rice-ice.md) — alternative prioritization (numeric, not categorical)
- [Jobs To Be Done](jobs-to-be-done.md) — focuses on jobs, not features
- [Outcomes vs outputs](outcomes-vs-outputs.md) — Kano is feature-shaped; pair with outcome thinking
