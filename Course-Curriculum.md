---
title: VSU Innovation Program — Course & Curriculum
compiled: 2026-07-31
updated: 2026-08-14
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
- **Strive for sense-*and*-actuate projects, not just passive
  monitoring — but don't mandate it (per VoltPop, 2026-08-06):** given
  the AI-agriculture positioning developed for the Southern Company
  pitch (`Stakeholder-Notes.md`) and the expectation that a real share
  of student projects will land on some kind of sensor relevant to
  agri-tech, projects should be encouraged to not just monitor an
  environment but meaningfully modify it (e.g., a moisture sensor
  driving an irrigation actuator, not just a moisture readout) — closer
  to what an actual "AI-powered farm" needs, and a stronger portfolio
  outcome than a read-only dashboard. **Not a hard requirement**: not
  every real regional problem a team picks will have a natural fit for
  actuation, and forcing it onto a mismatched problem would undercut
  the "specific sensor/component is irrelevant" philosophy above —
  strive for it where the problem allows, don't force it where it
  doesn't.

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

**Week-count, confirmed authoritative (per VoltPop, 2026-08-14 tag-up):**
**16 weeks total calendar span (including 1 week off for spring
break); 15 weeks of actual course content.** This resolves the pitch
deck's week-count reconciliation flag (`TODOs-by-Owner.md`'s VoltPop
Administrative table) in the deck's favor. **Not yet reconciled against
the table below:** the V2 table shows 14 numbered content weeks (one of
which, Week 13, is an explicit no-new-content Buffer Week) plus separate
unnumbered spring-break and Finals rows — that structure doesn't cleanly
map onto "15 content weeks" yet. Reconciling the actual week-by-week
table to match is still open, not assumed done by this note.

## 4. Full V2 schedule table (current authoritative schedule)

| Week | Tue | Thu | Topic | Description | Skill | Deliverables | Tools | Lead | Support |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Jan 19 | Jan 21 | Course Kickoff | Program intro, account creation, git/GitHub basics, notes-KB setup (Kiro-fronted), prompt engineering, first social post | Prompt Engineering & Context Management | Portfolio & LinkedIn; First Public Post | GitHub, Kiro | All | All |
| 2 | Jan 26 | Jan 28 | Understanding Systems & IoT | Use-case exploration; students pick their own use case; device tinkering | Systems Thinking | Use Case Report; Systems Mapping & Post | + IoT Prototypes | **VoltPop** | Builder Tech, Explay |
| 3 | Feb 2 | Feb 4 | Problem & User Discovery | Problem validation, persona, current-state stories & flow | Design Thinking & Problem Solving | Problem Statement; Persona & Journey Map & Post | + TL Draw | Builder Tech | Explay |
| 4 | Feb 9 | Feb 11 | Business Models & Market Fit | Generate/evaluate ideas, brand identity, project page | Business Model Design & Strategic Planning | Business Model Canvas; Brand Identity Launch & Post | same | Explay | Builder Tech |
| 5 | Feb 16 | Feb 18 | Hardware Setup & Sensor Basics | Extend the existing GitHub repo to hardware/firmware code, open-source governance intro, ESP32 power-on/sensor/breadboard; firmware | Hardware Prototyping & Firmware Basics | Hardware Repo Setup; Firmware & Docs & Post | + Canva, MicroPython/Thonny, ESP32/Breadboard/Sensors | **VoltPop** | Builder Tech, Explay (TBD) |
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

**Explay ownership confirmation (2026-07-31):** Explay confirmed the
lead and support assignments shown above: lead for Weeks 4 and 9–12,
and support for Weeks 2, 5, 7, and 8. Week 9's detailed division of
product-iteration, technical-debugging, integration, and security work
between Explay and VoltPop remains to be defined.

**Day 1 plan — updated 2026-08-08 (per VoltPop):** account creation is
now **GitHub and Kiro**, replacing ChatGPT/Claude/Codex/Gemini —
Claude Code/Codex and Gemini are expected to be superseded by Kiro
outright (see §7 item #15), and Lovable is deferred out of Day 1
entirely (UI-design-only, introduced later when actually used). Day 1
now also covers **git/GitHub basics** (hand out the Git Cheat Sheet,
§6) and setting up the **notes knowledge base, fronted by Kiro** — the
same git-based-KB model this program's own team uses. **Portfolio setup
and the first public LinkedIn post both stay on Day 1**, per VoltPop.
**Portfolio mechanism — proposed, not yet locked (per VoltPop,
2026-08-08): a per-group GitHub Pages site**, not an individual
portfolio — fits the GitHub-from-day-one direction above, and pairs
naturally with the git-based notes KB (same repo, same tool). **Open
tension worth resolving explicitly:** VoltPop also floated using
Lovable for that GitHub Pages site's UI — which would mean Lovable
comes back into Day 1 for this one specific use (UI design for the
portfolio site), even though it's otherwise being deferred out of Day 1
entirely (see above). Worth deciding directly: Lovable-designed on Day
1, or a plainer Day-1 page with Lovable's UI polish applied later once
it's actually introduced. Also unconfirmed: whether "group" replaces an
individual portfolio outright, or sits alongside one. Needs resolving
before this reaches an actual lesson-plan rewrite (the built file lives
outside this repo, in VoltPop's own working files —
see §6 below).

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

4. **Regional/Tri-Cities industry focus dropped from Week 2 (flagged
   2026-08-06, per VoltPop).** V1's Week 2 explicitly said "choose a
   Tri-Cities industry/problem focus." V2's equivalent week (Week 2:
   Understanding Systems & IoT) just says "students pick their own use
   case" — the explicit regional-industry steering is gone, not
   carried forward. This matters beyond internal consistency: several
   stakeholder pitches in `Stakeholder-Notes.md` (Cameron Foundation,
   Virginia Gateway Region, Southern Company's AI-agriculture angle,
   Dominion's smart-grid angle) all assume students land on regionally-
   and industrially-relevant projects — nothing in the current schedule
   actually guarantees that. **Needs re-introducing**, ideally back into
   Week 2's use-case-selection language rather than left as an
   unenforced assumption.

## 6. Lesson-plan status

Lesson plans tracked in this repo live in the `Curriculum/` directory,
one subdirectory per week (`Curriculum/WeekN/`, restructured
2026-08-28 from a flat one-file-per-week layout so each week has a
place for its lesson plan, assets, and eventually presentations — see
`AGENTS.md`'s file-split conventions). Weeks not yet moved in still
have working notes, if any, in `~/Documents/VoltPop/IoT_Course/`
(VoltPop's own working files, outside this repo):
- [`Curriculum/Week1/Lesson-Plan.md`](./Curriculum/Week1/Lesson-Plan.md) — the prior version (built
  against V2's original Lovable/ChatGPT/Claude/Codex/Gemini plan) was
  lost — VoltPop's external working-files copy couldn't be located
  (2026-08-08). **Rebuilt from scratch, now tracked in this repo** (not
  an external file anymore, precisely so it can't go missing the same
  way again) — reflects the 2026-08-08 Day 1 update above: GitHub/Kiro
  account creation, git basics, notes-KB setup, and a proposed
  per-group GitHub Pages portfolio. Marked `status: draft` in its own
  frontmatter — several real open items listed at the bottom of the
  file (portfolio mechanism, GitHub org structure, Kiro provisioning,
  untested timing) still need resolving before it's final.
- `Week5_AI_Wiring_Firmware_Prompt_Template.md` — built for
  MicroPython/Thonny (confirmed as the right toolchain, see §4); needs
  one new section added for Week 5's Tuesday content (GitHub migration,
  open-source governance intro) that isn't in the file yet. **When that
  section gets built (flagged 2026-08-08, per VoltPop):** include
  GitHub Education's [Git Cheat
  Sheet](https://education.github.com/git-cheat-sheet-education.pdf) as
  a student handout — students are being introduced to git/GitHub cold
  here, same onboarding gap this KB itself solves for the five program
  parties via `AGENTS.md`'s own pointer to the same resource. **Open
  question, same day (per VoltPop):** whether this git/GitHub
  introduction should actually move earlier than Week 5 — possibly
  Week 1 — so students have git-based-knowledge-base literacy from day
  one rather than only once firmware work starts; see §7 item #15's
  per-tool timing breakdown.
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
- [`Curriculum/Week2/Lesson-Plan.md`](./Curriculum/Week2/Lesson-Plan.md) —
  built 2026-08-28 (V2 makes VoltPop Lead for this week, which wasn't
  anticipated under the earlier schedule version, so no prior draft
  existed to build from). Marked `status: draft` — re-introduces the
  regional/Tri-Cities framing dropped between V1 and V2 (§5 finding #4,
  §7 item #13) as a design call needing explicit confirmation, and
  leaves hardware-kit checkout/return logistics unresolved (see the
  file's own Open Items).
- **Weeks 4, 9, 10, 11, 12** (all Explay-led) have no lesson-plan-status
  tracking in this KB at all — unlike the VoltPop-led weeks above, it's
  not documented here whether lesson plans for any of these exist,
  are drafted, or still need to be built from scratch.

## 7. Open items — curriculum and teaching

1. Decide how (or whether) to restore a dedicated Security
   Considerations deliverable given the demotion in V2 Week 9.
2. Confirm/add a mentor-interview deliverable to Week 3 if that
   requirement still stands. **Higher stakes than a Scope-Doc technicality
   (flagged 2026-08-06, per VoltPop):** mentors/guest speakers are one of
   the in-kind asks actively being made of donors (Siemens/Jabil/
   Huntington Ingalls cluster, ASF, Deloitte all carry a mentor or
   guest-speaker ask in `Stakeholder-Notes.md`) — if the curriculum has
   no early, structured mentor touchpoint, there's a real mismatch
   between what's being solicited from stakeholders and what the course
   actually does with it. Resolve this alongside the donor-mentor asks,
   not as a separate curriculum-only question.
3. Build a lesson plan for Week 2.
4. Rewrite Week 7's lesson plan around Data Flow & Systems Architecture.
5. Adapt the MCP-server lesson into Week 8.
6. Retrofit Week 5's materials to explicitly name the 4D/RTFC framework,
   and name RTFC explicitly as Week 8's default template.
7. Design Week 9's shrunken security/APIs content around the 4D lens
   rather than leaving it unstructured.
8. Get Week 8's leadership (VoltPop) and the API→MCP swap actually
   entered into the live schedule sheet.
9. Correct Week 5's tools column (Arduino IDE → MicroPython/Thonny) in
   the live schedule sheet.
10. Resolve which AI-coding tool students will actually have funded
    access to (Claude Code vs. ChatGPT/Codex) — see
    `Admin-Business-Legal.md` §6 — before further lesson-plan rewrites
    lock in one tool's prompts over the other.
11. Establish lesson-plan status (built / drafted / not started) for
    Explay's five lead weeks (4, 9, 10, 11, 12), matching the tracking
    already kept for VoltPop's weeks in §6.
12. Decide whether to reintroduce a named "elevator pitch" deliverable
    in Weeks 11–12 (Explay-led), present in V1's schedule but dropped
    from V2's pitch weeks (see §5).
13. **Re-introduce the Tri-Cities/regional-industry focus into Week 2**
    (flagged 2026-08-06, per VoltPop, see §5 finding #4) — dropped
    between V1 and V2; several stakeholder pitches depend on students
    actually landing on regionally-relevant projects, which the current
    Week 2 language no longer requires.
14. **Pare down the full tools list to what's roughly essential**
    (flagged 2026-08-08, per VoltPop) — the current list, compiled
    across this schedule's per-week Tools column and
    `Admin-Business-Legal.md` §6's software/hardware budget tables, is
    long (ChatGPT Plus, Claude Code/Codex, Claude/ChatGPT, Gemini/DALL-E,
    Kiro, Lovable, TLDraw, GitHub, Postman, Canva, MS Office, Zoom, plus
    the firmware/hardware toolchain) and has never been deliberately
    trimmed — related to, but broader than, item #10's narrower
    AI-coding-tool funding question above.
15. **Decide when each tool actually gets introduced in the
    curriculum** (flagged 2026-08-08, per VoltPop) — **stated principle:
    earlier is better**, but no actual per-tool integration timing has
    been agreed on beyond what's implicit in the existing per-week Tools
    column. Resolve alongside item #14 above, since a shorter tool list
    is also an easier one to front-load early — don't decide the list
    and the timing as two separate passes. **"Earlier" isn't a blanket
    rule for every tool — per-tool emerging direction (2026-08-08, per
    VoltPop):**
    - **Git/GitHub — scope clarified, 2026-08-08 (per VoltPop): not
      just the microcontroller/firmware code, but the entire curriculum
      notes corpus too** — students keeping their own notes/docs in a
      git repo, the same git-based-knowledge-base model this actual KB
      uses internally, not just a Week-5 firmware-versioning tool. This
      materially strengthens the case for introducing it **earlier than
      Week 5, possibly Week 1** — a notes corpus is needed from day one,
      not just once hardware work starts. Still an open timing question,
      not decided (see the note added to §6 above).
      **Architecture, same day (per VoltPop): the students' git-based
      notes knowledge base is meant to be *frontended by Kiro*** — Kiro
      as the interface students actually interact with, sitting on top
      of the git repo, mirroring exactly how this program's own
      five-party KB works (this repo + Kiro/Claude/Gemini as
      interchangeable front-ends via `AGENTS.md` and its per-tool
      mirrors). Worth cross-referencing the still-open "give me
      information about this program" web-feature idea and the
      "something more polished for presentation day" idea
      (`TODOs-by-Owner.md`) — a Kiro-fronted KB may be the actual answer
      to both, not a separate third thing.
    - **Kiro (Amazon):** per the escalated claim in
      `Stakeholder-Notes.md`'s Amazon/Kiro profile, **Claude Code/
      Codex and Gemini may all be replaced by Kiro outright** — reasoning
      given: "Kiro + GitHub is not as heavy a lift." If this holds,
      Week 1's current tools list (Lovable, Claude Code/Codex, Claude/
      ChatGPT, Gemini/DALL-E) shrinks considerably. Not yet a locked
      decision.
    - **Lovable — scope narrowed, 2026-08-08 (per VoltPop): UI design
      only**, not the broader app-build/portfolio-hosting role implied
      by Week 1's current "portfolio via Lovable" framing. Combined with
      the deferred-timing call below, this is a smaller, later role than
      the current schedule gives it — **defer introduction to whenever
      it's actually first used** for UI design specifically, rather than
      Week 1's current Day-1 portfolio setup. "Earlier is better"
      applies to tools students need continuously from day one (git, the
      core AI assistant); it doesn't automatically apply to a
      narrow-scope tool whose real use starts later in the schedule.
16. **Does the Kiro-replaces-Claude/Codex/Gemini direction break
    anything Javon already laid out? (raised 2026-08-08, per VoltPop)**
    Checked against the current V2 schedule (§4) and lesson-plan status
    (§6) — three findings:
    - **Core course structure: unaffected.** All 14 weeks' topics,
      skills, deliverables, and lead/support assignments are untouched;
      the Tools column cascades cleanly from Week 1 via "same," so
      Weeks 2–14 don't need individual edits.
    - **VoltPop's built lesson-plan content: confirmed not a blocker
      (per VoltPop, 2026-08-08)** — "VoltPop doesn't have anything in
      particular written around Claude that wouldn't also apply to
      Kiro," despite `Admin-Business-Legal.md` §8's note that his
      lesson plans were "written specifically around Claude Code."
      Resolved: the content itself is generically AI-assisted-
      development, not Claude-specific in a way that breaks.
    - **Still open, not yet addressed:** Week 8's "MCP integration"
      content assumes MCP server support — unconfirmed whether Kiro
      supports MCP the same way Claude Code does.
    - **Resolved (per VoltPop, 2026-08-12): deprioritize the Claude
      Corps/Claude for Education funding pitch.** VoltPop's current
      leaning is that the program uses Kiro as the classroom tool — not
      yet locked in (still needs an explicit "yes, actually decided"
      checkpoint, per the escalated note in `Stakeholder-Notes.md`'s
      Amazon/Kiro profile), but firm enough to shift funding-pitch
      priority now: Claude Corps' strongest angle was tooling match,
      which no longer holds if Kiro is the actual classroom tool.
      Funding focus shifts to the Amazon AI-tooling donation angle
      (`Stakeholder-Notes.md`'s Amazon/Kiro profile) instead.
17. **[New, backfilled 2026-08-24 from the 2026-08-18 tag-up, per
    VoltPop]** Reconcile the cohort's academic composition with the
    2026-08-18 decision to bring actual Agriculture students into the
    cohort alongside Business and Engineering (`Admin-Business-Legal.md`
    §4/§9) — the "audience is business students, not ag-science
    students" caveat in `Stakeholder-Notes.md`'s Southern Company
    section no longer holds as stated and needs updating, and the
    curriculum itself may need Ag-relevant project options/examples
    once this is formalized. Not yet assessed for schedule/content
    impact — this item just flags that the assessment is needed.

## 8. Curriculum vs. stated objectives, and stakeholder reception (2026-08-06)

Reference check requested by VoltPop — how V2's actual schedule holds
up against the program's own stated goals/outcomes (`Admin-Business-
Legal.md` §4), and how it would land with the stakeholders profiled in
`Stakeholder-Notes.md`. Kept here (not just in conversation) since both
are likely to come up again, including at the Aug 7 meeting.

### Goals/outcomes scorecard

| Goal/outcome | Curriculum support | Gap |
|---|---|---|
| Competitive job candidates | Portfolio (Wk1, Wk14), resume, Career Day | Solid |
| Regional economic reinvestment | Week 2 use-case selection | **Weakened** — Tri-Cities framing dropped V1→V2 (see §7 item 13) |
| Explore emerging tech on real problems | IoT hardware weeks, AI-assisted dev throughout | Solid |
| Entrepreneurship/PMF | BMC (Wk4), idea evaluation, pitch weeks | Solid |
| Connect to mentors *early* | — | **Missing** — Week 2/3 mentor-interview deliverable absent from V2 (see §7 item 2); only known mentor touchpoint is Career Day at the very end |
| Outcome: "elevator pitch" named deliverable | — | Already-flagged gap (§5) — dropped from V2's pitch weeks despite being a stated outcome |
| Outcome: financial model | BMC (partial) | No explicit financial-model deliverable — weakens the Virginia Credit Union financial-literacy pitch specifically |

### Stakeholder reception, given what's actually in the schedule

- **Claude Corps** — strongest alignment of any stakeholder pitch. The
  4D framework isn't just mentioned, it's the course's literal
  structural spine (§1) — this pitch is fully backed by the actual
  curriculum, not just narrative.
- **Digital-manufacturing cluster (Siemens/Jabil/Huntington Ingalls)** —
  solid. Hardware weeks (5, 7, 8) genuinely deliver hands-on IoT
  exposure, consistent with the "toe-dip, not engineering-depth"
  framing already used in outreach.
- **Apache Software Foundation** — solid. GitHub + open-source
  governance is explicitly in Week 5.
- **Open Trellis / Deloitte (business-education)** — solid. BMC and
  pitch weeks directly support this pitch.
- **Southern Company (AI-agriculture)** — the sense-and-actuate
  encouragement added to §1 helps, but it's a philosophy note, not yet
  propagated into the actual Week 5/8/9 deliverable language — and it
  still depends on a team choosing an ag-relevant use case, which
  nothing currently steers toward (see §7 item 13).
- **Cameron Foundation / VGR / Dominion (regional/utility)** — same
  structural risk as Southern Company: the pitch promises regional
  relevance the schedule doesn't currently guarantee.
- **Virginia Credit Union (financial literacy)** — weakest-supported
  pitch of the group; no named financial-model deliverable exists to
  point to.

**Bottom line:** one fix — restoring Week 2's regional/industry-focus
requirement (§7 item 13) — de-risks the largest number of stakeholder
pitches at once (Cameron, VGR, Southern Company, Dominion all depend on
it). Everything else here is stakeholder-specific and smaller in scope.
