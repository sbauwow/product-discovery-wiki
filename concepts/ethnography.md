# Ethnography & Contextual Inquiry

> Sources: Anthropology (ethnography itself, ~1900s); Hugh Beyer & Karen Holtzblatt's *Contextual Design* (1998) for the productized version. Field observation of users in their natural environment. Captures what [interviews](user-interviews.md) cannot.

## Why field observation matters

Interviews ask users to *report* behavior. Reports are filtered, abstracted, edited. Ethnography *observes* behavior directly. The two often disagree:

```
INTERVIEW (what user said):
"I check the dashboard every morning."

OBSERVATION (what actually happened over a week):
- Day 1: opened dashboard, glanced 12 seconds, closed
- Day 2: didn't open
- Day 3: opened, but only because manager linked it in Slack
- Day 4: opened, exported a CSV, then worked in the CSV
- Day 5: didn't open
```

The user *believes* they check it daily. They check it twice a week, mostly under prompt, and the actual work happens in the CSV they exported. Wildly different product implications.

## Contextual Inquiry (the operationalized version)

Beyer & Holtzblatt's framing turned anthropological ethnography into a product-research method. Four key principles:

### 1. Context
The research happens in the user's actual environment — their office, their kitchen, their car — not in your lab or on Zoom. Context reveals constraints invisible elsewhere (interruptions, paper notes, cluttered desk, slow wifi).

### 2. Partnership (master/apprentice model)
The researcher is the **apprentice**; the user is the **master**. Researcher asks "show me how you do this" and watches. The user explains as they go. Reverses the usual interview dynamic.

### 3. Interpretation
Researcher and user together interpret what's happening. Hypotheses are surfaced and confirmed/disconfirmed in real time:
> "It looks like you're avoiding the new dashboard because the export is broken. Is that right?"
> "Yeah, exactly. I exported once, it crashed, now I just go straight to the old one."

### 4. Focus
The session has a defined research focus. Not "let's hang out" — "we're studying how you handle expense reports during month-end close."

## Session structure

```
0-15  min  Establish rapport, explain the master/apprentice model
15-90 min  User does their actual work; researcher observes and asks
90-105 min Wrap-up; share interpretations; user confirms/corrects
```

Length: 60-120 minutes. Longer than an interview because work cycles take time. Run 5-10 sessions; saturation usually appears around session 6-8.

## What you're looking for

| Signal | What it tells you |
|---|---|
| **Workarounds** | The product fails to do something users need; they kludge around it |
| **Tool-switching** | Where they leave your product to do part of the job (Excel, paper, Slack, email) |
| **Interruptions** | Context-switching reality vs your "ideal user" assumption |
| **Notes on paper / sticky notes** | Information your product should hold but doesn't |
| **Unwritten rules** | "We always copy the manager on these" — invisible until observed |
| **Failure recovery** | What happens when something goes wrong; reveals trust level |
| **Time allocation** | Where the actual minutes go vs where the user *thinks* they go |

The most-actionable insights are usually **workarounds**. A workaround = an unmet need + a kludge. Both are interesting.

## Worked example: B2B expense reporting

In-person observation of a finance manager during month-end close.

What you'd never get from an interview:
- They print PDFs of every receipt because they don't trust the OCR
- They keep a parallel Excel spreadsheet because the in-product report can't filter by sub-account
- They get interrupted by Slack ~6 times in 30 minutes; each interruption costs ~3 min to recover
- They have a sticky note next to their monitor with the codes they always forget
- The "approved" button on your product crashes if the file size > 10MB; they've learned to split files

Product implications surface immediately:
- OCR confidence indicator (or human-review fallback)
- Sub-account filter
- Save state across interruptions
- Glossary in-product (no more sticky notes)
- File-size handling fix (table stakes)

None of this comes from interviews. The user wouldn't think to mention any of it.

## Ethnography vs contextual inquiry vs usability testing

| Method | Setting | Researcher role | What it captures |
|---|---|---|---|
| Ethnography | User's environment | Silent observer | Cultural patterns, unspoken rules |
| Contextual inquiry | User's environment | Active "apprentice" | How a specific job actually gets done |
| [Usability testing](usability-testing.md) | Lab / Zoom | Task-giver | Where the product breaks |
| [User interview](user-interviews.md) | Anywhere | Conversationalist | What user reports thinking/doing |

Ethnography is most informative; most expensive. Reserve for high-stakes research where stated behavior is suspect.

## Remote contextual inquiry

Pure ethnography requires being there. Adapted versions:
- **Screen-share + think-aloud during real work** — close-ish to in-person observation
- **Diary studies** ([see separate page](diary-studies.md)) — user self-records over time
- **Day-in-the-life videos** — user records their own day, researcher reviews
- **Slack/Discord embedding** — researcher joins customer's workspace

Not as rich as physical presence, but tractable for distributed teams.

## When to use ethnography

✅ **High-stakes new product** — entering a new domain you don't yet understand
✅ **Mature product mystery** — usage data confuses; behavior doesn't match interviews
✅ **B2B / regulated** — work is constrained by org rules invisible from outside
✅ **Hardware** — physical environment matters

## When too heavy

❌ Quick UI iteration (use [usability testing](usability-testing.md))
❌ Pre-launch validation (use prototypes + interviews)
❌ Consumer apps with broad use cases (single environment isn't representative)
❌ When budget is tight (each session is 2-3 hours of researcher time)

## Common failure modes

- **Pretending to be silent observer** — purely silent ethnography doesn't surface interpretations; aim for contextual inquiry's apprentice model
- **Single-session ethnography** — 60 minutes captures a slice; real patterns need multiple visits
- **Researcher contamination** — your presence changes behavior. Some adjustment for "Hawthorne effect" needed.
- **Polished participants** — users tidy up their workflow when observed. Ask to see "the messy part."
- **Failing to interpret** — observation without synthesis = anecdotes, not insights
- **No confirmation step** — interpretations should be checked with the user in real time, not invented post-hoc

## See also

- [User interviews](concepts/user-interviews.md) — surfaces stated behavior; ethnography surfaces actual
- [Diary studies](concepts/diary-studies.md) — longitudinal cousin
- [Usability testing](concepts/usability-testing.md) — what users do *with your product*; ethnography is what they do *around it*
- [Jobs To Be Done](concepts/jobs-to-be-done.md) — ethnography is one way to discover the real job
