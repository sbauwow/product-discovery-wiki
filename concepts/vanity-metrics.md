# Vanity Metrics

> Source: Eric Ries, *The Lean Startup*. Numbers that look impressive, always grow, but don't tell you whether the product is working.

## Examples

| Vanity | Why it's vanity | Better metric |
|---|---|---|
| Total signups | Always grows; doesn't show retention | Cohort retention curves |
| Pageviews | Doesn't separate engagement from accidents | Pages per active session |
| Total downloads | Grows even if app is uninstalled | Day-30 retention |
| Followers | Doesn't reflect engagement | Engaged followers (recent activity) |
| Total revenue (alone) | Grows from customer count alone | Revenue per cohort, LTV |
| Total transactions | Inflates with new user acquisition | Repeat-purchase rate |
| App rank in store | Volatile, gameable | Cohort retention from store traffic |
| Email opens | Gameable by image-load tricks | Click-through, post-click conversion |
| GitHub stars | Doesn't reflect usage | Active contributors / weekly active forks |
| Demo requests | Says nothing about close rate | Demo → close conversion |

## The Ries definition

A metric is vanity if:
1. It always goes up (cumulative, not rate-based)
2. It's not actionable (you can't do something specific to move it)
3. It doesn't reflect cause and effect (correlated with success but doesn't measure it)

## Why teams use them

- **They look good in board decks** — "we hit 1M signups!"
- **They're easy to measure** — counters, no segmentation needed
- **They reward over time** — every quarter is "the best quarter ever"
- **They avoid hard truths** — actionable metrics often look bad

CEOs and growth teams reach for vanity because they're flattering. The cost is delayed: the org optimizes the wrong thing for years before reality intrudes.

## Actionable metric counterparts

| Vanity | Actionable |
|---|---|
| Cumulative count | Per-period rate (weekly, monthly) |
| Aggregate average | Cohort breakdown |
| Total | Per-user / per-cohort |
| Up-only | Bidirectional (can go down) |
| Single number | Distribution / segment |

## The "always-up" tell

If the metric can only go up, it's vanity. Real product health metrics can go down — that's what makes them informative.

```
Vanity: total signups (cumulative)
        ↗↗↗↗↗↗↗↗ (always up)

Actionable: weekly new signups (rate)
        ↗↘↗↘↗↘↗↘ (varies, tells you something)

Actionable: 30-day retention (per cohort)
        ↗↘↗↗↘↗↘↘ (can degrade — that's a signal)
```

## The board-deck problem

Many orgs are *forced* to report vanity metrics to investors / board. This is OK as long as:

1. Internal team metrics are different (and actionable)
2. Vanity is reported alongside cohort/segment data
3. Leadership knows the difference

Trouble starts when vanity is the *only* metric the org tracks, internally and externally. Then the org becomes the metric.

## A worked replacement

Bad dashboard:
```
Total users:        1.2M    (↑12% MoM)
Total revenue:      $4.5M   (↑8% MoM)
Total downloads:    3.8M    (↑15% MoM)
```

Looks great. Tells you nothing.

Good dashboard:
```
WAU/MAU stickiness:    42%     (target: 50%)
30-day retention:      32%     (degraded from 38% in Jan; investigate)
Activation rate:       54%     (target: 70%)
LTV:CAC:               2.8:1   (target: 3:1)
NPS:                   34      (segment: power users 58, casual 12)
```

Tells you what's working and where to look.

## Common pitfalls

- **Mixing vanity and actionable** in the same review without separation — vanity dominates attention
- **Tracking only top-line metrics** — no segment breakdown
- **Celebrating cumulative milestones** ("1M users!") more than cohort improvements
- **Optimizing what you measure** — if vanity is what's tracked, that's what gets optimized

## When "vanity" metrics are useful

Cumulative metrics aren't *useless*:
- Marketing for credibility ("trusted by 1M users")
- Threshold milestones for funding ("reached 100k MAU")
- Product-market fit signals (early-stage growth)

The error is treating them as *health indicators*, not as headline summaries.

## See also

- [Lean Startup](lean-startup.md) — origin of the term
- [North Star Framework](north-star.md) — properly chosen, an actionable metric
- [Cohort analysis](cohort-analysis.md) — the antidote to most vanity
- [Pirate Metrics](pirate-metrics.md) — funnel that breaks down vanity into actionable stages
