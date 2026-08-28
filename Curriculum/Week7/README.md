---
title: Week 7 — Data Flow & Systems Architecture
week: 7
status: skeleton — created 2026-08-28, structure only. Day1.md/Day2.md need actual talking points, exercises, and timing before this is teachable (same depth as Weeks 1–2).
see_also: Course-Curriculum.md §1 (judgment-mechanical pattern, build stand-ups), §4 (schedule), §6 (lesson-plan status, MCP-content relocation), §7 items #4, #18; Curriculum/Week5/README.md (hardware this week builds on)
---

# Week 7 — Data Flow & Systems Architecture

Two 3-hour classes, Tuesday and Thursday. **This is a skeleton, not a
full lesson plan** — structure, known context, and open questions only.

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

- TLDraw (introduced Week 3) is the likely tool for the architecture
  diagram, but this hasn't been confirmed anywhere in this KB.
- Hardware/firmware from Week 5 must actually be working — this week
  assumes that, not re-teaches it.

## Open items — resolve before this is more than a skeleton

1. **No actual day-by-day content yet.** Day1.md/Day2.md need real
   talking points, a data-flow/payload-design exercise, an integration
   build session, and timing — same depth as Weeks 1–2.
2. **This is new content, not adapted from an existing file** —
   confirmed per Course-Curriculum.md §6: unlike Week 8 (which has old
   MCP content to relocate), Week 7 has nothing to adapt from. Building
   it is a full design task, not a rewrite.
3. **Diagramming tool unconfirmed.** TLDraw is the natural candidate
   (introduced Week 3) but nothing in this KB actually says Week 7 uses
   it for the System Architecture Diagram.
4. **Support-party involvement (Explay) is marked TBD in the schedule
   table itself** — not just a KB gap, the schedule row says "Explay
   (TBD)."
