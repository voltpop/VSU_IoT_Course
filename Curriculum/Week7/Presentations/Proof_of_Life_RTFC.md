# Proof of Life & RTFC

*Source: [`../Day2.md`](../Day2.md) item 2. ~60 min. Extends Week 5's
firmware rather than starting over — the mechanical-generation step,
scaffolded the same way as every prior RTFC exercise.*

---

## What "proof of life" means today

- No real app exists yet to send data to — Week 6 only just started the
  app's UX design, Week 8 is where it actually gets built.
- Today's goal is narrower: prove the **whole path** works — sensor to
  somewhere off the device — using a free placeholder endpoint.

---

## The placeholder endpoint: webhook.site

- No signup. Gives you a unique URL. Shows each request live in the
  browser the moment it arrives.
- Makes "proof of life" **visible** — a non-technical team can watch
  their own reading show up in real time, not just trust that code ran
  without erroring.

---

## RTFC, extending Week 5's firmware

- **Role:** "You're a MicroPython firmware assistant for ESP32."
- **Task:** "Extend my existing sensor-reading firmware to connect to
  Wi-Fi and send each reading as an HTTP POST, using this payload
  structure, to this URL."
- **Format:** "Modify my existing script — keep the sensor-reading
  logic from Week 5, add Wi-Fi connection and an HTTP POST using
  `urequests`, with brief comments on the new parts only."
- **Context:** Week 5's working firmware (paste it in), yesterday's
  settled payload structure, your webhook.site URL, and the classroom
  Wi-Fi network name.

> Speaker notes: classroom network access is confirmed available
> (2026-09-02, per VoltPop) — individual device Wi-Fi connection issues
> are still normal on the day, just not a network-policy blocker.

---

## Verify

- Check your webhook.site page. Your payload showing up **is** the
  test passing — nothing more is required today.
- **No connection at all** → Wi-Fi credentials/network access issue,
  not a code problem — flag for an instructor rather than debugging
  firmware.
- **Connects but nothing arrives** → feed the actual error back into
  Context. Same debug loop as every prior RTFC exercise.

---

## What's next

- Week 8 replaces webhook.site with a real receiving app — today's
  endpoint was always a stand-in for proving the pattern, not the final
  destination.
