# Wardley Mapping

> Source: Simon Wardley (CTO at Fotango, then LEF), 2005-present. Wardley's *Wardley Maps* (free online) is the canonical text. Strategic-positioning visualization adjacent to product discovery — answers "what should we build vs buy vs commodify?"

## The map

```
   VISIBLE
   to user
       │
       │  user (e.g. shopper)
       │     │
       │     ▼
       │   need (e.g. checkout)
       │     │
       │     ▼
       │   ┌─ product/service
       │   │
       │   ▼
       │   payment processing
       │     │
       │     ▼
       │   compute / database
       │     │
       │     ▼
       │   power
   INVISIBLE
   ────────────────────────────────────→ EVOLUTION
   Genesis    Custom    Product    Commodity/Utility
   ─────       ──────     ───────    ───────────────
   novel       built       multiple   well-understood
   uncertain   in-house    vendors    cheap, ubiquitous
```

Two axes:
- **Vertical (visibility)** — how visible to the user. Top = direct user-facing. Bottom = invisible infrastructure.
- **Horizontal (evolution)** — how mature the component is. Left = novel/uncertain. Right = commoditized/utility.

Components are nodes; dependencies are arrows.

## The four evolution stages

| Stage | Properties | Examples (2026) |
|---|---|---|
| **Genesis** | Novel, uncertain, R&D-heavy, no shared definition | quantum-error-corrected compute |
| **Custom-built** | Built in-house, expensive, bespoke | early enterprise AI agents |
| **Product** | Multiple vendors, differentiated, marketable | most SaaS today |
| **Commodity / Utility** | Standardized, cheap, undifferentiated | electricity, S3-compatible storage, LLM inference |

Components **always** evolve left → right. Never reverse. The pace varies, but the direction is fixed.

## Why this matters for product discovery

Different stages need different strategy:

| Stage | Right strategy | Wrong strategy |
|---|---|---|
| Genesis | Experiment, research, prototype | Mass-produce |
| Custom | Build internally, learn what's possible | Buy off shelf (none exists) |
| Product | Use vendors, differentiate above the layer | Build from scratch |
| Commodity | Buy / use utility, focus differentiation elsewhere | Build custom version |

Most product strategy mistakes are stage-mismatched: building custom what's commoditized (waste), or buying off-shelf what's still genesis (no shelf to buy from).

## Worked example

A new SaaS startup considering "build our own LLM" (2026):

```
LLM inference is currently:
  Stage: late Product, early Commodity
  
Building your own:
  Mismatch: commodity-stage components shouldn't be custom-built
  Cost: 1000x more to train from scratch than to use OpenAI/Anthropic API
  Differentiation: zero (everyone can build the same model with the same data)

Right move: use commoditized inference, differentiate at the application layer
```

Wardley's framing surfaces this directly. Without it, founders argue about whether to build or buy without a model for *why*.

## The doctrine and gameplay

Wardley extends the map with two layers of strategic moves:

**Doctrine** — universal rules that apply to all maps:
- Focus on user need
- Use a common language (the map)
- Challenge assumptions
- Remove duplication and bias
- Use appropriate methods at each stage

**Gameplay** — strategic moves you can make on the map:
- **Pioneer** — build genesis-stage components (high-risk, high-reward)
- **Settler** — productize custom components (turn 1-off into product)
- **Town planner** — commoditize products into utilities (efficiency play)
- **Standards play** — push for an open standard at a specific stage
- **Inertia** — deliberately slow a competitor's evolution

Plus ~60 named moves (Wardley catalogues them). Most product orgs only use the map; the doctrine + gameplay are advanced.

## Where Wardley intersects discovery

- **Above the discovery layer** — Wardley maps inform *which problems* are worth solving (genesis ones), not *how* to solve them
- **Build/buy decisions** — feeds into the [feasibility](cagan-four-risks.md) and [viability](cagan-four-risks.md) risk assessment
- **Strategy → outcomes** — Wardley clarifies *why* certain outcomes matter strategically; [OST](opportunity-solution-tree.md) figures out how to move them
- **PMs without strategy** — most product teams operate without strategic frame. Wardley fills the gap above PM-level discovery.

## Common failure modes

- **Pretty maps, no decisions** — drawing the map is easy; using it to kill or pursue work is the point
- **Static map** — maps are time-anchored. Re-draw quarterly.
- **Treating map as truth** — it's a model. Components' evolution stage is judgment-call.
- **Skipping the user need** — bottom-up technology maps, not top-down user-need maps. Top of the map should always be a user need.
- **Overusing it** — Wardley is high-context. Most teams need [outcomes](outcomes-vs-outputs.md) before they need maps.

## When to use Wardley

✅ Strategic planning (annual / quarterly leadership)
✅ Build vs buy vs use-utility decisions
✅ New-market entry analysis
✅ Competitive positioning

## When not to

❌ Day-to-day product discovery (overkill)
❌ Tactical feature decisions
❌ Teams not yet at outcome-thinking maturity (start there first)

## See also

- [Cagan's four risks](cagan-four-risks.md) — Wardley informs feasibility/viability inputs
- [Outcomes vs outputs](outcomes-vs-outputs.md) — Wardley sits *above* outcomes, informing which outcomes are strategic
- [Build trap](build-trap.md) — Wardley's "doctrine" includes "remove duplication" — a cure for build-trap output proliferation
