# Experimentation Plan (Module 5)

## Get your documents ready
- **From M3, your hypothesis sentence:** Based on N-08 (“Half my calls start with me asking for the same details…”) and M3 evidence that 69.7% of agent contacts repeat identity/affordability checks—fed by mid-journey stalls such as Income document→Plan review (−22.1%)—I believe that solving the blind handoff for Daniel, the context-blind Collection Agent, will result in faster, keepable resolution instead of voice restart, as measured by a drop in repeated identity/affordability checks from 69.7% to ≤55% (~15 pp). I will protect SSR resolved % of journey starters (baseline 34.7%) and will make a go/no-go decision after 8 weeks.
- **From M3, your primary success metric & guardrail metric:** agent_repeated_identity_or_affordability_checks — Baseline 69.7% (1 807 / 2 592)
- **From M4, the feature you scoped in your PRD this is what you're testing:** B4 — Agent Handoff Summary (read-only handoff of the digital instalment attempt for Daniel).

## Define your experiment parameters
- **Feature under test pull from your M4 PRD:** B4 — Agent Handoff Summary (read-only handoff of the digital instalment attempt for Daniel).
- **Persona pull your M2 persona:** Daniel
- **Expected outcome the behaviour change you expect, from your M3 hypothesis:** Read-only one-screen handoff for Daniel: identity, affordability, last journey step, plan + rationale, freshness — so inbound calls start where the consumer stopped, not at zero.
- **Primary success metric the one number that defines success, from M3:** agent_repeated_identity_or_affordability_checks
- **Baseline rate today's rate of your primary metric, from your M3 data:** 69.7%
- **Guardrail metric & boundary what must not break, and how far it can move before you investigate:** SSR resolved % of journey starters — Baseline 34.7%
- **Minimum Detectable Effect (MDE) the smallest improvement worth shipping, your floor:** ≥5 pp Drop bei agent_repeated_identity_or_affordability_checks
(69.7% → ≤64.7%)
- **Sample size per arm use the calculator in the builder, baseline + MDE:** 1260
- **Traffic split & test duration 50/50 standard · cover ≥ 2 weekly cycles:** 50/50, 2 weeks (based on feature flag)
- **Significance threshold p < 0.05 is standard, explain any deviation:** < 0.05

## Define your control and variant
- **Control (A) the current experience, reference your M2 moment of misery and M3 funnel/workflow data:** Agent workspace without handoff summary
- **Variant (B) your single change, copy the relevant screens & functional requirements from your M4 PRD:** Agent workspace with the read-only Agent Handoff Summary (PRD Screens 1–3): digital attempt context at intake — identity, affordability, last step, plan + rationale, freshness — plus no-reask / re-ask mark.
- **Isolation check, what has NOT changed? list everything identical between arms (app version, eligibility rules, notifications, onboarding). If something changed inadvertently, your test is compromised.:** Area	Unchanged
App / build	Same agent-workspace version; same fixtures/cases; no new APIs, auth, telephony/IVR
Eligibility	Same inbound phone contacts / case queue rules; same who gets a case
Consumer journey	Portal/instalment flow unchanged (no B5 upload, B6 payday, B7 shortest-plan, B8 chat)
Plan engine	Same offer logic / affordability engine (no B3 rebuild); no create/edit plan from agent UI
Write-path	No plan create/edit, no input editing on either arm
Notifications	Same agent/consumer notifications (none added for this test)
Onboarding / training	Same agent process except Variant may see summary; no new coaching scripts that change resolution policy
Routing / queue	Same case list, search, Open case; same channel = Phone
Multi-claim	B1 one-plan-for-several-claims not in either arm
Case content dump	No full case/comms dump added
Guardrail policy	Same keepability/SSR stance (no push for fragile agree-only volume)
Metric definition	Same primary metric & SSR guardrail measurement rules
LLM / AI	No hallucinated rationale / “AI suggest why” on either arm

## Formalize your hypothesis & shipping criteria
- **Your hypothesis (filled in):** I believe that B4 — Agent Handoff Summary (read-only handoff of the digital instalment attempt) for Daniel will result in Read-only one-screen handoff for Daniel: identity, affordability, last journey step, plan + rationale, freshness — so inbound calls start where the consumer stopped, not at zero., as measured by a + 5 pts change in agent_repeated_identity_or_affordability_checks within 14. We will protect SSR resolved % of journey starters throughout the test.
- **Your shipping criteria (filled in):** We will SHIP if agent_repeated_identity_or_affordability_checks improves by ≥ + 5 pts at < 0.05 and SSR resolved % of journey starters does not reach 34.7% after 14. We will ITERATE if direction is positive but lift is below MDE. We will KILL if the primary metric shows no improvement or moves negatively. The read date is fixed at the end of 14, no results reviewed before then.
- **Hardest parameter to define, and did it change your hypothesis? quick debrief:** Ambition could be higher (< -5 pp e.g. -15 pp).
