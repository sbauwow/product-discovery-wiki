# Diary Studies

> A longitudinal research method where users self-report their experience over days or weeks. Captures behavior across **time** that single-session interviews and [usability tests](usability-testing.md) cannot.

## Why time matters

Many product experiences only reveal themselves across time:

| Phenomenon | Why diary studies catch it |
|---|---|
| First-week onboarding decay | Day 1 enthusiasm vs day 7 confusion |
| Habit formation (or failure) | Did they come back? When? Why? |
| Trigger-action-reward loops | What made them open the app on day 3? |
| Edge cases | Tax-quarter-end, vacation, illness — single-session misses |
| Mood-driven usage | Tired user vs alert user behaves differently |
| Multi-tool workflows | Steps span days; can't observe in one sitting |

A 60-minute session is a snapshot. A diary study is a video.

## How a diary study works

```
DAY 0 (kickoff)
├── Brief participants on what to log and how often
├── Tool setup (app, email prompts, paper diary)
└── Show example entries

DAYS 1-N (capture)
├── Participant logs entries when [something specific] happens
│   - "Every time you open the app"
│   - "Every time you encounter the problem"
│   - "Daily at end of work"
├── Researcher monitors for incomplete data and prompts
└── Optional: mid-study check-in interviews

DAY N+1 (debrief)
├── 1-on-1 interview reviewing the diary
├── Probe specific entries
└── Surface patterns across the period
```

Total: typically **5-30 days**. Most useful at 7-14 days.

## Capture methods

### Active diary
User logs entries when prompted to (e.g. "every time you used the product").

Format options:
- App-based (Dscout, Indeemo, dScout) — modern standard
- Email-prompted form — DIY, lower friction
- Paper journal — for physical workflows
- Voice recordings — fastest input

### Passive diary
Researcher captures data without active user input:
- Screen recording
- Usage logs from product
- Wearable data (rare)

Active = richer, lower volume. Passive = higher volume, less context.

### ESM (Experience Sampling Method)
A specific active variant: random or scheduled prompts ("how are you feeling about [X] right now?"). Captures in-the-moment state without recall bias.

## What to ask participants to log

Bad: "Tell us your thoughts."
Good: structured prompts.

Example log template (per entry):
```
TIMESTAMP: ____________
WHAT YOU WERE TRYING TO DO: ____________
WHAT HAPPENED: ____________
HOW DID YOU FEEL? (😊 😐 😤): ____________
PHOTO/SCREENSHOT (optional): ____________
1-2 SENTENCES: ____________
```

Structure forces consistent data; free text alone produces unusable variance.

## Sample size

| # participants | Use case |
|---|---|
| 3-5 | Pilot, format validation |
| 8-12 | Most studies — saturation usually here |
| 15-20 | Multi-segment studies, more confidence |
| 30+ | Quantitative claims about diary entries |

Like other qualitative methods, returns diminish past ~12 in a single segment.

## When to use

✅ **Onboarding/activation research** — first 1-2 weeks of new user life
✅ **Habit formation studies** — does usage stick?
✅ **Pre-purchase journey** — buyers researching over weeks
✅ **Complex workflows** — happens irregularly across days
✅ **Emotional / motivational research** — ESM-style
✅ **Validating a [Hooked](hooked.md) loop hypothesis**

## When less useful

❌ Quick UI tweaks — overkill, use [usability testing](usability-testing.md)
❌ One-off task observation — use ethnography or moderated session
❌ Massive segment studies — use [surveys](surveys.md)
❌ When recruit can't commit 7+ days

## Recruiting

Harder than for one-shot studies. Participants commit days, not minutes. Pay accordingly:
- 7-day study: $150-300 typical
- 14-day study: $300-600
- Plus completion bonus to encourage finishing

Drop-out rate is high (30-50%). Over-recruit by 2x.

## Worked example: SaaS onboarding diary

Goal: understand week-1 experience for new users of a B2B analytics product.

Setup:
- Recruit 12 new signups (in-product intercept after signup)
- Compensate $250 + $50 completion bonus
- 14-day study via Dscout app
- Daily prompt at 5pm: "Open the diary entry, answer 3 questions about today"

Findings (typical pattern):
- Days 1-2: high enthusiasm; users explore, set up first dashboard
- Day 3: friction — couldn't find a feature they expected; ~40% logged frustration
- Days 4-6: silence — most users didn't open diary; later interview reveals they didn't open the product either
- Day 7: re-engagement triggered by the weekly summary email — surprise insight: email was the trigger, not in-product behavior
- Days 8-14: split into "stuck" and "thriving" cohorts; thriving users had collaborated with a teammate on day 7

Implications:
- Day-3 friction needs onboarding intervention
- Email trigger more powerful than expected; double down
- Multi-user setup correlates with retention; push during onboarding

None of this comes from a single interview or usability test.

## Synthesis

Diary studies produce volume — 12 users × 14 days × 3 entries = 500+ data points. Synthesis approaches:

1. **Per-user timeline** — what happened to each user across days
2. **Daily aggregation** — what happened on day 1 across users
3. **Theme coding** — tag entries by topic; surface frequencies
4. **Quote pulls** — verbatim entries that crystallize patterns
5. **Mid-study interviews** — supplement raw entries with explanation

Tools: Dovetail, Notably, or spreadsheet for small studies.

## Common failure modes

- **No structure** — free-form entries become unusable
- **Over-prompted** — fatigue causes drop-off
- **Under-prompted** — entries thin and uninformative
- **No mid-study check-in** — drift goes undetected until end
- **Wrong people** — "active users" instead of "new users" gives wrong slice
- **Treating diary as primary** — diary entries should be supplemented with interviews; raw entries lack interpretive context

## See also

- [Ethnography](concepts/ethnography.md) — single-session field observation, shorter timeframe
- [User interviews](concepts/user-interviews.md) — paired with diary debrief
- [Cohort analysis](concepts/cohort-analysis.md) — quantitative cousin; diary studies surface the *why* behind cohort curves
- [Hooked](concepts/hooked.md) — diary studies are how you validate habit-loop hypotheses
- [Aha moment](concepts/aha-moment.md) — diary studies surface what users *experience* as the aha
