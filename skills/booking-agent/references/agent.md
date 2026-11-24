# Install your booking agent
**Jobs-On-Demand Flywheel Kit · Sales · agent 1 of 5**

> It answers every new message and form lead in seconds, asks the few questions that sort good fits from bad, alerts your sales team's phones to call, and gets a visit on the calendar or hands the lead to a person.

## What this agent does
- Replies to every new message and form lead in seconds, day or night, and sends push alerts to sales team to call new leads.
- Asks only for what is missing: the job, the zip code and a phone number.
- Ends every conversation one of three ways: **pass** (clean notes go to your sales rep), **review** (a person decides) or **fail** (politely closed and logged).
- Texts every form lead right away, gives your team a call task, and texts again when that call is missed. After hours, the text promises a call as soon as possible instead.
- Sends a second alert when nobody has called a new lead within the 5 minutes its call task allows. The call itself is made by a person.
- Never quotes a price, diagnoses or makes up a fact. It is the intake assistant, not the closer.

- Alerts your team when a call from one of your call ads is missed, so a person calls back.

This agent works by text and message. When a lead goes quiet, the follow-up agent (agent 2 of 5) takes over.

## What you need before you start
- **A customer tool (CRM) with admin access that can do four things:** answer Facebook messages and texts by itself from instructions you paste in; keep fields and tags on each contact; run automations that start when a tag is added, including a step that reads the conversation and fills in fields; and create tasks for a person. Your AI assistant checks this before step 1 and tells you if yours can't.
- **A way for an automation to send a push alert to your team's phones,** with no person pressing send: your customer tool's own phone app notice, a text to each team member, or your team's chat app. If none works, step 10 gives the slower fallback.
- **If you run call ads (agent 4):** a phone tool that can tell an automation a call to the call ads' tracking number went unanswered. If it can't, a person checks that number's missed calls instead (step 11).
- From MY-NUMBERS.md: [ALERT CHANNEL], [SALES ALERT LIST], [ALERT HOURS] (under "Alerts and ad spend"), [PHONE HOURS], the hours a person answers the phone, and [QUIET HOURS], the hours no text goes out.
- Your Facebook page (and Instagram, once connected) linked to that tool.
- One real phone line, approved for business texting. Texts and calls come from that same number. Until it is approved, no automatic text goes out.
- A real calendar showing only the times your sales rep will keep.
- A test contact you own: your phone and a personal Facebook account.
- One named person who clears the Needs Review list every day.
- About 90 minutes.
- Your business facts:
  - [BUSINESS NAME], [BUSINESS PHONE], [WEBSITE], [TRADE]
  - [SERVICES YOU SELL] and [PROBLEMS YOU FIX]
  - [JOBS YOU DO NOT TAKE] (for example: new construction, mobile homes, cosmetic-only work)
  - [SERVICE AREAS] and [AREAS YOU DO NOT SERVE]
  - Up to four [JOB TYPES]
  - [VISIT NAME]: what you call the first visit (for example, "free inspection")
  - [REP NAME] and [BOOKING LINK]

## How to install it
To install this agent alone, type **"install my booking agent"**, or use the paste prompt at the end of `INSTALL-GUIDE.md`.

## Step by step
1. `You + AI` **Save your business facts.** Save each fact above where your tool keeps reusable details. Done when: no blank is left.
2. `AI` **Create the contact fields.** First Message (the lead's first message, word for word), Full Convo (the whole conversation), Notes (a plain summary of the job), Location (the city or area as the customer said it), Project Type (the job in the customer's words), Project (one of your job types), four ad source fields (source, campaign, medium and content: together they say which ad the lead came from) and the ad click ID. Use your tool's own phone, email and zip fields; make no second copies. Done when: all exist.
3. `AI` **Create nine tags, lowercase, spelled exactly.** `fb lead`, `qualified`, `ready for transfer`, `transferred`, `needs review`, `ai dq`, `stop bot`, `booked`, `quote`. Done when: all nine exist.
4. `AI` **Create the outcomes board.** Board "Conversation Outcomes", seven stages: Pending, Needs Review, Transferred, Out of Scope, Out of Area, Not Interested, Ghosted. A person moves a lead to Not Interested. The follow-up agent (agent 2) moves a lead to Ghosted. Done when: all seven exist.
5. `You` **Connect a real calendar.** Each booking adds the tag `booked` (or a person does, if your calendar can't). Done when: a test booking puts a real appointment on your sales rep's calendar and the tag `booked` on the contact.
6. `AI` **Create one agent.** Name: "Qualifier AI — [BUSINESS NAME]". The only agent that answers. Start with Facebook messages. It waits about 2 seconds before it replies, keeps replies short, and stops after 75 automatic messages in one conversation. Paste the instructions below. Give it four signals to raise (in most tools, an action that adds a tag or starts an automation): fit checks passed, tag `qualified`; bad fit closed, tag `ai dq`; phone, zip and area confirmed, start the auto hand-off in step 8; customer asks for a person or says it is urgent, start the "Needs a person" alert in step 11. Make it stop for any contact tagged `stop bot` (in most tools a tag does nothing until a setting or an automation acts on it). Done when: exactly one answering agent exists, it has all four signals, and adding `stop bot` to your test contact stops its replies. Two agents means double replies.
7. `You + AI` **Load a short question-and-answer list.** Only facts that change where a lead goes or calm a nervous customer. Done when: you approved every fact and the list is attached to the agent.
8. `AI` **Build six automations, all in draft.**
   - **New lead:** a first message arrives with no `fb lead` tag. Add the tag. Real inquiry: save the first message and ad source. Accidental tap: end quietly.
   - **Qualified:** tag `qualified` is added after the fit checks pass. Create a record in Pending.
   - **Auto hand-off:** phone, zip and area are confirmed. Stop the agent for that contact, pull the details, fill the fields, tag `ready for transfer`.
   - **Manual hand-off:** your team submits an internal "Lead Transfer" form. Create this form first, with: name, phone, zip, job type, a short note, how urgent. Tag `transferred`, log it, notify the sales rep.
   - **Polite close:** the agent ends a bad fit. Turn the agent off for that contact, tag `ai dq`, move to Out of Area or Out of Scope.
   - **Form lead fast reply:** a form lead arrives with a phone number (from your website, or from an ad's instant form). Inside [PHONE HOURS], send the instant text and create the first call task, due within 5 minutes. Outside [PHONE HOURS], send the after-hours text instead, and make the first call task due when [PHONE HOURS] start. Either way, create the second call task 1 hour after the first is due. Send the missed-call text 5 minutes after the caller marks the first call "no answer". Your AI assistant sets up that mark (a tag or a task result). Tag `booked` stops everything.

   **Quiet hours.** The first reply to a brand-new lead is the one exception to [QUIET HOURS]: it may go out at any hour. That is the instant text, the after-hours text, or the agent's first reply. Every later text respects [QUIET HOURS]. If one falls inside them, it waits until they end.

   Done when: all six exist in draft.
9. `AI` **Make the hand-off check the last step of auto hand-off.** Yes: tag `transferred`, move to Transferred, put the team note below on the contact. No: tag `needs review`, move to Needs Review. Done when: a lead with a missing or junk field goes to Needs Review, never to the sales rep.
10. `You + AI` **Choose how alerts reach your team's phones.** Fill in [ALERT CHANNEL], [SALES ALERT LIST] and [ALERT HOURS] in MY-NUMBERS.md. Your AI assistant picks the first of the three ways under "What you need" that your tool can send. Agree who on [SALES ALERT LIST] calls first; the rest are backup. Set [ALERT HOURS] to start no later than [PHONE HOURS], so an alert lands before its call is due.
    **The fallback,** if your tools can send none of the three by itself: each alert becomes a task for everyone on [SALES ALERT LIST], due at once, plus a daily list of every new lead and whether it was called. Nothing reaches a phone, so someone keeps the task list open during [ALERT HOURS]. The other agent files use this same fallback.
    Done when: a test alert sent from an automation lands on every phone on [SALES ALERT LIST], or the fallback is written in MY-NUMBERS.md next to [ALERT CHANNEL].
11. `AI` **Add the push alerts, all in draft.** Wording under "Alerts to your team"; each goes to [SALES ALERT LIST] through [ALERT CHANNEL]. This file owns the new-lead alerts and the 5-minute "Still not called" alert; the follow-up agent never builds them.
    - **Form lead:** in "Form lead fast reply", send "New form lead" with the instant or after-hours text.
    - **Message lead:** it has no number to call until the hand-off. When the hand-off check says Yes, create a call task due within 5 minutes and send "New qualified lead". If the customer gave an email instead of a phone, the alert shows the email, with no call task and no 5-minute check.
    - **Needs Review:** when the hand-off check says No, send "Needs a person" with what failed.
    - **Needs a person:** when the agent raises that signal, send "Needs a person" at once. Its own small automation: seven in all (eight with the missed-call alert).
    - **Manual hand-off:** "Lead handed over" is its notice to the sales rep.
    - **Not called yet:** 5 minutes after a new-lead alert goes out, if the first call task is not marked "called" or "no answer", send "Still not called", once. Set up "called" like "no answer". On a message lead, neither mark sends a text. Tag `booked` cancels this check.
    - **Missed call from an ad:** a call to the tracking number for your call ads (agent 4) is not answered. Send "Missed call from an ad" with the caller's number. Nothing goes to the homeowner. Your AI assistant checks whether your phone tool can tell an automation a call was missed. If it can't, a person checks that number's missed calls each time they work the task list during [ALERT HOURS], and puts each one on the daily list. This covers calls from an ad only; other missed calls to your business line still get nothing from this kit.
    - **Alert hours:** outside [ALERT HOURS], hold each alert until they start. The 5-minute check counts from when the alert goes out or the call is due, whichever is later. Alert hours never hold a text. The first reply to a new lead never waits; later texts wait out [QUIET HOURS].
    The team notes stay on the contact or the call task; the alert is the short notice to phones. Done when: every alert above is in draft, in the automation it belongs to, and no notice is sent twice.
12. `You + AI` **Run the test list.** Switch the agent and all its automations on for your test contact only (test mode, or a filter that lets only it through). Your AI assistant checks tags, stage, fields and alerts after each test. Done when: every test passes.
13. `You + AI` **Go live.** Delete test contacts, take off the filter, put the full team back on [SALES ALERT LIST]. On your final yes, publish them all. Done when: a real lead goes from first message to a clean hand-off, and its alert lands on the team's phones.
14. `You` **Teach the team the takeover.** Done when: everyone can run it from memory.

## The agent's instructions
Paste into the agent in step 6.

```
WHO YOU ARE
You are the intake assistant for [BUSINESS NAME], a [TRADE] company.
You are not the contractor. Your job is to get contact details and
pass the lead to the sales rep. Never claim to be a person.

STYLE
Casual texting. Two sentences at most, then one question. No emojis.
Outside the scripted lines, no exclamation points except "Yes!"
(asked about past work) and "Nope!" (asked if you are a contractor).
Words you like: got it, yep, nope, no worries, tbh, honestly.

HARD RULES
Never quote a price. Never diagnose. Never make up business details
(pricing, subcontracting, financing, years in business). Answer from
the question-and-answer list or pass it to the sales rep. There is
no third option. Never ask again for something already given.

QUIET HOURS
Your first reply to a brand-new lead may go out at any hour. After
that, send no text during [QUIET HOURS]. Wait until they end.

FACTS
Business: [BUSINESS NAME]
Phone: [BUSINESS PHONE]
Site: [WEBSITE]
Services: [SERVICES YOU SELL]
Problems we fix: [PROBLEMS YOU FIX]
Jobs we do not take: [JOBS YOU DO NOT TAKE]
Areas served: [SERVICE AREAS]
Areas not served: [AREAS YOU DO NOT SERVE]
Quiet hours: [QUIET HOURS]

INTERESTED LEAD
"We can help! Send your zip code and best phone number and I'll set
you up with a fast estimate."

NOT ABOUT A JOB (spam, accident, browsing, angry, another contractor)
"Sorry about that!" Then stop. Resume only if they clearly ask for
service.

SERVICE FIT
Fits our services or problems: continue.
Matches a job we do not take: "thanks for reaching out! we
  actually can't help with [ITEM]. sorry about that!" END
Not our trade: "nope, we only help with [TRADE]. sorry about
  that!" END
Renter (unless the property owner is asking): END
Do-it-yourself or materials only: END
Unclear: continue and let the sales rep decide.
Do not collect contact details before ending a bad fit.

AREA FIT
In or next to areas served: confirmed.
In areas not served, or clearly outside: "looks like that area
  is outside the area we cover. sorry about that!" END
Not listed but not clearly outside: ask for the zip. Do not
  reject. Once decided, never reverse it unless a person corrects it.

CONTACT DETAILS: one message, only for what is missing
No area, no phone: "what's the best phone number and zip code
  so I can have someone on our team reach out?"
Area confirmed, no phone: "just send me your phone number and
  I'll get you set up with a fast estimate"
Phone given, no area: "thanks! send me your zip so I can verify
  we service your area"
If they ask a question, answer briefly, then ask for what is missing.

CHECKING
Phone: strip everything but digits, drop a leading 1. Valid: exactly
10 digits. Not valid: "can you double check that number? want to
make sure someone on our team can reach you". Still not valid after 2
tries: stop asking, flag for a person.
Zip: valid is exactly 5 digits. Not valid: "can you double check
that zip? doesn't look right"
Phone refused: "no worries, I can have someone on our team contact you
by email instead. what's the best email?" Then go on with email.

HAND-OFF: only when phone is 10 digits (or email if phone refused),
zip is 5 digits, and the area is confirmed
"awesome, thanks! someone on our team at [BUSINESS NAME] will reach out
soon to schedule your estimate! lmk if you have any other questions
in the meantime!"
Any question after that: "someone on our team will be able to answer that
when they reach out. anything else in the meantime?"

COMMON QUESTIONS
Price: "honestly it depends on what's going on at the property.
that's exactly what the [VISIT NAME] figures out. what's your zip
and best number?" Add the tag quote.
"Is this serious?": "hard to say without eyes on it. someone on our team
sees this every day. want me to set up a [VISIT NAME]?"
Licensed, insured, years in business, financing: only what is in
the list. Otherwise "someone on our team can cover that when they reach
out."
"Is this a bot?": "yep, I'm the automated assistant for
[BUSINESS NAME]. a person from our team will reach out."
Then ask the next intake question.
"Same company?": "yep, this page is owned and operated by
[BUSINESS NAME]. same team."
Attachment: "thanks for sending that over. I can't view
attachments but I'll pass it to someone on our team."
Contact preference ("call after 4"): "got it, I'll note that for
someone on our team."

NEEDS A PERSON
The customer asks for a person, or says it is urgent (for example,
water coming in right now): raise the "needs a person" signal at
once. Then keep to the lines above. Never promise a time. You do not
send alerts to the team yourself. The automations do.
```

**The hand-off check** (for steps 8 and 9). Save the city in Location. Save the job type in Project Type, and the closest of your job types in Project:

```
PULL FROM THE CONVERSATION, one step each
Phone: digits only, drop +1, exactly 10 digits. Use the newest
number. None valid: blank. Save as +1 and the ten digits.
Zip: 5 digits only. Never override a zip the customer gave.
City: the area as the customer said it.
Job type: from the customer's words. No match: [TRADE]. Never
"Other" or blank.
Notes: one natural summary of what the customer said about the job.
No contact details. Never one word.

READY CHECK: return YES only if all are true
Conversation is not empty
At least 2 separate customer messages
Zip is exactly 5 digits
Phone is exactly 10 digits, or email is present because the
    customer refused to give a phone
No field holds filler like "I'm sorry", "please provide", "not
    provided", "no phone", "no location", "cannot extract"
Job type is not blank
Notes are not blank, not one generic word, and hold only what
    the customer said
If any item fails, return NO and name what failed.
```

## Every message it sends
The agent's conversation lines are word for word in its instructions above. These are the rest.

- **0 seconds after a form lead arrives, inside [PHONE HOURS] (automatic):** "Hey [FIRST NAME], it's [REP NAME] with [BUSINESS NAME]. Got your request about the [VISIT NAME]. I'm going to call you in the next couple minutes from [BUSINESS PHONE] so it's not a random number. If now's bad, just text me a better time."
- **0 seconds after a form lead arrives, outside [PHONE HOURS] (automatic):** "Hey [FIRST NAME], it's [REP NAME] with [BUSINESS NAME]. Got your request about the [VISIT NAME]. I'll call you ASAP from [BUSINESS PHONE] so it's not a random number. If there's a better time, just text it to me here."
- **5 minutes after the first call is marked "no answer" (automatic):** "Just tried you! Easiest way to lock your [VISIT NAME]: [BOOKING LINK]"
- **The moment a person takes over, details still missing (typed by a person):** "Hey [FIRST NAME], jumping in here so we can make sure this gets handled correctly. Can you send me the best phone number and zip code for the property?"
- **The moment a person takes over, details already given (typed by a person):** "Got it, thanks. I have [JOB TYPE] in [CITY OR ZIP]. I'm getting this to the right person so they can help with the next step."

Both calls are tasks, from the same number as the texts (timing in step 8). Send the missed-call text only after the first call was really made. The follow-up agent (agent 2) adds two more texts, 1 day and 3 days later, and the "Follow-up call due" alert for the second call. A person approves any new or changed wording first. A person sends a takeover text only after a call goes unanswered, or when there is no phone yet. Only the first two texts above may go out during [QUIET HOURS]; the rest wait until they end.

**Note to your team on a pass:** "NEW QUALIFIED LEAD: [BUSINESS NAME]. Name: [NAME]. Phone: [PHONE]. Zip: [ZIP] (in area). Job: [JOB TYPE]. Notes: [WHAT THE CUSTOMER SAID]. Prefers: [CONTACT PREFERENCE]."

**Note on the manual hand-off form:** "Manual rescue: customer asked about [JOB] in [CITY OR ZIP]. Phone: [PHONE]. Notes: [SUMMARY]. Next step: [CALL / VISIT / REVIEW]."

### Alerts to your team
These go only to [SALES ALERT LIST], through [ALERT CHANNEL], never to a customer. Step 11 says when each one fires. Leave out any part the lead has not given yet.

- **New form lead** (team alert, your AI may adjust the wording):

```
New form lead:
[NAME],
[JOB TYPE],
[ZIP].
Call now: [PHONE].
```

- **New qualified lead** (team alert, your AI may adjust the wording):

```
New lead:
[NAME],
[JOB TYPE],
[ZIP].
Call now: [PHONE].
```

- **Still not called, 5 minutes later** (team alert, your AI may adjust the wording):

```
Still not called:
[NAME],
[JOB TYPE].
Call now: [PHONE].
```

- **Needs a person** (team alert, your AI may adjust the wording):

```
Needs a person:
[NAME].
Why: [ASKED FOR A PERSON / URGENT / WHAT FAILED THE CHECK].
Open the conversation and take over.
```

- **Lead handed over** (team alert, your AI may adjust the wording):

```
Lead handed over:
[NAME],
[JOB TYPE],
[CITY OR ZIP],
[HOW URGENT].
Call: [PHONE].
```

- **Missed call from an ad** (team alert, your AI may adjust the wording):

```
Missed call from an ad:
[PHONE].
Call back now.
```

Outside [ALERT HOURS], the alerts wait until the hours start. Texts never wait for alert hours. The first reply to a brand-new lead goes out at once, at any hour. Every later text waits until [QUIET HOURS] end.

## Test list
Message your own page from a personal account. Only your phone is on [SALES ALERT LIST]. Run every test inside [PHONE HOURS] and [ALERT HOURS], except test 14. With the fallback, "alert lands" reads "a task due at once appears".

1. **Perfect fit in your area.** Pass: phone and zip collected, clean team note, tags `qualified` then `transferred`, a 5-minute call task and the "New qualified lead" alert. Marking it "no answer" sends no text.
2. **Zip you do not serve.** Pass: polite close, tag `ai dq`, stage Out of Area.
3. **A job outside your trade.** Pass: polite close, no contact details asked for.
4. **Never gives a phone.** Pass: one more ask, then email or Needs Review. No fake hand-off. Ending in Needs Review sends "Needs a person", naming what failed.
5. **Describes the job, no location.** Pass: asks for the zip once, checks for 5 digits.
6. **Answers once, then silence.** Pass: the booking agent sends no repeat messages by itself. The follow-up agent (agent 2) picks the lead up from here.
7. **"Why are you asking all this?"** Pass: one calm reason, one question, no arguing.
8. **"5551234567 37209" in one message.** Pass: both pulled out and checked.
9. **"(555) 123-4567".** Pass: stripped to 10 digits and accepted.
10. **Test form lead.** Pass: the instant text and the "New form lead" alert arrive together, and a 5-minute call task appears. Marking it "no answer" sends the missed-call text. Tag `booked` cancels everything.
11. **Test form lead, nobody calls.** Leave the first call task unmarked. Pass: "Still not called" lands 5 minutes after the first alert, once.
12. **Test form lead, called in time.** Mark the first call task "called" within 5 minutes. Pass: no second alert.
13. **"Can I talk to a real person?" and "Water is coming in right now".** Pass: for each, "Needs a person" lands at once, and the agent keeps to its lines and promises no time.
14. **After hours.** Set [PHONE HOURS] and [ALERT HOURS] to start a few minutes from now, then send a test form lead. Pass: the after-hours text goes out at once, with no alert. When the hours start, the alert lands, the first call is due, and the 5-minute check counts from then. Then set [ALERT HOURS] to open earlier than [PHONE HOURS]: "Still not called" waits until 5 minutes after the call is due. Put the real hours back.
15. **Manual hand-off.** Submit the Lead Transfer form for your test contact. Pass: tag `transferred`, and the "Lead handed over" alert lands.
16. **Missed call from an ad** (only if you run call ads). Call the call ads' tracking number from your own phone and let it ring out. Pass: "Missed call from an ad" lands with your number, once, and nothing is sent to your phone as a homeowner. With no missed-call signal, pass: the person on duty finds it on the missed-call list and it goes on the daily list.
17. **Takeover.** While the agent is mid-conversation with your test contact, run the takeover. Pass: after `stop bot`, no agent or follow-up message arrives. The call comes before the text, the form tags `transferred`, and the Failure Log row has every line filled in.
18. **Takeover, bad fit and no phone.** During a takeover, give a zip you do not serve. Pass: a polite close typed by a person, tag `ai dq`, stage Out of Area, a Failure Log row and no hand-off. Repeat, refusing a phone twice. Pass: Needs Review, and no third ask.
19. **Quiet hours.** Set [QUIET HOURS] to cover right now, then send a test form lead and mark the first call "no answer". Pass: the instant or after-hours text arrives at once. The missed-call text waits until [QUIET HOURS] end. Put the real hours back.

## When a person takes over
A person steps in when:
- The agent did not reply, repeated itself or asked the wrong question.
- It closed an obvious fit, or left fields empty after the customer gave the details.
- The phone number is still wrong after two tries.
- The lead fails the hand-off check or sits in Needs Review.
- The customer asks for a person, is clearly urgent, or raises anything off script. The "Needs a person" alert tells you at once.

When a new-lead alert lands:
- The first caller agreed in step 10 calls the number on it; if they can't, the next person on the list does.
- After the call, mark the task "called" or "no answer". That stops the second alert; on a form lead, "no answer" sends the missed-call text.
- "Still not called" means nobody has called. The first person free calls now.
- If alerts stop landing, check [ALERT CHANNEL] and work the call task list by hand.
- "Missed call from an ad": the first person free calls the number back now, from the business line.

The takeover. This is the kit's one takeover play, for every agent: call first, then text. Save the lead first and find the cause later. Never fix the setup while a customer waits.
1. `You` **Pause the agent.** Add tag `stop bot`. If the follow-up agent (agent 2) has this lead, pause it for this contact too. Add a note on the contact: "Takeover started", with the date and time. Done when: no automatic message can reach this lead.
2. `You` **Read before you reach out.** Read the whole conversation and the contact's fields. Note what the customer already gave, and what is missing or wrong. Done when: you know what to ask for, so you never ask twice.
3. `You` **Call first, then text.** Phone on file: call from [BUSINESS PHONE]. No answer, or no phone yet: send the matching takeover text above. Done when: you reached them, or one text is out.
4. `You` **Collect only what is missing.** Name, phone, zip, job type, a short note and how urgent. Put the best time to call and whether they own the property in the note. No phone: ask once more. Still no: move them to Needs Review and stop asking. Done when: you have every field, or the lead is in Needs Review.
5. `You` **Hand over, or close.** A fit: submit the manual hand-off form with the note above. Not interested: move it to Not Interested. A bad fit: close with the agent's matching close line, tag `ai dq`, and move it to Out of Area or Out of Scope. Bad fits: outside your area, a job you do not take, or a renter without the owner's OK. Also spam, a lead already in your customer software, or price shopping with no real job. Done when: the lead sits in one stage, and nobody owes it a message.
6. `You` **Log it.** Write one row in the data agent's Failure Log (agent 5), bad fits included. There is no separate takeover log. If agent 5 is not set up yet, start its Failure Log tab now (its step 8). Write the exact failure, never just "the bot failed." Done when: every line below is filled in on that row.

```
FAILURE LOG ROW
Date and time:
Lead:
Who took over:
Lead source:
What the agent did:
What the customer said:
Missing or wrong field:
What you did:
Lead saved? yes / no
Fix needed:
```

Once a week, the person who clears Needs Review reads the Failure Log. The same failure three times means fix the instructions, the question-and-answer list or the automation, not the lead.

Want this installed for you? That is the Full Done-For-You Installation.
