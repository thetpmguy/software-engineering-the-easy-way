# 🌐 Module 03 — How the Internet Works

> **What you'll learn:** what the internet physically is, how a message finds one
> computer among billions, what really happens in the two seconds after you type a web
> address, and what that padlock in your browser actually protects.
>
> **Why it matters:** you did something remarkable to read this page — you asked a
> computer you've never seen, possibly on another continent, for a file, and it
> answered in under a second. By the end of this module, that will make sense.

---

## 🧠 Start with the miracle

Type a few words into your phone. Tap once. In well under a second, an answer arrives —
possibly from a computer 10,000 kilometers away, across an ocean, in a building you will
never visit. It works on a train. It works in bed. It works so reliably that we only
notice it when it takes *three* seconds and we get annoyed.

How? Not magic — two things:

**Wires and agreements.** That's the internet.

The **internet** is a worldwide network of computers connected by cables (and some
radio links), all following the same shared rules for passing messages. The wires part
is real and physical: fiber-optic cables under streets, under fields, and — we'll get
there — under oceans. The agreements part is the clever bit. A **protocol** is an
agreed set of rules for how computers talk to each other — who says what, in what
order, in what format.

> 🌉 **Analogy:** Protocols are postal etiquette. Any letter, anywhere in the world,
> works the same way: address on the front, in a known format, country at the bottom,
> stamp in the corner. No postal worker in the chain needs to know you personally —
> they follow the shared rules, and the letter arrives. The internet is the same trick:
> billions of machines from thousands of companies cooperate *only* because they all
> follow the same rules for addressing and passing messages.
>
> **Where the analogy breaks down:** postal rules are enforced by governments; internet
> protocols are voluntary agreements — engineers follow them because a machine that
> breaks the rules gets ignored, like a letter with no address.

The postal system is such a good match for the internet that we'll use it for the whole
module. Every piece has a postal twin.

## 🏠 IP addresses: every machine has a street address

For a letter to arrive, the destination needs an address. Same for data.

An **IP address** is a unique number that identifies a computer on the internet, written
as four numbers separated by dots — something like `142.250.190.46`. Every device that's
online has one: your phone, your laptop, and every machine that serves websites. It's
the street address of the digital world.

(You'll find your own IP address in the lab. Yes, you have one right now.)

## ✉️ Packets: big messages travel as many small envelopes

Here's the first genuinely surprising design decision. The internet does not send your
message in one piece.

A **packet** is a small chunk of data with the destination address attached — the
internet cuts every message into packets and sends each one separately. A photo you
send might become hundreds of packets. Each packet carries the destination IP address,
the sender's address, and a number saying which piece of the message it is ("part 47 of
212").

> 🌉 **Analogy:** Imagine mailing a 200-page manuscript, but the postal service only
> accepts single-page letters. You'd mail 200 envelopes, each labeled "page 47 of 200",
> and your friend would reassemble the manuscript on arrival. Envelopes might arrive
> out of order — some might take different routes, and a lost one can be re-requested —
> but numbered pages make reassembly foolproof.
>
> **Where the analogy breaks down:** re-mailing a lost page would take days by post; on
> the internet, "that packet never arrived, send it again" happens automatically in
> milliseconds, thousands of times a day, without anyone noticing.

Why bother? Because small packets share the wires fairly (your video call and your
neighbor's movie interleave their envelopes instead of blocking each other), and because
losing one packet means resending one packet — not the whole photo.

## 🏤 Routers: the post offices in between

Your packet does not fly straight to its destination. It hops.

A **router** is a machine whose whole job is to look at each packet's destination
address and pass it one step closer — like a post office forwarding mail toward the
right city. Your home WiFi box is a small router. Between you and a distant website
there might be 10–20 of them: your router, your internet provider's routers, big
exchange points, the destination's routers. Each one reads the address and forwards.
No single router knows the whole path — each only knows a good next step. That
step-by-step relay is resilient: if one route is congested or broken, packets flow
around it, like mail rerouted past a flooded road.

> ✅ **Check yourself**
> 1. What are the two ingredients the lesson says make up the internet?
> 2. Why is a big photo cut into packets instead of sent whole?
> 3. What does a router do with a packet?
>
> <details><summary>Show answers</summary>
>
> 1. Wires (physical cables and radio links) and agreements (protocols — shared rules
>    for how machines talk).
> 2. Small chunks share the wires fairly with everyone else's traffic, and a lost chunk
>    can be resent alone instead of resending the whole photo.
> 3. Reads the destination address and forwards the packet one hop closer — a post
>    office passing mail toward the right city.
> </details>

## 📖 DNS: the phone book of the internet

There's a gap in the story so far. You typed `wikipedia.org` — a *name*. Packets need an
IP address — a *number*. Who translates?

**DNS** (the Domain Name System) is the internet's phone book: a worldwide service that
turns human-friendly names like `wikipedia.org` into IP addresses like `208.80.154.224`.
Before your device can request any website, it quietly asks DNS: "what number is
`wikipedia.org`?" — gets the number back — and *then* starts addressing envelopes.

This happens for every new site you visit, usually in a few hundredths of a second, and
you never see it. When DNS breaks (it happens!), the internet feels "down" even though
the wires are fine — like having a working phone but no phone book: everyone's still
reachable, you've lost the numbers.

## 🏪 Servers and clients: shops and customers

One more pair of words, and they'll follow you for the rest of this course.

A **server** is a computer that stays on all the time, waiting for requests from other
computers and answering them. A **client** is the computer that asks — your phone, your
laptop, your browser. Servers are shops that never close; clients are customers who
walk in and order.

Websites live on servers. When people say a website is "down", they mean its server
isn't answering. And to kill the fluffiest myth in tech early: **the "cloud" is
servers.** Rooms — warehouses — full of them, called **data centers**: buildings packed
with thousands of servers, with industrial cooling and backup power. Your "photos in
the cloud" are bytes in labeled boxes (Module 02!) on specific physical machines in
buildings with actual street addresses. More on this in Module 15.

## ⏱️ The 2-second journey: what happens when you visit a website

Let's put every character on stage at once. You type `wikipedia.org` and press Enter.
In roughly two seconds (usually less):

1. **Phone book (DNS).** Your browser asks DNS: "what's the IP address for
   `wikipedia.org`?" Answer: `208.80.154.224` (for example).
2. **Handshake.** Your device exchanges a few tiny packets with that server to agree
   they're both ready — like a phone call's "Hello?" "Hi, can you hear me?" before the
   real conversation.
3. **The request.** Your browser sends a small message: "please send me your main
   page." This travels as packets, hopping router to router.
4. **The server responds.** The server finds or builds the page and sends it back —
   as text describing the page's content and structure, cut into many packets.
5. **Reassembly.** Your device collects the packets, puts them in order, asks for any
   stragglers again, and hands the complete text to the browser.
6. **More requests — many more.** Reading the page text, the browser discovers it also
   needs images, fonts, styling, and scripts — each one a separate request. A typical
   page triggers *dozens* of these little journeys (you'll count them yourself in the
   lab).
7. **Drawing.** The browser turns it all into the glowing page you see.

All of that — a phone-book lookup, a handshake, and dozens of round trips, each hopping
through a dozen post offices — in the time it takes you to blink twice. *That's* the
miracle, and now you know its moving parts.

> ✅ **Check yourself**
> 1. What has to happen before your browser can even send its first request to a new
>    website?
> 2. Roughly how many requests does one ordinary web page trigger — one, a few, or
>    dozens?
> 3. Is your phone a client or a server?
>
> <details><summary>Show answers</summary>
>
> 1. A DNS lookup — translating the site's name into an IP address, because packets are
>    addressed by number, not by name.
> 2. Dozens — the page text, then each image, font, style file, and script as a
>    separate request.
> 3. A client — it asks; servers answer. (Nothing physically stops a phone from acting
>    as a server, but in daily life your devices are customers, not shops.)
> </details>

## 🔒 HTTP, HTTPS, and the padlock

Two acronyms you see every day, decoded. **HTTP** is the protocol — the agreed etiquette
— that browsers and web servers use to request and deliver pages ("please send me this
page" / "here it is"). It's the reason any browser can talk to any website: shared
rules.

Plain HTTP has a flaw: it sends everything like a **postcard** — any post office
(router) along the way could read the contents. **HTTPS** is HTTP with encryption
added: the contents are scrambled so that only your device and the server can read
them — a sealed, tamper-proof envelope instead of a postcard. The padlock icon in your
browser's address bar means HTTPS is on.

Worth being precise about what the seal protects: with HTTPS, someone watching the
wires can still see *where* you sent mail (which website you connected to) — envelopes
need a readable address to be deliverable — but not *what's inside* (the pages you
read, the password you typed, the card number you entered).

> ⚠️ **Watch out:** the padlock means "sealed envelope", not "trustworthy recipient".
> A scam website can use HTTPS too — then your data travels securely straight to a
> scammer. The padlock protects the *journey*, not the *destination*. (Much more on
> this in Module 14.)

## 🌊 WiFi, mobile data, and the ocean floor

How does your device reach the first post office? Three on-ramps, same highway:

| Connection | What it is | Postal twin |
|---|---|---|
| **Cable** | a physical wire into your device or home | mail truck to your door |
| **WiFi** | short-range radio to a router in the building | tossing letters to the mailbox across the room |
| **Mobile data** | longer-range radio to a cell tower | handing mail to a courier on the street |

Here's the part almost nobody knows: whichever on-ramp you use, long-distance traffic
travels through physical cables — and between continents, those cables lie **on the
ocean floor**. Hundreds of submarine cables, each roughly the thickness of a garden
hose, carry almost all intercontinental internet traffic (satellites carry only a small
fraction). Ships lay them; when one breaks, a repair ship goes and fishes it up. When
you message someone overseas, your words genuinely travel under the sea. The cloud is
not in the sky. **The cloud is under the ocean** — and in those data-center warehouses.

## 🐢 Why pages load slowly sometimes

With the whole picture assembled, slowness stops being mysterious. Any leg of the
journey can drag:

- **Weak radio:** your WiFi or mobile signal is poor, so packets are lost near you and
  must be resent (the most common culprit).
- **Distance:** the server is far away, and even light in a cable takes noticeable
  time to cross an ocean — twice, for every request and reply.
- **Crowds:** a busy server answers slowly, like one barista facing fifty customers.
- **Congestion:** a router along the path is overloaded and packets queue up, like
  mail before a holiday.
- **Heavy pages:** the page itself triggers a hundred requests for huge images —
  many trips, big parcels.

Next time a page crawls, you can diagnose it like an engineer instead of glaring at it
like a curse.

## 🎯 Recap

- The internet = **wires + agreements**. A **protocol** is a shared rulebook, like
  postal etiquette.
- Every online device has an **IP address** (street address). Messages travel as
  **packets** (numbered envelopes) that may arrive out of order and get reassembled.
- **Routers** are post offices, forwarding each packet one hop closer. **DNS** is the
  phone book turning names into numbers. **Servers** are always-open shops; **clients**
  (your devices) are the customers.
- Visiting a website = DNS lookup → handshake → request → response in packets →
  reassembly → dozens more requests → drawing. All in about two seconds.
- **HTTPS** = sealed envelopes: watchers can see *where* your mail goes, not *what's
  inside*. The padlock protects the journey, not the destination.
- WiFi and mobile data are radio on-ramps to the same wired highway — including
  **undersea cables**. Websites physically live on servers in **data centers**.

## 🚀 Next up

That completes Part 1 — The Machine. You now know what a computer is, what software is,
and how machines talk across the planet. In Part 2, you switch from spectator to
player: how do you break a problem into steps so literal that even a computer can
follow them? That skill is the real heart of programming, and it starts in
[Module 04: How to Think Like a Programmer](../04-think-like-a-programmer/README.md).

*Before you go: the [lab](lab.md) lets you watch the postal system in action from your
own browser — including counting a page's dozens of requests yourself. Then the
[quiz](quiz.md), and the [extra resources](resources.md) (one is a live map of the
undersea cables).*
