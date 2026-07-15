# 🧑‍🤝‍🧑 Module 18 — Who Does What in Tech

> **What you'll learn:** every job title you'll meet at a tech company — what each person
> actually does all day, in plain English — plus how teams organize their work ("agile",
> demystified), and the unwritten rules for talking to engineers so they'll love working
> with you.
>
> **Why it matters:** software is made by *people*, and most of them don't code. Whether
> you want to join a tech team, manage one, sell to one, or found one, knowing who does
> what — and how to speak to them — is a superpower. This module is the org chart,
> translated.

---

## 🧠 Welcome to the set

Have you ever stayed through a film's end credits? Hundreds of names scroll past:
gaffer, best boy, foley artist, script supervisor. You watched the actors for two hours,
but the credits reveal the truth — a film is made by a small army of specialists, most
of whom never appear on screen.

A tech company is the same. When you use an app, you're watching the "actors" — the
screens and buttons. Behind them stands a crew you never see. Today we walk the set and
meet everyone.

> 🌉 **Analogy:** A tech company is a film production. The product is the film. Engineers
> are the crew who physically make it. The product manager is the producer deciding what
> film to make. Designers are the cinematographers and set designers deciding how it
> looks and feels. QA is the continuity checker catching mistakes before the audience
> does. DevOps keeps the projectors running in every cinema, all night.
>
> **Where the analogy breaks down:** a film *wraps*. One day, shooting ends and everyone
> goes home. Software never wraps — you learned in
> [Module 07](../07-idea-to-app/README.md) that software is a garden, tended forever. So
> picture a film production that re-shoots and re-releases a slightly better film every
> two weeks, for years. That's a software team.

Let's meet the crew, one role at a time.

## 🔨 Software engineer — the builders

A **software engineer** (also called a **developer**) is the person who writes the code
that makes the product exist. On our film set, they're the camera operators, carpenters,
and effects artists — the hands that physically make the thing.

What do they do all day? Less typing than you'd guess. A typical day is a mix of:
reading existing code (like reading the previous chapters before writing the next one),
writing new code, reviewing teammates' work, fixing bugs, and talking — to each other,
to designers, to the product manager — about what to build and how.

You already know the main varieties from [Module 10](../10-anatomy-of-an-app/README.md):

- A **frontend engineer** builds the part users see and touch — the dining room of the
  restaurant.
- A **backend engineer** builds the hidden machinery — the kitchen, where the real
  cooking happens.
- A **full-stack engineer** works on both sides of the kitchen door.
- A **mobile engineer** specializes in apps for phones (iPhone, Android).

## 🎼 Engineering manager — the conductor

An **engineering manager** (often "EM") is the person responsible for the engineers
themselves — their growth, their workload, their happiness — rather than for the code.

> 🌉 **Analogy:** A conductor doesn't play an instrument during the concert — and is
> almost never the best violinist in the room. Their job is to make forty musicians
> sound like one orchestra: setting the tempo, balancing the sections, noticing who's
> struggling.
>
> **Where it breaks down:** a conductor makes real-time artistic decisions all night. A
> good engineering manager mostly does the opposite — they set direction, then get out
> of the way, and spend their days in one-on-one conversations, hiring, and clearing
> obstacles.

This surprises many newcomers: becoming a manager in tech is a *career change*, not a
promotion for the best coder. The best coder often stays a senior engineer — and may
earn more than their manager.

## 🎬 Product manager — the producer

A **product manager** (**PM**) decides *what* to build and *why*. They study users,
watch competitors, gather ideas, and turn all of it into a prioritized plan — often
written as the **user stories** you practiced in [Module 07](../07-idea-to-app/README.md)
("As a rider, I want to see my driver on a map, so that…").

They're the film's producer: the one asking "who is the audience for this? Why this film
and not another one? What can we afford?"

Here's the part outsiders always get wrong: **the PM is not anyone's boss.** Engineers
don't report to the PM; they report to the engineering manager. A PM leads by evidence
and persuasion — showing user research, data, and reasoning until the team agrees on
what matters most. In tech this is called *influence without authority*, and it's why
good PMs are excellent communicators. They spend their days in conversations, documents,
and decisions — and write no code.

## 🎨 Designer — architect of the experience

A **designer** decides how the product looks, feels, and flows. Two flavors you'll hear:

- **UX design** (**user experience**) is designing how the whole experience *works*:
  what steps a user takes, in what order, and how it feels. The UX designer is the
  *architect* — deciding where the rooms go and how you move between them.
- **UI design** (**user interface**) is designing how each screen *looks*: colors,
  spacing, typography, that satisfying button. The UI designer is the *interior
  decorator* — making each room beautiful and usable.

Many designers do both. Their days: interviewing users and watching them struggle
(called **user research** — studying real people to learn what they actually need),
sketching **wireframes** (you drew some in [Module 07's lab](../07-idea-to-app/lab.md)),
and refining pixel-perfect screens for engineers to build.

## 🔍 QA engineer — the continuity checker

A **QA engineer** (**quality assurance** — the person whose job is to find problems
before users do) is the professional breaker of things. You met their world in
[Module 09](../09-bugs-and-testing/README.md). On set, they're the continuity checker
who notices the coffee cup that teleports between shots — before the audience does.

Their day: writing test plans, trying the weird inputs no one expected, writing
automated tests that check the software thousands of times a day, and — importantly —
reporting bugs so precisely that engineers can reproduce and fix them.

## 🚒 DevOps / SRE — the stage crew and the fire brigade

Someone has to keep the show running in every cinema, at 3am, during a storm. That's
**DevOps** and **SRE**.

- A **DevOps engineer** (from "development" + "operations") builds the systems that
  move code safely from an engineer's laptop to the real servers — the conveyor belts,
  safety checks, and alarm systems of shipping software.
- An **SRE** (**site reliability engineer**) is responsible for keeping the product *up*
  — running, fast, and available — even when servers fail and traffic spikes.

Here's the honest part: these roles usually include **on-call** duty — carrying a
(digital) pager for a week at a time, and being the person who gets woken at 3am if the
product goes down. Teams rotate this duty, pay extra for it at many companies, and work
hard to make alarms rare. But it's real. When your favorite app "goes down" and comes
back twenty minutes later, a human somewhere got out of bed and fixed it.

## 🔮 The data trio — analyst, scientist, engineer

Three roles with "data" in the name, constantly confused, genuinely different:

- A **data analyst** *reads the tea leaves*: they examine the data a company already has
  and answer questions with it. "Did sales drop after the price change?" Their tools:
  spreadsheets, **SQL** (the database language from
  [Module 12](../12-databases/README.md)), and charts.
- A **data scientist** *builds crystal balls*: they build models that predict what will
  happen next — which customers might leave, what a rider will pay. This is the machine
  learning world from [Module 16](../16-ai-without-the-hype/README.md).
- A **data engineer** *builds the plumbing that carries the tea*: the pipelines that
  collect, clean, and deliver data so the other two have something trustworthy to work
  with. Unglamorous, essential, well-paid.

## 🛡️ Security engineer — the locksmith who thinks like a burglar

A **security engineer** protects the product and its users from attackers — the world
you explored in [Module 14](../14-security/README.md). Their days: reviewing designs for
weaknesses, running practice attacks against their own company (with permission!),
responding when something suspicious happens, and gently insisting that yes, everyone
really does have to use two-factor authentication.

## 📝 The connectors: writer, advocate, support

Three roles that keep humans and software understanding each other:

- A **technical writer** writes the guides, manuals, and help pages that explain the
  product — turning engineer-speak into human-speak. (This entire course is technical
  writing.)
- A **developer advocate** is the friendly face a company shows to outside programmers
  who use its products: giving talks, writing tutorials, and carrying feedback back to
  the team. Part teacher, part diplomat.
- A **support engineer** helps real users when things go wrong — and is often the first
  to spot a new bug in the wild. Great support engineers are detectives, and support is
  one of the most common doors *into* tech (more in
  [Module 19](../19-your-path-into-tech/README.md)).

## 🏢 And upstairs: the executives

One line each, as promised:

- The **CTO** (**chief technology officer**) sets the company's overall technical
  direction — which big bets to make, years out.
- The **VP of Engineering** runs the engineering organization day to day — hiring,
  budgets, and making sure fifty teams pull in the same direction.

> ✅ **Check yourself**
> 1. Who decides *what* to build — and is that person the engineers' boss?
> 2. Your app went down at 3am and recovered in 20 minutes. Which role probably woke up?
> 3. Data analyst, data scientist, data engineer — match each to: plumbing, tea leaves,
>    crystal ball.
>
> <details><summary>Show answers</summary>
>
> 1. The **product manager** decides what to build and why — but is *not* anyone's boss.
>    Engineers report to the engineering manager; the PM leads by evidence and persuasion.
> 2. An **SRE** or DevOps engineer on **on-call** duty.
> 3. Analyst = reads the tea leaves (answers questions from existing data). Scientist =
>    builds crystal balls (predictive models). Engineer = builds the plumbing that
>    carries the tea (data pipelines).
> </details>

## 🎯 The squad: how these people actually sit together

Companies don't pool everyone into one giant room. They form small units, often called
**squads** (or simply "teams"): typically **4–8 engineers, one product manager, and one
designer**, who together *own* one area of the product — the search team, the payments
team, the sign-up team.

Owning an area means: they plan it, build it, test it, ship it, and get woken up if it
breaks. Small enough to share one pizza order, complete enough to ship without asking
permission. Everything below describes how one squad works.

## 📺 The sprint: two-week episodes

You met **agile** in [Module 07](../07-idea-to-app/README.md) — build a small piece,
learn, adjust, repeat. Here's what it looks like on the ground.

Work happens in **sprints** — fixed two-week rounds in which the team commits to a small
goal and shows working results at the end. Think of a TV series: each episode (sprint)
must stand on its own and end with something watchable, while the season (the product)
adds up to something bigger.

Each sprint has a handful of recurring meetings — teams call them **rituals** or
**ceremonies**. Here they are, stripped of mystique, with what they honestly cost:

| Ritual | What it is, in plain terms | Time cost |
|---|---|---|
| **Standup** | Daily huddle. Each person, in ~1 minute: what I did yesterday, what I'll do today, what's blocking me. Standing up keeps it short. | 15 min daily |
| **Planning** | Start of sprint: pick which items from the wish-list fit into the next two weeks, and agree what "done" means for each. | 1–2 hours per sprint |
| **Demo** | End of sprint: show the *working* results to anyone interested. Not slides — the real thing. | 30–60 min per sprint |
| **Retro** | Short for **retrospective**: the team asks "what went well? what went badly? what will we change?" The golden rule is **blameless** — fix the system, not the person. | 1 hour per sprint |

That's it. That's "agile" — a wish-list, two-week episodes, a daily huddle, and the
humility to ask "how could we do this better?" every fortnight.

## 📌 The board, the tickets, and the backlog

Walk past any squad (or open their software) and you'll see a **board**: three columns —
**To do → Doing → Done** — with cards moving left to right across the sprint. One glance
tells anyone the state of the work. The most famous software for these boards is called
Jira; you'll hear the name, and now you know it's a digital corkboard.

Each card is a **ticket** (also called an **issue**): a written work order describing one
piece of work — what's needed, why, and how you'll know it's done. Like a repair shop's
work orders: numbered, tracked, and never done from memory.

And where do cards come from? The **backlog** — the team's list of *everything* anyone
has ever wished for, roughly sorted with the most important on top.

> 🌉 **Analogy:** The backlog is a restaurant's master list of every dish anyone ever
> suggested. Tonight's menu (the sprint) holds maybe six dishes. The list holds six
> hundred. Most will never be cooked, and that's healthy — the list is for *choosing*,
> not promising.
>
> **Where it breaks down:** a restaurant's list stays private. Backlogs are visible to
> the whole company, which is why people get upset finding their request at position 214.
> Position 214 doesn't mean "we hate your idea". It means 213 things currently matter
> more — and the order changes as the team learns.

## 🍳 Tech debt: why engineers ask for time to clean the kitchen

Sooner or later you'll hear an engineer say "we need to pay down some tech debt" or "we
need a sprint to **refactor**." Here's what that means, because it's the most
misunderstood request in software.

**Tech debt** (technical debt) is the cost of the shortcuts a team took to ship faster.
Every shortcut is a small loan: you save a day now, and you repay it later — with
interest — because the shortcut makes every *future* change slower and riskier.

> 🌉 **Analogy:** A restaurant kitchen during a rush. To get plates out fast, cooks skip
> the deep clean — pans pile up, the good knife goes missing under something. Reasonable!
> But a kitchen that's *never* cleaned gets slower every night, until one day it can't
> cook at all. **Refactoring** — reorganizing existing code to be cleaner without
> changing what it does — is cleaning the kitchen between rushes.
>
> **Where it breaks down:** a dirty kitchen is visible to any health inspector. Tech
> debt is invisible from outside — the app looks fine while the inside rots. That's
> exactly why engineers have to *ask* for cleaning time, and why wise managers grant it.

So when an engineer asks for time to refactor, they are not gold-plating. They're
telling you the kitchen is slowing down the food.

## 🎲 Estimates and story points, honestly

Teams often size work in **story points** — rough numbers (1, 2, 3, 5, 8…) expressing
how big a ticket *feels* relative to other tickets, rather than promising hours. Here's
the honest paragraph: all software estimates are educated guesses, and they're often
wrong, for the reason you learned in Module 07 — unknown unknowns, the pipes you can't
see until you open the wall. Points exist to make guessing *faster and less painful*,
not accurate. A team that says "that's an 8" means "that's one of the bigger things
we've done lately" — nothing more precise than that. Treat any estimate as a weather
forecast: useful for planning, foolish to treat as a promise.

> ✅ **Check yourself**
> 1. What are the three questions everyone answers at standup?
> 2. A card on the board, the team's full wish-list, and reorganizing code without
>    changing behavior — name all three.
> 3. Why is a retro "blameless"?
>
> <details><summary>Show answers</summary>
>
> 1. What did I do yesterday? What will I do today? What's blocking me?
> 2. A **ticket** (or issue), the **backlog**, and **refactoring**.
> 3. Because the goal is to fix the *system* that allowed a mistake, not to punish a
>    person. Punished people hide problems; safe people surface them — and surfaced
>    problems are the only ones you can fix.
> </details>

## 🗣️ How to talk to engineers

If you manage, market to, sell with, or found alongside engineers, this section repays
its reading time a hundredfold.

**1. Bring problems, not solutions.** "Users can't find the checkout button" is a gift —
it invites the team to find the best fix, which might be moving it, renaming it, or
redesigning the page. "Make the button red" is an order that skips the thinking. The
person who sees the *problem* firsthand (you) and the people who know the *possible
solutions* (them) do their best work when each contributes their half.

**2. Respect the maker's schedule.** A manager's day is naturally sliced into 30-minute
blocks. An engineer's day is not — the hard parts of their work require holding a huge
invisible structure in their head at once.

> 🌉 **Analogy:** Deep coding work is a soufflé. It takes a long, undisturbed bake to
> rise. Open the oven for "one quick question" and the soufflé collapses — and restarting
> isn't quick, because it must rebuild from cold. A 15-minute interruption genuinely
> costs about an hour of productive focus.
>
> **Where it breaks down:** unlike a soufflé, an engineer can tell you when the oven is
> safely open. So don't avoid them — *batch* your questions, prefer a written message
> they can answer between bakes, and save "got a sec?" for actual emergencies.

**3. Ask "what would make this easier?"** This one question — asked sincerely — will get
you more goodwill than any pizza budget. Often the answer is small: a clearer document,
one decision made, one meeting cancelled.

**4. Never say "it's a small change, right?"** The button is small. The plumbing behind
it may not be. Software is an iceberg: the visible tip (the screen) sits on nine-tenths
you can't see (data, systems, edge cases, tests). Only the person who can see underwater
can tell you the size — so ask, don't assert.

**5. Ask for estimates kindly.** Instead of "when will it be done?" (which demands a
promise), try: *"No commitment — is this a days thing, a weeks thing, or a months
thing?"* You'll get an honest range instead of a defensive silence, because you've made
it safe to be uncertain.

And a field guide to meetings:

| Engineers usually love | Engineers usually dread |
|---|---|
| A demo of real working software | A status meeting that repeats the board out loud |
| A whiteboard session on a hard problem | A "quick sync" with no agenda at 2pm (mid-soufflé) |
| A retro that actually changes something | Being asked for a commitment estimate on the spot |
| A crisp decision meeting that ends early | A meeting that could have been a message |

> ✅ **Check yourself**
> 1. Rewrite "add a search bar to the top of every page" as a problem statement.
> 2. Why does a 15-minute interruption cost more than 15 minutes?
> 3. What's a kinder way to ask "when will it be done?"
>
> <details><summary>Show answers</summary>
>
> 1. Something like: "Users on inner pages can't find products without going back to the
>    home page — they give up and leave." (A search bar is *one* possible fix.)
> 2. Because deep work is a soufflé: the engineer must rebuild a large mental structure
>    from scratch after the interruption — roughly an hour of lost focus.
> 3. "No commitment — is this a days thing, a weeks thing, or a months thing?" It invites
>    an honest range instead of demanding a promise.
> </details>

## 🎁 Recap

- A tech company is a **film production**: engineers build (frontend/backend/full-stack/
  mobile), the **engineering manager** conducts people (not code), the **product
  manager** produces — deciding *what* and *why*, leading without authority — and
  **designers** architect the experience (UX) and decorate it (UI).
- Around them: **QA** breaks things on purpose, **DevOps/SRE** keep the show running
  (including honest 3am **on-call**), the data trio reads tea leaves / builds crystal
  balls / lays plumbing, **security** guards the doors, and writers, advocates, and
  support engineers keep humans and software understanding each other.
- Work happens in **squads** (4–8 engineers + PM + designer) running two-week
  **sprints** with four rituals: **standup**, **planning**, **demo**, **retro** — plus a
  **board** of **tickets** fed by the **backlog**.
- **Tech debt** is borrowed time repaid with interest; **refactoring** is cleaning the
  kitchen. **Story points** are honest guesses, not promises.
- To talk to engineers: bring **problems, not solutions**; protect the **soufflé**;
  ask what would make things easier; never say "small change, right?"; ask for
  estimates as ranges.

## 🚪 Next up

You now know every seat on the set — and maybe one of them sounded like it could be
*yours*. The final lesson of this course is an honest, hype-free map of how real people
(nurses, teachers, shop owners) actually get into tech: what to learn, in what order,
what employers really look for, and how long it truly takes.

**Next:** [Module 19 — Your Path Into Tech](../19-your-path-into-tech/README.md)
