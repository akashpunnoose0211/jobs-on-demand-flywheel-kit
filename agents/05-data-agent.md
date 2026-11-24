# Install your data agent
**Jobs-On-Demand Flywheel Kit · Data · agent 5 of 5**

> This agent writes down where every lead, visit and dollar came from, keeps one weekly scoreboard, and alerts you when a number is getting worse, so you can see which marketing brings signed jobs.

## What this agent does
- Tracks where every lead, appointment, and dollar came from, maintains one weekly scoreboard of everything that matters, and sends push alerts when metrics are trending down.
- Records each lead's first source, never overwritten, plus whether the visit happened, whether the job signed and for how many dollars, so each counts back to that source and ad.
- Keeps one weekly scoreboard: one row per source, one per ad for paid sources, from first inquiry to signed dollars and reviews asked for.
- Every Friday, alerts [NUMBERS ALERT LIST] when a watched number got worse two weeks in a row, or dropped below the floor you set.
- Hands the ads agent (file 04) the rows for each ad, which it uses to move ad spend.
- Drafts a Friday review that calls each ad keep, fix, rotate or pause, judged the way the ads agent judges: booked appointments and their cost. You decide.
- Logs every decision and every failure, so the same mistake is not paid for twice.
- Walks you through setting up your own simple database, so customer, ad and job records sit in one place.

What it does not do: it never messages customers, and never changes a live ad, a budget or anything a person recorded. This do-it-yourself version does not join every tool you own into one brain that improves by itself; that is a separate, larger build.

## What you need before you start
**For the scoreboard (about one hour, then 20 minutes every Friday):**
- A spreadsheet your team can share. A Google Sheet or an Excel file both work.
- The software you keep your customers and jobs in (often called a CRM). It must hold a permanent "first source" field and the few fields in step 4 on each contact. It must also give you the week's contacts as a saved list or an export, with those fields showing. If it cannot export, your office reads the counts out each Friday instead.
- Access to your ad accounts and your Google Business listing.
- Optional: extra tracking phone numbers. Each one rings your normal office line and records which ad, mailer or sign the caller saw. Many customer tools sell these; GoHighLevel does. Without them, the person who answers asks how the caller heard of you.
- Your own test contact (your name, your mobile) and your [AVERAGE SOLD JOB] in dollars.
- From MY-NUMBERS.md: [REVIEW TIME] (when the Friday review runs), [COST PER APPOINTMENT LINE], and for the alerts [ALERT CHANNEL], [NUMBERS ALERT LIST], [ALERT HOURS], your floors, and [OUTCOME CHECK TIME] (when the sales rep is reminded, on the evening of a visit, to record what happened).
- **Push alerts** sent by your tools: your customer tool's own phone app notice, a text to the team member, or your team's chat app. A push alert goes to your team, never to a customer.

**Part 1 is the whole agent, and it needs no database.** Your customer software already holds every lead, booking and signed job. Part 1 adds the missing fields, a shared spreadsheet and a 20-minute Friday review where your AI fills the sheet from an export. Each step says what to do when your tools can't.

**Part 2 is optional.** It only removes the Friday typing: a database fills the scoreboard and sends the trend alerts by itself. Build it after a few weeks of real numbers, once you know which ones you watch.

**For your own database (about one weekend):** hand this part to whoever builds things for you, such as a tech-comfortable office manager.
- A hosted database. This guide uses Supabase as its example. Supabase is a website that hosts a database for you. A database is one place that holds your records in tables, like linked spreadsheets. The free plan works.
- Admin access to your customer software, plus its API key. An API key is a password that lets one piece of software read another.
- A way to run small jobs on a timer. Supabase has one built in, so you need nothing else. If you already use an automation tool, your AI assistant can use it instead. For automatic alerts it must be able to send on [ALERT CHANNEL].
- A payment or invoicing account.
- An AI coding tool, such as Claude Code or Codex.
- A password manager, to hold every key and password.

## How to install it
To install this agent alone, type **"install my data agent"**, or use the paste prompt at the end of `INSTALL-GUIDE.md`.

## Step by step

**Part 1: the scoreboard**

1. `AI` **Build the scoreboard sheet.** One spreadsheet, five tabs: Scoreboard, Definitions, Decision Log, Failure Log, Alert Log.
   - Scoreboard columns: Week, Source, Campaign, Ad, Spend, Inquiries, Leads, Qualified, Booked, Showed, No Outcome Yet, Quotes Sent, Signed, Signed Revenue, Jobs Finished, Review Asks, then the ten numbers from the agent's instructions below.
   - One row per source per week. A paid source gets one row per ad, with the source in its own column. One "All sources" row per week adds them up.
   - Put the formulas in row 2 so each new week works itself out. A source with no spend shows "no spend" in its cost columns, not an error.
   - Definitions tab: when each count counts (the rule is in the agent's instructions), and the watch list from step 7.
   Done when: all five tabs exist, and a made-up test row works out all ten numbers with no errors.

2. `You + AI` **Give every source its own trackable path.** If you use tracking numbers, you buy one each for Meta ads, Google Ads, your Google Business listing, mailers and yard signs. AI makes one QR code or short link for each print piece. AI adds one permanent "first source" field in your customer software, with a fixed list to pick from. Start the list from: Google search ads, Google pay per lead ads, Google Business listing, Google free search, Facebook ads, Instagram, Mailer, Yard sign, Referral, Returning customer. Keep only what you run. Whoever answers a new call asks how they heard of you and picks from the list. Tie call recordings and outcomes to the same contact and the same sold job. The source tags from the reviews agent (file 03, its source tags step) count as first sources too.
   Done when: every channel that matters has its own traceable path, the first-source field exists, and a second contact from a new source does not change it.

3. `You + AI` **Make every lead traceable to one ad.** AI drafts plain names for everything you run. You approve before any live ad is renamed.
   - Campaign: `[MARKET] - [TRADE] - [OFFER] - [MONTH YEAR]`
   - Ad set: `[MARKET] - [AUDIENCE] - [BUDGET] - [VERSION]`
   - Ad: `[PROBLEM] - [AD TYPE] - [VERSION]`

   No "Copy of Copy of" stays live. Each new contact gets stamped with the source, the campaign and the exact ad, using short labels at the end of each ad link. An ad that opens a Messenger chat has no link: the source comes from the ad details your customer software saves with the conversation. An instant form passes the ad name with the form. A call comes in on the tracking number for Meta ads, if you use one. (The ads agent, file 04, its page and tracking step.) Also save the customer's first message.
   Done when: a test lead from each live ad shows the source, the campaign and the exact ad on its contact. The lasting proof comes later: pick any job sold after tracking went live and name the exact ad behind it in under 60 seconds.

4. `You + AI` **Give every lead a record from first source to dollars.** AI adds four fields to each contact: Visit Date, Visit Outcome (held / no-show / cancelled / moved), Signed Date and Signed Amount. It reuses the other agents' fields, or creates them here if you skipped that agent. Every field gets one filler:

   | Field | Filled by | When |
   |---|---|---|
   | First source, campaign, ad | Automatic, from the ad or the tracking number. On a call, the person who answers. | First contact |
   | Qualified (tag `qualified`) | The booking agent (file 01) | During the first conversation |
   | Booked (tag `booked`) and Visit Date | The calendar booking. An automation copies the appointment time into Visit Date. If your tools can't, the person who books types it. | When the visit is booked |
   | Visit Outcome | The sales rep on that visit ([REP NAME]). If moved, the new time goes in Visit Date. | The same day as the visit |
   | Quote Sent At, Quote Amount | The sales rep (file 02 fields) | When the quote goes out |
   | Decision Status won, Signed Date, Signed Amount | The quote owner, [SALES OWNER] | The day the homeowner signs |
   | Job Completed At, Review Requested At | File 03 fields, on the job record linked to the contact | When the job is finished and the ask goes out |

   Done when: every field exists on your test contact, each has a named filler, and a test booking fills Visit Date.

5. `AI` **Build the missing-outcome alert.** One automation in your customer tool. At [OUTCOME CHECK TIME] each day, for every visit today with Visit Outcome empty, it sends alert 6 to the sales rep on that visit. No Outcome Yet counts the visits still empty. With the fallback, it makes a task for the rep (or a row on a shared list, if your tools have no tasks), checked daily by a named person.
   Done when: your test contact, booked for today with no outcome, gets the alert to your own phone at the check time (for the test, set the time a few minutes ahead). A test contact whose outcome is filled first gets none.

6. `You + AI` **Run the Friday review.** Every Friday at [REVIEW TIME], 20 minutes. A scoreboard week runs from one review to the next.
   - Until Part 2 is built, your office exports the week's contacts with the step 4 fields, or reads the counts out, and the AI fills the rows by the Definitions tab.
   - Spend comes from the billing page of each ad account, not the campaign report. Spend per ad comes from the ad report. If the two totals differ, the AI lists the gap.
   - The AI checks the trend alerts (step 7), then drafts a call for each live ad. You decide. Every call goes in the Decision Log.
   - The ads agent reads the Scoreboard rows for each ad: Spend, Booked and Cost per booked appointment. It needs to open this sheet. If it can't, you paste it those rows.
   Done when: every live ad has a logged keep, fix, rotate or pause call (or "not tested yet") with a one-sentence reason, two Fridays in a row.

7. `You + AI` **Set the trend alerts.** You write a floor in MY-NUMBERS.md for each number you want watched. The AI copies the watch list into the Definitions tab: each number, which way is worse, its floor and a named person. Each Friday the AI checks the trend rule, logs each alert and puts it at the top of the Friday draft. If it can send on [ALERT CHANNEL], it sends each alert to [NUMBERS ALERT LIST]; if not, you forward it.
   Done when: on three made-up weeks, a number that got worse twice gives the two-week alert, a number under its floor gives the floor alert, steady numbers give none, and each alert is in the Alert Log.

8. `You + AI` **Start the Failure Log.** AI builds the tab. Columns: Date, Lead source, What the agent did, What the customer said, What was missing or wrong, What a person did, Was the lead saved, Fix needed.
   Done when: the tab exists and every failure this week has a row that names the exact failure.

**Part 2: your own database**

9. `You + AI` **Create the database.** You open a database project (Supabase, in this guide's example). AI creates five tables and explains each in plain words: contacts (every person who ever inquired, with first source and ad), conversations (what was said), ad results (one row per ad per day), bookings (every appointment, its visit date and its outcome), jobs (signed work, signed date and signed amount).
   Done when: all five tables show in your database's table view (in Supabase, the Table Editor).

10. `You + AI` **Connect your customer software.** You supply the API key through your password manager. AI builds a timed job (in Supabase, its built-in scheduler) that runs every 15 minutes. It fetches only contacts changed since the last good run, with every step 4 field, and updates the same row each time, so there is never a duplicate.
    Done when: you change your test contact's Visit Outcome, wait one 15-minute cycle, and see its row update in the database.

11. `AI` **Connect your ad account.** A second job runs daily at 6am. It pulls yesterday's spend, views, clicks and results for each ad.
    Done when: yesterday's spend in the database matches your ad account to the cent. If not, the date range or time zone is off.

12. `AI` **Connect payments.** A third job runs on every payment or invoice (or a daily pull). It saves the customer, the contract amount, what was sold and the date.
    Done when: one test invoice shows as a job row with the right dollar amount on the right contact. If it differs from Signed Amount, the job row shows both.

13. `AI` **Build the two scoreboards.** AI saves two views. A view is a saved question that works itself out fresh each time someone opens it. One is the weekly scoreboard by source and ad, with the same columns as the Scoreboard tab. One is the Monday numbers. Your team, and the ads agent, can open both in your database's table view.
    Done when: both views open and fill with real numbers with nobody typing. If you put them on a web page, the page uses a read-only key. Never the master key.

14. `AI` **Send the trend alerts by themselves.** A fourth job runs every Friday before [REVIEW TIME], inside [ALERT HOURS]. It reads the weekly view and the watch list (AI copies the Definitions tab's watch list into the database), checks the trend rule, sends each alert to [NUMBERS ALERT LIST] through [ALERT CHANNEL], and saves it in an alert log table. If your automation tool cannot send on [ALERT CHANNEL], the alerts go at the top of the Friday draft instead.
    Done when: a made-up week that breaks the rule sends the alert to your phone with nobody typing, and it shows in the alert log table.

15. `You` **Set the safety rules.** Each team member gets their own logins; nobody shares a password; every key lives in the password manager. From day one, back up the database at least weekly: your plan's backups, or a scheduled export your AI assistant sets up. Name one person who owns this agent.
    Done when: backups show as scheduled, no shared passwords exist, and one owner is named in writing.

16. `AI` **After one month of real records, let the review draft itself.** AI reads the weekly scoreboard and the last four reviews, then drafts Friday's calls.
    Done when: the Friday review arrives drafted and you only judge the close calls.

## The agent's instructions
Save these as the standing instructions for the AI assistant you use every Monday and Friday (for example, a saved project or a custom assistant). That assistant is the data agent.

```
You are the data agent for [BUSINESS NAME], a [TRADE] business in [SERVICE AREA].

Your job: record where every lead, visit and dollar came from, keep the
weekly scoreboard, alert [NUMBERS ALERT LIST] when a watched number gets
worse, and draft the Friday review. You never message customers.

THE SIX STAGES
1. Inquiry: a conversation started, real or by accident.
2. Lead: we have a phone number or email.
3. Qualified: right service, right area, a real problem, owns the home,
   phone and ZIP on file.
4. Booked: on [REP NAME]'s calendar with a time.
5. Showed: the appointment happened. Visit Outcome says held.
6. Sold: signed job, with the signed amount.
After the sale, also count: quotes sent, jobs finished, review asks sent.

THE RECORD FOR EACH LEAD
First source, campaign and ad. Then Booked, Visit Date, Visit Outcome,
Quote Sent At, Decision Status, Signed Date, Signed Amount. Every visit,
quote and dollar counts back to that lead's first source and ad.
Only people record Visit Outcome and Signed Amount. You never fill them.

WHEN A COUNT COUNTS
Each event counts in the week it happened: booked in the week it was
booked, showed in the week of the visit, signed in the week it was
signed. A week runs from one Friday review to the next. A visit with
no outcome counts under No Outcome Yet, never as held.

THE TEN NUMBERS (per source, per paid ad, per week)
- Cost per inquiry = spend / inquiries
- Cost per lead = spend / leads
- Cost per qualified lead = spend / qualified
- Cost per booked appointment = spend / booked. This is the owner's number.
- Show rate = showed / booked
- Close rate = signed / showed
- Sales per ad dollar = signed revenue / spend
- Quote rate = quotes sent / leads
- Review ask rate = review asks / jobs finished
- Signed jobs with a named source = signed jobs with a first source /
  all signed jobs (All sources row only)

RULES
- One row per source per week. A paid source gets one row per ad.
- Never overwrite a contact's first source. Record later sources as
  assists when they are known.
- The last source shows what closed the loop, not that it worked alone.
- Use only numbers from the records. If a number is missing, say it is
  missing. Never guess.
- Every answer names the records it came from.
- Use [BUSINESS NAME]'s own average sold job: [AVERAGE SOLD JOB]. Never
  borrow another trade's number.
- Never judge an ad or a week on cost per inquiry, cost per lead or
  clicks.
- Never change a live ad, a budget or a customer record. Draft the change
  and ask [OWNER NAME]. The ads agent moves ad spend by its own rules,
  from the rows for each ad. You give it those rows. You never move money.

THE TREND ALERTS (every Friday, after the rows are filled)
Watch list: the numbers in the Definitions tab. Until [OWNER NAME]
changes it, watch these three: booked appointments by source, cost per
booked appointment by paid source, and signed jobs with a named source
(All sources row). Also watch any number with a floor in MY-NUMBERS.md.
Worse means lower for counts and rates, and higher for costs. For a
cost, the floor is the most [OWNER NAME] will accept.
Send an alert when either is true:
- Two weeks in a row: this week is worse than last week, and last week
  was worse than the week before.
- Past the floor: this week is worse than its floor.
When a number rests on only a few leads or visits, say so in the
Friday draft. One job can swing it.
[OWNER NAME] can change the watch list, the floors, or the two-week
rule. Use what the Definitions tab says today.
Each alert names the number, the source, the two values and the one
thing to check first. Take it from WHERE THE LEAK IS below, for the
stage the number belongs to. Cost per booked appointment: check the
booked count, then spend from billing. Quote rate: quotes that sat
after the visit. Review ask rate: jobs not marked complete, or asks
not sent. Signed jobs with a named source: empty first-source fields.
If visits behind that number have no outcome yet, the one thing to
check is recording them.
Send alerts only inside [ALERT HOURS]. Log every alert in the Alert Log.

THE FRIDAY REVIEW
Every Friday at [REVIEW TIME], fill the week's rows. Check the trend
alerts. Then call each live ad, by the same rule the ads agent uses.
The line is [COST PER APPOINTMENT LINE]. Read the last 21 days.
- NOT TESTED YET: live under 21 days, or spent less than the line. In
  its first 7 days, only check that it spends, is approved and links
  right.
- KEEP: 3 or more booked appointments, each at or under the line.
- PAUSE: spent 3 times the line or more and booked nothing, or the path
  is broken.
- FIX: a set-up problem. Wrong city in the ad, a broken page or link,
  the first reply wasting leads.
- ROTATE: it booked under the line before and now costs more. Add a new
  ad from its angle beside it. Change one thing only. Never the
  service, the market, the offer or the lead path.
Give one sentence of reason for each call. Never pause a good ad over
one noisy week. Check set-up before blaming the ad. Read the 12-week
trend, not one week.

WHERE THE LEAK IS
- High spend, few clicks: the ad or its opening.
- Many clicks, few leads: the offer or the message path.
- Many leads, few qualified: targeting, the ad's promise, or the first reply.
- Many qualified, few booked: slow first reply, the hand-off, or the calendar.
- Booked, low show rate: the confirmation and reminder messages.
- Shows, low close rate: the sales process or the offer. Not marketing.
- Many booked, low job value: who counts as qualified, or the mix of jobs.
Never solve a booking problem with more ads.

FAILURES
Log each failure with the exact thing that went wrong. One failure:
a person rescues it and moves on. Three alike: tell [OWNER NAME] it needs
a root cause this week.
```

## Every message it sends
Nothing goes to customers. If [ALERT CHANNEL] is a text, alerts use the business texting line agents 1 to 3 set up. Your AI assistant writes the Monday and Friday messages from the scoreboard when you open it.

**1. Monday numbers.** Every Monday morning, to [OWNER NAME]. Last week's full numbers, and the alerts already sent on Friday.

```
Monday numbers, week of [DATE]. Last week in brackets.
Spend: [SPEND] ([LAST WEEK])
Inquiries: [NUMBER] ([LAST WEEK])
Leads: [NUMBER] ([LAST WEEK])
Qualified: [NUMBER] ([LAST WEEK])
Booked: [NUMBER] ([LAST WEEK])
Visits held: [NUMBER] ([LAST WEEK]). No outcome yet: [NUMBER]
Signed: [NUMBER] for [AMOUNT] ([LAST WEEK])
Cost per booked appointment: [AMOUNT] ([LAST WEEK])
Cost per lead: [AMOUNT] ([LAST WEEK])
Cost per qualified lead: [AMOUNT] ([LAST WEEK])
Numbers alerts this week: [NUMBER, OR "NONE"]
```

**2. Friday review draft.** Every Friday at [REVIEW TIME], to [OWNER NAME].

```
Friday review draft, week of [DATE]. Nothing has been changed.
Numbers alerts: [EACH ALERT, OR "NONE"]
[AD NAME]: [KEEP / FIX / ROTATE / PAUSE / NOT TESTED YET]. [ONE-SENTENCE REASON]
[AD NAME]: [KEEP / FIX / ROTATE / PAUSE / NOT TESTED YET]. [ONE-SENTENCE REASON]
Cost per booked appointment this week: [AMOUNT]
Broke twice this month: [WHAT BROKE, OR "NOTHING"]
Reply with your decision on each line. I will log it.
```

**3. Repeat-failure flag.** The same day a third similar failure is logged, to [OWNER NAME].

```
The same failure has happened three times: [EXACT FAILURE].
Lead sources: [SOURCES]. Leads saved: [NUMBER] of 3.
This needs a root cause this week.
```

### Alerts to your team
Each is a team alert, your AI may adjust the wording. Each goes through [ALERT CHANNEL], inside [ALERT HOURS]. One outside those hours waits and goes out first thing.

**4. Number getting worse two weeks in a row.** To [NUMBERS ALERT LIST]. Team alert, your AI may adjust the wording.

```
Numbers alert:
[NUMBER] for [SOURCE] got worse two weeks in a row.
Was [LAST WEEK], now [THIS WEEK].
Check first: [ONE THING TO CHECK].
```

**5. Number below its floor.** To [NUMBERS ALERT LIST]. Team alert, your AI may adjust the wording.

```
Numbers alert:
[NUMBER] for [SOURCE] is [THIS WEEK],
below your floor of [FLOOR].
Check first: [ONE THING TO CHECK].
```

**6. Visit with no outcome.** To the sales rep on that visit ([REP NAME]), at [OUTCOME CHECK TIME] on the day of the visit. Team alert, your AI may adjust the wording.

```
No outcome yet:
[NAME],
[VISIT NAME] today at [TIME].
Mark it held, no-show, cancelled or moved.
```

## Test list
Use only made-up test leads on your own test contact (or copies), each with a different first source, and point every alert at your own phone.

| Test | Pass mark |
|---|---|
| Type one made-up week into the Scoreboard tab | All ten numbers work out, no errors. A source with no spend shows "no spend" |
| If you use tracking numbers, call each one from your own phone | Your test contact shows the right first source each time |
| Reach your test contact again through a second source | First source has not changed |
| Book a test lead for today and leave Visit Outcome empty | The no-outcome alert reaches your phone at the check time |
| Mark a test lead's visit held | It counts under Showed in its own source's row |
| Mark a test lead's quote won with a Signed Amount | Signed and Signed Revenue rise in its own source's row |
| Type three made-up weeks where Booked falls twice | On Friday, one two-week alert, with both values and its one thing to check, logged in the Alert Log |
| Type a made-up week past one of your floors | One floor alert, naming the floor |
| Type a made-up week with steady numbers | No alert |
| Change a floor in MY-NUMBERS.md, then re-check the same week | The alert follows the new floor |
| Give Show rate a test floor, leave one test visit with no outcome, and type a week under that floor | The alert's one thing to check is recording that visit |
| Type made-up rows for three ads after 21 days: one booked 3 under the line, one spent 3 times the line with none, one spent under the line | The Friday draft calls them keep, pause and not tested yet, the same piles the ads agent's practice run gives |
| Pick any job sold after tracking went live | You name the exact ad in under 60 seconds |
| Change your test contact in your customer software | Its row updates in the database within one 15-minute cycle |
| Compare yesterday's ad spend | Database matches the ad account to the cent |
| Send one test invoice | It shows as a job row, right amount, right contact |
| Open both scoreboard views | Both fill with real numbers with nobody typing |
| Let the Friday job run on a made-up week that breaks the rule | The alert reaches your phone with nobody typing |
| Check the safety rules | Backups scheduled, no shared passwords, one named owner |

## When a person takes over
- **Every Friday call.** The agent drafts. [OWNER NAME] decides on fixes and new ads. The agent never changes a live ad or budget; turning ads off and moving spend is the ads agent's job, by its own rules.
- **What happened at a visit.** Only the sales rep records it. The agent reminds, and never fills it in.
- **The signed amount.** [SALES OWNER] types it. If it differs from the invoice, a person decides which is right.
- **A numbers alert.** The person on [NUMBERS ALERT LIST] checks the data first, then picks the fix. Never blame a person over a number nobody has checked.
- **The watch list, the floors and the two-week rule.** Only [OWNER NAME] changes them.
- **A number does not match.** If ad spend is off by even a cent, stop. A person fixes it before anything is built on top. Tell [APPROVER NAME] too, so the ads agent does not move money on a wrong row.
- **A sold job cannot be traced in 60 seconds.** A person fixes the tracking before any budget moves.
- **Three similar failures.** A person finds the root cause that week.
- **A scheduled job, an alert or a backup did not run.** The named owner checks all four jobs, the missing-outcome alert and the backup every week.
- **A decision that cannot be explained in one sentence.** Nobody changes anything yet.
- **Accounts, keys and access.** A person buys the phone numbers, opens the accounts, stores every key and decides who sees what.

Want this installed for you? That is the Full Done-For-You Installation.
