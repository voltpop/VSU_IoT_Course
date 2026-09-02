---
title: Week 8 — Full Build, Iterations 1 & 2
week: 8
status: draft — scripted 2026-09-02, same depth as Weeks 1, 2, 5, 7. Day1.md/Day2.md have real talking points, exercises, and timing; untested live, same caveat as every other drafted week.
see_also: Course-Curriculum.md §1 (build stand-ups), §4 (schedule — lead/tools discrepancies not yet in the live sheet), §6 (lesson-plan status, MCP-content relocation), §7 items #5, #8, #18
---

# Week 8 — Full Build, Iterations 1 & 2

Two 3-hour classes, Tuesday and Thursday. **Scripted 2026-09-02** — real
talking points, exercises, and timing, same depth as Weeks 1, 2, 5, and
7. Still `status: draft`, not final: untested live.

- [Day 1 (Tuesday)](./Day1.md)
- [Day 2 (Thursday)](./Day2.md)

## Where this fits in the schedule

**Week 8 of 15** — Full Build — Iterations 1 & 2, Mar 16 (Tue) / Mar 18
(Thu). Lead: **VoltPop** *(confirmed at the 2026-07-31 meeting, but
**not yet entered into the live shared schedule sheet**, which as of
the last check still shows Explay as Lead and "Integrate API
connections" instead of the MCP swap below — Course-Curriculum.md §4)*.
Support: Explay.

- ← Previous: **[Week 7](../Week7/README.md)** — Data Flow & Systems
  Architecture, Mar 2 (Tue) / Mar 4 (Thu). Lead: VoltPop. *(preceded by
  Spring Break, Mar 9/11 — no classes)*
- → Next: **[Week 9](../Week9/README.md)** — Full Build — Iterations 3
  & 4, Mar 23 (Tue) / Mar 25 (Thu). Lead: **VoltPop** (reassigned from
  Explay, 2026-08-28 — Course-Curriculum.md §4 footnote 1). Support:
  All.

## What we know so far (from Course-Curriculum.md §4)

- **Description:** full app build; **MCP integration** (replacing the
  prior "API integration" framing); hardware integration; submit
  Iteration 1 and Iteration 2.
- **Skill:** AI-Assisted Development & Full-Stack Integration.
- **Deliverables:** Iteration 1; Iteration 2 & Post.
- **Tools added this week:** Postman.

**MCP content: built fresh, not adapted (2026-09-02, per VoltPop) —
Course-Curriculum.md §6, §7 item #5.** The *old*
`Week7_MCP_Server_Design_Prompts.md` (built for the earlier "Week 7 =
MCP server design" topic, before Week 7 got reassigned to Data Flow &
Systems Architecture) couldn't be located — confirmed lost, same as the
Week 5 and Week 7 external files. **New framing (per VoltPop, 2026-09-02):**
this week centers on building a real MCP server and closing the
**sense-react loop** first introduced conceptually in Week 2 and made
technical in Week 7 — Iteration 1 replaces Week 7's webhook.site
placeholder with a real server (sense), Iteration 2 extends it with a
"react" capability (Course-Curriculum.md §1's sense-and-actuate
direction, encouraged not mandatory).

**Build stand-up (Course-Curriculum.md §1, §7 item #18):** this is
exactly the kind of week the pattern was designed for — an iterative,
multi-day build with real recurring blockers. Open **both** days with
one.

## Learning objectives

- Design an MCP server's tool set as a 4D judgment exercise, then
  build it with RTFC.
- Replace Week 7's webhook.site placeholder with a real, team-built
  server (Iteration 1).
- Extend the server with a "react" tool, closing the sense-react loop
  (Iteration 2) — physical actuation where a project supports it, a
  meaningful non-physical reaction otherwise.
- Use Postman to test server endpoints directly before layering
  agent- or firmware-driven calls on top.
- Submit two working iterations, incorporating stand-up-surfaced fixes
  between them.

## Deliverables

- Iteration 1
- Iteration 2 & Post

## Materials / resources

- **Postman** (new tool this week) — testing MCP server endpoints.
- **ngrok** — design call made in this draft, not yet confirmed (see
  Open Item 5): exposes the team's locally-run MCP server with a public
  URL, the same low-friction precedent as Week 7's webhook.site.

## Open items — resolve before this is fully final

1. **Resolved, 2026-09-02:** Day1.md/Day2.md now have real talking
   points, the MCP-server design (4D) and build (RTFC) exercises, the
   react/closing-the-loop exercise, and timing — same depth as Weeks 1,
   2, 5, and 7. **Still needs a live timing check.**
2. **Resolved, 2026-09-02 — old Week 7 MCP content confirmed lost.**
   Built fresh per VoltPop's new sense-react-loop framing rather than
   adapted from the old file, which couldn't be located.
3. **Live shared schedule sheet still needs updating** (Course-
   Curriculum.md §4, §7 item #8) — Lead should say VoltPop, not Explay;
   Tools/Description should reflect the MCP swap, not "Integrate API
   connections." No Google Sheets access available in this session to
   make that edit directly — flagged, not done.
4. **Resolved, 2026-09-02 — Week 9's division of labor.** The original
   VoltPop/Explay split question is superseded by the 2026-08-28
   reassignment (Course-Curriculum.md §4 footnote 1): Week 9 is now
   VoltPop-led solo, Support: All. No division-of-labor question
   remains between VoltPop and Explay specifically.
5. **New, 2026-09-02 — ngrok as the MCP server's public-exposure tool
   is a design call, not confirmed.** Same pattern as Week 5's
   Kiro-vs-Canva and Week 7's Kiro-vs-TLDraw calls in this draft — a
   reasonable default, not something previously decided anywhere in
   this KB. Revert if a different approach (a real cloud deployment,
   for instance) is actually intended.
