# ⏰ Module 08 — Git & GitHub: The Time Machine for Teamwork

> **What you'll learn:** how thousands of people edit the same giant pile of code every
> day without destroying each other's work — using a "time machine for files" called
> Git, and a collaboration website called GitHub. You'll learn what commits, branches,
> merges, and pull requests are, entirely through everyday analogies.
>
> **Why it matters:** Git and GitHub are used by essentially every software team on
> Earth. In the lab, you'll create your own GitHub account and make your first real
> commits — the same actions professional engineers do dozens of times a day. Many
> employers look at GitHub profiles the way they look at résumés.

---

## 🧠 The problem: essay_final_FINAL_v3_REALLYFINAL.docx

Be honest. Somewhere on a computer you own, there is a folder that looks like this:

```
essay.docx
essay_final.docx
essay_final_v2.docx
essay_final_FINAL.docx
essay_final_FINAL_v3_REALLYFINAL.docx
```

Everyone has lived this. You kept copies because you were afraid — afraid of losing a
version that worked, afraid of changing something you couldn't undo. And the copies
"solved" it in the messiest possible way: now you have five files, no record of *what*
changed between them or *why*, and no idea which one your cousin edited.

Now scale the problem up. A large app is a "document" of **ten million lines**, edited
by **3,000 people**, every single day, often the *same files* on the same day. If they
used the FINAL_v3 method, the company would collapse by lunchtime.

Software's answer to this problem is one of its most elegant inventions. **Version
control** is a system that records every change ever made to a set of files — who made
it, when, and why — and lets you jump back to any previous version at any time. It's a
time machine plus a lab notebook: the time machine lets you travel back; the notebook
tells you what happened at every step and who did it.

## 🆚 Git vs. GitHub — the tool vs. the meeting place

Two names, endlessly confused, and the distinction matters. Let's nail it down early.

- **Git** is the version-control *tool* itself — a free program that tracks the history
  of your files. It runs on your own computer (or, in our labs, behind a website's
  browser buttons). Git was created in 2005 by Linus Torvalds, the same person who
  created Linux.
- **GitHub** is a *website* where copies of Git projects live online, so people anywhere
  can share them and work on them together. It's a company (owned by Microsoft), and the
  world's largest gathering place for code — well over 100 million people have accounts.

> 🌉 **Analogy:** Git is to GitHub as **Word is to Google Drive**. Word is the tool you
> write with; Drive is the place online where documents live so others can reach them.
> You can use Word without Drive. You can't do much with an empty Drive and no writing
> tool.
>
> **Where the analogy breaks down:** with Git, every person has a *complete copy* of
> the entire project and its full history on their own machine — not a fragment that
> lives only online. If GitHub vanished tomorrow, every engineer with a copy would still
> have everything. GitHub also isn't the only such website (GitLab and Bitbucket are
> rivals) — it's the most popular one.

> ✅ **Check yourself**
> 1. What problem does version control solve, in one sentence?
> 2. Is GitHub a tool or a website? What about Git?
>
> <details><summary>Show answers</summary>
>
> 1. It records every change to a set of files — who, when, and why — so a team can work
>    on the same files without chaos and can rewind to any past version.
> 2. GitHub is a website (a meeting place where copies of projects live online). Git is
>    the tool that actually tracks the file history. Word vs. Google Drive.
> </details>

## 📚 The core ideas, one analogy at a time

Git has a small vocabulary of ideas. Each one maps to something you've done in ordinary
life. Take these slowly — this list *is* the module.

### The repository — the project's binder

A **repository** (everyone says **repo**) is one project's complete home: all its files,
plus the entire recorded history of every change ever made to them. Think of it as the
project's big three-ring binder — the current pages up front, and every past draft and
margin note preserved behind them. One project, one repo.

### The commit — a saved snapshot, plus a note

A **commit** is a saved snapshot of your project at one moment, together with a short
written message saying what you changed and why. When your work reaches a good point,
you *commit*: click goes the camera, and a line goes in the lab notebook — *"Fixed the
typo in the welcome message."*

If you've ever played a video game, you already have the right instinct: a commit is a
**saved game**. Reach a checkpoint, save, and no matter what disaster happens next, you
can reload from there.

Commit messages matter more than beginners expect. Six months later, "changed stuff" is
useless; "Increase button size so it's tappable on small phones" is a gift to your
future self and your teammates. The notebook is only as good as its notes.

### History — flipping back through the snapshots

Every commit is kept, forever, in order. The **history** of a repo is that full sequence
of commits — and you can flip back through it like pages: see the project as it was last
Tuesday, see exactly which commit changed a given line and what the message said. The
fear that drove essay_final_FINAL_v3 evaporates. Nothing committed is ever lost, so you
can change anything with confidence.

### The branch — a photocopy of the recipe

Suppose the team's app works today, and you want to try a risky experiment — a redesign
of the whole menu screen. You don't dare wreck the working version.

> 🌉 **Analogy:** You make a photocopy of the recipe and experiment on the copy. Scribble
> on it, cross things out, try paprika. The original recipe stays safe in the book the
> whole time. If your experiment is a disaster, throw the photocopy away — nothing of
> value was lost.

A **branch** is exactly this: a parallel line of work inside the repo, where you can
make commits freely without touching the main version. The main version lives on a
branch usually called **main**. Teams create a new branch for each new feature or fix,
which means dozens of experiments can proceed at once, none endangering the others.

### The merge — combining the photocopy back in

Your paprika experiment worked. Time to make it official: copy your improvements back
into the master cookbook. In Git this is called a **merge** — taking the changes from
one branch and combining them into another. Git does the combining automatically, and
it's cleverer than you'd expect: if you changed the recipe's step 3 and a teammate
changed step 7, Git merges both edits without complaint.

### The merge conflict — two people edited the same line

But what if you changed step 3 to "add paprika" and your teammate changed *the same
step 3* to "add cumin"? Git is a tool, not a chef. It cannot know which is right — so it
stops and asks a human. That situation is a **merge conflict**: two branches changed the
very same lines, and a person must look at both versions and decide (paprika, cumin, or
both).

Hear this clearly, because it saves beginners real anxiety: **a merge conflict is not a
disaster, an error, or anyone's fault.** It's Git being appropriately humble — refusing
to guess about your work. On a busy team, conflicts happen weekly. Resolving one is
ordinary housekeeping, like two editors comparing margin notes.

### The pull request — "please review my changes"

On a real team, you don't merge your branch the instant you're done. First, you show
your work. A **pull request** (a **PR**) is a request you open on GitHub that says:
*"Here are my changes, side by side with the current version — would someone please
review them before we merge?"* Teammates read the changes, leave comments on specific
lines ("what happens if the list is empty?"), request tweaks, and finally approve.
Then — merge.

This ritual is called **code review**, and it's how quality survives at scale. Think of
writers exchanging drafts: not because anyone's a bad writer, but because every draft
improves under a second pair of eyes. On healthy teams, *everyone's* code gets reviewed,
from the newest hire to the most senior engineer. It also quietly spreads knowledge: the
reviewer now understands a corner of the project they didn't write.

### Clone and fork — checking out your own copy

Two last words you'll meet constantly. To **clone** a repo is to download a full copy of
it — files *and* entire history — to work with. To **fork** a repo is to make your own
separate copy of someone else's project *on GitHub itself*, under your account, which
you're then free to change. Forking is how strangers contribute to projects they don't
control: fork it, improve your copy, then open a pull request offering the improvement
back to the original.

> ✅ **Check yourself**
> 1. What two things does a commit contain?
> 2. Why do teams work on branches instead of editing main directly?
> 3. A merge conflict just appeared. Should you panic?
>
> <details><summary>Show answers</summary>
>
> 1. A snapshot of the project at that moment, plus a short message saying what changed
>    and why. A saved game with a note.
> 2. So risky, unfinished work can proceed on a "photocopy" while the original stays
>    safe and working. Many experiments can run at once without endangering each other.
> 3. No. It only means two branches changed the same lines and Git refuses to guess
>    which version is right. A human looks at both and chooses. It's routine.
> </details>

## 🌍 How strangers build software together

Here's where it gets genuinely wonderful. Some of the most important software on Earth —
Linux (which runs most of the internet's servers and every Android phone), Firefox,
Python, the encyclopedia-like sprawl of tools behind nearly every app you use — is
**open source**: software whose code is public for anyone to read, use, and improve.

Stop and consider how strange that is. Thousands of strangers, across every time zone,
many of whom never meet, jointly editing the same code — and producing software that
runs the world. It works because of exactly the machinery you just learned. Anyone can
**fork**, improve their copy, and open a **pull request**. Maintainers **review** it.
Nothing merges without scrutiny, and every change is recorded forever in the
**history**. Git and GitHub are the town square, the ballot box, and the archive all at
once. It's Wikipedia's model — strangers collaborating in public — but for the code that
runs civilization.

And here's a small delight: **this very course lives in a Git repository.** The page
you're reading is a file with commits behind it. If you spot a confusing sentence, you
could — using nothing beyond what this module teaches — fork the course, fix the
sentence, and open a pull request. That's not a metaphor. That's an invitation.

## 💼 Why employers care about your GitHub

A résumé says "I know things." A GitHub profile *shows* them: projects you've built,
commits over time, contributions to other people's projects, code others can actually
read. Many hiring managers glance at a candidate's GitHub before an interview. You don't
need a spectacular one — even a few small, honest projects with clear commit messages
signal real skill and real care. In this module's lab, you'll create yours and put your
first commits on it — and, if you do the bonus, publish a live website from it.

## 🎁 Recap

- **Version control** records every change to a project — who, when, why — and lets you
  rewind. A time machine plus a lab notebook. It's how 3,000 people edit 10 million
  lines without chaos.
- **Git** is the tool; **GitHub** is the website where copies live and people
  collaborate. Word vs. Google Drive.
- A **repository** is a project's binder. A **commit** is a snapshot plus a note (a
  saved game). **History** is the full flip-book of commits.
- A **branch** is a photocopy of the recipe for safe experiments; a **merge** folds the
  improvements back into the cookbook; a **merge conflict** means two people edited the
  same line and a human must choose — normal, not a disaster.
- A **pull request** says "please review my changes"; **code review** is editing each
  other's drafts. **Clone** = download a full copy; **fork** = make your own copy of
  someone else's project to build on.
- Open source — Linux and friends — is strangers worldwide using these exact tools to
  build shared software in public. This course is in a Git repo too.

## 🚪 Next up

You can now save every version of your work and collaborate without fear. Which frees
you to confront an uncomfortable truth: no matter how carefully anyone works, **all
software has bugs** — including a bug that once cost a company $460 million in 45
minutes. Why? And what do the armies of tests actually do? That's next.

**Next:** [Module 09 — Why Software Breaks: Bugs, Testing & Quality](../09-bugs-and-testing/README.md)
