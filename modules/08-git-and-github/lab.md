# 🔧 Lab 08 — Your First Repository (and Maybe Your First Website)

> **Goal:** do the real thing. By the end of this lab you will have a GitHub account, a
> repository, commits with your name on them, a merged pull request — and, if you take
> the bonus, a live personal webpage on the internet, for free.
>
> **You'll need:** a web browser and an email address. That's all. Everything happens on
> the GitHub website — no installation. Works on a phone, though a laptop is more
> comfortable. Time: 30–45 minutes (+20 for the bonus).

> ⚠️ **Watch out:** websites redesign their buttons and menus constantly. If a button
> isn't exactly where we say, don't worry — we describe the *intent* of every step
> ("find the option for creating a new repository"), and GitHub's layout labels those
> intents in plain words. Look for the words, not the pixel.

---

## Part 1 — Create your GitHub account (5 minutes)

*(This is the one sign-up this course ever asks of you — see our style guide's promise.)*

1. Go to **[github.com](https://github.com)** and find the **Sign up** button.
2. Follow the prompts: email, a password, and a **username**.
3. **Choose your username with care** — it becomes part of your public web address
   (github.com/yourname), it's what employers may one day see, and the bonus will put it
   in your website's address. Something professional-ish you'd put on a résumé beats
   `xXdragonlord99Xx`. Lowercase letters, numbers, and hyphens work best.
4. Verify your email when GitHub asks. The free plan is genuinely free and is all you
   need — skip any paid offers.

**✅ What you should see:** your GitHub home page, and your profile at
`github.com/yourusername` — mostly empty. Not for long.

---

## Part 2 — Create your first repository (5 minutes)

1. Find the option to create a **new repository**. It's usually behind a **+** icon near
   the top of the page, or a green **New** button.
2. Name it `my-first-repo`.
3. For the description, write anything — try *"Learning Git, one commit at a time."*
4. Keep it **Public** (nothing secret is going in it, and public repos are what
   employers can see).
5. **Important:** tick the checkbox that says **"Add a README file"**. This gives your
   repo a first file — and, quietly, your very first commit.
6. Click **Create repository**.

**✅ What you should see:** a page showing your repository, containing one file called
`README.md`, with its contents (your repo's name and description) displayed below the
file list. Congratulations — that's a repository with one commit in its history.

---

## Part 3 — Edit a file and make your first hand-written commit (10 minutes)

1. Click on the `README.md` file, then find the **pencil icon** (✏️) — the intent is
   "edit this file". Click it. You're now in GitHub's web editor.
2. Add a few lines below what's there. Try:

   ```
   ## About me

   I'm learning how software really works.
   This is my first repository, and this line is my first real commit.
   ```

3. Find the button to save — it will say something like **Commit changes**.
4. A box appears asking for a **commit message**. This is your lab-notebook note! Don't
   accept the vague default. Write something future-you would thank you for:
   *"Add an About Me section to the README"*.
5. Confirm the commit (commit directly to the `main` branch when asked).

**✅ What you should see:** your README now shows the new text. Now find the repo's
**history** — look for a link mentioning **commits** (often a small clock icon or a
"2 commits" label near the file list). Click it. There they are: two snapshots, newest
first, each with its message, your name, and a timestamp. That's the time machine.
Click any commit to see exactly what changed, with additions in green.

---

## Part 4 — Branch, change, pull request, merge (15 minutes)

Time for the full professional workflow — the photocopy, the edit, the "please review",
and the merge. Yes, you'll be reviewing yourself. Every engineer's first PR works this
way.

**Make a branch:**

1. On your repo's main page, find the button that currently says **main** (the branch
   selector, near the file list).
2. Click it, type a new branch name — `improve-readme` — and choose the option to
   **create branch `improve-readme` from `main`**.

**✅ What you should see:** the selector now says `improve-readme`. You are standing on
your photocopy. Anything you change here leaves `main` untouched.

**Change a file on the branch:**

3. Still on the `improve-readme` branch, edit `README.md` again (pencil icon). Add a
   line — perhaps *"Fun fact: this line was written on a branch."*
4. Commit it with a good message, e.g. *"Add a fun fact line"*. Make sure it commits to
   `improve-readme`, not `main`.

**Open the pull request:**

5. GitHub will likely show a yellow banner suggesting **"Compare & pull request"** —
   that's your shortcut. (No banner? Find the **Pull requests** tab and choose **New
   pull request**, comparing `improve-readme` into `main`.)
6. Give the PR a title and, in the description, one sentence on what you changed and
   why. Create the pull request.

**✅ What you should see:** the pull request page — your change displayed side by side
(old vs. new), a conversation area for comments, and a green **Merge** button. On a real
team, a colleague would review here. Take a second to appreciate this page: it's where a
huge fraction of the world's software work actually happens.

**Merge it:**

7. Click **Merge pull request**, then confirm. GitHub may offer to delete the
   `improve-readme` branch — go ahead; the photocopy has served its purpose, and the
   merge is recorded forever.

**✅ What you should see:** back on `main`, your fun-fact line is there, and the commit
history shows the merge. You have now personally performed: branch → commit → pull
request → review → merge. That is, honestly, the daily loop of professional software
development.

---

## 🌟 Part 5 (Bonus) — Publish a real website with GitHub Pages (20 minutes)

GitHub will host a personal website for you, free, at
`https://yourusername.github.io`. Here's the whole trick: it serves any repo with that
exact special name as a live website.

1. Create a **new repository** (as in Part 2). Name it **exactly**
   `yourusername.github.io` — replacing `yourusername` with your actual username,
   spelled precisely. (Wrong spelling = no website.) Public, and tick "Add a README".
2. In the new repo, find the option to **create a new file** (often under an **Add
   file** button). Name the file `index.html` — the traditional name for a website's
   front page.
3. Paste in this template (edit the words to be yours!):

   ```html
   <html>
     <head>
       <title>My first website</title>
     </head>
     <body style="font-family: sans-serif; max-width: 600px; margin: 40px auto;">
       <h1>Hello, world. I'm [Your Name].</h1>
       <p>I built this page myself, with a Git commit,
          and it is live on the actual internet.</p>
       <p>I'm currently learning how software really works.</p>
       <hr>
       <p>Made with about 15 lines of HTML and one commit.</p>
     </body>
   </html>
   ```

4. Commit the new file with a message like *"Add my first web page"*.
5. Now enable Pages: go to the repo's **Settings**, find the **Pages** section, and make
   sure it's set to serve from the `main` branch. (For a repo with this special name,
   GitHub usually switches Pages on automatically.)
6. Wait a minute or two, then visit **`https://yourusername.github.io`** in a new tab.

**✅ What you should see:** your page. Live. On the internet. Anyone on Earth can visit
that address. When it sinks in, edit `index.html`, commit, wait a minute, refresh —
your edit is live too. You now update a website the way professionals do: with commits.

*(Don't worry about what the HTML lines mean yet — Module 10 dissects HTML properly.
Today was about shipping.)*

---

## 🎉 Done!

Look at your profile page (`github.com/yourusername`). This morning it didn't exist. Now
it shows repositories, commits, and possibly a live website — real, public evidence of
real skills. Keep committing to it as the course continues; the little activity graph
fills in, and future-you (and maybe a future employer) will be glad.
