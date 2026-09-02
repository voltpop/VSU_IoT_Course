---
title: Week 7 — Data Flow & Systems Architecture
week: 7
status: draft — scripted 2026-09-02, same depth as Weeks 1–2, 5. Day1.md/Day2.md have real talking points, exercises, and timing; untested live, same caveat as every other drafted week.
see_also: Course-Curriculum.md §1 (judgment-mechanical pattern, build stand-ups), §4 (schedule), §6 (lesson-plan status, MCP-content relocation), §7 items #4, #18; Curriculum/Week5/README.md (hardware this week builds on)
---

# Week 7 — Data Flow & Systems Architecture

Two 3-hour classes, Tuesday and Thursday. **Scripted 2026-09-02** — real
talking points, exercises, and timing, same depth as Weeks 1, 2, and 5.
Still `status: draft`, not final: untested live.

- [Day 1 (Tuesday)](./Day1.md)
- [Day 2 (Thursday)](./Day2.md)

## Where this fits in the schedule

**Week 7 of 15** — Data Flow & Systems Architecture, Mar 2 (Tue) / Mar
4 (Thu). Lead: **VoltPop**. Support: Explay (TBD) (Course-Curriculum.md
§4, full table).

- ← Previous: **Week 6** — Designing the User Experience, Feb 23 (Tue)
  / Feb 25 (Thu). Lead: Builder Tech. *(not yet drafted)*
- → Next: *Spring Break, Mar 9 (Tue) / Mar 11 (Thu) — no classes* — then
  **[Week 8](../Week8/README.md)**, Full Build — Iterations 1 & 2, Mar
  16 (Tue) / Mar 18 (Thu). Lead: VoltPop.

## What we know so far (from Course-Curriculum.md §4)

- **Description:** map the sensor→app data flow/payload; a "proof of
  life" hardware-software integration test.
- **Skill:** AI-Assisted Design & Systems Integration.
- **Deliverables:** System Architecture Diagram; End-to-End Integration
  Test & Post.
- **Tools:** same as prior weeks — no new tools added.

**This topic replaced the old Week 7 content (MCP server design) —
important not to rebuild the wrong thing.** Course-Curriculum.md §6:
the *old* `Week7_MCP_Server_Design_Prompts.md` file (in VoltPop's
external working files, never pulled into this repo) is being
**relocated to Week 8**, where MCP integration now replaces the old
"API integration" framing. This week needs genuinely new content built
around payload/data-flow design and a proof-of-life integration build
— following the same 4D+RTFC pattern (§7 item #4).

**Build stand-up (Course-Curriculum.md §1, §7 item #18):** teams have
had two weeks since Week 5's hardware work (Week 6 is UX design, not
technical) — Day 1 can reasonably open with one, reflecting on where
hardware/wiring stands going into this integration-focused week.

## Learning objectives (draft — refine once days are scripted)

- Diagram their system's actual sensor→app data flow (a System
  Architecture Diagram), not just the conceptual sense/connect/act loop
  from Week 2.
- Define a concrete payload format for their sensor data.
- Achieve a "proof of life" — some real signal moving from hardware to
  app, even if minimal.
- Apply 4D to the architecture judgment calls (what should the payload
  include? what's the right integration approach?) and RTFC to
  generating the actual integration code.

## Deliverables

- System Architecture Diagram
- End-to-End Integration Test & Post

## Materials / resources

- **Kiro** generates the System Architecture Diagram directly (changed
  2026-09-02, per VoltPop — see Open Item 3), same pattern as Week 5's
  wiring diagram. No TLDraw needed this week.
- **webhook.site** (free, no signup) as the Day 2 placeholder receiving
  endpoint.
- Hardware/firmware from Week 5 must actually be working — this week
  assumes that, not re-teaches it.
- Classroom Wi-Fi with outbound internet access (confirmed available,
  2026-09-02, per VoltPop — see Open Item 5).

## Open items — resolve before this is fully final

1. **Resolved, 2026-09-02:** Day1.md/Day2.md now have real talking
   points, a data-flow/payload-design exercise (4D-scaffolded), an
   integration build session (RTFC-scaffolded), and timing — same depth
   as Weeks 1, 2, and 5. **Still needs a live timing check.**
2. **Built as new content, not adapted from an existing file** — per
   Course-Curriculum.md §6: unlike Week 8 (which has old MCP content to
   relocate), Week 7 had nothing to adapt from.
3. **Changed, 2026-09-02 (per VoltPop) — TLDraw replaced with Kiro for
   the System Architecture Diagram.** Same pattern as Week 5's wiring
   diagram: Kiro generates the labeled diagram directly from a prompt
   (RTFC-scaffolded), rather than teams hand-drawing it. **Raises a
   broader question, not yet resolved:** does TLDraw's actual
   introduction point — **Week 3** (Course-Curriculum.md §4's `+ TL
   Draw`, Builder Tech-led, not yet drafted) — still need it, now that
   Kiro can generate diagrams directly? Not decided here; Week 3 is
   Builder Tech's to draft, this just flags the question for whoever
   drafts it. See also Course-Curriculum.md §7 item #14 (tools-trim
   goal) and Week 5's parallel Canva reconsideration.
4. **Support-party involvement (Explay) is marked TBD in the schedule
   table itself** — not just a KB gap, the schedule row says "Explay
   (TBD)." Still open.
5. **Resolved, 2026-09-02 (per VoltPop) — VSU network access for the
   Day 2 integration exercise.** Classroom Wi-Fi will have outbound
   internet access, confirmed. This was the same underlying question as
   `TODOs-by-Owner.md`'s "Confirm classroom/lab space for hardware weeks
   + network access" row (`Admin-Business-Legal.md` §7) — that broader
   row isn't necessarily fully closed by this, but Week 7's specific
   dependency (ESP32 → internet, for the webhook.site proof-of-life
   test) is confirmed.
