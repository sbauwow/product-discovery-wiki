# The Mom Test

> Source: Rob Fitzpatrick, *The Mom Test* (2013, ~120 pages). The most concentrated guide to user interviews. Title = "Ask questions that even your mom can't lie to you about."

## The premise

Everyone, including your mom, lies about products. Not maliciously — politely. Asked "would you buy my idea?" a friend, family member, or random user will say nice things to spare your feelings. The data is poisoned.

Fitzpatrick's three rules transform the conversation so the lying-by-politeness can't happen:

## The three rules

### Rule 1: Talk about *their life*, not your idea

❌ "I'm building an app that does X. What do you think?"
✅ "Tell me about the last time you dealt with [problem area]."

The moment you mention your idea, the user shifts from informant to evaluator. Their job is no longer to give you data; it's to make you feel okay about your idea.

### Rule 2: Ask about *specifics in the past*, not generics or hypotheticals about the future

❌ "Would you use a feature that did X?"
✅ "What did you do the last time you needed to do X?"

❌ "Do you usually waste time on Y?"
✅ "Walk me through your last week — when did Y come up?"

The future is unknown to the user. Generics ("usually", "typically") are abstractions they fabricate on the spot. Past specific behavior is the only honest data.

### Rule 3: Talk less, listen more

PMs talk too much in interviews. The pitch is irresistible. Resist. The interview is for *learning*, not for selling.

Practical tactics:
- Ask the question, then **stop**
- Count to 3 in silence after the user's answer
- Resist following up your own question with another version of it
- Take notes (or have a co-attendee take them) — gives you a reason not to talk

## The "compliments" trap

When users compliment your idea, **discard the compliment**:

> "That's a really cool idea. I'd totally use that."

This is meaningless. Could mean:
- "I'm being polite."
- "I find it intellectually interesting (but won't pay)."
- "I can imagine someone using it."
- "I want this conversation to end."

What's not meaningless: actions, money, time committed.

```
Compliments → noise (discard)
Verbal commitments → weak signal ("would you mind doing a demo next Tuesday?")
Money / time committed → strong signal (pre-orders, signed LOIs)
```

## What good answers sound like

**Good (actionable):**
- "Yeah, last Tuesday I spent 3 hours doing X by hand. Here's how it went..."
- "We tried product Z but switched because of Y."
- "I'd pay $200/mo for that, want me to introduce you to my CFO who'd sign off?"
- "I don't have that problem at all. Sorry."

**Bad (compliments):**
- "I love this! Such a smart idea."
- "I'd totally use it!"
- "You should add a feature for X."

The first set: data. The second set: politeness.

## Customer commitments

Fitzpatrick's most useful idea after the three rules: **commitments and currencies**.

Currency = anything of value the customer can give you. Time, money, reputation, social capital.

A real interview ends with a **commitment ask**:

| Currency | Weak commitment | Strong commitment |
|---|---|---|
| Time | "I'd love to see it" | "Send me a calendar invite for Tuesday" |
| Reputation | "I know other people with this problem" | "Let me intro you to 3 of them this week" |
| Money | "I'd pay for that" | "Send me a contract; I'll sign by Friday" |

If the user won't give *any* currency, the interest is theoretical. Treat the data as such.

## Bad-data-recovery techniques

Sometimes you've already broken the rules. Fitzpatrick's recovery moves:

- **Anchor in past behavior**: "What did you actually do last time?"
- **Probe for cost**: "How much time did that take?" "How much have you spent trying to fix this?"
- **Search for workarounds**: "What are you doing to deal with this today?" (a duct-tape solution = real problem)
- **Probe for concrete examples**: "Tell me about the most recent example."

If they have no past examples, no workarounds, no time/money spent — the problem isn't real for them.

## How this fits with [user interviews](user-interviews.md)

The Mom Test is a more concentrated version of the [user interview](user-interviews.md) discipline. Same principles, more rigorous formulation.

| User interviews (general) | Mom Test (specific) |
|---|---|
| Past-behavior probing | Same, but with concrete language rules |
| Avoid leading questions | Same, plus "no mentioning your idea" |
| Listen more than talk | Same, with explicit silence techniques |
| — | Add: customer commitment ask |

A team that's read *The Mom Test* runs better interviews than one that hasn't. It's the rare 2-hour read with outsized impact.

## Common failure modes

- **Pitching anyway** — "I'll just describe my idea briefly..." (no, you won't briefly)
- **Mistaking compliments for validation** — celebrating "I love it!" responses
- **Skipping the commitment ask** — interview ends with a smile, no follow-up commitment
- **Self-selecting only friendly users** — everyone's polite; no real signal
- **Not asking about cost** — without time/money currently spent, no real problem

## See also

- [User interviews](concepts/user-interviews.md) — the broader practice
- [Solutioning trap](concepts/solutioning-trap.md) — what happens when you break Rule 1
- [Customer Development](concepts/customer-development.md) — Blank's framework that Fitzpatrick operationalizes
- [Continuous Discovery](concepts/continuous-discovery.md) — the cadence that requires Mom-Test-quality interviews
