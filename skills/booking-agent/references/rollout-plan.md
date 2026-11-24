# Your 7-day rollout plan
**Jobs-On-Demand Flywheel Kit · what software you need, and what to install each day**

> This plan assumes you use GoHighLevel. Days 1 to 7 build all five agents inside GoHighLevel, easiest first. The advanced setup, your own database in Supabase, comes after day 7 and is optional.

## The software you need

### Required
| Software | What it is | What it does here |
|---|---|---|
| **GoHighLevel** | Customer software: contacts, texting, calendar, automations and an AI chat bot in one account. | Runs all five agents every day. The chat bot answers leads, automations send the texts and create call tasks, the calendar books visits, and its phone app sends your team's alerts. |
| **An AI assistant that works on your computer: Claude Code (recommended), the Claude desktop app, or Codex** | AI that reads files, writes files and connects to your accounts. Claude Code and the Claude desktop app come with a paid Claude plan. Codex comes with a paid ChatGPT plan. | Reads this kit, asks for your facts, builds what it can in GoHighLevel, gives you click-by-click steps for the rest, checks every test, edits ad videos and runs the weekly numbers. |

**Check before you buy:** pick the GoHighLevel plan that includes workflows (its name for automations) and Conversation AI (its name for the chat bot). On some plans the chat bot is a paid add-on, and texts and calls are billed by use. Prices change, so check each company's pricing page.

### Free accounts you probably already have
- **A Facebook business page and ad account,** with payment set up (agents 1 and 4).
- **A Google Business listing,** for its review link (agent 3).
- **A free Google Drive folder** for crew job videos (agent 4).

### Advanced setup only (after day 7, optional)
- **Supabase,** a website that hosts a database for you. The free plan works.

### What you do NOT need
- **n8n or Zapier.** GoHighLevel runs the automations. Your AI assistant runs the weekly numbers, and Supabase has its own scheduler for the advanced setup.
- **A separate texting tool, calendar, call-tracking service or video editor.** GoHighLevel covers the first three, and your AI assistant edits video with free tools it installs.

Strongly recommended, not required: a password manager to hold your logins and keys.

## What the agent files' words mean in GoHighLevel

| The agent files say | In GoHighLevel it is |
|---|---|
| Customer tool, CRM | Your GoHighLevel account for your business |
| The agent, the bot | Conversation AI (under AI Agents) |
| Fields / business facts | Custom Fields / Custom Values (both in Settings) |
| Board, stages | A pipeline and its stages (Opportunities) |
| Automation | A workflow (Automation) |
| Push alert to your team | A workflow step that sends an internal notification to the GoHighLevel phone app |
| Internal form | A form (Sites, then Forms) |
| Test mode | A filter at the top of each workflow: only contacts tagged `test contact` get through |
| Forwarding number | An extra GoHighLevel phone number that rings your main line |

Menus in GoHighLevel move. If a name is not where this plan says, search for it inside GoHighLevel.

**Who does what:** your AI assistant builds what GoHighLevel's connection allows (fields, tags, custom values, test contacts) and checks every test. You click for the parts only a person can build there (workflows, the chat bot, the calendar, pipelines, forms), one step at a time as the AI directs. Buying, payment, phone approval and every "yes, go live" are always you.

## The prompt to start
Open this kit's folder in your AI assistant and paste:

```
You are my implementation manager. This folder is the Jobs-On-Demand
Flywheel Kit. I use GoHighLevel. Read ROLLOUT-PLAN.md, START-HERE.md
and MY-NUMBERS.md first, then follow ROLLOUT-PLAN.md one day at a time.

Use GoHighLevel's names for everything. Build what your connection to
GoHighLevel allows yourself. For anything only a person can build there,
give me one click-by-click step at a time, then check my work from my
test contact before you go on.

Build every workflow in draft, with the test contact filter at the top.
Show me every new message before a customer can see it. Ask me for any
fact you do not have. Never guess. Never save a key or password in any
file. Turn nothing on for real customers until every test in that
agent's file passes and I say yes.

Keep PROGRESS.md: one line per step, with its status (done / waiting on
me / blocked) and its "Done when" check. Start with day 1.
```

---

## Day 1: Set up and connect (about 3 hours)
The texting approval takes days, so it starts today. Everything else is built in draft while you wait.

**Never used GoHighLevel or Claude Code?** Do `SETUP-GOHIGHLEVEL.md` and `SETUP-CLAUDE-CODE.md` first. Between them they cover steps 1 to 6 below, click by click.

1. `You` **Set up GoHighLevel.** Company name, address, logo, time zone.
2. `You` **Get your number and start the texting approval.** Buy a local number (or bring your main one over) in GoHighLevel's phone system, then submit the business texting registration (GoHighLevel calls it A2P, in its Trust Center). No automatic text goes out until it is approved.
3. `You` **Add your team.** Each person on an alert list gets a GoHighLevel user and logs into its phone app (LeadConnector in the app store) with notifications on.
4. `You` **Install your AI assistant** and open this kit's folder in it.
5. `You + AI` **Connect the AI to GoHighLevel.** Create a private integration key (Settings, then Private Integrations) with access to contacts, conversations, custom fields, custom values, tags, opportunities, calendars, users and workflows. The AI tells you how to save it in its own settings. Never paste a key into a chat or a file.
6. `You` **Connect Facebook, Instagram and Google.** Connect your Facebook page (and Instagram), your Google Business listing and your Google calendar inside GoHighLevel.
7. `You + AI` **Fill in MY-NUMBERS.md and make your test contact.** The AI asks every line. For alerts, write "GoHighLevel phone app". It then creates your test contact (your phone, your email, tag `test contact`).
8. `AI` **Send one test alert** from a draft workflow to your phone.

**Done when:** texting approval is submitted, the AI reads your business name back from GoHighLevel, a message from your personal Facebook shows in Conversations, MY-NUMBERS.md has no blank, and the test alert landed on your phone.

## Day 2: Reviews agent (file 03, about 2 hours)
The easiest agent: one field starts it, and it only talks to customers you already know.
- Fields and stages from step 1 of file 03, a workflow started by Job Completed At, the four reply routes, the review ask and one reminder with your Google review link, and alerts A to H.
- Run its test list on your test contact. Texts wait for the approval, and everything else can pass today.

**Done when:** every test in file 03 passes on your test contact. It goes live the day texting is approved.

## Day 3: Booking agent, on Facebook messages (file 01, about 3 hours)
Facebook messages do not need the texting approval, so this agent can go live first.
- Fields, tags, the "Conversation Outcomes" pipeline, the calendar, and one Conversation AI bot with file 01's instructions pasted in, answering Facebook and Instagram messages.
- The workflows for new lead, qualified, auto hand-off (its AI step runs the hand-off check), polite close, manual hand-off (with the Lead Transfer form), and needs a person. Add a workflow started by the tag `stop bot` that turns the bot off for that contact.

**Done when:** file 01's message tests (1 to 9, 13 and 15) pass. On your yes, the bot goes live on Facebook messages.

## Day 4: Booking agent, form leads and calls (file 01, about 2 hours)
- The form lead fast reply workflow, started by a website form or a Facebook instant form: the instant or after-hours text, the two call tasks, the missed-call text, and the "Still not called" alert.
- Optional: one forwarding number for your call ads, and the missed-call alert.

**Done when:** file 01's tests 10 to 12, 14 and 16 pass. The texts go live the day texting is approved.

## Day 5: Follow-up agent (file 02, about 3 hours)
- Ladder 1 adds the 1-day and 3-day texts to day 4's workflow. Ladder 2 is one workflow, with each wait set as the gap between two rows.
- The quote follow-up is its own workflow, started when Quote Sent At is filled, with its own pipeline (Quote Sent, Decision Pending, Won, Lost).
- Every step checks the stop list: any reply, `booked`, decided, opted out, `ai dq`, `stop bot`.

**Done when:** every test in file 02 passes with the waits shortened to a minute or two. Put the real waits back.

## Day 6: Numbers agent, the scoreboard (file 05, part 1 only, about 2 hours)
- A permanent First Source field, plus one GoHighLevel forwarding number per source you run (Facebook ads, Google ads, Google listing, mailers, yard signs, referrals). Each one tags the caller with its source.
- The visit fields, and the "no outcome yet" reminder workflow at your evening check time.
- The scoreboard as a spreadsheet the AI builds in your kit folder (or a Google Sheet to share). Every Friday the AI pulls the week from GoHighLevel and Facebook, fills the rows, checks the trend alerts and drafts the review.
- Trend alerts: the AI tags a contact record for your business `numbers alert`, and a GoHighLevel workflow sends that to your phone.

**Done when:** file 05's Part 1 tests pass on made-up weeks.

## Day 7: Ads agent, then go live (file 04, about 4 hours)
- The morning "Film today" crew alert as a GoHighLevel workflow, and the shared clips folder.
- The AI writes the nine starting ads, edits job clips into vertical videos with captions, and builds the campaign switched off. To let it work in your ad account, add a Facebook "system user" that can manage campaigns only (no payment, no admin rights). Without that, it tells you each click.
- The morning spend check runs as a daily scheduled task in your AI app while your computer is on. If it's off, open the AI and say "run the morning spend check". It starts in practice mode.
- **Go-live check:** run one real-looking lead through every agent end to end. Turn on each agent whose tests all passed, and texts as soon as the approval lands. Launch ads on your approver's yes. Teach your team the takeover play from each file.

**Done when:** a real lead runs from first message to a clean hand-off with its alert on the team's phones, and the ads are on (or waiting only on your approver).

---

## Advanced setup: your own database (optional, about one weekend)
Do this only after the five agents have run for a few weeks. It moves your numbers into one place so the scoreboard fills itself, with nobody pulling it on Fridays.

**You need:** a Supabase account (free plan), and Claude Code or Codex. This part writes code, so a plain chat assistant can't do it.

1. `You` **Open a Supabase project.** Save its keys in your password manager and in your AI's settings, never in a file.
2. `AI` **Create the five tables** from file 05, step 9: contacts, conversations, ad results, bookings, jobs.
3. `AI` **Pull from GoHighLevel every 15 minutes, and from Facebook ads daily,** using Supabase's built-in scheduled jobs. No n8n needed. If you already use n8n, file 05 steps 10 to 12 show that way.
4. `AI` **Connect payments** (file 05, step 12) from whatever you invoice with.
5. `AI` **Build the two scoreboard views and the automatic Friday alerts** (file 05, steps 13 and 14). Alerts still go to the GoHighLevel phone app by tagging the contact record for your business.
6. `You` **Set the safety rules** (file 05, step 15): your own logins, weekly backups, one named owner.

**Done when:** every Part 2 test in file 05 passes, and Friday's numbers fill with nobody typing.

## If you get stuck
- Ask your AI: "I'm stuck on day [number], step [number]. Here is what I see." Paste or describe the screen.
- If GoHighLevel can't do a step the way a file says, the AI gives you the simplest way around it and writes it in PROGRESS.md.

Want this installed for you? That is the Full Done-For-You Installation.
