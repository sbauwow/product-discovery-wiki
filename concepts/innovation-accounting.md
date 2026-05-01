# Innovation Accounting

> Source: Eric Ries, *The Lean Startup* (2011). The accounting system for startups (or new bets inside companies) that measures **learning**, not just shipping.

## The problem it solves

Standard accounting (revenue, profit, growth) is built for businesses with known business models. Applied prematurely to startups, it produces nonsense:
- Pre-revenue startup looks like a money-loser
- Vanity-driven growth looks like progress
- Pivots look like failures
- Validated learning looks like nothing

Innovation accounting reframes "progress" as **rate of validated learning**, with metrics that pre-revenue and early-stage teams can actually move.

## The three levels

Ries proposes three escalating tiers:

### Level 1: Vanity metrics
Total signups, pageviews, downloads. Always grow. Tell you nothing. See [vanity metrics](vanity-metrics.md).

❌ Don't use as a metric of progress.

### Level 2: Actionable metrics
Per-cohort, rate-based, segment-specific. Conversion, retention, activation per cohort.

✅ Use these for daily/weekly product decisions.

### Level 3: Innovation accounting
A causal model: "If we make change X, metric Y will move by Z." Each release tests a hypothesis. Track:
- Hypothesis → result
- Validated learning per cycle
- Decision: pivot or persevere

✅ Use for strategic decisions (whether the model is working).

## The startup as math

Ries's framing: a startup is a **machine that converts ideas into validated learning** at some rate. Innovation accounting measures the rate.

```
Velocity of learning = (validated experiments) / (time + cost)
```

A startup that ran 10 experiments in Q1, validated 4 hypotheses, killed 6 → high velocity, even if revenue is zero.
A startup that shipped 12 features in Q1 with no measurement → low velocity, even if shipping volume is high.

## The three milestones

Ries proposes a 3-stage model:

### 1. Establish baseline
Build the simplest [MVP](lean-startup.md) that produces measurable behavior. Get real numbers from real users.

Example: signup → activation → retention rate, baselined at 100 → 30 → 12.

### 2. Tune the engine
Iterate. Each release should improve the actionable metrics. Track *delta* per release.

Example: redesign onboarding → activation 30 → 38. Validated.
Example: pricing change → conversion flat. No effect; revert or learn from it.

### 3. Pivot or persevere
After enough cycles, ask: are the metrics moving toward a viable business?
- **Yes** → persevere; the engine works, scale it
- **No** → pivot; the model needs a substantive change

The key: innovation accounting *forces the pivot decision* with data, not vibes.

## Worked example

```
Cycle 1 baseline:
  Signups/week: 100
  Activation rate: 12%
  Day-30 retention: 8%
  
Hypothesis 1: "Adding sample data on signup will improve activation."
  Action: ship sample data feature
  Result: activation 12% → 14%
  Verdict: Persevere. Marginal but positive.

Hypothesis 2: "Onboarding tour will improve activation further."
  Action: ship tour
  Result: activation 14% → 13%, retention dropped
  Verdict: Tour annoyed users. Kill.

Hypothesis 3: "Switching from individual to team-first onboarding will compound activation + retention."
  Action: rebuild onboarding flow for teams
  Result: activation 14% → 35%, retention 8% → 22%
  Verdict: PIVOT. Team-first is the model. Refactor product around it.
```

The pivot in cycle 3 isn't a failure — it's the most valuable cycle.

## Learning per dollar

A useful framing: how much *learning* did a dollar of spend produce?
- $50k on a 6-month engineering build → did it test a critical assumption?
- $5k on a fake-door test → did it kill or validate the idea before the build?

Innovation accounting prefers cheap experiments because the **denominator (cost)** matters as much as the numerator (learning).

## Why orgs reject it

Innovation accounting is unpopular for the same reason [outcomes](outcomes-vs-outputs.md) are unpopular:
- It exposes failed assumptions (uncomfortable)
- It can't be reported as "shipped X features" (illegible to standard execs)
- It punishes vanity metrics that look good (some incumbents like vanity)
- It requires real measurement infrastructure (orgs underinvest)

Most orgs talk about it; few practice it.

## When it's most useful

- **New ventures** — pre-PMF, zero revenue, need a way to measure progress
- **Internal innovation labs** — corporate ventures need a different KPI than the parent org
- **Pivot decisions** — quantitative basis for the hardest call a startup makes
- **Investor reporting** — sophisticated investors increasingly accept innovation-accounting reports for early-stage portfolio companies

## When it's less useful

- **Mature, scaled products** — actionable metrics suffice; full innovation-accounting overhead unnecessary
- **Single-quarter decisions** — too short for the full pivot/persevere cycle

## See also

- [Lean Startup](concepts/lean-startup.md) — the parent framework
- [Outcomes vs outputs](concepts/outcomes-vs-outputs.md) — innovation accounting *is* outcome accounting for startups
- [Vanity metrics](concepts/vanity-metrics.md) — Level 1 in the hierarchy
- [Cohort analysis](concepts/cohort-analysis.md) — Level 2 in the hierarchy
- [PMF](concepts/pmf.md) — innovation accounting tells you when you've reached PMF
