# Tracking Plans and Instrumentation

> The best discovery frameworks in the world collapse if the underlying telemetry is untrustworthy. Funnels, cohorts, activation, HEART, pricing tests, and A/B tests all depend on one hidden layer: someone has to define the events, properties, identities, and metrics cleanly enough that the numbers mean what the team thinks they mean.

## Core thesis

Instrumentation is product strategy made measurable.

A team without a tracking plan usually ends up with:
- dashboards nobody trusts
- ambiguous definitions of activation / retention / conversion
- experiments that cannot be interpreted
- broken funnels
- endless arguments about what the metric "really means"

A tracking plan exists to prevent that.

## What instrumentation is

Instrumentation is the act of deciding:
- which user behaviors matter,
- how they will be recorded,
- what properties will be attached,
- which identities and entities are counted,
- and how metrics will be computed from that data.

This is not just analytics plumbing.
It is discovery infrastructure.

## The tracking stack

Think in layers:

```
USER / ACCOUNT BEHAVIOR
        ↓
EVENTS
        ↓
EVENT PROPERTIES + IDENTITIES
        ↓
DERIVED METRICS
        ↓
DASHBOARDS / FUNNELS / COHORTS / EXPERIMENT READOUTS
        ↓
DECISIONS
```

If the lower layers are weak, the upper layers become fiction.

## The tracking plan

A tracking plan is a source-of-truth doc for product telemetry.

At minimum, it should define:
- event name
- event description
- trigger condition
- required properties
- optional properties
- actor / identity
- object / entity
- downstream metrics that use it

Example:

| Event | Meaning | Fires when | Key properties |
|---|---|---|---|
| `signup_completed` | new account created | user successfully finishes signup | plan_type, signup_method, country |
| `workspace_connected` | core setup step complete | first data source connected | source_type, team_size, elapsed_minutes |
| `activation_reached` | user hit defined activation event | criteria met for first value | activation_path, days_since_signup |
| `upgrade_started` | user entered paid conversion flow | pricing CTA begins checkout | plan_shown, billing_period |

This prevents every team from inventing its own interpretation.

## Event design principles

### 1. Instrument behavior, not intentions
Good event:
- `checkout_started`

Weak event:
- `interested_in_pricing`

Behavior is observable. Intent is inferred.

### 2. Name events from the business meaning, not the UI label
Good:
- `workspace_connected`

Weak:
- `clicked_blue_button`

UI labels change. Underlying behavior matters more.

### 3. Prefer stable semantic names
If the UI changes from "project" to "workspace," you should not need to rename the whole ontology every month.

### 4. Separate event from interpretation
Event:
- `task_completed`

Metric:
- activation rate = % of new users who complete task X within 7 days

Do not encode every metric definition directly into event names.

## Properties matter

The event alone is not enough.
Properties make segmentation and diagnosis possible.

### Common property types
- user properties: country, signup source, role
- account properties: plan tier, company size, industry
- event properties: source_type, latency_ms, experiment_variant
- contextual properties: device, surface, entry point
- timing properties: days_since_signup, step_number

Example:

Event:
- `workspace_connected`

Useful properties:
- `integration_type`
- `connection_method`
- `time_since_signup_minutes`
- `workspace_size`
- `variant`

Without properties, you can count events but cannot explain them.

## Identity design

One of the biggest hidden sources of bad analytics.

You must decide the unit of analysis:
- user
- session
- account
- workspace
- device
- order

Different metrics need different units.

Examples:
- activation may be user-level
- B2B conversion may be account-level
- network-effect health may need workspace-level metrics
- session UX may be session-level

If identity is unclear, funnels and cohorts become misleading.

## Metric definitions must be explicit

A metric without a written definition is a future argument.

For every important metric, define:
- exact formula
- time window
- entity counted
- exclusions
- source events

Example:

```
Activation rate
= % of new users
who complete `workspace_connected`
and `first_project_created`
within 7 days of `signup_completed`
measured at user level
excluding internal/test accounts
```

Now the team can debate the definition once, instead of rediscovering it weekly.

## Instrumentation for key discovery methods

### Funnels
To build a usable [funnel analysis](funnel-analysis.md), each step must:
- map to a real event
- fire reliably once the step occurs
- have unambiguous ordering
- be joinable to the same user/account identity

### Cohorts
To build honest [cohort analysis](cohort-analysis.md), you need:
- clear cohort anchor event (`signup_completed`, `first_purchase`, etc.)
- clean identity
- stable active-event definition

### Activation / aha
To identify [activation](aha-moment.md), you need:
- enough event coverage to compare first-week behaviors
- confidence that the events reflect real value, not shallow clicks

### HEART
To implement [HEART](heart-framework.md), signals must become measurable events or survey joins.

### A/B tests
For [A/B testing](ab-testing.md), instrumentation must support:
- variant assignment logging
- exposure event
- primary metric event
- guardrail events
- identity stability across sessions/devices where relevant

If variant exposure is not logged correctly, the experiment is not trustworthy.

## The difference between event logging and measurement design

Teams often think:
> We log lots of events, so analytics is covered.

No.

Logging many events is not the same as designing a measurement system.

Event logging answers:
- what did we capture?

Measurement design answers:
- what counts as success?
- what event chain proves it?
- how should it be segmented?
- how reliable is the metric?

Discovery needs the second, not just the first.

## Common event taxonomy mistakes

### 1. Button-click obsession
Tracking every click, but not the core value-creation moments.

### 2. Missing setup / state-change events
Funnels break because key transitions are inferred instead of logged.

### 3. Inconsistent naming
Examples:
- `signed_up`
- `signup_complete`
- `user_registered`

Three names for one idea = chaos.

### 4. Missing exclusions
Internal users, QA sessions, bots, and migrations pollute the metrics.

### 5. No versioning awareness
Meaning of an event drifts after UI / product changes, but dashboards stay unchanged.

### 6. No ownership
Nobody owns the telemetry ontology, so drift accumulates silently.

## Instrumentation QA

Telemetry should be tested like product code.

Checks to run:
- does the event fire at the right moment?
- does it fire once or multiple times unexpectedly?
- are required properties always present?
- are property values normalized?
- does the event appear in prod with correct timestamps?
- are internal/test accounts excluded downstream?

Useful verification methods:
- event debugger / live inspector
- QA scripts
- dashboard spot checks
- replaying real flows and comparing expected vs observed events
- automated tests for analytics-critical flows

Instrumentation quality decays if not actively maintained.

## Metric drift

A metric can stay numerically stable while its meaning changes.

Causes:
- product flow changed
- event semantics changed
- population changed
- logging bug introduced
- new exclusion rules added
- one event started firing earlier/later than before

This is metric drift.

Every major metric should have:
- owner
- definition doc
- change log when semantics move

Otherwise trend lines become misleading historical fiction.

## Good instrumentation questions

Before adding a metric, ask:
- What decision will this support?
- What exact behavior does it stand for?
- What identity is correct for counting?
- What segments matter most?
- What event chain could fake this metric without value actually being delivered?
- How could this metric be gamed by the team?
- What event would serve as a guardrail?

That last two matter a lot.
Metrics shape behavior.

## Guard against local gaming

Example:
- team optimizes clicks on an onboarding CTA
- metric looks better
- activation and retention stay flat

Why?
The instrumented metric captured compliance, not value.

This is why important metrics should usually be paired:
- one leading metric
- one value-confirming metric
- one guardrail

Example:
- leading: onboarding step completion
- value-confirming: activation reached within 7 days
- guardrail: week-1 retention / support burden

## Good artifacts to maintain

### 1. Tracking plan
Source-of-truth event dictionary.

### 2. Metric dictionary
Definitions of core metrics.

### 3. Event ownership map
Who owns taxonomy quality for which domain.

### 4. Analytics QA checklist
Used before major launches and experiments.

### 5. Instrumentation changelog
What changed, when, and what dashboards may be affected.

## Practical workflow

### Step 1. Start from decisions, not events
Ask:
- what decisions do we need to make?
- what behaviors would answer them?

### Step 2. Define core value milestones
Example:
- signup
- setup complete
- first value
- repeated value
- upgrade start
- paid conversion

### Step 3. Define event names and properties
Keep them stable and semantic.

### Step 4. Define metrics explicitly
Do this in writing before dashboarding.

### Step 5. QA the flow end-to-end
Verify that real user journeys produce the expected event stream.

### Step 6. Review quarterly
Instrumentation is a living system.

## Common failure modes

### Over-instrumentation
Tracking everything, trusting nothing.

### Under-instrumentation
Core behavior missing, forcing analysts to infer what happened.

### Dashboard-first analytics
Beautiful charts built on undefined metrics.

### Copy-pasted event names from old products
Ontology mismatch creates misleading metrics.

### Treating analytics as a data-team-only concern
Product discovery depends on it; PM/design/eng all need shared ownership.

### Retrofitting after launch
Possible, but expensive. Better to define core tracking before major experiments.

## Heuristic

If two smart people on the team can answer
> "What exactly counts as activation?"

differently,
then your instrumentation system is not mature enough.

## How this connects to the wiki

```
[product strategy](product-strategy.md)
        ↓
[outcomes](outcomes-vs-outputs.md)
        ↓
tracking plans + metric definitions
        ↓
[funnel analysis](funnel-analysis.md)
[cohort analysis](cohort-analysis.md)
[HEART](heart-framework.md)
[A/B testing](ab-testing.md)
        ↓
decisions you can trust
```

Instrumentation is what makes quantitative discovery honest.

## See also

- [Funnel analysis](funnel-analysis.md) — requires clean event sequencing
- [Cohort analysis](cohort-analysis.md) — requires stable cohort anchors and active definitions
- [HEART framework](heart-framework.md) — signals need measurable instrumentation
- [A/B testing](ab-testing.md) — assignment, exposure, and metric logging must be correct
- [Aha moment / Activation](aha-moment.md) — activation only works if the event definition is trustworthy
- [Vanity metrics](vanity-metrics.md) — poor instrumentation makes vanity easy
