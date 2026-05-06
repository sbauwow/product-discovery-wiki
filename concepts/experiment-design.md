# Experiment Design

> Discovery quality is limited not just by what you test, but by how you test it. A bad experiment can make a bad idea look good, a good idea look bad, or teach you nothing at all. Experiment design is the discipline of creating tests that produce decision-worthy evidence.

## Core thesis

A discovery experiment is not "trying something and seeing what happens."

A discovery experiment is:
- a specific hypothesis,
- tested with a specific method,
- against a specific assumption,
- with predefined success and failure criteria,
- producing a decision.

If you skip the last two, you usually get theater instead of learning.

## What an experiment is for

Experiments exist to reduce uncertainty around one or more of the four risks:
- value
- usability
- feasibility
- viability

They do not exist to:
- create stakeholder comfort
- generate vanity evidence
- justify work already decided
- make the team feel "data-driven"

## The minimum experiment spec

Every serious experiment should answer these six questions:

1. What assumption are we testing?
2. Why is it risky / important?
3. What method are we using?
4. What result counts as success?
5. What result counts as failure?
6. What decision follows either way?

If you cannot fill all six, the design is weak.

## Hypothesis format

A strong hypothesis is specific and falsifiable.

Useful format:

```
We believe that [segment]
who [context / problem]
will [behavior]
if we [change / offer / intervention]
resulting in [expected outcome].
We'll know this is true if [predefined success criterion].
```

Example:

> We believe that new PLG SaaS users who stall during onboarding will complete setup more often if we show a task-based first step instead of a generic dashboard. We'll know this is true if activation rate improves from 28% to at least 36% without reducing week-1 retention.

Bad hypothesis:
> We think users will like the redesign.

Too vague. Not falsifiable. No decision edge.

## Assumption → method matching

Different assumptions need different experiment types.

| Assumption type | Good methods |
|---|---|
| Value / demand | fake door, concierge, pre-order, landing page, concept test |
| Usability | prototype test, task-based usability session, first-click test |
| Feasibility | engineering spike, benchmark, technical prototype |
| Viability | pricing test, sales conversation, cost model, legal review |
| Behavior change | live-data prototype, A/B test, staged rollout |

The common error:
- using interviews to answer willingness-to-pay,
- using A/B tests to discover unknown opportunities,
- using prototype tests to answer infra feasibility,
- using surveys to answer actual behavior.

Match the method to the question.

## Cheap-to-expensive test ladder

Best practice:
- test cheap before testing expensive
- test reversible before testing irreversible
- test directional before testing polished

Typical ladder:

```
opinion / smoke test
        ↓
behavioral intent signal
        ↓
prototype usage
        ↓
concierge / Wizard-of-Oz
        ↓
live limited rollout
        ↓
full production experiment
```

Not every idea needs every rung. But most teams move too quickly to expensive tests.

## Success criteria and kill criteria

This is where most experiments go bad.

### Success criteria
Pre-commit what good looks like.

Examples:
- at least 25% of exposed users click through to setup
- at least 4 of 6 target users complete task unaided
- at least 3 design partners use workflow twice in one week
- benchmark stays under 200ms p95 latency

### Kill criteria
Pre-commit what would invalidate the bet.

Examples:
- fewer than 10% click through
- most users misunderstand the concept within 5 seconds
- activation lift is below 3 percentage points
- support burden per user is too high to sustain manually

No kill criterion = experiment bias.
The team will reinterpret ambiguous outcomes as success.

## Guardrail metrics

A change that improves one thing while damaging something more important is not a win.

Guardrails are the metrics you refuse to break while chasing the primary metric.

Examples:
- activation up, but week-1 retention cannot drop
- signup conversion up, but fraud cannot increase materially
- engagement up, but latency cannot degrade past threshold
- revenue up, but refund rate cannot spike

This is especially important in [A/B testing](ab-testing.md), pricing experiments, and onboarding changes.

## Decision rules

A good experiment ends with a clear next move.

Possible decisions:
- ship
- iterate and retest
- narrow to a specific segment
- reframe opportunity
- kill idea
- escalate to a stronger test

If an experiment ends with:
> interesting, let's keep thinking

then either the test was weak or the decision owner is avoiding commitment.

## Good experiment design questions

Before launch, ask:
- What belief would this actually change?
- What is the weakest evidence source in this design?
- Are we measuring behavior or just opinion?
- Are we testing the idea, or the copy, or the visual polish, or the channel?
- What confounds could explain the result?
- Is the assignment unit correct?
- What would we do if the result is neutral?
- Are we running this because it is the best test, or because it is the easiest test?

## Common confounds

Experiments are easy to misread.

### 1. Novelty effect
Users respond to newness, not real value.

### 2. Selection bias
The people who saw the experiment are not representative.

### 3. Channel contamination
The channel used to recruit/test shapes the result more than the idea itself.

### 4. Segment mixing
Different segments respond differently, but the team averages them together.

### 5. Ambiguous instrumentation
The metric does not actually capture the behavior you care about.

### 6. Too many variables changed at once
Now you do not know what caused the effect.

## Segment-aware experiment design

A test result is only as useful as the segment it applies to.

Always ask:
- For whom is this true?
- Was this tested with the target segment or just whoever was available?
- Does this result generalize, or is it local?

A strong experiment in the wrong segment is still weak discovery.

This is why [ICP / segmentation](icp-segmentation.md) should exist before major testing.

## Qual vs quant experiment roles

| Qualitative | Quantitative |
|---|---|
| discover why | measure how much |
| find unknown failure modes | validate effect size |
| small sample, deep detail | large sample, shallow detail |
| prototype / interview / observation | A/B / funnel / cohort / pricing data |

Good experiment programs use both.

Example flow:
- 5-user prototype test reveals confusion
- revised design tested again qualitatively
- then A/B test quantifies impact at scale

## Experiment strength hierarchy

Not all evidence is equal.

```
opinion
  ↓
stated preference
  ↓
recalled behavior
  ↓
observed prototype behavior
  ↓
real workflow behavior
  ↓
real money / repeated usage / retention
```

As stakes go up, evidence quality should go up too.

## Experiment brief template

Use a short written brief:

```
Experiment:
Owner:
Date range:

Assumption:
Why risky:

Target segment:
Method:
Assignment unit:

Primary metric:
Guardrails:

Success criterion:
Kill criterion:

Confounds to watch:
Decision if success:
Decision if failure:
Decision if ambiguous:
```

If the team does this consistently, experiment quality rises fast.

## Common failure modes

### Fake rigor
A lot of structure, but weak underlying evidence.

### Success criteria written after the fact
Classic self-deception.

### Testing the comfortable assumption
Not the riskiest one.

### Multiple goals in one experiment
Trying to answer five questions with one test.

### No segment definition
Result cannot be interpreted cleanly.

### No owner / no decision
The evidence goes nowhere.

### Shipping because test was "promising"
Promising is not a criterion.

## Practical cadence

For a healthy discovery team:
- every meaningful experiment has a written brief
- every brief has success + kill criteria
- every result updates OST / assumptions / roadmap
- every month, review which experiment types produced the strongest learning

The point is not to run more experiments.
The point is to run experiments that sharpen decisions.

## Heuristic

If an experiment can only tell you:
> Something happened.

but not:
> Therefore we should do X.

then the experiment was not designed tightly enough.

## How this connects to the wiki

```
[research synthesis](research-synthesis.md)
        ↓
clear opportunity
        ↓
[assumption mapping](assumption-mapping.md)
        ↓
experiment design
        ↓
[RAT](rat.md), [prototyping](prototyping.md), [A/B testing](ab-testing.md)
        ↓
decision
```

Experiment design is the bridge between identified uncertainty and trustworthy learning.

## See also

- [Assumption mapping](assumption-mapping.md) — identifies what to test first
- [RAT](rat.md) — tests the riskiest assumption first
- [Prototyping](prototyping.md) — one class of experiment vehicle
- [A/B testing](ab-testing.md) — quant experiment design at scale
- [Research Synthesis](research-synthesis.md) — clarifies what uncertainty remains
- [Cagan's four risks](cagan-four-risks.md) — the risk taxonomy experiments should reduce
