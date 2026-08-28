# GitHub Primer

*Source: [`../Day1.md`](../Day1.md) items 2 (GitHub portion), 3, and 4.
~120 min combined — the single largest deck of the day. Covers
everything GitHub/git related as one coherent block before pivoting to
Kiro in the AI Primer deck.*

**Blocking dependency:** this deck assumes the workspace repo
(`VoltPop-Workspace.md` item #13) already exists — see Day1.md's note
at the top. If it isn't built yet, swap in the manual fallback steps
noted below.

---

## What is GitHub, in one line

- A shared folder with history for your team.
- Everyone's copy stays in sync through it.

---

## Create your GitHub account

- Go to `github.com/join`.
- Use a personal (not university) email — one you'll keep after
  graduation.
- Verify your email.
- Turn on 2FA.

---

## Join your team's repo

- Your team's repo is already set up (from a template, with your
  notes-KB and Kiro already wired in).
- Accept the invite link / redeem the join-code (exact mechanic TBD —
  see `../README.md` open items).

> Speaker notes: **manual fallback** if the workspace repo isn't ready
> — instructor creates one repo per team by hand ahead of time and adds
> each student as a collaborator individually.

---

## Handout: Git Cheat Sheet

- Pass out the [Git Cheat Sheet](../Assets/git-cheat-sheet-education.pdf)
  now — a one-page reference for the concepts and commands coming up
  next.

---

## Git concepts, plain-language

- **Repo** — a shared folder with history.
- **Commit** — a saved checkpoint.
- **Push / pull** — sync your copy with the shared one on GitHub.
- No deep internals — recipe-following, same as the hardware weeks.

---

## Live demo

1. `git clone <group-repo-url>`
2. Open the folder — point out the notes-KB scaffold and Kiro steering
   file that are already there.
3. Make a trivial edit → `git status` → `git add <file>` →
   `git commit -m "..."` → `git push`.
4. `git pull` — *why* you'd run this ("a teammate changed something and
   you want their update").

> Speaker notes: screen-share and narrate; have every team follow along
> on their own machine.

---

## Exercise: your first real commit

- As a team, open Kiro and write a one-paragraph "who we are" note
  (team name, members, one sentence on what excites you about the
  course) into the notes-KB.
- Save it, then `git add` / `commit` / `push`.

> Speaker notes: this is the same fork-and-commit workflow this
> program's own staff KB runs on (`AGENTS.md`) — *"you're doing what we
> do."*

---

## Looking ahead (not today)

- **Proposed, not locked:** an `upstream` remote on your repo, so
  future material updates (e.g. Week 5 firmware starters) can be
  pulled in with `git fetch upstream && git merge upstream/main`.
- See `../README.md` open items for status.
