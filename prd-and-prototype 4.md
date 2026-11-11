# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** B4 - Handoff summary for the agent when a consumer calls, Direct test of the hypothesis; attacks 69.7% repeated checks.
- **My finalized Must-Haves (after overriding the AI):** MUST HAVE (Sprint 1 — without these the hypothesis test fails)
Case lookup at call intake — Agent opens the case and sees whether a digital instalment attempt exists (including a clear “no attempt” state).
Identity & affordability fields, read-only — Exact online inputs that are re-asked today (N-08 / primary metric).
Journey status — Last reached step + timestamp (e.g. stuck at income doc / plan review / failed agreement).
Plan-offer rationale — Offered plan plus a short why (not just “a number” — N-09).
Data freshness — Visible timestamp / “as of …” so Daniel trusts the summary.
Empty / partial states — Clear messaging when the attempt is missing or incomplete (no crash, no guessing).
Instrumentation — Event/flag that the summary was shown/used, plus tracking of agent_repeated_identity_or_affordability_checks (and SSR guardrail).
Litmus test: Remove any one of these → blind restart remains, or the hypothesis is not measurable.
- **What I demoted from Must → Should/Won’t, and why:** _(not filled in)_

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** Instrumentation of no_reask vs reask_required (FR-7) — including the target 69.7% → ≤55%.

A vague brief only says “show the agent online context.” Your PRD makes explicit that without an agent decision and a measurable proxy, the hypothesis isn’t testable — and that missing plan rationale must show as Unavailable, never invented.

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** Nothing
- **My prototype: save Claude's HTML as prototype.html in 04-roadmap/, open it in your browser, and add a screenshot:** OK
