# 03 — Plants, Individuals and Lineages

**Status:** conceptual. This document fixes the concepts and their separation. It does not define a genetic model, data schemas or simulation rules.

> Species come from reality. Individuals and lineages come from the game world.

## 1. Concepts kept separate

These concepts must never be merged into one another, in documents or in data (AMO-D012).

| Concept | What it is | Where it lives (AMO-D021) |
|---|---|---|
| **Species** | A real *Amorphophallus* species, identified by a permanent `AMO-SP-` ID. Defines identity and visual foundation. | approved reality input |
| **Individual** | One persistent plant, with a unique identity. | world state |
| **Genotype** | The individual's heritable makeup, in whatever abstraction the game adopts. Fixed for the individual's life. | world state |
| **Phenotype** | How the individual actually looks and performs: size, vigour, appearance, game traits. | world state (derived) |
| **Environment** | The effective environment the individual lives in (see [02_WORLD_MODEL.md](02_WORLD_MODEL.md#effective-environment)). | world state |
| **Population** | A group of individuals living together, natural or cultivated. | world state |
| **Lineage** | A line of descent across generations. | world state |
| **History** | Everything that has happened to an individual: owners, places, propagation, events, combat. | world state |

Conceptually:

```
phenotype = f(genotype, effective environment, age and history)
genotype  = inherited at creation; never changed afterwards
```

How an individual responds to its environment is layered from **species baseline**, **individual traits** and **current condition** into an effective response profile, which Environmental Fit then evaluates (AMO-D048). See [12_ENVIRONMENT_AND_FIT_MODEL_V0.md](12_ENVIRONMENT_AND_FIT_MODEL_V0.md).

## 2. Species

A species exists in Amorpho only because it appears in approved input (AMO-D004, AMO-D017). Its identity is a permanent, opaque species ID such as `AMO-SP-000001`; its scientific name is mutable metadata that may change in a later approved export without affecting the identity (AMO-D022). The approved species list currently contains no species.

A species determines what an individual fundamentally *is* — its identity and visual foundation — but not how large, strong or valuable a particular individual becomes. A naturally enormous species can remain small in an undersized pot (AMO-D014). A species also has no direct combat power (AMO-D006).

## 3. Individuals

Every plant is a persistent individual with a unique identifier that is never reused (AMO-D011, AMO-D022).

Over its life an individual can accumulate provenance such as:

- species (or parent species, for a hybrid);
- unique identity;
- origin, founder population;
- parentage, where known;
- generation and lineage;
- previous and current owners;
- cultivation locations and current location;
- propagation history;
- notable events;
- phenotype and game traits;
- transformation and combat history, where appropriate.

An individual is also not the same thing as its **current visible structure**. Across its life it may be a tuber, a leaf-form plant or a flowering individual, and identity, lineage, genotype and history stay attached to the individual through every phase — a plant that loses its leaf and grows another has not become a second plant (AMO-D058, [15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md)). The same individual persists through embodiment, where its **Tuber travels inside the animated manifestation as the central core**, and through the loss of that manifestation, where whatever core survives lies exposed at the site with its identity and history intact ([37](37_MANIFESTATION_DESTRUCTION_TUBER_CORE_VIABILITY_AND_PHYSICAL_DROP_V0.md), AMO-D129, AMO-D130).

**Knowing is not showing.** The simulation may track all of this; what any player sees is a separate design decision (L14). For example, a player might know only that a plant was "bought from a collector", while the world knows its full chain of custody.

## 4. Acclimation versus genetic change

Moving an individual somewhere else does **not** change its genetics. An individual can *acclimate*: its phenotype responds to its new effective environment, so it may grow differently, larger or smaller, faster or slower. A favourable environment may genuinely improve it — recovery, healthier growth, better development, improved reproductive condition — and that is still not evolution (AMO-D039).

Genetic change happens only **across generations and populations**, through reproduction, variation and selection (AMO-D012). That process is owned by its own simulation domain, the **Evolutionator** (AMO-D038), which knows nothing about geography: adaptation emerges from variation, differential success and inheritance, and is never granted by a place. See [10_WORLD_AMORPHO_EVOLUTIONATOR.md](10_WORLD_AMORPHO_EVOLUTIONATOR.md).

## 5. Reproduction and propagation

Propagation paths fall into two conceptual categories:

Every new individual — however produced — begins **unowned and without an Astral Anchor**. Parent ownership and anchoring never propagate to offspring, and anchoring is never required for reproduction or population persistence (AMO-D064).

- **Vegetative propagation** produces new individuals that are genetically copies of the parent. Each is still a separate individual with its own identity and history, linked to its parent; together they form a clone line.
- **Sexual reproduction** (pollination, seed) produces new individuals with new genetic combinations from two parents. This is the only route to genetic change and to hybrids.

Which vegetative methods, pollination requirements and life-cycle stages apply to which species is not known to Amorpho and must not be assumed. Researching it is not Amorpho's job; if a game system needs such facts, they will arrive as approved input (AMO-D024, AMO-D025). How deeply the plant life cycle is simulated is open (AMO-Q012).

## 6. Variation within a species

Members of a species are not identical. Amorpho should eventually support meaningful within-species variation that affects visible characteristics and possibly other systems. This is the main source of diversity that does not require inventing species.

The genetic abstraction — how variation is represented and inherited — is open (AMO-Q013). The requirement is a model that is sophisticated enough to produce emergent, recognisable lineages, and simple enough to be playable and explainable.

## 7. Lineages

Over many in-game generations, reproduction in particular places or under particular player choices can produce recognisable lineages. Conceptually:

```
species
  → original population
    → population moved elsewhere
      → repeated reproduction in the new environment
        → locally selected lineage
          → distinctive long-term traits
```

Such lineages — player-created or location-created — may become one of Amorpho's most important sources of emergent uniqueness. A lineage is always a world-state phenomenon, never a new species (AMO-D005).

Two kinds of selection can drive this, possibly at once (AMO-D040): the **World** creates selection pressure simply by producing conditions under which some heritable variants do better, and **players** create it deliberately by choosing which individuals reproduce. A cultivated line may therefore reflect both what a player selected and what the world allowed to thrive. There is no `EVOLVE` action: change is generational and emergent. How lines are identified or named, how far they may diverge, and how selection interacts with hybrids are open (AMO-Q053, AMO-Q054, AMO-Q055).

## 8. Hybrids

Hybridization exists, but only between approved compatible pairs (AMO-D027):

- Compatibility is a **symmetric species-pair relationship**: `A + B` is either an approved compatible pair or not approved. Pairs come only from approved input; the research evidence behind them stays outside Amorpho.
- A pair that is not approved cannot hybridize in the game. "Not approved" is not a claim of biological incompatibility. No approved pairs exist yet.
- Both deliberate and accidental hybridization may exist. Accidental hybridization typically happens outdoors when a compatible plant is flowering nearby and pollination conditions allow it.
- A hybrid individual is an individual like any other, with two parent species rather than one. Which parent plant carried the seed is part of the individual's parentage — world-state history — even though compatibility itself is symmetric. Whether hybrids themselves reproduce is open (AMO-Q018).

## 9. Open questions

Plant simulation depth (AMO-Q012), genetic abstraction (AMO-Q013), pollinators (AMO-Q014), changes in the approved species list (AMO-Q016), hybrid fertility (AMO-Q018), initial populations (AMO-Q019), and pests and pathogens (AMO-Q020). From the Evolutionator: generation timing and selection strength (AMO-Q052), populations and divergence limits (AMO-Q053), player-created lines (AMO-Q054), and selection's interaction with hybridization (AMO-Q055). See [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).
