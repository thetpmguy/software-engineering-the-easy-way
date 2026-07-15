# 🏗️ Module 07 — From Idea to App: The Software Development Lifecycle

> **What you'll learn:** how a scribble on a sticky note becomes an app used by millions —
> the six stages every piece of software goes through, why teams plan in two-week
> "sprints", what an MVP is, and why software projects are famously late.
>
> **Why it matters:** whether you want to work in tech, work *with* tech people, or
> launch your own idea one day, this is the map of how it actually happens. After this
> lesson, phrases like "we're still in the requirements phase" or "let's ship an MVP"
> will make perfect sense.

---

## 🧠 Every app you love started as a sticky note

Instagram started as a clunky check-in app called Burbn. WhatsApp began as a way to show
tiny status messages next to your name. Somewhere, right now, an idea that will change
your daily life in five years is written on a napkin.

So how does a napkin become an app on a million phones? Not by one genius typing
furiously for a weekend. It happens through a *process* — a repeatable series of stages
that the software world calls the **software development lifecycle** (often shortened to
**SDLC**): the journey every piece of software takes from idea, to plan, to working
product, to ongoing care.

The best way to understand it is to build a house.

> 🌉 **Analogy:** Building software is like building a house. You don't start by pouring
> concrete. You start by asking who will live there and what they need. Then you draw
> blueprints. Then you build. Then an inspector checks the work. Then the family moves
> in. And then — forever after — someone has to fix the leaky roof.
>
> **Where the analogy breaks down:** we'll be honest with you right away, because this
> is one of the most important truths in this whole course. A house, once built, mostly
> stays built. Software *never stops changing*. Users ask for new rooms every month. The
> ground under the house (phones, browsers, laws, competitors) shifts constantly. Many
> engineers say software is less like building a house and more like **gardening**: you
> plant it, and then you tend it forever. Keep both pictures in mind as we walk through
> the stages.

Let's tour the house — stage by stage.

## 📋 Stage 1: Requirements — who lives here, and what do they need?

Before anyone draws a blueprint, an architect asks questions. How many kids? Do you cook
a lot? Do you work from home? Skip this conversation and you'll build a beautiful house
for the wrong family.

In software, this stage is called gathering **requirements** — the list of things the
software must do, written down *before* anyone builds it. Teams get requirements by
talking to the people who will actually use the product: interviewing them, watching
them work, studying what frustrates them today.

The most popular way to write a requirement down is a **user story** — a single sentence
describing one thing one kind of user needs, in this shape:

> *As a **[kind of person]**, I want **[to do something]**, so that **[reason]**.*

Real examples from a ride-hailing app:

- "As a **rider**, I want **to see my driver moving on a map**, so that **I know when to
  walk outside**."
- "As a **driver**, I want **to see my earnings for the day**, so that **I know when I've
  hit my goal**."

Notice what user stories are *not*: they say nothing about databases, screens, or code.
They describe a human need. The team figures out the "how" later. That's the point — it
keeps the conversation about people, not technology.

> ⚠️ **Watch out:** the most expensive mistakes in software are made here, not in the
> code. A bug in the building stage might cost an hour to fix. Building the wrong
> product entirely costs months. This is why good teams spend real time talking to users
> before writing a single line.

## 📐 Stage 2: Design — drawing the blueprints

Now the architect draws. Where do the walls go? Which materials — brick or timber?

Software teams produce two kinds of blueprints:

- A **design doc** is a written plan describing how the software will work on the
  inside — what the major pieces are and how they'll talk to each other. It's a few
  pages of plain writing and diagrams that teammates read and argue about *before*
  building. Arguing over a document is cheap. Arguing over half-built software is not.
- **Wireframes** (also called **mockups** when they're polished) are rough sketches of
  what each screen will look like — boxes for buttons, lines for text, no colors needed.
  A wireframe answers "where does the user tap?" before anyone builds the screen.

There's one more design decision, and it's choosing your building materials. A team's
**tech stack** is the set of tools, programming languages, and services they choose to
build with. Brick or timber? Python or JavaScript? Rent computers from Amazon or Google?
Like materials, these choices are hard to change once the walls are up, so teams choose
carefully.

> ✅ **Check yourself**
> 1. What's the template for a user story?
> 2. Why write a design doc instead of starting to build immediately?
>
> <details><summary>Show answers</summary>
>
> 1. "As a [kind of person], I want [to do something], so that [reason]." It describes a
>    human need, not a technical solution.
> 2. Because finding a flaw in a document costs an afternoon of discussion; finding the
>    same flaw in half-built software costs weeks of rebuilding. Paper is cheaper than
>    construction.
> </details>

## 🔨 Stage 3: Build — pouring the foundation

This is the stage everyone pictures when they imagine software: engineers writing code.
The formal word is **implementation** — turning the design into actual working software.

Here's what surprises most people: on a healthy team, building is often the *most
predictable* stage. If the requirements are clear and the design is solid, the building
goes smoothly. When projects go wrong, the root cause is usually upstream — a fuzzy
requirement, a design nobody questioned — discovered only when the concrete is already
poured.

You already know from Modules 04 and 05 what this stage feels like from the inside:
breaking problems into steps and writing them in a language a machine can follow.

## 🔍 Stage 4: Test — the building inspector

No serious builder says "the house is done" without an inspection. Do the doors close?
Does the wiring spark? Does the roof leak when it rains?

Software gets inspected too. Testers (and automated checks written by engineers) try the
software the way real users will — including the weird ways. What happens if someone
types their name as 3,000 letters? What if the internet cuts out mid-payment?

Testing is such a deep and delightful topic that it gets its own module —
[Module 09](../09-bugs-and-testing/README.md) is entirely about bugs and testing. For
now, know that it's a formal stage, not an afterthought.

## 🚚 Stage 5: Release — moving day

The house passed inspection. Time to hand over the keys.

In software, releasing has a word you'll hear constantly in tech conversations: to
**deploy** software means to move it from the engineers' computers onto the real
computers where actual users can use it. Before deploying, only the team can see the new
feature. After deploying, the whole world can. When an engineer says "we're deploying at
3pm", they mean: at 3pm, this goes live.

Moving day is nervous-making in both worlds. Careful teams deploy gradually — new
software goes to 1% of users first, then 10%, then everyone — so that if something's
broken, few people are affected and the team can roll back, like a moving truck that can
reverse out of the driveway.

## 🔧 Stage 6: Maintain — the leaky roof, forever

The family moved in. Done? Not remotely. Roofs leak. Pipes freeze. The family has a baby
and needs another bedroom.

**Maintenance** is all the work of keeping released software healthy: fixing bugs users
discover, updating it when phones and browsers change, and adding the features people
ask for. This is where the house analogy quietly collapses and the gardening one takes
over — because for successful software, maintenance isn't a small afterthought. **Most
of the money and engineering time spent on software over its lifetime is spent after
release.** This is why "the app is finished" still requires a team of engineers, and why
your apps update every week.

> ✅ **Check yourself**
> 1. What does "deploy" mean, in plain words?
> 2. Which stage consumes the most engineering effort over a product's lifetime?
>
> <details><summary>Show answers</summary>
>
> 1. To move software from the team's computers to the real computers where actual users
>    can use it — to make it live.
> 2. Maintenance — the ongoing fixing, updating, and improving after release. Software is
>    a garden, not a finished house.
> </details>

## 🍳 Waterfall vs. Agile: the banquet and the taste test

Here's a question that split the software world for decades: should you do those six
stages *once, in order* — or over and over in small loops?

The do-it-once-in-order approach is called **waterfall** — finish all the requirements,
then all the design, then build everything, then test everything, then release, each
stage flowing down into the next like water over a falls.

> 🌉 **Analogy:** Waterfall is cooking a 10-course banquet from a menu fixed months in
> advance. You plan every dish, buy every ingredient, cook for three days, and serve it
> all at once. If the guests turn out to hate seafood — you find out at course four, with
> six seafood courses still coming and no way to change the menu.

For decades this was the standard, borrowed from construction and manufacturing. And for
some things it still fits: you can't launch half a rocket. But for most software it kept
failing in the same painful way — teams spent a year building exactly what was requested,
only to discover that what was *requested* wasn't what was *needed*. People are bad at
knowing what they want until they can touch it.

So the industry moved to **agile** — a way of working where you build a small piece,
show it to real users, learn from their reactions, and adjust the plan, again and again.

> 🌉 **Analogy:** Agile is tasting-and-adjusting as you cook. Make one dish. Have the
> guests taste it. Too salty? Adjust. They loved the sauce? Make more things with the
> sauce. You still might cook ten courses — but each one is shaped by what you learned
> from the last.
>
> **Where the analogy breaks down:** dinner guests are politely stuck with you. Software
> users aren't — if your first course is bad enough, they leave and never come back. Agile
> teams still have to make the *first* small thing genuinely worth using.

In agile, work happens in **sprints** — fixed periods, usually two weeks, in which the
team commits to a small goal, builds it, and shows working results at the end. Think of
each sprint as one cooking round: plan the dish Monday, serve a taste in two weeks,
listen, repeat. All six SDLC stages still happen — but a little of each, every sprint,
instead of once ever.

## 🛹 The MVP: build the skateboard, not the car

Agile thinking produced one of the most useful ideas in modern product-building. An
**MVP** — **minimum viable product** — is the smallest version of your idea that real
people can genuinely use, built so you can start learning from them as soon as possible.

There's a famous drawing about this, and it's worth describing in words. Suppose your
grand vision is a car. The *wrong* way to build it in stages is: first a wheel, then two
wheels, then a chassis, then finally a car. Why wrong? Because a wheel is useless. For
months, users can't do anything with your partial car, so you learn nothing.

The *right* way: first build a **skateboard**. It's humble, but a person can actually get
from A to B on it. Then a scooter. Then a bicycle. Then a motorbike. Then the car. At
every stage, users are *going somewhere* — and telling you things you'd never have
guessed. Maybe they say "I love the fresh air — do I even want an enclosed car?" and you
end up building a convertible. The skateboard wasn't a small piece of the car. It was a
small *version of the whole idea*: getting a person from A to B.

That's the discipline of an MVP: not "a fraction of the features", but "the whole
purpose, in miniature". Deciding what to leave out of version one is some of the hardest
and most valuable thinking a team does.

## ⏰ Why is software always late?

You've heard the jokes. The project that was "two weeks away" for a year. Why is
estimating software so hard, when a builder can quote you a garage to within a week?

> 🌉 **Analogy:** Estimating software is like renovating an old house. You quote two
> weeks to redo the bathroom. Then you open the wall — and find sixty-year-old wiring,
> a pipe that isn't on any plan, and a wasp nest. Nobody lied. Nobody was lazy. The
> information you needed *did not exist* until you opened the wall.

Software is full of walls you can't see behind: a tool that doesn't work as documented, a
requirement that turns out to have a hidden contradiction, an old piece of code nobody
fully understands. Engineers call these **unknown unknowns** — problems you couldn't have
listed in advance, because you didn't know they existed. And unlike a house, every
software project is being built for the first time; if identical software already
existed, you would use *that* instead of building it. Every project is a renovation of a
house no one has renovated before.

This is a big part of why agile won: if estimates beyond a few weeks are guesses, plan in
detail for two weeks and re-plan when you know more.

## 🧑‍🤝‍🧑 Who does all this? A quick cast of characters

You may be picturing "developers" doing all six stages. Real teams share the work: a
**product manager** decides *what* to build and why; **designers** shape what it looks
and feels like; **engineers** build it; **testers** (QA) inspect it; and other roles
besides. Each deserves a proper introduction, and gets one —
[Module 18](../18-who-does-what-in-tech/README.md) decodes every job title in tech. For
now, remember: software is a team sport, and most of the players don't code all day.

> ✅ **Check yourself**
> 1. What's the difference between waterfall and agile, in one sentence each?
> 2. Why is a skateboard a better first version of "a car" than a wheel?
> 3. Why couldn't the renovation contractor give an accurate quote?
>
> <details><summary>Show answers</summary>
>
> 1. Waterfall: do every stage once, in order, and release at the end. Agile: build a
>    small piece, learn from real users, adjust, and repeat in short loops (sprints).
> 2. A skateboard actually transports a person, so users can use it and teach you things.
>    A wheel does nothing on its own, so you learn nothing while you build the rest.
> 3. Because the crucial problems were hidden behind the wall — unknown unknowns. The
>    information needed for an accurate estimate didn't exist until the work began.
> </details>

## 🎁 Recap

- The **software development lifecycle (SDLC)** is the journey from idea to living
  product: **requirements** (what do users need? — captured as **user stories**),
  **design** (design docs, wireframes, choosing a **tech stack**), **build**, **test**,
  **release** (to **deploy** = make it live for real users), and **maintain** (forever —
  software is a garden, not a house).
- **Waterfall** does the stages once, in order — like a fixed banquet menu. **Agile**
  loops through them in short **sprints**, tasting and adjusting. The industry moved to
  agile because people can't fully know what they want until they can touch it.
- An **MVP** is the smallest *complete* version of the idea — the skateboard, not the
  wheel — built to start learning from real users fast.
- Software estimates are hard because of **unknown unknowns**: like renovating an old
  house, you don't know what's behind the wall until you open it.

## 🚪 Next up

You now know the process teams follow. But wait — if dozens of people are all editing
the same code at once, why doesn't it collapse into chaos? The answer is one of the most
elegant tools in all of software, and you'll use it yourself, hands-on, in the next
module.

**Next:** [Module 08 — Git & GitHub: The Time Machine for Teamwork](../08-git-and-github/README.md)
