# Onboarding Patterns (FTUX)

> First-Time User Experience patterns. The tactical UX vocabulary for getting new users to [activation](aha-moment.md). Mostly conventional knowledge; the discipline is choosing the right pattern for the right product.

## Why onboarding matters disproportionately

```
Day 1 attention: 100%
Day 2 attention: ~30%
Day 7 attention: ~5%
```

The first session is when users decide whether the product is worth learning. Bad onboarding doesn't just slow adoption — it *prevents* it. A user who bounces in the first 60 seconds will likely not return.

The pattern library is well-known; the failure is choosing wrong.

## The major patterns

### 1. Empty states
What the user sees before any data exists in their account.

```
No projects yet.

[Big illustration]
"Create your first project to get started."
[Create project button]   [Watch 60-sec demo]
```

Best practice: every empty state is a *recruitment moment* for the next action. Don't show a literal blank screen.

Effective empty states:
- Show what the *populated* state will look like (preview)
- Suggest a single, clear next action
- Optionally offer demo data / templates

### 2. Sample data / templates
Pre-populated content so users see the product *working* before they create anything.

Examples:
- Notion's template gallery
- Figma's "Try in browser" with sample design
- Linear's pre-filled issues for new accounts
- Datadog's demo dashboard

Tradeoff: lower-effort onboarding vs delayed sense of ownership. Templates that import-then-customize hit the sweet spot.

### 3. Guided tours / coachmarks
Sequential overlays pointing at UI elements.

```
[1/5] "Click here to create a new task"  ← arrow points at button
[2/5] "Set a due date with the calendar"
[3/5] "Tag teammates with @mention"
...
```

Most overused, most ineffective pattern. Users skip; guides feel patronizing; takes them away from doing.

When tours work:
- Truly novel UI (genuinely unfamiliar paradigm)
- Power features users wouldn't discover (advanced shortcuts)
- Optional, not gating ("Would you like a quick tour?")

When they fail:
- Tour while user is trying to do something
- Long sequences (>5 steps)
- Replicating discoverable interactions
- "Click 'next' to continue" friction

### 4. Progressive disclosure
Hide advanced features until the user is ready. Show only what's needed for the current step.

```
Day 1 settings:        Day 30 settings:
- Account name          - Account name, plan, billing, SSO,
- Plan                    permissions, audit log, API keys,
- Save                    integrations, advanced security, ...
                          (everything available)
```

Reduces cognitive load on day 1. Surfaces advanced features only when needed.

Risk: hidden features remain undiscovered. Pair with contextual prompts ("Did you know you can also...").

### 5. Activation milestones (gamified)
Show progress toward key actions, often with checklists.

```
Get started (3 of 5)
✅ Create your first project
✅ Invite a teammate
✅ Connect a data source
☐ Generate your first report
☐ Set up notifications
```

Effective for products where the path to value has clear discrete steps. Slack's getting-started checklist is the canonical reference.

Risks: feels patronizing; users completing checklist for sake of completion (not value); activates on the wrong checklist items.

### 6. Tooltips / contextual help
Help that appears in context when needed, not in a sequence.

Example: hover on a setting → tooltip explains it.

Best when:
- User actively engaged in a task
- Help is brief (one sentence)
- Doesn't gate progress

Tools: Pendo, Appcues, Intercom, Userpilot.

### 7. Magic moment optimization
Reorganize entire onboarding around the **fastest path to [aha](aha-moment.md)**.

Example: Loom doesn't ask about your team size, role, or use case before recording. It just lets you record. The "magic" of seeing your first video shareable shapes everything else.

Pattern: defer setup. Get user to value first; collect details later.

### 8. Interactive product tour (sandbox)
Let users *do* the product in a contained mode (vs read about it).

Examples:
- Linear's marketing site has a usable Linear-in-browser
- Webflow's tutorial is *building inside Webflow*
- Stripe Checkout demo lets you make a test transaction

Higher production cost; dramatically higher conversion. Activates the user before they've signed up.

### 9. Personalization questions
"What brings you here?" "What do you want to accomplish?"

Used to:
- Branch onboarding to relevant flow
- Personalize empty states / templates
- Segment users for analytics / marketing

Risk: friction. Each question costs ~10-15% drop-off. Use sparingly. Maximum 3-5 questions, ideally optional.

### 10. Social proof in onboarding
Show that other users have succeeded.

Examples:
- "Joined by Stripe, Notion, and 50,000 other teams"
- "1,432 people created a project this week"
- Customer logos / testimonials inside onboarding flow

Reduces uncertainty for new users; signals credibility.

## Pattern selection by product type

| Product type | Best patterns |
|---|---|
| Solo productivity (Notion, Bear) | Sample data + empty-state-as-recruitment + magic moment |
| Team collaboration (Slack, Linear) | Activation checklist + invite-first onboarding + sandbox |
| Marketplace (Airbnb, Amazon) | Personalization (search context) + social proof + minimal onboarding |
| Power tool (Figma, Photoshop) | Templates + sandbox + progressive disclosure |
| Data / analytics (Datadog, Mixpanel) | Demo data + integration setup wizard + checklist |
| Consumer social (Instagram, TikTok) | Social context onboarding ("follow these accounts") + content first |

## What to avoid

- **Mandatory tours** — let users skip
- **Long forms** — break into steps; ask only what's necessary
- **Setup walls** — gating product use until full setup complete (especially "connect your data first")
- **Inconsistent voice** — onboarding writing tone doesn't match product
- **Empty state with nothing to do** — purely textual empty state with no action

## Measuring onboarding

Critical metrics:
- **Step-by-step funnel** ([funnel analysis](funnel-analysis.md)) — where do users drop?
- **Time to [aha moment](aha-moment.md)** — minutes from signup to first value
- **% reaching activation event** — by acquisition channel, by segment
- **Power-user predictors** — onboarding behaviors correlated with eventual [power users](power-user-analysis.md)

A/B test individual onboarding patterns. Each step is a candidate for optimization.

## Common failure modes

- **Designed by committee** — every team adds their step (security wants verification, sales wants context, marketing wants personalization, eng wants telemetry consent) → 14-step onboarding nobody completes
- **No magic moment focus** — onboarding optimizes for "completing onboarding" instead of "reaching value"
- **Tour for sake of tour** — coachmarks because "we should explain things"
- **No segmentation** — same onboarding for power user and casual; misses both
- **One-shot design** — built once, never updated as product changes
- **Adding steps under pressure** — every quarterly review adds another step "to capture this signup data"; never removes any
- **Confusion of completion with success** — measuring "% who finished onboarding" instead of "% who reached value"

## When to redesign onboarding

✅ Activation rate < 30%
✅ Time-to-aha > 10 minutes
✅ Onboarding hasn't been touched in 12+ months
✅ Major product redesign or new feature shipped
✅ Major segment shift (mobile launch, enterprise tier, new region)

## See also

- [Aha moment / Activation](concepts/aha-moment.md) — what onboarding aims to deliver
- [Funnel analysis](concepts/funnel-analysis.md) — how to measure step-by-step
- [Power user analysis](concepts/power-user-analysis.md) — what behaviors onboarding should encourage
- [PLG](concepts/product-led-growth.md) — onboarding is existentially important for PLG
- [Five-second test](concepts/five-second-test.md) — first impression of onboarding screens
- [Hooked](concepts/hooked.md) — onboarding kicks off the habit loop
