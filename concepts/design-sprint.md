# Design Sprint

> Source: Jake Knapp at Google Ventures. Book: *Sprint* (2016).

A 5-day timeboxed process to go from problem to tested prototype. Heavy artillery for stuck problems, not weekly cadence.

## The 5 days

```
Mon: MAP       — agree on the problem, pick a target
Tue: SKETCH    — each person sketches solutions individually
Wed: DECIDE    — choose one sketch to prototype
Thu: PROTOTYPE — build a façade prototype (not real)
Fri: TEST      — 5 users, 1-on-1, observed by team
```

## When to use it

✅ Stuck on a hard strategic question
✅ New product or major direction call
✅ Stakeholders aligned on importance, not solution
✅ Can free 7 people for 5 days

❌ Weekly product work — overkill
❌ Problem already understood — just prototype
❌ Can't get team in same room (sprints work much worse remote)

## Why 5 days

- Long enough to build a real prototype + test it
- Short enough that calendar pressure forces decisions
- Single uninterrupted week prevents context-switching cost

## The prototype rule

Friday's prototype is a **façade**, not real code. Acceptable:
- Keynote slides with click areas
- Figma click-through
- Wizard of Oz (human behind curtain)
- Brochure / printed mockup

The point is to test the *idea*, not the *implementation*.

## The test

5 users on Friday is enough. Reasoning (Nielsen's 5-user finding):

```
% of usability problems found ≈ 1 - (1-L)^N
where L = % a single user finds (~31% empirically), N = # users
```

5 users finds ~85% of problems. 15 users finds ~95%. Diminishing returns.

## Decider role

One person has final decision authority. Without this, the sprint deadlocks Wednesday. Usually founder, GM, or product head.

## Sprints vs continuous discovery

| Design Sprint | [Continuous Discovery](continuous-discovery.md) |
|---|---|
| 5 days, intensive | Weekly, ongoing |
| One big question | Many small questions |
| Whole team locked in | Trio, embedded in normal work |
| Output: tested prototype | Output: updated [OST](opportunity-solution-tree.md) |
| Use for stuck/new problems | Use for everything else |

They complement. A sprint can kick off a new branch in the OST; continuous discovery maintains it.

## Common failure modes

- **Sprint without commitment** — half the team in meetings during sprint week. Kills the format.
- **No decider** — Wednesday becomes a debate, not a decision
- **Prototype too real** — engineers build production code Thursday, can't iterate
- **Test waterfalled** — testing pushed to "next week", insights forgotten

## Variants

- **2-day sprint** — Knapp's later "Sprint 2.0" for time-pressed teams
- **Remote design sprint** — works but requires more facilitation; AJ&Smart has open-source playbooks
- **Pretotype** (Alberto Savoia) — adjacent technique, focuses on "build the right it" before "build it right"

## See also

- [Prototyping](prototyping.md) — types of prototypes
- [Lean Startup](lean-startup.md) — adjacent loop philosophy
