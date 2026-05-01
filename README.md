# Product Discovery Wiki

A first-principles reference for modern product discovery. Dense, hyperlinked, opinionated. Each concept lives on its own page; this index connects them.

> **Discovery** = deciding *what to build* and *why*. **Delivery** = building it. Most failed products are correctly built solutions to wrongly chosen problems. Discovery is the work of not doing that.

---

## Mental model

```
                    Product Strategy            ← what game we're playing
                          │
                    North Star Metric           ← single anchor outcome
                          │
                       Outcome
                          │
              ┌───────────┴───────────┐
         Opportunity              Opportunity   ← user needs/pains
              │                       │
        ┌─────┴─────┐           ┌─────┴─────┐
     Solution   Solution     Solution   Solution ← ideas
        │                       │
    Experiment              Experiment           ← tests of assumptions (RAT)
        │                       │
   ──────────────────────────────────
        validated bets enter delivery
```

Top-down: strategy → outcome → opportunities → solutions → experiments. Bottom-up: evidence reshapes the tree weekly.

---

## The four risks ([Cagan](concepts/cagan-four-risks.md))

Every product idea is killed by one of:

1. **Value** — will users buy/use it?
2. **Usability** — can they figure it out?
3. **Feasibility** — can engineers build it with available time/tech/data?
4. **Viability** — does it work for the business (legal, finance, brand, GTM)?

Discovery exists to reduce these *before* delivery commits.

---

## Core concepts

### Strategy & vision (what game are we playing)
- [Product strategy](concepts/product-strategy.md) — Rumelt-style diagnosis + policy + actions; the missing layer in most orgs
- [Wardley Mapping](concepts/wardley-mapping.md) — strategic positioning by visibility × evolution
- [North Star Framework](concepts/north-star.md) — one outcome metric anchoring strategy
- [PR/FAQ (Working Backwards)](concepts/pr-faq.md) — Amazon's press-release-first method

### Frameworks (how to organize discovery)
- [Dual Track Agile](concepts/dual-track-agile.md) — discovery and delivery as parallel tracks within one team
- [Continuous Discovery](concepts/continuous-discovery.md) — weekly user touchpoints, not quarterly research sprints
- [Opportunity Solution Tree (OST)](concepts/opportunity-solution-tree.md) — Torres's central artifact
- [Lean UX](concepts/lean-ux.md) — Gothelf; hypothesis-driven design, outcomes over deliverables
- [Lean Startup loop](concepts/lean-startup.md) — build → measure → learn
- [Customer Development](concepts/customer-development.md) — Steve Blank; search vs execution
- [Innovation Accounting](concepts/innovation-accounting.md) — Ries's metric system for pre-PMF teams
- [Cynefin](concepts/cynefin.md) — Snowden; complexity-domain framework for choosing approach
- [Design Sprint](concepts/design-sprint.md) — 5-day timeboxed discovery for stuck problems
- [Shape Up](concepts/shape-up.md) — Basecamp's 6-week-cycle alternative methodology
- [Now / Next / Later](concepts/now-next-later.md) — outcome-shaped roadmap format

### Methods (how to generate insight)
- [Jobs To Be Done (JTBD)](concepts/jobs-to-be-done.md) — users hire products to do jobs
- [Outcome-Driven Innovation (ODI)](concepts/odi.md) — Ulwick; quantitative cousin to JTBD
- [User interviews](concepts/user-interviews.md) — past-behavior probes, not opinion polls
- [The Mom Test](concepts/mom-test.md) — Fitzpatrick; three-rule discipline for honest interviews
- [Empathy maps](concepts/empathy-map.md) — Says/Thinks/Does/Feels synthesis
- [Personas](concepts/personas.md) — composite users, with critique
- [Assumption mapping](concepts/assumption-mapping.md) — list, plot, test the riskiest
- [Riskiest Assumption Test (RAT)](concepts/rat.md) — sharper alternative to MVP
- [Prototyping](concepts/prototyping.md) — feasibility, user, live-data, Wizard-of-Oz
- [Five-second test](concepts/five-second-test.md) — quick clarity / value-prop check
- [A/B testing](concepts/ab-testing.md) — quantitative validation via random assignment
- [Story mapping](concepts/story-mapping.md) — user journey as backbone, slices as releases
- [Customer journey maps](concepts/customer-journey-maps.md) — end-to-end experience across all touchpoints
- [Service blueprints](concepts/service-blueprint.md) — CJM extended with backstage operations

### Strategic canvases & artifacts
- [Business Model Canvas](concepts/business-model-canvas.md) — Osterwalder; nine-block business model viz
- [Lean Canvas](concepts/lean-canvas.md) — Maurya; startup-adapted BMC
- [Value Proposition Canvas](concepts/value-proposition-canvas.md) — Osterwalder; pain/gain → product fit

### Metrics & prioritization
- [Outcomes vs outputs](concepts/outcomes-vs-outputs.md) — the single most-violated rule
- [Pirate Metrics (AARRR)](concepts/pirate-metrics.md) — funnel: acquisition → activation → retention → revenue → referral
- [RARRA (retention-first)](concepts/rarra.md) — modern reordering of AARRR
- [Cohort analysis](concepts/cohort-analysis.md) — the only honest way to measure product health
- [Aha moment / Activation](concepts/aha-moment.md) — the highest-leverage discovery
- [Product-Market Fit (PMF)](concepts/pmf.md) — Sean Ellis test, retention curves, Andreessen
- [HEART framework](concepts/heart-framework.md) — Google's UX metrics system
- [RICE / ICE scoring](concepts/rice-ice.md) — coarse prioritization, tiebreaker only
- [Kano model](concepts/kano-model.md) — feature categories: basic, performance, excitement
- [OKRs (done right)](concepts/okrs.md) — outcome-shaped goals; most-misused framework

### Roles & teams
- [Empowered product team](concepts/empowered-team.md) — Cagan's PM/Design/Eng trio
- [Strong PM](concepts/strong-pm.md) — the skill profile that makes discovery work
- [Feature team vs product team](concepts/feature-vs-product-team.md) — output factory vs outcome owner

### Behavior & habit
- [Hooked](concepts/hooked.md) — Eyal's habit-forming product loop (trigger → action → variable reward → investment)

### Anti-patterns
- [Build trap](concepts/build-trap.md) — Perri's diagnostic for output-obsessed orgs
- [Feature factory](concepts/feature-factory.md) — shipping features as the goal
- [Vanity metrics](concepts/vanity-metrics.md) — numbers that look good and tell you nothing
- [HiPPO decisions](concepts/hippo.md) — highest-paid person's opinion overrides evidence
- [Roadmap-as-commitment](concepts/roadmap-trap.md) — dates over outcomes
- [Solutioning in interviews](concepts/solutioning-trap.md) — asking users what to build

---

## Reading order (if new)

1. [Outcomes vs outputs](concepts/outcomes-vs-outputs.md) — the philosophical prerequisite
2. [Cagan's four risks](concepts/cagan-four-risks.md) — what discovery is *for*
3. [Build trap](concepts/build-trap.md) — what discovery is *against*
4. [Mom Test](concepts/mom-test.md) — how to talk to users honestly
5. [Dual Track Agile](concepts/dual-track-agile.md) — when discovery happens
6. [Opportunity Solution Tree](concepts/opportunity-solution-tree.md) — the artifact that ties it together
7. [Continuous Discovery](concepts/continuous-discovery.md) — the cadence that keeps the tree alive
8. [Assumption mapping](concepts/assumption-mapping.md) + [RAT](concepts/rat.md) — what to test first
9. [Prototyping](concepts/prototyping.md) + [Five-second test](concepts/five-second-test.md) — how to test cheaply
10. [Pirate Metrics](concepts/pirate-metrics.md) + [Cohort analysis](concepts/cohort-analysis.md) — measuring whether it worked

---

## Reading order (if practitioner)

You've read *Inspired*, *Continuous Discovery Habits*, and a few others. Higher-leverage paths:

- **Strategy layer** → [Product strategy](concepts/product-strategy.md) → [Wardley Mapping](concepts/wardley-mapping.md) → [PR/FAQ](concepts/pr-faq.md)
- **Quantitative literacy** → [A/B testing](concepts/ab-testing.md) → [Cohort analysis](concepts/cohort-analysis.md) → [Innovation Accounting](concepts/innovation-accounting.md) → [Vanity metrics](concepts/vanity-metrics.md)
- **PMF & retention** → [PMF](concepts/pmf.md) → [Aha moment](concepts/aha-moment.md) → [Hooked](concepts/hooked.md) → [RARRA](concepts/rarra.md)
- **Decision-making under uncertainty** → [Cynefin](concepts/cynefin.md) → [Lean Startup](concepts/lean-startup.md) → [RAT](concepts/rat.md)
- **JTBD depth** → [JTBD](concepts/jobs-to-be-done.md) → [ODI](concepts/odi.md) → [Value Proposition Canvas](concepts/value-proposition-canvas.md)
- **Alternative methodologies** → [Shape Up](concepts/shape-up.md) → [Lean UX](concepts/lean-ux.md) → [Customer Development](concepts/customer-development.md)
- **Strategic canvases** → [BMC](concepts/business-model-canvas.md) → [Lean Canvas](concepts/lean-canvas.md) → [VP Canvas](concepts/value-proposition-canvas.md)
- **Anti-pattern diagnosis** → [Build trap](concepts/build-trap.md) → [Feature factory](concepts/feature-factory.md) → [HiPPO](concepts/hippo.md) → [Roadmap trap](concepts/roadmap-trap.md)

---

## Canonical sources

### Core (read first)
- **Inspired**, **Empowered**, **Transformed** — Marty Cagan (SVPG)
- **Continuous Discovery Habits** — Teresa Torres
- **Escaping the Build Trap** — Melissa Perri
- **The Mom Test** — Rob Fitzpatrick (under 150 pages, outsized impact)

### Methodology
- **The Lean Startup** — Eric Ries
- **The Four Steps to the Epiphany** + **Startup Owner's Manual** — Steve Blank
- **Lean UX** — Jeff Gothelf & Josh Seiden
- **Sprint** — Jake Knapp
- **Shape Up** — Ryan Singer (free at basecamp.com/shapeup)
- **Running Lean** — Ash Maurya

### Frameworks & canvases
- **Business Model Generation** — Alex Osterwalder
- **Value Proposition Design** — Osterwalder
- **Testing Business Ideas** — David Bland & Osterwalder
- **Wardley Maps** — Simon Wardley (free)

### Jobs & users
- **Competing Against Luck** — Clayton Christensen (JTBD narrative)
- **What Customers Want** + **Jobs To Be Done: Theory to Practice** — Tony Ulwick (ODI)
- **User Story Mapping** — Jeff Patton

### Behavior, growth, habit
- **Hooked** + **Indistractable** — Nir Eyal
- **The Loyalty Effect** + **The Ultimate Question** — Fred Reichheld

### Strategy
- **Good Strategy / Bad Strategy** — Richard Rumelt
- **Play Bigger** — Christopher Lochhead (category design)
- **Measure What Matters** — John Doerr (OKRs)

### Decision-making
- **Cynefin: Weaving Sense-Making into the Fabric of Our World** — Dave Snowden
- **Working Backwards** — Colin Bryar & Bill Carr (Amazon PR/FAQ)

## Glossary

See [glossary.md](glossary.md) for one-line definitions of every term used across the wiki.
