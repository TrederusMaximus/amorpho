# 02 — World Model

**Status:** conceptual. This document fixes the concepts and rules of the world. It deliberately does not specify scale, resolution, formulas or implementation. Where something is undecided it points to [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).

## 1. The World is Earth

The player exists as a human character in a persistent representation of **the real Earth** (AMO-D045). This is a foundational commitment, not a flavour note. Amorpho is not set on an abstract fantasy map, an Earth-inspired fictional planet, a handful of disconnected regions, or a simplified botanical habitat map.

This is one canonical Earth-based Amorpho World across platform clients. Different devices may present different local detail, but no device creates a separate Earth or biological history (AMO-D102, AMO-D104; [27_PLATFORM_AND_WORLD_SOVEREIGNTY_V0.md](27_PLATFORM_AND_WORLD_SOVEREIGNTY_V0.md)).

The World should ultimately contain a coherent representation of the globe, continents, countries, regions, real cities, natural areas, climatic regions, the real areas associated with real *Amorphophallus* species, and whatever other places human and Amorpho gameplay need. Amorpho does not invent a fictional substitute for Thailand, Indonesia, Africa, India, Australia, Europe or Russia in order to simplify the world. Real geographic identity is part of what makes a plant's origin and journey mean anything.

This does **not** require every road, building, street or tree at one-to-one fidelity. Detail may grow progressively over the project's lifetime (§1.3).

Cities and world geography exist independently of any individual player (AMO-D009). How faithfully and at what scale Earth is represented is open (AMO-Q001), as is how players travel (AMO-Q002) and how real places relate to player homes (AMO-Q003).

### 1.1 One Earth, two gameplay domains

The same World must serve two very different kinds of play, and neither may reduce the other to scenery:

| | **Human World** | **Amorpho World** |
|---|---|---|
| Needs | an inhabited civilisation layer: countries, cities, towns, travel, homes, apartments, property, greenhouses, stores, collectors, trade, infrastructure, transport, social life | a biological layer: natural environments, climate, seasons, weather, vegetation, terrain, growing conditions, native and introduced populations, outdoor cultivation, microclimates, reproduction and population history |
| Test | a believable place for a human to live | a biologically meaningful place for Amorphos to exist |

These are **not separate maps**. They are two ways of interacting with the same persistent Earth, and the world model is wrong if it satisfies only one of them.

It follows that the world is never designed as *cities or wilderness*. A player may live in a city apartment, keep Amorphos in pots, use a greenhouse, travel out of the city, reach natural habitat, establish plants outdoors, and travel to another country — ideally as one coherent world rather than a set of disconnected modes.

### 1.2 Origin is not permission

Where a species comes from and where it can live are different questions, and this decision does not blur them.

A species may have a real original distribution. What happens to a plant in a given place is still decided by Environmental Fit — the World's local conditions met with that individual's biology (§4, AMO-D035–AMO-D037). A plant may therefore survive or even thrive far outside its origin if conditions suit it, and may fail inside it if they do not.

```
Earth        → determines place
World        → determines local conditions
the Amorpho  → determines biological requirements
Environmental Fit → determines the result
```

`native country = allowed` and `non-native country = forbidden` remain excluded (L9, AMO-D013).

### 1.3 Fidelity grows; structure does not change

Geographic representation is conceptually a hierarchy, from the globe down to a single root zone:

```
Earth → continent / country → region → city → district / local area
      → property / outdoor site → building / greenhouse → pot / bed → root zone
```

This is a conceptual ordering, not an implementation mandate and not a required set of levels. Its purpose is to let the World become progressively more detailed without invalidating the structure above it, and to let environmental state exist at increasingly local scales (§4).

No map technology, data source, streaming architecture or world-instance model follows from any of this (AMO-D020, AMO-Q001, AMO-Q066). Nothing here authorises a global map, GIS ingestion, imagery, procedural cities, terrain generation, navigation or a weather service.

### 1.4 Local spaces sit inside Earth

A house, apartment, greenhouse or garden is a place *within* Earth geography, not an unrelated instance:

```
Earth → country → city → local area → property → greenhouse → growing bed → rooted Amorpho
```

This matters because outside conditions reach inside. A greenhouse in northern Europe and one in tropical Southeast Asia start from very different external conditions even when internal control brings their local environments close together — and that difference should emerge from the architecture rather than from special rules (AMO-Q064, AMO-Q065).

Real Earth geography never implies anything about a player's real residential address. That separation is a safety requirement, and how player homes and properties are represented remains open (AMO-Q003).

## 2. The world continues without players

If no player intervenes, natural *Amorphophallus* populations continue to exist and develop in their natural regions. Players can change this history — by collecting, moving, cultivating, propagating, trading or losing plants — but the world does not wait for them.

The world's clock and how fast plant life unfolds relative to play time are open (AMO-Q004).

## 3. Finite populations: nothing comes from nothing

The world begins with **finite** natural populations and cultivated stocks (AMO-D010). After that, the number and distribution of plants change only through world processes:

| Way plants enter or spread | Way plants leave or decline |
|---|---|
| vegetative propagation | death (environment, pests, neglect, events) |
| seed production and germination | removal from a population by collection |
| trade and human transport | whatever loss rules combat may have (AMO-Q026) |
| deliberate cultivation | |
| natural establishment, where appropriate | |

Trade, transport, collection and theft move plants between places and owners; they never create or destroy them. Plants never spawn because a player, quest or shop needs one. As a result, the global population develops historically, and an individual plant can matter because of where it has been.

### Introductions and new populations

Because the World is Earth and it persists, players can change where plants are over long spans of time:

```
natural population → collection → transport → cultivation elsewhere
  → propagation → possible outdoor establishment → new game-world population
```

A species originating in one region may eventually have native populations, cultivated populations, greenhouse populations, player-created outdoor populations and long-established introduced lineages elsewhere on Earth. None of this creates plants from nothing (AMO-D010); it moves and multiplies what already exists.

No population ecology is designed here. What is preserved is the spatial foundation that makes it possible, and the fact that distribution is world history rather than a fixed property of a species.

How initial populations are sized and placed is open (AMO-Q019), as is how natural and introduced populations are represented spatially (AMO-Q068). How a species added to the approved list later enters a live world is open (AMO-Q033).

## 4. Environment and Environmental Fit

Environmental Fit replaces country locks (AMO-D013). A species is neither allowed somewhere merely because it is native to that country nor forbidden everywhere else.

> **Terminology.** This concept was introduced at foundation as *suitability*. It is now called **Environmental Fit**, because the name has to carry an ownership boundary: the World describes conditions, the individual knows its own requirements, and Fit is derived from their interaction (AMO-D035, AMO-D036, AMO-D037). The full ownership model is in [10_WORLD_AMORPHO_EVOLUTIONATOR.md](10_WORLD_AMORPHO_EVOLUTIONATOR.md); this section covers the world side of it.

The concept has three parts:

1. **Location environment.** A place has environmental properties. Candidate properties include temperature range, seasonality, rainfall, moisture, dry season, light/shade and drainage — and perhaps soil or others where gameplay value justifies them. The final set is open (AMO-Q005). The World describes these conditions; it does not know whether they suit any particular plant (AMO-D035).
2. **Species tolerance profile.** Each species has a corresponding profile of what it tolerates and prefers, and each individual has its own condition and variation on top of that (AMO-D036). This is reality-derived knowledge. Once the environment model is designed, the approved input format will be extended with exactly the facts it needs (AMO-D025). No profile data exists yet, and none may be invented.
3. **Environmental Fit.** Comparing an effective environment with an individual yields what happens to it there. The first concrete model — five World dimensions, a zoned response profile and a defined output contract — is [12_ENVIRONMENT_AND_FIT_MODEL_V0.md](12_ENVIRONMENT_AND_FIT_MODEL_V0.md) (AMO-D046–AMO-D049). Fit is best thought of as graded rather than a simple allowed/forbidden switch, and its range genuinely extends into the positive: an environment may cause deterioration, hold an individual in equilibrium, or let it recover, grow and improve (AMO-D033, AMO-D037). Fit is **not** a synonym for stress. The exact form — continuous or tiered — is undecided.

### Effective environment

A plant does not experience only its location. It experiences an **effective environment**:

```
location environment
   modified by cultivation context (pot, home, greenhouse, outdoors)
   modified by care (player actions, neglect)
   = effective environment  →  met with the individual  →  Environmental Fit
```

This is how a species can survive far outside its natural range under cultivation, and how the same species can do very differently in two gardens in the same city.

Buildings and greenhouses work by **modifying local conditions**, not by granting exemptions. A greenhouse should never need a special rule such as `greenhouse makes tropical plant valid`; it produces different temperature, humidity, exposure and protection, and the ordinary mechanism handles the result (AMO-D035, AMO-Q049).

Every level produces the same environmental dimensions, so complexity can be inserted between levels without Environmental Fit ever learning about buildings (AMO-D046). Environmental state can exist at increasingly local scales, nested inside the World rather than replacing it:

```
world / city conditions → house → room → pot → root zone
```

This is what lets a plant in a pot experience something different from the room, the house and the street outside. How deep this nesting goes — and where it usefully stops — is open (AMO-Q065), as is substrate (AMO-Q050). None of it is being built now; only the principle is preserved.

Environmental Fit affects how an individual *develops and expresses itself*. It does not change the individual's genetics (AMO-D012). Genetic change happens across generations, and belongs to a separate domain, the Evolutionator (AMO-D038, AMO-D039); see [03_PLANTS_INDIVIDUALS_LINEAGES.md](03_PLANTS_INDIVIDUALS_LINEAGES.md) and [10_WORLD_AMORPHO_EVOLUTIONATOR.md](10_WORLD_AMORPHO_EVOLUTIONATOR.md).

## 5. Cultivation contexts

Plants can survive outside their natural regions through human cultivation. Each context is a different trade-off (AMO-D014); none is strictly best.

| Context | Control | Typical benefits | Typical risks and limits |
|---|---|---|---|
| **Pot** | depends on where the pot stands | mobility; plant can be moved between contexts | pot size constrains development — a naturally enormous species can remain small or develop poorly in an undersized pot |
| **Home** | high | control; reduced exposure to weather, some pests, discovery, theft and uncontrolled pollination | not a perfect safe zone — pests and other problems can still occur; limited space; pot limits apply |
| **Greenhouse** | stronger | stronger environmental control; greater capacity; a natural target for long-term player investment and progression | cost; still not risk-free (exact risks open) |
| **Outdoors** (suitable climate) | low | potentially better development, faster or less restricted growth, natural pollination opportunities, larger plants or stronger reproductive output | weather; pests and pathogens; environmental problems; discovery by other players; theft; unintended pollen transfer; unintended hybridization where the pair is approved as compatible |

Two consequences follow:

- **Species identity does not equal achieved size.** How large and vigorous a plant becomes is an outcome of genetics, effective environment, pot size and history.
- **Outdoors is where the drama is.** The best growth, natural pollination, exposure, theft and accidental hybrids all concentrate there.

Cultivation context is one of the things that turns a location environment into an effective environment; a pot, a room and a greenhouse are progressively more local environments, not exemptions from biology (AMO-D046, [12_ENVIRONMENT_AND_FIT_MODEL_V0.md](12_ENVIRONMENT_AND_FIT_MODEL_V0.md)).

The World also never blocks a player from taking a plant somewhere unsuitable. It states the conditions and the player judges the risk (L39, AMO-D051).

Property, greenhouse and home systems are open (AMO-Q032). Pests, pathogens and weather events are open (AMO-Q020).

## 6. Flowering and discoverability

A flowering plant becomes easier for other players to find, because of its scent (AMO-D015). The most spectacular moment in a plant's life is also its most exposed.

Possible future implementations include a detection radius, local reports or rumours, environmental clues, pollinator attraction, temporary map information, or approximate location signals rather than exact coordinates. **None is chosen** (AMO-Q015). Whatever is chosen must preserve the rule: *flowering can make a valuable outdoor plant easier for others to find.*

Flowering also connects to reproduction: pollination opportunities, pollinators (AMO-Q014) and accidental hybridization between approved compatible pairs (AMO-D027).

## 7. The human layer

The player is a human in the world, not a disembodied collector. Over time the player can:

- live in a house and use homes, gardens and greenhouses;
- travel and explore;
- discover, acquire and collect plants;
- trade with other people;
- cultivate, propagate and maintain collections, including pots;
- plant outdoors;
- interact with collectors and other players;
- build a personal history inside the world.

The human body is also where the player's consciousness starts and returns, and it stays physically in the world while they inhabit an Amorpho (AMO-D029). Two consequences belong to the world model:

- **Where the human body rests matters.** Astral transfer happens from a physical location, and the world continues around that location while the body is unattended (AMO-Q039, AMO-Q041).
- **Safe rooting locations are world infrastructure.** A player's own home need not be the only one. Other owned properties, greenhouses, suitable outdoor habitat, trusted friends' greenhouses and shared infrastructure may all serve, which makes cultivation infrastructure social and strategic rather than merely personal (AMO-Q043, AMO-Q046).

Who the "other people" are — other players, non-player characters, or both — is open (AMO-Q010), as are multiplayer topology (AMO-Q006), ownership (AMO-Q007), theft rules (AMO-Q008) and economy (AMO-Q009).

## 8. Deliberately not specified yet

- map scale, projection and level of detail;
- any map technology, geographic data source, streaming architecture or world-instance model;
- how cities, borders, interiors and wilderness are represented, and how much is authored versus procedural;
- the environmental variables and their resolution;
- any Environmental Fit formula;
- time compression;
- server or simulation architecture;
- how much of the world is simulated in detail at once.

Earth is the world (AMO-D045); *how* Earth is represented is exactly the part that stays open.

These should be decided through small experiments (see [07_INCUBATION_ROADMAP.md](07_INCUBATION_ROADMAP.md)), not up front.
