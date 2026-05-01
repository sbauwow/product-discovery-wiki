# Hooked / Habit-Forming Products

> Source: Nir Eyal, *Hooked* (2014). Model for designing products users *return to* without external prompting. Adjacent to [activation](aha-moment.md) but focused on long-term habit formation.

## The Hook Model

```
        ┌──────────► TRIGGER ──────────┐
        │             (external/internal)│
        │                               ▼
   INVESTMENT                        ACTION
   (user effort,                    (simple behavior)
    storing value)                       │
        ▲                               ▼
        │           VARIABLE REWARD     │
        └─────────  (uncertain          ◄┘
                    payoff)
```

Four phases, looping:

### 1. Trigger
What prompts the user to act.
- **External:** notification, email, ad, badge, friend's share
- **Internal:** emotional state ("I'm bored", "I'm anxious") that triggers the user without external prompt

The transition from external → internal triggers is the goal. Habits are formed when the user reaches for the product without being told to.

### 2. Action
The simplest behavior in anticipation of reward.
- Pull-to-refresh on Twitter
- Scroll on Instagram
- Tap to play a video on YouTube
- Open an app

Should be one action, low friction, immediately rewarded.

### 3. Variable Reward
The payoff — but unpredictable. Skinner's variable-ratio reinforcement schedule, the most addictive pattern.

Eyal classifies three types:
- **Tribe** — social variability (likes, comments, mentions). Facebook, Instagram, Twitter.
- **Hunt** — resource variability (next thing in the feed, search results). Pinterest, Google, YouTube.
- **Self** — mastery variability (level up, score, completion). Duolingo, fitness apps, games.

Variability is the load-bearing element. **Predictable rewards stop being rewarding.** A slot machine that always paid out the same wouldn't hook anyone.

### 4. Investment
The user puts something *in* — content, data, social connections, time, money. This:
- Increases perceived value (sunk cost)
- Improves the next session's experience (more data → better recs)
- Loads the next trigger (notifications about user's content)

Investment closes the loop and makes it *self-reinforcing*. The next trigger is more likely *because* of the investment.

## Why it works

Habit formation is variable-reward conditioning + investment. After enough loops, the user no longer needs external triggers — internal emotional states fire the loop.

```
Habit strength = frequency of loop × hedonic value of reward × investment depth
```

The product becomes an emotional regulation tool. Users open Twitter when bored, Instagram when lonely, Headspace when anxious. They're not "deciding" to use the app; the emotion fires the trigger.

## Examples

| Product | Trigger | Action | Variable reward | Investment |
|---|---|---|---|---|
| Instagram | Boredom (internal); push (external) | Open, scroll | Photos from friends/follows (tribe) | Posting, following |
| Twitter | FOMO; mentions | Refresh feed | Latest takes (hunt) | Tweets, follows |
| Duolingo | Reminder | Lesson | Progress, streak (self) | Streak, XP, friends |
| Slack | @mention | Open thread | Replies, decisions (tribe) | Messages, channels |
| LinkedIn | Connection request | Open profile | Profile views, jobs (tribe + hunt) | Profile, network |

## Ethical considerations

The Hook model is a *neutral* description of behavior. Same model that makes Duolingo work also makes Candy Crush addictive and Instagram doom-scrollable.

Eyal himself wrote *Indistractable* (2019) as a counter-book on resisting the same patterns he documented. The model is **value-neutral**; the application is not.

Test: would the user, after 30 days of habit, **thank** you?
- Duolingo user with 30-day streak feels accomplished → yes
- Twitter user with 30-day daily-scroll feels worse → likely no

Eyal calls this the "manipulation matrix":

```
                  DOES MAKER USE IT?
                  No              Yes
              ┌────────────┬────────────┐
        No    │ Peddler    │ Dealer     │   ← ethical red flag
DOES IT       │ (vitamins) │ (drugs)    │
HELP USER?    ├────────────┼────────────┤
        Yes   │ Entertainer│ Facilitator│   ← ethical
              │ (games)    │ (Duolingo) │
              └────────────┴────────────┘
```

Build "facilitator" products (you use it AND it helps). Avoid "dealer" products (you wouldn't use it AND it harms).

## Where Hooked fits in discovery

Most useful **after** product/market fit is established:
- [Aha moment](aha-moment.md) gets users to first value
- Hook model gets them to come back
- Together they define the activation → retention bridge

Less useful before PMF — there's no point optimizing habit loops on a product nobody wants.

## Common failure modes

- **Triggers without value** — notifications that pull users in but deliver no reward → users mute or churn
- **Predictable rewards** — variability is the point; constant payoff loses its grip
- **No investment phase** — without investment, the loop doesn't compound; user has no reason to prefer your app over competitor's
- **Dealer products** — manipulating users into habits that don't help them. Short-term wins, long-term backlash, regulation.

## See also

- [Aha moment / Activation](aha-moment.md) — gets users *into* the loop
- [Cohort analysis](cohort-analysis.md) — measures whether the hook is working
- [North Star Framework](north-star.md) — habit-formation often shows up as the North Star (Spotify "time spent listening")
- [Pirate Metrics](pirate-metrics.md) — Hooked drives the Retention stage
