# 🔧 Lab 04 — Thinking in Exact Steps

> Time: about 90 minutes total (you can split it across days). Tools: paper, a pen, a web browser. Nothing to install, nothing to sign up for.

This lab has four exercises. They build on each other, so do them in order. Exercises 1–3 need only paper. Exercise 4 uses a free website.

---

## Exercise 1: The Peanut Butter Sandwich Game (20 min)

You met this in the lesson — now live it. You can use any spreadable food you have: peanut butter, jam, butter, chocolate spread.

**With a partner (best version):**

1. Put on a table: a bag or loaf of bread (closed), a jar of spread (lid on), and a butter knife.
2. One person is the **Writer**, the other is the **Robot**. The Writer writes numbered instructions for making a sandwich — *without touching anything*.
3. The Robot follows the instructions with total, merciless literalness. No filling gaps. No common sense. If the instructions say "put peanut butter on bread" and the jar is closed, put the closed jar on the bag.
4. Watch it go wrong. Laugh. Then the Writer revises the instructions and you run it again.
5. Repeat until the Robot produces an actual sandwich.

**Solo version:** write your instructions first, then switch hats. Follow your own instructions as the most maliciously literal robot you can be. Be honest — did you say to open the jar? To pick up the knife? Which end of the knife?

**✅ What you should see:** your first version fails in at least three funny ways. Your final version is *much* longer than you expected — probably 15–25 steps. That gap between "what I meant" and "what I said" is the whole point of this module.

---

## Exercise 2: Pseudocode for a Cup of Tea (20 min)

1. On paper, write pseudocode for making a cup of tea (or coffee, if that's your drink). One step per line. Number the lines.
2. Include at least **one decision** (an IF — for example, "IF the person takes sugar…") and at least **one loop** (a repeat — for example, "WHILE the water is not boiling, wait").
3. Now trade with a partner, or set it aside for an hour and come back to it as a stranger.
4. Attack it for exactness, peanut-butter style. Circle every gap: Did you say to get a cup? Is the kettle plugged in? How much water? How long does the teabag stay in? What does "wait" mean — check *what*, and *how often*?
5. Rewrite it once, fixing the circled gaps.

**✅ What you should see:** version 2 is roughly twice as long as version 1, and it contains at least one diamond-shaped decision moment and one "go back and check again" loop. If it does, you have written a real algorithm.

---

## Exercise 3: Flowchart — "Is This Email Spam?" (20 min)

Time to draw. You'll design the decision logic a spam filter might use — on paper.

1. Draw a rounded box at the top: **Start: an email arrives**.
2. Draw your first diamond (decision). For example: *"Is the sender in my contacts?"* Draw two arrows out: **Yes** and **No**.
3. Keep going. Use at least **three diamonds**. Ideas for questions: Does the subject line contain "FREE" or "WINNER"? Does it ask for my password or bank details? Have I ever replied to this sender? Are there lots of spelling mistakes?
4. Every path must eventually end in one of two boxes: **Inbox** or **Spam folder**.
5. Test your flowchart with two real emails from your own inbox — one genuine, one junk. Trace each one through the diamonds with your finger.

**✅ What you should see:** both test emails land in the right box. If your genuine email lands in Spam, congratulations — you've found a bug, and it's in your instructions, not in the emails. Fix a diamond and trace again. (Real spam filters have exactly this problem; that's why real mail sometimes lands in your junk folder.)

---

## Exercise 4: One Hour of Code (60 min)

Now feel loops and decisions *move*, with zero typing.

1. In any web browser (phone, tablet, or laptop), go to **code.org** and find **Hour of Code** — a free set of hour-long beginner activities. No account or sign-up is needed to play (if the site offers you a sign-in, look for the option to continue without one).
2. Pick any activity that appeals to you — the dance, game, or maze-style ones are all good. They use **blocks**: puzzle pieces you drag together instead of typing code.
3. Work through the levels for about an hour. Take your time; the levels get gradually trickier.
4. As you play, keep a hunt list on paper and tick these off when you meet them:
   - A **loop** block (often called "repeat") — one block doing something many times.
   - A **decision** block (often called "if") — the program choosing between paths.
   - A moment where your solution *ran* but did the **wrong thing** — and you fixed it by changing the blocks, not by blaming the computer.

**✅ What you should see:** all three items ticked. That third tick is your first real debugging experience: the machine did exactly what your blocks said, the blocks were wrong, and you fixed them. Welcome to the club.

> **⚠️ Watch out:** websites change their menus now and then. If a button isn't where these steps suggest, don't panic — look for anything labeled "Hour of Code," "Try now," or "Start." The activity itself will guide you once you're in.

---

## Done?

You have now: given literal instructions and watched them fail, written and hardened pseudocode, drawn a flowchart with decisions, and steered a program with loops and conditions. Take the [quiz](quiz.md), then browse the [extra resources](resources.md). Next module, we swap blocks for real Python: [Your First Code](../05-your-first-code/README.md).
