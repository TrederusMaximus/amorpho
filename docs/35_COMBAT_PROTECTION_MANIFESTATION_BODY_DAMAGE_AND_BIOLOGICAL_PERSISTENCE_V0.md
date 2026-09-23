# 35 — Combat Protection, Manifestation Body Damage and Biological Persistence, v0

**Status:** conceptual architecture pass using owner-supplied design direction. It resolves the boundary that [34](34_EMBODIMENT_ACROSS_TERMINAL_MANIFESTATION_COLLAPSE_V0.md) deliberately deferred: what damage during embodiment means for the biological manifestation. It defines no combat system, HP value, damage or armour formula, shield capacity, KO or round rule, move, hit location, item, recovery rate, biological damage threshold, balance figure or implementation.

> **The Warden fights through the actual living manifestation. Protection may stop the blow; a body that is struck cannot ignore it.**

## 1. Purpose

AMO-D119 recorded that the mapping from astral-state damage to biological persistence was undecided, and forbade both silent defaults. This pass decides it, on a simpler ontological basis than the abstract "rare carryover" idea it replaces: **the inhabited Amorpho is not a projection of the plant — it is the plant's current manifestation, animated.** Damage that actually reaches that body is therefore biological damage, with no second conversion step. What remains distinct is the **combat state** the fighting game runs on, and what sits between an attack and the body is **protection**.

## 2. Embodiment ontology

The animated Amorpho uses the actual biological Leaf or Bloom as its body (AMO-D030, L16, L24, [09](09_EMBODIMENT_AND_ASTRAL_TRANSFER.md)). It is not a hologram, a disposable duplicate, a magical clone or an unrelated combat avatar, and no architecture may introduce risk-free combat copies of a plant. One consciousness inhabits one body at a time (AMO-D028, L22).

This is precisely why combat can have persistent biological consequence: there is no separate fighter object to absorb it. The plant you raised is the fighter you play, and it is also the thing that gets hurt.

## 3. The four layers

| Layer | What it holds | Status here |
|---|---|---|
| **A — Combat / astral state** | the embodied Amorpho's current capability inside active fighting: future combat vitality, guard, stagger, magical stability, combat energy and similar | named only; **nothing defined** (AMO-Q109, AMO-Q112) |
| **B — Protection** | whatever sits between a hostile effect and the body: magical shields, wards, armour, worn protection, blocking, parrying, evasion, positioning, defensive abilities | architectural role only; **no mechanics** |
| **C — Biological manifestation body** | the actual Leaf, Replacement Leaf or Bloom, with **Structural Integrity**, **Leaf Functional Capacity**, scarring, stabilization, recovery, Functional Collapse ([23](23_ACUTE_EVENT_TO_LEAF_IMPAIRMENT_V0.md), [24](24_SAME_PHASE_LEAF_RECOVERY_V0.md), [33](33_MATURE_LEAF_FUNCTIONAL_COLLAPSE_BOUNDARY_V0.md)) | damage here is **biological** |
| **D — Persistent Tuber** | the persistent biological individual: identity, condition, reserves, Developmental Maturity, history | reached only downstream, never directly by combat |

Layers A and C are **distinct but coupled**. Layer B is the reason that separation can exist in practice. Layer D keeps the ordinary manifestation-first rule (AMO-D079, AMO-D111, L55).

## 4. Combat state is not biological condition

> **Combat state answers “can this Amorpho continue this fight?”. Biological state answers “what condition is this Leaf or Bloom actually in?”.**

Neither is a view of the other, and no proportional translation exists in either direction. Depleted combat capability does not mean an equivalently damaged Leaf, and combat-state exhaustion is not a dead plant. Magical state was never a view of leaf integrity or Tuber vitality (AMO-D084, L49), and biological state is not a combat meter.

Separation is not independence:

- **Body → combat.** Real damage to the manifestation may reasonably reduce what the embodied form can do or sustain. How is combat design and stays open (AMO-Q109).
- **Combat → body only through the body.** Astral exhaustion, guard failure or a future combat-state defeat can occur with little or no biological damage, which is exactly what keeps the layers distinct.
- **Recovery domains stay apart.** Future restoration of combat state repairs no scars, structure or function; biological stabilization says nothing about how combat resources return (AMO-D086, L48).

One event may legitimately touch several layers at once — reducing combat capability, depleting a shield, damaging armour and injuring the body — without those effects being the same quantity. How anything distributes is future combat design.

## 5. The protection boundary

```text
INCOMING COMBAT OR HOSTILE EFFECT
        ↓
COMBAT / DEFENSIVE RESPONSE          movement, timing, guard, ability, positioning
        ↓
PROTECTION INTERCEPTION              shield, ward, armour, worn protection
        ↓
RESIDUAL EFFECT
   ├── does not reach the body  → combat-state and protection consequences only
   └── reaches the body         → REAL BIOLOGICAL MANIFESTATION DAMAGE
                                     ↓
                                 existing mature biology: stabilization, recovery or decline
                                     ↓
                                 possible Functional Collapse
                                     ↓
                                 possible downstream Tuber consequence
```

Three outcomes are all canonical: **fully intercepted** (combat or protection consequence, biology intact), **partially intercepted** (some effect reaches the body, biological damage occurs), and **unprotected** (the body takes it directly). No absorption value, capacity, recharge, durability figure or hit-determination rule is defined, and protection may itself be depleted or damaged — recorded only as extensibility.

Magical shielding and physical armour are both permitted as future first-class protection types, as are skilful blocking, parrying, evasion and positioning. The consequence worth stating now is a design connection rather than a mechanic:

> **Player skill and good equipment protect a living manifestation, not just a win condition.** Defending an Amorpho is part of plant stewardship.

Existing equipment rules are unchanged: worn protection helps the **animated** body and does not become rooted-plant environmental protection when the individual roots ([09](09_EMBODIMENT_AND_ASTRAL_TRANSFER.md) §17, AMO-Q048). *Animated traversal capability and rooted survival capability remain different things.*

Two product requirements pull against each other deliberately, and future balance owes both:

| Requirement | Failure mode it prevents |
|---|---|
| Serious fighting must risk the manifestation | protection so effective that the biological connection becomes decorative |
| Regular skilled fighting must remain viable | combat that ruins a manifestation every time, making participation irrational |

## 6. Manifestation body damage

When an effect reaches the body, the biological manifestation changes **then**, not on de-embodiment. The Warden continues fighting through an already-damaged body. De-embodiment therefore **reveals continuity rather than creating persistence**: nothing is converted or applied late, because embodiment never created a second temporary body.

Such damage enters the **existing** mature pathway. There is no combat-specific biological damage model: an effect reaching the Leaf produces changed Structural Integrity and Leaf Functional Capacity exactly as any other injury does, and is assessed with the same separations ([23](23_ACUTE_EVENT_TO_LEAF_IMPAIRMENT_V0.md), AMO-D091, L51). Appearance still decides nothing, and structural loss is not a percentage of function.

Not defined here, and deliberately left open: how an effect is judged to reach the body at all, what magnitude of biological damage follows, any hit location or body-zone model, and what physically destroys a manifestation outright (AMO-Q026, AMO-Q086, AMO-Q109). No plant anatomy is asserted or researched (AMO-D024).

## 7. Biological pause is not biological invulnerability

This is the distinction the pass turns on:

| During embodiment | |
|---|---|
| **Ordinary biological progression** | **suspended** — no growth, productive development, maturity gain, reproduction, life-cycle progression, Programmed Tuber Draw or biological recovery (AMO-D084, L49) |
| **Explicit injury to the body** | a **state change**, not progression — it can still occur, and it changes the manifestation's biological condition immediately |

So embodiment neither ages the body nor shields it. Because recovery is part of what is paused, damage taken across a long embodiment **accumulates** with no rooted stabilization between encounters. That produces real pressure against careless overuse without any stamina bar, cooldown or artificial timer.

## 8. Accumulated use, and overuse

> **Overuse is repeated exposure of the same biological manifestation to combat risk without sufficient biological recovery.**

It is a description of a situation, not a new variable: no Overuse meter, counter or threshold is created. It emerges from accumulated biological damage plus deferred recovery, and it is legible in the manifestation's own condition.

## 9. Withdrawal, rooting and rehabilitation

A player does **not** have to wait for Functional Collapse, or for a combat meter to empty, before stopping. A manifestation may be scarred, reduced and still perfectly capable, and withdrawing it is a legitimate and often sensible move:

```text
still-viable but damaged Leaf → Warden exits → rooted biological life resumes
   → stabilization, scarring, functional recovery where biology permits ([24](24_SAME_PHASE_LEAF_RECOVERY_V0.md))
   → the active phase may still be completed successfully
```

Rooting is rehabilitation through **ordinary** biology. No combat-recovery system, infirmary or repair abstraction is introduced; conditions matter through Environmental Fit exactly as they always do ([12](12_ENVIRONMENT_AND_FIT_MODEL_V0.md), AMO-D033, L27). Rooting is not a reset either: existing damage remains and recovery starts from the actual condition (AMO-D072, L50).

Mature architecture still does not regrow into its pristine form (AMO-D094). Combat scars can therefore matter for the rest of that manifestation's life, while stabilization and compensation may restore useful function ([32](32_IMPERFECTLY_DEPLOYED_MATURE_LEAF_STABILIZATION_OR_DECLINE_V0.md)).

The opposite choice is equally valid. A Warden may keep fighting a valued manifestation and spend it — accepting scars, reduced capacity, Functional Collapse or the loss of that Leaf. The game permits the risk and passes no judgement on it.

How an encounter actually ends — surrender, escape, conscious withdrawal or objective resolution, with destruction reachable only by refusing those exits — is specified in [36](36_COMBAT_RESOLUTION_SURRENDER_ESCAPE_AND_WITHDRAWAL_V0.md) (AMO-D124–AMO-D127). Ending the encounter does not by itself end the embodiment or root the plant (AMO-D126).

## 10. Collapse and terminal interaction

Accumulated body damage may push a Leaf across the existing boundary: impairment, loss of active-role viability, **Functional Collapse**, **Collapse Commitment**, terminal period, end of the manifestation ([33](33_MATURE_LEAF_FUNCTIONAL_COLLAPSE_BOUNDARY_V0.md), AMO-D114, AMO-D115). There is no separate “combat collapse”: the criterion is biological and unchanged, and routing afterwards is the same Tuber-level routing as any other collapse ([25](25_TUBER_FUNDED_MANIFESTATION_AND_REPLACEMENT_ROUTING_V0.md), [26](26_PLANT_AUTONOMY_ASTRAL_LEVERAGE_AND_ROUTING_V0.md)).

Terminal embodiment is unchanged: a committed terminal manifestation may be inhabited, its ordinary terminal progression stays suspended while embodiment continues, and no timer may be introduced to end it (AMO-D117, [34](34_EMBODIMENT_ACROSS_TERMINAL_MANIFESTATION_COLLAPSE_V0.md)). The new rule resolves what that pass left ambiguous:

> A terminal body is still a real body. Explicit injury can damage it and can **destroy** it, even while ordinary terminal progression is paused — because destruction is a state change, not senescence running its course.

If the manifestation is destroyed, it ceases to exist, and embodiment ends with it (AMO-D118, L57). The persistent Tuber remains unless separately harmed.

Two further separations hold. **Combat defeat is not body destruction:** a future combat-state failure may end an encounter or force de-embodiment while the manifestation survives. And **body damage may become catastrophic before any combat meter says so**, because biological consequence follows what happened to the body, not the abstraction. No defeat, KO or destruction rule is defined (AMO-Q026, AMO-Q113).

## 11. Seasonal renewal

Losing a manifestation is not losing the individual. If the damaged Leaf's life ends — through Collapse, retreat or the ordinary course of the season — the Tuber persists, and a later Emergence builds a **new** Leaf with newly constructed architecture that does not inherit the old one's physical scars (AMO-D074, AMO-D113).

That is renewal, not respawn: it costs biological time and requires the lifecycle to get there ([29](29_REPLACEMENT_EMERGENCE_TO_ASTRAL_READINESS_V0.md), AMO-D109). And the persistent individual keeps its history, so the next manifestation may differ because the **Tuber** has changed through growth, maturity, condition, prior success or persistent harm, and later lineage systems where they apply (AMO-D080, AMO-D095, AMO-Q116). Retiring a valuable Amorpho before catastrophic damage may therefore preserve or improve its future potential. None of this is experience points, and no progression or stat-inheritance rule is defined.

## 12. Roster and risk management

Because the body is a living individual, a collection becomes a risk-management problem rather than a bench of interchangeable fighters. A Warden may choose which individual to expose, which to root and rest, which to hold for particular conditions, and which body suits a challenge — and the reason to rotate is **biological condition, not an availability clock**. A manifestation may be perfectly usable and still be worth resting.

Nothing here prohibits future game systems, but biology should supply the primary systemic reason to rotate valuable Amorphos. One Consciousness still limits direct control to one body (AMO-D028, AMO-D101, L22, L53); other plants continue under ordinary world biology, and only the inhabited manifestation's progression is suspended (AMO-D009, AMO-D084). No party, squad, selection interface or simultaneous control is created.

Because the manifestation is one body throughout, **damage is physically continuous** across the boundary: scars present before entry are present while embodied, and damage taken while embodied remains visible once rooted. No rendering, visual or interface behaviour is designed. Biological history may later be recorded as individual history — major injuries, recovery episodes, collapse events, successful seasons after damage — without any storage schema here (AMO-Q120). Scars carry history, never a strength rating in either direction (L51).

## 13. The Tuber boundary

A Leaf hit is not a Tuber hit; a Bloom hit is not a Tuber hit. Combat **must never** use Tuber condition, reserves or vitality as a hidden combat life pool: the Tuber is persistent context, not the fighter's health bar (AMO-D084, AMO-D111, L55). Manifestation damage reaches persistent state only through the established pathways — lost function, lost opportunity, condition, and the Pathological Tuber Impact boundary ([21](21_PATHOLOGICAL_TUBER_IMPACT_V0.md), AMO-D079, AMO-D090–AMO-D092, AMO-Q116, AMO-Q118). Direct harmful exposure to the Tuber itself remains a separate route (AMO-D090).

The dependence runs the other way as biology: a strong or weak Tuber shaped which manifestation exists, its starting condition and its recovery potential (AMO-D095, AMO-Q110). That is biological influence, not a combat statistic.

## 14. Leaf, Replacement Leaf and Bloom

The body-damage law is generic to inhabited manifestations. A fully deployed **Replacement Leaf** is a mature manifestation and uses exactly these rules — protection can shield it, damage reaching it is biological, and accumulated damage persists — which makes risking one strategically expensive because it already represents scarce Tuber investment (AMO-D096, AMO-D111). No special replacement damage law exists.

For **Bloom**, damage reaching the inhabited Bloom body is real Bloom biological damage on the same basis. Bloom's mature biology is less developed, and nothing about its consequences, recovery or reproductive effects is invented here; Programmed Tuber Draw remains normal spending rather than harm (AMO-D087, AMO-Q088, AMO-Q086). Leaf and Bloom may later differ in what body damage costs them, because they serve different biological roles.

## 15. Worked traces

**A — fully protected hit.** A healthy mature Leaf is inhabited. An attack arrives and protection intercepts it. Combat state and the protection itself may change; the manifestation body is not reached, and no new biological damage occurs. The fight continues.

**B — partial penetration.** Protection absorbs part of an effect and the residual reaches the Leaf. Combat state is affected **and** the biological Leaf takes real damage: Structural Integrity and Leaf Functional Capacity may change. That damage is already part of the manifestation and remains after embodiment ends.

**C — accumulation and overuse.** The Leaf begins healthy and is used across many encounters. Several body-reaching effects accumulate biological damage, and no rooted recovery occurs because progression stays suspended. The Leaf remains combat-capable. The player chooses whether to keep risking it; nothing forces the decision.

**D — responsible withdrawal.** A scarred, somewhat impaired but viable Leaf is voluntarily withdrawn. The individual roots in favourable conditions, ordinary biology resumes, stabilization and functional recovery proceed where biology permits, and the Leaf completes its season. No Replacement was needed. **Canonical desired outcome.**

**E — overuse into Collapse.** Body damage repeats while embodiment continues, so mature recovery never runs. Condition worsens until the Leaf loses active-role viability; Collapse Commitment follows and its fate is fixed. The Warden may still inhabit it, and terminal progression stays paused until biological life resumes (AMO-D117).

**F — terminal fighter preserved.** A terminally committed Leaf is held through continuous embodiment. Terminal progression remains paused indefinitely and the body remains usable while it exists and the gates permit. The player accepts the opportunity cost: the single presence is committed and the individual's lifecycle waits. No anti-exploit timer is added.

**G — terminal body destroyed.** The same terminal Leaf is inhabited when a hostile effect overcomes protection and physically destroys the manifestation. This is explicit injury, not senescence: the manifestation ceases to exist despite paused progression, embodiment ends (AMO-D118), and the Tuber remains if not separately harmed. **This resolves the earlier ambiguity.**

**H — combat-state defeat, Leaf survives.** A well-protected Leaf reaches a future combat-state failure condition with little or manageable biological damage. The encounter or embodiment may end under future combat rules; the Leaf survives, and rooted biology resumes from its actual condition. No biological destruction is implied.

**I — new season, fresh body.** A combat-used Leaf completes its lifecycle and is lost. The Tuber persists through dormancy, later Emergence produces a new Leaf, and Full Deployment gives the Warden a fresh manifestation body. The new Leaf carries no old scars; the individual carries all of its history.

## 16. Deferred combat implementation and acceptance

Everything in Layer A remains to be designed. AMO-Q026 owns what combat does to the individual, including combat-state semantics, defeat, forced de-embodiment, the conditions under which an effect reaches or destroys a body, and safe or training contexts. AMO-Q109 owns how biological condition changes a playable Amorpho and how protection architecture, shields, armour and hit determination work. AMO-Q112 and AMO-Q113 own Astral Readiness and forced exit; AMO-Q086 owns the biological response to a body-reaching effect; AMO-Q048 owns equipment on rooting; AMO-Q051 keeps traversal, rooting and long-term tolerance separate; AMO-Q116 and AMO-Q118 own productivity and persistent loss; AMO-Q088 owns Bloom's content; AMO-Q120 may record combat history. No new question is required.

| Check | Result |
|---|---|
| Shielded hit | Protection may stop an effect entirely; combat consequence without biological damage. |
| Body hit | An effect reaching the body is biological manifestation damage, immediately (AMO-D120). |
| Separate meters | Combat state implies no equivalent biological damage, and vice versa (AMO-D121). |
| Coupling | Body damage may reduce combat capability and persists after exit. |
| Withdrawal | A damaged but viable manifestation may be withdrawn and rehabilitated through ordinary biology. |
| Overuse | Damage accumulates while recovery is suspended; no meter, cooldown or timer is added. |
| Collapse | Combat-caused damage uses the existing Collapse boundary and routing, with no combat-specific path. |
| Terminal embodiment | Unchanged: progression paused, indefinite embodiment permitted (AMO-D117). |
| Explicit destruction | Can end a manifestation while progression is paused; embodiment ends with it (AMO-D123, AMO-D118). |
| Combat defeat | May end an encounter while the manifestation survives. |
| Tuber | No automatic Tuber debit and never a hidden combat health pool (AMO-D111, L55). |
| New season | A later Leaf is fresh architecture of the **same** individual, not a new individual or a respawn. |
| Bloom and Replacement | Same body-damage law; downstream biology may differ. |
| Same body | Scars persist across entry and exit; the fighter and the plant are one body. |

**Result:** the fighting game and the plant game are one system. Cultivation determines what body exists, protection and skill determine what reaches it, combat determines what it risks, and post-combat care determines how much of its biological season can still be salvaged. Combat meters answer whether the fight can continue; the manifestation answers what it cost.
