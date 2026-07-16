# ✅ Quiz 11 — Algorithms & Data Structures

Answer in your head or on paper, then open each fold to check. No scores, no
judgment — wrong answers here are how the right ones stick.

---

**1. A friend says: "If an app is slow, the company should buy faster servers."
Based on this module, what's the more powerful fix — and why?**

<details><summary>Show answer</summary>

Choosing a better algorithm (recipe). Faster hardware might make a bad recipe 2×
quicker, but a better recipe — say, replacing an O(n²) approach with an O(log n) one —
can make it thousands or millions of times quicker on big piles of data.
</details>

**2. Why does binary search need the data to be sorted before it can work?**

<details><summary>Show answer</summary>

Binary search works by peeking at the middle and concluding "my target must be in
this half." That conclusion is only valid if items are in order. In a shuffled pile,
the middle item tells you nothing about where anything else is, so you can't throw
away half.
</details>

**3. A sorted phone book has 1,000,000 names. Roughly how many peeks does binary
search need in the worst case? And if the book doubles to 2,000,000?**

<details><summary>Show answer</summary>

About 20 peeks for a million names — each peek halves the remaining pile. Doubling
to two million adds only *one* more peek (about 21). That "doubling costs one step"
behavior is exactly what O(log n) means.
</details>

**4. Match each Big-O label to its everyday picture: O(1), O(log n), O(n), O(n²).
Pictures: reading every page of a book; grabbing keys from a hook; everyone in a
room shaking everyone's hand; finding a word in a dictionary by halving.**

<details><summary>Show answer</summary>

- O(1) → grabbing keys from a hook (effort never changes)
- O(log n) → dictionary halving (doubling the pile adds one step)
- O(n) → reading every page (doubling the pile doubles the effort)
- O(n²) → the handshake room (doubling the people *quadruples* the handshakes)
</details>

**5. Why do apps bother sorting data at all, when sorting itself takes effort?**

<details><summary>Show answer</summary>

Sorting is an upfront investment that unlocks binary search — near-instant lookups —
on every future search. Pay the sorting cost once; collect fast searches forever
after. That's why contacts are alphabetized and emails are time-ordered.
</details>

**6. In one or two sentences each, how does bubble sort work, and how does merge
sort work?**

<details><summary>Show answer</summary>

Bubble sort repeatedly walks the row comparing neighbors and swapping any pair in the
wrong order, sweeping again and again until a full sweep needs no swaps. Merge sort
splits the pile in half, sorts each half (by splitting again, down to single items),
then merges the sorted halves like combining two sorted card decks — always taking
the smaller front card.
</details>

**7. Your team is building an Undo button and a customer-support ticket line. Which
container fits each, and what's the one-line reason?**

<details><summary>Show answer</summary>

Undo → a **stack**: the most recent change must come off first (last in, first out,
like plates). Ticket line → a **queue**: tickets must be handled in arrival order
(first in, first out, like a bakery line).
</details>

**8. Why is looking something up in a hash table near-instant, even with a billion
entries?**

<details><summary>Show answer</summary>

Because the key works like a coat-check ticket: a rule turns it directly into a
storage location. There's no scanning through other entries, so the size of the pile
barely matters — it's O(1). (Occasionally two keys land on the same spot — a
collision — and there's a tiny bit of extra work.)
</details>

**9. What's the difference between a tree and a graph, and give one real app
feature powered by each.**

<details><summary>Show answer</summary>

A tree is a strict hierarchy — one top item, branches that never reconnect (like
folders inside folders). A graph is a free-form web where anything can connect to
anything (like friendships in a city). Trees power your file system and database
indexes; graphs power social networks' "people you may know" and map navigation.
</details>

**10. What is recursion, in plain words? Name the sorting recipe from this module
that uses it.**

<details><summary>Show answer</summary>

Recursion is a recipe that solves a problem by applying *itself* to smaller pieces
of the same problem — like opening Russian nesting dolls, or counting files in a
folder by doing the same in every subfolder. It works because the pieces keep
shrinking until nothing is left to do. Merge sort is recursive: "sort a shelf"
means "sort each half-shelf" until each shelf is one book.
</details>

**11. True or false: professional engineers keep sorting algorithms memorized and
write them from scratch regularly.**

<details><summary>Show answer</summary>

False. The recipes live in well-tested libraries that everyone reuses. What
professionals actually carry is judgment: knowing which *container* fits which job
(hash table for instant lookups, queue for order, tree for hierarchy) and how effort
grows as data grows.
</details>

**12. 🗣️ Explain it to a friend.** Someone asks: "Why can Google search the whole
internet in half a second, but my spreadsheet freezes when I sort 10,000 rows?"
Explain it out loud in under a minute, using at least one analogy from this module —
the dictionary, the handshake room, or the coat check.

<details><summary>One possible answer</summary>

"It's not about computer power — it's about the recipe. Google prepares its data in
advance, sorted and indexed, so finding something works like finding a word in a
dictionary: open the middle, throw away half, repeat. Even with billions of pages
that takes a few dozen peeks. Your spreadsheet is probably following a
clumsier recipe — more like everyone in a room shaking hands with everyone else,
where doubling the rows quadruples the work. Same computer, different recipe,
wildly different speed."
</details>
