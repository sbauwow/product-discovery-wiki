# Shape Up

> Source: Ryan Singer, *Shape Up* (2019, free online at basecamp.com/shapeup). Basecamp's product methodology. A distinct alternative to scrum/sprint-based [agile](dual-track-agile.md).

## Core ideas

| Concept | Definition |
|---|---|
| **Shaping** | Pre-work where senior people define a problem + rough solution + appetite (time budget) |
| **Appetite** | How much time a problem is worth — not an estimate. "We'll spend 6 weeks on this, no more." |
| **Betting table** | Decision meeting; leadership picks shaped pitches to bet on next cycle |
| **6-week cycle** | One uninterrupted block of work; teams of 1–3 build a single shaped project |
| **Cool-down** | 2-week buffer between cycles — bug fixes, exploration, no scheduled work |
| **Hill chart** | Progress visualization replacing burndown; tracks "uphill = unknowns, downhill = execution" |
| **Circuit breaker** | If work overruns the appetite, project is killed, not extended |

## The cycle

```
6 weeks ────────────────────────  2 weeks ────────  6 weeks ────────
│ build cycle                   │ cool-down       │ next build cycle
│ shaped pitches → execute      │ no commitments   │ ...
└───────────────────────────────┴─────────────────┴────────────────
                                  ↑
                        betting table happens here
                        leadership picks next cycle's pitches
```

## Shaping (the discovery half)

A *shaped pitch* contains:
1. **Problem** — concrete, with example user/scenario
2. **Appetite** — small batch (1–2 weeks) or big batch (6 weeks)
3. **Solution** — rough sketches; "fat marker" level, not detailed
4. **Rabbit holes** — explicitly identified pitfalls
5. **No-gos** — out-of-scope items

Shaping is done by senior PMs/designers, NOT the building team. The team gets the pitch and figures out the details during the cycle.

## Hill chart

Replaces story-point burndown:

```
        ↑                          peak (figured out the unknowns)
  unknowns
        │              ┌────────●  
        │             /          \  
        │            /            \  
        │           /              \  ← downhill = just executing
        │          /                \  
        │         ●                  \  
        │  uphill                     \  
        │  (figuring out)              ●  done
        └────────────────────────────────→
              time
```

Each scope (a chunk of work) is a dot. Dots move left-to-right and up-to-down as work progresses. Tells you whether progress is "discovery" (uphill) or "execution" (downhill) — surface the difference burndowns hide.

## Why no backlog

Shape Up explicitly rejects the persistent backlog:
- Backlogs grow without bound
- Old items rot; revisiting them is overhead
- Most never get built; those that do have stale context

Instead: pitches die at the betting table if not picked. If a problem is real, it'll come back next cycle, freshly shaped.

## How it differs from scrum/agile

| Shape Up | Scrum |
|---|---|
| 6-week cycle | 1–2 week sprint |
| 1 project, no interruptions | Multiple stories, mid-sprint changes possible |
| Shaping precedes commitment | Backlog grooming inside sprints |
| Hill chart | Burndown |
| Circuit-breaker (kill on overrun) | Carry over to next sprint |
| Pitches die if not bet | Backlog persists |
| 1–3 person teams | 5–9 person teams |

## How it differs from [continuous discovery](continuous-discovery.md) / [dual-track](dual-track-agile.md)

| Shape Up | Cagan/Torres model |
|---|---|
| Discovery = shaping (upstream, by seniors) | Discovery = continuous, by team |
| Building team gets pitch | Building team participates in discovery |
| 6-week build commitment | Discovery output ≠ time commitment |
| Less customer interview cadence | Weekly customer touchpoints |
| Better fit: small, founder-led | Better fit: larger product orgs |

Both reject feature-factory thinking. Different mechanisms.

## When Shape Up works well

✅ Small org (10–50 product/eng)
✅ Founder/leadership has product judgment
✅ Single product or coherent line
✅ Internet/SaaS with no hardware coordination
✅ Strong shaping skill in leadership

## When it struggles

❌ Hardware/regulated products with longer cycles
❌ Multi-team coordination at scale
❌ Junior leadership (shaping requires experience)
❌ External commitment pressure (sales selling features ahead)

## See also

- [Dual Track Agile](dual-track-agile.md) — the contrast
- [Roadmap trap](roadmap-trap.md) — Shape Up's bet structure avoids this
- [Outcomes vs outputs](outcomes-vs-outputs.md) — Shape Up frames bets as outcomes-with-time-budgets
