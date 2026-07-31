# Agent Instructions for this repository

This repository is a **shared** knowledge base for the VSU Innovation
Program, worked on by multiple parties (Builder Tech, VoltPop, Explay,
and VSU) — not a single person's private notes. Treat every change
accordingly.

## Required workflow: worktree + PR, never direct commits to `main`

The human you're working for should never need to know git, check their
own GitHub permissions, or run any git commands themselves — figure out
which path below applies and handle it end-to-end, then just hand them
the resulting PR URL.

1. **Create a git worktree** for any update or new work, rather than
   editing directly in the primary checkout or committing straight to
   `main`:
   ```
   git worktree add ../vsu-iot-course-<short-topic> -b <short-topic>
   ```
   Do the actual editing in that worktree.
2. **Commit your changes** with a clear, specific message describing
   what changed and why (not just "update docs").
3. **Check whether you actually have push access to this repo** before
   assuming you do:
   ```
   gh api repos/voltpop/VSU_IoT_Course --jq '.permissions.push'
   ```
   - **If `true`** (you're a collaborator with write access): push the
     branch directly and open a PR against `main` with `gh pr create`.
   - **If `false`** (most outside contributors — Builder Tech, Explay,
     VSU staff, or anyone else working through their own agent, unless
     they've been explicitly added as a collaborator): **fork the repo
     to your own account and PR from the fork.** This is the normal,
     zero-configuration way any public GitHub repo accepts outside
     contributions — it does not require the repo owner to grant
     anything in advance:
     ```
     gh repo fork voltpop/VSU_IoT_Course --clone=false
     git remote add fork git@github.com:<your-username>/<fork-name>.git
     git push fork <branch>
     gh pr create --repo voltpop/VSU_IoT_Course --base main \
       --head <your-username>:<branch> --title "..." --body "..."
     ```
     (`gh repo fork` prints the fork's URL/name — use exactly what it
     reports, since GitHub may suffix the name, e.g. `-1`, if you
     already have a same-named repo.)
   - **If your branch was built from a fresh/empty local repo** rather
     than an up-to-date clone, `gh pr create` may fail with `"branch
     has no history in common with main"` — this happens when your
     local history and the real remote `main` diverged from the start
     (e.g. remote `main` already had a commit yours didn't start from).
     Fix by rebasing before pushing/PRing:
     ```
     git fetch origin
     git rebase origin/main
     git push --force fork <branch>   # only safe because this branch
                                       # isn't shared/merged anywhere yet
     ```
4. **Do not force-push over a branch other than your own
   not-yet-merged one**, rewrite history on `main`, or merge your own
   PR automatically — leave the merge decision to whoever is reviewing
   on the human side, since multiple parties may be reviewing changes
   to shared documents like the budget or the schedule.
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
