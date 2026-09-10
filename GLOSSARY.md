# Glossary

Plain-English definitions for every technical term in the
[onboarding guide](README.md). Nobody is born knowing these.

## Using a computer like a programmer

**Terminal** (also *command line*, *shell*, *PowerShell*)
A text window where you type commands instead of clicking buttons. It looks
intimidating and mostly isn't. On a Mac it's called Terminal; on Windows,
PowerShell.

**Command**
A line of text you type into the terminal, then press Return to run.

**`cd`**
"Change directory" — moves you into a different folder. `cd ~/Documents` moves
into your Documents folder.

**localhost**
Your own computer, acting as a website. When a guide says open
`http://localhost:8088`, that page is running on *your machine*. It is not on
the internet and nobody else can see it.

## Git and GitHub

**Git**
Software that tracks every change to a set of files, forever. It's the "track
changes" of software, except it never loses anything.

**GitHub**
A website that hosts Git projects so a team can share them. Git is the tool;
GitHub is the place.

**Repository** (*repo*)
One project's folder, with its complete history. Ours is called
`noorda-kickoff-demo`.

**Clone**
Download your own full copy of a repository, history included.

**Commit**
A saved snapshot of your changes, with a short note explaining what you changed
and why. Roughly a lab-notebook entry.

**Branch**
A parallel version of the project where you can work without disturbing anyone
else's copy.

**Pull request** (*PR*)
Formally proposing your changes so a teammate can review them before they become
part of the real project. This is where feedback happens — expect comments, and
don't take them personally.

**Two-factor authentication** (*2FA*)
A second proof of identity beyond your password, usually a code from a phone app.
GitHub requires it.

**Recovery codes**
One-time backup codes that get you into your account if you lose your phone.
Save them somewhere real. Losing them along with your phone means losing the
account permanently.

## Healthcare software

**EHR** — Electronic Health Record
The software a clinic runs on: charts, orders, notes. athenahealth, Epic, and
Cerner are common ones.

**FHIR** (pronounced "fire") — Fast Healthcare Interoperability Resources
The standard format EHRs use to exchange health data, so an app can read a
medication list without being custom-built for one vendor.

**SMART on FHIR**
The standard for apps that launch *inside* an EHR — how our prototype would
appear as a screen within athenaOne rather than a separate website.

**HPI** — History of Present Illness
The narrative paragraph describing why the patient came in. What our prototype
drafts.

**ROS** — Review of Systems
The checklist of symptoms across body systems. "Patient denies fever, chills,
night sweats" is a review of systems.

**Pertinent negative**
A symptom the patient specifically *doesn't* have, that matters anyway. Chest
pain *without* shortness of breath is a different picture than chest pain with
it — so the absence is worth writing down.

## Research and compliance

**PHI** — Protected Health Information
Any information that could identify a real patient. Names and dates of birth,
but also addresses, phone numbers, medical record numbers, dates of service,
and photographs. Legally protected under HIPAA. **Never goes in our code, our
messages, or any AI tool.**

**Synthetic data**
Fabricated patients that look and behave like real ones. Carries no privacy
risk. The only data we develop against.

**De-identified data**
Real patient data with identifiers stripped out. **Still not something you
handle on your own judgment** — re-identification is easier than people expect,
and this needs approval.

**IRB** — Institutional Review Board
The committee that reviews and approves research involving human subjects.
Nothing touches a patient without it.

**CITI Program**
The standard online research-ethics training. Required before human-subjects
work. Available through your Noorda accounts.

## AI terms you'll hear in lab meeting

**LLM** — Large Language Model
The kind of AI behind Claude and ChatGPT. Predicts text; doesn't look anything
up unless given a tool to do so.

**AI agent**
An AI system that takes multi-step *actions* — running code, editing files,
calling other software — rather than only answering a question.

**Hallucination**
When a model states something false with complete confidence. The central safety
problem in clinical AI, and the reason our prototype has no generative model in
the part that writes the note.

**Human in the loop** (*HITL*)
A person positioned to review, approve, or override what an automated system
does. Whether that person can *actually* do so meaningfully is our research
question.

**Automation bias**
The documented tendency to accept a computer's suggestion even when it's wrong —
and even when you had the information needed to catch it.

**Anchoring**
Latching onto the first idea you encounter and adjusting insufficiently
afterward. It's why our prototype deliberately shows you *no* suggested
diagnosis: so you form your own impression first.

**Deskilling**
Losing a skill through disuse because a tool always did it for you. The reason
the paper worries most about people who are new.
