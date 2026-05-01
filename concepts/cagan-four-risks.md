# Cagan's Four Risks

> Source: Marty Cagan, *Inspired*, *Empowered*. The single most useful frame for deciding what discovery work to do.

Every product idea fails for one of four reasons. Discovery exists to reduce each *before* engineering commits to building.

| Risk | Question | Owner | Cheapest test |
|---|---|---|---|
| **Value** | Will customers buy it / choose it / use it? | PM | User prototype + interview |
| **Usability** | Can they figure out how to use it? | Designer | Usability test on prototype |
| **Feasibility** | Can engineers build it with the time/tech/data we have? | Tech lead | Engineering spike |
| **Viability** | Does it work for our business? (legal, sales, finance, brand, support, GTM) | PM + stakeholders | Stakeholder review |

## Why this list

Earlier framings (e.g. desirability/feasibility/viability — IDEO) collapsed value and usability. Cagan splits them because they fail differently:
- **Value failure** = users don't want it. Solved by problem reframe.
- **Usability failure** = users want it but can't operate it. Solved by design iteration.

These need different evidence and different fixes.

## Order of attack

Test the **riskiest** assumption first, not the easiest. Common ordering by domain:

- **Consumer**: value > usability > feasibility > viability
- **Enterprise**: viability (will the buyer approve?) > value > feasibility > usability
- **Hard tech**: feasibility > value > viability > usability

Wrong ordering wastes time. Building a feasible, usable, viable product nobody wants is the standard failure mode of feature factories.

## Connection to other concepts

- [Assumption mapping](assumption-mapping.md) — categorize assumptions by which of the four risks they address
- [Prototyping](prototyping.md) — different prototype types attack different risks
- [Empowered teams](empowered-team.md) — the trio (PM/Design/TL) maps 1:1 to the first three risks

## Anti-pattern

Treating feasibility as the only risk ("can we build it?") and shipping. This is the [feature factory](feature-factory.md).
