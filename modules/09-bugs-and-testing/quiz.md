# ✅ Quiz 09 — Bugs, Testing & Quality

Answer in your head or on paper, then open the fold to check.

---

**1. What is a bug, in the plainest possible terms?**

<details><summary>Show answer</summary>

The gap between what you *meant* the software to do and what you actually *wrote*. The
machine is perfectly obedient and perfectly literal — it executes the letter of the
instructions, never the spirit. When letter and spirit differ, that difference is the
bug.
</details>

---

**2. In the Mars Climate Orbiter disaster, both pieces of software "worked perfectly."
So what went wrong?**

<details><summary>Show answer</summary>

One program calculated in imperial units (pound-force) while the other expected metric
(newtons). Each followed its own instructions flawlessly — but the *shared intention*
("we're using the same units") never made it into the instructions. A $327 million
spacecraft burned in the Martian atmosphere over a unit mix-up. It's the perfect example
of a logic error: nothing crashed, the math ran, the thinking was wrong.
</details>

---

**3. Where does the word "bug" come from — and was it Grace Hopper's team's invention?**

<details><summary>Show answer</summary>

In 1947, engineers on the Harvard Mark II (Grace Hopper's team) traced a malfunction to
an actual moth stuck in a relay, and taped it into the logbook: "First actual case of
bug being found." But the word was *already* engineers' slang for a defect — even Edison
used it — which is exactly why the note was a joke. The moth-in-the-logbook is real and
lives at the Smithsonian.
</details>

---

**4. What's the difference between a syntax error and a logic error — and which should
scare you more?**

<details><summary>Show answer</summary>

A **syntax error** breaks the language's spelling/grammar rules; the pedantic
proofreader catches it instantly and the code won't run at all. A **logic error** is
grammatically perfect code built on wrong thinking — it runs happily and produces wrong
results. The logic error is scarier: the recipe with salt instead of sugar bakes
beautifully, and a wrong-but-plausible number can hide for years.
</details>

---

**5. Name three edge cases for an app that stores people's names and birthdays.**

<details><summary>Show answer</summary>

Any three of, e.g.: a birthday on February 29th (doesn't exist most years); a
3,000-character name; a one-letter name; a name with accents or characters from other
alphabets; a missing birthday; a birthday today; a birthday in the future (typo?);
someone whose age is over 120 (typo, or record-holder?); a name containing only spaces.
Edge cases live at the boundaries of what the author imagined — and with millions of
users, every boundary gets visited.
</details>

---

**6. Why is "reproduce it first" the golden rule of debugging?**

<details><summary>Show answer</summary>

Because a bug you can trigger on demand can be investigated systematically — you can
test suspects, and above all you can *verify your fix*: make the bug happen, apply the
fix, confirm it no longer happens. "It crashed once yesterday" allows none of that; you
could "fix" it and never know whether you did.
</details>

---

**7. A program has 1,000 parts and one of them is corrupting the data. Roughly how many
well-chosen checks does the halving strategy need to find the culprit — 10, 100, or
500?**

<details><summary>Show answer</summary>

About **10**. Each check tests the middle of the remaining suspects and cuts the search
space in half: 1,000 → 500 → 250 → 125 → 63 → 32 → 16 → 8 → 4 → 2 → 1. That's binary
search — the same idea that finds a name in a phone book — pointed at a bug.
</details>

---

**8. What is rubber duck debugging, and why does it actually work?**

<details><summary>Show answer</summary>

Explaining your problem out loud, line by line, to an inanimate object (traditionally a
rubber duck). It works because converting fuzzy mental shorthand into explicit spoken
sentences forces you to actually read what the code *says* rather than what you assume
it says — and the wrong assumption becomes audible, often mid-sentence. It's a real,
named practice; engineers keep real ducks on real desks.
</details>

---

**9. Match each test type to the food-safety analogy: unit test, integration test,
end-to-end test.**

<details><summary>Show answer</summary>

**Unit test** = the chef tasting each individual sauce (one small piece of code, in
isolation — each Lego brick). **Integration test** = checking the sauce works on the
dish it's served with (pieces working *together* — bricks snapped together).
**End-to-end test** = the health inspection of the entire kitchen, delivery door to
dining table (a robot drives the whole assembled product like a real user —
test-driving the whole car).
</details>

---

**10. Why can't a team with unlimited budget test *every* possibility?**

<details><summary>Show answer</summary>

**Combinatorial explosion**: possibilities multiply. Ten input fields with a handful of
interesting values each already yields millions of combinations; add sequences of
actions, timing, and device differences and the count exceeds anything checkable in the
lifetime of the universe. So testing is judgment — cover the common paths, the risky
paths, and the edges — which is why QA is a genuine profession, not an afterthought.
</details>

---

**11. Your weather app's update broke the sunrise widget, which had worked for two
years. What is this called, why does it happen, and what practice exists to catch it?**

<details><summary>Show answer</summary>

A **regression** — a change broke something that used to work. It happens because
software is deeply interconnected, like plumbing hidden in walls: fixing the sink can
crack a pipe two rooms away. The defense is **regression testing**: keep every test ever
written and re-run all of them on every change — with **CI** (continuous integration)
robots doing exactly that automatically the moment any change is proposed, stamping a
green check or red X on it before humans even review.
</details>

---

**12. 🗣️ Explain it to a friend**

Your friend fumes: *"My banking app UPDATE broke the fingerprint login! How does a bank
with ten thousand engineers break something that already worked?! Did nobody check?"*

In under a minute, jargon-free: explain why all software has bugs, what likely happened
(a regression), and why "did nobody check" isn't quite fair — while being honest about
what the bank could do better.

<details><summary>One possible answer</summary>

"Software is millions of lines of instructions written by humans, and the computer
follows them exactly as written — including the mistakes. So every app on Earth has
bugs; the only question is which ones are found first. What probably happened to your
login is called a regression: they changed something else — maybe the payments screen —
and software is so interconnected that it's like a plumber fixing your sink and cracking
a pipe inside the wall two rooms away. The bathroom worked fine until the *sink* got
fixed. And they almost certainly did check — banks run thousands of automated re-checks
on every change, every day. But you can't test everything: the possible combinations of
phones, settings, and actions multiply beyond counting, so they test the most common and
most dangerous paths and some things slip through the edges. The fair criticism isn't
'nobody checked' — it's 'fingerprint login is important enough that it deserved one of
those permanent automated re-checks.' After your complaint, it'll probably get one."
</details>
