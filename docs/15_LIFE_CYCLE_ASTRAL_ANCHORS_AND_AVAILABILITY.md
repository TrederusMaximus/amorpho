# 15 — Life Cycle, Astral Anchors and Availability

**Status:** conceptual architecture. This document establishes how an individual's biological phase, its physical astral connection, and its playable availability relate. It designs no state machine, no damage system, no anchor economy and no combat kit, and it contains no botanical facts. Where something is undecided it points to [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).

> The individual persists; its biological manifestation changes.
> Deep dormancy closes the astral door.
> The soul may travel. The Anchor must move by human hands.

## 1. The persistent individual versus its current manifestation

A persistent Amorpho individual is **not identical to its current visible plant structure** (AMO-D058):

```
PERSISTENT AMORPHO INDIVIDUAL
          ▼
  developmental / life-cycle state
          ▼
  current biological manifestation
```

The same individual may exist at different times as a rooted tuber, an actively growing leaf-form plant, a flowering individual, or something transitional. Identity, lineage, genotype, provenance, ownership and history stay attached to the **individual** throughout (AMO-D011, AMO-D030).

Each phase is never a new individual. A plant that loses its leaf and later grows another has not become a second plant, any more than an inhabited Amorpho is a separate creature from the plant it is.

This has a direct consequence for harm, developed in §4 and §7: **damage to a temporary manifestation and damage to the persistent core have different consequence horizons.**

## 2. Developmental State becomes gameplay-relevant

The separation already accepted in [14_CURRENT_BIOLOGICAL_CONDITION_V0.md](14_CURRENT_BIOLOGICAL_CONDITION_V0.md) now carries real weight (AMO-D057):

| | Answers |
|---|---|
| **Developmental State** | *What biological phase and body is currently expressed?* |
| **Current Biological Condition** | *How well is the individual doing?* |

They remain orthogonal, and the combinations are all meaningful: a healthy dormant tuber, a damaged active leaf, a healthy flowering individual, a stressed emerging sprout. Collapsing them would make "dormant" read as "unwell", which it is not.

## 3. Life-cycle architecture v0

Five broad phases are recognised. This is **not** a finished state machine, and no species' real life cycle is assumed or imported (AMO-D024, AMO-Q084):

| Phase | What it is |
|---|---|
| **Tuber / Dormant** | the persistent underground or storage phase |
| **Emergence / Sprouting** | transition from tuber toward active above-ground growth |
| **Leaf** | the primary active vegetative phase |
| **Bloom / Flowering** | a short, exceptional reproductive phase |
| **Senescence / Dormancy entry** | transition from active form back toward dormancy |

Sequencing, overlap, duration, how far species differ, and whether leaf and bloom can coexist are all open (AMO-Q084).

## 4. Leaf Phase

The Leaf Phase is expected to be one of the major active embodiment forms, and its above-ground structure is **seasonally replaceable**.

Damage to the current leaf is therefore not destruction of the individual. It may reduce current performance, impair phase-specific abilities, reduce biological productivity during this growth period, raise stress, reduce reserve accumulation, and contribute to early dormancy — without the individual being permanently harmed.

### Persistent for the phase, not permanent for the individual

A damaged leaf may stay damaged for the rest of its active phase. It does not simply regrow because Environmental Fit improved: the structure is what it is until the phase ends.

When that leaf is naturally abandoned and a later cycle produces a new one, the new structure begins fresh.

> Damage may be **persistent for the current manifestation** without being **permanent for the persistent individual**.

This gives consequences a real horizon — a ruined season is a genuine loss — without making every injury existential. Combat consequences are not designed here (AMO-Q026, AMO-Q086).

## 5. Premature retreat into tuber state

Severe stress or severe loss of functional structure may eventually cause an individual to abandon the active phase early:

```
LEAF PHASE
  → severe stress / severe functional compromise
  → premature dormancy entry
  → above-ground structure abandoned
  → return toward tuber state
```

The cost may be substantial: reserves depleted, a resulting tuber smaller or weaker than after a successful season, developmental progress lost, and later re-emergence starting from a reduced state.

No trigger, threshold or magnitude is defined (AMO-Q087). What matters architecturally is that retreat is a **survivable failure with a lasting price**, distinct from both a minor setback and death.

## 6. Dormancy entry should be visible

Dormancy should not arrive as a surprise. The player should not simply be told *character unavailable* with no biological transition (AMO-Q085).

> Dormancy entry should normally give visible biological warning before astral availability closes.

Real senescence often shows as visible change, and that is the design inspiration — but it is **not** asserted as a universal fact about every species (AMO-D024). Possible future signals include visible senescence, weakening astral resonance, or status information. The presentation is open.

## 7. The tuber is closer to the persistent core

The Tuber Phase is not "Leaf Form without graphics". It represents the persistent biological core and storage structure of the individual.

Serious compromise of the core is therefore more consequential than ordinary seasonal leaf damage, and belongs to the long-horizon vitality model rather than to phase-specific structure (AMO-D056, §12). Tuber damage mechanics are not designed (AMO-Q086).

### Fragment survival is an identity question, not only a damage question

If catastrophic core damage leaves a viable surviving fragment, does regeneration continue **the same persistent individual**, or create a **new clonal descendant** linked by provenance?

This is deliberately undecided (AMO-Q094). It matters more than it first appears: identity is never reused (AMO-D011, AMO-D022), so the answer determines whether a lineage record can survive its own near-destruction. No botanical rule is encoded here.

## 8. Bloom Phase

Bloom is treated as **rare, short-lived and strategically important** — an extraordinary temporary state, not Leaf Form with better numbers.

A flowering individual may eventually have phase-specific abilities, a distinct interaction kit, unusual powers, reproductive opportunity and greatly increased discoverability. None of that is designed here (AMO-Q088).

### A superstate, not a strictly better state

> Bloom may function as a temporary biological superstate.

That does **not** mean stronger at everything, automatically superior in combat, or universally optimal. It should offer capabilities unavailable in other forms while carrying its own costs and risks — plausibly high reserve investment, a short window, high discoverability and reproductive consequence. Balance is not decided.

Bloom structure is also temporary, so the same architecture as the leaf applies: a bloom-specific integrity distinct from persistent core vitality may eventually be needed (§12, AMO-Q086).

### Bloom and discoverability

Flowering already makes a plant easier for others to find (AMO-D015, L11). For an anchored, valuable individual this becomes a sharp trade-off:

```
Bloom → strong discoverability signature → increased attention and risk
                                        → reproductive opportunity
```

No detection radius, marker or signal mechanism is chosen (AMO-Q015).

## 9. Rooted biological life continues without the player

A rooted, uninhabited individual is not inactive (AMO-D054). Depending on phase and on systems that do not exist yet, it may grow, recover, accumulate stress, build reserves, enter dormancy, emerge, flower, reproduce, participate in pollination and contribute to local populations.

The player's consciousness is not required for biological life. This is central to a persistent world (AMO-D009).

## 10. Astral accessibility varies across the life cycle

Astral accessibility is **not constant**. Developmental state may permit or prevent entry regardless of how healthy the individual is — which is a different gate from biological inhabitability (AMO-D063).

### Deep Dormancy closes the astral door

> A deeply dormant tuber is not astrally inhabitable (AMO-D060).

The Anchor may still be physically present. The relationship may still be recorded. Normal consciousness transfer simply cannot enter. This is **biological unavailability**, not loss of ownership and not loss of the Anchor.

### Transitional windows may exist

The whole tuber phase is not assumed equally closed (AMO-Q085):

| | Current design direction |
|---|---|
| shortly after dormancy entry | a limited transitional period may remain reachable |
| **deep dormancy** | **astrally inaccessible** |
| pre-emergence / pre-sprout | accessibility may begin returning before above-ground growth |

If those windows exist they may eventually create distinctive tuber and transition gameplay. The boundaries are not fixed.

### Deep dormant tubers are naturally hidden

> A deeply dormant, unexposed tuber is normally extremely difficult or impossible for others to discover unless its physical location is already known (AMO-D060).

No leaf, no flower, no scent signature, no movement, and below ground or buried in substrate. This is **concealment, not magical invisibility**: a player who knows the exact outdoor site, the pot or the greenhouse bed can still physically find it. What must not exist is a generic world signal that reveals dormant tubers.

### Dormancy is safety bought with unavailability

| Benefit | Cost |
|---|---|
| greatly reduced discoverability | no normal astral entry |
| natural protection through concealment | cannot be activated to solve an immediate problem |
| biological rest | physical human intervention may be needed if the location becomes threatened |

That trade is deliberate, and it reinforces human/Amorpho complementarity (L23): the safest state for a plant is the one in which the player can only reach it as a human.

## 11. Astral Anchors

An **Astral Anchor** is a physical, reusable magical object attached to an individual Amorpho. It provides the physical side of the astral access path (AMO-D061). The name is working terminology and the visual form is open (AMO-Q089).

### An individual does not need an Anchor to exist

Unanchored plants grow, enter dormancy, emerge, flower, reproduce, die, establish populations and participate in evolution exactly as anchored ones do.

> Astral anchoring is not biological ownership of existence. It enables human astral access, nothing more.

### Anchors belong to the individual, not the place

The Anchor is associated with the **persistent individual**, not with the pot, the property, the greenhouse or the location. If the plant is repotted, moved, animated or rooted elsewhere, the Anchor stays with it until physically removed. The physical attachment method is open (AMO-Q089).

### Anchors are reusable

A human may remove an Anchor from one individual and later attach it to another eligible one. Anchor count therefore becomes a strategic constraint.

Nothing about the economy is decided — starting count, maximum, rarity, price, crafting, acquisition, destructibility, grades, or whether Anchors can be stolen independently (AMO-Q090, AMO-Q091).

### Removing an Anchor releases access, not life

```
ANCHORED  →  human physically removes Anchor  →  UNBOUND  →  biological life continues
```

The plant remains the same individual: lineage, genotype, condition, developmental state and world history all remain. Only normal astral access through that Anchor ends. Release may be entirely intentional — a deliberate path from *playable character* to *unbound living individual*, with nothing deleted.

### Only the human may move an Anchor

> **Only the human player can physically attach, remove, transfer or reconfigure Astral Anchors** (AMO-D062).

An inhabited Amorpho cannot remove its own Anchor, move it to another individual, reconfigure the anchored roster, or attach Anchors remotely. No other Amorpho can do it on the player's behalf.

> The soul may travel. The Anchor must move by human hands. (L42)

This is deliberate. It means changing which individuals are playable always requires human-world action, which prevents the astral layer from quietly replacing the human layer (L23, AMO-D029).

### Anchors are not roster slots

Although Anchors are reusable resources, they are **physical world objects**, not invisible slots reassigned from a menu. A future interface may assist the process; the underlying event stays physical.

## 12. Phase-specific integrity versus persistent core

Not designed here, but the architecture is reserved (AMO-D058, AMO-Q086):

| | Horizon |
|---|---|
| **Persistent core integrity** — the vitality of [14](14_CURRENT_BIOLOGICAL_CONDITION_V0.md) | long; survives phase changes |
| **Phase-specific integrity** — leaf integrity, and possibly bloom integrity | bounded by the phase; ceases to exist when the manifestation does |

When a phase ends its temporary structure ceases to exist along with whatever damage it carried. Persistent core state remains. Variable names, magnitudes and mechanics are all undecided, and this pass deliberately **precedes** the resolution of lasting vitality damage, death thresholds and combat damage (AMO-Q045, AMO-Q026) — because what is temporary and what is core must be settled before deciding what can be lost permanently.

## 13. The Warden artifact and the access path

The personal magical artifact remains as previously established — an amulet, a belt, or another Warden object (AMO-D007, AMO-Q021). The clean architecture is:

```
HUMAN WARDEN ARTIFACT  ↔  ASTRAL ANCHOR ON INDIVIDUAL  ↔  BIOLOGICALLY ACCESSIBLE INDIVIDUAL
```

Astral entry occurs only when the whole path is valid. The artifact's form, lore, origin and any pairing ritual are open (AMO-Q021, AMO-Q089).

## 14. The three gates

Astral entry requires **all three** independently (AMO-D063):

```
          ASTRAL ANCHOR            is there a physical access path?
                 +
     LIFE-CYCLE ACCESSIBILITY      does this phase permit entry?
                 +
  BIOLOGICAL INHABITABILITY        is this individual well enough?
                 ▼
                ENTRY
```

Each can block on its own, and they are genuinely orthogonal:

| Situation | Result |
|---|---|
| active, healthy, **no Anchor** | biologically fine; no astral path |
| **anchored**, deep dormancy | path exists; phase closed |
| anchored, active, **critical stress** | path and phase fine; condition blocks (AMO-D050, AMO-D031) |
| anchored, active, healthy | potential entry |

### The Astral Radar is a view of connections

The player's astral interface shows the individuals connected through their own Anchor system — **not** every Amorpho on Earth (AMO-D061).

> The Astral Radar is a view of the player's astral connections, not a global botanical scanner.

It may eventually show anchored individuals, their availability, biological accessibility and perhaps broad condition or resonance. An anchored deep dormant tuber may remain listed as connected while being unreachable, and the information available during deep dormancy may be deliberately minimal. No interface is designed, and it is not automatically a positioning system (AMO-Q092).

## 15. Existence, ownership, custody, anchoring and availability

Five axes that may disagree, and must never be collapsed into a single `owner_id` (AMO-D065):

| Axis | Question |
|---|---|
| **Biological individual** | does this plant exist? — independent of everything else |
| **Ownership** | who, if anyone, has recognised ownership? |
| **Physical custody** | who physically controls the plant or its location? |
| **Astral anchoring** | whose astral system is physically connected through an Anchor? |
| **Astral availability** | do current biological and life-cycle conditions permit entry? |

### Unowned biological life is normal

A plant may be alive, unowned, unanchored and growing naturally. That is not an exceptional state — it is the **default** for wild populations, and it must remain possible indefinitely (AMO-D064). The game never assumes every plant belongs to a player.

### Every new individual begins unbound

> Every newly created biological individual begins without an Astral Anchor (AMO-D064).

Seedlings, germinated seeds, vegetative offspring, bulbils, other clonal propagation and hybrids all begin as their own unbound individuals. **Parent ownership and anchoring never propagate to offspring**, and Anchors are never required for reproduction or population persistence. Anchoring is a human fantasy-control layer laid over a biological world that does not need it (AMO-D038, AMO-D040).

### Theft and trade are physical

Because Anchors are physical objects, theft may involve the plant, the Anchor, or both. If an anchored individual is stolen together with its Anchor, the original player no longer physically controls that Anchor — a real world event, not a bookkeeping change. Physical possession is **not** assumed to grant the thief astral access; whether and how rebinding works is open (AMO-Q091, AMO-Q008).

Legitimate trade or gift may likewise involve the individual, ownership, custody, the Anchor and any pairing:

> Astral access cannot change merely because an ownership field changed.

The transaction protocol is not designed (AMO-Q093).

## 16. Availability, roster and emergent strategy

> **Ownership is not availability** (L43).

A player may own an individual that cannot currently be played, and may physically hold an unowned or unbound plant that is not playable at all. The playable roster is an **emergent subset** of the collection:

```
individuals that exist
  ∩ anchored individuals
  ∩ life-cycle accessible
  ∩ biologically inhabitable
  = currently playable roster
```

Owning a hundred plants does not produce a hundred playable characters — and the one-body law means only one of them is ever inhabited anyway (AMO-D028).

### Seasonal and geographic strategy, without hemisphere rules

Because the world is Earth and environments are time-dependent (AMO-D045, AMO-D046), different places support different life-cycle timing. Nothing hemisphere-specific is hard-coded; the outcome emerges:

```
Earth location + time/season + local environment + Amorpho biology → life-cycle response
```

Geographically distributed collections may therefore make different individuals playable at different times of year, and controlled cultivation may influence timing where biology allows — a greenhouse modifies the local environment and the individual responds through its biology, never a flag that overrides it (AMO-D035, AMO-Q049).

### What this generates

These are **illustrations of emergent play, not mechanics** (L37):

- an anchored individual approaching deep dormancy: leave the Anchor attached, or remove it and reassign it to something active?
- a valuable unanchored individual entering Bloom, with no free Anchor — reallocation requires physically travelling to both plants;
- maintaining collections across hemispheres, climates or greenhouses so that something is always playable;
- a deeply dormant tuber that is safe precisely because it cannot be reached or found.

None of these is a feature. Each falls out of the anchor rules, the life cycle and Earth's seasons acting together.

### The Human Layer becomes structurally necessary

Only the human can physically collect unbound plants, attach Anchors, remove them, redistribute a limited supply, perform any future pairing, and physically manage dormant individuals.

That is the point. The human layer must stay essential even when Amorpho embodiment becomes powerful (L23, AMO-D029).

## 17. Open questions

Life cycle: the state machine (AMO-Q084) · astral access windows (AMO-Q085) · phase-specific abilities and damage (AMO-Q086) · premature dormancy (AMO-Q087) · Bloom (AMO-Q088). Anchors: form, attachment and pairing (AMO-Q089) · economy (AMO-Q090) · transfer, theft and rebinding (AMO-Q091) · the Astral Radar (AMO-Q092). Ownership and wild state (AMO-Q093). Identity after severe core loss (AMO-Q094). Related: the artifact (AMO-Q021), discoverability (AMO-Q015), inhabitability (AMO-Q042), lasting damage and death (AMO-Q045), condition dynamics (AMO-Q073), combat consequences (AMO-Q026).
