# ✅ Quiz 16 — AI & Machine Learning

Answer in your head or on paper, then open each fold. If you get one wrong, that's the
quiz working — reread that section over coffee.

---

**1. Fill in the arrows. Traditional programming: ___ in, ___ out. Machine learning:
___ in, ___ out.**

<details><summary>Show answer</summary>

Traditional programming: **rules** in, **answers** out (humans write the rules).
Machine learning: **examples** in, **rules** out (the machine finds the patterns
itself). The spam filter learned from two million labeled emails instead of 10,000
hand-written if-rules.
</details>

**2. Why did hand-written rules lose the spam war?**

<details><summary>Show answer</summary>

Spammers adapt faster than humans can write rules. Every new rule ("block 'FREE
MONEY'") got dodged ("FR3E M0NEY"), and rule piles started catching real email too. A
model trained on millions of examples finds subtler patterns and can be retrained as
spam evolves.
</details>

**3. Training vs. using: which one costs millions, and what does the exam analogy say
about chatting with an AI?**

<details><summary>Show answer</summary>

Training costs millions — months of computing to tune the model. Using it (inference)
is fast and cheap-ish. The exam analogy: when you chat with an AI, it's *taking the
exam*, not studying — no new learning happens during your conversation, and the model
stays frozen until its makers retrain it. That's also why it doesn't know last week's
news.
</details>

**4. What is a model made of, and what's honestly strange about the knobs?**

<details><summary>Show answer</summary>

A model is millions or billions of adjustable numbers — "knobs" on a giant mixing desk
— tuned automatically during training until answers stop being wrong. The strange part:
no human set them, and often nobody — including the creators — can say what any single
knob means. That's why AI can be hard to explain and audit ("black box").
</details>

**5. In an image-recognizing neural network, what do the layers do — and is it a
brain?**

<details><summary>Show answer</summary>

Each layer spots patterns in the previous layer's output, stacking simple into
sophisticated: edges → shapes → parts (eyes, wheels) → whole things (faces, cars). It's
*loosely inspired* by neurons but it is not a brain — it's arithmetic in layers, a
paper airplane to the brain's falcon.
</details>

**6. A large language model has one core trick. What is it, and why does that humble
trick produce such impressive results?**

<details><summary>Show answer</summary>

Predicting the next word. Done at colossal scale — trained on a mountain of human text
with billions of knobs — predicting the next word *well* forced the model to absorb
grammar, facts, styles, and the shapes of arguments. Stack enough good next-word
predictions and you get essays, code, and poetry.
</details>

**7. Define "hallucination," and explain why an LLM's hallucinations arrive with no
warning signs.**

<details><summary>Show answer</summary>

A hallucination is output that is fluent, confident, and false — an invented paper, a
wrong date, a fake court case. There's no warning because the model's only compass is
"what sounds plausible next" — truth isn't part of the mechanism — so falsehoods wear
the exact same confident tone as facts. Like the friend who read the whole library but
never says "I'm not sure."
</details>

**8. Your colleague pastes an LLM's answer — including two statistics and a citation —
straight into a client report. What's the rule they broke, and what should they do
instead?**

<details><summary>Show answer</summary>

Never trust an LLM for facts you can't verify. Statistics, names, dates, and citations
are exactly where hallucinations hide. The fix: use the LLM for the draft (its
strength), then verify every checkable claim against a real source before it ships —
brilliant intern, unread work, never straight to the client.
</details>

**9. The hiring-model story: what happened, and what's the general moral?**

<details><summary>Show answer</summary>

A company trained a hiring model on ten years of its own decisions — which skewed male
— so the model learned to downgrade CVs mentioning women's activities and colleges. It
was scrapped. The moral: garbage in, gospel out — a model trained on a biased history
will faithfully repeat that history, with a machine's false authority.
</details>

**10. Sort these into "exists today" vs. "does not exist today": (a) software that
spots tumors in scans, (b) AGI — AI as flexible as a human across all tasks, (c) photo
search that finds "dog", (d) an AI that knows when it's wrong.**

<details><summary>Show answer</summary>

Exists today: (a) and (c) — narrow pattern-recognition is AI's home turf. Does not
exist today: (b) AGI is hypothetical; and (d) — today's models have no reliable sense
of their own wrongness, which is exactly why hallucinations come out confident.
</details>

**11. Name three pieces of everyday machine learning you probably used this week
without calling it "AI".**

<details><summary>Show answer</summary>

Any three of: face unlock, photo search finding "dog", maps predicting arrival time,
autocorrect/autocomplete, spam filtering, and every recommendation feed ("the
algorithm™") — music, video, shopping. ML has been in your pocket for years; only the
chatbots made it famous.
</details>

**12. 🗣️ Explain it to a friend.** Your uncle says: "I read that ChatGPT knows
everything — and my neighbor says it lies constantly. Which is it?" Give him a
two-minute answer using at least one analogy from this module. Cover: what an LLM
actually does, why it's both brilliant and unreliable, and one rule for using it
safely.

<details><summary>Show a sample answer (read only after trying!)</summary>

"Both, and here's why that's not a contradiction. ChatGPT is a giant autocomplete — its
whole trick is predicting the next word, after training on a huge slice of everything
ever written. Predicting words *that* well makes it genuinely brilliant at drafting,
summarizing, and explaining. But 'sounds plausible' is its only compass — it has no
sense of true versus false and no feeling of not-knowing. So it's like a charming
friend who read the entire library but sometimes misremembers and never says 'I'm not
sure' — the mistakes come out in the same confident voice as the facts. They're called
hallucinations. The rule: use it for drafts and ideas, and verify any fact that
matters — names, numbers, dates — before you repeat it. Treat it like a brilliant
intern: wonderful first drafts, but you never send them out unread."
</details>
