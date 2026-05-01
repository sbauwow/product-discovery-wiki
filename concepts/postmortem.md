# Postmortem (Blameless)

> Sources: Google SRE book (2016) for the modern blameless variant; Etsy's "Blameless PostMortems and a Just Culture" (2012). Originally an incident-response practice; increasingly applied to product launches, failed bets, and organizational learning.

## The shape

```
1. The incident / failure happens
2. Resolve immediately (production restored, ship hot fix, etc.)
3. Within 5 days: schedule the postmortem
4. Write a postmortem document covering:
   - Summary
   - Timeline (UTC, minute-by-minute)
   - Impact (users, revenue, reputation)
   - Root cause(s)
   - Resolution + recovery
   - What went well
   - What went poorly
   - Action items (prevent + detect + mitigate)
5. Run the postmortem meeting (1-2 hours)
6. Publish broadly; track action items to completion
```

Output: a learning artifact + concrete actions. The point is not blame; it's understanding.

## The "blameless" principle

The single most-important property:

> A postmortem assumes everyone involved acted with **good intent** and made the **best decision they could** with the **information they had at the time**.

The system failed, not the person. If a human "made an error," the system that *allowed* a human error to cause damage is the real defect.

Why blameless matters:
- **Honesty** — engineers will hide mistakes if blame is attached. Hidden mistakes can't be fixed.
- **Systemic fixes** — punishing individuals doesn't prevent the next person from making the same error
- **Compounding learning** — orgs with blameless culture accumulate reliability advantages over years
- **Psychological safety** — required for engineers to take calculated risks at all

Blameless does *not* mean consequence-free. Repeated negligence, malicious behavior, or violations of clear standards still warrant consequences. But the *first* response to any incident is "what about the system allowed this?"

## Postmortem types

### Incident postmortem
Production outage, data loss, security event. Most familiar type.

### Launch postmortem
A product launch that did or didn't go as expected. Captured before context decays. Even successful launches benefit (capture what worked).

### Bet postmortem
A strategic bet (new feature, new market, pricing change) reaches its evaluation point. Did it move the metric? Why or why not?

### Learning review (retrospective)
Lighter; runs every cycle. Covers what went well, what could improve, and what to try next. See agile retrospectives.

All four use the same blameless principle. Different cadences and scope.

## The Five Whys

Adjacent technique. Sakichi Toyoda's root-cause-analysis method:

```
Problem: The site went down.
  Why? The database ran out of connections.
  Why? A bug in the new feature opens connections without closing.
  Why? The PR didn't include connection-pool tests.
  Why? The team's test framework doesn't cover database integration.
  Why? Database integration tests are slow, so they were skipped.
→ Root cause: testing infrastructure forces a tradeoff between speed and coverage.
```

Stops at the first systemic answer (not "negligence"). The fix targets the system, not the person.

Variations: 3 Whys (lighter), 7 Whys (deeper). The technique is named for "five" but the count isn't sacred — go until you reach a genuine root cause.

## Action items

A postmortem with no action items is a story. A postmortem with action items is a learning system. Each action item should have:
- **Owner** (one person, named)
- **Due date** (specific, not "ASAP")
- **Type**: prevent / detect / mitigate
- **Tracked** in the team's normal workflow

Three categories:
- **Prevent** — eliminate the condition that caused the failure
- **Detect** — surface the condition faster next time (alert, monitor, dashboard)
- **Mitigate** — reduce blast radius if it recurs (rollback automation, circuit breakers)

Mature orgs track postmortem action-item completion as a KPI. Items left open six months mean the postmortem produced no learning.

## Timeline construction

Most-skipped, most-valuable section. UTC timestamps, minute-by-minute, of:
- What happened in the system
- What humans observed
- What humans did
- When information arrived

Reveals subtleties:
- "We knew at 14:32 but didn't act until 14:51" → information flow problem
- "Alert fired at 14:00 but on-call engineer was off-duty until 14:15" → on-call rotation gap
- "Customer complaints arrived 12 minutes before our monitoring fired" → monitoring gap

Timelines surface the *system* of detection and response, not just the technical fault.

## Worked example: a product launch postmortem

Launched new pricing tier. Post-launch metrics: trial conversion *down* 15%, churn *up* 8%. Postmortem (4 weeks after launch):

**Timeline:**
- T-30 days: tier announced internally; sales trained
- T-7 days: marketing site updated; customer email sent
- T-0: tier live
- T+1: trial conversion drops 12%; assumed novelty
- T+5: confirmed downward trend; initial diagnosis = pricing issue
- T+14: identified that "team plan" CTA disappeared; users assumed no team option
- T+21: emergency fix; conversion partial recovery

**Root causes (5 whys):**
- Why did conversion drop? Team plan CTA was hidden.
- Why hidden? Pricing page redesign moved it to a tab.
- Why was the tab change shipped? It was visual cleanup; nobody flagged the funnel implication.
- Why didn't anyone flag it? PR review didn't include funnel analysis.
- Why? No process for funnel-impact review on pricing-page changes.

**Action items:**
- Prevent: Add "funnel-impact review" to all checkout/pricing PRs (owner: PM lead, due: 2 weeks)
- Detect: Add weekly auto-alert on >5% conversion-rate change (owner: data team, due: 1 month)
- Mitigate: Build dashboard with rollback playbook for pricing-page changes (owner: platform, due: 6 weeks)

No blame on the designer who shipped the cleanup. The system allowed the change to ship without funnel review. Fix the system.

## Postmortem culture indicators

Healthy:
- Postmortems written within a week of incidents
- Action items tracked to completion
- Engineers volunteer information about mistakes
- Repeated similar incidents are rare (compounds learning)
- Junior engineers attend and participate

Unhealthy:
- Postmortems delayed for weeks
- Action items written but ignored
- Engineers hide errors / blame other teams
- Same incidents recur
- "Postmortem" is a career-ending event (people refuse to participate)

## When postmortems apply outside ops

Increasingly applied to:
- Failed product bets ([why didn't the OKR move?](okrs.md))
- Failed launches
- Pivots / strategy shifts
- Hire / fire decisions in retrospect
- M&A integration

The blameless principle scales. The mechanic adapts.

## Common failure modes

- **Blame culture** — postmortem becomes a search for the responsible person; everyone defends themselves; no learning
- **Post-mortem theater** — write the document, hold the meeting, never act on items
- **Skip the timeline** — jump to "root cause" without minute-by-minute reconstruction; misses systemic insight
- **One-shot 5 whys** — stops at "person X did Y" instead of asking what allowed it
- **Action-item soup** — 30 items, none owned, none tracked
- **No publishing** — postmortem stays in private channel; lessons don't propagate
- **Skipping success postmortems** — only failures get postmortems; can't capture what worked

## Connection to discovery

Postmortems on **product bets** are an underused practice. After a launched solution proves out (or doesn't), most teams ship the next thing. A bet-postmortem asks:

- Did the metric move as predicted? Why / why not?
- What discovery did we miss?
- What [assumptions](assumption-mapping.md) did we test correctly? Which did we get wrong?
- What changes the next bet's design?

Without bet-postmortems, [discovery practice](continuous-discovery.md) doesn't compound. Each bet is independent. With bet-postmortems, the team's discovery quality improves cycle over cycle.

## See also

- [Premortem](concepts/premortem.md) — the prospective cousin (imagine failure *before* it happens)
- [Innovation accounting](concepts/innovation-accounting.md) — formalizes the bet-postmortem cycle
- [Cynefin](concepts/cynefin.md) — bet-postmortems most useful in Complex domain (where outcomes are uncertain)
- [Strong PM](concepts/strong-pm.md) — running good postmortems is a senior-PM skill
