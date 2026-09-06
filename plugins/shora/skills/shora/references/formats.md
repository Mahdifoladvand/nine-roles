# Meeting formats

Nine ways to seat the table. Each one names its seats, its rounds, its output
and the condition that ends it. When the user does not name a format, run
`council`.

Every format obeys the house rules in `SKILL.md`: numbers carry producer tags,
the Critic speaks after a plan exists, no action item without a name and a
date, and the meeting halts at every stop and waits for the owner in a separate
message.

## Stops, per format

A stop is a hard break. The message ends at the question and the next message
starts with the owner's answer. A format with no stop says so here, so a reader
can tell a decision from an omission.

| Format | Stops | Where |
|---|---|---|
| `council` | 2 | After round 4 and after round 5, per the table in `SKILL.md` |
| `idea` | 1 | After the Advisor, before the Analyst prices anything |
| `triage` | 1, only if the decisive number is unknown | After the Analyst names it |
| `premortem` | 1 | After the first failure list, to ask what the owner has seen fail before |
| `scenarios` | 1 | Before writing the triggers, to ask what would make the owner switch |
| `control` | 1 | Before setting thresholds, to ask what the owner would call unacceptable |
| `intel` | 1 | To ask which unknown the owner would pay to close first |
| `assign` | 0 | Names and skills came in with the request |
| `retro` | 0 | The facts are in the ledger and the owner is telling the story |
| `followup` | 1 | After reading the ledger, to ask what actually happened |

One of the questions at any stop is never about a number.

---

## `council` - the full meeting

**Use when** the question is open, the decision matters, and nobody has decided
anything yet.

**Seats.** All nine.

**Rounds.** The eleven-round table in `SKILL.md`.

**Output.** Transcript, then minutes from `templates/minutes.md`.

**Ends when** a decision exists, with owners, dates, dissent and a review date.

**Three flavours.**

- *Strategy.* Horizon of a year or more. The Analyst's money axis dominates.
  The Critic's three plans are mandatory, not optional.
- *Operational.* This week's problem. Cut rounds 2 and 3 to three lines each.
  The Closer and the Organizer get the space instead.
- *Crisis.* Something is on fire. Seats: Coordinator, Closer, Controller,
  Critic. Twelve lines total. First question is "what stops the bleeding
  today", second is "what caused it", and the second question does not get
  answered until the first one has an owner.

---

## `triage` - the twelve-line verdict

**Use when** the user wants a fast opinion, not a meeting.

**Seats.** Coordinator, Analyst, Critic, Closer.

**Rounds.**
1. Coordinator: the question in one line, and what a good answer looks like.
2. Analyst: the one number this turns on, and whether we have it. Two lines.
3. Critic: the single strongest objection, with its trigger. Two lines.
4. Closer: the call, and the first action inside 48 hours. Two lines.

**Output.** One of exactly three verdicts:
- **Do it now** - and the first action.
- **Test it first** - and the cheapest test that would settle it, with a cost
  and a deadline.
- **No, because ___** - and the condition under which the answer would change.

**Ends when** one of those three sentences is written. Never end on "it
depends".

---

## `idea` - reviewing one idea properly

**Use when** somebody brings a proposal and wants it examined rather than
applauded.

**Seats.** Coordinator (frames), Spotter, Advisor, Analyst, Critic, Closer.

**Rounds.**
1. Coordinator: restate the idea in one sentence the proposer would accept.
2. Spotter: what is genuinely new in it, and what is a rewording of what we
   already do.
3. Advisor: what we would need to know, where that lives, what it costs.
4. **STOP.** The Coordinator holds the meeting. Ask the owner the figures the
   Analyst is about to assume, plus one question from `references/questions.md`.
   The message ends here. Wait.
5. Analyst: market, technical, money. Every number tagged. The decisive number
   named.
6. Critic: the failure, the trigger, and the number at which this is wrong.
7. Closer: go, no-go, or go-if - with the condition and the date.

**Output.** `templates/idea-review.md`.

**Ends when** the decisive unknown has a price and a deadline attached to it.

**Rule.** An idea is never rejected for being unfamiliar. It is rejected for a
number, a law, a capacity, or a customer who does not exist. Write which.

---

## `premortem` - it already failed, why?

**Use when** the plan is written and everybody likes it. That is when it
needs attacking.

**Seats.** Critic (leads), Controller, Analyst.

**Method.** Set a date six or twelve months out. State it as fact: "It is
March. The project failed. It was not close." Then each seat writes the story
of how.

**Rounds.**
1. Critic: five failure stories, one paragraph each, most likely first.
2. Analyst: which of the five is arithmetically most probable, and what would
   have had to move.
3. Controller: for each of the top three, the earliest observable signal, and
   who would see it first.

**Output.** A table: failure, likelihood (high/medium/low, stated not
computed), cost if it happens, earliest signal, guard, owner.

**Ends when** the top three failures each have a signal and a named watcher.

**Rule.** "The market might not want it" is not a failure story. "We launch in
month two, the first fifty customers do not reorder, and by month four we are
paying rent on a room we are not using" is a failure story.

---

## `scenarios` - three plans, with triggers

**Use when** something important is outside the company's control: a currency,
a regulation, a landlord, a supplier, a single large customer.

**Seats.** Analyst, Advisor, Critic, Coordinator.

**Rounds.**
1. Advisor: name the uncontrolled variable, its current value, and where its
   value is published.
2. Analyst: the plan at the current value - the realistic plan.
3. Analyst: the plan if the constraint lifts - the optimistic plan. What do we
   do with the room, and how fast can we take it?
4. Analyst: the plan if it doubles against us, or the permission is refused -
   the pessimistic plan. What survives, what gets cut, in what order?
5. Critic: for each plan, the observable trigger that switches us onto it.
6. Coordinator: what is common to all three plans - because that part starts
   today, whatever happens.

**Output.** `templates/three-plans.md`.

**Ends when** each trigger is an event somebody could observe, with a name
attached to watching it. "If things get bad" is not a trigger. "If the exchange
rate closes above X for five working days" is a trigger.

**Why this format exists.** A plan that works at today's exchange rate can stop
working at next month's. Somebody has to watch that number, and the switch has
to be written down before the number moves.

---

## `control` - designing the inspection

**Use when** something has been decided and now has to actually happen out in
the field, in branches, in vehicles, in shifts, in other people's hands.

**Seats.** Controller (leads), Organizer, Critic.

**Rounds.**
1. Controller: the standard, in physical terms. What does compliance look like
   to the eye?
2. Controller: the inspection - object, place, frequency, sample size, who.
3. Organizer: who does the inspecting, and who inspects them.
4. Critic: how would a clever person pass this inspection while breaking the
   standard? Close that.
5. Controller: the threshold that means stop, and what happens at that moment.

**Output.** `templates/qc-plan.md`.

**Ends when** every row has a number and a name, and the whole plan could be
read aloud to the team it inspects without anybody being ambushed.

**Hard rule.** Announce the check to the people it checks. If you cannot,
redesign it.

---

## `assign` - mapping nine roles onto real people

**Use when** the user has a real team and wants to know who plays what.

**Seats.** Organizer, Coordinator.

**Input needed.** Names, current jobs, and one line each on what that person is
actually good at. If the user gives only job titles, ask once for the second
half, then proceed with what you have and mark the guesses.

**Rounds.**
1. Organizer: the mapping. Nine roles, each with a primary name and a backup.
2. Organizer: the double-ups, and whether any breaks a rule (Critic plus
   Ideator on one person, Coordinator analysing their own proposal).
3. Coordinator: the empty seats, ranked by what each one costs this company
   specifically.
4. Coordinator: the cover plan for the most expensive empty seat, and whether
   it should be hired, trained, or rotated.

**Output.** `templates/role-map.md`.

**Ends when** every one of the nine roles has either a name or a written
admission that it is empty.

**Rule.** Name the empty seat. Filling it with the wrong person hides the gap.

---

## `intel` - the information plan

**Use when** the meeting keeps stalling on things nobody knows.

**Seats.** Advisor, Analyst.

**Rounds.**
1. Analyst: list the unknowns the decision actually rests on. Usually there are
   two, not eleven.
2. Advisor: for each - where the fact lives, the method, the cost, the days,
   the owner.
3. Analyst: rank by "would this change the decision?" Anything that would not
   change the decision comes off the list, however interesting.
4. Advisor: what will still be unknown on decision day, stated plainly.

**Output.** A table: question, why it matters, source, method, cost, days,
owner. Followed by the list headed "still unknown when we decide".

**Ends when** the cheapest decisive measurement has an owner and a date.

**Sources, in order of cost.** What we already hold and have not looked at
(receipts, bookings, complaints, the CRM). Ten phone calls to real customers.
A one-week live test. Public registries and published filings. A supplier who
already knows. A bought report, last, and only if a decision truly waits on it.

**Legal and consent boundary.** Public information, willingly given
information, and your own records. Not other people's confidential material,
not personal data collected without consent, not anything obtained by
pretending to be someone else.

---

## `retro` - after it landed

**Use when** a project, a campaign, an event or a quarter has finished.

**Seats.** Controller, Critic, Coordinator, Closer.

**Rounds.**
1. Controller: what we predicted and what actually happened, side by side, with
   numbers where numbers exist and `[NO DATA]` where they do not.
2. Critic: what went wrong, and what it cost. One number, not a mood.
3. Closer: what worked and should be repeated. Also one number.
4. Coordinator: one rule for next time, written as a rule.

**Output.** Four lines. That is the whole document.

**Rule.** Write the lesson as a rule. "We were too
optimistic" is an apology. "No launch date is set before the supplier confirms
in writing" is a rule. The second one changes what you do next time.

---

## `followup` - what happened to the last decision

**Use when** a review date has arrived, or the owner asks what became of an
earlier decision, or a new meeting is about to spend money the last one already
committed.

**Seats.** Coordinator, Controller, Critic, Closer.

**Input.** The ledger at `./decisions.md`, or the meeting pages under
`./meetings/`. Read `references/ledger.md` first. With no ledger, say so in one
line and offer to start one from this meeting forward.

**Rounds.**
1. Coordinator: which decision, taken when, and what it promised.
2. Controller: what we predicted against what happened, side by side, with the
   numbers that exist and `[NO DATA]` where the measurement never ran.
3. **STOP.** Ask the owner what actually happened, in their words, and one
   question from family 9 of `references/questions.md`. The message ends here.
4. Critic: which of our triggers fired and nobody acted on it.
5. Closer: what we still owe from that decision, with names and dates.
6. Coordinator: what carries forward, what is closed, and what capacity is now
   free again.

**Output.** An updated ledger entry, plus the four-line retro if the decision is
finished.

**Ends when** every open action from the earlier decision is either done,
reassigned with a new date, or killed on the record.

**Rule.** A promise nobody checked is the reason people stop believing meetings.
This format exists to check them.

## Running this with real people in a real room

The formats work the same when the nine roles are nine humans:

- Announce the roles at the start. People behave differently when they know
  their job is to object.
- Timebox each round out loud. The Coordinator cuts.
- Nobody objects before the plan exists. Say this at the beginning, every time,
  until it stops needing saying.
- One person writes the minutes during the meeting, not afterwards from memory.
- The dissent goes in the minutes with the name of who held it. When nobody disagrees, either the meeting decided nothing or somebody stayed
  quiet.
- End on the owners table. Read it aloud before anyone stands up.
