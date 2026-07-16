# 🔧 Lab 06 — Touch Real Data

> Time: about 60 minutes. Tools: a web browser, a phone with photos on it, paper and a pen. Nothing to install, nothing to sign up for.

Four exercises. Each one puts your hands on *real* data — the same formats and structures the lesson described. Do them in order if you can, but each stands alone.

---

## Exercise 1: Make and open a CSV (15 min)

You'll create a real CSV file about five friends, then open it as plain text to prove there's no magic inside.

**Route A — with a plain text editor (works on any computer):**

1. Open the simplest text editor you have: Notepad on Windows, TextEdit on Mac (in TextEdit, use the menu to switch the document to "plain text" mode first).
2. Type a heading line, then one line per friend — exactly this shape, with your own real friends:

   ```
   name,city,favorite_food
   Amara,Lagos,jollof rice
   Ben,Toronto,pancakes
   Chloe,Manchester,dumplings
   Deepa,Pune,dosa
   Elias,Berlin,pretzels
   ```

3. Save the file as `friends.csv` (if the editor insists on `.txt`, save it, then rename the ending to `.csv`).
4. Now double-click the file. On most computers it opens in a spreadsheet program — your typed commas have become columns, your lines have become rows.

**Route B — with Google Sheets (works on a phone or any browser):**

1. Go to **sheets.google.com** and start a blank spreadsheet (this route does need a Google account — if you'd rather not, use Route A).
2. Type the same table: headings in the first row (`name`, `city`, `favorite_food`), one friend per row below.
3. Find the **Download** option in the File menu and choose **Comma-separated values (.csv)**.
4. Now open the downloaded file with a plain **text** editor (not a spreadsheet app — on a phone, a notes or file-viewer app that shows raw text).

**✅ What you should see (both routes):** the same information wearing two outfits. In a spreadsheet: a tidy table. In a text editor: bare lines with commas. Nothing hidden, nothing binary — a CSV *is* text, and now you've verified it personally. You have created structured data: every row, same slots. That's the tax form, not the shoebox.

---

## Exercise 2: Look at live JSON from a real public service (15 min)

Real services all over the internet hand out data as JSON to anyone who asks — no password needed. You're going to ask, using nothing but your browser's address bar.

1. In your browser, try this address (type or paste it exactly):

   ```
   https://api.open-meteo.com/v1/forecast?latitude=52.52&longitude=13.41&current_weather=true
   ```

   This asks **Open-Meteo**, a free public weather service, for the current weather in Berlin (latitude 52.52, longitude 13.41).
2. Look at what comes back: curly braces, `"labels": values`, nested boxes — live JSON, generated for you a second ago. Find the temperature in it. Find the wind speed.
3. Make it *yours*: replace the latitude and longitude in the address with your own city's (search the web for "latitude longitude" plus your city name), and reload.
4. Also try **worldtimeapi.org** — its front page explains a simple pattern like `worldtimeapi.org/api/timezone/Europe/London` for asking the current time anywhere, again returned as JSON.

> **⚠️ Watch out:** public services occasionally move or retire their addresses. If either one fails, nothing is wrong with you or your browser — search the web for **"free public JSON API"**, pick any example that needs no key or sign-up, and paste its address. The goal isn't these two services; it's seeing real JSON arrive in your browser.

**✅ What you should see:** a wall of `{ "curly": "braces" }` that, after this module, you can actually *read*. Notice it's the exact shape from the lesson: keys, values, boxes inside boxes. Your weather app does precisely this every time you open it — it fetches JSON like yours and paints a sun icon over it.

---

## Exercise 3: Inspect a photo's metadata on your phone (10 min)

Time to read the label on the box — on your own photos.

1. Open your phone's photo app and pick a photo you took yourself, outdoors, months or years ago.
2. Find the details view:
   - **iPhone:** open the photo and swipe up on it, or tap the ⓘ info button.
   - **Android:** open the photo, tap the three-dot menu, and choose **Details** or **Info** (or swipe up, on some models).
3. Read what your phone wrote down without asking you: the exact date and time, the phone model, camera settings — and, if location was on, a **map of where you stood**.
4. Now the privacy check: think of the last photo you sent or posted. Did you know it might carry a map pin? Explore your camera settings — every phone has a switch for whether photos record location, and most messaging apps strip location metadata when sending, but not all services do.

**✅ What you should see:** more than you expected. That's the point. The photo is data; everything on the details screen is metadata — and it wrote itself. You don't need to turn anything off today; you need to *know it's there*, and now you do.

---

## Exercise 4: Sketch the table behind your favorite app (15 min)

Paper and pen. You're going to do real data design — the same first step professional engineers do on whiteboards.

1. Pick an app you use daily. WhatsApp works beautifully; Instagram or your banking app also work.
2. Ask: *what is the main "thing" this app stores?* For WhatsApp: a message. One row per message.
3. Draw a table. Write column headings: what facts must the app record about each message for the app to work? Start with these and add your own:

   | sender | recipient | text | time_sent | read_yet? |
   |---|---|---|---|---|

4. Fill in three rows with made-up-but-realistic messages between you and a friend.
5. Now interrogate your design — each question you can answer from the table is a feature you've explained:
   - Which column makes the ✓✓ "seen" ticks possible?
   - How would the app show messages in order? (Which column? This is why `time_sent` matters.)
   - What column would you *add* to support group chats? Voice notes? Deleting a message "for everyone"?
6. Stretch goal: sketch a second table your app must also have (WhatsApp: a `contacts` or `groups` table) and draw an arrow showing how a column in one table points at rows in the other. If you do this, you have independently reinvented the core idea of relational databases — [Module 12](../12-databases/README.md) will feel like coming home.

**✅ What you should see:** a paper table that explains real app behavior. The moment "read_yet?" clicks as *the ✓✓ column*, something permanent happens: apps stop being magic surfaces and become tables with good outfits. That lens never turns off — you'll catch yourself sketching the table behind every new app you meet.

---

## Done?

You've now written, fetched, inspected, and designed real data — four formats, zero installs. Take the [quiz](quiz.md), skim the [resources](resources.md), and then it's on to Part 3: [Module 07 — From Idea to App](../07-idea-to-app/README.md).
