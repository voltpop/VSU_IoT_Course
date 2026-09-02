---
title: Week 8, Day 1 — Full Build, Iterations 1 & 2 (Tuesday)
week: 8
day: 1
date: Mar 16 (Tue)
duration: 3 hours (180 min): 140 min fixed content, 40 min buffer
status: draft
see_also: ./README.md (shared framing, deliverables, open items); ./Day2.md
---

# Week 8, Day 1 (Tue) — Design & Build the MCP Server

*First day back from Spring Break.*

**1. Build stand-up** *(~20 min, per Course-Curriculum.md §1)*
Longer than the usual ~10–15 min — expect more to surface after the
break-length gap since Week 7. Prioritize teams whose Week 7 firmware
stopped working or whose webhook.site data stopped flowing; they can't
start today's work until that's re-confirmed.

**2. Recap + reframe: from a placeholder to the real thing** *(~10 min)*
Week 7 proved the **sense** side of the loop works — a reading reaching
somewhere off the device (webhook.site, a placeholder). Today replaces
that placeholder with something real: **an MCP server your team
builds and controls** — and starts pushing the loop from *sense* toward
*react*, not just passive monitoring (Course-Curriculum.md §1's
sense-and-actuate framing, encouraged but not required).

**3. Designing the MCP server — the judgment step** *(~40 min)*
Before generating any server code, decide what it should actually
expose. Run this as a 4D exercise:
1. **Delegate** — hand the AI a first-draft set of MCP tool
   definitions, not the final call on what the server does.
2. **Describe** — give it real context: *"I'm building an MCP server
   for [your project]. My device sends [your Week 7 payload]. Draft
   the MCP tools this server should expose — at minimum, one to fetch
   the latest reading."*
3. **Discern** — check the draft tools against one standard: could an
   AI agent that's never seen your project understand what each tool
   does and when to call it, from its name and description alone?
4. **Diligence** — sanity-check scope: is this buildable today, given
   everything else due this week? A server with one solid "sense" tool
   beats three half-built ones.

*Deck: [Designing the MCP Server & the 4D Judgment Step](./Presentations/MCP_Server_Design_4D.md).*

**4. Building the server — Iteration 1** *(~70 min)*
Mechanical-generation step, scaffolded with **RTFC**:
- *Role:* "You're an MCP server development assistant."
- *Task:* "Build an MCP server exposing [your settled tools from item
  3], starting with a tool that returns the latest sensor reading."
- *Format:* "Working server code, plus instructions for running it
  locally and exposing it publicly."
- *Context:* your settled payload structure (Week 7), your settled
  tool list (item 3), and your project's use case.

**Design call made in this draft — flag for confirmation:** expose the
server publicly with **ngrok** (free tier, no signup complexity — same
"no-friction placeholder tool" precedent as Week 7's webhook.site), then
extend the Week 5/7 firmware to POST to the ngrok URL instead of
webhook.site. Not previously confirmed anywhere in this KB — see README
Open Item 5.

**Iteration 1 target:** real sensor data flowing from your device into
a server your team built and controls — the placeholder is gone.

*Deck: [Building the MCP Server & RTFC](./Presentations/MCP_Server_Build_RTFC.md).*

**5. Buffer / open work time** *(~40 min)*
Items 1–4 sum to 140 of the real 180-minute class. This is likely to be
the week's highest-variance day — server deployment/exposure issues are
new territory (unlike firmware, which every team has now done twice).
Every team should leave today with Iteration 1 working before starting
Day 2's "react" work.

## Carry-over to Day 2

Today's working sense-only MCP server is the foundation Day 2 extends
toward a "react" capability — Iteration 2.
