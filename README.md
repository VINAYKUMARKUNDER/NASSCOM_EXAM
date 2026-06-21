# NASSCOM Mock Exam

A self-contained practice exam tool for the NASSCOM certification test. Pulls 50 random questions from a bank of 250 every time you start, runs entirely in your browser, and needs no installation, login, or internet connection after the page loads.

**Live demo:** [https://nasscom-exam.vercel.app/](https://nasscom-exam.vercel.app/)

---

## What this is

A single HTML file (`nasscom_mock_exam.html`) containing everything: the question bank, the styling, and all the logic. There is no backend, no database, and no API calls. Open the file in any browser and the exam works.

This was built to help prepare for the NASSCOM exam by going beyond the original ~40-question sample bank — covering the same seven topic areas in much greater depth so practice doesn't just become memorizing the same fixed set of questions.

## How it works

1. **Open the file** — double-click `nasscom_mock_exam.html`, or visit the live demo link above.
2. **Set your preferences** — choose how many questions (default 50, max 250) and a time limit (default 45 minutes).
3. **Take the exam** — answer questions one at a time, jump between them using the question palette, flag your progress visually (green = answered).
4. **Submit** — manually, or automatically when the timer hits zero.
5. **Review results** — see your overall score, a topic-by-topic breakdown, and (optionally) a full review of every question with the correct answer highlighted.

Every time you start a new exam, the tool:
- Randomly picks N questions out of the full 250-question bank (Fisher–Yates shuffle)
- Randomly reorders the four options within each question

This means two attempts almost never look identical, so repeated practice tests genuinely test recall instead of pattern memorization.

## Question bank

250 questions across the same seven categories the real NASSCOM exam materials covered:

| Topic | Questions |
|---|---|
| SDLC (phases, models, DevOps, deployment) | 40 |
| Architecture, UI/UX, Security by Design | 30 |
| Software Testing | 45 |
| Quality Assurance (QA) | 30 |
| Network Management | 30 |
| Cybersecurity | 45 |
| Project Management | 30 |

Each question has exactly four options and one correct answer, stored as plain data inside the file — no external requests are made to fetch or grade questions.

## Features

- **Adjustable exam length and timer** — practice a quick 10-question drill or a full 250-question marathon
- **Countdown timer** with visual warnings (amber under 5 minutes, red and pulsing under 1 minute) and auto-submit on timeout
- **Question palette** for quick navigation and an at-a-glance view of what's answered
- **Topic-wise score breakdown** after submission, so you know exactly which areas need more revision
- **Review mode** with filters (all / correct only / incorrect only) showing the right answer next to your selection
- **"Browse full question bank"** mode — read through all 250 questions untimed, useful as a study pass before attempting a timed run

## Why it's frontend-only

Everything — the question data, the random selection, the timer, the scoring — runs as vanilla JavaScript in your browser. Nothing is sent to a server, nothing is logged anywhere, and there's no account or login involved. Your answers and results exist only in the browser tab for that session; closing or refreshing the page resets everything, by design.

This also means the file is fully portable: email it, put it on a USB drive, host it anywhere (which is what the Vercel link above does), or just keep it locally — it behaves identically everywhere.

## Limitations

- No persistence — scores and progress are not saved between sessions
- No multi-user or leaderboard features
- Question bank is fixed at build time; adding new questions means editing the file directly

## Disclaimer

This is an unofficial practice tool created independently for self-study. It is not affiliated with or endorsed by NASSCOM. Question topics are based on publicly shared NASSCOM exam preparation material, but actual exam questions will differ.
