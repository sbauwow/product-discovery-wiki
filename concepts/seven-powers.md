# 7 Powers (Helmer)

> Source: Hamilton Helmer, *7 Powers* (2016). The most rigorous taxonomy of strategic moats. Helmer is a longtime strategy consultant and Hawaii-based investor. The book itself is short, dense, philosophical — strategic-thinking infrastructure.

## What a "Power" is (Helmer's definition)

> The set of conditions creating the potential for **persistent differential returns**.

Three components:
1. **Benefit** — a value advantage (lower cost, higher willingness to pay, etc.)
2. **Barrier** — something preventing competitors from arbitraging the benefit away
3. **Persistent** — must hold for years, ideally decades

Power = benefit + barrier. Without barrier, benefit gets competed away. Without benefit, barrier is irrelevant.

A product without a Power is a commodity. Commodities have low margins, no defensibility.

## The seven powers

Helmer's exhaustive list (he claims these are the *only* sources of true Power):

### 1. Counter-positioning
A new entrant adopts a new business model that the incumbent **cannot** copy without damaging its existing business.

The incumbent's *strength* is the barrier. They could match the new model technically, but doing so would cannibalize their core revenue. They're trapped.

Examples:
- **Vanguard** vs Fidelity (low-cost index funds — Fidelity couldn't match without crushing its high-fee mutual fund business)
- **Netflix streaming** vs Blockbuster (DVD-by-mail was first counter-position; streaming was second; Blockbuster's store revenue trapped them)
- **Generic drug makers** vs branded pharma

The most under-appreciated Power. Often invisible to incumbents until too late.

### 2. Scale economies
Cost-per-unit decreases as scale grows. Larger competitor inherently has lower cost.

Barrier: smaller competitors face higher cost per unit; can't profitably match price.

Examples:
- **Walmart** (logistics scale → lower retail prices)
- **Amazon AWS** (data-center scale)
- **TSMC** (semiconductor manufacturing scale)

### 3. Network economies
Value to each user grows with total users. See [network effects](network-effects.md).

Barrier: a competitor starting from zero is at zero value; can't recruit users.

Examples:
- **Facebook** (social graph)
- **Visa/Mastercard** (cardholder ↔ merchant network)
- **App Store** (developers ↔ users)

### 4. Switching costs
Users face cost to switch to a competitor — financial, learning, integration, social.

Barrier: even a competitor with a 20% better product can't win because switching cost > benefit.

Examples:
- **Salesforce** (data, training, integrations)
- **iPhone** (apps, photos, ecosystem)
- **Bloomberg Terminal** (workflow lock-in)

### 5. Branding
Customers assign higher value to a product because of brand associations (trust, status, identity), independent of functional difference.

Barrier: building a competing brand takes decades + significant investment.

Examples:
- **Tiffany** (jewelry indistinguishable from competitors gets 5-10x markup)
- **Coca-Cola** (taste tests show parity with Pepsi)
- **Hermès** (handbag brand)

Helmer notes: branding is the most-misused word. True Power-grade brand requires *multi-decade* trust building, not marketing campaigns.

### 6. Cornered Resource
Privileged access to a resource (talent, IP, supplier relationship, government concession) that competitors can't get.

Barrier: the resource is finite and held.

Examples:
- **Disney/Pixar** in 2000s (a small set of geniuses producing hits)
- **De Beers** (historical diamond mining concentration)
- **Chinese rare-earth processing**
- **Genentech early biotech** (specific scientific talent)

Risk: cornered resources can leak (people quit, contracts expire). Less durable than other Powers.

### 7. Process Power
Embedded organizational processes that produce a sustained advantage; cannot be copied via hiring or imitation because they're tacit.

Barrier: process is *learned*, not codified. Even with a manual, competitors can't replicate it without years of practice.

Examples:
- **Toyota Production System** (decades; competitors with full manuals couldn't replicate)
- **TSMC manufacturing know-how** (process, not just scale)
- **Stripe / Apple operational excellence**

Process Power is rare and slow-built. The most under-claimed Power because it sounds boring.

## Power × business stage

Helmer's key insight: different Powers are accessible at different stages.

| Stage | Powers easiest to establish |
|---|---|
| **Origination** (startup, pre-PMF) | Counter-positioning, Cornered Resource |
| **Take-off** (post-PMF, scaling) | Scale economies, Network economies, Switching costs |
| **Stability** (mature) | Branding, Process Power |

Trying to build the wrong Power at the wrong stage usually fails. A startup focused on Branding before product-market fit is usually wasting money. A mature company trying to "counter-position itself" can't — incumbents can't counter-position.

## Why this matters for product

Most product strategy ignores defensibility. Teams build features users want without asking: *what stops competitors from copying?*

Without a Power, even successful products are temporary. The seven categories give a checklist:

1. Could a competitor copy our value prop within 12 months? If yes, no Power yet.
2. If yes, what barrier keeps them out? Map to one of the seven.
3. If no barrier, you're building a commodity. Reposition, or accept low margins.

## The route to power

Helmer argues each Power has a typical *route*:

| Power | Route |
|---|---|
| Counter-positioning | Identify business-model trap incumbent is in; build around it |
| Scale economies | Aggressively grow share early; cost advantage compounds |
| Network economies | Solve [cold-start](cold-start-problem.md); reach tipping point |
| Switching costs | Embed deeply in workflow / data / habits |
| Branding | Decade+ of consistent quality + signaling |
| Cornered Resource | Lock up the resource via contracts, equity, exclusivity |
| Process Power | Iterate the process for years; resist documentation pressure |

Different Powers, different time horizons, different organizational capabilities. Strategy = picking which Power to pursue *first*, given startup-stage constraints.

## Comparison with other strategy frameworks

| Framework | Focus |
|---|---|
| **Porter's Five Forces** | Industry attractiveness; mostly red-ocean |
| **[Wardley Mapping](wardley-mapping.md)** | Component evolution and positioning |
| **[Disruption Theory](disruption-theory.md)** | Why incumbents lose; pattern of attack |
| **[Blue Ocean](blue-ocean.md)** | Differentiation through new value curves |
| **7 Powers** | Defensibility — *what's the moat?* |

7 Powers is the most rigorous treatment of moats specifically. Pair with Wardley/Disruption for positioning, with JTBD/discovery for value creation, with Blue Ocean for differentiation.

## When 7 Powers matters

✅ Strategic planning at any stage
✅ Pitch / fundraising (investors care about moats)
✅ M&A diligence (assessing target's defensibility)
✅ Long-horizon strategic bets
✅ Identifying which Power to pursue next (vs. all of them)

## When less useful

❌ Tactical product decisions
❌ Pre-PMF discovery (need to find PMF first; defensibility comes later)
❌ Single-quarter execution
❌ Markets where regulation provides the moat (banks, utilities)

## Common failure modes

- **"We have brand"** — saying it doesn't make it true; few startups have brand-grade differentiation
- **Imagined network effects** — community features ≠ network economies
- **Counter-positioning that can be copied** — incumbent isn't actually trapped; they will respond
- **Switching costs that customers tolerate** — too low to deter
- **Pursuing all seven simultaneously** — strategy is choice; can't focus on all
- **Confusing benefit with Power** — having a benefit that competitors *will* copy isn't Power

## See also

- [Network effects](concepts/network-effects.md) — Power #3 in detail
- [Disruption theory](concepts/disruption-theory.md) — Power #1 (counter-positioning) deep dive
- [Wardley Mapping](concepts/wardley-mapping.md) — adjacent strategic frame
- [Blue Ocean](concepts/blue-ocean.md) — differentiation; complements Powers
- [Product strategy](concepts/product-strategy.md) — Powers inform what game to play
