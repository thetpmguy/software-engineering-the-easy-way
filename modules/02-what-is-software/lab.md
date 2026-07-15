# 🔧 Lab 02 — Software Safari

> **Goal:** spot every layer of software on your own device — the OS, the apps, the
> files — and then look at real, professional code on the internet with your own eyes.
>
> **You need:** your phone or laptop and a web browser. Nothing to install, no account
> needed. We are only looking and making one harmless note file.

---

## Part 1 — Identify your operating system (5 minutes)

Every device has exactly one hotel manager. Let's find yours, and its version number.

1. **iPhone/iPad:** Settings → General → About → look for **iOS Version** (e.g. "17.5").
2. **Android:** Settings → About phone → look for **Android version** (e.g. "14").
3. **Windows:** Start → Settings → System → About → look under "Windows specifications"
   (e.g. "Windows 11").
4. **Mac:** Apple menu () → About This Mac → the name and number (e.g. "macOS
   Sonoma 14.4").

Write down the OS name and version.

> **✅ What you should see:** a name and a version number. The number matters: it tells
> you which edition of the "hotel management handbook" your device runs. When your
> device says "update available", it's offering to replace this exact software with a
> newer edition — same hardware, new manager.

## Part 2 — Take an app census (10 minutes)

1. Look at your device's home screen or app list and pick **five apps** you actually use.
2. For each one, write a line with three things: its **name**, what **kind** of app it
   is in plain words, and one thing it must ask the OS for.

Example census:

| App | Kind | Something it must ask the OS for |
|---|---|---|
| WhatsApp | messaging | the network, to send messages; the microphone, for voice notes |
| Google Maps | navigation | your location; the network |
| Camera | photo-taking | the camera hardware; storage, to save photos |
| Spotify | music player | the speaker; the network |
| Calculator | tiny tool | almost nothing — the screen and your taps |

3. Bonus: on your phone, open Settings and find **Permissions** or **Privacy** (both
   Android and iOS have it). Pick one app and see the list of things it's *allowed* to
   ask the OS for. That permissions screen is the hotel manager's guest rulebook, made
   visible.

> **✅ What you should see:** five very different apps that all depend on the same OS
> for hardware access. Notice the pattern from the lesson: apps ask, the OS provides.

## Part 3 — Make a file and read its label (10 minutes)

Time to create a labeled box of bytes yourself.

### On a laptop (Windows or Mac)

1. **Windows:** right-click on the Desktop → New → **Text Document**. Name it
   `hello.txt`. **Mac:** open the **TextEdit** app, choose Format → **Make Plain
   Text**, then save the file as `hello` (it becomes `hello.txt`).
2. Open your file and type a sentence, e.g. `This file is a labeled box of bytes.`
   Save it.
3. Now look at the file's size: right-click → **Properties** (Windows) or **Get Info**
   (Mac). It will show something like "37 bytes".
4. Count the characters in your sentence, including spaces. Compare with the byte
   count.

### On a phone

1. Open your notes app — or better, a files app (**Files** on iPhone, **Files by
   Google** or **My Files** on Android).
2. In the files app, look at any document and check its details (long-press → info on
   most phones). Find the **size in bytes/KB** and, where shown, the extension.
3. If your phone's files app allows "New file" or lets you save a note "as .txt", make
   a `hello.txt` with one sentence in it.

> **✅ What you should see (laptop version):** the byte count roughly *equals* the
> character count — because in a plain text file, each letter is stored as one byte,
> exactly as Module 01's binary table showed. You typed 37 characters; the box contains
> about 37 bytes. That's the least magical, most satisfying arithmetic in computing.

> ⚠️ **Watch out:** Windows hides extensions by default, which is why many people have
> never seen `.txt` or `.jpg` on their own files. To reveal them: open any folder,
> click the **View** menu, and tick **File name extensions**. The labels were there all
> along.

## Part 4 — See real software in the wild (15 minutes)

The lesson claimed: *software is text files written by people.* Don't take our word for
it. Let's look at the single most famous open-source project on Earth — Linux, the OS
running most of the internet — in its actual home.

1. In your browser, go to **github.com** (no account needed for looking).
2. In the search bar at the top, type `torvalds/linux` and open the result. This is the
   real Linux code repository, started by Linus Torvalds in 1991 and now worked on by
   thousands of people.
3. Look at the page. You should see a list of folders and files with names like
   `kernel`, `drivers`, `mm` — this is the filing cabinet of one of the most important
   programs ever written.
4. Click the file called **README** and read the first few lines. It's a plain-English
   note from the developers to anyone visiting — proof that even legendary software
   ships with a welcome note written by a human.
5. That's it — don't feel obliged to open the code files themselves yet. The point of
   this safari is only to *see* the habitat: software is folders of text files, written
   and signed by people, sitting in public where anyone can read them.
6. Optional detour: click "commits" (a number near the top of the file list). You'll
   see a feed of individual changes — each one a small edit by a named person, with a
   one-line description. Software is edited the way a shared document is edited.

> **✅ What you should see:** a folder listing, a README greeting you in plain English,
> and (optionally) a stream of human-made changes. If Linux felt like an untouchable
> monument before, it should now feel like what it is: a very large community cookbook.

## 🎉 Done!

You identified your hotel manager, took a census of its guests, built a labeled box of
bytes and verified its size byte-for-letter, and visited real world-class source code
in its natural habitat. Next: [the quiz](quiz.md), then
[Module 03](../03-how-the-internet-works/README.md).
