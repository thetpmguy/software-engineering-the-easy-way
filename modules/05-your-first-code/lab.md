# 🔧 Lab 05 — Write and Run Real Python

> Time: 60–90 minutes. Tools: a web browser — laptop is comfiest, but a phone works. Nothing to install. Free.

Today you run real code. Five exercises, each building on the last. Type the code yourself rather than copy-pasting — your fingers learn faster than your eyes.

---

## Step 0: Open a Python playground (5 min)

You need a website where you can type Python and press Run. Any of these works — pick the first one that loads for you:

1. **trinket.io** — go to the site and look for an option to try or create a Python trinket without an account. You'll get two panels: one to type code in, one showing the output, with a **Run** button (often a "play" ▶ triangle).
2. **The official Python console at python.org/shell** — a black box where you type one line, press Enter, and see the result immediately. Fine for Exercise 1, but for the later exercises (which have many lines) a two-panel site like trinket is more comfortable.
3. **Fallback:** search the web for "run Python online free". Many good sites exist (look for names like Replit or Programiz). You want: a place to type multiple lines, and a Run button. Avoid anything demanding payment; sign-up should not be required — if a site insists on one, try another.

> **⚠️ Watch out:** websites redesign their buttons regularly, so don't worry if yours doesn't match these descriptions word for word. Whatever the site looks like, you are looking for exactly two things: *a box to type code in* and *a Run button*. Find those and you're in business.

**✅ What you should see:** an empty code area, ready for you. That blank box is the same blank box every programmer on Earth started with.

---

## Exercise 1: Hello, world (5 min)

1. In the code area, type exactly (capitals, brackets, and quotes matter):

   ```python
   print("Hello, world!")
   ```

2. Press **Run**.

**✅ What you should see:**

```
Hello, world!
```

3. Now make it yours. Change the message to greet you by name, and add a second `print` line below it saying anything you like. Run again.

**✅ What you should see:** your two messages, in order, top to bottom. Programs run top to bottom — you've now proven it.

---

## Exercise 2: Mad-libs with variables (10 min)

Variables are labeled jars. Let's fill some and build a silly sentence.

1. Clear the code area (or start a new file) and type:

   ```python
   name = "Zork"
   animal = "hedgehog"
   number = 17
   print(name + " owns " + str(number) + " " + animal + "s.")
   ```

2. Press **Run**.

**✅ What you should see:**

```
Zork owns 17 hedgehogs.
```

3. Now change *only the first three lines* — new name, new animal, new number — and run again. The sentence updates without touching the `print` line. That's the point of variables: the sentence is a template; the jars hold the changeable parts.
4. Notice the `str(number)` in line 4. Try removing `str(` and its matching `)` so it reads `... + number + ...`, and run.

**✅ What you should see:** an error mentioning something like `can only concatenate str (not "int") to str`. Translation from proofreader-speak: "you asked me to glue text to a *number*, and I only glue text to text." Put the `str(...)` back — it converts the number into text first. Congratulations: that was your first deliberate error, and you read the message. That's the habit.

---

## Exercise 3: The age gate (10 min)

The bouncer from the lesson, live.

1. New program:

   ```python
   age = int(input("How old are you? "))
   if age >= 18:
       print("Come on in!")
   else:
       print("Sorry, adults only.")
   ```

2. Careful with the details: the lines under `if` and `else` are indented (pushed right — use 4 spaces or the Tab key), and both `if` and `else` lines end with a colon `:`.
3. Run it. The program will *wait* for you — type an age into the output panel and press Enter.

**✅ What you should see:** with `25`, you get `Come on in!`. Run again with `12`: `Sorry, adults only.` Same program, different path — that's the fork in the road.

4. Stretch goal: add an `elif age >= 16:` branch between the `if` and the `else` that prints something like `"You may enter with a guardian."` Run all three cases: 25, 16, 12.

---

## Exercise 4: Countdown (10 min)

1. New program:

   ```python
   countdown = 5
   while countdown > 0:
       print(countdown)
       countdown = countdown - 1
   print("Lift off! 🚀")
   ```

2. Note which lines are indented: the two lines under `while` are inside the loop; the final `print` is not indented, so it runs *after* the loop finishes.
3. Run it.

**✅ What you should see:**

```
5
4
3
2
1
Lift off! 🚀
```

4. Experiment time: change the starting number to 10. Then try changing `countdown - 1` to `countdown - 2` — before running, predict what will print. Were you right?

> **⚠️ Watch out:** if you ever remove the `countdown = countdown - 1` line, the loop becomes infinite — it will print the same number forever. This is a rite of passage, and it's harmless: every playground has a **Stop** button (often where Run was). Press it, fix the code, carry on. You are now officially someone who has survived an infinite loop.

---

## Exercise 5: Mini-project — the Compliment Machine (20 min)

Your first program designed by *you*. Specification: the program asks for the user's **name** and their **mood**, then responds with a compliment that uses both answers.

1. Start from this skeleton and finish it:

   ```python
   print("Welcome to the Compliment Machine!")
   name = input("What's your name? ")
   mood = input("How are you feeling today? ")
   ```

2. Add lines so the machine responds. Minimum version: one `print` that weaves `name` into a compliment.
3. Better version: use `if` / `elif` / `else` on the `mood` answer. For example: `if mood == "sad":` print something extra kind; `elif mood == "happy":` print something celebratory; `else:` a general-purpose compliment. (Note the **double** equals `==` — it means "is equal to?", a question — while single `=` means "store this in the jar." Mixing them up is a classic; the proofreader will tell you.)
4. Deluxe version: end with a `for` loop that showers them with three compliments from a list — flip back to the lesson's `for` example for the shape of it.

**✅ What you should see** (your wording will differ — that's the point):

```
Welcome to the Compliment Machine!
What's your name? Maria
How are you feeling today? sad
Maria, anyone would be lucky to know you.
Chin up — bad days are outnumbered by good ones.
```

If it runs and responds using both answers: **you have written your first real program from a specification.** That's not a beginner's imitation of the job. That *is* the job.

---

## 🩹 When you get an error (read this the moment you need it)

You will hit errors in this lab. Everyone does; it is part of the plan, not a deviation from it. When it happens:

1. **Breathe.** Nothing is broken. Your code is saved. The computer is not upset.
2. **Read the last line of the message** — it names the problem (`SyntaxError: '(' was never closed`, `NameError: name 'nme' is not defined`...).
3. **Find the line number** in the message and look at that line — and the line *above* it (a missing bracket on line 3 is often reported on line 4).
4. **Check the usual suspects:** a missing closing bracket `)`, a missing quote `"`, a missing colon `:` after `if`/`else`/`while`/`for`, indentation that doesn't match, or a variable name spelled two different ways.
5. Fix one thing, run again. The proofreader complains about one problem at a time; that's normal.

Still stuck after five minutes? Retype the example from the lab exactly, confirm it runs, then re-make your changes one at a time, running after each. The step that breaks it *is* the bug — and now you know where it lives.

---

## Done?

Save or copy your Compliment Machine somewhere — it's the first entry in your portfolio. Then take the [quiz](quiz.md), browse the [resources](resources.md), and when you're ready, on to [Module 06 — Data](../06-data/README.md).
