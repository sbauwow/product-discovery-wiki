# Cynefin Framework

> Source: Dave Snowden, IBM Knowledge Management, 1999. Pronounced "kuh-NEV-in" (Welsh for "habitat"). Sense-making framework for decision-making under different types of uncertainty. Underused in product, very useful.

## The five domains

```
                          COMPLEX
                  ┌───────────────────┐
                  │                   │
                  │  Probe →           │
                  │   Sense →          │
                  │    Respond         │
                  │                   │
                  │ "emergent"         │
                  ├───────────────────┤
                  │                   │
                  │   COMPLICATED      │
                  │                   │
                  │  Sense →           │
                  │   Analyse →        │
                  │    Respond         │
                  │                   │
                  │ "good practice"    │
   ───────────────┼───────────────────┼────────────────
                  │                   │
                  │     CHAOTIC        │
                  │                   │
                  │  Act →             │
                  │   Sense →          │
                  │    Respond         │
                  │                   │
                  │ "novel practice"   │
                  ├───────────────────┤
                  │                   │
                  │     CLEAR          │
                  │     (Obvious)      │
                  │  Sense →           │
                  │   Categorise →     │
                  │    Respond         │
                  │                   │
                  │ "best practice"    │
                  └───────────────────┘
                  
                  At the center: DISORDER
                  (we don't know which domain we're in)
```

## The five domains in detail

### Clear (formerly "Simple", "Obvious")
Cause and effect are obvious. Best practice exists.
- Approach: **Sense → Categorise → Respond**
- Example: a payment failed because the card expired → re-prompt for card
- Product application: rare in discovery; common in support runbooks, onboarding flows

### Complicated
Cause and effect knowable, but requires expertise.
- Approach: **Sense → Analyse → Respond**
- Example: scaling a database under load → architect knows how, requires analysis
- Product application: feasibility spikes, performance optimization, technical migrations
- "Good practice" exists but not "best practice" (multiple expert opinions valid)

### Complex
Cause and effect only knowable in retrospect. The system reacts to interventions in unpredictable ways.
- Approach: **Probe → Sense → Respond** (run safe-to-fail experiments)
- Example: will users adopt this new feature? — can't be analyzed, only tested
- Product application: **most product discovery lives here**
- Patterns emerge from experiments; no "right answer" exists in advance

### Chaotic
No discernible cause and effect. Crisis mode.
- Approach: **Act → Sense → Respond** (do something, anything, to stabilize)
- Example: production outage during peak traffic → roll back first, diagnose later
- Product application: PR crisis, severe outage, security incident
- Goal is to escape chaos to complex (where you can experiment) or complicated (where you can analyze)

### Disorder
You don't know which domain you're in. Default state when first encountering a problem.
- Approach: **Break the problem into parts; assess each**
- Most "we're stuck in meetings" situations are disorder, mistaken for complex

## Why Cynefin matters for product

The framework's central claim: **different domains require different approaches.** The error is using one approach in the wrong domain.

| Domain | Right tool | Common product wrong tool |
|---|---|---|
| Clear | SOP, automation | Discovery process (overkill) |
| Complicated | Expert analysis, planning | Lean Startup MVP (insufficient analysis) |
| Complex | Experiments, [continuous discovery](continuous-discovery.md) | Detailed planning ([roadmap trap](roadmap-trap.md)) |
| Chaotic | Quick action, stabilize | Discovery (no time) |
| Disorder | Decompose, diagnose | Treating it as complex by default |

## The most common product mistake

Treating **complex** problems as **complicated** ones.

```
Stakeholder: "We need to decide what to build for Q3."
Product team: builds detailed plan, estimates, Gantt chart, commitments

Reality: which features will work is COMPLEX (only knowable through experiments).
The plan is theater. It will be wrong, blamed on execution, and cycle repeats.
```

The fix is recognizing the domain. Complex problems require **safe-to-fail experiments**, not plans. This is the philosophical foundation of [Lean Startup](lean-startup.md) and [continuous discovery](continuous-discovery.md), even if those frameworks don't cite Cynefin.

## Domain transitions

Real problems often span domains:
- A complex problem (will users adopt?) becomes complicated once validated (now scale it)
- A complicated problem (architecture rewrite) can flip to chaotic (production outage)
- A complex problem can collapse to clear (we now know exactly how onboarding should work, just execute)

A team's job is partly to *recognize the transition* and switch approach.

## Snowden's "safe-to-fail experiments"

In the complex domain, run multiple small experiments simultaneously. Each:
- **Safe to fail** — failure doesn't sink the org
- **Coherent** — has a plausible mechanism for why it might work
- **Detectable** — measurable signal (positive or negative)
- **Diverse** — try different theories at once

Sounds exactly like [assumption mapping](assumption-mapping.md) + parallel experiments on an [OST](opportunity-solution-tree.md). The vocabulary differs; the discipline is the same.

## Common misuses

- **Cynefin as taxonomy** — used to label problems, never used to *change approach*
- **"Complex" as excuse** — used to avoid rigor ("it's complex, can't plan")
- **Confusing complex and complicated** — the most common error
- **Skipping disorder** — pretending you know which domain you're in

## When to invoke Cynefin

- A team is stuck and arguing about *how* to approach a problem
- Stakeholders demand certainty in a complex domain
- Diagnosing why "best practice" isn't working
- Deciding whether to plan or experiment

Less useful in day-to-day execution; very useful as a meta-framework when teams disagree about method.

## See also

- [Lean Startup](concepts/lean-startup.md) — the build-measure-learn loop is Snowden's "probe-sense-respond"
- [Assumption mapping](concepts/assumption-mapping.md) — the practical tool for complex-domain experiments
- [Roadmap trap](concepts/roadmap-trap.md) — what happens when complex problems are mis-treated as complicated
