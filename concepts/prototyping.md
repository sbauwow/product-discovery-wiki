# Prototyping

> A prototype is a learning artifact, not a product artifact. Its purpose is to answer a question cheaply.

## Prototype types (Cagan's taxonomy)

Different prototypes attack different [risks](cagan-four-risks.md). Pick by what you're trying to learn.

| Type | Risk attacked | Fidelity | Cost | Build time |
|---|---|---|---|---|
| **Feasibility prototype** | Feasibility | Code, real | Med | 1–5 days |
| **User prototype** | Value, Usability | Visual, fake | Low | hours–days |
| **Live-data prototype** | Value | Real backend, fake UI | High | 1–2 weeks |
| **Hybrid / Wizard-of-Oz** | Value | Fake everything | Very low | hours |

### 1. Feasibility prototype

An engineering spike. "Can we build this with our time/tech/data?"
- Real code, ugly, throwaway
- Built by an engineer, not a team
- Output: yes/no + risks + estimate
- Example: "Can we run inference under 200ms on this hardware?" → write the inference loop, measure.

### 2. User prototype

A clickable façade for users to react to. Figma/Framer/HTML.
- No real backend
- Resolution scales with what you're testing:
  - **Low-fi** (paper, wireframes) — concept reactions
  - **Mid-fi** (Figma) — flow, IA, layout
  - **High-fi** (interactive Figma, Framer) — visual polish, micro-interactions

### 3. Live-data prototype

A real, functional product slice — but narrow.
- Real backend, real auth, real data
- One feature, one segment, no marketing
- Used when interviews/clickable prototypes can't capture real-context behavior
- Example: "Will users actually integrate this API?" → ship the API to 5 design partners

### 4. Hybrid / Wizard-of-Oz

Fake the hard parts with humans behind the curtain.
- User sees what looks like an automated product
- A human is doing the work in the back room
- Use when the *automation* is the expensive part but the *experience* is testable
- Example: "Will users trust an AI to draft their emails?" → ship a UI; humans write the drafts; measure usage and satisfaction. If it works, automate later.

## Prototype fidelity vs learning

```
Fidelity
   │
   │   high-fi visual ─── tests aesthetic, polish
   │                  │
   │   functional ────┼─── tests interaction
   │                  │
   │   click-through ─┼─── tests flow
   │                  │
   │   wireframe ─────┴─── tests concept
   │
   └────────────────────────── time/cost
```

**Match fidelity to question.** A wireframe is enough to test "does this concept resonate?" — building a high-fi prototype to answer that is waste.

Higher fidelity bias: users react to **polish**, not the **idea**. A pretty prototype gets pretty feedback. Sometimes you want low fidelity *specifically* to surface concept-level objections.

## Concierge / manual MVP

Adjacent technique. Deliver the service entirely manually before automating.

- **Food on the Table** (early Lean Startup case): founder personally drove to grocery stores and built meal plans for users. Validated demand before any code.
- **Zappos** (Tony Hsieh's origin): photographed shoes at stores, listed online, bought from store when ordered, mailed manually. Tested "will people buy shoes online?" without inventory.

Concierge tells you whether the *job* is real. Automation is a separate question, asked after.

## Pretotyping (Alberto Savoia)

Before prototyping. Test "is this the right *it*" before "build *it* right".

Techniques:
- **Mechanical Turk pretotype** — humans simulate the product
- **Pinocchio pretotype** — non-functional mockup (a wooden phone in your pocket)
- **Fake door** — link to a feature that doesn't exist; measure clicks

## What a prototype is NOT

- A v1 of the product (it's throwaway)
- A spec for engineers (write a spec separately)
- Proof of feasibility for shipping (different from feasibility prototype)
- Guaranteed signal — prototype tests overstate intent; combine with behavioral data where possible

## Common failure modes

- **Prototype too real** — engineers build production code; can't iterate
- **Prototype too pretty** — users give aesthetic feedback when you wanted concept feedback
- **One-shot prototype** — built, tested, done; not iterated on insights
- **Wizard-of-Oz that scales accidentally** — see Magic ($5/yr SMS concierge) which couldn't scale humans

## See also

- [Assumption mapping](assumption-mapping.md) — picks which prototype to build
- [Design Sprint](design-sprint.md) — formalized prototype + test in 5 days
- [Lean Startup](lean-startup.md) — MVP is one kind of prototype
