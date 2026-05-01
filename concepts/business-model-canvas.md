# Business Model Canvas (BMC)

> Source: Alexander Osterwalder & Yves Pigneur, *Business Model Generation* (2010). One-page strategic visualization of a complete business model. The most-used strategic doc after the OKR.

## The 9 blocks

```
┌──────────────┬────────────┬─────────────┬─────────────┬──────────────┐
│              │            │             │             │              │
│   KEY        │   KEY       │   VALUE      │  CUSTOMER    │  CUSTOMER    │
│ PARTNERS     │ ACTIVITIES  │ PROPOSITIONS │RELATIONSHIPS│   SEGMENTS   │
│              │            │             │             │              │
│ who helps    │ what we do  │ what we     │ how we      │ who we       │
│ us deliver   │            │ promise     │ engage      │ serve        │
│              ├────────────┤             ├─────────────┤              │
│              │            │             │             │              │
│              │   KEY       │             │  CHANNELS    │              │
│              │ RESOURCES   │             │             │              │
│              │            │             │ how we      │              │
│              │ what we     │             │ reach them  │              │
│              │ have/use    │             │             │              │
├──────────────┴────────────┴─────────────┴─────────────┴──────────────┤
│                                                                     │
│       COST STRUCTURE                  REVENUE STREAMS                │
│       what costs                      what we earn from              │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
                  LEFT = EFFICIENCY      RIGHT = VALUE
```

Three sections, mapped to business logic:
- **Right side** — value to customer (segments, value props, channels, relationships, revenue)
- **Left side** — operations (partners, activities, resources, costs)
- **Center** — value propositions (what links the two sides)

## The 9 blocks in detail

### 1. Customer Segments
Who specifically? Mass market, niche, segmented, multi-sided platform, etc. Differentiate by what they need, not demographics.

### 2. Value Propositions
What value do we deliver to each segment? See [Value Proposition Canvas](value-proposition-canvas.md) for deeper decomposition. Often: solving a pain, creating a gain, enabling a job.

### 3. Channels
How do we reach customers? Direct (sales force, website) vs partner (retail, distributors). Awareness → evaluation → purchase → delivery → after-sales — channels can specialize per stage.

### 4. Customer Relationships
Type of relationship per segment: personal assistance, self-service, automated services, communities, co-creation. Different segments often want different relationships.

### 5. Revenue Streams
How do we monetize? Asset sale, usage fee, subscription, lending/leasing, licensing, brokerage, advertising. Pricing mechanism: fixed, dynamic, market-based, auction.

### 6. Key Resources
Physical (warehouses, equipment), intellectual (brand, patents, data), human (talent), financial (cash, credit). What's structurally required.

### 7. Key Activities
Production, problem-solving (consultancies), or platform/network (marketplaces). What we *do* every day.

### 8. Key Partners
Strategic alliances, joint ventures, supplier-buyer relationships. *Why* partner: optimization/economies, risk reduction, resource acquisition.

### 9. Cost Structure
Fixed vs variable, economies of scale vs scope. Cost-driven (low-cost airlines) vs value-driven (luxury hotels).

## Why one page

The BMC's leverage is the **forced compression**. A 50-page business plan hides incoherence; a one-page canvas exposes it. If you can't articulate revenue streams in a paragraph, you don't yet know your model.

## Filling order (Osterwalder's prescription)

```
1. Customer Segments    (right edge)
2. Value Propositions   (center, paired with segments)
3. Channels             (right side)
4. Customer Relationships (right side)
5. Revenue Streams      (bottom right)
6. Key Resources        (left side, derived)
7. Key Activities       (left side, derived)
8. Key Partners         (left side, derived)
9. Cost Structure       (bottom left, last)
```

Right side first (customer-derived), then left side (operations-derived). Cost structure last because it falls out of the rest.

## BMC as a living artifact

The canvas is meant to be iterated. As the business validates assumptions:
- Customer segment narrows or shifts
- Value prop sharpens
- Channels prove or fail
- Revenue streams discovered
- Costs become known

Every quarter, the BMC should look at least slightly different. If it's identical to last quarter, the org is either fully validated (rare) or not learning (common).

## BMC vs [Lean Canvas](lean-canvas.md)

Ash Maurya adapted the BMC for startups:

| BMC (Osterwalder) | Lean Canvas (Maurya) |
|---|---|
| Key Partners | Problem |
| Key Activities | Solution |
| Key Resources | Key Metrics |
| Customer Relationships | Unfair Advantage |
| Same: VP, Channels, Segments, Revenue, Cost | Same |

BMC = established business. Lean Canvas = early-stage startup. See [Lean Canvas](lean-canvas.md).

## When to use BMC

- **Early-stage strategic alignment** — founder team aligning on the model
- **Investor pitches** — many VCs ask to see the BMC
- **Strategic shifts** — repositioning, new segments, new channels
- **Cross-functional onboarding** — quick way to give a new exec the whole picture

## When less useful

- **Pure tactical decisions** — overkill for "should we add feature X"
- **Already-defined businesses** — if all blocks are settled and stable, BMC is documentation, not strategy
- **Multi-product companies** — one canvas per product/business unit, not one company-wide

## Common failure modes

- **Treated as a one-time fill** — built in a workshop, never updated
- **Filled with wishful thinking** — "Customer Segment: everyone" (segment of one = no segment)
- **Skipping the why** — boxes filled but not understood; team can't defend the choices
- **Single canvas for multi-sided business** — marketplaces need separate canvases per side

## See also

- [Lean Canvas](concepts/lean-canvas.md) — startup-focused variant
- [Value Proposition Canvas](concepts/value-proposition-canvas.md) — drills into the VP block
- [Wardley Mapping](concepts/wardley-mapping.md) — strategic positioning above the canvas
- [Customer Development](concepts/customer-development.md) — the validation loop the canvas feeds
