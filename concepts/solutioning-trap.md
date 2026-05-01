# The Solutioning Trap

> The most common interview and discovery failure. Asking users (or yourself) about solutions before understanding the problem.

## The pattern

User says: "I wish you had a button that did X."

Bad PM response: "Got it, we'll add a button."
Good PM response: "Tell me about the last time you wanted to do X. Walk me through what you tried."

The user's stated solution is almost never the right solution. It's a *symptom*, pointing to an underlying problem. The PM's job is to follow it back.

## Why solutioning is so seductive

- **It feels productive** — "we got 5 feature requests this week"
- **It's concrete** — easier to write down than a fuzzy job-to-be-done
- **It validates the user** — "we're listening"
- **It avoids hard thinking** — building something is easier than understanding why
- **It generates a backlog** — visible work product

## Forms it takes

### 1. Asking users what to build

> "What features would you like to see?"
> "Would you use a feature that does X?"

Users answer with reference to **products they've seen**, not problems they have. You'll get a wishlist of features cargo-culted from competitors.

### 2. Roadmap-by-request

Customer requests → backlog → ship the loudest. Skips the question of whether the request is the right solution. See [feature factory](feature-factory.md).

### 3. Solution-first interviews

> "We're thinking about building X. What do you think?"

User now anchors on X. Won't volunteer better problems. Worse, social pressure pushes them toward "yeah, sounds great" — useless data. See [user interviews](user-interviews.md).

### 4. Self-solutioning

PM has an idea, runs interviews to confirm it. Selectively hears confirmation. Calls it "validated." Builds it. Fails. This is confirmation bias dressed in discovery language.

### 5. JIRA-shaped thinking

The team thinks in tickets, sprints, features. There's no room in the workflow for "we don't know yet." Every meeting needs a deliverable, so problems get solutioned to fill the slot.

## The Henry Ford quote

> "If I had asked people what they wanted, they would have said faster horses."

Probably apocryphal but the spirit holds: users describe solutions inside their current paradigm. Their *job* (get from A to B faster) is real. Their *solution* (faster horse) is local-optimum thinking. The product team's job is to surface the job and consider all solutions, not just the user-named one.

## How to escape solutioning

### In interviews:

When user mentions a solution:

| User says | You ask |
|---|---|
| "Add a button for X" | "Walk me through the last time you wanted to do X." |
| "I want feature Y" | "What problem would feature Y solve?" |
| "Why don't you have Z?" | "What were you trying to do when you noticed Z was missing?" |

The pattern: **trace any stated solution back to the underlying job/problem**.

### In planning:

When stakeholder demands a solution:

> Stakeholder: "Build feature X."
> PM: "What problem does X solve? For whom? How will we know it worked?"

If the answers are vague → the request hasn't been thought through; PM should run discovery, not build.
If the answers are sharp → still verify with users; even sharp asks miss things.

### In your own thinking:

When you have a "great idea":

1. What problem is this solving?
2. Whose problem?
3. How do they currently solve it?
4. Why is the current solution insufficient?
5. What evidence do I have for any of this?

If you can't answer 1–4 cleanly, you have a solution looking for a problem.

## When user-stated solutions are useful

Not always wrong. Useful as:
- **Signal of an underlying problem** — multiple users asking for "X" suggests a real pain
- **Vocabulary** — how users describe things informs naming
- **Mental-model check** — what they expect tells you their model

The error is treating their stated solution as the *answer*, not as the *clue*.

## Adjacent failures

- **Premature OST solutions** — building solutions on the [tree](opportunity-solution-tree.md) before opportunities are validated
- **Skipping opportunities entirely** — outcome → solution, no user need in between
- **Single-solution branches** — picking one solution per opportunity, no real comparison

## See also

- [User interviews](user-interviews.md) — past-behavior probing as the antidote
- [Jobs To Be Done](jobs-to-be-done.md) — separates jobs (stable) from solutions (volatile)
- [Opportunity Solution Tree](opportunity-solution-tree.md) — enforces opportunity → solution → experiment ordering
