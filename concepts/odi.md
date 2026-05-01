# Outcome-Driven Innovation (ODI)

> Source: Tony Ulwick, *What Customers Want* (2005), *Jobs To Be Done: Theory to Practice* (2016). Strategyn methodology. The **quantitative** cousin to Christensen-style [JTBD](jobs-to-be-done.md).

## The thesis

> Customers can't tell you what to build, but they *can* tell you which **outcomes** matter and how well existing solutions deliver them.

ODI takes the JTBD frame ("customers hire products to do jobs") and operationalizes it through structured customer surveys. Replaces interview narratives with statistical rigor.

## The five steps

```
1. Identify the JOB the customer is trying to do
       ↓
2. Decompose the job into 50-150 DESIRED OUTCOMES
       ↓
3. Survey customers: rate each outcome on
   IMPORTANCE and SATISFACTION
       ↓
4. Calculate OPPORTUNITY SCORE per outcome:
   Opportunity = Importance + max(Importance - Satisfaction, 0)
       ↓
5. Target the highest-opportunity outcomes (underserved)
```

## Step 1: The job

Same as Christensen JTBD. A *core functional job* + emotional/social aspects. Stated solution-agnostic.

Example: "Translate written content from one language to another" (job for a translation product).

## Step 2: Desired outcomes

The crucial differentiator. Each job decomposes into ~50–150 outcomes — measurable steps along the way to job completion. Format:

> [Direction of improvement] + [unit of measure] + [object of control] + [contextual clarifier]

Examples for "translate written content":
- "Minimize the **time** it takes to detect the source language"
- "Minimize the **likelihood** of mistranslating idioms"
- "Maximize the **accuracy** of translated technical jargon"
- "Minimize the **effort** required to verify translation quality"

Notice: no products, no features, no brands. Pure outcome statements.

## Step 3: Importance × Satisfaction survey

Survey 200+ customers. For each outcome, ask:
- **Importance**: How important is this outcome to you? (1–10)
- **Satisfaction**: How satisfied are you with current solutions on this outcome? (1–10)

This produces, for every outcome, two numbers from real customers.

## Step 4: The opportunity score

```
Opportunity = Importance + max(Importance - Satisfaction, 0)
```

Interpretation:
- **High importance + low satisfaction** = underserved → big opportunity
- **High importance + high satisfaction** = served → no opportunity
- **Low importance** = no opportunity regardless of satisfaction
- **Low importance + low satisfaction** = nobody cares; don't bother

```
                       SATISFACTION
                  Low              High
              ┌─────────────┬─────────────┐
   IMPORTANCE │             │             │
       Low    │  IGNORE     │   IGNORE    │
              │             │             │
              ├─────────────┼─────────────┤
       High   │  TARGET ★   │   SERVED    │
              │ (underserved)│  (no opp.) │
              └─────────────┴─────────────┘
```

## Step 5: Target the underserved

Solutions get developed for the high-opportunity outcomes. Other outcomes are deprioritized.

Critically: solutions are **outcome-targeted**, not feature-driven. "Reduce the time to detect source language by 50%" → could be solved by AI auto-detection, by user toggle defaults, by integration with browser language settings, etc. ODI tells you *which outcome to attack*; solution discovery follows.

## Worked example: financial planning software

Top opportunities (post-survey):

| Outcome | Imp | Sat | Opp | Action |
|---|---|---|---|---|
| Minimize time to forecast cash flow 90 days out | 9.2 | 4.1 | 14.3 | **Target** — underserved |
| Minimize likelihood of missing tax deadlines | 9.5 | 8.7 | 10.3 | Don't bother — already served |
| Maximize confidence in retirement projections | 9.0 | 5.8 | 12.2 | **Target** |
| Minimize effort to share plans with accountant | 6.0 | 7.0 | 6.0 | Skip — low importance |
| Maximize ability to model "what-if" scenarios | 8.8 | 4.5 | 13.1 | **Target** |

Engineering investment goes into cash-flow forecasting, retirement projection confidence, and what-if modeling. *Not* tax deadline reminders (already solved by current tools).

## ODI vs Christensen JTBD

| Christensen JTBD | Ulwick ODI |
|---|---|
| Narrative ("hire a milkshake") | Quantitative ("opportunity = X") |
| Switch interviews | 200+ surveys |
| Qualitative insight | Statistical ranking |
| Few jobs deeply explored | All outcomes systematically |
| Strategic framing | Operational research |
| Lighter to apply | Heavier; needs research budget |

Both are valid. Most teams use the Christensen frame because it's accessible. Big-budget product teams (Strategyn's clients are often Fortune 500) use ODI for rigor.

## Strengths

- **Unbiased prioritization** — opportunity scores are derived, not negotiated
- **Solution-agnostic** — outcomes survive any technology shift
- **Long shelf life** — outcome lists are stable for years; only satisfaction scores update
- **Customer-validated** — every outcome was real to >n customers in your survey

## Weaknesses

- **Heavy upfront** — 50-150 outcomes + 200-survey is weeks of work
- **Misses emerging jobs** — surveys target current users; future users don't appear
- **Stated > revealed** — survey responses still differ from actual behavior
- **Best for established products** — early-stage startups can't field a 200-customer survey on a job they're inventing

## When to use ODI

- ✅ Mature products with large customer base
- ✅ Major feature/portfolio decisions ("which gap matters most?")
- ✅ Adjacent-market entry (which outcomes does the new market care about?)
- ✅ Product-line rationalization (which existing features serve which outcomes?)

## When not to

- ❌ Pre-PMF startups (use [Mom Test](mom-test.md) interviews)
- ❌ Tactical feature decisions
- ❌ Markets where the customer base is too small for statistical surveys

## See also

- [Jobs To Be Done](concepts/jobs-to-be-done.md) — the qualitative cousin
- [Opportunity Solution Tree](concepts/opportunity-solution-tree.md) — opportunity scores feed OST opportunity prioritization
- [Value Proposition Canvas](concepts/value-proposition-canvas.md) — Osterwalder's lighter alternative
- [Kano model](concepts/kano-model.md) — adjacent feature-categorization
