# 10 — World, Amorpho and Evolutionator

**Status:** conceptual. This document fixes three ownership boundaries and the derived bridge between them. It defines no variables, formulas, thresholds, genetics or numbers, and it contains no botanical facts. Where something is undecided it points to [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).

> The World says what exists here. The Amorpho says what it needs. Environmental Fit determines what happens between them. The Evolutionator handles inheritance, variation and generational change.

## 1. Three independent long-term simulation domains

Amorpho's long-term simulation is separated into three domains that own different truths, plus one derived evaluation that owns none.

| Domain | Owns | Answers |
|---|---|---|
| **World** | environmental truth | *What conditions exist here, now?* |
| **Amorpho** | biological traits, requirements and individual condition | *What does this individual need, prefer and tolerate?* |
| **Evolutionator** | inheritance, variation and generational change | *How are traits transmitted and changed across reproduction and generations?* |
| *(derived)* **Environmental Fit** | nothing — it evaluates | *What happens when these conditions meet this individual?* |

Each domain must be able to become substantially more sophisticated over the lifetime of the project **without forcing the others to change** (AMO-D035, AMO-D036, AMO-D037, AMO-D038).

## 2. The World owns environmental truth

The World describes conditions. It may eventually model location, season, time, temperature, humidity, rainfall, current weather, light, substrate, soil, drainage, exposure, shelter, local microclimate and other variables. The final list is open (AMO-Q005).

Those conditions have a geographic source: the World is a coherent representation of the real Earth (AMO-D045). Geography, environment and biology stay separate while feeding one another:

```
EARTH GEOGRAPHY
      ▼
WORLD SYSTEMS
      ▼
location + time + weather + local modifiers
      ▼
LOCAL ENVIRONMENT STATE  +  AMORPHO BIOLOGICAL STATE
      ▼
ENVIRONMENTAL FIT
      ▼
deterioration / equilibrium / recovery / growth
```

Earth decides *place*. The World decides *conditions*. The individual decides *requirements*. Fit decides *what happens*. See [02_WORLD_MODEL.md](02_WORLD_MODEL.md).

The key rule is ownership, not content:

> The World describes conditions. It does not know whether those conditions are good or bad for a particular Amorpho.

Nothing of the form `species X allowed here` or `species Y forbidden here` belongs inside World logic. That is the same rule as suitability-not-borders (L9, AMO-D013), stated as an ownership boundary.

## 3. The Amorpho owns its own biology

The Amorpho side owns what an individual is and needs: preferred ranges, tolerance ranges, critical limits, health, developmental state, dormancy, acclimation, individual variation, inherited traits and other biological properties. None of these are populated, and no real values may be invented (L4, AMO-D025). Botanical facts arrive only as approved input, once the model that needs them exists.

> The Amorpho knows itself. It does not know countries.

Rules such as `Thailand = good` or `Russia = bad` must never be encoded in the plant. Place names are the World's business, and even there they are labels, not mechanics.

## 4. Environmental Fit is derived

The effect of an environment on an individual belongs to neither side alone. It is derived from their interaction (AMO-D037):

```
WORLD ENVIRONMENT  +  AMORPHO REQUIREMENTS / CONDITION
                 │
                 ▼
          ENVIRONMENTAL FIT
                 │
                 ▼
  STABILITY / STRESS / RECOVERY / GROWTH
                 │
                 ▼
  HEALTH / DEVELOPMENT / REPRODUCTIVE EFFECTS
```

Environmental Fit must not become a third source of truth (AMO-D037). It does not store its own weather, invent its own biology, or accumulate a parallel model of the world. It evaluates, and its results feed stress, stability, recovery, growth, development, reproductive performance and — across generations — selection pressure.

**Terminology.** Environmental Fit is the same concept [02_WORLD_MODEL.md](02_WORLD_MODEL.md) introduced as *suitability*; "Environmental Fit" is now the name, because it makes the ownership boundary explicit. The World-side term **effective environment** is unchanged: it is the local environment an individual actually experiences, after cultivation context and care have modified the location environment. Effective environment is an input to Environmental Fit, not a synonym for it.

## 5. Fit is not a synonym for stress

Stress is one possible outcome among several. Without committing to discrete tiers — the eventual model may well be continuous — the conceptual range is:

| Fit | Conceptual trajectory |
|---|---|
| very poor | rapid stress accumulation → deterioration → possible loss of inhabitability → critical condition → possible death |
| marginal | slow or moderate stress; reduced growth; gradual deterioration or unstable equilibrium |
| adequate | stable survival |
| good | stable health; growth and development; long-term inhabitability |
| excellent | recovery; strong development; favourable growth; potentially improved reproductive performance |

No numerical thresholds are defined, and the tiers above are illustration, not schema. What matters is that the range genuinely extends into the positive: an environment can **improve** a plant — *surviving is not thriving* (L38).

The first concrete model of all of this is [12_ENVIRONMENT_AND_FIT_MODEL_V0.md](12_ENVIRONMENT_AND_FIT_MODEL_V0.md): five neutral World dimensions, a zoned Amorpho response profile, and a Fit output contract that keeps per-dimension detail alongside an aggregate trajectory (AMO-D046–AMO-D049).

This is what makes rooting a real decision rather than a penalty (AMO-D033), and what makes rescue windows emergent rather than fixed (AMO-D034). See [09_EMBODIMENT_AND_ASTRAL_TRANSFER.md](09_EMBODIMENT_AND_ASTRAL_TRANSFER.md).

## 6. Environment varies in time, not only in space

Environmental conditions come from the simulated World, so the same species can have different outcomes with:

- a different location;
- the same location in a different season;
- the same location and season in different weather;
- the same location outdoors versus in a greenhouse there.

This is intentional. A location may be favourable in one season, marginal in another, dangerous during an extreme event, temporarily excellent or temporarily catastrophic. Environmental Fit is never permanently static.

No real-world survival claims are made here. The system principle is only:

> Location × time × current conditions produce the World environment.

Time scale, season model, weather and extreme events are open (AMO-Q004, AMO-Q005).

## 7. Controlled environments modify conditions; they do not override biology

Homes, greenhouses and future controlled spaces do not grant exemptions:

```
WORLD OUTDOOR ENVIRONMENT
        │  building / environmental control
        ▼
LOCAL INDOOR ENVIRONMENT
        │
        ▼
evaluated by the same Environmental Fit mechanism
```

A greenhouse should therefore never need a special rule such as `greenhouse makes tropical plant valid`. It produces different temperature, humidity, exposure and protection, and the ordinary mechanism handles the result. How buildings modify local conditions, and how deeply indoor environments are simulated, is open (AMO-Q049).

## 8. The Evolutionator owns inheritance and generational change

The third domain owns inheritance, heritable variation, recombination where appropriate, future mutation and variation mechanisms where appropriate, transmission of traits through reproduction, generational change, and population-level change over time (AMO-D038).

It does **not** own environmental conditions. It does **not** decide what an individual needs. It does **not** decide that a population ought to become adapted to a particular named place.

### The Evolutionator does not know geography

Logic of the form `if location == Russia → increase cold resistance`, `if location == Thailand → increase heat tolerance`, or `if region == Australia → create Australian form` violates the architecture. The Evolutionator needs no country names, continents, climatic-zone labels, political borders or player-created region names.

Instead:

1. individuals possess inherited variation;
2. the World produces environmental conditions;
3. Environmental Fit affects survival, health, growth and reproductive success;
4. some individuals perform better than others;
5. reproduction transmits traits, with variation;
6. trait distributions may therefore shift across generations.

> Adaptation emerges. It is not commanded by geography.

## 9. Acclimation is not evolution

Two kinds of change must never be conflated (AMO-D039, extending AMO-D012):

| | **Individual acclimation and development** | **Evolutionary change** |
|---|---|---|
| Scope | one plant, within its own lifetime | a population, across reproduction and generations |
| Examples | acclimation, developmental response, health and condition changes, resource accumulation, different phenotypic expression, recovery, stress response | shifting trait distributions through inheritance and differential success |
| Owner | Amorpho (condition) evaluated through Environmental Fit | Evolutionator |

A plant does **not** become genetically cold-adapted because it spent a long time somewhere cold. A population may gradually shift if individuals vary, some inherited variants perform better under those conditions, those individuals survive or reproduce more successfully, their traits are inherited, and this repeats over many generations.

Genetics are deliberately not over-specified here (AMO-Q013, AMO-Q052).

## 10. Environmental selection

The World can create selection pressure while knowing nothing about evolution.

Consider a population that repeatedly experiences conditions near the lower end of its tolerance. Individuals differ slightly through inherited variation. Some may remain healthier, grow better, reproduce more successfully, or survive environmental events better. If those differences are heritable, the population may gradually shift over generations.

The World never says *"become more cold tolerant"*. The World simply remains the World. Selection emerges from differential performance. That is the intended architecture.

## 11. Player-driven selection

Players may create selection pressure deliberately, eventually choosing which individuals reproduce on the basis of traits they value — appearance, size, environmental tolerance, growth behaviour, reproductive traits or other inheritable characteristics. This may produce cultivated lines.

No selectable trait list is defined and no breeding algorithm is designed (AMO-Q013, AMO-Q052, AMO-Q054). The principle is:

> Environmental selection and player-driven selection may operate simultaneously.

A cultivated lineage may therefore reflect both what the player selected **and** what the World allowed to thrive (AMO-D040).

## 12. Evolution is emergent, not a button

There is no generic `EVOLVE` action that upgrades a species once enough experience has accumulated. Amorpho is not building stage-evolution in the creature-collecting tradition (see the conceptual reference points in [00_PRODUCT_VISION.md](00_PRODUCT_VISION.md)).

> Evolutionary change emerges through inheritance, variation, reproduction and selection.

Players should be able to create conditions that influence outcomes. The system itself stays generational and systemic.

## 13. Emergent local and player-created lineages

The real species remains the real species. Within it, the game world may produce many distinctive lineages, recognisable because of inherited variation, many generations, environmental selection, player selection, geographic history, cultivation history, founder effects, and whatever later genetic mechanisms are implemented.

One real species could eventually be associated with many game-world lineages — particular players, regions, greenhouses, cultivation histories or selective goals. These are **never** new species (L3, AMO-D005):

> Species come from reality. Individuals and lineages come from the game world.

How lines are identified, named or recognised is open (AMO-Q054), as are divergence limits within a species and the interaction with hybridization (AMO-Q053, AMO-Q055). See [03_PLANTS_INDIVIDUALS_LINEAGES.md](03_PLANTS_INDIVIDUALS_LINEAGES.md).

## 14. Improvement without evolution

A favourable environment may improve an **individual** during its own lifetime through recovery, healthier growth, better development, resource accumulation, improved reproductive condition and better overall condition. That is Environmental Fit acting on one plant.

Separately, repeated reproduction under the same conditions may shift **population** genetics through selection across generations. That is the Evolutionator.

The two are related — the first supplies the differential success the second acts on — but they are distinct processes, and a document or model that merges them is wrong.

## 15. Complexity may grow independently on each side

This is the long-term architectural payoff. The World may begin with very few environmental dimensions and later gain better modelling of seasons, weather, microclimates, rainfall, wind, extreme events, controlled environments, substrates and more. That must not require rewriting the Evolutionator.

Likewise, the Amorpho trait model may become much richer without the World needing to understand plant biology internally, and the Evolutionator may gain a more sophisticated inheritance model without the World changing how it represents weather.

The domains meet through explicit boundaries, never through shared hidden assumptions.

> Complexity may grow independently on each side of the boundary.

## 16. The architecture in one picture

```
                    WORLD
            (environmental truth)
                      │
            environmental state
                      │
                      ▼
AMORPHO ────────▶  ENVIRONMENTAL FIT
traits / needs /       │
condition              ▼
        stress / stability / recovery / growth
                       │
                       ▼
          survival and reproduction effects
                       │
                       ▼
                 EVOLUTIONATOR
     (inheritance / variation / generations)
                       │
                       ▼
                   OFFSPRING
```

The diagram is illustration. The ownership is the decision.

## 17. Open questions

Environmental variables and resolution (AMO-Q005), time and seasons (AMO-Q004), controlled environments (AMO-Q049), substrate (AMO-Q050), the three tolerance concepts (AMO-Q051), genetic abstraction (AMO-Q013), generation timing and selection strength (AMO-Q052), populations and divergence limits (AMO-Q053), player-created lines (AMO-Q054), and selection's interaction with hybridization (AMO-Q055). See [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).
