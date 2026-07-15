# 🐍 Module 05 — Your First Code

> **Part 2 — Thinking Like an Engineer** · Previous: [How to Think Like a Programmer](../04-think-like-a-programmer/README.md) · Next: [Data: The World's New Oil](../06-data/README.md)

## What you'll learn

- How to write and run **real Python code** — in your browser, nothing to install
- How a program speaks (`print`), remembers (**variables**), and listens (`input`)
- How a program makes decisions (`if`/`else`) and repeats itself (**loops**)
- How to read an **error message** without panic
- Honestly: what you can and can't build after one lesson

## Why it matters

In [Module 04](../04-think-like-a-programmer/README.md) you wrote algorithms in pseudocode — structured English for humans. Today we take the final step: writing instructions a computer will *actually run*. That moment — typing something, pressing Run, and watching a machine obey you — is a small, permanent change in how you see every app on your phone. After today, software stops being magic. It's instructions, and you can write them.

You don't need to install anything. Everything in this module runs in a free website in your browser, on any laptop or phone. The [lab](lab.md) tells you exactly where to go.

---

## 🐍 Why Python?

A **programming language** is a set of writing rules that both humans and computers can understand — you write in it, and the computer runs it. There are hundreds of programming languages. We start with **Python**, and here's why:

- **It reads almost like English.** Python was designed to be readable. You will look at real Python in a minute and understand most of it before we explain anything.
- **It's not a toy.** Python runs at NASA, at Netflix, in banks, and in science labs around the world. Scientists analyzing telescope data and analysts crunching spreadsheets both reach for Python.
- **It's forgiving for beginners.** Fewer strange symbols, less punctuation to get wrong.

> **⚠️ Watch out:** the goal of today is *not* to memorize Python. It's to recognize the five moving parts every language shares: speaking, remembering, listening, deciding, repeating. Learn these once and every other language is the same story with different spelling.

---

## 📢 print() — the program speaking

Here is a complete, genuine Python program. One line:

```python
print("Hello, world!")
```

Run it, and the screen shows: `Hello, world!`

Line by line (there's only one): `print` is Python's word for "display this on the screen." The parentheses `()` hold *what* to display. The quotation marks say "this is text, show it exactly as written."

> **🌉 Analogy:** `print` is the program's **mouth**. A program does its work silently, inside the machine. Every time you want it to say something out loud, you give it a `print` line.
>
> *Where the analogy breaks down:* a mouth speaks and the words vanish. `print` writes to the screen, where the words stay — more like a mouth attached to a ticker-tape machine.

By tradition, "Hello, world!" is every programmer's first program. When you run it in the lab, you'll be joining a ritual that goes back to the 1970s.

---

## 🫙 Variables — the program remembering

A **variable** is a named container that stores a piece of information so the program can use it later. Remember the "oldest so far" note from Module 04? That note was a variable.

> **🌉 Analogy:** a variable is a **labeled jar** on a kitchen shelf. The label says `sugar`; the contents are whatever you put in. You can look inside whenever you like, and you can empty the jar and put something new in — the label stays the same.
>
> *Where the analogy breaks down:* pour new contents into a real jar and the old contents are still around somewhere (on the counter, probably). Put a new value in a variable and the old value is *gone*, instantly and completely.

```python
name = "Priya"
age = 34
print(name)
print(age)
```

Line by line:

1. `name = "Priya"` — make a jar labeled `name`, put the text `"Priya"` inside. In code, `=` doesn't mean "equals" like in school math; it means **"store this on the right into the jar on the left."**
2. `age = 34` — a second jar, labeled `age`, containing the number 34.
3. `print(name)` — no quotation marks this time! So Python doesn't print the word `name`; it opens the jar called `name` and prints what's inside: `Priya`.
4. `print(age)` — opens the other jar: `34`.

And you can swap contents: if a later line says `age = 35`, the jar now holds 35, and the 34 is gone. Happy birthday.

## 🔢 Numbers vs. text: why `5` and `"5"` are different

A quick but important preview. Python treats *kinds* of information differently. A **data type** is the kind of value something is — for now, two kinds matter:

- A **number**, like `5` — something you can do math with.
- A **string** — programmer-speak for a piece of text, like `"hello"` or `"5"`. Anything in quotation marks is a string.

Why care? Because `5 + 5` is `10`, but `"5" + "5"` is `"55"` — Python glues strings together instead of adding them. To Python, `"5"` is not a quantity; it's a character, the same kind of thing as `"a"` or `"?"`. Confusing numbers with strings is one of the most common beginner stumbles, so when it happens to you, you'll know: check the quotation marks. (We'll dig deeper into kinds of data in [Module 06](../06-data/README.md).)

> **✅ Check yourself**
>
> 1. What does the `=` sign do in `city = "Lagos"`?
> 2. What will `print(city)` show — the word `city` or the word `Lagos`?
> 3. Is `"34"` a number or a string?
>
> <details><summary>Show answer</summary>
>
> 1. It stores the value on the right (`"Lagos"`) into the variable (jar) named on the left (`city`).
> 2. `Lagos` — no quotation marks around `city` means "open the jar and show what's inside."
> 3. A string. The quotation marks make it text, even though it looks like a number. `"34" + "1"` would give `"341"`, not 35.
> </details>

---

## 👂 input() — the program listening

`print` is the mouth; `input` is the **ear**. The `input` instruction makes the program pause, wait for the person at the keyboard to type something, and hand over whatever they typed.

```python
name = input("What is your name? ")
print("Nice to meet you, " + name)
```

Line by line:

1. `name = input("What is your name? ")` — display the question, then *wait*. Whatever the person types goes into the jar labeled `name`.
2. `print("Nice to meet you, " + name)` — glue two strings together: the fixed text and the contents of the jar. If you typed `Sam`, the screen shows `Nice to meet you, Sam`.

Two lines, and your program is already interactive — it behaves differently for every person who runs it. One catch worth knowing now: **everything `input` hands you is a string**, even if the person types `34`. Keep that in your back pocket; it explains a classic beginner surprise in the lab.

---

## 🚦 if / elif / else — forks in the road

Programs constantly choose between paths — the diamonds in your Module 04 flowchart. In Python, the diamond is spelled `if`.

> **🌉 Analogy:** `if` is a **bouncer at a club door**, checking IDs. *If* you're 18 or over → come in. *Otherwise* → sorry, not tonight. One check, two paths, everybody goes down exactly one of them.
>
> *Where the analogy breaks down:* a human bouncer can be argued with, or waves in someone who looks 25. The `if` never bends. 17 years and 364 days is a no.

```python
age = 20
if age >= 18:
    print("Welcome in!")
elif age >= 16:
    print("You can enter, but no wristband.")
else:
    print("Sorry, come back in a few years.")
```

Line by line:

1. `age = 20` — a jar with 20 in it.
2. `if age >= 18:` — the first check: is the value in `age` greater than or equal to 18? The colon `:` means "here comes what to do if yes."
3. `    print("Welcome in!")` — notice this line is pushed to the right. That indent is how Python knows this line belongs *inside* the if. It runs only when the check passes.
4. `elif age >= 16:` — short for "else if": a second check, tried **only if the first one failed**.
5. Its indented line — runs only if check 1 failed and check 2 passed.
6. `else:` — the catch-all: what to do if *every* check above failed.
7. Its indented line — the "sorry" message.

With `age = 20`, the first check passes, so the screen shows `Welcome in!` — and Python skips the rest entirely. One fork, one path taken.

---

## 🔁 Loops — the program repeating

Module 04's big insight: computers are phenomenal at repetition. Loops are how you ask for it. Python has two, and the difference is *what kind of stopping* you want.

**A `for` loop repeats once for each item in a collection.**

> **🌉 Analogy:** unpacking a shopping basket. *For each item in the basket:* take it out, put it away. You don't decide in advance how many times to repeat — the basket decides. Empty basket, loop over.

```python
for friend in ["Amara", "Ben", "Chloe"]:
    print("Hello, " + friend + "!")
```

Line 1: "for each item in this list of three names, calling the current one `friend`, do the indented lines." Line 2 runs three times, and each time the jar `friend` holds the next name. Output:

```
Hello, Amara!
Hello, Ben!
Hello, Chloe!
```

**A `while` loop repeats as long as a condition stays true.**

> **🌉 Analogy:** a recipe that says "**stir until thick**." Nobody tells you how many stirs. You stir, check, stir, check — and stop the moment the condition changes.
>
> *Where both analogies break down:* you would eventually stop stirring out of boredom or suspicion that something's wrong. A computer will not. If the condition never changes, a `while` loop runs *forever* — the famous **infinite loop**, and every programmer has caused one. (The fix is undramatic: stop the program and find out why your condition never became false.)

```python
countdown = 3
while countdown > 0:
    print(countdown)
    countdown = countdown - 1
print("Lift off!")
```

Line by line: start the jar at 3. While the jar holds more than 0: print it, then put back one less than what's inside. So it prints 3, 2, 1 — then the check `countdown > 0` fails (0 is not more than 0), the loop ends, and the final unindented line prints `Lift off!`.

> **✅ Check yourself**
>
> 1. You want to send the same message to everyone in your contacts list. `for` loop or `while` loop?
> 2. You want to keep asking for a password until the right one is typed. `for` or `while`?
> 3. In the countdown, what would happen if we forgot the line `countdown = countdown - 1`?
>
> <details><summary>Show answer</summary>
>
> 1. `for` — you have a collection, and you want one repeat per item.
> 2. `while` — you don't know how many tries it will take; repeat *while* the password is wrong.
> 3. The jar would stay at 3 forever, `countdown > 0` would always be true, and the program would print 3 endlessly — an infinite loop.
> </details>

---

## 🧩 Putting it all together: one small, complete program

Everything above, in one program you'll build yourself in the lab. Read it slowly — you now know every piece.

```python
print("Welcome to the Rocket Club!")
name = input("What is your name? ")
age = int(input("How old are you? "))

if age >= 12:
    print("You're cleared for launch, " + name + "!")
    countdown = 5
    while countdown > 0:
        print(countdown)
        countdown = countdown - 1
    print("Lift off! 🚀")
else:
    print("Sorry " + name + ", pilots must be 12 or older.")
    print("Come back in " + str(12 - age) + " years!")
```

The walkthrough:

- **Line 1** — the program speaks: a welcome banner.
- **Line 2** — the program listens: your name goes into the `name` jar.
- **Line 3** — listens again, with a twist. Remember, `input` always hands over a *string* — and you can't compare the string `"9"` with the number 12. `int(...)` converts the string into a real number (int is short for **integer**, a whole number). Jar `age` now holds a number.
- **Line 5** — the bouncer: is `age` at least 12?
- **Lines 6–10** — the "yes" path (all indented under the `if`): a personalized message, then a jar set to 5, then a `while` loop that prints 5, 4, 3, 2, 1, then lift-off.
- **Lines 11–13** — the "no" path: a gentle rejection. `str(...)` is the reverse of `int(...)` — it turns the number `12 - age` back into a string so it can be glued into the sentence.

Fifteen lines. Speaking, listening, remembering, converting, deciding, repeating. That is — honestly — the skeleton of most software you have ever used, at a much smaller scale.

---

## 🩹 Errors are normal (and weirdly polite)

At some point today you will see something like:

```
File "main.py", line 3
    print("Hello"
                 ^
SyntaxError: '(' was never closed
```

Your first instinct will be *I broke it*. You didn't. Nothing is broken, and nobody is judging you.

> **🌉 Analogy:** an error message is the computer being a **pedantic proofreader**. It read your instructions, hit something it couldn't understand, and handed the page back with a note: *which line* (line 3), *where on the line* (the little `^` arrow), and *what confused it* (a bracket was opened and never closed).
>
> *Where the analogy breaks down:* a proofreader reads the whole page and marks everything. The computer stops at the *first* problem it hits and refuses to go on. Fix that one, run again, and it will tell you about the next — one complaint at a time.

The habit to build from day one: **read the message**. Beginners look away from error text as if it were an angry red exam mark. It isn't — it's the machine doing half your detective work from Module 04 for you, usually naming the exact line. Professional programmers see errors every single working day. The difference between a beginner and a pro is not fewer errors; it's less fear of them.

---

## 💪 What you can and can't do now — honestly

Let's be straight with each other, because motivation built on hype collapses fast.

**What you cannot do yet:** build Instagram. Real apps involve screens, databases, servers, and teams — the topics of Parts 3, 4, and 5 of this course. Anyone who promises "build the next Facebook in a weekend" is selling something.

**What you genuinely can do, or nearly can:** automate small, boring chores. A program that renames 200 photo files. One that adds up expenses. One that picks whose turn it is to do the dishes. One that quizzes your kid on multiplication tables. These sound humble. They are the *actual* daily magic of knowing how to code — thousands of people save hours every week with programs the size of the rocket example above. (The [Automate the Boring Stuff](resources.md) book in this module's resources is an entire, wonderful free book about exactly this.)

---

## 🎁 Recap

- **Python** is a real, professional programming language that happens to read almost like English — that's why we start there.
- `print` is the program's mouth; `input` is its ear.
- A **variable** is a labeled jar: store a value, look at it, replace it.
- Numbers and **strings** (text) are different kinds of data — `5 + 5` is `10`, but `"5" + "5"` is `"55"`.
- `if` / `elif` / `else` is the bouncer: one check, one path taken.
- `for` repeats once per item in a basket; `while` repeats until a condition changes.
- Errors are a pedantic proofreader, not a verdict on you. Read the message; it names the line.

## 🌉 Next up

Every program you wrote today worked on little scraps of information — a name, an age, a list of three friends. Real software works on *oceans* of information: every photo, message, and payment you've ever made. In [Module 06 — Data: The World's New Oil](../06-data/README.md), we look at what data actually is, the containers programs keep it in, and why companies are so hungry for yours.

But first: the [lab](lab.md). Today is the day you actually run code. Go press the button.
