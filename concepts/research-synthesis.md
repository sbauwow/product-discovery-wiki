# Research Synthesis

> Discovery does not fail only because teams gather bad evidence. It also fails because teams gather good evidence and never convert it into decisions. Synthesis is the discipline of turning messy notes, quotes, recordings, and observations into patterns, opportunities, and choices.

## Core thesis

Research collection answers:
> What did we hear? What did we observe?

Research synthesis answers:
> What does it mean? What should change?

Without synthesis, interviews become theater:
- lots of notes
- lots of quotes
- little change in strategy, OST, roadmap, or experiments

Good synthesis compresses many observations into a smaller set of actionable truths.

## What synthesis is not

- ❌ a transcript archive
- ❌ a folder full of clips
- ❌ a slide deck of quotes
- ❌ "top 10 feature requests"
- ❌ one PM's vibes after the call

Those may be inputs. They are not synthesis.

## The output of synthesis

A good synthesis pass should produce some combination of:
- recurring themes
- user problems phrased clearly
- evidence-backed opportunities
- contradictions worth investigating
- segment differences
- implications for strategy / ICP / positioning
- assumptions to test next

The output is not "notes complete."
The output is: the team now sees the problem space more clearly.

## Why synthesis is hard

### 1. Raw research is noisy
Users ramble, contradict themselves, forget details, and speak in solution-shaped language.

### 2. The human brain overweights vivid anecdotes
One dramatic quote can dominate ten quieter but more important patterns.

### 3. Teams jump too early to solutions
Before the pattern is clear, someone says:
> We should add a dashboard.

Now the synthesis has been polluted by solution gravity.

### 4. Researchers often stop at description
They summarize what happened, but never elevate it into opportunities or decisions.

## The synthesis ladder

Think of synthesis as moving up a ladder:

```
RAW DATA
(transcripts, notes, clips)
        ↓
OBSERVATIONS
(specific things seen/heard)
        ↓
PATTERNS
(repeated signals across users)
        ↓
INSIGHTS
(why the pattern matters)
        ↓
OPPORTUNITIES / DECISIONS
(what the team should explore, test, or change)
```

Many teams stop at observations.
Strong teams climb to insight and action.

## Observation vs pattern vs insight

### Observation
A thing one user said or did.

Example:
> User 7 exported data to CSV and finished analysis in Excel.

### Pattern
A repeated behavior or issue across multiple users.

Example:
> 6 of 8 users exported data to Excel before making decisions.

### Insight
A meaning-bearing explanation or implication.

Example:
> Users do not trust the in-product analysis workflow for decision-making; they treat the product as a data source, not a decision surface.

### Opportunity
A discovery-oriented reframing of where value might be created.

Example:
> Reduce the trust gap between data visibility and decision confidence inside the product.

## Basic synthesis workflow

### Step 1. Debrief immediately
Same day if possible.

Capture:
- surprises
- strong moments
- recurring friction
- contradictions
- things that changed your mental model

Memory decays fast. Raw impression is an important input, but only one input.

### Step 2. Extract atomic observations
Break notes into small units.

Good atomic observation:
- one behavior
- one quote
- one failure point
- one workaround
- one emotional reaction

Bad:
> User liked some parts of the flow but had some issues and maybe wanted more integrations.

Too mushy.

### Step 3. Cluster by meaning
Group observations that appear related.

This is often done through **affinity mapping**:
- one observation per sticky
- cluster similar ones
- name the cluster after the pattern, not the feature

Example clusters:
- uncertainty after signup
- fallback to manual work
- low trust in automation
- need for internal sharing / proof

### Step 4. Name the pattern clearly
Pattern names should sound like real user truths.

Good:
- Users cannot tell whether setup succeeded.
- Buyers need internal proof before inviting teammates.
- Admins fear data corruption more than slow workflows.

Bad:
- onboarding
- analytics
- dashboard issues

Those are buckets, not insights.

### Step 5. Check evidence strength
Before elevating a pattern, ask:
- how many users showed this?
- from which segments?
- is it a one-off or repeated?
- did we observe behavior, or only hear opinion?
- is this strong enough to change a roadmap or just strong enough to test further?

### Step 6. Turn patterns into opportunities
Patterns become opportunities when phrased as unmet progress, pain, or desired outcome.

This is where synthesis connects to the [OST](opportunity-solution-tree.md).

### Step 7. Decide what changes
Strong synthesis always changes something:
- the OST
- the target segment
- the positioning hypothesis
- the next experiment
- the roadmap priority
- the team's understanding of the buyer

If nothing changes, either:
- the research was weak, or
- the synthesis was weak, or
- the team is ignoring the evidence.

## Affinity mapping

The canonical synthesis mechanic.

### How it works
1. Put one observation per note.
2. Put all notes on a wall / board.
3. Group by similarity of meaning.
4. Label each cluster.
5. Group clusters into larger themes if needed.

### Rules
- do not sort by feature area first
- do not force every note into a neat bucket
- let clusters emerge bottom-up before naming them
- name clusters after user reality, not internal ownership

Example:

```
RAW NOTES
- "I wasn't sure if import worked"
- user refreshed 3 times after upload
- "I usually ask support to confirm"
- user waited 2 minutes before proceeding

CLUSTER NAME
"Users do not trust import completion signals"
```

That cluster is already more useful than four isolated notes.

## Segment-aware synthesis

Not every pattern is global.

A critical synthesis question:
> Who is this true for?

Look for differences by:
- segment
- role
- maturity
- use case
- buyer vs end user
- new vs experienced user

Example:
- new users need confidence and handholding
- advanced users need control and exception handling

Blending these together creates fake average users and bad product choices.

## Strong evidence vs weak evidence

Evidence has a quality gradient.

```
Weakest                                           Strongest
opinion → stated preference → recalled behavior → observed behavior → repeated observed behavior across segment → behavioral + quantitative confirmation
```

Examples:
- "I'd love that" = weak
- "Last week I did X workaround" = better
- observed screen recording showing workaround = stronger
- same workaround repeated by 7 of 10 target users = much stronger
- matched by drop-off data in funnel = strongest

Good synthesis respects this hierarchy.

## Quant + qual triangulation

The strongest synthesis often combines:
- interviews
- session replays
- support tickets
- funnel data
- retention cohorts
- win/loss notes

Example:
- interviews say users are confused after signup
- session recordings show repeated hovering / backtracking
- funnel data shows large drop at step 2

Now you have triangulated evidence.

One source can mislead. Multiple aligned sources are much harder to ignore.

## Good synthesis questions

Ask these after every round:
- What surprised us?
- What repeated more than expected?
- What only happened in one segment?
- What contradiction do we not yet understand?
- What behavior mattered more than what people said?
- What assumption just got weaker?
- What opportunity is emerging?
- What should we stop believing now?

That last question is especially valuable.

## Turning synthesis into artifacts

### 1. OST updates
The highest-leverage destination for synthesis.

Research should add, split, merge, or reprioritize opportunities.

### 2. Insight memo
Short written output:
- context
- methods
- top patterns
- implications
- decisions / next tests

### 3. Opportunity cards
One per synthesized opportunity:
- user truth
- evidence sources
- affected segment
- confidence
- related outcome

### 4. Assumption list
What still needs testing after synthesis?

## Common failure modes

### Quote dumping
A deck full of quotes with no pattern extraction.

### Feature-request synthesis
Collapsing everything into requested features.

### Premature certainty
Seeing 3 interviews and declaring a universal truth.

### Averaging across segments
Merging different user types into one fake pattern.

### No evidence weighting
Treating all comments as equal.

### No decision linkage
Synthesis ends as a doc instead of changing strategy or experiments.

### Overfitting anecdote
One memorable user story bends the whole roadmap.

## Practical cadence

For ongoing discovery:
- after each interview: 5–10 minute debrief
- after 5–8 interviews in a segment: synthesis round
- weekly: update OST / assumptions / next tests
- monthly: publish a short insight memo

Synthesis works best as a cadence, not a quarterly cleanup operation.

## Heuristic

If your synthesis can only answer:
> What did users say?

but not:
> What changed in our understanding?

then you do not have synthesis yet.

## How this connects to the wiki

```
[user interviews](user-interviews.md)
        ↓
research synthesis
        ↓
[opportunity-solution-tree](opportunity-solution-tree.md)
        ↓
[assumption mapping](assumption-mapping.md)
        ↓
[RAT](rat.md) / experiments
```

Synthesis is the bridge between learning and choosing.

## See also

- [User interviews](user-interviews.md) — one key evidence source
- [Opportunity Solution Tree](opportunity-solution-tree.md) — where synthesized opportunities should land
- [Assumption mapping](assumption-mapping.md) — what to test once the opportunity is clear
- [Continuous discovery](continuous-discovery.md) — cadence that keeps synthesis alive
- [JTBD](jobs-to-be-done.md) — one lens for interpreting patterns
- [Power user analysis](power-user-analysis.md) — synthesis of observed high-value user behavior
