# 🔧 Lab 03 — Watch the Postal System Work

> **Goal:** see every character from the lesson in real life: your own IP address, a
> real DNS lookup, the dozens of requests behind one web page, and the padlock's
> certificate.
>
> **You need:** a web browser. Parts 1–3 and 5 work on a phone or laptop; Part 4 (the
> best one) needs a laptop or desktop with Chrome, Edge, or Firefox. Nothing to
> install, no accounts, nothing you can break — we are only watching.

---

## Part 1 — Find your own street address (5 minutes)

The lesson said every online device has an IP address. Let's see yours.

1. Open your browser and search for exactly this phrase: **what is my ip**.
2. Most search engines show your address right at the top of the results, before any
   links — four numbers separated by dots, like `84.203.112.9`. (Some devices show a
   newer, longer format with colons and letters — that's the modern version of the
   same idea, needed because the four-number kind is running out.)
3. Write it down. Then, if you can, switch networks — turn WiFi off so your phone uses
   mobile data — and search again.

> **✅ What you should see:** an IP address — and a *different* one after switching
> networks. Why? Because on WiFi you're mailing letters from your home's address, and
> on mobile data you're mailing them via the phone network's address. Your "street
> address" belongs to your connection point, not to your device forever.

## Part 2 — Look someone up in the phone book (10 minutes)

Now do manually what your browser does secretly before every visit: a DNS lookup.

1. Search for: **DNS lookup**. The results will include several free lookup tools —
   pick any of the first few (they all do the same thing; no sign-up needed).
2. In the tool's search box, type a famous website's name, e.g. `wikipedia.org`, and
   run the lookup.
3. Look for a result line labeled **A** (that's the record type meaning "here is the
   IP address for this name"). You should see one or more IP addresses.
4. Try two or three more names you use daily — your favorite news site, a shopping
   site. Note that some names return *several* addresses.

> **✅ What you should see:** every name turns into at least one IP address — the phone
> book working before your eyes. Several addresses for one name means the site runs
> many servers and lets clients spread across them, like a shop with many branches so
> no single counter gets swamped.

## Part 3 — Trace the journey in your head (5 minutes)

No tool for this one — a rehearsal. Pick a website you visited today and narrate its
two-second journey out loud (or on paper), postal style, from memory:

1. My browser asked the phone book (DNS): "what number is this name?"
2. It got back an IP address.
3. My device did a quick handshake with that server, then mailed a request, cut into
   packets, each hopping through maybe a dozen post offices (routers).
4. The server mailed back the page as numbered envelopes.
5. My device reassembled them, discovered the page needed images and fonts too, and
   fired off dozens more requests.
6. The browser drew the page.

> **✅ What you should see:** you can tell the whole story without looking at the
> lesson. If a step feels fuzzy, reread that section — the next part will show all of
> this happening for real, and it's more fun when you can name what you're seeing.

## Part 4 — Watch the dozens of requests (15 minutes, laptop)

Every browser ships with a hidden engineer's dashboard. Let's open it. Steps below are
for **Chrome**; Edge is nearly identical, and Firefox is close (the tool is called
DevTools in all of them).

1. Open Chrome and go to any news website's front page.
2. Press **F12** (or **Ctrl + Shift + I**; on a Mac, **Cmd + Option + I**). A panel
   opens on the side or bottom of the window, full of tabs — this is **DevTools**, the
   browser's built-in inspection kit. Don't worry about most of it.
3. In the panel's row of tabs, click **Network**. It's probably empty, with a note
   telling you to reload.
4. Reload the page: **Ctrl + R** (Mac: **Cmd + R**). Now watch.
5. The panel fills with a cascade of rows — each row is *one request*: one little
   postal journey out and back. Look at the bottom of the panel for the total count:
   "**87 requests**" is typical; heavy pages exceed 150.
6. Read a few rows. You'll spot images (`.jpg`, `.png`), style files (`.css`), scripts
   (`.js`) — extensions, exactly as Module 02 promised. A **Size** column shows how
   big each parcel was, and a **Time** column shows how long its round trip took.
7. Find the *first* row in the list — that's the original request for the page itself.
   Every row below it was discovered while reading that first reply.
8. When you're done marveling, press **F12** again to close the panel. (You changed
   nothing — DevTools is a window, not a switch.)

> **✅ What you should see:** several dozen requests for one single page, each with its
> own size and travel time. This is the lesson's step 6 made visible: a web page is not
> one delivery, it's a whole day's postal round. On a phone you can't open DevTools —
> but now you know why a "simple" page can still feel slow on a weak signal: dozens of
> journeys, each losing packets.

## Part 5 — Inspect the padlock (5 minutes)

1. Visit any major website and look at the address bar. Look for the **padlock icon**
   (in newer Chrome versions it may look like a small settings/tune icon instead —
   click it either way).
2. Click it, then choose **Connection is secure**, then **Certificate is valid** (menu
   wording varies slightly by browser and version).
3. A small window shows the site's **certificate** — an identity document, issued to
   the site's owner by an organization browsers trust, with "issued to", "issued by",
   and validity dates.

> **✅ What you should see:** proof that "the padlock" is a real, inspectable document —
> the site proved its identity, and your traffic there travels in sealed envelopes.
> And remember the lesson's warning: the seal secures the *journey*. It doesn't promise
> the shop at the destination is honest.

## 🌊 Bonus — See the ocean floor (2 minutes)

Visit **submarinecablemap.com** and look at the real map of undersea internet cables.
Find the cables nearest your country. Every one on that map is a physical hose-thick
cable lying on the seabed, carrying conversations right now — quite possibly including
the packets that loaded the map itself.

## 🎉 Done!

You found your address, used the phone book, narrated the two-second journey, counted a
page's requests like an engineer, and read a certificate. Next: [the quiz](quiz.md),
then on to Part 2 with
[Module 04: How to Think Like a Programmer](../04-think-like-a-programmer/README.md).
