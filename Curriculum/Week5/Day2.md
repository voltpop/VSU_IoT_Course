---
title: Week 5, Day 2 — Hardware Setup & Sensor Basics (Thursday)
week: 5
day: 2
date: Feb 18 (Thu)
duration: 3 hours (180 min): 130 min fixed content, 50 min buffer
status: draft
see_also: ./README.md (shared framing, deliverables, open items); ./Day1.md
---

# Week 5, Day 2 (Thu) — Finish the Build, Document It, Post It

**1. Build stand-up** *(~15 min, per Course-Curriculum.md §1)*
First live run of this pattern anywhere in the course — spend the first
~3–5 min explaining it before running it:
1. **Write (~5 min).** Each team posts a 3-line note to their notes-KB:
   what we got wired/working since Day 1, what we're stuck on, what we
   need.
2. **Match (~5–10 min).** Instructor scans the room/notes and calls out
   2–3 pairings — a team stuck on something another team already solved
   (a common one to expect: 3.3V-vs-5V confusion, or a firmware read
   returning garbage values). Those teams huddle briefly.
3. **Optional public share** if time allows — one callout to the room.

*Deck: [Build Stand-Up](./Presentations/Build_Standup.md).*

**2. Finish wiring/firmware from Day 1** *(~40 min)*
Whatever didn't finish Tuesday — prioritize teams still stuck on the
safety-diligence check (item 3 in Day 1) over teams just polishing
firmware output. Use the stand-up's pairings from item 1 as the first
place to send a stuck team before pulling in an instructor.

**3. Hardware Repo Setup + Firmware & Docs work** *(~45 min)*
Finalize the deliverables:
- Commit the working firmware to the team repo.
- Fill in the README started Day 1: purpose, **final** wiring pin-map,
  how to run the firmware in Thonny.
- **Commit the wiring diagram and connection table Kiro already
  generated during Day 1's 4D exercise** (item 3) into the repo docs —
  no separate diagramming step or tool needed. **Changed, 2026-09-02
  (per VoltPop):** earlier drafts of this plan had teams redraw the
  wiring in Canva here; testing showed Kiro's own output (breadboard
  diagram + connection table + build steps, in one generation) already
  covers this, so that redundant step is cut. Canva's role this week is
  now unresolved again — see README Open Item 3.
- Confirm the license file added Day 1 is actually committed.

*Deck: [Hardware Repo Docs & Post](./Presentations/Hardware_Docs_and_Post.md).*

**4. Post + submit** *(~20 min)*
Publish the recurring "& Post" update (portfolio/LinkedIn) — a short
one covering what got built this week, with a photo of the physical
wiring and/or the Kiro-generated diagram. This is the first "& Post"
with an actual physical artifact behind it, not just a written
deliverable — worth naming that shift to students.

**5. Wrap — preview Week 6** *(~10 min)*
Name explicitly that Week 6 (Designing the User Experience) shifts lead
to Builder Tech and moves from hardware to the app-side user flow — the
hardware built this week is what that app will eventually connect to
(Week 7's data-flow work), not something this week finishes for good.
Teams should expect to revisit and extend this wiring/firmware later,
not treat it as done.

**6. Buffer / open work time** *(~50 min)*
Items 1–5 above sum to 130 of the real 180-minute class. Not idle time
— circulate and confirm every team has committed working firmware, a
filled-in README with wiring pin-map, the Kiro-generated wiring diagram
and connection table, a license file, and a published post before the
day ends. This is the
day most likely to need the buffer for genuine catch-up (finishing
Day-1 wiring/firmware), not just polish.

## Deliverables due

- Hardware Repo Setup
- Firmware & Docs & Post
