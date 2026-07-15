# ✅ Quiz 08 — Git & GitHub

Answer in your head or on paper, then open the fold to check.

---

**1. What problem does version control solve? Answer using the
"essay_final_FINAL_v3_REALLYFINAL.docx" situation.**

<details><summary>Show answer</summary>

Saving endless renamed copies "works" for one person but records nothing: you can't see
what changed between copies, why, or who changed it — and it collapses completely when
many people edit the same files. Version control records every change with its author,
time, and reason, and lets you rewind to any version. One set of files, full history, no
FINAL_v3.
</details>

---

**2. Git vs. GitHub — which is which?**

<details><summary>Show answer</summary>

**Git** is the tool: a program that tracks the complete history of a project's files.
**GitHub** is a website: the place online where copies of Git projects live so people
can share and collaborate on them. The analogy: Git is Word (the tool you work with),
GitHub is Google Drive (the shared place online). And remember the analogy's limit —
with Git, everyone holds a *complete* copy of the project and its history, not a
fragment that lives only online.
</details>

---

**3. What is a repository?**

<details><summary>Show answer</summary>

One project's complete home: all its files plus the entire recorded history of every
change ever made. The project's binder — current pages up front, every past draft
preserved behind them.
</details>

---

**4. A commit is a snapshot plus something else. What — and why does that second part
matter so much?**

<details><summary>Show answer</summary>

Plus a **message** saying what changed and why — the note in the lab notebook. It
matters because six months later, the snapshot alone tells you *what* the files were,
but only the message tells you *why* they changed. "Changed stuff" helps nobody;
"Increase button size so it's tappable on small phones" is a gift to your teammates and
your future self.
</details>

---

**5. Your teammate is about to try a risky redesign. Using the recipe analogy, what
should they do first, and what is it called in Git?**

<details><summary>Show answer</summary>

Make a photocopy of the recipe and experiment on the copy, so the original stays safe.
In Git: create a **branch** and commit the risky work there, leaving the `main` branch
untouched and working. If the experiment fails, discard the branch — nothing of value
lost.
</details>

---

**6. What is a merge, and when does a merge conflict happen?**

<details><summary>Show answer</summary>

A **merge** combines the changes from one branch into another — folding your improved
photocopy back into the master cookbook. A **merge conflict** happens when two branches
changed the *same lines*: Git refuses to guess which version is right, and a human must
look at both and decide.
</details>

---

**7. True or false: a merge conflict means someone made a serious mistake.**

<details><summary>Show answer</summary>

**False.** A conflict means two people did normal work that happened to touch the same
lines. Git stops and asks a human to choose — that's the tool being appropriately
careful, not anyone failing. On busy teams it happens all the time and is resolved as
routine housekeeping.
</details>

---

**8. What is a pull request, and what happens during code review?**

<details><summary>Show answer</summary>

A **pull request** is a request on GitHub saying "here are my changes, side by side with
the current version — please review before we merge." During **code review**, teammates
read the changes, comment on specific lines, suggest improvements, and approve — like
writers editing each other's drafts. It catches problems early and spreads knowledge of
the code across the team. Only after approval does the branch merge.
</details>

---

**9. What's the difference between cloning a repo and forking it?**

<details><summary>Show answer</summary>

**Clone** = download a complete copy of a repo (files and full history) to work with.
**Fork** = create your own separate copy of *someone else's* project on GitHub itself,
under your account, which you're free to change — and from which you can offer
improvements back via a pull request. Forking is how strangers contribute to projects
they don't control.
</details>

---

**10. How can thousands of strangers who never meet safely build one piece of software
together (like Linux)?**

<details><summary>Show answer</summary>

With exactly this module's machinery: anyone can **fork** the project and improve their
own copy; they offer changes back through a **pull request**; maintainers **review**
every change before it merges; and the **history** records every change and its author
forever. Nothing enters the shared version unreviewed, and nothing is ever silently
lost — so trust doesn't have to come first; the process provides it.
</details>

---

**11. Why might an employer look at your GitHub profile, and what do they hope to see?**

<details><summary>Show answer</summary>

Because a résumé *claims* skills, while a GitHub profile *shows* them: real projects,
commits over time, and code others can read. They're not looking for something
spectacular — a few small, honest projects with clear commit messages already signal
genuine skill and care.
</details>

---

**12. 🗣️ Explain it to a friend**

A friend who writes novels asks: *"My co-author and I email drafts back and forth and
it's chaos — we keep overwriting each other. You said programmers solved this?"*

Explain version control to them in under a minute, using no jargon — then tell them the
two or three ideas from it they'd want (snapshots, safe experiments, reviewing changes).

<details><summary>One possible answer</summary>

"They did solve it — it's called version control, and it's a time machine plus a lab
notebook for files. Instead of emailing copies, the book lives in one shared place, and
every time either of you finishes a chunk, you save a snapshot with a note — 'rewrote
the ending of chapter 3, sadder now.' Nothing is ever lost: you can flip back to any
snapshot from any day. Want to try a risky rewrite? You work on a private copy — like
photocopying the manuscript to scribble on — while the real version stays safe, and if
the rewrite works, the system folds it back in. And if you both edited the very same
paragraph, it doesn't silently overwrite anyone — it shows both versions and makes you
choose. Best of all, before changes become official, your co-author can see exactly
what you changed, line by line, and comment on it. It's the drafts-and-margin-notes
system you already wish you had, run by a machine that never forgets."
</details>
