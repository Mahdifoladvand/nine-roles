# Persian output

When the user writes in Persian, the whole meeting is in Persian: the speaker
labels, the tags, the minutes, the tables.

## Fixed names - never re-translate mid-meeting

| # | English | فارسی | Do not use |
|---|---|---|---|
| 1 | Ideator | ایده‌پرداز | خلاق، مبتکر |
| 2 | Spotter | کاشف | شکارچی ایده |
| 3 | Analyst | تحلیل‌گر | آنالیزور، کارشناس |
| 4 | Closer | نتیجه‌گیر | تمام‌کننده، فینیشر |
| 5 | Organizer | سازمان‌دهنده | مجری، هماهنگ‌کننده |
| 6 | Controller | کنترلر | بازرس، ناظر |
| 7 | Advisor | مشاور | تحلیلگر اطلاعات |
| 8 | Critic | نقاد | منتقد، مخالف |
| 9 | Coordinator | هماهنگ‌کننده | رهبر، کاپیتان، مدیر |

One word, one meaning. If the meeting calls something «رزرو» in round two, it
is «رزرو» in round eleven. Never swap to «نوبت» or «بوکینگ» for variety. A
reader who sees two words assumes two things.

## Evidence tags

| English | فارسی |
|---|---|
| `[OBSERVED]` | `[مشاهده‌شده]` |
| `[ASSUMED]` | `[فرض]` |
| `[NO DATA]` | `[بدون داده]` |

## Writing rules

- One idea per sentence. One instruction per sentence.
- Active voice, and name the actor: «سرور درخواست را رد می‌کند», not «درخواست
  رد می‌شود».
- No ambiguous pronoun. If «آن» could point at two nouns, repeat the noun.
- The warning comes before the action, never after it.
- State the fact, then the consequence.
- Numbers instead of adjectives: «۱۹ ثانیه» beats «کند». «۹ از ۱۱» beats
  «تقریباً همه».
- Use «بدون داده» exactly where a number is unknown. Never write صفر instead.

## Typography

- Guillemets «...» for quotations, not "...".
- Half-space in compound words: ایده‌پرداز، هماهنگ‌کننده، تحلیل‌گر.
- Latin technical terms keep their Latin spelling in brackets on first use, then
  the Persian word only: «حاشیه سود مشارکتی (contribution margin)».
- Keep numerals in the form the user used. Do not convert ۱۲۰ to 120 or the
  reverse.
- Currency stays as the user wrote it. Never convert تومان to ریال silently, or
  either one to a foreign currency.

## Transcript labels

```
**هماهنگ‌کننده:** موضوع جلسه ...
**ایده‌پرداز:** ...
**نقاد:** ...
```

## Minutes headings

| English | فارسی |
|---|---|
| Decision | تصمیم |
| Owners and dates | مسئول و تاریخ |
| Recorded dissent | مخالفت ثبت‌شده |
| Unknowns and their price | مجهولات و هزینه‌ی دانستن‌شان |
| Review date | تاریخ بازبینی |
| First action within 48 hours | نخستین اقدام تا ۴۸ ساعت |
