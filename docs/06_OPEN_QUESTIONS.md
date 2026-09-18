# 06 — Open Questions

This register lists what is **not decided**. Nothing here is design law. Accepted rules live in [DECISIONS.md](DECISIONS.md) and [01_DESIGN_PRINCIPLES.md](01_DESIGN_PRINCIPLES.md); each question lists the accepted decisions that constrain its answer.

## How to use this register

- IDs (`AMO-Q###`) are permanent and never reused.
- Statuses: **OPEN** (undecided), **EXPLORING** (actively being investigated; say where), **RESOLVED → AMO-D###** (answered; the answer is recorded as a decision). Resolved questions stay in the register.
- *Notes* record considerations and candidate options. A candidate is not a decision, however attractive it looks.
- Add new questions freely. Resolving one is a deliberate act: write the decision, then update the status here.

---

## World and geography

### AMO-Q001 — World map scale and representation
**Status:** OPEN · **Constraints:** AMO-D009, AMO-D013
How faithfully, at what scale and at what level of detail is Earth represented? Full-scale, compressed, region-based, abstracted network of places?
*Notes:* Drives almost every technical decision (streaming, persistence, simulation cost, travel). Should be answered by experiment, not assumption.

### AMO-Q002 — Travel model
**Status:** OPEN · **Constraints:** AMO-D009, AMO-D010
How do players move around the world: continuous travel, fast travel, travel with time or cost, transport of plants (including risk in transit)?
*Notes:* Travel cost is what gives plant movement and provenance meaning.

### AMO-Q003 — Real-world geography, cities and player homes
**Status:** OPEN · **Constraints:** AMO-D009, AMO-D013
How are real cities and places represented? Where can player homes be, and how are they allocated?
*Notes:* The game must never map player homes to players' real-world addresses or reveal players' real locations. Discovery and theft mechanics (AMO-D015, AMO-Q008) make this a safety concern, not only a design one.

### AMO-Q004 — Time scale
**Status:** OPEN · **Constraints:** AMO-D009, AMO-D012
How does world time relate to real time? How are real plant timescales (not Amorpho's to research; they would arrive as approved input if needed) compressed into play? Do seasons and hemispheres follow reality?
*Notes:* Tension between meaningful long-term history and session-sized play. Multi-generation lineages (AMO-D012) require generations to be reachable within a player's lifetime in the game.

### AMO-Q005 — Environmental model: variables and resolution
**Status:** OPEN · **Constraints:** AMO-D013
Which environmental variables are modelled, at what spatial and temporal resolution, and how is suitability computed?
*Notes:* Candidates: temperature range, seasonality, rainfall, moisture, dry season, light/shade, drainage, perhaps soil. Species tolerance facts are reality-derived: once this model is designed, the approved input format is extended with exactly the subset it needs (AMO-D025). No environmental fields exist until then.

## Society, multiplayer and economy

### AMO-Q006 — Multiplayer topology
**Status:** OPEN · **Constraints:** AMO-D009, AMO-D018
One shared world, several shards, private worlds, or a mix? Can the game be played offline? How do the persistent world and real-time combat relate technically?
*Notes:* Persistent-world authority and low-latency fighting have different technical needs; they may not share one solution.

### AMO-Q007 — Ownership
**Status:** OPEN · **Constraints:** AMO-D010, AMO-D011
What can a player own (plants, pots, homes, land, greenhouses), how is ownership established and transferred, and what happens to property of inactive players?
*Notes:* Inactive players' plants are part of a persistent world with finite populations; their fate affects everyone.

### AMO-Q008 — Theft rules and anti-griefing
**Status:** OPEN · **Constraints:** AMO-D014, AMO-D015
When, where and how can plants be stolen? What protections, consequences and recovery exist? How is harassment prevented?
*Notes:* Theft risk is part of the outdoor risk/reward law (L10), but must not make the game miserable or enable targeted harassment.

### AMO-Q009 — Economy and trade
**Status:** OPEN · **Constraints:** AMO-D010, AMO-D011
Currency, prices, markets, player-to-player trade, collectors, value of provenance.
*Notes:* Finite populations and persistent individuals create genuine scarcity; the economy needs protection against hoarding and exploitation.

### AMO-Q010 — Other people: players and non-player characters
**Status:** OPEN · **Constraints:** AMO-D009
Who are the collectors, traders and residents of the world? Players, non-player characters, or both? Do non-player characters own and move plants in the persistent world?

### AMO-Q011 — Business model
**Status:** OPEN · **Constraints:** AMO-D003, AMO-D008, AMO-D010
How is Amorpho funded and sold?
*Notes:* Not discussed at foundation. Any model must not undermine scarcity (L8) or skill-based combat (L15). Any link between in-game plants and real plants is outside the game architecture (AMO-D018) and has legal and ethical implications.

## Plants and biology

### AMO-Q012 — Plant simulation depth
**Status:** OPEN · **Constraints:** AMO-D003, AMO-D011, AMO-D012
Which life-cycle stages, growth processes and care actions are simulated, and in how much detail?
*Notes:* Real life-cycle facts per species are not Amorpho's to research and must not be assumed; if a system needs them, they arrive as approved input (AMO-D025).

### AMO-Q013 — Genetic abstraction
**Status:** OPEN · **Constraints:** AMO-D012, AMO-D027
How are genotype and inheritance represented? Discrete genes, continuous trait values, a hybrid of both? How many traits, and which ones affect gameplay?
*Notes:* Must support within-species variation and emergent lineages while remaining playable.

### AMO-Q014 — Pollinator abstraction
**Status:** OPEN · **Constraints:** AMO-D015, AMO-D027
Are pollinators simulated, abstracted as a probability field, or represented otherwise? How far does pollen travel?

### AMO-Q015 — Scent and discovery mechanics
**Status:** OPEN · **Constraints:** AMO-D015
How does flowering make a plant discoverable: detection radius, local reports, environmental clues, pollinator attraction, temporary map information, approximate signals?
*Notes:* Must preserve the law while respecting AMO-Q003 and AMO-Q008.

### AMO-Q016 — Game handling of changes in the approved species list
**Status:** OPEN · **Constraints:** AMO-D004, AMO-D005, AMO-D022, AMO-D024
Taxonomy is decided outside Amorpho (AMO-D024); the game question is what happens *in Amorpho* when the approved list changes. What happens to existing individuals, lineages and fighter identities if a species ID leaves the approved list, or if the external process later treats two approved species as one, or one as two? May the approved list contain infraspecific taxa (subspecies, varieties) as separate entries?
*Notes:* Renames are already handled: the `AMO-SP-` ID stays and only the name changes (AMO-D022). Until this is answered, an approved export that drops an existing ID is not accepted automatically (see `data/input/README.md`).

### AMO-Q017 — Species ID convention
**Status:** RESOLVED → AMO-D022
Should species IDs be readable (derived from the name) or opaque?
*Resolution:* Opaque, permanent IDs of the form `AMO-SP-000001`, never derived from the scientific name.

### AMO-Q018 — Hybrid fertility and later-generation hybrids
**Status:** OPEN · **Constraints:** AMO-D025, AMO-D027
Can hybrid individuals reproduce further — backcross to a parent species, or cross with other species or hybrids? An approved species pair does not answer this. If the game needs it, what is the minimal approved input that would express it?
*Notes:* Research into hybrid fertility stays outside Amorpho (AMO-D024). The conservative default is that nothing beyond approved species pairs is possible.

### AMO-Q019 — Initial populations and native ranges
**Status:** OPEN · **Constraints:** AMO-D009, AMO-D010, AMO-D013
Where are natural populations at world start, how large are they, and which cultivated stocks exist? What minimal native-range information would the game need from approved input?
*Notes:* Native ranges are reality-derived and would arrive as approved input once a game system needs them (AMO-D025); population sizes are a design choice.

### AMO-Q020 — Pests, pathogens and weather events
**Status:** OPEN · **Constraints:** AMO-D014
Which problems exist, how they spread, and whether they reflect real organisms or are abstracted.

## Transformation and combat

### AMO-Q021 — The artifact: form, name and origin
**Status:** OPEN · **Constraints:** AMO-D007
What is the artifact (amulet, belt, something else)? What is it called, where does it come from, and what does it mean in the fiction? Also: the plural of "Amorpho", and the name of the act of awakening.

### AMO-Q022 — Transformation rules
**Status:** OPEN · **Constraints:** AMO-D007
What makes a plant suitable? How long does awakening last, what does it cost, where can it happen, and does it affect the plant afterwards?

### AMO-Q023 — Combat control model
**Status:** OPEN · **Constraints:** AMO-D008
Input scheme, input devices, motion inputs versus simplified inputs, accessibility options.

### AMO-Q024 — Combat camera and perspective
**Status:** OPEN · **Constraints:** AMO-D008
2D side view, 2.5D, full 3D arena, or something else?
*Notes:* Strongly coupled to animation cost, roster scale (AMO-Q027) and engine choice (AMO-Q036).

### AMO-Q025 — Whether and how cultivation affects combat
**Status:** OPEN · **Constraints:** AMO-D006, AMO-D008
Do size, health, age, lineage or care affect an Amorpho in combat? If so, how much?
*Notes:* Must not replace skill (L15). Too little influence disconnects the layers; too much turns combat into a cultivation contest.

### AMO-Q026 — Death, loss and recovery
**Status:** OPEN · **Constraints:** AMO-D007, AMO-D011
Can combat harm or kill the plant? What is lost on defeat, and how does a plant recover?
*Notes:* Players may refuse to fight with plants they have raised for years if the stakes are too high.

### AMO-Q027 — Roster scale versus combat content
**Status:** OPEN · **Constraints:** AMO-D004, AMO-D005, AMO-D006
How are distinct fighters produced for a large real species list: bespoke kits, shared archetypes with species-specific identity, staged roster growth?

### AMO-Q028 — Where and against whom combat happens
**Status:** OPEN · **Constraints:** AMO-D008, AMO-D009
Player versus player, against non-player characters, arenas, the open world, tournaments? Is there ranked play?

## Player experience and progression

### AMO-Q029 — First-player onboarding
**Status:** OPEN · **Constraints:** AMO-D003
How does a new player enter the world, meet the artifact, and learn both layers without the game becoming educational software?

### AMO-Q030 — How a player obtains the first plant
**Status:** OPEN · **Constraints:** AMO-D010
Where does a new player's first plant come from, given that plants never spawn from nothing?
*Notes:* Needs a sustainable source that respects finite populations, even when many players join at once.

### AMO-Q031 — Progression
**Status:** OPEN · **Constraints:** AMO-D008, AMO-D014
What does a player progress in: skill, collection, property, reputation, knowledge, lineages? How do these relate?

### AMO-Q032 — Property and greenhouse systems
**Status:** OPEN · **Constraints:** AMO-D014
Houses, gardens and greenhouses as player investments: acquisition, capacity, upgrades, risks.

## Production and process

### AMO-Q033 — New approved species in a live world
**Status:** OPEN · **Constraints:** AMO-D004, AMO-D010, AMO-D017
When the approved species list gains a new species, how does it appear in a running world, and where do its first plants come from? How are players informed?
*Notes:* One candidate: newly added species appear as newly discovered wild populations in suitable regions — which mirrors how real species are described.

### AMO-Q034 — Content rating and tone
**Status:** OPEN · **Constraints:** AMO-D003
What is the target age rating and tone? The plants' appearance, names and smell invite crude humour; the concept also offers genuine wonder.

### AMO-Q035 — Art direction
**Status:** OPEN · **Constraints:** AMO-D004
Visual style for plants, Amorpho, humans and the world.
*Notes:* Must make real species recognisable while allowing fantasy.

### AMO-Q036 — Engine and technology choice
**Status:** OPEN · **Constraints:** AMO-D020
Which engine or technology stack, and is it one stack or several (for example world and combat)?
*Notes:* Decide from evidence, using the criteria in [08_CONCEPTUAL_ARCHITECTURE.md](08_CONCEPTUAL_ARCHITECTURE.md#engine-and-technology-decision-criteria).

### AMO-Q037 — Target platforms
**Status:** OPEN · **Constraints:** AMO-D008
PC, consoles, mobile? Affects controls, performance budgets and networking.

### AMO-Q038 — Automating approved-input validation
**Status:** OPEN · **Constraints:** AMO-D018, AMO-D020, AMO-D026
Should validation of approved input files be automated, and if so, with what tool or language? Rules are documented in `data/input/README.md` and can be checked by hand for now.
*Notes:* Decide when manual checking becomes a burden. The choice should not force the engine choice.

---

## Suggested next to resolve

In rough order of value for the next phase:

1. **AMO-Q016** (changes in the approved species list) — needed before the second approved species export, not the first.
2. **AMO-Q013** and **AMO-Q012** (genetics, simulation depth) — shape the individual-plant model.
3. **AMO-Q025** and **AMO-Q026** (cultivation's effect on combat; loss) — decide whether the two layers reinforce each other.
4. **AMO-Q027** (roster scale) — decides whether the combat layer is producible at all.
5. **AMO-Q001** and **AMO-Q004** (world scale, time) — decide the cost of everything else.
