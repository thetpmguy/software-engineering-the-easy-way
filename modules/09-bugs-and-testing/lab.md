# 🔧 Lab 09 — The Bug Hunt

> **Goal:** find and fix real bugs in real Python code, write a test plan the way QA
> professionals do, and perform one (1) sincere conversation with a duck.
>
> **You'll need:** a browser Python playground — go to
> **[trinket.io](https://trinket.io)** and choose "Try it out" / the Python trinket (no
> account needed), or any similar in-browser Python you used in Module 05. Time: about
> 45–60 minutes.

---

## Part 1 — Bug hunt: five snippets, five bugs (30 minutes)

Each snippet below has **one planted bug**. For each one:

1. Read the code and predict what it does.
2. Paste it into your browser Python and run it.
3. Compare **expected** vs. **actual** behavior.
4. Play detective: find the bug, fix it, and re-run to confirm.
5. Only then, open the fold to check.

Don't rush to the folds — the struggle *is* the exercise. Reproduce, narrow down, and if
you're stuck, read the code out loud (Part 3 will explain why that works).

---

### 🐛 Bug 1 — The broken greeting

```python
name = "Maria"
print("Welcome back, + name + !")
```

**Expected:** `Welcome back, Maria!`
**Actual:** run it and see.

<details><summary>Show the bug and the fix</summary>

**The bug:** the quotation marks wrap the *whole line*, so Python treats
`+ name +` as ordinary text inside a sentence instead of as "glue in the variable
here". It prints the plus signs and the word `name`, literally.

**The fix:** close the quotes around each piece of text, keeping `name` outside them:

```python
name = "Maria"
print("Welcome back, " + name + "!")
```

**Species:** this prints the wrong thing rather than refusing to run — the machine
obeyed the letter of what we wrote. (If you *delete* a quote mark entirely, you'll see
its cousin, a true syntax error: Python's proofreader refuses to run at all. Try it!)
</details>

---

### 🐛 Bug 2 — The generous discount (logic error)

```python
price = 100
discount_percent = 20
final_price = price - discount_percent
print("You pay:", final_price)
```

**Expected:** 20% off $100 is **$80** — and it prints 80, which *looks* right! Now
change `price` to `50` and run again. 20% off $50 should be **$40**.
**Actual:** …run it.

<details><summary>Show the bug and the fix</summary>

**The bug:** the code subtracts the *number* 20, not *20 percent*. It only looked
correct at first because 20% of 100 happens to equal 20 — a coincidence that hid the
bug. This is a classic **logic error**: valid code, wrong thinking, and it can lurk
until the input changes. (Salt instead of sugar — and the first bite happened to taste
fine.)

**The fix:**

```python
price = 50
discount_percent = 20
final_price = price - (price * discount_percent / 100)
print("You pay:", final_price)
```

Now it prints 40.0 — and works for *any* price.
</details>

---

### 🐛 Bug 3 — The off-by-one countdown

```python
print("Counting down to launch!")
for number in range(5, 1, -1):
    print(number)
print("LIFTOFF!")
```

**Expected:** `5 4 3 2 1 LIFTOFF!`
**Actual:** run it — listen for what's missing.

<details><summary>Show the bug and the fix</summary>

**The bug:** it never says "1". Python's `range(start, stop, step)` stops *before* the
stop value — `range(5, 1, -1)` gives 5, 4, 3, 2 and quits. This whole family of mistakes
is so common it has a name: an **off-by-one error** — the code does one time too few (or
too many).

**The fix:** tell the range to stop before **0** instead:

```python
for number in range(5, 0, -1):
    print(number)
```

**Species:** logic error, boundary flavor. Boundaries (first item, last item, empty
list) are where bugs love to live — remember that for Part 2.
</details>

---

### 🐛 Bug 4 — The average that crashes (edge case)

```python
scores = []
total = 0
for score in scores:
    total = total + score
average = total / len(scores)
print("Average score:", average)
```

**Expected:** with an empty list, ideally a polite message.
**Actual:** run it — you get your first traceback (Python's crash report). Read it!
The last line names the crime.

<details><summary>Show the bug and the fix</summary>

**The bug:** with no scores, `len(scores)` is 0 — and the code divides by zero, which
mathematics (and Python) refuse to allow: `ZeroDivisionError`. The code works for 2
scores or 200, and crashes at exactly one boundary: zero. A textbook **edge case** —
the author pictured "a list of scores" and never pictured "no scores yet", which is
precisely the state every new user starts in.

**The fix:** handle the empty case before dividing:

```python
scores = []
if len(scores) == 0:
    print("No scores yet!")
else:
    total = 0
    for score in scores:
        total = total + score
    print("Average score:", total / len(scores))
```

Test your fix *both* ways: with `[]` and with `[80, 90, 100]` (should say 90.0).
</details>

---

### 🐛 Bug 5 — The password checker that always agrees

```python
password = "banana"
guess = "grape"
if guess == "banana" or "Banana":
    print("Access granted!")
else:
    print("Access denied.")
```

**Expected:** "grape" is wrong, so: `Access denied.`
**Actual:** run it. Uh oh. Try `guess = "anything at all"`. Bigger uh oh.

<details><summary>Show the bug and the fix</summary>

**The bug:** the condition reads naturally in English — *"if the guess is banana or
Banana"* — but Python reads it as two separate questions: (1) is `guess == "banana"`?
and (2) is `"Banana"` … well, is it "truthy"? In Python, any non-empty text counts as
true on its own. So the second half is *always* true, the door is always open, and
every guess is granted access. Code that reads correctly in English and means something
else to the machine — the letter vs. the spirit, in one line.

**The fix:** each side of `or` must be a complete comparison:

```python
if guess == "banana" or guess == "Banana":
    print("Access granted!")
else:
    print("Access denied.")
```

**Species:** logic error — and a genuinely dangerous shape of one, since this bug was a
security hole.
</details>

---

**✅ Checkpoint:** five bugs found, five fixed, and you've now personally met a syntax-
rule tangle, two logic errors, an off-by-one, an edge-case crash, and a security hole.
That's a respectable first day as a detective.

---

## Part 2 — Write a manual test plan: attack a login form (15 minutes)

You're now the QA professional. The product: an ordinary login form — an email box, a
password box, a "Log in" button. Your job: plan how to test it *before* trusting it.

Copy this template onto paper or into a note:

```
TEST PLAN: Login form
Date:            Tester: (you)

#  | What I'll try                  | What SHOULD happen
---+--------------------------------+-------------------------
1  | Correct email + correct pass   | Logged in
2  | Correct email + wrong pass     | Polite error; NOT logged in
3  |                                |
...
```

Rows 1–2 are done for you: the "happy path" and the most obvious failure. Now fill in
**at least 10 more rows of evil inputs**. Channel every edge case instinct from the
lesson. To get you unstuck, three hints — think about:

- **Emptiness** (what if a box — or both — is left blank?)
- **Extremes** (a 3,000-character password? an email that's one character?)
- **The unexpected** (spaces before the email? CAPITALS? emoji 🦆? someone pasting a
  whole paragraph? pressing the button five times fast?)

<details><summary>After you have 10+, compare with our list</summary>

Some favorites (yours don't need to match — different evil is good evil):

1. Both boxes empty. 2. Email filled, password empty. 3. Password filled, email empty.
4. Email with no `@`. 5. Email with *two* `@`s. 6. Leading/trailing spaces in the email
(should they be forgiven? decide!). 7. Correct email in ALL CAPS (emails usually
shouldn't be case-sensitive; passwords must be). 8. A 3,000-character password.
9. A one-character password. 10. Emoji or accents (José@…) in either box. 11. Rapidly
clicking "Log in" ten times (does it try to log in ten times?). 12. Wrong password ten
times in a row (does anything slow the guessing down?). 13. The word `null` as a
password. 14. Turning the phone sideways mid-typing. 15. Pressing Enter instead of the
button.

Notice what you did: for each row you wrote *what should happen* **before** trying it.
Deciding the expected result in advance is the entire discipline of testing — otherwise
you're not testing, you're watching.
</details>

**✅ Checkpoint:** a table with 12+ rows, each with an expected outcome. Congratulations
— this artifact is a genuine **manual test plan**, and writing one for a form is a real
interview exercise for QA jobs.

---

## Part 3 — The rubber duck ceremony (5 minutes, no skipping)

Pick the Part 1 bug that fooled you longest. Now find a listener: a rubber duck, a
houseplant, a pet, a photo of a duck on your screen. Not a person — that's the point.

Out loud — actually out loud — explain to the duck:

1. What the code was *supposed* to do.
2. What it *actually* did.
3. Line by line, what each line really says (not what you assumed it said).
4. Where the gap between *meant* and *wrote* was hiding.

It will feel ridiculous for about forty seconds. Notice what happens anyway: to speak
each line, you must *actually read* each line — and assumptions you didn't know you were
making become audible. This is why rubber duck debugging survives as a real practice on
real teams: the duck never interrupts, never judges, and works for free.

**✅ Checkpoint:** you explained a bug aloud, start to finish, and can honestly report
whether saying it out loud showed you anything reading silently didn't. (For most
people, most of the time: it does.)

---

## 🎉 Done!

You reproduced bugs, narrowed suspects, fixed all five species, planned an attack on a
login form like a QA pro, and consulted the duck. Next module, we cut an app open and
look at its organs.
