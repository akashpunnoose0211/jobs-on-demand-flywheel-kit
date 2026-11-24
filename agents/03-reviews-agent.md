# Install your reviews agent
**Jobs-On-Demand Flywheel Kit · Brand · agent 3 of 5**

> After every finished job, this agent checks the customer is happy, asks happy customers for an honest review and a referral, hands every problem to a person, and alerts your team the moment a person needs to act.

## What this agent does
Checks in after every finished job, then asks happy customers for a review, and sends push alerts to sales team to follow up with every customer for a review.

- Sends a check-in the next business day after a job is finished.
- Sorts the answer four ways: happy, has a question, unhappy, or no reply.
- Sends a question or complaint to a person. That customer gets no review link.
- Asks happy customers for an honest review, with one reminder, and offers your referral reward as a separate thing.
- Sends past customers a useful reminder when there is a real reason, and stops the moment they say stop.
- Alerts your sales team for every happy customer with no review after the reminder, so a person follows up. Alerts at once when a customer is unhappy, and wherever else a person must act.

"Every customer" here means every happy customer, and every customer whose problem a person has marked fixed. An unhappy customer gets a person and a fix first, never a review ask.

## What you need before you start
- **A customer record tool (a CRM) that can do two things:** mark a job as truly complete, and send texts. Any CRM that does both works.
- **A business texting line that is approved to send.** Until your phone carrier has approved the line, no automatic text will go out.
- **Three named people:** one who owns customer experience, one backup, and one production contact for open problems.
- **Push alerts to your team's phones,** sent by an automation: your customer tool's own phone app notice, a text to the team member, or your team's chat app. From MY-NUMBERS.md: [ALERT CHANNEL], [SALES ALERT LIST] (who gets review follow-up alerts) and [ALERT HOURS]. The customer experience owner and the backup must also be reachable on [ALERT CHANNEL]. **Fallback,** if none can: a task for the named person plus a daily list of open alert tasks. Then nothing reaches a phone; a person sees an alert only when they open the list.
- **Your [DIRECT REVIEW LINK]** on Google, plus any other review sites you approve.
- **Your approved referral reward:** what it is ([APPROVED THIRD-PARTY REWARD], written [APPROVED REWARD] in the messages), what earns it ([APPROVED TRIGGER]), the limit, the end date, who delivers it, and who accounts for it. The card in step 5 holds it.
- **[CALL-FIRST JOBS]:** the high-ticket or complicated jobs that get a check-in call from a person instead of a text.
- **Your own test contact.** Your own phone number, saved as a contact. Every test uses this and nothing else.
- **Three finished jobs** to pilot on before you roll this out to every crew.

Do not set a review or referral target yet. First get the asks going out reliably. Then measure your own numbers.

## How to install it
To install this agent alone, type **"install my reviews agent"**, or use the paste prompt at the end of `INSTALL-GUIDE.md`.

## Step by step

**1. Add the fields and stages. `You + AI`**
Add these fields to each job record:

| Field | What goes in it |
|---|---|
| Job Completed At | The checked date and time |
| Completion Owner | The person who answers for the job |
| Quality Status | happy / unresolved / unhappy / unreachable |
| Issue Owner | The person fixing the problem |
| Review Requested At | Date and time |
| Review Completed | yes / no / unknown |
| Referral Offered | The exact approved program |
| Referral Source Customer | The record ID of the customer who referred |
| Next Reminder Date | The next past-customer message this person agreed to |

Add these eight stages, in this order: Work Complete, Quality Check Due, then Happy, Unresolved or Unhappy, then Recovery Open (a problem) or Ready to Ask (a happy customer), then Closed. You name the owner, the backup and the production contact.
Done when: every field and stage exists, and the owner, the backup and the production contact are named. From here on, no finished job closes without a quality status and one owner.

**2. Build the next-business-day check-in. `You + AI`**
The AI builds the check-in message and the four routes below. You pick [CALL-FIRST JOBS]: they get a call from a person instead.

| Customer's answer | What happens |
|---|---|
| Happy, all done | Moves to Ready to Ask |
| Has a question, something open | A person owns it, with a dated next step |
| Unhappy, complaint | Every review, referral and promo ask stops. Recovery opens. |
| No reply | One respectful second try, then leave the door open |

The agent sorts only after the customer answers. A person, not the AI, decides when a complaint is fixed.
Done when: all four test answers from your own test contact land on the right route, and the unhappy route sends no ask.

**3. Build the problem guard. `You + AI`**
When Quality Status turns to unresolved or unhappy:

1. Name one person as owner right away.
2. Acknowledge the exact concern. Do not argue. Do not diagnose by message.
3. Set the next contact or visit time.
4. Log what was promised and who promised it.
5. Check with the customer after the fix.
6. Only a person can mark it resolved. A ticked-off office task does not release the review ask.

Done when: a test complaint pauses every promotional message, and they stay paused until a person marks it resolved.

**4. Install the review ask and one reminder. `You + AI`**
You supply the direct review link. The AI builds the ask and the reminder, both in draft. They go only to customers on the happy route, or after a person has confirmed a problem is fixed. A person sets Review Completed to yes when the review shows up, unless your tool can see your reviews by itself.
Done when: your happy test contact and your unresolved test contact get different behavior, and the direct link opens the review page.

**5. Install the referral reward. `You + AI`**
Pick a third-party reward the customer values, not another discount on work they just bought. Keep it easy to explain and safe for your budget. Fill in this card:

```text
REFERRAL PROGRAM
Customer who refers gets: [APPROVED THIRD-PARTY REWARD]
What earns it: [REFERRED PERSON BOOKS or BUYS - PICK ONE]
New customer gets: [APPROVED OFFER or NONE]
Services and area it covers: [FACT]
Most rewards allowed: [LIMIT]
Ends: [DATE or NONE]
Owner: [NAME]
Tracking: referring customer's record ID + referral code
Review needed: NONE
```

Give each referring customer a referral code. The AI makes the referral link or card that carries the code. The referral message sends it. The AI tracks the referring customer, the referred person, whether they qualified, booked and bought, the reward owed and the reward delivered. Never promise a reward nobody can deliver.
Done when: one test referral runs the full path without making a duplicate contact or a duplicate reward.

**6. Install the past-customer messages. `You + AI`**
These are useful reminders, not a blast you send when the schedule is empty. Pick the groups that fit your trade:

- A seasonal check or maintenance visit is due.
- A past job with a real related need.
- A warranty or service anniversary.
- A past customer in an area where you are now working.
- A customer who asked you to come back after a date.

Do not hint at a new problem you cannot know about. Do not make up urgency. Only message people you have a lawful reason to contact, and always give a way to opt out.
Done when: every group has a reason, an owner, an exact message, a source tag and a stop rule.

**7. Add the source tags. `AI`**
Tag every new inquiry so the data agent (agent 5) can trace it back to the finished job:

- `post-job-review`
- `customer-referral-[CODE]`
- `past-customer-reactivation-[CAMPAIGN]`

Done when: a test referral and a test past-customer reply each show up with the correct source.

**8. Build the team alerts. `You + AI`**
If you set up alerts in agent 1 (its step 10), keep those settings. The AI builds one automation per alert under "Alerts to your team", sent to the person named there. When each fires is in ORDER OF WORK in the instructions. Alert A waits the same 3 to 5 days after the reminder that the reminder waited after the ask. Alert B fires the moment Quality Status turns to unhappy. With the fallback, each alert is a task for the same person, on a daily list with a named checker.
Done when: an alert marked TEST reaches every person on [SALES ALERT LIST], the customer experience owner and the backup (with the fallback: a task for each, on the daily list).

**9. Run the test list. `You + AI`**
The list is below. Shorten the waits to a minute or two, and point every alert at your own phone. Put the real waits and people back after.
Done when: every test passes and no test message reaches a real customer.

**10. Approve, pilot, then keep watch. `You`**
A person approves every message before a customer sees it. Run the full loop on three finished jobs before you roll it out to every crew. Then:

- Daily: every finished job has a quality status and one owner. Unresolved and unhappy jobs are visible, and their asks are paused.
- Daily: every alert sent has a person who acted on it, logged on the record. With the fallback, the named person works the daily list.
- Weekly: check five finished jobs from check-in through source tag.
- Weekly: referral rewards owed match rewards delivered.

Done when: three pilot jobs have run cleanly, every alert they raised reached the right person, and the daily and weekly checks have an owner.

## The agent's instructions
If your tool has an assistant that can read customer replies, paste these into it. If not, the automations send the approved messages and a person sorts each reply by the same four routes. Either way, the alerts are the step 8 automations, and they fire when Quality Status is set.

```text
You are the reviews agent for [COMPANY], a [TRADE] business in
[SERVICE AREA]. You work by text only.

YOUR JOB
After a job is marked complete, check the customer is happy. Ask
happy customers for an honest review and offer the referral reward.
Send every question and complaint to a person. Send a team alert
every time a person needs to act.

FACTS
Customer experience owner: [NAME]
Backup: [NAME]
Production contact for open problems: [NAME]
Direct review link: [DIRECT REVIEW LINK]
Referral reward: [APPROVED THIRD-PARTY REWARD]
What earns it: [APPROVED TRIGGER]
Jobs that get a call from a person, not a text: [CALL-FIRST JOBS]
How alerts reach phones: [ALERT CHANNEL]
Review follow-up alerts go to: [SALES ALERT LIST]
Alerts may go out during: [ALERT HOURS]

ORDER OF WORK
1. The next business day after Job Completed At, send the check-in.
   For [CALL-FIRST JOBS], send no text. Send alert D (check-in call due).
2. Wait for the answer. Sort only after the customer replies.
   - Happy or complete: set Quality Status to happy.
   - Question or something open: set unresolved. Assign the owner
     with a dated next step. Stop all asks. Send alert C (open
     question).
   - Complaint: set unhappy. Stop every review, referral and promo
     message. Open recovery. Send alert B (unhappy customer) at once.
   - No reply: send alert E (no reply to the check-in). A person
     approves one respectful second try or makes a call. If that
     gets no reply, set unreachable, send alert F (unreachable),
     and leave the door open.
3. To happy customers only, send the review ask. Send one reminder
   3 to 5 days later. Never send a second reminder.
4. Wait the same 3 to 5 days after the reminder. If Review
   Completed is still not yes and no stop applies, send alert A
   (review follow-up) to [SALES ALERT LIST]. Then send that
   customer no more review messages. A person follows up and logs
   it.
5. Offer the referral reward as its own message. Never put it in
   the review ask. When a referral meets the trigger, log the
   reward as owed and send alert G (referral reward owed).
6. Send past-customer messages only to an approved group with a
   real reason.

TEAM ALERTS
- Use only the wording in "Alerts to your team" (A to H), blanks
  filled from the record. Team only, never a customer.
- Once per customer per event. Where a step 8 automation sends the
  alert when a status is set, setting the status is the send.
- A stop on a customer stops messages to them and alert A. It never
  stops alerts B to H.
- Outside [ALERT HOURS], hold the alert until they start.
- No phone channel: a task for the same person, on the daily list.

RULES
- Ask for an honest review. Never ask for a positive or five-star
  review.
- Never offer money, discounts, gifts or the referral reward for a
  rating or a public review.
- Never hide or block a bad review. A person fixes the problem and
  the customer's choice stays theirs.
- Never decide by yourself that a complaint is fixed. Only a person
  marks it resolved, after checking with the customer.
- Never argue. Never diagnose a problem by message.
- Never promise a reward that is not in the approved program.
- Never hint that a past customer has a new problem.
- Stop all messages to a customer on any of these: review done,
  opt-out, do-not-contact flag, complaint, or a person's hold.
- Stop past-customer messages on any reply.
- Send only messages a person has approved. If you have no approved
  message for a case, send nothing and send alert H (no approved
  message).
- Log every send, reply, promise and status change on the record.
```

## Every message it sends
Each one is approved by a person before a real customer sees it.

**1. Check-in.** Next business day after the job is marked complete. [NAME] is a real person on your team who will read the replies.

> Hi [FIRST NAME], it's [NAME] with [COMPANY]. I wanted to make sure yesterday's [PROJECT] was finished cleanly and that you know what happens next. Is everything looking and feeling right, or is there anything we need to address?

If the job was not finished the day before (a Friday job checked on Monday), change "yesterday's" to the day it was finished.

**2. Second try.** Once only, when the check-in gets no reply. The kit has no separate wording for this. A person either approves a resend of the check-in or makes a call.

**3. Review ask.** Only after a happy answer, or after a person confirms a problem is fixed.

> Glad everything landed the way it should. Would you mind sharing an honest review and adding a photo if you're comfortable? It helps nearby homeowners understand what the work actually looks like: [DIRECT REVIEW LINK]

**4. Review reminder.** Once, 3 to 5 days after the ask, and only if no review is logged.

> Quick reminder in case the review link got buried: [DIRECT REVIEW LINK]. No pressure. An honest review helps us improve and helps neighbors know what to expect.

**5. Referral offer.** To happy customers only, as its own message or said in person. Never inside the review ask.

> If a neighbor asks who did the work, here's the referral link/card. If they [APPROVED TRIGGER], we'll send you [APPROVED REWARD]. It is separate from reviews. There's nothing you need to post.

**6. Past-customer reminder.** Only to an approved group, on that group's date. Example:

> Hi [FIRST NAME], it's [COMPANY]. We completed your [PROJECT] around this time last year. We're checking nearby homes for [RELEVANT SEASONAL CONDITION]. Want us to include yours, or would you rather not receive these reminders?

### Alerts to your team
These go to your team through [ALERT CHANNEL], never to a customer. Each is a team alert, your AI may adjust the wording. The blanks come from the customer's record. [REPLY] is the customer's own words.

**A. Review follow-up.** To [SALES ALERT LIST]. 3 to 5 days after the reminder, if a happy customer still has no review logged.

```
Review follow-up:
[FIRST NAME],
[PROJECT].
Happy, no review after the reminder.
Follow up for an honest review: [PHONE].
Already reviewed?
Set Review Completed to yes.
```

The person asks for an honest review only. No reward, discount or gift for a review or a rating. If the customer raises a problem, it goes to the customer experience owner and the asks stop.

**B. Unhappy customer.** To the customer experience owner and the backup, at once. Outside [ALERT HOURS], first thing when they start.

```
Unhappy customer:
[FIRST NAME],
[PROJECT].
They said: "[REPLY]".
All asks paused.
Own it today: [PHONE].
```

**C. Open question.** To the Issue Owner, or the customer experience owner if none is named yet.

```
Open question:
[FIRST NAME],
[PROJECT].
They said: "[REPLY]".
Set a dated next step: [PHONE].
```

**D. Check-in call due.** To the customer experience owner, the next business day after a job in [CALL-FIRST JOBS] is finished.

```
Check-in call due:
[FIRST NAME],
[PROJECT],
finished [DATE].
Call today: [PHONE].
```

**E. No reply to the check-in.** To the customer experience owner.

```
No reply to check-in:
[FIRST NAME],
[PROJECT].
Approve one resend or call: [PHONE].
```

**F. No reply to the second try.** To the customer experience owner.

```
Unreachable:
[FIRST NAME],
[PROJECT].
No reply to the second try.
Nothing more will send.
Your call: [PHONE].
```

**G. Referral reward owed.** To the referral program owner named on the card in step 5.

```
Referral reward owed:
[REFERRER NAME] referred [NEW CUSTOMER NAME].
Deliver [APPROVED REWARD] and log it.
```

**H. No approved message.** To the customer experience owner.

```
No approved message:
[FIRST NAME],
[PROJECT],
[CASE].
Nothing was sent.
Decide the next step.
```

## Test list
Use your own test contact and made-up jobs, with every alert pointed at your own phone (step 9). With the fallback, "alert arrives" reads "a task appears for the right person, on the daily list".

| # | Test | Pass mark |
|---|---|---|
| 1 | Happy customer | Moves to Ready to Ask. Gets the review ask with a working link. |
| 2 | Open question | A person is named owner with a dated next step. No review or referral ask goes out. |
| 3 | Complaint | Every review, referral and promo message stops. Recovery opens. Asks stay paused until a person marks it resolved. |
| 4 | No reply | One second try goes out. Then the record shows unreachable. Nothing else is sent to the test contact. |
| 5 | Review completed | No reminder goes out. |
| 6 | Referral meets the trigger | The reward is logged as owed, once. No duplicate contact is made. |
| 7 | Referral does not meet the trigger | No reward is logged. |
| 8 | Past customer opts out | All past-customer messages to that contact stop. |
| 9 | Happy, no review after the reminder | After the wait, review follow-up alert A arrives once, with name, job and number. The test contact gets no new message. |
| 10 | Happy, Review Completed set to yes before the wait ends | No review follow-up alert goes out. |
| 11 | Happy, then opts out before the wait ends | No review follow-up alert goes out. |
| 12 | Complaint, alert check | Unhappy alert B arrives at once, with the customer's words. No review follow-up alert ever goes out while it is open. |
| 13 | Open question, no reply, no reply to the second try, a [CALL-FIRST JOBS] job, a referral that meets the trigger, a case with no approved message | Each one sends its own alert (C to H) once, to the right person. |
| 14 | Event outside [ALERT HOURS] | The alert waits and arrives first thing when the hours start. |

## When a person takes over
The agent stops and a person steps in when:

- Alert A: a happy customer has no review after the reminder. A person follows up for an honest review and logs the result. The agent sends that customer no more review messages.
- Alert B: the customer is unhappy. A person owns it the same day.
- Alert C: a question or something still open. The issue owner sets a dated next step.
- A complaint needs to be marked fixed. Only a person does this, after checking with the customer.
- Alert D: a [CALL-FIRST JOBS] job. A person makes the check-in call.
- Alert E: no reply to the check-in. A person approves the second try or calls.
- Alert F: no reply to the second try either.
- Alert G: a referral reward is owed. A person delivers it and logs it.
- Alert H: no approved message for the case.
- The customer opts out, or someone on your team puts a hold on the record.

Want this installed for you? That is the Full Done-For-You Installation.
