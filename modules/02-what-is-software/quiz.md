# ✅ Quiz 02 — What Is Software?

> Answer in your head first, then open each fold. Missed a few? Perfectly normal —
> revisit the [lesson](README.md) section with the matching heading.

---

**1. In your own words: what's the difference between hardware and software?**

<details><summary>Show answer</summary>

Hardware is the physical machine — anything you could touch or drop. Software is the
instructions the machine follows — untouchable information. The piano vs the sheet
music: same piano, different music, completely different behavior.
</details>

**2. What is a program?**

<details><summary>Show answer</summary>

A list of instructions for a computer, written in advance and stored (as a file) so it
can be followed on demand. Every app, from Calculator to WhatsApp, is one of these
lists — some run to millions of lines.
</details>

**3. What is a file, really? And what does the extension (like `.jpg`) do?**

<details><summary>Show answer</summary>

A file is a labeled box of bytes — a chunk of data stored under a name. The extension
is part of the label: a hint about what kind of bytes are inside (`.jpg` = photo,
`.txt` = plain text), which tells the computer which program should open it. Renaming
the extension changes the label, not the contents.
</details>

**4. Why do programming languages exist, when computers only understand binary?**

<details><summary>Show answer</summary>

Because humans can't comfortably read or write millions of 0s and 1s. A programming
language lets people write instructions as near-human text, and a translation step
(compiler or interpreter) converts that text into the binary the machine follows. The
language exists for the humans, not for the machine.
</details>

**5. Compiler vs interpreter — which is the book translator, and which is the live
interpreter?**

<details><summary>Show answer</summary>

A **compiler** translates the whole program in advance (the finished translated book —
runs at full speed afterward). An **interpreter** translates and executes line by line
while the program runs (starts instantly, runs a bit slower, and a mistake on "page
300" only surfaces when you get there).
</details>

**6. Your phone is playing music, downloading email, and showing a map — apparently all
at once. What is really happening, and who arranges it?**

<details><summary>Show answer</summary>

The operating system rapidly switches the CPU between the apps, thousands of times per
second — turn-taking too fast to perceive. The OS (the hotel manager) also gives each
app its own memory "room" and handles all the shared hardware, so each app behaves as
if it had the machine to itself.
</details>

**7. Name three operating systems — and say what makes something an OS rather than an
app.**

<details><summary>Show answer</summary>

Any three of: Windows, macOS, Linux, Android, iOS. An OS exists to run the *machine* —
managing memory, CPU time, and hardware for all other programs. An app exists to do a
*task for you* (chat, navigate, edit) and gets everything it needs by asking the OS.
</details>

**8. Why do apps update so often? Give at least two of the three honest reasons.**

<details><summary>Show answer</summary>

(1) Fixing bugs — mistakes in the instructions that the literal-minded machine
faithfully follows; (2) patching security holes before attackers exploit them;
(3) adding or changing features. An update is a fresh box of instruction-bytes
replacing the old one — new sheet music for the same piano.
</details>

**9. When you "install" an app, what physically happens inside your device?**

<details><summary>Show answer</summary>

A package of files — instructions plus images, sounds, and settings — is copied over
the network into your storage (the pantry), and the OS records that it's available to
run. Uninstalling deletes those boxes of bytes again.
</details>

**10. Open source vs closed source — explain the difference with the cookbook analogy,
and name one famous open-source project.**

<details><summary>Show answer</summary>

Closed source keeps the recipe secret: you get the finished dish (the packaged app) but
never the recipe (the code). Open source publishes the recipe for anyone to read, copy,
and improve — a community cookbook. Famous examples: Linux (which runs most of the
internet's servers) — and this very course, which lives openly on GitHub.
</details>

**11. True or false: computer code is stored as ordinary text that humans can read.**

<details><summary>Show answer</summary>

True — and if you did the lab, you saw it yourself in the Linux repository on GitHub.
Developers write code as text files. Translation (compiling/interpreting) is what turns
that human-readable text into machine-runnable binary.
</details>

**12. 🗣️ Explain it to a friend.** A friend asks: *"My phone says 14 apps need
updating. What even is an app, and why do they update constantly?"* Answer out loud in
under two minutes, using at least one analogy from this module.

<details><summary>Stuck? Here's one way to start</summary>

"An app is a program — a huge list of instructions for your phone, stored as files.
Think of your phone as a piano and each app as sheet music: the hardware never changes,
the instructions do. The people who wrote those instructions keep fixing mistakes,
closing security gaps, and adding features — so every few days they send out corrected
sheet music, and 'updating' means swapping your old copy for the new one…"
</details>

---

*Done? On to [Module 03: How the Internet Works](../03-how-the-internet-works/README.md),
or browse the [extra resources](resources.md).*
