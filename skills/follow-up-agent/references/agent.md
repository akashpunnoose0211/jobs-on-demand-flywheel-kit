# Install your follow-up agent
**Jobs-On-Demand Flywheel Kit · Sales · agent 2 of 5**

> This agent keeps going with every lead who went quiet until they book or say no. It reminds every booked homeowner so they show up, and rescues a missed visit fast. It chases every quote your rep sends until the homeowner decides. It alerts your sales team on their phones every time a person should act.

## What this agent does
- Follows up every quiet lead and sends push alerts to sales team to follow up with every lead.
- It still follows up every sent quote: a separate follow-up starts the moment a quote is sent and runs until the homeowner decides.
- Follows up with a quiet lead on a set clock, by text and email (Ladder 1 and Ladder 2 below).
- Reminds every booked homeowner before the visit, and rescues a missed visit the same day (Ladder 3 below).
- Gives your rep, and the texts it drafts, short approved answers to common objections.
- Creates a call task for your team at the right moments, and sends a push alert with it. This agent works by text, email and alert.
- Sends a push alert the moment a quiet lead or a quoted homeowner replies, and when a quote's follow-up ends with no decision.
- Stops the second the homeowner replies, cancels, decides or opts out. A booking ends the lead follow-up and starts the reminders. It never talks over a live conversation.
- Never sends "just following up". Every message carries something useful: a next step, an answer, proof, or a clear close.

## What you need before you start
- **Your customer tool (CRM), with automations.** It must keep fields, tags and stages on each contact, wait a set time, send a text or an email, and create a task for a person. Your AI assistant needs access to it, or it walks you through each click.
- **An approved business texting line,** and one number that sends both calls and texts. Check this first.
- **A real calendar and booking link** with true open times ([CALENDAR] and [BOOKING LINK]). Fake time slots kill trust.
- **Your booking agent (agent 1 of 5).** It sends the first reply, asks the intake questions and builds the first calls and their alerts. This agent picks up after.
- **A named owner for open quotes ([SALES OWNER]), and a backup ([BACKUP NAME]).**
- **Your approved facts:** [FINANCING YOU REALLY OFFER, OR "NONE"], the [REAL OBJECTION] homeowners raise after a quote and your [APPROVED ANSWER], your [EXACT WARRANTY FACTS], and your discount rules ([WHO MAY APPROVE, LIMIT, END DATE]).
- **Proof:** before-and-after photos of finished local jobs.
- **Push alerts to your team's phones,** sent by an automation: your customer tool's phone app notice, a text, or your team's chat app. Fallback: each alert becomes a task with the same words, on one fallback list. A named person keeps that list open all day, as agent 1 says. Nothing reaches a phone, so a reply or a due call waits until that person sees it.
- **From MY-NUMBERS.md:** [ALERT CHANNEL], [SALES ALERT LIST], [ALERT HOURS], [QUIET HOURS], [CALLER NAME] and [REP NAME].
- **One test contact you own:** your own phone number and email.

## How to install it
To install this agent alone, type **"install my follow-up agent"**, or use the paste prompt at the end of `INSTALL-GUIDE.md`.

## Step by step
1. `You` **Gather your facts.** Collect everything under "What you need" and every blank in the instructions below.
   Done when: your AI assistant has every fact and no blank is left.
2. `You` **Check the texting line.** Confirm the line is approved to send, and calls and texts use one number.
   Done when: a text sent from the business line lands on your own phone.
3. `AI` **Create the fields, tags and stages.** Fields: Quote Sent At, Quote Amount, Decision Status (pending, won or lost), Lost Reason, Financing Discussed, Next Follow-up (date and owner), Visit Date (the booked date and time; skip it if agent 1 or your calendar already has it), Visit Outcome (held, no-show, cancelled or moved; agent 5 reuses this field). A visit counts as booked when it has the `booked` tag and a Visit Date. Booked is not a Visit Outcome value. Tags: `booked`, and `stop bot` (a person has taken over; this is the manual hold). Both already exist if you installed agent 1. Stages: Ghosted for leads (already on the agent 1 board); Quote Sent, Decision Pending, Won and Lost for quotes, on their own board.
   Done when: every field, tag and stage exists and an automation can read it.
4. `AI` **Build the follow-up for leads who left a phone number.** Use Ladder 1 below. If you installed agent 1, its "Form lead fast reply" automation already sends the first text, both call tasks and the "Just tried you" text. Do not build those twice. Add only the 1-day and 3-day texts, in the same automation or in one that starts where it ends. Each call is a task for a person.
   Done when: the automation sits in draft with every wait, text and call task in order, and no step is built in both agents.
5. `AI` **Build the follow-up for leads who messaged you.** Use Ladder 2 below, and the channel rule under it. If you installed agent 1, its hand-off already creates the 5-minute call task. Do not build it again.
   Done when: the automation sits in draft with every step in order, and no call task is built in both agents.
6. `AI` **Build the show-up reminders.** Use Ladder 3 below. It starts when a visit is booked, and its times count back from the visit. The no-show rescue starts only when a person sets Visit Outcome to "no-show".
   Done when: the automation sits in draft, a test booking lines up every reminder at the right time, and setting Visit Outcome to "no-show" starts the rescue.
7. `You + AI` **Write the messages that have no fixed words.** Ladder 2's texts and email, the four weekly texts and the later quote touches are described below, not scripted. Your AI assistant drafts each from your facts; a person approves each. It also fits the objection answers to your trade, for a person to approve.
   Done when: every message has approved words and no blank.
8. `AI` **Build the quote follow-up.** It starts only when Quote Sent At is filled. Keep it separate from the lead ladders.
   Done when: filling Quote Sent At on your test contact starts it, and nothing else does.
9. `AI` **Wire the stop rules into every branch.** Use the "Stop at once when" list in the instructions.
   Done when: every branch has an owner and a stop rule. The test results come in step 13.
10. `You + AI` **Set up how alerts reach your team.** If you did this in agent 1 (its step 10), keep those settings and go to the "Done when". If not, fill in [ALERT CHANNEL], [SALES ALERT LIST] and [ALERT HOURS]. If no automation in your tools can send to a phone by itself, write "fallback" as [ALERT CHANNEL] and name the person who keeps the fallback list open all day.
    Done when: one test alert, sent by an automation to your own phone, lands there. Or, with the fallback: a test alert task shows on the fallback list, and the person who keeps it open is named.
11. `AI` **Add the push alerts.** Add an alert step at each moment under "Alerts to your team", in that moment's automation, on top of the task, never instead of it.
    - **One call task, one alert.** Agent 1 owns the alerts for the first call (its new-lead alert and its 5-minute "Still not called" alert). Never add an alert to that call task. Ladder 1's second call is built in agent 1 with no alert: add "Follow-up call due" to it. Every call task this agent builds gets "Follow-up call due".
    - **Replies from Ghosted:** a small automation of its own. It starts on any reply from a contact in Ghosted, creates a task for [SALES OWNER] with their words, and sends the reply alert.
    Done when: each of these carries exactly one alert step, in draft. Every call task on all three ladders, and the 1-day text task if you made one. Every reply branch, including Ghosted and Ladder 3. The end of the quote follow-up.
12. `You` **Name the owners.** Every open quote gets one owner and a next follow-up date. A quote stays "pending" only when it has both. A lost quote gets one reason from this list: price or budget; financing unavailable or declined; timing or not ready; chose a competitor; decision-makers not agreed; scope or service mismatch; trust or proof concern; could not reach after the full follow-up; solved it another way; duplicate or invalid. Add a short note of what the homeowner said and the date. Never write only "bad lead".
    Done when: every open quote shows a stage, an owner and a next date.
13. `You + AI` **Run the test list.** You play the homeowner from your own phone. Shorten every wait to a minute or two and set [SALES ALERT LIST] to only you; put both back after. For Ladder 3, book test visits a short time out. Your AI assistant checks the tags, stages and fields.
    Done when: every test passes, no real customer got a test message, and no team member got a test alert.
14. `You` **Teach the team the takeover play, then turn it on.** Delete the test contacts first. Show everyone on [SALES ALERT LIST] the takeover play in agent 1 (section "When a person takes over") and what each alert asks. Show [REP NAME] how to set Visit Outcome on each visit: held, no-show, cancelled or moved.
    Done when: every team member can run the play without looking it up, and the automations are live.
15. `You` **Set the check.** Daily: clear quotes with no owner and overdue follow-ups. With the fallback, also clear every alert task still open. Weekly: look at quotes that are 2, 7 and 30 days old. Also count how many booked visits were held, and how many no-shows booked again.
    Done when: one named person owns that check.

## The agent's instructions
These are the rules every automation in this file must follow. Your AI assistant builds them into steps 4 to 11.

```
You are the follow-up agent for [BUSINESS NAME], a [TRADE] company.

YOUR JOB
Keep going with every lead who went quiet until they book or say no.
Remind every booked homeowner so they show up, and rescue a missed
visit fast.
Chase every quote that has been sent until the homeowner decides.
You are not the closer. You never quote a price, never diagnose a
problem, and never invent a fact.

WHAT YOU MAY SEND
Only the exact approved messages, at the times listed. Nothing else
goes out automatically.
A person approves any new or changed message before a customer sees it.
Never send "just following up" or "just checking in". Every message
carries something useful: a next step, an answer, proof, or a clear
close.
Texts and calls come from [BUSINESS PHONE] only.
Offer only real open times from [CALENDAR]. Booking link: [BOOKING LINK].
Send nothing during quiet hours: [QUIET HOURS]. Every follow-up text
in this file respects them. The one exception is the booking agent's
first reply to a brand-new lead, which may go out at any hour.
Use the homeowner's preferred channel when one is on file.

CALLS
You work by text, email and alert. When the schedule says "a person
calls", create a call task for [CALLER NAME], send the call alert,
and wait. Send the "Just tried you" text only after that person's
call got no answer. The booking agent sends the alerts for the first
call. Never send a second alert for that call.

PUSH ALERTS TO YOUR TEAM
Every time a person must act, send a push alert to [SALES ALERT
LIST] through [ALERT CHANNEL], on top of the task:
- each later call on Ladder 1 or Ladder 2, and the no-show call on
  Ladder 3, when its call task is created
- the 1-day text on Ladder 1, when a person must fill in the times
- any reply on a ladder or a quote follow-up, or from a lead in
  Ghosted, except an opt-out
- a quote whose follow-up ends with no decision
Use only the words under "Alerts to your team". Alerts go to your
team, never to a homeowner. One alert per moment, never repeated.
Outside [ALERT HOURS], hold the alert and send it when alert hours
start. After a stop rule, send no more call alerts for that contact.
A contact on manual hold (tag: stop bot) gets no alerts at all.
If [ALERT CHANNEL] is "fallback": make each alert a task with the
same words, on the fallback list.

LEAD FOLLOW-UP
Ladder 1 starts after the booking agent's first reply. Ladder 2
starts at the booking agent's hand-off, when its bot hands the lead
to a person, so it never talks over the bot.
Ladder 1 ends with its 3-day text. Ladder 2 goes on with
one useful touch a week for four weeks. When a ladder ends with no
answer: move the lead to Ghosted and stop. No loops.

SHOW-UP REMINDERS (LADDER 3)
Starts when a visit is booked: tag booked, with Visit Date filled
from [CALENDAR]. Send only the Ladder 3 texts, at their times.
Skip any reminder whose time passed before they booked. If two
reminders would land within an hour of each other, send only the
later one.
The confirmation waits until quiet hours end. Skip any other
reminder that falls in quiet hours. Never send one late.
A reschedule (Visit Outcome: moved, with a new Visit Date) clears
the old reminders and starts Ladder 3 again.
The no-show rescue starts only when a person sets Visit Outcome to
"no-show". After 48 hours with no reply: move the lead to Ghosted
and stop.
A plain yes ("yes", "works", "ok", a thumbs up) keeps the reminders
going. Any other reply stops Ladder 3 and goes to a person, with the
reply alert. That person sends any later reminder by hand.
Ladder 3 ends when Visit Outcome is "held" or "cancelled".

QUOTE FOLLOW-UP
Starts only when Quote Sent At is filled. Separate from the lead
ladders. Four useful touches in the first nine days, then one each at
about one, two and three months.
When the three-month touch has gone out and there is still no
decision: send the quote-end alert, keep the quote open with its
owner, and stop.
Owner of open quotes: [SALES OWNER]. Backup: [BACKUP NAME].

FACTS YOU MAY REPEAT (never add to these)
Financing: [FINANCING YOU REALLY OFFER, OR "NONE"]
Common question after a quote: [REAL OBJECTION]
Approved answer: [APPROVED ANSWER]
Warranty: [EXACT WARRANTY FACTS]
Discounts: [WHO MAY APPROVE, LIMIT, END DATE]
Objection answers: only the approved words under "Short answers to
common objections". Use them only inside scheduled touches. A live
objection still goes to a person.
Never invent an approval, a rate, a monthly payment, a warranty, a
discount, a "spots are running out" claim, or a legal term. Financing
is an option, never a judgment about the homeowner. Same messages and
same timing for every homeowner. No pressure. No false urgency.

STOP AT ONCE WHEN
- the homeowner replies (any reply; except a plain yes to the visit
  time on Ladder 3, or a thumbs-up or "got it" to the first quote text)
- they book (tag: booked). This stops Ladders 1 and 2 and starts
  Ladder 3.
- they decide on the quote (won or lost), or cancel
- Ladder 3 only: Visit Outcome is set to held or cancelled
- they opt out or are marked do not disturb
- they fail the service or area check (tag: ai dq)
- a person puts the contact on manual hold (tag: stop bot)
Never talk over a live conversation.

HAND TO A PERSON WHEN
The reply is off-script, a correction, unclear, an objection, a
complaint, an unusual job, urgent, or a request for a person. Stop.
Create a task for [SALES OWNER] with the homeowner's exact words, and
send the reply alert. Send the homeowner nothing more. Any other reply
(for example "yes, Tuesday works") also stops the follow-up, goes to
[SALES OWNER] as a task, and sends the reply alert.
Never claim to be a person. If asked who is writing, hand over.
```

## Every message it sends

### Ladder 1: the lead left a phone number
The booking agent sends the first text at 0 seconds and promises a call from the same number. If you installed agent 1, it already builds the first three rows below. Do not build them twice. This agent adds the 1-day and 3-day texts, and the alert for the second call. After hours, agent 1 sends its after-hours text, and the first call is due when [PHONE HOURS] start; the rows below count from that call.

| When | What happens |
|---|---|
| 5 minutes in | A person calls, from the same number as the first text. |
| 5 minutes after that call is marked "no answer" | Text: "Just tried you! Easiest way to lock your [VISIT NAME]: [BOOKING LINK]" |
| 1 hour later | A person calls a second time. |
| 1 day later | Text: "Still want me to take a look at [THE PROBLEM THEY DESCRIBED]? I've got [DAY] morning or [DAY] afternoon open." |
| 3 days later | Text: "Closing out your request — want me to hold a spot or should I let it go?" |

The two [DAY] times must be real open times on your calendar. If your tool cannot fill them in by itself, make the 1-day text a task: a person fills in the two times and sends it.

### Ladder 2: the lead messaged you, then went quiet
The clock starts at the hand-off from the booking agent: the moment its bot hands the lead to a person. It never starts at the bot's first reply, so it never talks over the bot. Every time counts from that hand-off. Most tools count each wait from the step before, so set each wait as the gap between two rows.

| When | What happens |
|---|---|
| 5 minutes | A person calls. With agent 1 installed, this is the call task its hand-off creates, with its alerts. |
| 1 hour | Short text: confirm the problem they described and give the easiest next step. |
| 3 hours | Email: proof, a line that says you serve their area, and [BOOKING LINK]. |
| 24 hours | Text: one useful answer to a common question or objection. |
| 48 hours | A person calls. |
| Weeks 1 to 4 | One useful text each week. The fourth one closes out the request. |

Use the channel the lead wrote in on. A call or a text needs a phone number. The email needs an email address. Skip any step you have no details for. Facebook and Instagram limit how long after a customer's last message a business may write back. Your AI assistant checks the current limit before it builds the later touches.

These texts and the email have no fixed words. They are written and approved in step 7.

### Ladder 3 — Booked: get them to show up
It starts when the visit is booked. Most times count back from the visit's date and time. Agent 1 sends no booking confirmation, so this ladder owns it. A person approves these words in step 7 before any homeowner sees them.

| When | What happens |
|---|---|
| 5 minutes after booking | Text: "Hi [FIRST NAME], it's [BUSINESS NAME]. You're booked for your [VISIT NAME] on [DATE] at [TIME]. Does that time still work?" |
| 2 days before the visit | Text: "Before your [VISIT NAME], here's a recent job we finished nearby. We'll look at [THE PROBLEM THEY DESCRIBED] and walk you through the next step." Attach one before-and-after photo. |
| The day before | Text: "Quick reminder: your [VISIT NAME] is tomorrow at [TIME]. If anything changed, just reply here." |
| Morning of the visit | Text: "Your [VISIT NAME] is today at [TIME]. If anything changed, reply here and we'll find a new time." |
| 1 hour before | Text: "See you in about an hour. Keep an eye out for [BUSINESS PHONE]." |
| A person sets Visit Outcome to "no-show" | Text: "Hi [FIRST NAME], we're ready for your [VISIT NAME]. Is now still a good time?" Then a person calls right away. |
| 5 minutes after that call is marked "no answer" | Text: "Tried to reach you for your [VISIT NAME]. Life happens. Want to pick a new time? [BOOKING LINK]" |
| The next day | Text: "Still want help with [THE PROBLEM THEY DESCRIBED]? Happy to find you a new time this week: [BOOKING LINK]" |
| 48 hours after the no-show, no reply | Move the lead to Ghosted and stop. |

Stop rules for this ladder:
- A plain yes to the visit time ("yes", "works", "ok", a thumbs up) keeps the reminders going.
- Any other reply, a cancel, or STOP ends the automatic texts. The reply goes to a person with the "Booked homeowner replied" alert.
- After that, the person sends any later reminder by hand, from the same number.
- A reschedule (Visit Outcome: moved) clears the old reminders and starts this ladder again for the new Visit Date.
- Never text during [QUIET HOURS]. The 5-minute text waits until they end; any other reminder that falls inside them is skipped.
- Skip a reminder whose time passed before they booked. If two would land within an hour, send only the later one.

Words a person may send when they reply:
- If the time works: "Great. We'll reach you from this number. Before then, what's the main thing you want us to look at?"
- If it doesn't: "No problem. What works better: morning, afternoon or evening?"
- If your calendar sends invites: "I just sent the calendar invite. Can you accept it now so it doesn't get lost?"

If you have no booking link, end those texts with "Reply with a time that works." instead.

### Quote follow-up
The clock starts when the quote is sent; set each wait as the gap between two rows (for example: 48 hours, then 3 more days to reach day 5).

| When | Sent as | Message |
|---|---|---|
| Right away | The rep who wrote the quote | "Just sent the proposal for [PROJECT]. Can you give me a quick thumbs-up when it lands? That way I know the photos and options came through." |
| 48 hours | Sales owner | "One question that comes up after this [VISIT NAME] is [REAL OBJECTION]. The short answer is [APPROVED ANSWER]. If payment timing is the concern, I can also send the financing options we actually offer." |
| Day 5 | Sales owner | "This nearby [PROJECT TYPE] had a similar [PROBLEM]. Here's the before/after and what changed. Want me to walk through how it compares with your home?" Attach the photo. |
| Days 6 to 9 | Sales owner | "I don't want to clutter your phone. Should I keep this open, revisit it in [MONTH], or close it out? Any answer is fine." |
| About 1 month | Owner of old quotes | New proof, or a useful seasonal reason to look again. |
| About 2 months | Owner of old quotes | A similar finished job, a financing update, or a scheduling update. |
| About 3 months | Owner of old quotes | A last check that asks permission to stay in touch. |

Cut the financing sentence from the 48-hour text if you offer no financing. [MONTH] is a later month you pick when you approve this text in step 7. The last three touches have no fixed words. They are written and approved in step 7.

### Short answers to common objections
Your rep uses these when replying by hand. Your AI assistant may use them in the scheduled texts it drafts in step 7. Examples are Ladder 2's 24-hour text and the 48-hour quote text. A person approves the words first. A live objection still goes to a person. The agent never answers one by itself.

| They say | A short answer |
|---|---|
| "That's more than I expected." (after the quote) | "Fair. Is it the total, or the timing of the payment? If it's timing, I can send the financing options we actually offer." |
| "I need to think about it." | "Totally fair. What part are you still unsure about: the problem, the timing, or the cost?" |
| "We're getting other quotes." | "Smart. When you compare, check what each quote covers. Want me to walk you through ours line by line?" |
| "I need to talk to my spouse." | "Of course. Want [REP NAME] to walk you both through it? Pick a time that works for both of you: [BOOKING LINK]" |
| "Now's not a good time." | "No problem. Should I check back later this week, or later in the month?" |

Before the visit, a price question gets agent 1's approved price line (its "Common questions" rules). This file has no price answer of its own. Cut the financing sentence if you offer no financing. One question per answer. No pressure, no false urgency, and no fact that is not in your approved facts.

### Alerts to your team
These go to [SALES ALERT LIST] through [ALERT CHANNEL], never to a homeowner, with the blanks filled from the contact's record. Outside [ALERT HOURS], an alert waits until they start.

| When | Alert |
|---|---|
| A call task is created on Ladder 1 or Ladder 2, or for a no-show on Ladder 3. Skip the first call: agent 1 already alerts for it. | "Follow-up call due" |
| Ladder 1's 1-day text is a task, because your tool cannot fill in open times | "Text due" |
| A quiet lead replies, during a ladder or after it ended in Ghosted (any reply except an opt-out) | "Quiet lead replied" |
| A homeowner with an open quote replies (any reply except an opt-out) | "Quote reply" |
| The three-month quote touch has gone out with no decision | "Quote follow-up ended" |
| A booked homeowner replies to a Ladder 3 text (any reply except an opt-out) | "Booked homeowner replied" |

**The "Follow-up call due" alert.**

```
Follow-up call due:
[NAME],
[JOB].
Call now from the business line: [PHONE].
```

**The "Text due" alert.**

```
Text due:
[NAME],
[JOB].
Pick two real open times and send the 1-day text from the task.
```

**The "Quiet lead replied" alert.**

```
Quiet lead replied:
[NAME],
[JOB].
They said: '[THEIR WORDS]'.
Reply to them now, from the business number.
```

**The "Quote reply" alert.**

```
Quote reply:
[NAME],
[PROJECT].
They said: '[THEIR WORDS]'.
Reply to them now, from the business number.
```

**The "Quote follow-up ended" alert.**

```
Quote follow-up ended, no decision:
[NAME],
[PROJECT],
[QUOTE AMOUNT].
Set a next date or close it with a reason.
```

**The "Booked homeowner replied" alert.**

```
Booked homeowner replied:
[NAME],
[VISIT NAME] on [DATE] at [TIME].
They said: '[THEIR WORDS]'.
Reply to them now, from the business number.
```

Each one is a team alert, your AI may adjust the wording. If you use the fallback, each alert is a task with these same words, on the fallback list.

## Test list
Use only your own test contact and made-up quotes, with only you on [SALES ALERT LIST]. With the fallback, "alert lands" reads "a task with the same words shows on the fallback list".

1. **Quiet lead with a phone number.** Never reply. Pass: every Ladder 1 step fires once, in order. Call tasks land with the named person, once each. The first call carries only agent 1's new-lead alert; the second call brings one "Follow-up call due" alert.
2. **Quiet lead from a message.** Message your page, answer the bot until it hands you to a person, then never reply. Pass: nothing from Ladder 2 arrives while the bot is still talking. Ladder 2 starts at the hand-off and runs in order with four weekly texts, the lead ends in Ghosted, and nothing repeats. The 5-minute call carries only agent 1's alert; the 48-hour call brings one "Follow-up call due" alert. Then reply once. Pass: one "Quiet lead replied" alert lands, and nothing sends to the contact.
3. **Reply mid-ladder.** Pass: nothing else sends to the contact. One "Quiet lead replied" alert lands with your exact words, and the sales owner gets a task.
4. **Booking mid-ladder.** Pass: the `booked` tag cancels every Ladder 1 and Ladder 2 branch and starts Ladder 3. No more lead call alerts come.
5. **Opt-out.** Pass: nothing more sends, and no alert comes.
6. **Wrong area or wrong service.** Pass: the ladder stops.
7. **Manual hold.** Add `stop bot`. Pass: nothing sends while a person is in the conversation, and no alert comes.
8. **Quote sent.** Fill Quote Sent At. Pass: the first quote text goes out. With the field empty, nothing starts.
9. **Financing question.** Reply asking about monthly payments. Pass: the follow-up stops and the sales owner gets a task. No rate or payment is invented.
10. **Objection.** Reply with a pushback on price. Pass: it goes to a person. The agent does not answer.
11. **Won.** Pass: every quote message stops.
12. **Lost.** Pass: the reason is recorded and every message stops.
13. **Quote reply.** Fill Quote Sent At, then reply to the first quote text. Pass: the quote messages stop, and one "Quote reply" alert lands with your exact words.
14. **Quote ends with no decision.** Fill Quote Sent At and never reply or decide. Pass: after the three-month touch, one "Quote follow-up ended" alert lands. The quote stays open with its owner. Nothing more sends.
15. **Outside alert hours.** Set [ALERT HOURS] to start a few minutes from now, then reach Ladder 1's second call. Pass: its alert waits and lands when alert hours start, once. Put the real hours back.
16. **Fallback only.** If [ALERT CHANNEL] is "fallback", rerun test 3. Pass: the alert shows as a task with the same words, on the fallback list.
17. **Booked: reminders.** Book a test visit a short time out, with the reminder times shortened. Pass: the confirmation, proof, day-before, morning-of and 1-hour texts each land once, in order.
18. **Booked during quiet hours.** Pass: the confirmation waits until quiet hours end. No text lands inside [QUIET HOURS].
19. **Booked for later today.** Pass: reminders whose time has passed are skipped. Two reminders within an hour send only the later one.
20. **Reply to a reminder.** Reply "yes" to the confirmation. Pass: the reminders keep coming and no alert goes out. Then reply "can we do Thursday instead?". Pass: the automatic texts stop, and one "Booked homeowner replied" alert lands with your exact words.
21. **Cancel, reschedule or STOP.** Pass: a cancel (Visit Outcome: cancelled) or STOP ends every reminder, and STOP brings no alert. A reschedule (Visit Outcome: moved) clears the old reminders and starts them again for the new time, once.
22. **No-show.** Set the test visit's Visit Outcome to "no-show". Pass: the "we're ready" text goes and one call task brings one "Follow-up call due" alert. Mark the call "no answer". Pass: the new-time text goes, then the next-day text. With no reply, the lead lands in Ghosted after 48 hours and nothing more sends.

## When a person takes over
- The scheduled calls, each a task with a push alert.
- Every push alert. The person who picks it up does the one thing it says, from the business line, then closes the task.
- An alert that never arrived, came twice, or went to the wrong person. A person fixes the alert step, and the daily check catches anything missed.
- Any reply that is off-script: a correction, an unclear answer, an objection, a complaint or an unusual job.
- The homeowner asks for a person, or the matter is urgent.
- A booked homeowner replies to a reminder, or misses the visit. The rep sets Visit Outcome on each visit the same day: held, no-show, cancelled or moved.
- The agent did not respond, repeated itself, or said the wrong thing.
- The follow-up ends with no decision. The quote owner sets a next date or closes the file with a reason.
- Any new or changed message. A person approves it before a customer sees it.

**Replying vs taking over.** A reply alert means a person answers by hand. If the lead is stuck, upset or slipping away, run the takeover play instead. It lives only in agent 1, section "When a person takes over": call first, then text, then log it in the data agent's Failure Log.

One takeover is good service. Three alike means the message or the rule needs fixing, not the lead.

Want this installed for you? That is the Full Done-For-You Installation.
