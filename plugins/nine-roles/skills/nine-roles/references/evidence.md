# Evidence rules and the arithmetic

This file is what stops a nine-role meeting from becoming nine confident voices
inventing numbers. Read it whenever the Analyst speaks, or whenever any figure
appears anywhere in the output.

---

## 1. Every number carries its producer

Three tags, and no fourth:

| Tag | فارسی | Means |
|---|---|---|
| `[OBSERVED]` | `[مشاهده‌شده]` | The user supplied it, or it was measured, or it was read from a named source |
| `[ASSUMED]` | `[فرض]` | You assumed it, and the reasoning is written next to it |
| `[NO DATA]` | `[بدون داده]` | Nobody knows, and pretending otherwise would be a lie |

An untagged number is a defect, even when it happens to be correct. The reader
cannot tell your measurement from your guess, so they must treat all of it as a
guess - which destroys the value of the parts that were real.

**Never invent:** market sizes, growth rates, competitor revenues, conversion
rates, industry benchmarks, survey results, academic studies, or case-study
figures. If it was not supplied and not fetched, it is `[NO DATA]`, and the
Advisor's job becomes "here is how we would find out, and what that costs".

**A measured zero and a missing number are different facts.** Write "0 bookings
in March `[OBSERVED]`" or write "March bookings `[NO DATA]` - the till was
replaced and the old export was lost". Never draw them the same way, and never
let a chart show an empty month as a zero.

---

## 2. Rules that stop the common lies

**Under 30 observations, use counts.** "4 of 11 customers" - never "36%". A
percentage on a small sample invents precision that the sample cannot carry.

**No growth rate on a zero or missing base.** Write "first period, no
comparison". Growth from one customer to three is not 200% growth, it is two
extra customers.

**An average hides its distribution.** If the range matters - and for revenue,
waiting time, order size and delivery time it always matters - give the range
or the median beside it.

**Revenue is not margin.** A busy day and a profitable day are different days.
Any option that is argued on revenue alone gets sent back to the Analyst.

**Intent is not purchase.** People who say they would buy are not customers.
Count deposits, pre-orders, signed contracts, actual visits. Ask what the
person did, not what they said they would do.

**Reach is not response.** Do not report how many people saw it. Report how
many answered, and what that cost each.

**Free is not demand.** Take-up of something free tells you almost nothing
about take-up of the same thing at a price.

**One large customer is not a market.** State the concentration: "68% of
revenue from 2 customers `[OBSERVED]`" changes every plan on the table.

---

## 3. The minimum arithmetic

The Analyst does not need a financial model. The Analyst needs these five
lines, and must refuse to skip any of them.

**Contribution margin per unit**
`price - variable cost per unit`
Variable cost means what it actually costs to serve one more: materials,
packaging, the commission, the delivery, the payment fee. Not rent.

**Break-even volume**
`fixed costs per month / contribution margin per unit`
Say it in units per day as well as per month, because a person can picture
"eleven a day" and cannot picture "330 a month".

**Cash out before cash in**
`days of stock + days until the customer pays - days until we pay the supplier`
This number, in days, multiplied by daily spend, is the cash the plan needs
before it earns anything. It is what kills small companies far more often than
a bad margin does.

**Payback**
`money spent up front / monthly contribution`
In months. If the answer is longer than the lease, the licence, the equipment
warranty or the season, say so in the same line.

**The decisive number**
One number that the whole option hangs on. Name it. If it is `[NO DATA]`, the
Analyst's veto applies: measure it before deciding, or decide explicitly to
gamble on it and write that in the minutes.

---

## 4. Sensitivity - what happens when the number moves

For anything the company does not control - exchange rate, fuel, rent, a
platform's commission, a regulated price - give three columns, not one:

| | -30% | today | +30% |
|---|---|---|---|
| Contribution per unit | | | |
| Break-even per day | | | |
| Payback in months | | | |

If the option only works in the middle column, that is not a plan, that is a
bet. Say the word "bet" in the minutes, so the owner is choosing it knowingly.

---

## 5. When there is no data - the cheapest measurement ladder

Climb from the bottom. Most decisions are settled on the first two rungs, and
most teams start on the fifth.

1. **Look at what you already have.** Receipts, bookings, the complaints book,
   the CRM, the delivery log, last year's schedule. Most companies are sitting
   on the answer and have never queried it.
2. **Ask ten real customers.** Not a survey. Ten conversations, same three
   questions, written down the same day.
3. **Run it once, small.** One week, one branch, one shelf, one route, one
   day's menu. A real transaction beats any forecast.
4. **Public sources.** Registries, published filings, competitors' own price
   lists and job adverts, official statistics.
5. **Someone who already knows.** A supplier, a distributor, a former employee
   of the sector, an industry association.
6. **Buy the report.** Last. Only when a real decision is waiting on it, and
   only when you know which page you need.

State the cost and the days for each rung you propose. "We could know this for
about two days of one person's time" is a decision-grade sentence. "We should
do more research" is not.

---

## 6. Presenting numbers honestly

- Put the unit and the period on every figure: "per order", "per month",
  "per branch".
- Put the sample beside every rate: "3 of 12 `[OBSERVED]`".
- Put the assumption on the same line as the number it produced, not in a
  footnote nobody reads.
- Round to the precision you actually have. "About 40" is honest. "41.7" from a
  guess is not.
- If an element cannot be computed honestly, do not render it. An empty space
  with "`[NO DATA]` - the till does not record this" is worth more than a zero
  that will be quoted back to you in six months as a fact.
- Currency: use whatever the user uses, and never silently convert.

---

## 7. The three axes, in full

The Analyst tests every surviving option on all three. An option that passes
two and fails one has failed.

**Market.** Who buys it, specifically enough to name a group you could reach
this week. How we reach them and at what cost per person reached. What they do
today instead. What would make them switch, in their words. How many of them
there are, and where that count came from.

**Technical.** Whether we can make or run it with the people, space and
equipment we already have. The one step nobody in the company has done before.
What breaks at ten times the volume. Which outside party has to agree - a
supplier, a landlord, a regulator, a platform. How long their agreement takes.

**Money.** The five lines in section 3, plus the sensitivity table when an
uncontrolled price is involved.

Then one sentence, always: **"This works only if ___ is true."** That blank is
what the Critic attacks, and it is the most useful sentence in the whole
meeting.
