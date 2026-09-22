# 25 — Tuber-Funded Manifestation and Replacement Routing, v0

**Status:** conceptual specification. This extends the [life-cycle state machine](17_LIFE_CYCLE_STATE_MACHINE_V0.md) at one damaged-Leaf routing point. It defines no species facts, cost amounts, time spans, thresholds, formulas, player interface or combat mapping. The owner-supplied replacement direction is a game-system capability; species scope awaits approved input (AMO-D024).

> The Tuber funds the manifestation. The Leaf works for the future Tuber. A replacement salvages what remains; it does not restore what was spent or missed.

## The persistent body funds temporary manifestations

The **Tuber is the persistent primary biological body of one individual**, not a discarded resource container under a primary Leaf. It carries identity, genetics, lineage, current condition, reserves, Developmental Maturity, any persistent injury and life-cycle history through Leaf, Bloom, retreat, dormancy and re-emergence (AMO-D058, AMO-D080, AMO-D087). Leaf and Bloom are temporary manifestations of that same individual. A new Leaf is neither a new plant nor repair of an old Leaf (AMO-D074, AMO-D094).

Emergence is a biological investment from the Tuber's current capacity. A primary Leaf's possible scale and biological capability therefore depend on persistent development, current condition, available reserves and future species interpretation; a weak Tuber cannot produce or sustain any desired Leaf on command (AMO-D095, AMO-Q110). The Leaf can later do useful biological work that supports future Tuber state. **Funding now and productivity later are different events**; this is a direction of dependence, not a balance equation or one universal Tuber-capacity meter (AMO-Q106, AMO-Q116). Biological Leaf scale is not combat strength (L5, AMO-Q109).

## Keep the current Leaf while it remains useful

The mature Leaf's architecture does not regrow into its pristine form (AMO-D094). Repeated small injuries can accumulate as scars, asymmetry and wear while the **same Leaf** stabilizes, compensates and retains useful **Leaf Functional Capacity** ([24](24_SAME_PHASE_LEAF_RECOVERY_V0.md), AMO-Q103). Visible damage alone does not open a replacement route (AMO-D091, L51). Repeated microdamage normally stays with the current Leaf as long as it remains a viable active manifestation.

The **functional-collapse routing point** is qualitatively different: after damage, the current Leaf can no longer adequately perform its central biological role for the remaining active phase, even considering feasible same-Leaf stabilization. This is not ordinary end-of-phase Senescence. A dramatic break may contribute, but neither appearance nor one named injury is a trigger by itself. The biological definition of inadequate function, including whether a temporarily impaired Leaf could still recover, remains AMO-Q101 with AMO-Q103. This specification gives the boundary a place in the lifecycle; it assigns no threshold or verdict from structural loss alone (AMO-D096).

## Replacement is funded salvage

When the current Leaf cannot adequately continue, **Replacement Emergence** may form a new Leaf from the same Tuber during the disrupted active period. It is an **intra-cycle salvage route**, not ordinary emergence after dormancy and not a fresh annual cycle. The Tuber invests again in emergence, formation and establishment, and biological time passes before the new Leaf becomes useful. Earlier opportunity is gone; development time also consumes part of what remains. The new manifestation starts structurally fresh yet inherits the individual's condition and history, never the old Leaf's physical wound (AMO-D074, AMO-D094).

Replacement must have a meaningful biological price and a limit. Its investment carries forward in persistent Tuber state: capacity has been spent, potentially leaving fewer reserves or less ability to withstand another adverse event than if the replacement had not been made. This **normal biological investment is not Pathological Tuber Impact** merely because capacity is spent (AMO-D087, AMO-D092). Whether harmful persistent loss later occurs is downstream (AMO-Q118). A replacement is generally expected to be smaller or otherwise reduced compared with the primary Leaf because the Tuber has already invested and opportunity has passed; this is a **design direction**, not a universal species fact or a fixed ratio (AMO-Q084, AMO-Q110). Its biological scale does not determine combat power.

Replacement potential follows current Tuber capacity, condition, reserves, developmental context and **Remaining Productive Opportunity**. Opportunity is biological, shaped by the future environment, life-cycle timing and emergence time, **not a visible season countdown** (AMO-D091, AMO-Q116). A strong Tuber may fund a useful replacement; a depleted one may fund only a reduced one or none. None of those labels is a new stored score. Funding one replacement can narrow later options; another injury cannot trigger unlimited free re-emergence. Whether a further replacement is ever biologically possible remains open (AMO-Q084, AMO-Q101).

## The routing boundary: eligibility before strategy

At serious impairment, the life-cycle system first tests whether the current Leaf can still adequately continue. **Only after functional collapse is confirmed** does it evaluate the biologically available replacement and retreat routes using Amorpho state and Environmental Fit. These are distinct questions:

| Route | Eligibility question | Strategic question still open |
|---|---|---|
| **Continue current Leaf** | Can it still stabilize and perform useful work? | Is continued use sensible under subsequent conditions? |
| **Replacement Emergence** | Can this Tuber fund and establish another Leaf while opportunity remains? | Is the cost worthwhile compared with conserving capacity? |
| **Early retreat** | Must or may active growth be abandoned? | When is conservation the better course? |

Functional collapse rules out **adequate continuation by the present Leaf**; its prospect of later recovery is judged before that verdict. Replacement **eligibility** does not command replacement. A capable Tuber may conserve itself and retreat when little opportunity remains; a weak Tuber may have no replacement option at all (AMO-D096). Early retreat uses the existing **Senescence** path, not a new dormancy state (AMO-D070, AMO-Q087). The exact eligibility, advisability and retreat triggers stay with AMO-Q101; the full productivity valuation stays with AMO-Q116.

**Eligibility is not preference, and preference is not the Warden's.** With nothing intervening, the individual's own biology selects the route serving its long-term continuation — which may be conserving capacity rather than spending it on an eligible replacement (AMO-D098). A Warden may select differently only with **direct astral presence**, established while the individual is still reachable, only among biologically feasible routes, and only at the cost the plant itself would have paid; ownership, an Astral Signal, Astral Capacity or inhabiting another Amorpho grants none of it (AMO-D099–AMO-D101, L52). The **Tuber stays non-playable** throughout — presence at a transitional Tuber influences a routing decision and never becomes a body (AMO-D089). The three-layer model, the Astral Window and their limits are specified in [26_PLANT_AUTONOMY_ASTRAL_LEVERAGE_AND_ROUTING_V0.md](26_PLANT_AUTONOMY_ASTRAL_LEVERAGE_AND_ROUTING_V0.md). The Warden cannot create capacity, time or a larger Leaf by choice, and while this individual is astrally embodied normal biology and phase progression pause (AMO-D084); no replacement grows merely because the Warden requests it. How presence is established and what a player may know remain AMO-Q119.

If no presence is established, the World still advances: the biological system must choose an eligible route autonomously. It cannot suspend a damaged rooted individual indefinitely for a menu. **An autonomous outcome is required; its objective is the individual's own continuation, and its policy is still unspecified** (AMO-D097, AMO-D098, AMO-Q101). A player who can choose need not know exact future weather, replacement cost or outcome; simulation truth and player prognosis are separate (L14, AMO-Q119).

## Smallest life-cycle extension

The existing seven-state graph can represent replacement by **reusing Emergence in a replacement context**, without adding a state:

```text
ACTIVE LEAF → same-Leaf stabilization → ACTIVE LEAF
            → functional-collapse routing
                 → eligible and selected: EMERGENCE (replacement) → ACTIVE LEAF
                 → retreat selected or required: SENESCENCE → dormant family
```

The replacement loop remains in the **same broader active period**; it does not traverse Deep Dormancy or reset the persistent individual. Existing Emergence means a manifestation is forming; its replacement context identifies why it was entered (AMO-D096). The new Leaf may assume the active role after formation. Exactly how old and new Leaf coexist or hand over function, and when either is astrally detectable, ready or inhabitable, remain AMO-Q084, AMO-Q085, AMO-Q112 and AMO-Q115. Reusing the state is **not** a ruling that the old Leaf vanishes on entry or that the Warden can transfer into the new one.

## Worked routing checks

**A — scarred but successful.** A mature Leaf takes repeated small injuries. Its appearance becomes worn, but stabilization and compensation preserve useful function. It remains the same active Leaf through the season. No replacement eligibility follows from scars alone.

**B — early collapse, capable Tuber.** A strong Tuber has already funded a substantial primary Leaf. Early loss of central Leaf function leaves substantial biological opportunity, and the present Leaf cannot recover enough. Replacement is eligible and is selected, whether by available agency or future autonomous policy. The Tuber invests again; after biological emergence time, a smaller, structurally new Leaf can do useful work in the **remaining** period. Stop before calculating its final Tuber outcome.

**C — late collapse, eligibility without obligation.** The Tuber could fund another Leaf, but little useful opportunity may remain after emergence. Conserving capacity through early Senescence is a plausible route; replacement is still technically possible. No universal late-season rule or perfect forecast is implied.

**D — insufficient capacity.** The present Leaf collapses while the Tuber is depleted or compromised. It cannot fund a viable replacement. No player choice can create that route; early retreat or failure remains for the life-cycle rules to resolve.

**E — unattended plant.** A rooted individual suffers functional collapse while its player is elsewhere or offline. Biological eligibility and an autonomous route still have to be evaluated. The simulation does not wait for player input. A later second injury to a funded replacement would meet a newly constrained Tuber, not an unlimited refresh loop.

**F — agency available.** If a Warden establishes direct astral presence at this rooted individual's routing point (AMO-D101), the life-cycle system first establishes that both replacement and retreat are biologically possible. The player may then choose between costly salvage and conserving capacity, without an exact forecast. They cannot order a larger Leaf, restore elapsed time or choose a route that the Tuber cannot support (AMO-Q119).

## What remains open

AMO-Q084 owns replacement overlap, repeated attempts, species scope and interpretation of the Emergence loop. AMO-Q101 owns functional-collapse and funding eligibility, route selection and autonomous policy. AMO-Q106/AMO-Q110 own how persistent development and species interpretation shape primary or replacement manifestation scale; AMO-Q116 owns opportunity and productivity integration. AMO-Q087 owns retreat triggers and costs; AMO-Q119 owns how astral presence is established and what prognosis a player may have; AMO-Q120 owns whether route authorship is ever recorded ([26_PLANT_AUTONOMY_ASTRAL_LEVERAGE_AND_ROUTING_V0.md](26_PLANT_AUTONOMY_ASTRAL_LEVERAGE_AND_ROUTING_V0.md)). AMO-Q085/AMO-Q112/AMO-Q115 own magical access during replacement; AMO-Q109 owns any playable consequences. No rate, size ratio, cost, biological threshold, player command or combat stat is defined here.
