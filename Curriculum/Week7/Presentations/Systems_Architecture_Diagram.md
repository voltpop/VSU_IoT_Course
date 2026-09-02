# Systems Architecture Diagram

*Source: [`../Day1.md`](../Day1.md) item 4. ~40 min. Tool: **TLDraw**
(introduced Week 3) — no new tool needed this week.*

---

## From conceptual to technical

- Week 2 sketched **sense → connect → act/inform** — a plain loop,
  analog, conceptual.
- Today's diagram is the same loop, but with the actual technical
  stages a builder could follow, using this week's settled payload as
  the arrow labels.

---

## The stages to diagram

**Sensor → ESP32 → Wi-Fi → HTTP request → [receiving endpoint]**

- **Sensor** — physical device from Week 5.
- **ESP32** — local read + payload assembly (today's settled JSON
  structure).
- **Wi-Fi** — how the device gets online.
- **HTTP request** — the payload, sent somewhere.
- **[receiving endpoint]** — a placeholder today (Day 2), a real app
  starting Week 8. Label it as a placeholder explicitly — don't let
  the diagram imply this is the final destination.

---

## Do this in TLDraw

- One diagram per team, their own system, not a shared template
  filled in identically.
- Box-and-arrow, same notation as Week 2 — just more technically
  specific stages this time.
- Label each arrow with what actually crosses it (a sensor reading, a
  Wi-Fi connection, an HTTP POST with the settled payload).

---

## This becomes a deliverable

- Today's diagram **is** the System Architecture Diagram deliverable —
  commit it Day 2, alongside the integration test results.
