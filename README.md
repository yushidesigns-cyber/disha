# Disha's Bachelorette — What Did Savu Say?

A single-page, mobile-friendly Q&A game for Disha's bachelorette. Three rounds —
**Regular**, **Spicy**, and **Wild Cards** — each showing a question with a
"What did Savu say?" button that plays his actual recorded answer.

## Structure
- `index.html` — the whole app (markup, styles, and script in one file).
- `audio/` — 32 individual answer clips, cut from the 3 original recordings
  (`regular-01.mp3`…`regular-16.mp3`, `spicy-01.mp3`…`spicy-06.mp3`,
  `wild-01.mp3`…`wild-10.mp3`), numbered to match the on-screen question order.

## How to use
Open `index.html` in a browser (locally, or host the folder anywhere static,
e.g. GitHub Pages). No build step, no dependencies.

## Note on the audio clips
The three original recordings were each one continuous take, with Savish
repeating each question before answering. This environment had no network
access to a speech-to-text service, so the clips were split using pause
detection cross-checked against the words that *did* come through clearly
(e.g. "wedding", "in front of you", "grandkids", "ten minutes", "their own
jokes", "who initiated…I did"). Most boundaries are anchored on an actual
matching phrase; a few (where he answered two questions back-to-back with
barely a breath in between, mostly early in the "Regular" round) are best-
effort. If any clip sounds like it's answering the wrong question or is
missing its start/end, flag which one — the original full recordings are
easy to re-cut for just that clip.
