---
title: Week 7, Day 2 — Data Flow & Systems Architecture (Thursday)
week: 7
day: 2
date: Mar 4 (Thu)
duration: 3 hours (180 min): 145 min fixed content, 35 min buffer
status: draft
see_also: ./README.md (shared framing, deliverables, open items); ./Day1.md
---

# Week 7, Day 2 (Thu) — Proof of Life

**1. Build stand-up** *(~15 min, per Course-Curriculum.md §1)*
- What's blocking today's integration attempt before it starts? Common
  Week 7 blocker to expect: a team whose payload from Day 1 is still
  vague, not a coding problem — send them back to the 4D exercise
  before they touch code.

**2. "Proof of life" integration — the mechanical-generation step**
*(~60 min)*
No real app exists yet to send data to — Week 6 only just started the
app's UX design, and the actual app isn't built until Week 8. Today's
goal is narrower and achievable: prove the **whole path** works, sensor
to somewhere off the device, using a free placeholder endpoint
(**webhook.site** — no signup, shows each request live in the browser
as it arrives, which makes "proof of life" visible to a non-technical
team in real time).

Scaffold with **RTFC**, extending Week 5's settled firmware rather than
starting over:
- *Role:* "You're a MicroPython firmware assistant for ESP32."
- *Task:* "Extend my existing sensor-reading firmware to connect to
  Wi-Fi and send each reading as an HTTP POST, using this payload
  structure, to this URL."
- *Format:* "Modify my existing script — keep the sensor-reading logic
  from Week 5, add Wi-Fi connection and an HTTP POST using `urequests`,
  with brief comments on the new parts only."
- *Context:* Week 5's working firmware (paste it in), yesterday's
  settled payload structure, the team's webhook.site test URL, and the
  classroom Wi-Fi network name (**pending confirmation this actually
  works on VSU's network** — see README Open Item 5).

**3. Verify + debug** *(~30 min)*
Confirm the payload actually shows up on the webhook.site page —
that's the whole test. If it doesn't:
- No connection at all → Wi-Fi credentials or network access issue,
  not a code problem.
- Connects but nothing arrives → feed the actual error back into RTFC's
  Context, same debug loop as every prior firmware exercise.

**4. Commit + post** *(~30 min)*
- Commit the integration firmware and the Day 1 architecture diagram to
  the team repo.
- Publish the recurring "& Post" update — this time with something
  genuinely demonstrable: a screenshot of their own reading arriving on
  webhook.site.

**5. Wrap — preview Spring Break, then Week 8** *(~10 min)*
Name explicitly: Spring Break is next (no classes), then Week 8 is
where a real receiving app replaces today's placeholder endpoint — the
webhook.site URL was a stand-in for proving the pattern works, not the
final destination.

**6. Buffer / open work time** *(~35 min)*
Items 1–5 sum to 145 of the real 180-minute class. This is the day
most likely to need genuine catch-up time — Wi-Fi/network issues are
the highest-variance failure mode of the whole week and may not be
something a team can debug their way out of alone (see README Open
Item 5).

## Deliverables due

- System Architecture Diagram
- End-to-End Integration Test & Post
