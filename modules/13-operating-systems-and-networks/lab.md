# 🔧 Lab 13 — Meet Your Two Managers in Person

> **Goal:** watch your OS juggle real processes, take a safari to your router's admin
> page, count the devices in your home, and measure your connection like an engineer.
>
> **Time:** 40–60 minutes. Everything uses equipment you already own.

---

## 👀 Lab 1 — Watch the manager work (processes & memory)

Open your device's built-in window into the OS:

- **Windows:** press `Ctrl + Shift + Esc` to open **Task Manager**. Click "More
  details" if you see a small view.
- **Mac:** open **Activity Monitor** (press `Cmd + Space`, type "Activity Monitor",
  press Enter).
- **Android:** Settings → "Battery" and Settings → "Apps" (device memory screens
  vary; battery usage lists are the closest view).
- **iPhone:** Settings → Battery (iOS hides its process list — the battery list
  shows who's been using the chef's time).

Now explore:

1. **Identify 5 processes you recognize** — your browser, a chat app, maybe the
   music player. On a computer you'll also see dozens of strangers with odd names:
   those are the hotel staff — OS services doing background chores. Don't touch,
   don't worry.
2. **Find the memory hog.** Sort by the Memory column (click its header). Which
   process holds the most rooms? On most machines, the browser wins by a landslide —
   each tab is roughly its own sealed kitchen.
3. **Watch scheduling live.** Sort by CPU and watch the percentages flicker and
   reorder every second. That flicker *is* the chef switching pans.
4. **Safely force-quit something.** Open a program you don't need (a calculator, a
   notes app), find it in the list, and end it — "End task" (Windows), the ⓧ button
   (Mac), or swipe it away (phone). That was an eviction: the manager reclaimed the
   rooms.

> ⚠️ **Watch out:** only force-quit apps *you* opened and recognize. Ending an OS
> service can freeze or restart the machine. (It recovers — but let's not.)

**✅ What you should see:** far more processes than open windows; a memory column
dominated by your browser; CPU numbers dancing; and one calculator, evicted.

## 🧭 Lab 2 — Home router safari

Time to visit the mailroom. You'll look at your router's admin page — the little
website the router itself serves inside your home.

1. **Find the router** physically. On its label, look for: the admin address (often
   `192.168.1.1` or `192.168.0.1`), the WiFi name, and a default admin password.
2. On a device connected to your WiFi, type that address into the browser's address
   bar. A login page appears — this page comes from the box in your corner, not the
   internet.
3. Log in with the label's admin credentials (or ask whoever set up the router). No
   luck? Search the web for "*your router's brand* admin page" — but never install
   anything to do this.

> ⚠️ **Watch out — the safari rules:** you are here to *look, not touch*. Router
> settings can knock the whole house offline. Change nothing... with **one
> recommended exception**: if the admin password is still the factory default
> (like "admin"), change it to something long and write it on the router's label in
> pen. A default password means anyone on your WiFi can reconfigure the mailroom.

4. Wander (looking only): find the list of **connected devices**, the WiFi settings,
   and — if your router shows it — your **public IP address**. Compare it with the
   local addresses in the device list: street address vs. apartment numbers, exactly
   as in the lesson.

**✅ What you should see:** a device list with each gadget's local IP (`192.168.x.x`
style apartment numbers), and one public IP for the whole household. You've just read
NAT's ledger.

## 🔢 Lab 3 — The device census

From that connected-devices page:

1. **Count the devices.** Phones, laptops, TV, printer, doorbell, robot vacuum...
   most households guess low by 3 or more.
2. **Name every entry.** Anything you can't identify? Usually it's a gadget with a
   cryptic name (TVs and smart plugs are notorious). Compare the listed name against
   each device's Settings → About → local IP until it's accounted for.
3. If something genuinely isn't yours, changing the WiFi password evicts everyone —
   and only devices given the new password return. (That's a change beyond today's
   look-only rule; note it for later if needed.)

**✅ What you should see:** a complete census, every device accounted for — and a
new reflex: *the mailroom knows exactly who lives in the building.*

## 🚴 Lab 4 — Bike courier vs. truck (speed test)

1. Visit **[speedtest.net](https://www.speedtest.net)** or **[fast.com](https://fast.com)**
   in a browser. Run the test. (On fast.com, click "Show more info" to reveal
   latency.)
2. Record three numbers:
   - **Download bandwidth** (Mbps) — your truck's cargo capacity.
   - **Upload bandwidth** (Mbps) — the truck heading *out*; usually smaller.
   - **Latency / ping** (ms) — your bike courier's round-trip time.
3. Interpret with the lesson's rules of thumb: latency under ~30 ms is a swift
   courier (calls feel natural); 30–80 ms is fine; well past 100 ms, video calls
   start talking over each other — regardless of how big the truck is.
4. **Experiment:** run the test twice more — once right beside the router, once as
   far away as your home allows. Then, if you can, once while someone streams video.

**✅ What you should see:** distance from the router usually hurts bandwidth
noticeably; a busy network can raise latency. And you now know whether call trouble
at your home is a courier problem or a truck problem — which is exactly what your
internet provider's support line will want to hear.

---

## 🎉 Done!

You've watched scheduling flicker in real time, performed a lawful eviction, read
your mailroom's ledger, taken a census of your building, and measured your couriers
and trucks. Both invisible managers are now visible. On to the [quiz](quiz.md).
