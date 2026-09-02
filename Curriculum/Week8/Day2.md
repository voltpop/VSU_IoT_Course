---
title: Week 8, Day 2 — Full Build, Iterations 1 & 2 (Thursday)
week: 8
day: 2
date: Mar 18 (Thu)
duration: 3 hours (180 min): 155 min fixed content, 25 min buffer
status: draft
see_also: ./README.md (shared framing, deliverables, open items); ./Day1.md
---

# Week 8, Day 2 (Thu) — Closing the Sense-React Loop

**1. Build stand-up** *(~15 min, per Course-Curriculum.md §1)*
What's blocking today's "react" work before it starts? Common blocker
to expect: a team whose Iteration 1 server works locally but whose
ngrok URL isn't reachable from their device — a networking problem,
not a code problem; send them to a team that got it working yesterday.

**2. Closing the loop — adding "react"** *(~50 min)*
Yesterday's server can **sense**. Today it learns to **react** —
extending it with RTFC, the same mechanical-generation pattern as every
prior firmware/server exercise:
- *Role:* "You're an MCP server development assistant."
- *Task:* "Add a tool to my existing MCP server that [your team's
  react action]."
- *Format:* "Extend my existing server code — keep the sense tool from
  yesterday, add the new tool with brief comments on what's new."
- *Context:* yesterday's working server code (paste it in), and what
  "react" means for your specific project.

**What "react" means is genuinely open per team** (Course-Curriculum.md
§1 — sense-and-actuate is encouraged, not mandatory):
- **If your project has an actuator:** a real action tool the server
  can trigger (e.g., a motor/relay) — the firmware polls the server for
  a pending action and executes it, since the device can't be reached
  directly from outside.
- **If it doesn't:** a meaningful non-physical reaction still counts —
  an alert, a status change, a logged decision. The point is a system
  that does something with a reading, not just displays it. Don't force
  a fake actuator onto a project where it doesn't fit.

*Deck: [Closing the Loop & RTFC](./Presentations/Closing_the_Loop_RTFC.md).*

**3. Test with Postman** *(~30 min)*
New tool this week. Before wiring the react tool into any agent-driven
or firmware-driven flow, hit both server endpoints **directly** in
Postman — the sense tool and the new react tool — to confirm each
works in isolation. This isolates "is my server broken" from "is my
integration broken," the same debugging instinct as every prior debug
loop, applied to a new tool.

**4. Full loop demo — Iteration 2** *(~30 min)*
Exercise the complete path end to end: device senses → data reaches
your MCP server → the react tool fires. This is Iteration 2's bar —
not a finished product, a demonstrated loop.

**5. Post + submit** *(~20 min)*
- Submit Iteration 1 and Iteration 2.
- Commit the MCP server code to the team repo.
- Publish the recurring "& Post" update — this time describing the
  loop itself: what it senses, what it does about it.

*Deck: [Iteration Submission & Post](./Presentations/Iteration_Submission_and_Post.md).*

**6. Wrap — preview Week 9** *(~10 min)*
Name explicitly: Week 9 is Iterations 3 & 4 — incorporating feedback on
this week's build and introducing security concepts, still VoltPop-led
(Course-Curriculum.md §4 footnote 1). Today's server is a first pass,
not final — expect real feedback to reshape it.

**7. Buffer / open work time** *(~25 min)*
Items 1–6 sum to 155 of the real 180-minute class. Prioritize teams
who don't yet have a working sense-react loop over teams polishing an
already-working one.

## Deliverables due

- Iteration 1
- Iteration 2 & Post
