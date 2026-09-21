# 17 — Life-Cycle State Machine, v0

**Status:** specification, version 0. This document defines the minimum durable life-cycle topology the accepted architecture needs: which manifestation exists, which transitions are possible, and where the astral door opens and closes. It is **species-neutral** and contains no botanical facts, no durations, no thresholds, no triggers, no abilities and no runtime representation.

It sits under [15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md), which established the concepts, and beside [14_CURRENT_BIOLOGICAL_CONDITION_V0.md](14_CURRENT_BIOLOGICAL_CONDITION_V0.md), which owns condition.

> The individual persists; the biological manifestation changes.
> Rooted does not mean dormant. Dormant does not mean dead. Astral exit is not dormancy.

## 1. Scope and non-claims

The state machine belongs to **one persistent individual** and describes only its developmental phase. It does not decide combat kits, pollination, core-damage mechanics, timings or species biology.

It makes **no claim** that every species spends equal time in a phase, follows identical timing, flowers between the same states, has the same dormancy depth, or exposes the same access windows. What follows is a **topology**, deliberately parameterisable, so that approved data and game rules can later shape it per species without changing its structure (AMO-D024, AMO-Q084).

## 2. Identity sits above the machine

```
PERSISTENT INDIVIDUAL
        ▼
DEVELOPMENTAL / LIFE-CYCLE STATE
        ▼
CURRENT BIOLOGICAL MANIFESTATION
```

A transition **never** creates a new individual, and never resets provenance, lineage, genotype, Anchor state, ownership or custody (AMO-D058, AMO-D011). Nor does it reset **Developmental Maturity**, which accumulates across cycles and is what makes one individual developmentally further along than another in the same phase (AMO-D080, [19_DEVELOPMENTAL_MATURITY_V0.md](19_DEVELOPMENTAL_MATURITY_V0.md)).

If a leaf is lost, the individual remains. If a Bloom ends, the individual remains. If the individual enters dormancy, the individual remains. This is obvious and worth writing down anyway, because future character, roster and interface systems must **never key identity to the current visual manifestation** (AMO-D070).

## 3. Three separate ideas

These are routinely confused and must not be:

| | What it is |
|---|---|
| **Life-cycle state** | the biological developmental phase |
| **Manifestation** | the temporary body or structure that currently exists |
| **Astral accessibility** | whether this phase permits normal astral entry |

They are related but not one-to-one, and v0 does not assume they always will be. Two states may share a manifestation kind; one state may change accessibility across its own span (§6).

## 4. Topology v0

Three families and seven states. Families group states that behave alike for access and manifestation; they are an organising device, not an extra layer of mechanics.

```
                     ┌──────────────── DORMANT FAMILY ────────────────┐
                     │                                                 │
                     │   EARLY DORMANCY ──▶ DEEP DORMANCY ──▶ PRE-EMERGENCE
                     │        ▲                                   │    │
                     └────────┼───────────────────────────────────┼────┘
                              │                                   ▼
                        SENESCENCE                           EMERGENCE
                              ▲                                   │
                     ┌────────┼───────── ACTIVE FAMILY ───────────┼────┐
                     │        │                                   ▼    │
                     │   ┌────┴──────────────────────────────────────┐ │
                     │   │   ACTIVE LEAF   ◀───────▶   BLOOM         │ │
                     │   └───────────────────────────────────────────┘ │
                     └─────────────────────────────────────────────────┘
```

| Family | States | Manifestation | Access |
|---|---|---|---|
| **Dormant** | Early Dormancy · Deep Dormancy · Pre-Emergence | storage / core structure | narrowing → **closed** → widening |
| **Transition in** | Emergence | forming | widening → open |
| **Active** | Active Leaf · Bloom | above-ground structure | **open** |
| **Transition out** | Senescence | receding | open → narrowing |

Entry into the Active family comes through Emergence; exit is through Senescence. Routing *within* the Active family, and which active state an individual first enters, is **parameterised** — see §5.

## 5. Bloom is a sibling active state

This was the one genuinely open structural question, and three candidate shapes were considered.

**Rejected — Bloom as a linear stage** (`Emergence → Leaf → Bloom → Senescence`). It forces every individual through Bloom every cycle, which contradicts Bloom being rare and exceptional (AMO-D059), and hard-codes a leaf-then-bloom ordering that cannot be assumed for all species.

**Rejected — Bloom as an overlay on Leaf.** An overlay cannot express an individual that blooms *without* an active leaf, because the overlay would have nothing to attach to. It also muddles manifestation: a bloom structure is its own temporary body, not a modifier on another one.

**Adopted — Bloom as a sibling active state** (AMO-D071). Leaf and Bloom are peers inside the Active family. Entry into the family, and movement between and out of its states, is parameterised rather than fixed:

```
EMERGENCE ──▶ ACTIVE LEAF ──▶ SENESCENCE
          └─▶ BLOOM      ──▶ SENESCENCE
              ▲     │
              └─────┘   routing between active states is parameterised
```

This buys exactly the extensibility the architecture needs:

- an individual may bloom, or may never bloom;
- an individual may enter the active family *as* Bloom, without a leaf first;
- post-Bloom routing is open — return to another active state, or proceed to Senescence (§19 of the brief's concern; AMO-Q084);
- a species that never blooms simply never enters that state, with no special case;
- Bloom keeps its own manifestation, so bloom-specific integrity and a bloom-specific kit can attach later (AMO-Q086).

v0 does **not** assume Leaf and Bloom can be occupied simultaneously. Because they are siblings in one family, a future model that needs concurrency can express it without restructuring; whether any species needs that is open (AMO-Q084).

## 6. Access status is a property, not a label per state

Astral accessibility takes three conceptual values (AMO-D070):

| | Meaning |
|---|---|
| **Open** | the phase permits normal astral entry |
| **Transitional** | entry may be possible, but access is changing as the transition proceeds |
| **Closed** | the phase does not permit normal astral entry |

Steady states hold one value. **Transitional states change value across their own span**, which is why access is derived from state *and progress through it* rather than stamped on the state:

| State | Access |
|---|---|
| Active Leaf | **Open** |
| Bloom | **Open** |
| Senescence | Open → narrowing → Transitional |
| Early Dormancy | Transitional → Closed |
| **Deep Dormancy** | **Closed** — hard rule (AMO-D060) |
| Pre-Emergence | Closed → Transitional |
| Emergence | Transitional → Open |

Exact opening and closing points are **not** fixed (AMO-Q085). What is fixed is the shape: access narrows on the way down and widens on the way up, with a genuinely closed floor.

A **second, independent curve** runs alongside it: the **Astral Signal**, which fades through Senescence, is absent in Deep Dormancy (*Astral Silence*) and returns in Pre-Emergence — potentially before inhabitability does. Detectable and enterable are different questions and need not move together (AMO-D088, [20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md](20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md)).

### Deep Dormancy is not tuber gameplay

Deep Dormancy exists precisely as a **biologically closed** state. It is not a "tuber fighter mode" with the graphics turned off. If tuber-form gameplay ever exists it belongs to the transitional windows — shortly after dormancy entry, or during pre-emergence — or to some other explicitly defined active tuber state, never to deep dormancy itself (AMO-D060, AMO-Q086).

## 7. The states

### Early Dormancy
The above-ground manifestation has recently been abandoned. Access is narrowing toward closed. This is where a post-dormancy transitional window would live if one exists.

### Deep Dormancy
The persistent core at rest. **Astrally closed** — the Anchor may remain attached, the individual is alive, ownership and custody are untouched, and entry is simply not possible (AMO-D060). Natural discoverability is at its minimum: no leaf, no flower, no signal, no movement.

### Pre-Emergence
The individual begins leaving deep dormancy. Current design direction is that **accessibility may begin returning before any above-ground manifestation exists**; the exact opening point is open (AMO-Q085).

### Emergence
The return toward active manifestation. The phase-specific body begins forming, access widens toward open, and biological vulnerability may differ from a fully established active phase. Where within Emergence access becomes fully open is open.

### Active Leaf
The primary sustained above-ground state, and the strongest candidate for default embodiment. Access is open subject to the other gates. Environmental Fit acts on condition, reserves and development here; sustained good Fit supports healthy growth, and severe compromise can end the phase early (§9).

**Leaf integrity is phase-specific.** Damage to the current leaf is not damage to the individual (AMO-D058). It may persist for the rest of the phase and does not regrow because conditions improved. A later cycle's leaf begins structurally fresh — but the *season's* consequences persist indirectly, through depleted reserves, accumulated stress, reduced development, possible core compromise, or an early retreat. **Nothing is erased; only the structure is replaced.** Nor does structural damage automatically reach the persistent individual: it does so only past the **Core-Impact Threshold**, so an impaired leaf can still carry a successful season (AMO-D079). No integrity variable is formally defined (AMO-Q086).

### Bloom
Bloom draws on persistent Tuber resources — **Programmed Tuber Draw**, normal biological spending rather than harm — and that draw is paused while the Bloom is astrally inhabited (AMO-D087, AMO-D084). *Leaf rebuilds; Bloom spends.*

Eligibility is gated: an individual must have reached its **species-specific flowering maturity** before Bloom is biologically possible at all, and reaching that threshold enables rather than guarantees it (AMO-D078, [18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)). Once eligible, Bloom is repeatable in later cycles, and later manifestations may be larger and more developed as maturity grows.

An exceptional, temporary, reproductive active state, and **astrally playable** — Deep Dormancy's closure does not reach it (AMO-D059, AMO-D071). It is extraordinary without being universally better: unique capabilities, real costs, a short window, elevated discoverability and reproductive significance. Nothing about its kit, cost or duration is designed (AMO-Q088).

Bloom is biologically consequential — plausibly drawing on reserves, developmental state and condition — and the state machine exposes `individual is in reproductive Bloom` so that future discoverability, pollination and reproduction systems can react without any of them being designed now (AMO-Q079, AMO-Q015).

### Senescence
The active manifestation recedes. This is a **real transition, not a disappearance**: access narrows rather than snapping shut, and the player should get a legible opportunity to react — reallocate an Anchor, relocate the individual, adjust plans (§10).

Visible senescence is a useful real-world-inspired **presentation direction**, not a universal biological claim about any species (AMO-D024).

## 8. One Senescence, two ways in

Premature retreat needs **no separate state**. Senescence is entered either on the ordinary course of a cycle or early under severe pressure:

```
ACTIVE LEAF ──(ordinary cycle)──▶ SENESCENCE ──▶ EARLY DORMANCY ──▶ DEEP DORMANCY
ACTIVE LEAF ──(severe stress /
               phase compromise)─▶ SENESCENCE ──▶ EARLY DORMANCY ──▶ DEEP DORMANCY
```

The difference is **not in the graph** — it is carried by condition, reserves and development (AMO-D056). A successful season ends with reserves built and development advanced; a failed one ends with reserves depleted, progress lost, and a weaker starting position for the next cycle.

This is deliberate. A "successful season" flag would duplicate what condition already records, and premature retreat is not a different *kind* of event — it is the same transition arriving early and expensively. It is a **survivable failure with a lasting price**, and it is not death (AMO-Q087, AMO-Q045).

## 9. What drives transitions — and what does not

Transition triggers are **abstract in v0** (AMO-Q101). Candidate input categories only, with no formulas, weights or thresholds:

- developmental state and internal cycle progress;
- Environmental Fit;
- reserves;
- current condition;
- species-specific biology, parameterised later.

The ownership boundary is unchanged and must stay clean:

```
WORLD                 → what conditions exist here, now
AMORPHO CONDITION     → what biological state this individual is in
ENVIRONMENTAL FIT     → what trajectory results
LIFE-CYCLE SYSTEM     → which phase transitions occur
```

Environmental Fit may push *toward* continued healthy activity, recovery, developmental progression or premature retreat. **It does not become the life-cycle system** (AMO-D035–AMO-D037). Controlled environments change conditions and biology responds; there is no `force_bloom` or `prevent_dormancy` flag (AMO-D046, AMO-Q049).

## 10. Rooting, astral exit and dormancy are three different things

Conflating these would break the model, so they are separated explicitly (AMO-D072):

| | Means |
|---|---|
| **Rooted** | the individual exists in plant state rather than animated — compatible with **every** phase |
| **Astral exit** | the player's consciousness leaves; the manifestation stops being animated |
| **Dormancy** | a life-cycle phase in which the core rests and access closes |

So a **rooted Active Leaf**, a **rooted Bloom**, a rooted Senescence and a rooted dormant tuber are all ordinary states of affairs. Rooting is not a synonym for dormancy (AMO-D032).

And astral exit does **not** cause a phase transition:

```
inhabited Leaf ──astral exit──▶ rooted Leaf plant     (still Active Leaf)
inhabited Bloom ──astral exit──▶ rooted blooming plant (still Bloom)
```

Conversely, **inhabitation animates the current manifestation without changing the underlying state**. An active-leaf plant inhabited is a leaf-form Amorpho; a blooming plant inhabited is a bloom-form Amorpho; an accessible transitional individual inhabited would be whatever that form turns out to be. No tuber kit is designed (AMO-Q086).

Phase-specific damage also **outlasts embodiment**: leaving and re-entering does not repair a damaged leaf, because the damage belongs to the manifestation, not to the animation.

## 11. Availability follows the biological clock

The playable roster changes because individuals **move through phases**, not because anything schedules it (AMO-D073, L45).

There is **no seasonal roster timer, rotation or availability event**. Availability emerges from the conjunction already established (AMO-D063):

```
    Astral Capacity              how many connections the human can sustain (AMO-D067)
            ▼
    active Anchor relationships
            ▼
  ┌──────── the three gates ────────┐
  │ Anchor · LIFE-CYCLE · condition │   ← this document supplies the middle gate
  └────────────────┬────────────────┘
                   ▼
        currently playable roster
```

Life-cycle state supplies the middle gate and **is not a fourth one**. Three consequences follow:

- **Hemisphere and geography strategy stays emergent.** Nothing encodes *northern = dormant*; world conditions and individual biology produce phases, and a distributed collection can therefore have different individuals available at the same global moment (AMO-D045, AMO-D046).
- **Human Astral Capacity cannot force a phase open.** A high-capacity Warden still cannot enter deep dormancy (AMO-D069, L44).
- **An Anchor persists through every phase change.** It stays attached through Leaf, Bloom, Senescence, dormancy and emergence until a human physically removes it (AMO-D061, AMO-D062).

### Transitions should be legible

Because availability is what players plan around, phase transitions should normally be **legible enough to support decisions** — reallocating an Anchor before dormancy, relocating an individual, timing a mission — rather than arriving as arbitrary lockouts. No interface is designed (AMO-Q085, AMO-Q100).

## 12. Phase and discoverability

The machine exposes phase identity so discoverability can react later. Direction only, with no values, and **never phase alone** — location, custody and environment matter at least as much (AMO-D015, AMO-Q015):

```
Deep Dormancy   minimum natural discoverability
Pre-Emergence   very low
Emergence       low, increasing
Active Leaf     ordinary visual discoverability
Bloom           maximum biological discoverability
Senescence      decreasing
```

A dormant tuber buried at an unknown outdoor site and one sitting labelled on a greenhouse shelf are not equally hard to find. **Deep Dormancy removes natural biological signals; the world and custody decide whether the physical plant can still be located** (AMO-D060).

## 13. State is not condition

A plant can be healthy and dormant, stressed and in leaf, healthy and blooming, stressed and senescing, healthy and deeply dormant. **Dormancy is a phase, never damage** (AMO-D057, L40), and nothing may encode `dormant = unhealthy`.

Condition and developmental state both feed the effective response profile, and they do so differently: condition degrades it, phase changes which sensitivities apply at all (AMO-D048).

## 14. Extension points

Each can be added without changing the topology:

| Extension | Enters at |
|---|---|
| species-specific phase timing and routing | parameterisation of §4–§5 |
| species that never enter deep dormancy | a dormant-family path that stays shallow (AMO-Q084) |
| leafless flowering, or concurrent leaf and bloom | Active family membership (§5) |
| transitional tuber-form gameplay | Early Dormancy / Pre-Emergence access windows (AMO-Q086) |
| phase-specific integrity variables | per-state manifestation (§7) |
| transition trigger model | §9's input categories (AMO-Q101) |
| pollination and reproduction | the exposed Bloom state (AMO-Q079) |
| core damage, recovery and death | condition, not the graph (AMO-D074–AMO-D076) |

## 15. The model against the required cases

| Case | How |
|---|---|
| one individual across many seasons | identity sits above the machine; the cycle returns to Deep Dormancy and out again (§2) |
| leaf damage gone structurally, consequences kept | new cycle, fresh structure; reserves, stress and development carry the season (§7) |
| Deep Dormancy blocks entry | hard closed state (§6) |
| Pre-Emergence may reopen access | transitional state widening before manifestation (§6–§7) |
| astral exit without dormancy | exit changes animation, not state (§10) |
| rooted Active Leaf · rooted Bloom | rooted is orthogonal to phase (§10) |
| premature retreat | Senescence entered early; cost in condition, not in the graph (§8) |
| seasonal roster change without timers | availability follows phase (§11) |
| Bloom-specific gameplay without being strictly better | own state, own manifestation, own costs (§5, §7) |
| Anchor survives phase change | Anchor belongs to the individual (§11) |
| Capacity does not override phase | separate gates, separate owners (§11) |

## 16. Open questions

The state machine's remaining detail (AMO-Q084) · access opening and closing points, and transition legibility (AMO-Q085) · phase-specific abilities and integrity, including transitional tuber forms (AMO-Q086) · premature retreat cost (AMO-Q087) · Bloom's content (AMO-Q088) · transition triggers (AMO-Q101). Related: controlled environments (AMO-Q049), reproduction (AMO-Q079), discoverability (AMO-Q015), core damage and recovery ([18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)), the Astral Radar (AMO-Q092).
