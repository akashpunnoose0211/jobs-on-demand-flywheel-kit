# Set up Claude Code (for beginners)
**Jobs-On-Demand Flywheel Kit · read this first if you have never used Claude Code**

> Claude Code is the AI that installs the kit with you. It works on your own computer: it reads the kit's files, asks you questions, builds what it can, and tells you exactly where to click for the rest. This guide gets you from nothing to "start" in about 20 minutes. No coding needed.

## What you need
- A Mac or Windows computer. A phone or tablet is not enough.
- A paid Claude plan. Pro (about $20 a month) is enough to start; Max gives you more use per day. Prices change, so check claude.com/pricing.
- The kit: the GitHub link from your thank-you page, or the zip.

## The easy way: the Claude desktop app (no typing commands)

1. `You` **Make your Claude account and pick a plan.** Go to claude.ai, sign up with your business email, then choose Pro or Max in Settings, then Billing.
   Done when: your account shows the paid plan.

2. `You` **Download the Claude desktop app.** Go to claude.ai/download, install it, and sign in.
   Done when: the app opens and shows your name.

3. `You` **Open the Code tab.** In the desktop app, switch to **Code** (that's Claude Code inside the app). If it asks for a folder, keep reading.
   Done when: you see a box to type in and a button to pick a folder.

4. `You` **Put the kit on your computer.** Pick one:
   - **Zip:** download it from your thank-you page, double-click it to unzip, and move the folder to `Documents`.
   - **GitHub:** open the GitHub link, click the green **Code** button, then **Download ZIP**, then unzip it the same way.
   Done when: a folder called `jobs-on-demand-flywheel-kit` sits in your Documents.

5. `You` **Open the kit folder in Claude Code.** Pick that folder when the Code tab asks which folder to work in.
   Done when: you type "what files are in this folder?" and it lists START-HERE.md, INSTALL-GUIDE.md and the agents and setup folders.

6. `You` **Type "start".** Claude Code reads the kit's instructions by itself and picks up at phase 2 of the install guide (`INSTALL-GUIDE.md`, in the main kit folder).

## The other way: Claude Code in the terminal
Use this only if you like typing commands. Everything else in the kit works the same.

1. **Open the terminal.** Mac: press Command and Space, type "Terminal", press Return. Windows: press the Windows key, type "PowerShell", press Return.
2. **Install Claude Code.** Paste the install command shown at claude.com/claude-code for your computer, then press Return.
3. **Go to the kit folder.** Type `cd ` (with a space), drag the kit folder into the window, and press Return.
4. **Start it.** Type `claude` and press Return. The first time, it opens your browser so you can sign in.
5. **Install the kit as a plugin (optional, makes the agents one sentence each).** Inside Claude Code, type the two `/plugin` lines from the kit's README.
6. **Type "start".**

## Five things every beginner should know
- **Claude Code asks before it acts.** You will see boxes asking to allow it to read a file, make a file or run a command. Allow reading and writing inside the kit folder. If you don't understand a request, don't allow it yet. Type "what does this do, in plain words?" first.
- **It never touches your accounts without a key you give it.** On day 1 it asks for a GoHighLevel key so it can build fields and tags for you. It shows you where to make the key and keeps it out of the kit's files and out of the chat.
- **Your progress is saved.** Claude Code keeps a file called `PROGRESS.md` in the kit folder. Close the app any time. When you come back, open the same folder and type "what's next?".
- **Plain words work best.** "I'm stuck on day 3, step 2. I see a page that says X" gets you the fastest help. You can paste a screenshot too.
- **Nothing goes live by itself.** Every agent is built switched off and tested on your own phone. Nothing reaches a customer until you say yes.

## Using Codex instead
Codex (OpenAI's version, with a paid ChatGPT plan) works the same way: install the Codex app, open the kit folder, and type "start". The kit's `AGENTS.md` file gives Codex the same instructions Claude Code gets.

## If something goes wrong
| What you see | What to do |
|---|---|
| "Please log in" or a sign-in loop | Sign out of claude.ai in your browser, sign back in, then reopen the app. |
| It can't find the kit's files | You opened the wrong folder. Open the `jobs-on-demand-flywheel-kit` folder itself, not the folder around it. |
| "Usage limit reached" | You've used up your plan for now. Wait for the reset time it shows, or move up to Max. |
| It asks for something you don't have | Say "I don't have that. What's the simplest way around it?" |

Done when: Claude Code is open in the kit folder and has started the install guide.
