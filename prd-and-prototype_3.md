# B4 - Handoff summary for the agent when a consumer calls, Direct test of the hypothesis; attacks 69.7% repeated checks., Simplified PRD (Riverty BU Collection, A Fair Way Forward)

**Scenario:** Riverty BU Collection, A Fair Way Forward

**Author:** Me · **Status:** Draft · **Target:** High-Fidelity Prototype · **Persona:** Daniel — the context-blind Collection Agent

## 1. The Big Picture
- **Vision:** Give Daniel a one-screen, read-only handoff of Mara’s digital instalment attempt so every inbound call starts where she stopped — not at zero.
- **Press release:** Today, when a consumer stalls mid-journey or a plan fails, Daniel opens a nearly empty agent screen. He rebuilds identity and affordability by phone, burns ~11–13 minutes of handle time, and pushes the consumer back into avoidance. Roughly 69.7% of contacts repeat checks the portal already captured.

With the Agent Handoff Summary, Daniel opens the case and immediately sees what was entered online, where the journey stopped, and why a plan was offered. He coaches a keepable outcome instead of rediscovering the case. Riverty Collection moves from digital volume of agreements to sustainable digital resolution — fewer blind restarts, steadier recovery, and a cleaner path to dropping repeated checks from 69.7% to ≤55% within the 8-week decision window, without harming SSR (≥34.7%).
- **Success metric:** agent_repeated_identity_or_affordability_checks ≤55% (~15 pp drop)
- **Guardrail:** SSR resolved % of journey starters must not drop below 34.7%

## 2. The Details
### User stories
- US-1 · See the digital attempt at intake
- As Daniel, the collection agent, I want a handoff summary of the consumer’s digital instalment attempt when I open the inbound call case, so that I start where they stopped instead of voice-restarting identity and affordability.
- Acceptance criteria
- Given a case with a digital attempt, when Daniel opens it, then identity fields, affordability fields, last journey step, and timestamp are visible without extra clicks beyond opening the case.
- Given a case with no digital attempt, when Daniel opens it, then a clear “No digital instalment attempt” state is shown (not a blank panel).
- Summary is read-only; Daniel cannot edit consumer inputs on this screen.
- US-2 · Understand why that plan was offered
- As Daniel, I want the offered plan and a short rationale on the same summary, so that a failed or stalled plan is explainable — not “just a number” (N-09).
- Acceptance criteria
- When a plan was offered or agreed, the summary shows plan length, monthly amount (or equivalent sample fields), and a one-line rationale.
- When no plan was offered yet, the summary shows “No plan offered” plus the last reached step.
- Rationale text is sourced from the attempt record (prototype fixture), never invented on the fly.
- US-3 · Trust freshness and measure the hypnosis test
- As Daniel (and as PM), I want a visible “as of” timestamp and usage/re-ask instrumentation, so that agents trust the data and we can prove movement on 69.7% → ≤55%.
- Acceptance criteria
- Summary always shows as_of datetime.
- Prototype logs (or visibly toggles) summary_shown = true when the handoff panel renders.
- Prototype exposes a measurable proxy for repeated checks (e.g. agent marks “Used online data — no re-ask” vs “Had to re-ask”), tied to the contact.
### Screens to build
- Screen 1 — Entry point: Agent inbound call / case list
- Purpose: Daniel picks the consumer who just called.
- UI elements
- Header: “Collection Agent Workspace · Daniel”
- Inbound queue / case list (3–5 sample rows): consumer name, claim ref, channel = Phone, badge “Digital attempt” | “No attempt”
- Search/filter by claim ref (client-side only)
- Primary action per row: Open case
- Footer note: Primary metric reminder strip — “Target: cut repeated identity/affordability checks 69.7% → ≤55%”
- Screen 2 — Feature core: Handoff Summary (case detail)
- Purpose: Replace blind restart with shared digital context.
- UI elements
- Case header: consumer name, claim ref, call timer (static/demo)
- Handoff Summary panel (core):
- Data freshness: As of: [timestamp] + status chip Fresh / Stale (>24h) / Missing
- Journey status: last step + step timestamp (e.g. Income document · stalled)
- Identity block (read-only): name, DOB/ref, contact channel used online
- Affordability block (read-only): income band / declared ability-to-pay fields from fixtures
- Plan offer block: offered plan + Why offered one-liner; or “No plan offered”
- Stall/blocker hint (SHOULD, if capacity): e.g. Upload failed on mobile
- Empty/partial banners for missing attempt / incomplete affordability
- Actions: Start where they stopped (scrolls/highlights summary), Mark: no re-ask / Mark: had to re-ask (eval proxy)
- Explicit non-actions (disabled/ghost): Create plan, Edit inputs, Open chat assistant
- Screen 3 — Success / confirmation: Contexted intake complete
- Purpose: Confirm Daniel is oriented and the hypnosis signal is captured.
- UI elements
- Confirmation state: “Handoff loaded — continue from digital attempt”
- Checklist of what was reused: Identity ✓ · Affordability ✓ · Plan rationale ✓ (or N/A)
- Agent decision captured: no_reask | reask_required with reason dropdown if re-ask
- Success metric micro-copy: “This contact will count against the 69.7% baseline”
- CTA: Return to queue · Secondary: Open next case
- Guardrail reminder: “Do not push fragile agree-only plans — protect SSR ≥34.7%”
### Functional requirements
- FR-1 Case lookup: Opening a case always resolves one of: attempt_present | attempt_absent within the prototype dataset (100% of demo cases classified).
- FR-2 Identity & affordability read-only: When attempt_present, 100% of fixture identity + affordability fields render; no edit controls on those fields.
- FR-3 Journey status: Display last_step + last_step_at whenever an attempt exists; if missing step data, show partial state (not invent a step).
- FR-4 Plan rationale: If plan_offered = true, show plan summary + rationale string from data; if false, show “No plan offered” — never fabricate rationale.
- FR-5 Freshness: Every summary render shows as_of; if older than 24h (demo rule), chip = Stale.
- FR-6 Empty/partial states: attempt_absent and incomplete affordability each have dedicated UI copy; blank white space is a defect.
- FR-7 Instrumentation: Every summary view sets summary_shown=true; agent must select no_reask or reask_required before confirmation completes.
- FR-8 Scope lock: No write-path controls for creating/editing instalment plans on these three screens.
### Smart behaviors (Situation → Outcome)
- Situation (If)	Outcome (Then)
- Case has digital attempt with complete identity + affordability	Show full Handoff Summary; enable Mark: no re-ask as default recommendation
- Case has attempt but affordability incomplete	Show partial banner “Affordability incomplete online — ask only missing fields”; pre-check re-ask reason = partial_affordability
- Case has no digital attempt	Hide plan/identity blocks; show “No digital instalment attempt — standard discovery”; force reask_required path
- Plan offered + rationale present	Show plan + why; talking-point: “Explain keepability from this rationale”
- Plan offered but rationale field empty	Show plan amounts only + safety banner “Rationale unavailable — do not invent why”; block fake rationale text
- Last step = income document / upload fail	Show stall hint “Likely blocker: income document”; do not claim upload is fixed
- as_of older than 24h	Stale chip + copy “Confirm critical fields verbally if consumer says data changed”
- Agent selects no_reask	Confirmation screen counts contact as non-repeat (metric-positive)
- Agent selects reask_required	Confirmation stores reason; counts as repeat (baseline-like)
- Agent tries Create plan / Edit inputs / Chat	Control disabled; tooltip “Out of scope for B4 V1 — WON'T HAVE”
### Technical constraints
- One HTML file with plain JavaScript (and CSS in-file or same file) — no framework build step.
- No login / auth.
- No external APIs, no network calls, no LLM endpoints — all cases from in-file fixtures/JSON.
- No hallucination path: rationale and field values only from fixtures; if missing → explicit unavailable state (see Smart Behaviors).
- Desktop agent-workspace layout; three screens navigable in-page (no router library required).
- Read-only handoff; no persistence beyond localStorage optional for demo marks (not required).

## 3. The Logistics
### Features out
- Write-path: create/edit instalment plan from the summary
- Consumer UI or portal chat assistant (B8 — cut)
- Multi-claim one-plan (B1)
- Affordability-engine rebuild (B3)
- Mobile photo upload / skip threshold (B5)
- Payday-aligned due date (B6)
- “Shortest plan first” default (B7 — cut; already hurt miss rate 15.6%→19%)
- New telephony / IVR integration
- Full case dump / full communication history dump
### Edge cases & safety guard
- Unhappy path	Product response
- No digital attempt	Explicit empty state; standard discovery; counts as re-ask
- Incomplete affordability	Partial summary; ask only gaps
- Failed agreement, plan = number only	Show amounts + “Rationale unavailable”; forbid invented why
- Stale data (>24h)	Stale chip; verbal confirm if consumer disputes
- Conflicting consumer statement vs summary	Agent re-ask allowed; mark reask_required + reason consumer_dispute
- Safety / hallucination guard	UI never auto-generates plan rationale, income, or identity; missing fields render Unavailable / Not provided online. Any “AI suggest why” control is out of scope and must not appear in the prototype.
### Decision log
- Read-only handoff only in Sprint 1 / prototype — Attacking 69.7% requires surfacing typed identity/affordability, not building a new resolution engine. Write-path would inflate effort past the scored E=2 Quick Win and blur the hypothesis test.
- Instrument re-ask vs no-reask on confirmation, not AHT alone — Primary success signal is repeated identity/affordability checks (69.7%→≤55%). AHT is directional; SSR ≥34.7% is the hard guardrail. No feature work that raises agree-volume while risking keepability (explicitly excludes B7/B8).
### Evals
- Eval	Target	How measured in prototype / pilot
- 1. Context accuracy	≥95% of rendered summary fields match fixture source (zero invented rationale/identity/affordability values)	Fixture equality checks + manual script walkthrough of all demo cases
- 2. Time-on-task to oriented intake	≤20 seconds from Open case to confirmation that identity+affordability+status are understood (vs multi-minute verbal rebuild)	Stopwatch on prototype task: open flagged “Digital attempt” case → mark no_reask
- 3. Safety triggers	0 prototype paths that fabricate rationale; 100% of missing-rationale cases show Unavailable + disable inventing	QA script: open “plan without rationale” fixture; assert banner + no generated text

## MoSCoW scope
- **Must:** Case lookup at call intake; Identity & affordability fields, read-only; Journey status — Last reached step + timestamp; Plan-offer rationale; Data freshness; Empty / partial states; Instrumentation
- **Should:** Stall / blocker hint; Short talking points; Deep link into the existing case view; Failed-plan context
- **Could:** Communication history; Inline correction of online data by the agent; Confidence / completeness score for the attempt; Multi-claim overview in the handoff; Autopopulate call notes from the summary; Live sync while Mara is still in the portal
- **Won't (now):** No create/edit instalment plan from the summary; No consumer UI / chat assistan; No multi-claim one-plan; No mobile upload fix; No “shortest plan first"; No new telephony / IVR integration; No full case dump

