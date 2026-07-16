# ✅ Quiz 10 — Frontend, Backend & APIs

Answer in your head or on paper, then open the fold to check.

---

**1. Using the restaurant analogy: what are the frontend, the backend, and the API?**

<details><summary>Show answer</summary>

The **frontend** is the dining room — everything the customer sees and touches, running
on *your* device. The **backend** is the kitchen — where the real work happens, on the
company's servers, off-limits to customers. The **API** is the menu plus the waiter —
the fixed list of things you may ask for, and the carrying of structured orders in and
dishes out.
</details>

---

**2. Where does the frontend physically run, and where does the backend physically
run?**

<details><summary>Show answer</summary>

The frontend runs on the user's own device — their phone, laptop, or browser. The
backend runs on the company's **servers**: ordinary computers that stay on all the time
so other computers can ask them for things. (The biggest crack in the restaurant
analogy: this dining room is in your home, and one faraway kitchen serves millions of
dining rooms at once.)
</details>

---

**3. In the lab, you changed a news site's headline in your browser — and a refresh
brought the real one back. What does that demonstrate about frontends?**

<details><summary>Show answer</summary>

That the frontend is merely *your copy* of the dining room, fully in your hands — you
can redecorate it, and the kitchen never knows. Which is exactly why nothing important
(payments, passwords, permissions) can be decided in the frontend: users control that
hardware and can tamper with it. Trust lives in the backend.
</details>

---

**4. Put the Like-button journey in order: □ database updates the count □ finger taps
the heart □ backend checks who you are □ response travels back □ heart turns red
□ frontend composes the order □ API request crosses the internet □ backend replies
"done".**

<details><summary>Show answer</summary>

Finger taps the heart → frontend composes the order → API request crosses the internet
→ backend checks who you are → database updates the count → backend replies "done" →
response travels back → heart turns red. (Fun confession from the lesson: many apps
turn the heart red early, right after step 2, because waiting feels slow — and quietly
undo it on the rare failure.)
</details>

---

**5. Why does the backend check who you are (step 4) before updating anything?**

<details><summary>Show answer</summary>

Because the kitchen can't take orders from strangers. The request arrives from a device
the company doesn't control, so the backend verifies the included token proves you're
logged in as you — and that you're allowed to do what you're asking (can you even see
that photo?). Skipping this check would let anyone like, read, or delete anything by
sending forged orders.
</details>

---

**6. HTML, CSS, JavaScript — give each one's body-part analogy and its one-line job.**

<details><summary>Show answer</summary>

**HTML** = the skeleton (the nouns): lists what is *on* the page — headings, paragraphs,
buttons. **CSS** = the clothing: how it all *looks* — colors, fonts, sizes, spacing.
**JavaScript** = the muscles: what the page *does* when you interact — what happens on
a click, a keystroke, a scroll.
</details>

---

**7. A small website offers "Sign in with Google." Does that site learn your Google
password? What actually happens?**

<details><summary>Show answer</summary>

No — that's the whole point. The small site never sees your password. It asks Google's
API, in effect, "is this person really who they claim?" — you prove yourself to
*Google's* kitchen, and Google's API tells the site "yes, it's them." One restaurant
ordering a service from another restaurant's kitchen, via its published menu.
</details>

---

**8. What is JSON, and where did you meet it in the lab?**

<details><summary>Show answer</summary>

**JSON** is the simple labeled-values text format most APIs use to send data — braces,
labels, colons, values, like `{ "temperature": 24, "condition": "sunny" }` — readable
by machines and humans alike. In the lab, you saw it in the Network tab's responses,
and again raw in your browser when you called the Open-Meteo weather API yourself.
</details>

---

**9. Your travel app compares prices from forty airlines. Did its developers strike
deals to build forty airline systems? What's really going on — and why is this pattern
everywhere?**

<details><summary>Show answer</summary>

Its backend calls the airlines' **APIs** — forty published menus — and plates the
answers on one screen. The pattern is everywhere because APIs let companies offer their
kitchen to other restaurants: maps, payments, weather, and sign-in inside your apps are
usually other companies' kitchens, ordered from via API. Nobody builds everything;
almost everybody serves somebody.
</details>

---

**10. What does a full-stack developer do? And what's the one-sentence difference
between a monolith and microservices?**

<details><summary>Show answer</summary>

A **full-stack** developer works on both sides — dining room and kitchen, frontend and
backend. A **monolith** is a backend built as one big program (one big restaurant, one
kitchen); **microservices** split it into many small cooperating programs (a food court
of tiny specialized kitchens). Both are legitimate; teams argue trade-offs endlessly —
and for now, the two words and the food-court picture are all you need.
</details>

---

**11. The quick test from the lab: how do you decide whether something in an app is
frontend or came from the backend?**

<details><summary>Show answer</summary>

Ask: **"Could my phone know this all by itself, even in airplane mode?"** The button's
shape, the colors, the layout — yes: frontend. Your friend's new post, your bank
balance, search results, live prices — no: they came from a kitchen, carried by an API
waiter. (Try it: put your phone in airplane mode and open an app. What still works is
frontend; every spinner and error is a missing waiter.)
</details>

---

**12. 🗣️ Explain it to a friend**

Your friend says: *"A developer quoted me for building my shop's app, and the quote
says 'frontend', 'backend', and 'API integration' as three separate line items. Is he
padding the bill with jargon?"*

In under a minute, plain words: explain what each line item is and why they're
genuinely three different pieces of work.

<details><summary>One possible answer</summary>

"Not padding — those really are three different jobs. Think of your app as a
restaurant. The *frontend* is the dining room: everything customers see and tap on
their phones — screens, buttons, the look and feel. The *backend* is the kitchen: a
program running on always-on computers that does the real work — keeping your product
list, taking orders, knowing who's logged in. Customers never see it, but without it
the app is an empty room. And *API integration* is hiring the waiters — building the
defined ways the dining room orders things from the kitchen, and probably also
connecting to other companies' kitchens, like a payment service so you're not handling
card numbers yourself, or a maps service for delivery. Different pieces, often even
different specialists — that's why they're separate lines. If you want to check the
quote's balance rather than its honesty, ask him what's in version one of each — now
you can follow the answer."
</details>
