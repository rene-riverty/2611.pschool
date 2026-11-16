# A/B Experiment Brief, Riverty BU Collection, A Fair Way Forward

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | B4 — Agent Handoff Summary (read-only handoff of the digital instalment attempt for Daniel). |
| Persona | Daniel |
| Expected outcome | Read-only one-screen handoff for Daniel: identity, affordability, last journey step, plan + rationale, freshness — so inbound calls start where the consumer stopped, not at zero. |
| Primary success metric | agent_repeated_identity_or_affordability_checks |
| Baseline rate | 69.7% |
| Guardrail metric | SSR resolved % of journey starters |
| Guardrail boundary | 34.7% |
| Second guardrail | · |
| Minimum Detectable Effect | - 5 pts |
| Sample size per arm | 1.260 |
| Traffic split | 50/50 |
| Test duration | 14 |
| Significance threshold | < 0.05 |

## Control vs. Variant
- **Control (A):** Agent workspace without handoff summary
- **Variant (B):** Agent workspace with the read-only Agent Handoff Summary (PRD Screens 1–3): digital attempt context at intake — identity, affordability, last step, plan + rationale, freshness — plus no-reask / re-ask mark.
- **Held constant (isolation check):** Area	Unchanged
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

## Hypothesis
> I believe that B4 — Agent Handoff Summary (read-only handoff of the digital instalment attempt for Daniel). for Daniel will result in Read-only one-screen handoff for Daniel: identity, affordability, last journey step, plan + rationale, freshness — so inbound calls start where the consumer stopped, not at zero., as measured by a - 5 pts change in agent_repeated_identity_or_affordability_checks within 14. We will protect SSR resolved % of journey starters throughout the test.

## Shipping criteria
> We will **ship** if agent_repeated_identity_or_affordability_checks improves by ≥ - 5 pts at < 0.05 and SSR resolved % of journey starters does not reach 34.7% after 14.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 14, no results reviewed before this date.
