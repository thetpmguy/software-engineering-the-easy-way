# 🔧 Lab 16 — Poke the AI (Politely)

> **Goal:** stop reading *about* AI and put your hands on it: find its genuine
> strengths, catch it hallucinating red-handed, and train a real machine-learning model
> yourself in five minutes. Everything runs in a browser, free, no installs.
>
> **Time:** 60–75 minutes across three parts. Part 2 is most people's favorite.

---

## Part 1 — Break an AI politely (25 minutes)

Open any free AI chatbot you can access — ChatGPT's free tier, Claude, or Gemini all
work. (If one requires sign-up you don't want, try another.) You'll give it five tasks
chosen to reveal both its brilliance and its cracks. **Keep a score sheet:** for each
task write *impressive / okay / wrong*.

### Task 1 — Summarize (expected: strength)

Paste in any long paragraph — from a news story, a work email, this course — and ask:
*"Summarize this in two sentences for a busy friend."*

**What you should see:** a genuinely good summary in seconds. This is home turf:
rewriting text it can see in front of it.

### Task 2 — Create (expected: strength)

Ask: *"Write a short funny poem about my street, where the neighbor's dog barks at
delivery vans."* Then push it: *"Now make it rhyme. Now make it a pirate sea shanty."*

**What you should see:** fluent, playful writing, reshaped on command. Notice how
iteration (asking again with tweaks) improves it — prompting tip 3 from the lesson in
action.

### Task 3 — Arithmetic (expected: check it!)

Ask it to multiply two 6-digit numbers, for example: *"What is 428,391 × 762,148?"*
Then check the answer with your phone's calculator.

**What you should see:** possibly a correct answer (some chatbots now quietly use a
calculator tool) — but possibly a confidently wrong one. Either way, the lesson lands:
a language model *predicts plausible text*; it isn't a calculator. Plausible-looking
digits are exactly what it produces, right or wrong. It answers wrong in the same
confident tone as right — no stammer.

### Task 4 — The hallucination hunt (the big one)

Ask: *"Cite three real research papers about [some niche topic — e.g., the sleep
patterns of garden snails, or the history of your small hometown]. Include authors,
year, and journal."*

Now **verify each paper**: search the exact title in a search engine or Google Scholar.

**What you should see:** this varies — and the variation is the lesson. You may get real
papers, papers with real authors but mangled titles, or beautifully formatted citations
for papers that **do not exist**. If you catch a fake: congratulations, you've witnessed
a hallucination — fluent, confident, false — firsthand. You will never again trust an
unverified citation, which puts you ahead of several lawyers who made the news.

### Task 5 — Ask about yourself (expected: limits lesson)

Ask: *"What do you know about [your full name]?"*

**What you should see:** unless you're famous, it should say it doesn't know you — and
well-trained chatbots will decline to speculate about private individuals. If it *does*
produce claims about you, treat them as task 4 taught you: plausible text, not facts.
Two lessons in one: models only "know" what was in public training data, and guessing
about private people is exactly where hallucination does real harm.

### Wrap up Part 1

Look at your score sheet. Typical result: brilliant at tasks 1–2, shaky-to-fraudulent at
3–4, humble (hopefully) at 5. That *profile* — great with text, unreliable with facts —
is the single most useful thing to know about today's AI.

## Part 2 — Train your own model: Teachable Machine (25 minutes)

Time to switch roles: from AI user to AI *trainer*. Google's **Teachable Machine** lets
you train a real image-recognition model in your browser with a webcam. Free, no
account, and images are processed in your browser.

1. Go to **teachablemachine.withgoogle.com** and choose **Get Started** → **Image
   Project** → **Standard image model**.
2. You'll see two classes. Rename **Class 1** to `Thumbs up` and **Class 2** to
   `Thumbs down`.
3. For `Thumbs up`: click **Hold to Record** with your webcam on and hold a thumbs-up,
   moving your hand around a bit — collect **around 50 images**.
4. Do the same for `Thumbs down`.
5. Click **Train Model**. Wait the few seconds. *That pause is real machine learning
   happening — knobs being tuned, right in your browser.*
6. Now show the webcam each gesture and watch the live prediction bars.

**What you should see:** confident, mostly-correct predictions. You've trained a neural
network. That was "training data": you made it, you fed it, it worked.

### Now break it (the best part)

7. Try to fool your model: put on a jacket, change the lighting, step back, have someone
   else try, or show it *no hand at all*.

**What you should see:** confidence wobbles or predictions flip — especially with no
hand in frame, since your model only ever learned two possible answers. Why? Your model
learned from ~50 images of *you*, in *one room*, in *one light*. It may have quietly
learned "this shirt + this wall = thumbs up." Congratulations: you've just experienced
**bias and overfitting** — a model faithfully learning the accidents of its training
data — with your own webcam. The hiring-model story from the lesson is this exact
phenomenon at company scale.

## Part 3 — Quick, Draw! (10 minutes)

1. Go to **quickdraw.withgoogle.com** and press **Let's Draw!**
2. You get 20 seconds to doodle each prompt while a neural network guesses out loud.
3. After six doodles, click each one to see *what the network compared it to*: thousands
   of other people's drawings of the same thing — its training data, on display.

**What you should see:** the network often guesses shockingly early — because your
"bicycle" scribble lands near the pattern of 100,000 other bicycle scribbles. You're
looking at pattern-matching over examples, the heart of this whole module, drawn in
crayon.

---

## ✅ Lab complete — what you proved

- AI is genuinely brilliant at reshaping text, and confidently unreliable at facts and
  figures — you caught it yourself (or verified you couldn't quite catch it today, which
  is also data).
- Hallucinations are real, fluent, and formatted beautifully. Verify before trusting.
- Training = showing labeled examples; you did it with your own hands and webcam.
- Models learn the accidents of their data (your shirt, your lighting) — bias isn't a
  headline abstraction anymore; it happened on your laptop.
