# ✍️ Style Guide — How Every Lesson in This Course Must Be Written

> This is a **working document**. Every lesson, lab, and quiz in this course follows these
> rules. If you contribute content, read this first. If you're a learner, this page tells
> you what to expect (and what to complain about if we break our own rules!).

## The One Rule Above All

**Write for a smart person who has never touched code and never wants to feel stupid.**

Our reader might be a nurse, a farmer, a shop owner, a lawyer, a student, a grandparent.
They are intelligent. They are busy. They have zero technical background. Every sentence
must respect that.

## The 10 Rules

1. **Plain English only.** If a 12-year-old couldn't follow the sentence, rewrite it.
   Short sentences. Everyday words.

2. **Never use a technical term before explaining it.** The first time a term appears,
   define it in one plain sentence *immediately*, in **bold**, like this:
   > A **server** is just a computer that stays on all the time so other computers can
   > ask it for things.
   Then add the term to the [Glossary](../GLOSSARY.md).

3. **Every big idea gets an analogy.** Anchor every abstract concept to something
   physical from daily life: kitchens, post offices, libraries, roads, recipes, filing
   cabinets. Introduce the analogy *before* the technical explanation, and also say
   where the analogy breaks down (all analogies do).

4. **Show, don't lecture.** Every concept gets a concrete example within a few
   paragraphs. Prefer examples with real numbers, real names, real situations.

5. **One idea per section.** Headings every few paragraphs. A reader should be able to
   stop at any heading and come back tomorrow.

6. **Tell them why before what.** Start every module and every major section with the
   problem it solves ("Have you ever wondered why apps update so often?") — not with a
   definition.

7. **Check understanding constantly.** Use "✅ Check yourself" boxes: 2–3 questions a
   reader can answer in their head. Answers go right below, hidden in a
   `<details><summary>Show answer</summary> ... </details>` fold.

8. **No gatekeeping words.** Banned: "simply", "just" (as in "just do X"), "obviously",
   "clearly", "of course", "trivial", "easy" (describing a task). If it were obvious,
   they wouldn't be reading a course. *(One deliberate exception: the course's own title,
   "Software Engineering — The Easy Way", is a brand promise about our teaching approach,
   not a claim that any particular task is easy. The rule still applies to all lesson,
   lab, and quiz content — never tell a reader a task is easy.)*

9. **Labs must work with zero installation.** Every hands-on exercise must run in a web
   browser on a phone or a cheap laptop. Free tools only. No sign-up unless unavoidable
   (GitHub itself is the one allowed sign-up).

10. **Be warm, never cute at the reader's expense.** Humor is welcome. Jokes about the
    reader's ignorance are not. The tone is: *a patient friend who happens to be an
    engineer, explaining over coffee.*

## Standard Module Layout

Every module folder contains:

| File | What it is |
|---|---|
| `README.md` | The lesson itself. Opens with "What you'll learn" + "Why it matters", ends with a recap and a bridge to the next module. |
| `lab.md` | A hands-on exercise doable in a browser, with numbered steps, screenshots described in words, and a "what you should see" checkpoint after every few steps. |
| `quiz.md` | 8–12 questions with answers in `<details>` folds, plus one "explain it to a friend" prompt. |
| `resources.md` | Curated *free* external links (videos, interactive sites, articles), each with one sentence on what it is and who it's best for. |

## Formatting Conventions

- Emoji in headings are welcome — they help scanning (🧠 concept, 🔧 hands-on, ⚠️ gotcha,
  ✅ check yourself, 🌉 analogy, 📚 go deeper).
- Analogies live in blockquotes starting with **🌉 Analogy:**.
- Warnings/gotchas in blockquotes starting with **⚠️ Watch out:**.
- Tables for comparisons; never more than 4 columns.
- Code appears only when the lesson is *about* code, always short (≤ 15 lines), always
  explained line by line in plain English.
- Links to other modules are relative paths, so they work on GitHub and offline.

## Reading Level Target

- Sentences: average under 20 words.
- Paragraphs: 2–4 sentences.
- If you need a comma-heavy 40-word sentence, split it into two.

## The Final Test for Any Page

Before publishing, ask: **"Would my aunt who runs a bakery read this whole page and feel
smarter — not lost, not talked down to?"** If not, rewrite.
