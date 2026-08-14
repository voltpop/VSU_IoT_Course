---
title: VSU Innovation Program — Shared Knowledge Base
compiled: 2026-07-31
updated: 2026-08-02
---

# VSU Innovation Program — Shared Knowledge Base

Working notes for Builder Tech, VoltPop, Explay, Dr. Shawn M. Nicholson
LLC, and VSU to collaborate from. Split by domain:

- **[`Admin-Business-Legal.md`](./Admin-Business-Legal.md)** — parties/roles,
  budget, legal/Agreement status, VSU calendar coordination, funding
  sources, open items.
- **[`Course-Curriculum.md`](./Course-Curriculum.md)** — curriculum
  philosophy, schedule (V1 history + V2 current), cross-check findings,
  lesson-plan status, open items.
- **[`Stakeholder-Notes.md`](./Stakeholder-Notes.md)** — per-stakeholder
  research/contact prep (what they want, outreach status); a tailored
  pitch deck gets built from this later, not guessed at now.
- **[`Press-Kit-Content.md`](./Press-Kit-Content.md)** — blurbs/about copy
  for press materials (logos/photos still need sourcing separately).
- **[`TODOs-by-Owner.md`](./TODOs-by-Owner.md)** — cross-party
  deliverables tied to a specific formal agreement, split by Builder
  Tech, VoltPop, Explay, and Dr. Shawn M. Nicholson LLC. One table per
  agreement per party (e.g. a Curriculum-MOU table, a Joint-Venture
  table), with checkbox / deliverable / due date / who assigned it / a
  short note — the scannable checklist, not the full story.
- **`<Party>-Workspace.md`** (e.g. `VoltPop-Workspace.md`) — each
  party's own personal work not tied to a cross-party agreement, plus
  the fuller history/quotes/decision-provenance behind every row in
  their `TODOs-by-Owner.md` tables. Trimming a shared table to stay
  scannable never actually loses anything — it just moves the depth
  here.
- **[`Files/`](./Files/)** — raw source documents (budget spreadsheet,
  program schedule, stakeholder tracker, meeting recap) kept alongside
  the markdown summaries above as reference copies. These are point-in-
  time snapshots, not synced to whatever live version anyone's actively
  editing elsewhere (e.g. Google Sheets) — check the markdown files
  above for the current state, not these files.
- **[`assets/`](./assets/README.md)** — press-kit pieces (logos,
  headshots, bios) and generated stakeholder handouts (see
  [`assets/stakeholder-handouts/`](./assets/stakeholder-handouts/)).

## New here? Using this KB with an AI assistant

If a knowledgebase like this is new to you, the easiest way in is to
open a coding assistant (e.g. Claude Code) pointed at a local clone and
just ask it questions in plain language — you don't need to know git or
read every file cover-to-cover first.

Things you can ask it:
- *"What's still open for [a stakeholder or party name]?"*
- *"Summarize `Course-Curriculum.md` for me."*
- *"Who owns [an action item from `TODOs-by-Owner.md`]?"*
- *"Find every mention of [a topic] across the whole KB."*
- *"Does anything in here contradict itself?"*
- *"Draft a status update / outreach note from these notes"* — from
  what's written, not invented.
- *"What's changed since [a date]?"* — an assistant can read git
  history for this.

Why this is worth doing here specifically: five parties write across
several documents that reference each other (e.g. `Stakeholder-Notes.md`
cites budget figures that live in `Admin-Business-Legal.md`). Keeping
that cross-referencing straight by hand gets harder as the KB grows — an
assistant that can search the whole KB at once is well-suited to
catching a figure that's stale in one file but already updated in
another, or two documents quietly disagreeing on the same deadline.

If you have an assistant make edits on your behalf, make sure it reads
and follows `AGENTS.md` first (branch + PR workflow, no PII, confirm
which party you're representing) rather than editing straight away.

## What this program is

- Placeholder name: **VSU Innovation Program**, at Virginia State
  University (an HBCU, Commonwealth of Virginia agency). **Per VoltPop
  (2026-08-02): this is an assumptive placeholder, not a name anyone
  has actually deliberately chosen** — it's genuinely just "a generic
  innovation program for VSU," described that way and never revisited
  as a naming decision. Don't state it as fact in stakeholder
  conversations, and treat naming the program as an open decision, not
  a confirmation task.
- Students build a **mobile web app addressing a real Tri-Cities-area
  business problem**, touching GenAI/ML/IoT/cybersecurity as their
  project needs.
- **VSU Spring 2027**, Program Dates **Jan 19 – Apr 29, 2027**.
- Five parties: **VoltPop LLC** (curriculum co-design + Engineering/CS
  instruction), **Builder Tech LLC** (Program Director/operator +
  Business Intelligence & Design instruction), **Explay** (curriculum
  design + Entrepreneurship/Innovation instruction), **Dr. Shawn M.
  Nicholson LLC** (Dr. Shawn Nicholson's business entity — his
  Operations Director & Institutional Liaison role runs through this
  LLC, not VSU employment), and **Virginia State University** (host
  institution).

## Submodule auto-bump hook

This repo is also linked into VoltPop as a git submodule
(`Engagements/VSU_IoT_Course`). A tracked `.githooks/post-merge` hook
auto-bumps and pushes VoltPop's pin whenever `main` advances here — see
`VoltPop/AI/Local/Repo-Architecture-Master-Scoped-KBs.md` §8 for the
full explanation. Enable it once per clone with
`git config core.hooksPath .githooks`.
