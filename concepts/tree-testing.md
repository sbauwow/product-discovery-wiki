# Tree Testing

> Information architecture (IA) **validation** method. Given a navigation hierarchy and a task, can users find the right item? Tests *findability* in isolation from visual design. Sister to [card sorting](card-sorting.md): card sorting generates IA candidates; tree testing evaluates them.

## The mechanic

```
1. Prepare: a tree (text-only nav hierarchy, no design)
2. Define tasks: "Find the section where you'd update your billing info"
3. Recruit 30-50 users
4. For each user, for each task:
   a. Show only the tree (a list of links, expanding by click)
   b. User clicks through, attempting to find the target
   c. Record: success/fail, path taken, time, backtracks
5. Analyze: per-task success rate, common wrong paths, abandonment points
```

Critical property: the tree is **text-only**. No icons, no design, no visuals. Tests pure label clarity and structure.

## Why text-only matters

A real navigation has:
- Visual hierarchy (size, color, position)
- Icons (Settings gear, etc.)
- Search bar, breadcrumbs, autocomplete
- Mouseover hints

Each can mask poor IA. A bad nav with great icons can still be findable. But icons are downstream — *first* the labels and structure should work, *then* visual design polishes.

Tree testing strips all that away. If users can't find "Update billing" in pure text, no icon will save you.

## Sample size

Tree testing is more quantitative than [card sorting](card-sorting.md):

| # users | Use case |
|---|---|
| 30 | Minimum for stat-significant findability |
| 50 | Robust per-task data, narrow CIs |
| 100+ | Comparing multiple tree variants |

For comparing two trees: 30+ per tree (60+ total).

## Output metrics

For each task, three numbers:

### 1. Success rate
% who found the correct destination.
- > 80% = strong findability
- 60-80% = okay, watch for friction
- < 60% = problem; redesign that section

### 2. Directness
Of those who succeeded, % who got there without backtracking.
- High success + low directness = users find it but stumble; label is unclear
- High both = easy and obvious

### 3. Time to find
Median seconds to reach the destination.
- Long times = exploration, hesitation
- Short times = confidence

A task with 90% success but 60% directness is less healthy than 90%/90% — users found it, but had to hunt.

## Failure patterns

| Pattern | Diagnosis |
|---|---|
| All users go to same wrong section | Label conflict — that section *should* have what they're looking for |
| Random wrong paths | No clear mental model; structure is bad |
| Fast wrong, slow right | Misleading top-level label that *seems* right |
| High abandonment | Path is too deep; users give up |
| Different segments take different paths | Multi-mental-model situation; consider redundant entry points |

## Worked example

Tree:
```
HOME
├── PRODUCTS
│   ├── Hardware
│   ├── Software
│   └── Services
├── ACCOUNT
│   ├── Profile
│   ├── Subscriptions
│   └── Preferences
└── SUPPORT
    ├── Help center
    ├── Contact
    └── Status
```

Task: "Find where to update your credit card."

Results across 50 users:
```
ACCOUNT > Subscriptions     58%  ← target, partial success
ACCOUNT > Profile           22%  ← wrong; users assume billing in Profile
ACCOUNT > Preferences        8%
SUPPORT > Help center        6%
PRODUCTS > Services          4%
Abandoned                    2%

Success rate: 58%
Directness: 71%
```

Analysis:
- 30% of users went to ACCOUNT > Profile thinking that's where billing lives
- The label "Subscriptions" doesn't unambiguously include "credit card"
- Implications: rename "Subscriptions" → "Billing & Subscriptions", or split into separate items

A tree test with this signal would block ship. The same site visually-launched with icons might pass surface usability testing while still hiding billing from 42% of users.

## Tools

- **Treejack** (Optimal Workshop) — most popular
- **Lyssna / UsabilityHub** — bundled with broader UX research
- **UserZoom / UXtweak** — enterprise-grade
- **DIY** — possible with a click-through prototype, but harder to analyze

## When to use

✅ Validating a proposed IA before visual design starts
✅ Comparing two candidate IAs (A/B-style)
✅ Diagnosing why users complain about navigation
✅ Post-launch: confirming real findability matches expected
✅ Internal-tool nav redesigns (often skipped, often bad)

## When not

❌ Brand-new product with no IA hypothesis (use [card sorting](card-sorting.md) first)
❌ Testing visual design or interaction patterns
❌ Sub-page layout decisions
❌ Highly search-driven products where nav is secondary

## Tree testing in the IA workflow

```
1. Discover: [card sorting](card-sorting.md) — what's the user mental model?
2. Synthesize: design candidate IA based on cluster patterns
3. Validate: tree testing — can users find things?
4. Iterate: based on tree-test failures, adjust labels/structure
5. Re-validate: tree test again
6. Build: implement with visual design
7. Confirm: [usability testing](usability-testing.md) on the real product
8. Scale-validate: [A/B testing](ab-testing.md) post-launch
```

Card sort and tree test are upstream of design. Skipping them means you discover IA problems at the most-expensive stage (after launch).

## Common failure modes

- **Visual aids in the tree** — defeats the point; users navigate via icons, not labels
- **Leading task language** — "Find Subscriptions" tells the user the answer
- **Tasks too generic** — "find the billing section" → users may interpret "billing" differently
- **Ignoring directness** — 100% success rate with 30% directness = users find it but hate the journey
- **Single-tree testing** — without comparison, you don't know if your tree is good or just acceptable
- **Wrong segments** — testing with internal employees who already know the IA

## See also

- [Card sorting](concepts/card-sorting.md) — generative companion (what should the tree be?)
- [Usability testing](concepts/usability-testing.md) — tests the live UI; tree test is upstream
- [Five-second test](concepts/five-second-test.md) — first-impression sister
- [A/B testing](concepts/ab-testing.md) — post-launch validation of IA changes
