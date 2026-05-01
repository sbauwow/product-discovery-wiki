# A/B Testing

> The dominant quantitative validation method in modern web/mobile products. Causal inference via random assignment. Powerful, often misused.

## Core mechanic

```
   Randomized split
        │
   ┌────┴────┐
   ▼         ▼
Variant A   Variant B
(control)   (treatment)
   │         │
   ▼         ▼
Measure metric X
   │
   ▼
Compare distributions
   │
   ▼
Statistical test → ship/kill/iterate
```

**Random assignment** is the load-bearing element. Without randomization, you have correlation, not causation.

## What you need

| Component | Purpose |
|---|---|
| **Hypothesis** | "If we do X, metric Y will move by Z%" — predicted direction and magnitude |
| **Primary metric** | One success criterion, decided *before* the test |
| **Guardrail metrics** | Things you don't want to break (latency, error rate, secondary engagement) |
| **Sample size calculation** | How many users needed to detect Z% lift at 80% power, 5% significance |
| **Random assignment unit** | User, session, account — pick consistent with what you're measuring |
| **Run duration** | At least 1 full week (covers weekly seasonality), longer if low traffic |

## Sample size: the math

Roughly:

```
n ≈ 16σ² / Δ²    per variant, for a two-sided test at α=0.05, β=0.20
```

Where σ = metric standard deviation, Δ = the lift you want to detect.

Implication: smaller lifts need *quadratically* more users. Detecting a 1% lift takes ~100x the sample of a 10% lift.

Use a calculator (Evan Miller's, Optimizely's). Don't eyeball it.

## Common failure modes

### 1. Peeking
Checking results daily, stopping when "significant". Inflates false positive rate dramatically. **Decide sample size up front, run to completion.**

Fix: sequential testing methods (Optimizely's stats engine, mSPRT) if you must peek.

### 2. Multiple comparisons
Testing 10 metrics, calling success on whichever is significant. With 10 independent metrics, ~40% chance one shows p<0.05 by chance alone.

Fix: declare *primary* metric in advance. Treat secondaries as exploratory.

### 3. Underpowered tests
Running the test for a week, seeing "not significant", concluding "no effect". Often the test was too small to detect the actual effect size.

Fix: power analysis up front. If you can't get the sample, the test isn't useful — don't run it.

### 4. Novelty effects
Treatment looks great in week 1; users were curious. By week 4, effect gone.

Fix: run long enough to see post-novelty steady state. Look at cohort retention curves, not just snapshot.

### 5. Sample ratio mismatch (SRM)
Variant A got 47% of users, B got 53%. Assignment is broken. **Any analysis is invalid until SRM is fixed.**

Fix: chi-square test on assignment counts. Investigate before trusting results.

### 6. Simpson's paradox
Treatment loses overall but wins in every segment (or vice versa). Usually because segments differ in size and metric levels.

Fix: pre-register segments of interest; report both aggregate and segmented.

### 7. Network effects
A/B testing a feature that affects shared experience (e.g. social product, marketplace). Treated user's behavior affects control user's experience → assignment leaks.

Fix: cluster randomization (assign whole groups, not individuals).

## When A/B testing works

✅ High-traffic products (millions of users)
✅ Small-to-medium changes with measurable impact
✅ Iteration on existing flows (checkout, signup)
✅ Pricing tests (with care)

## When it doesn't

❌ Low traffic — can't reach significance in reasonable time
❌ Big strategic bets — too many things change at once
❌ Network-effect features
❌ Brand/identity changes — slow signal, novelty distortion
❌ Things you should kill regardless of A/B (broken UX, accessibility)

## A/B testing vs interviews

| A/B test | [User interview](user-interviews.md) |
|---|---|
| What works at scale | Why something works |
| Causal effect, narrow | Mental model, broad |
| Lots of users, one variable | Few users, many variables |
| Validates known options | Surfaces unknown options |

They complement. A/B test optimizes the local optimum; interviews tell you whether you're on the right hill at all.

## Bayesian alternatives

Frequentist A/B testing (p-values, significance) is dominant. Bayesian A/B testing (posterior distributions, "P(B > A) = 87%") is increasingly popular:
- More intuitive ("there's an 87% chance B is better")
- Easier with continuous monitoring
- Same sample-size rigor needed

Both work. Pick one and be consistent.

## Ethical considerations

A/B tests on real users without consent are fine for UI tweaks. Become problematic for:
- Pricing (different users see different prices)
- Emotional manipulation (Facebook's 2014 mood experiment)
- Anything with material consequences

Disclose where appropriate; don't experiment on harm.

## See also

- [Cohort analysis](cohort-analysis.md) — for measuring retention effects of treatments
- [Assumption mapping](assumption-mapping.md) — A/B test is one experiment type
- [Lean Startup](lean-startup.md) — A/B testing is the quantitative half of build-measure-learn
- [Vanity metrics](vanity-metrics.md) — bad primary metrics make A/B tests worthless
