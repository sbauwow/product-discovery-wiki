# Churn and Retention Diagnosis

> Retention is the truth serum of product discovery. Acquisition can be bought. Activation can be manipulated. Revenue can be temporarily discounted into existence. But if users or accounts do not keep coming back, the product has not become part of their real workflow or life. Churn and retention diagnosis is the practice of figuring out why.

## Core thesis

Churn is not just a revenue problem.
It is a discovery problem.

A team that cannot explain:
- who churns,
- when they churn,
- why they churn,
- and what behaviors predict retention,

is still guessing about product-market fit.

## What retention tells you

Retention answers:
- did users get recurring value?
- did the product fit into a real habit or workflow?
- did the product solve a frequent enough problem?
- did onboarding create the right early behavior?
- did the segment you acquired actually fit?

Retention is often the cleanest proof that value is real.

## Churn vs retention

- **Retention** = users or accounts that continue using / paying over time
- **Churn** = users or accounts that stop using / paying

Both are the same phenomenon from opposite sides.

Formulaically:

```
retention = remaining / starting cohort
churn = lost / starting cohort
retention + churn ≠ always 100% in product analytics
```

Why not always?
Because definitions vary:
- user churn vs revenue churn vs logo churn
- active use vs paid status
- calendar windows vs rolling windows

Write the definition before debating the metric.

## The core diagnostic questions

Every retention investigation should answer:
1. Which cohort is churning?
2. At what point in the lifecycle do they churn?
3. Which segments churn more?
4. What early behaviors predict staying?
5. What reasons do churned users give?
6. What observable product frictions precede churn?

If you only know overall churn %, you know almost nothing.

## The retention lens hierarchy

Start with the broadest truth, then narrow.

### 1. Cohort shape
Use [cohort analysis](cohort-analysis.md).

Questions:
- does the curve flatten?
- where is the sharpest drop?
- are new cohorts improving or degrading?

### 2. Segment differences
Split by:
- acquisition channel
- plan tier
- use case
- company size / role
- geography
- first-week behavior
- self-serve vs sales-assisted

Average retention hides segment truth.

### 3. Activation correlation
Ask:
- which early behaviors predict retained users?
- who reached the [aha moment / activation](aha-moment.md)?
- who never got there?

### 4. VoC / churn reason analysis
Use:
- cancellation forms
- churn interviews
- support history
- CS notes
- usage history before churn

### 5. Workflow breakdown
Map where recurring value fails:
- setup
- first value
- repeated value
- collaboration / team spread
- habit formation
- pricing / ROI realization

This is where diagnosis becomes actionable.

## Common churn patterns

### 1. Immediate churn
Users leave almost right after signup.

Signals:
- day-1 / day-7 retention weak
- onboarding incomplete
- activation not reached

Likely causes:
- wrong audience
- confusing setup
- weak first value
- overpromising in acquisition messaging

### 2. Delayed churn after trial period
Users engage briefly, then disappear.

Signals:
- activation may look decent
- retention drops after first cycle or first billing boundary

Likely causes:
- novelty effect, not durable value
- no repeat use case
- unclear reason to return
- weak habit or workflow embedding

### 3. Team-level / expansion churn
Initial champion uses product, broader org does not adopt.

Signals:
- one active user, little teammate spread
- account usage narrows before renewal risk

Likely causes:
- product is valuable to one person, not a team
- collaboration value weak
- internal champion cannot justify expansion

### 4. Enterprise churn despite usage
Usage exists, contract still dies.

Signals:
- active users but renewal at risk
- CS notes mention procurement, trust, politics

Likely causes:
- viability issues
- weak ROI proof
- compliance / admin gaps
- stakeholder misalignment

## A practical retention diagnosis workflow

### Step 1. Define retention clearly
Examples:

```
User retention:
% of new users active in week 4

Account retention:
% of paid accounts still active after 90 days

Revenue retention:
% of starting MRR retained after 12 months
```

Do not mix them casually.

### Step 2. Plot the cohort curve
Look for:
- day-1 cliff
- week-2 cliff
- no flat floor
- degradation in recent cohorts

### Step 3. Segment the curve
Compare:
- channel A vs B
- free vs paid-acquired
- SMB vs enterprise
- activated vs non-activated
- role / use case clusters

### Step 4. Find predictive early behaviors
Ask:
- what do retained users do in week 1 that churned users do not?
- what thresholds correlate with later retention?

This is where activation and onboarding work connect.

### Step 5. Overlay qualitative evidence
Use:
- churn interviews
- support burden before churn
- renewal-risk notes
- cancellation text
- session recordings if available

Quant says where the leak is.
Qual says why.

### Step 6. Separate value failure from usability failure
A user can churn because:
- they never wanted this enough
- they could not figure it out
- they got value once but not repeatedly
- the product did not fit their segment / workflow
- the economics or switching costs did not work

These require different responses.

## The churn interview

One of the highest-value research formats.

Good questions:
- What were you hoping this product would help you do?
- Tell me about the moment you realized you might stop using it.
- What did you do instead?
- What part of the workflow never fit?
- What would have had to be true for you to stay?

Avoid:
- defensive rebuttals
- feature pitching
- trying to save the account during the learning conversation

The goal is truth, not recovery.

## Cancellation reasons: useful but dangerous

A cancellation form can help, but do not overtrust it.

Why dangerous:
- users pick the closest available option
- they may hide the real reason
- reasons are often multi-causal

Use cancellation reasons as a signal source, not as complete truth.

Best practice:
- combine form reason + actual usage history + support history + optional follow-up interview

## Segment-level churn diagnosis

Always ask:
> Who is this product retaining well for?

Sometimes "high churn" is actually:
- great retention in one segment
- terrible retention in another

This changes strategy dramatically.

Responses may include:
- narrow the ICP
- change positioning
- stop acquiring weak-fit users
- build for the strong segment first

This is why retention analysis is often a segmentation decision, not just a UX decision.

## Value failure vs habit failure

Two products can both churn, for different reasons.

### Value failure
The product never solved a meaningful problem.

Signals:
- low activation
- low repeat usage from the start
- cancellation reason: "not useful / not needed"

### Habit / workflow failure
The value was real, but it never became regular.

Signals:
- initial engagement exists
- later drop-off
- users say it was useful but stop returning

These require different fixes.
- value failure → rethink segment/problem/positioning
- habit failure → improve triggers, integration, repeat workflows, collaboration, or ongoing ROI visibility

## Revenue churn vs product churn

Especially in SaaS, not all churn is the same.

### Product churn
User stops using the product.

### Revenue churn
Customer downgrades, shrinks seats, or cancels payment.

A product can have:
- decent usage retention but bad revenue retention
- bad usage retention but temporary revenue stability due to annual contracts

Do not assume one explains the other.

## Common metrics to inspect

- day-1 / day-7 / day-30 retention
- week-N active retention by cohort
- logo churn
- revenue churn / net revenue retention
- activation rate
- time-to-value
- repeat usage frequency
- teammate invite / expansion behavior
- support tickets per retained vs churned cohort
- cancellation reasons by segment

Metrics alone do not diagnose. They locate the question.

## Churn diagnosis by product shape

### PLG products
Most important questions:
- did users reach activation quickly?
- did they repeat the core action?
- did they invite others?

### B2B SaaS
Most important questions:
- did the account operationalize the workflow?
- did multiple stakeholders adopt?
- was ROI visible before renewal?

### Marketplaces
Most important questions:
- did one side retain but the other not?
- did local liquidity fail?

### Consumer habit products
Most important questions:
- what triggers return behavior?
- what predicts habit formation vs one-time novelty?

## Common failure modes

### Looking only at aggregate churn
Hides the whole story.

### Confusing churn reasons with root causes
"Too expensive" may really mean "not enough value."

### Treating all churn as fixable
Some churn is healthy if it comes from bad-fit segments.

### Overreacting to anecdotal churn
One loud exit interview does not equal a pattern.

### Not separating product from market issues
Sometimes the product is fine and the acquired segment is wrong.

### Waiting too long to talk to churned users
Context decays fast.

## Good artifacts to maintain

### 1. Retention diagnosis memo
For a key cohort or segment:
- curve shape
- biggest cliff
- segment differences
- likely causes
- recommended next tests

### 2. Churn reason taxonomy
Simple normalized list:
- no recurring need
- confusing setup
- poor trust / quality
- missing capability
- pricing / ROI mismatch
- switched to competitor
- internal / organizational change

### 3. Save / no-save learning log
For churned accounts:
- what intervention was tried
- what, if anything, changed the outcome

### 4. Retained-user behavior profile
What strong retained users do early and repeatedly.

## Heuristic

If your team answers churn with
> We need more features

before answering
> Which segment churns, at what point, and why?

then you are still doing superstition, not diagnosis.

## How this connects to the wiki

```
[cohort analysis](cohort-analysis.md)
        ↓
retention pattern
        ↓
[aha moment / activation](aha-moment.md)
+ [VoC systems](voc-systems.md)
        ↓
segment-aware churn diagnosis
        ↓
[PMF](pmf.md), [RARRA](rarra.md), positioning, onboarding, experiments
```

Churn diagnosis is how teams learn whether value is truly recurring.

## See also

- [Cohort analysis](cohort-analysis.md) — the quantitative base layer
- [Aha moment / Activation](aha-moment.md) — early behavior most tied to retention
- [RARRA](rarra.md) — retention-first framing
- [PMF](pmf.md) — retention is one of the clearest PMF signals
- [Voice of Customer (VoC) Systems](voc-systems.md) — churn reasons as signal source
- [Product-Led Growth](product-led-growth.md) — activation / retention / expansion chain
