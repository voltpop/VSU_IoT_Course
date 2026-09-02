---
title: Week 5 — Hardware Setup & Sensor Basics
week: 5
status: draft — scripted 2026-09-02, same depth as Weeks 1–2. Day1.md/Day2.md have real talking points, exercises, and timing; untested live, same caveat as Weeks 1–2's draft status.
see_also: Course-Curriculum.md §1 (audience/safety framing, judgment-mechanical pattern, build stand-ups), §4 (schedule, tools-column correction), §6 (lesson-plan status), §7 items #6, #9, #14, #15, #18; Curriculum/Week1/README.md (git/Kiro basics assumed working); Curriculum/Week2/README.md (hardware kit continuity question)
---

# Week 5 — Hardware Setup & Sensor Basics

Two 3-hour classes, Tuesday and Thursday. **Scripted 2026-09-02** — real
talking points, exercises, and timing, same depth as Weeks 1–2. Still
`status: draft`, not final: untested live, same as every other drafted
week in this repo.

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

- Sensor kit ordered to each team's Week 2 choice (Admin-Business-
  Legal.md §6) — **resolved, 2026-09-02 (per VoltPop): not the same
  generic kit from Day 1 tinkering, and not a reassigned generic kit
  either.** Weeks 3–4 are procurement lead time so the specific sensors
  a team chose in Week 2 can be ordered and delivered in time for Week
  5 (Course-Curriculum.md §4). ESP32 units themselves may still be
  shared-pool/reused — only the sensor selection is confirmed
  choice-driven.
- MicroPython/Thonny (not Arduino IDE — confirmed toolchain).
- Git Cheat Sheet: reuse `Curriculum/Week1/Assets/git-cheat-sheet-education.pdf`.
- Canva — resolved, 2026-09-02: visual wiring-diagram documentation for
  the repo (see Day 2 item 3), a business-student-friendly alternative
  to EDA/schematic software.

## Open items — resolve before this is fully final

1. **Resolved, 2026-09-02:** Day1.md/Day2.md now have real talking
   points, a scripted wiring walkthrough (4D-scaffolded), a firmware-
   by-prompting exercise (RTFC-scaffolded), and timing — same depth as
   Weeks 1–2. **Still needs a live timing check**, same caveat every
   other drafted week in this repo carries.
2. **Resolved, 2026-09-02 — open-source governance intro.** Scoped as:
   picking a license (MIT default), a README that documents purpose/
   pin-map/how-to-run, and brief contribution norms (small commits,
   branch-per-change) — see
   [`Presentations/GitHub_Migration_and_Governance.md`](./Presentations/GitHub_Migration_and_Governance.md).
   Deliberately light for the audience, not a full governance module.
3. **Resolved, 2026-09-02 — Canva's purpose.** See the Materials note
   above and Day 2 item 3: visual wiring-diagram documentation, not
   app-build or portfolio work.
4. **Resolved, 2026-09-02 (per VoltPop) — hardware kit continuity
   (inherited from Week 2 Open Item 1):** Week 5's sensors are
   ordered-to-choice, not Week 2's tinkering kit carried forward and not
   a reassigned generic kit. Week 2 is where teams choose their sensor;
   Weeks 3–4 are the procurement lead time to get that specific sensor
   delivered by Week 5. Still open: whether the ESP32 unit/breadboard
   themselves are the same physical items from Day 1 or freshly issued —
   this resolution only confirms the sensor-choice-to-delivery logic,
   not full kit logistics (Week 2 Open Item 1 still covers Day 1
   checkout/return).
5. **Resolved, 2026-09-02 (per VoltPop) — external Week 5 file.**
   `~/Documents/VoltPop/IoT_Course/Week5_AI_Wiring_Firmware_Prompt_Template.md`
   couldn't be located; confirmed lost the same way the original Week 1
   file was. This week's content was built fresh from the schedule
   table and this KB's context, not reconciled against that draft.
6. **Resolved, 2026-09-02 — 4D/RTFC formally named.** Per
   Course-Curriculum.md §7 item #6: 4D is formally applied to the
   wiring-safety judgment step (Day 1 item 3), RTFC formally named for
   the first time on the firmware-generation step (Day 1 item 4).
7. **Not yet addressed:** hardware kit checkout/return logistics for
   Day 1's original shared-pool tinkering kit (Week 2 Open Item 1)
   remain unscoped — separate question from the sensor-ordering
   resolution above.
