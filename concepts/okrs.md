# OKRs (Done Right)

> Sources: Andy Grove (Intel, 1970s), John Doerr (*Measure What Matters*, 2018), popularized by Google. Most-used, most-misused goal framework.

## The structure

```
OBJECTIVE — qualitative, inspirational, time-bound
"Become the fastest way to publish a podcast"

  KEY RESULT 1 — quantitative, measurable, ambitious
  "Reduce upload-to-published time from 12 min to 2 min"

  KEY RESULT 2
  "Increase % of new shows that publish in week 1 from 40% to 65%"

  KEY RESULT 3
  "Achieve NPS ≥ 50 among new podcasters"
```

Rule: 1 objective, 3–5 key results, per team per quarter.

## What's hard about OKRs

The framework looks simple. Almost every org gets it wrong. The errors are predictable:

### Error 1: Output-shaped key results

❌ KR: "Ship redesigned editor"
❌ KR: "Launch v2 of the API"
❌ KR: "Complete migration to React 19"

These are *outputs* — see [outcomes vs outputs](outcomes-vs-outputs.md). You can hit them and the business can fail.

✅ KR: "Reduce edit-to-publish friction (measured by drop-off rate from edit start → publish complete) from 35% → 15%"

### Error 2: Sandbagged KRs

KRs the team is 95% sure to hit are useless. OKRs require **stretch** — Google's classic guideline:

> If you hit 70% of KRs, you're doing well.
> If you hit 100%, you sandbagged.

Hitting all KRs every quarter = the goals weren't ambitious. (This implies separating *committed* goals from *aspirational* goals — Google does both, with separate hit-rate expectations.)

### Error 3: Cascading mandate

Top-down OKR cascade ("CEO's OKRs become VPs', become directors', become teams'") turns OKRs into a Gantt chart. Teams get assigned KRs they didn't help shape.

Better: top-down on *objectives* (strategic direction), bottom-up on *key results* (how the team will move them).

### Error 4: KRs as task lists

❌ KR: "Conduct 5 user interviews"
❌ KR: "Run 3 A/B tests"

Activity ≠ result. The interview/test is the *means*; the result is the *change* it produced.

### Error 5: Too many

❌ 8 objectives, 30 KRs.

OKRs are about **focus**. The point is what you *don't* do. 1–2 objectives forces choosing.

### Error 6: Quarterly only

Setting and forgetting. Real OKRs are reviewed weekly (lightweight check-in) and updated mid-quarter if context changes.

## Properly-shaped OKR (worked example)

Bad version:
> **O:** Improve onboarding
> **KR1:** Ship redesigned onboarding flow
> **KR2:** Add email verification
> **KR3:** Update help docs

Good version:
> **O:** New users reach value before they lose interest
> **KR1:** Increase 7-day activation 32% → 50%
> **KR2:** Reduce time-to-first-value from 12 min to 4 min
> **KR3:** Reduce signup-to-week-1-active drop-off 60% → 35%

The good version: every KR is a behavior change. The team can pick *any* solution to move them.

## Connection to discovery

OKRs sit above the [Opportunity Solution Tree](opportunity-solution-tree.md):

```
   Company OKRs (strategy, 1 quarter)
         ↓
   Team OKRs (1 objective, 3 KRs)
         ↓
   OST per KR (outcome at the root)
         ↓
   Opportunities → Solutions → Experiments
```

The KR is the OST root. Without that connection, OKRs and discovery operate in separate universes.

## OKRs vs KPIs

| OKR | KPI |
|---|---|
| Goal (where you want to go) | Health metric (where you currently are) |
| Quarterly, time-bound | Continuous |
| Stretches the system | Monitors the system |
| Few, focused | Many, comprehensive |

Don't make every KPI an OKR. Pick the few you're trying to *change*.

## When OKRs don't fit

- **Steady-state operations** — running production at 99.9% uptime is a KPI, not an OKR (no stretch dimension)
- **Hard-deadline mandates** — "GDPR compliance by Q2" is a project, not an OKR (no real flexibility)
- **Pure exploration** — early-stage research where outcomes can't be predicted

## See also

- [Outcomes vs outputs](outcomes-vs-outputs.md) — the most common OKR failure mode
- [North Star Framework](north-star.md) — sits above OKRs, anchoring quarterly bets
- [Opportunity Solution Tree](opportunity-solution-tree.md) — discovery downstream of KRs
