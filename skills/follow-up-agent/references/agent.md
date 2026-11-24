# Install your follow-up agent
**Jobs-On-Demand Flywheel Kit · Sales · agent 2 of 5**

> This agent keeps going with every lead who went quiet until they book or say no, chases every quote your rep sends until the homeowner decides, and alerts your sales team on their phones every time a person should act.

## What this agent does
- Follows up every quiet lead and sends push alerts to sales team to follow up with every lead.
- It still follows up every sent quote: a separate follow-up starts the moment a quote is sent and runs until the homeowner decides.
- Follows up with a quiet lead on a set clock, by text and email (Ladder 1 and Ladder 2 below).
- Creates a call task for your team at the right moments, and sends a push alert with it. This agent works by text, email and alert.
- Sends a push alert the moment a quiet lead or a quoted homeowner replies, and when a quote's follow-up ends with no decision.
- Stops the second the homeowner replies, books, decides or opts out. It never talks over a live conversation.
- Never sends "just following up". Every message carries something useful: a next step, an answer, proof, or a clear close.

## What you need before you start
- **Your customer tool (CRM), with automations.** It must keep fields, tags and stages on each contact, wait a set time, send a text or an email, and create a task for a person. Your AI assistant needs access to it, or it walks you through each click.
- **An approved business texting line,** and one number that sends both calls and texts. Check this first.
- **A real calendar and booking link** with true open times ([CALENDAR] and [BOOKING LINK]). Fake time slots kill trust.
- **Your booking agent (agent 1 of 5).** It sends the first reply, asks the intake questions and builds the first calls and their alerts. This agent picks up after.
- **A named owner for open quotes ([SALES OWNER]), and a backup ([BACKUP NAME]).**
- **Your approved facts:** [FINANCING YOU REALLY OFFER, OR "NONE"], the [REAL OBJECTION] homeowners raise after a quote and your [APPROVED ANSWER], your [EXACT WARRANTY FACTS], and your discount rules ([WHO MAY APPROVE, LIMIT, END DATE]).
- **Proof:** before-and-after photos of finished local jobs.
- **Push alerts to your team's phones,** sent by an automation: your customer tool's phone app notice, a text, or your team's chat app. Fallback: each alert becomes a task with the same words, on a daily list a named person reads every morning. Then your team learns of a reply or a due call only when they open the list.
- **From MY-NUMBERS.md:** [ALERT CHANNEL], [SALES ALERT LIST], [ALERT HOURS], [QUIET HOURS] and [CALLER NAME].
- **One test contact you own:** your own phone number and email.

## How to install it
If you already pasted the prompt in START-HERE.md, skip this one. To install this agent by itself, give this file and MY-NUMBERS.md to your AI assistant (Claude, ChatGPT or similar). Then paste this:

```
Act as my implementation manager. Install the follow-up agent in this
file inside the customer tool I already use. Ask me which one first,
and use its names for things. Build every field, tag, message and
automation in draft. Use only my own test contact. Ask me for any business
fact you do not have. Never make one up. Show me every new message for
approval before a customer can see it. Do not turn on customer messaging
until every test passes, every "Done when" before the turn-on step
passes, and I say yes.
```

## Step by step
1. `You` **Gather your facts.** Collect everything under "What you need" and every blank in the instructions below.
   Done when: your AI assistant has every fact and no blank is left.
2. `You` **Check the texting line.** Confirm the line is approved to send, and calls and texts use one number.
   Done when: a text sent from the business line lands on your own phone.
3. `AI` **Create the fields, tags and stages.** Fields: Quote Sent At, Quote Amount, Decision Status (pending, won or lost), Lost Reason, Financing Discussed, Next Follow-up (date and owner). Tags: `booked`, and `stop bot` (a person has taken over; this is the manual hold). Both already exist if you installed agent 1. Stages: Ghosted for leads (already on the agent 1 board); Quote Sent, Decision Pending, Won and Lost for quotes, on their own board.
   Done when: every field, tag and stage exists and an automation can read it.
4. `AI` **Build the follow-up for leads who left a phone number.** Use Ladder 1 below. If you installed agent 1, its "Form lead fast reply" automation already sends the first text, both call tasks and the "Just tried you" text. Do not build those twice. Add only the 1-day and 3-day texts, in the same automation or in one that starts where it ends. Each call is a task for a person.
   Done when: the automation sits in draft with every wait, text and call task in order, and no step is built in both agents.
5. `AI` **Build the follow-up for leads who messaged you.** Use Ladder 2 below, and the channel rule under it. If you installed agent 1, its hand-off already creates the 5-minute call task. Do not build it again.
   Done when: the automation sits in draft with every step in order, and no call task is built in both agents.
6. `You + AI` **Write the messages that have no fixed words.** Ladder 2's texts and email, the four weekly texts and the later quote touches are described below, not scripted. Your AI assistant drafts each from your facts; a person approves each.
   Done when: every message has approved words and no blank.
7. `AI` **Build the quote follow-up.** It starts only when Quote Sent At is filled. Keep it separate from the lead ladders.
   Done when: filling Quote Sent At on your test contact starts it, and nothing else does.
8. `AI` **Wire the stop rules into every branch.** Use the "Stop at once when" list in the instructions.
   Done when: every branch has an owner and a stop rule. The test results come in step 12.
9. `You + AI` **Set up how alerts reach your team.** If you did this in agent 1 (its step 10), keep those settings and go to the "Done when". If not, fill in [ALERT CHANNEL], [SALES ALERT LIST] and [ALERT HOURS]. If no automation in your tools can send to a phone by itself, write "fallback" as [ALERT CHANNEL] and name the person who reads the daily list.
   Done when: one test alert, sent by an automation to your own phone, lands there. Or, with the fallback: a test alert task shows on the list, and its reader is named.
10. `AI` **Add the push alerts.** Add an alert step at each moment under "Alerts to your team", in that moment's automation, on top of the task, never instead of it.
    - **One call task, one alert.** Agent 1 owns the alerts for the first call (its new-lead alert and its 5-minute "Still not called" alert). Never add an alert to that call task. Ladder 1's second call is built in agent 1 with no alert: add "Follow-up call due" to it. Every call task this agent builds gets "Follow-up call due".
    - **Replies from Ghosted:** a small automation of its own. It starts on any reply from a contact in Ghosted, creates a task for [SALES OWNER] with their words, and sends the reply alert.
    Done when: every call task on both ladders, the 1-day text task (if you made one), every reply branch (including Ghosted) and the end of the quote follow-up each carry exactly one alert step, in draft.
11. `You` **Name the owners.** Every open quote gets one owner and a next follow-up date. A quote stays "pending" only when it has both. A lost quote gets one reason from this list: price or budget; financing unavailable or declined; timing or not ready; chose a competitor; decision-makers not agreed; scope or service mismatch; trust or proof concern; could not reach after the full follow-up; solved it another way; duplicate or invalid. Add a short note of what the homeowner said and the date. Never write only "bad lead".
    Done when: every open quote shows a stage, an owner and a next date.
12. `You + AI` **Run the test list.** You play the homeowner from your own phone. Shorten every wait to a minute or two and set [SALES ALERT LIST] to only you; put both back after. Your AI assistant checks the tags, stages and fields.
    Done when: every test passes, no real customer got a test message, and no team member got a test alert.
13. `You` **Teach the team the takeover play, then turn it on.** Delete the test contacts first. Show everyone on [SALES ALERT LIST] the play under "When a person takes over" and what each alert asks.
    Done when: every team member can run the play without looking it up, and the automations are live.
14. `You` **Set the check.** Daily: clear quotes with no owner and overdue follow-ups. With the fallback, also clear every alert task still open. Weekly: look at quotes that are 2, 7 and 30 days old.
    Done when: one named person owns that check.

## The agent's instructions
These are the rules every automation in this file must follow. Your AI assistant builds them into steps 4 to 10.

```
You are the follow-up agent for [BUSINESS NAME], a [TRADE] company.

YOUR JOB
Keep going with every lead who went quiet until they book or say no.
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
Send nothing during quiet hours: [QUIET HOURS]. Use the homeowner's
preferred channel when one is on file.

CALLS
You work by text, email and alert. When the schedule says "a person
calls", create a call task for [CALLER NAME], send the call alert,
and wait. Send the "Just tried you" text only after that person's
call got no answer. The booking agent sends the alerts for the first
call. Never send a second alert for that call.

PUSH ALERTS TO YOUR TEAM
Every time a person must act, send a push alert to [SALES ALERT
LIST] through [ALERT CHANNEL], on top of the task:
- each later call on Ladder 1 or Ladder 2, when its call task is created
- the 1-day text on Ladder 1, when a person must fill in the times
- any reply on a lead ladder or a quote follow-up, or from a lead in
  Ghosted, except an opt-out
- a quote whose follow-up ends with no decision
Use only the words under "Alerts to your team". Alerts go to your
team, never to a homeowner. One alert per moment, never repeated.
Outside [ALERT HOURS], hold the alert and send it when alert hours
start. After a stop rule, send no more call alerts for that contact.
A contact on manual hold (tag: stop bot) gets no alerts at all.
If [ALERT CHANNEL] is "fallback": make each alert a task with the
same words, on the daily list.

LEAD FOLLOW-UP
Starts after the booking agent's first reply. Follow Ladder 1 or
Ladder 2. Ladder 1 ends with its 3-day text. Ladder 2 goes on with
one useful touch a week for four weeks. When a ladder ends with no
answer: move the lead to Ghosted and stop. No loops.

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
Never invent an approval, a rate, a monthly payment, a warranty, a
discount, a "spots are running out" claim, or a legal term. Financing
is an option, never a judgment about the homeowner. Same messages and
same timing for every homeowner. No pressure. No false urgency.

STOP AT ONCE WHEN
- the homeowner replies (any reply)
- they book (tag: booked)
- they decide on the quote (won or lost), or cancel
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
The clock starts at the booking agent's first reply; every time counts from that start. Most tools count each wait from the step before, so set each wait as the gap between two rows.

| When | What happens |
|---|---|
| 5 minutes | A person calls. With agent 1 installed, this is the call task its hand-off creates, with its alerts. |
| 1 hour | Short text: confirm the problem they described and give the easiest next step. |
| 3 hours | Email: proof, a line that says you serve their area, and [BOOKING LINK]. |
| 24 hours | Text: one useful answer to a common question or objection. |
| 48 hours | A person calls. |
| Weeks 1 to 4 | One useful text each week. The fourth one closes out the request. |

Use the channel the lead wrote in on. A call or a text needs a phone number. The email needs an email address. Skip any step you have no details for. Facebook and Instagram limit how long after a customer's last message a business may write back. Your AI assistant checks the current limit before it builds the later touches.

These texts and the email have no fixed words. They are written and approved in step 6.

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

Cut the financing sentence from the 48-hour text if you offer no financing. [MONTH] is a later month you pick when you approve this text in step 6. The last three touches have no fixed words. They are written and approved in step 6.

### Alerts to your team
These go to [SALES ALERT LIST] through [ALERT CHANNEL], never to a homeowner, with the blanks filled from the contact's record. Outside [ALERT HOURS], an alert waits until they start.

| When | Alert |
|---|---|
| A call task is created on Ladder 1 or Ladder 2 (each call row in both tables, except the first call agent 1 already alerts for) | See alert 1 below |
| Ladder 1's 1-day text is a task, because your tool cannot fill in open times | See alert 2 below |
| A quiet lead replies, during a ladder or after it ended in Ghosted (any reply except an opt-out) | See alert 3 below |
| A homeowner with an open quote replies (any reply except an opt-out) | See alert 4 below |
| The three-month quote touch has gone out with no decision | See alert 5 below |

**Alert 1.**

```
Follow-up call due:
[NAME],
[JOB].
Call now from the business line: [PHONE].
```

**Alert 2.**

```
Text due:
[NAME],
[JOB].
Pick two real open times and send the 1-day text from the task.
```

**Alert 3.**

```
Quiet lead replied:
[NAME],
[JOB].
They said: '[THEIR WORDS]'.
Reply now in the same conversation.
```

**Alert 4.**

```
Quote reply:
[NAME],
[PROJECT].
They said: '[THEIR WORDS]'.
Reply now in the same conversation.
```

**Alert 5.**

```
Quote follow-up ended, no decision:
[NAME],
[PROJECT],
[QUOTE AMOUNT].
Set a next date or close it with a reason.
```

Each one is a team alert, your AI may adjust the wording. If you use the fallback, each alert is a task with these same words, on the daily list.

## Test list
Use only your own test contact and made-up quotes, with only you on [SALES ALERT LIST]. With the fallback, "alert lands" reads "a task with the same words shows on the daily list".

1. **Quiet lead with a phone number.** Never reply. Pass: every Ladder 1 step fires once, in order. Call tasks land with the named person, once each. The first call carries only agent 1's new-lead alert; the second call brings one "Follow-up call due" alert.
2. **Quiet lead from a message.** Give a phone number, then never reply. Pass: Ladder 2 runs in order with four weekly texts, the lead ends in Ghosted, and nothing repeats. The 5-minute call carries only agent 1's alert; the 48-hour call brings one "Follow-up call due" alert. Then reply once. Pass: one "Quiet lead replied" alert lands, and nothing sends to the contact.
3. **Reply mid-ladder.** Pass: nothing else sends to the contact. One "Quiet lead replied" alert lands with your exact words, and the sales owner gets a task.
4. **Booking mid-ladder.** Pass: the `booked` tag cancels every branch. No more call alerts come.
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
16. **Fallback only.** If [ALERT CHANNEL] is "fallback", rerun test 3. Pass: the alert shows as a task with the same words, on the daily list.

## When a person takes over
- The scheduled calls, each a task with a push alert.
- Every push alert. The person who picks it up does the one thing it says, from the business line, then closes the task.
- An alert that never arrived, came twice, or went to the wrong person. A person fixes the alert step, and the daily check catches anything missed.
- Any reply that is off-script: a correction, an unclear answer, an objection, a complaint or an unusual job.
- The homeowner asks for a person, or the matter is urgent.
- The agent did not respond, repeated itself, or said the wrong thing.
- The follow-up ends with no decision. The quote owner sets a next date or closes the file with a reason.
- Any new or changed message. A person approves it before a customer sees it.

**The takeover play:**
1. Add the `stop bot` tag first. A person and the agent must never message the same homeowner at once.
2. Reply from the same business number.
3. Log it: the date, what the agent did, what the homeowner said, and whether the lead was saved.

One takeover is good service. Three alike means the message or the rule needs fixing, not the lead.

Want this installed for you? That is the Full Done-For-You Installation.
