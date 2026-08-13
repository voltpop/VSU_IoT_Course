---
title: Week 1 — Course Foundations Lesson Plan
week: 1
dates: Jan 19 (Tue) / Jan 21 (Thu)
status: draft — new as of 2026-08-08, replaces a lost prior version
see_also: Course-Curriculum.md §4 (schedule), §6 (lesson-plan status), §7 item #15 (tool-timing decisions)
---

# Week 1 — Course Foundations

**Audience reminder (Course-Curriculum.md §1):** business students, not
developers or engineers. This week is pure environment setup and
orientation — no hardware, no firmware, no graded technical skill yet.
The goal is that every student leaves Day 1 able to actually use the
tools the rest of the course depends on, and leaves Day 2 having made
their first public statement about the program.

**Confirmed, per VoltPop, 2026-08-08: prompt engineering is the only
actual academic content in Day 1.** Everything else — account creation,
git basics, notes-KB setup, portfolio setup — is logistics/setup, not
instruction. Worth teaching Day 1 with that distinction explicit: run
items 1–5 below in checklist/walk-through mode (get everyone
functional, don't over-explain), then shift register for item 6 into
actual teaching mode.

**Not academic content doesn't mean low priority — per VoltPop,
2026-08-08: "it's vitally important that we get Git and Kiro set up and
configured, as those two tools will be driving 90% of this project."**
Items 2–4 (account creation, git basics, notes-KB setup) are the
highest-stakes part of Day 1 precisely *because* they're setup, not
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

## Day 1 (Tue, Jan 19)

*Items 1–5: setup/logistics, checklist mode. Item 6: the day's one
actual academic content block.*

**1. Program intro** *(setup)* (~20 min)
Plain-language overview of the semester: what the course is (a
one-semester "toe-dip" into IoT + AI-assisted development), who's
teaching it, what the end goal looks like (Career Day, Week 14), and
that this is exposure to a way of working, not a certification.

**2. Account creation — GitHub and Kiro** *(setup)* (~40 min)
- GitHub: create an account, verify email, join the class organization/
  repo (mechanics TBD — see Open Items below).
- **Kiro authenticates via GitHub OAuth — confirmed supported
  (kiro.dev/docs/getting-started/authentication, checked 2026-08-08):**
  Kiro's own sign-in flow lets students "choose the provider [GitHub],
  authenticate in your browser, and authorize the Kiro app" — so
  students sign into Kiro with the *same* GitHub account, not a second
  credential. This is a real, documented feature, not something this
  program has to build itself.
- **Install commands, confirmed from Kiro's own docs (2026-08-08):**
  - Kiro CLI: `curl -fsSL https://cli.kiro.dev/install | bash` (macOS/
    Linux) or `irm 'https://cli.kiro.dev/install.ps1' | iex` (Windows
    PowerShell); verify with `kiro-cli doctor`, re-authenticate with
    `kiro-cli login`.
  - Kiro Crew: `kirocrew setup` (interactive wizard for data dir,
    agent, credentials), `kirocrew doctor` (verify), `kirocrew gateway`
    (starts the local server). **Caveat:** Crew's own docs describe
    "device-code sign-in" during first launch, not explicitly GitHub
    OAuth the way the base Kiro CLI is documented — worth confirming
    hands-on whether Crew's credential step actually reuses the same
    GitHub session, rather than assuming it does.
- Kiro: confirm access, quick orientation to its interface as "the tool
  you'll talk to all semester."
- **Not created here, per the 2026-08-08 decision:** ChatGPT, Claude,
  Codex, or Gemini accounts — Kiro is the program's AI tool going
  forward (Course-Curriculum.md §7 item #15).

**3. Git/GitHub basics** *(setup)* (~40 min)
- Hand out the GitHub Education [Git Cheat
  Sheet](https://education.github.com/git-cheat-sheet-education.pdf).
- Plain-language walkthrough of the handful of commands/concepts
  students will actually touch this semester: clone, add, commit, push,
  pull, and what a repo/branch is at a conceptual level. No deep git
  internals — recipe-following, same philosophy as the hardware weeks.
- Frame this explicitly as "the same way our own class notes are kept"
  — not an abstract skill, but the thing they're about to do next.

**4. Set up the class notes knowledge base** *(setup)* (~40 min)
- Each group clones/sets up their own notes repo.
- Configure Kiro to front-end that repo — this is what "talking to your
  notes" will look like all semester, not a one-time setup step.
- First real use: write a one-paragraph "who we are" note into the repo
  and commit it — the first hands-on git action of the course.

**5. Portfolio setup** *(setup)* (~40 min)
- **Mechanism: a per-group GitHub Pages site** (proposed 2026-08-08,
  not yet fully locked — see Open Items below).
- Each group stands up a bare GitHub Pages site off their repo. Content
  can be minimal today (group name, member names, one sentence about
  what they're building) — this gets built out across the semester, not
  finished today.

**6. Prompt engineering & context management intro** *(academic content)* (~40 min)
- First hands-on use of Kiro: a short guided exercise giving it a role,
  a task, a format, and context (previewing RTFC, formally named in
  Week 5) to generate something small and low-stakes (e.g., a short
  bio paragraph for the portfolio site above).
- Point: the AI is a tool you direct with a clear ask, not a search box.

## Day 2 (Thu, Jan 21)

**1. Recap + troubleshooting** (~20 min)
Fix anything from Day 1 that didn't stick — account access, repo clone
issues, Kiro connectivity. Expect this to run long for some students;
budget for it rather than rushing ahead.

**2. First public LinkedIn post** (~40 min)
- Each student publishes a short LinkedIn post introducing themselves
  and the program (this is the semester's first public deliverable).
- Discuss, briefly, why this matters for the portfolio/Career Day
  throughline (Course-Curriculum.md §8) — not just an assignment for
  its own sake.

**3. Buffer / open work time** (~remaining time)
Groups continue setting up their portfolio site and notes repo; this is
intentionally not fully scripted, since setup pacing will vary a lot by
how comfortable each group is with the tools.

## Deliverables

- Portfolio & LinkedIn (per the schedule table, Course-Curriculum.md §4)
- First Public Post

## Materials / resources

- [GitHub Education Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- GitHub account + class org/repo access (mechanics TBD)
- Kiro account + setup instructions (TBD — depends on Amazon donation status, `Stakeholder-Notes.md`'s Amazon/Kiro profile). Sources checked 2026-08-08: [Kiro CLI setup](https://kiro.dev/docs/cli/setup/), [Kiro Crew installation](https://kiro.dev/docs/crew/installation/), [Kiro authentication methods](https://kiro.dev/docs/getting-started/authentication/).
- Setup/install automation is being built as a separate standalone repo (VoltPop's own account initially, to be transferred later) — see the new workspace-repo item in `TODOs-by-Owner.md`.

## Open items — resolve before this plan is considered final

1. **Portfolio mechanism isn't fully locked.** Per-group GitHub Pages is
   the current proposal, but whether **Lovable** gets used for that
   site's UI (bringing Lovable back into Day 1 for this one purpose) or
   whether the page starts plain and gets Lovable-polished later (once
   Lovable is actually introduced) is still an open call.
2. **Group vs. individual portfolio** — unconfirmed whether "group"
   replaces an individual portfolio outright or sits alongside one.
3. **GitHub org/repo structure for students** — how groups actually get
   their own repos (a class GitHub organization? individual repos under
   each student's account? a template repo they fork?) isn't decided.
   This affects the account-creation walkthrough directly.
4. **Kiro provisioning** — whether students get individual Kiro
   accounts, a shared/classroom license, or something tied to the
   Amazon donation ask (`Stakeholder-Notes.md`) isn't resolved, and
   changes how "account creation" actually runs on Day 1.
5. **Density confirmed as intentional, not a problem to trim (per
   VoltPop, 2026-08-08): "Day 1 will be a long day of setting up
   accounts and learning to use the tools of the trade (GitHub and
   AI)."** Six ~40-minute blocks across account creation, git basics,
   notes-KB setup, portfolio setup, and prompt engineering is genuinely
   a lot for one day with a largely non-technical audience — but that's
   accepted as the actual shape of Day 1, not flagged as something to
   cut down. Still worth a real walkthrough/timing check to see how the
   blocks actually run, just not to justify shortening the day.
