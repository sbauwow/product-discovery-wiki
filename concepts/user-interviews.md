# User Interviews

> The most common discovery activity. Done well, the highest-leverage. Done badly, actively harmful.

## The fundamental rule

> **Probe past behavior. Don't ask about the future.**

Humans are bad at predicting their own future behavior. They are excellent at narrating what they actually did last Tuesday. Every good interview technique flows from this.

| ❌ Don't ask | ✅ Ask instead |
|---|---|
| Would you use a feature that did X? | Tell me about the last time you tried to do X. |
| Would you pay $20/month for this? | What did you spend money on last month to solve this? |
| Do you like the new design? | Walk me through what you did when you opened it yesterday. |
| What features do you want? | What was the last thing that frustrated you in our product? |

## Interview structure (generic 30-min)

```
0-5    Rapport + permission to record
5-10   Context: their role, goals, current setup
10-25  Past-behavior probe: "tell me about the last time..."
25-28  Open: "what didn't I ask that I should have?"
28-30  Wrap: thank, incentive, next-step ask
```

## Probing techniques

When the user says something interesting:
- **"Tell me more about that."** — neutral expansion
- **"What happened next?"** — timeline forward
- **"Walk me through that."** — get specifics
- **Silence** — count to 5; users fill the gap with the most honest detail
- **"Why?"** — but sparingly; can feel interrogative

## What to avoid

- **Leading questions** — "Don't you think the navigation is confusing?" (you've answered for them)
- **Hypotheticals** — "If we built X, would you...?" (they'll say yes; they're being polite)
- **Stacked questions** — three questions in one breath; user answers the easiest
- **Pitching** — describing your solution mid-interview. The interview is over once you do.
- **Confirmation seeking** — interpreting any positive signal as validation

## Sample size

For qualitative discovery: **5 users per segment** finds ~85% of major issues (Nielsen). Diminishing returns past ~12 in a single round.

For quantitative validation: depends on effect size. Most discovery is qualitative; if you need stats, run a survey or A/B test, not an interview.

## Interview types

| Type | Goal | Length | When |
|---|---|---|---|
| **Generative** | Find new opportunities | 45–60 min | Top of OST, exploratory |
| **Switch interview ([JTBD](jobs-to-be-done.md))** | Understand a purchase decision | 60 min | Buyer/segment understanding |
| **Usability test** | Find UX problems | 30–45 min | Solution validation |
| **Concept test** | Reaction to prototype | 30 min | Solution validation |
| **Customer/Win-loss** | Why they bought / didn't | 30–45 min | Sales-cycle insight |

## Recording & synthesis

- **Record** (with permission) — humans miss things in real time
- **Tools**: Otter, Grain, Dovetail, Notably
- **Synthesis cadence**: same day or next day. Memory decays fast.
- **Output**: opportunities for the [OST](opportunity-solution-tree.md), not "interview notes"

## Recruiting

The hardest part. Sources:
- In-app intercept (active users)
- Email panel (existing users who opted in)
- CRM warm intros (sales/CS team)
- Panel services (User Interviews, Respondent.io, dscout) — fast but expensive
- Personal network — for early-stage, fastest signal

Always pay. $50–$100 typical. Free interviews skew toward the over-helpful, who give bad data.

## Anti-patterns

- **PM-only interviews** — engineer/designer don't hear what they need to ([continuous discovery](continuous-discovery.md) prescribes the trio)
- **Interviewing only happy users** — survivorship bias; talk to churned users too
- **No update to artifact** — if the [OST](opportunity-solution-tree.md) doesn't change, the interview was theater
- **One-shot research** — quarterly studies forget context between rounds

## See also

- [Continuous Discovery](continuous-discovery.md) — the cadence
- [Jobs To Be Done](jobs-to-be-done.md) — switch interviews specifically
- [Solutioning trap](solutioning-trap.md) — the most common interview failure
