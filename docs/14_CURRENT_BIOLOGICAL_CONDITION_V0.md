# 14 — Current Biological Condition, Model v0

**Status:** specification, version 0. This document answers one question: what biological state must a persistent individual carry between Environmental Fit evaluations so that stress, recovery, growth, survival and inhabitability make coherent sense over time. It defines no values, units, rates, thresholds or formulas, and contains no botanical facts.

It companions [12_ENVIRONMENT_AND_FIT_MODEL_V0.md](12_ENVIRONMENT_AND_FIT_MODEL_V0.md), which governs the Fit boundary, and is tested against the worked cases in [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md).

> Give each persistent individual enough biological memory for the World to matter over time — and no more than that.

## 1. Where condition sits

An individual carries several kinds of state that persist for different reasons and must not be merged (a fifth, **developmental maturity**, was added later — see [18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)):

```
INDIVIDUAL
├── persistent identity      species, permanent ID, provenance, lineage, ownership
├── inherited traits         heritable and otherwise persistent individual variation
├── current biological condition    ← this document
└── developmental state             ← this document, deliberately separate (§7)
```

Identity answers *who is this*. Traits answer *what is this individual like*. Condition answers **what biological state is it in right now**. Development answers **what biological phase is it in**.

All four feed the effective response profile that Environmental Fit evaluates (AMO-D048, AMO-D056, AMO-D057).

## 2. The loop this state exists to serve

Condition is not a species property. It belongs to the persistent individual, and it is what makes the environment matter over time:

```
CURRENT CONDITION(t) + DEVELOPMENTAL STATE(t)
        + inherited traits + species baseline
                     ▼
        EFFECTIVE RESPONSE PROFILE
                     +
        LOCAL ENVIRONMENT(t)
                     ▼
          ENVIRONMENTAL FIT over Δt
                     ▼
              biological effects
                     ▼
        CURRENT CONDITION(t + Δt)
```

**This is not circular.** Condition is read at `t` and written at `t + Δt`: a feedback loop across time, not a definition in terms of itself (AMO-D056). No tick rate, interval or equation is implied (AMO-Q074).

Without persistent condition, every evaluation would start from nothing, and nothing in the accepted architecture would work: no accumulation, no recovery, no rescue window, no thriving.

## 3. Why one variable is not enough

Before adding variables, the null hypothesis was tested: could a single `health` scalar carry everything?

**It fails Scenario C.** In phase 2 the individual has fully recovered and favourable Fit must still have somewhere meaningful to go (L38, AMO-D054) — a single health value has already saturated at "healthy", so positive Fit would have nothing left to act on and output D would necessarily fall to zero. The spec explicitly forbids that.

It also collapses distinctions the worked scenarios depend on: a healthy but depleted individual versus a healthy and well-provisioned one; a plant under pressure that is not yet harmed versus one that is; two individuals of equal health with different capacity to survive the next shock.

Simplicity is not worth incoherence. At minimum, condition needs something that **saturates** at healthy and something that **keeps accruing**.

## 4. Current Biological Condition v0

Three variables. Each earns its place by doing work no other one does.

### 4.1 Vitality — biological integrity

**Definition.** How biologically sound and viable the individual is at present.

**Why it exists.** It is the variable that survival and inhabitability hang on. Something must carry "this individual is compromised" in a form that is *not* a recoverable buffer, because a buffer refills and the fact that an individual nearly died should not always vanish with it.

**Modified by.** Sustained stress that exceeds what reserves absorb; recovery under favourable Fit.

**Influences.** Inhabitability (§6), the conceptual path toward non-viability (§8), and the effective response profile — a compromised individual tolerates less (§9).

**Does not represent.** Growth progress · stress history · reserves · developmental stage · genetic quality · size · value. Vitality is not a general score and must not become one.

> **Settled 2026-09-21.** This section previously flagged vitality as possibly derivable, on the reasoning that only irreversible damage would require storing it. That reasoning is withdrawn — no harm is permanent while the individual lives (AMO-D075) — and the conclusion stands for a stronger reason. Two individuals with identical stress and identical reserves may still differ in remaining core compromise, recovery need and proximity to losing inhabitability, and **no function of the other two can distinguish them** once both have recovered. Vitality is stored state (AMO-D076, [18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)).

### 4.2 Stress Load — accumulated burden

**Definition.** Accumulated biological burden from adverse conditions. **History, not damage.**

**Why it exists.** It is what gives the individual memory of *exposure duration*. This is what makes Scenario A work: a hostile site does not compromise a healthy plant instantly, so the individual arrives inhabitable, accumulates burden, and only later crosses the threshold. Without it, the gap between "conditions are bad" and "this plant is in trouble" would not exist, and the rescue window would have nothing to emerge from.

It also discharges the accumulation half of exposure history: a separate exposure store is not needed at this depth, because stress load carries it (AMO-Q072).

**Modified by.** Negative Fit, which raises it; favourable Fit, which relieves it. Relief is not assumed to be symmetric with accumulation — one favourable moment need not erase prolonged prior exposure.

**Influences.** Vitality, once burden exceeds what reserves absorb; resilience to further pressure; plausibly inhabitability (AMO-Q042).

**Does not represent.** Damage itself · permanent harm · the environment's badness (that is Fit's output C, a *pressure*; stress load is the *accumulated total*, spec §9) · any identity or inherited property of the individual.

### 4.3 Reserves — biological reserves

**Definition.** Abstract internal capacity an individual can draw on and rebuild.

**Why it exists.** It is the buffer that explains why a well-provisioned individual withstands a bad spell that would harm a depleted one, and it is the non-saturating sink that positive Fit needs after recovery completes. Excellent conditions supporting **resource accumulation** is already accepted architecture (AMO-D054, spec §11); this is where that accumulation lives.

It is also what makes strategic establishment pay off beyond "not dying": time in a good place builds something real.

**Modified by.** Drawn down by adverse conditions and by the work of growth and development; rebuilt under favourable Fit.

**Influences.** Resilience to short adverse periods; the capacity to recover; the capacity to advance development.

**Does not represent.** Energy in any physiological sense · carbohydrate, water or nutrient pools · a currency · a general-purpose meter for future systems. It is deliberately one abstract quantity, and it must not become the place every unmodelled thing is quietly stored.

### 4.4 Why not fewer

| | Distinct job | Fails without it |
|---|---|---|
| **Vitality** | carries compromise in a form a buffer cannot | inhabitability and death have nothing to hang on |
| **Stress Load** | remembers exposure duration | Scenario A's delayed onset; the rescue window |
| **Reserves** | buffers, and receives positive Fit after recovery | Scenario C phase 2; differential resilience at equal health |

Stress load and reserves are **not** mirror images of one sign: reserves are also spent on growth, so under excellent Fit reserves may fall while stress is zero. Merging them would make flourishing indistinguishable from suffering.

### 4.5 Why not more

Deliberately excluded: hydration · carbohydrate state · membrane damage · leaf, root or organ damage · metabolic pools · hormone state · nutrient status · separate injury tracking.

Each is real biology and none does a job the accepted architecture needs. Adding them would be simulation design ahead of any system that consumes them (AMO-D047's discipline, applied to the Amorpho side).

## 5. Developmental State — a separate axis

**Developmental State sits beside Current Condition, not inside it** (AMO-D057).

**Definition.** What biological phase the individual is in.

Three arguments decided this, and the third is the strongest:

1. **They are orthogonal.** Healthy and dormant, healthy and actively growing, stressed and actively growing, healthy and reproductive are all coherent combinations. Which are legal is not decided here.
2. **Condition is evaluative; development is not.** Condition has a good/bad axis. Development does not: a seedling is not in worse condition than a mature plant, it is at a different point. Folding development into condition would make "more developed" read as "better", and a large unhealthy plant would score well — exactly the confusion the *surviving is not thriving* law exists to prevent (L38, L40).
3. **They shape the response profile differently.** Condition degrades the profile: a compromised individual tolerates less of everything. Development changes *which* sensitivities apply at all — a dormant individual and an actively growing one do not merely differ in degree. That is a categorical influence, not a degradational one, and categorical and degradational influences do not belong in the same variable.

**The phases now have a topology.** Seven states in three families, specified in [17_LIFE_CYCLE_STATE_MACHINE_V0.md](17_LIFE_CYCLE_STATE_MACHINE_V0.md) (AMO-D070). Condition carries something the graph deliberately does not: a season that ended early and expensively and one that completed well traverse the **same** transition, and the difference lives entirely in reserves, stress and development (AMO-D070). That is why no "successful season" flag exists.

**Maturity is specified separately.** Developmental Maturity is one continuous, species-relative axis of persistent development (AMO-D080, [19_DEVELOPMENTAL_MATURITY_V0.md](19_DEVELOPMENTAL_MATURITY_V0.md)), and it is not a condition variable. The sharpest consequence for this document: **vitality recovery does not restore lost maturity** — an individual may heal completely and still be developmentally a fraction of what it was, rebuildable only through successful biological life (AMO-D083, L48).

**Phases are now named.** Developmental state has v0 content — tuber/dormant, emergence, leaf, bloom, senescence — and it determines which body is expressed and whether that phase permits astral entry at all (AMO-D059, AMO-D063, [15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md)).

A second integrity concept may eventually sit beside condition: **phase-specific integrity**, bounded by the current manifestation, as distinct from the persistent core vitality defined here. Damage there reaches these three variables only once it crosses the **Core-Impact Threshold** — below it the current body is impaired while stress, reserves and vitality stay broadly untouched (AMO-D079, [18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)). Leaf damage may persist for a phase without being permanent for the individual; when the phase ends, its structure and whatever damage it carried cease to exist (AMO-D058, AMO-Q086). Whether that lives in condition, in developmental state, or beside both is open (AMO-Q073).

**The state machine is deferred.** Dormant, active growth, flowering, reproductive and any other phases are not designed here, and no botanical facts about any species' life cycle are assumed or imported (AMO-D024, AMO-Q012). This document settles only *where such state belongs*.

> **Condition says how the individual is doing. Development says what phase it is in.** (L40)

## 6. Inhabitability

Inhabitability is **derived, never stored as independent truth** (AMO-D050). It is not a fourth condition variable and must not become one.

```
CURRENT CONDITION → future astral-entry rules → INHABITABLE / NOT
```

v0 says only that it reads condition — principally **vitality**, plausibly also **stress load**. The rule, the threshold, and whether it is a binary gate or a continuous quality all remain open (AMO-Q042).

This is what makes `alive ≠ inhabitable` work: an individual whose vitality has fallen below the entry threshold but not to non-viability is alive, present in the world, and unreachable astrally (AMO-D031).

## 7. Death

Not designed here. What v0 preserves is the **path**:

```
viable → deteriorating → critical → non-viable
```

Whether death is a vitality threshold, a terminal developmental state, or something at the intersection of both is open, as is whether it is ever instantaneous (AMO-Q045).

## 8. Recovery, and what comes after it

The model supports the full sequence without claiming all harm is reversible:

| Phase | What changes |
|---|---|
| under adverse Fit | stress accumulates; reserves draw down; vitality falls once they are exhausted |
| under favourable Fit | stress relieves; reserves rebuild; vitality recovers **where it can** |
| once recovered | stress at rest, vitality at baseline — and **reserves and development continue to receive positive Fit** |

That last row is the point. Recovery completing does not exhaust what a good environment can do (L38, AMO-D054), and it is why output D does not fall to zero when condition returns to baseline (spec §9).

Whether any vitality loss is permanent is deliberately unanswered (AMO-Q045).

## 9. Condition feeds back into the response

Two individuals sharing species baseline, inherited traits and environment may still diverge, because condition is one of the layers forming the effective response profile (AMO-D048).

A depleted, burdened individual has a narrower usable profile than a sound one, so the same conditions press harder on it — which makes decline accelerate, and, run forward, makes recovery firm up as it proceeds. This is the feedback already demonstrated in Scenario A §3.9 and Scenario D §21.

The function is not defined (AMO-Q073).

## 10. What condition is *not* connected to

- **Not inherited.** A stressed parent does not produce genetically stressed offspring. The Evolutionator works from inherited traits, never from condition (AMO-D038, AMO-D039, L32). Condition may eventually influence *whether* and *how successfully* an individual reproduces; that mechanism is not designed (AMO-Q079).
- **Not taxonomic.** Condition is live world state belonging to an individual (AMO-D021, layer 3). It never appears in approved input, and no condition field is added to the species CSV (AMO-D053).
- **Not lost when animated.** The rooted plant and the animated Amorpho are one persistent individual (AMO-D030), so condition persists across the transition. Whether animation *costs* anything — reserves spent, stress added — is open (AMO-Q083).
- **Not closed to combat.** Whether combat consumes reserves, adds stress or harms vitality is not decided (AMO-Q026). v0 deliberately leaves each of those possible without asserting any.

## 11. Tested against the worked scenarios

| Scenario | What the model has to explain | How |
|---|---|---|
| **A — deteriorating** | delayed onset, then loss of inhabitability while alive | stress accumulates and reserves draw down first; vitality falls only once they are exceeded, crossing the entry threshold before non-viability |
| **A §3.9 — stressed arrival** | same site, worse outcome | depleted reserves and existing burden narrow the effective profile and remove the buffer |
| **B — equilibrium** | indefinite stability under mild chronic pressure | low stress accrual is offset by relief; reserves hold; vitality untouched; modest opportunity goes to reserves and slow development |
| **C — recovery** | improvement from a stressed start | stress relieves, reserves rebuild, vitality returns toward baseline |
| **C — thriving** | positive Fit still matters after recovery | reserves keep accumulating and development advances; neither saturates at "healthy" |
| **D — interaction** | prior condition changes the response to identical pressure | condition narrows the effective profile, so the same combination can be tolerable for one individual and critical for another |
| **development ≠ health** | a healthy seedling and an unhealthy mature plant | separate axes; neither implies the other |
| **traits ≠ condition** | cold tolerance versus being cold-stressed | different layers, different persistence, different owners |

All eight cases in the consistency audit are explicable with three condition variables and one developmental axis. No case required a fourth condition variable, and no case was left unexplained.

## 12. Open questions

Dynamics and thresholds (AMO-Q073) · vitality recovery dynamics (AMO-Q102) · inhabitability rule and threshold (AMO-Q042) · the death condition (AMO-Q104) · developmental maturity (AMO-Q106) · exposure history beyond a single accumulated value (AMO-Q072) · the developmental state machine and acclimation (AMO-Q012) · what a rooted individual does over time (AMO-Q077) · animated-form effects on condition (AMO-Q083) · combat consequences (AMO-Q026) · condition's influence on reproduction (AMO-Q079) · simulation time step (AMO-Q074).
