# HiPPO

> **H**ighest **P**aid **P**erson's **O**pinion. Coined by Avinash Kaushik (Google Analytics evangelist, ~2006). The decision-making pattern in which the most senior person in the room overrides evidence.

## The pattern

```
  Evidence: 5 user interviews say feature X is confusing
  Data:     usage drops 12% post-launch
  PM:       recommends rollback

  CEO (in meeting): "I think it's fine. Let's keep it."

  → feature stays. Evidence ignored.
```

Repeat over months → team learns to predict what the HiPPO wants → discovery becomes theater.

## Why it persists

- **Hierarchy bias** — senior = right, in many cultures
- **Loss aversion** — disagreeing with execs is career risk
- **Evidence is uncomfortable** — data showing "your idea is wrong" is socially expensive
- **Speed framing** — execs say "we don't have time to test, just ship"
- **Genuine intuition** — sometimes the senior person *is* right; the team can't tell which times

## Why it's destructive

Even when the HiPPO is right 60% of the time, the system has no way to learn. The team can't:
- Build calibration ("how often is exec X right?")
- Evolve good ideas through disagreement
- Hold anyone accountable for outcomes (the HiPPO doesn't get measured against their picks)
- Develop junior judgment (everyone defers, nobody learns)

## Telltale signs

- Decisions reverse based on which exec is in the room
- Junior PMs frame ideas in language the HiPPO will accept rather than the strongest case
- "Strong opinions, weakly held" turns into "weak opinions, strongly held by whoever has the title"
- The phrase "[Exec] mentioned in passing that…" drives major work
- Post-mortems blame individual contributors when the bet was a HiPPO call

## Counter-mechanisms

### 1. Pre-commit to the test

Before discussing the result, agree on the criterion:
> "If post-launch retention drops more than 5%, we roll back."

Now the HiPPO has to override a *pre-agreed* decision rule, which is harder politically.

### 2. Measure the HiPPO's track record

Quietly. Privately. Many discover their senior decisions are 50/50. This is informative if you survive long enough to use it.

### 3. Reframe as bets

"This is a bet. We expect outcome Y. We'll measure at T+30 days." Forces the HiPPO to acknowledge the experimental frame.

### 4. Outcome ownership

If the HiPPO overrides, they own the outcome. Document. ("Per [exec] decision on [date], we proceeded with X. Result: Y.") This rarely happens explicitly but the trail is real.

### 5. Strong product leadership

The product head's job is partly to absorb HiPPO pressure so the team doesn't. If your PM/CPO doesn't push back on the CEO, no one will.

## When the HiPPO is right

It happens. Senior people often have:
- Pattern-matching from prior products/markets
- Information teams don't see (financial pressure, partnership deals)
- Strategic intuition that's hard to articulate

The fix isn't "ignore execs". It's "make sure their input is one input among several, not the override."

## Cultural antidotes

- **Disagree and commit** (Amazon) — frame disagreement as healthy, then align once decided
- **Strong opinions, weakly held** (Saffo) — confidence to argue, humility to update
- **Evidence-first reviews** — the meeting opens with data, not the loudest voice
- **Anonymous pre-reads** — Amazon-style 6-pagers; everyone reads silently before speaking

## See also

- [Feature factory](feature-factory.md) — HiPPO is the engine
- [Outcomes vs outputs](outcomes-vs-outputs.md) — outcomes make HiPPO calls measurable
- [Empowered team](empowered-team.md) — the org-design antidote
