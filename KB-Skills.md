---
title: KB Skills — Function Reference
created: 2026-08-14
---

# KB Skills — Function Reference

This is the **one canonical place** the "how" for this KB's assistant
functions lives. `AGENTS.md` and its per-tool mirrors (`CLAUDE.md`,
`GEMINI.md`, `.kiro/steering/agents.md`) carry the *policy* — who's
involved, merge authority, no-PII — and point here for the actual
steps. Written tool-agnostically on purpose: follow this regardless of
which AI assistant you're using, so behavior stays the same across
Claude Code, Gemini CLI, Kiro, or anything else reading `AGENTS.md`.

If a step here ever conflicts with policy stated in `AGENTS.md`,
`AGENTS.md` wins — flag the drift rather than picking one silently.

## `kb-checkin` — start of session

1. State your role (coordination expert / GitHub steward) and ask who
   you're working with (VoltPop, Builder Tech, Explay, Dr. Shawn M.
   Nicholson LLC, VSU staff, a student). Don't guess, and don't skip
   this because a past session already established it — confirm fresh
   each session.
2. Determine local vs. remote/cloud: a real local git clone under the
   human's own synced folder, or an ephemeral/hosted sandbox?
   - **Local:** full read/write mode — every function below is
     available.
   - **Remote/cloud:** read-only mode. Answer from the KB's content
     freely; don't edit, commit, or open a PR. If changes are wanted
     and a real clone isn't reachable, write a standalone markdown file
     summarizing the intended change and reasoning, for later import by
     someone with a real clone.
3. Everything else — sync, GitHub auth, the open-PR queue — defer until
   actually needed rather than checking upfront.

## `save-to-kb` — landing any change

Every other function ends here. Never commit straight to `main`.

1. Confirm `.git` actually exists (not a downloaded/exported copy). If
   it doesn't, `git clone` the real repo first, or fall back to the
   standalone-markdown-file approach above.
2. Scan the diff for PII before committing — student names, personal
   contact details, or anything identifying a specific individual
   beyond named program staff already documented in the KB. If in
   doubt, anonymize or leave it out rather than asking first.
3. Work in a branch/worktree, commit, sync against the latest `main`
   (fetch + rebase or merge), then open a PR. Handle push access
   yourself (fork-and-PR if you don't have write access) — the human
   should never need to touch git.
4. If a real conflict comes up: never blanket-favor one side
   (`--ours`/`--theirs`, an auto-merge tool's pick) and never let a
   clean-looking auto-merge stand in for reading both sides. Manually
   reconcile so both parties' edits survive. If reconciling requires a
   judgment call that could drop or reinterpret someone's content, stop
   and surface it to both the branch owner and whoever holds merge
   authority rather than resolving it unilaterally.
5. Sync again immediately before merging, for the same reason.
6. Keep changesets small — open a PR for what's done rather than
   batching more into one giant diff.
7. Merge/close authority sits with VoltPop. Do the PR mechanics for
   anyone, but only actually merge or close when working with VoltPop
   or explicitly directed by him. For anyone else, hand off with a
   recommendation. Never force-push, and never force-push or merge
   anything other than your own not-yet-reviewed branch.

## `kb-assign` — assign a deliverable to a party

1. Requires a confirmed identity from `kb-checkin` — "assigned by" must
   be the actual confirmed caller, never guessed or assumed.
2. Find the deliverable's agreement table in `TODOs-by-Owner.md` for
   the assignee party (create the table if this is that agreement's
   first item for that party).
3. Add a row: unchecked checkbox, deliverable text, due date (dated
   items sorted before undated ones), assigned-by = confirmed caller,
   short note if useful.
4. If the deliverable's scope naturally spans more than one party, tag
   it **(shared: ...)** rather than filing it under one party alone.
5. Land it via `save-to-kb`.

## `kb-message` — leave a note for someone

1. Requires a confirmed identity from `kb-checkin` for the "from" field.
2. Write the note into a "Messages" section at the top of the
   recipient's `<Party>-Workspace.md`: date, from, message text.
3. **Ephemeral, not permanent:** only deliver/clear a message when
   actually working live with the named recipient. When they've read
   it, replace the full message body with a one-line tombstone (date
   read + "acknowledged by \<party\>") rather than deleting it outright
   — so there's a trace that it was sent and seen.
4. Don't clear or tombstone a message on someone's behalf when they
   aren't the one in the session.
5. Land writes via `save-to-kb`.

## `kb-audit` — integrity sweep

1. Cross-file checks: figures or facts that changed in one file but
   are still stale in another, dead internal links/anchors, dead PR
   links, `TODOs-by-Owner.md` rows with no corresponding history in
   their party's Workspace file.
2. **Tombstone cleanup:** remove `kb-message` tombstones once they've
   served their purpose (present for at least one prior audit cycle) so
   Workspace files don't accumulate dead markers indefinitely.
3. Report findings rather than silently resolving everything —
   contradictions, stale figures, and owner gaps are judgment calls for
   the affected parties. Only auto-fix pure mechanical cleanup (like
   aged tombstones); land that via `save-to-kb`.

## `kb-prs` — PR queue steward

1. List open PRs, summarize what's pending review, flag merge conflicts
   or staleness.
2. Before referring to any PR as still open, re-check its actual
   current state (`gh pr view <number>` or `gh pr list`) — don't trust
   a status from earlier in the session or a prior session.
3. Merge/close authority sits with VoltPop, per `save-to-kb` step 7 —
   apply the same rule here.
