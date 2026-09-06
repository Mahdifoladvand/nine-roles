# The decisions ledger

A meeting that nobody reads back is a meeting that did not happen. The ledger is
one file in the folder the owner works in, `./decisions.md`, and it is the
memory that survives between councils.

Three jobs:

1. **Before a meeting** it says what earlier meetings already committed, so the
   room does not spend the same money twice.
2. **On a review date** it says what we predicted, so somebody can check.
3. **On the third meeting with the same company** it stops the council asking a
   question the owner already answered.

## Reading it, before the meeting starts

Read `./decisions.md` at intake, next to the organization profile. Pull four
things into the room and say them out loud in round 1:

- **Open commitments.** Money already promised over the next 90 days, and whose
  hours are already spoken for. This is the capacity envelope. A council that
  approves a fourth thing when three are running is writing a wish.
- **Review dates now due.** If one has passed and nobody checked, say so before
  the new decision. That is a finding.
- **Triggers that fired.** A pessimistic scenario with a trigger that already
  happened turns the new meeting into a `followup`.
- **Deep questions already asked.** Never ask the owner the same question from
  `references/questions.md` twice. Ask a different family, or ask what changed
  since their answer.

If the file does not exist, run the meeting anyway and offer once, at the end,
to start one from `templates/decisions-ledger.md`.

## Writing it, after the decision

Append. Never rewrite an entry, and never delete one. A decision that was
reversed gets a second block under the first, with the date and the reason.
People trust a record that shows its own mistakes.

One entry carries:

- Date, topic, and the mode that produced it.
- The decision in one sentence.
- The two or three reasons, each with its number and tag.
- The numbers register: every figure the decision rested on, with its tag.
- Owners, actions and dates.
- Blockers, with who clears them.
- The triggers to watch and who watches each.
- What was still unknown when the decision was made.
- Capacity committed: money over 90 days, and whose hours.
- The deep questions asked and what the owner answered.
- Status: open.

## Closing an entry

On the review date, `followup` adds an outcome block under the original:

- What we predicted, what happened, and the gap.
- Which trigger fired, and whether anybody acted.
- What it cost, or saved, with a number.
- One rule for next time, written as a rule.
- Status: closed, or killed, or extended with a new date.

## What the ledger is not

It is not a task tracker. Actions live in it because they came out of a
decision, and the ledger records whether they happened, not their daily state.

It is not a place for anything a person would not want written down about them.
Record decisions and numbers. When a blocker is a person, name the role and the
behaviour, never a judgement about the person.

## Where it lives

`./decisions.md` in the owner's working folder. One file, plain markdown, opens
in any editor, survives without this skill. If the owner keeps meetings in a
folder, `./meetings/` holds the HTML pages and `./decisions.md` indexes them.
