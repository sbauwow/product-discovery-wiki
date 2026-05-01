# Heuristic Evaluation

> Source: Jakob Nielsen & Rolf Molich, ~1990. Expert review of an interface against a checklist of usability principles. Cheap, fast, no users required. Catches obvious issues before they reach a [usability test](usability-testing.md).

## The mechanic

```
1. Pick 3-5 evaluators (ideally UX-trained, not the people who designed it)
2. Each evaluator independently reviews the interface
3. Each notes violations of the heuristics, with severity ratings
4. Evaluators meet to consolidate findings
5. Output: prioritized list of issues to fix
```

Why multiple evaluators: a single expert finds ~35% of issues. Three find ~60%. Five find ~75%. Past five = diminishing returns.

The evaluator is *not* the designer. Self-evaluation is too biased.

## Nielsen's 10 heuristics

The canonical checklist. Evaluator looks for violations of each:

### 1. Visibility of system status
> The system should always keep users informed about what's going on.

Examples: loading spinners, progress bars, status messages, save indicators.
Violation: button click → silence; user wonders if anything happened.

### 2. Match between system and the real world
> Speak the users' language, with words familiar to the user.

Examples: "Save" not "Persist", "Folders" not "Directories", "Trash" not "Buffer".
Violation: domain jargon ("commit", "merge") in consumer software.

### 3. User control and freedom
> Users need clearly marked emergency exits.

Examples: Cancel button, Undo, Back navigation, "Are you sure?" before destructive action.
Violation: long flow with no way back; modal with no escape.

### 4. Consistency and standards
> Users should not have to wonder whether different words/actions mean the same thing.

Examples: button styles consistent, terminology consistent across screens.
Violation: "Save" on one screen, "Submit" on the next, "Apply" on the third — for the same action.

### 5. Error prevention
> Eliminate error-prone conditions before they happen.

Examples: confirmation for destructive actions, smart defaults, format hints.
Violation: free-text date input with no format guide → user types "next Tuesday" → error.

### 6. Recognition rather than recall
> Make objects, actions, and options visible.

Examples: dropdowns, autocomplete, recent items.
Violation: requiring users to memorize commands or hidden gestures.

### 7. Flexibility and efficiency of use
> Accelerators (often unseen by novices) speed up expert interaction.

Examples: keyboard shortcuts, bulk actions, saved templates.
Violation: power users forced through novice flows.

### 8. Aesthetic and minimalist design
> Dialogues should not contain irrelevant information.

Examples: progressive disclosure, hide-by-default for advanced settings.
Violation: every setting visible at once; user can't find the important one.

### 9. Help users recognize, diagnose, and recover from errors
> Error messages should be in plain language; precisely indicate the problem; constructively suggest a solution.

Examples: "Email already in use. Try a different one or sign in" not "Error 422: duplicate".
Violation: error codes shown to users; vague "something went wrong".

### 10. Help and documentation
> If documentation is needed, make it easy to search and focused on the user's task.

Examples: contextual help, in-product tooltips, searchable docs.
Violation: no help; or help that requires reading 30 pages before the user can do anything.

## Severity ratings

Nielsen suggests rating each issue:

| Rating | Meaning | Action |
|---|---|---|
| **0** | Not a usability problem | Ignore |
| **1** | Cosmetic — fix only if extra time | Backlog |
| **2** | Minor problem — low priority | Plan to fix |
| **3** | Major problem — high priority | Fix in current cycle |
| **4** | Catastrophe — must fix | Block ship |

A heuristic-evaluation report ranks all violations by severity, giving the team a prioritized fix list.

## Strengths

- **Cheap** — no users to recruit; 3-5 evaluators × ~3 hours each
- **Fast** — output in 1-2 days
- **Catches obvious bugs** — surface-level UX failures that don't need user testing
- **Pre-test cleanup** — clean up the easy stuff before paying for usability testing
- **Standard checklist** — Nielsen's 10 are well-known; consistent vocabulary

## Weaknesses

- **No real users** — expert opinion ≠ user behavior; experts predict <50% of real-user issues
- **False positives** — experts flag things real users wouldn't notice
- **Misses task-specific problems** — heuristics are generic; domain-specific issues invisible to outsiders
- **Doesn't surface motivation issues** — heuristics test usability, not desirability
- **Not a substitute for user testing** — only a *supplement*

## When to run heuristic evaluation

✅ Pre-launch sanity check before paying for [usability testing](usability-testing.md)
✅ Quick triage of an inherited product
✅ Acceptance review before handoff to engineering
✅ Internal tools (where users are stuck with what you build, so basic UX failures are unforgiveable)
✅ When you can't recruit users (regulated industries, specialized domains)

## When not

❌ As a substitute for user testing — different method, different signal
❌ For early-concept work — no UI to evaluate yet
❌ For motivation/value questions — heuristics don't address these

## Cousin: cognitive walkthrough

Adjacent expert-review method. Evaluator role-plays a *specific user task*:

```
1. Define a target task
2. Define a user profile
3. Walk through each step from that user's POV:
   - "Will the user know what action to take?"
   - "Will the user notice the right control?"
   - "Will the user understand the feedback?"
4. Note where the user *would* fail
```

Cognitive walkthrough is task-specific where heuristic eval is general. Pair them: heuristic eval finds general issues; cognitive walkthrough finds task-flow issues.

## Heuristic eval in the research stack

```
EARLIEST                                                    LATEST

Sketches / wireframes
   ↓
Heuristic evaluation                  ← cheap expert review
   ↓
Prototypes
   ↓
[Five-second test](five-second-test.md)
   ↓
[Usability testing](usability-testing.md)
   ↓
Real product
   ↓
[A/B testing](ab-testing.md)          ← scale validation
```

Each method catches different issues. Skipping heuristic eval means usability tests catch issues that should have been obvious — wasting expensive panel time on bugs.

## Worked example

A team is preparing to ship a new settings page. Heuristic evaluation by 3 evaluators surfaces:

| Issue | Heuristic | Severity |
|---|---|---|
| No save indicator after edit | #1 Visibility of system status | 3 (major) |
| "Persist" used instead of "Save" | #2 Match real world | 2 (minor) |
| No undo for delete | #3 User control | 4 (catastrophe) |
| "Submit" + "Apply" + "Save" on different tabs | #4 Consistency | 3 (major) |
| Error: "Validation failed (E0042)" | #9 Error recovery | 4 (catastrophe) |
| Help link goes to 50-page doc | #10 Help & docs | 2 (minor) |

Two catastrophic issues caught before any user saw the product. The team fixes those, runs usability testing on the cleaned-up version, and finds *task-specific* issues — not the heuristic-level ones already gone.

## Common failure modes

- **Single evaluator** — finds <40% of issues; use 3+
- **Designer evaluating own work** — biased; bring in fresh eyes
- **Mechanical checklist** — going down the 10 in order without engaging with the actual UI
- **No severity ratings** — issue list with no priority is unactionable
- **Treating heuristics as rules** — they're guidelines; sometimes good design violates them deliberately
- **Skipping consolidation** — evaluators report independently but don't meet to align; duplicates and disagreements stay
- **Using heuristic eval as substitute for users** — cheap quick = "we don't need real testing" — wrong

## See also

- [Usability testing](concepts/usability-testing.md) — the user-based method this complements
- [Five-second test](concepts/five-second-test.md) — adjacent first-impression test
- [Cynefin](concepts/cynefin.md) — heuristic eval treats UX as Complicated (expert-knowable), which is mostly true for surface UX
