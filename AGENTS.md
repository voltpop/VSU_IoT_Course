# Agent Instructions for this repository

This repository is a **shared** knowledge base for the VSU Innovation
Program, worked on by multiple parties (Builder Tech, VoltPop, Explay,
and VSU) — not a single person's private notes. Treat every change
accordingly.

## Required workflow: worktree + PR, never direct commits to `main`

1. **Create a git worktree** for any update or new work, rather than
   editing directly in the primary checkout or committing straight to
   `main`:
   ```
   git worktree add ../vsu-iot-course-<short-topic> -b <short-topic>
   ```
   Do the actual editing in that worktree.
2. **Commit your changes** in the worktree branch with a clear,
   specific message describing what changed and why (not just "update
   docs").
3. **Push the branch and open a pull request against `main`** rather
   than merging or pushing directly. Use `gh pr create` if the `gh` CLI
   is available; otherwise push the branch and note that a PR needs to
   be opened.
4. **Do not force-push, rewrite history, or merge your own PR**
   automatically — leave the merge decision to whoever is reviewing on
   the human side, since multiple parties may be reviewing changes to
   shared documents like the budget or the schedule.
5. Clean up the worktree (`git worktree remove`) once its branch has
   been merged or is no longer needed.

## Why this matters here specifically

- Multiple organizations' agents/assistants may work in this repo. A
  direct commit to `main` from one party's agent could silently
  overwrite or conflict with another party's edits to the same shared
  document (e.g., the budget figures in `Admin-Business-Legal.md`, or
  the schedule table in `Course-Curriculum.md`).
- A PR gives every party a chance to see what changed before it becomes
  the shared source of truth, which matters more here than in a typical
  single-owner notes repo.

## Other conventions

- Keep the file split established in `README.md` — business/legal/budget
  content in `Admin-Business-Legal.md`, curriculum/schedule content in
  `Course-Curriculum.md`, stakeholder-facing material in
  `Stakeholder-Pitch-Deck-Draft.md` and `Press-Kit-Content.md`, and
  cross-party action items in `TODOs-by-Owner.md`. Don't fork new
  top-level files for content that fits an existing one without a clear
  reason.
- When a figure or fact changes (budget numbers, schedule dates, role
  assignments), update it in place rather than leaving stale figures
  alongside new ones — but note *what changed and when* if the change
  is non-obvious or corrects an earlier assumption, since this repo is
  read by people who weren't in the room when the change was decided.
- Avoid adding personal/private information belonging to any one party
  (e.g., someone's individual negotiating position, personal financial
  details not relevant to the shared program) — this repo is meant to be
  readable by all four parties.
