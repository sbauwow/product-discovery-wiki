# RICE / ICE Scoring

> Sources: Sean McBride at Intercom (RICE, 2017). ICE attributed to Sean Ellis. Lightweight prioritization formulas.

## The formulas

**RICE** = (Reach × Impact × Confidence) ÷ Effort

| Variable | Unit | How to estimate |
|---|---|---|
| Reach | users / time period | "How many users hit this in a quarter?" |
| Impact | 0.25 / 0.5 / 1 / 2 / 3 | minimal / low / medium / high / massive |
| Confidence | 0–100% | 100=data-backed, 80=some, 50=guess |
| Effort | person-months | engineering + design |

**ICE** = Impact × Confidence × Ease (often each on a 1–10 scale)

ICE is RICE without explicit reach. Faster, less rigorous.

## Worked example (RICE)

| Idea | Reach | Impact | Conf | Effort | Score |
|---|---|---|---|---|---|
| Improve checkout error messages | 50k | 1 | 80% | 0.5 | 80,000 |
| Add new payment provider | 15k | 2 | 60% | 3 | 6,000 |
| Redesign settings page | 80k | 0.25 | 90% | 1 | 18,000 |
| AI-powered recommendations | 100k | 3 | 30% | 6 | 15,000 |

Order: error messages → settings → AI recs → payment provider.

Note: low-confidence items get penalized hard. The formula rewards certainty.

## What it's good for

- **Forcing structure** on a list of ideas that would otherwise be ranked by loudness
- **Surfacing assumptions** — the conversation around "what's the impact?" is more valuable than the number
- **Tiebreaker** when 5–10 items are roughly equal

## What it's bad for

- **Comparing across categories** — "improve UX" and "build new product line" don't fit one formula
- **Strategic bets** — high-impact, low-confidence, high-effort items always lose. RICE-driven roadmaps drift toward incrementalism.
- **False precision** — 80,000 vs 18,000 looks meaningful; both numbers are made up
- **Hiding behind math** — "RICE said so" is not a strategy

## The deeper problem

Prioritization formulas treat ideas as **independent**. They aren't:
- A bad onboarding makes every other feature score lower (because reach is gated)
- A platform investment unlocks 10 future features
- An aesthetic redesign has emotional value formulas don't capture

A good [Opportunity Solution Tree](opportunity-solution-tree.md) handles this better: solutions compete *within* an opportunity, not across the whole roadmap.

## When to use RICE/ICE

- Pre-tree triage of opportunities
- Within a single OST branch, ranking sibling solutions
- Sanity check on a stakeholder request

## When NOT to use it

- Strategic decisions (use evidence + judgment, not a formula)
- Vision-level bets (formulas kill ambition; nothing high-impact has high confidence early)
- Comparing across distinct outcomes (apples to oranges)

## Variants and adjacent

- **WSJF** (Weighted Shortest Job First, SAFe) — Cost of Delay / Job Size. More finance-flavored.
- **MoSCoW** — Must / Should / Could / Won't. Categorical, not numeric.
- **Kano model** — categorize features by user delight (basic / performance / excitement). Better for *kinds* of features than ranking.
- **Value vs Effort 2x2** — RICE without the multiplications; same idea, less precision

## See also

- [Opportunity Solution Tree](opportunity-solution-tree.md) — the better way to compare
- [Feature factory](feature-factory.md) — what RICE-driven backlogs degenerate into
