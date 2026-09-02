# Building the MCP Server & RTFC

*Source: [`../Day1.md`](../Day1.md) item 4. ~70 min. Mechanical
generation — the tool list is already settled (last block), this is
about turning it into working code.*

---

## RTFC, applied to the server

- **Role:** "You're an MCP server development assistant."
- **Task:** "Build an MCP server exposing [your settled tools], starting
  with a tool that returns the latest sensor reading."
- **Format:** "Working server code, plus instructions for running it
  locally and exposing it publicly."
- **Context:** your settled payload structure (Week 7), your settled
  tool list, and your project's use case.

---

## Making it reachable: ngrok

**Design call in this draft — confirm before teaching:**
- **ngrok** (free tier, no signup complexity) exposes your locally-run
  server with a public URL — same low-friction precedent as Week 7's
  webhook.site.
- Once you have that URL, extend your Week 5/7 firmware: change the
  POST destination from webhook.site to your ngrok URL.

---

## Iteration 1: the bar

- Real sensor data flowing from your device into a server **your team
  built and controls** — not a placeholder.
- Nothing about "react" yet — that's Day 2. Today is sense, done for
  real.

---

## Debug loop

- Same instinct as every prior firmware exercise: if something's
  broken, feed the **actual error** back into Context, not "it doesn't
  work."
- New failure mode to watch for: **networking, not code.** If your
  server runs fine locally but nothing arrives from the device, check
  the ngrok URL and firmware's destination before touching server code.

---

## Before you close today

- Confirm a real reading — from your physical device — shows up when
  you call your server's sense tool.
- That's Iteration 1. Day 2 builds "react" on top of it.
