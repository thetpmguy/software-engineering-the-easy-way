# 🦁 Module 17 — Websites, Apps & Everything Else

> **What you'll learn:** the safari across every kind of software — websites, mobile
> apps, desktop programs, the hidden code in your car and washing machine, and games —
> organized by one question: *where does the code run?* Plus: how teams decide which
> kind to build, and why WhatsApp is one kitchen with five dining rooms.
>
> **Why it matters:** "should this be an app or a website?" is a million-dollar question
> asked in real meetings every day. After this lesson you'll know the honest trade-offs
> — and you'll start noticing that you're surrounded by a hundred computers you never
> counted.

---

## 🧠 One question organizes everything

Have you ever wondered why some things are apps you install, some are websites, and some
— like the software in your car — you never see at all? The software world looks like a
zoo of unrelated species. But one question sorts every animal into its habitat:

**Where does the code run?**

In your browser? On your phone? On your desktop machine? Inside your washing machine?
That single question explains how each kind is built, what it can do, and what it costs.
Let's take the safari, habitat by habitat.

## 🌐 Habitat 1: Websites and web apps — code that runs in the browser

Quick recap from [Module 10](../10-anatomy-of-an-app/README.md), in two lines: web pages
are built from **HTML** (the content and structure), **CSS** (the looks), and
**JavaScript** (the behavior). Your browser downloads those files and brings them to
life.

Here's the reframe that matters: **the browser is a universal app-player.** The same
Chrome or Safari, on any device, can run any web page ever made. Write your software as
a website and *everyone on Earth can use it in seconds* — no install, no app store, no
"sorry, not available on your device."

Within the browser habitat there are two species:

- A **website** presents information you mostly read — like Wikipedia or a restaurant's
  homepage.
- A **web app** is a full interactive tool that happens to run in a browser — like
  Google Docs or your online banking.

> 🌉 **Analogy:** A website is a *brochure*; a web app is a *workshop*. Both live in the
> same building (the browser), but one you read and one you work in. Wikipedia:
> brochure. Google Docs: workshop.
>
> **Where the analogy breaks down:** paper brochures never change; websites update
> constantly. And there's no crisp wall between the species — many sites are brochure at
> the front, workshop once you log in.

One more term you'll hear: **responsive design** — building one page that automatically
rearranges itself to fit any screen, from cinema-wide monitor to phone. One page, every
screen size. (You'll watch it happen with your own hands in the lab.)

## 📱 Habitat 2: Mobile apps — code that runs on the phone

Why isn't everything a web app, then? Because code installed *on* the phone gets
privileges a browser page doesn't: smooth access to the camera, GPS, notifications,
offline use, and every drop of the phone's speed.

A **native app** is one built specifically for one kind of phone, in that phone-maker's
preferred language — **Swift** for iPhone, **Kotlin** for Android.

> 🌉 **Analogy:** A native app is a *tailor-made suit*: it fits its platform perfectly —
> every gesture, every animation feels right. The catch: iPhone and Android are two
> differently-shaped customers, so you sew **two suits** — two codebases, two teams,
> roughly double the cost.
>
> **Where the analogy breaks down:** suits are sewn once; apps need constant re-tailoring
> as phones and their rules change every year. The two-suit bill repeats forever.

The double cost hurt enough that the industry invented **cross-platform frameworks** —
tools like **React Native** and **Flutter** that let one codebase produce both an iPhone
app and an Android app. One pattern, two suits. The honest price: small compromises —
the fit is very good but rarely *perfect*, and unusual platform tricks can take extra
work. For most apps, most users never notice. And a confession from inside the industry:
some "apps" are secretly just websites wrapped in an app-shaped costume — a thin shell
around a browser view. Fastest and cheapest of all; also the most likely to feel
slightly "off."

One more feature of this habitat: you can't hand your app to users directly. It goes
through the **app stores** — Apple's and Google's — and they behave like landlords.
They review every app before letting it in (safety for users, delays and rejections for
builders) and take a commission of roughly **15–30%** of sales made inside the app.
That cut is why some companies grumble loudly — a few have even gone to court over it —
and why others quietly steer you to their website to pay.

> ✅ **Check yourself**
> 1. Website vs. web app — which is Wikipedia, which is Google Docs?
> 2. Why does native development cost roughly double?
> 3. What do app stores take, and what do they give?
>
> <details><summary>Show answers</summary>
>
> 1. Wikipedia is a website (brochure — you read it). Google Docs is a web app
>    (workshop — you work in it).
> 2. iPhone and Android need separate codebases in separate languages (Swift, Kotlin) —
>    two tailor-made suits, sewn and re-tailored forever.
> 3. They take a 15–30% cut of in-app sales and control entry via review. They give
>    distribution to billions of phones and a safety screening users trust.
> </details>

## 🖥️ Habitat 3: Desktop software — code that runs on your computer

The classic species: Photoshop, Excel, video editors, serious games — big tools
installed on a PC or Mac, with full access to the machine's power, files, and hardware.
When professionals need heavy lifting, the desktop is still where it happens.

But here's the plot twist of the modern desktop. Many of today's desktop apps — very
possibly your chat app or music app — are **secretly browsers in a costume**. A tool
called **Electron** lets developers take a web app and ship it as an installable desktop
program: the "app" is a stripped-down browser showing one website, wearing a desktop
icon.

Why? Build once. The company already built the web version; Electron turns it into
Windows, Mac, and Linux apps almost for free — one team instead of four. The cost?
**Memory.** Every Electron app carries an entire hidden browser on its back, which is
why a "simple chat window" can consume as much of your computer's memory as fifty open
tabs. Engineers grumble about this constantly. The companies' accountants remain
unmoved.

## 🔌 Habitat 4: Embedded software — the hidden 90%

Now for the habitat nobody sees. Count the computers in your home. You'll say three or
four. The real answer is likely **dozens**: your washing machine, microwave, TV, car,
thermostat, printer, watch, even your electric toothbrush — each contains a small
computer running **embedded software**: code built into a device to do one job for the
life of the machine.

The numbers here are wilder than anywhere else on the safari. A modern car runs on the
order of **100+ million lines of code** — more than many famous "big" programs. Traffic
lights, elevators, pacemakers, aircraft: embedded code, all of it. By sheer count of
running programs, this hidden habitat may be most of the software on Earth.

Embedded programming is its own craft: tiny computers with tiny memories (thousands of
times less than your phone), no screen, no keyboard, and often no way to update. Which
raises the honest question — is *no updates* fine or frightening? Both. Your microwave's
code does one job, touches no network, and will run flawlessly for twenty years —
unpatched and perfectly safe. A pacemaker or a car is a different conversation, which is
why those industries test to standards ordinary app developers never face.

Then someone had an idea: what if we put WiFi in *everything*? That's the **Internet of
Things (IoT)** — everyday objects connected to the internet. Here's the honest
smart-lightbulb paragraph: connecting your lightbulb gives you real conveniences (dim
the lights from bed, heating that learns your schedule) and real costs — every connected
device is a tiny computer that can be hacked, that may stop working when its maker's
cloud shuts down, and that may be reporting your habits to someone's database. "Smart"
means *connected*, and connected cuts both ways. Buy accordingly.

## 🎮 Habitat 5: Games — the everything-discipline

Games deserve their own stop because they're the safari's apex species: the only kind of
software that must do *everything at once*. A modern game runs physics (how objects
fall and collide), 3D graphics, artificial intelligence for characters, audio,
networking for multiplayer, and player input — all recomputed **60 times every second**,
because that's what smooth motion requires. Most software waits for you to click. A
game redraws an entire world faster than you can blink, forever.

Building all that machinery from scratch for every game would be madness, so almost
nobody does. A **game engine** — the famous ones are **Unity** and **Unreal** — is a
pre-built foundation providing the physics, graphics, lighting, and sound machinery, so
creators build the *game*, not the plumbing.

> 🌉 **Analogy:** A game engine is a pre-built movie studio. A filmmaker walking into a
> studio doesn't invent cameras, build lighting rigs, and construct sound stages — those
> exist; they bring the script and the vision. Unity and Unreal are studios for rent, so
> a three-person team can make something gorgeous.
>
> **Where the analogy breaks down:** a studio is passive walls and gear. An engine is
> active machinery running inside the finished game on your device, simulating and
> drawing 60 times a second — the studio ships *with* the movie.

> ✅ **Check yourself**
> 1. Why might your chat app use as much memory as fifty browser tabs?
> 2. Where is most of the world's software, by count of running programs?
> 3. What does a game engine save a game creator from doing?
>
> <details><summary>Show answers</summary>
>
> 1. It may be an Electron app — a web app in a desktop costume, carrying an entire
>    hidden browser. The company builds once; your memory pays.
> 2. Hiding in embedded devices — cars (100+ million lines), washing machines,
>    pacemakers, traffic lights. The invisible habitat is the biggest one.
> 3. Rebuilding physics, graphics, lighting, and sound from scratch — the engine is the
>    rented movie studio, so the creator brings the script, not the cameras.
> </details>

## 🤔 How teams actually choose

So: web, native mobile, cross-platform, desktop, or several? In real meetings the
decision comes down to three factors: **who are the users** (and what device are they
on at the moment of need?), **budget** (one codebase or two-plus?), and **timeline**
(a website ships today; two native apps ship next quarter).

| If you need… | Build… | Because… |
|---|---|---|
| Everyone, right now, no installs | Web app | The browser is the universal app-player |
| Camera, offline use, top polish | Native apps | Full phone powers; tailor-made fit; costs double |
| Both stores on one budget | Cross-platform | One pattern, two suits, small compromises |
| Heavy professional power | Desktop | Full machine access for big tools |
| To live inside a device | Embedded | The code *is* the product's behavior |

> ⚠️ **Watch out:** when a company's job listings mention Swift, Kotlin, *and* React,
> that's not indecision — successful products usually end up needing several bodies at
> once. Which brings us to the safari's final sight.

## 🍽️ Same app, many bodies

Open WhatsApp on an Android phone. Now on an iPhone, then web.whatsapp.com in a browser,
then the desktop app. Four different frontends — different codebases, different teams —
yet your messages are identical in all of them, instantly.

Remember Module 10's restaurant: the **frontend** is the dining room (what you see and
touch), the **backend** is the kitchen (the servers where the real data and logic
live). WhatsApp is **one kitchen with many dining rooms**. The Android dining room, the
iPhone dining room, the browser dining room — all send orders to the same kitchen,
which is why your conversation follows you across every device.

That's the safari's souvenir. "An app" isn't one thing — it's a kitchen plus however
many dining rooms the audience demands, each built with the trade-offs from this
module.

## 📝 Recap

- Sort all software by **where the code runs**.
- **Browser:** websites (brochures) and web apps (workshops); the browser is a
  universal app-player; **responsive design** = one page, every screen.
- **Phone:** **native** apps (Swift/Kotlin) are tailor-made suits — perfect fit, double
  cost; **cross-platform** (React Native/Flutter) = one pattern, two suits, small
  compromises; app stores are landlords — review plus a 15–30% cut.
- **Desktop:** big full-power tools — and many modern ones are **Electron**: websites
  in a costume; build once, pay in memory.
- **Embedded:** the hidden 90% — 100+ million lines in your car; no updates is
  sometimes fine, sometimes scary; **IoT** = WiFi in everything, convenience and risk
  in the same bulb.
- **Games:** everything at once, 60 times a second; **engines** (Unity/Unreal) are
  rented movie studios.
- Teams choose by users, budget, timeline — and big products build many bodies: one
  kitchen, many dining rooms.

## 🚪 Next up

The safari showed you every kind of software. But software doesn't build itself — and
"engineer" is only one chair at the table. Who are the designers, product managers,
testers, and data scientists, and what do they all *do* between 9 and 5? Meet the whole
cast in [Module 18 — Who Does What in Tech](../18-who-does-what-in-tech/README.md).
