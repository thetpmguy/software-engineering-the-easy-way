# 🔍 Audit Report — The Course, Reviewed From a Non-Technical Reader's Point of View

> This course promises that **confusion is our bug, not yours**. This page is us holding
> ourselves to that promise in public. It records how the course was reviewed, what we
> found, what we fixed, and what we're still watching. Audits are never "finished" —
> this is a living document, and your [confusion reports](../CONTRIBUTING.md) feed it.

**Last full audit:** 2026-07 · **Scope:** all 19 modules (lesson + lab + quiz + resources),
the capstone, every course-wide reference page, and all 15 homepage translations.

---

## The persona we audited as

We didn't review this as engineers. We reviewed it as **"the bakery owner"**: a smart,
busy, curious adult with *zero* technical background, reading on a phone, who will quietly
close the tab and blame themselves the moment a page makes them feel stupid. Every finding
below answers one question: *would that reader keep going, and feel smarter?*

## Overall verdict

**The course holds its core promise.** A determined non-technical reader can start at
Module 01 knowing nothing — not even what a file is — and arrive at the capstone able to
explain how software works, write small programs, and publish a live website. The writing
is consistently warm, analogy-first, and free of the gatekeeping language that sinks most
"beginner" material. The main residual risks are the ordinary ones for a resource like
this: external links rot over time, and real tool screens drift from written steps.

## What we checked, and the method

| Dimension | How we checked it |
|---|---|
| **Jargon leaks** (terms used before they're defined) | Read every lesson in reading order, in persona, flagging any term used before a bold plain-English definition. This is the #1 sin — it's how "no experience needed" quietly becomes a lie. |
| **Banned gatekeeping words** | Automated scan of all content for *simply, just do, obviously, clearly, easy, trivial* — the words that tell a stuck reader the fault is theirs. |
| **Analogy discipline** | Every abstract idea must have an everyday analogy **and** an honest note on where the analogy breaks down. Counted analogy blocks and breakdown notes per lesson. |
| **Self-check structure** | Every lesson needs "✅ Check yourself" boxes; every quiz needs 8–12 questions, hidden answers, and a final "explain it to a friend". Counted across all 19 modules. |
| **Zero-install labs** | Scanned every lab for any instruction to download, install, or pay for software. The promise is that a phone and a browser are enough. |
| **Link integrity** | Programmatically resolved every relative link in every `.md` file (English + translations) against the actual files on disk. |
| **Resource stability** | Listed every external domain and link type; favored large, stable, free providers over deep pages that 404. |
| **Factual trust** | Spot-checked the real-world stories the course leans on (Knight Capital, Mars Climate Orbiter, Grace Hopper's moth) and the runnable code starters. |
| **Global reach** | Watched for culture-locked references and jargon that wouldn't survive translation. |

## Findings

### ✅ Strengths confirmed (not just claimed)

- **No jargon cliff.** Modules open with a plain-language problem ("have you ever wondered
  why apps update so often?") before any terminology, and new terms are bolded and defined
  on first use, then collected in the [Glossary](../GLOSSARY.md).
- **Zero banned words in lesson content.** The automated scan came back clean across all
  modules and the capstone — no "simply", "obviously", "just do X", or "easy".
- **Analogies are honest.** Every lesson carries multiple 🌉 analogies, and each lesson
  includes at least one explicit "where this breaks down" note — so readers don't over-trust
  a metaphor. Signature analogies (restaurant = frontend/backend/API, CPU = chef, RAM =
  counter, OS = hotel manager, DNS = phone book, Git = time machine) are used consistently
  across modules rather than contradicting each other.
- **Every lab is genuinely zero-install.** No lab requires installing or paying for anything;
  all run in a browser, phone included. The one sign-up (GitHub) is flagged in advance as
  the single allowed exception.
- **Consistent self-testing.** All 19 quizzes have hidden-answer folds and end with an
  "explain it to a friend" prompt; every lesson has check-yourself boxes.
- **Honest where it counts.** The AI module is hype-free and explicit about hallucinations
  and limits; the careers module gives a realistic 12–24 month timeline rather than a
  "job-ready in 8 weeks" fantasy; every analogy admits its edges.

### 🟠 Medium-severity findings

| # | Where | Finding | Action |
|---|-------|---------|--------|
| M1 | All modules | A handful of lessons (notably 08 and 10) carry rich analogies but state the "where it breaks down" caveat less often than the strongest chapters (11, 06). Not a leak — a consistency gap. | **Watching.** Flagged for a future pass to add one explicit breakdown note per major analogy. No reader is misled today; the caveats that exist are correct. |
| M2 | `resources.md` (all) | Extra-resource links lean on a small set of providers (YouTube, Khan Academy, CS50, freeCodeCamp). Individual YouTube *videos* can be removed even when the channel survives. | **Accepted with mitigation.** We prefer playlists/channels over single videos, and each link has a one-line description so a reader can re-find it by searching if it moves. Dead links are treated as reportable bugs. |
| M3 | Labs referencing tool UIs | Labs that tour real tools (browser DevTools, GitHub's web editor, phone Settings, router pages) describe *intent* rather than exact buttons, but UIs still drift over time. | **Accepted by design.** Labs are written to survive small UI changes and say so; readers are told menus may move. |

### 🟢 Low-severity findings (fixed)

| # | Where | Finding | Action |
|---|-------|---------|--------|
| L1 | `CONTRIBUTING.md` | The "open an issue" link used a repo-relative path that only resolves on GitHub, not when reading the file locally/offline. | **Fixed** — replaced with the full GitHub issues URL. |
| L2 | Whole repo | Needed proof that every internal link actually resolves. | **Fixed/verified** — an automated pass now confirms every relative link across all English pages and all 15 translations resolves to a real file (this report was the last missing target). |

### 🌍 Translation note

The homepage is translated into 15 languages, each with links correctly rewired for its
folder depth and technical terms shown bilingually (local term + English in parentheses) so
learners recognize the words they'll meet in real tools and job posts. **The lessons
themselves are currently English-only**, and every translated homepage says so plainly, so
no reader is misled about what's available in their language. Translating the lessons is the
project's most-wanted contribution — see the [translation guide](../translations/README.md).

## Known limitations (stated honestly)

- **Link rot is inevitable.** With dozens of external resources, some will eventually move
  or vanish. We minimize it by linking stable homepages and series, and we rely on readers
  to [report dead links](../CONTRIBUTING.md).
- **Text-first, by choice.** The course has no video of its own. That keeps it searchable,
  translatable, low-bandwidth, and screen-reader friendly — but some learners prefer video,
  so every module points to good free videos.
- **English lessons only, for now.** See the translation note above.
- **An audit is a snapshot.** New content and edits can introduce new confusion. This report
  will be re-run and updated; treat any page that loses you as a bug we haven't caught yet.

## How you can help audit

You are the audit that matters most. If any sentence in this course made you feel lost or
stupid, that is a defect in *our* writing — please
[report it](../CONTRIBUTING.md). "I didn't understand this paragraph" is a complete,
genuinely valuable bug report, and it's how this course keeps its promise to every reader.
