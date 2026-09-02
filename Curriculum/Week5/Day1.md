---
title: Week 5, Day 1 — Hardware Setup & Sensor Basics (Tuesday)
week: 5
day: 1
date: Feb 16 (Tue)
duration: 3 hours (180 min): 125 min fixed content, 55 min buffer
status: draft
see_also: ./README.md (shared framing, deliverables, open items); ./Day2.md
---

# Week 5, Day 1 (Tue) — GitHub Migration, Wiring & First Firmware

*No build stand-up today (Course-Curriculum.md §1) — nothing's been
built yet for teams to report on. Day 2 opens with the first one.*

**1. Recap + bridge from Weeks 3–4** *(~10 min)*
Quick round: each team names their locked-in brand/idea from Week 4 in
one sentence. Frame the shift explicitly: *"the last four weeks were
about deciding what to build and why — starting today, you're actually
building it."* Name that this is the start of the course's primary
technical arc (Weeks 5, 7, 8, 9, 10), which stays hands-on through
testing/go-live.

**2. GitHub migration + open-source governance intro** *(~20 min)*
Extend each team's **existing** repo (from Week 1) with hardware/
firmware content — not a new repo. Cover, at a business-student level of
depth:
- **Why this matters now, not before:** the repo was a private notes-KB
  through Week 4; from today it also holds real project code, which
  changes what "public-facing" means for it.
- **Pick a license** — plain-language framing: *"this file just says
  what other people are allowed to do with your code."* Default
  recommendation: **MIT** (permissive, one paragraph, the most common
  choice for a student/portfolio project) — don't turn this into a
  license-comparison lecture, just get one added.
- **A README that actually documents the build** — purpose, current
  wiring pin-map, how to run the firmware. This becomes real starting
  today's wiring work; today's README is intentionally incomplete.
- **Contribution norms, briefly** — branches + small commits, same
  pattern this program's own KB uses (worth naming the parallel
  explicitly: *"this is literally how the adults running this program
  keep their own notes in sync"*).

*Deck: [GitHub Migration & Governance](./Presentations/GitHub_Migration_and_Governance.md).*

**3. ESP32 + sensor wiring — the judgment step** *(~50 min)*
Hand out each team's kit — **their specific sensor, ordered to their
Week 2 choice** (Course-Curriculum.md §4's Week 3–4 procurement-lead-
time note), plus the shared-pool ESP32/breadboard/jumper-wire/resistor
kit (Admin-Business-Legal.md §6).

Frame the question directly: ***is this wiring safe?*** Not an EE
question (no Ohm's law, no GPIO internals — Course-Curriculum.md §1) —
an equipment-damage question: *"let's not waste kit budget,"* not a
lab-safety briefing. Essentially zero personal-injury risk at 3.3V.

Run this as the course's first live 4D exercise applied to a physical
(not just informational) judgment call:
1. **Delegate** — hand the AI the wiring-plan draft, not the final
   safety call.
2. **Describe** — give it real context: your specific sensor, the
   ESP32's available pins, and what you're trying to build. Not
   *"how do I wire a sensor,"* but *"I have [sensor] and an ESP32-
   DevKitC-32 — draft a breadboard wiring plan and pin-map for reading
   it, and flag any voltage-compatibility issues."*
3. **Discern** — check the AI's answer against the three things that
   actually break kit: **(a)** nothing above 3.3V going into a GPIO
   pin, **(b)** VCC/GND not reversed, **(c)** no bare wires that could
   short across the board. If the AI's plan doesn't clearly account for
   these, that's a bad answer — go back to Describe with tighter
   context (sensor's actual voltage spec), not straight to wiring.
4. **Diligence** — before powering on, one more set of eyes (a
   teammate, then an instructor/TA) checks the physical breadboard
   against the settled plan. This is the actual safety gate — the AI
   step drafts the plan, a human confirms it before power touches the
   board.

Wire it, then power on and confirm nothing smokes/overheats before
moving to firmware.

*Deck: [Wiring Safety & the 4D Judgment Step](./Presentations/Wiring_Safety_4D.md).*

**4. First firmware — the mechanical-generation step** *(~45 min)*
Where wiring was the judgment call, turning a **settled** pin-map into
working code is mechanical generation — scaffold it with **RTFC**,
formally named here for the first time (previewed in Week 1, applied
live in Week 2's Use Case Report, now on real hardware):
- *Role:* "You're a MicroPython firmware assistant for ESP32."
- *Task:* "Write firmware that reads my sensor and prints its value
  every 2 seconds."
- *Format:* "A complete, runnable MicroPython script with brief
  comments explaining each step — no unrelated boilerplate."
- *Context:* paste the settled pin-map from item 3, the sensor's name/
  type, and what the reading should represent for your project.

Run it in **Thonny** against the physical board. Debug loop: if it
doesn't work, that's new context to feed back in (the actual error
message, not "it doesn't work") — same specificity lesson as every
prior RTFC exercise, now with a hardware feedback loop instead of just
text output.

*Deck: [First Firmware & RTFC](./Presentations/Firmware_RTFC.md).*

**5. Buffer / open work time** *(~55 min)*
Items 1–4 above sum to 125 of the real 180-minute class. Not idle time
— this is the block most likely to actually get absorbed today: wiring
and first-firmware debugging are the day's highest-variance activities
for a non-technical audience, and every team should leave with **a
sensor physically wired and at least attempting to read** before Day 2.
Circulate; prioritize unblocking teams stuck on the safety-diligence
step over ones just iterating on firmware output formatting.

## Carry-over to Day 2

Whatever wiring/firmware work doesn't finish today carries to Day 2,
which opens with a build stand-up covering it — the first live use of
that pattern anywhere in the course (Course-Curriculum.md §1, §7 item
#18).
