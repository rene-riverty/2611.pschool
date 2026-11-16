## Sign-off review — B4 Agent Handoff Summary GTM

**Verdict: Conditional approve (M-tier Engagement).** Strategy fits an internal ops habit-change. **Do not lock** until Eng / Pilot TL / Analyst names are filled and the metric strip is owned without a dashboard gap.

---

### Pressure-test

**1. Audience vs goal — pass**  
Goal is **Engagement**, audience is **Daniel (pilot agents)** — not consumers, not “market awareness.” Channels and assets follow that. No awareness-default.

**2. Launch tier — pass (honest M)**  
Reach (~1.8k re-ask contacts/mo via pilot agents), indirect revenue, high silence-risk for behavior → **M is right**. Not S (needs coaching), not L/XL (no external/ARR motion).

**3. Channels — mostly pass; one soft spot**  
| Channel | Hold-to-account view |
|---|---|
| In-product badge + panel | **Keep — primary.** Where the call starts. |
| TL huddle / week-1 refresh | **Keep — required.** Habit changes on the floor. |
| Confluence + Loom | **Keep as backup**, not primary. Desk reference only. |
| `#handoff-pilot` | **Keep**, only if TL owns triage daily in week 1–2. |
| Peer demos + TL shout-outs | **Keep — strongest earned.** |
| Paid | Correctly **none**. |

**Won’t work alone:** Confluence/Loom without floor coaching = silent ship. Treat as secondary.

**4. Ownership & gaps — fail until fixed**  
Still placeholders: Eng, Pilot TL, Analyst, Compliance, Early adopter. That is the classic GTM failure mode you called out.  
**Surfaced gaps OK:** no dashboard; TL time; €0 paid.  
**Missing:** who covers TL if absent on go-live day; who defines `eligible contact` in the warehouse.

**5. Metrics & bad signal — pass, tighten definitions**  
Adoption + time-to-action + `no_reask` match Engagement. Bad signal (high `summary_shown`, flat `no_reask`) is actionable. Make week-2 thresholds numeric so stakeholders can hold you to them.

---

### Rewrites stakeholders can hold you to

**Goal (locked)**  
By end of week 8 of pilot, Collection Agents on inbound cases **with a digital instalment attempt** use the Handoff Summary at case-open and select `no_reask` or `reask_required` on **100%** of those contacts; repeated identity/affordability checks fall from **69.7% to ≤55%** without SSR falling below **34.7%**.

**Audience (locked)**  
Named pilot cohort: **N agents** on **one TL’s queue** (target **5–8** in beta, full that queue at launch). Out of audience: consumers, sales, company-wide Cosima users.

**Tier justification (one paragraph)**  
**M — targeted.** Affects pilot agents on ~31% journey-starter→agent path (~2.6k contacts/mo; ~1.8k re-ask pattern). Revenue impact is ops/recovery quality, not a SKU. Silence kills the behavior test; ads would over-invest. Enablement + in-product discovery only.

**Channels (commitment)**  
Primary: in-product + TL floor. Secondary: Confluence/Loom + `#handoff-pilot`. Earned: ≥2 peer demos by week 2. Paid: **€0**.

**Enablement one-liner (locked)**  
“Start where they stopped — don’t re-ask identity/affordability already in the summary.”

**Ownership (must name before go-live)**  

| Activity | Owner (replace before lock) | Done-when |
|---|---|---|
| GTM + week-8 decision | **René Weise** | Written go/iterate/kill note |
| Flag + instrumentation | **Eng: ___** | Events in prod for pilot |
| Weekly metric strip | **René** + **Analyst: ___** | Posted every Monday 10:00 |
| Floor briefings | **Pilot TL: ___** | Go-live + week-1 done |
| Peer demos | **Agent: ___** (TL coaches) | 2 demos by day 14 |
| Channel triage | **Pilot TL: ___** | ≤24h response week 1–2 |
| “No invent rationale” copy | **Compliance: ___** | Written OK before Phase 2 |

**Budget gaps (explicit)**  
- Extra: ~30 min team time (2×15 min); optional Loom seat.  
- Gap: no live dashboard → **René ships manual strip from export until Analyst delivers v1 by launch−3 days.**  
- Blocker: unnamed Eng/TL/Analyst = **no Phase 2**.

**Phase gates (hold-to-account)**  
- **Exit Beta:** ≥1 live `no_reask`; **0** invented-rationale incidents; instrumentation verified on 10 sample cases.  
- **Launch day:** TL huddle completed; Loom+one-pager live; full pilot queue flagged on.  
- **Day 0–1:** `summary_shown` ≥**70%** eligible (ramp); week 2 ≥**90%**.  
- **Week 4:** re-ask rate down **≥5 pp** or iterate plan filed.  
- **Week 8:** ≤**55%** re-asks + SSR ≥**34.7%** → double-down; else iterate/pivot/deprioritize per triggers below.

**Success metrics (locked)**  

| Metric | Definition | Target | Early warning |
|---|---|---|---|
| Adoption | Eligible = inbound + `attempt_present`; event `summary_shown=true` | ≥90% by end week 2 | &lt;70% day 3 → TL re-brief + UI discoverability |
| Time to decision | Case open → `no_reask`/`reask_required` | Median ≤20s on attempt_present | Median &gt;45s week 1 → simplify panel / coaching |
| Habit / outcome | Share repeating identity/affordability checks | ≤55% by week 8 (leading: ≥5 pp by week 4) | `summary_shown` ≥90% **and** re-ask drop &lt;5 pp → trust/enablement iterate, not more channels |

**Post-launch decision (default expectation: Iterate)**  
- **Double-down:** ≤55% re-asks + SSR ≥34.7% + adoption ≥90%.  
- **Iterate:** ≥5 pp drop but &gt;55%, or high shown / flat `no_reask`.  
- **Pivot:** &lt;5 pp drop despite adoption ≥90%.  
- **Deprioritize:** SSR &lt;34.7% or miss-rate worse with flat leading metric.

---

### Sign-off conditions (PMM)

1. Fill every `___` name.  
2. Publish metric definitions (`eligible`, `summary_shown`, re-ask) in one Confluence para.  
3. Confirm Analyst backup for Monday strip.  
4. Compliance sign-off on Do/Don’t before launch huddle.

**Then: approve M-tier Engagement GTM.** Until then: **revise — ownership incomplete.**