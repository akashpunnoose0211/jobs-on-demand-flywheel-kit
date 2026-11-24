# The Jobs-On-Demand Flywheel Kit: start here

**What this is:** five agents you install in your own business, with the scripts each one uses and the steps to set it up. Where a message has no fixed words yet, the file says so, and your AI assistant drafts it for you to approve. You do the installing, with your own AI assistant doing most of the work beside you.

**Who it's for:** a home service business doing $1 million to $10 million a year. A team answers the phones and writes the proposals, and it all still runs through you.

**What you need:** two pieces of software. **GoHighLevel** runs the agents. **An AI assistant that works on your computer** builds them with you: Claude Code (recommended), the Claude desktop app, or Codex. You do not need n8n, Zapier or Supabase. `ROLLOUT-PLAN.md` lists everything, including the free accounts you probably already have, and walks you through the install in 7 days.

**New to either one?** Start with `SETUP-CLAUDE-CODE.md` (about 20 minutes) and `SETUP-GOHIGHLEVEL.md` (about an hour). Both assume you've never used them.

---

## One flywheel, three parts, five agents

A lead comes in. Sales signs the job. The crew finishes it. Brand turns that finished job into the next lead. Data writes down what happened, so both get better.

| Part | Agent | What it does | File |
|---|---|---|---|
| Sales | 1. Booking agent | Replies to every new message and form lead in seconds, day or night, and sends push alerts to sales team to call new leads. | `01-booking-agent.md` |
| Sales | 2. Follow-up agent | Follows up every quiet lead and sends push alerts to sales team to follow up with every lead. | `02-follow-up-agent.md` |
| Brand | 3. Reviews agent | Checks in after every finished job, then asks happy customers for a review, and sends push alerts to sales team to follow up with every customer for a review. | `03-reviews-agent.md` |
| Brand | 4. Ads agent | Sends push alerts to tell the crew what to film, edits every video, writes every ad, launches every ad, and manages ad spend automatically. | `04-ads-agent.md` |
| Data | 5. Data agent | Tracks where every lead, appointment, and dollar came from, maintains one weekly scoreboard of everything that matters, and sends push alerts when metrics are trending down. | `05-data-agent.md` |

The follow-up agent still follows up every sent quote too.

## Alerts to your team

A push alert is a short notice on a team member's phone. It lands the moment a person needs to act: call this lead, follow up on this quote, ask this customer for a review, film this job.

- Alerts go to your team. Never to a customer.
- You set them up once, in `MY-NUMBERS.md`: how alerts reach your team, who gets which ones, and the hours they may go out.
- They go out through what your tools can already do: your customer tool's phone app, a text to the team member, or your team's chat app.
- If your tools cannot send any of those by themselves, the alert goes onto a task list or report instead, and a named person reads it. It no longer reaches a phone the moment it happens. Each agent file says how, and your AI assistant tells you before it builds.

---

## How to use this kit (3 steps)

1. **Open `ROLLOUT-PLAN.md`.** It says what software you need and what to install each day, easiest first.
2. **Open this folder in your AI assistant and paste the prompt from `ROLLOUT-PLAN.md`.** On day 1 your AI helps you fill in `MY-NUMBERS.md` (about 10 minutes; guesses are fine to start).
3. **Install one agent a day, in the plan's order.** Each agent file says what you need before you start.

Each agent file also has its own short prompt. Use that one only when you install a single agent by itself.

## Not using GoHighLevel? Paste this prompt instead
The rollout plan is written for GoHighLevel. With other customer software, paste the prompt below. Your AI assistant checks first whether your software can do each step.

```
You are my implementation manager. This folder is the Jobs-On-Demand
Flywheel Kit: five agents to install in my home service business.

Read START-HERE.md and MY-NUMBERS.md first.

Before agent 1, ask me which tools I already use: where I keep my
customers, how I text them, my calendar, and where I run ads. Map every
step to those tools and use their names for things. If one of my tools
cannot do a step, tell me before you go on, and give me the simplest
way around it.

Also before agent 1, ask me three things and write my answers into
MY-NUMBERS.md: how alerts will reach my team's phones (and who gets
each kind), the most the ads agent may spend in a month, and who
approves each new ad.

If you cannot reach one of my tools yourself, give me click-by-click
steps for that step. Then check my work from what I paste or show you.

Then work through the five agent files in order, 01 to 05.

For every step:
- If it is tagged AI, do it for me now and show me the result.
- If it is tagged You, put it on my to-do list with exact instructions.
- If it is tagged You + AI, ask me the questions you need, then do the rest.

Build everything in draft. Test only on my own test contact. Turn nothing
on for real customers until every test in that agent's file passes, every
"Done when" before its go-live step passes, and I say yes.

Keep a file called PROGRESS.md: one line per step, with its status
(done / waiting on me / blocked) and its "Done when" check.

Start now: confirm my numbers from MY-NUMBERS.md, then begin agent 1.
```

---

## Five rules that apply to every agent

1. **A person approves anything new before a customer sees it.** That includes each new ad: it goes to your approver first, and on their yes the ads agent launches it.
2. **Built for GoHighLevel.** `ROLLOUT-PLAN.md` maps every step to it. Other customer software works only if it can answer messages and texts by itself from pasted instructions, keep tags and fields, run automations started by a tag, and create tasks. Each agent file lists exactly what it needs.
3. **Your business texting line must be approved to send** before any automatic text will go out. Your texting provider handles this. Start it first, because it can take days.
4. **Nothing goes live until its test list passes.** Run every test on your own test contact only. Use your tool's test mode, or switch the automation on with a filter that lets only your test contact through, then switch it off again. For the tests, shorten long waits to a minute or two. Put the real waits back before you go live.
5. **Ad spend stays inside your monthly budget.** The ads agent moves money between ads by itself, never above the number you set. It starts in practice mode: it only tells your approver what it would change, until they say start. Every change is written down and sent to your approver as an alert. Your payment method and your ad account stay in a person's hands.

---

Want this installed for you? That is the Full Done-For-You Installation.
