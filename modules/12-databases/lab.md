# 🔧 Lab 12 — Talk to a Real Database (No Installation)

> **Goal:** write real SQL in your browser, then practice on paper with a pretend
> bakery, then design the tables behind your favorite app.
>
> **Time:** 45–60 minutes. Part B works completely offline.

---

## 🖥️ Part A — Browser SQL with SQLBolt (recommended)

1. Open **[sqlbolt.com](https://sqlbolt.com)** in any browser — phone or laptop. It's
   free, needs no sign-up, and runs a real (tiny) database right on the page.
2. Work through **Lessons 1 through 6**. Each lesson explains one idea, then gives
   you a table of movie data and asks you to write queries against it.
3. Type each query into the box and press Enter. When your result matches the task,
   the row turns green.

**✅ What you should see:** by Lesson 3 you're writing `SELECT` with `WHERE` clauses
like the ones from the lesson, and green checkmarks are piling up. If a query errors,
read it letter by letter — a missing quote or a stray comma is the usual culprit. The
librarian is meticulous, remember.

> ⚠️ **Watch out:** don't rush to finish all of SQLBolt. Lessons 1–6 cover
> everything this module taught. The later lessons are there when you want them.

## 📝 Part B — Paper SQL at the bakery (works offline)

No internet? No problem. Here is your database, on paper. Read the two tables
carefully — every exercise below uses them.

**customers**

| customer_id | name | city |
|---|---|---|
| 1 | Amara Obi | Lagos |
| 2 | Chen Wei | Singapore |
| 3 | Rosa Diaz | Bogotá |
| 4 | Kwame Mensah | Accra |
| 5 | Lena Novak | Lagos |

**orders**

| order_id | customer_id | item | price |
|---|---|---|---|
| 101 | 1 | Sourdough loaf | 6.50 |
| 102 | 3 | Croissant ×4 | 8.00 |
| 103 | 1 | Birthday cake | 42.00 |
| 104 | 5 | Rye loaf | 7.00 |
| 105 | 2 | Croissant ×4 | 8.00 |
| 106 | 5 | Sourdough loaf | 6.50 |

Write each query on paper (or in any notes app). Then check the fold. Spelling of
keywords matters less than getting the *shape* right.

**Exercise 1.** Ask for the names of all customers.

<details><summary>Show answer</summary>

```sql
SELECT name FROM customers;
```

Result: all five names.
</details>

**Exercise 2.** Ask for the names of customers who live in Lagos.

<details><summary>Show answer</summary>

```sql
SELECT name FROM customers WHERE city = 'Lagos';
```

Result: Amara Obi and Lena Novak.
</details>

**Exercise 3.** Ask for every order that cost more than 7.00. (Comparison symbols
work in WHERE: `>` means "greater than".)

<details><summary>Show answer</summary>

```sql
SELECT * FROM orders WHERE price > 7.00;
```

`*` means "all columns". Result: orders 102, 103, and 105.
</details>

**Exercise 4.** *Read* the tables like the librarian would: which customer placed
order 104? (No query to write — follow the key with your finger.)

<details><summary>Show answer</summary>

Order 104 has customer_id 5. Row 5 in customers is Lena Novak. You performed a join
by hand — matching a key across two tables.
</details>

**Exercise 5.** A new customer signs up: Ines Costa, from Porto. File her.

<details><summary>Show answer</summary>

```sql
INSERT INTO customers (name, city) VALUES ('Ines Costa', 'Porto');
```

The database assigns her customer_id 6 automatically.
</details>

**Exercise 6.** Amara Obi moves from Lagos to Abuja. Correct her record — and hers
only.

<details><summary>Show answer</summary>

```sql
UPDATE customers SET city = 'Abuja' WHERE customer_id = 1;
```

The WHERE is essential. Without it, all six customers would "move" to Abuja.
</details>

**Exercise 7.** Order 105 was cancelled. Remove it — carefully.

<details><summary>Show answer</summary>

```sql
DELETE FROM orders WHERE order_id = 105;
```

Before running any DELETE, engineers often run the same WHERE as a SELECT first —
`SELECT * FROM orders WHERE order_id = 105;` — to see exactly which rows are about
to disappear. Steal that habit.
</details>

**Exercise 8.** The danger drill. What would this do: `DELETE FROM orders;` — and
which one word makes it catastrophic by its *absence*?

<details><summary>Show answer</summary>

It deletes every row in the orders table — all six orders, gone, no undo. The
missing word is WHERE. This is the query that makes engineers sweat, and why
production databases have backups and strict permissions.
</details>

**✅ What you should see:** your queries match the folds in shape — SELECT/FROM/WHERE
in that order, quotes around text values, and a healthy new respect for WHERE.

## ✏️ Part C — Design the tables behind your favorite app

In Module 06's lab you listed the *data* your favorite app remembers. Time to level
up: now design its **tables and relationships**.

1. Pick the app (WhatsApp, Spotify, a food-delivery app — anything).
2. On paper, draw 2–3 tables as boxes. Give each a name and 3–5 columns. Every table
   gets a primary key column (its passport number).
3. Draw **lines between the boxes** where one table refers to another, and label the
   line with the key that connects them. For a food app: `orders.customer_id → customers.customer_id`,
   and `orders.restaurant_id → restaurants.restaurant_id`.
4. Test your design with the one-place-to-fix rule: if a customer changes their
   delivery address, how many places in your design need editing? If the answer is
   more than one, move that fact into its own single home.

**✅ What you should see:** a sketch where every fact lives in exactly one table, and
arrows carry ID numbers — not copied names or addresses — between tables. Keep the
sketch; it makes you dangerous (in a good way) in any meeting about "the data model".

---

## 🎉 Done!

You've queried a real database in the browser, run the librarian's four big commands
on paper, survived the danger drill, and designed a relational schema for an app you
use every day. On to the [quiz](quiz.md).
