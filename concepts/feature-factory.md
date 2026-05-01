# Feature Factory

> Term popularized by John Cutler. The most common product anti-pattern at scale.

## Definition

An organization that measures success by **features shipped**, not by **outcomes achieved**. Optimizes throughput at the cost of value.

## Cutler's diagnostic checklist (paraphrased)

You're in a feature factory if:

1. ✅ No measurement of post-ship impact ("we shipped it, on to the next one")
2. ✅ Rapid shuffling of priorities — roadmap changes weekly
3. ✅ Obsession with "velocity" — story points, throughput, sprint output
4. ✅ Ship-celebrating culture (launch parties; no "we killed a bad idea" parties)
5. ✅ Roadmap is a list of features with dates, not bets with outcomes
6. ✅ Long backlog of unprioritized "stakeholder asks"
7. ✅ Engineers/designers don't talk to users
8. ✅ "Discovery" means writing specs faster
9. ✅ Big-batch releases ("Q4 launch") with no mid-cycle learning
10. ✅ Success = shipped on time, on scope. Outcome unmeasured.

Three or more = feature factory.

## How it forms

No one designs a feature factory. They emerge:

```
Pressure to ship
   → roadmap as commitment
      → specs over discovery
         → feature counts as success metric
            → teams optimize counts
               → outcomes ignored
                  → company misses revenue
                     → exec response: "ship more"
                        → loop tightens
```

The exec response is the trap. Faced with declining revenue, the instinct is more output. The cure is more *discovery*. The cost of discovery is short-term throughput, which the org has been measuring for years. So the cure looks like the disease.

## Symptoms in the wild

- "We shipped 47 features last quarter and revenue was flat. Must mean we need to ship more."
- "Engineers asked to attend user interviews; declined as 'not their job.'"
- "PM asked 'what outcome will this move?' — exec response: 'just build it.'"
- Roadmap document is a Gantt chart of features.
- OKR key results are feature names with dates.
- Promotion criteria reward shipping, not impact.

## The harm

- **Customer harm** — products bloat with features users didn't want
- **Engineering harm** — burnout from churn, low morale from building unused things
- **Product harm** — no learning compounds; the org gets dumber over time
- **Business harm** — revenue eventually misses; companies die or get disrupted

## Escape routes

(In approximate order of feasibility for a single PM/team.)

1. **Measure post-ship outcomes anyway** — even if not asked. Build a quiet record.
2. **Rephrase one feature as an outcome** — "ship onboarding" → "increase 7-day activation 5%"
3. **Run one experiment** — kill one feature in discovery before building. Document the savings.
4. **Bring eng/design to one user interview** — they convert fast.
5. **Replace one roadmap quarter with bets** — "we'll move metric X by Y%" instead of feature list.
6. **Get an executive sponsor** — without exec air cover, escape attempts get reverted.

Full cultural shift requires senior leadership commitment. No PM single-handedly converts a feature factory; they can demonstrate proof-of-concept on one team.

## Adjacent / related

- **Roadmap roulette** — features added/dropped weekly with no logic
- **Bus factor of one** — only the loudest exec's ideas get built
- **Stakeholder-driven dev** — prioritization = whoever asked loudest
- **Output theater** — performative shipping for visibility

## See also

- [Outcomes vs outputs](outcomes-vs-outputs.md) — the philosophical antidote
- [Feature vs product team](feature-vs-product-team.md) — the org-shape antidote
- [Empowered team](empowered-team.md) — the staffing-model antidote
- [Roadmap trap](roadmap-trap.md) — the artifact that perpetuates feature factories
- [HiPPO](hippo.md) — the decision-making pattern feature factories run on
