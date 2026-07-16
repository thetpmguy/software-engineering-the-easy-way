# ✅ Quiz 03 — How the Internet Works

> Think first, then open the fold. If several answers surprise you, reread the matching
> section of the [lesson](README.md) — the postal analogy carries every one of these.

---

**1. The lesson defines the internet in four words. What are they, and what does each
half mean?**

<details><summary>Show answer</summary>

"Wires and agreements." The wires are the physical part — fiber cables under streets
and oceans, plus radio links like WiFi. The agreements are **protocols**: shared rules
for how machines address and pass messages, which let billions of machines from
thousands of companies cooperate without knowing each other.
</details>

**2. What is an IP address, and what's its postal twin?**

<details><summary>Show answer</summary>

A unique number identifying a computer on the internet (like `142.250.190.46`) — the
street address of the digital world. Every online device has one, including your phone
right now.
</details>

**3. Your friend sends you a large photo. Describe its trip in packet terms.**

<details><summary>Show answer</summary>

The photo is cut into hundreds of **packets** — numbered envelopes, each carrying the
destination address and "part X of Y". They travel separately, may take different
routes, and may arrive out of order. Your device reassembles them by number and
automatically re-requests any that went missing.
</details>

**4. Why does the internet bother cutting messages into packets at all?**

<details><summary>Show answer</summary>

Two reasons: fairness — small chunks let everyone's traffic interleave on shared wires,
so one big download doesn't block the road; and resilience — a lost packet means
resending one small piece, not the whole message.
</details>

**5. What is a router? Does any single router know the full path to the destination?**

<details><summary>Show answer</summary>

A machine that reads each packet's destination address and forwards it one hop closer —
a post office in the relay. No — each router only knows a good *next step*. The
step-by-step relay is what makes the network resilient: traffic flows around broken or
congested routes like mail past a flooded road.
</details>

**6. What is DNS, and what would the internet feel like if it stopped working?**

<details><summary>Show answer</summary>

DNS is the internet's phone book — the worldwide service that translates names
(`wikipedia.org`) into IP addresses (`208.80.154.224`). If it broke, the internet would
feel "down" even with every wire intact: sites still exist and are reachable by number,
but nothing can be found by name — a working phone with no phone book.
</details>

**7. Server vs client — define both, and say which one your phone is.**

<details><summary>Show answer</summary>

A **server** is a computer that stays on all the time, waiting to answer requests — a
shop that never closes. A **client** is the computer that asks — the customer. Your
phone is a client. Websites live on servers, physically located in **data centers**
(warehouses full of servers).
</details>

**8. Put these steps of visiting a website in order: reassembly · DNS lookup · server
responds · browser sends request · handshake · dozens more requests · browser draws
the page.**

<details><summary>Show answer</summary>

DNS lookup → handshake → browser sends request → server responds (in packets) →
reassembly → dozens more requests (images, fonts, styles, scripts) → browser draws the
page. Total time: usually under two seconds.
</details>

**9. With HTTPS on (padlock showing), what can someone watching the network see, and
what can't they see?**

<details><summary>Show answer</summary>

They can see *where* your traffic goes — which site you connected to — because
envelopes need a readable delivery address. They cannot see *what's inside*: the pages
you read, the passwords and card numbers you typed. Sealed envelope, visible address.
</details>

**10. True or false: the padlock icon means a website is trustworthy.**

<details><summary>Show answer</summary>

False — and this one matters for your safety. The padlock means the *connection* is
encrypted: a sealed envelope for the journey. A scam site can have a padlock too; then
your data travels securely straight to a scammer. The padlock protects the journey,
never the destination.
</details>

**11. Your cousin says "the cloud" means data floating in space via satellites. Set
them straight in two sentences.**

<details><summary>Show answer</summary>

The cloud is physical: your "cloud" files sit on servers in data-center buildings with
street addresses. And between continents, traffic travels overwhelmingly through
cables on the ocean floor — hose-thick, laid and repaired by ships — with satellites
carrying only a small fraction.
</details>

**12. A page is loading painfully slowly. Name three different places along the journey
the delay could be.**

<details><summary>Show answer</summary>

Any three of: weak WiFi/mobile signal losing packets near you; a distant server (ocean
crossings twice per request); an overloaded server answering slowly; a congested
router queueing packets along the path; or a heavy page making a hundred requests for
huge images. Slowness is a diagnosis now, not a mystery.
</details>

**13. 🗣️ Explain it to a friend.** A friend asks: *"Seriously, what happens when I type
a website name and hit Enter?"* Tell the two-second journey out loud, in under two
minutes, using the postal analogy — phone book, envelopes, post offices, sealed
envelopes. If they follow the whole trip, you've mastered Part 1 of this course.

<details><summary>Stuck? Here's one way to start</summary>

"Your phone first checks the internet's phone book — DNS — to turn the name into a
number, because machines address everything by number. Then it mails a request to that
number: the message gets cut into little numbered envelopes that hop between post
offices called routers, maybe a dozen of them, possibly through a cable on the ocean
floor. The server — a computer that never sleeps — mails the page back the same way,
your phone reassembles the envelopes, notices it still needs the pictures and fonts,
sends off dozens more requests, and draws the page. All in about two seconds. And the
padlock means every envelope was sealed…"
</details>

---

*That's Part 1 complete! Onward to
[Module 04: How to Think Like a Programmer](../04-think-like-a-programmer/README.md),
or linger in the [extra resources](resources.md) — the undersea cable map is worth it.*
