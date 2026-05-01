# PRD vs One-Pager

> Sources: Marty Cagan (anti-PRD essays at SVPG), Lenny Rachitsky (modern PRD templates), Amazon (working backwards / PR-FAQ). The single most contested artifact in product management. Strong opinions on both sides.

## What a PRD is

**Product Requirements Document.** Traditional spec for a feature or product. Describes what should be built, for whom, why.

Typical sections (verbose template):
1. Problem statement
2. Background / context
3. Goals / non-goals
4. User stories / scenarios
5. Functional requirements
6. UX requirements / mocks
7. Technical considerations
8. Acceptance criteria
9. Metrics / success
10. Timeline / dependencies
11. Open questions
12. Appendices

Long PRDs run 20-80 pages. They are the dominant artifact in big-company product management.

## Why traditional PRDs fail (Cagan's critique)

Cagan's argument across multiple essays: long PRDs are a **fundamental mistake** in product orgs. Reasons:

### 1. They confuse output with outcome
The PRD describes *what to build* — output. The team should be assigned *what to move* — outcome. Detailed specs implicitly assume the spec is right.

### 2. They are written too early
Detailed requirements written before user testing or [discovery](continuous-discovery.md) hardcodes assumptions that will be wrong.

### 3. They generate waste
Time writing 50 pages → time writing 50 pages of *fictional* feature description that gets revised 10 times. Most words never load.

### 4. They reflect feature-team mode
Long PRDs are typical of [feature teams](feature-vs-product-team.md) — teams given specs to build. [Product teams](feature-vs-product-team.md) need *problems*, not specs.

### 5. Engineers ignore them
Engineers read what's necessary to build, ignore the rest. Time spent on the PRD's full prose is read by no one.

### 6. They are political artifacts, not engineering ones
Long PRDs exist to satisfy stakeholders ("we documented it"), not to help engineers. They're CYA, not specs.

## The alternatives

### 1. The one-pager
Cagan's recommendation. ~1 page (sometimes 2). Includes:
- Problem (1-2 paragraphs)
- Outcome / metric (1 paragraph)
- Hypothesis / approach (1 paragraph)
- Risks / unknowns (bullets)
- Links to deeper artifacts (designs, research, OST branch)

The one-pager is a **living problem statement**. It evolves as discovery happens. It does NOT specify implementation; that emerges through cross-functional design.

### 2. PR/FAQ ([Amazon's working backwards](pr-faq.md))
Write the press release first. Forces customer-language clarity. Used at Amazon in lieu of PRDs for net-new product launches.

### 3. RFC (Request for Comments)
Engineering-flavored. Decisions document with rationale, alternatives considered, tradeoffs. Common at GitHub, Stripe, Cloudflare.

### 4. Memo (Amazon's 6-pager)
Tight written prose, narrative format. Read silently at the start of meetings. Used for major decisions.

### 5. Design Doc
Engineering-led. Architecture, data flow, API design. Often paired with a one-pager or PRD for product context.

### 6. Notion / Linear / shared docs
Modern stack: collaborative living docs that combine product context, design assets, engineering notes, links to relevant tools. Less formal, more useful.

## When a PRD-style artifact is justified

Even Cagan acknowledges some cases need detailed specs:

✅ **Compliance / regulated products** — FDA, FedRAMP, financial services. Auditors need the spec.
✅ **Cross-team interface contracts** — when team A's deliverable becomes team B's input. Specs as contracts.
✅ **API design** — public APIs are external commitments; spec rigor matters.
✅ **Vendor handoff** — outsourced engineering needs precise specs.
✅ **High-risk migrations** — database schema changes, billing system rewrites — need detailed plans.

## What a useful one-pager looks like

```
WHAT WE'RE WORKING ON
─────────────────────
[Outcome]: Increase trial→paid conversion from 4% to 7% in Q2.

WHO + WHY
─────────
Target: Free-tier users who reached activation but haven't converted by day 14.
Insight from interviews: 60% of these users say they "want to keep using" but
"haven't decided" — pricing friction more than value uncertainty.

APPROACH (current best bet)
───────────────────────────
1. Replace generic upgrade banner with usage-based contextual prompt
2. Add 14-day-extension offer instead of immediate cutoff
3. Surface team-pricing CTA when user invites a collaborator

These are *hypotheses*. Discovery in progress; details may change.

RISKS / UNKNOWNS
────────────────
- May reduce free-tier viral spread if too aggressive
- Pricing-engineering team needs to enable extension logic
- Will A/B test before broad rollout

LINKS
─────
Discovery doc: [link]
Designs: [link]
OST branch: [link]
Sales / CS feedback: [link]

OWNERS
──────
PM: [name]    Design: [name]    Engineering: [name]
Stakeholders: Sales lead, CS lead
```

That's it. ~1 page. Links to deeper artifacts. Easily revised. No 50-page bloat.

## What changes when [discovery](continuous-discovery.md) is real

In a [continuous discovery](continuous-discovery.md) team with active [OSTs](opportunity-solution-tree.md):

- The OST replaces sections 1-4 of a traditional PRD (problem, context, goals, scenarios)
- The discovery work-in-progress replaces sections 5-6 (functional + UX requirements)
- Engineering design docs replace section 7 (technical considerations)
- The one-pager + cycle plan replaces sections 8-12 (acceptance, metrics, timeline)

The PRD as a single mega-document collapses into a portfolio of artifacts that *each do one thing well*. The one-pager is just the index.

## What good PRDs do (when they exist)

If your org requires a PRD-style artifact, optimize for:

| Quality | Description |
|---|---|
| **Brief** | <5 pages whenever possible. Long is not thorough. |
| **Outcome-anchored** | Lead with the change you're trying to produce, not the feature |
| **Linked, not embedded** | Link to designs, research, code, not paste them in |
| **Living, not frozen** | Updated as work progresses; date-stamped |
| **Authored, not committee'd** | One voice; one PM responsible; not a 7-stakeholder amendment war |
| **Reviewable in 10 minutes** | If it takes 30+ to read, it's too long for the audience that matters |
| **Test-driven** | Includes hypothesis + how you'll know if you're right |

## Common failure modes

- **PRD as everyone-please-sign-this contract** — political; long because it has to satisfy everyone
- **PRD before discovery** — describes a solution that hasn't been tested
- **PRD as substitute for cross-functional alignment** — writing replaces conversation; usually badly
- **PRD without metric** — described feature with no success criterion
- **PRD that engineers ignore** — symptom of broken process, not engineer fault
- **Multiple PRDs per quarter, none tied to a coherent strategy** — feature factory in document form

## Starting fresh

If you have authority to change the artifact culture:

1. Replace 30-page PRDs with one-pagers
2. Add a [PR/FAQ](pr-faq.md) for net-new launches
3. Use OST + design docs + cycle plans for active work
4. Reserve formal PRD-style specs for the cases that need them (compliance, contracts, APIs)

If you don't have authority: write the document leadership demands, but *also* maintain the lighter artifacts that actually drive your team's work.

## See also

- [PR/FAQ](concepts/pr-faq.md) — Amazon's customer-facing alternative
- [Outcomes vs outputs](concepts/outcomes-vs-outputs.md) — long PRDs are output documents
- [Continuous discovery](concepts/continuous-discovery.md) — the practice that makes long PRDs unnecessary
- [Opportunity Solution Tree](concepts/opportunity-solution-tree.md) — replaces problem/scenario sections of a PRD
- [Strong PM](concepts/strong-pm.md) — writing tight one-pagers is a senior PM skill
