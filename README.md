<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="beat.me.at landing page" width="880">
  </picture>
</p>

<h1 align="center">beat.me.at</h1>

<p align="center"><strong>Beat me at games: a free solo browser arcade of bespoke React and canvas games with a public leaderboard.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/status-live-171717?style=flat-square" alt="Status: live">
  <img src="https://img.shields.io/badge/license-source--available-404040?style=flat-square" alt="License: source-available">
  <img src="https://img.shields.io/badge/part%20of-me.at-737373?style=flat-square" alt="Part of me.at">
</p>

<p align="center">
  <a href="https://beat.me.at">Website</a> ·
  <a href="#features">Features</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#built-with">Built with</a>
</p>

A quick game in the browser should not need an install, and a high-score board should not believe whatever number it is sent. I built beat.me.at as a free single-player arcade: pick one of 29 games and it starts in the same tab, with nothing to install or stream and no account needed to play. Signing in is only what puts a score on the public board, and every score comes from the game itself, never from a text box.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/overview-dark.svg">
    <img src=".github/assets/overview.svg" alt="beat.me.at at a glance: 29 games with no install, scores come from play, fair public boards, boards that stay open" width="880">
  </picture>
</p>

## Why beat.me.at

| The usual high-score board | beat.me.at |
| --- | --- |
| Accepts whatever number is submitted | Scores come only from the game itself |
| Outliers go straight to the top | Implausible scores are flagged, never ranked |
| One all-time board nobody can catch | All-time, this week and today for every game |
| A big download before you play | Each game is its own chunk, loaded when you pick it |

## Features

- **29 games, 5 categories**: arcade, puzzle, racing, physics, and board and card games behind one filterable picker, from Asteroids and Tetris to Sudoku, Pinball, and Solitaire.
- **Loaded on demand**: each game is its own chunk, so you download only the one you pick.
- **Touch-playable**: every game declares touch support, so a phone is told before it scrolls.
- **Three boards per game**: All-time, This week, and Today, so an old score never closes the race.
- **Scores come from play**: games report their own scores; signed-out players still keep a local personal best in the browser.
- **Fair leaderboards**: server-side session gating, a per-account write budget, and plausibility checks that flag (never rank) implausible scores.
- **Shareable scores**: every score has a public share page with its own social preview image.
- **Card tables against AI**: Online Poker and Online UNO pit you against AI seats, with level progression after you clear the bar.

## How it works

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/flow-dark.svg">
    <img src=".github/assets/flow.svg" alt="How beat.me.at works: pick, play, report, check, rank" width="880">
  </picture>
</p>

Each game is its own chunk, so picking one downloads only that game. When a run ends, the game reports its own score: signed-out players keep a local personal best, and signed-in scores pass server-side session gating, a per-account write budget and plausibility checks before they rank on the all-time, weekly and daily boards. Implausible scores are flagged, never ranked.

## Built with

<p>
  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js 16">
  <img src="https://img.shields.io/badge/React-19-171717?style=flat-square&logo=react&logoColor=white" alt="React 19">
  <img src="https://img.shields.io/badge/TypeScript-5-262626?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind%20CSS-4-404040?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4">
  <img src="https://img.shields.io/badge/Drizzle-Postgres-525252?style=flat-square&logo=drizzle&logoColor=white" alt="Drizzle ORM and Postgres">
</p>

- Next.js 16 (App Router), React 19, TypeScript
- Tailwind CSS 4
- Canvas-based game components
- oRPC + TanStack Query for the leaderboard API
- Drizzle ORM + Postgres
- Better Auth (shared `*.me.at` account)

## Part of the me.at family

beat.me.at is one of my [`*.me.at`](https://me.at) apps. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

Source-available. See [LICENSE](LICENSE).
