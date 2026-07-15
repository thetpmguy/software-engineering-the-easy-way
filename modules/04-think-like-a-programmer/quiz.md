# ✅ Quiz 04 — How to Think Like a Programmer

Answer in your head or on paper, then open each fold to check. No scores, no grades — the folds are there so you can be honest with yourself first.

---

**1. What is an algorithm, in one plain sentence?**

<details><summary>Show answer</summary>

An algorithm is a list of exact steps, in order, that solves a problem or gets a job done — like a recipe. It doesn't have to involve computers at all: a tax form and a knitting pattern are algorithms too.
</details>

---

**2. True or false: to be a programmer, you need to be good at advanced math.**

<details><summary>Show answer</summary>

False. Most everyday programming uses little more than basic arithmetic. The core skill is breaking big fuzzy problems into small exact steps — computational thinking. (Some specialties, like graphics or machine learning, do use more math, but they are the exception.)
</details>

---

**3. You have to organize a big family reunion. You split it into: guest list, food, venue, activities. Which move of computational thinking is that?**

<details><summary>Show answer</summary>

Decomposition — cutting one overwhelming problem into smaller problems you can handle one at a time.
</details>

---

**4. You notice that emailing each of the 40 guests involves exactly the same steps, with only the name changing. Which move is that — and why do computers love it?**

<details><summary>Show answer</summary>

Pattern recognition — spotting that many tasks are really one task repeated. Computers love it because repeating a step a million times, identically, without getting bored or sloppy, is the thing they do best.
</details>

---

**5. Your written reunion plan says "set up the hall" as a single step, even though it hides two hours of detailed work. Which move is that, and what's the benefit?**

<details><summary>Show answer</summary>

Abstraction — hiding a bundle of details behind one short label. The benefit: you can think and plan at a higher level without drowning in details, and you can reuse the label ("set up the hall") without re-explaining the steps every time.
</details>

---

**6. In the peanut butter sandwich exercise, the parent smears peanut butter on the plastic bag. What is this teaching us about computers?**

<details><summary>Show answer</summary>

Computers are perfectly literal. They do exactly what the instructions say — never what the writer *meant*. Every gap or unstated assumption in your instructions becomes a wrong result, because a computer has no common sense to fill gaps with.
</details>

---

**7. In a flowchart, what does a diamond shape mean, and what does an arrow pointing back to an earlier step mean?**

<details><summary>Show answer</summary>

A diamond is a decision — a yes/no question with one arrow for each answer. An arrow pointing back to an earlier step is a loop — a set of steps that repeat until some condition changes (like "is the water boiling yet?").
</details>

---

**8. What is pseudocode, and why do programmers bother writing it when it can't even run?**

<details><summary>Show answer</summary>

Pseudocode is an algorithm written in plain, structured English — one step per line, with words like IF and FOR EACH showing the structure. Programmers write it to work out the *logic* of a plan first, without being distracted by the strict spelling and punctuation rules of a real programming language. Getting the logic right is the hard part; translating it to code afterwards is the smaller step.
</details>

---

**9. In the "find the oldest person in a room" pseudocode, we kept a note saying "oldest so far." After asking Amara (34), Ben (61), and Chloe (52) in that order, what did the note say at each stage?**

<details><summary>Show answer</summary>

Start: *nobody, age 0*. After Amara: *Amara, 34* (34 beats 0). After Ben: *Ben, 61* (61 beats 34). After Chloe: still *Ben, 61* (52 does not beat 61). Final answer: Ben. The note is a piece of remembered information that changes as the loop runs — in Module 05 we'll call it a variable.
</details>

---

**10. Your program gives the wrong answer. A programmer friend says: "Well, the computer did exactly what you told it." Is your friend being mean? What should you do next?**

<details><summary>Show answer</summary>

Not mean — accurate, and secretly encouraging. The computer followed your instructions perfectly; the mistake is somewhere in the instructions, which means it is findable. Next step: debug like a detective — re-run the program, follow your own instructions line by line with total literalness, and track what each value is until you find the line that does what you *wrote* instead of what you *meant*.
</details>

---

**11. 🗣️ Explain it to a friend**

Imagine a friend says: *"I'd love to learn coding but I was hopeless at math in school."* In two or three sentences, out loud or on paper, reassure them — using the words *algorithm* and *breaking problems down*, and one everyday example (recipe, tax form, morning routine…).

<details><summary>Show one possible answer</summary>

"Coding is barely about math — it's about breaking problems down into small exact steps, which you already do every day. A recipe is an algorithm: exact steps, in order, and anyone who follows them gets pancakes. Programming is writing recipes like that for a machine — the only twist is the machine has no common sense, so your steps have to be really precise."

Yours will sound different — what matters is: (1) math isn't the core skill, (2) an algorithm is exact ordered steps, (3) an everyday example, (4) breaking problems down is the real skill.
</details>
