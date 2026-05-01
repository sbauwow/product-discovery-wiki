# Network Effects

> Sources: Theodore Vail (Bell Telephone, ~1908) original observation; Bob Metcalfe (Metcalfe's Law, 1980); Reid Hoffman, James Currier (NFX), Sangeet Choudary (modern formulation). The most powerful — and most defensible — moat in software.

## Definition

> A product has network effects if it gets *more valuable* as more people use it.

Counter-examples: most SaaS tools (each user gets the same value regardless of how many others use it). Network-effect products: Facebook (more friends = more value), Uber (more drivers = faster pickup = more riders = more drivers).

The key property: the product **defends itself**. More users → better product → more users. Compounds.

## Metcalfe's Law

The original quantification:

```
Value of a network ≈ n²
where n = number of users
```

Adding a user doesn't add 1 unit of value; it adds *n* units (since they can interact with all existing users). Doubling users quadruples value.

Modern critiques: pure n² overstates real networks (most users don't interact with most others). More accurate models:
- **n log(n)** — Briscoe/Odlyzko/Tilly — better fit to real social networks
- **Sub-linear** — Reed's Law: groups of users (n²ⁿ) overstates again

Whatever the exact curve, the principle holds: value scales **non-linearly** with users in network-effect businesses.

## Five major types (NFX taxonomy, simplified)

### 1. Direct (same-side) network effects
Users get value from other users *of the same kind*.

Examples: Facebook (friends connect), WhatsApp (any contact can message), Skype.

Strongest type. Each new user makes every other user's experience better.

### 2. Indirect (cross-side) network effects
Two distinct sides; each side benefits from growth of the other.

Examples: Uber (riders ↔ drivers), Airbnb (guests ↔ hosts), eBay (buyers ↔ sellers), credit card networks (cardholders ↔ merchants).

Powerful but harder — must grow both sides; see [cold-start problem](cold-start-problem.md).

### 3. Data network effects
Product gets better as more users generate more data.

Examples: Google Search (queries → ranking signal), Waze (drivers → traffic data), Spotify recommendations.

Defensibility from accumulating data is increasingly central to AI products. Often paired with direct network effects.

### 4. Social network effects
Users join because their social circle is on it; status / identity tied to use.

Examples: Instagram, LinkedIn, BeReal (briefly).

Strongest "lock-in" type but most fragile to fashion shifts (MySpace → Facebook → ...).

### 5. Marketplace / Platform network effects
Cross-side + market dynamics — pricing, search, discovery, trust mechanics.

Examples: Amazon, Shopify, App Store.

Most complex; combines multiple effect types.

Plus: tech, language, belief, expertise (Currier lists ~13 sub-types).

## Why network effects defend incumbents

Once dominant, they're hard to dislodge:

| Mechanism | Explanation |
|---|---|
| **Switching cost** | All my friends are on FB; can't take them with me |
| **Cold start cost** | Competitor starts at 0 users → 0 value → can't recruit users |
| **Density advantage** | Uber arrives in 3 min; competitor in 12 — riders pick the faster one |
| **Multi-homing tax** | Users keep both apps; competitor pays full cost, captures partial value |

The result: even better products lose if they lack network density. Google+ vs Facebook. Path vs Instagram. Many would-be competitors die in the cold-start phase.

## Tipping points

Network effects often have a **threshold**:

```
Value
  │                              ╱──── steep growth, dominant
  │                            ╱
  │                          ╱
  │                        ╱
  │     ─────────────╱── tipping point (~10-20% of TAM)
  │   ╱
  │ ╱  flat, sub-critical, vulnerable
  └─────────────────────────────────→ users
```

Below tipping point: product is fragile, can be killed. Above: self-reinforcing, hard to kill.

Hitting tipping point is the hardest startup task in network products. See [cold-start problem](cold-start-problem.md).

## Strength gradient

Not all network effects are equal. NFX's categorization (rough):

| Strength | Examples |
|---|---|
| **Strongest** | Direct + dense (FB, WeChat, telephone) |
| **Strong** | Two-sided marketplace at density (Uber, Airbnb) |
| **Medium** | Data network effects (Google, Spotify) |
| **Weak** | Light social (Strava, Goodreads) |
| **None** | "Community features" bolted onto utility products |

The strength determines defensibility. A product with weak network effects can still win — but on execution, not moat.

## Local vs global network effects

| Local | Global |
|---|---|
| Need density in a *region* | Need density worldwide |
| Uber, Tinder, food delivery | Email, Skype, Bitcoin |
| Easier to bootstrap (city by city) | Harder to bootstrap |
| Multiple regional winners possible | Winner-take-most likely |

Uber didn't need NYC to be on the same network as Paris. Bitcoin did. Strategy implication: local-network products can be regionally bootstrapped; global-network products need critical mass everywhere at once.

## The 2x2 of network effects + winner-take-all

```
                 STRONG NETWORK EFFECTS
                          │
                  WTM ←───┼──→ Multi-homing
                          │      acceptable
                  ──────────────────────→ Switching cost
            ↓
       weak network effects
```

Strong NFX + high switching cost = winner-take-most (Facebook in social).
Strong NFX + multi-homing OK = several winners coexist (Slack and Teams).
Weak NFX = competitive market (most B2B SaaS).

## How to design for network effects

If you're building a product that *could* have network effects:

1. **Identify which type** — direct, two-sided, data, etc. Different design implications.
2. **Find the atomic network** — the smallest unit of value (more in [cold-start](cold-start-problem.md))
3. **Solo value first** — product must be useful to user 1, not just user 1000. Single-player mode before multi-player. (Notion, Figma both did this.)
4. **Reduce friction at every step** — cold start is fragile; one bad onboarding kills the network
5. **Measure density, not users** — total signups means nothing if density per atomic network is low
6. **Defend post-tipping** — once dominant, switching cost / multi-homing tax / data advantage compounds

## Common failure modes

- **Imagined network effects** — "we have community features, so we have network effects" — usually false
- **Network effects without product-market fit** — can't bootstrap any network if the underlying product doesn't deliver value
- **Single-side focus** — building only the supply (or demand) side of a marketplace; the other side never bootstraps
- **Density confusion** — celebrating user count when local density is what matters
- **Late multi-homing tolerance** — once users keep both apps, your switching-cost moat is gone; defend density obsessively
- **Misjudging strength** — claiming "strong network effects" when effects are weak; investors and competitors see through

## See also

- [Cold-start problem](concepts/cold-start-problem.md) — how to bootstrap a network from zero
- [Growth loops](concepts/growth-loops.md) — UGC and density loops produce network effects
- [Wardley Mapping](concepts/wardley-mapping.md) — strategic positioning relative to network effect dynamics
- [PMF](concepts/pmf.md) — network products often have segment-specific PMF (a city, a niche) before global PMF
- [Hooked](concepts/hooked.md) — habit + network effects compound defensibility
