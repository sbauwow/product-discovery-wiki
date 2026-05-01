# Customer Journey Maps

> A visualization of the user's end-to-end experience across all touchpoints, including emotional state, pain points, and opportunities. Distinct from [story maps](story-mapping.md), which are product-internal.

## The structure

```
PHASES        Awareness    Consideration    Onboarding    Daily use    Renewal
              ─────────────────────────────────────────────────────────────────
                                                                    
DOING         Sees ad      Compares         Signs up,     Uses core   Gets
              Hears        3 tools          configures    feature     renewal
              from peer    Reads docs                     daily       email

THINKING      "Is this     "Is it           "How do I     "This       "Worth
              for me?"     better?"          start?"      saves time" the cost?"

FEELING       😐 curious   🤔 uncertain     😤 lost      😊 happy    😠 anxious
              
TOUCHPOINTS   Twitter      Website          Onboarding    App         Email
              Podcast      Sales call       Email seq     Slack int.  Billing
              
PAIN POINTS               No pricing       Complex       —           Hidden
                          on landing       integration                price hike

OPPORTUNITIES Self-serve   Free trial       Better        —           Proactive
              calculator   on landing       wizard                    value email
```

Rows: dimensions of experience. Columns: phases over time. Each cell: what's happening for the user.

## Why it differs from [story mapping](story-mapping.md)

| Customer Journey Map | Story Map |
|---|---|
| All channels & touchpoints | Inside the product only |
| Pre-purchase + post-purchase | Mid-product use |
| Includes emotion, sentiment | Functional steps only |
| Cross-org artifact (sales, marketing, product, support) | Product-team artifact |
| Used to spot org-wide gaps | Used to slice MVP / releases |

A CJM might show: "user gets renewal email → confused by pricing → calls support → support refuses discount → user churns." That's a sales/billing/CS issue, not a product feature gap. Story map can't show this.

## When to build one

- **Cross-functional alignment** — getting marketing, product, support, sales on the same page about the experience
- **Identifying off-product friction** — pain points that aren't UI/UX but are still product problems
- **Onboarding for new team members** — vivid summary of how users actually live
- **Service design** — services with heavy human-touch components

## Phases (typical)

Customer journeys often follow:

1. **Awareness** — first encounter
2. **Consideration** — evaluating options
3. **Decision / Purchase** — committing
4. **Onboarding** — first use
5. **Adoption** — habitual use
6. **Retention / Renewal** — staying
7. **Advocacy** — referring others

Adjust phases for your business. A marketplace has separate journeys for buyers and sellers.

## Building one

1. **Pick one persona/segment** — different journeys for different users; don't mix
2. **Get research data** — interviews, support tickets, NPS comments, session recordings
3. **Map the timeline** — what they do, when
4. **Add emotion** — happy/anxious/frustrated at each phase
5. **List touchpoints** — every interaction with you (ads, app, support, email)
6. **Mark pain points** — friction, drop-off, confusion
7. **Note opportunities** — where intervention could move the journey

Tools: Miro, FigJam, Mural, or paper. Keep it visible — a CJM hidden in a Confluence page never gets used.

## Service blueprint (extension)

A **service blueprint** adds a layer below the CJM showing what your *organization* does behind the scenes:

```
USER    visible actions (the CJM above)
─────────────────────────────────────────
        line of visibility
─────────────────────────────────────────
ORG     front-stage employees
        back-stage processes
        supporting systems
```

Blueprint = CJM + ops layer. Useful when product depends on humans (CS, sales, professional services).

## Common failure modes

- **Built once, ignored** — CJMs decay if not part of regular team practice
- **No research basis** — invented in a conference room
- **Too detailed** — every micro-step listed, hard to scan
- **Not enough emotion** — just functional steps; loses the why
- **Mixes personas** — one CJM should be one journey; multi-persona maps confuse
- **Owned by no one** — CJM that crosses orgs needs a clear champion

## See also

- [Story mapping](story-mapping.md) — product-internal cousin
- [Personas](personas.md) — the unit of measurement for a CJM
- [Jobs To Be Done](jobs-to-be-done.md) — JTBD switch interviews surface CJM phases
- [User interviews](user-interviews.md) — primary input
