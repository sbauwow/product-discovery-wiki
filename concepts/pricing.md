# Pricing

> Sources: Madhavan Ramanujam (*Monetizing Innovation*), Patrick Campbell (ProfitWell/Paddle), Hermann Simon (*Power Pricing*), McKinsey pricing literature. The single highest-leverage product decision — and the one most often delegated, deferred, or anchored on cost-plus rather than value.

## Why pricing matters more than features

A 1% price increase produces (on average) a 7-11% profit increase. A 1% volume increase produces ~3%. Pricing has roughly **3x the leverage** of acquisition or retention efforts on the bottom line.

Yet most teams:
- Spend 100x more time on features than pricing
- Set price by copying competitors or marking up cost
- Don't run pricing experiments
- Use pricing tiers designed by engineering, not user needs
- Never revisit pricing after launch

The math punishes this. A pricing rethink can outweigh a year of feature development.

## Three pricing approaches

### 1. Cost-plus pricing
Price = cost × markup.

Useful for commodities, regulated industries, or genuine utilities. Useless for software, where marginal cost ≈ 0 and price has nothing to do with cost.

Avoid for SaaS / digital products. Always.

### 2. Competitor-anchored pricing
Price = competitor's price ± 20%.

Common, lazy, sometimes right. Works when you're a "me-too" product in a known category. Fails when you're differentiated, when category is forming, or when competitors are themselves mispricing.

The trap: competitors mispriced often → you copy → race to the bottom.

### 3. Value-based pricing
Price = function of value delivered to customer.

Right approach for differentiated products. Hard to do well. Requires understanding what customer values, what they currently pay, what alternatives cost.

## The Van Westendorp Price Sensitivity Meter (PSM)

The most practical pricing-research tool. Survey-based, asks four questions per respondent:

```
1. At what price would [product] be too expensive to consider?           → Too expensive
2. At what price would [product] be a bargain — great value?             → Bargain
3. At what price would [product] start to seem expensive (still buy)?    → Expensive
4. At what price would [product] be so cheap you'd doubt its quality?    → Too cheap
```

Plot cumulative distributions:

```
% respondents
  100% │  ╲                                            
       │   ╲                                            ╱
       │    ╲ "Too cheap"                              ╱  "Too expensive"
       │     ╲                                        ╱
       │      ╲                                      ╱
       │       ╲          ●  Optimal Price Point   ╱
       │        ╲       ╱  ╲                      ╱
       │         ╲    ╱      ╲                  ╱
       │          ╲ ╱          ╲              ╱
       │   "Bargain"             ╲          ╱   "Expensive"
       │     ╱                     ╲      ╱
       │   ╱                         ╲  ╱
       │ ╱                             ╲
       └────────────────────────────────────────→ price
```

Intersections give:
- **Indifference Price Point** — Bargain × Expensive
- **Optimal Price Point** — Too cheap × Too expensive
- **Range of Acceptable Prices** — between intersections

Sample size: 200+ for stable curves. Per-segment: 200 each. Caveats: stated preference, not behavioral. PSM is directional, not definitive — pair with [A/B testing](ab-testing.md) on real prices when possible.

## Pricing dimensions

Beyond "what's the number," pricing has structural dimensions:

### Pricing model
- **Subscription** (monthly/annual) — recurring revenue, predictable
- **Per-seat** — scales with team size; aligns with usage in collaborative tools
- **Usage-based** — pay-as-you-go; tracks value delivered (Snowflake, Twilio, OpenAI API)
- **Tiered** — Free / Starter / Pro / Enterprise; segment customers
- **Freemium** — free forever for some, paid for more
- **One-time** — single purchase (legacy software, hardware)
- **Marketplace fees** — % of GMV (Stripe, App Store, Airbnb)

Right model depends on the product's value mechanism. A storage product priced per-seat is mispriced. A collaborative product priced by storage is mispriced.

### Tier structure
Standard 3-tier:
```
FREE / STARTER  →  PROFESSIONAL  →  ENTERPRISE
"try it"           "main offering"   "everything + sales"
```

Tier triggers should align with [aha moment](aha-moment.md) progression — what unlocks at each tier maps to the user's growing usage. Bad: tiers separated by random feature gates ("white label" in Pro? why?).

### Anchoring
The way prices are presented affects willingness to pay:
- **Decoy pricing** — show 3 tiers; middle becomes obvious choice
- **Annual discount anchoring** — show monthly first ($20/mo) then annual ($15/mo, billed annually) to imply discount
- **Strike-through** — original price crossed, sale price highlighted
- **High-anchor enterprise** — "Enterprise: contact us" makes Pro look reasonable by comparison

These work behaviorally; they're also easy to over-rotate into manipulation. Use carefully.

## Pricing strategy for new products

Two strategic choices for launch:

### Penetration pricing
Start low, gain share, raise prices later.
- Pros: faster adoption, harder for competitors to enter
- Cons: leaves money on table; later price hikes anger early users; can anchor low forever

Examples: most consumer SaaS, mobile apps.

### Skim pricing
Start high, capture early-adopter willingness-to-pay, lower over time.
- Pros: maximize early revenue, position as premium
- Cons: slower adoption, attracts competitors

Examples: Apple hardware, premium B2B SaaS, anything aimed at enterprise.

## The Bain pricing zones

Madhavan Ramanujam's product-pricing framework:

```
                     PRICE
                       │
                       │
 OVERSHOT  ←──── willingness to pay ────→  UNDERPRICED
                       │
                  → product price
                       │
                       │
                  CUSTOMER VALUE
```

Common pricing failures:
- **Overshoot** — price > willingness; market shrinks (B2B enterprise pricing on a consumer product)
- **Undershoot** — price < willingness; profit left on table (most SaaS, especially early)
- **Wrong slope** — pricing doesn't increase with value (per-seat pricing for usage-driven product)

## Pricing experiments

Pricing should be **tested**, not assumed.

Methods:
1. **A/B test prices** — show different visitors different prices, measure conversion
   - Legal/ethical concerns: usually OK for new visitors, problematic for existing customers
2. **Cohort price changes** — new sign-ups face new pricing; old customers grandfathered
3. **Plan migration** — offer new tiers; track who picks what
4. **Sales price discovery** — for B2B, sales reps probe price ceiling per deal
5. **Discount opt-in research** — offer discount with reason ("first 100"); measures price elasticity

Caveat: pricing changes can damage brand. Experimentation needs to be invisible to public eye. Most successful pricing changes are small + segment-specific + grandfathered.

## Pricing in PLG

[Product-led growth](product-led-growth.md) products have specific pricing patterns:

- Free tier as marketing — not for revenue, for spread
- Self-serve up to ~$2K/year; sales-assist above
- Triggers (limits, features) cause natural upgrades
- Annual contracts preferred for retention; monthly for early revenue

Pricing in PLG is *also* user experience — encountering a price ceiling is part of the product flow. Bad pricing = bad UX in PLG.

## Pricing in enterprise

Different rules apply:
- Negotiated pricing (each deal custom)
- Annual contracts (multi-year preferred)
- Volume discounts (sliding scale)
- Custom features tied to ACV (annual contract value)
- Procurement gauntlet (SOC 2, security review, MSA)

Pricing here is less about list-price discovery and more about price-realization (what % of list customers actually pay).

## Common failure modes

- **Set once, never revisit** — pricing should be reviewed at least quarterly
- **Cost-plus on software** — almost always wrong
- **Mimicking competitors who are mispriced** — cascading wrongness
- **Pricing anchored on engineering effort** — engineers spent a year on it ≠ customers value it
- **One-size-fits-all** — different segments value differently; need different tiers/plans
- **Discount addiction** — always-on discounts erode list price perception
- **Free tier too generous** — see [PLG](product-led-growth.md) failures
- **No segmentation** — measuring "average price" hides segment-level reality
- **Pricing as afterthought** — assigned to marketing or sales when it should be product-strategic

## When to invest in pricing research

✅ Pre-launch (before pricing is "set")
✅ Pre-fundraise (revenue uplift impacts valuation)
✅ Quarterly review (always)
✅ When competitor moves prices
✅ Before adding a new tier or plan
✅ Annually after launch (markets shift)

## Tools

- **Paddle / Stripe Billing** — payment + experimentation
- **ProfitWell (now Paddle)** — pricing benchmarks, retention analytics
- **Conjoint analysis tools** — Sawtooth, Qualtrics — for advanced research
- **Custom Van Westendorp surveys** — Typeform, Qualtrics

## See also

- [PLG](concepts/product-led-growth.md) — pricing as part of self-serve flow
- [Surveys](concepts/surveys.md) — Van Westendorp PSM is one survey method
- [PMF](concepts/pmf.md) — without PMF, pricing is mostly guesswork
- [Cohort analysis](concepts/cohort-analysis.md) — how pricing changes show up in retention
- [A/B testing](concepts/ab-testing.md) — for live pricing experiments
