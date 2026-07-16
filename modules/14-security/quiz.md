# ✅ Quiz 14 — Security

Answer before you peek. If one stumps you, that section is worth a re-read — this
is the module your real accounts depend on.

---

**1. "Nobody would bother hacking me." What's wrong with this sentence, based on
how attackers actually operate?**

<details><summary>Show answer</summary>

It assumes attackers pick targets. Most don't — they're burglars trying every door
handle by machine, millions per hour, and they take whichever doors open: reused
passwords, unpatched devices, no 2FA. You don't need to be interesting to be
robbed; you only need to be unlocked.
</details>

**2. Authentication vs. authorization — define both with the hotel analogy, and
say which one a fingerprint reader performs.**

<details><summary>Show answer</summary>

Authentication is the front desk checking ID — proving who you are (something you
know, have, or are). Authorization is what your keycard opens once you're in —
your room and the pool, not the manager's office. A fingerprint reader performs
authentication ("something you are").
</details>

**3. Why does `purple tortoise umbrella daylight` beat `P@ssw0rd1`, when the
second one looks more "secure"?**

<details><summary>Show answer</summary>

Cracking machines try billions of guesses per second, starting with dictionary
words and the classic substitutions — @-for-a is page one of their playbook, so
the short "clever" password falls in minutes. Every added character multiplies
the guessing work by dozens of times, so a long boring passphrase pushes the job
past the age of the universe. Length beats cleverness.
</details>

**4. What is credential stuffing, and which everyday habit makes it devastating?**

<details><summary>Show answer</summary>

Taking email+password pairs leaked from one breached site and trying them,
by machine, on thousands of other sites. Password *reuse* makes it devastating:
one leaked key opens all your doors, so your security equals that of the
sloppiest site you ever joined.
</details>

**5. Why do app-based 2FA codes beat SMS codes — and why is SMS 2FA still far
better than nothing?**

<details><summary>Show answer</summary>

Phone numbers can be hijacked by sweet-talking the phone company into moving your
number to an attacker's SIM; an authenticator app's codes live only on your
physical device. But either way, a password thief still needs a second factor
they don't have — so SMS 2FA still blocks the vast majority of break-ins.
</details>

**6. Explain the padlock-mailbox trick: what can anyone do, what can only you do,
and which everyday browser feature works this way?**

<details><summary>Show answer</summary>

Anyone can take one of your open padlocks and snap it shut on a box — locking a
message so that even the sender can't reopen it. Only you hold the key that opens
those padlocks. That's public-key encryption, and it's how HTTPS (the browser's
padlock icon) starts every secure connection: your browser locks a fresh shared
key with the site's public padlock, and then both sides switch to the fast
shared-key lockbox.
</details>

**7. WhatsApp says your chats are "end-to-end encrypted." What specifically does
that claim mean about who can read them?**

<details><summary>Show answer</summary>

Only the sender's and receiver's devices hold the keys. The message is locked
before it leaves your phone, and the company in the middle relays a sealed box it
cannot open — so not even WhatsApp can read the contents.
</details>

**8. A website emails you your actual password when you click "forgot password."
What did they reveal, and why is it a leave-now red flag?**

<details><summary>Show answer</summary>

Honest sites store only a hash — a fingerprint of your password that can't be
reversed back into it — and could only send a *reset* link. Emailing the real
thing proves they stored it un-hashed, so a breach there leaks actual passwords —
including yours, on every site where you reused it.
</details>

**9. Name the three tells of a phishing message, and the single habit that
defeats most phishing entirely.**

<details><summary>Show answer</summary>

Urgency ("act within 24 hours or lose your account"), links whose real address
(hover or long-press to see it) doesn't match the claimed one, and sender
addresses that are almost-but-not-quite right. The habit: never log in via a link
that came to you — open the site yourself and log in there.
</details>

**10. What does ransomware do, in the burglar language of this module — and which
Module 12 practice turns it from catastrophe into nuisance?**

<details><summary>Show answer</summary>

It's the burglar who gets inside, changes your locks — encrypts your own files —
and sells you the key. Backups (the museum's copies, 3-2-1 style) defang it: you
restore your files and decline the sale.
</details>

**11. Why is postponing updates riskier than most people think? Use the word
"patch" in your answer.**

<details><summary>Show answer</summary>

Updates deliver patches — fixes for security holes — and the act of publishing a
patch announces the hole's existence to attackers, who immediately scan for
devices not yet fixed. An unpatched device is a door whose broken lock has been
publicly documented. "Remind me later" leaves it broken after the burglars got
the memo.
</details>

**12. 🗣️ Explain it to a friend.** A relative says: "I use one really good
password for everything — it has symbols and numbers, so I'm safe." In under a
minute, gently explain the two problems and the two fixes. Analogies encouraged.

<details><summary>One possible answer</summary>

"Two things, and neither is your fault for not knowing. First, symbols don't help
much — cracking machines try billions of guesses a second and check all the
usual swaps first; what actually defeats them is *length*, like four random words.
Second — and this is the big one — using one password everywhere means one key
opens your whole life. When any site you've ever joined gets breached, and one
eventually will, thieves take the leaked passwords and try them on everyone's
email and bank automatically. So: a password manager remembers a different long
key for every door, you memorize only the master one — and turn on two-factor for
your email, so even a stolen key isn't enough on its own. One afternoon, and
you're safer than almost everyone they're robbing."
</details>
