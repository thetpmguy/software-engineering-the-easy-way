# 🗄️ Module 12 — Databases: Where Everything Lives

> **What you'll learn:** what a database really is, why every serious app refuses to
> keep its data in a spreadsheet, how tables relate to each other, the polite rigid
> English called SQL, and why engineers break into a sweat before typing DELETE.
>
> **Why it matters:** your bank balance, your medical records, your chat history, your
> loyalty points — every fact about your life that an app "remembers" lives in a
> database right now. Today you find out where, and how it's kept safe.

---

## 🧠 Every app is secretly a careful spreadsheet

Have you ever wondered where your money *is*? Not the paper kind — the number you see
when you open your banking app. Here is the slightly dizzying truth: **your bank
balance is a row.** One row, in one table, in a database, on computers your bank runs.
When you get paid, nobody moves anything anywhere. A number in that row changes.

The same goes for everything else. Your Instagram account is a row. Each of your
photos is a row that *points to* your row. Your last online order, your airline seat,
your library loans: rows, rows, rows.

So what is this thing holding the rows? A **database** is an organized collection of
data, plus the software that guards it, organizes it, and answers questions about it.
The data and its guardian come as a package — and the guardian is the interesting part.

> 🌉 **Analogy:** Picture a filing cabinet with a meticulous librarian standing in
> front of it. The librarian never sleeps, never loses a paper, remembers where every
> record is, and can fetch any one of them in milliseconds. You never open the drawers
> yourself — you ask the librarian, and the librarian enforces the rules.
>
> **Where the analogy breaks down:** a human librarian serves one person at a time.
> This librarian calmly serves *thousands of people in the same second*, without
> mixing up their requests — and that superpower is precisely why databases exist.

## 📁 Why not a spreadsheet or a folder of files?

A fair question. You've used spreadsheets; they hold rows and columns too. Why do
companies bother with databases? Three reasons, and each one is a disaster story.

**Disaster 1: the crowd.** Imagine 10,000 people editing one Excel file at the same
moment. Two people type into the same cell; whose edit wins? Someone sorts the sheet
while someone else is halfway through reading it. A shared file simply has no referee.
A database *is* the referee: the librarian takes every request in turn, keeps them
from trampling each other, and gives each person a consistent view.

**Disaster 2: the rules.** A spreadsheet will happily accept a birth date of
"banana", a negative order quantity, or two customers with the same customer number.
A database can be told the rules of your business — "this column must be a date",
"this number is never negative", "no duplicates here" — and the librarian *refuses*
to file anything that breaks them. Bad data gets bounced at the door.

**Disaster 3: the half-save.** This one matters most, so it gets its own section.

## 💸 Transactions: the all-or-nothing promise

Suppose you send your friend $100. Two things must happen: subtract $100 from your
row, and add $100 to theirs. Now imagine the power fails *between* those two steps.
Your money is gone, and your friend never got it. The bank has vaporized $100 — or,
if the steps ran in the other order, invented $100.

Databases solve this with a **transaction**: a group of changes that must all happen
together, or not happen at all. There is no in-between state — no half-save, ever.

> 🌉 **Analogy:** Moving money with two hands. One hand takes the bill from your
> envelope while the other places it in your friend's — one motion. If anything jolts
> the table mid-move, the bill goes back where it started. Nobody can ever peek and
> see a moment where the money is in neither envelope, or both.
>
> **Where the analogy breaks down:** hands fumble. A database transaction genuinely
> cannot end half-done — if the power dies mid-transaction, the database wakes up,
> checks its diary, and rolls the incomplete change back as if it never began.

You may hear engineers say a database is "ACID". Don't memorize the letters — it's
shorthand for exactly this family of **all-or-nothing promises**. When someone says
"is that operation transactional?", they're asking "could this half-save on us?"

> ✅ **Check yourself**
> 1. Why is a shared spreadsheet a bad home for 10,000 users' data?
> 2. In the money transfer, what exactly does a transaction promise?
>
> <details><summary>Show answers</summary>
>
> 1. No referee: simultaneous edits collide, nothing enforces the rules about what
>    valid data looks like, and a crash mid-edit can leave the file half-saved or
>    corrupted.
> 2. That the subtract and the add happen together or not at all. There is never a
>    moment — even during a crash — where money has left one account and not arrived
>    in the other.
> </details>

## 🔗 Relational databases: tables that know each other

The most common kind of database is the **relational database** — one that stores data
in tables (rows and columns) *and* records how those tables relate to each other.
The "relational" part is the genius bit. Watch.

A small bakery's database might have two tables:

**customers**

| customer_id | name | city |
|---|---|---|
| 1 | Amara Obi | Lagos |
| 2 | Chen Wei | Singapore |
| 3 | Rosa Diaz | Bogotá |

**orders**

| order_id | customer_id | item | price |
|---|---|---|---|
| 101 | 1 | Sourdough loaf | 6.50 |
| 102 | 3 | Croissant ×4 | 8.00 |
| 103 | 1 | Birthday cake | 42.00 |

Notice what the orders table does *not* contain: Amara's name, city, or address. It
carries only her `customer_id` — the number 1. Why? Because if Amara moves house,
there must be exactly **one** place to fix it. If her address were copied onto every
order, you'd have to hunt down every copy, and the day you miss one, her cake ships
to the old apartment. Store each fact once; point to it everywhere else. This single
principle drives most database design.

That id column deserves its name: a **primary key** is a column whose value uniquely
identifies each row — no two rows may share it, ever.

> 🌉 **Analogy:** A primary key is a passport number. Two people can both be named
> "Chen Wei"; no two people share a passport number. When another table needs to
> refer to a customer, it writes down the passport number, not the name.
>
> **Where the analogy breaks down:** passport numbers come from a government office.
> Primary keys are usually assigned by the database itself, counting up quietly:
> 1, 2, 3...

When the bakery asks "show me each order *with* the customer's name", the librarian
matches the numbers across tables and stitches the rows together on the fly.
Engineers call that stitching a **join** — and it's the everyday magic of relational
databases.

## 🗣️ SQL: a polite, rigid English for the librarian

How do you actually ask the librarian for something? Nearly every relational database
speaks the same language. **SQL** (pronounced "sequel" or "ess-cue-ell") is a small,
formal language for telling a database what data you want or how to change it. It
reads almost like stiff English. Four tiny examples — read the plain translation
first, then the query:

**"Librarian, give me the names of customers who live in Lagos."**

```sql
SELECT name FROM customers WHERE city = 'Lagos';
```

Word by word: `SELECT name` — I want the name column. `FROM customers` — out of the
customers table. `WHERE city = 'Lagos'` — but only rows whose city is Lagos. The
answer here: Amara Obi.

**"Librarian, file a new customer."**

```sql
INSERT INTO customers (name, city) VALUES ('Kwame Mensah', 'Accra');
```

`INSERT INTO customers` — add a row to that table. The rest lists which columns get
which values. The librarian assigns the new primary key itself.

**"Librarian, correct a record."**

```sql
UPDATE customers SET city = 'Abuja' WHERE customer_id = 1;
```

`UPDATE customers` — change rows in this table. `SET city = 'Abuja'` — the change.
`WHERE customer_id = 1` — and *only* for Amara's row. That WHERE part matters more
than anything else in this lesson, because...

**"Librarian, shred a record." (the dangerous one)**

```sql
DELETE FROM customers WHERE customer_id = 2;
```

This removes Chen Wei's row. Forever. And here is why engineers sweat: if you forget
the `WHERE` clause and type only `DELETE FROM customers;` — the librarian obediently
shreds **every customer in the table**. No confirmation dialog, no undo. It did
exactly what you said. Every experienced engineer has a story about this (their own,
or the near-miss that trained them). It's why real teams protect production databases
with permissions, backups, and code review.

> ⚠️ **Watch out:** SQL is rigid. `WHERE city = 'Lagos'` finds Lagos; `where City =
> Lagos` (wrong quotes, wrong capitalization of the value) may find nothing or refuse
> to run. The librarian is meticulous, not imaginative — Module 01's "extremely
> literal" machine, wearing reading glasses.

> ✅ **Check yourself**
> 1. Why store Amara's address once in `customers` instead of on every order?
> 2. What does the WHERE clause do — and what happens to a DELETE without one?
>
> <details><summary>Show answers</summary>
>
> 1. So there is exactly one place to fix mistakes or make updates. Copies drift out
>    of sync; a single source of truth can't contradict itself.
> 2. WHERE filters which rows a command touches. A DELETE without a WHERE touches
>    *all* rows — it empties the whole table, permanently.
> </details>

## 📑 Indexes: the index at the back of the book

If a table holds 50 million customers, must the librarian read all 50 million rows to
find the ones in Lagos? Without help — yes. That's the linear search from Module 11.

The fix is an **index**: a separate, sorted lookup structure the database maintains so
it can find rows without scanning the whole table — exactly like the index at the back
of a textbook. Want "photosynthesis"? You don't read all 900 pages; you check the
sorted index and jump straight to page 412. Database indexes are typically built as
the balanced trees from Module 11, so lookups take a handful of steps even across
millions of rows.

The trade-off (there is always one): the index takes extra storage space, and every
time a row is added or changed, the librarian must also update the index. Fast reads,
slightly slower writes, more shelf space. Engineers add indexes to the columns people
search by — and not to the rest.

## 📦 NoSQL: labeled boxes instead of strict tables

Not everything fits neatly into rows and columns. What if every product in your shop
has *different* attributes — books have authors, t-shirts have sizes, cheeses have
ages? Forcing them into one rigid table gets awkward.

A **NoSQL database** is any database that organizes data some other way than strict
relational tables — most commonly as flexible labeled documents (often in the JSON
format you met in Module 10, if you took the API detour). Each record is a labeled
box that holds whatever that record needs.

> 🌉 **Analogy:** A filing cabinet vs. a flexible closet. The cabinet (relational)
> insists every paper fits a pre-printed form — rigid, but wonderfully consistent and
> queryable. The closet (NoSQL) has labeled boxes that can each hold different
> things — flexible, but nobody guarantees every box even *has* a "price" slip inside.
>
> **Where the analogy breaks down:** real closets get messy with no consequences.
> A messy database quietly breaks the apps built on top of it — flexibility is a
> loan you repay with discipline.

Names you'll hear: **MongoDB** (a popular document database) and **Redis** (a
lightning-fast key-value store — essentially the hash table from Module 11, all grown
up). Neither is "better" than relational; they're different containers for different
jobs, and big companies typically run both.

## 💾 Backups: the museum keeps copies

Even a perfect librarian can't survive a flood, a fire, or a typo'd DELETE. So real
teams keep **backups** — regular copies of the entire database, stored elsewhere,
from which everything can be restored.

> 🌉 **Analogy:** A serious museum photographs and documents every painting, and
> stores the records in a different building. Losing the gallery is a tragedy;
> losing the gallery *and* every record of what was in it is oblivion.
>
> **Where the analogy breaks down:** a photo of a painting isn't the painting. A
> database restored from last night's backup really is the data — minus whatever
> changed since last night, which is why backup *frequency* matters.

You may hear the **3-2-1 rule**: keep 3 copies of your data, on 2 different kinds of
storage, with 1 copy far away from the others. One line, decades of hard-won wisdom —
and it applies to your family photos too.

## 🧑‍💼 Who actually touches databases?

Practically everyone in tech, it turns out. Backend engineers (Module 10) read and
write them constantly — most API calls end in a database query. Operations engineers
keep them healthy and backed up. And an entire profession — **data analysts** —
spends all day asking databases questions with SQL: "which product sold best in
March?", "where do customers give up mid-purchase?" If SQL intrigued you today, keep
that feeling; it resurfaces as a career door in
[Module 18](../18-who-does-what-in-tech/README.md).

> ✅ **Check yourself**
> 1. What does a database index speed up, and what does it cost?
> 2. When might a team pick a document (NoSQL) database over a relational one?
>
> <details><summary>Show answers</summary>
>
> 1. It speeds up finding rows by the indexed column — a jump-to-the-page lookup
>    instead of scanning every row. It costs extra storage and a little extra work
>    on every write, since the index must be kept up to date.
> 2. When records naturally vary in shape (every product having different
>    attributes), or when flexibility matters more than strict cross-table rules.
> </details>

## 🎁 Recap

- A **database** = organized data + a tireless librarian who guards it, and your bank
  balance is literally a row in one.
- Files and spreadsheets fail at crowds, rules, and half-saves; databases handle
  thousands of simultaneous users and enforce your business rules at the door.
- A **transaction** is an all-or-nothing group of changes — money transfers subtract
  AND add, or do neither. "ACID" is shorthand for these promises.
- **Relational databases** store facts once and connect tables by **primary keys**
  (passport numbers for rows); stitching tables together is a **join**.
- **SQL** is the polite, rigid English for the librarian: SELECT asks, INSERT files,
  UPDATE corrects, DELETE shreds — and a DELETE without WHERE shreds *everything*.
- An **index** is the back-of-the-book lookup: fast reads, at the cost of space and
  upkeep.
- **NoSQL** databases (MongoDB, Redis) trade the filing cabinet's rigor for a
  flexible closet of labeled boxes.
- **Backups**, ideally 3-2-1 style, are the museum's records in another building.

## ➡️ Where next?

You now know where data lives. But underneath the database, the librarian is itself a
program — running on an operating system, talking over a network, sharing a machine
with hundreds of other programs. Who keeps *that* circus in order? Two invisible
managers you've been living with your whole digital life. Let's meet them properly.

**Next up:** [Module 13 — Operating Systems & Networks: The Invisible Managers](../13-operating-systems-and-networks/README.md)
