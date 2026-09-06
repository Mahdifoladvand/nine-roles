# Nine Roles

*فارسی: [README.fa.md](README.fa.md)*

A team council for Claude. You give it a question, it seats nine roles, runs
the meeting, prints what every role said, and hands you a decision with owners
and dates.

Works for any organization: a bakery, a factory, a clinic, a software company,
a charity. Answers in your language, including Persian.

**The problem it fixes.** Ask an AI about a business decision and you get a
confident essay with invented percentages. Ask a real team and you get whoever
speaks loudest. This skill does neither: it runs a structured meeting, tags
every number with where it came from, and refuses to invent the ones nobody
has.

---

## The nine roles

| # | Role | نقش | What it does |
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

A team of five people can still play nine roles. A role is a job inside a
meeting, not a job title.

---

## Nine ways to use it

| Say this | You get |
|---|---|
| "Hold a meeting about opening a second branch" | Full council: transcript, decision, owners, dates |
| "Quick take: should we raise prices 8%?" | A twelve-line verdict - do it, test it, or no because |
| "Review this idea" | Feasibility on market, technical and money, then go / no-go |
| "What could go wrong with this plan?" | Pre-mortem: ranked failures, early signals, guards |
| "Plan for next year, the currency is unstable" | Three plans with observable switch triggers |
| "How do we know the branches follow the rule?" | An inspection plan you could read aloud to the team |
| "Here is my team, who should do what?" | The nine roles mapped to real people, plus the gaps |
| "What do we not know?" | An information plan with costs and days |
| "The campaign finished" | A four-line retro, written as rules |
| "What happened to that decision?" | The ledger read back: predicted against actual, and what you still owe |

---

## What it will not do

This matters more than the feature list.

- **It does not invent numbers.** Market sizes, growth rates, competitor
  revenue, benchmarks, studies: if you did not supply it, it is marked
  `[NO DATA]` and the Advisor tells you how to find out, what it costs, and how
  many days it takes.
- **Every figure carries its producer:** `[OBSERVED]`, `[ASSUMED]` or
  `[NO DATA]`. A measured zero and a missing number never look the same.
- **No percentages on small samples.** Under 30 observations you get "4 of 11".
- **No action item without a name and a date.**
- **No secret tests on your own staff.** A control you could not describe to
  the team afterwards is a trap, not a control - the skill will redesign it.
- **No competitor work beyond public information.** No trade secrets, no
  inducing anyone to break a contract, no pretending to be someone else.
- **No personal data without consent**, and the skill names which law you
  should check rather than pretending to be your lawyer.
- **No legal, medical, tax or investment advice.** For those, the output is
  "who to ask".

---

## What the output looks like

From a real run - a confectionery with 14 staff, deciding on a second branch:

> **Spotter:** Hold on. At the start you said you send boxes to two offices on
> Thursdays. So you already have a delivery route and corporate customers, and
> nobody has counted them.
>
> **Analyst:** I worked out the second branch. Rent 28, four salaries 96,
> energy and supplies 15. That's 139M a month `[ASSUMED]`. Divide by the
> 101,000 each order leaves you and it needs 1,376 orders a month. **46 a
> day.** The current branch does 129 `[OBSERVED]`. Daily orders in the new
> neighbourhood: nobody knows `[NO DATA]`.
>
> **Critic:** That 42% margin is last year's flour and oil. At 35% the
> break-even goes to 55 a day. So the number this whole decision sits on is
> itself an assumption.
>
> **Closer:** Saturday morning the cashier starts asking which neighbourhood
> people came from. Ms Rezaei. Costs nothing, ten seconds a sale.

Decision: not this year, measure for three weeks first - because the number the
whole decision rests on costs nothing to find out, and 770M is locked up if it
is wrong.

## The meeting stops and asks you

Twice in a council, the meeting halts. The Coordinator asks you at most three
questions and the message ends there. Nothing else is printed until you answer.

One of those questions is never about a number. It asks what the decision is
for, what would make you stop, what you cannot take back, or what would change
your mind. The bank of them is in
[references/questions.md](plugins/nine-roles/skills/nine-roles/references/questions.md),
with a rule attached: before asking, the council writes down what changes with
each plausible answer, and cuts the question if the answer changes nothing.

Your answers retag figures from assumed to observed, and the transcript says
what each answer changed.

## It remembers the last decision

Every council appends to `decisions.md` in your folder: the decision, the
numbers it rested on with their tags, the owners, the triggers to watch, and
what was still unknown. The next meeting reads it first, so the room knows what
money and whose hours are already committed, and never asks you the same deep
question twice.

When a review date arrives, `followup` reads the ledger back: what we predicted
against what happened, which trigger fired, and what you still owe from that
decision.

## The manager page

The person who has to act on a meeting is usually not the person who ran it, so
a council does not end in a chat window.

Every council and idea review also writes one self-contained HTML file. A
manager opens it on a phone, prints it to PDF, or emails it as it is. No
server, no login, no other file needed.

The page answers the questions a manager asks in order:

1. **What did you look at?** Every option that reached the table, with a
   verdict and a reason. Options nobody discussed say so, instead of
   disappearing.
2. **What did you decide?**
3. **Why?** Two or three reasons, each carrying its number.
4. **What is in the way?** Each blocker with what it stops, who clears it, by
   when, and what happens if nobody does.
5. **Who does what, by when?**
6. **What do we still not know**, and what does finding out cost?

Then the full transcript, where every figure carries its evidence tag. The
header counts the meeting: options examined, speaking turns, and how many
numbers were measured against how many were assumed.

The page is built from
[`templates/meeting-page.html`](plugins/nine-roles/skills/nine-roles/templates/meeting-page.html)
and saved next to your work as `meetings/<date>-<topic>.html`.

**Font.** The page asks for Peyda first and falls back to Vazirmatn, which it
loads from Google Fonts. Peyda is a commercial font from fontiran.com, so this
repository ships no font file. If your organization holds a Peyda licence, put
your `@font-face` blocks between the `PEYDA-FONT-START` and `PEYDA-FONT-END`
markers in the template, and the page stays one self-contained file. Any other
Persian font works the same way.

Full examples: [Persian council](plugins/nine-roles/skills/nine-roles/examples/meeting-fa.md) ·
[English idea review](plugins/nine-roles/skills/nine-roles/examples/idea-review-en.md) ·
[the same council as a manager page](plugins/nine-roles/skills/nine-roles/examples/meeting-fa.html)
(download the file and open it in a browser)

---

## Install

### Claude Code, as a plugin (recommended)

```
/plugin marketplace add mahdifooladvand/nine-roles
```

```
/plugin install nine-roles@nine-roles
```

### Claude Code, by copying the folder

Copy the skill folder from this repo into your skills folder:

- macOS / Linux: `~/.claude/skills/nine-roles`
- Windows: `C:\Users\<you>\.claude\skills\nine-roles`

```bash
git clone https://github.com/mahdifooladvand/nine-roles.git
cp -r nine-roles/plugins/nine-roles/skills/nine-roles ~/.claude/skills/
```

For one project only, put it in `.claude/skills/nine-roles` inside that
project.

### Claude.ai or the API

Upload the contents of `plugins/nine-roles/skills/nine-roles/` as a skill, or paste
`plugins/nine-roles/skills/nine-roles/SKILL.md` into a Project's instructions and attach the
`references/` files.

---

## Make it fit your organization

Once, write a short profile and keep it in the folder you work in. The council
reads it before every meeting and stops giving generic advice.

Copy [`templates/org-profile.md`](plugins/nine-roles/skills/nine-roles/templates/org-profile.md)
to `nine-roles.md` in your working folder, and fill in what you know: sector,
size, the team and what each person is actually good at, the real constraints,
and the numbers you genuinely have.

Leave blanks rather than guessing. A blank becomes `[NO DATA]`, and `[NO DATA]`
is information. A guess becomes a number somebody quotes back at you in six
months.

---

## What is inside

```
plugins/nine-roles/skills/nine-roles/
  SKILL.md                  the engine: modes, rounds, house rules, red lines
  references/
    roles.md                the nine role cards, with veto powers
    characters.md           who the nine are, and how each one talks
    questions.md            ten families of question that change a decision
    formats.md              ten meeting formats, seat by seat, with their stops
    evidence.md             the arithmetic, and the rules that stop fake numbers
    ledger.md               the decisions ledger and the follow-up loop
    sectors.md              ten sectors: what to inspect, which number lies
    persian.md              Persian names, tags and typography
  templates/                the manager page, minutes, org profile, decisions
                            ledger, idea review, three plans, inspection plan,
                            role map
  examples/                 one full Persian meeting (markdown and manager page),
                            one English idea review
```

---

## راهنمای فارسی

راهنمای کامل فارسی، با همه‌ی بخش‌های این صفحه، اینجاست:
**[README.fa.md](README.fa.md)**

نصب سریع در Claude Code:

```
/plugin marketplace add mahdifooladvand/nine-roles
```

```
/plugin install nine-roles@nine-roles
```

---

## Contributing

Sector notes are the most useful thing to add: what a controller in your
industry actually inspects, and which number your industry habitually flatters
itself with. Open a pull request against `references/sectors.md`.

## Credits

The voice rules that keep the nine roles sounding like people come from
[stop-slop](https://github.com/hardikpandya/stop-slop) by Hardik Pandya, MIT.

## License

MIT. Use it inside your company, change it, ship it with your own product.
