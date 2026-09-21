# 18 — Phase Damage, Core Recovery and Bloom Maturity, v0

**Status:** specification, version 0. This document settles how biological harm works across the layers already established, and adds the developmental rule that gates Bloom. It defines no values, thresholds, formulas, damage sources or species facts, and it does not design treatment, combat or reproduction.

It resolves the policy half of AMO-Q045 and builds on [14_CURRENT_BIOLOGICAL_CONDITION_V0.md](14_CURRENT_BIOLOGICAL_CONDITION_V0.md) and [17_LIFE_CYCLE_STATE_MACHINE_V0.md](17_LIFE_CYCLE_STATE_MACHINE_V0.md).

> Temporary manifestations can be damaged and replaced. The persistent individual carries the consequences across cycles.
> If the individual lives, recovery remains possible. Death is final.
> Bloom is reached through biological maturity, not unlocked by player points.

## 1. Harm is not one thing

The architecture already distinguishes the persistent individual, its developmental state, its current manifestation and its condition. Harm therefore cannot stay a single undifferentiated concept:

- a damaged leaf is not a damaged core;
- a damaged bloom structure is not a damaged core;
- a stressed individual is not structurally damaged;
- a depleted individual is not compromised.

Different harm operates over different horizons, and the horizon is what matters (AMO-D074).

## 2. Three harm horizons

| | **A. Temporary manifestation damage** | **B. Persistent core damage** | **C. Reversible burden** |
|---|---|---|---|
| What | structural harm to the currently expressed body — leaf integrity, bloom structure | harm to what carries the individual across phases | stress load, depleted reserves |
| Horizon | bounded by the manifestation | spans phases, dormancy, new emergence | short to medium |
| Recorded in | phase-specific integrity (AMO-Q086) | **vitality** (AMO-D056) | stress load and reserves |
| Ends when | the manifestation ends | recovery completes | conditions improve |

**Persistent is not permanent.** Core damage may last across astral exit, senescence, dormancy, new emergence and the end of a bloom — and still be fully recoverable (§3).

**The horizons recover at different speeds, and the asymmetry is deliberate.** Reversible burden recovers substantially faster than severe core compromise: stress falls and reserves rebuild over favourable conditions, while deep vitality loss may need repeated healthy phases across multiple cycles. Without that gap, core damage would be indistinguishable from a bad week, and the severity ladder in §11 would collapse into a single rung. Actual rates are open (AMO-Q102).

### Crossing from manifestation to core

Harm does not move freely between the horizons, and the boundary between A and B is itself a design object (AMO-D079).

> **Manifestation damage affects the current manifestation first.** It must become deep enough in its biological consequences before it propagates into persistent state.

This boundary is called the **Core-Impact Threshold**. It is a *conceptual* boundary, not a number, and nothing about where it sits is defined (AMO-Q108).

**Below it — manifestation-only consequence.** The current leaf or bloom stays damaged, the inhabited Amorpho may be substantially impaired, some capabilities may be unavailable for that manifestation, and yet the manifestation may still complete its active period, persistent growth may continue broadly unaffected, developmental maturity need not regress, and the next manifestation emerges structurally whole.

> A difficult season can impair the current fighter without costing long-term biological progress.

**Above it — core-impact consequence.** Severity, or the biological stress that comes with it, becomes sufficient for persistent consequences to begin: reserve depletion, inadequate persistent growth, developmental maturity regression, premature senescence, a reduced next-cycle starting point, vitality compromise. All of it still recovers while the individual lives (AMO-D075).

**Visible damage does not determine the crossing by itself.** Two manifestations with similar apparent damage may have entirely different persistent consequences depending on current condition, reserves, Environmental Fit, developmental context, how long the impairment lasted and eventual species biology. A percentage of a structure lost is not a biological verdict, and nothing may treat it as one (AMO-Q108).

## 3. The recovery law

> **If the biological individual survives, all forms of biological damage are ultimately recoverable** (AMO-D075, L46).

The harm classes therefore differ in **severity, depth, cost, duration, how many life cycles recovery needs, how much favourable growth it requires, and what capability is lost meanwhile** — never in *recoverable versus permanent*.

This is a deliberate playability rule. Irreversible injury on a persistent individual a player may have cultivated for years converts a bad season into a permanent grievance, and the architecture already provides consequences severe enough without it (§6, §8).

### Only death is terminal

> Death is the only normal permanently terminal biological outcome (AMO-D075).

Death occurs when biological viability is lost. It is **not** dormancy, senescence, a phase transition, or severe stress by itself (AMO-D072). A dead individual does not recover, and no routine resurrection exists — any exception would need its own explicit decision. The exact death condition is open (AMO-Q104).

Death does not erase history: provenance, lineage, offspring and world history all remain. The biological individual is gone; the record is not (AMO-D011). No memorial system is designed.

## 4. Leaf damage

During Active Leaf the current leaf may be damaged, which may eventually reduce function, impair abilities in inhabited leaf form, reduce growth opportunity and reserve accumulation, raise stress, or contribute to early retreat. None of that is designed (AMO-Q086).

The rule that matters: **a damaged current leaf does not by itself mean serious core damage.**

### Recovery of the individual is not repair of the structure

These are separate, and conflating them is the easy mistake:

| | |
|---|---|
| **Biological recovery of the individual** | stress falls, reserves rebuild, vitality returns — driven by Environmental Fit |
| **Repair of the current manifestation** | a physically damaged leaf does not become structurally whole because conditions improved |

Some impairment may simply last until the leaf is abandoned. How much in-phase repair is possible at all is open (AMO-Q103).

### A new leaf is a new structure

A later cycle's leaf **does not inherit** the previous leaf's physical damage (AMO-D074). The old structure is gone.

But the individual enters that cycle carrying everything else — reserves, stress load, vitality, developmental maturity, overall development. **Seasonal structural renewal without erasing biological history.**

### Damaged seasons are graded, not binary

Moderate leaf damage need not destroy the active season. The individual may remain functional, complete the phase, accumulate some reserves, hold or even increase developmental maturity, and enter dormancy normally.

Leaf damage therefore does **not** automatically imply premature retreat, maturity loss, core damage or a failed season (AMO-D079). A damaged leaf may still provide enough biological function to carry a successful cycle. How structural impairment translates into biological productivity at all is open (AMO-Q108).

Nothing in the model produces a binary *healthy season / failed season*, and nothing should (AMO-D070).

## 5. Premature retreat

Severe stress or severe manifestation compromise may force early retreat:

```
ACTIVE LEAF → serious compromise → SENESCENCE → EARLY DORMANCY → DEEP DORMANCY
```

This is **not death**. It is a biological survival response — the same Senescence transition arriving early, with the difference carried in condition rather than in the graph (AMO-D070).

### The cost can be severe without being permanent

Premature retreat may cost remaining growth opportunity, reserve replenishment, existing reserves, developmental gain, **accumulated developmental maturity**, a weaker next emergence, delayed Bloom eligibility and a long recovery.

> The individual may survive while losing substantial progress (AMO-D075, AMO-D077).

A severe failed season can leave the persistent individual with fewer resources and less developmental mass, so the **next manifestation may begin from a reduced position** — smaller, less capable, further from its former development, further from flowering. No size relationship is defined (AMO-Q106).

## 6. The three condition variables under harm

### Reserves bridge the phases
Successful active periods replenish and build reserves, funding future emergence, development and eventually Bloom. Poor periods leave low reserves and reduced resilience. Reserves always recover (AMO-D056).

### Stress load remains reversible burden
> Stress is history, not damage.

It accumulates under adverse conditions and falls under favourable ones. It never becomes permanent, never becomes identity, and is **never inherited** (AMO-D039). It may contribute to lost inhabitability, premature retreat, reduced performance and greater vulnerability.

### Vitality carries core compromise
**Vitality is the current long-horizon biological integrity and viability of the persistent individual** (AMO-D076). It is distinct from phase integrity, stress load, reserves, developmental maturity, size, age and genotype.

Vitality reduction may be shallow and quickly recovered, substantial and slow, or extremely severe and need multiple life cycles — but **while the individual is alive, vitality can return to full integrity.**

Core damage remains one of the most serious setbacks available. Its seriousness comes from **recovery depth and duration**, not from irreversible loss.

## 7. Vitality is stored state

[14](14_CURRENT_BIOLOGICAL_CONDITION_V0.md) flagged vitality as the variable most likely to prove derivable, on the reasoning that a derived summary could not carry irreversible damage. **That reasoning is now superseded — and the conclusion is unchanged**, for a better reason (AMO-D076).

Two individuals may have identical stress and identical reserves and still not be equivalent:

| | Stress | Reserves | Vitality |
|---|---|---|---|
| Individual A | low | high | full |
| Individual B | low | high | reduced after earlier severe core trauma |

B needs recovery that A does not, is closer to losing inhabitability, and responds differently to further pressure. **No function of stress and reserves can distinguish them**, because both have already recovered. Vitality must therefore be stored, and this argument does not depend on permanence at all.

### No second core variable

A separate stored `Core Integrity` beside vitality is **not** added. It would do no distinct work: *core damage* is the causal event, and *vitality* is the persistent state outcome it produces.

```
core damage  →  reduces vitality        ✓
core integrity meter + vitality meter   ✗
```

Two meters that always move together is exactly the redundancy the condition model already rejected (AMO-D056).

### Dormancy does not reset vitality

Entering Deep Dormancy does not automatically restore anything. A severely compromised individual may remain compromised straight through dormancy and into the next emergence.

> Life-cycle transition does not erase persistent condition.

Whether dormancy itself ever *assists* recovery is deliberately open, and would depend on future biology and design (AMO-Q102).

### Excellent conditions enable deep recovery

Favourable Environmental Fit supports stress reduction, reserve rebuilding, vitality restoration, growth and renewed development (AMO-D049). For severe core damage this may require long-term establishment, repeated healthy phases and multiple cycles — which is precisely what makes **strategic establishment** matter (AMO-D054). No timing is defined (AMO-Q102).

## 8. Developmental Maturity

A further persistent dimension, distinct from everything already defined (AMO-D077). *Developmental Maturity* is a working name (AMO-Q106).

```
Life-Cycle State        → what phase is happening now
Vitality                → how biologically intact the individual is
Developmental Maturity  → how far the individual has developed across repeated cycles
```

**It can grow.** Sustained favourable conditions across successful cycles let an individual accumulate biological mass and development, so repeated good seasons make it progressively larger and more developed.

**It can regress.** Severe stress, premature retreat, major core damage or extreme reserve loss may cost part of previously accumulated maturity. The individual survives and may later rebuild — meaningful regression without permanent damage.

**It does not regress merely because a manifestation is damaged.** Regression requires meaningful consequence at the *persistent* level — crossing the Core-Impact Threshold (AMO-D079). `Leaf integrity loss` and `maturity loss` are different events, and equating them would make every torn leaf cost years of development (AMO-Q106).

**It is not experience points.** Maturity is biological development, not a combat currency, and it emerges from successful life cycles, favourable growth and biological condition rather than from activity (AMO-D077, L47).

The axis is now specified in [19_DEVELOPMENTAL_MATURITY_V0.md](19_DEVELOPMENTAL_MATURITY_V0.md) (AMO-D080–AMO-D083): one continuous, species-relative quantity; growth from persistent biological surplus rather than awarded by Fit; regression only on Core Impact, with **lost opportunity distinct from regression**; and **healing distinct from regrowth** — full vitality recovery does not restore lost development (L48).

## 9. Bloom requires flowering maturity

> **A biologically healthy individual is not automatically Bloom-capable** (AMO-D078).

Bloom requires the individual to have reached a **species-specific developmental threshold**:

```
current developmental maturity  ≥  species flowering-maturity threshold
        →  Bloom becomes biologically possible
```

No threshold is defined, researched or assumed, and no universal threshold exists — species may differ in flowering requirements, developmental scale and flowering tendency. If the game later needs those facts they arrive as approved input, once the model consuming them exists (AMO-D024, AMO-D025, AMO-D053, AMO-Q076). **Nothing is added to the species CSV.**

### The gate enables; it does not guarantee

Reaching the threshold means *this individual is mature enough that Bloom may occur* — not that Bloom happens. Actual Bloom may further depend on condition, reserves, life-cycle routing, environment and species biology. The trigger is not defined (AMO-Q107, AMO-Q101).

### Eligibility can be lost and regained

If a setback drops maturity below the flowering threshold, Bloom becomes unavailable **until maturity is rebuilt** (AMO-D077, AMO-D078). Real consequences from a failed season or core damage, with no permanent loss.

### First Bloom is not maximum Bloom

Reaching the minimum threshold is not full development. A newly Bloom-capable individual keeps growing across later successful cycles, so:

```
Bloom-capable  ≠  fully developed
```

### Bloom is repeatable, and may become more impressive

The architecture supports **repeated Bloom** after maturity — for species whose eventual biological model permits it, sustained favourable development may allow Bloom in repeated future cycles. Roughly annual recurrence is possible where future data supports it; it is **not** assumed universal, and no interval is defined (AMO-Q107).

As maturity grows beyond the minimum, later Bloom manifestations may become larger, more developed, more visually impressive and potentially more capable in Bloom-specific gameplay. No scaling rule is defined, and linear scaling is not assumed (AMO-Q088).

> Bloom expression may reflect the history and maturity of the individual.

A long-lived individual repeatedly given favourable Fit, low stress, strong reserves, good vitality and continued growth may produce progressively more developed Blooms over successive cycles. **This is one of the largest rewards available for long-term successful cultivation** — and it is why a setback that delays or shrinks a future Bloom is a real loss even though nothing is permanent (AMO-D054).

### Bloom is not a player unlock

There is no *Unlock Bloom* action bought with points. The living individual reaches eligibility by becoming sufficiently mature for its species (L47).

This is a central product distinction: the player creates the conditions, and the plant reaches the state.

### Everything else about Bloom is unchanged

Bloom remains short-lived, exceptional, highly discoverable, reproductively significant and capable of unique gameplay — never "Leaf with better stats" (AMO-D059, AMO-D071). Maturity governs eligibility and expression, not duration or permanence.

**Bloom manifestation damage is temporary**, exactly parallel to the leaf: damage may persist for that Bloom, the structure ends when the Bloom does, future Blooms begin fresh, and consequences carry through stress, reserves, vitality and maturity (AMO-D074).

The Core-Impact boundary applies identically. A damaged Bloom may lose Bloom-specific capabilities, lose reproductive opportunity and stay structurally compromised for that Bloom — **without** reducing persistent developmental maturity or vitality. Only consequences deep enough to cross the threshold propagate further (AMO-D079), so losing a Bloom is not the same as losing the eligibility to bloom again.

## 10. Harm and astral access

**Manifestation damage does not by itself block access.** A damaged leaf-form Amorpho may be alive, astrally accessible and impaired — a meaningful injured state rather than a lockout (AMO-D063).

**Severe vitality reduction may close access.** An individual may be alive but not inhabitable, and as vitality recovers inhabitability may return. No threshold is defined (AMO-D050, AMO-Q042).

**Playable recovery precedes full restoration.** A deeply damaged individual need not regain its former size or maturity before becoming usable again:

```
critical core damage → not inhabitable → favourable recovery → biologically stable
   → astral access returns → developmental rebuilding continues far longer
```

These are two different recoveries on two different timescales, and separating them is what keeps a severe setback from becoming an indefinite exclusion from play.

## 11. The severity ladder

What the model now supports, graded, without arbitrary permanent injury:

| Severity | What happened | Recovery |
|---|---|---|
| **Early rescue** | stress or reserve problem | relatively quick |
| **Manifestation crisis** | leaf or bloom badly compromised | current phase may be lost; structure renews next cycle |
| **Premature retreat** | survived, lost growth and development | rebuild over cycles |
| **Core crisis** | vitality falls; astral entry may close | long-term care, multiple cycles |
| **Fragment survival** | near-total biological setback | very long rebuild; identity unresolved (§12) |
| **Death** | viability lost | none |

Only the last is permanent. A poor rooting decision can lead anywhere on this ladder — stress, reserve loss, a damaged manifestation, premature dormancy, developmental regression, vitality loss, prolonged recovery, fragment-level survival, or death (AMO-D033).

The positive trajectory matters equally: strategic establishment in excellent conditions leads to low stress, strong reserves, full vitality, developmental growth, flowering maturity, repeated and increasingly developed Blooms, reproduction and long-term lineage success (AMO-D054).

## 12. Surviving fragments

If catastrophic core damage leaves viable biological material capable of regeneration, **living biological continuity never ended**, so the event is not necessarily equivalent to death.

Regeneration from a small fragment should be representable as an **enormous developmental setback**:

```
large mature individual → catastrophic core destruction → viable fragment survives
   → regeneration → very small developmental state → long rebuilding path
```

This is consistent with the recovery law: **recovery does not mean instant restoration of prior size.** Years of development can be lost without the individual being lost.

**Identity remains unresolved** (AMO-Q094). Whether the regenerated result is the *same persistent individual* — continuity never broke — or a *new clonal descendant* with provenance linking back, is deliberately not decided here. It affects Anchor continuity, ownership, combat history, lineage, the Warden relationship and player attachment. Whether the original Anchor remains valid after fragmentation depends on that answer and is equally open.

## 13. The architecture in one picture

```
PERSISTENT INDIVIDUAL
├── identity · lineage · genotype · provenance
├── PERSISTENT DEVELOPMENT
│     └── developmental maturity / biological size
├── CURRENT BIOLOGICAL CONDITION
│     ├── vitality        ← carries core compromise across phases
│     ├── stress load     ← reversible burden
│     └── reserves        ← reversible buffer
├── LIFE-CYCLE STATE
└── CURRENT MANIFESTATION
      └── phase-specific integrity where relevant
```

```
species baseline (future flowering-maturity requirement)
        +  developmental maturity  +  condition  +  reserves
        +  life-cycle routing      +  environment
                        ▼
              BLOOM ELIGIBILITY / OPPORTUNITY
```

Conceptual architecture, not an implementation schema.

## 14. Worked cases

Non-numeric, species-neutral, with no real biology.

| Case | What happens |
|---|---|
| **A — moderate leaf damage, successful season** | leaf damaged and the inhabited form impaired; damage stays **below the Core-Impact Threshold**; individual stays viable; season completes; maturity still increases somewhat; next cycle produces a structurally fresh leaf |
| **B — severe leaf damage, premature retreat** | stress rises, reserves spent, early retreat; **vitality largely intact**; maturity falls or gains far less than expected; next emergence smaller and weaker; full recovery still possible |
| **C — severe core damage** | vitality drops substantially; individual survives; damage **persists through dormancy and into next emergence**; long-term excellent care slowly restores vitality; maturity may have regressed significantly; full eventual recovery possible |
| **D — flowering maturity reached** | repeated successful cycles raise maturity past the species threshold; Bloom becomes **possible but not guaranteed**; further cycles keep raising maturity; later Blooms may be more developed |
| **E — mature individual suffers major setback** | maturity and reserves fall; Bloom **delayed or temporarily unavailable**; after sufficient recovery and growth, eligibility returns |
| **G — damaged Bloom** | Bloom-specific capabilities and reproductive opportunity lost for that Bloom; structure stays compromised until the Bloom ends; **no automatic core damage and no maturity regression**; eligibility to bloom again is untouched |
| **F — catastrophic damage, viable fragment** | no death declared while living continuity remains; maturity effectively collapses; long rebuild begins; **identity unresolved** (AMO-Q094) |

## 15. Open questions

The Core-Impact Threshold and how structural impairment becomes biological consequence (AMO-Q108) · how phase integrity alters a playable Amorpho's capabilities (AMO-Q109) · vitality recovery dynamics and whether dormancy assists (AMO-Q102) · manifestation repair within a phase (AMO-Q103) · the death condition (AMO-Q104) · treatment and care (AMO-Q105) · representation, growth and regression of developmental maturity (AMO-Q106) · Bloom eligibility inputs beyond maturity, and repeated-Bloom timing (AMO-Q107). Related: phase-specific integrity (AMO-Q086), premature retreat cost (AMO-Q087), Bloom content and manifestation scale (AMO-Q088), fragment identity and Anchor continuity (AMO-Q094), inhabitability threshold (AMO-Q042), condition dynamics (AMO-Q073), combat consequences (AMO-Q026), approved input for species thresholds (AMO-Q076).
