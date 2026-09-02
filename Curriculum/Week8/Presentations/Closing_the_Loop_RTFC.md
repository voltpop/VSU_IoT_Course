# Closing the Loop & RTFC

*Source: [`../Day2.md`](../Day2.md) items 2–3. ~80 min total (build +
Postman testing). Extends yesterday's server rather than starting
over.*

---

## Sense → React

- Yesterday: your server can answer *"what's the latest reading?"*
- Today: it learns to **do something** with that reading.
- This is Course-Curriculum.md §1's sense-and-actuate direction, made
  concrete — encouraged, not mandatory.

---

## RTFC, extending yesterday's server

- **Role:** "You're an MCP server development assistant."
- **Task:** "Add a tool to my existing MCP server that [your team's
  react action]."
- **Format:** "Extend my existing server code — keep the sense tool
  from yesterday, add the new tool with brief comments on what's new."
- **Context:** yesterday's working server code (paste it in), and what
  "react" means for your specific project.

---

## What "react" means — genuinely open per team

- **Have an actuator?** A real action tool the server can trigger.
  Since the device can't be reached directly from outside, the
  **firmware polls the server** for a pending action and executes it —
  not the server pushing to the device.
- **Don't?** A meaningful non-physical reaction still counts: an alert,
  a status change, a logged decision. The point is a system that acts
  on a reading, not just displays it.
- **Don't force a fake actuator onto a project where it doesn't fit** —
  same "not a hard requirement" framing as every sense-and-actuate
  mention so far.

---

## Test with Postman before wiring anything else up

- Hit the sense tool directly. Hit the react tool directly.
- Confirm both work **in isolation** before layering an agent or the
  firmware poll loop on top.
- Same instinct as every debug loop: isolate "is my server broken" from
  "is my integration broken."

---

## Iteration 2: the bar

- The complete path, demonstrated: device senses → data reaches your
  server → the react tool fires.
- Not a finished product — a demonstrated loop.
