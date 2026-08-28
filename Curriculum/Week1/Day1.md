---
title: Week 1, Day 1 — Course Foundations (Tuesday)
week: 1
day: 1
date: Jan 19 (Tue)
duration: 3 hours (180 min), fully packed — no buffer block
status: draft
see_also: ./README.md (shared framing, deliverables, open items); ./Day2.md
---

# Week 1, Day 1 (Tue) — Setup & Tooling

*All setup/logistics, checklist mode — no academic content today. See
[README](./README.md) for why: prompt engineering, Week 1's one real
teaching block, was moved to [Day 2](./Day2.md) so this day's five
setup items fit the actual 3-hour class length without cutting
anything.*

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

**1. Program intro** *(~20 min)*
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

**2. Account creation — GitHub and Kiro** *(~40 min)*

Per-student sequence:
1. **GitHub account.** Go to github.com/join, sign up with a personal
   (not university) email — one they'll keep after graduation, since
   the portfolio repo/site is meant to outlive the course. Verify
   email. Turn on 2FA (quick, worth the habit).
2. **Join the group repo.** Once the workspace repo exists (see the
   blocking-dependency note above), each group's repo is already
   provisioned org-side from a template; students accept an invite link
   the instructor sends (or redeem a join-code the init script
   consumes — exact mechanic TBD, part of README Open Item 3).
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

**3. Git/GitHub basics** *(~40 min)*
- Hand out the GitHub Education [Git Cheat
  Sheet](../Assets/git-cheat-sheet-education.pdf) — mirrored locally in
  `Assets/` for distribution.
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

**4. Set up the class notes knowledge base** *(~40 min)*
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
- **Proposed, not yet locked (see README Open Item 3): upstream sync.**
  If the template-repo/upstream-sync direction is adopted, this is also
  where each group's repo gets an `upstream` remote pointed at the
  class template (`git remote add upstream <template-url>`) — so that
  when instructors push updates later in the semester (e.g. Week 5's
  firmware starter files), groups pull them in with
  `git fetch upstream && git merge upstream/main`. Introduce the remote
  today; save the actual sync exercise for whenever there's a real
  update worth pulling, so it's a genuine skill exercise and not a
  no-op demo.

**5. Portfolio setup** *(~40 min)*
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
  within the group's, are both still open (see README Open Items 1 and
  3). Don't build today's walkthrough around a tool/location that might
  not be the final answer.
- **Leave the bio placeholder empty for now.** Writing it is Day 2's
  first exercise, right after the prompt-engineering lesson — don't
  pre-empt it today.

**End of Day 1.** No academic content block today — that shifted to
[Day 2](./Day2.md) to keep this day inside the real 3-hour limit (see
README Open Item 5). If everything above ran on time, there's no slack
left; anything unfinished rolls into Day 2's recap/troubleshooting.
