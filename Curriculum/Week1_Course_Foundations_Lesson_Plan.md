---
title: Week 1 — Course Foundations Lesson Plan
week: 1
dates: Jan 19 (Tue) / Jan 21 (Thu)
status: draft — new as of 2026-08-08, replaces a lost prior version
see_also: Course-Curriculum.md §4 (schedule), §6 (lesson-plan status), §7 item #15 (tool-timing decisions); VoltPop-Workspace.md item #13 (workspace-repo scoping this day's account-creation/repo steps assume); Admin-Business-Legal.md §9 (cohort size)
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

**Blocking dependency — confirm before running this day as scripted:**
everything in items 2–4 below assumes the **workspace repo**
(`TODOs-by-Owner.md`, still an unchecked ☐ item; scoped in
`VoltPop-Workspace.md` item #13) already exists — instructor-side
org-level provisioning of a per-group repo (from a template, with the
notes-KB scaffold and a Kiro steering file already in it) plus a
per-group init script students run to install/authenticate tooling.
**That repo hasn't been built yet.** Either build it before this runs,
or these blocks fall back to a slower, fully-manual walkthrough (each
step below notes the manual fallback where it differs).

**1. Program intro** *(setup)* (~20 min)
Plain-language overview of the semester: what the course is (a
one-semester "toe-dip" into IoT + AI-assisted development), who's
teaching it, what the end goal looks like (Career Day, Week 14), and
that this is exposure to a way of working, not a certification.

Suggested talking points, in order:
1. Welcome, and name who's in the room (Course-Curriculum.md §4: Week 1
   lead is shared across all three teaching parties).
2. One-sentence course description: *"In one semester, small teams
   build a working IoT device and the app around it, using AI tools to
   do a lot of the heavy lifting — the point is learning to* **direct**
   *AI and hardware toward a real problem, not becoming an engineer."*
3. Name the destination up front: Career Day (Week 14) — a live pitch
   of a working device + app, plus a portfolio site each student can
   point to afterward.
4. Set the Day 1 expectation explicitly: *"today is almost entirely
   account setup — it will feel slow at points, that's expected, and
   everyone leaves with working tools."*
5. Confirm teams. Cohort is capped at 60 students in teams of 3–4
   (Admin-Business-Legal.md §9) — roughly 15–20 teams. **This lesson
   plan assumes teams are already assigned before Day 1**; the actual
   assignment mechanism (self-select vs. instructor-assigned) isn't
   decided anywhere in this KB yet — flag and resolve separately if it
   isn't already handled elsewhere.

**2. Account creation — GitHub and Kiro** *(setup)* (~40 min)

Per-student sequence:
1. **GitHub account.** Go to github.com/join, sign up with a personal
   (not university) email — one they'll keep after graduation, since
   the portfolio repo/site is meant to outlive the course. Verify
   email. Turn on 2FA (quick, worth the habit).
2. **Join the group repo.** Once the workspace repo exists (see the
   blocking-dependency note above), each group's repo is already
   provisioned org-side from a template; students accept an invite link
   the instructor sends (or redeem a join-code the init script
   consumes — exact mechanic TBD, part of Open Item 3 below).
   **Manual fallback if the workspace repo isn't ready:** instructor
   creates one repo per team by hand ahead of time and adds each
   student as a collaborator individually — slower, but unblocks Day 1.
3. **Kiro account — via GitHub OAuth, confirmed supported
   (kiro.dev/docs/getting-started/authentication, checked 2026-08-08):**
   on Kiro's sign-in screen, choose "Continue with GitHub," authenticate
   in the browser, authorize the Kiro app. Same GitHub account, no
   second credential to manage.
4. **Install and authenticate the CLI tooling** — ideally by running
   the group's init script from the workspace repo (per
   `VoltPop-Workspace.md` item #13, this script wraps the steps below);
   run manually if the script isn't ready yet:
   - Kiro CLI: `curl -fsSL https://cli.kiro.dev/install | bash`
     (macOS/Linux) or `irm 'https://cli.kiro.dev/install.ps1' | iex`
     (Windows PowerShell); confirm with `kiro-cli doctor`, and
     `kiro-cli login` if it isn't already authenticated.
   - Kiro Crew: `kirocrew setup` (interactive wizard for data dir,
     agent, credentials), then `kirocrew doctor` to verify, then
     `kirocrew gateway` to start the local server. **Caveat, still
     unverified hands-on:** Crew's own docs describe a "device-code
     sign-in" at first launch rather than explicitly confirming it
     reuses the GitHub session from step 3 — check this live with a
     real student machine before Day 1, don't assume it just works.
5. **Orientation.** Open Kiro, point out the chat pane, confirm it can
   see the group's repo. Frame it once, plainly: *"this is the tool
   you'll talk to all semester."*

**Not created here, per the 2026-08-08 decision:** ChatGPT, Claude,
Codex, or Gemini accounts — Kiro is the program's AI tool going forward
(Course-Curriculum.md §7 item #15).

**3. Git/GitHub basics** *(setup)* (~40 min)
- Hand out the GitHub Education [Git Cheat
  Sheet](https://education.github.com/git-cheat-sheet-education.pdf).
- Plain-language concept pass, no deep internals (same recipe-following
  philosophy as the hardware weeks): a **repo** is a shared folder with
  history, a **commit** is a saved checkpoint, **push/pull** sync your
  copy with the shared one on GitHub.
- Live demo, instructor screen-shares and narrates while each group
  follows along on their own machine:
  1. `git clone <group-repo-url>`
  2. Open the cloned folder — point out the notes-KB scaffold and Kiro
     steering file that are already there (provisioned org-side, see
     item 2's blocking-dependency note).
  3. Make a trivial edit to a scratch file, then `git status` (see what
     changed), `git add <file>`, `git commit -m "..."`, `git push`.
  4. `git pull` — explain *why* you'd run this ("a teammate changed
     something and you want their update").
- Frame this explicitly as "the same way our own class notes are kept"
  — not an abstract skill, but the thing they're about to do next in
  item 4.

**4. Set up the class notes knowledge base** *(setup)* (~40 min)
- Confirm the notes-KB scaffold from item 3's clone is there, and that
  Kiro's steering file (provisioned org-side) already points Kiro at
  it — nothing left to wire up manually if the workspace repo did its
  job.
- **Exercise:** as a group, open Kiro and write a one-paragraph "who we
  are" note (team name, members, one sentence on what excites them
  about the course) into the notes-KB. Save it, then `git add` /
  `commit` / `push` — the first hands-on git action of the course that
  isn't a throwaway scratch edit.
- Call out explicitly: this is the same fork-and-commit workflow this
  program's own staff KB runs on (`AGENTS.md`) — *"you're doing what we
  do."*
- **Proposed, not yet locked (see Open Item 3): upstream sync.** If the
  template-repo/upstream-sync direction is adopted, this is also where
  each group's repo gets an `upstream` remote pointed at the class
  template (`git remote add upstream <template-url>`) — so that when
  instructors push updates later in the semester (e.g. Week 5's
  firmware starter files), groups pull them in with
  `git fetch upstream && git merge upstream/main`. Introduce the remote
  today; save the actual sync exercise for whenever there's a real
  update worth pulling, so it's a genuine skill exercise and not a
  no-op demo.

**5. Portfolio setup** *(setup)* (~40 min)
- **Mechanism: a per-group GitHub Pages site, plus an individual
  portfolio for each student (confirmed per VoltPop, 2026-08-28)** —
  the group site doesn't replace an individual one.
- **Group site, step by step:**
  1. In the group repo, add a minimal `index.html` (repo root or a
     `docs/` folder).
  2. GitHub → repo **Settings → Pages** → Source: *Deploy from a
     branch* → `main` → `/ (root)` or `/docs` → Save.
  3. Confirm the published `github.io` URL loads (can take a couple
     minutes the first time — don't panic if it's not instant).
  4. Content today: group name, member names, one sentence about what
     they're building. Expand across the semester, not today.
- **Individual site:** same GitHub Pages mechanism in principle, but
  **run this block plain (no Lovable) for now** — whether Lovable
  styles this later, and whether it lives in its own repo or as a page
  within the group's, are both still open (see Open Items 1 and 3)
  below. Don't build today's walkthrough around a tool/location that
  might not be the final answer.

**6. Prompt engineering & context management intro** *(academic content)* (~40 min)
Register shift here: from checklist mode to actual teaching. Core idea:
the AI is a tool you *direct* with a clear ask, not a search box —
previewing RTFC (Role, Task, Format, Context), formally named in Week
5.

Guided exercise, demo first then per-group:
1. **Bad-prompt example** (show live): *"write me a bio."* — call out
   how generic/rambling the result is, and that this is what happens
   with no role, task, format, or context given.
2. **Good-prompt example**, narrating each RTFC piece aloud as you
   build it: *"You're a [Role: concise, friendly bio writer]. [Task:
   write a 3-sentence bio introducing me and my team's project for my
   portfolio site]. [Format: plain text, first person, no headers].
   [Context: I'm a business student in a semester-long IoT/AI program;
   my team is building ___; keep it approachable, not corporate]."*
3. Each group runs their own version through Kiro and drops the result
   into their portfolio site's bio placeholder from item 5.
4. **Debrief question:** *"what changed between the bad prompt and the
   good one, and why did that change the output?"* — the point isn't
   the bio itself, it's noticing that specificity is what moved the
   needle.

## Day 2 (Thu, Jan 21)

**1. Recap + troubleshooting** (~20 min)
Don't just ask "anything broken?" — walk the room checking the specific
failure points Day 1 is most likely to leave behind:
- GitHub email not yet verified.
- Kiro authorized via OAuth in the browser, but the CLI never
  authenticated (`kiro-cli login` not actually run).
- Repo cloned but no push access (invite never accepted), or never
  cloned at all.
- GitHub Pages site not live yet (first publish can lag a few minutes,
  easy to mistake for broken).

Expect this to run long for some groups; budget for it rather than
rushing ahead, and treat item 2 below as staggered/interruptible rather
than needing the whole room in lockstep.

**2. First public LinkedIn post** (~40 min)
- Each student publishes a short LinkedIn post introducing themselves
  and the program — the semester's first public deliverable.
- Suggested structure (a talking point, not a rigid template): who you
  are, one line naming the program, one line on what you're excited to
  build. Check `Press-Kit-Content.md` for whether the program has an
  established LinkedIn presence/hashtag to tag.
- Optional: reuse Day 1 item 6's RTFC pattern with Kiro to draft a first
  pass, then have the student personalize it before posting — the same
  skill, immediately reinforced with a real public stake.
- **No-PII reminder is about this KB, not personal posts** — students
  posting publicly about themselves is expected and fine; the rule
  (`AGENTS.md`) only bars putting personal/student info back into the
  shared class notes-KB repo.
- Each group logs their post URL(s) in their own notes-KB entry — the
  day's second hands-on git commit.
- Discuss, briefly, why this matters for the portfolio/Career Day
  throughline (Course-Curriculum.md §8) — not just an assignment for
  its own sake.

**3. Buffer / open work time** (~remaining time)
Not idle time — an instructor circulation checklist. Confirm every
group has: (a) a working repo clone, (b) Kiro authenticated end to end,
(c) a live (even if bare) group portfolio page, (d) a published
LinkedIn post. This is also the natural moment to *note* (not
necessarily fix live) anything that surfaces as evidence bearing on the
Open Items below — e.g., a group's snag that's really a sign one of the
pending decisions needs to go a particular way.

## Deliverables

- Portfolio & LinkedIn (per the schedule table, Course-Curriculum.md §4)
  — both the group site and each student's individual portfolio
  (confirmed per VoltPop, 2026-08-28), started today
- First Public Post

## Materials / resources

- [GitHub Education Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- GitHub account + class org/repo access (mechanics TBD)
- Kiro account + setup instructions (TBD — depends on Amazon donation status, `Stakeholder-Notes.md`'s Amazon/Kiro profile). Sources checked 2026-08-08: [Kiro CLI setup](https://kiro.dev/docs/cli/setup/), [Kiro Crew installation](https://kiro.dev/docs/crew/installation/), [Kiro authentication methods](https://kiro.dev/docs/getting-started/authentication/).
- Setup/install automation is being built as a separate standalone repo (VoltPop's own account initially, to be transferred later) — see the workspace-repo row in `TODOs-by-Owner.md` (still ☐ unbuilt) and its fuller scoping in `VoltPop-Workspace.md` item #13. **This is the single biggest thing standing between this plan and being run as scripted** — see the blocking-dependency note at the top of Day 1.

## Open items — resolve before this plan is considered final

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
   group's. Day 1 item 5 and the Deliverables section need the
   individual-portfolio step added, not just the group site.
3. **GitHub org/repo structure for students — still open, but
   substantially informed by existing scoping this file hadn't
   cross-referenced until now (found 2026-08-28): `VoltPop-Workspace.md`
   item #13's "workspace repo."** That item already answers most of
   what this open item was asking: instructor-side provisions org-level
   (per-group repo + Pages scaffold from a template, notes-KB scaffold,
   Kiro steering file), students run a lightweight per-group init
   script. **What's still genuinely open:**
   - The workspace repo itself is unbuilt (`TODOs-by-Owner.md`, ☐) —
     this whole day's account-creation/repo steps (items 2–4 above)
     depend on it existing.
   - Whether the per-group template stays connected as a live
     `upstream` remote so groups can pull later material updates — the
     **upstream-sync lesson idea** floated 2026-08-28 (per VoltPop:
     "we're going to have to plan out the larger structure... perhaps
     there can be a lesson in pulling upstream changes baked into the
     repo process") — isn't part of item #13's existing scoping and
     needs adding there if adopted, not just noted here. Item 4 above
     sketches the mechanism (`git remote add upstream`, later
     `fetch`/`merge`), mirroring this KB's own fork-and-sync workflow.
   - The individual-portfolio repo location (own repo vs. a page within
     the group's, Open Item 2 above) still isn't decided.
   - Exact invite/join mechanics for students landing in their
     already-provisioned group repo (Day 1 item 2, step 2).
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
5. **Density confirmed as intentional, not a problem to trim (per
   VoltPop, 2026-08-08): "Day 1 will be a long day of setting up
   accounts and learning to use the tools of the trade (GitHub and
   AI)."** Six ~40-minute blocks across account creation, git basics,
   notes-KB setup, portfolio setup, and prompt engineering is genuinely
   a lot for one day with a largely non-technical audience — but that's
   accepted as the actual shape of Day 1, not flagged as something to
   cut down. Still worth a real walkthrough/timing check to see how the
   blocks actually run, just not to justify shortening the day.
