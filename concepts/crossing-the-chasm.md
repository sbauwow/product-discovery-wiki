# Crossing the Chasm

> Sources: Everett Rogers, *Diffusion of Innovations* (1962) for the underlying tech adoption lifecycle. Geoffrey Moore, *Crossing the Chasm* (1991) for the chasm framing. Foundational for B2B and disruptive product launches.

## The Tech Adoption Lifecycle (Rogers)

Five segments adopt new technology in distinct phases:

```
                    ┌─────────────────────────┐
                    │                          │
          ┌─────────┤      EARLY MAJORITY      │─────────┐
          │         │      "pragmatists"       │         │
          │         └──────────────────────────┘         │
          │                                              │
   ┌──────┴───┐                                    ┌─────┴────┐
   │  EARLY   │                                    │   LATE   │
   │ ADOPTERS │           DIFFUSION                │ MAJORITY │
   │ "vision- │                                    │ "conserv-│
   │  aries"  │                                    │  atives" │
   └─────┬────┘                                    └─────┬────┘
         │                                               │
         │      ┌──────────────────┐                     │
   ┌─────┴──┐   │                   │              ┌────┴─────┐
   │INNOVATORS  │     ROGERS' CURVE  │              │LAGGARDS  │
   │"techies"   │  (bell-shaped)     │              │"skeptics"│
   └────────┘   └────────────────────┘              └──────────┘
   
   2.5%      13.5%        34%             34%            16%
```

Each segment has different motivations:
- **Innovators (2.5%)** — love new tech for its own sake; try anything
- **Early adopters (13.5%)** — visionaries; willing to bet on early products for competitive advantage
- **Early majority (34%)** — pragmatists; want proven, well-supported products
- **Late majority (34%)** — conservatives; want everyone else to have proven it first
- **Laggards (16%)** — skeptics; adopt only when forced

## Moore's chasm

Moore's insight (1991): there's a **gap** between early adopters and the early majority. Most tech products die in this gap because the two segments want fundamentally different things.

```
INNOVATORS │ EARLY ADOPTERS │ ── CHASM ── │ EARLY MAJORITY │ LATE MAJ │ LAGGARDS
techies      visionaries                    pragmatists       conservatives
                            ↑
                  this is where most products die
```

| Early adopters want | Early majority wants |
|---|---|
| Cutting-edge tech | Proven solutions |
| Competitive advantage | Risk reduction |
| Custom configuration | Standardized, supported |
| Direct relationship with vendor | Whole product (vendor + ecosystem) |
| Tolerate bugs / rough edges | Demand polish |
| Buy on vision | Buy on references |
| Few in number | Many in number |

A startup that's been winning with visionary buyers suddenly hits a wall: the next group won't buy.

## Why the chasm is real

The early majority is **rationally** waiting:
- They've been burned by early adopters' enthusiasm before
- They want to see *similar* companies use it successfully
- They want a complete solution (product + integrations + support + community)
- Their reference is *each other*, not visionaries

Early adopter testimonials don't count. Pragmatists trust other pragmatists.

The result: a startup with 50 enthusiastic early adopters often can't sell deal #51 to a pragmatist.

## Moore's "beachhead" / D-Day strategy

To cross the chasm:

```
1. Pick ONE niche segment of the early majority
2. Build the complete "whole product" for them
   (not just core; integrations, partnerships, support)
3. Become the dominant solution in that niche
4. Use that beachhead's references to invade adjacent niches
5. Expand outward — niche by niche
```

Pick the niche by:
- **Pain** — segment with severe, undeniable pain
- **Reachability** — easy to find, market to, sell to
- **Reference value** — winning here gives credibility for next segment
- **Whole-product feasibility** — you can build the complete solution for *them* without expanding to "everyone"

Worked example: **Salesforce** beachhead = small/mid sales teams (15-100 reps). Built complete solution for them (CRM + workflow + reports + community). Dominated. Then moved to enterprise. Then to platform.

## "Whole product" gap

Early adopters buy a **product**.
Pragmatists buy a **whole product**:

```
WHOLE PRODUCT (what pragmatists actually buy)
┌────────────────────────────────────┐
│ ┌─────────┐   ┌──────────────────┐ │
│ │ Product │   │ Integrations     │ │
│ │ (core)  │   │ Partner ecosystem│ │
│ └─────────┘   │ Training         │ │
│               │ Support          │ │
│               │ References       │ │
│               │ Best practices   │ │
│               │ Communities      │ │
│               │ Certifications   │ │
│               └──────────────────┘ │
└────────────────────────────────────┘
```

The gap between core product and whole product is what kills chasm-crossers. Building "the complete product" for one niche is the discipline.

## Diffusion math

Per Rogers, adoption follows an **S-curve**:

```
Cumulative adoption
       │
  100% │              ───────────  saturation
       │            ╱
       │          ╱
       │        ╱  ← steepest slope: early + late majority
       │       │
       │     ╱
       │    │
       │   ╱  ← chasm period: slow growth, easy to mistake for failure
       │  │
       │ ╱
       │╱  ← innovators + early adopters
       └─────────────────────────────→ time
```

Time across the chasm can be 1-3 years for B2B products. Many startups die there because growth slows and runway runs out.

## How to know which side of the chasm you're on

Signs you're still selling to early adopters:
- Customers are visionary individuals (CTO, CEO, head of innovation)
- Each deal is custom; little repeatability
- Buyers cite "competitive advantage" or "transformation"
- You build heavily for each customer
- Few customers can articulate what makes the product good *for businesses like theirs*

Signs you've crossed:
- Customers are department heads / functional buyers
- Sales cycles repeat; playbook works
- Buyers cite "industry standard" or "everyone our size uses it"
- Whole-product ecosystem exists (training, partners, community)
- Customers refer to *each other*, not to you

## Connection to other concepts

| Concept | Relationship |
|---|---|
| [PMF](pmf.md) | First PMF is usually with early adopters; the chasm is "PMF with the next segment" |
| [Cold-start problem](cold-start-problem.md) | Local atomic network ≈ beachhead within a niche |
| [Disruption theory](disruption-theory.md) | Disruptive products sometimes skip the chasm by addressing nonconsumers |
| [JTBD](jobs-to-be-done.md) | Different segments hire products for different jobs; beachhead JTBD ≠ visionary JTBD |
| [Wardley Mapping](wardley-mapping.md) | Crossing the chasm = a component moving from custom-built → product evolution stage |

## When the chasm framing matters

✅ B2B SaaS, enterprise tech, developer tools
✅ Hardware with adoption requirements (e.g. EVs, IoT)
✅ Complex / regulated tech (medical, fintech, edtech)
✅ Platform-shift products (mobile-first, AI-native, etc.)

## When it matters less

❌ Pure consumer apps with low switching cost (TikTok didn't need to "cross a chasm" — it expanded virally without segment gating)
❌ Commodity products with established demand (e-commerce within a known category)
❌ Niche tools with no mass-market intent

## Common failure modes

- **Skipping the niche** — trying to sell to "everyone" the moment early-adopter sales succeed; spread too thin to dominate any segment
- **Confusing visionary references with pragmatist references** — pragmatists ignore visionary testimonials
- **No whole product** — selling core product when pragmatists want whole product
- **Premature platform play** — trying to be a horizontal platform before dominating a beachhead vertical
- **Mistaking slow growth for failure** — the chasm period naturally has slower growth; killing the product here is the most expensive mistake

## See also

- [PMF](concepts/pmf.md) — segment-specific PMF; chasm = next-segment PMF problem
- [Cold-start problem](concepts/cold-start-problem.md) — atomic network ≈ beachhead concept
- [Disruption theory](concepts/disruption-theory.md) — alternative path to mass market
- [Customer Development](concepts/customer-development.md) — Blank's segment validation maps onto chasm staging
- [Network effects](concepts/network-effects.md) — strong network effects can change chasm dynamics dramatically
