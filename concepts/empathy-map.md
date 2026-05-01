# Empathy Map

> Source: Dave Gray / XPLANE, ~2009. Synthesis tool that captures what a user *says, thinks, does, feels* — usually after interviews, before [opportunity-mapping](opportunity-solution-tree.md).

## The classic 4-quadrant version

```
┌──────────────────┬──────────────────┐
│                  │                  │
│      SAYS        │     THINKS       │
│                  │                  │
│  verbatim quotes │  unspoken beliefs│
│  from interviews │  inferred from   │
│                  │  behavior        │
├──────────────────┼──────────────────┤
│                  │                  │
│      DOES        │      FEELS       │
│                  │                  │
│  observed        │  emotions during │
│  behaviors       │  the experience  │
│                  │                  │
└──────────────────┴──────────────────┘
```

The user (or persona) sits in the middle. Each quadrant captures one dimension.

## Extended (6-quadrant) version

Gray's later version adds:
- **Hears** — what voices in their environment say (boss, peers, ads)
- **Sees** — what they observe in their environment (competitors, market signals)

Often supplemented with:
- **Pain** — frustrations
- **Gain** — desired outcomes

## Why "says vs thinks" matters

The most useful split. Users *say* one thing publicly and *think* another. Surfacing the gap is where insight lives.

```
Says:  "I love the new dashboard."
Thinks: "I don't understand half the metrics, but I don't want to look stupid."

Says:  "Pricing seems fair."
Thinks: "$50/mo is fine but I'd never get it past procurement."

Says:  "We use Slack for everything."
Thinks: "It's overwhelming and I miss messages constantly."
```

Behavior tells you what they *think* — not what they say. Empathy maps force the team to surface the gap.

## When to build one

- **Synthesis after interviews** — turns transcripts into a digestible artifact
- **Onboarding new team members** — fast empathy ramp
- **Pre-design alignment** — get team on same mental model before sketching
- **Anti-feature-creep** — "would [user] actually feel that?" cuts pet ideas

## How to build

1. **Interview 5–10 users** in target segment
2. **Extract verbatim quotes** for "Says"
3. **Note observed behaviors** for "Does"
4. **Infer thoughts and feelings** from contradictions, hesitations, body language
5. **Mark divergence** — where says ≠ does ≠ thinks
6. **Identify pain & gain** at the bottom

A good empathy map is *anchored* in research. A bad one is invented in a workshop.

## Empathy map vs [persona](personas.md) vs [JTBD](jobs-to-be-done.md)

| | Empathy Map | Persona | JTBD |
|---|---|---|---|
| Unit | One user / segment | Composite individual | A job |
| Source | Direct interviews | Often invented | Switch interviews |
| Stable? | Snapshot | Static | Stable across products |
| Best for | Quick alignment | Design empathy | Solution-agnostic targeting |

They stack: JTBD identifies the job, persona embodies it, empathy map captures the felt experience. Many teams use only one and miss layers.

## Common failure modes

- **Made-up content** — quadrants filled in workshop without interview data
- **Demographic dump** — using Says/Does to repeat persona facts (age, role)
- **No divergence noted** — Says and Thinks identical, missing the insight
- **Built once, ignored** — like CJMs, decays without ritual
- **Too many users mixed** — averaging across segments hides differences

## A 30-min template

For each interview:

```
USER:        ____________________  SEGMENT: ___________

SAYS         (3 verbatim quotes)
1. "..."
2. "..."
3. "..."

DOES         (3 observed actions)
1. ...
2. ...
3. ...

THINKS       (inferred — note evidence)
1. ... (from: hesitation when asked about X)
2. ... (from: contradiction between A and B)

FEELS
- Frustration when: ...
- Confidence when: ...
- Anxiety when: ...

INSIGHT (1 sentence): ___________________________________
```

The bottom "Insight" line is the load-bearing output — what an opportunity in the [OST](opportunity-solution-tree.md) might be.

## See also

- [User interviews](concepts/user-interviews.md) — the source material
- [Personas](concepts/personas.md) — empathy maps inform research-grounded personas
- [Jobs To Be Done](concepts/jobs-to-be-done.md) — the rigorous framing for what users actually want
- [Opportunity Solution Tree](concepts/opportunity-solution-tree.md) — empathy-map insights become OST opportunities
