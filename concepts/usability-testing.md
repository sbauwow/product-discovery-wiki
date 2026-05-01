# Usability Testing

> The canonical UX research method. Watch a user attempt a task; learn where they struggle. Older than the web (Jakob Nielsen formalized it in the 90s); still the highest-leverage UX method ever.

## The mechanic

```
1. Pick a task ("buy a pair of shoes in your size")
2. Recruit 5 users matching the target segment
3. One at a time: user sits with a prototype/product
4. Moderator asks them to attempt the task
5. User THINKS ALOUD as they work
6. Moderator observes silently, asks neutral probing questions
7. Take notes on points of confusion, friction, error
8. Synthesize: top 3-5 issues across users
```

**The user does the task. You watch. You don't help.**

## Think-aloud protocol

The single most useful technique. Ask the user to **narrate their thoughts continuously**:

> "Tell me what you're thinking as you go. What you're looking at, what you're trying to do, what you expect to happen."

Why it works:
- Surfaces *mental models* in real time
- Reveals *expectations* that differ from your design
- Catches confusion before the user resolves it silently
- Distinguishes "I figured it out eventually" from "this is intuitive"

Without think-aloud, you only see *outcomes* (succeeded / failed). With it, you see *why*.

## Sample size: Nielsen's 5

Jakob Nielsen's empirical finding (1993):

```
% of usability problems found ≈ 1 - (1-L)^N
where L = % a single user finds (~31% empirically)
      N = number of users
```

| N users | % of problems found |
|---|---|
| 1 | 31% |
| 3 | 67% |
| 5 | 85% |
| 10 | 97% |
| 15 | 99% |

**Five users find ~85% of major issues.** Diminishing returns past 5 in a single round. Better to run *more rounds of 5* (test → fix → re-test) than *one round of 15*.

Caveat: Nielsen's 5 finds *common* problems. Edge-case or accessibility issues may need more users. For different segments, use 5 *per segment*.

## Moderated vs unmoderated

| | Moderated | Unmoderated |
|---|---|---|
| Setup | Live session w/ moderator | User self-completes asynchronously |
| Cost | Higher (~$200-500/user) | Lower (~$50-100/user) |
| Speed | Slower (scheduling) | Faster (24-48h turnaround) |
| Probing | Can ask follow-ups | Pre-scripted only |
| Edge cases | Captures unexpected behavior | Misses anything not pre-scripted |
| When | Complex tasks, novel UIs | Validating known designs |

Use moderated for *learning*. Use unmoderated for *validation*.

## What you're looking for

Categorize observations by severity:

| Severity | Definition | Action |
|---|---|---|
| **Critical** | User cannot complete task | Fix before ship |
| **Major** | User completes but with significant struggle | Fix in current cycle |
| **Minor** | User notices but proceeds | Backlog, fix later |
| **Cosmetic** | User barely notices | Often ignore |

A test producing *zero* issues usually means the test is wrong (too easy, biased moderator, wrong users) — not that the design is perfect.

## Common moderator mistakes

### 1. Helping the user
The single biggest sin. The moment you say "click that button there", the test is over. Sit on your hands.

### 2. Leading questions
- ❌ "Was that confusing?"
- ✅ "What were you thinking just now?"

### 3. Defending the design
- ❌ "Well, it's there because..."
- ✅ "Tell me more about what you expected."

### 4. Stacking questions
- ❌ "Why did you click that, what were you looking for, did you see the menu?"
- ✅ One question, then silence.

### 5. Silent moderator
The other extreme. Some probing is essential to surface *why*, not just *what*.

## Test design

A good test plan:

```
RESEARCH GOAL: What we want to learn (e.g. "Can users find the export feature?")

TASKS (3-5, ordered):
1. "You've been working on this dashboard. You want to send the data to your CFO. Walk me through how you'd do that."
2. ...

OBSERVATIONS TO COLLECT:
- Time to complete
- Errors / wrong paths
- Verbal frustration / confusion
- Quotes about expectations
- Final emotional state

RECRUITMENT:
- 5 users
- Segment: existing users, weekly+ active
- Excluded: prior beta testers
```

Tasks should be **goal-shaped** ("you want to send data to your CFO"), not **feature-shaped** ("click the export button"). Feature-shaped tasks bypass the test.

## Tools

- **Maze** — async unmoderated, prototypes
- **UserTesting / Userlytics** — moderated + unmoderated, panel-based
- **Lookback** — moderated, real-time observer access
- **Useberry** — async, lighter
- **Dovetail / Notably** — synthesis tools (not testing platforms)
- **Zoom + screen share + recording** — DIY, fine for moderated

## Connection to other discovery work

| Method | Purpose |
|---|---|
| [User interviews](user-interviews.md) | What users *think and do* in their lives |
| Usability testing | What users *can do* with your product |
| [A/B testing](ab-testing.md) | What users *actually do* at scale |
| [Five-second test](five-second-test.md) | What users *understand* at first glance |

These complement; they don't substitute. Usability testing tells you *why* an A/B test result happened — A/B testing tells you which variant *won at scale*.

## Common failure modes

- **Testing the wrong users** — "we tested with our team" — biased panel
- **Testing too late** — running usability tests on production code where fixes are expensive
- **One-shot testing** — one round, ship, no iteration; misses fixed issues' downstream effects
- **Confirmation bias** — picking tasks the design handles well; avoiding the broken flows
- **Ignoring qualitative signal** — "5 users used it, must be fine" — but they all hated it
- **Confusing usability with usefulness** — usability test confirms users *can* use it; doesn't confirm they *want* to (that's [interviews](user-interviews.md) and [A/B testing](ab-testing.md))

## See also

- [User interviews](concepts/user-interviews.md) — adjacent qualitative method
- [Five-second test](concepts/five-second-test.md) — usability for first-impression specifically
- [Prototyping](concepts/prototyping.md) — what you usually test
- [Heuristic evaluation](concepts/heuristic-evaluation.md) — expert review without users (cheap pre-test pass)
- [Tree testing](concepts/tree-testing.md) — usability for IA specifically
