# Five-Second Test

> Quick UX test. Show a user a screen for 5 seconds, hide it, ask what they remember. Tests *clarity of value, hierarchy, and first impression*. Cheap, fast, surprisingly informative.

## The mechanic

```
1. User sees screen for exactly 5 seconds
2. Screen hides
3. Ask: "What is this for?"
4. Ask: "What stood out?"
5. Ask: "Who do you think it's for?"
```

Optional follow-ups:
- "What would you do next?"
- "How would you describe what you saw?"

Total time per user: 1–2 minutes. Sample size: 20–50 users for a robust signal.

## What it tests

The first 5 seconds are when users decide whether to continue. The test surfaces:

- **Value clarity** — can they tell what the product does?
- **Audience match** — do they think it's for *them*?
- **Hierarchy** — what visually dominates? (often not what you intended)
- **Memorability** — what sticks after the screen disappears?
- **Confusion** — what made them go "wait, what?"

## Famous failure modes the test catches

| Issue | What users say |
|---|---|
| Vague hero | "Some kind of software?" |
| Wrong audience implied | "Looks like it's for engineers" (when target is marketers) |
| Buried CTA | "I didn't see a button" |
| Generic visual | "Could be any SaaS landing page" |
| Tagline failure | "I have no idea what they actually do" |
| Logo dominance | "Just remember the logo, not the product" |

A landing page that produces "I'm not sure what this does" 60% of the time has a value-clarity problem regardless of conversion data.

## When to run it

✅ **Landing pages** — most common use; first 5 seconds determine bounce rate
✅ **Empty states** — what does a new user see on first open?
✅ **Pricing pages** — does the right plan stand out?
✅ **Marketing emails** — what catches the eye in inbox preview?
✅ **App store screenshots** — most users skim 3-5 seconds before deciding to install
✅ **Marketing creative** — ads, social posts

## When not to run it

❌ Tasks requiring extended attention (form filling, deep workflows)
❌ Discovery (understanding *why* — use [interviews](user-interviews.md) instead)
❌ B2B products with long evaluation cycles (the 5s isn't representative)

## Sample size

| # users | Confidence |
|---|---|
| 5 | Directional, anecdotal |
| 15–20 | Robust qualitative signal |
| 50+ | Quantifiable percentages on common reactions |

UsabilityHub's research suggests **15 users** is a sweet spot for most landing-page tests.

## Tools

- **UsabilityHub / Lyssna** — purpose-built; runs paid panels
- **Maze** — broader UX testing including 5-second
- **PingPong / userlytics** — alternatives
- **DIY** — show screenshots in interviews; same result, lower volume

## Worked example

A B2B analytics startup runs a 5-second test on their new homepage with 20 users.

Results:
- 14/20 said "analytics tool" (✅ category clear)
- 6/20 said "for developers" (❌ target was business analysts)
- 18/20 mentioned the chart screenshot (visual hierarchy correct)
- 4/20 noticed "free trial" CTA (❌ buried)
- 2/20 said "for sales teams" (❌ wrong segment entirely)

Conclusions:
1. Audience signaling is broken — 30% mistarget
2. CTA needs to dominate more
3. Either rewrite copy to anchor on "business analyst" or accept the mistarget

A traditional usability test would surface task failures. The 5s test surfaced *positioning* failures.

## Five-second test vs first-click test

Adjacent technique:
- **5-second test** — what does the user *understand* after a quick look?
- **First-click test** — given a goal, where does the user click first?

Use 5-second for clarity/positioning. First-click for navigation/IA. Often paired.

## Common failure modes

- **Too few users** — 3 users tells you nothing
- **Cherry-picking responses** — confirmation bias on the data
- **Testing your own design with your team** — biased panel
- **Interpreting "didn't notice X" as fixable bug** — sometimes attention is finite, the question is *which* X to make notice
- **Running once** — 5s tests should iterate; test, change copy, re-test, compare

## See also

- [Prototyping](concepts/prototyping.md) — 5-second tests work on prototypes too
- [User interviews](concepts/user-interviews.md) — the deeper companion
- [A/B testing](concepts/ab-testing.md) — quantitative confirmation after 5s test directs the changes
- [Aha moment](concepts/aha-moment.md) — first impression is the gateway to activation
