# 🖥️ Module 01 — What Is a Computer, Really?

> **What you'll learn:** what a computer actually is, why everything inside it comes down
> to tiny on/off switches, what the main parts do (in kitchen terms), and why turning it
> off and on again genuinely fixes things.
>
> **Why it matters:** you use a computer for hours every day. After this lesson, the
> glowing rectangle stops being magic and starts being a machine you understand.

---

## 🧠 The glowing rectangle is not magic

Have you ever watched a phone light up and thought, *"I have no idea what is happening in
there"*? You are in good company. Most people — including many people who work in tech
companies — could not explain it either.

Here is the honest truth, and it is the foundation of this whole course:

**A computer is a machine that follows instructions.** That's it. That's the secret.

It has three superpowers, and only three:

1. **It is extremely fast.** A modern phone can follow *billions* of instructions per
   second. Not thousands. Not millions. Billions.
2. **It is extremely obedient.** It never gets bored, never skips a step, never decides
   your instructions are beneath it.
3. **It is extremely literal.** It does exactly what it is told — including the mistakes.
   If the instructions say "add" where they should say "subtract", it will cheerfully
   subtract nothing and add everything, forever.

> 🌉 **Analogy:** A computer is like a brilliant, tireless assistant who takes every
> word you say *literally*. Tell them "put the milk in the fridge" while you're holding
> the milk, and they will stand there waiting, because you never said *when*. Everything
> impressive a computer does — video calls, maps, games — is built from mountains of
> painfully precise instructions written by humans.
>
> **Where the analogy breaks down:** a human assistant would eventually guess what you
> meant. A computer never guesses. It has no "meaning" at all — only instructions.

Every "smart" thing your devices do was made possible by people writing instructions
carefully enough for a machine this literal. That is what software engineering *is*, and
we will spend the rest of the course unpacking it.

## 💡 Binary: why everything is on/off switches

Let's open the box. Inside every computer, there are no words, no pictures, no songs.
There is only electricity, flowing through billions of microscopic switches. Each switch
is either **on** or **off**. Nothing in between.

Why build a machine out of yes/no switches? Because switches are *reliable*. Electricity
is messy — voltage wobbles, wires get warm. But "is the switch on or off?" is a question
with a crisp answer even when things get messy. Two clean states beat ten fuzzy ones.

> 🌉 **Analogy:** Think of a hallway with one light switch. It can say exactly two
> things: on or off. Yes or no. One or zero. Now imagine a hallway with *eight* light
> switches in a row. Suddenly you can express 256 different patterns
> (on-off-off-on-off-on-on-off is one of them). Add more switches, and the number of
> possible patterns explodes.
>
> **Where the analogy breaks down:** your hallway switches flip a few times a day.
> A computer's switches flip *billions of times per second*, and there are billions of
> them on a chip smaller than your fingernail.

This on/off language has a name. **Binary** is a way of writing any number using only
two symbols: 0 (off) and 1 (on). One single on/off switch — one 0 or 1 — is called a
**bit**, the smallest piece of information a computer can hold. Eight bits grouped
together are called a **byte**.

### From switches to numbers

How can a row of switches be a *number*? The same way "352" is a number. In everyday
counting, each position is worth ten times the one to its right: hundreds, tens, ones.
In binary, each position is worth *two* times the one to its right: eights, fours, twos,
ones.

So the binary pattern `0110` means: no eight, one four, one two, no one. Four plus two.
**Six.** With enough switches, you can write any number you like.

### From numbers to everything

Here is the trick that makes the whole digital world possible: **everything is numbers.**

- **Letters?** Give each one a number. Computers use an agreed-upon code where, for
  example, the capital letter "A" is 65. The word "HI" is the numbers 72, 73.
- **Pictures?** A photo is a grid of tiny dots called pixels. Each dot's color is three
  numbers: how much red, how much green, how much blue.
- **Sound?** A microphone measures air pressure thousands of times per second. Each
  measurement is a number. Play the numbers back fast enough, and you hear music.
- **Video?** Pictures, many times per second, plus sound. Numbers and more numbers.

Your favorite song, your family photos, this very sentence: all of it is enormous
piles of 0s and 1s, which are patterns of on/off switches, which are tiny flows of
electricity. No magic. Agreed-upon numbers, all the way down.

> ✅ **Check yourself**
> 1. What are the only two "letters" in a computer's native alphabet?
> 2. How can a computer store a photo if it can only store numbers?
> 3. What is a bit?
>
> <details><summary>Show answers</summary>
>
> 1. 0 and 1 — off and on. That's the entire alphabet.
> 2. A photo is a grid of colored dots, and each dot's color is written as numbers
>    (amounts of red, green, and blue).
> 3. A bit is one single 0-or-1 — the smallest possible piece of information, like one
>    light switch. Eight of them make a byte.
> </details>

## 🔧 The parts: a tour of the kitchen

Time to meet the main parts inside the box. Every computer — a gaming PC, a cheap
laptop, the phone in your pocket — has the same cast of characters. We will use one big
analogy: **a computer is a restaurant kitchen.**

### The CPU — the chef

The **CPU** (central processing unit) is the part of the computer that actually carries
out instructions, one after another, incredibly fast. It is the chef. Every instruction
— add these numbers, compare these letters, move this data — passes through the chef's
hands.

When you hear that a chip runs at "3 gigahertz", that means the chef's internal clock
ticks about three *billion* times per second, doing a small piece of work on each tick.
Modern CPUs actually contain several chefs (called *cores*) working side by side.

### RAM — the kitchen counter

The **RAM** (the computer's short-term working memory) is where the computer keeps
everything it is actively working on *right now*. It is the kitchen counter. The chef
can grab anything on the counter instantly — but the counter has limited space, and here
is the crucial part: **when the power goes off, the counter is wiped completely clean.**

That is why an unsaved document disappears when your laptop dies. It was living on the
counter.

### Storage — the pantry

**Storage** (a hard drive or SSD) is where the computer keeps things permanently, even
with the power off. It is the pantry, or a filing cabinet in the back room. Your photos,
apps, and documents live here. Walking to the pantry is much slower than grabbing
something off the counter — thousands of times slower — but the pantry is huge, and
nothing in it vanishes overnight.

A **hard drive** stores data on spinning magnetic discs (older, cheaper, slower). An
**SSD** (solid-state drive) stores data on chips with no moving parts (newer, faster —
it is why modern laptops start up in seconds). Your phone uses SSD-style storage.

> ⚠️ **Watch out:** People say "memory" for both RAM and storage, and it causes endless
> confusion. When your phone says "storage full", that's the pantry. When a laptop ad
> brags about "16 GB of RAM", that's the counter. Counter = fast and temporary.
> Pantry = slow and permanent.

### The motherboard — the building itself

The **motherboard** is the large circuit board that all the other parts plug into, with
wiring that lets them talk to each other. It is the restaurant building: the plumbing,
the electrical wiring, the hallways between the kitchen and the pantry. It does no
cooking itself, but without it, nothing is connected to anything.

### The GPU — a thousand junior chefs

The **GPU** (graphics processing unit) is a chip designed to do thousands of small,
simple calculations at the same time. If the CPU is one master chef, the GPU is a
thousand junior chefs who each know how to do only one simple thing — but all at once.

Need to update the color of two million screen pixels sixty times a second? Don't hand
the master chef two million tiny tasks. Hand each junior chef a small batch. This is why
GPUs power video games — and, as it turns out, modern AI, which also needs oceans of
small calculations done in parallel. (More on that in Module 16.)

### Input and output — the doors

**Input devices** are how information gets *into* the computer: keyboard, mouse,
touchscreen, microphone, camera. **Output devices** are how information gets *out*:
screen, speakers, printer. In kitchen terms: the order slips coming in, and the finished
plates going out.

> 🌉 **Analogy recap — the whole kitchen:** the **CPU** is the chef, **RAM** is the
> counter (fast, small, wiped clean at closing time), **storage** is the pantry (slow,
> huge, permanent), the **motherboard** is the building's wiring and plumbing, the
> **GPU** is a thousand junior chefs, and **input/output devices** are the order slips
> and the finished plates.
>
> **Where the analogy breaks down:** in a real kitchen, food moves once. In a computer,
> data is *copied*, not moved — reading a file from the pantry leaves the original
> exactly where it was. Also, this kitchen serves a billion plates per second.

> ✅ **Check yourself**
> 1. Your laptop was writing a document, the battery died, and the document is gone.
>    Which part was it living in?
> 2. Which is bigger on a typical device: RAM or storage? Which is faster?
> 3. Why do video games and AI both love GPUs?
>
> <details><summary>Show answers</summary>
>
> 1. RAM — the kitchen counter. Power off means the counter is wiped clean. Saving a
>    file means copying it from the counter into the pantry (storage).
> 2. Storage is much bigger (often 20–50 times bigger). RAM is much faster.
> 3. Both need millions of small, similar calculations done at the same time, and a GPU
>    is built to do exactly that — many simple workers in parallel.
> </details>

## 🔄 Why "turn it off and on again" actually works

It is the most famous advice in tech, and it is not a joke. It really works. Now you can
see why.

As a computer runs for days, the kitchen counter (RAM) gets messy. Apps open and close
but leave crumbs behind. Two programs end up waiting for each other, frozen in an
awkward standoff. Little errors pile up in that temporary working space.

Turning the machine off wipes the counter completely — remember, RAM forgets everything
without power. Turning it back on gives the chef a spotless counter and a fresh start.
The pantry (your files, your photos, your apps) is untouched, because storage keeps its
contents without power.

So a restart doesn't fix anything *permanent*. It throws away the temporary mess. Since
most day-to-day glitches live in the temporary mess, a restart cures a remarkable share
of problems.

## 📱 Your phone IS a computer

Everything above describes your phone, too. A smartphone has a CPU, RAM, storage, a GPU,
input devices (touchscreen, microphone, cameras) and output devices (screen, speaker).
It is not "like" a computer. It **is** a computer — one that happens to fit in a pocket
and include a radio for making calls.

And it is not a weak one. The phone in your pocket is millions of times more powerful
than the computers that guided the Apollo missions to the Moon. When this course says
"computer", your phone always counts.

## 📈 Moore's law, in one paragraph

In 1965, an engineer named Gordon Moore noticed that engineers were managing to fit
roughly *twice* as many switches onto a chip every couple of years — and he predicted
the trend would continue. It did, for decades, and that observation became known as
**Moore's law**: the number of switches on a chip doubles roughly every two years.
Doubling compounds fast. It is why a 1990s computer filled a desk and struggled to show
a photo, while today's phone edits video in your hand. The doubling has been slowing
down lately as switches approach the size of individual atoms — but it explains how we
got here.

## 🎯 Recap

- A computer is a machine that follows instructions: **extremely fast, extremely
  obedient, extremely literal**. It never guesses.
- Inside, everything is **binary** — patterns of on/off switches — because two clean
  states are reliable. One switch is a **bit**; eight bits are a **byte**.
- **Everything is numbers**: letters, photos, songs, and videos are all stored as
  numbers, which are stored as 0s and 1s.
- The kitchen: **CPU** = chef, **RAM** = counter (fast, temporary), **storage** =
  pantry (slow, permanent), **motherboard** = the building's wiring, **GPU** = a
  thousand junior chefs, **input/output** = orders in, plates out.
- **Restarting works** because it wipes the messy counter (RAM) while leaving the
  pantry (storage) untouched.
- **Your phone is a computer.** A very powerful one.

## 🚀 Next up

You now know what the machine is. But a machine that follows instructions is useless
without... instructions. Where do they come from? What is an "app", really? What is a
file? That is **software** — and it is the subject of
[Module 02: What Is Software?](../02-what-is-software/README.md)

*Before you go: try the [lab](lab.md) — a guided tour of your own device's kitchen —
then take the [quiz](quiz.md). Curious for more? See the [extra resources](resources.md).*
