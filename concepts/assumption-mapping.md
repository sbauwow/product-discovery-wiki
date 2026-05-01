# Assumption Mapping

> Source: David Bland & Alex Osterwalder, *Testing Business Ideas* (2019). Also called "assumption testing" or "leap of faith assumption" identification.

## The problem it solves

Every solution carries hidden assumptions. Most are obvious; a few are existential. Building before testing the existential ones = expensive failure. Assumption mapping makes them explicit and ranks them by risk.

## The 2x2

```
                    IMPORTANT
                        │
            (3) test    │   (1) test FIRST
            later       │   (most critical
            (low risk)  │    leap of faith)
                        │
   ─── KNOWN ───────────┼─────────── UNKNOWN ───
                        │
            (4) ignore  │   (2) test
            (low value, │   (cheap, useful
             low risk)  │    confidence)
                        │
                  UNIMPORTANT
```

Two axes:
- **Importance** — if this assumption is wrong, does the solution fail?
- **Evidence** — how much do we know? (known = data exists; unknown = guess)

Test order: (1) → (2) → (3). Quadrant (4) you can ignore.

## How to run it

1. Pick one solution from your [OST](opportunity-solution-tree.md).
2. Brainstorm assumptions. Categorize by [Cagan's four risks](cagan-four-risks.md):
   - **Desirability/value** — "users want this"
   - **Usability** — "users can figure this out"
   - **Feasibility** — "we can build this"
   - **Viability** — "the business can sustain this"
3. Write each on a card. Place on the 2x2.
4. Top-right (important + unknown) = your **leap of faith** assumptions. Test first.

## Example

**Solution:** "AI feature that auto-summarizes meeting notes"

| Assumption | Risk type | Importance | Evidence |
|---|---|---|---|
| Users actually read meeting notes | Value | HIGH | LOW → **test first** |
| Summary quality is acceptable | Feasibility | HIGH | LOW → **test first** |
| Users will share AI summaries with team | Value | MED | LOW → test |
| API costs are sustainable at scale | Viability | HIGH | LOW → test |
| Web framework can render markdown | Feasibility | LOW | HIGH → ignore |
| Users prefer button at top vs bottom | Usability | LOW | LOW → ignore |

The first four matter. The last two are noise.

## Picking the test

For each leap-of-faith assumption, pick the **cheapest experiment that gives a clear signal**. Bland's *Testing Business Ideas* catalogs ~44 experiment types. Common ones:

| Assumption type | Cheap test |
|---|---|
| Value | Landing page + signup form, fake-door, concierge MVP |
| Usability | 5-user prototype test |
| Feasibility | Engineering spike (1–3 days) |
| Viability | Cost model spreadsheet, legal review, sales convo |

## The 80/20 rule of testing

Most teams test the wrong assumptions:
- ✅ Easy + already-believed assumptions → confirms what you already knew
- ❌ Hard + unknown + critical → these are the ones that matter

If your test result doesn't change what you'd do, you tested the wrong thing.

## Strong vs weak evidence

Evidence isn't binary. A signal hierarchy:

```
Weakest                                                Strongest
─────────────────────────────────────────────────────────────────
Opinion → Survey → Interview → Prototype use → Real money paid
```

A user *saying* they'd pay is opinion. A user *paying* is evidence. Move down the line where possible.

## Common failure modes

- **Solutioning the test** — picking the experiment that confirms your bias
- **Mock-money tests** — "would you pay?" without actual transaction. Always overstates demand 5–10x.
- **Vanity validation** — celebrating a 60% positive interview when 40% red flags should kill the idea
- **Single test = green light** — one positive result rarely sufficient for a leap-of-faith assumption

## See also

- [Cagan's four risks](cagan-four-risks.md) — the categorization scheme
- [Prototyping](prototyping.md) — most common experiment type
- [Lean Startup](lean-startup.md) — the broader build-measure-learn frame
