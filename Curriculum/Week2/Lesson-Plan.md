---
title: Week 2 — Understanding Systems & IoT Lesson Plan
week: 2
dates: Jan 26 (Tue) / Jan 28 (Thu)
status: draft — new as of 2026-08-28, first lesson plan built for this week (Course-Curriculum.md §6 previously listed it as not-yet-built)
see_also: Course-Curriculum.md §1 (curriculum philosophy, judgment/mechanical pattern), §4 (schedule), §5 finding #4 & §7 item #13 (regional-focus gap this plan re-introduces), §8 (stakeholder stakes), §6 (lesson-plan status); Admin-Business-Legal.md §6 (hardware kit quantities); Curriculum/Week1/Lesson-Plan.md (tooling this week assumes is already working)
---

# Week 2 — Understanding Systems & IoT

**Audience reminder (Course-Curriculum.md §1):** still business students,
not developers or engineers. This is the course's first real academic
content week (Skill: **Systems Thinking**), but hardware stays purely
exploratory — actual wiring/firmware doesn't start until Week 5. Today's
"device tinkering" is a motivator, not instruction.

**Prerequisite:** every team has working GitHub + Kiro access and a
functioning notes-KB repo from Week 1
(`Curriculum/Week1/Lesson-Plan.md`). If a team's
setup didn't fully land, fix it before this week's content — everything
below assumes teams can already commit to their repo and talk to Kiro.

**Design call made in this draft — flag for confirmation:** this plan
re-introduces the Tri-Cities/regional-industry framing into use-case
selection that V1's schedule had and V2's dropped (Course-Curriculum.md
§5 finding #4, §7 item #13). The KB's own cross-check (§8) names this
the single highest-leverage fix for stakeholder alignment — several
pitches (Cameron Foundation, VGR, Southern Company, Dominion) assume
students land on regionally-relevant projects, and nothing in the
current schedule actually required that. This draft treats item #13 as
resolved in that direction; revert Day 1 item 3 below if that's not
actually the call.

## Learning objectives

By the end of Week 2, students can:
- Describe an IoT system as a loop — **sense → connect → act/inform** —
  and give an example that isn't the one taught in class.
- Explain the difference between a passive-monitoring system and a
  sense-*and*-actuate one, and why the latter is a stronger (not
  mandatory) target for this course (Course-Curriculum.md §1).
- Name a real, regionally-relevant problem as their team's candidate use
  case, and justify it in one paragraph.
- Have physically powered on and explored an ESP32 + sensor kit, with no
  wiring or code involved yet.
- Apply the **4D framework** (Delegation, Description, Discernment,
  Diligence) to evaluate an AI-assisted brainstorm of use-case ideas —
  the course's first real exercise of the judgment-step pattern named in
  Course-Curriculum.md §1.
- Produce a Use Case Report and a Systems Mapping diagram for their
  chosen candidate use case, and publish a post about it.

## Day 1 (Tue, Jan 26) — Systems Thinking & Regional Use-Case Exploration

**1. Recap + bridge from Week 1** *(~10 min)*
Quick round: confirm every team's repo/Kiro/portfolio survived the week.
Frame the shift explicitly: *"last week was tools, this week is the
first real content — what actually is an 'IoT system,' and what's ours
going to be?"*

**2. Systems thinking mini-lecture** *(~25 min)*
Teach the loop, not the electronics:
- **Sense** — something measures a piece of the physical world (a
  temperature, a door opening, a soil moisture level).
- **Connect** — that reading gets somewhere it can be used (an app, a
  dashboard, another device).
- **Act / inform** — something happens with it: a person is told, or a
  device *does* something in response.
- Two or three concrete, non-technical examples, contrasting
  passive-monitoring vs. sense-and-actuate: a smart thermostat (senses
  temp, acts by changing HVAC) vs. a basic temperature display (senses,
  informs, doesn't act); a soil-moisture sensor that just shows a number
  vs. one that triggers irrigation. Reinforce §1's framing: sense-and-
  actuate is the stronger portfolio outcome, not a requirement — don't
  let a team force it onto a problem where it doesn't fit.

**3. Regional framing — pick something real, ideally something local**
*(~20 min)*
Explicit prompt: *"look for a problem in our own region."* Offer
already-researched regional sectors as **inspiration, not a
checklist** — agriculture (see the AI-agriculture angle in
`Stakeholder-Notes.md`), manufacturing/shipbuilding, the power grid,
personal finance — but make clear a team can pick anything real to them
near where they live. The point of naming these is credibility ("real
people are already thinking about this"), not narrowing the field.
Avoid over-anchoring every team on agriculture — regional relevance is
the goal, not a specific industry.

**4. Device tinkering — hands-on, no wiring/code** *(~40 min)*
Hand out one kit per team from the shared hardware pool (ESP32-DevKitC-
32, breadboard, a couple of sensors — Admin-Business-Legal.md §6; 84
ESP32 / 80 breadboards / 131 sensors bought as an undifferentiated pool
on purpose, since the specific sensor is irrelevant per Course-
Curriculum.md §1). Today's only ask: power the board on via USB, look at
what's on the board and the sensor(s), poke at them. No wiring, no
firmware — that's Week 5. The point is tactile: *"what could this thing
sense or do inside a system you actually care about?"*

**5. 4D framework preview — is this actually a good use case?**
*(~25 min)*
Model this live with Kiro, naming each step as you go (first real
exercise of the judgment-step pattern, Course-Curriculum.md §1):
1. **Delegation** — decide what to hand to the AI vs. decide yourselves.
   Delegate the brainstorm; keep the final pick as your own call.
2. **Description** — give Kiro real context, not a generic ask:
   *"Brainstorm 5 IoT use-case ideas for [a regional problem your team
   names], each with a rough sense/act loop."* A vague ask like "give me
   IoT ideas" produces generic junk — same lesson as Week 1's bad-prompt
   demo, now applied to a judgment task instead of a mechanical one.
3. **Discernment** — as a team, throw out the weak/generic ideas. Keep
   what's actually specific and locally grounded.
4. **Diligence** — sanity-check what's left: can an ESP32 + a sensor +
   an app actually approximate this, in the ~13 weeks remaining, by a
   team with no EE/CS background? If not, it's not a good pick yet — go
   back to step 2 with tighter context.

**Carry-over to Day 2:** each team narrows to 1–2 candidate use cases.

## Day 2 (Thu, Jan 28) — Systems Mapping & Use Case Report

**1. Recap** *(~10 min)*
Rapid-fire, one sentence per team: their 1–2 candidate use cases.

**2. Systems mapping exercise** *(~40 min)*
Teach a plain box-and-arrow notation: **Sense → Connect →
Process/Decide → Act/Inform**, plus a note on who/what is affected at
each stage. **Keep this analog for now** — paper or a whiteboard sketch,
or a simple diagram sketched directly in the notes-KB. TLDraw isn't
introduced until Week 3 (Course-Curriculum.md §4's tools column); don't
reach for it early. Each team maps their leading candidate use case.

**3. Use Case Report — an RTFC exercise** *(~40 min)*
Where Day 1's use-case *pick* was the judgment-heavy step (4D), turning
the team's rough notes into a written report is the mechanical-
generation step — scaffold it with **RTFC**, previewed in Week 1 and
formally named in Week 5:
- *Role:* "You're a concise business analyst."
- *Task:* "Turn my rough notes below into a 1-page Use Case Report."
- *Format:* "Markdown, with headers: Problem / Users / Current State /
  Proposed IoT Solution / Why It Matters Locally."
- *Context:* the team's actual notes from Day 1–2 pasted in.
Each student/team runs this through Kiro, then edits the output rather
than accepting it verbatim — same "specificity changes the output"
lesson as Week 1's bio exercise, now on a real deliverable.

**4. Post + submit** *(~20 min)*
- Commit the Use Case Report and the Systems Mapping diagram (or a
  photo/scan of the analog sketch) to the team's notes-KB repo.
- Publish a short post (portfolio and/or LinkedIn, per the recurring
  "& Post" pattern from Week 1) about the chosen use case — what it is,
  why it's regionally relevant, and what the team wants to build.

**5. Wrap — set expectations for Week 3**
Name explicitly that this use case is a **candidate, not locked in** —
Week 3 (Problem & User Discovery) validates it against real users and
personas before the team commits further. Don't let today's report read
as a final decision.

## Deliverables

- Use Case Report (per the schedule table, Course-Curriculum.md §4)
- Systems Mapping & Post

## Materials / resources

- One hardware kit per team from the shared pool: ESP32-DevKitC-32,
  breadboard, 1–2 sensors (Admin-Business-Legal.md §6). **Checkout/
  return logistics aren't decided anywhere in this KB** — see Open Items
  below.
- Paper/whiteboard for systems mapping (TLDraw deferred to Week 3).
- Kiro + GitHub access from Week 1 (`Curriculum/Week1/Lesson-Plan.md`).
- `Stakeholder-Notes.md` — source for the regional-sector examples
  offered in Day 1 item 3 (don't hand this file to students as-is; it
  contains outreach/fundraising content, not a student-facing resource).

## Open items — resolve before this plan is considered final

1. **Hardware kit checkout/return logistics aren't decided anywhere in
   this KB.** Who hands out the 84 ESP32 units / 80 breadboards / pooled
   sensors to ~15–20 teams, how it's tracked, and whether a team keeps
   the same physical kit all semester or it's checked back in after
   today's tinkering — none of this is scoped. Directly affects Day 1
   item 4's timing and whether Week 5 can assume teams already have
   "their" kit.
2. **Regional-focus reintroduction (see the design-call note at the
   top) needs explicit confirmation, not just this draft's assumption.**
   If confirmed, Course-Curriculum.md §7 item #13 and §5 finding #4 can
   be marked resolved and cross-referenced here; if not, Day 1 item 3
   needs rewriting to drop the regional steering.
3. **This is the first time the 4D framework is actually scripted as a
   classroom exercise anywhere in this KB** — Day 1 item 5's script is
   original design, not sourced from an existing plan or a decision
   VoltPop has already reviewed. Worth a sanity check before teaching
   from it, same as any new exercise.
4. **Not this week's gap, but adjacent — noted so it isn't mistaken for
   an oversight here:** the Scope Doc's mentor-interview deliverable
   (Course-Curriculum.md §5 finding #2, §7 item #2) lands on **Week 3**
   under V2's renumbering, not Week 2. Nothing above addresses it on
   purpose.
