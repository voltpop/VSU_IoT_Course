---
title: Week 7, Day 1 — Data Flow & Systems Architecture (Tuesday)
week: 7
day: 1
date: Mar 2 (Tue)
duration: 3 hours (180 min): 110 min fixed content, 70 min buffer
status: draft
see_also: ./README.md (shared framing, deliverables, open items); ./Day2.md
---

# Week 7, Day 1 (Tue) — Payload Design & Systems Architecture

**1. Build stand-up** *(~15 min, per Course-Curriculum.md §1)*
Second live use of the pattern (first was Week 5 Day 2) — no need to
re-explain it, just run it: *(Deck: [Week 5's Build
Stand-Up](../Week5/Presentations/Build_Standup.md))*
- Where does hardware/wiring actually stand, two weeks after Week 5's
  build (Week 6 was UX design, not technical)?
- Surface anyone whose Week 5 firmware never got to a reliable sensor
  read before today's data-flow work builds on top of it.

**2. Recap + bridge: from "it reads locally" to "it goes somewhere"**
*(~10 min)*
Week 5 ended with firmware that reads a sensor and prints the value —
visible only on the device itself. Frame today's question directly:
*"how does that value get anywhere useful?"* This is Week 2's
sense → connect → act/inform loop (Course-Curriculum.md §4), now made
concrete and technical instead of conceptual.

**3. Payload design — the judgment step** *(~45 min)*
Before writing any integration code, decide **what** gets sent, not
just how. Run this as a 4D exercise:
1. **Delegate** — hand the AI a first-draft payload structure, not the
   final call on what's actually needed.
2. **Describe** — give it real context: *"I have a [sensor type]
   reading a [value] for [your project's use case]. Draft a JSON
   payload structure for sending one reading, including whatever
   metadata a receiving system would need to make sense of it on its
   own."*
3. **Discern** — check the draft against what it's actually missing.
   Common gaps to watch for: no timestamp, no unit on the value, no way
   to tell readings from different teams/devices apart.
4. **Diligence** — sanity-check: could someone who's never seen your
   project read this JSON and understand what it means? If not, it's
   not settled yet.

*Deck: [Payload Design & the 4D Judgment Step](./Presentations/Payload_Design_4D.md).*

**4. Systems Architecture Diagram** *(~40 min)*
**Changed, 2026-09-02 (per VoltPop):** generate this with **Kiro**
rather than hand-drawing it in TLDraw — same pattern confirmed in Week
5's wiring diagram. This is mechanical generation, not a new judgment
call, so scaffold it with **RTFC**:
- *Role:* "You're a systems-diagramming assistant."
- *Task:* "Diagram the technical path our sensor data takes, labeled
  end to end."
- *Format:* "A labeled block diagram: Sensor → ESP32 (local read +
  payload assembly) → Wi-Fi → HTTP request → [receiving endpoint] —
  mark the receiving endpoint as a placeholder, not final."
- *Context:* today's settled payload structure (item 3) and your
  project's use case.

This extends Week 2's plain sense/connect/act sketch into something
with actual technical stages a builder could follow. Each team
generates their own diagram from their own settled payload.

*Deck: [Systems Architecture Diagram](./Presentations/Systems_Architecture_Diagram.md).*

**5. Buffer / open work time** *(~70 min)*
Items 1–4 sum to 110 of the real 180-minute class. Circulate; payload
design (item 3) is the block most likely to run long — a team that
can't articulate what their reading means is going to struggle with
Day 2's integration work no matter how well it's coded. Every team
should leave today with a settled payload structure and a diagram
before starting to code the integration tomorrow.

## Carry-over to Day 2

Today's settled payload and architecture diagram are the **context**
Day 2's RTFC integration exercise runs on — don't start Day 2 without
them both settled.
