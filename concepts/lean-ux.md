# Lean UX

> Source: Jeff Gothelf & Josh Seiden, *Lean UX* (2013, 3rd ed. 2021). Integrates UX into agile delivery via hypothesis-driven design. Predecessor framing for [outcomes over outputs](outcomes-vs-outputs.md).

## The thesis

> Stop producing UX deliverables. Start producing UX outcomes.

Traditional UX: designer produces wireframes, mockups, specs, hands them off to engineers. Process is deliverable-heavy and assumes the design is right.

Lean UX: design, research, and engineering work in tight integrated loops. The artifact isn't a deliverable — it's *learning*. Design is a hypothesis to be tested, not a spec to be implemented.

## The Lean UX canvas (8 boxes)

```
┌────────────────────────────────────────────────────────────────┐
│ 1. Business Problem                                            │
│    What's broken from the business perspective?                │
├──────────────────────────────────┬─────────────────────────────┤
│ 2. Business Outcomes             │ 3. Users & Customers        │
│    Measurable changes wanted      │ Who has the problem?        │
├──────────────────────────────────┼─────────────────────────────┤
│ 4. User Outcomes & Benefits      │ 5. Solutions                │
│    Why would users want this?    │ Many candidate solutions     │
├──────────────────────────────────┼─────────────────────────────┤
│ 6. Hypotheses                    │ 7. What's the most important │
│    Testable belief statements    │   thing we need to learn?   │
├──────────────────────────────────┴─────────────────────────────┤
│ 8. What's the least amount of work to test it?                 │
└────────────────────────────────────────────────────────────────┘
```

A team fills the canvas before designing. Forces explicit hypothesis + minimal test before any UX work.

## Hypothesis statements

Lean UX format:
> We believe that [building/doing X] for [user Y] will result in [outcome Z]. We will know this is true when we see [evidence].

Example:
> We believe that adding a "skip onboarding" link for return visitors will result in faster time-to-value for repeat users. We will know when 7-day repeat-user activation rises 10%+.

Every UX work item gets a hypothesis. Without one, the team is making changes for their own taste, not user value.

## Three principles

### 1. Cross-functional collaboration
Designer, PM, engineer co-create. No designer-as-service-bureau ("send me your wireframes when ready"). Same room, same problem.

### 2. Outcomes over outputs
A wireframe shipped is output. A user behavior changed is outcome. See [outcomes vs outputs](outcomes-vs-outputs.md). Lean UX directly inspired Cagan's [empowered team](empowered-team.md) framing.

### 3. Continuous discovery
Not a project with start/end. Ongoing user research, prototype, test, iterate. Aligned with Torres's later [continuous discovery](continuous-discovery.md).

## Lean UX vs traditional UX

| Lean UX | Traditional UX |
|---|---|
| Hypothesis-driven | Specification-driven |
| Lightweight artifacts (sketch, prototype) | Heavy artifacts (wireframes, specs) |
| Continuous validation | Big-bang research → handoff |
| Designer embedded in team | Designer in separate UX dept |
| Outcomes measured | Deliverables shipped |
| 1–2 week loops | Months-long studies |

## Lean UX vs Lean Startup

Lean UX = Lean Startup applied to UX work. Same loop:
- Hypothesis → MVP/prototype → measure → learn → pivot/persevere
- Just scoped to UX/design decisions instead of whole business

## Lean UX in delivery cycles

Each sprint or cycle:

```
Sprint N
├── Hypothesis written
├── Sketch / lo-fi prototype
├── 5-user test (or A/B in production)
├── Results synthesized
└── Decision: ship, iterate, kill
```

Output of the sprint includes *what we learned*, not just *what we built*.

## Common failure modes

- **Hypothesis-as-checkbox** — written in passing, never tested
- **Continuous discovery without rigor** — many "user touchpoints", no shifts in product direction
- **No designer** — without a strong UX mind, teams make UX decisions on autopilot
- **Aesthetic sprints** — endless prototype iteration, no test, no decision
- **"We did Lean UX"** — claiming the practice without the discipline (the most common pattern)

## See also

- [Continuous Discovery](concepts/continuous-discovery.md) — the modern descendant
- [Outcomes vs outputs](concepts/outcomes-vs-outputs.md) — Lean UX's philosophical core
- [Empowered team](concepts/empowered-team.md) — Cagan's evolution of the cross-functional idea
- [Assumption mapping](concepts/assumption-mapping.md) — what hypotheses get tested first
