# ✅ Quiz 12 — Databases

Think first, then open the fold. Getting one wrong and re-reading the section is the
whole point.

---

**1. In plain words: what is a database, and what are its two ingredients?**

<details><summary>Show answer</summary>

An organized collection of data, plus the guardian software that stores it, protects
it, enforces the rules, and answers questions about it — the filing cabinet *and*
the meticulous librarian, sold as a package.
</details>

**2. Give two reasons a shared spreadsheet fails as the data home for an app with
10,000 users.**

<details><summary>Show answer</summary>

Any two of: (1) no referee for simultaneous edits — users trample each other's
changes; (2) no rule enforcement — nothing stops "banana" in a date column or
duplicate customer numbers; (3) no protection against half-saves — a crash mid-edit
can corrupt or lose data with no all-or-nothing guarantee.
</details>

**3. A money transfer subtracts $100 from one account and adds $100 to another.
What does wrapping those two steps in a transaction guarantee?**

<details><summary>Show answer</summary>

That both steps happen or neither does — all-or-nothing. Even if the power dies
between them, the database rolls the half-done work back, so money can never vanish
from one account without arriving in the other. (The famous "ACID" letters are
shorthand for this family of promises.)
</details>

**4. Why does the orders table store `customer_id = 1` instead of copying Amara's
name and address onto every order?**

<details><summary>Show answer</summary>

So each fact lives in exactly one place. If Amara moves, one row in `customers` gets
updated and every order automatically "knows", because orders only point to her by
ID. Copies drift out of sync — the day you miss one, the cake ships to the old
address.
</details>

**5. What is a primary key? What everyday document did the lesson compare it to?**

<details><summary>Show answer</summary>

A column whose value uniquely identifies each row — no two rows may share it. The
lesson compared it to a passport number: two people can share a name, never a
passport number.
</details>

**6. Translate this query into plain English:
`SELECT name FROM customers WHERE city = 'Lagos';`**

<details><summary>Show answer</summary>

"Librarian, from the customers table, give me the name of every customer whose city
is Lagos." SELECT = which column I want; FROM = which table; WHERE = which rows
qualify.
</details>

**7. Why do engineers get nervous around DELETE — and what one missing word turns
it from routine into catastrophe?**

<details><summary>Show answer</summary>

DELETE removes rows permanently, with no confirmation and no undo. Without a WHERE
clause, `DELETE FROM customers;` removes *every* row in the table. The missing word
is WHERE. That's why teams rely on backups, permissions, and the habit of running
the WHERE as a SELECT first.
</details>

**8. What is a database index, what does it speed up, and what two costs does it
add?**

<details><summary>Show answer</summary>

A separate, sorted lookup structure — like the index at the back of a book — that
lets the database jump to matching rows instead of scanning the whole table. It
speeds up reads on the indexed column. Costs: extra storage space, and extra upkeep
on every insert or update, which slows writes slightly.
</details>

**9. Filing cabinet vs. flexible closet: what's the core difference between
relational and NoSQL databases, and name one example of a NoSQL product.**

<details><summary>Show answer</summary>

Relational databases require every record to fit strict pre-defined tables (the
pre-printed forms in the cabinet) — rigid but consistent and great for
cross-referencing. NoSQL databases store flexible labeled documents or key-value
pairs (boxes in a closet) — each record can have its own shape, at the price of
fewer guarantees. Examples: MongoDB (documents) or Redis (key-value).
</details>

**10. Your friend keeps all family photos on one laptop. Apply the 3-2-1 idea to
their situation.**

<details><summary>Show answer</summary>

Keep 3 copies (laptop + external drive + cloud), on 2 different kinds of storage
(the drive and the cloud count), with 1 copy far away (the cloud, or a drive at a
relative's house). One flood or one theft should never be able to reach all copies.
</details>

**11. Name two different jobs whose daily work involves querying databases.**

<details><summary>Show answer</summary>

Backend engineers (most API calls end in a database query) and data analysts (who
spend all day asking business questions in SQL). Also acceptable: operations/
database administrators who keep the librarian healthy and backed up.
</details>

**12. 🗣️ Explain it to a friend.** Your cousin asks: "Why do banks need
'databases'? Couldn't they keep everyone's balance in a big Excel file?" Answer out
loud in under a minute. Bonus points for using the librarian, the two-hands money
move, or the passport number.

<details><summary>One possible answer</summary>

"Imagine millions of people editing one Excel file at the same second — edits would
collide and money would vanish. A database is that spreadsheet with a tireless
librarian in front of it: it serves thousands of requests at once without mixing
them up, refuses invalid data at the door, and makes transfers all-or-nothing — the
subtract and the add happen together like moving cash with two hands, so a crash
can never leave your money in limbo. Plus every account has a unique ID, like a
passport number, so records connect without confusion. Excel has none of that."
</details>
