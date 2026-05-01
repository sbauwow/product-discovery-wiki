# Dual Track Agile

> Sources: Jeff Patton (coined ~2007), Marty Cagan (popularized in *Inspired*), Lynn Cagan/Desirée Sy (early formulations at Autodesk).

One team, two concurrent tracks of work.

```
┌──────────────────────────────────────────────────────────────┐
│  DISCOVERY TRACK                                             │
│  PM + Designer + Tech Lead                                   │
│  Activities: interviews, prototypes, experiments, OST work   │
│  Output: validated backlog items (de-risked across 4 risks)  │
└──────────────────────────────┬───────────────────────────────┘
                               │ feeds validated work
                               ▼
┌──────────────────────────────────────────────────────────────┐
│  DELIVERY TRACK                                              │
│  Engineers (+ PM/Design as needed)                           │
│  Activities: build, test, ship, instrument                   │
│  Output: production code, telemetry                          │
└──────────────────────────────┬───────────────────────────────┘
                               │ surfaces new questions / data
                               ▼
                        back into discovery
```

## Critical points

- **Same team, not separate teams.** A discovery team that hands specs to a delivery team is just waterfall with extra steps.
- **Concurrent, not sequential.** Discovery does not "finish" before delivery starts. Both run every week.
- **Engineers participate in discovery.** Especially the tech lead — feasibility risk requires their judgment, and architectural insight often unlocks better solutions.
- **The backlog is an output, not an input.** Items only enter the delivery backlog after passing through discovery.

## What the tracks actually do in a week

**Discovery (typical week):**
- 1–3 user interviews ([continuous discovery cadence](continuous-discovery.md))
- Update [opportunity solution tree](opportunity-solution-tree.md)
- 1–2 prototype tests
- 1 engineering spike for feasibility

**Delivery (typical week):**
- Sprint work on validated items
- Code review, deployment, monitoring
- Bug fixes, instrumentation

## Why teams resist it

- "We don't have time for discovery" → really means "we don't have time to stop building things nobody wants"
- "Engineers don't want to be in interviews" → they do, once they see how much rework it prevents
- "The roadmap is committed for the quarter" → see [roadmap trap](roadmap-trap.md)

## Common failure modes

- **Discovery theater** — user interviews exist but don't change priorities. Stakeholders override evidence ([HiPPO](hippo.md)).
- **Discovery as a phase** — "we did discovery in Q1, now we're delivering in Q2-Q4". This is just waterfall.
- **Backlog as wishlist** — anyone can add items, no validation gate. Team ships [features](feature-factory.md), not outcomes.

## See also

- [Continuous Discovery](continuous-discovery.md) — the cadence that keeps the discovery track alive
- [Empowered team](empowered-team.md) — the staffing model dual-track requires
- [Outcomes vs outputs](outcomes-vs-outputs.md) — the success metric for the model
