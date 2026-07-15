# ✅ Quiz 15 — The Cloud

Answer in your head or on paper, then open each fold to check. No grades, no timer —
this is a mirror, not a judge.

---

**1. Your friend says: "I don't trust the cloud — I keep my photos somewhere real."
What's the kindest correction?**

<details><summary>Show answer</summary>

The cloud *is* somewhere real. It's other people's computers in data centers —
warehouse-sized buildings full of machines. Their photos, if backed up, sit on a
specific metal box in a specific building (usually copied across three buildings). The
cloud isn't less real than their phone; it's more buildings.
</details>

**2. Why are data centers often built near hydroelectric dams and in cool climates?**

<details><summary>Show answer</summary>

Electricity and cooling are a data center's two biggest hungers. Thousands of computers
draw enormous power (cheap electricity matters) and give off serious heat (cool air and
water for cooling matter). Cheap power plus free cold = ideal neighborhood.
</details>

**3. The lesson compared the cloud to the electricity grid. What's the key point of
that analogy — and where does it break down?**

<details><summary>Show answer</summary>

The point: nobody runs a generator at home; you plug into the grid and pay for what you
use. Same with computing — renting from a specialist beats owning your own machines.
The breakdown: electricity is identical everywhere, but each cloud provider's tools are
different and incompatible, which is how lock-in happens.
</details>

**4. Match the rental level to the kitchen: (a) renting bare computers, (b) renting a
managed platform, (c) renting finished software.**

<details><summary>Show answer</summary>

(a) Bare computers = the empty rented kitchen — you cook and clean everything (IaaS).
(b) Managed platform = kitchen with staff who clean and restock — you only bring your
recipe/code (PaaS). (c) Finished software = ordering the pizza — you don't cook at all
(SaaS: Gmail, Netflix, Google Docs).
</details>

**5. An online shop needs 10 computers on a normal day and 1,000 on Black Friday. Why
was this problem nearly unsolvable before the cloud?**

<details><summary>Show answer</summary>

With owned hardware you'd either buy 1,000 machines that sit idle 364 days a year
(ruinously wasteful) or keep 10 and crash on your most profitable day. The cloud lets
you rent 990 extra machines for one weekend and return them Monday — paying only for
what you used. That on-demand growing and shrinking is called scaling.
</details>

**6. What is redundancy, and why does it mean a flooded data center doesn't lose your
photos?**

<details><summary>Show answer</summary>

Redundancy is keeping spare copies so no single failure can hurt you — cloud providers
typically store three copies of your data in three different cities. If one building
floods, the other two copies take over so quickly you never notice.
</details>

**7. True or false: "serverless" computing has no servers. Explain.**

<details><summary>Show answer</summary>

False — there are always servers. "Serverless" means *you* never think about them: you
hand over code, the cloud finds a machine, runs it, and bills you per use. Like taxis:
cars are obviously involved, but you never buy, park, or maintain one.
</details>

**8. Your video call to a colleague on another continent has a slight delay, even with
perfect internet. What is that delay called, and what causes it?**

<details><summary>Show answer</summary>

Latency — the waiting time between sending and receiving. Its floor is physics: the
signal physically travels through cables (often under the ocean), and even at nearly the
speed of light, crossing the planet takes real milliseconds. Distance becomes waiting.
</details>

**9. What does a CDN do, and what's the supermarket version of the idea?**

<details><summary>Show answer</summary>

A CDN (content delivery network) keeps copies of popular files in small storage outposts
in hundreds of cities, close to viewers. It's the supermarket-chain trick: keep a
warehouse near every big town instead of shipping every yogurt from one national depot.
That's why Netflix rarely stutters.
</details>

**10. Why is "cloud cost engineer" a real job?**

<details><summary>Show answer</summary>

Because the cloud meter never stops. Every running machine bills by the hour, and
forgotten machines are taps left running — companies routinely waste thousands per month
on computers doing nothing. Someone whose whole job is finding and turning off those
taps can save more than their own salary many times over.
</details>

**11. Name two honest downsides of the cloud and give the one-line version of each.**

<details><summary>Show answer</summary>

Any two of: **Lock-in** — each provider's custom tools make moving out as painful as
leaving an apartment with built-in furniture. **Outages** — with most of the internet
renting from three landlords, one landlord's bad day breaks half the web at once.
**Privacy/sovereignty** — your data in another company's (or country's) building raises
real legal questions. **Environment** — data centers consume country-sized amounts of
electricity and real water, even as providers race toward renewables.
</details>

**12. 🗣️ Explain it to a friend.** Your cousin says: "My phone says my photos are in
the cloud. What does that even mean? Is it safe?" Give them a two-minute answer, out
loud or in writing, using at least one analogy from this module. Cover: what the cloud
physically is, why their photos probably exist in three cities, and one honest caveat.

<details><summary>Show a sample answer (read only after trying!)</summary>

"The cloud is a marketing word for other people's computers. Your photos got copied to a
warehouse full of computers owned by Apple or Google — a real building with a real
address, cooled like a giant fridge. It's like plugging into the electricity grid
instead of running a generator at home: they're specialists, so it's cheaper and more
reliable than doing it yourself. Safer than your phone alone, honestly — they keep three
copies in three different cities, so even if one building floods, your photos survive.
Your phone in the ocean loses everything; the cloud shrugs off a flood. The honest
caveat: your photos are on someone else's property, under whatever laws apply where that
building stands — so 'safe from loss' is nearly certain, while 'private forever' depends
on the company and the country."
</details>
