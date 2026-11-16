# GTM Launch Plan, Riverty BU Collection, A Fair Way Forward

| Field | Value |
|---|---|
| Feature | B4 — Agent Handoff Summary (read-only handoff of the digital instalment attempt for Daniel). |
| Goal | Engagement |
| Launch tier | M, Targeted |

## Goal & Audience
- **Goal:** Engagement, Agents with digital attempts use the handoff summary at call-start and mark no_reask, instead of asking for identity/affordability again.
- **Target audience:** Human agents like Daniel.

## Launch Tier
- **M, Targeted**, Reach: Affects Collection Agents on inbound cases with a digital instalment attempt — not all consumers and not a company-wide UI. ~31% of journey starters contact an agent within 7 days (~2.6k contacts/month); 69.7% of those still repeat identity/affordability checks (~1.8k/month). That is a meaningful ops cohort, but a pilot / team-scoped audience.
Revenue impact: Indirect, not a new SKU or sales motion. Value = less blind rework (AHT/re-asks), faster keepable resolution, steadier recovery — while protecting SSR ≥34.7%. Material for Collection economics, but not press-release / ARR-launch scale.
Risk of silence: High for behavior change, low for brand. If we only ship a changelog, Daniel keeps the voice-restart habit and the 8-week hypnosis test (69.7% → ≤55%) fails. Silence = wasted build + continued rework cost.
Honesty check: S under-invests (enablement + adoption coaching needed). L/XL over-invests (no external awareness campaign, no trial-to-paid motion). M = focused enablement + in-product discovery for the pilot team — enough noise to change the workflow, not a big launch circus.

## Channels
1. **Owned: In-product Agent Workspace — badge „Digital attempt“, Handoff panel on case open; Team huddle / TL floor briefing (15 min go-live + week-1 refresh); Internal Confluence / playbook one-pager + short Loom at desk; Pilot Slack/Teams channel #handoff-pilot**
2. **Earned: Peer demos — 2–3 early adopters show a real call in huddle; TL coaching shout-outs when no_reask rises**
3. **Paid: None**

## Enablement & Assets
One-liner: Start where the consumer stopped — don’t restart identity/affordability by voice.

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

## Ownership, Budget & Timeline
- **Ownership & budget:** Activity	Named owner	Extra cost?
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
- **Timeline:** Beta / Early Access
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

## Success Metrics
- **Metrics:** #	Metric	Target / rule	Why it matches Engagement
1	Feature adoption on eligible contacts — % cases with digital attempt where summary_shown = true	≥90% of eligible pilot contacts in week 1–2	Agents actually open/use the panel
2	Time to first key action — open case → mark no_reask or reask_required	≤20 seconds (oriented intake)	Onboarding/activation signal, not just “saw it”
3	no_reask rate on contacts with attempt present	Rising toward the product outcome: repeated checks 69.7% → ≤55%	Habit change = real engagement, not vanity reach
- **Bad signal to watch for:** High summary_shown, but no_reask flat → enablement/trust problem, not channel reach.
- **Likely post-launch decision:** Most likely iterate — engagement proves the panel is seen; only a clean 69.7%→≤55% with SSR intact triggers double-down.
