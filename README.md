# Amorpho

Amorpho is a game whose cast is real: the species of the plant genus *Amorphophallus*.

The player lives as a human in a persistent world modelled on Earth — exploring, discovering, acquiring, cultivating, propagating and trading individual plants, each with its own origin and history. Through a magical mechanism, the player's consciousness can leave their human body and inhabit a suitable plant, which becomes an **Amorpho**: a fighter controlled in real-time, skill-based combat. The plant they raised is the fighter they learn to master.

Amorpho targets one persistent World accessible through different platform experiences; each client is an entrance to the same Warden and history ([platform sovereignty](docs/27_PLATFORM_AND_WORLD_SOVEREIGNTY_V0.md)).

> Reality provides the cast. The game provides the fantasy.

## What makes it distinctive

Amorpho aims to create a distinct genre from a combination of ideas that are familiar individually:

- **The cast is real.** Species are the real species of the genus, from very small to enormous. No species are invented.
- **Every plant is an individual.** Plants are persistent, with identity, provenance and lineage — not interchangeable items.
- **The world has its own continuity.** Natural populations exist and develop whether or not players intervene. Plants never spawn on demand.
- **One Earth.** The world is a coherent representation of the real Earth — real countries, regions and cities — shared by human life and plant life alike.
- **Environment, not borders.** Where a plant can grow depends on climate and conditions, not on which country it is native to.
- **Risk is where the decisions are.** Protected cultivation is safer; outdoor planting can be better but exposes plants to weather, pests, theft and accidental pollination. A flowering plant's scent makes it easier for others to find.
- **The plant you raised is the fighter you play.** The same individual spans long-term cultivation and intense, skill-based fighting.
- **One consciousness, one body.** You have one human body and inhabit at most one plant at a time. A hundred Amorphos give you options and logistics, never an army.
- **Two speeds.** The living world moves quickly around a human who changes rarely but permanently.
- **What you can play shifts with the seasons.** A plant is playable only if it carries a physical Astral Anchor, is in an accessible life-cycle phase, and is well enough — and a dormant tuber is safe precisely because nobody can reach or find it.
- **Plants change across generations.** Inheritance, variation and selection — from the world and from you — can make distinctive lineages emerge within real species.
- **Two ways in, one world.** Standard and VR gameplay are both first-class entrances to the same persistent game. VR is optional, never secondary.

**Fun comes first.** Botanical realism grounds the world but never suffocates the game. A player with no interest in plants should be able to love Amorpho purely as a game.

## Two layers

| | Human / World layer | Amorpho / Combat layer |
|---|---|---|
| **You are** | a human character in a persistent world | one of your plants, inhabited and animated — while your human body waits somewhere |
| **You do** | travel, explore, discover, acquire, trade, cultivate, propagate, maintain homes, gardens and greenhouses | fight in real time: movement, positioning, timing, blocking, attacks, counters, learnable moves, combinations, rounds |
| **Timescale** | long-term, persistent | short, intense |
| **Mastery** | knowledge, planning, risk management | practised skill with a specific Amorpho |

The bridge between them is **transformation**, and its mechanism is **astral transfer**: the player's consciousness leaves the human body and inhabits one suitable individual, which becomes an active Amorpho. The human body stays in the world while this happens, so where it rests matters — and when the player leaves the Amorpho, the plant roots and is once again governed by its real relationship with its environment. Fighting uses fighting-game rounds, not turn selection.

## Real species, real limits

The known real species of *Amorphophallus* define the base cast. A species gives a character its identity and visual foundation; its combat design is authored for balance and fun, not derived from botany. Diversity grows from within-species variation, individual history, lineages and hybrids — and hybrids are possible only between species pairs approved as compatible on the basis of real-world research.

## The Reality Gate

Amorpho is completely independent, and it does not research botany. Detailed research about *Amorphophallus* happens outside this repository. Amorpho receives only a minimal **approved export** — initially a CSV list of species — through the **Reality Gate**: a simple, strictly one-way boundary where the file is validated and accepted.

```
external master data ──▶ approved export file ──▶ REALITY GATE ──▶ Amorpho data ──▶ game systems
```

Each species has a permanent, opaque ID such as `AMO-SP-000001`; its scientific name is metadata that may change. Once a file is accepted, the game never needs the external source again. See [docs/05_REALITY_GATE.md](docs/05_REALITY_GATE.md).

## Current maturity

**Foundation, plus the first systems pass.** This repository currently contains the product vision, design laws, decision ledger, open-question register, conceptual architecture, the input contract for the Reality Gate, and — from the first post-foundation design passes — the embodiment model, the three simulation domains, the Standard/VR interface principles, Earth as the World's geographic foundation, and the first environmental model.

It does **not** yet contain game code, an engine, art, or any species data. The species input file contains only its header until the first approved export is supplied. No engine or programming language has been chosen; that decision will be made from evidence.

## How the project develops

Amorpho is incubating as a low-pressure, long-running project:

- **Always moving, never rushed.** It may grow slowly, but it never stops growing.
- **Build irreversible knowledge now; defer expensive production** until capacity — tools, AI agents, generative media, people — catches up.
- **Small durable steps** over speculative infrastructure.

Progress is measured in maturity phases, not dates: see [docs/07_INCUBATION_ROADMAP.md](docs/07_INCUBATION_ROADMAP.md).

## Repository map

```
README.md                      this file
CLAUDE.md                      operational guidance for AI development agents
docs/
  00_PRODUCT_VISION.md         what Amorpho is, pillars, glossary
  01_DESIGN_PRINCIPLES.md      the design laws
  02_WORLD_MODEL.md            persistent world, environment, cultivation, discoverability
  03_PLANTS_INDIVIDUALS_LINEAGES.md  species, individuals, genetics, lineages, hybrids
  04_TRANSFORMATION_AND_COMBAT.md    the artifact, transformation, combat pillars
  05_REALITY_GATE.md           the one-way boundary for approved real-world input
  06_OPEN_QUESTIONS.md         what is not decided yet
  07_INCUBATION_ROADMAP.md     maturity phases and near-term steps
  08_CONCEPTUAL_ARCHITECTURE.md  data layers, boundaries, engine decision criteria
  09_EMBODIMENT_AND_ASTRAL_TRANSFER.md  one body at a time, rooting, rescue, equipment
  10_WORLD_AMORPHO_EVOLUTIONATOR.md     the three simulation domains and Environmental Fit
  11_STANDARD_AND_VR_GAMEPLAY.md        two first-class interfaces to one game
  12_ENVIRONMENT_AND_FIT_MODEL_V0.md    the first environmental model: vector, profile, fit contract
  13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md  worked cases that stress-test the v0 contract
  14_CURRENT_BIOLOGICAL_CONDITION_V0.md the biological state a persistent individual carries
  15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md  life-cycle phases, Astral Anchors, playable availability
  16_HUMAN_WARDEN_PROGRESSION_V0.md     the human's own slow magical progression
  17_LIFE_CYCLE_STATE_MACHINE_V0.md     the life-cycle topology and astral access windows
  18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md  harm horizons, recovery, Bloom maturity
  19_DEVELOPMENTAL_MATURITY_V0.md       the persistent developmental axis
  20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md  biology vs magic, Astral Readiness, astral signal
  21_PATHOLOGICAL_TUBER_IMPACT_V0.md    when adverse circumstances become persistent Tuber loss
  22_BIOLOGICAL_YEAR_WALKTHROUGH_V0.md  one abstract individual's year across the established systems
  23_ACUTE_EVENT_TO_LEAF_IMPAIRMENT_V0.md  World event through local exposure to post-event Leaf state
  24_SAME_PHASE_LEAF_RECOVERY_V0.md  mature Leaf stabilization, functional recovery and possible replacement
  25_TUBER_FUNDED_MANIFESTATION_AND_REPLACEMENT_ROUTING_V0.md  Tuber funding, Leaf collapse and replacement/retreat routing
  26_PLANT_AUTONOMY_ASTRAL_LEVERAGE_AND_ROUTING_V0.md  who selects a biological route: the plant, or a Warden with astral presence
  27_PLATFORM_AND_WORLD_SOVEREIGNTY_V0.md  one canonical World, Warden continuity and platform gateways
  28_ASTRAL_WINDOW_END_TO_END_TRACE_V0.md Leaf collapse through autonomous, Warden and missed-Window routes
  29_REPLACEMENT_EMERGENCE_TO_ASTRAL_READINESS_V0.md shared Leaf/Bloom emergence and Full Deployment before inhabitation
  30_EMERGENCE_INVESTMENT_AND_FULL_DEPLOYMENT_ACCOUNTING_BOUNDARY_V0.md sunk Tuber construction cost and mature manifestation handoff
  31_DAMAGED_EMERGENCE_TO_IMPERFECT_DEPLOYMENT_V0.md damage during construction, imperfect deployment and failure
  32_IMPERFECTLY_DEPLOYED_MATURE_LEAF_STABILIZATION_OR_DECLINE_V0.md first mature period of a Leaf that deployed compromised
  33_MATURE_LEAF_FUNCTIONAL_COLLAPSE_BOUNDARY_V0.md when a mature Leaf stops being serviceable and the manifestation ends
  34_EMBODIMENT_ACROSS_TERMINAL_MANIFESTATION_COLLAPSE_V0.md inhabiting a doomed manifestation, and where embodiment ends
  35_COMBAT_PROTECTION_MANIFESTATION_BODY_DAMAGE_AND_BIOLOGICAL_PERSISTENCE_V0.md protection, body damage and what persists after a fight
  DECISIONS.md                 the decision ledger (AMO-D###)
data/
  input/                       approved real-world input (species CSV, header only)
  canon/                       internal representation derived from input (not defined yet)
```

## Where to read next

1. [docs/00_PRODUCT_VISION.md](docs/00_PRODUCT_VISION.md) — the vision.
2. [docs/01_DESIGN_PRINCIPLES.md](docs/01_DESIGN_PRINCIPLES.md) — the laws.
3. [docs/DECISIONS.md](docs/DECISIONS.md) — what is decided.
4. [docs/06_OPEN_QUESTIONS.md](docs/06_OPEN_QUESTIONS.md) — what is not.
5. The remaining documents in [docs/](docs/) for detail, and [CLAUDE.md](CLAUDE.md) if you are contributing.

## About

Amorpho is a game project within the Trederus Maximus group.
