# Team Topologies

> Source: Matthew Skelton & Manuel Pais, *Team Topologies* (2019). Modern framework for designing software-org team structures. Operationalizes the [Inverse Conway Maneuver](conways-law.md). Replaces the older "Spotify model" as the canonical scaling reference.

## The four team types

```
┌──────────────────────────┬──────────────────────────────────┐
│ STREAM-ALIGNED           │ Default team type                │
│                          │ Owns end-to-end value stream     │
│                          │ Most teams should be this        │
├──────────────────────────┼──────────────────────────────────┤
│ ENABLING                 │ Helps stream-aligned teams       │
│                          │ Temporary engagement              │
│                          │ Skill / technique transfer       │
├──────────────────────────┼──────────────────────────────────┤
│ COMPLICATED-SUBSYSTEM    │ Owns specialized component       │
│                          │ Where deep expertise required    │
│                          │ E.g. crypto, DSP, ML core        │
├──────────────────────────┼──────────────────────────────────┤
│ PLATFORM                 │ Builds internal-product platform │
│                          │ Used by stream-aligned teams     │
│                          │ Internal users; "X as a service" │
└──────────────────────────┴──────────────────────────────────┘
```

Most orgs need only stream-aligned + platform. Enabling and complicated-subsystem are specialized.

### 1. Stream-aligned team
- Owns a value stream end-to-end (a customer-facing product, a feature area, a workflow)
- Has the trio: PM, design, engineering
- Empowered to discover and deliver
- Default team type — most teams in a healthy org are stream-aligned

This maps directly onto Cagan's [empowered team](empowered-team.md).

### 2. Enabling team
- Coaches and capability-spreads other teams
- Members are experts in some practice (testing, accessibility, security, ML ops)
- Engagement is *temporary* (3-6 months with a stream-aligned team), not permanent
- Goal: leave the stream-aligned team self-sufficient

### 3. Complicated-subsystem team
- Owns a piece of the system requiring deep specialist knowledge
- E.g. real-time video codec, ML inference pipeline, cryptographic library
- Justified only when expertise is rare and depth is unavoidable
- Should be small (3-5 people), tightly bounded interface

### 4. Platform team
- Builds and operates internal platforms used by stream-aligned teams
- Users are *other engineers*, not external customers
- Treats internal services as products — including discovery, support, documentation
- Reduces cognitive load on stream-aligned teams

## The three interaction modes

How teams interact matters as much as how they're structured. Three modes:

### 1. Collaboration
Two teams work closely together. High bandwidth, frequent meetings, shared decisions.

When: discovering new patterns, building a new product, novel territory.
Cost: high coordination overhead.
Should be *temporary* — when the territory becomes known, switch to "X-as-a-service."

### 2. X-as-a-Service
One team consumes a service from another team via well-defined interface.

When: known territory, established patterns, clear contracts.
Cost: low — the consumer team operates without daily coordination.
Should be the default when possible. Most platform-team interactions.

### 3. Facilitating
Enabling team coaches/teaches another team for a defined period.

When: spreading a new capability (e.g. test automation, performance optimization).
Cost: low to moderate.
Has a defined end — the engagement concludes when the receiving team is self-sufficient.

## Cognitive load

The book's most-original contribution. Each team has a finite **cognitive load capacity**. Loads come in three types:

- **Intrinsic** — fundamental complexity of the task domain (you can't reduce; you can only allocate)
- **Extraneous** — environment / tooling / process complexity (you can reduce; this is the platform team's job)
- **Germane** — specific knowledge to do the work (you can pay down via documentation, automation)

A team beyond cognitive capacity:
- Misses things, has incidents
- Resists change because every change costs scarce attention
- Over-coordinates with neighbors (anxiety mitigation)
- Leaks scope; loses focus

The fix: reduce extraneous load (platform teams), bound intrinsic load (don't make stream-aligned teams own too much), pay down germane load (docs, training).

## Worked example: e-commerce company

Bad org (output-shaped, ignoring topology):

```
- Frontend team
- Backend team
- Database team
- DevOps team
- QA team
- Design team
```

Each team siloed by *function*, not by value stream. Every product change requires coordinating 6 teams. Cognitive load fragmented. Conway's law produces fragmented user experience.

Good org (topology-aligned):

```
Stream-aligned:
  - Checkout team (owns checkout UX, payment flow, order placement)
  - Catalog team (owns search, browse, product pages)
  - Returns team (owns return flow, refund logic)
  - Account team (owns auth, profile, preferences)

Platform:
  - Infrastructure team (Kubernetes, CI/CD, observability)
  - Data platform team (warehouse, ETL, analytics tools)
  - Identity platform team (auth-as-a-service)

Complicated-subsystem:
  - Recommendations team (ML models, ranking)

Enabling:
  - Performance enabling team (rotates through stream-aligned teams)
  - Accessibility enabling team
```

Each stream-aligned team owns its value stream end-to-end. Platform teams reduce extraneous load. Conway's law now produces clean ownership boundaries in the architecture.

## Why this beat the Spotify model

The Spotify model (squads/tribes/chapters/guilds) was famously published in 2012, widely copied — and largely failed at the companies that adopted it. Why:
- Spotify itself didn't fully follow the model
- It described an internal aspiration, not a working system
- Lacked clear interaction patterns
- Conflated org chart with operating model

Team Topologies addresses these gaps:
- Defines team types by *purpose*, not by ceremony
- Specifies interaction modes explicitly
- Builds in cognitive-load thinking
- Doesn't require imitating any specific company

It's the more rigorous successor.

## Implementing it

Skelton/Pais's prescription, simplified:

1. **Map current state** — what teams exist? What do they own? How do they interact?
2. **Identify cognitive overload** — which teams are stretched thin or constantly firefighting?
3. **Identify Conway misalignment** — where does architecture force teams to coordinate constantly?
4. **Design target topology** — what stream-aligned teams, platforms, etc. would the system need?
5. **Sequence the changes** — multi-quarter; rarely a single big-bang reorg
6. **Establish interaction protocols** — explicit X-as-a-service contracts between teams
7. **Track team health** — cognitive load, internal NPS, value-stream metrics

## Connection to other concepts

| Concept | Relationship |
|---|---|
| [Conway's Law](conways-law.md) | Topology is the deliberate Conway maneuver |
| [Empowered team](empowered-team.md) | Stream-aligned teams *are* empowered teams |
| [Product Operating Model](product-operating-model.md) | Topology is the team-shape layer of the operating model |
| [Cynefin](cynefin.md) | Different team types fit different domains; complicated-subsystem fits the Complicated domain, stream-aligned fits Complex |

## Common failure modes

- **Renaming without redesigning** — rebrand existing teams as "stream-aligned" without changing ownership; nothing actually changes
- **Too many platform teams** — building platforms for things that should be in stream-aligned teams; overhead explodes
- **No cognitive-load measurement** — teams keep getting more responsibilities; overload is invisible until incidents
- **Permanent collaboration mode** — "we just always work closely with that team" — should be either X-as-a-service (less coupling) or merged (one team)
- **Enabling team becomes permanent** — should be temporary; if engagement never ends, the receiving team isn't actually learning
- **Skipping interaction-mode design** — teams know who they are but not how they work together; coordination ad-hoc

## See also

- [Conway's Law](concepts/conways-law.md) — the underlying observation
- [Product Operating Model](concepts/product-operating-model.md) — the broader org-level frame
- [Empowered team](concepts/empowered-team.md) — stream-aligned team unit
- [Cynefin](concepts/cynefin.md) — domain-fit reasoning for team types
