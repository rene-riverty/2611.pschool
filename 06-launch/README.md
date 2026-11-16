# Great support for human supporter

> For Collection Agents like Daniel, B4 surfaces a read-only handoff of the consumer’s digital instalment attempt at call-start — so you continue where they stopped instead of re-asking identity and affordability.

**René (Cohort 2 2026 Nov)** · https://github.com/rene-riverty/2611.pschool

Prototype: https://github.com/rene-riverty/2611.pschool/blob/main/04-roadmap/prototype-b4-handoff-summary.html

---

## Final Project Deliverables

### Slide 5 · Strategy
- **Problem:** ## Responses
- **Chosen path, which Riverty business-unit case are you using?:** Collection - instalment plan
- **Strategic crisis, based on the brief, if the company does nothing for 12 months, what happens to its market position?:** less cashflow than possible - loss of benchmark position or customer satisfaction
- **Moment of misery, what is the user likely doing outside the product (Google, spreadsheets, a competitor) because your tool isn’t serving them?:** Waiting/ do nothing instead of come into action
- **Problem hook, summarize the business risk and user pain into one urgent sentence.:** Not setting up a sustainable payment plan leads to loosing benchmark position.
- **Value proposition, based on the initiative in your assigned Riverty case, what is the new value and why is it urgent to launch now?:** For consumers like Mara who cannot clear a balance in one go, Riverty Collection offers a digital instalment journey that helps them agree to a plan they can actually keep — and hands them to an agent with full context when they cannot finish alone — so recovery stays responsible, self-service rises for real, and avoidable agent work falls. The new product promise is: sustainable digital resolution - not digital volume of agreements.

## Cold-read your own hook
- **Is the business risk high enough to justify a new initiative, a high-stakes threat, or a minor inconvenience?:** high-priority operating risk inside a strategic program
- **Is the moment of misery a systemic problem or just an edge case?:** Systemic — not an edge case. In this initiative, the “moment of misery” is avoidance: delay, close the tab, wait for the next letter/reminder, or call later instead of finishing a plan.
- **Does the value proposition actually remove the obstacle you identified, or is it a generic feature?:** Primary VP (consumer): Must break Mara’s silence — the freeze where waiting feels safer than agreeing. If she never acts, there is no plan, no SSR win that sticks, and Daniel only sees her later in a worse state.
Secondary / system VP (agent): Must fix Daniel’s pain — context-rich handoff — because when she does get stuck or calls, a blind restart pushes her back into avoidance and burns cost.
- **Value proposition:** Collection Agents who take over stalled or failed digital instalment attempts get a read-only, one-screen handoff (identity, affordability, last step, plan + why, freshness) at case-open — so every inbound call starts with shared context, not a voice restart — cutting repeated identity/affordability checks 69.7% → ≤55% without harming SSR ≥34.7%.
- **Hypothesis:** ## Pre-work · Hypothesis check
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

### Slide 6 · Research
- **Competitive analysis:** ## Responses
- **Role, who are you solving for? (the specific user segment or profile):** Daniel - the context-blind Collection Agent
A collection agent who takes over when the digital journey stalls or a plan fails and must resolve the case by phone.
- **Goal, what is this user ultimately trying to achieve?:** Help the consumer finish a fair, explainable plan quickly - using what they already entered online, without rediscovering the case from scratch.
- **Friction, the main barrier (moment of misery) stopping them from succeeding:** His workspace shows almost nothing of the online attempt (no entries, no plan-offer rationale), so half his calls restart with the same questions — a blind handoff that pushes Mara back into avoidance and burns handle time.
- **External tools, the outside platforms or tools the user is forced to use:** tools outside the digital product (phone, letter... aka Voice-Restart-Hack).
- **The process, the 3 to 5 manual steps the user takes to get the job done:** 1. The consumer stalls digitally or calls (income uncertainty, multi-claim, amount mismatch, upload fail…).
2. Daniel opens the case — sees no online history and no rationale for the offered plan.
3. He re-asks the same details Mara already typed (“Half my calls start with me asking for the same details…” — N-08).
4. On failed plans he sees “just a number” and must guess/ask why that plan was offered (N-09).
5. He rebuilds a plan / explanation verbally — often without the digital context Mara already had.
- **Core frustration, the exact moment the process feels most “broken”:** Double work: the data already exists — the product doesn’t surface it → AHT rises (~11–13 min contacts in the sample). 
Trust break: Mara must retell her story → frustration → more likely to wait / do nothing again.
In short: the hack scales avoidance instead of recovery.
- **The evidence, a specific quote or behavior from the research that proves this:** “Half my calls start with me asking for the same details…” — N-08
- **Your journey map file name (e.g. journey-map.html):** daniel-future-state-journey.md
- **Journey map:** #	Moment	Who	What happens	B4 job	Risk if weak
1	Stall / fail online	Mara	Journey stalls or plan fails; she calls	Creates attempt_present	No attempt → empty state, standard discovery
2	Case open (GTM activation)	Daniel	Opens inbound case; sees badge + Handoff Summary	Contexted intake — start where she stopped	Blind restart; summary_shown miss
3	Trust check	Daniel	Reads as of / Fresh·Stale·Missing	Decide reuse vs confirm	Ignores panel → re-ask habit
4	Explain the offer	Daniel	Reads plan + why offered (or Unavailable)	Fix N-09 “just a number”	Invents rationale (compliance fail)
5	Orient & mark	Daniel	Continues from last step; marks no_reask / reask_required	Engagement proof (≤20s)	Shown but flat no_reask
6	Keepable resolve	Daniel + Mara	Coach keepable plan (no fragile agree-push)	Protect SSR ≥34.7%	Volume over keepability
7	Close + learn	Daniel / PM·TL	Contact counts to re-ask metric; weekly strip / coaching	Habit → 69.7%→≤55%	Silence after launch

### Slide 7 · Blueprint
- **Roadmap:** # Feature Roadmap, Module 4 · BU Collection

**Scenario:** Riverty BU Collection, A Fair Way Forward

**Team:** [your assumed team size]

## Strategic anchors
- **Persona:** Daniel — the context-blind Collection Agent
- **Primary metric:** agent_repeated_identity_or_affordability_checks - baseline 69.7%
- **Moment of misery:** Blind handoff / voice restart — his workspace does not show the online attempt, so he re-asks the same details.
- **Guardrail:** SSR resolved % of journey starters — baseline 34.7% (Month 6)

## Scoring
| Feature | Value | Effort | Quadrant | Decision | Rationale |
| B1 B4 - Handoff summary for the agent when a consumer calls | 5 | 2 | Quick Win | Now | Direct test of the hypothesis; attacks 69.7% repeated checks. |
| B2 B2 - Plain explainer for why income is asked | 4 | 1 | Quick Win | Now | Cheap; cuts Mara freeze + top call reason before Daniel is needed. |
| B3 B5 - Mobile photo upload / skip under threshold | 4 | 3 | Major Project | Next | Hits largest in-journey leak (Income doc→Plan −22%). |
| B4 B1 - One plan for several open claims | 5 | 4 | Major Project | Next | Multi-claim = 40–43% agent contact; biggest segment pain, heavier build. |
| B5 B3 - Affordability check before plan options | 4 | 3 | Major Project | Later | Supports keepability after handoff works; not the first gap to close. |
| B6 B6 - Pick a payment date that matches pay day | 3 | 2 | Fill-In | Later | Nice keepability tweak; weak link to Daniel’s blind-handoff metric. |
| B7 B8 - Chat assistant on every portal page | 2 | 4 | Time Sinker | Cut | Raises agree but already lifts miss risk; volume, not sustainable handoff. |
| B8 B7 - Show the shortest plan first to raise recovery | 1 | 1 | Fill-In | Cut | Month-4 default already hurt keepability (miss 15.6%→19%); anti-hypothesis. |

### NOW, this sprint
- **B1 B4 - Handoff summary for the agent when a consumer calls**, Direct test of the hypothesis; attacks 69.7% repeated checks.
- **B2 B2 - Plain explainer for why income is asked**, Cheap; cuts Mara freeze + top call reason before Daniel is needed.

### NEXT, the following sprints
- **B3 B5 - Mobile photo upload / skip under threshold**, Hits largest in-journey leak (Income doc→Plan −22%).
- **B4 B1 - One plan for several open claims**, Multi-claim = 40–43% agent contact; biggest segment pain, heavier build.

### LATER, backlog
- **B5 B3 - Affordability check before plan options**, Supports keepability after handoff works; not the first gap to close.
- **B6 B6 - Pick a payment date that matches pay day**, Nice keepability tweak; weak link to Daniel’s blind-handoff metric.

### ✂ Cut List
- **B7 B8 - Chat assistant on every portal page**, Raises agree but already lifts miss risk; volume, not sustainable handoff.
- **B8 B7 - Show the shortest plan first to raise recovery**, Month-4 default already hurt keepability (miss 15.6%→19%); anti-hypothesis.
- **PRD highlights:** Vision: One-screen, read-only handoff of Mara’s digital attempt so Daniel starts where she stopped — not at zero.
Problem: Blind handoff / voice restart — 69.7% of contacts re-ask identity/affordability already typed (N-08; N-09 “just a number”).
Success: Repeated checks 69.7% → ≤55%; guardrail SSR ≥34.7%; 8-week decision window.
US-1: See attempt at intake (identity, affordability, last step, timestamp; empty state if none).
US-2: Plan + why offered from data — never invent rationale.
US-3: as of freshness + summary_shown / no_reask|reask_required instrumentation.
3 screens: Case list (badge) → Handoff Summary core → Confirmation with metric capture.
MUST: lookup, RO fields, journey status, rationale rules, freshness, empty/partial, instrumentation.
WON'T: create/edit plan, consumer UI/chat, multi-claim, affordability-engine rebuild.
Safety: Missing fields = Unavailable; no AI “suggest why.”
- **Prototype:** https://github.com/rene-riverty/2611.pschool/blob/main/04-roadmap/prototype-b4-handoff-summary.html

### Slide 8 · Validation
## Parameters
| Parameter | Decision |
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

### Slide 9 · Launch
- **GTM:** ## Get your prior work ready
- **The feature you're launching from your M4 PRD, one feature, not a list:** B4 — Agent Handoff Summary (read-only handoff of the digital instalment attempt for Daniel).
- **What your M5 experiment will test your hypothesis, primary metric and ship / iterate rule, the evidence the launch rests on:** Read-only one-screen handoff for Daniel: identity, affordability, last journey step, plan + rationale, freshness — so inbound calls start where the consumer stopped, not at zero.
- **Your persona pull your M2 persona, this anchors your audience:** Daniel

## Set your goal, then your audience
- **Primary GTM goal awareness · engagement · conversion, pick one:** Engagement
- **Why this goal? what makes this the right goal for this feature right now:** Agents with digital attempts use the handoff summary at call-start and mark no_reask, instead of asking for identity/affordability again.
- **Target audience the specific segment your goal implies, be precise:** Human agents like Daniel

## Size your launch
- **Launch tier S (minimal) · M (targeted) · L (multi-channel) · XL (full GTM):** M
- **Justification reach + revenue impact + what silence would risk:** Reach: Affects Collection Agents on inbound cases with a digital instalment attempt — not all consumers and not a company-wide UI. ~31% of journey starters contact an agent within 7 days (~2.6k contacts/month); 69.7% of those still repeat identity/affordability checks (~1.8k/month). That is a meaningful ops cohort, but a pilot / team-scoped audience.
Revenue impact: Indirect, not a new SKU or sales motion. Value = less blind rework (AHT/re-asks), faster keepable resolution, steadier recovery — while protecting SSR ≥34.7%. Material for Collection economics, but not press-release / ARR-launch scale.
Risk of silence: High for behavior change, low for brand. If we only ship a changelog, Daniel keeps the voice-restart habit and the 8-week hypnosis test (69.7% → ≤55%) fails. Silence = wasted build + continued rework cost.
Honesty check: S under-invests (enablement + adoption coaching needed). L/XL over-invests (no external awareness campaign, no trial-to-paid motion). M = focused enablement + in-product discovery for the pilot team — enough noise to change the workflow, not a big launch circus.
- **Is this a launch or a release? does it need go-to-market, or can it just ship?:** Release ships the feature; M-tier GTM ships the behavior change. Silence = failed launch even if deploy succeeded.

## Choose your top three channels and plan assets
- **Channel 1 owned / earned / paid, and why it reaches your audience:** Owned: In-product Agent Workspace — badge „Digital attempt“, Handoff panel on case open; Team huddle / TL floor briefing (15 min go-live + week-1 refresh); Internal Confluence / playbook one-pager + short Loom at desk; Pilot Slack/Teams channel #handoff-pilot
- **Channel 2 owned / earned / paid, and why:** Earned: Peer demos — 2–3 early adopters show a real call in huddle; TL coaching shout-outs when no_reask rises
- **Channel 3 owned / earned / paid, and why:** None
- **Enablement & assets what Sales / CS / Support need, plus the assets to build (one-pager, demo, etc.):** One-liner: Start where the consumer stopped — don’t restart identity/affordability by voice.

Field	Copy
Problem
Blind handoff: ~69.7% of contacts re-ask details already typed online (N-08)
What ships
Read-only Agent Handoff Summary — identity, affordability, last step, plan + why, as of
Who
Pilot Collection Agents (Daniel) on inbound cases with a digital attempt
Do
Open case → read summary → continue from last step → mark no_reask or reask_required
Don’t
Invent plan rationale; edit online inputs; push fragile agree-only plans
Success
Engagement → repeated checks 69.7% → ≤55%; guardrail SSR ≥34.7%
Out of scope
Create/edit plan, consumer UI, chat assistant

## Make it executable
- **Ownership named owner per key activity, individual, not department:** Activity	Named owner	Extra cost?
Overall GTM + success read (8 weeks)	René Weise (PM)	No
Feature flag / pilot cohort wiring	[Eng owner — name]	No (existing capacity)
Instrumentation: summary_shown, no_reask / reask_required	[Eng owner — name]	No
Weekly metric strip (re-asks %, SSR)	René Weise (PM) + pull from [Analyst — name]	Gap if no dashboard yet
1-page talk track + FAQ + objection card	René Weise (PM)	No
Annotated Screen-2 screenshot + 3 call scenarios	René Weise (PM)	No
Floor briefing (go-live + week-1 refresh)	[Pilot TL — name]	Maybe: 2×15 min team time / overtime
Peer demos in huddle	[Early adopter agent — name] (coached by TL)	No
#handoff-pilot Slack/Teams triage	[Pilot TL — name]	No
Compliance check on “don’t invent rationale” copy	[Compliance — name] (from N-12 stance)	No
Paid channels / ads	—	N/A — $0
- **Budget & resource gaps what costs extra, and any asset you can't currently build:** Pilot TL floor time: ~2 huddles × 15 min (ops cost, not marketing €)
Optional: Loom/video seat if none exists (~€0–20/mo) for desk Loom
Optional: Analyst hours for first weekly strip if no self-serve BI

Honest M-tier: budget is mostly people time, not ads. Biggest risk is unowned enablement, not underfunded marketing.
- **Timeline Phase 1 beta → Phase 2 launch moment → Phase 3 post-launch:** Beta / Early Access
René: brief, FAQ, screenshots, scenarios locked
Eng: flag on for ~5–8 pilot agents; instrumentation live
TL: soft brief; 1 peer dry-run call
Gate to Phase 2: ≥1 successful no_reask path + zero invented-rationale incidents

Launch moment
TL: 15-min go-live huddle (talk track)
René: Confluence one-pager + Loom posted; channel #handoff-pilot open
Eng: badge + panel on for full pilot queue
Day-0 check: % eligible cases with summary_shown

Post-launch adoption
Week 1: TL refresh huddle + 1 peer demo
Weekly: René posts metric strip; TL coaches re-ask habits
Week 4: leading-signal read (re-asks direction)
Week 8: go / iterate / kill (SSR ≥34.7% hard guardrail)
No new paid spend; scale only if engagement holds

## Define how you'll know it worked
- **Success metrics 2 to 3 metrics that match your GTM goal:** #	Metric	Target / rule	Why it matches Engagement
1	Feature adoption on eligible contacts — % cases with digital attempt where summary_shown = true	≥90% of eligible pilot contacts in week 1–2	Agents actually open/use the panel
2	Time to first key action — open case → mark no_reask or reask_required	≤20 seconds (oriented intake)	Onboarding/activation signal, not just “saw it”
3	no_reask rate on contacts with attempt present	Rising toward the product outcome: repeated checks 69.7% → ≤55%	Habit change = real engagement, not vanity reach
- **Bad signal to watch for e.g. high reach, zero signups = message-market mismatch:** High summary_shown, but no_reask flat → enablement/trust problem, not channel reach.
- **Most likely post-launch decision double-down · iterate · pivot · deprioritize, and what would trigger it:** Most likely iterate — engagement proves the panel is seen; only a clean 69.7%→≤55% with SSR intact triggers double-down.
- **Metrics:** #	Metric	Target	Bad signal → act
1	Adoption — % eligible contacts (attempt_present) with summary_shown = true	≥90% by end week 2	<70% by day 3 → re-brief TL + check badge/panel discoverability
2	Time to first key action — open case → no_reask / reask_required	Median ≤20s	Median >45s in week 1 → simplify panel / coaching (onboarding fail, not reach)
3	Habit / outcome — repeated identity/affordability checks	→ ≤55% by week 8 (leading: ≥5 pp drop by week 4)	summary_shown ≥90% but re-ask drop <5 pp → trust/enablement/stale data — iterate enablement, don’t add channels

Guardrail: SSR resolved % of journey starters ≥34.7% (if it drops → pause scale / deprioritize path).

Primary early warning: High shown, flat no_reask = agents see it but don’t change behavior.

### Slide 10 · Story
- **Friction + aha:** Daniel opens the case, sees Mara’s identity + affordability + last step + plan why on one screen, and realizes: I don’t have to start at zero — I can continue where she stopped. First no_reask mark = the hypnosis click; that’s when Engagement becomes real.
- **Takeaways / next:** Key takeaways

B4 is a release + M-tier launch, not “just ship”: success = Engagement (use + no_reask), not awareness.
Audience is Daniel / pilot agents — show up in workspace + floor, not paid/social.
Tier M is honest: meaningful ops cohort (~1.8k re-ask contacts/mo pattern), indirect revenue, silence kills the habit test.
Metrics must match the goal: summary_shown ≥90%, time-to-mark ≤20s, re-asks 69.7%→≤55%; guardrail SSR ≥34.7%.
Bad signal: high shown, flat no_reask → fix enablement/trust, not more channels.
Most likely post-launch: Iterate; double-down only on a clean week-8 read.
What I’d do next

Name owners (Eng, Pilot TL, Analyst, Compliance) — unblock sign-off.
Lock metric definitions + Monday strip (manual OK until dashboard).
Run Phase 1 beta (5–8 agents): brief, dry-run, instrumentation check.
Launch moment: TL huddle + in-product on; day-0 adoption check.
Week 4 / 8 reads: iterate enablement or double-down / kill per triggers — no scope creep into write-path.

---

Submitted to the Product Management Certification learning platform · Product School.
