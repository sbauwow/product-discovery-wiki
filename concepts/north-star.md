# North Star Framework

> Sources: Sean Ellis (coined "North Star Metric" at GrowthHackers), Amplitude (formalized into a framework, *The North Star Playbook*).

## The thesis

A single metric, chosen carefully, captures the value the product delivers to customers in a way that — if it grows — drives the business. Plus a set of **input metrics** that feed it. The North Star is the **outcome you anchor [OSTs](opportunity-solution-tree.md) to**.

## What makes a good North Star

| Property | Why |
|---|---|
| **Captures value to the customer** | Not "revenue" — that captures value to *us*. North Star tracks user value, which precedes revenue. |
| **Represents vision and strategy** | If it grows, you're winning at the thing you said you'd win at |
| **Leading indicator of revenue** | Moves before revenue does, gives time to act |
| **Actionable** | The team's daily work plausibly moves it |
| **Understandable** | Whole company can name it without checking a doc |
| **Not a vanity metric** | Excludes things that always go up (total signups) |

## Examples

| Company | North Star Metric |
|---|---|
| Spotify | Time spent listening |
| Airbnb | Nights booked |
| Slack | Messages sent in active teams |
| Facebook (early) | Daily active users with ≥7 friends in 10 days |
| Amazon | Number of purchases per Prime member |
| Quora | Questions answered |
| Zoom | Weekly hosted meetings |

Pattern: usually a verb + measurable unit + qualifier. Captures *active engagement that delivers value*.

## Input metrics (Amplitude framework)

The North Star is downstream. Input metrics are levers the team can pull. Usually 3–5 inputs, each addressing a dimension of the North Star.

```
       NORTH STAR: Nights booked
              │
   ┌──────────┼──────────┬─────────────┐
   │          │          │             │
Hosts     Searchers   Booking      Repeat
listing   converting  completion   bookers
properties to bookings rate         per cohort
```

Input metrics are the *bridge* between team work and the North Star. A team owns 1–2 inputs.

## Common mistakes

- **Picking revenue as North Star** — revenue lags, and optimizing it directly creates dark patterns. User-value metric instead, with revenue downstream.
- **Picking a vanity metric** — total signups (always grows), pageviews (decoupled from value)
- **Multiple North Stars** — by definition there's one. Multiple = you haven't decided.
- **Changing it every quarter** — the metric is supposed to anchor strategy across years
- **Output mistaken for outcome** — "ship 10 features" is not a North Star. See [outcomes vs outputs](outcomes-vs-outputs.md).

## North Star math

Sometimes the metric is a composite:

```
DAU with ≥7 friends in 10 days  =  Daily Active × Friend Density × Cohort Window
```

Composite metrics force precision: you have to define each term. Simple metrics (e.g. "nights booked") often hide ambiguity ("nights booked when?" "free or paid?").

## Connection to discovery

The North Star sits **above** the [opportunity solution tree](opportunity-solution-tree.md). The OST asks "how do we move our outcome?" — that outcome is usually an input metric to the North Star, not the North Star itself (which is too abstract for a single tree to attack).

```
Vision
   ↓
North Star Metric (one)
   ↓
Input metrics (3-5)
   ↓
Quarterly outcomes
   ↓
OST per outcome
```

## See also

- [Outcomes vs outputs](outcomes-vs-outputs.md) — why metric choice matters
- [HEART framework](heart-framework.md) — Google's UX-specific metric system, complementary
- [Opportunity Solution Tree](opportunity-solution-tree.md) — anchors to outcomes derived from North Star
