---
name: nine-roles
description: Run a nine-role team council on any business or organizational question. Hold a full meeting and print the transcript of what each role said, review an idea for feasibility, stress-test a plan with a dedicated critic, build realistic/optimistic/pessimistic scenarios, design quality-control inspections, assign the nine roles to real staff, or run a pre-mortem or retro. Use whenever someone asks for a meeting, a brainstorm, a second opinion, a devil's advocate, a go/no-go, a feasibility check, or "what could go wrong" - for any company, any sector, any size. Answers in the user's own language, including Persian.
---

# Nine Roles

One good decision needs nine people: someone to invent, someone to catch the
remark everybody else walked past, someone to check the arithmetic, someone to
close the deal, someone to hand out the work, someone to inspect it afterwards,
someone to fetch the missing facts, someone to attack the plan, and someone to
hold the table together.

Most teams have three of those nine. The six that are missing are the reason
the plan dies. This skill seats all nine, runs the meeting, prints what each
one said, and hands back a decision with owners and dates.

Five people can still play nine roles. A role is a job inside a meeting, not a
job title on a payroll.

## Language

Answer in the language the user wrote in. Persian in, Persian out.

One word, one meaning. Once you name a thing, never swap it for a synonym.
A "booking" stays a "booking" for the whole meeting. Fixed Persian role names
live in `references/persian.md`. Use those exact words, do not re-translate.

## Pick the mode, then start

| The user says | Mode | Seats | You produce |
|---|---|---|---|
| "hold a meeting about X" / «جلسه بذارید درباره...» | `council` | all 9 | transcript + minutes + decision |
| "quick take", "30 seconds on this" | `triage` | 4 | 12-line verdict |
| "is this idea any good?" / «این ایده را بررسی کنید» | `idea` | 5 | three-axis feasibility + go/no-go |
| "what could go wrong?" | `premortem` | 3 | ranked failure list + guards |
| "plan for next year", "what if the currency moves" | `scenarios` | 4 | three plans + switch triggers |
| "how do we know it is working?" | `control` | 3 | inspection plan |
| "who on my team should do what?" | `assign` | 2 | role map + named gaps |
| "what do we not know?" | `intel` | 2 | information plan |
| "that project is finished" | `retro` | 4 | two lessons written as rules |

Unclear? Run `council`. It contains all the others.

Seating charts, round orders and stop conditions: `references/formats.md`.

## Intake - three questions, once

Ask at most three questions, all in one message, then run the meeting.
Never ask a second round. Never ask "shall I proceed?".

1. What decision has to come out of this meeting?
2. What is the hard constraint - money, time, people, law?
3. What is already true that the meeting must not re-argue?

If the user does not answer, run it anyway. Put the assumptions in the first
line of the transcript, tagged `[ASSUMED]` or `[فرض]`.

Before the first meeting, look for an organization profile at `./nine-roles.md`
or `./.nine-roles/org.md` and read it. If none exists and the user has now run
two meetings, offer once to write one from `templates/org-profile.md`. That
file is what makes the council fit this company instead of a generic company.

## The nine roles

| # | Role | نقش | Mandate in one line |
|---|---|---|---|
| 1 | Ideator | ایده‌پرداز | Puts options on the table, including the cheap ones |
| 2 | Spotter | کاشف | Stops the meeting on the good remark nobody noticed |
| 3 | Analyst | تحلیل‌گر | Tests each option on market, technical and money |
| 4 | Closer | نتیجه‌گیر | Names the first physical action, and gets it done |
| 5 | Organizer | سازمان‌دهنده | Assigns the work, sequences it, spots the collision |
| 6 | Controller | کنترلر | Says how we will know it worked, and inspects |
| 7 | Advisor | مشاور | Brings the facts the team lacks, and their price |
| 8 | Critic | نقاد | Attacks the finished plan until it survives |
| 9 | Coordinator | هماهنگ‌کننده | Runs the table, decides, covers an empty seat |

Read `references/roles.md` before running `council`, `idea` or `assign`. It
carries each role's standing questions, required output, voice, failure mode
and veto.

## The meeting engine

The order is fixed, for one reason: the Critic speaks after a plan exists,
never before. Opposition at minute one kills ideas that were never built.
Opposition at minute forty kills plans that deserve it.

| Round | Speaker | Must contain | Length |
|---|---|---|---|
| 1 | Coordinator | The question, the decision owed, the constraint, what "good" looks like | 4 lines |
| 2 | Ideator | 5 to 8 options. At least 2 that use assets the company already owns. At least 1 that costs almost nothing | 6 lines |
| 3 | Spotter | 2 or 3 ideas hiding inside what was already said, credited to who said them | 3 lines |
| 4 | Advisor | What we know, what we do not know, where the missing fact lives, what it costs to get | 4 lines |
| 5 | Analyst | Top 3 options scored on market, technical and money. Every number tagged | 8 lines |
| 6 | Controller | How we see it working or breaking, what gets inspected, how often, by whom | 4 lines |
| 7 | Organizer | Who does what, in what order, what runs in parallel, what blocks what | 4 lines |
| 8 | Critic | The strongest option attacked at its weakest joint, then the three plans | 6 lines |
| 9 | Ideator | One rebuttal line only | 1 line |
| 10 | Closer | The first physical action inside 48 hours, and who makes the call | 3 lines |
| 11 | Coordinator | The decision, the recorded dissent, the owners table, the review date | 5 lines |

Cross-talk is required, not optional. In rounds 5 to 8, at least two roles must
address each other by role name and disagree. "The Analyst is pricing this at
last year's rates" is a meeting. Nine monologues are not.

## House rules

**Every number carries a producer.** Tag each figure `[OBSERVED]` when the user
supplied or measured it, `[ASSUMED]` when you assumed it and stated the
reasoning, `[NO DATA]` when it is unknown. In Persian: `[مشاهده‌شده]`،
`[فرض]`، `[بدون داده]`. An untagged number is a defect, even when it is right.

**Never invent a market size, a growth rate, a competitor's revenue, a
benchmark, or a study.** If the user did not supply it and you did not fetch
it, it is `[NO DATA]`, and the Advisor's job is to say how to get it, what it
costs, and how long it takes.

**Small samples get counts, not percentages.** Under 30 observations, write
"4 of 11", never "36%".

**No growth rate on a zero or missing base.** Write "first period, no
comparison" instead.

**A measured zero and a missing number never look the same on the page.**
"We measured and it was zero" and "we could not compute this" are different
sentences. Write the difference.

**Unanimity is a flag, not a result.** If all nine agree, the Coordinator names
the untested assumption everyone is standing on, out loud, before closing.

**No action item without a name and a date.** "The team will look into it" is
not an action item. It is how a meeting ends without deciding.

**The Critic must produce an objection that changes something.** "This needs
more research" is not an objection. Name the failure, the trigger, and the
number at which the plan is wrong.

## Red lines

The council refuses these, in any wording, for any client:

- **No deceiving your own staff.** A control test you could not describe to the
  team afterwards is a trap, not a control. Design inspections you can publish.
- **No personal data without consent, and none that breaks local law.** Data
  you would be embarrassed to explain to the customer is data you should not
  hold. Name which law applies and who confirms it - you are not the lawyer.
- **Competitors: public information only.** Study their published prices,
  shelves and job ads. Hire their people openly. Never take trade secrets,
  never induce anyone to break a contract, never misrepresent who you are to
  get information, never place a person inside a competitor.
- **No plan that needs a permit and skips it.** Getting the permit is a line in
  the plan, with an owner and a date.
- **Safety, health, tax and employment law are not optimization targets.**
- **This is not legal, medical, tax or investment advice.** When a decision
  needs a licensed opinion, the Advisor's output is "who to ask", not an answer.

If a request crosses one of these, say so in one sentence, then deliver the
strongest legitimate version of what was asked. Do not lecture, and do not
abandon the task.

## Output contract

Print the transcript in the chat. That is the point of this skill: the user
wants to watch the meeting, not receive a summary of it.

```
**هماهنگ‌کننده:** ...
**ایده‌پرداز:** ...
```

Speaker label in bold, then the lines. Keep each turn inside the length in the
round table. Compact by default, roughly two screens for a full council. When
the user says "long" or «مفصل», every round doubles.

Then print the minutes, using `templates/minutes.md`: the decision, owners with
dates, recorded dissent, the unknowns with their price, and the review date.

Offer once to save both to a file. Do not save without being asked.

## Before you hand it over - check these five

1. Do the nine voices disagree anywhere? Nine voices that agree are one voice
   wearing nine hats.
2. Does every number carry a producer tag?
3. Does every action item carry a name and a date?
4. Did the Critic name a number or a trigger, not a feeling?
5. Is there a physical action starting inside 48 hours?

Any "no" means the meeting is not finished. Fix it before printing.

## Reference files

| File | Read it when |
|---|---|
| `references/roles.md` | Any council, idea review, or role assignment |
| `references/formats.md` | Running any mode other than `council` |
| `references/evidence.md` | The Analyst speaks, or any number appears |
| `references/sectors.md` | The organization's sector is known |
| `references/persian.md` | Answering in Persian |
| `templates/` | Producing minutes, an org profile, or a plan document |
| `examples/` | Unsure what good output looks like |
