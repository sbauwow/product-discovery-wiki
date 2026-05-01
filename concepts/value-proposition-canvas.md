# Value Proposition Canvas

> Source: Alex Osterwalder, *Value Proposition Design* (2014). Companion to the [Business Model Canvas](#). A two-circle diagram aligning what users *need* with what your product *offers*.

## The canvas

```
┌───────────────────────────────┐    ┌────────────────────────────────┐
│   VALUE PROPOSITION (you)     │    │   CUSTOMER PROFILE (them)      │
│                               │    │                                │
│   Products & Services         │    │   Customer Jobs                │
│   ─────────                    │    │   ─────────                     │
│   What you offer              │    │   What user trying to do       │
│                               │    │                                │
│   Pain Relievers              │ ↔  │   Pains                        │
│   ─────────                    │    │   ─────                         │
│   How you reduce pains        │    │   Frustrations, risks, costs   │
│                               │    │                                │
│   Gain Creators               │    │   Gains                        │
│   ─────────                    │    │   ─────                         │
│   How you produce gains       │    │   Outcomes user wants          │
└───────────────────────────────┘    └────────────────────────────────┘
              ↑                                       ↑
              │                                       │
        you control                            you must research
```

Right side: **research-derived**. Sourced from interviews, [JTBD](jobs-to-be-done.md), observation. NOT invented.

Left side: **your design choices**. The product as designed to fit the right side.

The canvas is "fit" if every pain on the right has a pain reliever on the left, and every gain has a gain creator. If not — misalignment.

## Customer profile (right side)

### Jobs
What the user is trying to get done. Functional, social, emotional.
- Functional: "automate my recurring expense reports"
- Social: "look organized to my manager"
- Emotional: "feel in control of my finances"

Use [JTBD](jobs-to-be-done.md) format and discipline here.

### Pains
What hurts when they try to do those jobs:
- **Undesired outcomes** — "spent 2h on reports last month"
- **Obstacles** — "can't get receipts from drivers"
- **Risks** — "afraid I'll miss a deductible"

Severity matters. Rank: extreme / moderate / mild.

### Gains
What success looks like:
- **Required gains** — without these, no purchase ("must integrate with QuickBooks")
- **Expected gains** — assumed table stakes ("automatic backups")
- **Desired gains** — wanted but not required ("AI categorization")
- **Unexpected gains** — delighters ("predicts my next expense")

Maps loosely to [Kano model](kano-model.md) categories.

## Value proposition (left side)

### Products & Services
The bundle. Concrete: "expense scanner mobile app + web dashboard + accountant integration."

### Pain Relievers
For each customer pain, what your product specifically does about it.
- Pain: "spent 2h on reports" → Reliever: "auto-generates monthly report from receipts"
- Pain: "can't get receipts" → Reliever: "drivers email receipts, we OCR"

### Gain Creators
For each customer gain, what produces it.
- Gain: "look organized" → Creator: "shareable monthly summary PDF"
- Gain: "feel in control" → Creator: "real-time spend dashboard with budget alerts"

## The fit test

A value prop has *problem-solution fit* if:
- Every **major** pain has a reliever
- Every **required** gain has a creator
- Pain relievers and gain creators are *substantive*, not superficial

Common failure: feature list on the left, no clear mapping to pains/gains on the right. Result: products that work but don't *land*.

## How to use it

1. **Pick one segment** — different segments have different profiles
2. **Build the right side first** — from interviews, not whiteboard
3. **Brainstorm left side** — multiple solutions per pain/gain
4. **Test fit** — line up pain ↔ reliever, gain ↔ creator
5. **Identify gaps** — pains without relievers = unmet needs; relievers without pains = features no one wanted

## When to use

- **Net-new product** — clarifying who you're for and why
- **Feature pruning** — features without a pain/gain anchor are candidates to kill
- **Competitive differentiation** — comparing your canvas vs competitor's reveals positioning
- **Marketing message** — gain creators and pain relievers become headline copy

## Common failure modes

- **Right side invented** — built in workshop, not from research → fit is fictional
- **One canvas per product, not per segment** — averages across users, blurs fit
- **Feature dump on the left** — ignoring whether features map to pains
- **Skipping the priority** — every pain treated equal; in reality, severity differs 100x

## See also

- [Jobs To Be Done](jobs-to-be-done.md) — the rigorous version of "customer jobs"
- [Kano model](kano-model.md) — finer categorization of gains
- [Customer Development](customer-development.md) — Blank's process for building the right side
- [Opportunity Solution Tree](opportunity-solution-tree.md) — pains become opportunities
