# Cohort Analysis

> The single most-honest way to measure product health. Aggregate metrics lie; cohorts tell the truth.

## The mechanic

A **cohort** is a group of users who share an entry point in time. Track each cohort's behavior *separately* over their lifetime.

```
            Week 1    Week 2    Week 3    Week 4    Week 5
Jan cohort  100%      45%       30%       25%       22%
Feb cohort  100%      50%       38%       33%       30%
Mar cohort  100%      52%       42%       37%
Apr cohort  100%      55%       46%
May cohort  100%      60%
```

Read across rows: this cohort's retention over time.
Read down columns: how the same week-N retention has changed across cohorts.

If columns trend up = product is improving. If flat = stagnant. If down = degrading.

## Why aggregates lie

Plot total weekly active users (WAU):

```
WAU
  │           ╱╲╱╲╱╲╱╲╱╲   ← line goes up!
  │       ╱╲╱╲
  │   ╱╲╱
  │╲╱
  └─────────────────────→ time
```

Looks great. But this could be:
- **Healthy:** retention solid, acquisition adding more
- **Leaky bucket:** retention bad, acquisition outpacing churn
- **Mix shifting:** old users dying, new users growing

You can't tell from WAU alone. Cohorts disambiguate.

## Retention curves

Three shapes that matter:

### 1. Smile curve (great)
```
Retention
  100% │●
       │ \
   60% │  \
       │   ●─────────●─────●  ← stabilizes, then grows
   40% │    \       /
       │     ●─────●
       └───────────────────→ time
```
Some users churn, but the ones who stay come back more frequently. Product is sticky for the right users.

### 2. Flat curve (good)
```
Retention
  100% │●
       │ \
   60% │  ●──────●──────●  ← levels off
       │
       └───────────────────→ time
```
Power product. SaaS gold standard. ~50% retention at month 3+ is excellent for most categories.

### 3. Frown curve (bad)
```
Retention
  100% │●
       │ \
       │  ●
       │   \
       │    ●
       │     ●─────●─────●  ← keeps decaying toward zero
       └───────────────────→ time
```
Leaky bucket. Acquisition can mask this for a while. Eventually CAC > LTV.

## Reference benchmarks

Ballpark month-12 retention:

| Category | Healthy | Stretch | Best in class |
|---|---|---|---|
| Consumer social | 25% | 40% | 60%+ (Facebook, IG) |
| Consumer paid | 20% | 35% | 50%+ (Spotify, Netflix) |
| B2B SaaS | 80% | 90% | 95%+ (Slack, Figma) |
| Marketplace | 30% | 50% | 70%+ (Airbnb hosts) |
| Mobile games | 5% | 15% | 30%+ (top 1%) |

Numbers vary widely by definition (DAU? WAU? MAU? "Active" how?). Define rigorously.

## Cohort dimensions

Beyond signup-week cohorts:

| Cohort by | What it reveals |
|---|---|
| **Signup date** | Default; tracks product changes over time |
| **Acquisition channel** | Which channels bring sticky users |
| **Geography** | Localization, cultural fit |
| **Onboarding path** | Which onboarding completes drive retention |
| **First action** | The "[aha moment](aha-moment.md)" predictive of retention |
| **Plan tier** | How feature access affects retention |

Most-useful single insight: cohort by **first-week behavior**. Find the action correlated with month-3 retention. That's your activation event.

## How to read a cohort table

Things to look for:

1. **Day-1 drop**: massive churn in the first 24h = onboarding broken
2. **Week-2 cliff**: users churn after their first "complete cycle" = product didn't deliver promised value
3. **Stable floor**: retention asymptotes to X% = your true product-market fit segment
4. **Improving cohorts**: each new cohort retains better at week-N than prior = product is improving
5. **Degrading cohorts**: opposite. Investigate.

## Tools

- **Mixpanel / Amplitude** — built-in cohort views
- **Heap / PostHog** — same, more raw data
- **SQL** — for serious analysis, write your own. Foundational query is `GROUP BY cohort_week, periods_since_signup`.
- **Google Analytics** — has cohorts but limited

## Common failure modes

- **Average retention** — meaningless without cohort decomposition
- **No segmentation** — aggregating power users with casual users hides the truth
- **Short window** — measuring week-1 retention is fine, but the *shape of the curve* needs months of data
- **Survivorship bias in interviews** — interviewing only retained users; talk to churned ones too
- **Defining "active" badly** — "logged in" ≠ active. Pick a behavioral metric that means value delivered.

## See also

- [Pirate Metrics](pirate-metrics.md) — retention is stage 3 of AARRR
- [Aha moment / Activation](aha-moment.md) — the metric that predicts cohort retention
- [Vanity metrics](vanity-metrics.md) — aggregate metrics that look good but hide bad cohorts
- [North Star Framework](north-star.md) — North Star metric should reflect cohort health
