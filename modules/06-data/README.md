# 📊 Module 06 — Data: The World's New Oil

> **Part 2 — Thinking Like an Engineer** · Previous: [Your First Code](../05-your-first-code/README.md) · Next: [From Idea to App](../07-idea-to-app/README.md)

## What you'll learn

- Why every app you love is mostly a wrapper around **data**
- What data actually is — and the difference between **structured** and **unstructured** data
- The three containers programs keep data in: **lists**, **dictionaries**, and **tables**
- What file formats like **.csv** and **.json** really look like inside
- Where apps keep data: memory vs. files vs. **databases** (a preview)
- What **metadata** is — and why it matters for your privacy
- Why companies want your data so badly

## Why it matters

Have you ever wondered what Instagram *is*? Strip away the logo and the filters, and here's the unglamorous truth: Instagram is a gigantic table of photos, a table of users, and a table of who-liked-what. WhatsApp? A table of messages: who sent it, to whom, the text, the time. Your bank? At its heart, a very, very careful spreadsheet of amounts moving between accounts.

Almost every app is a pretty face on top of stored facts. The pretty face changes with fashion; the stored facts are the actual product. That's why people call data "the new oil" — and why understanding data means understanding most of what software really does. In [Module 05](../05-your-first-code/README.md) your programs handled scraps of information. Today we look at what information *is*, how it's shaped, and where it lives.

---

## 🧾 What is data, really?

**Data** is recorded facts. That's the whole definition. Your height is a fact; written on a doctor's chart, it becomes data. The temperature outside is a fact; logged by a weather station, it's data. A fact that nobody records vanishes; a recorded fact can be stored, copied, searched, and added up.

**Digital data** is facts written down as numbers, so a computer can store them. And truly *everything* digital is numbers underneath — you may remember this from [Module 01](../01-what-is-a-computer/README.md). Text is numbers (each letter has a number code). Photos are numbers (each dot's color, as three numbers). Songs are numbers (thousands of tiny air-pressure measurements per second). If a computer holds it, it's numbers all the way down.

> **🌉 Analogy:** data is the difference between *remembering* your grandmother's soup and having her **recipe card**. The memory fades and can't be shared. The card is a recorded fact: it can be copied, mailed, filed, and followed by a stranger in another country.
>
> *Where the analogy breaks down:* a recipe card degrades and there's only one original. Digital data copies perfectly and endlessly — the millionth copy is identical to the first. That perfect copyability is why data spreads so fast, for better and for worse.

## 🗂️ Structured vs. unstructured

Not all recorded facts are equally usable. There are two broad kinds:

**Structured data** is facts arranged in a fixed, predictable layout — every item has the same labeled slots.

**Unstructured data** is facts recorded free-form, with no fixed layout — text, photos, voice notes.

> **🌉 Analogy:** a **filled-in tax form** versus a **shoebox of receipts**. The tax form is structured: line 4 is always income, line 9 is always deductions, on everyone's form. A clerk (or a machine) can process a thousand of them without thinking. The shoebox holds the same underlying facts — but crumpled, in every layout, some faded, some in handwriting. Finding "total spent on fuel" means reading every slip.
>
> *Where the analogy breaks down:* a human can at least read the shoebox slowly. For decades computers mostly couldn't use unstructured data at all — that's changing now with AI (Module 16), which is precisely software that learns to read shoeboxes.

The lesson hiding here: **structure is what makes data powerful.** A million tax forms can be summed in a second. A million shoeboxes are a warehouse of sadness. Much of software engineering is the art of getting facts *into* structure.

> **✅ Check yourself**
>
> 1. Your contact list, with a name slot and a phone slot for every person — structured or unstructured?
> 2. Three years of your voice memos — structured or unstructured?
>
> <details><summary>Show answer</summary>
>
> 1. Structured — every entry has the same labeled slots.
> 2. Unstructured — free-form recordings with no fixed layout. Useful to you, but hard for software to search or add up without AI help.
> </details>

---

## 📦 Data structures: the containers

Once facts are structured, programs keep them in standard containers. A **data structure** is a standard shape for holding data so a program can work with it. There are many; three cover most of daily life. (Module 11 goes deeper.)

### The list — a shopping list

A **list** is an ordered sequence of items. It has a first item, a second, a last — and the same value can appear twice.

> **🌉 Analogy:** a **shopping list**. `milk, eggs, bread, eggs` — order preserved, duplicates allowed, and you can add to the bottom or cross things off.
>
> *Where it breaks down:* on paper, inserting an item in the middle means squeezing handwriting. A program's list inserts anywhere, instantly and neatly.

You met one in Module 05: `["Amara", "Ben", "Chloe"]`. Lists are what `for` loops love to walk through. Your message history is a list. A playlist is a list — it's in the name.

### The dictionary — look it up by name

A **dictionary** (also called a **key-value store**) holds pairs: a **key** you look things up by, and a **value** stored under that key.

> **🌉 Analogy:** a real dictionary, or better, your **contacts app**. You don't find Priya's number by reading contacts from the top — you jump straight to "Priya" (the key) and read her number (the value). One key, one value, instant lookup.
>
> *Where it breaks down:* a paper dictionary is sorted alphabetically and that's *why* lookup is fast. A program's dictionary doesn't need sorting at all — it jumps straight to any key by a cleverer trick (Module 11 reveals it). Also, paper dictionaries are printed once; a program's dictionary adds and removes entries constantly.

Anywhere software goes "give me the thing filed under X," there's a dictionary: your username → your profile, a word → its translation, a product code → its price.

### The table — rows of things, columns of facts

A **table** holds many items of the same kind: one **row** per item, one **column** per fact about it.

> **🌉 Analogy:** a **spreadsheet** — because that's honestly what it is. Rows are the things (one row per friend), columns are the facts (name, city, birthday). The power move: whole-column questions. "Everyone in Nairobi?" "Average age?" One glance down a column answers questions about *all* the rows.
>
> *Where it breaks down:* your spreadsheet has a few hundred rows and one user — you. Real app tables hold billions of rows with millions of people reading and writing at once, which needs the heavy machinery of databases (previewed below, full story in Module 12).

Now the opening claim becomes concrete. Instagram's core is a `photos` table (row per photo: who posted, when, caption) plus a `likes` table (row per like: who, which photo, when). WhatsApp's core is a `messages` table. Your bank's core is a `transactions` table where every row is money moving. Fancy wrapper, humble tables.

| Container | Analogy | Superpower |
|---|---|---|
| List | Shopping list | Keeps order; loop through items one by one |
| Dictionary | Contacts app | Instant lookup by name (key) |
| Table | Spreadsheet | Ask questions about all rows at once |

> **✅ Check yourself**
>
> 1. Which container fits "the queue of songs to play next"?
> 2. Which fits "given a flight number, find its departure gate"?
> 3. Which fits "all 50,000 customers, with name, email, and signup date for each"?
>
> <details><summary>Show answer</summary>
>
> 1. A list — order is the whole point of a queue.
> 2. A dictionary — flight number is the key, gate is the value.
> 3. A table — many items of the same kind, same facts (columns) for each.
> </details>

---

## 💾 Files and formats: what data looks like on disk

When a program saves data, it writes a file — and the **file format** is the agreed-upon layout of what's inside, usually signaled by the ending of the file's name (`.txt`, `.csv`, `.jpg`). A format is a promise: "anything that knows the rules can read this." Let's open three common ones. They're less mysterious than they look.

**.txt — plain text.** Nothing but the characters themselves. What you see is literally what's stored.

**.csv — a spreadsheet as plain text.** CSV stands for *comma-separated values*: one row per line, columns separated by commas. Here is a complete, real CSV file — three lines:

```
name,city,age
Amara,Lagos,34
Ben,Toronto,61
```

First line: the column headings. Each following line: one row. That's the entire format. When someone "exports a spreadsheet as CSV," this is all that happens — and you can open it in a plain text editor and read it yourself, as you'll do in the [lab](lab.md).

**.json — nested labeled boxes.** JSON (pronounced *JAY-sun*) is the format apps and websites use to send structured data to each other. It's built from labeled values in curly braces — like a dictionary written down:

```json
{
  "name": "Amara",
  "city": "Lagos",
  "pets": ["cat", "parrot"]
}
```

Read it out loud: name is Amara; city is Lagos; pets is a list of two. Keys on the left of each colon, values on the right — and values can be boxes or lists themselves, nested as deep as needed: labeled boxes inside labeled boxes. When your weather app fetches today's forecast, a little JSON like this is what actually arrives over the network. You'll look at real, live JSON in the lab.

**Images and audio are data too.** A photo file is a long list of numbers — three per dot (how much red, green, blue). A `.jpg` adds clever compression, but underneath: numbers. An audio file: thousands of loudness measurements per second. Not human-readable like CSV, but the same deep idea — facts as numbers, in an agreed layout.

---

## 🏠 Where apps keep data: memory, files, databases

An app has three places to keep data, with a trade-off between speed and permanence.

**Memory** — the working values inside a running program. Every variable from Module 05 lived here. Blazing fast, but it evaporates the moment the program stops. A game's current score lives in memory — close the app without saving and it's gone. (This is the RAM from [Module 01](../01-what-is-a-computer/README.md).)

**Files** — data written to storage, surviving shutdowns. Fine for one document, one photo, one program's settings.

**Databases** — the professional option. A **database** is a program whose entire job is storing large amounts of structured data safely and answering questions about it fast, even with many users at once.

> **🌉 Analogy:** files are boxes in your garage — fine until you have ten thousand boxes and three family members rummaging at once. A database is a **filing cabinet with a librarian who never sleeps**: everything indexed, retrieval in seconds, and the librarian makes sure two people updating the same record don't scribble over each other.
>
> *Where it breaks down:* a librarian handles one request at a time; a real database handles thousands per second. And no librarian will refuse mid-filing and undo half a change — databases do exactly that to keep money-moving operations safe.

This is a preview on purpose. Databases get their own full module: [Module 12](../12-databases/README.md). For now, hold the picture: memory = whiteboard (fast, wiped), files = garage boxes (permanent, clumsy at scale), database = librarian (permanent *and* fast *and* safe).

---

## 🏷️ Metadata: the label on the box

**Metadata** is data *about* data — not the content itself, but facts describing it.

> **🌉 Analogy:** the **label on a moving box**. The label isn't the dishes; it says "KITCHEN — FRAGILE — packed 12 March." Small, but it decides how the box gets handled without anyone opening it.
>
> *Where it breaks down:* you write box labels deliberately. Digital metadata mostly writes *itself*, silently — which is exactly why it deserves your attention.

Take one photo on your phone. The image is the data. Attached to it, automatically: the date and time, the camera model, the exposure settings — and, very often, the **GPS location where you stood**. Post that photo, and depending on the service, that label may travel with it. A stranger could learn where you live from a picture of your breakfast.

Metadata is genuinely useful — it's how your phone builds those "One year ago today" albums. But here's the fact worth remembering: **metadata can reveal nearly as much as content.** Who you called, when, how often, and from where sketches your life in detail without a single word of any call — which is why the lab has you go and look at what your own photos are carrying around.

---

## 💰 Why companies want your data

Time to answer the module's title. Why is data "the new oil"?

Because recorded facts about people are worth money, in at least three ways:

1. **Data improves the product.** Netflix's watch tables tell it what to recommend — and what shows to make next.
2. **Data targets advertising.** This is the big one. An advertiser pays far more to reach "people who searched for baby strollers this week" than to reach everyone. Detailed facts about you make the ad slot next to your feed dramatically more valuable. When an app is free, this is usually the actual business: you pay in facts.
3. **Data compounds.** More users → more data → better product and better targeting → more users. Oil burns once; data keeps working, which is roughly where the metaphor gives out.

None of this needs a villain — mostly it's ordinary companies optimizing. But it explains the modern world: why everything wants an account, why apps ask for location, why "free" is everywhere. And it hands you a good habit: when a product is free, ask *what facts am I paying with, and am I OK with that trade?* Sometimes yes, sometimes no — but now you know to ask, and by Module 14 (Security) you'll know how to act on the answer.

> **✅ Check yourself**
>
> 1. What's the difference between a photo's data and its metadata?
> 2. Why is a free app usually not really free?
>
> <details><summary>Show answer</summary>
>
> 1. The data is the image itself; the metadata is the attached facts *about* it — when it was taken, on what device, and often where.
> 2. Because the business is usually your data: the facts you generate improve the product and make advertising aimed at you more valuable. You pay in facts instead of cash.
> </details>

---

## 🎁 Recap

- **Data** is recorded facts; digital data is facts written as numbers. Apps are mostly fancy wrappers around stored facts.
- **Structured** data (tax form) is machine-friendly; **unstructured** (shoebox of receipts) is not. Structure is where the power is.
- Three everyday containers: **list** (shopping list — ordered, repeats allowed), **dictionary** (contacts app — look up by key), **table** (spreadsheet — rows of things, columns of facts).
- Formats are agreed layouts: **.csv** is a spreadsheet as plain text; **.json** is nested labeled boxes; images and audio are numbers in fancier layouts.
- Data lives in **memory** (fast, evaporates), **files** (permanent, clumsy at scale), or a **database** (the tireless librarian — full story in [Module 12](../12-databases/README.md)).
- **Metadata** — the label on the box — can reveal nearly as much as the contents. Check what your photos carry.
- Free apps are usually paid for with your facts. Worth asking about, every time.

## 🌉 Next up

You now hold all three foundations: how machines work (Part 1), how to think in exact steps and write code (Modules 04–05), and what that code operates *on* (this module). Part 3 changes the question from "what is software?" to "**how does real software actually get built?**" In [Module 07 — From Idea to App](../07-idea-to-app/README.md), we follow a sticky-note idea all the way to a shipped product, and meet the process professional teams really use. See you there.
