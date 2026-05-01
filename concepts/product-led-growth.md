# Product-Led Growth (PLG)

> Sources: OpenView Venture Partners (coined the term, 2016), Wes Bush (*Product-Led Growth*, 2019). The dominant modern B2B SaaS go-to-market motion. Product itself drives acquisition, conversion, and retention — sales is secondary or absent.

## Definition

> A go-to-market strategy where the **product** is the primary vehicle for acquisition, activation, expansion, and (often) revenue.

Contrast with:
- **Sales-led growth** — sales reps acquire and convert; product follows the contract
- **Marketing-led growth** — content/ads acquire; sales closes
- **PLG** — user signs up, uses product, converts to paid, expands without (or with minimal) human touch

## Examples

| Company | PLG mechanism |
|---|---|
| Slack | Free tier; team expands organically; team admin upgrades for unlocks |
| Figma | Free editor; collaborators invited; teams pay for shared assets |
| Notion | Free personal; user adopts at work; team upgrades for collaboration features |
| Calendly | Free scheduling; recipients see Calendly; some sign up |
| Loom | Record video; share; recipients sign up; org pays for analytics |
| Zoom | Free 40-min meetings; viral spread; org buys for unlimited |
| Datadog (early) | Free tier; engineers adopt; spend grows with usage |
| Atlassian | Free / cheap entry products; viral within org |

Pattern: **try → like → spread → upgrade**. Product creates the conditions for its own growth.

## Why PLG works (when it works)

Three structural advantages:

### 1. Lower CAC
Users acquire themselves. No sales rep means no comp + commission. CAC for PLG products is typically 30-70% lower than sales-led.

### 2. Faster time-to-value
User experiences the product directly, immediately. No "schedule a demo" gate. The product proves value in minutes.

### 3. Compounds via [growth loops](growth-loops.md)
PLG products almost always have viral, content, or network-density loops. User → invites → new users → invite more.

These compound: lower CAC + faster TTV + viral spread = the most efficient SaaS GTM ever.

## When PLG fits

PLG isn't universal. It works when:

✅ **Self-serve adoption** — user can extract value alone in minutes (no implementation team needed)
✅ **Bottom-up demand** — individuals or small teams can start without procurement
✅ **Low complexity** — onboarding doesn't require professional services
✅ **Multi-user value** — features get better with more users (sharing, collaboration)
✅ **Low contract risk** — purchase decision doesn't need legal/security review for $20/mo

## When PLG doesn't fit

❌ **Enterprise-only** — products requiring board-level signoff, legal review, multi-month implementation
❌ **Long evaluation cycles** — products users can't evaluate in a single session
❌ **Expensive to provision** — products with high marginal cost per user (some hardware, regulated services)
❌ **Compliance-gated** — HIPAA, FedRAMP, etc., often block self-serve
❌ **Complex configuration** — products that genuinely require services to start

Many companies try PLG and fail because their product isn't self-servable. The product → simple → useful → shareable chain has to actually work.

## The PLG funnel (Bush's framing)

```
Visitor
  ↓ (low-friction signup)
Free user
  ↓ (activation: reach value)
Active user
  ↓ (in-product trigger: hit limit / want feature)
Paid user
  ↓ (expansion: add team, more features)
Champion / advocate
  ↓ (refer)
new visitor (loop closes)
```

Compare to sales-led:

```
Visitor → Lead → MQL → SQL → Demo → Eval → Negotiation → Close
```

PLG funnel has fewer steps and no gatekeepers. Each step must be designed; friction at any step cuts the whole funnel.

## The two PLG models

### 1. Freemium
Free tier exists permanently. Free users have meaningful value but limited features/usage. Examples: Slack, Notion, Figma.

Tradeoff: more users, harder to convert. Conversion rates 1-5% typical.

### 2. Free trial
Time-bounded full access (7-30 days). Either credit-card-required or not. Examples: Linear (14-day trial), Datadog (14-day full), most modern SaaS.

Tradeoff: forces conversion decision; loses long-term virality.

Hybrid: many products do both (free tier + premium trial).

## The activation gate

The single most important PLG metric: **% of new signups who reach the activation event**.

If users sign up but don't activate, every other metric collapses. PLG products obsess over the path from signup → first value:
- Removing setup friction (no install, no config)
- Sample data / templates so users see value immediately
- Tight onboarding focused on activation, not feature tour
- Time-to-first-value (TTV) measured in minutes, not days

See [aha moment / activation](aha-moment.md). PLG is the methodology where activation is most existential.

## Conversion triggers

PLG conversion happens when the user *needs* something the free tier doesn't provide:

- **Limit triggers** — file size, project count, history retention, # users
- **Feature triggers** — advanced analytics, integrations, API access, SSO
- **Collaboration triggers** — invite teammates, share externally, permissions
- **Compliance triggers** — audit log, SAML, on-prem option

The "right" trigger varies by product. Best PLG products have multiple triggers; users hit different ones.

## PLG + Sales (hybrid)

Pure PLG is rare in practice. Most successful PLG companies *eventually* add sales:

```
Stage 1: Pure PLG (early users, $0-$1M ARR)
Stage 2: PLG + automated upgrades ($1M-$10M)
Stage 3: PLG + inside sales for mid-market ($10M-$100M)
Stage 4: PLG + enterprise sales for top-of-pipeline ($100M+)
```

The sales motion sits *on top* of the product motion: sales reps convert PLG-acquired teams into larger contracts. The pipeline is generated by the product, not the SDR.

This is "Product-Led Growth" + "Sales-Assist", not "Sales-Led".

## Common failure modes

### 1. PLG without self-serve product
Wrapping a sales-led product in a free trial doesn't make it PLG. If users can't get value alone, the funnel collapses at activation.

### 2. Free tier too generous
Users get all the value free; never convert. The free tier should be *useful enough to spread* but *constrained enough to drive upgrades*.

### 3. Free tier too stingy
Users hit limits before reaching value; bounce. Free tier must let users experience the product genuinely.

### 4. No virality / sharing built in
PLG products without growth loops grow linearly, not exponentially. CAC may be low but compounding doesn't happen.

### 5. Sales sabotage of PLG
Sales reps "save" PLG leads by converting them to enterprise deals — slowing the PLG funnel. Compensation structure matters: don't reward poaching.

### 6. Wrong metric obsession
Focusing on signups (vanity) instead of activation/retention/conversion (cohort).

### 7. PLG aspirational
"We're going PLG" while still requiring demos for everything. Decide and commit.

## Connection to other concepts

| Concept | Relationship |
|---|---|
| [Aha moment / Activation](aha-moment.md) | Existentially important for PLG |
| [Growth loops](growth-loops.md) | PLG depends on at least one strong loop |
| [PMF](pmf.md) | PLG amplifies PMF; doesn't substitute for it |
| [Pirate Metrics / RARRA](rarra.md) | PLG is fundamentally retention-first |
| [Hooked](hooked.md) | Habit + PLG = strong retention compounding |
| [Cold-start problem](cold-start-problem.md) | PLG products with multi-user value face cold-start |

## See also

- [Aha moment / Activation](concepts/aha-moment.md) — the metric PLG lives or dies on
- [Growth loops](concepts/growth-loops.md) — the structural mechanism behind PLG
- [PMF](concepts/pmf.md) — PLG only works post-PMF
- [Pricing](concepts/pricing.md) — PLG pricing differs from sales-led pricing
- [Cohort analysis](concepts/cohort-analysis.md) — how PLG companies measure health
