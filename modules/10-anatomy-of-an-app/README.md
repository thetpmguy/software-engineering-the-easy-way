# 🍽️ Module 10 — The Anatomy of an App: Frontend, Backend & APIs

> **What you'll learn:** what an app is actually made of. We'll dissect one like a frog
> in biology class — no formaldehyde needed — and name the organs: the **frontend** you
> see, the **backend** you never see, and the **APIs** carrying messages between them.
> You'll follow a single tap of the "Like" button through the entire system, step by
> numbered step.
>
> **Why it matters:** "frontend", "backend", and "API" are probably the three most-used
> words in any tech workplace. After this module, they're yours. In the lab, you'll
> peek behind a real website's curtain with tools already hiding in your browser.

---

## 🧠 One analogy to rule this module: the restaurant

Have you ever wondered where an app *is*? When you tap Instagram, some of it must be
on your phone — you can see it. But your photos don't live in your phone; ten friends
in three countries can see them. So where's the rest of it?

Answer: an app is not one thing in one place. It's at least two programs in two places,
talking over the internet. And the cleanest way to understand the whole arrangement is
one analogy we'll keep for the entire module: **an app is a restaurant.**

> 🌉 **Analogy:** A restaurant has a **dining room** — everything the customer sees and
> touches: tables, menus, decor, the arrangement of it all. It has a **kitchen** —
> where orders are actually cooked, with equipment and processes customers never see
> (and are not allowed to enter). And between them runs the **waiter** — carrying
> structured orders in, and finished dishes out. You don't need to know the chef, or
> how the stove works, to get dinner. You need a menu and a waiter.
>
> **Where the analogy breaks down:** we'll collect the cracks as we go — the biggest
> one being that this restaurant's dining room is *inside your own home* (your device),
> and the kitchen is often thousands of miles away serving millions of dining rooms at
> once.

Now let's name the organs properly.

## 🎨 The frontend — the dining room

The **frontend** is the part of an app that you see and touch — and it runs on *your*
device: your phone, your laptop, your browser. Every button, every animation, every
screen of Instagram-the-app-on-your-phone is frontend. When people say an app is
beautiful, or confusing, or snappy, they're almost always talking about the frontend.

The dining room's job is presentation and interaction. It draws the menu, takes your
tap, shows a spinner while the kitchen works, and displays the dish when it arrives.
Note what it does *not* do: your phone does not store your friends' photos, doesn't
know anyone's password, and doesn't decide whether your payment goes through. The
dining room doesn't cook.

## 🍳 The backend — the kitchen

The **backend** is the part of an app that runs on the company's computers — not
yours — doing the work users never see: checking passwords, saving data, moving money,
deciding what shows up in your feed. If the frontend is what the app *looks like*, the
backend is what the app *actually does*.

Where does a backend physically run? On **servers** — which, as you learned back in
Module 03, are ordinary computers that stay on all the time so other computers can ask
them for things. A backend is programs running on always-on computers, in buildings
full of such computers. When Instagram "is down," those programs are having a bad day —
the app icon on your phone is fine.

Why keep the important work in the kitchen instead of the dining room? Same reasons as
a restaurant:

- **Trust.** Customers can't be allowed to grill their own steaks — and your phone
  can't be allowed to decide "the payment succeeded." Anything users could tamper with
  must be decided in the kitchen. (Much more in [Module 14](../14-security/README.md).)
- **Shared state.** All ten of your friends see the same photo because there is *one*
  kitchen with *one* pantry, not ten separate copies in ten pockets.
- **Heavy equipment.** Some cooking needs industrial ovens — computing power and
  storage no phone carries.

## 🤵 The API — the waiter (and the menu)

So the dining room is in your pocket and the kitchen is a thousand miles away. How do
they talk? They talk through the third organ, and it's the one non-technical people ask
about most.

An **API** (application programming interface) is a menu of things one program can ask
another program to do — plus the waiter that carries those requests over and brings
the answers back. Two halves to that definition, both essential:

- **The menu**: a fixed, published list of what you may ask for. Instagram's backend
  offers requests like *get the latest photos for this user*, *post this comment*,
  *like this photo*. You can order anything on the menu — and *nothing that isn't*.
  There is no "let me into the kitchen to rummage" option, which is precisely the
  point.
- **The waiter**: the actual carrying of a structured order to the kitchen ("table 12:
  one Like, on photo #8817263") and of the response back ("done — that photo now has
  205 likes").

The deep idea: **you don't need to know the chef to order.** The frontend team doesn't
need to know *how* the backend cooks, and vice versa — they agree on the menu, then
work independently. That agreement is what lets a hundred teams build one product, and
what lets total strangers' programs use each other, as we'll see shortly.

> ⚠️ **Watch out:** in everyday tech talk, "API" gets used loosely — for the menu, the
> waiter, or the kitchen door itself ("we call their API"). Don't let it rattle you:
> it's always the same idea — a defined way for one program to ask another for things.

> ✅ **Check yourself**
> 1. Frontend, backend — which runs on your device, and which on the company's?
> 2. Why must "did the payment succeed?" be decided in the backend?
> 3. An API is two things in one — what are they?
>
> <details><summary>Show answers</summary>
>
> 1. The **frontend** runs on your device (the dining room, in your home); the
>    **backend** runs on the company's servers (the kitchen, far away).
> 2. Because the frontend is on hardware users control and could tamper with. Anything
>    involving trust — money, passwords, permissions — must be decided in the kitchen,
>    where customers can't reach.
> 3. A **menu** (the fixed list of things one program may ask another to do) and the
>    **waiter** (the mechanism that carries each structured request over and the answer
>    back).
> </details>

## ❤️ Follow one tap: what happens when you "Like" a photo

Time for the dissection proper. You tap the little heart under a friend's photo. It
turns red in a fraction of a second. Here is everything that actually happened, step by
step:

```
 YOUR PHONE (dining room)          THE INTERNET           COMPANY SERVERS (kitchen)
┌──────────────────────────┐                          ┌───────────────────────────┐
│ 1. finger taps ♡          │                          │ 4. backend checks you are │
│ 2. frontend notices,      │   3. API request  ───▶  │    really you             │
│    sends the "order"      │                          │ 5. database: likes +1     │
│ 8. heart turns red ❤️     │  ◀───  7. response       │ 6. backend replies "done" │
└──────────────────────────┘                          └───────────────────────────┘
```

1. **Your finger taps the heart.** The frontend — code running on your phone — detects
   a touch at those screen coordinates and knows a heart lives there.
2. **The frontend composes an order.** Not a screenshot, not a phone call — a small,
   structured message: *"User token XYZ requests: like photo #8817263."*
3. **The API request travels over the internet.** The waiter walks to the kitchen —
   through the wifi, the cables, and the routing you learned in Module 03. This is the
   longest step, and it still usually takes well under a second.
4. **The backend checks who you are.** The kitchen doesn't take orders from strangers:
   it verifies the token proves you're logged in as you, and that you're allowed to see
   that photo at all.
5. **The database updates a number.** The backend tells its **database** — the app's
   permanent, organized memory, the pantry and recipe book of our restaurant — to
   record your like: that photo's count goes from 204 to 205, and a note is stored that
   *you* liked it. (Databases are a whole world; [Module 12](../12-databases/README.md)
   is entirely about them.)
6. **The backend replies.** "Done — 205 likes."
7. **The response travels back** across the internet to your phone.
8. **The heart turns red.** The frontend receives "done" and updates the screen.

One small confession that makes engineers smile: many apps turn the heart red at step 2,
*before* the kitchen confirms — because waiting feels slow, and un-liking a photo on the
rare failure is a cheap price for feeling instant. The dining room sometimes flatters
you. Now you know.

## 🦴 The web frontend's three ingredients

When the frontend is a *website*, it's built from exactly three languages, each with one
job. One gentle paragraph and one tiny example each — you'll meet all three alive in the
lab.

**HTML is the skeleton — the nouns.** **HTML** is the language that lists what is *on*
a page: this is a heading, this is a paragraph, this is a button. No colors, no
behavior — structure only.

```html
<h1>Rosa's Bakery</h1>
<p>Fresh bread daily.</p>
<button>Order now</button>
```

Reading it plainly: a big heading saying "Rosa's Bakery", a paragraph of text, a button.
The angle-bracket labels — **tags** — name what each thing *is*.

**CSS is the clothing — the style.** **CSS** is the language that describes how things
should *look*: colors, sizes, fonts, spacing. It points at the skeleton and dresses it.

```css
h1 {
  color: darkred;
  font-family: Georgia;
}
```

Plainly: "every big heading: dark red, in the Georgia typeface." Change the CSS and the
same skeleton becomes a different-looking page — same body, new outfit.

**JavaScript is the muscles — the behavior.** **JavaScript** is the programming
language that makes pages *do* things when you interact with them. HTML can show a
button; only JavaScript decides what happens when it's pressed.

```javascript
button.addEventListener("click", function () {
  alert("Thanks for your order!");
});
```

Plainly: "when that button is clicked, pop up a thank-you message." Every like-button
animation, every form that checks your email as you type — JavaScript. (It is, note,
a different language from the Python you wrote in Module 05 — same ideas, different
spelling.)

Skeleton, clothing, muscles: nouns, style, behavior. Every website you have ever
visited is these three, in different proportions.

## 🌐 Why APIs are *everywhere*

Here's where the waiter idea pays off big. APIs don't only connect a company's own
dining room to its own kitchen — companies publish APIs so that *other companies'*
programs can order from their kitchen:

- Your calendar app shows the weather? The calendar's backend orders forecasts from a
  weather company's API.
- **"Sign in with Google"** on some small website? That site never sees your password —
  it asks Google's API "is this really them?", and Google's kitchen answers.
- A travel site comparing forty airlines? Its backend calls forty airline APIs and
  plates the answers on one page.

It's restaurants offering their kitchen to other restaurants: the little café doesn't
build a bakery — it orders bread from Rosa's, via Rosa's menu, on Rosa's terms. Whole
businesses exist that are *only* a kitchen with a great menu — companies you've never
heard of whose APIs handle the payments, maps, and text messages inside the apps you
use daily. When engineers say "there's an API for that", this is what they mean, and
there almost always is.

## 🗺️ How engineers draw all this

Sketch the restaurant as labeled boxes and arrows and you've drawn an **architecture
diagram** — the standard back-of-napkin way engineers depict a system's major parts and
who talks to whom. You've already read one (the Like diagram above). The general shape
of almost every app on Earth:

```
[ frontend ] ──API──▶ [ backend ] ──▶ [ database ]
 your device            servers         the pantry
```

Two last vocabulary gifts. Engineers who work mostly in the dining room are *frontend
developers*; mostly in the kitchen, *backend developers*; and a **full-stack**
developer works across both sides. And one term you'll hear in the news: some companies
build the backend as one big program (a **monolith** — one big restaurant, one kitchen,
one menu), others as many small cooperating programs (**microservices** — a food court
of tiny specialized kitchens). Each has trade-offs that teams argue about with
religious intensity; for this course, knowing the two words and the food-court picture
is genuinely enough.

> ✅ **Check yourself**
> 1. In the Like-button journey, which steps happen on your phone, and which on the
>    company's servers?
> 2. HTML, CSS, JavaScript — match each to skeleton, clothing, muscles.
> 3. Your recipe app shows a map of nearby grocery stores. Did the app's company
>    probably build its own maps? What happened instead?
>
> <details><summary>Show answers</summary>
>
> 1. Steps 1, 2, and 8 happen on your phone (frontend); steps 4, 5, and 6 happen on the
>    servers (backend + database); steps 3 and 7 are the trip across the internet.
> 2. HTML = skeleton (what's on the page — the nouns); CSS = clothing (how it looks);
>    JavaScript = muscles (what it does when touched).
> 3. Almost certainly not. Its backend (or frontend) calls a mapping company's API —
>    ordering from someone else's kitchen instead of building one. That's why the same
>    familiar map style appears inside so many different apps.
> </details>

## 🎁 Recap

- An app is a **restaurant**: the **frontend** is the dining room (everything you see
  and touch, running on *your* device), the **backend** is the kitchen (the real work,
  running on the company's **servers**), and the **database** is the pantry and recipe
  book (the app's permanent memory — Module 12).
- An **API** is a menu of things one program can ask another to do, plus the waiter
  carrying structured requests and responses. You don't need to know the chef to order.
- A tap of the Like button = 8 steps: tap → frontend → API request across the internet
  → backend checks identity → database +1 → response → red heart.
- Web frontends are three languages: **HTML** (skeleton/nouns), **CSS**
  (clothing/style), **JavaScript** (muscles/behavior).
- APIs are everywhere because companies serve their kitchens to each other: weather in
  your calendar, "Sign in with Google", travel comparison sites.
- **Full-stack** = both sides. **Monolith** vs. **microservices** = one big restaurant
  vs. a food court. **Architecture diagrams** = the boxes-and-arrows napkin sketch.

## 🚪 Next up

You've now seen how software is planned (07), versioned (08), tested (09), and
assembled (10) — Part 3 complete. Part 4 goes deeper and more famous: why are some apps
instant and others sluggish? The answer lives in the classic ideas of computer
science — algorithms and data structures — served, as always here, without the scary
math.

**Next:** [Module 11 — Algorithms & Data Structures in Plain English](../11-algorithms-and-data-structures/README.md)
