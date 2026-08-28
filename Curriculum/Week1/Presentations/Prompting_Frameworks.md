# Prompting Frameworks — RTFC & 4D

*Source: previewed in [`../Day2.md`](../Day2.md) item 2, formally named
in Week 5, and reused as the course's default scaffold for every
**mechanical-generation** step from here on (Course-Curriculum.md §1's
judgment-step/mechanical-step pattern). Also covers **4D**
(Delegation, Description, Discernment, Diligence), the companion
scaffold for **judgment-heavy** steps, first taught hands-on in
`Curriculum/Week2/Day1.md`. Written generic on purpose — the
bio/LinkedIn and use-case examples are illustrations, not the point.
Reuse or adapt this deck wherever either framework comes up again, not
just Week 1.*

---

## The AI is a tool you direct

- Not a search box.
- A vague ask gets a vague answer.
- A specific ask gets a specific, useful one.

---

## RTFC — four things to give it

- **Role** — who should it act as?
- **Task** — what exactly are you asking for?
- **Format** — what should the output look like?
- **Context** — what does it need to know to get this right?

> Speaker notes: these four don't have to arrive in this order in a
> real prompt — the point is that all four are present *somewhere*,
> not that you recite them like a form.

---

## Bad prompt (live demo)

> *"Write me a bio."*

- Generic. Rambling. Could be about anyone.
- This is what happens with no role, task, format, or context.

---

## Good prompt (live demo, build it piece by piece)

> *"You're a [**Role:** concise, friendly bio writer]. [**Task:** write
> a 3-sentence bio introducing me and my team's project for my
> portfolio site]. [**Format:** plain text, first person, no headers].
> [**Context:** I'm a business student in a semester-long IoT/AI
> program; my team is building ___; keep it approachable, not
> corporate]."*

> Speaker notes: narrate each bracketed piece aloud as you type it —
> the point is watching the prompt get built, not just seeing the
> finished version.

---

## Debrief

- *What changed between the bad prompt and the good one?*
- *Why did that change the output?*
- The takeaway isn't the bio — it's that **specificity is what moved
  the needle**.

---

## Not every question is a writing task

- RTFC is for *"I've already decided what I want — turn it into
  output."*
- But some questions aren't settled yet: *"is this even a good idea?"*
- Handing an unsettled judgment call to RTFC just gets you a
  confident-sounding answer to the wrong problem. That's what **4D**
  is for instead.

---

## 4D — four things to work through

- **Delegation** — what do you hand to the AI, and what do you decide
  yourselves?
- **Description** — give it real context, not a generic ask.
- **Discernment** — evaluate what comes back; throw out the weak stuff.
- **Diligence** — sanity-check what's left before you commit to it.

> Speaker notes: unlike RTFC, 4D isn't a prompt template — it's a
> sequence of moves *you* make while using the AI, not something you
> say to it in one shot.

---

## Worked example: picking an IoT use case (Week 2)

1. **Delegate** the brainstorm — ask Kiro for ideas, not the final
   decision.
2. **Describe** it with real context: *"Brainstorm 5 IoT use-case ideas
   for [a regional problem you name], each with a rough sense/act
   loop"* — not *"give me IoT ideas."*
3. **Discern** — as a team, cut the generic ones, keep what's specific
   and locally grounded.
4. **Diligence** — can this actually be built with an ESP32 + a sensor
   + an app, by this team, in the time left? If not, back to step 2.

> Speaker notes: full script in `Curriculum/Week2/Day1.md` item 5 — this
> is where 4D first gets taught hands-on.

---

## Debrief

- Same instinct as the RTFC demo: a vague ask produces generic junk —
  except this time the vague thing is a *decision*, not a paragraph.
- 4D doesn't hand the decision to the AI. It structures how you use the
  AI while *you* make the call.

---

## Where this fits in the bigger picture

The course has two kinds of ambiguous-to-working-code steps
(Course-Curriculum.md §1):

1. **Judgment-heavy step** — *is this a good idea? what should the spec
   say?* → scaffolded with **4D**, which you just saw.
2. **Mechanical-generation step** — *turn a settled spec into actual
   output* → scaffolded with **RTFC**, which you saw first.

You'll use both again all semester — RTFC every time you're turning a
decision into a deliverable (today's bio and LinkedIn post, firmware-
by-prompting from Week 5 on), 4D every time the question itself is
still open (use-case picks, design tradeoffs, "is this feasible?").
