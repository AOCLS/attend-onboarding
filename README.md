# Welcome to the `attend` project

**Onboarding for first-year medical students**
Dr. Joseph Kingston's laboratory · Noorda College of Osteopathic Medicine

We study how AI agents change clinical work — and whether they support or
quietly erode a physician's ability to oversee them.

**You do not need any programming background.** You need a laptop, three
accounts, and a willingness to ask questions when something doesn't make sense.
Everything here is written for someone who has never opened a terminal.

---

## ⚠️ If you read only one thing, read this

Three rules. These are not bureaucratic boxes — breaking the first one can end
a medical career before it starts.

> ### 1. Never use real patient data. Anywhere.
> Not in code. Not in a screenshot. Not in a Teams message. **Not pasted into
> Claude, ChatGPT, or any other AI tool.** Not data you de-identified yourself.
> We build only against *synthetic* patients — realistic fake people.
>
> ### 2. Nothing we build touches a real patient until it clears IRB review and Noorda IT.
> Prototypes stay prototypes. Don't install our code on a clinic machine. Don't
> demo it with a real chart — not even your own.
>
> ### 3. Finish your CITI research-ethics training before doing human-subjects work.
> Ask Dr. Kingston which modules this project requires, then send him your
> completion certificate.

**When you're unsure, ask before you act.** Nobody has ever gotten in trouble
here for asking a question. People get in trouble for guessing.

---

## What you'll do today

About **75 minutes**, and most of that is waiting on accounts to activate.
Do the steps in order — each one depends on the last.

| | Step | Time |
|---|---|---|
| 1 | [Check your Noorda-COM account](#step-1--your-noorda-com-account) | ~10 min |
| 2 | [Create a GitHub account](#step-2--github) | ~20 min |
| 3 | [Install Claude Code](#step-3--claude-code) | ~30 min |
| 4 | [Run the project on your laptop](#step-4--run-the-project) | ~15 min |

New to any of these words? The **[Glossary](GLOSSARY.md)** defines every term in
plain English. It's fine to keep it open in another tab.

---

## Step 1 — Your Noorda-COM account

⏱ **~10 minutes**

**Why:** it's how you reach Teams (where the lab talks), your email, and CITI
training.

### You don't sign up for this one

Your Noorda account is **created for you when you matriculate.** You're not
registering — you're confirming credentials you already have. If you can get
into Canvas, you already have it.

### Confirm it works

1. Go to **<https://myapps.microsoft.com/>** — the portal that fronts nearly
   every Noorda system.
2. Sign in with your Noorda-COM email and password.
3. Complete multi-factor authentication if prompted. **Use the Microsoft
   Authenticator app on your phone rather than text messages** — it's faster and
   works when you have no signal.
4. You'll land on a dashboard of app tiles.

### What you need from it for this project

- **Teams** — where all lab discussion happens. Not personal text messages.
- **Outlook** — your Noorda email. You'll use it in Step 2.
- **CITI Program** — research ethics training (see Rule 3).

✅ **You're done when:** you can open Teams and you've found the lab channel and
said hello.

🆘 **If it doesn't work:** email the IT helpdesk at **helpdesk@noordacom.org**
with your full name, student ID, and what you see when login fails. Library
resources: **library@noorda.edu**. Main line: **385-378-5201**.

> 💡 The college's [Tech Ready Guide](https://noordacom.libguides.com/techreadyguide)
> documents every system Noorda provides. Worth ten minutes even if you think
> you know it all.

---

## Step 2 — GitHub

⏱ **~20 minutes**

**Why:** GitHub is where our code lives. Think of it as a shared folder that
remembers every change anyone ever made, and who made it. You'll use it to get
the project and to submit your own work.

### Create your account

1. Go to **<https://github.com/signup>**.

2. **Choose your username carefully.** Your real name or a close variant. This
   becomes a professional identity attached to published work and visible to
   residency programs — it is not a gamertag. You cannot cleanly change it later.

3. **Register with your *personal* email**, not your Noorda one. Then add your
   Noorda address as a secondary in *Settings → Emails*. Your school account
   gets deactivated when you graduate; you want to keep your work.

4. Verify your email address.

### Turn on two-factor authentication — this is required

*Settings → Password and authentication → Two-factor authentication.* Use an
authenticator app.

GitHub requires 2FA for contributors, so **you will be locked out of our project
without it.**

> 🔑 **Save your recovery codes somewhere you will actually find them again** —
> a password manager, not a screenshot buried in your camera roll. If you lose
> both your phone and your codes, the account is gone permanently.

### Get the Student Developer Pack — free, start it now

<https://education.github.com/pack> gives students free professional tools,
including GitHub Copilot. Verify with your Noorda email or student ID.

**Approval can take several days,** so submit it before you need it.

### Post your username in Teams

Tell Dr. Kingston your GitHub username in the lab channel so you can be added to
the project. **The repository is private — you can't see the code until someone
grants you access.**

✅ **You're done when:** 2FA is on, recovery codes are saved somewhere safe, and
your username is posted in Teams.

---

## Step 3 — Claude Code

⏱ **~30 minutes**

**Why:** Claude Code is an AI coding assistant that runs in your terminal. On
this project it's both a tool we use *and* part of what we study.

> 💳 **Before you install:** ask Dr. Kingston which account or plan the lab uses.
> Claude Code needs a paid Claude subscription or API access, and the lab may
> already have one for you. **Don't put a personal subscription on your own
> credit card assuming you'll be reimbursed.** Check first.

### First, open a terminal

A terminal is a text window where you type commands instead of clicking things.

- **On a Mac:** press `Cmd + Space`, type `Terminal`, press Return.
- **On Windows:** press the Start key, type `PowerShell`, open **Windows
  PowerShell**. Check that the prompt starts with `PS C:\` — the older black
  `cmd` window will not work.

Never used one? Read Anthropic's
**[terminal guide for new users](https://code.claude.com/docs/en/terminal-guide)**
first. Fifteen minutes there saves hours of confusion later.

### Install it

**Mac or Linux** — copy this whole line, paste it into the terminal, press Return:

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

**Windows (PowerShell):**

```powershell
irm https://claude.ai/install.ps1 | iex
```

**Then close the terminal window and open a new one.** The install won't take
effect in the old one.

<details>
<summary>Alternative: install with npm (only if you already have Node.js 22+)</summary>

```bash
npm install -g @anthropic-ai/claude-code
```

**Do not put `sudo` in front of this.** It causes file-permission problems that
are genuinely annoying to undo. If npm complains about permissions, use the
native installer above instead.
</details>

### Start it

```bash
claude
```

A browser window opens for sign-in. Follow it, come back to the terminal, and
you'll get a prompt.

**Type a question in plain English and press Return.** Claude Code is
conversational — there are no commands to memorize. Type `/help` any time to see
what it can do.

Anthropic's [quickstart](https://code.claude.com/docs/en/quickstart) is the best
next thirty minutes you can spend.

✅ **You're done when:** typing `claude` opens a prompt and it answers a question.

### Using it responsibly here

- **Rule 1 applies double.** Never paste patient data into Claude Code or any
  AI tool. Synthetic data only.
- **Read what it writes.** You are responsible for code submitted under your
  name. *"Claude wrote it"* is not a defense in a code review — and it would not
  be a defense in a clinical setting either.
- **Notice yourself using it.** Our research question is whether AI tools erode
  the human oversight they depend on. The moment you catch yourself approving
  output you didn't really read, that's **data**. Bring it to lab meeting.

---

## Step 4 — Run the project

⏱ **~15 minutes**

Ask in Teams for the repository address, then type these lines one at a time:

```bash
# Go to wherever you keep your work, for example:
cd ~/Documents

# Paste the address you got from Teams in place of <REPOSITORY-URL>
git clone <REPOSITORY-URL>
cd noorda-kickoff-demo
```

Start the prototype:

```bash
cd attend-hpi
./serve.sh
```

Now open **<http://localhost:8088>** in Google Chrome.
(`localhost` means *your own computer* — this is not on the internet.)

You should see a patient intake screen with a synthetic patient loaded. Work
through an intake, then switch to **Physician review** with the toggle at the
top right.

Check that the tests pass:

```bash
npm test
```

You should see **`11 passing`**.

✅ **You're done when:** the app loads in Chrome and the tests pass.

🆘 **If a test fails on a fresh copy, that is useful information, not your
fault.** Paste the full output in Teams.

### Then read the README

Open **`attend-hpi/README.md`** in the project folder. It explains what the
prototype does and — more importantly — *why* it's built the way it is. Those
design constraints are the actual intellectual content of this project.

---

## ✅ Day-one checklist

- [ ] Signed in at <https://myapps.microsoft.com/>, MFA working
- [ ] Found the lab channel in Teams and introduced myself
- [ ] Started CITI training (asked Dr. Kingston which modules)
- [ ] GitHub account created with a professional username
- [ ] GitHub 2FA on, **recovery codes saved somewhere safe**
- [ ] GitHub username posted in Teams
- [ ] Student Developer Pack application submitted
- [ ] Confirmed with Dr. Kingston which Claude plan to use
- [ ] Claude Code installed, `claude` runs and answers
- [ ] Repository cloned, app loads, `npm test` shows 11 passing
- [ ] Read `attend-hpi/README.md`
- [ ] Read the project paper (below)

---

## What we're actually researching

Start with **Mitchell, Ghosh & Passi, _AI Agents Push Humans Out of the Loop_**
([arXiv:2608.23642](https://arxiv.org/abs/2608.23642)).

Read it as **an argument to be tested, not a result to be cited** — it's a
position paper, not an experiment. Its central claim: *the act of overseeing an
AI system degrades the very capacities that oversight requires.* A tired
reviewer approves faster, and a system trained on approvals learns to produce
output that's easy to approve.

Our first prototype, `attend-hpi`, drafts a patient history from intake answers
while keeping **every single sentence traceable back to the exact question the
patient was asked**. Every design decision in it is a bet about physician
attention. Some of those bets are probably wrong. Finding out which ones is the
work.

### A note on being new

That paper argues the harm from these tools falls hardest on **novices** — people
who may never build the skills they'd need to catch the tool's mistakes, because
the tool was always there. Then it offers no solution for that group.

You are that group.

Your perspective on this isn't a limitation to work around. It's the most
interesting vantage point in the lab, and it's one the literature is currently
missing. **Say what you notice.**

---

## Getting help

| Problem | Where to go |
|---|---|
| Can't log into a Noorda system | **helpdesk@noordacom.org** |
| Library databases, Tech Ready Guide | **library@noorda.edu** |
| GitHub access to the repository | **Lab Teams channel** |
| Code won't run, a test fails | **Lab Teams channel** — paste the full error |
| Claude Code billing or which plan | **Dr. Kingston** |
| Anything involving real patient data | **🛑 Stop. Ask Dr. Kingston first.** |

**How to ask well:** paste the *entire* error message, say exactly what you
typed, and say what you expected to happen. "It doesn't work" can't be debugged.

Nobody expects you to solve things alone. **An hour of being stuck in silence
helps no one** — ask at fifteen minutes.

---

## Also in this repo

- **[GLOSSARY.md](GLOSSARY.md)** — every technical term in plain English

---

*Onboarding documentation only. This repository contains no patient data, no
protected health information, and no project source code.*
