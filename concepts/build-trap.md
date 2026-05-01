# The Build Trap

> Source: Melissa Perri, *Escaping the Build Trap* (2018). The most rigorous treatment of why product orgs degenerate into [feature factories](feature-factory.md).

## Definition

> Organizations stuck in **the build trap** measure success by *output* — features shipped, releases made — rather than by *outcomes* — value delivered to customers and the business.

Adjacent to [feature factory](feature-factory.md), but Perri's framing is more diagnostic. The *trap* explains *why* feature factories form: the org's measurement, incentive, and management systems all reward output, so the system locks in.

## The doom loop

```
Pressure to grow / show progress
        ↓
"Ship more features"
        ↓
Output goals set (roadmap, OKRs, deadlines)
        ↓
Teams measured on output completion
        ↓
Teams optimize output, not outcome
        ↓
Outcomes don't move
        ↓
Pressure to grow / show progress  (loop)
```

The trap is self-reinforcing because **output is legible**. Executives can see "30 features shipped". They can't easily see "we killed 12 bad ideas in discovery, saving 6 months of build cost."

## Perri's diagnostic questions

A team is in the build trap if it can't answer:

1. What's the *outcome* this work moves? (not output)
2. Who is the customer? What problem do they have?
3. What's the *evidence* this is the right solution?
4. How will we know if it worked?
5. What will we *stop* doing if it didn't?

If most answers are "I don't know" or "the roadmap says so," the team is trapped.

## Mechanisms of the trap

### 1. Output-based incentives
Promotion criteria reward shipping. Nobody gets promoted for *killing* a feature in discovery, even if the kill saved $2M.

### 2. Output-based reporting
Quarterly business reviews ask "what did you ship?" not "what did you learn?" or "what did you decide *not* to ship?"

### 3. Output-based planning
Roadmaps are feature lists with dates. Stakeholders treat them as commitments. See [roadmap trap](roadmap-trap.md).

### 4. Output-based contracts
Sales sells features ahead of build. Engineering must deliver to honor the deal. Discovery can't influence what was already sold.

### 5. Output-based hiring
Roles defined as "build X" rather than "own outcome Y." New PMs inherit feature lists, not problems.

## Escaping (Perri's prescription)

The book is structured as a transformation playbook. Key moves:

### 1. Establish product strategy

Most orgs have a vision and a roadmap, no strategy. Strategy = how you'll achieve the vision given constraints. Without it, every feature looks equally important.

### 2. Build the product kata

Lean from Toyota: an experimental learning loop run by every team:
- Where are we? (current state)
- Where do we want to be? (target state, outcome)
- What's the next step? (smallest experiment)
- What did we learn? (review)

### 3. Create a discovery culture

- Outcomes in OKRs, not outputs
- Discovery time protected (≥20% capacity)
- Customer access for teams
- Reward learning, not shipping

### 4. Restructure incentives

- PM career path tied to outcome impact
- Quarterly reviews ask "what did you learn / kill / ship that worked"
- Roadmap reframed as bets ("now/next/later" outcome columns)

## Why the trap is so common

Perri's structural answer:
- Shipping is **legible** to non-product execs
- Discovery is **invisible** until outcomes prove it worked
- Outcomes **lag** by months; output is **immediate**
- The org's lower-tier orgs (sales, finance, marketing) all want feature commitments
- Most product orgs were *founded* as feature factories; the cultural inertia is enormous

It's not that anyone wants the trap. It's the equilibrium most orgs collapse into.

## Connection to other concepts

- [Feature factory](feature-factory.md) — the symptom
- [Roadmap trap](roadmap-trap.md) — the artifact
- [HiPPO](hippo.md) — the decision pattern
- [Outcomes vs outputs](outcomes-vs-outputs.md) — the conceptual fix
- [Empowered team](empowered-team.md) — the org-design fix
- [Product strategy](#) — Perri's missing piece in most orgs

## See also

- [Feature factory](feature-factory.md)
- [Outcomes vs outputs](outcomes-vs-outputs.md)
- [Roadmap trap](roadmap-trap.md)
- [Empowered team](empowered-team.md)
