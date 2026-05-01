# Product Strategy

> Sources: Marty Cagan (*Empowered*, *Transformed*), Melissa Perri (*Escaping the Build Trap*), Richard Rumelt (*Good Strategy / Bad Strategy*), Christopher Lochhead (*Play Bigger*). The most-misunderstood layer in product orgs — and the most-missing.

## What strategy is NOT

- ❌ A roadmap (roadmaps are *outputs* of strategy)
- ❌ A vision (vision is *where*; strategy is *how given constraints*)
- ❌ Goals or OKRs (goals are *what to achieve*; strategy is *how*)
- ❌ A list of features
- ❌ A mission statement ("delight users with delightful products")
- ❌ Generic ambition ("be #1 in the market")

A strategy that fits any company isn't a strategy. It's slogan.

## What strategy IS (Rumelt's "kernel")

Rumelt's *Good Strategy / Bad Strategy* defines strategy as three components:

### 1. Diagnosis
A clear-eyed identification of the **specific challenge** the org faces. Not a list of problems — the *core* obstacle.

> "Our enterprise customers churn at 18% because the migration process takes 3 months and during that time their users find workarounds that make the platform feel optional."

Specific. Causal. Actionable.

### 2. Guiding Policy
The **chosen approach** to address the challenge. Not a goal — a *direction*.

> "We will eliminate the migration phase entirely by making the product work alongside existing tools, then progressively replace them as users see value."

Constraints implicit. Direction clear.

### 3. Coherent Actions
The **set of moves** that follow from the policy and reinforce each other. NOT a list of features — a coordinated set of decisions.

> - Build a Slack/Teams integration first (alongside existing tools)
> - Hire two integrations engineers
> - Pause the standalone-mode roadmap until Q4
> - Reposition messaging from "replace your stack" to "augment your stack"
> - Restructure sales comp to reward integration adoption

Each action only makes sense in light of the policy. They reinforce each other.

## Cagan's three layers

Cagan distinguishes:

| Layer | What | Example |
|---|---|---|
| **Vision** | Where we're going long-term | "Every team uses our product to ship better software" |
| **Strategy** | How we get there given constraints | Focus on enterprise; integrations-first; build moats via data |
| **Tactics** | What we do quarterly | Specific [OKRs](okrs.md), bets, [OSTs](opportunity-solution-tree.md) |

Most orgs have vision and tactics. The middle layer is missing — and that's why tactics drift, [feature factories](feature-factory.md) form, and roadmaps become wishlist negotiations.

## What good product strategy looks like

A good product strategy identifies:

1. **Focus** — what (and who) we're *not* doing/serving. Strategy is choosing.
2. **Insight** — a non-obvious belief about the market that we're betting on.
3. **Principles** — durable rules that resolve future trade-offs.

### Focus
> "We serve mid-market SaaS companies (50-500 employees) who already have product-led growth. We do not serve SMBs or Fortune 500. Their needs are different and we'd lose focus."

This says *what we won't do*. Most orgs won't put that in writing because it's politically painful. Painful = real.

### Insight
> "We believe the next decade of B2B will be agent-native (LLMs operating products on behalf of users), and that products designed for agents-first will accumulate a 10× UX moat over products retrofitted later."

A non-obvious bet. Falsifiable. Frames every other decision.

### Principles
> "When a feature only serves one segment, we say no.
> When in doubt, ship simpler over more capable.
> Pricing transparency over discount negotiation.
> Every roadmap question first asks 'does this fit our agent-native thesis?'"

Principles resolve future trade-offs without re-litigating strategy each time.

## Lochhead: category design

Christopher Lochhead's *Play Bigger* argues a different angle: the most-valuable companies *create new categories* rather than compete in existing ones.

- Don't be the best CRM → invent the "RevOps platform" category
- Don't be the best video conferencing → invent the "asynchronous video" category
- Category creators capture ~76% of the category's market cap

Category design is one strategic move; not the only one. But Lochhead's frame — design the category, not the product — is a useful lens for ambitious teams.

## How strategy connects to discovery

```
Strategy
   ↓
Outcomes ← strategy decides which outcomes matter
   ↓
[OST](opportunity-solution-tree.md) per outcome
   ↓
Solutions ← strategy decides which solutions fit (others get killed)
```

Without strategy, every opportunity looks equally important. The OST has nothing to anchor "should we?" against — only "could we?".

## Why most orgs lack strategy

- **Strategy is hard** — requires saying no in writing, which has political cost
- **Vision is easy** — "delight users", "be the leader" — uncontroversial, useless
- **Tactics feel like progress** — features shipped, OKRs hit, even without strategy
- **Founders avoid commitment** — keeping options open *feels* safer; in practice it diffuses focus
- **Mid-execs don't push up** — easier to execute given goals than to debate them

The result: a strategy vacuum. Tactics fill it ([feature factory](feature-factory.md)). [Roadmaps](roadmap-trap.md) become contracts. [Discovery](continuous-discovery.md) feels disconnected from the company.

## How to write one (Rumelt-style)

A 1–2 page document:

1. **Diagnosis** (1 paragraph) — what specific challenge?
2. **Guiding policy** (1 paragraph) — what's our chosen approach?
3. **Coherent actions** (5–10 bullets) — what we're doing, and *not* doing
4. **What we're betting on** (1 paragraph) — the non-obvious belief
5. **Falsifying conditions** (1 paragraph) — what would convince us we're wrong

Test: read it aloud. If a competitor could equally write this for *themselves*, your strategy isn't specific enough.

## Common failure modes

- **Strategy = vision** — confusing "where" with "how"
- **Strategy = goals** — confusing "what" with "how"
- **Strategy = roadmap** — confusing "output" with "approach"
- **Strategy as adjective list** — "we will be agile, customer-centric, ambitious" — meaningless
- **Strategy without saying no** — if it doesn't exclude, it's not strategy
- **Strategy never updated** — written once, ignored; treated as a doc, not a tool

## See also

- [Wardley Mapping](concepts/wardley-mapping.md) — strategic positioning analysis
- [OKRs](concepts/okrs.md) — tactics layer that should derive from strategy
- [Outcomes vs outputs](concepts/outcomes-vs-outputs.md) — strategy chooses which outcomes
- [Feature factory](concepts/feature-factory.md) — what fills the strategy vacuum
- [Build trap](concepts/build-trap.md) — Perri's diagnosis of strategy-less orgs
