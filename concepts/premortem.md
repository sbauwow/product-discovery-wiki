# Premortem

> Source: Gary Klein, *The Power of Intuition* (2003), Harvard Business Review article 2007. A risk-surfacing exercise: imagine the project has already failed; brainstorm why. Pre-empts failures while still cheap to prevent.

## The technique

```
1. Gather the team (5-10 people involved in the work)
2. Frame: "Imagine it's [end of project]. The project has FAILED catastrophically.
   The press release is bad. We've been called to a postmortem. What happened?"
3. Each person silently writes ALL the reasons it failed (10 min)
4. Round-robin share: each person reads one reason at a time
5. Cluster the reasons; identify themes
6. Top 3-5 risks → each gets a mitigation owner + plan
7. Re-run mid-project if the risk picture changes
```

That's it. 60-90 minutes. Output: a prioritized, owned risk list.

## Why imagining failure works

Klein's research on decision-making found that **prospective hindsight** (imagining a future event has already happened) increases the team's ability to identify possible reasons by 30%.

```
"What could go wrong?"           → vague, abstract list
"It went wrong. Why did it?"     → concrete, specific reasons
```

The framing matters. The first elicits cautious hedging. The second forces narrative — and narratives surface specific risks. Saying "the launch failed because we didn't anticipate X" feels different from "X might fail."

## Why teams resist it

Three common objections:

### 1. "It's negative"
Imagining failure feels demotivating. Team morale!

Counter: assuming success is what's actually risky. Premortem doesn't predict failure; it identifies what would *cause* failure if not addressed. That's how teams ship successfully.

### 2. "We've already done risk planning"
Most "risk planning" produces a generic risk list (timeline slip, scope creep, dependency block) that nobody acts on. Premortem produces *specific*, *actionable*, *prioritized* risks tied to *this* project's context.

### 3. "Founders / leaders don't want to hear it"
Usually the most senior person should run it. Their participation legitimizes surfacing concerns the team usually self-censors.

## When to run a premortem

✅ Before a major launch
✅ At project kickoff (~week 1)
✅ Before a significant strategic bet
✅ When the team feels overconfident
✅ Before a deadline crunch (when bias toward optimism is highest)
✅ Before [PR/FAQ](pr-faq.md) finalization for a launch

## When less useful

❌ Tactical decisions (overkill)
❌ Teams below ~5 people (too few perspectives)
❌ Highly junior teams without context (premortems require some domain knowledge)
❌ Routine work with known patterns

## Worked example: launching a new pricing tier

Team gathers a week before pricing change rollout. Premortem prompt:

> "It's three months from now. The pricing change has been a disaster. Customers are angry. Churn spiked. Sales reps are frustrated. Our reputation is damaged. The CEO is asking what went wrong. What's our answer?"

Silent brainstorm; 5 people generate ~40 reasons. Clustering produces themes:

| Theme | Specific risks | Mitigation owner |
|---|---|---|
| **Existing customer rage** | Grandfathering policy unclear; perception of price hike for loyalty; CS team blindsided | PM: write grandfathering FAQ; train CS this week |
| **Competitor exploitation** | Competitor runs "price-stable" campaign capturing churned users | Marketing: monitor churn destination; prep counter-message |
| **Sales team confusion** | New tier overlaps with old; sales can't explain; deals stall | Sales lead: 30-min training + 1-pager |
| **Tech rollout failures** | Old plans don't migrate cleanly; double-billing; permission errors | Eng: full migration test on staging before rollout |
| **Wrong segments hit hardest** | Power users on legacy plans pay more; advocates churn | PM: segment-specific email + retention offer |

Five owned mitigations. Project still launches in a week. Each mitigation pre-empts a likely-bad outcome.

Without the premortem, ~3 of these 5 would have gone unaddressed and become real failures.

## Premortem vs other techniques

| | Premortem | [Postmortem](postmortem.md) | Risk register | [Assumption mapping](assumption-mapping.md) |
|---|---|---|---|---|
| When | Before action | After incident | Throughout project | Before/during discovery |
| Frame | Imagined failure | Actual failure | Generic risks | Untested beliefs |
| Output | Prioritized risks + owners | Lessons learned | Risk log | Test plan |

Premortem is closest to assumption mapping. Both surface unknowns; both produce action items. Difference: premortem is **outcome-framed** (imagine the bad outcome), assumption mapping is **input-framed** (which assumptions could be wrong). Use premortem for project risk; assumption mapping for solution validity.

## Premortem variants

### "Pre-parade"
Klein's positive variant. Imagine the project is wildly successful; what made it work? Less common; useful for surfacing unrecognized success factors.

### "Murder boarding"
Military / consulting practice. A panel deliberately tries to attack the plan's weak points. Adversarial framing.

### "Red team / Blue team"
Cybersecurity origin, applied broadly. One team designs; another team attacks. Continuous, not one-shot.

### "Devil's advocate"
Lighter version. One person assigned to argue against the plan. Less structured than full premortem; can be rotated meeting-to-meeting.

## The "10x bigger team" caveat

Klein noted: small teams (3 people) sometimes can't generate enough perspectives. Premortems benefit from **diversity of role** — PM, design, eng, sales, CS, exec all see different failure modes.

For solo work or pair work, the technique is weaker. Add someone outside the project for fresh perspective.

## Common failure modes

- **Generic risks list** — "the timeline could slip" — too abstract; demand specifics
- **Premortem theater** — runs the exercise but doesn't follow through with mitigations or owners
- **Senior person dominates** — silent brainstorm step is critical; round-robin sharing prevents anchoring on first speaker
- **No follow-through** — premortem identifies risks; nobody owns mitigation; risks materialize anyway
- **One-shot premortem** — risk picture changes mid-project; re-run at major milestones
- **Treating risks as immutable** — sometimes a surfaced risk *should* kill the project, not be mitigated. Be willing to act on what surfaces.

## In product discovery

Premortems are particularly useful in [discovery](continuous-discovery.md):

- **Before launching a [RAT](rat.md)** — what could cause us to misread the test result?
- **Before a major [bet](opportunity-solution-tree.md) is committed** — what would make this bet fail?
- **Before crossing into delivery** — what could go wrong in implementation that discovery missed?

Pair with [assumption mapping](assumption-mapping.md): premortem surfaces *outcome-failures*; assumption mapping surfaces *input-falsifications*. Both useful, slightly different.

## See also

- [Assumption mapping](concepts/assumption-mapping.md) — adjacent risk-surfacing tool
- [PR/FAQ](concepts/pr-faq.md) — premortem on the press release before writing it
- [RAT](concepts/rat.md) — premortem identifies which assumption to test first
- [Cynefin](concepts/cynefin.md) — premortems work best in Complex domain (where outcomes uncertain)
