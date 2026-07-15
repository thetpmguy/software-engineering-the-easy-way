# ✅ Quiz 05 — Your First Code

Answer in your head or on paper first, then open the fold. If you get one wrong, that's the quiz working — reread that section and it will stick twice as hard.

---

**1. Why does this course start with Python rather than another programming language?**

<details><summary>Show answer</summary>

Because Python reads almost like English, so beginners can concentrate on the ideas instead of the punctuation — and because it's a serious professional language (used at NASA, Netflix, banks, and science labs), so nothing you learn is wasted.
</details>

---

**2. What will this line show on the screen: `print("2 + 2")` — and why isn't it `4`?**

<details><summary>Show answer</summary>

It shows exactly `2 + 2`. The quotation marks make it a string — text to display as-is, not math to work out. Without the quotes, `print(2 + 2)` would show `4`.
</details>

---

**3. In plain English, what happens when Python runs `score = 10`? What does the `=` mean here?**

<details><summary>Show answer</summary>

Python creates (or reuses) a jar labeled `score` and stores the value 10 inside it. The `=` means "store the thing on the right in the variable on the left" — an action, not a math statement of equality.
</details>

---

**4. A variable is like a labeled jar. Name one way real jars and variables behave differently.**

<details><summary>Show answer</summary>

When you put a new value into a variable, the old value is gone completely — unlike a real jar, where the old contents end up somewhere. (Also acceptable: a variable's contents are replaced instantly; you can't have a "half-emptied" variable.)
</details>

---

**5. What's the difference between `5` and `"5"` in Python? What is `"5" + "5"`?**

<details><summary>Show answer</summary>

`5` is a number — you can do math with it. `"5"` is a string — a piece of text that happens to look like a digit. `"5" + "5"` is `"55"`, because `+` on strings glues them together instead of adding.
</details>

---

**6. What does `input()` do, and what type of value does it always hand back — even if the user types `42`?**

<details><summary>Show answer</summary>

`input()` pauses the program, waits for the person to type something and press Enter, then hands back what they typed. It always hands back a **string** — so a typed `42` arrives as `"42"`, and you need `int(...)` to turn it into a number before doing math or comparisons with it.
</details>

---

**7. Read this code. What prints when `age` is 16? And when it's 70?**

```python
if age >= 65:
    print("Senior ticket")
elif age >= 18:
    print("Adult ticket")
else:
    print("Child ticket")
```

<details><summary>Show answer</summary>

With 16: `Child ticket` — both checks fail, so the `else` catch-all runs. With 70: `Senior ticket` — the first check passes, and Python skips the rest entirely (even though 70 is also ≥ 18, only the first passing branch runs).
</details>

---

**8. Your friend wants a program that prints one thank-you message per person on their 30-name guest list. Which loop fits better, `for` or `while` — and why?**

<details><summary>Show answer</summary>

`for` — you have a collection (the basket of 30 names) and want the loop to run once per item. `while` is for "repeat until some condition changes," when you don't know the number of repeats in advance (like "keep asking until the password is right").
</details>

---

**9. What is an infinite loop, and what everyday-kitchen mistake in a `while` loop causes one?**

<details><summary>Show answer</summary>

A loop whose condition never becomes false, so it repeats forever. It happens when nothing inside the loop changes the condition — like the countdown loop without the `countdown = countdown - 1` line: the jar stays at 5 forever, and "is it more than 0?" is always yes. In kitchen terms: "stir until thick" when you never actually check, or when nothing you do could ever make it thick.
</details>

---

**10. You run your program and get: `NameError: name 'naem' is not defined` pointing at line 4. What is the computer telling you, and what's probably wrong?**

<details><summary>Show answer</summary>

The pedantic proofreader is saying: "On line 4 you asked me to open a jar labeled `naem`, and no such jar exists." Almost certainly you created a variable called `name` earlier and misspelled it as `naem` on line 4. Error messages usually name the line and the problem — reading them is half of debugging.
</details>

---

**11. True or false: after this module you could build a simple version of Instagram, since it's mostly code like this but longer.**

<details><summary>Show answer</summary>

False — and this course won't pretend otherwise. Real apps need screens, databases, servers, and usually teams (Parts 3–5 of this course explain all of it). What you genuinely *can* work toward now: small programs that automate boring chores — renaming files, adding up expenses, quizzing your kids. That's real, useful programming, and it's how nearly every professional started.
</details>

---

**12. 🗣️ Explain it to a friend**

A friend watches over your shoulder as you run the rocket countdown program, and asks: *"Wait — how does the computer know to stop at zero?"* Explain it out loud in two or three sentences, using the words **variable** and **loop**.

<details><summary>Show one possible answer</summary>

"There's a variable — think of it as a labeled jar — that starts out holding 5. The loop says: as long as the jar holds more than zero, print the number and put back one less. So it prints 5, 4, 3, 2, 1 — and the moment the jar holds 0, the 'more than zero?' check fails, the loop stops, and the program moves on to print 'Lift off!'"

Your wording will differ. What matters: (1) a variable stores a changing number, (2) the loop repeats while a condition is true, (3) something inside the loop changes the variable so the condition eventually fails.
</details>
