# Agent Instructions for this repository

This repository is a **shared** knowledge base for the VSU Innovation
Program, worked on by multiple parties (Builder Tech, VoltPop, Explay,
and VSU) — not a single person's private notes. Treat every change
accordingly.

## Required workflow: worktree + PR, never direct commits to `main`

Work in a worktree/branch, commit, and open a PR against `main` — never
commit straight to `main`. Handle this entirely yourself: check push
access, fork-and-PR instead if you don't have it, fix any git mechanics
that come up (e.g. unrelated-history errors) without asking. The human
should never need to touch git, check permissions, or read a workflow
doc — just hand them the PR URL when it's done. Don't force-push or
merge anything other than your own not-yet-reviewed branch.

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
