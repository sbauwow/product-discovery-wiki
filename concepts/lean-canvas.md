# Lean Canvas

> Source: Ash Maurya, *Running Lean* (2010). Adaptation of Osterwalder's [Business Model Canvas](business-model-canvas.md) for early-stage startups. Replaces 4 blocks with startup-specific ones.

## The 9 blocks

```
┌──────────────┬────────────┬─────────────┬─────────────┬──────────────┐
│              │            │             │             │              │
│   PROBLEM    │  SOLUTION   │   UNIQUE     │  UNFAIR      │  CUSTOMER    │
│              │            │ VALUE PROP   │  ADVANTAGE   │  SEGMENTS    │
│  top 3       │ top 3       │             │             │              │
│  problems    │ features    │ single, clear│ what can't  │ who has the  │
│              │            │  message     │ be copied   │ problem      │
│              ├────────────┤             ├─────────────┤              │
│              │            │             │             │              │
│              │  KEY        │             │  CHANNELS    │              │
│              │ METRICS     │             │             │              │
│              │            │             │             │              │
│              │ what we     │             │ how we       │              │
│              │ measure     │             │ reach them   │              │
├──────────────┴────────────┴─────────────┴─────────────┴──────────────┤
│                                                                     │
│       COST STRUCTURE                  REVENUE STREAMS                │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

Same 9-block layout as BMC. Four blocks replaced.

## Replaced blocks

| BMC block (replaced) | Lean Canvas block (new) |
|---|---|
| Key Partners | **Problem** — top 3 customer problems |
| Key Activities | **Solution** — top 3 features that solve them |
| Key Resources | **Key Metrics** — measurable activity that indicates progress |
| Customer Relationships | **Unfair Advantage** — what cannot be easily copied |

Same 5 blocks: Customer Segments, UVP, Channels, Cost Structure, Revenue Streams.

## Why these replacements

Maurya's reasoning: early-stage startups don't *have* established partnerships or organized activities. They have hypotheses about a problem and a solution. The original BMC blocks (key partners, activities, resources, customer relationships) are *operational* and irrelevant pre-product.

The new blocks force startups to articulate:

### Problem
What are the top 3 problems your customer segment has? *Validated*, not assumed. Plus: how do they currently solve them? (Existing alternatives = your real competition, often more than direct competitors.)

### Solution
The top 3 features in your MVP that address those problems. Three only. If you list 12, you don't yet know.

### Key Metrics
What single number measures whether you're making progress? Often the [North Star](north-star.md) or [pirate metrics](pirate-metrics.md) input metric. If you can't pick one, you don't yet have a model.

### Unfair Advantage
What can't be copied or bought? Examples: insider information, proprietary data, an existing community, brand, patents, network effects.

Most startups have **no unfair advantage** at start. Acknowledging that is itself a strategic insight.

## Worked example: an AI legal research tool

```
PROBLEM:                    SOLUTION:                      UVP:                         UNFAIR ADV:                   SEGMENTS:
- Legal research is slow    - AI search across 50M cases   "Find the precedent           - 5-year exclusive deal      Solo & small-firm
- Junior assoc bottleneck   - Auto-generated brief snippets you need in 30 seconds,      with Court Listener data     attorneys (1-10 lawyers)
- $40+/lookup on Westlaw    - Citation network              not 30 minutes."             - Founding team is ex-DOJ    
                            
                            KEY METRICS:                                                  CHANNELS:
                            - Searches/lawyer/week                                        - Bar association partnerships
                            - Time to first useful result                                 - LinkedIn ads to attorneys
                                                                                          - Free trial via state bar emails
                                                                                          
COST STRUCTURE:                                              REVENUE STREAMS:
- Court data licensing                                       - $200/month per attorney
- LLM inference                                              - Annual contracts (10% discount)
- 4 engineers                                                
```

Lean Canvas captures this in one page. A traditional business plan would take 30.

## How to fill it (Maurya's order)

```
1. Customer Segments    — who is this for?
2. Problem              — what hurts?
3. Unique Value Proposition — what's the promise?
4. Solution             — top 3 features
5. Channels             — how to reach customers
6. Revenue Streams      — how to monetize
7. Cost Structure       — fixed/variable
8. Key Metrics          — what indicates progress
9. Unfair Advantage     — defensibility
```

Top 3 (segments, problem, UVP) are most important. Most startups fail because problem-segment-UVP fit is wrong, not because the solution is wrong.

## The "existing alternatives" rule

Maurya emphasizes: under "Problem", note **existing alternatives**. How does the customer solve this *today*?
- "They use Excel + email"
- "They hire an intern"
- "They don't solve it; they live with it"

Existing alternatives are the real competitive set. Often "doing nothing" is the strongest competitor — users tolerate the problem rather than learn a new tool.

## Iterating the canvas

The canvas is meant to be **versioned**:
- v1: built from founder hypotheses
- v2: after first 10 [Mom Test](mom-test.md) interviews
- v3: after MVP launch
- vN: after each major learning

Comparing canvases over time = the startup's narrative arc.

## Lean Canvas vs BMC

| Lean Canvas | BMC |
|---|---|
| Pre-PMF | Post-PMF |
| Problem-solution focus | Operational completeness |
| Unfair advantage explicit | Implicit in resources/partners |
| Built and rebuilt rapidly | More stable artifact |
| Output-of-discovery focused | Operations-focused |

Use Lean Canvas pre-PMF, evolve to BMC as the operational complexity grows.

## Common failure modes

- **No existing alternatives noted** — pretending you have no competition
- **Vague UVP** — "the best thing for X" is not a value prop
- **5+ items per box** — under-constrained; force top-3
- **Solution before Problem** — building backwards
- **Static canvas** — built once, never updated; loses its power

## See also

- [Business Model Canvas](concepts/business-model-canvas.md) — the parent
- [Value Proposition Canvas](concepts/value-proposition-canvas.md) — drills into the UVP block
- [Customer Development](concepts/customer-development.md) — the validation methodology Maurya pairs with
- [Lean Startup](concepts/lean-startup.md) — the broader frame
- [Mom Test](concepts/mom-test.md) — how to validate the Problem block
