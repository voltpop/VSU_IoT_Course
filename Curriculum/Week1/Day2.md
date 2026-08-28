---
title: Week 1, Day 2 — Course Foundations (Thursday)
week: 1
day: 2
date: Jan 21 (Thu)
duration: 3 hours (180 min): 100 min fixed content, 80 min buffer
status: draft
see_also: ./README.md (shared framing, deliverables, open items); ./Day1.md
---

# Week 1, Day 2 (Thu) — Prompt Engineering & First Public Post

*Week 1's one actual academic content block lives here (moved from the
original combined plan's Day 1 item 6 — see [Day 1](./Day1.md) and
README Open Item 5 for why). This day also carries the built-in slack
the week needs: 100 minutes of fixed content in a 180-minute class.*

**1. Recap + troubleshooting** *(~20 min)*
Don't just ask "anything broken?" — walk the room checking the specific
failure points Day 1 is most likely to leave behind:
- GitHub email not yet verified.
- Kiro authorized via OAuth in the browser, but the CLI never
  authenticated (`kiro-cli login` not actually run).
- Repo cloned but no push access (invite never accepted), or never
  cloned at all.
- GitHub Pages site not live yet (first publish can lag a few minutes,
  easy to mistake for broken).

Expect this to run long for some groups; budget for it rather than
rushing ahead, and treat item 2 below as staggered/interruptible rather
than needing the whole room in lockstep.

**2. Prompt engineering & context management** *(~40 min)*
Register shift here: from checklist mode to actual teaching. Core idea:
the AI is a tool you *direct* with a clear ask, not a search box —
previewing RTFC (Role, Task, Format, Context), formally named in Week
5.

Guided exercise, demo first then per-group:
1. **Bad-prompt example** (show live): *"write me a bio."* — call out
   how generic/rambling the result is, and that this is what happens
   with no role, task, format, or context given.
2. **Good-prompt example**, narrating each RTFC piece aloud as you
   build it: *"You're a [Role: concise, friendly bio writer]. [Task:
   write a 3-sentence bio introducing me and my team's project for my
   portfolio site]. [Format: plain text, first person, no headers].
   [Context: I'm a business student in a semester-long IoT/AI program;
   my team is building ___; keep it approachable, not corporate]."*
3. Each group runs their own version through Kiro and drops the result
   into the portfolio bio placeholder they left empty on Day 1.
4. **Debrief question:** *"what changed between the bad prompt and the
   good one, and why did that change the output?"* — the point isn't
   the bio itself, it's noticing that specificity is what moved the
   needle. Keep this lesson fresh for item 3 below — the same pattern
   gets reused immediately.

**3. First public LinkedIn post** *(~40 min)*
- Each student publishes a short LinkedIn post introducing themselves
  and the program — the semester's first public deliverable.
- Suggested structure (a talking point, not a rigid template): who you
  are, one line naming the program, one line on what you're excited to
  build. Check `Press-Kit-Content.md` for whether the program has an
  established LinkedIn presence/hashtag to tag.
- Reuse item 2's RTFC pattern with Kiro to draft a first pass, then have
  the student personalize it before posting — the same skill applied
  twice in one sitting, immediately after learning it.
- **No-PII reminder is about this KB, not personal posts** — students
  posting publicly about themselves is expected and fine; the rule
  (`AGENTS.md`) only bars putting personal/student info back into the
  shared class notes-KB repo.
- Each group logs their post URL(s) in their own notes-KB entry — the
  day's second hands-on git commit.
- Discuss, briefly, why this matters for the portfolio/Career Day
  throughline (Course-Curriculum.md §8) — not just an assignment for
  its own sake.

**4. Buffer / open work time** *(~80 min)*
Not idle time — an instructor circulation checklist. Confirm every
group has: (a) a working repo clone, (b) Kiro authenticated end to end,
(c) a live (even if bare) group portfolio page with its bio filled in,
(d) a published LinkedIn post. This is also where anything that
overran from Day 1 (see Day 1's end note — it has zero slack of its
own) actually gets absorbed, and the natural moment to *note* (not
necessarily fix live) anything that surfaces as evidence bearing on the
[README](./README.md)'s Open Items — e.g., a group's snag that's really
a sign one of the pending decisions needs to go a particular way.
