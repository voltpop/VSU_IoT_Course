---
title: Week 2 — Understanding Systems & IoT
week: 2
status: draft — split into per-day files 2026-08-28 (was one combined Lesson-Plan.md, mirroring Week 1's split)
see_also: Course-Curriculum.md §1 (curriculum philosophy, judgment/mechanical pattern), §4 (schedule), §5 finding #4 & §7 item #13 (regional-focus gap this plan re-introduces), §8 (stakeholder stakes), §6 (lesson-plan status); Admin-Business-Legal.md §6 (hardware kit quantities); Curriculum/Week1/README.md (tooling this week assumes is already working); Curriculum/Week1/Presentations/Prompting_Frameworks.md (4D and RTFC, reused this week rather than re-explained)
---

# Week 2 — Understanding Systems & IoT

Two 3-hour classes, Tuesday and Thursday. Day-by-day content lives in
its own file:
- [Day 1 (Tuesday)](./Day1.md)
- [Day 2 (Thursday)](./Day2.md)

This file holds what's shared across both days: framing, learning
objectives, deliverables, materials, and the open items that still need
resolving before Week 2 is final.

## Where this fits in the schedule

**Week 2 of 15** — Understanding Systems & IoT, Jan 26 (Tue) / Jan 28
(Thu). Lead: VoltPop (Course-Curriculum.md §4, full table).

- ← **Previous: [Week 1](../Week1/README.md)** — Course Kickoff,
  Jan 19 (Tue) / Jan 21 (Thu). Lead: all three teaching parties.
- → **Next: Week 3** — Problem & User Discovery, Feb 2 (Tue) / Feb 4
  (Thu). Lead: Builder Tech. *(not yet drafted — no directory yet.)*

**Audience reminder (Course-Curriculum.md §1):** still business
students, not developers or engineers. This is the course's first real
academic content week (Skill: **Systems Thinking**), but hardware stays
purely exploratory — actual wiring/firmware doesn't start until Week 5.
Day 1's "device tinkering" is a motivator, not instruction.

**Prerequisite:** every team has working GitHub + Kiro access and a
functioning notes-KB repo from Week 1 (`Curriculum/Week1/README.md`).
If a team's setup didn't fully land, fix it before this week's content
— everything below assumes teams can already commit to their repo and
talk to Kiro.

**Design call made in this draft — flag for confirmation:** this plan
re-introduces the Tri-Cities/regional-industry framing into use-case
selection that V1's schedule had and V2's dropped (Course-Curriculum.md
§5 finding #4, §7 item #13). The KB's own cross-check (§8) names this
the single highest-leverage fix for stakeholder alignment — several
pitches (Cameron Foundation, VGR, Southern Company, Dominion) assume
students land on regionally-relevant projects, and nothing in the
current schedule actually required that. This draft treats item #13 as
resolved in that direction; revert Day 1's regional-framing block if
that's not actually the call.

## Agenda at a glance

### Day 1 (Tuesday) — Systems Thinking & Regional Use-Case Exploration, 180 min

Full detail: [Day1.md](./Day1.md).

1. **Recap + bridge from Week 1** (~10 min) — confirm every team's
   repo/Kiro/portfolio survived the week; frame the shift from tools to
   content.
2. **Systems thinking mini-lecture** (~25 min) — the sense → connect →
   act/inform loop, passive-monitoring vs. sense-and-actuate examples.
3. **Regional framing** (~20 min) — "pick something real, ideally
   something local," regional sectors offered as inspiration, not a
   checklist.
   *Decks 2–3: [Systems Thinking & Regional Framing](./Presentations/Systems_Thinking_and_Regional_Framing.md).*
4. **Device tinkering** (~40 min) — hands-on ESP32/breadboard/sensor
   kit, power-on only, no wiring or code.
   *Deck: [Device Tinkering](./Presentations/Device_Tinkering.md).*
5. **4D framework exercise** (~25 min) — the course's first live 4D
   exercise, evaluating an AI-brainstormed use case. Builds on the
   framework explained in Week 1's Prompting Frameworks deck.
   *Deck: [4D Use-Case Exercise](./Presentations/4D_Use_Case_Exercise.md).*
6. **Buffer / open work time** (~60 min, added 2026-08-28) — items 1–5
   summed to only 120 of 180 minutes; see Open Item 5. Circulate: help
   teams narrow to their 1–2 candidate use cases for Day 2.

### Day 2 (Thursday) — Systems Mapping & Use Case Report, 180 min

Full detail: [Day2.md](./Day2.md).

1. **Recap** (~10 min) — rapid-fire, one sentence per team on their
   candidate use case(s).
2. **Systems mapping exercise** (~40 min) — plain box-and-arrow
   notation, analog for now (TLDraw isn't introduced until Week 3).
   *Deck: [Systems Mapping](./Presentations/Systems_Mapping.md).*
3. **Use Case Report — an RTFC exercise** (~40 min) — turning notes
   into a written report, reusing Week 1's RTFC pattern.
4. **Post + submit** (~20 min) — commit the report/map to the notes-KB,
   publish a post about the use case.
5. **Wrap** (~10 min) — set the expectation that this use case is a
   candidate, not locked in; Week 3 validates it with real users.
   *Deck 3–5: [Use Case Report](./Presentations/Use_Case_Report.md).*
6. **Buffer / open work time** (~60 min, added 2026-08-28) — items 1–5
   summed to only 120 of 180 minutes; see Open Item 5.

## Learning objectives

By the end of Week 2, students can:
- Describe an IoT system as a loop — **sense → connect → act/inform** —
  and give an example that isn't the one taught in class.
- Explain the difference between a passive-monitoring system and a
  sense-*and*-actuate one, and why the latter is a stronger (not
  mandatory) target for this course (Course-Curriculum.md §1).
- Name a real, regionally-relevant problem as their team's candidate use
  case, and justify it in one paragraph.
- Have physically powered on and explored an ESP32 + sensor kit, with no
  wiring or code involved yet.
- Apply the **4D framework** (Delegation, Description, Discernment,
  Diligence) to evaluate an AI-assisted brainstorm of use-case ideas —
  the course's first real exercise of the judgment-step pattern named in
  Course-Curriculum.md §1.
- Produce a Use Case Report and a Systems Mapping diagram for their
  chosen candidate use case, and publish a post about it.

## Deliverables

- Use Case Report (per the schedule table, Course-Curriculum.md §4)
- Systems Mapping & Post

## Materials / resources

- One hardware kit per team from the shared pool: ESP32-DevKitC-32,
  breadboard, 1–2 sensors (Admin-Business-Legal.md §6). **Checkout/
  return logistics aren't decided anywhere in this KB** — see Open Items
  below.
- Paper/whiteboard for systems mapping (TLDraw deferred to Week 3).
- Kiro + GitHub access from Week 1 (`Curriculum/Week1/README.md`).
- `Stakeholder-Notes.md` — source for the regional-sector examples
  offered in Day 1 (don't hand this file to students as-is; it contains
  outreach/fundraising content, not a student-facing resource).

## Open items — resolve before this week is considered final

1. **Hardware kit checkout/return logistics for Day 1's shared-pool
   tinkering kit still aren't decided anywhere in this KB.** Who hands
   out the 84 ESP32 units / 80 breadboards / pooled sensors to ~15–20
   teams for Day 1, and how it's tracked, remains unscoped. **Resolved,
   2026-09-02 (per VoltPop), for the separate question of what Week 5
   assumes:** teams don't keep Day 1's generic tinkering kit all
   semester — Week 2 is where each team lands on a sensor choice, and
   Weeks 3–4 are procurement lead time to order those specific sensors
   for Week 5 delivery. See Course-Curriculum.md §4's "Why Weeks 3–4
   have no hardware content" note.
2. **Regional-focus reintroduction (see the design-call note above)
   needs explicit confirmation, not just this draft's assumption.** If
   confirmed, Course-Curriculum.md §7 item #13 and §5 finding #4 can be
   marked resolved and cross-referenced here; if not, Day 1's regional-
   framing block needs rewriting to drop the regional steering.
3. **This is the first time the 4D framework is actually scripted as a
   classroom exercise anywhere in this KB** — Day 1's 4D-exercise script
   is original design, not sourced from an existing plan or a decision
   VoltPop has already reviewed. Worth a sanity check before teaching
   from it, same as any new exercise.
4. **Not this week's gap, but adjacent — noted so it isn't mistaken for
   an oversight here:** the Scope Doc's mentor-interview deliverable
   (Course-Curriculum.md §5 finding #2, §7 item #2) lands on **Week 3**
   under V2's renumbering, not Week 2. Nothing above addresses it on
   purpose.
5. **Resolved (2026-08-28), mirroring Week 1's timing check: both days'
   scripted content only summed to 120 of the real 180-minute class
   length.** Fixed by adding an explicit 60-minute buffer/open-work
   block to each day, rather than leaving the gap unaccounted for. Unlike
   Week 1 Day 1 (which ended up fully packed), both Week 2 days now have
   real slack — worth a live timing check to confirm the buffer is
   actually needed and isn't masking blocks that are scripted too short.
