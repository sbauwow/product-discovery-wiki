# Product Operating Model

> Source: Marty Cagan, *Transformed* (2024). The org-level frame for *how* a company runs product. Distinct from individual practices like [continuous discovery](continuous-discovery.md) — addresses the whole system: strategy, structure, culture, hiring, decision-making.

## What it is

> "How a company creates, develops, and delivers products to its customers."

The product operating model is the org-wide answer to:
- How are decisions made about what to build?
- Who has authority over those decisions?
- How are teams structured?
- How is success measured?
- What's the relationship between product, design, engineering, and the rest of the business?
- How is talent hired, developed, and promoted?

Most orgs have an *implicit* operating model — usually inherited, usually broken. Cagan argues making it *explicit* and deliberately designed is the senior leadership task.

## The transformation Cagan diagnoses

```
FROM (feature factory model)               TO (product operating model)
────────────────────────────────────       ────────────────────────────
Stakeholder requests → roadmap             Outcomes → discovery → bets
Project managers, BAs                       Empowered PMs
Specs handed to engineers                  Engineers in discovery
Output measured                            Outcomes measured
Roadmap as commitment                      Roadmap as bets
Fragmented design / eng / product          Trio model
Quarterly planning theater                 Continuous discovery
Hiring for "execution"                     Hiring for judgment
```

The "transformation" is from feature-factory to outcome-driven. Cagan's argument: this isn't a process change; it's an operating-model change touching every part of the company.

## The four dimensions

### 1. Product Strategy
How the company decides what game to play. Includes:
- [Vision and product strategy](product-strategy.md)
- Translating strategy into team-level outcomes
- Connection to business strategy

Most orgs jump straight to tactics ([roadmap](roadmap-trap.md)) without product strategy. Cagan: this is the most-missing layer.

### 2. Product Discovery
How the company decides which solutions to build. Includes:
- [Continuous discovery](continuous-discovery.md) practice
- [Empowered teams](empowered-team.md) with the trio
- [OST](opportunity-solution-tree.md) and similar artifacts
- Customer access for teams

### 3. Product Delivery
How the company gets shipped solutions to users. Includes:
- Engineering practices (CI/CD, testing, release engineering)
- Design system and component libraries
- Production telemetry and operations
- Cross-team coordination

Cagan's frequent observation: many orgs are good at one of discovery/delivery and bad at the other. Both must work for the operating model to function.

### 4. Product Culture
The norms and behaviors that make the rest possible. Includes:
- Outcome-orientation
- Customer-centricity
- Continuous learning, comfort with failure
- Strong-opinion-loose-grip leadership
- Trust between PM, design, eng

Culture is downstream of leadership behavior + hiring. Hard to "install"; can be lost in months.

## The hard parts

### Talent
Strong PMs, strong designers, strong tech leads are scarce. Most orgs underinvest:
- PMs hired for project management skills, not product judgment
- Designers treated as service bureau
- Tech leads not paired with PMs for shared ownership

Cagan: 70%+ of "transformation failures" come down to inadequate talent. Process won't fix a weak trio.

### Trust from leadership
Empowered teams require executive trust — accepting that teams will sometimes make bets that don't pay off, in service of higher-leverage wins. Most leadership teams say they want this; few accept the variance.

### Sales / customer commitments
Sales-led businesses promise features to customers ahead of build. This locks the team out of discovery. Reconciling sales urgency with product discovery is the most-common organizational fight.

### Compensation alignment
PMs comp'd on shipping ≠ PMs comp'd on outcomes. The metric that pays is the metric that gets optimized. Misaligned comp silently destroys operating-model intent.

## Operating model vs methodology

| Methodology | Operating model |
|---|---|
| How a *team* works | How the *company* works |
| Discovery practice (interviews, prototypes) | Discovery culture (cross-team) |
| Sprint cadence | Quarterly bet cadence |
| OKRs | Outcome culture |
| Tactical | Strategic |

A team can practice [continuous discovery](continuous-discovery.md) inside a feature-factory company — but it's swimming upstream. The operating model determines whether the team's good practices propagate or get crushed.

## Cagan's reform sequence

In *Transformed*, Cagan describes the sequence orgs typically need:

1. **Leadership commitment** — without senior commitment to outcomes-over-output, nothing else lands
2. **Build a strong product leader** — head of product who can model the change
3. **Hire/develop strong PMs** — the trio core
4. **Pair with strong designers and tech leads** — complete the trio
5. **Restructure teams around outcomes** — not features or systems
6. **Replace the roadmap** — outcomes, not features, with [Now/Next/Later](now-next-later.md)
7. **Build discovery rhythm** — weekly customer touchpoints
8. **Measure outcomes, not output** — even when outputs are easier to count
9. **Re-align comp + promotion** — to outcome impact
10. **Defend culture** — every decision either reinforces or erodes the operating model

The sequence isn't linear; reality is messy. But skipping #1 dooms the rest.

## What about scaled product orgs

Cagan's work focuses on tech-product companies. For larger orgs (1000+ engineers), operating models often layer:

- **Squads / teams** — each runs the trio model
- **Tribes / domains** — multi-team ownership of broader outcome areas
- **Platform / enabling teams** — see [Team Topologies](team-topologies.md)
- **Product leadership** — strategy, hiring, culture

Spotify popularized one variant (later widely critiqued). [Team Topologies](team-topologies.md) is the modern reference for scaled team-shape design.

## Common failure modes

- **Process imitation without culture change** — adopting OKRs, OSTs, dual-track agile while keeping output-oriented leadership; result: theater
- **Org chart change without operating-model change** — restructuring teams to look right while keeping feature-factory behavior
- **CPO without leadership trust** — strong product leader hired but vetoed by CEO/exec on every bet; transformation stalls
- **Metric games** — orgs claim outcome focus while reporting feature counts to the board
- **Premature scaling** — trying to install the operating model before strong PMs/designers/eng leads exist
- **Single-team success without spread** — one team adopts the model but the rest of the org doesn't; team eventually conforms or burns out

## Connection to other concepts

| Concept | Relationship |
|---|---|
| [Empowered team](empowered-team.md) | The team-level unit of the operating model |
| [Continuous discovery](continuous-discovery.md) | The discovery practice the model enables |
| [Outcomes vs outputs](outcomes-vs-outputs.md) | The philosophical core |
| [Build trap](build-trap.md) | The operating-model failure Perri diagnoses |
| [Feature factory](feature-factory.md) | The dominant alternative operating model |
| [Team Topologies](team-topologies.md) | The scaled team-shape framework |
| [Product strategy](product-strategy.md) | The strategy layer of the model |

## See also

- [Empowered team](concepts/empowered-team.md)
- [Continuous Discovery](concepts/continuous-discovery.md)
- [Build trap](concepts/build-trap.md)
- [Team Topologies](concepts/team-topologies.md)
- [Product strategy](concepts/product-strategy.md)
- [Strong PM](concepts/strong-pm.md)
