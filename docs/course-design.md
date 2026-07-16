# 🏗️ Course Design Notes (Working Document)

This document explains *how and why* this course is built the way it is. It's the
"engineering behind the teaching" — kept public because transparency makes the course
better and because it's a useful example of a design doc (Module 07 explains what design
docs are!).

## The problem we're solving

Almost every software course fails non-technical people in one of three ways:

1. **The invisible ladder.** It claims "no experience needed", then uses words like
   *runtime*, *compile*, or *terminal* in lesson two without explanation. The learner
   assumes *they* are the problem. They are not.
2. **Trivia without a map.** It teaches syntax ("here's a for-loop") without ever
   explaining where code lives, how it becomes an app, or why any of it matters.
3. **Toy isolation.** Exercises produce nothing real, so nothing is retained and nothing
   can be shown to anyone.

## Our design principles

| Principle | How it shows up in the course |
|---|---|
| **Zero assumed knowledge** | Module 01 starts at "what is a computer". Every term is defined on first use *and* in the [Glossary](../GLOSSARY.md). |
| **Analogy-first teaching** | Every abstract idea is anchored to daily life *before* the technical version. Rules in the [Style Guide](style-guide.md). |
| **Whole map before details** | Parts 1–3 give the complete picture (machine → thinking → how software is built) before Part 4 goes deep. Learners always know where they are. |
| **Do, don't just read** | Every module has a browser-based lab. No installs, no cost, works on a phone. |
| **Spaced self-testing** | Every module has a quiz with answers, plus "explain it to a friend" prompts (retrieval practice — the best-evidenced learning technique). |
| **Real artifacts** | Learners publish a real website (Module 08 lab + capstone) and automate something from their own life. |
| **Honest about limits** | Every analogy states where it breaks down. The AI module is hype-free. The careers module is realistic about timelines. |

## Curriculum architecture

The course is a **narrative in six acts**, not a topic list:

1. **Part 1 — The Machine:** demystify the physical world (computer, software, internet).
   Emotional goal: *"It's not magic. It's machinery I can understand."*
2. **Part 2 — Thinking:** install the engineer's mindset and first code.
   Emotional goal: *"I can make the machine do things."*
3. **Part 3 — How software is really built:** lifecycle, Git, testing, architecture.
   Emotional goal: *"I understand what tech teams actually do all day."*
4. **Part 4 — Computer science:** algorithms, databases, OS/networks, security.
   Emotional goal: *"The famous 'hard' ideas are within my reach."*
5. **Part 5 — The modern world:** cloud, AI, platforms.
   Emotional goal: *"I can decode the news and the buzzwords."*
6. **Part 6 — People & careers:** roles, process, paths in.
   Emotional goal: *"There is a place for me in this world if I want it."*

The **capstone** converts knowledge into proof: a live website, a PM project plan, or a
real-life automation.

## Quality process

1. Content is written to the [Style Guide](style-guide.md) (banned words list, analogy
   rules, reading-level targets).
2. Every page is then **audited from a non-technical reader's point of view** — checked
   for jargon leaks, banned words, missing analogies, and broken links before publishing.
3. Learner confusion reports are treated as bugs (see [Contributing](../CONTRIBUTING.md)).

## Known limitations & future work

- **English only, for now.** Translations are the most-wanted contribution.
- **Links rot.** External resources are chosen from large, stable, free providers to
  minimize this, and we prefer linking to homepages/series over deep pages.
- **No video of our own yet.** The course is text-first by design (searchable,
  translatable, low-bandwidth), but companion videos are on the wishlist.
- **Accessibility.** Plain text + GitHub rendering is screen-reader friendly; we avoid
  meaning carried only by images. Diagrams are described in words.
