# Personas

> Source: Alan Cooper, *The Inmates Are Running the Asylum* (1999). Composite fictional users meant to focus design decisions. Widely used, widely critiqued.

## The classic format

```
┌──────────────────────────────────┐
│  Sarah, 34                       │
│  Marketing manager, mid-size SaaS│
│  Goals:                          │
│    - reduce reporting time       │
│    - look smart in meetings      │
│  Frustrations:                   │
│    - can't pull data herself     │
│    - tools too technical         │
│  Tech savvy: medium              │
│  Quote: "I just want answers"    │
└──────────────────────────────────┘
```

A persona is a fictional user profile, intended to be vivid enough that designers/PMs can ask "what would Sarah want?" instead of "what would the user want?".

## Why they were invented

Pre-personas, designers spoke about "the user" abstractly. This led to:
- Design-by-committee ("but what about the other type of user?")
- Feature creep ("we need to support every case")
- Self-projection ("I'd want this, so users will too")

Personas constrain. Naming a target = saying *who you're not* designing for.

## Why they get criticized

### 1. Demographic overemphasis
Age, gender, job title rarely predict product behavior. A 24-year-old and 54-year-old can have identical jobs-to-be-done. Persona templates emphasize demographics because they're easy to fill in.

### 2. Made-up details
Many personas are invented in a conference room, not derived from research. "Sarah likes yoga" — based on what?

### 3. Static
Real users change. Personas don't update.

### 4. Confused with segments
A *segment* is a real measurable group (e.g. "users on free plan, with team size 5–10"). A *persona* is a fictional individual. Teams conflate them.

### 5. Overrun by [JTBD](jobs-to-be-done.md)
Christensen's argument: a persona named Sarah doesn't predict behavior. The *job* she's trying to do does. A 60-year-old man and 24-year-old woman both "hire a milkshake to make a boring commute less boring" — same job, no shared persona.

## When personas still work

- **Early-stage** — no data yet; personas keep the team aligned on a target
- **Cross-functional alignment** — sales/marketing/product talking about the same archetype
- **Anti-feature-creep tool** — "Sarah wouldn't use this" is a useful kill argument
- **Research-grounded** — personas built from interview data, with verbatim quotes, not invented demographics

## Behavioral / data-driven personas

A modern, defensible variant. Build personas from observed behavior, not invented demographics:

```
Power user (12% of base)
- 4+ sessions/week
- Uses 3+ advanced features
- 80% paid conversion at month 6
- Top requests: bulk operations, API access

Casual user (68% of base)
- 1 session/week
- Uses 1-2 core features only
- 8% paid conversion at month 6
- Top requests: clearer onboarding, faster results
```

Demographic-free, behavior-anchored, segment-derived. These are essentially behavioral segments dressed as personas — and they work.

## Personas vs JTBD vs Segments

| | Persona | [JTBD](jobs-to-be-done.md) | Segment |
|---|---|---|---|
| Unit | Fictional individual | Job | Measurable group |
| Source | Sometimes invented | Interviews | Data |
| Stable? | Static | Stable across time | Updates with cohorts |
| Use | Empathy / focus | Solution-agnostic targeting | Quantitative analysis |

Best practice: use all three for different jobs. Segments for analytics. Jobs for opportunity identification. Personas (research-grounded) for design conversations.

## Common failure modes

- **Persona = demographics + a stock photo** — invented detail, no research
- **Too many** — 9 personas, all designed for. No focus.
- **Forgotten** — created in Q1, never referenced again
- **Confused with users** — "we tested with 5 personas" — no, you tested with 5 users; personas are fictional
- **Demographic targeting** — "we're building for women 25–34" — better question: "what job?"

## How to build research-grounded personas

1. Interview 12–20 users, segment-spread
2. Cluster by **behavior + motivation**, not demographics
3. Name 2–4 archetypes that emerge
4. Each archetype: jobs (verbatim from interviews), goals, frustrations, current solutions, anti-goals
5. Include quotes
6. Re-validate every 6 months

A persona built this way is a *summary of research*, not a fiction.

## See also

- [Jobs To Be Done](jobs-to-be-done.md) — the alternative framing
- [User interviews](user-interviews.md) — the only legitimate source for personas
- [Customer journey maps](customer-journey-maps.md) — usually anchored to a persona
