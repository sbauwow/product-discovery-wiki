# Customer Development

> Source: Steve Blank, *The Four Steps to the Epiphany* (2005), *The Startup Owner's Manual* (2012). The intellectual predecessor to [Lean Startup](lean-startup.md). Eric Ries was Blank's student.

## The thesis

> "There are no facts inside the building. Get out of the building."

Engineers and PMs build products in conference rooms based on speculation about users. Customer Development is the structured discipline of replacing speculation with field-tested evidence.

## The four phases

```
   Customer Discovery       Customer Validation
   ──────────────           ─────────────────
   Understand the problem   Find paying customers
   Verify the problem real  Verify the solution sells
            ↓                        ↓
   ────────────────  pivot back if needed  ─────────────────
            ↓                        ↓
   Customer Creation        Company Building
   ────────────────         ──────────────
   Scale demand             Scale the org
```

Phases 1–2 are search (still figuring out the business). Phases 3–4 are execution (scaling a known business).

The dangerous error Blank diagnosed: orgs treat phase 1 work as if they're already in phase 4. They scale (build, hire, market) before they've found product/market fit.

## Customer Discovery

Goal: validate that the **problem** is real and the **customer** is who you think.

Activities:
- Define hypotheses about customer + problem
- Get out of the building — interview prospective customers
- Verify their problem matches your hypothesis
- Pivot the hypothesis if not

Output: a problem statement grounded in real-customer evidence, not founder intuition.

## Customer Validation

Goal: validate that customers will **buy** your **solution**.

Activities:
- Build minimum sellable product
- Sell it (literally) to early customers
- Build a repeatable sales playbook
- Verify unit economics work

Output: proof that the business can sell the solution, not just that customers like the idea.

This is where most "validated" startups die. Customers will *say* they'd buy. They often won't *actually* buy. Sales-with-money is the only real test.

## Customer Creation

Goal: scale demand. Now that you have product/market fit, create the market category, run marketing, scale sales.

## Company Building

Goal: scale the org. Move from a flat search team to a real company structure.

## Why phases ≠ stages of agile sprints

Customer Development is **non-linear**. The expected behavior is to pivot between phases — find a problem in Validation → return to Discovery to refine. The discipline is recognizing *which phase you're in*, not progressing linearly.

## The pivot, defined

Blank's original term (Ries popularized it): a substantive change in the business model based on validated learning. NOT:
- Changing tactics
- Tweaking features
- Renaming the product

Real pivot examples:
- **Customer pivot** — same product, different segment ("we built for SMBs but enterprises bought it")
- **Problem pivot** — same customer, different problem ("they didn't want analytics, they wanted alerts")
- **Solution pivot** — same problem, different solution ("they wanted alerts, not via dashboard, via SMS")
- **Channel pivot** — same product, different distribution ("inside sales not self-serve")

## Customer Development vs Lean Startup

| Customer Development (Blank) | Lean Startup (Ries) |
|---|---|
| Search vs Execution | Build-Measure-Learn |
| 4-phase model | Single iteration loop |
| Sales-flavored | Product-flavored |
| Strong in B2B / enterprise | Strong in consumer / SaaS |
| Pre-product framing | Product-iteration framing |
| Founder-led search team | Cross-functional team |

Same intellectual lineage. Different emphases. Most modern product orgs use Lean Startup vocabulary; the Customer Development *frame* (search vs execution) remains useful for diagnosing what mode the org is in.

## Common failure modes

- **Skipping discovery** — "we already know the problem" → wrong. Always validate.
- **Confirmation interviews** — pitching the solution and asking "would you buy?" — see [solutioning trap](solutioning-trap.md)
- **Premature scaling** — hiring sales before validation; spending on marketing before product/market fit
- **Wrong phase, wrong activities** — building features in phase 1 (when the problem isn't validated) or running discovery in phase 3 (when scale is the issue)

## When CD is most useful

- **Founder-led startups** — original use case
- **B2B / enterprise** — sales-cycle realities the framework was built for
- **New category creation** — when there's no playbook to copy
- **Pivoting** — recognizing you're back in search mode

## When less useful

- **Established products with known PMF** — phases 3–4 territory; CD frame less relevant
- **Pure consumer apps with cheap acquisition** — Lean Startup loop fits better
- **Internal tools** — no "customers" in the buying sense

## See also

- [Lean Startup](lean-startup.md) — the popularized successor
- [Value Proposition Canvas](value-proposition-canvas.md) — the artifact that captures discovery output
- [User interviews](user-interviews.md) — the core CD activity
- [Solutioning trap](solutioning-trap.md) — the most common CD interview failure
