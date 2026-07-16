# ✅ Quiz 18 — Who Does What in Tech

Answer in your head or on paper, then open the fold to check. No grades, no timer —
this is for you.

---

**1. Match the film-set role to the tech role: producer, continuity checker, camera
crew, fire brigade.**

<details><summary>Show answer</summary>

Producer = **product manager** (decides what to make and why). Continuity checker =
**QA engineer** (catches mistakes before the audience does). Camera crew = **software
engineers** (physically build the thing). Fire brigade = **DevOps/SRE** (keeps the show
running, including at 3am).
</details>

---

**2. True or false: the product manager is the engineers' boss.**

<details><summary>Show answer</summary>

**False.** Engineers report to the **engineering manager**. The PM decides *what* to
build and *why*, but leads by evidence and persuasion — influence without authority.
It's one of the strangest and most important facts about how tech teams work.
</details>

---

**3. Why is an engineering manager like a conductor — and why is "promoting the best
coder to manager" a questionable idea?**

<details><summary>Show answer</summary>

A conductor doesn't play an instrument during the concert and is rarely the best
violinist — their job is making forty musicians sound like one orchestra. Likewise, an
engineering manager manages *people*, not code: one-on-ones, growth, hiring, removing
obstacles. It's a career change, not a level-up — and the best coder often contributes
more (and may earn more) by staying a senior engineer.
</details>

---

**4. Your friend is choosing between "UX designer" and "UI designer" job ads. Explain the
difference with the lesson's analogy.**

<details><summary>Show answer</summary>

**UX** (user experience) is the *architect*: designing how the whole experience works —
what steps a user takes, in what order, how it flows. **UI** (user interface) is the
*interior decorator*: how each screen looks — colors, spacing, typography. Many
designers do both.
</details>

---

**5. A company has a data analyst, a data scientist, and a data engineer. The CEO asks:
"Which customers will probably cancel next month?" Who builds the answer — and what do
the other two do?**

<details><summary>Show answer</summary>

The **data scientist** builds the prediction (the crystal ball). The **data engineer**
built the plumbing that collects and cleans the customer data the model needs. The
**data analyst** answers questions about what *already happened* ("how many cancelled
last month, and did the price change matter?") — the tea leaves.
</details>

---

**6. What is a "squad", and what does it mean that a squad "owns" an area?**

<details><summary>Show answer</summary>

A squad is a small unit — typically **4–8 engineers plus a product manager and a
designer** — responsible for one area of the product (search, payments, sign-up).
"Owning" means they plan it, build it, test it, ship it, and get woken up if it breaks —
they can deliver without asking permission from a central committee.
</details>

---

**7. Name the four sprint rituals and give each one's rough time cost.**

<details><summary>Show answer</summary>

**Standup** (daily, 15 minutes: yesterday / today / blocked), **planning** (1–2 hours
per sprint: choose what fits in the next two weeks), **demo** (30–60 minutes per sprint:
show the real working thing), and **retro** (about an hour per sprint: what went well,
what went badly, what we'll change — blameless).
</details>

---

**8. At standup, a teammate says "I'm blocked." Why is that the most valuable sentence
in the whole meeting?**

<details><summary>Show answer</summary>

Because a blocked person can silently lose *days* waiting, and standup exists precisely
to surface this within 24 hours. Yesterday's and today's updates are useful context, but
"I'm blocked, and here's on what" is the sentence that lets someone act immediately —
often the blocker is a two-minute fix for the right person.
</details>

---

**9. An engineer asks for two weeks to "refactor" — the app will look exactly the same
afterward. Using the kitchen analogy, explain to a skeptical executive why this isn't
wasted time.**

<details><summary>Show answer</summary>

The team took shortcuts to ship fast — that's **tech debt**, a loan of time repaid with
interest, because every shortcut makes future changes slower and riskier. Refactoring is
cleaning the kitchen between rushes: pans put away, knives where they belong. The food
(the app) looks the same tonight — but a kitchen that's never cleaned gets slower every
service until one day it can't cook at all. The two weeks buy back speed on everything
that comes after.
</details>

---

**10. Your colleague is about to tell the engineering team: "Add a filter dropdown to
the reports page — should be a small change, right?" Name *both* things wrong with this
sentence and suggest a better version.**

<details><summary>Show answer</summary>

First, it's a **solution demand**, not a problem — it skips the team's thinking about
what would fix things best. Second, "small change, right?" asserts the size of an
iceberg while looking only at its tip; only someone who can see the plumbing can size
it. Better: "Users can't narrow the reports down and end up exporting everything to
Excel to filter by hand — what are our options, and roughly how big is each: days,
weeks, or months?"
</details>

---

**11. Story points: a team labels a ticket "8". What are they actually claiming — and
what are they *not* claiming?**

<details><summary>Show answer</summary>

They're claiming: "relative to our other work lately, this feels like one of the bigger
items." They are **not** claiming it will take 8 hours, 8 days, or any specific time.
All software estimates are educated guesses (unknown unknowns — the pipes behind the
wall), and points exist to make guessing faster and less painful, not accurate. Treat
estimates like weather forecasts: plan with them, don't treat them as promises.
</details>

---

**12. 🗣️ Explain it to a friend**

A friend just became a marketing manager at a software company. She says: *"I sit near
the engineers and I'm terrified of them. There's a 15-minute meeting every morning I
don't understand, and when I asked for one small change, everyone went quiet."*

In under a minute, jargon-free: explain what that morning meeting is, why "one small
change" landed badly, and give her two tips for becoming the colleague the engineers
love.

<details><summary>One possible answer</summary>

"That morning meeting is a standup — a quick huddle where each person says what they did
yesterday, what they'll do today, and whether anything's blocking them. It's a
coordination ritual, not a status report to bosses — you're welcome to listen in.

The 'small change' thing: software is like an iceberg. The button you see is the tip;
under the water there's plumbing you can't see, and sometimes the tiny button sits on a
huge pipe. Saying 'small' about someone's iceberg, sight unseen, is what made the room
go quiet.

Two tips: first, bring problems, not solutions — 'customers can't find our pricing page'
works better than 'move the pricing link', because it lets them find the best fix.
Second, protect their focus: their hard work is like baking a soufflé, and a quick
interruption collapses an hour of it — so batch your questions into one message they can
answer when the oven's open. Do those two things and you'll be their favorite person in
marketing."
</details>
