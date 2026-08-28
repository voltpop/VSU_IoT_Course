---
title: Week 5 — Hardware Setup & Sensor Basics
week: 5
status: skeleton — created 2026-08-28, structure only. Day1.md/Day2.md need actual talking points, exercises, and timing before this is teachable (same depth as Weeks 1–2).
see_also: Course-Curriculum.md §1 (audience/safety framing, judgment-mechanical pattern, build stand-ups), §4 (schedule, tools-column correction), §6 (lesson-plan status), §7 items #6, #9, #14, #15, #18; Curriculum/Week1/README.md (git/Kiro basics assumed working); Curriculum/Week2/README.md (hardware kit continuity question)
---

# Week 5 — Hardware Setup & Sensor Basics

Two 3-hour classes, Tuesday and Thursday. **This is a skeleton, not a
full lesson plan** — structure, known context, and open questions only.

- [Day 1 (Tuesday)](./Day1.md)
- [Day 2 (Thursday)](./Day2.md)

## Where this fits in the schedule

**Week 5 of 15** — Hardware Setup & Sensor Basics, Feb 16 (Tue) / Feb
18 (Thu). Lead: **VoltPop**. Support: Builder Tech, Explay (TBD)
(Course-Curriculum.md §4, full table).

- ← Previous: **Week 4** — Business Models & Market Fit, Feb 9 (Tue) /
  Feb 11 (Thu). Lead: Explay. *(not yet drafted)*
- → Next: **Week 6** — Designing the User Experience, Feb 23 (Tue) /
  Feb 25 (Thu). Lead: Builder Tech. *(not yet drafted)*

## What we know so far (from Course-Curriculum.md §4)

- **Description:** extend the existing GitHub repo to hardware/firmware
  code, an open-source governance intro, ESP32 power-on/sensor/
  breadboard work, and firmware.
- **Skill:** Hardware Prototyping & Firmware Basics.
- **Deliverables:** Hardware Repo Setup; Firmware & Docs & Post.
- **Tools added this week:** Canva, **MicroPython/Thonny** (confirmed
  toolchain — the live shared schedule sheet may still say Arduino IDE,
  which is wrong; the two are incompatible ESP32 toolchains, §4's
  tools-column note), ESP32/Breadboard/Sensors.

**Audience framing carries forward but gets tested for real here
(Course-Curriculum.md §1):** still no EE/electricity fundamentals — no
Ohm's law, no GPIO internals. Wiring is recipe-following ("plug the red
wire into the red rail"), not conceptual grounding. Safety framing is
**3.3V / equipment-damage risk** ("let's not waste kit budget"), not a
lab-safety briefing — essentially zero personal-injury risk at these
voltage/current levels.

**This week is the canonical example of the course's own reusable
pattern (Course-Curriculum.md §1):**
1. **Judgment-heavy step** — *is this wiring safe?* → scaffold with 4D.
2. **Mechanical-generation step** — *turn a settled wiring spec into
   working firmware* → scaffold with RTFC, **formally named here** (it
   was only previewed in Weeks 1–2).

**Build stand-up (Course-Curriculum.md §1, §7 item #18):** doesn't fit
Day 1 — nothing's been built yet to report on. Plan to open **Day 2**
with one instead, once Day 1's wiring/firmware attempts give teams
something real to share/get stuck on.

## Learning objectives (draft — refine once days are scripted)

- Extend their team's existing repo with hardware/firmware code and
  docs, rather than starting a new one.
- Explain, in plain terms, what open-source governance means for their
  own repo (license, contribution norms) — content not designed yet,
  see Open Items.
- Safely power on an ESP32, wire a sensor via breadboard, and explain
  *why* a given wiring choice is safe (equipment-damage framing, not
  EE theory).
- Generate working firmware from a settled wiring spec using RTFC,
  formally named this week.

## Deliverables

- Hardware Repo Setup
- Firmware & Docs & Post

## Materials / resources

- One hardware kit per team, continuing from Week 2's tinkering
  (Admin-Business-Legal.md §6) — **whether it's the same physical kit
  each team already touched, or newly assigned, is still open** (see
  Week 2's Open Item 1; this week inherits that gap).
- MicroPython/Thonny (not Arduino IDE — confirmed toolchain).
- Git Cheat Sheet: reuse `Curriculum/Week1/Assets/git-cheat-sheet-education.pdf`.
- Canva (new tool this week per the schedule; purpose not yet specified
  in this KB — see Open Items).

## Open items — resolve before this is more than a skeleton

1. **No actual day-by-day content yet.** Day1.md/Day2.md need real
   talking points, a scripted wiring walkthrough, a firmware-by-
   prompting exercise, and timing — same depth as Weeks 1–2.
2. **Open-source governance intro has no designed content anywhere in
   this KB.** The schedule Description names it, but what it actually
   covers (a license? contribution norms? how their repo becoming more
   public-facing changes anything?) has never been scoped.
3. **Canva's purpose this week is unclear.** It's new in the Tools
   column but nothing in this KB says what it's used for in Week 5
   specifically (Course-Curriculum.md §7 item #14 flags the tools list
   generally as never having been deliberately trimmed/timed).
4. **Hardware kit continuity (inherited from Week 2 Open Item 1):**
   whether Week 5 assumes teams already have "their" kit from Week 2's
   tinkering, or kits get reassigned, isn't decided.
5. **Old external Week 5 file exists but isn't in this repo.**
   Course-Curriculum.md §6 references
   `~/Documents/VoltPop/IoT_Course/Week5_AI_Wiring_Firmware_Prompt_Template.md`
   (VoltPop's own working files) as a prior draft needing one new
   section (the Tuesday GitHub-migration/governance content) — that
   file was never pulled into this repo, so this skeleton was built
   from the schedule table alone, not from that draft. Worth reconciling
   before writing full content, so nothing already built there gets
   redone from scratch.
6. **4D/RTFC should be formally named here, not just previewed** — per
   Course-Curriculum.md §7 item #6 ("retrofit Week 5's materials to
   explicitly name the 4D/RTFC framework"). This skeleton notes it
   above; actual day content needs to do the formal naming explicitly.
