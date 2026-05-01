# Now / Next / Later Roadmap

> Source: Janna Bastow (ProductPlan, 2014), popularized by Marty Cagan, Teresa Torres. The roadmap format that resists the [roadmap trap](roadmap-trap.md). Replaces dates with horizons.

## The format

```
┌──────────────────────┬──────────────────────┬──────────────────────┐
│      NOW             │       NEXT           │       LATER          │
│                      │                      │                      │
│  in active discovery │ on deck after now    │ ideas / directions   │
│  or delivery         │ confidence: medium   │ confidence: low      │
│                      │                      │                      │
│  - Outcome A         │ - Outcome D          │ - Outcome G          │
│    (active OST)      │   (research starting)│   (vague hypothesis) │
│                      │                      │                      │
│  - Outcome B         │ - Outcome E          │ - Outcome H          │
│    (in delivery)     │                      │                      │
│                      │                      │                      │
│  - Outcome C         │ - Outcome F          │                      │
│                      │                      │                      │
└──────────────────────┴──────────────────────┴──────────────────────┘
   high confidence       medium confidence       low confidence
   committed             likely                  exploratory
   ~1 quarter            ~next 1-2 quarters       6+ months
```

Three columns of decreasing certainty. No dates. No Gantt chart. No locked-in feature list.

## Why it's better than dated roadmaps

| Dated roadmap | Now/Next/Later |
|---|---|
| Implies precision we don't have | Honest about uncertainty |
| Treats commitments as dates | Treats commitments as outcomes |
| Hard to revise (looks like broken promise) | Designed to revise |
| Locks in features pre-discovery | Discovery can reshape |
| Sales sells features ahead | Sales sells outcomes / direction |
| Misses encourage extending dates | Misses encourage moving cards |

The dated roadmap pretends a startup operates like a construction project. It doesn't. NNL acknowledges the actual epistemic state: high certainty about now, less about next, much less about later.

## What goes in each column

### Now
- Active **outcomes** the team is currently moving (not features)
- Items in [discovery](continuous-discovery.md) AND in [delivery](dual-track-agile.md)
- High confidence — committed for the current quarter
- Clear measurable success criteria

### Next
- Outcomes likely to enter Now in 1–2 quarters
- Some discovery may have started
- Confidence: medium — will probably happen, may shift
- Used to align stakeholders on direction without committing dates

### Later
- Directional bets, themes, or unexplored hypotheses
- Sometimes only described as themes ("improve enterprise security posture") not specific outcomes
- Confidence: low — explicitly speculative
- Useful for telling investors/board "we're aware of these"

## What does NOT go in NNL

- ❌ Specific features ("Ship dark mode")
- ❌ Dates within columns ("by March 15")
- ❌ Engineering tasks ("migrate Postgres")
- ❌ Sales commitments ("client X needs feature Y by Q3")

NNL is for **outcomes the team is committing to move**. Everything else lives in different docs.

## Worked example

```
NOW (Q4 2025)
- Increase trial→paid conversion 4% → 7%
  [active discovery; OST in progress]
- Reduce p90 dashboard load from 3.2s to 1.5s
  [in delivery; sprint 3 of 4]
- Activate 50% of new signups in week 1 (currently 32%)
  [active discovery; first prototypes in test]

NEXT (Q1-Q2 2026)
- Reduce day-30 churn 8% → 5%
- Land first 5 enterprise customers (10K+ seats)
- Improve mobile app retention to parity with web

LATER (Q3+ 2026, exploratory)
- AI-native experience layer
- Marketplace / partner ecosystem
- International expansion (3+ markets)
```

This roadmap is honest. The Now items have measurable outcomes; the Later items are themes. Stakeholders can argue priority without arguing dates.

## Communication patterns

### To execs
"Here's what we're moving Now (with confidence), Next (likely), and Later (exploratory). The Now items are our quarterly bets."

### To sales
"We can't commit to feature dates, but we can tell you which *outcomes* we're investing in. If a customer's need maps to a Now/Next outcome, your timing is good. If it maps to Later, we're not yet investing."

### To customers
"Our roadmap is outcome-shaped. Tell us your problem; we'll tell you whether and roughly when we're tackling it."

### To engineering
"Outcomes are commitments. Specific features are emergent from discovery. Don't pre-build features for Next or Later — discovery may change them."

## When NNL works

- ✅ Mature product orgs with discovery practice
- ✅ Companies whose customers/sales can adopt outcome-shaped commitments
- ✅ Multi-team coordination where directional alignment matters more than precise dates
- ✅ B2B companies that want to surface direction without contractual commitment

## When it struggles

- ❌ Orgs where sales/board demand date commitments
- ❌ Hardware / regulated products with hard-deadline mandates
- ❌ Customers who need contractual feature/date commitments (rare; usually negotiable)
- ❌ Pre-PMF startups where everything is "Now" or "Later" with nothing in between

## Common failure modes

- **Hidden dates** — team writes "Next = Q1" implicitly; same as a dated roadmap
- **Features sneak in** — "ship dark mode" appears in Now; outcome thinking abandoned
- **Now too crowded** — 12 items in Now means nothing is committed
- **Later as graveyard** — items go to Later and never come back; ditch them entirely
- **Stakeholder pushback** — "I want dates" — answered by demonstrating that *outcomes* are commitments and dates were always fictional

## Variants

- **Now/Next/Later/Future** (4 columns) — adds an even-more-speculative column
- **Themes/Outcomes/Bets** — restructures around themes (areas) → outcomes (changes) → bets (active work)
- **Two-track NNL** — separate Now/Next/Later for discovery vs delivery
- **Quarterly OKR + NNL** — OKRs in Now; thematic outcomes in Next/Later

## See also

- [Roadmap trap](concepts/roadmap-trap.md) — the anti-pattern NNL solves
- [Outcomes vs outputs](concepts/outcomes-vs-outputs.md) — the philosophical foundation
- [OKRs](concepts/okrs.md) — Now items often equal current quarter OKRs
- [Shape Up](concepts/shape-up.md) — alternative format, with bet structure instead of NNL columns
- [Product strategy](concepts/product-strategy.md) — the layer above NNL that decides what goes where
