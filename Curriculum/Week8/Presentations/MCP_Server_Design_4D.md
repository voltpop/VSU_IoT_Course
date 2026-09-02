# Designing the MCP Server & the 4D Judgment Step

*Source: [`../Day1.md`](../Day1.md) item 3. ~40 min. If the room hasn't
seen 4D before (unlikely by Week 8), start with [Week 1's Prompting
Frameworks](../../Week1/Presentations/Prompting_Frameworks.md) — this
deck applies it, it doesn't re-teach it.*

---

## From placeholder to real

- Week 7's webhook.site proved the path works — it was never meant to
  be the destination.
- Today you build the real thing: **an MCP server your team builds and
  controls.**

---

## What's an MCP server, briefly

- A standard way to expose what your app can do as **tools** — things
  an AI agent (or your own app) can call by name.
- At minimum today: a tool that answers *"what's the latest sensor
  reading?"*

---

## The question

- *What should this server actually expose?*
- A judgment call before any code gets written — that's what 4D is for,
  not RTFC.

---

## Delegate

- Hand the AI a **first-draft tool list**.
- Keep the **final call on what the server does** as a team decision.

---

## Describe

- *"I'm building an MCP server for [your project]. My device sends
  [your Week 7 payload]. Draft the MCP tools this server should
  expose — at minimum, one to fetch the latest reading."*

---

## Discern

- One standard: could an AI agent that's never seen your project
  understand what each tool does and when to call it, **from its name
  and description alone?**
- If not, that tool isn't settled yet.

---

## Diligence

- Is this buildable **today**, given everything else due this week?
- A server with one solid "sense" tool beats three half-built ones.
- If the draft list is too ambitious, cut — don't carry scope into a
  70-minute build block that can't finish it.

---

## Carry into the build

- Today's settled tool list is the Context you'll hand RTFC in the next
  block.
