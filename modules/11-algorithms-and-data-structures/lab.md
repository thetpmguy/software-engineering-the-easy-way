# 🔧 Lab 11 — Feel the Algorithms With Your Own Hands

> **Goal:** experience the speed differences from the lesson physically — with paper,
> playing cards, and (optionally) a browser. No installation, no code. Labs 1–3 need
> nothing but this page and something to write on.
>
> **Time:** 30–45 minutes.

---

## 🏁 Lab 1 — The dictionary race (linear vs. binary search)

You'll search the same sorted list two ways and count your steps.

Here is your "phone book" — 32 names, alphabetized and numbered:

| # | Name | # | Name | # | Name | # | Name |
|---|---|---|---|---|---|---|---|
| 1 | Abara | 9 | Elif | 17 | Kwame | 25 | Rosa |
| 2 | Amara | 10 | Emeka | 18 | Lena | 26 | Sana |
| 3 | Bilal | 11 | Farid | 19 | Maya | 27 | Tariq |
| 4 | Carmen | 12 | Grace | 20 | Nadia | 28 | Uma |
| 5 | Chen | 13 | Hana | 21 | Omar | 29 | Vera |
| 6 | Dara | 14 | Ines | 22 | Priya | 30 | Wei |
| 7 | Diego | 15 | Ivan | 23 | Quinn | 31 | Yusuf |
| 8 | Ebba | 16 | Jonas | 24 | Ravi | 32 | Zara |

**Your target: find "Tariq".**

1. **Linear search first.** Start at #1. Read each name aloud, in order, counting as
   you go, until you reach Tariq. Write down your count.
2. **Now binary search.** Look at the *middle* of the current range and halve:
   - Whole list is 1–32. Middle is #16 (Jonas). Tariq comes *after* Jonas
     alphabetically → throw away 1–16. That was **peek 1**.
   - Range is now 17–32. Middle is #24 (Ravi). Tariq comes after Ravi → keep 25–32.
     **Peek 2.**
   - Keep halving. Count every peek until you land on Tariq.
3. Write both counts side by side.

**✅ What you should see:** linear search took 27 steps. Binary search took about 5.
Now imagine the list had a million names: linear could take a million steps; binary
would take at most 20. You've now *felt* O(n) vs. O(log n).

4. **Bonus:** race a family member — one of you searches linearly, the other halves.
   Loser makes the tea.

## 🃏 Lab 2 — Sort 8 cards, two ways, and count

You need 8 playing cards with different values — or 8 paper scraps numbered
**5, 2, 8, 1, 9, 3, 7, 4**. Lay them out in exactly that order for both rounds.

### Round A: bubble sort

1. Compare the first two cards. If the left one is bigger, swap them. That's
   **1 comparison** — keep a tally.
2. Move one position right; compare that pair; swap if needed. Continue to the end of
   the row. (That full sweep is 7 comparisons.)
3. Go back to the start and sweep again. Repeat sweeps until one full sweep needs
   **zero swaps**.
4. Write down your total comparison tally.

**✅ What you should see:** the cards end up 1–9 in order, and your tally is
somewhere around 20–28 comparisons. Notice how big numbers slowly "bubble" to the
right — and how often you re-compared pairs you'd already looked at.

### Round B: merge sort

1. Reset the cards to 5, 2, 8, 1, 9, 3, 7, 4.
2. Split into two piles of 4: (5, 2, 8, 1) and (9, 3, 7, 4).
3. Split each pile into pairs: (5,2) (8,1) (9,3) (7,4). Sort each pair — 1 comparison
   each, so 4 so far.
4. **Merge pairs into sorted 4s:** take (2,5) and (1,8), both face up. Repeatedly move
   the smaller *front* card to a new pile, counting each comparison. Do the same with
   (3,9) and (4,7).
5. **Merge the two sorted 4s** into one sorted 8 the same way — always compare the two
   front cards, move the smaller.
6. Write down the total tally.

**✅ What you should see:** the same sorted row — for roughly 15–17 comparisons,
noticeably fewer than bubble sort. With 8 cards the gap is modest; with 1,000,000
items it's the gap between ~20 million comparisons and ~1,000,000,000,000.

## 🧥 Lab 3 — The human hash table (coat-check game)

This one shows why hash-table lookups feel instant.

**Family version (3+ people):**

1. Lay out 10 paper "hooks" numbered 0–9 in a row on a table.
2. One person is the **attendant**. Their one rule for storing any word: **count its
   letters, keep only the last digit, that's the hook number.** ("UMBRELLA" has 8
   letters → hook 8. "TOOTHBRUSH" has 10 → hook 0.)
3. Players hand the attendant 6 word-cards, one at a time. The attendant applies the
   rule and places each card on its hook. No memorizing allowed!
4. Now players ask: "where is TOOTHBRUSH?" The attendant *recomputes* the rule
   (10 letters → hook 0) and grabs it directly. No searching through hooks.
5. Try to cause trouble: hand over two words with the same rule-result ("CAT" and
   "DOG" — both 3 letters → hook 3). Both cards share hook 3, and the attendant must
   flip through that one hook's small stack. Congratulations: you've caused a
   **collision**, the exact thing real hash tables handle quietly all day.

**Solo paper version:** draw 10 boxes numbered 0–9. "Store" these words using the same
letters-count rule: PEN, WINDOW, BICYCLE, SUN, TEA, ELEPHANT. Then, *without looking
back at your list*, answer: which box holds BICYCLE? Recompute the rule — 7 letters →
box 7 — and check. You found it without scanning any other box.

**✅ What you should see:** finding a word never requires searching — the rule *is*
the address. Also: PEN, SUN and TEA collided in box 3. Real systems use fancier rules
so collisions stay rare, but the idea is exactly this.

## 🖥️ Lab 4 (optional, browser) — Watch the sorts race

If you have a browser handy:

1. Visit **[visualgo.net](https://visualgo.net)** and choose "Sorting".
2. Pick Bubble Sort, press play, and watch the bars swap — recognize your Round A?
3. Now pick Merge Sort on the same data and watch the halving-and-merging.
4. Alternatively, search YouTube for **"15 sorting algorithms in 6 minutes"** — a
   famous visualization where you can *hear* the difference in speed.

**✅ What you should see:** bubble sort visibly plodding while merge sort finishes in
a fraction of the passes. The animations are the lesson's tables, brought to life.

---

## 🎉 Done!

You have now: raced linear against binary search, sorted the same cards with a slow
recipe and a fast one, and run a working hash table using only paper and a counting
rule. That's more hands-on algorithm work than many people do in a first-year
university course. Head to the [quiz](quiz.md) when you're ready.
