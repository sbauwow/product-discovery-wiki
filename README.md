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
- [Disruption theory](concepts/disruption-theory.md) — Christensen; why incumbents lose to inferior-looking entrants
- [Crossing the Chasm](concepts/crossing-the-chasm.md) — Moore + Rogers; the gap between early adopters and mainstream
- [Blue Ocean Strategy](concepts/blue-ocean.md) — Kim/Mauborgne; create uncontested market space via ERRC
- [7 Powers](concepts/seven-powers.md) — Helmer; rigorous taxonomy of strategic moats / defensibility
- [Three Horizons](concepts/three-horizons.md) — McKinsey; portfolio innovation framework
- [North Star Framework](concepts/north-star.md) — one outcome metric anchoring strategy
- [PR/FAQ (Working Backwards)](concepts/pr-faq.md) — Amazon's press-release-first method
- [PRD vs One-pager](concepts/prd.md) — Cagan's argument for short specs over long PRDs
- [Pricing](concepts/pricing.md) — value-based, Van Westendorp PSM, freemium, B2B
- [ICP, Segmentation, and Beachhead Market](concepts/icp-segmentation.md) — who exactly to serve first, and who not to
- [Competitive Analysis and Positioning](concepts/competitive-analysis-positioning.md) — how to think about alternatives, differentiation, and the comparison frame buyers use

### Frameworks (how to organize discovery)
- [Dual Track Agile](concepts/dual-track-agile.md) — discovery and delivery as parallel tracks within one team
- [Discovery Operating Loop](concepts/discovery-operating-loop.md) — the practical spine connecting strategy, evidence, experiments, delivery, measurement, and decisions
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

### Practical workflows (how to actually run discovery)
- [Discovery Operating Loop](concepts/discovery-operating-loop.md) — the end-to-end operating spine for discovery work
- [ICP, Segmentation, and Beachhead Market](concepts/icp-segmentation.md) — choose who to serve first
- [Competitive Analysis and Positioning](concepts/competitive-analysis-positioning.md) — define alternatives and comparison frame
- [Voice of Customer (VoC) Systems](concepts/voc-systems.md) — turn support, sales, churn, and surveys into signal flow
- [Research Synthesis](concepts/research-synthesis.md) — convert raw evidence into patterns, insights, and opportunities
- [Experiment Design](concepts/experiment-design.md) — design tests with explicit success, failure, and decision rules
- [Tracking Plans and Instrumentation](concepts/tracking-plans-instrumentation.md) — make funnels, cohorts, and experiments trustworthy
- [Churn and Retention Diagnosis](concepts/churn-retention-diagnosis.md) — explain who leaves, when, and why

### Methods (how to generate insight)
- [Jobs To Be Done (JTBD)](concepts/jobs-to-be-done.md) — users hire products to do jobs
- [Research Synthesis](concepts/research-synthesis.md) — how raw notes and observations become patterns, insights, and opportunities
- [Outcome-Driven Innovation (ODI)](concepts/odi.md) — Ulwick; quantitative cousin to JTBD
- [User interviews](concepts/user-interviews.md) — past-behavior probes, not opinion polls
- [The Mom Test](concepts/mom-test.md) — Fitzpatrick; three-rule discipline for honest interviews
- [Empathy maps](concepts/empathy-map.md) — Says/Thinks/Does/Feels synthesis
- [Personas](concepts/personas.md) — composite users, with critique
- [Assumption mapping](concepts/assumption-mapping.md) — list, plot, test the riskiest
- [Riskiest Assumption Test (RAT)](concepts/rat.md) — sharper alternative to MVP
- [Premortem](concepts/premortem.md) — Klein; imagine failure; surface risks before they become real
- [Postmortem (blameless)](concepts/postmortem.md) — retrospective learning from incidents and bets
- [Experiment Design](concepts/experiment-design.md) — how to turn assumptions into tests with real decision value
- [Prototyping](concepts/prototyping.md) — feasibility, user, live-data, Wizard-of-Oz
- [Story mapping](concepts/story-mapping.md) — user journey as backbone, slices as releases
- [Customer journey maps](concepts/customer-journey-maps.md) — end-to-end experience across all touchpoints
- [Service blueprints](concepts/service-blueprint.md) — CJM extended with backstage operations

### User research toolbox (specific research methods)
- [Usability testing](concepts/usability-testing.md) — watch users attempt tasks; the canonical UX method
- [Voice of Customer (VoC) Systems](concepts/voc-systems.md) — operational customer-signal intake across support, sales, churn, and surveys
- [Ethnography & Contextual Inquiry](concepts/ethnography.md) — field observation; what users actually do
- [Diary studies](concepts/diary-studies.md) — longitudinal self-reporting across days/weeks
- [Five-second test](concepts/five-second-test.md) — quick clarity / value-prop check
- [Card sorting](concepts/card-sorting.md) — generate IA from user mental models
- [Tree testing](concepts/tree-testing.md) — validate IA findability text-only
- [Surveys](concepts/surveys.md) — quant scale, with design-discipline caveats
- [Heuristic evaluation](concepts/heuristic-evaluation.md) — Nielsen's 10; expert review without users
- [Power user analysis](concepts/power-user-analysis.md) — Bangaly Kaba; study most-engaged users to find what works
- [A/B testing](concepts/ab-testing.md) — quantitative validation via random assignment
- [Multivariate testing & Bayesian A/B](concepts/multivariate-testing.md) — beyond standard A/B

### Strategic canvases & artifacts
- [Business Model Canvas](concepts/business-model-canvas.md) — Osterwalder; nine-block business model viz
- [Lean Canvas](concepts/lean-canvas.md) — Maurya; startup-adapted BMC
- [Value Proposition Canvas](concepts/value-proposition-canvas.md) — Osterwalder; pain/gain → product fit

### Metrics & prioritization
- [Outcomes vs outputs](concepts/outcomes-vs-outputs.md) — the single most-violated rule
- [Tracking Plans and Instrumentation](concepts/tracking-plans-instrumentation.md) — the measurement layer that makes funnels, cohorts, and experiments trustworthy
- [Pirate Metrics (AARRR)](concepts/pirate-metrics.md) — funnel: acquisition → activation → retention → revenue → referral
- [RARRA (retention-first)](concepts/rarra.md) — modern reordering of AARRR
- [Funnel analysis](concepts/funnel-analysis.md) — analytical method for finding step-by-step drop-offs
- [Cohort analysis](concepts/cohort-analysis.md) — the only honest way to measure product health
- [Aha moment / Activation](concepts/aha-moment.md) — the highest-leverage discovery
- [Churn and Retention Diagnosis](concepts/churn-retention-diagnosis.md) — how to explain who leaves, when, and why, rather than just reporting churn %
- [Product-Market Fit (PMF)](concepts/pmf.md) — Sean Ellis test, retention curves, Andreessen
- [HEART framework](concepts/heart-framework.md) — Google's UX metrics system
- [RICE / ICE scoring](concepts/rice-ice.md) — coarse prioritization, tiebreaker only
- [Kano model](concepts/kano-model.md) — feature categories: basic, performance, excitement
- [OKRs (done right)](concepts/okrs.md) — outcome-shaped goals; most-misused framework

### Growth & adoption
- [Growth loops](concepts/growth-loops.md) — Balfour/Reforge; compounding cycles vs leaky funnels
- [Network effects](concepts/network-effects.md) — Hoffman/NFX; the most defensible moat in software
- [Cold-start problem](concepts/cold-start-problem.md) — Andrew Chen; bootstrapping a network from zero
- [Product-Led Growth (PLG)](concepts/product-led-growth.md) — Wes Bush; the modern B2B SaaS motion
- [Onboarding patterns](concepts/onboarding-patterns.md) — FTUX patterns: empty states, tours, milestones, magic moment

### Roles, teams, & operating model
- [Empowered product team](concepts/empowered-team.md) — Cagan's PM/Design/Eng trio
- [Strong PM](concepts/strong-pm.md) — the skill profile that makes discovery work
- [Feature team vs product team](concepts/feature-vs-product-team.md) — output factory vs outcome owner
- [Product Operating Model](concepts/product-operating-model.md) — Cagan *Transformed*; org-level system for running product
- [Conway's Law](concepts/conways-law.md) — system architecture mirrors org structure; the inverse maneuver
- [Team Topologies](concepts/team-topologies.md) — Skelton/Pais; modern team-shape framework

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

## Start here if you're building a product team

Read in this order:
1. [Product strategy](concepts/product-strategy.md)
2. [Discovery Operating Loop](concepts/discovery-operating-loop.md)
3. [ICP, Segmentation, and Beachhead Market](concepts/icp-segmentation.md)
4. [Research Synthesis](concepts/research-synthesis.md)
5. [Experiment Design](concepts/experiment-design.md)
6. [Tracking Plans and Instrumentation](concepts/tracking-plans-instrumentation.md)
7. [Churn and Retention Diagnosis](concepts/churn-retention-diagnosis.md)

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

- **Practical discovery operating spine** → [Discovery Operating Loop](concepts/discovery-operating-loop.md) → [ICP / Segmentation](concepts/icp-segmentation.md) → [Research Synthesis](concepts/research-synthesis.md) → [Experiment Design](concepts/experiment-design.md) → [Tracking Plans & Instrumentation](concepts/tracking-plans-instrumentation.md) → [Churn / Retention Diagnosis](concepts/churn-retention-diagnosis.md)
- **Strategy layer** → [Product strategy](concepts/product-strategy.md) → [Wardley Mapping](concepts/wardley-mapping.md) → [PR/FAQ](concepts/pr-faq.md)
- **Quantitative literacy** → [A/B testing](concepts/ab-testing.md) → [Cohort analysis](concepts/cohort-analysis.md) → [Innovation Accounting](concepts/innovation-accounting.md) → [Vanity metrics](concepts/vanity-metrics.md)
- **PMF & retention** → [PMF](concepts/pmf.md) → [Aha moment](concepts/aha-moment.md) → [Hooked](concepts/hooked.md) → [RARRA](concepts/rarra.md)
- **Decision-making under uncertainty** → [Cynefin](concepts/cynefin.md) → [Lean Startup](concepts/lean-startup.md) → [RAT](concepts/rat.md)
- **JTBD depth** → [JTBD](concepts/jobs-to-be-done.md) → [ODI](concepts/odi.md) → [Value Proposition Canvas](concepts/value-proposition-canvas.md)
- **Alternative methodologies** → [Shape Up](concepts/shape-up.md) → [Lean UX](concepts/lean-ux.md) → [Customer Development](concepts/customer-development.md)
- **Strategic canvases** → [BMC](concepts/business-model-canvas.md) → [Lean Canvas](concepts/lean-canvas.md) → [VP Canvas](concepts/value-proposition-canvas.md)
- **Research method depth** → [Heuristic eval](concepts/heuristic-evaluation.md) → [Usability testing](concepts/usability-testing.md) → [Ethnography](concepts/ethnography.md) → [Diary studies](concepts/diary-studies.md) → [Surveys](concepts/surveys.md)
- **Information architecture** → [Card sorting](concepts/card-sorting.md) → [Tree testing](concepts/tree-testing.md) → [Usability testing](concepts/usability-testing.md)
- **Growth & adoption** → [Growth loops](concepts/growth-loops.md) → [Network effects](concepts/network-effects.md) → [Cold-start problem](concepts/cold-start-problem.md) → [PLG](concepts/product-led-growth.md)
- **Going to market** → [Crossing the Chasm](concepts/crossing-the-chasm.md) → [Disruption theory](concepts/disruption-theory.md) → [Pricing](concepts/pricing.md)
- **Specs that don't suck** → [PR/FAQ](concepts/pr-faq.md) → [PRD vs one-pager](concepts/prd.md) → [Now/Next/Later](concepts/now-next-later.md)
- **Risk surfacing** → [Premortem](concepts/premortem.md) → [Assumption mapping](concepts/assumption-mapping.md) → [RAT](concepts/rat.md)
- **Defensibility & moats** → [7 Powers](concepts/seven-powers.md) → [Network effects](concepts/network-effects.md) → [Disruption theory](concepts/disruption-theory.md) → [Blue Ocean](concepts/blue-ocean.md)
- **Org design at scale** → [Conway's Law](concepts/conways-law.md) → [Team Topologies](concepts/team-topologies.md) → [Product Operating Model](concepts/product-operating-model.md)
- **Innovation portfolio** → [Three Horizons](concepts/three-horizons.md) → [Innovation accounting](concepts/innovation-accounting.md) → [Disruption theory](concepts/disruption-theory.md)
- **Learning from outcomes** → [Premortem](concepts/premortem.md) → [Postmortem](concepts/postmortem.md) → [Innovation accounting](concepts/innovation-accounting.md)
- **Advanced quant** → [A/B testing](concepts/ab-testing.md) → [Multivariate / Bayesian](concepts/multivariate-testing.md) → [Power user analysis](concepts/power-user-analysis.md) → [Funnel analysis](concepts/funnel-analysis.md)
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
- **The Innovator's Dilemma** + **The Innovator's Solution** — Clayton Christensen (disruption)
- **Crossing the Chasm** — Geoffrey Moore
- **Diffusion of Innovations** — Everett Rogers
- **Blue Ocean Strategy** — W. Chan Kim & Renée Mauborgne
- **7 Powers** — Hamilton Helmer (defensibility/moats)
- **The Alchemy of Growth** — Baghai/Coley/White (Three Horizons)
- **Play Bigger** — Christopher Lochhead (category design)
- **Measure What Matters** — John Doerr (OKRs)

### Growth, adoption & monetization
- **The Cold Start Problem** — Andrew Chen
- **Product-Led Growth** — Wes Bush
- **Monetizing Innovation** — Madhavan Ramanujam (pricing)
- **The Lean Product Playbook** — Dan Olsen
- Reforge essays — Brian Balfour, Andrew Chen, Casey Winters (growth loops, retention)

### Decision-making & org design
- **Cynefin: Weaving Sense-Making into the Fabric of Our World** — Dave Snowden
- **Working Backwards** — Colin Bryar & Bill Carr (Amazon PR/FAQ)
- **Team Topologies** — Matthew Skelton & Manuel Pais
- **Site Reliability Engineering** — Google (blameless postmortems)
- **The Power of Intuition** / *Sources of Power* — Gary Klein (premortems, naturalistic decision-making)

## Glossary

See [glossary.md](glossary.md) for one-line definitions of every term used across the wiki.
