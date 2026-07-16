# ✅ Quiz 13 — Operating Systems & Networks

Answer first, then peek. If a question stumps you, the section heading it echoes is
the place to re-read.

---

**1. Your phone appears to run 50 things at once on a handful of processor cores.
What's the trick, and what is it called?**

<details><summary>Show answer</summary>

The OS switches each core between programs thousands of times per second — one chef
tending fifty pans so quickly that every pan seems to have a private chef. The trick
is called scheduling.
</details>

**2. Why doesn't one crashed app take the whole phone down with it?**

<details><summary>Show answer</summary>

Every app runs in its own process — a sealed workspace with its own walled-off
memory. The crash cannot reach other processes, and the OS can evict the broken one
alone (that's what force quit is).
</details>

**3. Your computer gets slow and the disk churns whenever too many programs are
open. Using the hotel analogy, what's happening?**

<details><summary>Show answer</summary>

The guests have outnumbered the rooms: RAM is full, so the OS moves some processes'
memory to swap — overflow storage in the basement (the disk). Every retrieval from
the basement is far slower than from a room, which is the sluggishness you feel.
</details>

**4. A flashlight app asks to access your contacts. Why does it have to ask — and
what should you think?**

<details><summary>Show answer</summary>

Apps can't touch hardware or data directly; everything goes through the OS, which
checks its permission list first — the manager checking the guest list. And you
should think like the manager: a flashlight has no business reading contacts, so
the answer is no.
</details>

**5. What is the kernel, in one sentence?**

<details><summary>Show answer</summary>

The innermost core of the operating system — the manager's inner office — with total
authority over the processor, memory, and hardware.
</details>

**6. Your laptop's address is 192.168.1.23 and so is your neighbor's laptop's.
Why is that not a problem, and what does the router do so the internet can still
reply to each of you correctly?**

<details><summary>Show answer</summary>

Local IPs are apartment numbers — meaningful only inside each building, so two homes
can reuse them. Each home shares one public IP (the street address). The router
performs NAT: it rewrites outgoing traffic to use the public address and keeps a
ledger of which conversation belongs to which device, so replies get sorted back to
the right apartment.
</details>

**7. What is a port? Which port does secure web traffic (HTTPS) use?**

<details><summary>Show answer</summary>

A numbered door on one address, so traffic reaches the right *program* on a device —
not only the right device. Secure web traffic knocks on door 443.
</details>

**8. Your friend says "I got a VPN, so now nobody can see what I do online."
What's accurate in that, and what's the honest correction?**

<details><summary>Show answer</summary>

Accurate: their internet provider (and anyone on the local WiFi) now sees only an
encrypted tunnel, not the sites they visit — genuinely useful on untrusted networks.
Correction: the VPN company's servers unwrap that tunnel to forward the traffic, so
the VPN company can see what the ISP no longer can. A VPN moves your trust to a
different party; it isn't invisibility.
</details>

**9. Latency vs. bandwidth: define each with the courier analogy, and explain why
video calls can stutter on a connection where huge downloads run perfectly.**

<details><summary>Show answer</summary>

Latency is the bike courier — how quickly one small message makes the round trip
(milliseconds). Bandwidth is the truck — how much data flows per second (Mbps).
Downloads are truck work: massive cargo, no urgency per box. Live calls are courier
work: tiny packets that must arrive right now, in rhythm — every late courier is a
frozen frame. A connection can have a great truck and unreliable couriers at once.
</details>

**10. "The WiFi is down!" Give the four-step checklist for finding which manager
actually failed.**

<details><summary>Show answer</summary>

(1) Do other apps/sites work? → one service's backend is down, not your network.
(2) Do other devices in the house work? → if only one device fails, restart that
device (its OS gets a clean shift). (3) Everything failing? → restart the router
(the mailroom gets a clean shift). (4) Still down? → the problem is your internet
provider's line, beyond your walls — call them, with your evidence.
</details>

**11. What is a driver, and why does "update the driver" so often fix a printer?**

<details><summary>Show answer</summary>

A small program that translates between the OS and one specific piece of hardware —
an interpreter for that gadget's dialect. Printers misbehave when the interpreter
mistranslates; an updated driver is an interpreter with corrected vocabulary.
</details>

**12. 🗣️ Explain it to a friend.** A family member asks: "Why does restarting the
router fix the internet so often?" Explain in under a minute, using the managers
from this module.

<details><summary>One possible answer</summary>

"The router is a little computer — your home's mailroom — running its own manager
that juggles thousands of letters a second and keeps a ledger of every ongoing
conversation. Over weeks, that ledger and its memory fill with clutter and the odd
stuck entry, and the manager starts misdelivering. Restarting doesn't repair
anything — it gives the manager a totally clean shift: empty ledger, fresh memory,
every conversation renegotiated from scratch. Same reason restarting a phone works.
And if the internet is still down after a clean shift, you've learned something
too: the problem is beyond your building, at the provider."
</details>
