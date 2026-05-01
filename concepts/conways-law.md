# Conway's Law

> Source: Melvin Conway, "How Do Committees Invent?" (1968). The most-cited and most-underused law in software organizations.

## The law

> "Any organization that designs a system (defined broadly) will produce a design whose structure is a copy of the organization's communication structure."

Translated: software architecture mirrors org chart. Whether you wanted it to or not.

## Why it's true

Two engineers in different teams must communicate via meetings, docs, tickets. Two engineers on the same team talk in person. The cost of communication shapes what gets built:

- Within-team interactions are cheap → fine-grained coupling, frequent change
- Across-team interactions are expensive → coarse-grained interfaces, infrequent change

Result: code modules tend to align with team boundaries. The shape of the org becomes the shape of the system.

## Empirical support

Studies (MIT, Microsoft Research, Carnegie Mellon, ~2008-2015) confirmed Conway empirically:
- Codebase modularity correlates with org modularity
- Code with tight cross-team coupling has more bugs
- Teams that change together produce code that changes together

The law is descriptive (this is what happens) and predictive (this is what *will* happen).

## Worked examples

### Case 1: company merges
TWO companies merge. Each had its own auth system. Post-merger:
- The two auth systems remain separate for years
- Bridging code becomes more complex over time
- Eventually rewritten as a unified system... by a single team

The org structure (two separate teams) → produced two systems → only collapses when one team owns it.

### Case 2: monolith breaks up
Monolithic codebase → org grows → "we should microservice this."
- If team boundaries are drawn first, microservices align cleanly
- If microservices are designed first without team alignment, they get shared by multiple teams → coupling reappears at the team level

The architecture follows the org. Skipping the org-design step produces brittle architecture.

### Case 3: platform team
Engineering needs shared infrastructure. Two options:
- **No platform team** → every team builds its own version → 5 incompatible CI systems
- **Platform team owns it** → shared CI system used by all → coherent architecture

Org structure (existence of platform team) determines whether the system has a unified or fragmented infrastructure.

## The Inverse Conway Maneuver

If org structure determines architecture, **design the org you need to produce the architecture you want.**

```
Step 1: Decide what architecture you want
  e.g. "We want microservices owned by autonomous teams"
Step 2: Design teams that match that architecture
  e.g. "One team per service, ~5-9 people each, full ownership"
Step 3: The architecture emerges naturally
  Teams build what their boundaries allow them to build
```

Inverse Conway Maneuver, coined by James Lewis at Thoughtworks (~2014). Common in microservice-adopting orgs.

The maneuver explains:
- Why "let's do microservices" without team restructuring fails (org still pulls toward monolith)
- Why team reorgs precede architectural changes in healthy companies
- Why the same engineering team can't successfully maintain wildly different architectures over time

## Practical implications

### 1. Org design = architecture design
Reorganization is an architectural decision. Treat it that way.

### 2. Scaling shapes shapes
Going from 5 → 20 → 50 → 200 engineers requires architectural shifts. The org structure that worked at 5 produces a different (worse) architecture at 50 if not redesigned.

### 3. Beware accidental coupling
If team A and team B are working on different products but share the same database, they will end up tangled. Conway's law applies even when undesired.

### 4. Communication structure ≠ org chart
Conway said "communication structure," not "reporting structure." Two teams that report separately but actually meet daily form a "single communication structure" — and produce single-system architecture, regardless of what the org chart says.

### 5. Modularity requires team modularity
A modular system requires modular teams. Trying to enforce modular code without modular teams = architecture rot over time.

## When Conway's law dominates

Real-world signals that Conway's law is shaping your system:

- "Why is this API so weirdly carved?" → look at the team boundaries
- "We can't change this without coordinating five teams" → the architecture has the same shape as the org
- "Migrating to microservices is taking forever" → the org probably hasn't fully restructured
- "We have three notification systems" → three teams each built their own

## Connection to [Team Topologies](team-topologies.md)

Skelton & Pais's *Team Topologies* (2019) operationalizes the inverse Conway maneuver. Four team types (stream-aligned, enabling, complicated-subsystem, platform) plus three interaction modes (collaboration, X-as-a-service, facilitating) — explicitly designed to produce desired system architectures.

If Conway's law is the *observation*, Team Topologies is the *prescription*.

## Common failure modes

- **Ignoring the law** — designing architectures without considering team structure
- **Reorgs without arch follow-through** — restructuring teams but not letting code reorganize accordingly
- **Org churn** — frequent reorgs prevent any architecture from stabilizing
- **Reporting structure ≠ collaboration structure** — drawing org charts that don't match how work actually flows
- **Forcing architecture against org grain** — "we're going microservices regardless" — predictably fails
- **Accidental Conway** — products built by disconnected teams end up with disconnected UX

## See also

- [Team Topologies](concepts/team-topologies.md) — modern operationalization
- [Product Operating Model](concepts/product-operating-model.md) — broader org-level frame
- [Empowered team](concepts/empowered-team.md) — the team-level unit Conway predicts will shape the architecture
