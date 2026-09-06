# Example: idea review (`idea` mode)

**The ask.** "We're a 14-person B2B software company. Our three largest
customers all asked for an AI assistant inside the product. Should we build it
this quarter?"

**Intake answers.** Decision: build it this quarter, yes or no. Constraint:
five developers, one quarter. Settled: we're not raising money.

**Numbers the user supplied.** 240 paying accounts `[OBSERVED]`. Annual
recurring revenue $1.2M `[OBSERVED]`. The three accounts asking hold $164k of
that `[OBSERVED]`. Five developers `[OBSERVED]`. 11 accounts cancelled in the
last 12 months `[OBSERVED]`. About 310 support tickets a month `[OBSERVED]`.

---

**Coordinator.** One decision today: do we build an AI assistant this quarter.
Five developers, thirteen weeks. Funding is off the table. I want the number
this turns on, and an action somebody starts within 48 hours.

**Spotter.** Two things to stop on. You said all three customers asked for an
AI assistant. Then in the same breath you said two of them described pulling a
monthly summary they build by hand in a spreadsheet. Which is it? Because a
summary report and an assistant are different builds.
Second thing: 310 tickets a month. Somebody on your team has already written
the answers to the common ones, 310 times a month. Has anyone read them
together?

**Advisor.** Nobody has, as far as I can tell. Two things we don't know, and
the decision sits on both. Running cost per active account per month
`[NO DATA]`. How many of the 240 accounts would switch it on `[NO DATA]`.
Both are cheap to find out. Run it by hand for five accounts for two weeks,
with a person doing the work behind the screen, and count. One developer-week
and about $300 of model usage `[ASSUMED]`. Fifteen days.
The third unknown costs three phone calls: what did those customers mean.

**Analyst.** Three axes.
Market. Three of 240 accounts asked `[OBSERVED]`, and they hold 14% of revenue
`[OBSERVED]`. The other 237 are `[NO DATA]`. Worth noticing: none of the three
said they'd leave without it, and nobody asked them.
Technical. Your five developers have shipped integrations and reporting. None
of them has shipped a feature that costs money every time somebody uses it
`[ASSUMED, from your description of the team]`. That's the new step, and it's
the one that generates support load.
Money. Two developers for ten weeks `[ASSUMED]` is 20 developer-weeks, about
$58k at $2,900 a week fully loaded `[ASSUMED]`. Price it at $80 a month, and
suppose running cost lands at $25 per active account per month `[ASSUMED, and
this is the number I trust least]`. Contribution is $55. Recovering $58k takes
1,055 account-months, so 88 accounts subscribed for a year. That's 37 of every
100 accounts you have.
If running cost is $60 instead of $25, contribution drops to $20 and you'd need
242 accounts. You have 240.
The decisive number is running cost per active account per month, and it's
`[NO DATA]`. Attach rate is second, also `[NO DATA]`.
This works only if a third of your accounts switch it on and keep it on.

**Critic.** Analyst, I'll argue with the framing before the arithmetic. Three
customers asked means three people said something on a call. Ask each of them
who signs the invoice and whether they'd pay $80 a month. Spotter is right
about what two of them described. A monthly summary is four days of work
`[ASSUMED]`.
The failure I'd bet on: you spend ten weeks, ship it, 14 accounts switch it on,
six of them stop within a month, and running cost comes in above the price.
The $58k isn't what hurts. You lose the quarter you could have spent on
whatever those 310 tickets are about.
Earliest signal: in a pilot, fewer than 12 of 20 invited accounts use it twice
in the second week.
Wrong at: running cost above $40 per active account at an $80 price, or attach
under 20%.
Drop the word assistant. Build what two of the three described and find out
whether anyone wants the rest.

**Closer.** Not a build, not a refusal. Three-week measured pilot.
Inside 48 hours the founder phones all three accounts and asks two questions:
what would you do with it on a Tuesday morning, and would you pay $80 a month.
Calls done by Friday. Done means three written answers, not three impressions.
Then one developer builds a manual version behind a form for 20 selected
accounts. Three weeks, about $4k `[ASSUMED]`. Owner is the engineering lead.
Done means 20 accounts invited and usage counted daily.

---

## Verdict

**Test first.**

- **The test.** Three weeks, 20 accounts, manual behind the interface, about
  $4k `[ASSUMED]`.
- **Go if** at least 12 of the 20 use it twice in week two, and measured
  running cost stays under $30 per active account per month.
- **No if** attach is under 20% of the pilot group, or running cost passes $40.
- **Either way**, ship the monthly summary report. Somebody asked for it, it
  takes four days `[ASSUMED]`, and it carries no variable cost.
- **Review date.** Three weeks after the pilot starts, against two numbers:
  active users in week two, and running cost per active account.

## Still unknown on decision day

Whether the 237 accounts that said nothing would ever switch it on. The pilot
measures 20 of them. Write that in the minutes, so nobody quotes the pilot's
attach rate later as the company's attach rate.
