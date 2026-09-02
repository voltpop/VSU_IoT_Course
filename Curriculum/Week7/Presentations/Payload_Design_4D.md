# Payload Design & the 4D Judgment Step

*Source: [`../Day1.md`](../Day1.md) item 3. ~45 min. If the room hasn't
seen 4D before (unlikely by Week 7), start with [Week 1's Prompting
Frameworks](../../Week1/Presentations/Prompting_Frameworks.md) — this
deck applies it, it doesn't re-teach it.*

---

## Where you are

- Week 5: your firmware reads a sensor value — visible only on the
  device itself.
- Today: decide what actually needs to travel off the device, and in
  what shape, before writing any code that sends it.

---

## The question

- *What should this payload actually contain?*
- Not a coding question yet — a judgment call about what a stranger
  receiving this data would need to make sense of it.

---

## Delegate

- Hand the AI a **first-draft payload structure**.
- Keep the **final call on what's actually needed** as a team decision.

---

## Describe

- *"I have a [sensor type] reading a [value] for [your project's use
  case]. Draft a JSON payload structure for sending one reading,
  including whatever metadata a receiving system would need to make
  sense of it on its own."*
- Not: *"give me a JSON format."*

---

## Discern

Check the draft against the gaps that show up almost every time:
- **No timestamp** — when was this reading taken?
- **No unit** — is `42` a percentage, a temperature, a raw sensor
  value?
- **No device/team identifier** — if every team's readings land on the
  same test endpoint, how would anyone tell them apart?

---

## Diligence

- Could someone who's never seen your project read this JSON and
  understand what it means?
- If not, it's not settled — back to Describe with what's missing.

---

## Carry into the architecture diagram

- This settled payload is the label on the arrow in today's next block
  — what actually travels from device to receiving endpoint.
