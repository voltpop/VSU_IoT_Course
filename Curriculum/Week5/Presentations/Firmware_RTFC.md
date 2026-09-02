# First Firmware & RTFC

*Source: [`../Day1.md`](../Day1.md) item 4. ~45 min. RTFC formally
named for the first time here (previewed in [Week 1's Prompting
Frameworks](../../Week1/Presentations/Prompting_Frameworks.md), applied
live in Week 2's Use Case Report) — this deck reuses it, it doesn't
re-teach it from scratch. First time it's applied to hardware instead
of text.*

---

## Where you are

- Wiring (last block) was the **judgment** call: is this safe?
- Turning a **settled** pin-map into working code is **mechanical
  generation** — same category as Week 1's bio or Week 2's Use Case
  Report, just with a physical feedback loop this time.

---

## RTFC, applied to firmware

- **Role:** "You're a MicroPython firmware assistant for ESP32."
- **Task:** "Write firmware that reads my sensor and prints its value
  every 2 seconds."
- **Format:** "A complete, runnable MicroPython script with brief
  comments explaining each step — no unrelated boilerplate."
- **Context:** your settled pin-map from the wiring block, your
  sensor's name/type, and what the reading should represent for your
  project.

---

## Run it

- **Thonny**, against the physical board — not a simulator.
- This is the first exercise all semester where "did it work" has a
  physical answer (a number prints, or it doesn't) instead of a
  subjective one (does this bio read well).

---

## Debug loop

- If it doesn't work, that's new context — feed it back in.
- **The actual error message**, not *"it doesn't work."*
- Same specificity lesson as every RTFC exercise so far — the fix isn't
  a smarter model, it's a more specific prompt.

---

## Before you move on

- Confirm a sensor value is actually printing and looks plausible (not
  wildly out of range) before calling this block done.
- This firmware is a first pass, not final — Day 2 finalizes it for the
  actual repo deliverable.
