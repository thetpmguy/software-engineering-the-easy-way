# 🌐 Capstone Track A — Ship Your Corner of the Internet

> **The mission:** build and publish a real, multi-page personal website — live on the
> internet, at a URL with your name in it, built and versioned like a professional.
>
> **You'll need:** your free GitHub account (Module 08), any web browser, and 10–20
> hours over 2–4 weeks. No installation — you'll edit files right on GitHub, exactly
> like the [Module 08 lab](../modules/08-git-and-github/lab.md). This track is that
> lab, grown up.

**A promise before we start:** every line of code below is explained. You will not
paste anything you don't understand.

---

## Milestone 1 — Plan like Module 07 (1–2 hours)

No code yet. Professionals plan first, and so do you.

1. **Write 3 user stories** for your site. Yes, a personal site has users! Examples:
   - *As a **potential employer**, I want **to see what this person has built**, so
     that **I can judge their skills from evidence**.*
   - *As a **friend or family member**, I want **to understand what they've been
     learning**, so that **I can cheer them on**.*
   - *As **the site's owner**, I want **a page I'm proud to link**, so that **my
     applications stand out**.*
   Write your own three — they decide what pages you need.
2. **Sketch a paper wireframe** for two pages: the home page and the about page. Boxes
   and lines, five minutes each (Module 07 lab rules: a box with an X is a photo,
   label every link).

**✅ Checkpoint:** three user stories and two sketches. Every decision below traces back
to these.

## Milestone 2 — Build `index.html` (2–3 hours)

1. On GitHub, create a **new public repository** named `yourusername.github.io` —
   exactly that, with your real username. This magic name is how GitHub Pages knows to
   publish it (Module 08 lab, remember?).
2. Tick **Add a README file**, create the repository.
3. Click **Add file → Create new file**, name it `index.html` (`index` is the
   universal name for "the front page").
4. Type in the starter below — typing beats pasting for learning, but pasting is
   allowed. **Change every line marked 👈 to be about you.**

```html
<!DOCTYPE html>                                <!-- Tells the browser: this is modern HTML -->
<html lang="en">                               <!-- The whole page lives inside this tag -->
<head>                                         <!-- The "backstage" area: info ABOUT the page -->
  <title>Jane Doe</title>                      <!-- 👈 The browser-tab text. Your name here -->
  <meta charset="utf-8">                       <!-- Lets the page show any character, ñ to 中 -->
  <meta name="viewport"
        content="width=device-width, initial-scale=1"> <!-- Makes phones show it at phone size -->
  <link rel="stylesheet" href="style.css">     <!-- "Also load my styling file" (Milestone 3) -->
</head>
<body>                                         <!-- The visible part starts here -->

  <nav>                                        <!-- Navigation: the site's signpost -->
    <a href="index.html">Home</a>              <!-- A link back to this very page -->
    <a href="about.html">About</a>             <!-- A link to the page you'll build in Milestone 4 -->
  </nav>

  <main>                                       <!-- The main content of this page -->
    <h1>Hi, I'm Jane 👋</h1>                   <!-- 👈 h1 = the page's one big headline -->
    <p>Former nurse, learning software
       engineering in public.</p>              <!-- 👈 p = a paragraph. Your one-liner -->

    <h2>What I've built</h2>                   <!-- h2 = a smaller section headline -->
    <ul>                                       <!-- ul = a bulleted list ("unordered list") -->
      <li>This website — hand-written HTML,
          published with GitHub Pages</li>     <!-- li = one bullet ("list item") -->
      <li>A Python expense splitter</li>       <!-- 👈 Swap in your real projects, or dreams -->
    </ul>

    <h2>Find me</h2>
    <p><a href="https://github.com/janedoe">
       My GitHub</a></p>                       <!-- 👈 a = a link. href = where it goes -->
  </main>

  <footer>                                     <!-- The small print at the bottom -->
    <p>Built by hand, with HTML I understand.</p>
  </footer>

</body>                                        <!-- Visible part ends -->
</html>                                        <!-- Page ends -->
```

What you're looking at: HTML is a labeling system. Every `<tag>` opens a labeled box,
every `</tag>` closes it, and boxes nest inside boxes — `<li>` inside `<ul>` inside
`<main>` inside `<body>`. That's the entire trick (Module 17 said so, and it was true).

5. Scroll down and **commit** the file with a message like `Add home page`.
6. Turn on publishing: repository **Settings → Pages**, source = the `main` branch,
   save. Within a few minutes, `https://yourusername.github.io` is live.

**✅ Checkpoint:** visit your URL. Your page — plain-looking, but *yours*, on the actual
internet. Screenshot this moment.

## Milestone 3 — Style it (2–3 hours)

Time to hire the interior decorator (Module 18's UI analogy). Create a new file named
`style.css` — the file your HTML already asks for by name:

```css
body {                              /* "For the whole visible page…" */
  font-family: Georgia, serif;      /* …use this font (serif = the kind with feet) */
  max-width: 42rem;                 /* …never stretch text wider than ~65 letters */
  margin: 0 auto;                   /* …center that column ("auto" splits leftover space) */
  padding: 1rem;                    /* …keep a finger's width of breathing room */
  line-height: 1.6;                 /* …space the lines out for comfortable reading */
  color: #222222;                   /* …very dark gray text (softer than pure black) */
}
nav a {                             /* "For links inside the nav…" */
  margin-right: 1rem;               /* …put space between them */
}
h1, h2 {                            /* "For both headline sizes…" */
  color: #1a5f7a;                   /* …a calm teal-blue. Pick your own! */
}
footer {                            /* "For the small print…" */
  margin-top: 3rem;                 /* …push it well below the content */
  font-size: 0.9rem;                /* …make it slightly smaller */
  color: #777777;                   /* …and gray, like small print should be */
}
```

How CSS reads: each block is `who { property: value; }` — *for this kind of element,
set this dial to this setting*. Commit it (`Add styles`), wait a minute, refresh your
site. Then **play**: change the colors (search "CSS color picker" for the dials), change
the font, commit each experiment. This is the fun part — take your time in it.

**✅ Checkpoint:** your live site has a centered, readable column with your colors.

## Milestone 4 — The about page and working nav (1–2 hours)

1. Create `about.html`. Structure it like `index.html` (same `<head>` — including the
   `style.css` line — same `<nav>`, same `<footer>`), but with its own content: your
   tech origin story from Lab 19 wants to live here.
2. The `<nav>` links now work in both directions. Click Home ↔ About on the live site
   until it stops being amazing. (It won't.)

**✅ Checkpoint:** a real multi-page website. Two pages, linked, styled, live.

## Milestone 5 — Let the history tell the story (ongoing)

Look at your repository's commit list. By ship day you want **at least 10 meaningful
commits** with honest messages: `Add home page`, `Add styles`, `Fix broken About link`,
`Rewrite intro to sound like me`. This isn't busywork — Module 19 told you hiring
managers read commit history. Ten real commits say: *this person works in steps, like an
engineer.*

## Milestone 6 — Test it, including on a phone (1 hour)

Your Module 09 instincts, applied:

- Open the live site **on a phone**. Comfortable to read? Links tappable? (That
  `viewport` line from Milestone 2 is doing this work — the Module 17 lab explained
  the trick.)
- Click **every** link on every page. A broken nav link is this track's most common bug.
- Read every word aloud once — typos hide from silent reading.
- Ask one other human to try it while you watch, *without helping them*. Watching
  someone use your thing is the whole QA profession in one humbling minute.

## Milestone 7 — SHIP it (30 minutes)

Send the URL to one human being with a sentence like: *"I built this myself — actual
code, published it with the tools professionals use."* Then add the link to your GitHub
profile README (Lab 19, Part 4 — the "coming soon" line has been waiting for this).

---

## ✅ Definition of done

- [ ] Live at `https://yourusername.github.io`
- [ ] At least two pages, linked to each other through a nav
- [ ] Styled with a CSS file you wrote and can explain line by line
- [ ] 3 user stories and 2 wireframe photos exist (in the repo is a nice touch)
- [ ] At least 10 meaningful commits with honest messages
- [ ] Tested on a phone; every link clicked; one human tried it while you watched
- [ ] URL sent to at least one person 🎉

## ✨ Stretch goals (optional, after done)

- **A projects page.** Add `projects.html` listing what you made in this course — the
  labs, your Track C program if you build one, this site itself. Add it to the nav.
  This turns your site into the portfolio gallery Module 19 described.
- **A custom domain.** You can buy a name like `janedoe.com` (roughly $10–20/year —
  this is the one item in this course that costs money, which is why it's optional) and
  point it at your GitHub Pages site; GitHub's Pages settings have a "Custom domain"
  box and step-by-step docs. Entirely skippable: `yourusername.github.io` is free
  forever and employers respect it just fine.

When done: add yourself to the **[Showcase](showcase.md)**. You've earned the row.
