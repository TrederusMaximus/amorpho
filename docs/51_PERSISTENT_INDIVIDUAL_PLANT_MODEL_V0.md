# 51 — Persistent Individual Plant Model, v0

**Status:** consolidation and specification pass using owner-supplied design direction. It gathers what one persistent Amorpho individual *is* — currently spread across [03](03_PLANTS_INDIVIDUALS_LINEAGES.md), docs 14–47 and [50](50_WARDEN_BIOLOGICAL_INFORMATION_AND_ROSTER_JUDGEMENT_MODEL_V0.md) — into one conceptual inventory. It is **semantic domain architecture, not a schema**: no fields, identifiers, classes, tables, events, serialization, storage, APIs, stats, input columns, psychology or technology.

> **Bodies change; the individual persists** (L41).

## 1. Purpose

Every recent pass has leaned on *the persistent individual* — its Tuber, its history, its Anchor, its Warden's knowledge of it — without one place saying what that individual consists of across its whole existence. This document is that place. It adds two clarifying decisions and changes no biological rule.

## 2. The persistent individual

> **The persistent Amorpho individual is the Tuber-centred biological individual that continues across temporary manifestations, lifecycle phases and Warden interactions** (AMO-D058, AMO-D030, AMO-D095).

- A Leaf is not the individual. A Bloom is not the individual. A combat body is not a separate individual: the animated Amorpho is the same manifestation, rooted or inhabited (AMO-D134, L24).
- **Identity is independent** of current manifestation, location, lifecycle phase, Warden, custodian and combat state. Manifestations change; the individual remains, and its identity is never reused (AMO-D011, L12).
- **It begins biologically, not at first embodiment.** The Tuber exists, so the individual exists. Neither a Warden connection nor an Astral Anchor creates it; the game relationship attaches to an already-existing organism, and every new individual begins unbound (AMO-D064).

No technical identifier is defined here.

## 3. Species, genetics and lineage

| | |
|---|---|
| **Species** | the real species identity, from approved input, with its species-level constraints and tendencies (AMO-D004, AMO-D022, AMO-D147) |
| **Individual** | one specific organism with its own history, condition, lifecycle, manifestations, lineage position and Warden relationships |

Two individuals of the same species are not interchangeable.

The individual carries its **genetic identity**, parentage and lineage where known or generated, **hybrid identity** where it is one of an approved pair, and inherited traits ([03](03_PLANTS_INDIVIDUALS_LINEAGES.md) §1, §8, AMO-D027). These persist across manifestations: **a new Leaf receives no new genetics**, and no manifestation has its own hybrid status.

**Ordinary life never changes species or genotype.** Damage, embodiment, dormancy, cultivation and combat do not rewrite them, and there is no individual magical mutation. Growth, maturity, condition, depletion, pathology, recovery and lifecycle history are **individual biology, not evolution**; generational change belongs to the Evolutionator (AMO-D012, AMO-D038, AMO-D039).

**Phenotype, carefully.** Two layers, with no variables defined:

- **persistent expression potential** — longer-lived characteristics arising from genetics, development and persistent condition;
- **current manifestation expression** — how this cycle's Leaf or Bloom actually developed.

> **A manifestation expresses the individual; it does not redefine the individual's genetic identity.**

## 4. Persistent biological state

The individual carries — never as one health value (AMO-D056, AMO-D150):

- **Current Biological Condition** ([14](14_CURRENT_BIOLOGICAL_CONDITION_V0.md));
- **persistent capacity and provisioning** — strong, moderately depleted, or severely but non-pathologically depleted, persisting until biology changes it; depletion is not injury (AMO-D148);
- **Developmental Maturity** — persists through Leaf end, Bloom end and dormancy, and each new Emergence begins from the same individual's maturity ([19](19_DEVELOPMENTAL_MATURITY_V0.md), AMO-D080);
- **Pathological Tuber Impact**, if any — a new Leaf, a new Bloom and dormancy are not cures; any future repair acts on the persistent individual (AMO-D149, AMO-Q105);
- **persistent developmental consequences** of its biological history.

**Core Viability is derived, not held.** Whether the individual could continue if its current manifestation were lost is a judgement on persistent state at a moment — not a trait, not species identity, and changeable with history (AMO-D131, AMO-D151).

**Productive Return is how the individual develops through time**: temporary Leaf → rooted work → persistent return → changed Tuber, and the realized result remains when the Leaf ends ([39](39_ACTIVE_LEAF_PRODUCTIVE_RETURN_AND_PERSISTENT_TUBER_BENEFIT_V0.md), AMO-D137).

## 5. Lifecycle state and history

**Current lifecycle position belongs to the individual** — active phase, Dormancy Approach, Dormancy Commitment, Senescence, the Tuber-only transition, Deep Dormancy, developing Reactivation Readiness, Reactivation Commitment, Pre-Emergence, Emergence — within the existing topology, with no new state ([17](17_LIFE_CYCLE_STATE_MACHINE_V0.md), [46](46_DORMANCY_COMMITMENT_BOUNDARY_V0.md), [47](47_DEEP_DORMANCY_DURATION_AND_ACTIVE_PHASE_REACTIVATION_BOUNDARY_V0.md)).

**Lifecycle history belongs to the individual** too: previous active phases and dormancies, Blooms, Replacement Leaves, early or late transitions, recoveries, manifestation destruction, rescue, core exposure, productive seasons.

> **History belongs to the individual even when the body that created part of it no longer exists.**

**Missed opportunity becomes history, never a property.** Unused opportunity is not banked (AMO-D145, AMO-D152). That an individual spent a season embodied, or had a poor one, matters historically only because it produced the persistent state that followed. There are no *missed-opportunity points*.

## 6. Temporary manifestations

At any time the individual may have no manifestation, a developing Leaf, a mature Leaf, a Replacement Leaf, a Bloom, or another future valid manifestation. **The manifestation belongs to the individual and is not the individual.**

A manifestation owns temporary state: architecture, Structural Integrity, Functional Capacity, Recovery Ceiling, scars, current damage, terminal yellowing, manifestation-specific wear ([23](23_ACUTE_EVENT_TO_LEAF_IMPAIRMENT_V0.md), [40](40_ROOTED_MATURE_LEAF_RECOVERY_CEILING_AND_COMPENSATORY_REMODELING_V0.md), [33](33_MATURE_LEAF_FUNCTIONAL_COLLAPSE_BOUNDARY_V0.md)). **When it ends, those structures end.** They do not transfer physically to the next Leaf or Bloom (AMO-D074).

> **A new Leaf is a new temporary biological construction of the same persistent individual** — not a respawned old Leaf, not a new individual, and not a physical continuation of the old Leaf's scars.

**Rooted and embodied are one manifestation body**, with damage continuous in both directions and no rooted/fighter copy (AMO-D134).

**Playability is not identity.** The current playable body is derived from current biology — which manifestation exists, its condition, its damage, its lifecycle and embodiment availability — and the Warden can never select a timeless fighter version of the individual. The individual is fully real with **no playable body** in Deep Dormancy, Pre-Emergence, Emergence before Full Deployment, and as a Tuber exposed after destruction (AMO-D099, AMO-D107). *Individual exists* is not *fighter available*.

## 7. Location, custody and ownership

**Location belongs to the actual individual.** During embodiment the Tuber travels inside the manifestation as its central core; rooting establishes the individual where it stands; after destruction the surviving Tuber lies where the body fell; nothing teleports ([37](37_MANIFESTATION_DESTRUCTION_TUBER_CORE_VIABILITY_AND_PHYSICAL_DROP_V0.md), AMO-D129, AMO-D130). Location is current state and world history, never identity: no country, region, greenhouse or home rewrites what the individual is (AMO-D013).

**Custody is a world relationship.** Holding, carrying, transporting or rooting a Tuber establishes physical custody. It changes no biological identity, genetics, lineage, Warden relationship or Anchor authorization. **Custody is not ownership**, and both remain separate from anchoring and availability (AMO-D065, L43). Legal and game ownership are not solved here (AMO-Q007, AMO-Q093).

**Provenance is history, not power.** Wild, cultivated or lineage origin may be recorded; none maps to combat power or rarity advantage (AMO-D162).

## 8. Astral Anchor and binding

The Anchor is physically associated with the persistent Tuber core, travels with the individual, persists across manifestations, supports the Warden–Amorpho connection, and may remain as an object if the individual is lost (AMO-D061, AMO-D132). **The Anchor is not the individual.**

Two things are distinct:

- **Biological identity** — the plant itself, which exists independent of who is bound to it;
- **Astral binding** — which Warden currently holds a valid astral relationship with it.

Rebinding is not solved (AMO-Q091).

## 9. Warden–individual relationships and Attunement

**Attunement belongs to a relationship**, not to the individual alone, the Anchor object, custody or species (AMO-D167, AMO-D169). Over a long life an individual may take part in more than one relationship:

```
Warden A ↔ Individual X     its own Attunement history
Warden B ↔ Individual X     a different relationship, if ever validly established
```

Warden A's Attunement never passes to Warden B. **Attunement is not a biological trait stored in the Tuber**; keeping it in the relationship is what lets theft, rebinding, separation and reunion each mean something.

**It survives manifestation turnover**: Leaf A → dormancy → Leaf B leaves the relationship intact while the binding continues.

**Separation interrupts access without rewriting history.** A Warden may lose access to an individual without the relationship ever having not existed. How that history behaves after separation, and whether reconnection restores anything, is AMO-Q131.

**No psychology is designed.** Attunement is connection and understanding, not affection, trust, loyalty, fear or recognition. Whether an Amorpho misses, trusts or recognises a Warden is a separate future layer. A Warden can still feel attachment, grief, familiarity and reunion, because the individual is persistent and known — **emotional gameplay does not require anthropomorphic psychology**.

**Warden technique is not plant state.** Combat mastery belongs to the Warden and carries across bodies; whether any technique is individual-specific is AMO-Q027 (AMO-D163).

## 10. Provenance and history

**Current State** is what is biologically true now. **Historical Record** is what happened before. A past damage event need not remain current damage, and it may remain history — which is exactly the case of an old Leaf's scars (AMO-D168).

Provenance the model must be able to carry includes origin and acquisition, lineage, previous Wardens where allowed, major lifecycle events, Bloom history, manifestation loss, rescue, notable fights, ownership and custody events, and major recovery. **Which events are retained, and which are ever shown, is not decided** (AMO-Q120, AMO-Q012).

**History is not automatically visible.** Historical truth is not Warden knowledge: a stolen or rebound individual may carry a history its new Warden knows nothing of (AMO-D164). A long-term Warden recognises familiar patterns through relationship history and Attunement without any hidden log being exposed.

**History does not stack mechanically by default.** Every past battle as a permanent bonus, every old scar as a hidden stat — both rejected. History may matter to provenance, narrative, Warden knowledge, Attunement and future explicit systems. A Warden who knows an individual once tolerated a recovery well has better judgement, not `Recovery +5`.

**Combat history splits by owner.** *This Leaf's scars, this Bloom's damage, current protection, current Recovery Ceiling* are manifestation state. *Survived a major fight, lost a Leaf in combat, was rescued after core exposure, came through repeated seasons* are individual history.

## 11. Ownership matrix

Conceptual ownership only — not an implementation schema.

| Domain | Persists across manifestations? | Example |
|---|---|---|
| Biological identity | Yes | the same individual |
| Species, genetics, lineage, hybrid identity | Yes | inherited identity; a new Leaf gets no new genetics |
| Persistent expression potential | Yes, changing only through individual biology | what this individual tends to express |
| Developmental Maturity | Yes | persistent development |
| Condition, capacity, depletion, pathology | Yes | a depleted or harmed Tuber stays so until biology changes it |
| Core Viability | Derived from persistent state | could it continue without this body now? |
| Lifecycle position and history | Yes | prior dormancies, Blooms, Replacements |
| Productive Return outcome | Yes | the changed persistent state |
| Location | Yes — with the core | where it was rooted, carried or fell |
| Custody, ownership | Yes, as separate world relationships | changeable without changing identity |
| Astral Anchor association | Yes, subject to future binding rules | the physical Anchor on the core |
| Astral binding | Relationship-specific | who is validly bound now |
| Warden–individual Attunement | Relationship-specific | survives manifestation turnover |
| Current manifestation expression | No | how this Leaf developed |
| Leaf or Bloom architecture, Structural Integrity | No | ends with the manifestation |
| Scars, current damage | No physically | may persist as history |
| Functional Capacity, Recovery Ceiling | Manifestation-specific | this Leaf only |
| Combat protection state | Manifestation- or equipment-specific | current use |
| Warden combat mastery | Belongs to the Warden | not plant state |

## 12. Theft, separation and reunion

**Theft makes no new individual.** A thief acquires custody of the **same** persistent individual; its genetics, lineage, biological history, previous manifestations and previous Warden relationship history do not reset (AMO-D065).

**Rebinding never erases provenance.** If a valid new binding is ever formed, a new relationship may begin and the individual's earlier history remains. Authority rules are AMO-Q091.

**Reunion stays possible.** The model retains enough identity and history that a Warden who meets a separated individual again meets **the same individual**, not an equivalent replacement (AMO-D169).

**Personal irreplaceability is intended.** Two biologically similar Amorphos need not be equivalent to a Warden, because persistent history and Attunement make individuals personally distinct — with no stat attached. Any future market value assigned to an individual **cannot capture its relationship value to a Warden**; no economy is designed (AMO-Q007).

The model does not assume multiple Wardens and does not break if *Warden A → separation → Warden B → later reunion with A* happens: each relationship stays distinguishable.

## 13. Losing a body versus losing the individual

**Losing a manifestation is not losing the individual while a viable Tuber survives.** The manifestation's state ends; identity, persistent state, history and relationships continue; a future Leaf may emerge and the same relationship may continue. No fighter respawned.

**Losing the persistent Tuber ends living biological continuity.** With no viable Tuber, the individual is lost: no future manifestation can legitimately be that individual, and nothing recreates it — **no resurrection from an Anchor**, and its identity is never reused (AMO-D131, AMO-D011). The physical Anchor may remain as an object and transmits nothing living (AMO-D132, AMO-D166). Its history may remain as record. Any residue of a lost relationship is AMO-Q131 and AMO-Q091.

**Persistent identity is the basis of emotional continuity.** Loss, rescue, theft, reunion and recovery mean something only because the individual is stable; without that, every one of them collapses into inventory replacement.

**One open edge is recorded rather than decided.** Vegetative propagation produces new individuals linked to their parent ([03](03_PLANTS_INDIVIDUALS_LINEAGES.md) §5). If a Tuber is ever divided, which piece continues the original individual — and how its history, Anchor and relationships follow — is not defined; it belongs with propagation depth under AMO-Q012.

## 14. Worked identity traces

**Continuity.**
```
TUBER INDIVIDUAL X
  → Leaf 1 → damage, recovery, Productive Return → Leaf 1 ends
  → Deep Dormancy → Tuber X remains
  → Leaf 2 → the Warden recognises the same individual through identity, Anchor, history and Attunement
  → Leaf 2 ends → Bloom → still Individual X
```

**Theft.** Warden A has a long relationship with X. Custody is lost to another actor. X remains biologically X, with its persistent state and history. A's Attunement is not transferred as property. A later Warden B relationship, if ever validly established, is distinct. Binding legality is not solved.

**Reunion.** X is separated from A; time and lifecycle continue; X goes through further manifestations elsewhere; X is eventually recovered by or returned to A. It is the same persistent individual, and the architecture lets the earlier relationship matter. How reconnection behaves is AMO-Q131.

**Manifestation loss.** A Leaf is destroyed and the Tuber survives. The manifestation's state ends; identity persists; a later Leaf emerges; the same relationship may continue. No respawn occurred.

**Individual loss.** A manifestation is destroyed and no viable Tuber survives. Biological continuity ends; the Anchor may remain; provenance remains recordable; no future manifestation is this living individual. **This is true biological loss.**

## 15. Acceptance and consistency audit

| Test | Result |
|---|---|
| **A — new Leaf** | Same individual. |
| **B — scars** | Gone physically; may remain as history. |
| **C — maturity** | Persists. |
| **D — pathology** | Persists. |
| **E — dormancy** | Identity persists with no playable body. |
| **F — Bloom** | Same individual. |
| **G — embodiment** | The mobile fighter is the same individual, not a copy. |
| **H — theft** | Custody changes; identity and history do not. |
| **I — rebinding** | A different relationship rewrites no biological history. |
| **J — Attunement** | Relationship-specific; not transferred by pickup. |
| **K — reunion** | A previous Warden can meet the same individual again. |
| **L — Tuber survives** | The individual persists. |
| **M — Tuber lost** | The living individual ends. |
| **N — Anchor** | May survive the individual; is not the individual. |

| Distinction | Holds |
|---|---|
| Species ≠ individual; manifestation ≠ individual; Anchor ≠ individual | §2, §3, §8 |
| Custody ≠ ownership ≠ binding ≠ Attunement | §7–§9 |
| Attunement ≠ biological trait | §9 |
| Current scars ≠ persistent scars; historical damage may persist as history | §6, §10 |
| New Leaf = new architecture of the same individual | §6 |
| Loss of body ≠ loss of individual, unless the persistent core is lost | §13 |

## 16. Deferred implementation

Identifier design, record structure, event model, persistence and serialization are deliberately not addressed; nothing here authorises a schema (AMO-D020, AMO-D021). AMO-Q120 keeps which history is retained and authorship; AMO-Q012 simulation depth, propagation and Tuber division; AMO-Q044 and AMO-Q111 what is visible; AMO-Q131 relationship history, separation and reunion; AMO-Q091 binding and rebinding; AMO-Q007, AMO-Q008 and AMO-Q093 ownership, theft and custody; AMO-Q105 persistent repair. No new question was required.

**Result:** one Tuber-centred life, carrying its kind, its genes, its development, its scars as memory rather than tissue, its place in the world and the relationships formed with it — through every body it grows and every body it loses, until the Tuber itself is gone.
