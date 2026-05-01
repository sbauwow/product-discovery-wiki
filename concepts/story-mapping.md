# Story Mapping

> Source: Jeff Patton, *User Story Mapping* (2014). Bridges discovery → delivery. Visualizes the user journey horizontally and feature depth vertically.

## The shape

```
                  ── narrative flow (left → right) ──→
                  
USER ACTIVITIES   [Sign up]──[Onboard]──[Use core]──[Pay]──[Refer]
                     │          │           │         │       │
USER STEPS         ┌─┼─┐      ┌─┼─┐       ┌─┼─┐     ┌─┼─┐  ┌─┴─┐
                   ▼ ▼ ▼      ▼ ▼ ▼       ▼ ▼ ▼     ▼ ▼ ▼  ▼   ▼
                   
                  ╔══════════════════════════════════════════════╗
RELEASE 1 (MVP)   ║ minimal slice: walk the spine end-to-end     ║
                  ╚══════════════════════════════════════════════╝
                   ╔════════════════════════════════════════════╗
RELEASE 2         ║ depth: more options, edge cases             ║
                  ╚════════════════════════════════════════════╝
                   ╔════════════════════════════════════════════╗
RELEASE 3         ║ polish: optimization, advanced flows         ║
                  ╚════════════════════════════════════════════╝
```

## Two axes

- **Horizontal (backbone)** — the sequence of activities a user does, left-to-right in time
- **Vertical (depth)** — alternative or detailed steps within each activity, stacked top-to-bottom by priority

## Why it beats a flat backlog

A flat backlog (JIRA list, spreadsheet) loses two crucial properties:

1. **Narrative coherence** — you can't tell the story of how a user actually flows through the product
2. **Slicing** — you can't easily cut "minimum end-to-end" from "everything"

Story mapping reintroduces both. The MVP is a horizontal *slice* that walks the entire spine — minimal at every step, but complete end-to-end.

## The MVP slicing rule

> A working spine beats a feature-complete fragment.

Wrong: build all of "Sign up" perfectly, then start "Onboard" → user can sign up but can't actually use the product.

Right: build *just enough* of every step to walk end-to-end → a real user can complete the whole journey, then you deepen.

This is also the difference between **walking skeleton** (Cockburn) and **iceberg backlog** (Schwaber).

## How to build one

1. **Frame the user** — one persona, one goal
2. **Big steps (backbone)** — 5–10 user activities, left to right in time
3. **Sub-steps** — under each big step, the fine-grained actions
4. **Detail items below sub-steps** — alternatives, edge cases, exceptions
5. **Slice horizontally** — draw a line through the map cutting MVP, then v2, etc.

Output: a wall (or Miro board) of sticky notes, organized 2D.

## Connection to other discovery work

- The **backbone** comes from [JTBD](jobs-to-be-done.md) or [user interviews](user-interviews.md) — what users actually do
- The **slices** become release commitments to delivery
- The **details** are stories ready for engineering

It's the handoff artifact between [opportunity solution tree](opportunity-solution-tree.md) (discovery) and the engineering backlog (delivery).

## When to use it

- Net new product or major feature
- Onboarding a new team to a product (great learning artifact)
- Replanning when scope is fuzzy

Not needed for small additions to an existing well-understood product.

## Common failure modes

- **Mapping the system instead of the user** — backbone is "API call → DB write → response" instead of "user signs up → user creates project". Fix: anchor on the user's verbs.
- **Vertical-first slicing** — building "Sign up" entirely before any other step. Loses the spine property.
- **Too many personas** — one map should serve one journey. Multi-persona maps usually need to be split.
- **Sticky notes outlive their context** — map gets stale once delivery starts; nobody updates it. Treat as a discovery snapshot, not a living artifact.

## See also

- [Opportunity Solution Tree](opportunity-solution-tree.md) — discovery upstream of mapping
- [Dual Track Agile](dual-track-agile.md) — story mapping is a discovery → delivery bridge
- [Outcomes vs outputs](outcomes-vs-outputs.md) — slices are still outputs; tie them to outcomes
