# RARRA (Retention-First Pirate Metrics)

> Source: Thomas Petit & Gabor Papp, ~2018, building on Reichheld and Sean Ellis. A reordering of [AARRR](pirate-metrics.md) that puts **retention first**.

## The reordering

```
AARRR (McClure, 2007):    Acquisition → Activation → Retention → Revenue → Referral
RARRA (Petit/Papp):       Retention → Activation → Referral → Revenue → Acquisition
```

Same five stages. Different priority order.

## Why retention-first

McClure's AARRR was written when **acquisition was hard and expensive**. Mobile-app-store competition, ad costs, and saturation have flipped the dynamic — *most* products can acquire users; few can keep them.

Reichheld's research (Bain, 1990s) showed:
- 5% increase in retention → 25–95% increase in profit
- Acquiring a new customer costs 5–25× retaining an existing one
- Reducing churn 1% can outweigh growth investments

If retention is broken, every other stage compounds the leak. Hence: **fix retention before you fix anything else.**

## The RARRA mental model

```
                  RETENTION  ←── start here
                      ↑
                      │ retention enables...
                      │
                  ACTIVATION
                      ↑
                      │ activation produces...
                      │
                  REFERRAL  
                      ↑
                      │ referral compounds...
                      │
                  REVENUE
                      ↑
                      │ revenue funds...
                      │
                  ACQUISITION  ← last, only after retention works
```

You scale acquisition only after the bucket holds water.

## The leaky bucket diagnosis

```
ACQUISITION: 1000 new users / month  ← pouring in
           ↓
ACTIVATION: 30% activate = 300 / month
           ↓
RETENTION:  Day-30 retention = 8%
           ↓
ACTIVE:     ~24 / month sticking
           ↓
REVENUE:    8% of those convert = ~2 paying / month

Result: paying $50 CAC × 1000 = $50,000 to acquire 2 paying users
        → CAC per paying user = $25,000
        → Unsustainable
```

Pouring more into acquisition makes it worse. Fix retention first.

## What RARRA practice looks like

### Step 1: Measure retention honestly
Use [cohort analysis](cohort-analysis.md), not aggregate metrics. Look at:
- Day-1, Day-7, Day-30 retention by cohort
- Retention curve shape (smile / flat / frown)
- Segment-by-acquisition-channel (some channels bring stickier users)

### Step 2: Find the activation event
[Aha moment / activation](aha-moment.md). The behavior most predictive of retention. Optimize the path to it.

### Step 3: Build habit loops
Once users hit aha, design the [Hooked](hooked.md) loop that brings them back: trigger → action → variable reward → investment.

### Step 4: Drive referral
Retained users are your best acquisition channel. Build in shareability, in-product invites, NPS-driven word-of-mouth.

### Step 5: Convert revenue
Among retained users, optimize the path to paid (free→paid trigger, plan choice).

### Step 6: Scale acquisition
Now that LTV is meaningful, paid acquisition becomes profitable. Scale.

## When RARRA fits better than AARRR

- **Mobile apps** — acquisition is paid, retention is the moat
- **SaaS** — recurring revenue requires retention by definition
- **Marketplaces** — both sides need to retain or the marketplace collapses
- **Subscription products** — churn = death; retention = survival

## When AARRR ordering can still work

- **Ultra-early stage** — no retention data yet; need users in the door first
- **Pure-play viral products** — acquisition is the whole game; retention follows network effects
- **Single-purchase products** — no retention concept (one-time SaaS purchase, hardware sale)

## Why RARRA is increasingly the default

- Ad costs up >> 10× since 2007
- Mobile attribution / privacy changes (iOS ATT, cookie deprecation) make acquisition harder + more expensive
- Saas + subscription dominance puts retention front and center
- Investor sophistication: VCs measure cohort retention, not signups

Most modern product orgs implicitly run RARRA even when they cite AARRR.

## Common failure modes

- **Optimize acquisition, hope retention follows** — classic mistake; bucket leaks faster than it fills
- **Aggregate retention metrics** — without cohorts, retention can look flat while individual cohorts collapse
- **Onboarding ≠ activation** — confusing "completed tour" (vanity output) with "reached aha" (real activation)
- **"Retention is just churn"** — narrow framing; retention also includes engagement frequency, not just attrition
- **Ignoring referral** — RARRA explicitly puts referral *before* revenue because retained-and-referring users are the cheapest acquisition channel

## See also

- [Pirate Metrics (AARRR)](concepts/pirate-metrics.md) — the original framework
- [Cohort analysis](concepts/cohort-analysis.md) — the only honest retention measurement
- [Aha moment / Activation](concepts/aha-moment.md) — gateway to retention
- [Hooked](concepts/hooked.md) — the habit loops that produce retention
- [Vanity metrics](concepts/vanity-metrics.md) — what most "growth" reporting actually shows
