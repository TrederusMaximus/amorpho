# 02 — World Model

**Status:** conceptual. This document fixes the concepts and rules of the world. It deliberately does not specify scale, resolution, formulas or implementation. Where something is undecided it points to [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).

## 1. A persistent representation of Earth

The player exists as a human character in a persistent representation of Earth. Real geography and climate ground the world: continents, regions, cities and climates are recognisable, so that a plant's origin and journey mean something.

Cities and world geography exist independently of any individual player (AMO-D009). How faithfully and at what scale Earth is represented is open (AMO-Q001), as is how players travel (AMO-Q002) and how real places relate to player homes (AMO-Q003).

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

How initial populations are sized and placed is open (AMO-Q019). How a species added to the approved list later enters a live world is open (AMO-Q033).

## 4. Environment and Environmental Fit

Environmental Fit replaces country locks (AMO-D013). A species is neither allowed somewhere merely because it is native to that country nor forbidden everywhere else.

> **Terminology.** This concept was introduced at foundation as *suitability*. It is now called **Environmental Fit**, because the name has to carry an ownership boundary: the World describes conditions, the individual knows its own requirements, and Fit is derived from their interaction (AMO-D035, AMO-D036, AMO-D037). The full ownership model is in [10_WORLD_AMORPHO_EVOLUTIONATOR.md](10_WORLD_AMORPHO_EVOLUTIONATOR.md); this section covers the world side of it.

The concept has three parts:

1. **Location environment.** A place has environmental properties. Candidate properties include temperature range, seasonality, rainfall, moisture, dry season, light/shade and drainage — and perhaps soil or others where gameplay value justifies them. The final set is open (AMO-Q005). The World describes these conditions; it does not know whether they suit any particular plant (AMO-D035).
2. **Species tolerance profile.** Each species has a corresponding profile of what it tolerates and prefers, and each individual has its own condition and variation on top of that (AMO-D036). This is reality-derived knowledge. Once the environment model is designed, the approved input format will be extended with exactly the facts it needs (AMO-D025). No profile data exists yet, and none may be invented.
3. **Environmental Fit.** Comparing an effective environment with an individual yields what happens to it there. Fit is best thought of as graded rather than a simple allowed/forbidden switch, and its range genuinely extends into the positive: an environment may cause deterioration, hold an individual in equilibrium, or let it recover, grow and improve (AMO-D033, AMO-D037). Fit is **not** a synonym for stress. The exact form — continuous or tiered — is undecided.

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
- the environmental variables and their resolution;
- any Environmental Fit formula;
- time compression;
- server or simulation architecture;
- how much of the world is simulated in detail at once.

These should be decided through small experiments (see [07_INCUBATION_ROADMAP.md](07_INCUBATION_ROADMAP.md)), not up front.
