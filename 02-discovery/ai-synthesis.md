# AI Synthesis, Product Health & Insights Summary (Module 2)

## Responses
- **Assumption to validate #1:** Not intuitive to use
- **Assumption to validate #2:** root causes of breaking processes are wide spreaded
- **Assumption to validate #3:** no clear log entry/ kpi to follow the impulse
- **Moment of misery / red flag #1 (e.g., “user gave up after 3 tries”):** Consumers don’t know which income figure is meant, and fear typing the wrong number will be used against them.
- **Moment of misery / red flag #2:** Consumers only see one claim at a time and don’t know if paying one stops letters about the other.
- **Moment of misery / red flag #3:** The online amount doesn’t match the letter - the journey dies before agreement.
- **Product Health & Insights Summary (Claude's output):** # Product Health & Insights Summary  
**Digital Instalment Journey · Practice evidence synthesis**  
_Sample data, illustrative — not Riverty research._

## Executive Summary
The journey can create agreements, but product health is uneven: several technical defects actively break completion and post-agreement behaviour, while deeper experience gaps leave consumers unsure what they are signing and whether they can keep it. Trust and clarity failures—especially around income, balance amounts, and missed-payment consequences—convert intended self-serve into hesitation, abandonment, or fragile plans. The same blind spots then land on agents and clients as repeated explanation work and visible broken-plan noise, so instability and UX friction reinforce each other rather than staying separate.

## Thematic Synthesis

### Technical Stability
Core steps that should be deterministic—document capture, form state, and reminder timing—are unreliable enough to erase progress or arrive too late to help. Failures concentrate on mobile and on the path after a plan is chosen, so “technical” defects show up as drop-off and early missed payments rather than as isolated engineering tickets.

- **Critical — Mobile income document upload fails / times out**, leaving large volumes of journeys with a requested document that never arrives.
- **High — Plan-review “Back” clears affordability answers**, forcing re-entry and raising abandonment risk mid-commit.
- **High — Pre-first-instalment reminders sometimes send after the due date**, undermining the keep-the-plan loop.
- **Minor Technical Debt —** residual UI/state edge cases that degrade polish but are secondary to the failures above.

### Onboarding / UX (journey design)
The flow is structured around single-claim, option-picking behaviour that does not match how many consumers experience debt. Choice architecture and claim visibility push people toward plans that look “correct” rather than affordable, or toward stopping because they cannot see the full picture.

- **Critical — No multi-claim view or combined plan**, so consumers cannot resolve linked obligations in one journey and remain unsure whether paying one stops pressure on another.
- **High — Plan options steer toward short / high monthly amounts** without enough affordability guidance, contributing to missed second payments.
- **Medium — Chat confirms plans quickly** but does not replace structured clarity on what happens next if payment fails.

### Trust & Clarity
Consumers hesitate not only because of bugs, but because the product asks for sensitive data and binding commitments without explaining purpose, data use, or downstream consequences. Amount mismatches versus the letter—especially on purchased portfolios—create a hard stop: people refuse to agree until a human reconciles the numbers. Compliance expectations amplify this: decisions must be explainable to both consumer and agent.

- **Critical — Portal balance differs from the letter** at material volume (notably purchased portfolios), blocking digital commitment.
- **High — Income request is ambiguous and feels risky** (which period; fear of “wrong” figures being used against them), with insufficient in-product explanation of why income is asked and how long it is kept.
- **High — Consequences of late / missed payment are not shown** at confirm time (including chat), so agreements form without shared understanding of downside.
- **Medium — Preference to call for human reassurance on total cost / fees**, signalling low confidence that the digital path is safe to finish alone.

### Support Load & Handoff
When digital stalls or agreements fail, the support layer cannot see the consumer’s online inputs or the rationale for the offered plan. Agents restart discovery from scratch; clients see complaint and broken-plan signals in reporting. Support load is therefore a product-health symptom of missing context and explainability, not only of call volume.

- **Critical — Agent workspace lacks consumer online entries and plan-offer rationale**, so a large share of contacts begins with re-asking data already typed.
- **High — Failed plans are not diagnostically transparent** (“just a number”), limiting recovery coaching and consistent promises across channels.
- **High — Broken-plan spikes surface in client reporting**, tying consumer journey quality directly to account-level complaint / recovery optics.
- **Medium — Portfolio data unevenness** (e.g. weak contact history on some acquired books) raises the chance that digital-first paths fail and fall back to costly assisted recovery.
- **Did the AI catch the specific moment of misery / pain point you found in Step 1?:** Yes
- **Did it smooth over a critical frustration into a generic bullet point?:** No
- **Did the AI try to suggest features or a roadmap despite the constraints?:** No
- **Logic leak / hallucination #1 (e.g., “AI suggested a new search bar feature, roadmap leak”):** _(not filled in)_
- **Logic leak / hallucination #2:** _(not filled in)_
