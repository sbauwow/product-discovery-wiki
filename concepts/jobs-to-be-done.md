# Jobs To Be Done (JTBD)

> Sources: Clayton Christensen (*Competing Against Luck*, 2016), Tony Ulwick (Outcome-Driven Innovation, 1990s), Bob Moesta (Switch Interview method).

## Core thesis

> Customers don't buy products. They **hire** products to do a **job**.

A "job" is the progress a customer is trying to make in a particular circumstance. It's stable across time and technology — the *solutions* people hire change, the underlying job doesn't.

Christensen's canonical example:
- **Job:** make my morning commute less boring and keep me full until lunch
- **Hired solutions:** McDonald's milkshake (one-handed, lasts 20 min) > banana, donut, bagel

The competitor of a milkshake isn't another milkshake. It's a banana, a podcast, or skipping breakfast.

## Why the framing works

It separates **stable jobs** from **unstable solutions**:
- People have always wanted to listen to music alone (job)
- Solutions: vinyl → tape → CD → MP3 → streaming → AI playlists (changes every decade)

Designing around the solution traps you in the current paradigm. Designing around the job lets you skate to the next one.

## Job statement structure

Christensen's format:
> When I [situation], I want to [motivation], so I can [expected outcome].

Example:
> When I'm commuting alone in the morning, I want to be entertained and lightly fed, so I can arrive at work in a good mood and not hungry.

Ulwick's format (more rigorous):
> [verb] + [object of the verb] + [contextual clarifier]

Example:
> Minimize the time it takes to confirm the recipient received the package.

Note: no mention of any product. The job is solution-agnostic.

## Functional, emotional, social dimensions

Every job has three:
1. **Functional** — the literal task ("listen to music")
2. **Emotional** — how the user wants to feel ("feel relaxed", "feel cool")
3. **Social** — how the user wants to be perceived ("look knowledgeable", "fit in")

Premium products usually win on emotional/social, not functional. Beats headphones don't sound better than Sony — they signal differently.

## The Switch Interview (Moesta/Spiek)

A specific interview format to surface jobs. Four "forces":

```
                  Push of current situation
                  ("my old phone is slow")
                          │
                          ▼
                ┌─────────────────────┐
   Pull of new │      THE SWITCH       │  Anxiety about new
   ("iPhone is │     (purchase/hire)   │  ("will my apps work?")
    fast")     └─────────────────────┘
                          ▲
                          │
                  Habits of present
                  ("I know how my old phone works")
```

Switch happens when **push + pull > anxiety + habit**.

The interview asks about a specific past purchase, walking the timeline:
1. First thought
2. Trigger to act
3. Consideration set
4. Decision moment
5. First use

Not "would you buy X?" — that's [solutioning](solutioning-trap.md). Past-behavior probes only.

## Outcome-Driven Innovation (Ulwick)

A more quantitative cousin. Steps:
1. Define the job
2. Decompose into ~50–150 desired outcomes (each a metric)
3. Survey customers: rate each outcome on **importance** and **satisfaction**
4. Compute **opportunity score** = importance + max(importance − satisfaction, 0)
5. High-opportunity outcomes = underserved, ripe for innovation

## How JTBD connects to discovery

- JTBD interviews surface **jobs** → become **opportunities** in the [OST](opportunity-solution-tree.md)
- Opportunity scores prioritize which jobs to attack
- Solutions are evaluated by how well they get the job done — not feature-by-feature comparison

## Critiques

- **Rigid taxonomy debates** — Christensen vs Ulwick camps argue about format more than they should
- **Hard to scale** — switch interviews are 60+ min, not lightweight
- **Confused with personas** — JTBD is anti-persona ("a 35-year-old marketing manager named Sarah" is a fiction; "a person trying to commute alone with their hands full" is a job)

## See also

- [User interviews](user-interviews.md) — switch interviews are one specific type
- [Opportunity Solution Tree](opportunity-solution-tree.md) — where jobs become opportunities
- [Outcomes vs outputs](outcomes-vs-outputs.md) — JTBD outcomes are measurable, not feature-shaped
