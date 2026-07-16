# ✅ Quiz 06 — Data: The World's New Oil

Think first, then open the fold. Getting one wrong means you found the exact paragraph worth rereading — a win, not a loss.

---

**1. Complete the sentence from the lesson: "Almost every app is a fancy wrapper around ______." Give one example.**

<details><summary>Show answer</summary>

…around **data** (stored facts). Examples: Instagram is essentially a photos table plus a likes table; WhatsApp is essentially a messages table; a bank is, at heart, a very careful spreadsheet of money moving between accounts.
</details>

---

**2. What is data, in one plain sentence? And what makes data "digital"?**

<details><summary>Show answer</summary>

Data is recorded facts. Digital data is facts written down as numbers so a computer can store them — and everything digital (text, photos, songs) is numbers underneath.
</details>

---

**3. A filled-in tax form versus a shoebox of receipts: which is structured data, which is unstructured — and why does the difference matter to a computer?**

<details><summary>Show answer</summary>

The tax form is structured: every form has the same labeled slots, so a machine can process a million of them without "reading." The shoebox is unstructured: the same facts, but in no fixed layout, so a computer historically couldn't do much with it. Structure is what makes data searchable, summable, and powerful.
</details>

---

**4. Match the container to the job: (a) the queue of songs to play next, (b) "given a username, fetch that person's profile," (c) all customers with a name, email, and signup date each.**

<details><summary>Show answer</summary>

(a) List — order matters, duplicates allowed, like a shopping list. (b) Dictionary — instant lookup by key, like jumping straight to a name in your contacts. (c) Table — many items of the same kind, one row each, one column per fact, like a spreadsheet.
</details>

---

**5. In a table, what does a row represent, and what does a column represent? Use WhatsApp messages as your example.**

<details><summary>Show answer</summary>

A row is one *thing* (one message). A column is one *fact recorded about every thing* (sender, recipient, text, time sent, read-yet). A million messages = a million rows, all with the same columns.
</details>

---

**6. Here is a complete file. What format is it, and what would you see if you opened it in a spreadsheet program?**

```
name,city,age
Amara,Lagos,34
Ben,Toronto,61
```

<details><summary>Show answer</summary>

It's a CSV (comma-separated values): plain text where the first line is column headings and each later line is a row, columns split by commas. A spreadsheet program would show it as a tidy table — two rows of data under three column headings. Same information, two outfits.
</details>

---

**7. Read this JSON out loud in plain English. What is the value under the key `"pets"`, and what kind of container is it?**

```json
{ "name": "Ben", "city": "Toronto", "pets": ["dog", "dog", "goldfish"] }
```

<details><summary>Show answer</summary>

"Name is Ben; city is Toronto; pets is a list containing dog, dog, and goldfish." The value under `"pets"` is a **list** — ordered, and duplicates allowed (Ben has two dogs). JSON is nested labeled boxes: dictionaries and lists written down, which is why apps use it to send structured data to each other.
</details>

---

**8. A game keeps your current score, your saved games, and (for its worldwide leaderboard) millions of players' best scores. Match each to memory, a file, or a database — and say why.**

<details><summary>Show answer</summary>

Current score → **memory**: fast, changes constantly, fine to lose if the app closes mid-game. Saved games → a **file**: must survive shutdown, small, one user. Worldwide leaderboard → a **database**: huge, structured, read and written by millions at once — the filing cabinet with the librarian who never sleeps.
</details>

---

**9. What is metadata? Name two pieces of metadata your phone attaches to every photo without asking — and the one with the biggest privacy implication.**

<details><summary>Show answer</summary>

Metadata is data *about* data — the label on the box, not the contents. A photo carries the date and time, the device model, camera settings, and often GPS location. The biggest privacy item is **location**: a shared photo can reveal exactly where you stood — potentially where you live — without a word of caption.
</details>

---

**10. "If the app is free, you're paying with something else." Explain what, and name two ways companies turn it into money.**

<details><summary>Show answer</summary>

You pay with your data — recorded facts about what you do, like, watch, and where you are. Companies turn it into money by (1) improving the product with it (better recommendations keep you using it) and (2) selling better-targeted advertising — an ad shown to "people who searched for strollers this week" is worth far more than an ad shown to everyone. There's a third effect too: data compounds — more users make more data, which makes a better product, which attracts more users.
</details>

---

**11. Where does the "data is the new oil" comparison break down?**

<details><summary>Show answer</summary>

Oil is used up when burned; data isn't used up when used. It copies perfectly and endlessly, can be used by many people at once, and keeps generating value — recommendations, targeting, training AI — for years. (Any one of these differences is a good answer.)
</details>

---

**12. 🗣️ Explain it to a friend**

A friend says: *"I don't get why everyone's paranoid — it's a photo app, it's free, what could they possibly want from me?"* In three or four sentences, explain — using the words **data**, **table**, and **metadata** — what the app actually stores and why it's valuable.

<details><summary>Show one possible answer</summary>

"Under the pretty screens, that app is mostly big tables of data — one row for every photo, every like, every follow, with columns saying who, what, and when. Each photo also carries metadata: hidden facts like when it was taken and often exactly where you stood. Add it up and the company has a detailed record of your tastes, habits, friends, and movements — which is exactly what advertisers pay top prices to aim at. The app is free because those tables about you are the product."

Yours will differ. What matters: (1) the app is stored facts in tables, not magic, (2) metadata rides along invisibly, (3) the business model — targeted advertising — is why those facts are worth money.
</details>
