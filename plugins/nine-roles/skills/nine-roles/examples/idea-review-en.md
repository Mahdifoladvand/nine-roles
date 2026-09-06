# Example: idea review (`idea` mode)

**The ask.** "We are a 14-person B2B software company. Our three largest
customers all asked for an AI assistant inside the product. Should we build it
this quarter?"

**Intake answers.** Decision: build it this quarter, yes or no. Constraint:
five developers, and one quarter. Already settled: we are not raising money.

**Numbers the user supplied.** 240 paying accounts `[OBSERVED]`. Annual
recurring revenue $1.2M `[OBSERVED]`. The three accounts asking account for
$164k of that `[OBSERVED]`. Five developers `[OBSERVED]`. 11 accounts
cancelled in the last 12 months `[OBSERVED]`. About 310 support tickets a
month `[OBSERVED]`.

---

**Coordinator.** One decision: does an AI assistant get built this quarter.
Constraint is five developers and thirteen weeks. We are not discussing
funding. A good answer names the number this turns on and the first action
inside 48 hours.

**Spotter.** Two things worth stopping on. First, you said all three customers
"asked for an AI assistant" - but in the same sentence you said two of them
described pulling a monthly summary they currently build by hand in a
spreadsheet. Those are not the same request, and one of them is a report, not
an assistant. Second, 310 tickets a month is a corpus. Somebody has already
written the answers to your customers' most common questions 310 times a month.

**Advisor.** What we know is in the numbers above. What we do not know, and the
decision rests on it: the running cost per active account per month
`[NO DATA]`, and how many of the 240 accounts would actually turn it on
`[NO DATA]`. Both are cheap to find: run the feature by hand for five accounts
for two weeks, with a person doing the work behind the interface, and count.
Cost is one developer-week and roughly $300 of model usage `[ASSUMED]`. Days:
fifteen. A third unknown is what the three customers meant - that costs three
phone calls.

**Analyst.** Three axes.

*Market.* The requesters are 3 of 240 accounts `[OBSERVED]`, holding 14% of
revenue `[OBSERVED]`. Whether the other 237 want it is `[NO DATA]`. Note the
shape of the risk: keeping three accounts is worth $164k a year, so this is
partly a retention question, not only a growth question - but none of the three
has said they would leave without it, and nobody has asked them.

*Technical.* The five developers have shipped integrations and reporting. None
has shipped a feature whose per-use cost is variable and whose output is
non-deterministic `[ASSUMED from the team description]`. That is the step
nobody here has done before, and it is the step that produces support load.
At ten times the volume, the cost line grows with usage, unlike every other
feature you own.

*Money.* Build cost: two developers for ten weeks `[ASSUMED]` = 20
developer-weeks, roughly $58k fully loaded at $2,900 per developer-week
`[ASSUMED]`. Priced as an $80 per month add-on `[ASSUMED]`, with a running
cost of $25 per active account per month `[ASSUMED, and this is the number I
am least sure of]`, contribution is $55 per account per month. Recovering
$58k needs about 1,055 account-months - that is 88 accounts subscribed for a
year, or 37 of every 100 accounts you have. If the running cost is $60 instead
of $25, contribution falls to $20 and you need 242 accounts, which is more
accounts than you have.

The decisive number: **running cost per active account per month**, currently
`[NO DATA]`. The second decisive number is the attach rate, also `[NO DATA]`.

This works only if a third of your existing accounts turn it on and keep it on.

**Critic.** I disagree with the Analyst's framing before I disagree with the
arithmetic. "Three customers asked" is three people who mentioned something in
a call. Ask each of them who signs the invoice and whether they would pay $80
a month for it. Two of the three, on the Spotter's reading, asked for a monthly
report - and a report is four days of work, not ten weeks.

Most likely failure: you spend ten weeks, ship it, 14 accounts turn it on, six
of them stop within a month, and the running cost is higher than the price. The
real damage is not the $58k. It is the quarter you did not spend on whatever
those 310 tickets are actually about.

Earliest signal: in a pilot, fewer than 12 of 20 invited accounts use it twice
in the second week.

The number at which this plan is wrong: running cost above $40 per active
account per month at an $80 price, or attach rate under 20%.

One thing to drop: the "assistant" framing. Build what two of the three
actually asked for - the monthly summary - and find out whether anybody wants
the rest.

**Closer.** Not a build, and not a refusal. A three-week measured pilot.
Action inside 48 hours: the founder phones all three accounts and asks two
questions - what would you do with it on a Tuesday morning, and would you pay
$80 a month for it. Owner: the founder, calls done by Friday. Done means three
written answers, not three impressions.

Then: one developer builds a manual version behind a form for 20 selected
accounts, three weeks, roughly $4k `[ASSUMED]`. Owner: the engineering lead.
Done means 20 accounts invited and usage counted daily.

---

## Verdict

**Test first.**

- **The test.** Three weeks, 20 accounts, manual behind the interface, about
  $4k `[ASSUMED]`.
- **Go if** at least 12 of the 20 use it twice in week two, and measured
  running cost stays under $30 per active account per month.
- **No if** attach is under 20% of the pilot group, or running cost exceeds $40.
- **Either way**, ship the monthly summary report. It was requested, it is four
  days of work `[ASSUMED]`, and it does not carry a variable cost.
- **Review date.** Three weeks from the pilot start, against two numbers:
  active users in week two, and running cost per active account.

## Still unknown on decision day

- Whether the 237 accounts that did not ask would ever turn it on. The pilot
  measures 20 of them, not 237. Say so in the minutes, and do not let the
  pilot's attach rate be quoted later as the company's attach rate.
