# 46 — Dormancy Commitment Boundary, v0

**Status:** qualitative lifecycle-architecture pass using owner-supplied design direction. It draws the boundary that [42](42_WORLD_TIME_SEASONAL_OPPORTUNITY_AND_EMBODIMENT_V0.md) and [45](45_REMAINING_PRODUCTIVE_OPPORTUNITY_QUALITATIVE_COMPOSITION_V0.md) both lean on — *approaching* dormancy versus *committed* to it — and adds **no new life-cycle state**. It defines no trigger value, rate, duration, calendar date, species dormancy fact, hormone, physiology, indicator or input field, and it researches no botany.

> **Commitment belongs to the plant, not the weather.**

## 1. Purpose

AMO-D146 settled that a Warden can chase suitable weather but cannot outrun dormancy *once biology has committed to the transition*, and doc 45 made that commitment the point at which **Biological Growth Availability** closes. Neither document said what commitment is. This pass answers one question:

> What does it mean for an individual to be approaching Dormancy, versus biologically committed to the Dormancy transition?

## 2. Dormancy Approach

> **Dormancy Approach** is the pre-commitment period in which the individual's biology is trending toward the end of its active phase but has not yet irreversibly committed to that transition.

During Approach the individual is still **in its active phase**:

- active growth may still be biologically available;
- Productive Return may still occur ([39](39_ACTIVE_LEAF_PRODUCTIVE_RETURN_AND_PERSISTENT_TUBER_BENEFIT_V0.md));
- Environmental Fit may still influence whether active biology continues;
- changing conditions matter, and relocation or a controlled environment may matter where the individual's lifecycle strategy permits.

Approach is a **condition within Active Leaf**, not a state. It needs no field, flag or meter, and it is never a promise that commitment will follow soon — or at all, for a strategy that rarely meets it (§10).

## 3. Dormancy Commitment

> **Dormancy Commitment** is the qualitative boundary at which the individual has biologically committed to ending its current active phase and proceeding toward Dormancy.

> **Approaching Dormancy and committed to Dormancy are not the same biological condition.** Before commitment, environment may still matter. After commitment, the current active phase is ending.

Once crossed, for the current active phase:

- Biological Growth Availability is closed;
- better weather does not restart the phase;
- relocation does not reset the lifecycle;
- greenhouse conditions do not cancel the commitment;
- Remaining Productive Opportunity from this phase cannot be restored by improving external conditions.

No threshold defines the crossing (AMO-D155).

### Where it sits in the topology

Dormancy Commitment is what the existing **Active Leaf → Senescence** transition means biologically. The seven-state graph is unchanged ([17](17_LIFE_CYCLE_STATE_MACHINE_V0.md) §4):

```
ACTIVE LEAF ─────────── Dormancy Approach: a condition, still active-capable
     │
     ▼  DORMANCY COMMITMENT — the transition edge, irreversible for this phase
SENESCENCE ──────────── normal retirement: the committed transition, manifestation receding
     ▼
manifestation ends; Tuber-only transition
     ▼
EARLY DORMANCY ──▶ DEEP DORMANCY
```

So **Approach is a condition, Commitment is the edge, and Senescence is the committed transition period** — the same shape as Collapse Commitment followed by a terminal period, without sharing its cause (§9).

**Commitment is not instantaneous Dormancy.** It begins an irreversible transition; Deep Dormancy may still be some way off, and the manifestation may still exist, be inhabitable under the ordinary gates and be relocated ([17](17_LIFE_CYCLE_STATE_MACHINE_V0.md) §7, Senescence).

**Commitment is not its appearance.** Visible yellowing, receding and retirement are **presentation that may follow** the biological crossing, possibly with a lag; they never define it (AMO-D134, AMO-D024). Biology owns the truth.

**Commitment closes the phase, not the plant.** Dormancy, renewed lifecycle readiness and a new Emergence may produce another active manifestation in a later cycle ([17](17_LIFE_CYCLE_STATE_MACHINE_V0.md) §2). Nothing about commitment is a permanent shutdown. When and how the dormant Tuber can begin another phase — Intrinsic Reactivation Readiness, External Emergence Suitability, feasibility and Reactivation Commitment — is specified in [47](47_DEEP_DORMANCY_DURATION_AND_ACTIVE_PHASE_REACTIVATION_BOUNDARY_V0.md); this document governs only the ending.

**Irreversibility, v0.** Once crossed, commitment is not reversed for that active phase by ordinary World change, relocation, rooting, embodiment or controlled environments. No exotic biological exception is defined; whether any could ever exist stays with AMO-Q101.

## 4. Lifecycle sovereignty

The World can provide good, poor or changing conditions. **Dormancy Commitment belongs to the individual Amorpho's lifecycle**: the World never commands `DORMANCY = TRUE`, and there is still no `force_dormancy` or `prevent_dormancy` flag ([17](17_LIFE_CYCLE_STATE_MACHINE_V0.md) §9, AMO-D035–AMO-D037, AMO-D046).

```
WORLD               → what conditions exist here, now
ENVIRONMENTAL FIT   → what those conditions do to this biology
LIFE-CYCLE SYSTEM   → whether and when this individual commits
```

**World and individual may disagree, and that is a valid state.** Excellent conditions plus a committed individual: no active growth. Poor conditions plus an active-capable individual: biology remains willing, and Fit prevents productive success. The two are independent inputs to doc 45's composition.

## 5. Environment before commitment

Before commitment, **favourable conditions may legitimately help an individual continue its active phase** where its lifecycle strategy permits — which is why extended growth, geographic relocation and controlled environments can matter at all ([42](42_WORLD_TIME_SEASONAL_OPPORTUNITY_AND_EMBODIMENT_V0.md) §5–§6). They never *always* prevent dormancy: the lifecycle remains sovereign.

**Poor conditions may influence Approach without being commitment.** Poor Fit may reduce active viability, move the individual toward a lifecycle transition, or leave it unable to use what opportunity exists. Bad weather is never itself commitment.

Severe pressure may lead an individual's own lifecycle to commit **early** — the existing premature-retreat path, the same Senescence transition arriving early ([17](17_LIFE_CYCLE_STATE_MACHINE_V0.md) §8, AMO-Q087). That is still the plant's commitment, reached under pressure; the environment pushed and the lifecycle decided. And such an early retreat may be **protective** rather than a loss (AMO-D092).

**Commitment is not a punishment for bad conditions.** For strongly seasonal biology it may be the correct outcome of a *successful* active phase. Healthy biology can choose Dormancy.

## 6. Irreversibility after commitment

After commitment the following are all rejected:

- good weather → the current phase returns to full active growth;
- travel to another latitude or hemisphere → commitment cleared;
- greenhouse → active phase reset;
- commitment → relocate → active-phase Productive Opportunity resets (*no last-minute productivity reset*).

> **Relocation changes the World, not the decision already made by the plant** (L65). **Infrastructure modifies the World, not lifecycle history.**

Before commitment, relocation and greenhouses may extend active opportunity; after it, they change only where the transition happens.

## 7. Embodiment pause

The two clocks of [42](42_WORLD_TIME_SEASONAL_OPPORTUNITY_AND_EMBODIMENT_V0.md) apply on both sides of the boundary: inhabitation pauses ordinary biological progression, lifecycle progression included, while World Time continues (AMO-D084, AMO-D136, AMO-D145).

**Embodiment before commitment.** An approaching individual that is inhabited does not progress toward commitment while embodied.

> **World time alone cannot push a biologically paused individual across the commitment boundary.** No hidden lifecycle ageing occurs while embodied.

But the World moves on: local external opportunity may disappear while the individual is frozen short of commitment. When the Warden roots, the individual resumes **from its actual paused lifecycle state** — and in the **current** World, whose conditions may now influence its trajectory according to its strategy. Whether commitment then follows quickly, slowly or not yet is future lifecycle modelling (AMO-Q101).

> **Biology resumes in the current World; it does not replay the World that existed when it was paused.**

**Embodiment after commitment.** A committed individual whose manifestation still exists may be inhabited under the ordinary gates. The transition pauses while embodied; **commitment remains**. On exit the Dormancy transition resumes from the same committed state, and favourable World conditions do not reopen active availability. This mirrors terminal embodiment exactly ([34](34_EMBODIMENT_ACROSS_TERMINAL_MANIFESTATION_COLLAPSE_V0.md), AMO-D117): *embodiment can pause the transition, but it cannot reverse commitment.* Exit-and-re-entry resets nothing (AMO-D157).

Embodiment stays open-ended either way — no forced exit, timer or cooldown (AMO-D117, AMO-D145).

## 8. Productive Opportunity handoff

At Dormancy Commitment, **Biological Growth Availability for the current active phase closes**, so usable Remaining Productive Opportunity closes **even if** external conditions remain excellent and the Leaf remains intact and functional ([45](45_REMAINING_PRODUCTIVE_OPPORTUNITY_QUALITATIVE_COMPOSITION_V0.md) §4, AMO-D153). Future active-Leaf work for the phase ends with the lifecycle, not with the external season.

**Realized Productive Return remains** (L61, AMO-D137). Commitment closes future ordinary work, never the history of work done, and the individual carries its completed productive history into dormancy and the next cycle ([44](44_FULL_BIOLOGICAL_YEAR_PERSISTENT_STATE_INTEGRATION_TRACE_V1.md)).

**Commitment timing is strategically meaningful.** Whether an individual is fully active, approaching or already committed changes what withdrawal, relocation, embodiment and roster choice are worth ([45](45_REMAINING_PRODUCTIVE_OPPORTUNITY_QUALITATIVE_COMPOSITION_V0.md) §16). No interface is designed, and **the Warden need not know exactly** where an individual stands; future cues may be biological, visual, historical or contextual. The state exists independently of player certainty (AMO-Q119); what the Warden can infer about it is specified in [50](50_WARDEN_BIOLOGICAL_INFORMATION_AND_ROSTER_JUDGEMENT_MODEL_V0.md) (AMO-D164).

**No countdown.** Rejected: *Dormancy in 3 days*, *Dormancy Commitment 82%*, a season meter, an active-days counter, a hidden seasonal score (AMO-D091, L67).

## 9. Collapse versus Dormancy

Two commitment concepts now exist. They share a shape — a biological trajectory that ordinary conditions can no longer return to the prior viable phase — and nothing else.

| | **Collapse Commitment** | **Dormancy Commitment** |
|---|---|---|
| Belongs to | the current **Leaf** | the **individual's lifecycle** |
| Cause | loss of active-Leaf role viability through impairment or damage (AMO-D114, AMO-D115) | normal lifecycle ending of the active phase |
| Ends | that manifestation | that active phase |
| Afterwards | a terminal period, then routing from the Tuber | Senescence, then dormancy |
| Leaves Biological Growth Availability | possibly **open** — which is why Replacement can exist (AMO-D096) | **closed** for this phase |

> **Collapse ends a Leaf; Dormancy Commitment ends a phase.**

Consequences, all canonical:

- **A healthy, highly functional Leaf may enter Dormancy Commitment.** No damage is required.
- **A damaged, scarred, compensated but still viable Leaf may reach normal Dormancy Commitment.** Damage does not force every retirement through Collapse.
- **Functional Collapse may come first.** Severe damage → Collapse Commitment → the existing routing point, which may supersede the normal active-phase trajectory ([17](17_LIFE_CYCLE_STATE_MACHINE_V0.md) §8). If the individual then takes the retreat route, its lifecycle commits to ending the phase from the Tuber — a Dormancy Commitment with a **different causal history**. If it takes Replacement, no Dormancy Commitment has occurred. Collapse is never itself Dormancy Commitment, and routing is not redesigned here.

**Other distinctions held:** Dormancy Commitment is not Deep Dormancy (§3); not pathology — normal dormancy may be part of excellent health (AMO-D148); not resource exhaustion or low Core Viability — a robust, depleted, pathological or highly viable Tuber may each commit (AMO-D151); not a Productive Return threshold — no *enough return → dormancy* rule exists; and not Developmental Maturity, which is never a dormancy meter (AMO-D080).

**Bloom.** Bloom is a sibling active state and its ending is not designed here; how Bloom's own retirement relates to this boundary stays with AMO-Q088 and AMO-Q084.

## 10. Species strategy and individual history

The architecture must support later externally curated lifecycle strategies that differ in how readily Approach occurs, whether strong seasonal dormancy is typical, whether extended active growth remains possible, how responsive the lifecycle is to environment, and how strongly an individual tends toward dormancy after a given history ([42](42_WORLD_TIME_SEASONAL_OPPORTUNITY_AND_EMBODIMENT_V0.md) §7, AMO-D147). No real species is assigned to any of them (AMO-D024).

- **Extended-growth strategies** may meet commitment rarely, differently, or much less often. **No universal annual cycle** is imposed.
- **Strongly seasonal strategies** may rely on commitment as a prominent recurring transition. That is biological differentiation, not a disadvantage to normalize away.
- **More active time is not automatically better.** A strategy may benefit from ending its active phase; no such benefit is designed.

**Commitment is history-sensitive.** It is never reducible to month, latitude, temperature alone or species lookup alone. The individual may carry current Tuber condition, previous active duration, Productive Return history, prior dormancy history, manifestation state, Fit history and current condition; how these combine is not defined (AMO-Q101).

**No hidden anti-exploit rule.** Rejected: *travelled too often → forced dormancy*, a maximum season-extension count, and mandatory annual sleep for all species. Commitment arises from biology only.

## 11. Worked traces

**A — continued active phase before commitment.** An individual trends toward dormancy; commitment has not occurred. Conditions improve, or relocation reaches better Fit, and its lifecycle strategy still permits continuation. Active growth continues and Productive Opportunity remains. Not every strategy can do this, and no guarantee is given.

**B — normal commitment.** A healthy, productive Leaf. The individual's lifecycle reaches the boundary and commits. Biological Growth Availability closes for the phase; the Leaf moves into ordinary retirement; realized return stays with the Tuber; dormancy follows. **No pathology.**

**C — excellent environment after commitment.** Commitment occurs. The Warden moves the individual to excellent conditions. External opportunity is excellent; Biological Growth Availability stays closed; the phase does not reopen.

**D — embodiment before commitment.** An approaching individual, not yet committed, is inhabited. Lifecycle progression pauses while the World season advances. The Warden later roots; the individual resumes from its pre-commitment state, and current conditions may now influence what follows. **No lifecycle advancement occurred because World time passed.**

**E — embodiment after commitment.** The individual commits; the Warden inhabits while the manifestation still exists. Progression pauses and commitment remains. On exit the transition resumes, and favourable conditions do not reopen active availability.

**F — Collapse instead of Dormancy.** An active-capable individual's Leaf is severely damaged, reaches Functional Collapse and crosses Collapse Commitment; the Leaf follows its terminal route. **This is not Dormancy Commitment.** The individual may later route toward dormancy from the Tuber, with a different causal history.

## 12. Acceptance and consistency audit

| Test | Result |
|---|---|
| **A — Approach** | Active biology may still continue. |
| **B — Commitment** | The current phase cannot be reopened by a better environment. |
| **C — travel before** | Relocation may extend the active phase where biology permits. |
| **D — travel after** | No lifecycle reset. |
| **E — greenhouse before** | May extend usable conditions. |
| **F — greenhouse after** | Cannot cancel commitment. |
| **G — embodiment before** | Biology paused; World time cannot itself cause commitment. |
| **H — embodiment after** | Transition pauses; commitment persists. |
| **I — healthy dormancy** | A healthy Leaf can commit. |
| **J — Collapse** | Functional Collapse stays a separate commitment. |
| **K — opportunity** | Commitment closes Biological Growth Availability in doc 45. |
| **L — no universal annual dormancy** | Extended-growth strategies remain possible. |

| Distinction | Holds |
|---|---|
| Approach ≠ Commitment ≠ Deep Dormancy | §2, §3 |
| Commitment ≠ Functional Collapse, pathology, resource exhaustion, Core Viability, maturity, return threshold | §9 |
| Good Fit may influence pre-commitment biology, never reset post-commitment lifecycle | §5, §6 |
| World Time continues during embodiment; lifecycle progression does not | §7 |
| Travel changes environment, not lifecycle history | §6 |

## 13. Deferred quantitative biology

AMO-Q101 keeps the exact trigger representation, how environmental influence before commitment works, individual-history weighting, timing, any reversibility exception and the quantitative lifecycle model. AMO-Q084 keeps species parameterization of Approach and Commitment, and Bloom's ending. AMO-Q119 keeps what the Warden can know, and any future player-facing cue. AMO-Q087 keeps how early a premature retreat may be; AMO-Q116 the quantitative opportunity model. No new question was required.

**Result:** a plant nearing the end of its season can still be persuaded by good conditions; a plant that has decided cannot. The weather can change where the ending happens and how it feels, the Warden can pause it, and neither can take the decision back.
