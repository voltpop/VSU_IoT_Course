# Wiring Safety & the 4D Judgment Step

*Source: [`../Day1.md`](../Day1.md) item 3. ~50 min. First live 4D
exercise applied to a physical (not just informational) judgment call.
If the room hasn't seen 4D before, start with [Week 1's Prompting
Frameworks](../../Week1/Presentations/Prompting_Frameworks.md)'s 4D
section — this deck applies it, it doesn't re-teach it.*

---

## The question

- ***Is this wiring safe?***
- Not an EE question — no Ohm's law, no GPIO internals.
- An **equipment-damage** question: *"let's not waste kit budget."*
- Essentially zero personal-injury risk at 3.3V — this is not a
  lab-safety briefing.

---

## What actually breaks kit

Three things, and only three things, matter today:
1. **Nothing above 3.3V into a GPIO pin.**
2. **VCC and GND not reversed.**
3. **No bare wires that could short across the board.**

> Speaker notes: if a team's AI-drafted plan doesn't clearly account
> for these three, that's a bad answer — same as any other vague-in,
> vague-out prompting failure, just with a physical consequence
> instead of a paragraph.

---

## Delegate

- Hand the AI the **wiring-plan draft**.
- Keep the **final safety call** as a human decision — yours, then your
  instructor's.
- **What "good" looks like here:** a labeled breadboard-view diagram, a
  pin-by-pin connection table, and a step-by-step build sequence — not
  just a paragraph of text. Kiro can generate all of this in one pass
  (confirmed 2026-09-02, per VoltPop's own test build) — this *is* the
  documentation your repo needs, not a draft to redo later in another
  tool.

---

## Describe

- Give it your specific sensor, the ESP32's available pins, and what
  you're building.
- *"I have [sensor] and an ESP32-DevKitC-32 — draft a breadboard
  wiring plan and pin-map for reading it, and flag any voltage-
  compatibility issues."*
- Not: *"how do I wire a sensor."*

---

## Discern

- Check the answer against the three things above.
- Missing or unclear on any of them → back to Describe with tighter
  context (the sensor's actual voltage spec is the usual gap), not
  straight to wiring.

---

## Diligence

- Before power touches the board: a teammate checks the physical
  breadboard against the settled plan.
- Then an instructor/TA does the same.
- **This is the actual safety gate.** The AI step drafts a plan; a
  human confirms it before anything gets powered on.

---

## Then: power on

- Confirm nothing smokes/overheats before moving to firmware.
- If something's wrong, that's new context — go back to Describe with
  what you actually observed, not "it didn't work."
