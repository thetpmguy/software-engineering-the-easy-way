# 🔧 Lab 15 — Touch the Cloud (Without Buying Anything)

> **Goal:** prove to yourself that "the cloud" is real, physical, and already woven
> through your daily life. Everything below runs in a web browser — phone or laptop, no
> installs, no sign-ups, and **absolutely no purchases**.
>
> **Time:** 45–60 minutes. Do the parts in any order.

---

## Part 1 — Trace your own cloud life (10 minutes)

You've been a cloud customer for years. Let's prove it.

1. Grab paper or open a notes app.
2. List **10 apps or services you used this week**. Anything counts: email, maps, music,
   banking, photos, messaging, video, shopping.
3. For each one, ask: *"Is the real work and storage happening on my device, or on
   someone else's computers?"* A quick test: **if you logged in on a friend's phone,
   would your stuff be there?** If yes, it lives in the cloud — that service is finished
   rented software (SaaS, from the lesson).
4. Mark each app: ☁️ for cloud, 📱 for "lives only on my device."

**What you should see:** almost every mark is ☁️. Maybe your calculator and camera are
📱 — and even your camera probably backs up to the cloud. Spoiler fulfilled: you didn't
"start using the cloud" today. You've been living in it.

## Part 2 — Find where your data physically lives (10 minutes)

Your photos have a street address. Let's get close to finding it.

1. In a search engine, type your email or photo provider's name plus "data center
   locations" — for example, **"Google data center locations"** or **"Microsoft Azure
   regions"** or **"Apple data centers"**.
2. Open the company's *official* page (Google and Microsoft both publish maps of their
   data center sites).
3. Write down the **three locations nearest to you**. One of them very likely holds a
   copy of your email.

**What you should see:** a real map with pins in real towns — places like Dublin,
Council Bluffs (Iowa), Eemshaven (Netherlands), or Jurong West (Singapore). Notice how
many sit in cool climates or near rivers and dams. Now you know why.

## Part 3 — Take the data center tour (10 minutes)

1. Go to YouTube and search **"Google data center tour"**.
2. Watch Google's official tour video (there are a few — any official one works).
3. While watching, spot and note: **(a)** the security layers at the entrance, **(b)**
   the cooling system, **(c)** what happens to old hard drives.

**What you should see:** aisles of servers like supermarket shelves, serious cooling
pipes, and — most people's favorite part — old drives being physically shredded so no
data can ever be recovered. That's redundancy's quieter sibling: careful destruction.

## Part 4 — Feel latency with your own hands (10 minutes)

The lesson claimed distance becomes waiting time. Let's measure it.

1. Search for an online latency test — try **"cloud ping test"** or search for
   "AWS latency test" / "Azure latency test". Several free browser tools will measure
   your delay to cloud regions around the world. (If one tool looks confusing, pick
   another — they all do the same thing.)
2. Let it run. It sends tiny messages to data centers on different continents and times
   the round trip in **milliseconds (ms)** — thousandths of a second.
3. Record the times for: the region **nearest you**, one in **North America**, one in
   **Europe**, one in **Asia or Australia**.

**What you should see:** something like — nearest region: 10–40 ms; same continent:
40–100 ms; other side of the planet: 150–300 ms. Now sort your numbers by distance.
They'll line up almost perfectly. You have personally measured the speed-of-light tax,
and you now know *exactly* why Netflix keeps a copy of your show near your house.

## Part 5 — Price a pretend server (15 minutes)

Let's window-shop at the world's biggest computer landlord. **No account needed, nothing
to buy — we are only looking at the menu.**

1. Go to **calculator.aws** (the official AWS pricing calculator).
2. Choose **Create estimate**.
3. In the service search box, type **EC2** — that's AWS's name for renting a plain
   computer — and select it.
4. Pick any region near you. For the machine size, find a **small** option (names look
   like `t3.small` — cryptic, but you're a menu-reader now, not a buyer).
5. Set it to run **24 hours a day, all month**, and look at the monthly total.
6. Now the fun part: change things and watch the meter. Try a giant machine (names with
   `xlarge`). Try 10 machines. Try running only 8 hours a day.

**What you should see:** a small machine costs roughly the price of a few coffees per
month. A monster machine can cost more than a car payment. And cutting the hours cuts
the bill — the meter really does only run while the tap is open.

> ⚠️ **Watch out:** the calculator is safe — it's a menu, not a checkout. But if you ever
> create a real cloud account, remember this lab: machines left running keep billing,
> forever. Now you've seen the meter with your own eyes.

---

## ✅ Lab complete — what you proved

- Nearly your whole digital life is rented cloud software.
- Your data lives in real buildings you can point to on a map.
- Distance = milliseconds. You measured it.
- Renting a computer costs pocket money — or a fortune — and the difference is a
  drop-down menu. That's why "cloud cost engineer" is a job.
