# 💿 Module 02 — What Is Software?

> **What you'll learn:** what software actually is, what a "file" really is, why
> programming languages exist, what an operating system does all day, and where the
> apps on your phone come from.
>
> **Why it matters:** in [Module 01](../01-what-is-a-computer/README.md) you met the
> machine — the tireless, literal instruction-follower. But a machine with no
> instructions does nothing at all. This module is about the instructions.

---

## 🧠 Hardware vs software: the piano and the sheet music

Have you ever wondered why a brand-new phone and a five-year-old phone can run the same
app? Or why "an update" can change what your phone does without anyone opening it up
with a screwdriver? The answer is the most important split in all of computing.

**Hardware** is every physical part of a computer — anything you could touch, drop, or
spill coffee on. **Software** is the instructions the hardware follows — you can't touch
software, only what it makes the hardware do.

> 🌉 **Analogy:** Hardware is a piano; software is the sheet music. The same piano can
> play a lullaby or a thunderstorm — the piano doesn't change, the music does. Or if
> you prefer: hardware is the body, software is the thoughts running through it.
>
> **Where the analogy breaks down:** a piano needs a human to read the sheet music.
> A computer reads and follows its own sheet music, billions of notes per second, with
> no performer in between.

This is why software can be sent over the internet, copied a million times for free, and
changed overnight. It's not a *thing*. It's *instructions* — and instructions are
information.

## 📝 What a program actually is

A **program** is a list of instructions for a computer, written in advance and saved so
it can be followed whenever you like. That's the whole definition. WhatsApp is a list of
instructions. A video game is a list of instructions. A very, very long list — big apps
run to millions of lines — but a list all the same.

Here's a program, written in plain English, for a task you know:

1. Wait until the user taps the "Send" button.
2. Read whatever text is in the message box.
3. If the box is empty, do nothing and go back to step 1.
4. Otherwise, send the text to the recipient over the internet.
5. Show the message in the chat with a little clock icon.
6. When the recipient's server confirms delivery, replace the clock with a tick.

Real programs are written more precisely than this (we'll get there in Module 05), but
the shape is exactly right: a numbered list of steps, including steps for when things
go wrong. And that list is *stored as a file*.

Which raises the question this course promised to answer honestly...

## 📦 What is a file, really?

You use files every day — "attach a file", "the file is too big" — but what *is* one?

A **file** is a labeled box of bytes: a chunk of data saved in storage under a name.
That's all. Remember from Module 01 that everything — text, photos, songs — becomes
numbers, and numbers become bytes. A file is a bunch of those bytes, kept together,
with a label so you can find it again.

- A photo file: bytes describing the color of every dot.
- A song file: bytes describing sound-pressure measurements.
- A document: bytes describing letters (and fonts, and margins).
- **A program: bytes describing instructions.** An app is a file too — that's the
  punchline. When you "install an app", you are copying a box of instruction-bytes into
  your pantry (storage).

The label on the box often ends with a short tag called an **extension** — the part of a
filename after the dot, like `.jpg` or `.txt`, which hints what kind of bytes are inside.
`holiday.jpg` says "these bytes are a photo". `letter.txt` says "these bytes are plain
text". The extension doesn't *make* the file a photo — it's a label on the box, not the
contents — but it tells the computer which program should open it.

> 🌉 **Analogy:** Storage is a warehouse of labeled boxes. Every box contains only one
> thing — bytes — but the labels (`report.txt`, `song.mp3`, `whatsapp.apk`) tell you how
> to interpret what's inside. A box labeled "photo" and a box labeled "song" are made of
> exactly the same stuff: numbers.
>
> **Where the analogy breaks down:** unlike warehouse boxes, files can be copied
> perfectly, instantly, and for free — and relabeling a box (renaming `song.mp3` to
> `song.txt`) doesn't change the bytes inside, it only confuses whoever opens it.

> ✅ **Check yourself**
> 1. Software vs hardware — which one is the sheet music?
> 2. What is a file, in one sentence?
> 3. Is an app a file?
>
> <details><summary>Show answers</summary>
>
> 1. Software. Hardware is the piano — the physical machine.
> 2. A labeled box of bytes saved in storage — data kept together under a name.
> 3. Yes (usually a bundle of files): a program's instructions, stored as bytes, ready
>    to be copied into memory and followed.
> </details>

## 🌐 Why programming languages exist

Module 01 showed that a computer's native language is binary: 0s and 1s. So in theory,
programmers could write apps as millions of 0s and 1s directly. In the 1940s, they
actually did — flipping physical switches, one instruction at a time. It was slow,
maddening, and almost impossible to get right.

Humans needed a better way. A **programming language** is a way of writing instructions
for a computer in something close to human words, which then gets translated into the
binary the machine actually follows. Instead of `10111000 01100100...`, a programmer
writes something like `price = 100`, and a translation step turns it into switch
patterns.

There are hundreds of programming languages — Python, JavaScript, C, Swift — the way
there are many human languages. They differ in style and purpose, but every one of them
exists for the same reason: humans think in words, machines run on 0s and 1s, and
something has to bridge the gap.

### The two kinds of translators

That "something" comes in two flavors, and the difference is worth knowing because
engineers mention it constantly.

> 🌉 **Analogy:** Imagine a French novel that an English-speaking friend wants to read.
> Option one: a translator converts the *whole book* in advance, and your friend reads
> the finished English edition at full speed. Option two: a live interpreter sits beside
> your friend and translates *line by line* as they go — they can start instantly, but
> reading is slower, and a mistake on page 300 isn't discovered until page 300.

A **compiler** is the book translator: it converts a whole program into machine-ready
binary in advance, producing a file the computer can run at full speed. An
**interpreter** is the live interpreter: it translates and follows the program line by
line, as it runs.

> **Where the analogy breaks down:** unlike human translation, computer translation is
> perfectly faithful — no nuance is lost. And many modern languages blur the line,
> mixing both approaches. Don't worry about the hybrids; the two pure flavors are the
> idea to keep.

Either way, the takeaway is the same: **the code humans write is text — readable words
in a file — and translation turns it into something a machine can follow.** You'll see
this with your own eyes in the lab.

## 🏨 The operating system: the hotel manager

Here's a puzzle. Your phone runs many apps at once — music playing, messages arriving,
a map navigating. But Module 01 said there's one CPU (well, a handful of cores), one
counter, one screen. Who decides which app gets the chef's attention? Who stops two
apps from scribbling over each other's part of the counter?

Meet the most important program on any computer. The **operating system** (or **OS**)
is the master program that manages the machine — it starts and stops other programs,
divides up memory and CPU time between them, and handles all the hardware so ordinary
apps don't have to.

> 🌉 **Analogy:** The OS is the manager of a grand hotel. Guests (apps) check in and
> are assigned rooms (memory) — and no guest may barge into another guest's room. The
> manager schedules the shared facilities (CPU time, like slots in the dining room),
> answers the front desk (your taps and clicks), and deals with deliveries and the
> front door (screen, network, speakers) so guests never have to. When a guest
> misbehaves, the manager can evict them — that's what happens when the system "force
> quits" a frozen app.
>
> **Where the analogy breaks down:** a hotel manager juggles a few hundred guests a
> day. An OS switches between programs *thousands of times per second*, so fast that
> every app feels like it has the whole hotel to itself. That illusion is the OS's
> greatest trick.

You already know several operating systems by name: **Windows** and **macOS** (on
laptops and desktops), **Android** and **iOS** (on phones), and **Linux** — a free OS
that quietly runs most of the servers behind the internet, and sits inside Android too.
Different brands, different looks, same hotel-manager job.

### Apps vs the OS

An **app** (short for *application*) is a program built to do a task for you — chat,
navigate, edit photos — as opposed to the OS, which exists to run the machine itself.
The division of labor: apps ask, the OS provides. When a messaging app wants to make a
sound, it doesn't operate the speaker hardware itself — it asks the OS, "play this,
please." That's why one app can run on thousands of different phone models: the OS
handles the hardware differences.

> ✅ **Check yourself**
> 1. Name three jobs the operating system does.
> 2. Why does one CPU feel like it's running ten apps "at the same time"?
> 3. Is Android an app or an OS?
>
> <details><summary>Show answers</summary>
>
> 1. Any three of: starting/stopping programs, dividing up memory, scheduling CPU time,
>    handling hardware (screen, speakers, network), keeping apps out of each other's
>    memory, force-quitting misbehaving programs.
> 2. The OS switches the CPU between apps thousands of times per second — too fast for
>    humans to notice the taking of turns.
> 3. An OS — the hotel manager of the phone. The apps are its guests.
> </details>

## 🚚 Where apps come from

So where does the weather app on your phone actually come from? The journey has four
stops:

1. **People write code.** A **developer** is a person who writes programs for a living.
   Developers (sometimes one, sometimes thousands) type instructions as text files in a
   programming language.
2. **The code is packaged.** The text is translated (compiled) and bundled with images,
   sounds, and settings into one installable package — one big labeled box of bytes.
3. **The package is distributed.** An **app store** is a catalog run by the OS maker
   (Apple's App Store, Google Play) that checks apps and delivers them to your device.
   On laptops, apps also arrive as direct downloads from websites. "Installing" =
   copying the package into your storage and telling the OS it's there.
4. **The package gets updated.** Developers keep changing the code — and ship you the
   new version.

Why do apps update *so often*? Three honest reasons: fixing **bugs** (mistakes in the
instructions — remember, the computer follows mistakes as obediently as everything
else), patching security holes before attackers use them, and adding or changing
features. An update is a new box of bytes replacing the old one. Nothing mystical —
new sheet music for the same piano.

## 📖 Open source vs closed source: the community cookbook

One last split you'll hear about for the rest of this course. Since programs are text
files written by people, a question follows: *who gets to read the text?*

**Closed source** software keeps its code secret — you get the packaged app, but the
recipe stays locked in the company vault (like Coca-Cola's formula). Windows, iOS, and
most big-name apps work this way. **Open source** software publishes its code for
anyone to read, copy, and improve — like a community cookbook that thousands of cooks
correct and extend together.

Open source is not a fringe hobby. **Linux**, the open-source OS mentioned above, runs
most of the world's servers — when you use almost any website, a Linux machine answers.
The cookbook approach built much of the internet's foundations.

And here's a nice full-circle fact: **this course itself is open source, and lives on
GitHub** — a website where people store and share code and collaborate on it (you'll
use it properly in Module 08). The lesson you're reading is a text file that anyone can
read and propose fixes to. In the lab, you'll go look at the Linux cookbook itself.

## 🎯 Recap

- **Hardware** is the piano; **software** is the sheet music — untouchable instructions
  that make the physical machine do things.
- A **program** is a stored list of instructions. An **app** is a program that does a
  task for you.
- A **file** is a labeled box of bytes; the **extension** (`.txt`, `.jpg`) is the label
  hinting what's inside. Programs are files too.
- **Programming languages** let humans write instructions as readable text; a
  **compiler** translates the whole book in advance, an **interpreter** translates live,
  line by line.
- The **operating system** is the hotel manager: rooms (memory), schedules (CPU time),
  the front door (hardware). Windows, macOS, Linux, Android, iOS — same job, different
  brands.
- Apps come from **developers** → packaging → **app stores**/downloads → endless
  **updates** (bug fixes, security, features).
- **Open source** = community cookbook (Linux, and this course); **closed source** =
  secret recipe.

## 🚀 Next up

You now have the machine (Module 01) and the instructions (this module). But your
devices spend most of their time doing something we haven't explained at all: *talking
to other computers, all over the planet*. How does a message cross an ocean in a blink?
That's [Module 03: How the Internet Works](../03-how-the-internet-works/README.md).

*Before you go: the [lab](lab.md) is a software safari on your own device — including
your first look at real code in the wild. Then try the [quiz](quiz.md) or the
[extra resources](resources.md).*
