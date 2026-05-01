# Funnel Analysis

> An analytical method for finding where users drop off in a multi-step process. Distinct from the [Pirate Metrics (AARRR)](pirate-metrics.md) *framework* — funnel analysis is the *method* for measuring any defined sequence of steps.

## The mechanic

```
Define a sequence of steps (the funnel).
For a cohort of users entering step 1, count:
  - how many reach step 2
  - how many reach step 3
  - ...
Calculate conversion rate at each step.
Identify the step with the largest drop-off.
Investigate why.
```

That's it conceptually. The discipline is in *how* you define steps and *which* drop-offs you investigate.

## Common funnels

### Activation funnel
```
Visit landing page → Sign up → Verify email → Complete profile → Reach aha moment
```

### Conversion funnel
```
Free user → Hit upgrade trigger → View pricing → Click upgrade → Enter payment → Confirm purchase
```

### Onboarding funnel
```
Sign up → Complete welcome screen → Connect data source → Create first project → Invite teammate
```

### Purchase funnel (e-commerce)
```
View product → Add to cart → Checkout → Enter shipping → Enter payment → Confirm order
```

### Sales funnel (B2B)
```
Lead → MQL → SQL → Demo scheduled → Demo completed → Proposal sent → Closed-won
```

Each funnel has its own steps and norms. The shape of healthy conversion varies wildly: e-commerce checkout might be 60-80%; B2B sales might be 5-15%.

## Reading a funnel

Two metrics per step:

| Metric | What it tells you |
|---|---|
| **Step conversion rate** | % who completed *this* step out of those who entered it |
| **Cumulative conversion rate** | % who reached this step from the *top* of the funnel |

Example funnel for an onboarding flow:

```
Step 1: Sign up                  10,000  (100%)
Step 2: Verify email              7,000  (70% step / 70% cumulative)  ← 30% drop
Step 3: Complete profile          5,500  (79% step / 55% cumulative)  ← 21% drop
Step 4: Connect data source       2,800  (51% step / 28% cumulative)  ← 49% drop ★
Step 5: Create first project      2,400  (86% step / 24% cumulative)  ← 14% drop
Step 6: Reach aha moment          2,100  (88% step / 21% cumulative)  ← 12% drop
```

Step 4 is the big leak. Half of users fail to connect a data source. *That* is where to invest design/research effort.

## Why this is more than AARRR

[AARRR](pirate-metrics.md) is a 5-stage *framework* covering the whole user lifecycle. Funnel analysis is the *method* applied to:
- A single AARRR stage (e.g. activation funnel inside the Activation stage)
- A specific user flow (checkout, onboarding, signup)
- A specific feature (upload → process → share)
- A sales motion (B2B funnel)

```
AARRR    →  Acquisition - Activation - Retention - Revenue - Referral
              │
              ▼
            Activation funnel    →  Step 1 - Step 2 - Step 3 - Step 4
              │
              ▼
            Step 3 funnel        →  Substep - Substep - Substep
```

Funnels nest. Each level reveals different drop-offs.

## What good funnel analysis surfaces

### 1. The biggest leak
The step with the largest drop-off is usually the highest-leverage place to invest. Fixing the worst step often outweighs improving every other step combined.

### 2. Segment differences
Different user segments funnel differently:
- New vs returning users
- Mobile vs web
- Acquired through ad X vs ad Y
- Free tier vs trial tier

A segmented funnel often reveals that the "average" funnel is the result of two very different funnels overlaid.

### 3. Unexpected paths
Users sometimes skip steps, repeat steps, or take parallel paths. A linear funnel hides this. **Sankey diagrams** complement funnels by showing flow between any two states.

### 4. Time decay
A user who reaches step 3 immediately is healthier than one who reaches it after 14 days. Time-windowed funnels matter (e.g. "% who reach aha within 7 days").

### 5. Cohort drift
Today's funnel might be 28% end-to-end; six months ago it was 35%. Something degraded. [Cohort analysis](cohort-analysis.md) of funnel performance over time surfaces drift.

## Common failure modes

### 1. Wrong funnel definition
If your steps don't match how users actually move, the funnel is fiction. Validate steps against real session recordings before measuring.

### 2. Too many steps
A 12-step funnel produces noise. Conversion compounds: 12 steps at 80% each = 7% end-to-end. Hard to read.

### 3. Too few steps
A 2-step funnel ("signup → paid") hides everything between. Aggregates the leak.

Sweet spot: 4-7 steps for most product funnels.

### 4. Aggregate without segments
Average funnel hides the truth. Always segment by at least one dimension (channel, user type, plan).

### 5. Static measurement
Measuring the funnel once is diagnostic. Measuring weekly is a system. Build a dashboard, watch trends.

### 6. Investigating the smallest leak
Don't fix the 5% leak when there's a 50% one. Prioritize.

### 7. Treating funnel as causal
"We added X and step 3 conversion went up." Maybe. Maybe seasonal. Maybe a different cohort. [A/B test](ab-testing.md) to confirm causation.

### 8. Ignoring the "did not enter" cohort
Funnels start at the first step. But some users might *never enter* the funnel. The funnel says nothing about them. Always pair with TAM (top-of-funnel) data.

## Tools

- **Mixpanel / Amplitude / PostHog / Heap** — built-in funnel analysis
- **Google Analytics** — basic funnels (limited flexibility)
- **Looker / Mode / Hex** — SQL-driven custom funnels
- **Pendo / FullStory** — product-flow with session-level visibility
- **Excel / Sheets** — for small funnels, often enough

## Worked example: PLG conversion funnel diagnosis

A SaaS startup wants to improve trial → paid conversion. Build the funnel:

```
Trial signup                100%
Activated (used core feature) 65%   ← 35% drop
Used core feature 3+ times  42%   ← 35% relative drop
Invited a teammate           18%   ← 57% drop ★
Hit pricing trigger          12%   ← 33% drop
Viewed pricing page          11%   ← 8% drop
Started checkout             6%    ← 45% drop ★
Completed payment            5%    ← 17% drop
```

Two large drops:
1. **Invited a teammate (57% drop)** — many users use solo; never collaborate
2. **Started checkout (45% drop)** — pricing page viewed but flow exits

Investigate each:
- Solo-only users might be a different segment than collaborative ones; segment funnel by team-size at signup
- Checkout flow: where exactly do users drop? sub-funnel into checkout steps

Each leak gets its own investigation. Can't fix what you don't measure.

## Funnel analysis in B2B

B2B funnels span weeks to months and involve multiple stakeholders. Adapt:

- **Time per stage** matters more than just conversion (long stages = stalls)
- **Account-level**, not user-level (one account = many users)
- **Multi-touch attribution** (which channel/content moved them between stages?)
- **Manual stages** (sales rep input data, not tracked automatically)

Tools: HubSpot, Salesforce, Marketo. Methodology same; data sources different.

## See also

- [Pirate Metrics (AARRR)](concepts/pirate-metrics.md) — the framework funnel analysis is most often applied to
- [Cohort analysis](concepts/cohort-analysis.md) — funnel-over-time for trend visibility
- [Aha moment / Activation](concepts/aha-moment.md) — the most important funnel step in most products
- [A/B testing](concepts/ab-testing.md) — what to do once you've identified a leaky step
- [Vanity metrics](concepts/vanity-metrics.md) — top-of-funnel without conversion data is vanity
- [PLG](concepts/product-led-growth.md) — PLG products live or die by their funnels
