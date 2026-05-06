# Discovery Operating Loop

> The wiki now contains many important concepts. This page is the practical spine: the repeating loop that connects strategy, segmentation, research, synthesis, experimentation, measurement, and decision-making into one operating rhythm.

## Core thesis

Discovery is not a one-time phase.
It is a loop.

The loop exists to answer, repeatedly:
- which problems matter most,
- for which segment,
- why now,
- what to test,
- what to ship,
- and what we learned from the result.

Without the loop, the concepts stay disconnected.
With the loop, the concepts become an operating system.

## The full loop

```
1. STRATEGY
   decide what game we are playing
        ↓
2. SEGMENT / ICP
   decide for whom we are solving first
        ↓
3. SIGNAL INTAKE
   gather evidence from users, data, support, sales, churn
        ↓
4. SYNTHESIS
   turn evidence into patterns and opportunities
        ↓
5. OUTCOME + OPPORTUNITY CHOICE
   decide what user / business change matters now
        ↓
6. ASSUMPTIONS + EXPERIMENTS
   test the riskiest beliefs cheaply
        ↓
7. DELIVERY
   build and ship what survived discovery
        ↓
8. INSTRUMENTATION + MEASUREMENT
   observe what happened in reality
        ↓
9. DECISION
   scale / iterate / narrow / kill / reposition
        ↓
back to strategy, segment, and signals
```

This is not linear forever.
It is recursive.
Each loop sharpens the next one.

## Step 1. Strategy

Start with:
- what market / problem space matters,
- what constraints matter,
- what non-obvious bet the company is making.

This is the layer from [product strategy](product-strategy.md).

Without strategy, discovery becomes:
- feature fishing
- random interviews
- stakeholder negotiation disguised as learning

Strategy gives the loop a frame.

Question:
> What game are we playing, and what are we explicitly not playing?

## Step 2. Segment / ICP

Next decide:
- who specifically are we serving first,
- which segment is best-fit now,
- which beachhead gives the cleanest chance to win.

This is the layer from [ICP, Segmentation, and Beachhead Market](icp-segmentation.md).

Without this step:
- research gets muddy
- product requests conflict
- PMF signals become noisy averages

Question:
> For whom is this loop being run?

## Step 3. Signal intake

Now gather evidence from multiple channels:
- interviews
- surveys
- support tickets
- sales calls
- churn reasons
- product telemetry
- session recordings
- win/loss notes

This includes both:
- scheduled discovery work ([continuous discovery](continuous-discovery.md))
- operational signal flow ([Voice of Customer (VoC) Systems](voc-systems.md))

Question:
> What are users, buyers, and accounts actually doing, struggling with, or saying?

## Step 4. Synthesis

Raw input is not insight.
Synthesis turns messy signal into:
- patterns
- contradictions
- segment differences
- opportunities
- reframed understanding

This is the layer from [research synthesis](research-synthesis.md).

Without synthesis, teams confuse:
- notes with learning
- quotes with decisions
- volume with clarity

Question:
> What changed in our understanding?

## Step 5. Outcome + opportunity choice

After synthesis, choose:
- which outcome matters now,
- which opportunity branch to pursue,
- which segments matter most for this cycle.

This is where [outcomes vs outputs](outcomes-vs-outputs.md) and the [Opportunity Solution Tree](opportunity-solution-tree.md) come together.

This step matters because the loop is not:
- solve everything
- fix every complaint
- satisfy every segment

It is:
> choose one meaningful thing to move.

Question:
> What change in user or business behavior are we trying to cause next?

## Step 6. Assumptions + experiments

Once an opportunity is chosen:
- identify the riskiest assumptions,
- select the cheapest valid test,
- define success, failure, and guardrails.

This is the layer from:
- [assumption mapping](assumption-mapping.md)
- [RAT](rat.md)
- [experiment design](experiment-design.md)
- [prototyping](prototyping.md)
- [A/B testing](ab-testing.md)

The key discipline:
- do not build first if a cheaper test can answer the question.

Question:
> What belief must become more certain before we commit more resources?

## Step 7. Delivery

After discovery reduces enough uncertainty, move into delivery.

Delivery is not outside the loop.
Delivery is one phase of the loop.

You ship:
- the solution that survived discovery,
- into production,
- with instrumentation,
- knowing what outcome it was intended to move.

This is where [dual-track agile](dual-track-agile.md) matters.

Question:
> What deserves real build investment now?

## Step 8. Instrumentation + measurement

After shipping, the loop needs reality.

That requires:
- event definitions
- metric definitions
- funnel tracking
- cohort tracking
- experiment readouts
- retention visibility

This is the layer from:
- [tracking plans and instrumentation](tracking-plans-instrumentation.md)
- [funnel analysis](funnel-analysis.md)
- [cohort analysis](cohort-analysis.md)
- [HEART](heart-framework.md)
- [aha moment / activation](aha-moment.md)
- [churn and retention diagnosis](churn-retention-diagnosis.md)

Question:
> What actually happened after contact with reality?

## Step 9. Decision

This is where many teams quietly fail.

Evidence should force a decision:
- scale
- iterate
- narrow the segment
- reposition the message
- redesign onboarding
- kill the idea
- revisit the strategy

If the loop ends with:
> interesting, let's keep thinking

then the loop has not closed.

Question:
> What do we now believe differently, and what changes because of that?

## How the loop runs at different speeds

Different parts move on different cadences.

### Weekly
- user touchpoints
- VoC review
- synthesis
- OST update
- experiment planning

### Biweekly / monthly
- prototype tests
- experiment readouts
- feature / flow refinements
- insight memo publication

### Quarterly
- strategy refresh
- ICP refinement
- bigger outcome choice
- broader retention / PMF review

A healthy product org nests these cadences.

## The loop by artifact

The loop becomes much easier when each phase has a corresponding artifact.

| Loop phase | Artifact |
|---|---|
| Strategy | strategy memo |
| Segment / ICP | ICP memo / segment map |
| Signal intake | VoC board / interview notes / telemetry dashboards |
| Synthesis | insight memo / affinity clusters |
| Outcome choice | OST / outcome brief |
| Experiments | experiment briefs / assumption map |
| Delivery | validated backlog / shipped changes |
| Measurement | funnel / cohort / experiment dashboards |
| Decision | decision log / roadmap update |

Artifacts are not the point.
They are the memory of the loop.

## The loop in a PLG example

Example:

```
Strategy:
  win PLG SaaS teams via activation improvement

Segment:
  SaaS companies with 3–20 PMs and measurable onboarding funnels

Signal intake:
  interviews + support tickets + funnel data

Synthesis:
  users do not trust setup completion and fail to reach first value

Outcome:
  increase 7-day activation from 28% to 40%

Assumption:
  task-based onboarding will get users to first value faster

Experiment:
  prototype + later A/B test

Delivery:
  ship task-based first-run flow

Measurement:
  activation up, week-1 retention flat, support burden down

Decision:
  scale to target segment, keep iterating on time-to-value
```

That is the loop in action.

## The loop in a B2B enterprise example

Example:

```
Strategy:
  win security-conscious enterprise accounts in a narrow vertical

Segment:
  public-company security teams with audit-heavy workflows

Signal intake:
  sales losses + CS calls + churn interviews

Synthesis:
  product value is real, but admin controls block trust and renewal

Outcome:
  increase 12-month logo retention in target segment

Assumption:
  stronger audit / permissions controls reduce renewal risk

Experiment:
  design partner validation + admin prototype + sales testing

Delivery:
  ship enterprise admin layer

Measurement:
  adoption spreads to more stakeholders, renewal risk decreases

Decision:
  deepen enterprise wedge instead of broadening to SMB
```

Same loop, different context.

## Common failure modes

### Discovery without strategy
Interesting research, no focus.

### Strategy without signal
Leadership opinions masquerading as truth.

### Signal without synthesis
Lots of notes, no changed decisions.

### Synthesis without outcome choice
Everything feels important, nothing gets prioritized.

### Experiments without decision criteria
Evidence accumulates, nothing dies.

### Delivery without instrumentation
Shipped changes cannot be evaluated honestly.

### Measurement without interpretation
Dashboards grow, understanding does not.

### No loop closure
The team learns, but the learning never alters strategy, roadmap, or behavior.

## The operating question for every team

At any moment, a healthy team should be able to answer:
- What outcome are we trying to move?
- For which segment?
- What evidence shaped that choice?
- What is the riskiest current assumption?
- What are we testing now?
- What did we just learn?
- What changed because of it?

If those answers are fuzzy, the loop is probably broken.

## Heuristic

If your team is busy but cannot point to:
- the current outcome,
- the current opportunity,
- the current test,
- and the last real learning,

then you are not in a discovery loop.
You are in motion without learning.

## How this connects to the wiki

This page is the connective tissue across the whole library.

Core path:
- [product strategy](product-strategy.md)
- [ICP, Segmentation, and Beachhead Market](icp-segmentation.md)
- [Voice of Customer (VoC) Systems](voc-systems.md)
- [research synthesis](research-synthesis.md)
- [Opportunity Solution Tree](opportunity-solution-tree.md)
- [assumption mapping](assumption-mapping.md)
- [experiment design](experiment-design.md)
- [tracking plans and instrumentation](tracking-plans-instrumentation.md)
- [churn and retention diagnosis](churn-retention-diagnosis.md)

## See also

- [Product strategy](product-strategy.md)
- [Dual Track Agile](dual-track-agile.md)
- [Continuous discovery](continuous-discovery.md)
- [Product Operating Model](product-operating-model.md)
- [Outcomes vs outputs](outcomes-vs-outputs.md)
