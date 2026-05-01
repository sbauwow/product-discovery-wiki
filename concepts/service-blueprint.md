# Service Blueprint

> Source: G. Lynn Shostack, "How to Design a Service" (Harvard Business Review, 1984). Mary Jo Bitner extended in academic service design. Visualizes service delivery across what the *user* sees and what the *org* does behind the scenes.

## The structure

```
                            TIME / JOURNEY PHASES →
┌─────────────────────────────────────────────────────────────────┐
│ PHYSICAL EVIDENCE                                               │
│ tangible artifacts user encounters (receipt, app screen, email) │
├─────────────────────────────────────────────────────────────────┤
│ CUSTOMER ACTIONS                                                │
│ what the user does                                              │
├─────────────────────────────────────────────────────────────────┤
│ ════════════════ LINE OF INTERACTION ═══════════════════════    │
├─────────────────────────────────────────────────────────────────┤
│ FRONTSTAGE (visible to user)                                    │
│ employee/system actions user can see (chat agent, app response) │
├─────────────────────────────────────────────────────────────────┤
│ ════════════════ LINE OF VISIBILITY ════════════════════════    │
├─────────────────────────────────────────────────────────────────┤
│ BACKSTAGE                                                       │
│ employee actions user doesn't see (warehouse pick, eng on-call) │
├─────────────────────────────────────────────────────────────────┤
│ ════════════════ LINE OF INTERNAL INTERACTION ══════════════    │
├─────────────────────────────────────────────────────────────────┤
│ SUPPORT PROCESSES                                               │
│ systems and partners (payment processor, fulfillment vendor)    │
└─────────────────────────────────────────────────────────────────┘
```

Five horizontal lanes, separated by three lines:
- **Line of interaction** — where user and org meet
- **Line of visibility** — what user can see vs not
- **Line of internal interaction** — between front-line staff and back-office systems

Time runs left-to-right (the customer journey).

## Worked example: subscription box company

```
PHASE:        Browse        Subscribe       First box        Box arrives    Cancel
─────────────────────────────────────────────────────────────────────────────────
EVIDENCE:     Website       Confirmation    Tracking email   Box, packing   Email
                            email                            slip           confirmation
CUSTOMER:     Search,       Sign up, pay    Wait, track      Open, use      Click cancel
              click product                                                 in account
═══════════════════════════════════════════════════════════════════════════════════
FRONTSTAGE:   Web app       Checkout flow   Order status     —              Cancel flow
              (search, prod) (Stripe)        (Shopify)
═══════════════════════════════════════════════════════════════════════════════════
BACKSTAGE:    Catalog mgmt  Payment recon   Warehouse pick   QC inspection  Retention
                                            & pack                          team review
═══════════════════════════════════════════════════════════════════════════════════
SUPPORT:      Inventory DB  Stripe API      3PL vendor       Carrier (UPS)  CRM, billing
              CMS                           WMS              Tracking API   system
```

A blueprint reveals dependencies the customer never sees but feels: a slow warehouse pick = late box = bad customer experience.

## Why blueprint vs [customer journey map](customer-journey-maps.md)

| Customer Journey Map | Service Blueprint |
|---|---|
| User experience focus | Org delivery focus |
| Emotion, perception | Operations, dependencies |
| What user does/feels | What org does + what user sees |
| Useful for marketing/UX | Useful for ops/process design |
| One layer (user) | Five layers (user + org backbone) |

CJM tells you what users feel. Blueprint tells you why. Blueprints are the artifact when product depends on operations (logistics, support, professional services, regulated industries).

## When to use it

- **Service products** — anything with human delivery (healthcare, hospitality, support)
- **Marketplace operations** — both sides (e.g. Uber: rider + driver + dispatcher + risk team)
- **Multi-team coordination** — when product touches sales, CS, billing, ops, legal
- **Failure analysis** — bad customer outcomes often trace to backstage failures invisible from the CJM
- **Automation candidates** — backstage manual steps map to candidates for tooling

## How to build one

1. **Pick one journey** — one persona, one major job
2. **Get research** — interview customers AND frontline employees AND backstage staff
3. **Map customer actions left-to-right**
4. **For each customer action, list what's frontstage** (visible to them)
5. **Below each frontstage step, list what backstage makes it work**
6. **Below that, the systems/partners involved**
7. **Mark fail points** — places where the chain breaks

Output: a wall-sized artifact (Miro, FigJam, or paper). Like CJMs, it dies if not updated.

## Common failure modes

- **Built without backstage research** — frontstage people don't know what backstage does; the model is wrong
- **Treats blueprint as documentation** — it's a *design* artifact, meant to drive change
- **Too detailed** — every micro-step listed; nobody reads
- **No fail-point analysis** — pretty diagram, no decisions
- **Ignored after creation** — same fate as CJMs

## Connection to discovery

Service blueprints sit alongside [customer journey maps](customer-journey-maps.md):
- CJM surfaces what users feel
- Blueprint surfaces *why* — operational dependencies
- Together: actionable map of where to invest

For SaaS-only products with little ops layer, blueprints add less. For any product with humans-in-the-loop, they're essential.

## See also

- [Customer Journey Maps](concepts/customer-journey-maps.md) — the user-side companion
- [Story mapping](concepts/story-mapping.md) — product-internal companion
- [Opportunity Solution Tree](concepts/opportunity-solution-tree.md) — fail points become opportunities
