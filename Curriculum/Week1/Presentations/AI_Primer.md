# AI Primer — Meet Kiro

*Source: [`../Day1.md`](../Day1.md) item 2 (Kiro portion). ~part of the
40-min account-creation block, presented as its own short deck after
GitHub Primer. Note: this is orientation only — the actual
prompt-engineering lesson (RTFC) is Day 2, not here.*

---

## Kiro is our AI tool this semester

- Not ChatGPT, not Claude, not Codex, not Gemini.
- One tool, used all semester (Course-Curriculum.md §7 item #15).

---

## Sign in with GitHub

- On Kiro's sign-in screen: **Continue with GitHub**.
- Authenticate in the browser, authorize the Kiro app.
- Same GitHub account from the GitHub Primer deck — no second
  credential to manage.

---

## Install the tooling

- Kiro CLI:
  `curl -fsSL https://cli.kiro.dev/install | bash` (macOS/Linux)
  or `irm 'https://cli.kiro.dev/install.ps1' | iex` (Windows).
  Confirm with `kiro-cli doctor`; `kiro-cli login` if not authenticated.
- Kiro Crew: `kirocrew setup` → `kirocrew doctor` → `kirocrew gateway`.

> Speaker notes: Crew's device-code sign-in flow hasn't been verified
> hands-on to confirm it reuses the same GitHub session — check this
> live before Day 1, don't assume it just works (Day1.md item 2).

---

## Orientation

- Open Kiro, point out the chat pane.
- Confirm it can see your team's repo.
- One line to land: *"this is the tool you'll talk to all semester."*

---

## What's next

- Today was just getting Kiro installed and signed in.
- **Day 2** is when we actually learn to direct it well — that's where
  prompt engineering and the RTFC pattern come in.
