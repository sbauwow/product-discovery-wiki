# Multivariate Testing (MVT) & Bayesian A/B

> Beyond [A/B testing](ab-testing.md): more rigorous and more flexible variants. MVT tests many variables simultaneously; Bayesian methods change the statistical framework. Both are mature techniques widely misused.

## Multivariate testing (MVT)

A/B testing varies one element. MVT varies *multiple* elements simultaneously, measuring interactions.

```
A/B test: vary headline, hold rest constant
  Variant A: "Buy now"
  Variant B: "Get started today"

MVT: vary headline AND button color AND image
  2 headlines × 2 button colors × 3 images = 12 variants
  Measure: which combination wins
```

## When MVT helps

✅ **Large sample volume** — the math demands it
✅ **Interaction effects** — when you suspect element A and element B combine non-linearly (red button works with serious headline; green button works with playful headline)
✅ **Polishing** — late-stage optimization on a known-good page
✅ **Bundled changes** — testing multiple changes that ship together

## When A/B is better

❌ Low traffic — MVT splits sample many ways; insufficient power per variant
❌ Big strategic decisions — too many things change at once; can't isolate cause
❌ When you don't have a good hypothesis about interactions
❌ Complex setups — bug risk, attribution risk

For most product teams, A/B is right. MVT is for very high-traffic surfaces (top-of-funnel landing pages, search results, ad creative).

## Sample-size implications

A/B test for 5% lift detection: ~10,000 users per variant.

MVT with 12 variants and 5% lift detection: ~120,000 users *per cell*.

The sample-size requirement scales with the number of variants. Most products can't afford true MVT.

## Fractional factorial designs

If you must MVT with limited traffic: **fractional factorial** designs. Test a strategic subset of all combinations rather than all combinations.

Example: 3 variables × 2 levels each = 8 combinations full factorial. Fractional design tests 4-5 carefully chosen combinations, infers main effects.

Statistical literature is dense. Tools (Optimizely, VWO) handle the math.

## Bayesian A/B testing

Different *statistical framework* for analyzing A/B tests. Compares to traditional **frequentist** methods.

### Frequentist (standard A/B)
```
"Variant B converts 5% better than A, p = 0.03."
Translation: "If A and B were equal, we'd see this difference < 3% of time by chance."
Decision rule: ship if p < 0.05.
```

### Bayesian
```
"There is an 87% probability that B is better than A.
 Expected lift if we ship B: +4.2% (95% CI: +1.1% to +7.3%)."
Decision rule: ship when probability of better-ness exceeds threshold (e.g. 95%).
```

Same data, different framing. Both can give the same decision; Bayesian is often more interpretable.

## Bayesian advantages

### 1. Better interpretation
"87% probability B wins" is what stakeholders actually want to know. Frequentist p-values are notoriously misinterpreted.

### 2. Continuous monitoring
Bayesian methods let you peek at results as they accumulate without inflating false positive rates (subject to corrections). Frequentist NHST forbids this strictly.

### 3. Effect-size estimation
Bayesian gives a distribution of likely effects, not just "significant or not." More useful for decisions about magnitude.

### 4. Prior incorporation
You can encode prior knowledge ("most landing-page changes are small"). Useful when traffic is limited.

## Bayesian disadvantages

### 1. Tooling
Tools (Optimizely's stats engine, vwo, Eppo, GrowthBook) implement Bayesian. Rolling your own is non-trivial.

### 2. Prior selection
Bad priors → bad posteriors. Defaults are usually OK; custom priors require statistical care.

### 3. Misinterpretation
"87% probability B wins" sounds compelling — but means *given the model*. Garbage in, garbage out.

### 4. Less standardization
Frequentist p-values are universal; Bayesian results need explanation across teams.

## Frequentist vs Bayesian: the practical difference

For a typical product team, the choice is mostly *philosophical* until traffic is large. Both produce similar decisions on well-designed tests. Pick:

- **Frequentist** if your team knows it; tooling supports it; want standardization
- **Bayesian** if continuous monitoring matters; stakeholders need interpretable outputs; you have the tooling (Optimizely, etc.)

Many modern A/B platforms use Bayesian by default (Optimizely Stats Engine, GrowthBook).

## Sequential testing

A specific solution to the "peeking problem" in [A/B](ab-testing.md). Standard frequentist tests assume you decide sample size upfront; checking results early inflates false-positive rates.

Sequential methods (mSPRT, group sequential, alpha spending) are designed for monitoring. Stop the test when stable signal emerges; account for the multiple looks.

Both Bayesian methods and sequential frequentist methods solve the same practical problem: "we need to peek without breaking the math."

## When to invest in advanced testing

✅ High-traffic products (millions of users)
✅ Mature growth org with statistical resources
✅ Search / recommendations / personalization
✅ Pricing experiments (high-stakes; need rigor)
✅ Network / marketplace products (need cluster randomization, etc.)

## When standard A/B is enough

❌ Mid-traffic startups (10K-100K users)
❌ Quarterly major launches with clear hypotheses
❌ Teams without statistical leads

Most product teams overestimate their statistical sophistication. Get good at A/B first; advance only when scale demands it.

## Counterfactual / synthetic-control methods

When randomization is impossible (a feature can't be A/B tested — e.g. pricing change, network features, product redesigns):

- **Difference-in-differences** — compare treated geography/cohort to similar untreated, accounting for general trends
- **Synthetic controls** — construct a synthetic "control group" from weighted similar units
- **Regression discontinuity** — exploit cutoffs (e.g. "users with 5+ logins got the experience"; compare just-above vs just-below)

These are causal inference methods. Less rigorous than A/B; sometimes the only option. Pair with strong domain priors.

## Common failure modes

- **MVT with insufficient sample** — 12 variants, 1000 users; results meaningless
- **Bayesian as magic** — bad data with Bayesian framing produces bad answers, just more interpretably
- **Continuous monitoring with frequentist** — peeking inflates false positives; misuse is rampant
- **Ignoring guardrails** — winning variant on primary metric tanks secondary metric; ship without noticing
- **Multiple comparisons** — testing 10 metrics at p<0.05; ~40% chance of false positive
- **Skipping power analysis** — running a test too small to detect the lift you care about
- **Causation overclaim** — counterfactual methods give correlational evidence; treating as causal misleads

## Tools

- **Optimizely / VWO** — full-featured experimentation platforms; Bayesian default
- **GrowthBook** — open-source, Bayesian, increasingly popular
- **Eppo** — more advanced; warehouse-native
- **LaunchDarkly** — feature flags + experiments
- **Statsig** — modern integrated experimentation
- **Custom R / Python** — for advanced teams; statsmodels, PyMC for Bayesian

## See also

- [A/B testing](concepts/ab-testing.md) — the foundation
- [Funnel analysis](concepts/funnel-analysis.md) — what tests aim to improve
- [Cohort analysis](concepts/cohort-analysis.md) — long-term effect measurement
- [Power user analysis](concepts/power-user-analysis.md) — segmentation that informs test design
