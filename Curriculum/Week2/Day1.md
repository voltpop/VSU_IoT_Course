---
title: Week 2, Day 1 — Understanding Systems & IoT (Tuesday)
week: 2
day: 1
date: Jan 26 (Tue)
duration: 3 hours (180 min): 120 min fixed content, 60 min buffer
status: draft
see_also: ./README.md (shared framing, deliverables, open items); ./Day2.md
---

# Week 2, Day 1 (Tue) — Systems Thinking & Regional Use-Case Exploration

**1. Recap + bridge from Week 1** *(~10 min)*
Quick round: confirm every team's repo/Kiro/portfolio survived the week.
Frame the shift explicitly: *"last week was tools, this week is the
first real content — what actually is an 'IoT system,' and what's ours
going to be?"*

**2. Systems thinking mini-lecture** *(~25 min)*
Teach the loop, not the electronics:
- **Sense** — something measures a piece of the physical world (a
  temperature, a door opening, a soil moisture level).
- **Connect** — that reading gets somewhere it can be used (an app, a
  dashboard, another device).
- **Act / inform** — something happens with it: a person is told, or a
  device *does* something in response.
- Two or three concrete, non-technical examples, contrasting
  passive-monitoring vs. sense-and-actuate: a smart thermostat (senses
  temp, acts by changing HVAC) vs. a basic temperature display (senses,
  informs, doesn't act); a soil-moisture sensor that just shows a number
  vs. one that triggers irrigation. Reinforce §1's framing: sense-and-
  actuate is the stronger portfolio outcome, not a requirement — don't
  let a team force it onto a problem where it doesn't fit.

*Deck for items 2–3: [Systems Thinking & Regional Framing](./Presentations/Systems_Thinking_and_Regional_Framing.md).*

**3. Regional framing — pick something real, ideally something local**
*(~20 min)*
Explicit prompt: *"look for a problem in our own region."* Offer
already-researched regional sectors as **inspiration, not a
checklist** — agriculture (see the AI-agriculture angle in
`Stakeholder-Notes.md`), manufacturing/shipbuilding, the power grid,
personal finance — but make clear a team can pick anything real to them
near where they live. The point of naming these is credibility ("real
people are already thinking about this"), not narrowing the field.
Avoid over-anchoring every team on agriculture — regional relevance is
the goal, not a specific industry.

**4. Device tinkering — hands-on, no wiring/code** *(~40 min)*
Hand out one kit per team from the shared hardware pool (ESP32-DevKitC-
32, breadboard, a couple of sensors — Admin-Business-Legal.md §6; 84
ESP32 / 80 breadboards / 131 sensors bought as an undifferentiated pool
on purpose, since the specific sensor is irrelevant per Course-
Curriculum.md §1). Today's only ask: power the board on via USB, look at
what's on the board and the sensor(s), poke at them. No wiring, no
firmware — that's Week 5. The point is tactile: *"what could this thing
sense or do inside a system you actually care about?"*

*Deck: [Device Tinkering](./Presentations/Device_Tinkering.md).*

**5. 4D framework exercise — is this actually a good use case?**
*(~25 min)*
Model this live with Kiro, naming each step as you go (first real
exercise of the judgment-step pattern, Course-Curriculum.md §1). If the
room hasn't seen 4D before, start with [Week 1's Prompting Frameworks
deck](../Week1/Presentations/Prompting_Frameworks.md)'s 4D section —
don't re-explain the framework from scratch here, apply it live:
1. **Delegation** — decide what to hand to the AI vs. decide yourselves.
   Delegate the brainstorm; keep the final pick as your own call.
2. **Description** — give Kiro real context, not a generic ask:
   *"Brainstorm 5 IoT use-case ideas for [a regional problem your team
   names], each with a rough sense/act loop."* A vague ask like "give me
   IoT ideas" produces generic junk — same lesson as Week 1's bad-prompt
   demo, now applied to a judgment task instead of a mechanical one.
3. **Discernment** — as a team, throw out the weak/generic ideas. Keep
   what's actually specific and locally grounded.
4. **Diligence** — sanity-check what's left: can an ESP32 + a sensor +
   an app actually approximate this, in the ~13 weeks remaining, by a
   team with no EE/CS background? If not, it's not a good pick yet — go
   back to step 2 with tighter context.

*Deck: [4D Use-Case Exercise](./Presentations/4D_Use_Case_Exercise.md).*

**6. Buffer / open work time** *(~60 min, added 2026-08-28)*
Items 1–5 above summed to only 120 of the real 180-minute class length
(see README Open Item 5). Not idle time — circulate and help teams
narrow toward their 1–2 candidate use cases; device tinkering (item 4)
is also the most likely block to run long with a largely non-technical
audience, so expect some of this buffer to get absorbed there.

**Carry-over to Day 2:** each team narrows to 1–2 candidate use cases.
