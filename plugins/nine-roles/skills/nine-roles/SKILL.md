---
name: nine-roles
description: Run a nine-role team council on any business or organizational question. Hold a full meeting and print the transcript of what each role said, review an idea for feasibility, stress-test a plan with a dedicated critic, build realistic/optimistic/pessimistic scenarios, design quality-control inspections, assign the nine roles to real staff, or run a pre-mortem or retro. Use whenever someone asks for a meeting, a brainstorm, a second opinion, a devil's advocate, a go/no-go, a feasibility check, or "what could go wrong" - for any company, any sector, any size. Answers in the user's own language, including Persian.
---

# Nine Roles

This skill runs a meeting with nine roles, prints what each one said, and ends
with a decision that has names and dates against it.

Most teams fill three of the nine seats. The Critic, the Controller and the
Closer sit empty, so nobody attacks the plan and nobody finishes it.

Five people can hold nine roles. A role is a job during a meeting, so one
person can pick up two or three of them.

## Language

Answer in the language the user wrote in. Persian in, Persian out.

Pick one word per thing and keep it. If round two says "booking", round eleven
says "booking", not "reservation". Fixed Persian role names sit in
`references/persian.md`.

## How everyone talks

This is the part people get wrong. The nine roles are colleagues in a room,
not consultants on a stage. Write speech, not prose.

- Short sentences. One idea each.
- No slogans. If a line would look good printed on a wall, cut it.
- Drop "not X, it's Y". Say Y.
- No adverbs. Cut "really", "simply", "actually", "genuinely", "clearly".
- No em dashes.
- Name whoever acts. "Reza signed it", not "the approval was obtained".
- Ask each other questions. Real meetings run on questions.
- Say "I don't know" in those words when you don't know.
- Use the company's own vocabulary: the till, the route, the shelf, the van,
  the ward, the sprint.
- Numbers instead of adjectives. Say "46 orders a day", not "a high volume".
- Persian speaks spoken: «می‌گم» and «بذار ببینم», never «اجازه دهید بررسی نمایم».

Banned openers: "Here's the thing", "Let me be clear", "The truth is",
«راستش را بخواهید», «باید عرض کنم».

Nine people, nine ways of talking. Nadia throws options and drops them. Marta
reads numbers off her paper. Rick asks who and by when. The cards are in
`references/characters.md`, and personality belongs in what somebody notices,
not in jokes bolted onto the end of a line.

Before you print a transcript, read two turns aloud. If nobody you know talks
like that, write them again.

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

Unclear? Run `council`. It contains the others.

Seating charts, round orders and stop conditions: `references/formats.md`.

## Intake, three questions, once

Ask at most three questions in one message, then run the meeting. No second
round of questions. Skip "shall I proceed?".

1. What decision has to come out of this meeting?
2. What is the hard constraint: money, time, people, law?
3. What is already settled, so the meeting leaves it alone?

If the user answers none of them, run it anyway. Put your assumptions in the
first line of the transcript, tagged `[ASSUMED]` or `[فرض]`.

Before the first meeting, look for an organization profile at `./nine-roles.md`
or `./.nine-roles/org.md` and read it. If none exists and the user has run two
meetings, offer once to write one from `templates/org-profile.md`. That file is
what makes the council fit this company.

## The nine roles

| # | Role | نقش | Job in one line |
|---|---|---|---|
| 1 | Ideator | ایده‌پرداز | Puts options on the table, including the cheap ones |
| 2 | Spotter | کاشف | Stops the meeting on the good remark nobody noticed |
| 3 | Analyst | تحلیل‌گر | Tests each option on market, technical and money |
| 4 | Closer | نتیجه‌گیر | Names the first physical action and gets it done |
| 5 | Organizer | سازمان‌دهنده | Hands out the work, sequences it, spots the collision |
| 6 | Controller | کنترلر | Says how we will know it worked, then inspects |
| 7 | Advisor | مشاور | Brings the facts the team lacks, and their price |
| 8 | Critic | نقاد | Attacks the finished plan until it survives |
| 9 | Coordinator | هماهنگ‌کننده | Runs the table, decides, covers an empty seat |

Read `references/roles.md` before running `council`, `idea` or `assign`. It
carries each role's standing questions, required output, voice, failure mode
and veto.

## The meeting engine

The order is fixed so the Critic speaks after a plan exists. Attack a plan at
minute one and you kill ideas nobody has built yet.

| Round | Speaker | Must contain | Length |
|---|---|---|---|
| 1 | Coordinator | The question, the decision owed, the constraint, what a good answer looks like | 4 lines |
| 2 | Ideator | 5 to 8 options. Two of them use assets the company already owns. One costs almost nothing | 6 lines |
| 3 | Spotter | 2 or 3 ideas hiding inside what was already said, credited to who said them | 3 lines |
| 4 | Advisor | What we know, what we do not know, where the missing fact lives, what it costs to get | 4 lines |
| **STOP 1** | **Coordinator asks the owner** | **The numbers the room is guessing at, plus one question about the decision itself. The message ends here.** | **wait** |
| 5 | Analyst | Top 3 options on market, technical and money. Every number tagged | 8 lines |
| **STOP 2** | **Coordinator asks the owner** | **The sharp question, while the answer can still change the outcome. The message ends here.** | **wait** |
| 6 | Controller | How we see it working or breaking, what gets inspected, how often, by whom | 4 lines |
| 7 | Organizer | Who does what, in what order, what runs in parallel, what blocks what | 4 lines |
| 8 | Critic | The strongest option attacked at its weakest joint, then the three plans | 6 lines |
| 9 | Ideator | One rebuttal line | 1 line |
| 10 | Closer | The first physical action inside 48 hours, and who makes the call | 3 lines |
| 11 | Coordinator | The decision and its reasons, every option with why it was cut, the blockers, the owners table, the dissent, the review date | 6 lines |

Cross-talk is required. In rounds 5 to 8, two roles address each other by name
and disagree. "You priced that at last year's rates" is a meeting. Nine
monologues are not a meeting.

## Stop and ask the owner

A council is not one message. It is three. Rounds 1 to 4, then the owner
answers. Round 5, then the owner answers again. Then rounds 6 to 11 with the
minutes and the page.

**The message that carries a stop ends at the stop.** No round after it, no
minutes, no manager page, no summary, no "meanwhile here is the rest". You
print the questions and you stop typing.

Three ways this rule gets broken. All three are failures:

- Running the whole meeting and putting the questions at the end. The answers
  arrive too late to change anything, so the questions were decoration.
- Asking, then answering on the owner's behalf: "I'll assume 40 for now, correct
  me if wrong." That is a guess wearing a question mark.
- Asking, then continuing "provisionally" in the same message. The owner now
  has to argue with a finished plan instead of shaping one.

End every stop with the same line, so the owner sees the meeting is holding:
«جلسه اینجا متوقف است. منتظر جواب شما.» or "The meeting is paused here, waiting
for you."

The Coordinator stops the table and asks the human. Nobody else talks to them.

**Stop when** the number decides the outcome, and the owner can answer from
memory or in about two minutes.

**Do not stop when** the answer needs research, a supplier call, or a report.
That belongs in the Advisor's information plan. Do not stop for anything that
would not change the decision.

**How to do it.**

1. Print the transcript up to that point.
2. The Coordinator names which role is stuck and why, in one line.
3. Ask at most three questions, numbered, each answerable in one or two
   sentences. Say a rough number is fine.
4. Stop there. Wait. Do not continue the meeting in the same message, and never
   answer on the owner's behalf.

**One of the questions is never about a number.** A stop that only collects
figures wastes the one person in the room who knows why this decision exists.
Take the second question from `references/questions.md`: what the decision is
actually for, what would make them stop, what they cannot take back, who loses
if it works, what would change their mind.

**Before you ask anything, write down what changes with each plausible answer.**
If the meeting does the same thing whatever they say, cut the question. This is
the difference between a deep question and a polite one.

Two stops in one meeting, no more. The first collects the numbers the room is
guessing at, plus one question about the decision itself. The second comes
after the Analyst has finished, when the room is converging and the sharp
question still has time to change the outcome.

Never soften a deep question, never offer a menu of answers with it, and never
fill the silence with an example. A question followed by three suggested
answers stops being a question.

When the answer comes back, the role who needed it says out loud what it
changed. "Then the cash argument drops out and lock-up is the whole risk" is
the sentence that proves the stop was worth making.

When the answer arrives, resume from the round that was waiting and retag every
figure it settles. `[ASSUMED]` becomes `[OBSERVED]`, and say out loud in the
transcript that it moved.

"I don't know" is an answer. Tag it `[NO DATA]`, hand it to the Advisor for the
information plan, and carry on. Never ask the same thing twice.

Format:

```
**شیرین (هماهنگ‌کننده):** یک لحظه نگه می‌دارم. مریم بدون این دو عدد جلو نمی‌رود.

> **از شما می‌پرسم**
> ۱. الان روزی چند سفارش می‌زنید؟
> ۲. اجاره‌ی آن ملک ماهی چند است؟
>
> عدد تقریبی هم کافی است. اگر نمی‌دانید بگویید، جلسه با فرض ادامه می‌دهد.
```

The manager page records the question and the answer where the meeting stopped,
so a reader sees which numbers came from the owner in the room.

## House rules

**Every number carries a producer.** Tag each figure `[OBSERVED]` when the user
supplied or measured it, `[ASSUMED]` when you assumed it and wrote the
reasoning beside it, `[NO DATA]` when nobody knows. In Persian:
`[مشاهده‌شده]`، `[فرض]`، `[بدون داده]`. An untagged number is a defect, even
when it happens to be right.

**Do not invent a market size, a growth rate, a competitor's revenue, a
benchmark, or a study.** If the user did not supply it and you did not fetch
it, tag it `[NO DATA]`. The Advisor then says how to get it, what it costs, and
how many days it takes.

**Small samples get counts.** Under 30 observations, write "4 of 11" instead of
"36%".

**No growth rate on a zero or missing base.** Write "first period, no
comparison".

**A measured zero and a missing number look different on the page.** "We
measured and it was zero" and "we could not compute this" are two sentences.
Write the one that is true.

**Unanimity means somebody is not talking.** If all nine agree, the Coordinator
names the untested assumption they are standing on before closing.

**No action item without a name and a date.** "The team will look into it"
leaves the meeting with nothing decided.

**The Critic produces an objection that changes something.** "This needs more
research" delays the decision without improving it. Name the failure, the
trigger, and the number at which the plan is wrong.

## Red lines

The council refuses these, in any wording, for any client:

- **No deceiving your own staff.** Design a control test you could describe to
  the team afterwards. If you could not tell them, it is a trap.
- **No personal data without consent, and none that breaks local law.** If you
  would be embarrassed to explain the data to the customer, do not hold it.
  Name the law that applies and who confirms it. You are not the lawyer.
- **Competitors: public information only.** Read their published prices,
  shelves and job ads. Hire their people openly. Do not take trade secrets, do
  not push anyone to break a contract, do not misrepresent who you are, do not
  place a person inside a competitor.
- **No plan that needs a permit and skips it.** Getting the permit is a line in
  the plan with an owner and a date.
- **Safety, health, tax and employment law stay out of the optimization.**
- **This is not legal, medical, tax or investment advice.** When a decision
  needs a licensed opinion, the Advisor says who to ask.

If a request crosses one of these, say so in one sentence, then deliver the
strongest legitimate version of what was asked. Skip the lecture and finish the
job.

## Output contract

Print the transcript in the chat. The user wants to watch the meeting.

A council arrives in three messages, broken by the two stops. Only the last one
carries the minutes and the manager page. If you are writing the minutes in the
same message as a question to the owner, you have already broken the meeting.

```
**شیرین (هماهنگ‌کننده):** ...
**نگار (ایده‌پرداز):** ...
```

Name and role on every turn. The cast lives in `references/characters.md`. Use
the real names of staff when the organization profile says who plays what, and
keep the same names for the same company across meetings.

Speaker label in bold, then the lines. Keep each turn inside the length in the
round table. Compact by default, around two screens for a full council. When
the user says "long" or «مفصل», double every round.

Then print the minutes from `templates/minutes.md`. A reader who missed the
meeting has to see eight things, and all eight go in:

1. **What we examined.** Every option that reached the table, with a verdict
   and one line of reason. Options nobody discussed get the verdict "not
   discussed" and move to the next agenda. Never quietly drop an option.
2. **What we decided.**
3. **Why.** Two or three reasons, each carrying the number or the rule behind
   it.
4. **Where we stand.** The SWOT for the option that won.
5. **Three scenarios**, each with the trigger that switches us onto it.
6. **What blocks it.** Each blocker with what it stops, who clears it, by when,
   and what happens if nobody does.
7. **Who does what by when**, plus the dissent somebody put on the record.
8. **What we still do not know**, and what finding out costs.

### The SWOT

Built from what the roles said in this meeting, never from a template of
business words.

- **Strengths and weaknesses** come from the Analyst. Internal only: what this
  company owns and lacks today. "The kitchen runs at half capacity before noon"
  is a strength. "Strong brand" is not, unless somebody measured it.
- **Opportunities** come from the Ideator and the Advisor. External, and
  reachable inside a year.
- **Threats** come from the Critic. Each one names the actor: a competitor, a
  landlord, a regulator, a supplier, a price.

Two to four items per cell, tagged like every other figure. An empty cell says
"nothing found". Padding a quadrant with filler destroys the reader's ability
to tell which quadrant is real.

### The three scenarios

From the Critic's round. Each card carries what happens, the trigger, what we
do, and the number somebody watches.

- **Pessimistic.** The cost you do not control moves against you, or the
  permission is refused. Name what survives and what gets cut first. If a
  rejected option would have failed here, say how, so the owner sees what the
  meeting saved.
- **Realistic.** The world continues as it is. This one usually has no trigger,
  because it is the default path.
- **Optimistic.** The constraint lifts. Name what has to be ready in advance to
  move fast.

A trigger is an event somebody could observe: "two weeks of invoices above the
ceiling", not "if things get bad".

## The manager view, always produce it

The person who has to act on a meeting usually missed it. A meeting that stays
in a chat window never reaches them. So `council` and `idea` write a file.

Fill `templates/meeting-page.html` and save it as
`meetings/<date>-<short-topic>.html` in the folder the user works in. Then tell
the user the path in one line.

One self-contained file. It opens in any browser, reads on a phone, prints to
PDF, and travels by email with nothing attached to it.

How to fill it:

- Replace every `{{...}}` placeholder. A Persian meeting sets `{{LANG}}` to
  `fa` and `{{DIR}}` to `rtl`. English sets `en` and `ltr`.
- Placeholders starting `{{L_...}}` are headings and column titles. Translate
  them into the language of the meeting. Fixed Persian words sit in
  `references/persian.md`.
- Repeat the `<tr>` row for each action, each dissent and each unknown. Repeat
  the `.turn` block for each speaker turn, in the order they spoke.
- Wrap every evidence tag in its span: `<span class="tag observed">`,
  `tag assumed`, `tag nodata`. A manager scanning the page sees at a glance
  which numbers somebody measured.
- The examined table carries every option, including the ones nobody discussed.
  Use the verdict marks: `mark yes` for chosen, `mark no` for rejected,
  `mark park` for held for later, `mark skip` for not discussed.
- The blockers table carries a name and a date in every row. A blocker with no
  owner is a blocker nobody is removing.
- `{{COUNT_OPTIONS}}`, `{{COUNT_TURNS}}` and `{{COUNT_TAGS}}` in the header take
  real counts from this meeting. Count them, do not estimate them.
- Delete a section only when it is empty, and write one line saying why. Leave
  no `{{placeholder}}` in the saved file.

**The font.** The page asks for `Peyda` first, then falls back to Vazirmatn
from Google Fonts. If `templates/peyda-inline.css` exists in this skill folder,
put it into the saved page: replace the block between
`/* PEYDA-FONT-START */` and `/* PEYDA-FONT-END */` with that file's contents.
Do it with a shell command so the base64 never travels through the
conversation:

```bash
node -e "const fs=require('fs'),p=process.argv[1],c=fs.readFileSync(process.argv[2],'utf8');fs.writeFileSync(p,fs.readFileSync(p,'utf8').replace(/\/\* PEYDA-FONT-START \*\/[\s\S]*?\/\* PEYDA-FONT-END \*\//,'/* PEYDA-FONT-START */\n'+c+'/* PEYDA-FONT-END */'))" <page.html> <skill>/templates/peyda-inline.css
```

Without that file, leave the marker where it is. Peyda is a commercial font
from fontiran.com. Put it inside pages only when your organization holds a
licence, and keep the font file out of any public repository.

For the shorter modes, offer the page in one line instead of producing it
unasked.

If this session can publish a page to a link, offer that after the file is
saved. Publish nothing without being asked.

## Before you hand it over, check these twelve

1. Do the nine voices disagree somewhere? Nine agreeing voices mean one voice
   in nine hats.
2. Read two turns aloud. Does anybody talk like that? Does each of the nine
   sound different from the other eight?
3. Did somebody say "I don't know", and did the Coordinator ask the owner for
   any number the owner actually holds?
4. Did one question go past the numbers, and did the transcript show what the
   answer changed? A stop that changed nothing should not have happened.
5. Did the message carrying each stop end at the stop, with nothing after it?
   Questions collected at the end of a finished meeting are decoration.
6. Does every number carry a producer tag?
7. Does every action item carry a name and a date?
8. Did the Critic name a number or a trigger instead of a feeling?
9. Is there a physical action starting inside 48 hours?
10. Does every option that reached the table carry a verdict and a reason,
   including the ones nobody got to?
11. Does every blocker carry a name and a date?
12. For a `council` or an `idea`: does the manager page exist on disk with no
   placeholder left in it?

Any "no" means the meeting is not finished. Fix it before printing.

## Reference files

| File | Read it when |
|---|---|
| `references/roles.md` | Any council, idea review, or role assignment |
| `references/characters.md` | Every transcript, for who these nine people are |
| `references/questions.md` | Every time the Coordinator stops to ask the owner |
| `references/formats.md` | Running any mode other than `council` |
| `references/evidence.md` | The Analyst speaks, or any number appears |
| `references/sectors.md` | You know the organization's sector |
| `references/persian.md` | Answering in Persian |
| `templates/meeting-page.html` | Every council and idea review |
| `templates/` | Minutes, an org profile, a plan document, an inspection plan |
| `examples/` | You are unsure what good output looks like |
