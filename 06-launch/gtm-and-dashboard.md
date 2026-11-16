# GTM Strategy & Success Dashboard (Module 6)

## Get your prior work ready
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
