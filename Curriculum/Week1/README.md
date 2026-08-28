---
title: Week 1 — Course Foundations
week: 1
status: draft — split into per-day files 2026-08-28 (was one combined Lesson-Plan.md)
see_also: Course-Curriculum.md §4 (schedule), §6 (lesson-plan status), §7 item #15 (tool-timing decisions); VoltPop-Workspace.md item #13 (workspace-repo scoping Day 1's account-creation/repo steps assume); Admin-Business-Legal.md §9 (cohort size)
---

# Week 1 — Course Foundations

Two 3-hour classes, Tuesday and Thursday. Day-by-day content lives in
its own file:
- [Day 1 (Tuesday)](./Day1.md)
- [Day 2 (Thursday)](./Day2.md)

This file holds what's shared across both days: framing, learning
objectives, deliverables, materials, and the open items that still need
resolving before Week 1 is final.

**Audience reminder (Course-Curriculum.md §1):** business students, not
developers or engineers. This week is pure environment setup and
orientation — no hardware, no firmware, no graded technical skill yet.
The goal is that every student leaves Day 1 able to actually use the
tools the rest of the course depends on, and leaves Day 2 having made
their first public statement about the program.

**Confirmed, per VoltPop, 2026-08-08: prompt engineering is the only
actual academic content in Week 1 — and it now lives on Day 2** (moved
2026-08-28 when the week was split into two fixed 3-hour classes; see
Day 1's note on why). Everything else — account creation, git basics,
notes-KB setup, portfolio setup — is logistics/setup, not instruction:
run Day 1 in checklist/walk-through mode (get everyone functional,
don't over-explain), then shift register on Day 2 once the setup work
is done.

**Not academic content doesn't mean low priority — per VoltPop,
2026-08-08: "it's vitally important that we get Git and Kiro set up and
configured, as those two tools will be driving 90% of this project."**
Day 1's account creation, git basics, and notes-KB setup are the
highest-stakes part of the week precisely *because* they're setup, not
despite it — every subsequent week depends on students actually having
working git + Kiro access. Getting this right matters more than moving
quickly through it; don't let "checklist mode" above be read as "low
effort."

## Learning objectives

By the end of Week 1, students can:
- Create and access accounts for GitHub and Kiro.
- Explain, at a plain-language level, what a git repository is and why
  the course keeps its own notes in one (not "why version control
  matters for software teams" — "why does *our* class notes live in a
  place like this").
- Locate and use the GitHub Education Git Cheat Sheet as a reference.
- Describe what "prompt engineering and context management" means for
  this course specifically — directing an AI tool with a clear role,
  task, format, and context (the RTFC pattern, formally introduced in
  Week 5 but previewed here).
- Have published a first public LinkedIn post introducing themselves
  and the program.

## Deliverables

- Portfolio & LinkedIn (per the schedule table, Course-Curriculum.md §4)
  — both the group site and each student's individual portfolio
  (confirmed per VoltPop, 2026-08-28), started Day 1
- First Public Post (Day 2)

## Materials / resources

- [GitHub Education Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- GitHub account + class org/repo access (mechanics TBD)
- Kiro account + setup instructions (TBD — depends on Amazon donation status, `Stakeholder-Notes.md`'s Amazon/Kiro profile). Sources checked 2026-08-08: [Kiro CLI setup](https://kiro.dev/docs/cli/setup/), [Kiro Crew installation](https://kiro.dev/docs/crew/installation/), [Kiro authentication methods](https://kiro.dev/docs/getting-started/authentication/).
- Setup/install automation is being built as a separate standalone repo (VoltPop's own account initially, to be transferred later) — see the workspace-repo row in `TODOs-by-Owner.md` (still ☐ unbuilt) and its fuller scoping in `VoltPop-Workspace.md` item #13. **This is the single biggest thing standing between this plan and being run as scripted** — see Day 1's blocking-dependency note.

## Open items — resolve before this week is considered final

1. **Portfolio mechanism isn't fully locked.** Per-group GitHub Pages is
   the current proposal, but whether **Lovable** gets used for that
   site's UI (bringing Lovable back into Day 1 for this one purpose) or
   whether the page starts plain and gets Lovable-polished later (once
   Lovable is actually introduced) is still an open call.
2. **Resolved (per VoltPop, 2026-08-28): group *and* individual
   portfolios, both.** The per-group GitHub Pages site sits alongside
   an individual portfolio for each student, not in place of one — more
   Day 1 setup than the group-only option, but each student leaves with
   their own standalone artifact for résumés/LinkedIn as well as the
   group's.
3. **GitHub org/repo structure for students — still open, but
   substantially informed by existing scoping this file hadn't
   cross-referenced until now (found 2026-08-28): `VoltPop-Workspace.md`
   item #13's "workspace repo."** That item already answers most of
   what this open item was asking: instructor-side provisions org-level
   (per-group repo + Pages scaffold from a template, notes-KB scaffold,
   Kiro steering file), students run a lightweight per-group init
   script. **What's still genuinely open:**
   - The workspace repo itself is unbuilt (`TODOs-by-Owner.md`, ☐) —
     Day 1's account-creation/repo steps depend on it existing.
   - Whether the per-group template stays connected as a live
     `upstream` remote so groups can pull later material updates — the
     **upstream-sync lesson idea** floated 2026-08-28 (per VoltPop:
     "we're going to have to plan out the larger structure... perhaps
     there can be a lesson in pulling upstream changes baked into the
     repo process") — isn't part of item #13's existing scoping and
     needs adding there if adopted, not just noted here. Day 1's notes-
     KB item sketches the mechanism (`git remote add upstream`, later
     `fetch`/`merge`), mirroring this KB's own fork-and-sync workflow.
   - The individual-portfolio repo location (own repo vs. a page within
     the group's, Open Item 2 above) still isn't decided.
   - Exact invite/join mechanics for students landing in their
     already-provisioned group repo (Day 1's account-creation step).
4. **Kiro provisioning — still open (confirmed still unresolved,
   2026-08-28): VoltPop hasn't yet asked Amazon** whether students get
   individual accounts, a shared/classroom license, or something tied
   to the donation ask (`Stakeholder-Notes.md`'s Amazon/Kiro profile).
   Blocks locking how "account creation" runs on Day 1 until asked.
   **Checked 2026-08-28: Kiro's own free student tier
   (kiro.dev/students) doesn't currently cover this.** It's free (1,000
   credits/month for a year, no card required) and signup is per-student
   via GitHub/Google/AWS Builder ID + SheerID enrollment verification —
   but eligibility is restricted to a named list of partner universities
   (ASU, Cal Poly, CSUF, CMU, Georgia Tech, Hampton, NYU, U Chicago, UT
   Austin, U Toronto, U Waterloo) and **VSU isn't on it.** There's also
   no documented instructor/class-wide provisioning path — each student
   verifies individually. Worth asking Amazon directly whether VSU could
   be added to the eligible list, rather than assuming this tier is a
   ready-made answer to the provisioning question.
5. **Resolved (2026-08-28): the original combined plan was over
   budget for the real class length.** Six ~40/20-min blocks in one
   sitting summed to **3h40m against a fixed 3-hour (180 min) class** —
   40 minutes over. Fixed by moving the prompt-engineering block
   (previously Day 1 item 6) to Day 2, which had 120 minutes of slack —
   both days now total exactly 180 minutes with no content cut. **Day 1
   is now fully packed with zero buffer** (unlike Day 2's built-in 80
   minutes), which is a real risk given setup days are exactly where
   things run long — worth a live timing check before trusting it, and
   worth deciding in advance what gets cut/deferred if Day 1 overruns.
