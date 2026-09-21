# 08 — Conceptual Architecture

**Status:** conceptual. This document describes boundaries, data layers and dependency direction. It is not a module plan: none of the systems below exists yet, and none should be built speculatively.

## 1. Dependency direction

```
  external curated master data        (outside Amorpho)
            │
            ▼
  approved export file
            │
            ▼   REALITY GATE — one way
  1. Approved Reality Input           ◀── referenced by 2 and 3
            ▲
            │ references
  2. Game Design Data                 ◀── referenced by 3
            ▲
            │ references
  3. Persistent World State

  Game systems read layers 1 and 2, and read and write layer 3.
```

- Knowledge enters only through the Reality Gate, and only inward (AMO-D017).
- The game has no runtime dependency on any external system (AMO-D018).
- Higher-numbered layers may reference lower-numbered ones; never the reverse.

## 2. Data layers

Amorpho's data is separated into three conceptual layers (AMO-D021).

| Layer | Holds | Changes through | Examples |
|---|---|---|---|
| **1. Approved Reality Input** | minimal real-world facts approved for use by Amorpho | the Reality Gate only | species IDs and approved scientific names; approved compatible pairs; later: selected environmental facts |
| **2. Game Design Data** | information Amorpho creates for gameplay | normal design work | combat characteristics, abilities, animations, balancing, transformation behaviour, progression, visual interpretation of species |
| **3. Persistent World State** | what exists or happens in a running world | simulation and player actions | individual plants, ownership, location, parentage, lineages, houses, pots, greenhouses, populations, trades, combat history |

Rules:

- Game design data may reference species by ID (for example, a combat kit keyed by `AMO-SP-` ID) but can never add species or compatible pairs.
- World state may reference both. Every individual's species ID must exist in approved input.
- Approved input references nothing in design data or world state.
- The genus, the species list and the approved pairs are reality. Everything the plants *do* as Amorpho is design.

Only Layer 1 has a location today: accepted files in [`data/input/`](../data/input/README.md), with [`data/canon/`](../data/canon/README.md) describing the internal representation that will later be derived from them ("canon"; not yet defined). Homes for design data and world state are created when there is something to put in them.

## 3. Conceptual systems

These are boundaries of responsibility, useful for reasoning and for future work allocation — not a component list to implement.

Three of them are **independent long-term simulation domains** that own different truths, and each must be able to become substantially more sophisticated without forcing the others to change (AMO-D035, AMO-D036, AMO-D038):

```
WORLD           what conditions exist here, now?
AMORPHO         what does this individual need, prefer and tolerate?
EVOLUTIONATOR   how are traits transmitted and changed across generations?
```

Between the first two sits **Environmental Fit**, which owns no truth at all and only evaluates their interaction (AMO-D037). The full model is in [10_WORLD_AMORPHO_EVOLUTIONATOR.md](10_WORLD_AMORPHO_EVOLUTIONATOR.md).

| System | Responsibility | Gameplay layer |
|---|---|---|
| **Approved reality** | species identities, names and approved pairs, derived from approved input; read-only at runtime | shared |
| **Environment** (World) | location environments; effective environment; conditions only, never verdicts | world |
| **Plant life** (Amorpho) | growth, life cycle, health, condition, requirements, tolerances, acclimation | world |
| **Environmental Fit** | derived evaluation of environment × individual: stress, stability, recovery, growth | world (derived) |
| **Evolutionator** | inheritance, variation, recombination, generational and population change | world |
| **Genetics and lineage** | genotype and phenotype representation; lineages; hybridization between approved compatible pairs | world |
| **Populations** | natural and cultivated populations; spread; establishment | world |
| **Geography and places** | the representation of Earth; cities; travel | world |
| **Human life** | player character, homes, property, cultivation actions | world |
| **Society and trade** | other people, ownership, exchange, theft | world |
| **Discovery** | flowering scent, detection, information about where plants are | world |
| **History** | provenance and event records for individuals and the world | world |
| **Transformation** | astral transfer: moving the player's consciousness into one eligible individual and back | bridge |
| **Combat** | real-time, skill-based fighting | combat |

Independence between the three domains is the point of the split: the World may gain seasons, microclimates and extreme events without the Evolutionator changing; the Amorpho trait model may become much richer without the World learning any biology; the Evolutionator may gain a more sophisticated inheritance model without touching how weather is represented. They meet through explicit boundaries, never shared hidden assumptions.

## 4. The bridge between the gameplay layers

Transformation is the only point where the two gameplay layers (world and combat) meet.

```
World state: individual plant ──▶ Transformation ──▶ Combat: fighter instance
                   ▲                                          │
                   └──────── outcomes recorded (if any) ◀──────┘
```

- The combat layer receives a **view** of an individual — its species, identity and whatever traits design decides are relevant (AMO-Q025). It does not need the world simulation to run.
- A view is not a second entity. The plant and the animated Amorpho are one persistent individual in two states, and identity, provenance, lineage, ownership and history stay attached to it across the boundary (AMO-D030). Nothing may duplicate the individual into an unrelated plant object and fighter object to be reconciled afterwards.
- The human body does not cross this bridge. It remains in world state, unattended, while the player's consciousness is elsewhere (AMO-D029) — so the world layer keeps running for the human even during combat.
- What, if anything, flows back into the world after combat (history entries, injury, fatigue) is open (AMO-Q026).
- Keeping this bridge narrow allows the two gameplay layers to be prototyped, and possibly implemented, separately.

### Interfaces are not layers

Standard Gameplay and VR Gameplay are two first-class ways of inhabiting the same game — not a third layer, not separate worlds, accounts or progression systems (AMO-D041, AMO-D042):

```
                 SAME AMORPHO GAME
                         │
              gameplay and world truth
                         │
                   player intent
                   ╱           ╲
         STANDARD GAMEPLAY     VR GAMEPLAY
```

The architectural consequence today is modest and deliberate: core rules should express gameplay intent rather than hard-code one physical input method, and core concepts should not fundamentally require a 2D UI. No intent API is defined, and no VR production system is built (AMO-D043). See [11_STANDARD_AND_VR_GAMEPLAY.md](11_STANDARD_AND_VR_GAMEPLAY.md).

## 5. Outside, import time and runtime

| | Outside Amorpho | Import time (Reality Gate) | Runtime |
|---|---|---|---|
| External master data and research | built, curated, approved | not present | unknown to the game |
| Approved export file | prepared | validated, then accepted into `data/input/` | source of the internal representation |
| Internal representation ("canon") | — | derived from accepted input | read-only |

## 6. Technology posture

- No engine, framework, programming language or runtime stack has been chosen (AMO-D020).
- No VR platform, SDK, middleware or headset has been chosen either, and none may be until there is evidence (AMO-D043, AMO-Q062).
- No shared cross-project VR framework exists or is planned; reuse is extracted from proven use, never designed in advance (AMO-D044).
- Repository contents are language-neutral: Markdown and CSV.
- No dependencies have been added. Add one only when a concrete step needs it, and record why.

## Engine and technology decision criteria

An eventual engine decision (AMO-Q036) must be evidence-driven and should answer at least these questions:

- **World scale.** Can it represent the world at the scale chosen for AMO-Q001, including streaming and level of detail?
- **Persistence.** How does persistent world state — many individuals with long histories — fit? Is the simulation deterministic or reproducible where auditability matters?
- **Networking.** What multiplayer topology does it support (AMO-Q006)? What server-authority model?
- **Fighting latency.** Can it deliver the input responsiveness and network techniques that competitive real-time fighting needs?
- **Animation.** Can it support expressive, distinct characters at roster scale (AMO-Q027) — including non-humanoid plant bodies?
- **VR capability.** Could it eventually support first-class VR — both layers, not a combat-only mode — without a rewrite, and without requiring VR work now (AMO-D042, AMO-D043, AMO-Q062)? This is a selection criterion, not a commitment to any VR technology.
- **Target platforms** (AMO-Q037).
- **Content pipeline.** How do approved input, design data and assets flow into builds? Is modding or user-generated content desirable?
- **Procedural and simulation systems.** Does it support large-scale background simulation (populations, environment, genetics) without fighting the engine?
- **Tooling.** Editors and tools for designers, curators and artists.
- **Team composition.** Which skills will future contributors — human and AI — realistically have?
- **Licensing and cost.** Terms, royalties, and the risk of license changes over a multi-year horizon.
- **Long-term maintainability.** Will it still be viable, supported and upgradable in ten years? Can the project migrate away from it?

It is possible that one stack does not suit everything: persistent-world simulation and low-latency fighting have different needs. That is a question to answer with evidence, not an assumption in either direction.
