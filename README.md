# Disha's Bachelorette — Game Night

A mobile-friendly hub of games for Disha's bachelorette. `index.html` is the
home page — pick a game, tap in, no sign-in or app required.

## Games
- **What Did Savu Say?** (`savu-says.html`) — three rounds of questions about
  Disha; guess first, then press play to hear the groom's actual recorded
  answer.
- **Never Have I Ever** (`never-have-i-ever.html`) — a bachelorette-edition
  "never have I ever" card deck across three rounds (Sweet, Cheeky, Wild).
- **Spin For A Dare** (`dare-wheel.html`) — a spinning wheel that lands on
  Mild / Bold / Wild and hands out a random dare from that category.
- **Bride Bingo** (`bride-bingo.html`) — a randomly-generated 5×5 bingo card
  of things that might happen during the party; tap squares live, first to
  five in a row wins.

## Structure
- `index.html` — the game hub / home page.
- `savu-says.html`, `never-have-i-ever.html`, `dare-wheel.html`,
  `bride-bingo.html` — one self-contained file per game (markup, styles, and
  script all in one file, no build step, no dependencies).
- `audio/` — 32 individual answer clips for "What Did Savu Say?", cut from
  the 3 original recordings (`regular-01.mp3`…`regular-16.mp3`,
  `spicy-01.mp3`…`spicy-06.mp3`, `wild-01.mp3`…`wild-10.mp3`), numbered to
  match the on-screen question order.
- `savu-local.html` — a fully self-contained, offline copy of "What Did Savu
  Say?" (audio embedded as data URIs) for opening directly as a local file
  without hosting.

## How to use
Open `index.html` in a browser (locally, or host the folder anywhere static,
e.g. GitHub Pages) and pick a game.

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
