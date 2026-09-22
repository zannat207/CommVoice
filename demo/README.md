# CommVoice — demo mock-up

A **single, self-contained HTML file** (`demo/index.html`) that shows the CommVoice
experience for a hackathon audience, with **no server, no API key, and no data leaving the page**.

Everything is scripted (canned content) so it always behaves the same on stage. It's built
around a real community scenario: a **City of Sydney draft planning agreement** on public
exhibition.

## What it demonstrates

1. **Empathetic, plain-words overview** — the document explained around the questions a resident
   actually asks (*What is being proposed? What does it mean for me? What might be difficult?*),
   in warm, jargon-free language.
2. **Answers with a source** — every answer taken from the document shows a **"See the exact words"**
   box with the quote and page, so people can trust it.
3. **The guardrail (the point)** — ask something the document doesn't cover (e.g. *"Will this
   increase my council rates?"*) and it **refuses honestly** instead of guessing:
   *"I can't find that in your document. I only answer from what it says, so I won't guess."*
4. **Barrier-free** — text-size controls, high-contrast mode, a friendly mascot, and a
   "read aloud"/voice affordance.

## Run it

Just open the file — double-click `demo/index.html`, or:

```
open demo/index.html          # macOS
```

No install, no build, no internet needed (a web font loads if online; it falls back gracefully offline).

## Suggested 90-second demo flow

1. Click **Try the sample document** → the overview appears in plain words.
2. Tap **"How many affordable homes will there be, and who can get one?"** → answer + exact-words box.
   Point out it *declines* to say who qualifies, because the document doesn't say.
3. Tap **"Will this increase my council rates?"** → the honest refusal. This is the trust story.
4. Toggle **High contrast** and the **A** text sizes to show accessibility.

## How this relates to the real app

The real CommVoice (in the repo root) is a Python/FastAPI app that does this for **any** uploaded
document using Google Gemini, enforced by a four-gate verification system (exact quote must exist,
numbers must match, a second model confirms). This demo reproduces the *look and behaviour* only —
it is not connected to any AI.
