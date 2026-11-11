# Hypothesis & Success Metrics (Module 3)

## Pre-work · Hypothesis check
- **Role , who you are solving for (from M2):** Daniel — the context-blind Collection Agent.
A collection agent who takes over when the digital instalment journey stalls or a plan fails and must resolve the case by phone — without seeing what the consumer already entered online.
- **Goal , what this user is ultimately trying to achieve:** Goal: Help the consumer finish a fair, explainable plan quickly — using what they already entered online, without rediscovering the case from scratch.
- **Friction / moment of misery , the specific pain blocking their goal:** His workspace shows almost nothing of the online attempt (no entries, no plan-offer rationale), so roughly half his calls restart with the same questions — a blind handoff that burns handle time and pushes the consumer back into avoidance.

(Evidence: “Half my calls start with me asking for the same details…” — N-08; failed plan = “just a number” — N-09)
- **Current workaround , the external tool or manual process they rely on (M2):** Voice-Restart-Hack outside the product: phone/hotline + manual letter↔portal amount check + re-asking/note-taking to rebuild the case verbally from scratch.
- **Problem Hook , your one-sentence framing of the business crisis (M1):** Not setting up a sustainable payment plan leads to losing benchmark position — cashflow and client trust erode while avoidable agent rework and consumer avoidance scale.
- **Value Proposition , the outcome your initiative promised to deliver (M1):** For consumers who cannot clear a balance in one go, Riverty Collection offers a digital instalment journey that helps them agree to a plan they can actually keep — and hands them to an agent with full context when they cannot finish alone — so recovery stays responsible, self-service rises for real, and avoidable agent work falls.
Promise: sustainable digital resolution — not digital volume of agreements.

## Read the evidence in your case
- **Where does your case say people stall or leave? Does that match the friction you wrote in Module 2?:** Biggest leaks sit before the journey: Outreach→Portal (−62%) and Portal→Journey start (−78%). Inside the journey, the sharpest drop is Income document→Plan review (−22%), then Affordability→Income document (−19%). Daniel’s M2 friction (blind handoff) is not a funnel step itself — it is the consequence when mid-journey leavers call. Top-of-funnel leaks are mostly out of Daniel’s reach; Income document→Plan review is where he can help if the product surfaces the digital attempt instead of forcing a voice restart.
- **What got better or worse in the case, and does that support the workaround your persona uses?:** Over six months, agreement rate and SSR rose and 7-day agent contact fell slightly — but after Month 4, when the plan screen defaulted to 6 months first, missed payments jumped from ~15–16% to 19%. That supports Daniel’s voice-restart workaround: more fragile agreements fail, and he still must recover them by phone without seeing why the plan was offered.
- **Which user in the case is carrying the pain, and is that the person your Module 2 persona describes?:** The pain concentrates on multi-claim consumers (and, secondarily, variable/shift income and mobile): much lower agreement/SSR and ~40–43% agent contact within 7 days vs ~26% for single-claim. That is Mara’s segment, not Daniel as a row in segments.csv. It still supports the Daniel persona: those users create the call load where his blind handoff / voice-restart friction shows up.

## Step 2 · Craft your hypothesis
- **Qualitative evidence (from M2) , quote the specific friction / moment of misery for your persona:** Daniel — qualitative friction quotes (M2)

N-08: “Half my calls start with me asking for the same details they already typed online. I cannot see what they entered.”
N-09 (supporting): “When a plan fails I need to know why it was offered in the first place. Right now I just see a number.”
- **Quantitative evidence (from M3) , name the metric or data point that confirms the pain; cite the number:** agent_repeated_identity_or_affordability_checks (69.7% of contacts (1 807 / 2 592) — agent re-asks identity/affordability details already typed online)
- **Persona , role, goal, and the friction you confirmed in the reconciliation steps:** Daniel — the context-blind Collection Agent

Role: A collection agent who takes over when the digital instalment journey stalls or a plan fails and must resolve the case by phone.

Goal: Help the consumer finish a fair, explainable plan quickly — using what they already entered online, without rediscovering the case from scratch.

Friction (confirmed in reconciliation): Blind handoff / voice restart — his workspace does not show the online attempt, so he re-asks the same details.
- **Problem you are solving , one sentence describing the specific friction this initiative removes:** This initiative removes the blind handoff: when a digital instalment attempt stalls, the agent no longer has to restart discovery by phone because the product finally surfaces what the consumer already entered and why a plan was offered.
- **Strategic outcome , what behaviour change do you expect, and how does it map to retention / revenue / churn?:** Agents stop rediscovering stalled digital attempts and resolve from a shared handoff — so more consumers leave with a keepable plan, not just an agreed one. Maps to:

Retention → plans kept past 60 days (missed-payment rate down).
Revenue / cashflow → steadier recovery from lasting instalments, less write-off / chase cost.
Churn → fewer broken-plan complaints and less client/consumer drop-back into avoidance (benchmark risk).
- **Primary success metric (initiative signal) , the leading indicator that tells you the gap is closing:** Share of agent contacts where the agent repeats identity/affordability checks (agent_repeated_identity_or_affordability_checks) — baseline 69.7%.
- **Guardrail metric (product signal) , the metric that must NOT drop; it protects your existing base:** SSR resolved % of journey starters — baseline 34.7% (Month 6).
- **Decision window , how much time or data before you scale, pivot, or kill? minimum threshold to proceed?:** 8 weeks after handoff goes live — ~4 weeks to read the leading signal on agent contacts, then enough runway for the first 60-day keep cohort to mature.

Minimum to proceed (scale):

Repeated identity/affordability checks: 69.7% → ≤55% (clear gap closing)
Guardrail: SSR resolved ≥34.7% (no drop)
Directional lagging: missed-payment 60d not worse than 19% on the first measurable cohort
Pivot if repeated checks barely move (<5 pp) but AHT/SSR wobble. Kill if SSR falls or miss rate rises while the leading metric stays flat.
- **Draft your full hypothesis sentence , one to three sentences; quote the metric, name the persona, name the outcome:** Based on N-08 (“Half my calls start with me asking for the same details…”) and M3 evidence that 69.7% of agent contacts repeat identity/affordability checks—fed by mid-journey stalls such as Income document→Plan review (−22.1%)—I believe that solving the blind handoff for Daniel, the context-blind Collection Agent, will result in faster, keepable resolution instead of voice restart, as measured by a drop in repeated identity/affordability checks from 69.7% to ≤55% (~15 pp). I will protect SSR resolved % of journey starters (baseline 34.7%) and will make a go/no-go decision after 8 weeks.
