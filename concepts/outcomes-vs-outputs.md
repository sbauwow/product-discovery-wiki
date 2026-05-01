# Outcomes vs Outputs

> The single most-violated principle in product. Internalize this and most other discovery practices follow.

## Definitions

- **Output** — something we produce. A feature shipped, a redesign deployed, a model trained.
- **Outcome** — a change in user or business behavior. A retention bump, a conversion lift, a support-ticket drop.
- **Impact** — long-term, downstream consequences. Revenue, market share, lifetime value.

```
Effort  →  Output  →  Outcome  →  Impact
(work)    (thing)    (change)    (consequence)
```

Most teams measure effort and output. Mature teams measure outcome.

## Why teams default to outputs

Outputs are:
- ✅ Easy to count (tickets closed, features shipped)
- ✅ Visible to executives ("we shipped X")
- ✅ Plannable on a Gantt chart
- ✅ Predictable in timeline

Outcomes are:
- ❌ Lagging (might take weeks/months to register)
- ❌ Multi-causal (was it our feature, or the season, or competitor's outage?)
- ❌ Sometimes flat or negative even after good work
- ❌ Embarrassing when missed

So orgs drift to output measurement out of legibility, not utility.

## The cost of output thinking

Output goals are uncorrelated with success:
- Ship the redesign on time → users hate it
- Ship 14 features in Q2 → none move the metric
- Hit roadmap commitments 100% → company misses revenue

Output completion ≠ value. The roadmap is theater if no outcome is named.

## Outcome-shaped goals

✅ "Increase week-1 retention 30% → 45%"
✅ "Reduce time-to-first-value from 8 min to 2 min"
✅ "Increase free-to-paid conversion 4% → 7%"
✅ "Reduce p50 support response time 4h → 1h"

Each is **measurable**, **bounded**, and a **change in behavior** (not a thing produced).

## Output-shaped goals (what to avoid)

❌ "Ship the new dashboard in Q2"
❌ "Launch v2 of the API"
❌ "Migrate to React 19"
❌ "Complete onboarding redesign"

These describe work, not effect. Worse: a team can hit them and the business can fail.

## When outputs are okay

Some work is genuinely output-shaped:
- **Compliance** — "GDPR-compliant by deadline X" is an output, but mandated by law
- **Platform/infrastructure** — "migrate to Postgres 16" — outcome ("reduce ops cost") may be too lagging
- **Foundational work** — design system, API layer

Even here, *name the outcome*. "Migrate to Postgres 16 to reduce on-call paging by 40%". The output is real, but the outcome anchors why.

## The Marty Cagan litmus test

> Ask: "If we ship this and the outcome doesn't move, is it still a success?"
>
> If yes → you have an output goal. Reframe.
> If no → it's an outcome goal.

## OKRs and the outcome trap

OKRs (Objectives and Key Results) are *supposed* to enforce outcomes. They usually don't.

Bad OKR:
- **Objective:** Improve onboarding
- **Key Result:** Ship redesigned onboarding flow ← *output*

Good OKR:
- **Objective:** Get new users to value faster
- **Key Result:** Increase 7-day activation 35% → 50% ← *outcome*

The KR test: can you check the box without changing user behavior? If yes, it's an output.

## Connection to discovery

- The [North Star](north-star.md) is an outcome.
- The root of an [Opportunity Solution Tree](opportunity-solution-tree.md) is an outcome.
- An [empowered team](empowered-team.md) is given outcomes, not features.
- A [feature factory](feature-factory.md) is a team that gets given outputs.

Every other concept in this wiki collapses if outcomes aren't real.

## See also

- [North Star Framework](north-star.md)
- [Empowered team](empowered-team.md)
- [Roadmap trap](roadmap-trap.md) — output-shaped roadmaps as a top failure mode
- [Feature factory](feature-factory.md)
