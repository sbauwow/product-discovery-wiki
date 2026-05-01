# Card Sorting

> Information architecture (IA) research method. Users group items into categories; researcher observes how *they* organize the content. Surfaces the user's mental model — which often differs sharply from the org's mental model.

## The mechanic

```
1. Prepare cards (50-100 items, one per card): features, content, navigation labels
2. Recruit 15-30 users from target segment
3. Each user, individually:
   a. Sorts cards into groups that "make sense to them"
   b. Names each group
   c. (Optional) Re-sorts at higher level
4. Researcher records: groupings, group names, items participants struggled with
5. Synthesize: cluster the cluster patterns across users
```

The output: a user-derived information architecture, contrasted against the org's IA.

## Three variants

### 1. Open card sort
- Users create their own categories.
- Output: groupings AND group labels — both organic.
- Use when: you have *no* prior IA, or you want to learn user mental models.

### 2. Closed card sort
- Categories pre-defined by you.
- Users assign each card to one of your categories.
- Output: how *your* categories perform; mismatches and unclassifiable items.
- Use when: you have a candidate IA and want to validate or compare options.

### 3. Hybrid
- Pre-defined categories *plus* a "create your own" option.
- Surfaces both fit-with-your-IA AND missing categories.

## When card sorting is the right tool

✅ Designing or redesigning navigation
✅ Categorizing a content library (knowledge base, docs, marketplace)
✅ Surfacing user mental models for a domain
✅ Resolving stakeholder disagreement about IA ("users will think of it as X")

## When it's not

❌ Validating a specific UI flow (use [usability testing](usability-testing.md))
❌ Discovering user *needs* (use [interviews](user-interviews.md), [JTBD](jobs-to-be-done.md))
❌ Page-level layout decisions
❌ When you have <30 items (overhead exceeds value)

## Sample size

| # users | Confidence |
|---|---|
| 5-10 | Directional, suggestive |
| 15-30 | Robust patterns emerge |
| 30+ | Diminishing returns; quantitative analysis possible |

Most studies use **15-20** for a single segment. Multi-segment? Run 15 *per segment*.

## What you'll see

### Strong patterns (most users group similarly)
- "Settings" cards clearly cluster; users name the group "Settings" or "Account"
- → IA decision is easy: this is a Settings section.

### Weak patterns (users disagree)
- A card like "Saved Templates" gets sorted into "Files", "Settings", "Tools" by different users
- → ambiguous label; the *concept* doesn't have a clear mental home for users
- → action: rename, split, or relocate

### Unclassifiable items
- A card no user knows where to put — usually a feature with unclear value or weird naming
- → action: simplify or drop

### Clusters that surprise you
- Users group "Export PDF" and "Print" together (output)
- Org categorizes them as "File" and "Tools" (action type)
- → user mental model is "what do I do with output", not "what kind of action"
- → IA implication: rethink primary navigation

## Tools

- **OptimalSort** (most-used) — moderated and unmoderated, online, statistical analysis
- **UserZoom / Lyssna** — bundled with broader UX research suites
- **UXtweak** — newer, similar features
- **DIY** — physical index cards or sticky notes, in-person; expensive but rich

## Synthesis

Card-sort data produces a co-occurrence matrix:

```
                  Settings  Files  Tools  Other
Saved Templates    35%      28%    25%    12%   ← split mental model
Profile            85%       2%     1%    12%   ← clearly Settings
Export PDF          5%      30%    50%    15%   ← weakly Tools
Notifications      60%      8%     5%    27%   ← split between Settings & Other
```

Most platforms render this as a **dendrogram** (cluster diagram) showing which items "want to be" near each other.

## Worked example: redesigning a B2B SaaS navigation

Existing IA (org's mental model):
```
Dashboards | Data | Models | Insights | Settings
```

Open card sort with 22 users yields clusters:
```
"Things I look at"    "Things I configure"   "Things I send"
- Dashboards          - Models                - Reports
- Charts              - Settings              - Exports
- Insights            - Permissions           - Subscriptions
- Reports (?)         - API keys
```

User mental model is **verbs** ("look at", "configure", "send"), not the org's nouns ("dashboards", "data"). Some items move (Reports → "send" not "look at"). Some categories merge (Insights with Dashboards).

Implication: top-level nav should reflect verbs, or at least feel verb-shaped.

## Common failure modes

- **Too many cards** — 100+ exhausts users, sort quality drops
- **Too few cards** — <30 doesn't surface meaningful clustering
- **Vague card labels** — users don't know what the card is, can't sort it (e.g. "API Configurator" without context)
- **Wrong users** — power users sort differently than newcomers; specify segment
- **Treating result as authoritative IA** — card sort is one input. Combine with [tree testing](tree-testing.md) on a candidate IA, [usability testing](usability-testing.md) on the live nav.
- **Open sort with 50 users** — high effort, high noise; closed sort or hybrid scales better

## Card sort vs tree testing

These are sister techniques:
- **Card sort** = generative ("how would users group these?")
- **[Tree testing](tree-testing.md)** = evaluative ("can users find X in this proposed IA?")

Workflow:
```
Card sort → derive candidate IA → tree test it → iterate → ship → A/B test
```

Card sort produces hypotheses about IA; tree testing validates them.

## See also

- [Tree testing](concepts/tree-testing.md) — the evaluative companion
- [Usability testing](concepts/usability-testing.md) — broader UX research method
- [Personas](concepts/personas.md) — different segments may sort differently; segment your card sort accordingly
- [User interviews](concepts/user-interviews.md) — surface mental models qualitatively before card-sorting
