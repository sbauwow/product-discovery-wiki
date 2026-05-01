# Surveys

> The default-and-most-misused quantitative research tool. Cheap, fast, scalable — but produces garbage data when designed poorly. Most product teams write bad surveys; the consequences ripple into bad decisions.

## When surveys work

✅ **Quantifying a known pattern** — you've heard "the dashboard is slow" from interviews; survey 500 users to confirm prevalence
✅ **Segment-level metrics** — NPS, CSAT, satisfaction over time
✅ **Tradeoff measurement** — MaxDiff, conjoint analysis (specialized)
✅ **Reach** — talking to many users cheaply
✅ **Feature/topic prioritization** — only when paired with [importance × satisfaction](odi.md), not standalone "what features do you want?"

## When surveys fail

❌ **Discovering opportunities** — use [interviews](user-interviews.md); surveys can't surface unknown unknowns
❌ **Asking about hypotheticals** — "would you use…" produces lies politely
❌ **Asking about prices** — Van Westendorp aside, stated WTP is unreliable
❌ **Causation** — surveys measure correlation; not why
❌ **Complex behaviors** — users can't accurately self-report nuanced workflows

A survey asking "what features would you like?" is the worst tool for that question. Past-behavior interviews and observation are better.

## The 7 deadly survey design errors

### 1. Leading questions
- ❌ "How satisfied are you with our excellent new dashboard?"
- ✅ "How satisfied are you with the dashboard?"

The word "excellent" tilts every response.

### 2. Double-barreled questions
- ❌ "How satisfied are you with the speed AND accuracy of search?"
- ✅ Two questions: one about speed, one about accuracy.

A double-barreled question forces respondents to average across two dimensions, losing both signals.

### 3. Unbalanced scales
- ❌ "Rate the feature: Excellent / Very Good / Good / Average"
- ✅ "Rate: Very Bad / Bad / Neutral / Good / Very Good"

Unbalanced scales push responses toward positive (or negative) — the answer reflects scale design, not user opinion.

### 4. Vague time references
- ❌ "How often do you use the app?"
- ✅ "In the past 7 days, how many times did you open the app?"

"Often" means different things to different people; specifying a time window forces concrete recall.

### 5. Forced choice without escape
- ❌ "Which feature do you use most? [a/b/c/d]"
- ✅ "Which feature do you use most? [a/b/c/d/none of these/I don't use any]"

Without escape, users pick whatever is closest, polluting the data.

### 6. Survey too long
- After ~10 minutes, response quality degrades sharply
- Last-question accuracy can be <50% of first-question accuracy
- Aim for 5-7 minutes, 15-20 questions max for typical work

### 7. Stated-preference for behavioral questions
- ❌ "Would you pay $30/mo for premium features?" (stated preference — overestimates)
- ✅ "What's the most you've paid in the past year for tools like this?" (revealed preference)

Future-pricing surveys are particularly unreliable. Use price tests with real money instead.

## NPS done right

The most-used customer-loyalty metric. Question:

> "On a scale of 0-10, how likely are you to recommend [product] to a friend or colleague?"

Scoring:
- **Promoters** (9-10) — % of users
- **Passives** (7-8) — ignored
- **Detractors** (0-6) — % of users
- **NPS = % Promoters − % Detractors**, range -100 to +100

Common NPS mistakes:
- **Treating NPS as a target metric** — gameable; teams pressure-prompt 9-10 ratings
- **Ignoring the verbatim** — the open-ended follow-up ("why did you give that score?") is more informative than the score
- **No segmentation** — overall NPS hides high promoter / high detractor split
- **Weekly NPS** — too noisy; quarterly minimum

NPS is best as a *trend over time within segments*, with verbatim analysis. As a single number on a dashboard, it's near-useless.

## CSAT vs NPS vs CES

Three customer-satisfaction surveys, used differently:

| Metric | Question | Best for |
|---|---|---|
| **CSAT** (1-5 or 1-7) | "How satisfied with [thing]?" | Specific interactions (post-support, post-task) |
| **NPS** (0-10) | "How likely to recommend?" | Overall product loyalty |
| **CES** (Customer Effort Score) | "How easy was it to [task]?" | Specific workflows / friction points |

Each has its place. Asking all three on every survey produces respondent fatigue and shallow data.

## Sample size for stat-significant survey results

For a binary outcome (e.g. % satisfied), confidence interval width depends on sample:

```
Sample of 100  → ±10% margin of error at 95% CI
Sample of 400  → ±5%
Sample of 1000 → ±3%
```

For most product decisions, **300-500 responses** in a clean segment is enough. More than 1000 is rarely necessary unless you're measuring small differences.

For multi-segment analysis: each segment needs its own sample size.

## Likert scales

The most-common survey response format:

```
Strongly disagree | Disagree | Neutral | Agree | Strongly agree
       1              2          3         4          5
```

5-point and 7-point scales are standard. 7-point gives finer granularity but more cognitive load. **5-point is the safe default.**

Avoid:
- 4-point (no neutral, forces preference) — only use intentionally
- 10-point (decision fatigue, false precision)
- Mixed scales in one survey (1-10 and 1-5 in adjacent questions)

## In-product vs email surveys

| | In-product | Email |
|---|---|---|
| Response rate | 5-30% | 1-5% |
| Bias | Active users only | Whole list, but recall-based |
| Question count | Should be 1-3 | Can be 10-20 |
| Best use | Specific interaction (post-task CSAT) | Periodic NPS, deeper research |

Mix both for different research questions. In-product surveys with 1-3 questions perform best.

## Open-ended vs closed questions

| Closed (multiple choice, scale) | Open (free text) |
|---|---|
| Quantifiable | Qualitative; needs coding |
| Faster to analyze | Richer signal |
| Limited to known options | Surfaces unknowns |
| 80% of survey questions | 20% of survey questions |

Best surveys mix both. A closed score followed by "Why did you give that score?" doubles the value at low cost.

## Tools

- **Typeform** — clean UX, good response rates
- **SurveyMonkey** — old but robust
- **Google Forms** — free, basic
- **Qualtrics** — enterprise; advanced logic, conjoint, MaxDiff
- **Sprig / Hotjar / Pendo** — in-product surveys
- **Wynter** — B2B-specific message/positioning surveys

## Common failure modes

- **Using surveys for discovery** — they can't generate insights, only validate hypotheses
- **Treating quotes from open text as quantitative** — "30% mentioned X" requires coding 1000+ responses, not 5
- **Ignoring response bias** — who *answers* a survey is not who *uses* the product
- **Survey-driven feature roadmaps** — "what features do you want?" produces a competitor's feature list, not your strategy
- **No follow-up interviews** — quant signal alone is shallow; pair with [user interviews](user-interviews.md) for *why*
- **Asking 50 questions, getting 100 responses** — completion rates collapse; data unusable

## Surveys in the discovery toolkit

Surveys are the **scale** layer of the research stack:

| Method | Sample | Depth |
|---|---|---|
| [Ethnography](ethnography.md) | 5-10 | Deepest |
| [Interviews](user-interviews.md) | 10-30 | Deep |
| [Diary studies](diary-studies.md) | 10-15 | Deep + longitudinal |
| [Usability testing](usability-testing.md) | 5-15 | Behavior-deep |
| **Surveys** | **300-1000+** | **Shallow but broad** |
| [A/B testing](ab-testing.md) | 1000+ | Behavioral, narrow |

Use surveys when the research question is breadth. Don't use surveys when it's depth.

## See also

- [User interviews](concepts/user-interviews.md) — the qualitative complement
- [A/B testing](concepts/ab-testing.md) — behavioral quant complement
- [ODI](concepts/odi.md) — survey-driven importance × satisfaction methodology
- [PMF](concepts/pmf.md) — Sean Ellis test is a (good) survey
- [Vanity metrics](concepts/vanity-metrics.md) — many survey-derived metrics are vanity if not segmented
