---
title: VSU Innovation Program — Course & Curriculum
compiled: 2026-07-31
updated: 2026-07-31
see_also: Admin-Business-Legal.md (business/legal side)
---

# VSU Innovation Program — Course & Curriculum

Curriculum philosophy, schedule, and lesson-plan status for the VSU
Innovation Program's technical track. For business/legal/budget
content, see `Admin-Business-Legal.md`.

## 1. Curriculum philosophy

The throughline that should govern all lesson design for the technical
track:

> **The audience is business students, not developers or engineers.**
> Most have no EE or programming background. The goal is a "toe-dip" —
> exposure to microcontrollers and AI-assisted development as tools —
> not fundamentals mastery of electricity, microcontrollers, or CS.

Concrete implications:

- **No electricity/EE fundamentals** — no Ohm's law, no GPIO internals.
  Hardware work is "plug the red wire into the red rail" recipe-
  following, not conceptual grounding.
- **The specific sensor/component is irrelevant — it's a vehicle, not
  the point.** The graded skill is using AI planning and prompt
  engineering to generate a wiring recipe, then generate firmware from
  it — not getting any particular sensor working.
- **3.3V safety framing**: essentially zero personal-injury risk at
  these voltage/current levels. The real risk is equipment damage (5V
  into a 3.3V-only GPIO, reversed polarity, shorts) — framed as "let's
  not waste kit budget," not a lab-safety briefing.
- **Heavy AI scaffolding, not open-ended prompting**: firmware-by-
  prompting needs a template/starter structure students fill in, not
  free generation from scratch.

### The reusable pattern: judgment-step / mechanical-step split

The course's structural spine, applied everywhere it asks students to
go from an ambiguous real-world ask to working code:

1. **Judgment-heavy step** (is this wiring safe? what should the spec
   include?) → scaffolded with Anthropic's **4D** AI-fluency framework:
   Delegation, Description, Discernment, Diligence.
2. **Mechanical-generation step** (turn the settled spec into working
   code) → scaffolded with **RTFC**: Role, Task, Format, Context.

## 2. Schedule history — V1 → V2 (current)

- **V1** — `Program Schedule & Sequence (2026 17 JULY - V1).ods`, full
  table in §3.
- **V2** — Google Sheet "Builder Tech Program Schedule (2026 July 31 -
  V2)", full table in §4. **Current authoritative schedule.** Note: the
  sheet's title date is a draft-date stamp, not a program-year claim —
  the actual dates are 2027, consistent with every other program doc.

## 3. Full V1 schedule table (superseded, kept for history)

| Week | Day | Topic | Description | Tools | Assignment |
|---|---|---|---|---|---|
| 1 | Tue/Thu | Prompt & Context Design and Engineering + Critical Thinking | Course intro; GitHub, Python; prompting and context management | Claude Code / Codex | Prompting exercise |
| 2 | Tue/Thu | Systems Thinking & Local Context | IoT as digitizing the physical world; choose a Tri-Cities industry/problem focus | Claude/ChatGPT/Gemini; Canva | Intro slide; industry focus slide |
| 3 | Tue/Thu | Design Thinking (Problem → User) | Validate the problem, persona, problem statement | Claude/ChatGPT/Gemini; Canva | Interview questions; persona slide; problem statement slide |
| 4 | Tue/Thu | Business Development & Product-Market Fit | Generate ideas, evaluate, lock direction | Claude/ChatGPT/Gemini; Canva | 5 ideas evaluated; chosen idea/brand |
| 5 | 3 sub-days | Hardware & Systems Eng Fundamentals, Sensor Survey & Wiring, Firmware Fundamentals | Microcontroller/electricity/GPIO intro, sensor wiring, firmware via AI prompting | ESP32/breadboard/sensors; Claude Code/Codex; Thonny | Wire sensor; firmware running |
| 6 | Day1/Day2 | Deploying & Debugging; "storyboard and data flow" | Confirm sensor data works; Day 2 owned by business SMEs | Thonny | Device working; confirmed in console |
| 7 | Tue/Thu | AI Assisted Prompt Design | Stack definition, user flow, data flow chart, web frontend, **MCP server design** | Claude Code/Codex; Replit/Lovable; Notion; Stitch | User stories; PRD; primary user flow; low-fi screens |
| 8 | Tue/Thu | AI Assisted Development | Build apps from prompts, test/debug | Claude Code/Codex; Replit/Lovable | Built first flow; testing notes |
| 9 | Tue/Thu | APIs & System Integration | Connect app to external system | same as Wk8 | Working API integration |
| 10 | Tue/Thu | Security Considerations | Continue building + security thinking | same as Wk8 | Continued build; security/PII/auth explanation |
| 11 | Tue/Thu | Test & Validate | Confirm works, validate with users, launch | GitHub | Full-scale user test; public launch |
| 12 | Tue/Thu | Pitch & Presentation Skills | Elevator pitches, self-presentation | Canva | Draft pitch materials |
| 13 | Tue/Thu | Build Presentations, Practice Pitch | Refine and rehearse | Canva | Practice run-throughs |
| 14 | Tue/Thu | Presentations (Live) | Live presentations | Canva | Final presentation delivered |
| 15 | Final Week | Present the Full Arc | Resume + portfolio due; Career Day | — | Resume, portfolio, Career Day |

## 4. Full V2 schedule table (current authoritative schedule)

| Week | Tue | Thu | Topic | Description | Skill | Deliverables | Tools | Lead | Support |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Jan 19 | Jan 21 | Course Kickoff | Program intro, account creation, prompt engineering, portfolio via Lovable, first social post | Prompt Engineering & Context Management | Portfolio & LinkedIn; First Public Post | Lovable, Claude Code/Codex, Claude/ChatGPT, Gemini/DALL-E | All | All |
| 2 | Jan 26 | Jan 28 | Understanding Systems & IoT | Use-case exploration; students pick their own use case; device tinkering | Systems Thinking | Use Case Report; Systems Mapping & Post | + IoT Prototypes | **VoltPop** | Builder Tech, Explay |
| 3 | Feb 2 | Feb 4 | Problem & User Discovery | Problem validation, persona, current-state stories & flow | Design Thinking & Problem Solving | Problem Statement; Persona & Journey Map & Post | + TL Draw | Builder Tech | Explay |
| 4 | Feb 9 | Feb 11 | Business Models & Market Fit | Generate/evaluate ideas, brand identity, project page | Business Model Design & Strategic Planning | Business Model Canvas; Brand Identity Launch & Post | same | Explay | Builder Tech |
| 5 | Feb 16 | Feb 18 | Hardware Setup & Sensor Basics | GitHub migration, open-source governance intro, ESP32 power-on/sensor/breadboard; firmware | Hardware Prototyping & Firmware Basics | GitHub Repo & Hardware Setup; Firmware & Docs & Post | + Canva, Arduino IDE (see note below), GitHub, ESP32/Breadboard/Sensors | **VoltPop** | Builder Tech, Explay (TBD) |
| 6 | Feb 23 | Feb 25 | Designing the User Experience | Future-state user flow, key screens, AI-polished prototype | User-Centered Design | Future State Journey Map; Low-Fidelity Prototype & Post | same | Builder Tech | Explay, VoltPop |
| 7 | Mar 2 | Mar 4 | Data Flow & Systems Architecture | Map sensor→app data flow/payload; "proof of life" hardware-software integration | AI-Assisted Design & Systems Integration | System Architecture Diagram; End-to-End Integration Test & Post | same | **VoltPop** | Explay (TBD) |
| — | Mar 9 | Mar 11 | SPRING BREAK | No classes | — | — | — | — | — |
| 8 | Mar 16 | Mar 18 | Full Build — Iterations 1 & 2 | Full app build; MCP integration (replacing prior API-integration framing); hardware integration; submit iter 1 & 2 | AI-Assisted Development & Full-Stack Integration | Iteration 1; Iteration 2 & Post | + Postman | **VoltPop** (pending update to shared sheet — see §5) | Explay |
| 9 | Mar 23 | Mar 25 | Full Build — Iterations 3 & 4 | Incorporate feedback, security concepts, submit iter 3 & final iter 4 | same | Iteration 3; Iteration 4 Final & Post | same | Explay | VoltPop |
| 10 | Mar 30 | Apr 1 | Testing & Going Live | Go-live publishing, go-to-market, public launch + demo video | Testing, Validation & Go-to-Market | Go-to-Market Strategy; Live Product & Demo Video & Post | same | Explay | VoltPop, Builder Tech |
| 11 | Apr 6 | Apr 8 | Crafting Your Pitch | Pitch structure/storytelling, pitch video, deck update | Pitch Development & Storytelling | Pitch Deck Outline; Pitch Deck Draft & Post | + PowerPoint | Explay | Builder Tech, VoltPop (TBD) |
| 12 | Apr 13 | Apr 15 | Practice & Feedback | Rehearse pitch, live judge feedback | Presentation Skills & Self-Review | Pitch Rehearsal & Peer Review; Video Submission & Post | same | Explay | Builder Tech, VoltPop (TBD) |
| 13 | Apr 20 | Apr 22 | Buffer Week | Slippage absorption, polish, no new content | — | — | — | — | — |
| 14 | Apr 27 | Apr 29 | Final Presentations & Portfolio Career Day | Final live presentations, portfolio recordings | Live Presentation & Portfolio Polish | Pitch Deck, Portfolio Site & MVP, Resume; Final Presentations | same | All | All |
| Finals Wk | May 4 / 11 | May 6 / 13 | Program Concluded | VSU Final Exams. No program activities | — | — | — | — | — |

**Tools-column note (Week 5)**: the shared sheet currently lists Arduino
IDE, but the actual firmware plan is **MicroPython/Thonny** (decided
2026-07-31 — Arduino IDE and MicroPython are incompatible ESP32
toolchains, so this needs correcting in the sheet, not just noted here).

**Week 8 leadership**: VoltPop was confirmed as Lead for Week 8 (was
Explay) in the 2026-07-31 Builder Tech meeting, on the basis that
VoltPop largely owns the technical portion of the program and should
drive the hardware/MCP-integration wrap-up before Explay's Week 9
iteration work. **This has not yet been entered into the live shared
schedule sheet** — as of the most recent check, the sheet still shows
Explay as Lead and still says "Integrate API connections" rather than
reflecting the MCP-integration swap. Both need updating in the actual
source sheet.

## 5. Cross-check findings (V2 schedule vs. Scope Doc / Agreement)

1. **Security Considerations demoted.** The Scope Doc/Agreement allocate
   a dedicated week to security with a named required deliverable
   (written/presented explanation of data security, PII, authentication).
   V2 only says "introduce security concepts" inside Week 9's hands-on
   build week, with no explicit deliverable — worth deciding whether to
   restore a real deliverable here.
2. **Mentor interview deliverable missing.** The Scope Doc requires a
   completed mentor interview (minimum 1) as a Week 2 deliverable. V2's
   equivalent week (Week 3: Problem & User Discovery) doesn't mention
   it — worth confirming whether this requirement still stands.
3. **Founder's Day / midterms-week calendar conflicts** — see
   `Admin-Business-Legal.md` §7.

Minor/non-blocking: the named "elevator pitch" outcome (present in V1's
schedule) isn't explicitly named in V2's pitch weeks, just deck/video/
rehearsal. The Scope Doc's optional "Agentic AI" stretch goal has been
dropped from V2 entirely — likely fine since it was optional, but worth
noting it as a dropped option rather than assuming it was never
considered.

## 6. Lesson-plan status

Built lesson plans live in `~/Documents/VoltPop/IoT_Course/` (VoltPop's
working files):
- `Week1_Course_Foundations_Lesson_Plan.md` — built, matches V2's Week 1
  closely; needs two small wording fixes (references to "designing an
  MCP server in Week 7," which no longer describes Week 7's topic).
- `Week5_AI_Wiring_Firmware_Prompt_Template.md` — built for
  MicroPython/Thonny (confirmed as the right toolchain, see §4); needs
  one new section added for Week 5's Tuesday content (GitHub migration,
  open-source governance intro) that isn't in the file yet.
- `Week7_MCP_Server_Design_Prompts.md` — originally built for the old
  Week 7 topic (MCP server design). Week 7's actual topic is now "Data
  Flow & Systems Architecture," which needs new content built for it
  (following the same judgment-step/mechanical-step 4D+RTFC pattern,
  re-pointed at payload/data-flow design and a proof-of-life
  integration build). The existing MCP-server content isn't wasted —
  it's being relocated into **Week 8**, where MCP integration now
  replaces the old "API integration" framing, and Week 8 is also
  VoltPop-led. Needs adaptation work, not a full rewrite, once that
  relocation is finalized.
- **Week 2** ("Understanding Systems & IoT") has no lesson plan built
  yet — V2 makes VoltPop Lead for this week, which wasn't anticipated
  under the earlier schedule version.

## 7. Open items — curriculum and teaching

1. Decide how (or whether) to restore a dedicated Security
   Considerations deliverable given the demotion in V2 Week 9.
2. Confirm/add a mentor-interview deliverable to Week 3 if that
   requirement still stands.
3. Build a lesson plan for Week 2.
4. Rewrite Week 7's lesson plan around Data Flow & Systems Architecture.
5. Adapt the MCP-server lesson into Week 8.
6. Fix Week 1's stray references to "designing an MCP server in Week 7."
7. Retrofit Week 5's materials to explicitly name the 4D/RTFC framework,
   and name RTFC explicitly as Week 8's default template.
8. Design Week 9's shrunken security/APIs content around the 4D lens
   rather than leaving it unstructured.
9. Get Week 8's leadership (VoltPop) and the API→MCP swap actually
   entered into the live schedule sheet.
10. Correct Week 5's tools column (Arduino IDE → MicroPython/Thonny) in
    the live schedule sheet.
11. Resolve which AI-coding tool students will actually have funded
    access to (Claude Code vs. ChatGPT/Codex) — see
    `Admin-Business-Legal.md` §6 — before further lesson-plan rewrites
    lock in one tool's prompts over the other.
