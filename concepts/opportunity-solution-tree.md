# Opportunity Solution Tree (OST)

> Source: Teresa Torres. The central artifact of [continuous discovery](continuous-discovery.md). A visual map from outcome to experiments.

## Structure

```
                        DESIRED OUTCOME
                       (measurable, single)
                              │
             ┌────────────────┼────────────────┐
             │                │                │
        Opportunity      Opportunity      Opportunity
        (user need)      (user need)      (user need)
             │
        ┌────┴────┬─────────┐
        │         │         │
     Solution  Solution  Solution
        │
    ┌───┴───┐
    │       │
Experiment Experiment
```

Four layers, top-to-bottom:

### 1. Outcome

A *single* measurable business or product outcome. Examples:
- "Increase week-1 retention from 30% to 45%"
- "Reduce time-to-first-value from 8 min to 2 min"
- "Increase paid conversion by 20%"

NOT an output ("ship onboarding redesign"). NOT a vague goal ("delight users"). See [outcomes vs outputs](outcomes-vs-outputs.md).

One tree, one outcome. Multiple outcomes → multiple trees, or you're conflating things.

### 2. Opportunities

User needs, pain points, and desires that — if addressed — would move the outcome. Phrased as **user statements**, not solutions.

✅ "I can't tell if my data synced"
✅ "Setting up takes longer than I have time for"
❌ "Add a sync indicator" (that's a solution)
❌ "Improve onboarding" (too vague)

Sourced from interviews, support tickets, session recordings, NPS comments. Mapped from data, not invented.

**Sub-opportunities:** opportunities can nest. "Onboarding is hard" → "Account setup is unclear" + "First import fails silently" + "Don't know what to do after signup".

**Prioritization within opportunities:** importance × market size × strategic fit. Pick *one* branch to attack first. The discipline is not solving every opportunity — it's choosing.

### 3. Solutions

Multiple candidate solutions per opportunity. The rule: **at least 3 solutions per opportunity you're attacking**. One solution = no real choice = first-idea-wins.

Solutions are ideas, not commitments. Most will be killed by experiments.

### 4. Experiments

Tests of the assumptions behind solutions. See [assumption mapping](assumption-mapping.md). Each solution has multiple assumptions; each risky assumption gets an experiment.

Cheapest experiment first. A 5-user prototype test beats a 6-week build.

## Why the tree shape matters

The tree forces three disciplines:

1. **Traceability** — every solution traces up to a user opportunity, which traces up to a business outcome. No orphan features.
2. **Comparison** — siblings in the tree are alternatives. Forces "this *or* that", not "this *and* that".
3. **Pruning** — branches die when evidence kills them. The tree shrinks and grows weekly.

A flat backlog has none of these properties.

## Worked example

```
OUTCOME: Increase week-1 retention 30% → 45%
│
├── OPP: "I don't know what to do after signup"
│   ├── SOL: Interactive product tour
│   │   └── EXP: Wizard-of-Oz tour with 5 users
│   ├── SOL: Empty-state suggested actions
│   │   └── EXP: A/B test 3 empty-state copies
│   └── SOL: Personalized first task based on signup intent
│       └── EXP: Prototype test, 8 users
│
├── OPP: "First import fails and I give up"
│   ├── SOL: Pre-flight check before import
│   │   └── EXP: Engineering spike — feasibility
│   ├── SOL: Auto-retry with progress
│   └── SOL: Sample data fallback
│
└── OPP: "I can't tell if it's worth paying for"
    └── ... (lower priority this quarter)
```

## How the tree updates

- **Weekly:** new opportunities added from interviews; killed solutions removed
- **Per experiment:** results promote a solution to delivery, or kill it
- **Quarterly:** outcome may change with strategy

Tools: Miro, FigJam, Mural, or paper. The medium matters less than the practice.

## Failure modes

- **Tree built once, never updated** — becomes wallpaper
- **Solutions without opportunities** — pet ideas with no user grounding
- **One solution per opportunity** — no real comparison
- **Outcome is an output** — "ship redesign" can't anchor a tree
- **Stakeholder requests skip the tree** — kills the discipline entirely

## See also

- [Continuous Discovery](continuous-discovery.md) — the cadence that feeds the tree
- [Outcomes vs outputs](outcomes-vs-outputs.md) — choosing the root
- [Assumption mapping](assumption-mapping.md) — designing the leaves
- [Jobs To Be Done](jobs-to-be-done.md) — a way to discover opportunities
