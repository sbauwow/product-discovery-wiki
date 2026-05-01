# Cold Start Problem

> Source: Andrew Chen, *The Cold Start Problem* (2021), former Uber growth, current a16z partner. The hardest problem in network/marketplace product strategy: how to launch a network when it has zero users and therefore zero value.

## The paradox

```
Network is valuable BECAUSE many users use it.
Few users WILL use it because it isn't yet valuable.
        ↓
        cold start
```

Without users, no value. Without value, no users. The standard launch playbook (build product → market → users come) fails for network products.

## Chen's five-stage model

```
1. The Cold Start (zero → working atomic network)
2. Tipping Point (atomic network → product can sustain itself)
3. Escape Velocity (compound, defend, expand)
4. The Ceiling (slow growth at scale)
5. The Moat (defensibility against incumbents)
```

The book's bulk addresses stage 1, the hardest. Stages 2-5 cover what comes after.

## The Atomic Network

The single most important concept. Every network has a **minimum viable network** — the smallest dense unit at which the product produces value.

| Product | Atomic network |
|---|---|
| Slack | A single team of 3+ people |
| Tinder | One city with ~1000+ users per gender |
| Uber | A single neighborhood with ≥5 drivers, hourly density |
| WhatsApp | One pair of communicators |
| Zoom | Two people on a call |
| Airbnb | One city with ~50 listings + travelers |
| Facebook (early) | One college campus |

Atomic network ≠ user count. It's the **density** required for the product to "work" for someone using it.

Strategy: don't try to launch the global network. Launch *one atomic network at a time*. Saturate it. Repeat.

## "Hard side first"

Multi-sided networks have a **hard side** and **easy side**:

- **Easy side** — those who get value from the network being there (Uber riders, Airbnb guests, Tinder users seeking matches)
- **Hard side** — those who *create* value for others (Uber drivers, Airbnb hosts, Tinder users being matched with)

Without the hard side, the network is empty. Without the easy side, the hard side has no audience.

**Rule: solve the hard side first.** Drivers before riders, hosts before guests, content creators before consumers.

Tactics for the hard side:
- Pay them directly (Uber's driver bonuses, Substack's writer guarantees)
- Build them yourself (Reddit's founders posting under fake accounts, Yelp seeding reviews)
- Give them a tool that's useful even alone (Instagram filters work without followers)
- Lower their cost to participate (creator-friendly tools, low fees)

## The single-player mode trick

Even network products should ideally have **value at user 1**:

- Notion: useful as a personal note app even with zero collaborators
- Figma: useful as a single-designer tool before teams
- Strava: useful as a personal fitness tracker before it's social
- Pinterest: useful as a personal mood board before social discovery

A single-player mode lets users onboard productively while you bootstrap the network. Without it, you depend on every user arriving in a pre-formed network — which they don't.

Pure-network products (Tinder, Uber) can't do this; they have to bootstrap density harder. But many "network" products are actually utilities-with-network-bonus, and that's a much easier path.

## Tipping point indicators

How do you know your atomic network is working? Andrew Chen's signals:

1. **Self-sustaining without subsidies** — once you stop paying drivers, do they keep coming? (No = pre-tipping. Yes = tipping.)
2. **Organic growth** — new users arrive without acquisition spend.
3. **Density retention** — atomic network density stays high after launch hype.
4. **Word of mouth** — users actively recruit others without prompts.
5. **Multi-homing reduces** — users stop using competitors as primary.

Until these signals appear, the atomic network is fragile. Premature scaling kills cold-start products.

## The launch playbook

Chen's pattern, distilled:

```
1. Pick ONE atomic network (one city, one campus, one community)
2. Manually recruit the hard side (concierge, paid, founder-led)
3. Recruit the easy side once hard side is dense enough
4. Solve all bugs, all friction, all everything in this single network
5. Grow density UNTIL the network self-sustains (tipping point)
6. Only then expand to a second atomic network
7. Repeat, learning the playbook
8. Eventually parallelize launches as the playbook becomes known
```

Counter-intuitive: don't launch in 50 cities. Launch in 1. Saturate it. Then 2. Then 5. The temptation to launch broadly is strong; resist it.

## Worked example: Tinder's launch

Tinder launched at USC. Single atomic network = USC student body.
- Founders threw parties to onboard hundreds of students at once
- Hard side and easy side were the same people (everyone is "looking")
- Density at one campus made matching meaningful
- Network compounded within USC; spread to other LA campuses; then nationally

Had Tinder launched a "national dating app" with national marketing on day 1, the same number of users spread thin → no city had density → product wouldn't work → would have died.

## Worked example: Uber's launch

Uber launched in San Francisco's downtown.
- Hard side (drivers): paid bonuses, surge guarantees
- Easy side (riders): single city, single neighborhood
- Achieved tipping point: drivers earned enough that bonuses weren't required
- Then expanded to next city, repeating the playbook

Each new city was its own cold-start problem. The playbook scaled because Uber was running 100+ atomic-network bootstraps in parallel by year 3.

## Common failure modes

### 1. National launch without atomic network
Spread thin across 50 markets, density inadequate in any one, product feels broken everywhere. Frequent in well-funded startups that can afford broad spend but burn through it before tipping anywhere.

### 2. Easy side first
"We'll build a marketplace; sellers will come because there's demand!" — usually false. Sellers don't show up to an empty marketplace. Have to subsidize the hard side first.

### 3. Confusing growth with tipping
Paid acquisition can mask a fragile network. Cut spend; see if growth survives. If not, pre-tipping.

### 4. Premature scaling
Atomic network looks good → expand to 10 more cities → spread thin → original city's density drops → tipping unwinds.

### 5. Wrong atomic network
"Our atomic network is the world." → no it isn't. Find the smallest dense unit; saturate that.

### 6. Chasing wrong side
Focusing on the side that's easier to acquire; forgetting the hard side has to be solved first or no value exists.

## When cold-start framing applies

✅ Marketplaces (Uber, Airbnb, eBay)
✅ Social networks (Facebook, LinkedIn)
✅ Communication tools (Slack, WhatsApp)
✅ Multi-sided platforms (App Store, Substack)
✅ Local-density products (food delivery, dating)
✅ Data network effects products (where data from users compounds)

## When less applicable

❌ Pure SaaS utility (Notion as a personal tool — no network required)
❌ E-commerce direct-to-consumer (no buyer-seller network; just store)
❌ Content sites without UGC
❌ B2B tools with no cross-customer value

(Many of these *do* have weak network effects, but the cold-start problem isn't existential.)

## See also

- [Network effects](concepts/network-effects.md) — what cold-start is bootstrapping toward
- [PMF](concepts/pmf.md) — network products often have *segment-specific* PMF before global PMF
- [Growth loops](concepts/growth-loops.md) — once tipping is reached, loops compound
- [Crossing the Chasm](concepts/crossing-the-chasm.md) — adjacent: bridging early-adopter to mainstream
- [Wardley Mapping](concepts/wardley-mapping.md) — strategic positioning of network products at different evolution stages
