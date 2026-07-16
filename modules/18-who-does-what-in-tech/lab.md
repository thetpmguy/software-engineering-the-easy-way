# 🔧 Lab 18 — Walk the Set Yourself

> **Goal:** turn the lesson into instinct — decode real job ads, run your own kanban
> board for a week, spot standup anti-patterns, and practice the single most valuable
> communication skill in tech: turning demands into problems.
>
> **You'll need:** a web browser, paper and sticky notes (or any notes app), and about
> 60 minutes now plus 5 minutes a day for one week (Part 2 runs in the background of
> your real life). No installation. No sign-up.

This lab has four parts. Parts 1, 3, and 4 you can do today. Part 2 takes a week — start
it today and let it run.

---

## Part 1 — Decode 5 real job ads (20 minutes)

Real job listings are written in dense tech-speak. After Module 18, you can read them.

**Steps:**

1. Open any job board in your browser — for example LinkedIn Jobs, Indeed, or a tech
   company's own "Careers" page. No account needed to *read* listings on most boards.
2. Search for each of these titles and open one real listing for each (any company,
   any city):
   - "Frontend Engineer"
   - "Product Manager"
   - "Site Reliability Engineer" (or "DevOps Engineer")
   - "Data Analyst"
   - "QA Engineer" (or "Test Engineer")
3. For **each** listing, write three lines on your paper:
   - **Role type:** which character from the lesson is this? (Builder? Producer? Fire
     brigade? Tea-leaf reader? Continuity checker?)
   - **Plain-English translation:** one sentence describing what this person will do all
     day, in words your neighbor would understand.
   - **One decoded phrase:** pick one piece of jargon from the ad (e.g. "CI/CD",
     "cross-functional", "on-call rotation", "SQL") and translate it using this course.

**Example** (so you know what good looks like):

> *Listing:* "Senior Backend Engineer — design and scale our payments APIs."
> *Role type:* builder — kitchen side (backend, Module 10).
> *Translation:* "You'll build and improve the hidden machinery that moves money when
> someone taps Pay."
> *Decoded phrase:* "APIs" — the waiter that carries requests between programs
> (Module 10).

**✅ What you should have:** five short decoded listings. If a phrase resists
translation, look it up in the [Glossary](../../GLOSSARY.md) — and if it's not there,
you've found a genuinely obscure term; searching `"the term" meaning plain english`
usually cracks it.

---

## Part 2 — Run a personal kanban for one real week (5 min/day for 7 days)

You read about the board. Now *feel* why it works, using your real life.

**Steps:**

1. Take a sheet of paper (or a wall, or a notes app) and make three columns:
   **TO DO | DOING | DONE**.
2. Write each real task from your week on its own sticky note (or line): errands,
   work tasks, "call the dentist", one lab from this course. Aim for 8–15 notes. Put
   them all in TO DO, most important at the top.
3. **The one rule that makes it work:** DOING may never hold more than **2 notes**.
   This is called a **WIP limit** — a cap on **work in progress**, the number of things
   you allow yourself to have started but not finished. Want to start a third thing?
   You must finish (or deliberately push back) one first.
4. Each morning, take 30 seconds: move finished notes to DONE, pull the top of TO DO
   into DOING if there's room.
5. **Friday: hold a 5-minute retro with yourself.** Three questions, written down:
   - What went well this week?
   - What went badly?
   - What one thing will I change next week?
   Remember the golden rule — blameless. "The system let me overcommit" beats "I'm
   lazy".

**✅ What you should see by Friday:** a DONE column that feels genuinely good to look
at, and — most people report this — the strange discomfort of the WIP limit, followed by
the discovery that finishing two things beats starting six. That feeling is why software
teams use boards.

---

## Part 3 — Watch a standup and spot the anti-patterns (15 minutes)

Below is a script of a fictional squad's daily standup. Four characters, about two
minutes if read aloud — and it contains **four classic standup mistakes**.

**Steps:**

1. Read the script aloud (roping in family members as cast is encouraged and funny).
2. Write down every moment where someone breaks the spirit of standup. Hint: standup is
   15 minutes, three questions each — yesterday / today / blocked.
3. Check your findings against the fold below.

---

> **THE STANDUP — 9:32 AM (scheduled for 9:15)**
>
> **MAYA (engineer):** Yesterday I finished the password-reset ticket. Today I'm starting
> the email templates. No blockers.
>
> **DEV (engineer):** So, okay, interesting story. Yesterday I was looking at the slow
> search bug, and I thought it was the database, so I opened the query logs, and at first
> the logs wouldn't even load, which reminded me of a bug we had in 2023 — Maya, remember
> that? — anyway, I tried three different index settings, and the second one was weird
> because — well, let me share my screen and walk you through the query plan…
>
> **SAM (engineer):** *(typing on phone throughout)* Uh — same as yesterday. Still on the
> big migration thing. It's fine.
>
> **PRIYA (PM):** Quick one from me: the checkout redesign — can we commit to shipping it
> by Friday? I need an answer for the sales team right now, while I have you all here.
>
> **MAYA:** …also, I'm blocked waiting for Sam's migration, but we can sort that after.
>
> **DEV:** Wait, before we go — one more thing about those index settings…

---

<details><summary>Show the anti-patterns</summary>

1. **It started 17 minutes late.** Standup lives or dies on being short and punctual —
   a 9:15 huddle that starts at 9:32 has already spent more than its budget.
2. **Dev told a story and tried to problem-solve in the meeting.** The 5-minute
   query-plan walkthrough belongs *after* standup with whoever's interested ("let's take
   it offline" is the standard phrase). Standup answers three questions; it doesn't
   debug.
3. **Sam gave a status that contains no information.** "Same as yesterday, it's fine" —
   for the third day? — hides trouble. A multi-day "still on it" with no end in sight is
   exactly what standup exists to surface. (The phone-typing signals the deeper issue:
   nobody's listening to updates that say nothing.)
4. **Priya turned standup into a commitment negotiation.** Asking a team for an on-the-
   spot shipping promise — in front of everyone, "right now" — is the meeting engineers
   dread (see the lesson's table). It's a real question, but it deserves its own
   conversation, with time to check the iceberg.

**Bonus finding, if you caught it:** Maya's real blocker (waiting on Sam) nearly slipped
away un-discussed — because the meeting's time had been eaten. Blockers are the most
valuable sentence in any standup.
</details>

**✅ What you should have:** at least three of the four anti-patterns spotted. If you
found all four plus the bonus — you'd be a better standup facilitator than many working
engineers.

---

## Part 4 — Translate demands into problems (10 minutes)

The lesson's rule: **bring problems, not solutions.** Practice the translation. For each
"solution demand" below, write the *problem statement* that's probably hiding behind it.
A good problem statement names **who** is affected, **what** they can't do, and **what
it costs** — and mentions no feature.

**Translate these three:**

1. "We need a dark mode by next month."
2. "Make the sign-up form shorter."
3. "Add a chatbot to the help page."

Write yours before opening the fold.

<details><summary>Show possible translations</summary>

1. **Dark mode →** "Several users say the app is uncomfortably bright when they check it
   at night, and some say they've stopped opening it in the evening." *(Now the team can
   consider dark mode — or a dimmer schedule, or fixing the one blinding screen.)*
2. **Shorter form →** "Six out of ten people who start sign-up never finish it; most
   quit on the second page." *(Maybe the fix is fewer fields — or maybe one confusing
   question, or a broken button on page two. The data will say.)*
3. **Chatbot →** "Support gets 200 messages a week asking the same five questions, and
   customers wait a day for answers they could have had instantly." *(Possible fixes: a
   chatbot — or a well-placed FAQ, or clearer wording in the app so the questions never
   arise.)*

Yours don't need to match these — check the shape: who + can't do what + at what cost,
and no feature named.
</details>

**✅ What you should have:** three problem statements a squad could act on without being
told *how*. Congratulations — you now communicate better with engineers than many people
who've worked beside them for years.

---

## 🎉 Done!

You've decoded the job market, run the method yourself, developed an eye for broken
rituals, and learned the translation skill that makes non-technical people beloved by
engineering teams. When your Friday retro is done, Part 2 is complete — and so is
this lab.
