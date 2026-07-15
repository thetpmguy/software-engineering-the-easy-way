# 🔧 Lab 01 — Meet Your Own Machine

> **Goal:** find the chef, the counter, and the pantry inside the device you're holding
> right now — and write your name the way a computer would.
>
> **You need:** your phone *or* any laptop, plus a pen and paper for Part 3. Nothing to
> install. Nothing to sign up for. You cannot break anything in this lab — we are only
> *looking*.

---

## Part 1 — Find your device's specs (10 minutes)

Every device will tell you what's inside it. Let's go find out. Pick the section that
matches your device and follow the numbered steps. Menu names vary slightly between
versions and brands — if a name doesn't match exactly, look for the closest one.

### On an iPhone or iPad

1. Open the **Settings** app (the gray gear icon).
2. Tap **General**, then tap **About**.
3. Look for **Model Name** (e.g. "iPhone 13") and **Capacity** (e.g. "128 GB").
   Capacity is your **storage** — the pantry.
4. Apple doesn't show RAM or chip name in Settings. That's fine: type your model name
   plus the word "specs" into any search engine, and the RAM (e.g. "4 GB") and chip
   (e.g. "A15") appear in the first results.

### On an Android phone

1. Open the **Settings** app.
2. Scroll to the bottom and tap **About phone**.
3. You should see the device name, and often **RAM** (e.g. "6 GB") and
   **Internal storage** (e.g. "128 GB") right there. On some phones, storage details
   live under **Settings → Storage** instead.
4. The chip name may be listed under "Processor". If not, search your phone's model
   name plus "specs" to find it.

### On a Windows laptop

1. Click the **Start** button, then the **Settings** gear.
2. Go to **System**, then scroll down to **About**.
3. Look at **Installed RAM** (e.g. "8 GB") and **Processor** (e.g. an "Intel Core" or
   "AMD Ryzen" chip name).
4. For storage: in Settings, search for "Storage" — you'll see something like
   "256 GB, 180 GB used".

### On a Mac

1. Click the **Apple menu** () in the top-left corner of the screen.
2. Click **About This Mac**.
3. You'll see the **Chip** (e.g. "Apple M2") and **Memory** (that's RAM, e.g. "8 GB").
4. For storage, click **More Info** (or the **Storage** tab on older Macs) to see
   something like "512 GB".

> **✅ What you should see:** three numbers, whatever your device — a RAM size (probably
> between 4 and 32 GB), a storage size (probably between 64 GB and 1 TB), and a chip
> name. Write all three down. If you found them: congratulations, you have officially
> read a spec sheet.

## Part 2 — Interpret the numbers like an engineer (5 minutes)

Now translate your three numbers using Module 01's kitchen:

1. **Your RAM number is the size of the kitchen counter.** More RAM = more apps can be
   "on the counter" at once without the chef shuffling things back to the pantry.
   Notice how much smaller it is than your storage — counters are expensive; pantries
   are cheap.
2. **Your storage number is the size of the pantry.** A quick sense of scale: one photo
   is roughly 3 MB (megabytes), and 1 GB is about 1,000 MB. So "128 GB" is room for
   very roughly 40,000 photos. How many photos would *your* pantry hold?
3. **Your chip name is your chef.** Search the chip name plus "how many cores" if
   you're curious how many chefs are actually in your kitchen. (Most phones today: 6–8.)

> **✅ What you should see:** your storage is many times larger than your RAM — usually
> 20 to 50 times larger. If yours fits that pattern, you've confirmed the
> counter-vs-pantry tradeoff with real hardware: fast space is scarce, slow space is
> plentiful.

## Part 3 — Watch the counter fill up (10 minutes)

RAM isn't a fixed fact — it's a workspace in constant use. Let's watch it move.

### On a Windows laptop

1. Press **Ctrl + Shift + Esc** together. A window called **Task Manager** opens — a
   live dashboard of everything your computer is doing. If it looks tiny, click
   **More details**.
2. Click the **Performance** tab, then click **Memory** in the left list. You'll see a
   moving graph: this is your kitchen counter, live. Note the "In use" number.
3. Now open a browser and open five or six tabs with different websites. Watch the
   "In use" number climb — each tab is claiming counter space.
4. Close the tabs. Watch the number drift back down as the counter is cleared.

### On a Mac

1. Press **Cmd + Space**, type "Activity Monitor", and press Enter.
2. Click the **Memory** tab. The list shows every running program and how much counter
   space each is using; the "Memory Used" figure at the bottom is the total.
3. Open several browser tabs, watch the numbers rise; close them, watch them fall.

### On an Android phone

1. Open **Settings** and search for "Memory" (on many phones it's under
   **Device care** / **Battery and device care**, or inside Developer options on some
   models — if you can't find it, skip to the "no dashboard" note below).
2. You'll see something like "5.1 GB / 6 GB used" — a live counter report.

### On an iPhone (and any phone without a memory dashboard)

iPhones don't show a RAM dashboard, and that's a deliberate design choice — the system
manages the counter for you. Instead, try this: open ten apps in a row, then go back to
the first one. If it reloads from scratch instead of resuming instantly, you've caught
the system clearing old apps off the counter to make room. That reload *is* RAM
management, visible with no tools at all.

> **✅ What you should see:** memory usage that rises when you open things and falls
> when you close them. You have now watched the kitchen counter in action.

## Part 4 — Write your initials in binary (10 minutes, pen and paper)

The lesson said letters are stored as numbers, and numbers as 0s and 1s. Prove it by
writing your own initials the way your computer does.

Computers use an agreed code called **ASCII** (a standard table that gives every letter,
digit, and symbol its own number). Here are the capital letters:

| Letter | Number | Binary | | Letter | Number | Binary |
|---|---|---|---|---|---|---|
| A | 65 | 01000001 | | N | 78 | 01001110 |
| B | 66 | 01000010 | | O | 79 | 01001111 |
| C | 67 | 01000011 | | P | 80 | 01010000 |
| D | 68 | 01000100 | | Q | 81 | 01010001 |
| E | 69 | 01000101 | | R | 82 | 01010010 |
| F | 70 | 01000110 | | S | 83 | 01010011 |
| G | 71 | 01000111 | | T | 84 | 01010100 |
| H | 72 | 01001000 | | U | 85 | 01010101 |
| I | 73 | 01001001 | | V | 86 | 01010110 |
| J | 74 | 01001010 | | W | 87 | 01010111 |
| K | 75 | 01001011 | | X | 88 | 01011000 |
| L | 76 | 01001100 | | Y | 89 | 01011001 |
| M | 77 | 01001101 | | Z | 90 | 01011010 |

1. Write your initials at the top of the paper. (Example: "R.K.")
2. For each initial, find its row and copy the 8-digit binary pattern.
   Example: R = `01010010`, K = `01001011`.
3. Look at what you wrote. Each 1 is a switch turned **on**; each 0 is a switch turned
   **off**. Sixteen tiny switches, and they spell *you*.
4. Bonus: check one letter by hand. The positions in a byte are worth 128, 64, 32, 16,
   8, 4, 2, 1 (left to right). For R = `01010010`: the "on" positions are 64, 16, and
   2. Add them: 64 + 16 + 2 = 82. Look at the table — R is 82. It checks out.

> **✅ What you should see:** your initials as two rows of eight 0s and 1s, and (if you
> did the bonus) the addition confirming the code. Every text message you have ever
> sent was stored exactly like this — a byte per character, switches all the way down.

## 🎉 Done!

You found the chef, measured the counter and the pantry, watched the counter fill and
empty, and hand-encoded your name into the machine's native language. Next stop:
[the quiz](quiz.md), then [Module 02](../02-what-is-software/README.md).
