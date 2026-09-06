# Nine Roles

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

> **Analyst:** Contribution per order: 240,000 × 42% ≈ 101,000 `[ASSUMED - using
> last year's cost of goods; this year it is lower]`. Fixed cost per month:
> rent 28 + four salaries 96 + energy 15 ≈ 139M `[ASSUMED]`. Break-even:
> 139M ÷ 101,000 ≈ **46 orders a day**. The current branch does about 129 a day
> `[OBSERVED]`. The decisive number - daily orders in the new neighbourhood -
> is `[NO DATA]`.
>
> **Critic:** I disagree with the Analyst before I disagree with the
> arithmetic. That 42% margin is last year's flour and oil price. At 35% the
> break-even jumps to 55 orders a day. The number the whole decision rests on
> is itself an assumption.
>
> **Closer:** From tomorrow morning the cashier asks each customer which
> neighbourhood they came from and writes it in the sales book. Owner: Ms
> Rezaei, starting Saturday. Cost: zero, ten seconds per sale.

Decision: not this year, measure for three weeks first - because the number the
whole decision rests on costs nothing to find out, and 770M is locked up if it
is wrong.

Full examples: [Persian council](plugins/nine-roles/skills/nine-roles/examples/meeting-fa.md) ·
[English idea review](plugins/nine-roles/skills/nine-roles/examples/idea-review-en.md)

---

## Install

### Claude Code, as a plugin (recommended)

```
/plugin marketplace add Mahdifoladvand/nine-roles
```

```
/plugin install nine-roles@nine-roles
```

### Claude Code, by copying the folder

Copy the skill folder from this repo into your skills folder:

- macOS / Linux: `~/.claude/skills/nine-roles`
- Windows: `C:\Users\<you>\.claude\skills\nine-roles`

```bash
git clone https://github.com/Mahdifoladvand/nine-roles.git
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
    formats.md              nine meeting formats, seat by seat
    evidence.md             the arithmetic, and the rules that stop fake numbers
    sectors.md              ten sectors: what to inspect, which number lies
    persian.md              Persian names, tags and typography
  templates/                minutes, org profile, idea review, three plans,
                            inspection plan, role map
  examples/                 one full Persian meeting, one English idea review
```

---

## راهنمای فارسی

**نُه نقش** یک شورای تیمی برای کلود است. موضوع را می‌دهید، نُه نقش سر میز
می‌نشینند، جلسه برگزار می‌شود، حرف هر نقش را می‌بینید، و در پایان یک تصمیم
با مسئول و تاریخ تحویل می‌گیرید.

برای هر سازمانی کار می‌کند: قنادی، کارخانه، کلینیک، شرکت نرم‌افزاری، خیریه.
اگر فارسی بنویسید، کل جلسه فارسی است.

**چه چیزی را درست می‌کند.** اگر از هوش مصنوعی درباره‌ی یک تصمیم کاری بپرسید،
یک متن مطمئن با درصدهای ساختگی می‌گیرید. این مهارت این کار را نمی‌کند: هر عدد
برچسب منبع دارد — `[مشاهده‌شده]`، `[فرض]`، یا `[بدون داده]` — و عددی که کسی
ندارد، ساخته نمی‌شود. به‌جایش مشاور می‌گوید چطور، با چه هزینه‌ای و در چند روز
می‌شود آن را فهمید.

**چند قاعده‌ی سخت:**
- هیچ اقدامی بدون نام مسئول و تاریخ ثبت نمی‌شود.
- زیر ۳۰ مشاهده، درصد داده نمی‌شود؛ «۴ از ۱۱» نوشته می‌شود.
- بازرسی مخفی از پرسنل طراحی نمی‌شود. کنترلی که نتوانید برای تیم بلند بخوانید،
  کنترل نیست، تله است.
- درباره‌ی رقیب فقط از اطلاعات عمومی استفاده می‌شود.
- نقاد آخر حرف می‌زند، بعد از اینکه نقشه ساخته شد.

**نصب:** دستور زیر را در Claude Code بزنید:

```
/plugin marketplace add Mahdifoladvand/nine-roles
```

```
/plugin install nine-roles@nine-roles
```

یا پوشه‌ی `skills/nine-roles` را در `~/.claude/skills/` کپی کنید.

**نمونه‌ی خروجی:** [جلسه‌ی کامل فارسی](plugins/nine-roles/skills/nine-roles/examples/meeting-fa.md)

---

## Contributing

Sector notes are the most useful thing to add: what a controller in your
industry actually inspects, and which number your industry habitually flatters
itself with. Open a pull request against `references/sectors.md`.

## License

MIT. Use it inside your company, change it, ship it with your own product.
