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
*Refined 2026-09-21:* the world **is** Earth (AMO-D045); what stays open is how Earth is represented. That includes global representation and streaming, how much detail cities and wilderness carry, how authored and procedural content mix (AMO-Q063), and how the game moves between global, regional and local scales. Fidelity may grow progressively without invalidating the structure above it.

### AMO-Q002 — Travel model
**Status:** OPEN · **Constraints:** AMO-D009, AMO-D010
How do players move around the world: continuous travel, fast travel, travel with time or cost, transport of plants (including risk in transit)?
*Notes:* Travel cost is what gives plant movement and provenance meaning.
*Refined 2026-09-21:* on a real Earth the distances are real, so this also covers how far travel is abstracted — between continents, between cities, and within a local area — and how transporting a plant differs from moving as a human or as an Amorpho (AMO-D045, AMO-Q046).

### AMO-Q003 — Real-world geography, cities and player homes
**Status:** OPEN · **Constraints:** AMO-D009, AMO-D013
How are real cities and places represented? Where can player homes be, and how are they allocated?
*Notes:* The game must never map player homes to players' real-world addresses or reveal players' real locations. Discovery and theft mechanics (AMO-D015, AMO-Q008) make this a safety concern, not only a design one.
*Refined 2026-09-21:* Earth is now the world (AMO-D045), which sharpens both halves. Open on the representation side: how countries, borders and cities are represented and named, and how player-created properties and interiors are placed inside real geography (AMO-Q064). Open on the safety side: real Earth geography must never imply anything about a player's real residential address — that separation is a requirement, and how it is maintained is the question.

### AMO-Q004 — Time scale
**Status:** OPEN · **Constraints:** AMO-D009, AMO-D012
How does world time relate to real time? How are real plant timescales (not Amorpho's to research; they would arrive as approved input if needed) compressed into play? Do seasons and hemispheres follow reality?
*Notes:* Tension between meaningful long-term history and session-sized play. Multi-generation lineages (AMO-D012) require generations to be reachable within a player's lifetime in the game.
*Refined 2026-09-20:* also covers the season model, since Environmental Fit varies with season and weather, not only with place (AMO-D035). Generation timing for the Evolutionator is tracked separately as AMO-Q052.

### AMO-Q005 — Environmental model: variables and resolution
**Status:** EXPLORING (version 0 specified in [12_ENVIRONMENT_AND_FIT_MODEL_V0.md](12_ENVIRONMENT_AND_FIT_MODEL_V0.md)) · **Constraints:** AMO-D013, AMO-D035, AMO-D036, AMO-D037, AMO-D046–AMO-D049
Which environmental variables are modelled, at what spatial and temporal resolution, and how is Environmental Fit computed?
*Notes:* Candidates: temperature range, seasonality, rainfall, moisture, dry season, light/shade, drainage, perhaps soil. Species tolerance facts are reality-derived: once this model is designed, the approved input format is extended with exactly the subset it needs (AMO-D025). No environmental fields exist until then.
*Refined 2026-09-20:* the ownership split is now decided (World describes, Amorpho requires, Fit evaluates — AMO-D035–AMO-D037); what remains open is the content on each side. Also covers weather, extreme events and how deep microclimates go. Substrate is tracked separately as AMO-Q050.
*Refined 2026-09-21:* version 0 answers the first cut — five neutral dimensions (temperature, water availability, light availability, air moisture, exposure/protection), local and time-dependent, with a specified Fit output contract (AMO-D046–AMO-D049). This question stays open for what v0 deliberately did not settle: spatial and temporal **resolution**, which further dimensions earn their place, and whether exposure/protection should decompose. Value representation is AMO-Q069, aggregation AMO-Q070, interactions AMO-Q071, time step AMO-Q074.

## Society, multiplayer and economy

### AMO-Q006 — Multiplayer topology
**Status:** OPEN · **Constraints:** AMO-D009, AMO-D018
One shared world, several shards, private worlds, or a mix? Can the game be played offline? How do the persistent world and real-time combat relate technically?
*Notes:* Persistent-world authority and low-latency fighting have different technical needs; they may not share one solution.

### AMO-Q007 — Ownership
**Status:** OPEN · **Constraints:** AMO-D010, AMO-D011
What can a player own (plants, pots, homes, land, greenhouses), how is ownership established and transferred, and what happens to property of inactive players?
*Notes:* Inactive players' plants are part of a persistent world with finite populations; their fate affects everyone.
*Refined 2026-09-21:* strategic establishment makes outdoor growing sites worth holding, sharing and protecting, so ownership now has to cover land and cultivation areas rather than mainly plants and buildings (AMO-D054, AMO-Q080).
*Refined 2026-09-21 ([15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md)):* ownership is now explicitly **one of five axes** — existence, ownership, custody, anchoring, availability — which may disagree and must not collapse into one field (AMO-D065). Wild, unowned, unanchored life is the default for natural populations (AMO-D064). The detailed ownership questions are AMO-Q093.

### AMO-Q008 — Theft rules and anti-griefing
**Status:** OPEN · **Constraints:** AMO-D014, AMO-D015
When, where and how can plants be stolen? What protections, consequences and recovery exist? How is harassment prevented?
*Notes:* Theft risk is part of the outdoor risk/reward law (L10), but must not make the game miserable or enable targeted harassment.
*Refined 2026-09-21 ([15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md)):* theft may now involve the plant, its **Astral Anchor**, or both, since Anchors are physical objects on the individual (AMO-D061). Physical possession is **not** assumed to grant astral access; rebinding is AMO-Q091. Note the interaction with dormancy: a deeply dormant tuber is naturally hard to find, so concealment is a real defence (AMO-D060).

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
*Refined 2026-09-21 (specified in [14_CURRENT_BIOLOGICAL_CONDITION_V0.md](14_CURRENT_BIOLOGICAL_CONDITION_V0.md)):* life-cycle phases now have an architectural home — **developmental state**, a separate axis from condition (AMO-D057) — but the **state machine is deferred to this question**. Dormant, active growth, flowering, reproductive and any other phases are undesigned, and no species' life-cycle facts are assumed or imported. Acclimation also sits in the condition layer of the response profile and remains part of this question.
*Refined 2026-09-21 ([15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md)):* five broad phases are now recognised (AMO-D059) and the state machine itself is tracked as **AMO-Q084**. This question keeps simulation *depth* — which processes are modelled and how finely — plus acclimation.
*Refined 2026-09-21:* also covers **acclimation** — whether and how an individual's response profile shifts with sustained exposure, which sits in the current-condition layer of the response profile (AMO-D048) and must stay distinct from genetic change (AMO-D039). Condition variables themselves are AMO-Q073.

### AMO-Q013 — Genetic abstraction
**Status:** OPEN · **Constraints:** AMO-D012, AMO-D027, AMO-D038, AMO-D039
How are genotype and inheritance represented? Discrete genes, continuous trait values, a hybrid of both? How many traits, and which ones affect gameplay?
*Notes:* Must support within-species variation and emergent lineages while remaining playable.
*Refined 2026-09-20:* this is the Evolutionator's core model (AMO-D038). It also covers recombination, mutation and variation mechanisms, inheritance probabilities, and where developmental plasticity sits relative to inherited traits — the latter being the boundary AMO-D039 protects.

### AMO-Q014 — Pollinator abstraction
**Status:** OPEN · **Constraints:** AMO-D015, AMO-D027, AMO-D054
Are pollinators simulated, abstracted as a probability field, or represented otherwise? How far does pollen travel?
*Refined 2026-09-21:* strategic establishment gives this a purpose beyond accidents outdoors — deliberately established individuals may be intended to reproduce (AMO-D054). Flowering timing and synchronisation are tracked as AMO-Q079.

### AMO-Q015 — Scent and discovery mechanics
**Status:** OPEN · **Constraints:** AMO-D015
How does flowering make a plant discoverable: detection radius, local reports, environmental clues, pollinator attraction, temporary map information, approximate signals?
*Notes:* Must preserve the law while respecting AMO-Q003 and AMO-Q008.
*Refined 2026-09-21 ([15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md)):* discoverability now varies by **life-cycle phase**. Bloom carries a strong signature at the moment an individual is most valuable; a deeply dormant unexposed tuber is normally undiscoverable without prior location knowledge, which is concealment rather than invisibility — someone who knows the pot or the site can still find it physically (AMO-D060). No generic world signal may reveal dormant tubers.

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
*Refined 2026-09-21:* with Earth as the world (AMO-D045), approved origin data could one day be placed in the corresponding real areas. The architectural ability to do so is preserved; no geographic facts are imported now and no geographic columns are added to the species input. How populations are represented spatially is AMO-Q068.

### AMO-Q020 — Pests, pathogens and weather events
**Status:** OPEN · **Conceptual acute-event handoff traced 2026-09-22** · **Constraints:** AMO-D014, AMO-D035, AMO-D037
Which problems exist, how they spread, and whether they reflect real organisms or are abstracted.
*Refined 2026-09-21 (evidence: [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md)):* this question now also carries **acute events** generally — a storm, a frost night, wind damage, an animal. The v0 environment vector models sustained conditions only and has nowhere to put a discrete occurrence. Exposure / protection gestures at vulnerability to exactly these, which is why that dimension could not be validated by sustained-condition scenarios (AMO-Q069). Answering this is therefore a precondition for judging whether exposure / protection earns its place.
*Refined 2026-09-22 ([23_ACUTE_EVENT_TO_LEAF_IMPAIRMENT_V0.md](23_ACUTE_EVENT_TO_LEAF_IMPAIRMENT_V0.md)):* an acute World occurrence and the exposure a particular rooted Leaf actually experiences are distinct. Local context and protection mediate exposure before biological susceptibility is evaluated. The World cannot assign Leaf damage. This question retains event content, occurrence and exposure representation; event-to-Leaf response belongs to AMO-Q086. The trace does not add a discrete event to the v0 environment vector or validate its provisional exposure/protection dimension.

## Transformation and combat

### AMO-Q021 — The artifact: form, name and origin
**Status:** OPEN · **Constraints:** AMO-D007, AMO-D029
What is the artifact (amulet, belt, something else)? What is it called, where does it come from, and what does it mean in the fiction? Also: the plural of "Amorpho", and the name of the act of awakening.
*Refined 2026-09-20:* the transfer may not depend on an object at all — a ritual room, an artifact, several artifacts, or a combination of place and object are all candidates. The lore question is tracked as AMO-Q039; this question remains the artifact-specific part of it.
*Refined 2026-09-21 ([15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md)):* the access path now has two physical halves — the human's **Warden artifact** and the **Astral Anchor** on the individual (AMO-D061). How they pair, and whether attachment alone suffices or a ritual is required, is AMO-Q089. This question stays the artifact's own form, name and origin.

### AMO-Q022 — Transformation rules
**Status:** OPEN · **Constraints:** AMO-D007, AMO-D028, AMO-D031, AMO-D032
What makes a plant suitable? How long does awakening last, what does it cost, where can it happen, and does it affect the plant afterwards?
*Refined 2026-09-20:* partly answered. Suitability now requires sufficient biological stability (AMO-D031), and awakening ends by rooting (AMO-D032). What remains open is duration, cost, and the finer rules — now tracked in more detail as AMO-Q042 (inhabitability and re-entry) and AMO-Q043 (rooting sites).

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
*Refined 2026-09-20:* a related question now exists outside combat — whether condition also affects what the animated Amorpho can do in the world, such as traversal tolerance (AMO-Q051). The two should be answered coherently, since both draw on the same individual condition (AMO-D030, AMO-D036).

### AMO-Q026 — Death, loss and recovery
**Status:** OPEN · **Constraints:** AMO-D007, AMO-D011, AMO-D030, AMO-D084
Can combat harm or kill the plant? What is lost on defeat, and how does a plant recover?
*Notes:* Players may refuse to fight with plants they have raised for years if the stakes are too high.
*Refined 2026-09-20:* combat is now only one of two routes to loss; environmental decline after rooting is the other (AMO-D033). Recovery, core damage and death as biological outcomes are tracked as AMO-Q045, and must be answered consistently with whatever combat does.
*Refined 2026-09-21 ([18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)):* the harm horizons are now fixed, so what combat must decide is **which horizon it touches** — manifestation integrity, vitality, reserves, stress, developmental maturity, or none. Whatever it touches recovers while the individual lives (AMO-D075), so combat cannot produce permanent injury without a new decision.
*Refined 2026-09-22 ([22_BIOLOGICAL_YEAR_WALKTHROUGH_V0.md](22_BIOLOGICAL_YEAR_WALKTHROUGH_V0.md)):* ordinary embodiment and combat use magical state while normal biology is suspended; they do not directly spend Tuber reserves or reduce vitality by default (AMO-D084). Defeat, forced exit and any explicitly exceptional consequence remain open; this question must not reintroduce an ordinary biological combat cost through the back door.

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
*Refined 2026-09-21 ([16_HUMAN_WARDEN_PROGRESSION_V0.md](16_HUMAN_WARDEN_PROGRESSION_V0.md)):* one strand is now named and separated: **human magical progression**, distinct from Amorpho biological progression and deliberately much slower (AMO-D066). Its first dimension is **Astral Capacity** (AMO-D067). The remaining strands — combat skill, collection, property, reputation, knowledge, lineages — and how they relate to each other and to the human strand are still open. Note that several of them advance at the world's pace rather than the human's, which is intentional.

### AMO-Q032 — Property and greenhouse systems
**Status:** OPEN · **Constraints:** AMO-D014, AMO-D029
Houses, gardens and greenhouses as player investments: acquisition, capacity, upgrades, risks.
*Refined 2026-09-20:* property now carries two further roles — it holds the unattended human body during astral transfer (AMO-Q041), and it is a safe rooting location that may belong to the player or to a trusted friend (AMO-Q046). How buildings modify local conditions is AMO-Q049.

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
**Status:** OPEN · **Constraints:** AMO-D020, AMO-D043
Which engine or technology stack, and is it one stack or several (for example world and combat)?
*Notes:* Decide from evidence, using the criteria in [08_CONCEPTUAL_ARCHITECTURE.md](08_CONCEPTUAL_ARCHITECTURE.md#engine-and-technology-decision-criteria).
*Refined 2026-09-20:* the candidate must also be able to support first-class VR eventually, without VR being built now (AMO-D043). That is a selection criterion, not a commitment to any VR technology.

### AMO-Q037 — Target platforms
**Status:** OPEN · **Constraints:** AMO-D008, AMO-D042
PC, consoles, mobile? Affects controls, performance budgets and networking.
*Refined 2026-09-20:* VR platforms are part of this question and tracked in more detail as AMO-Q062. No hardware commitment exists.

### AMO-Q038 — Automating approved-input validation
**Status:** OPEN · **Constraints:** AMO-D018, AMO-D020, AMO-D026
Should validation of approved input files be automated, and if so, with what tool or language? Rules are documented in `data/input/README.md` and can be checked by hand for now.
*Notes:* Decide when manual checking becomes a burden. The choice should not force the engine choice.

## Embodiment and astral transfer

### AMO-Q039 — Astral transfer: lore and mechanism
**Status:** OPEN · **Constraints:** AMO-D028, AMO-D029
What actually enables astral transfer? Is an amulet, a belt, another artifact, several artifacts, a ritual room, or a combination of place and object required? Where does the magic come from, and why can only some humans do it?
*Notes:* The ritual-room model is a strong current direction, not a decision. The artifact-specific part remains AMO-Q021. What is decided is only the consequence: the human body physically remains somewhere (AMO-D029).

### AMO-Q040 — Eligibility, permission and distance
**Status:** OPEN · **Constraints:** AMO-D028, AMO-D031
Which individuals may a player inhabit? Only plants they own? Can a plant owned by someone else be inhabited, borrowed or lent? Is transfer distance limited, and how is initiation gated?
*Notes:* Touches ownership (AMO-Q007) and social infrastructure such as a friend's greenhouse (AMO-Q046). Conservative default: only owned, eligible individuals.

### AMO-Q041 — The unattended human body
**Status:** OPEN · **Constraints:** AMO-D029
What can happen to the human body while the player inhabits an Amorpho? Can other players reach it or harm it? Can homes be entered? What protections exist, what happens if the transfer is interrupted, and how is harassment prevented?
*Notes:* Must be answered together with theft and anti-griefing (AMO-Q008) and with the safety constraint on player homes (AMO-Q003). The principle to preserve is that the body remains part of world reality (AMO-D029) — not that it must be vulnerable.
*Refined 2026-09-21 ([20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md](20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md)):* the metabolic side is now settled and **excluded from this question**: the trance is metabolically stable, and hunger, thirst or degeneration must never become a disguised astral countdown (AMO-D085). What remains open is genuine external threat — a reason to return only when something actually happens.

### AMO-Q042 — Inhabitability: threshold, granularity and re-entry
**Status:** OPEN · **Constraints:** AMO-D031, AMO-D034
Where is the line between inhabitable and merely alive? Is inhabitability binary or continuous? Does a moderately stressed plant become harder, riskier or costlier to inhabit rather than simply unavailable? What rules govern re-entry after emergency rooting?
*Notes:* No thresholds or state names may be fixed prematurely. The transition from astral rescue to physical rescue depends entirely on this answer.
*Refined 2026-09-21:* the evaluation path is now fixed — inhabitability derives from biological condition, never from the World or geography (AMO-D050). What stays open is the threshold itself, its granularity, and which condition variables feed it (AMO-Q073).
*Refined 2026-09-21 (specified in [14_CURRENT_BIOLOGICAL_CONDITION_V0.md](14_CURRENT_BIOLOGICAL_CONDITION_V0.md)):* the candidate inputs are now named — principally **vitality**, plausibly also **stress load** (AMO-D056). Inhabitability remains **derived, never stored**, and is not a fourth condition variable. The rule, the threshold and whether it is binary or continuous all remain open.
*Refined 2026-09-21 ([15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md)):* biological inhabitability is now one of **three** independent gates — the others being an Astral Anchor and life-cycle accessibility (AMO-D063). They fail for different reasons and are restored by different actions, so this question covers only the biological gate.

### AMO-Q043 — Valid rooting sites
**Status:** OPEN · **Constraints:** AMO-D032, AMO-D033
What counts as a place where an inhabited Amorpho can root and return to plant state? Its own pot, another pot, suitable substrate, a greenhouse bed, suitable outdoor soil, other cultivation infrastructure — and is bare unsuitable ground always possible, at a cost?
*Notes:* If rooting were possible only in prepared sites, emergency rooting would largely disappear; if possible anywhere, rooting infrastructure loses meaning. Relates to substrate (AMO-Q050).
*Refined 2026-09-21:* a valid rooting site is not only somewhere an individual *can* be left — for strategic establishment it is somewhere a player deliberately *chooses* (AMO-D054). The answer therefore has to serve emergency, operational and long-term establishment cases, which may have different requirements.

## Rescue and logistics

### AMO-Q044 — Environmental prognosis: what the player can know
**Status:** OPEN · **Constraints:** AMO-D034, AMO-D037
Before rooting, how much does the player learn about how the individual will fare there? Is the prognosis exact, approximate, uncertain, or learned through experience? Are forecasts available, and how reliable are they?
*Notes:* Certainty here decides whether rooting is a judgement call or a lookup. Too much information makes emergency rooting trivial; too little makes it arbitrary.
*Refined 2026-09-21:* the separation of **simulation truth** from **player knowledge** is now explicit (AMO-D051): the simulation may hold a trajectory without exposing certainty about it, and nothing assumes a visible countdown to non-inhabitability. The question is the information model — forecasts, sensors, cultivation knowledge, equipment, warnings, and how accurately a player can predict Fit before committing to a location or a rooting event.

### AMO-Q045 — Critical condition, recovery, core damage and death
**Status:** RESOLVED → AMO-D074, AMO-D075, AMO-D076 · **Constraints:** AMO-D031, AMO-D033, AMO-D034, AMO-D074
How does an individual recover from a critical state? Can some damage become permanent? How does plant death actually work, and is it ever instantaneous?
*Notes:* Must be coherent with whatever combat does to a plant (AMO-Q026). Permanent damage is powerful and risky: it raises stakes but can make players refuse to play.
*Refined 2026-09-21:* Fit's growth/recovery output makes recovery a first-class outcome rather than an exception (AMO-D049), so the open part is the **recovery model** — how fast, from how far down, and whether any damage is irreversible. Relates to AMO-Q072 and AMO-Q073.
*Refined 2026-09-21 (evidence: [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md)):* Scenario C walked recovery through two phases — restoring condition, then supporting development once baseline is reached — and the condition feedback loop means recovery firms up as it proceeds, then levels off. Irreversible damage remains entirely unmodelled: nothing in v0 prevents full recovery from any survivable state, which may or may not be the intent.
*Refined 2026-09-21 (specified in [14_CURRENT_BIOLOGICAL_CONDITION_V0.md](14_CURRENT_BIOLOGICAL_CONDITION_V0.md)):* this question now carries extra weight, because **it decides whether vitality needs to exist as stored state** (AMO-Q073, AMO-D056). If harm is always fully reversible, vitality could be derived from stress and reserves; if any harm is lasting, it cannot. The condition model also fixes the terms: stress load is *history*, not damage, so lasting damage — if it exists — would be a loss of vitality that does not return. Death's path `viable → deteriorating → critical → non-viable` is preserved, but whether death is a vitality threshold, a terminal developmental state or both remains open (AMO-D057).
*Refined 2026-09-21 ([15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md)):* the life-cycle architecture now **precedes** this question deliberately, and narrows it. Damage to a temporary manifestation ends with that manifestation; only damage to the **persistent core** is a candidate for permanence (AMO-D058, AMO-Q086). A further case now exists: if catastrophic core damage leaves a regenerating fragment, whether the result is the same individual is AMO-Q094.
*Resolved 2026-09-21 ([18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)):* **no harm is permanent while the individual lives.** Harm is classified by horizon — temporary manifestation damage, persistent core damage recorded in vitality, and reversible burden — and the classes differ in depth, cost and recovery duration, never in recoverability (AMO-D074, AMO-D075). **Death is the only permanently terminal outcome.** Vitality stays stored state, for a reason that no longer depends on permanence (AMO-D076). The earlier framing in this register — *whether any damage is irreversible* — is withdrawn. Recovery **dynamics** were not settled and moved to AMO-Q102; the death condition to AMO-Q104; treatment to AMO-Q105; in-phase repair to AMO-Q103.

### AMO-Q046 — Physical rescue: the human, and other players
**Status:** OPEN · **Constraints:** AMO-D029, AMO-D031
How does the human physically rescue a plant that can no longer be inhabited — retrieval, transport, repotting, treatment, relocation, controlled cultivation? Can friends rescue each other's plants, and on what permission?
*Notes:* This is what keeps the Human / World layer necessary (L23). Relates to travel (AMO-Q002), ownership (AMO-Q007) and distributed safe locations.

### AMO-Q047 — Amorpho-to-Amorpho rescue, carrying and transport
**Status:** OPEN · **Constraints:** AMO-D028, AMO-D030
Can an inhabited Amorpho rescue, carry, protect, transport or relocate another rooted Amorpho? Can it move a plant into better substrate, or carry it toward a greenhouse?
*Notes:* Follows naturally from the embodiment model and is explicitly **not** approved. It would be a significant new capability: it partially routes around the one-body constraint, so any answer must keep AMO-D028 meaningful.

### AMO-Q048 — Equipment at the moment of rooting
**Status:** OPEN · **Constraints:** AMO-D032
What happens to worn animated-state equipment when an Amorpho roots? Does it fall beside the plant, stay at the site, or go somewhere else? Who can pick it up, and can it be lost or stolen?
*Notes:* The law is fixed — equipment protecting the animated body does not automatically protect the rooted plant (AMO-D032). Only the inventory behaviour is open. Relates to theft (AMO-Q008).

## Environment and Environmental Fit

### AMO-Q049 — Controlled environments: buildings and greenhouses
**Status:** OPEN · **Constraints:** AMO-D014, AMO-D035
How do homes, greenhouses and other controlled spaces modify local conditions, and how deeply is an indoor environment simulated? How much control can a player exert, at what cost?
*Notes:* The architecture is decided: a building produces a modified local environment, evaluated by the ordinary mechanism — never a special rule such as `greenhouse makes tropical plant valid` (AMO-D035). What is open is fidelity and cost. Relates to AMO-Q032.
*Refined 2026-09-21:* a controlled environment modifies the five v0 dimensions and nothing else, so Fit never learns about buildings (AMO-D046, AMO-D047). Open: which dimensions a given structure can modify, how far, at what cost, and how reliably.
*Refined 2026-09-21 ([17_LIFE_CYCLE_STATE_MACHINE_V0.md](17_LIFE_CYCLE_STATE_MACHINE_V0.md)):* controlled environments may also influence **life-cycle timing** where biology permits — but only by changing conditions, to which biology responds. There is no `force_bloom` or `prevent_dormancy` flag, and none may be added (AMO-D070, AMO-D073).

### AMO-Q050 — Substrate and rooting medium
**Status:** OPEN · **Constraints:** AMO-D035, AMO-D036
Is substrate modelled at all, and if so how — soil type, drainage, quality, volume? Is it a World property, a property of a pot, or both?
*Notes:* Pot size already constrains development (AMO-D014). Substrate could extend that meaningfully or add depth nobody plays with. Real soil requirements per species are not Amorpho's to research (AMO-D024).
*Refined 2026-09-21:* the entry point is fixed — a container and its root zone extend the Local Environment State at the lowest level of the hierarchy, not as a separate system (AMO-D046). v0 adds no root-zone dimensions. Open: whether root volume, water state, drainage, substrate and root-zone temperature become dimensions of their own or modifiers of existing ones.
*Refined 2026-09-21 (evidence: [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md)):* now the **strongest candidate for the first extension**. In Scenario B, "healthy but developing slowly" could be caused by dim light or by an undersized pot, and the contract cannot tell them apart — yet pot size is an established constraint on development (AMO-D014). Root-zone temperature also became visible in Scenario A, where dry substrate under strong light would run hotter than the ambient value. Neither justifies a sixth environment dimension; both point at the root-zone layer.

### AMO-Q051 — Traversal, rooting and long-term suitability
**Status:** OPEN · **Constraints:** AMO-D032, AMO-D033, AMO-D037
How are the three environmental capabilities distinguished in practice: where an animated Amorpho can temporarily operate, where the individual can survive once rooted, and where it can genuinely persist, grow and reproduce? How much does equipment extend the first without touching the others?
*Notes:* They must never collapse into one `can live here / cannot live here` flag. This is the question behind *"I can travel here — but can I safely stop being Amorpho here?"* Relates to AMO-Q025 and AMO-Q005.
*Refined 2026-09-21:* v0 specifies the **rooted** evaluation and reserves a second context, *animated environmental response*, which would use the same World Environment plus animated-state protections and modifiers. That second model is undesigned. Long-term suitability is a question of trajectory sustained over time rather than a separate evaluation (AMO-D049).

## Evolutionator

### AMO-Q052 — Generation timing and selection strength
**Status:** OPEN · **Constraints:** AMO-D038, AMO-D040
How long is a generation in play terms, and how strongly does differential success translate into changed trait distributions? How many generations should a noticeable shift take?
*Notes:* Tightly coupled to time scale (AMO-Q004): lineages must be reachable within a player's playing life (L18 has no bearing here, but AMO-D012 does). Too strong and evolution becomes a stat button; too weak and it never becomes visible.

### AMO-Q053 — Populations, founder effects and divergence limits
**Status:** OPEN · **Constraints:** AMO-D005, AMO-D010, AMO-D038
How are populations modelled for inheritance purposes? How do founder effects work when a few individuals are moved somewhere new? How far may a lineage diverge while remaining the same species?
*Notes:* The divergence limit matters: a lineage is never a new species (AMO-D005), so the model needs a principled ceiling rather than an arbitrary cap.

### AMO-Q054 — Player-created lines: identity, naming and recognition
**Status:** OPEN · **Constraints:** AMO-D011, AMO-D040
Can players identify, name or formally register a line they have bred? Is there any recognition system for distinctive game-world lineages, and does the world track them independently of the player's claim?
*Notes:* Naming is a social and moderation question as well as a data one. "Knowing is not showing" applies (L14): the simulation may track lineages the interface never names.

### AMO-Q055 — Selection, lineage and hybridization interaction
**Status:** OPEN · **Constraints:** AMO-D027, AMO-D038, AMO-D040
How do selection and lineages interact with hybrids? Can a hybrid line be selectively bred, and does that depend on hybrid fertility?
*Notes:* Depends on AMO-Q018. Compatibility itself never changes through play: approved pairs come only from approved input (AMO-D027), and nothing in the Evolutionator may create or imply new pairs.

## Environment and Environmental Fit

These follow from [12_ENVIRONMENT_AND_FIT_MODEL_V0.md](12_ENVIRONMENT_AND_FIT_MODEL_V0.md). v0 is a boundary contract; these are the things it deliberately did not settle.

### AMO-Q069 — Value representation: units, normalisation, continuous or tiered
**Status:** OPEN · **Constraints:** AMO-D047, AMO-D048, AMO-D049
How are environmental values, response zones and fit results represented? Standard physical units per dimension, normalised abstract scales, or a mix? Is the internal model continuous, tiered, or continuous with categories exposed outward? Should exposure / protection decompose into more specific dimensions?
*Notes:* v0 deliberately chose nothing here. The seven labels in §10 of the model are documentation and UI vocabulary, not mandatory internal states, and nothing may lock an implementation to seven enumerated values. Physical units are a likely eventual representation for temperature and humidity; less obviously so for exposure. Exposure / protection is flagged as provisional precisely because a vague universal score can absorb every future variable and become meaningless.
*Refined 2026-09-21 (evidence: [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md)):* the worked scenarios used a synthetic 0.0–1.0 scale purely as a paper tool; it is **not** a candidate representation and nothing was decided from it. On **exposure / protection** the evidence is real: across a deteriorating, a stable and a flourishing case it never once decided an outcome. Diagnosis — it is a different kind of dimension from the other four, describing *vulnerability to events* rather than a continuously experienced condition, so sustained-condition scenarios cannot exercise it. Assessment: retain, scope clarified in the spec, **unproven rather than validated**, and genuinely testable only once acute events exist (AMO-Q020). Decomposition remains the likely eventual outcome.

### AMO-Q070 — Fit aggregation and limiting factors
**Status:** OPEN · **Constraints:** AMO-D049
How do per-dimension fits combine into a biological direction? What rule gives limiting factors their required weight without making every mildly poor dimension catastrophic?
*Notes:* The requirement is fixed: catastrophic failure in one dimension may not disappear behind excellent values elsewhere (AMO-D049). Candidate shapes include a minimum, a weighted minimum, a product, or a soft floor. None is chosen. The rule also has to leave room for the positive end of the range (L38) rather than only capping.
*Refined 2026-09-21 (evidence: [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md)):* the requirement is now **demonstrated rather than asserted** — Scenario A has four favourable dimensions and one past its critical boundary, and a naive mean reads ≈0.69, i.e. "favourable", for an individual dying of thirst. Two further constraints emerged: the rule must also gate **growth/recovery opportunity** (output D), since favourable warmth and light cannot be spent without water; and it must distinguish *concentrated* pressure (one dimension failed) from *diffuse* pressure (several mild shortfalls), which behave very differently. Still not resolved: which rule.

### AMO-Q071 — Representation of interactions between environmental factors
**Status:** OPEN · **Ownership half resolved 2026-09-21 → AMO-D055** · **Constraints:** AMO-D049, AMO-D055
**How** are interactions represented, now that where they live is settled? Interaction terms, response surfaces, conditional response curves, modifiers, nonlinear aggregation — or something else? How many interactions are worth modelling at all? How are they sourced, given that they are per-organism biology? How do interaction effects aggregate alongside single-dimension fits, and how is one ever explained to a player who can see that nothing individually looks wrong?
*Notes:* v0 treats dimensions independently and records this as an extension point. The architecture may not assume independence is permanent.
*Refined 2026-09-21 (evidence: [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md)):* **untested.** None of the three scenarios required two dimensions to combine, so the exercise provides no evidence either way. Scenario A came close — a dry root zone under strong light — but water had already decided the outcome, so no interaction was needed to explain it. This question needs a scenario built specifically to provoke it.
*Refined 2026-09-21 (evidence: [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md) §14–§22):* the scenario was then built. Raising temperature within its tolerable zone while holding water availability **identical** produced a materially worse trajectory — so interactions are real, and the case is expressible only as a Fit-side interaction. The **ownership half of this question is now resolved** (AMO-D055): physical, organism-independent interactions belong to World; interactions that change an organism's response belong to Fit, discriminated by asking whether the World could compute it without knowing what organism is present. Also settled: no sixth dimension and no new Fit output are implied, since an interaction is a relationship between existing dimensions. Two spec clarifications followed — output A is *independent* dimension fit, and output E may name an interaction as the binding constraint.
*What remains open:* the representation itself, how many interactions earn modelling, how they are sourced as approved biological data (AMO-Q076), how they aggregate (AMO-Q070), and how they are made explicable to a player. Also noted: **double-counting** is a live hazard whenever World later gains a physical process that Fit has been approximating (AMO-D055).

### AMO-Q072 — Exposure history and accumulation
**Status:** OPEN · **Constraints:** AMO-D048, AMO-D049
How is accumulated recent experience of conditions modelled, given that `brief cold ≠ prolonged cold` and `one dry interval ≠ sustained drought`? Does exposure history live in the individual's condition, in a separate accumulation layer, or in Fit's inputs?
*Notes:* v0 names the distinction between instantaneous environment and exposure history and defines no mathematics for it. This is likely a precondition for a credible recovery model (AMO-Q045) and for stress that feels biological rather than instantaneous.
*Refined 2026-09-21 (evidence: [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md)):* the scenarios show accumulation is already carried by **condition**, provided condition includes something like a stress load — so a separate exposure-history store may not be needed at this depth. The related clarification now in the spec is that stress pressure (output C) is a *rate*, with the accumulated total living in condition. Open: whether condition alone suffices, or whether recovery needs a richer history than a single accumulated value (AMO-Q073, AMO-Q102).
*Refined 2026-09-21 (specified in [14_CURRENT_BIOLOGICAL_CONDITION_V0.md](14_CURRENT_BIOLOGICAL_CONDITION_V0.md)):* **partially discharged.** Stress load now exists explicitly and carries the accumulation (AMO-D056), so no separate exposure store is needed at this depth. What remains is whether a single accumulated value is rich enough — in particular whether relief must be asymmetric with accumulation so that prolonged exposure is not erased by one favourable interval.

### AMO-Q073 — Condition dynamics and thresholds
**Status:** OPEN · **Variable set resolved 2026-09-21 → AMO-D056, AMO-D057** · **Constraints:** AMO-D048, AMO-D050, AMO-D056, AMO-D057
**How do the three condition variables move?** How does stress accumulate and relieve, and is relief symmetric with accumulation? When do reserves buffer versus fail? At what point does exceeded burden begin to cost vitality? How does condition narrow the effective response profile — the feedback function itself? And is vitality genuinely needed as stored state, or derivable?
*Notes:* Should be settled by what the Fit boundary genuinely requires, not by physiological ambition (AMO-D048). Fewer, broader variables are the conservative default. Relates to plant simulation depth (AMO-Q012) and the inhabitability threshold (AMO-Q042).
*Refined 2026-09-21 (evidence: [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md)):* three variables did real, distinguishable work across the scenarios — **health**, **stress load** and **stored resources**. Each was needed: resources to explain depletion under a critical constraint, stress load to carry accumulation, health to gate inhabitability. A **development or growth state** was also implied by Scenario C phase 2, where opportunity continues to be spent after recovery completes. Suggestive, not conclusive — one fictional value set is not a model. The exercise also confirmed condition sits on **both** sides of Fit, feeding the effective response profile and being modified by it.
*Refined 2026-09-21 (specified in [14_CURRENT_BIOLOGICAL_CONDITION_V0.md](14_CURRENT_BIOLOGICAL_CONDITION_V0.md)):* the **variable set is now resolved** — vitality, stress load and reserves, with developmental state as a separate axis (AMO-D056, AMO-D057). Tested against the four existing scenarios rather than new ones: a single `health` scalar fails Scenario C, since it saturates at healthy and leaves favourable Fit nothing to act on. No case required a fourth condition variable and none was left unexplained.
*Refined 2026-09-21 ([15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md)):* a second integrity concept may sit beside these — **phase-specific integrity** bounded by the current manifestation, distinct from persistent core vitality (AMO-D058, AMO-Q086). Whether it lives in condition, in developmental state, or beside both is open.
*What remains open:* the dynamics above and all thresholds.
*Refined 2026-09-21 ([18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)):* the stored-state question is **settled** — vitality stays stored (AMO-D076), but not because of permanence. Two individuals with identical stress and reserves may still differ in remaining core compromise, and no function of the other two can distinguish them once both have recovered. The earlier framing, that AMO-Q045 would decide it, is withdrawn.

### AMO-Q074 — Simulation time step and update frequency
**Status:** OPEN · **Constraints:** AMO-D046, AMO-D049
How often is environment recomputed and Fit re-evaluated, and at what granularity does condition accumulate? Does a plant nobody is watching update continuously, on a coarse schedule, or on demand?
*Notes:* v0 defines the shape `Condition(t + Δt) = Condition(t) + effects of Fit during Δt` and no rate. A persistent world full of individuals that develop unobserved (AMO-D009, AMO-D011) makes this a cost question as much as a design one. Coupled to world time scale (AMO-Q004) and to how populations are represented spatially (AMO-Q068).

### AMO-Q075 — Where randomness lives
**Status:** OPEN · **Constraints:** AMO-D052
Should the deterministic-evaluator position hold as the model matures? Which upstream systems own the randomness — weather, individual variation, stochastic events, pests, disease — and how much variation should two apparently similar plants show?
*Notes:* v0 takes the conservative position that Fit itself is deterministic for identical state and that randomness sits upstream, in the state being evaluated (AMO-D052). That is a claim about the evaluator, not about biology. Revisit if outcomes feel mechanical in a prototype.

### AMO-Q076 — Approved input for species response profiles
**Status:** OPEN · **Constraints:** AMO-D024, AMO-D025, AMO-D026, AMO-D053
Once the environmental model is settled enough to need them, what is the minimal approved input that expresses a species response profile? Which dimensions, which zones, and in what form?
*Notes:* Nothing may be imported before the consuming model exists (AMO-D053), and only what the game demonstrably needs may cross (AMO-D025). The research behind any such values stays outside Amorpho (AMO-D024). Note the shape problem: a per-species × per-dimension × per-zone table is considerably richer than the current two-column CSV, so this may be where CSV stops being sufficient (AMO-D026).
*Refined 2026-09-21 (evidence: [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md)):* the worked profiles make the shape concrete — five dimensions × three zones expressed as range boundaries, roughly twenty numbers per species before individual variation is considered. Whether approved input carries all of it, or only a baseline from which zones are derived, is part of this question. Nothing in the scenarios is importable: every value there is fictional and labelled as such.

## Human / Warden progression

These follow from [16_HUMAN_WARDEN_PROGRESSION_V0.md](16_HUMAN_WARDEN_PROGRESSION_V0.md) (AMO-D066–AMO-D069). Astral Capacity is the only confirmed dimension of human progression; nothing else is accepted.

### AMO-Q095 — Astral Capacity: values and curve
**Status:** OPEN · **Constraints:** AMO-D067, AMO-D068
What capacity does a player start with? Is there a maximum? How steeply does each further increase cost more, and how rare should high capacity be?
*Notes:* Fixed only that it accelerates and that `level N = N Anchors` is excluded (AMO-D068). This interacts with Anchor economy (AMO-Q090): if physical Anchors are plentiful, capacity is the binding constraint and its curve sets roster size alone; if Anchors are scarce, the two share the work. Which usually binds is itself undecided.

### AMO-Q096 — What advances a Warden
**Status:** OPEN · **Constraints:** AMO-D066
What actually produces human magical advancement — long-term experience, meaningful astral use, relationships with individual Amorphos, significant events, mastery, difficult milestones, story progression, something else? Is it accumulated or granted at milestones? Is it levels, ranks, stages, or a representation with no number at all?
*Notes:* The direction is that it must **resist trivial grind acceleration** (AMO-D066); the mechanism is entirely open, and conventional levelling is not assumed. A plausible tension to watch: anything measurable tends to become farmable, so the answer may need to be event- or milestone-shaped rather than quantitative.

### AMO-Q097 — World time, real time and human advancement
**Status:** OPEN · **Constraints:** AMO-D045, AMO-D066
Should human advancement be constrained by persistent world time or real elapsed time, rather than by gameplay activity alone?
*Notes:* Deliberately open **in both directions** — neither required nor forbidden. Real-time gating is a strong grind defence and an equally strong source of player frustration, so this should be settled with player experience in mind rather than by architecture. Relates to the world time scale (AMO-Q004).

### AMO-Q098 — Can Astral Capacity regress?
**Status:** OPEN · **Constraints:** AMO-D066
Can human progression ever be lost or reduced — through death, catastrophe, disuse, or a deliberate cost? Are there human death mechanics at all?
*Notes:* The default direction is to **avoid casually destroying long-term human progression**, since it is meant to be the slowest thing a player builds and the one constant across a lifetime of plants (AMO-D066). Any loss or regression needs its own explicit decision rather than arriving as a side effect of another system. Relates to loss generally (AMO-Q026).

### AMO-Q099 — Other human magical capabilities
**Status:** OPEN · **Constraints:** AMO-D069
Does human progression have dimensions beyond capacity — astral perception, transfer stability, richer Anchor information, ritual speed or reliability, sensitivity to life-cycle transitions, others? Does it touch combat at all?
*Notes:* **None of these is accepted**; they are recorded as possibilities so they are not reinvented as though new (AMO-D069). No skill tree exists or is implied. Any combat influence is constrained by skill remaining central to outcomes (L15, AMO-Q025). Adding a dimension should require the same justification a new environment dimension does: a demonstrated need, not a plausible idea.

### AMO-Q100 — Naming and communicating human progression
**Status:** OPEN · **Constraints:** AMO-D066, AMO-D068
What is this called player-facing — *Warden Progression*, *Astral Development*, *Astral Capacity*, something else? How is an increase presented so it reads as deep magical development rather than `+1 slot`?
*Notes:* Terminology is working-only and nothing is committed. Presentation matters more than usual here, because AMO-D068's whole intent is that an increase should feel significant; a curve alone will not carry that. No ceremony, ritual or interface is designed.

### AMO-Q116 — The active-phase productivity model
**Status:** OPEN · **Constraints:** AMO-D091, AMO-D081
How are **Leaf Functional Capacity** and **Remaining Productive Opportunity** represented? How does productive output integrate over an active phase into a persistent Tuber outcome? How much can early impairment be compensated later, and under what conditions?
*Notes:* Fixed: consequence follows function and opportunity rather than appearance, no structural-damage percentage may map directly to Tuber loss, and opportunity is **biological, not a UI countdown** (AMO-D091, L51). Opportunity is also **directional** — good late conditions cannot recreate productive time already gone, while good conditions after early damage may still salvage a season. Getting the integration wrong is costly either way: too forgiving and early damage never matters, too harsh and one bad week ends a year. Relates to in-phase repair (AMO-Q103) and premature retreat (AMO-Q087).
*Refined 2026-09-22 ([22_BIOLOGICAL_YEAR_WALKTHROUGH_V0.md](22_BIOLOGICAL_YEAR_WALKTHROUGH_V0.md)):* the same Leaf trace needs productive work to accumulate through changing Fit, brief embodiment pauses and temporary functional impairment, then inform a persistent outcome without a season-end award or automatic catch-up. The recovered branch and loss branch expose the missing integration rule; neither appearance nor timing alone supplies it.
*Refined 2026-09-22 ([24_SAME_PHASE_LEAF_RECOVERY_V0.md](24_SAME_PHASE_LEAF_RECOVERY_V0.md)):* this question consumes the **Leaf Functional Capacity trajectory** after AMO-Q103's same-Leaf recovery, or a later replacement Leaf state if AMO-Q084 permits it. It does not own stabilization, repair or the replacement trigger. Improved capacity affects future opportunity; it never restores productive time already elapsed.

### AMO-Q117 — Direct Tuber susceptibility, storage and transport
**Status:** OPEN · **Constraints:** AMO-D090, AMO-D093
What conditions harm a Tuber **directly**, with what duration and at what severity? What does an excavated or unrooted Tuber actually need, how long can it wait, and how is a transported individual's environment abstracted?
*Notes:* Fixed: direct harm may occur with no leaf present and bypasses the productivity pathway entirely, and **an excavated Tuber is neither automatically harmed nor in stasis** — *a biological Tuber does not become timeless because a Human is carrying it* (AMO-D090, AMO-D093). No harm mechanism, tolerance, timing or storage mechanic is defined; species tolerances must arrive as approved input, not be researched here (AMO-D024). This is where the Human transport layer gains real responsibility, so it should stay demanding enough to matter and forgiving enough not to punish ordinary handling. Relates to the time step (AMO-Q074) and substrate (AMO-Q050).
*Refined 2026-09-22 ([22_BIOLOGICAL_YEAR_WALKTHROUGH_V0.md](22_BIOLOGICAL_YEAR_WALKTHROUGH_V0.md)):* a dormant individual with no Leaf still experiences local conditions. The direct-harm side check reaches persistent Tuber loss without passing through Leaf productivity. This question must supply future susceptibility and handling rules without treating Deep Dormancy as biological stasis or excavation as automatic damage.

### AMO-Q118 — Where a neutral outcome becomes actual loss
**Status:** OPEN · **Constraints:** AMO-D092, AMO-D056
At what point does an insufficient season stop being *no gain* and become *regression*? How do reserve depletion and stress load relate to that crossing, and how does current condition modify susceptibility?
*Notes:* The **boundary is binary** — persistent loss did or did not occur — while severity beyond it is continuous (AMO-D092). Reserves buffer but are not a shield meter, and direct severe harm may bypass depletion entirely. Failed productivity *tends* to cost development while direct harm *tends* to compromise integrity — a tendency that must not become a fixed mapping. This decides how often a disappointing season is merely disappointing, which is a tone decision as much as a mechanical one (AMO-D082).
*Refined 2026-09-22 ([22_BIOLOGICAL_YEAR_WALKTHROUGH_V0.md](22_BIOLOGICAL_YEAR_WALKTHROUGH_V0.md)):* the recovered Leaf branch loses function and opportunity, uses reserves and experiences stress, yet has no pathological loss. The contrast branch posits actual maturity regression despite less dramatic appearance. A future rule must distinguish these outcomes without diagnosing pathology from reserve use, visible damage or missed expected growth.

## The magical layer

These follow from [20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md](20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md) (AMO-D084–AMO-D089).

### AMO-Q112 — Astral Readiness: representation, depletion and recovery
**Status:** OPEN · **Constraints:** AMO-D086, AMO-D084
How is readiness represented? What depletes it, and how fast? How quickly does rooted biological life restore it, and how much does Environmental Fit change that? Does it regenerate at all *while* embodied, or only once rooted? Can it be damaged independently of ordinary combat exhaustion?
*Notes:* Fixed: it persists across astral exit, it is not a view of any biological variable, rooted life is the fundamental recovery path, and recovery may be time-compressed (AMO-D086, L50). The "regenerates while embodied" question matters more than it looks — any regeneration at all makes indefinite embodiment self-sustaining, while none makes a long expedition a strictly worsening proposition. Relates to KO (AMO-Q113) and magical healing (AMO-Q114).

### AMO-Q113 — KO, collapse and forced exit
**Status:** OPEN · **Constraints:** AMO-D086, AMO-D072
What happens when an inhabited Amorpho is defeated or exhausted? Does it force astral exit, force rooting, simply deplete readiness, or something else? Where does the individual physically end up afterwards, and who decides?
*Notes:* Deliberately deferred until the biology–magic boundary existed, because the answer has to respect it: collapse is a **magical-layer** event and must not silently become biological harm (AMO-D084, L49). Note the interaction with rooting — an involuntary rooting in a hostile place is a very different consequence from a forced return to the human body (AMO-D033, AMO-Q043). Relates to combat loss generally (AMO-Q026).

### AMO-Q114 — Magical healing
**Status:** OPEN · **Constraints:** AMO-D086, AMO-D083
Does magical healing exist, and what does it reach — combat durability, status effects, short-term capability, and how far into Astral Readiness? Items, abilities, in-field regeneration, or none of these?
*Notes:* Fixed: *magic heals the fighter; biology heals the plant* — it must never directly restore leaf structure, Tuber vitality, developmental maturity or biological reserves (L48, AMO-D086). The open risk is readiness: healing that fully restores it would recreate the exit-and-re-enter exploit by another route (L50).

### AMO-Q115 — Astral Signal strength and location fidelity
**Status:** OPEN · **Constraints:** AMO-D088, AMO-D061
How strong is the signal in each phase, and what location fidelity does each strength provide? Exactly when does it fade through Senescence, how much residual signal remains in Early Dormancy, and at what point in Pre-Emergence does it return?
*Notes:* Fixed: the signal fades through senescence, is **absent in Deep Dormancy**, and returns in pre-emergence potentially before inhabitability does (AMO-D088). What is open is resolution and timing. The design tension is real: too precise and the Anchor becomes GPS, which AMO-D061 forbids; too vague and the senescence warning fails to give a player anything actionable. Interacts with the privacy constraint on locations (AMO-Q003) and with the Radar (AMO-Q092).

## Harm, recovery and maturity

These follow from [18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md) (AMO-D074–AMO-D078), which resolved the policy half of AMO-Q045.

### AMO-Q108 — Pathological Tuber Impact: the crossing into persistent loss
**Status:** OPEN · **Conceptually resolved 2026-09-22 → AMO-D090–AMO-D093** · **Constraints:** AMO-D074, AMO-D079, AMO-D090, AMO-D092
*Original question:* What determines when manifestation damage starts to affect persistent state? How does structural impairment translate into biological productivity in the first place — does a half-damaged leaf feed the individual half as well, or not proportionally at all? Does the threshold depend on current condition, so that the same damage crosses it for a depleted individual and not for a robust one? And can **prolonged moderate** impairment accumulate into core impact without any single catastrophic event?
*Notes:* The boundary is fixed and deliberately not numeric (AMO-D079).
*Refined 2026-09-21 ([19_DEVELOPMENTAL_MATURITY_V0.md](19_DEVELOPMENTAL_MATURITY_V0.md)):* the **Q106/Q108 split is now explicit**.
*Refined 2026-09-21 ([20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md](20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md)):* terminology is prepared, not answered. What crosses into the persistent Tuber is **Pathological Tuber Impact**, distinct from **Programmed Tuber Draw** — normal biological spending such as Bloom, which is not harm (AMO-D087). One further input is recorded: the **same leaf damage early and late in an active phase may have very different Tuber consequences**, because what matters is functional capacity, remaining productive opportunity, environment, time and condition. No rule such as *"up to 20% leaf damage has no persistent consequence"* may be introduced. **This question remains open.** AMO-Q106 owns what maturity is and what gain or loss *means* once persistent growth or loss has occurred; this question owns *when* harm crosses deeply enough to cause that loss. The maturity specification uses "Core Impact occurred" as an abstract trigger and deliberately does not solve for it, so nothing there should be read as defining this threshold.
*Conceptually resolved 2026-09-22 ([21_PATHOLOGICAL_TUBER_IMPACT_V0.md](21_PATHOLOGICAL_TUBER_IMPACT_V0.md)):* **Pathological Tuber Impact** is harmful loss of the persistent Tuber's integrity or accumulated development, reached by a **direct** pathway (the Tuber itself exposed or compromised, with or without a leaf present) or an **indirect** one (insufficient work by the active manifestation eventually causing actual loss), each of which may be **acute or cumulative** (AMO-D090). Crossing is judged by **outcome, not appearance**: no structural-damage percentage maps directly to Tuber loss, and consequence follows **Leaf Functional Capacity**, **Remaining Productive Opportunity**, Fit, condition and reserves — so identical visible damage early and late in a phase can produce opposite results (AMO-D091, L51). The diagnostic is that **persistent loss actually occurred**; reserve consumption, stress and lost expected growth do not qualify on their own (AMO-D092). A *Tuber Balance* concept was evaluated and rejected, because a blooming individual's balance is negative by design.
*What remains open:* the quantitative model — how productivity integrates over a phase (AMO-Q116), direct susceptibility and unrooted storage (AMO-Q117), and where a neutral outcome becomes actual loss (AMO-Q118). **Model completion is not numerical completion.** Two traps to avoid: making visible damage alone decide the crossing, which would turn a proportion of lost structure into a biological verdict; and making the threshold so high that manifestation damage never matters, or so low that every injury costs development. The accumulation question is the subtle one — if only single events can cross, a slow grinding season is free, which seems wrong. Relates to exposure history (AMO-Q072) and premature retreat (AMO-Q087).

### AMO-Q109 — How phase integrity alters a playable Amorpho
**Status:** OPEN · **Constraints:** AMO-D079, AMO-D008
How does damage to the current manifestation change the inhabited Amorpho — available skills, skill strength, durability, attack, movement, reach, or something else entirely?
*Notes:* Deliberately **downstream of the biological architecture** and belonging to character and combat design (AMO-Q026, AMO-Q086). What is fixed is only that such impairment can be substantial while leaving the persistent individual untouched (AMO-D079). Must respect skill remaining central to combat outcomes (L15), and must not become a stat-loss spiral that makes a damaged individual unplayable rather than merely harder to play.

### AMO-Q102 — Vitality recovery dynamics
**Status:** OPEN · **Constraints:** AMO-D075, AMO-D076
How fast does vitality recover, from how far down, and what conditions are required? How many life cycles should severe core compromise take to undo? Does **deep dormancy itself** ever assist recovery, hinder it, or neither?
*Notes:* The policy is settled — full recovery is always eventually possible while alive (AMO-D075) — and this is the dynamics. Getting it wrong is costly in either direction: too fast and core damage stops mattering, too slow and one bad season effectively removes an individual from play for a very long time. Preserve the deliberate asymmetry: stress and reserves recover substantially faster than severe vitality compromise. Relates to AMO-Q073 and AMO-Q074.

### AMO-Q103 — Repair within a manifestation
**Status:** OPEN · **Mature-Leaf concept resolved 2026-09-22 → AMO-D094** · **Constraints:** AMO-D074, AMO-D094
How much and how quickly can a damaged current Leaf or Bloom recover *during* its own manifestation, under which biological conditions? How are stabilization, compensation and any structural repair represented?
*Notes:* Fixed: biological recovery of the individual is not repair of the current structure, and a new manifestation never inherits the old one's damage (AMO-D074). Too much in-phase recovery would make manifestation damage inconsequential; none at all could let one bad event dominate a whole season.
*Refined 2026-09-21 ([18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)):* answering this shapes AMO-Q108 too — if in-phase repair is possible, prolonged moderate impairment is less likely to accumulate into core impact, because the individual can partly climb back out.
*Conceptually resolved for a mature Leaf 2026-09-22 ([24_SAME_PHASE_LEAF_RECOVERY_V0.md](24_SAME_PHASE_LEAF_RECOVERY_V0.md)):* same-Leaf recovery can stabilize and improve function without rebuilding lost mature architecture; a stable scarred Leaf can remain useful (AMO-D094). Initial recovery prospect is not actual recovery, and elapsed opportunity does not return. **Still open:** extent, rates, susceptibility, environmental and condition dependence, interruption by further exposure, representation, and whether/how Bloom repairs within its own manifestation. Replacement emergence is a **new Leaf**, not in-phase repair of the old one; AMO-Q084 owns that pathway's lifecycle routing and species scope, while AMO-Q101 owns its triggers. This question owns only change in the current manifestation before it ends.

### AMO-Q104 — The death condition
**Status:** OPEN · **Constraints:** AMO-D075, AMO-D076
What exactly constitutes loss of biological viability? Is death a vitality threshold, a terminal developmental outcome, or something at the intersection? Can it ever be instantaneous?
*Notes:* Death is the **only** permanently terminal outcome (AMO-D075), which makes its boundary unusually consequential — everything short of it must be recoverable. Must be coherent with fragment survival, which is explicitly *not* death while living continuity remains (AMO-Q094). Relates to AMO-Q026.

### AMO-Q105 — Treatment and care
**Status:** OPEN · **Constraints:** AMO-D075, AMO-D054
Beyond providing favourable conditions, can a human actively treat a compromised individual — and if so how? Is recovery purely environmental, or is there a care layer with actions, resources and skill?
*Notes:* Currently recovery is entirely a matter of Environmental Fit over time (AMO-D049). A treatment layer would give the human layer another essential role (L23) and make rescue an activity rather than a relocation — but it risks becoming a consumable-item minigame that short-circuits the environmental model. Relates to physical rescue (AMO-Q046).

### AMO-Q106 — Developmental Maturity: internal representation and rates
**Status:** OPEN · **Definition, growth and regression rules resolved 2026-09-21 → AMO-D080–AMO-D083** · **Constraints:** AMO-D077, AMO-D080, AMO-D081, AMO-D082
How is the continuous axis actually represented internally? How fast does maturity accrue from persistent surplus, and how is that surplus recognised? What is the relationship between reserves and growth in practice? How steep can regression be, and what starting maturity does a new individual have?
*Notes:* Fixed: it is biological development, **not** experience points, emerging from successful life cycles, favourable growth and condition rather than from activity (AMO-D077, L47). Open: everything quantitative, plus the name itself. The regression rule is the delicate part — it gives premature retreat its price, and it is what can cost a player years of cultivation without costing them the individual.
*Refined 2026-09-21 ([18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)):* one boundary is now fixed before this question is answered: maturity must **not** regress merely because a manifestation is damaged. `Leaf integrity loss` and `maturity loss` are different events, and regression requires crossing the Core-Impact Threshold (AMO-D079). Any regression rule that reads directly off structural damage is wrong by construction.
*Refined 2026-09-21 (specified in [19_DEVELOPMENTAL_MATURITY_V0.md](19_DEVELOPMENTAL_MATURITY_V0.md)):* **definition, growth and regression are resolved** — one continuous species-relative axis; growth from persistent biological surplus via the chain `Fit → opportunity → condition/reserves/growth → development`, never awarded directly; regression only on Core Impact; lost opportunity distinct from regression; healing distinct from regrowth (AMO-D080–AMO-D083). What remains is everything quantitative: representation, rates of gain and regression, how surplus is recognised, the reserves-to-growth relationship, and a new individual's starting point. Presentation is AMO-Q111 and species interpretation AMO-Q110.
*Refined 2026-09-22 ([21_PATHOLOGICAL_TUBER_IMPACT_V0.md](21_PATHOLOGICAL_TUBER_IMPACT_V0.md)):* the trigger this question abstracts is now specified: **Pathological Tuber Impact**, judged by whether persistent loss actually occurred, reached directly or indirectly (AMO-D090, AMO-D092). Maturity regression is one of its two possible outputs alongside vitality reduction, in no fixed proportion.

### AMO-Q110 — Species interpretation of maturity
**Status:** OPEN · **Constraints:** AMO-D080, AMO-D024, AMO-D053
How does a species profile turn a maturity coordinate into biological expression — manifestation scale, flowering threshold, Bloom scale, development potential? How does maturity map to physical size for a given species, and what minimal approved data would any of it need?
*Notes:* Fixed: maturity is **species-relative** and never directly comparable across species, and it is deliberately **not equated with any single physical measure** — height, span, diameter or mass may be *derived* per species, which is what stops one universal metric from failing across very different species (AMO-D080). No profile schema exists, nothing is researched, and the species CSV is untouched (AMO-D024, AMO-D053, AMO-Q076). Note the trap: a shared physical scale would be much easier to implement and would quietly reintroduce exactly the cross-species comparison this forbids.

### AMO-Q111 — Presenting maturity to players
**Status:** OPEN · **Constraints:** AMO-D080, AMO-D068
What does a player actually see — rough size or maturity bands, visual manifestation, Bloom readiness, biological indicators, or a precise figure? How is a slow axis made legible without turning it into a progress bar?
*Notes:* The simulation may hold a precise internal quantity while the player sees something coarser; presentation is deliberately undecided (AMO-D080). The risk is specific: displayed as a number that visibly ticks up, maturity will read as experience points no matter what the documentation says (L47). Relates to how human progression is communicated (AMO-Q100) and to knowing-is-not-showing (L14).

### AMO-Q107 — Bloom eligibility inputs and repeated-Bloom timing
**Status:** OPEN · **Constraints:** AMO-D078, AMO-D059
Beyond passing the flowering-maturity threshold, what determines whether a given cycle produces a Bloom — condition, reserves, life-cycle routing, environment, species biology, chance? How often can Bloom recur, and does it cost enough to make recurrence self-limiting?
*Notes:* Fixed: maturity **enables** but does not guarantee, and Bloom is repeatable rather than a one-time unlock (AMO-D078). Roughly annual recurrence is possible where future species data supports it but is **not** assumed universal, and no interval exists. This decides whether Bloom stays rare in practice — a gate easy to pass every cycle would make it ordinary, which AMO-D059 forbids. Relates to AMO-Q101 and AMO-Q079.

## Life cycle, anchors and availability

These follow from [15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md) (AMO-D058–AMO-D065).

### AMO-Q084 — Life-cycle parameterisation and species variation
**Status:** OPEN · **Base topology resolved 2026-09-21 → AMO-D070, AMO-D071** · **Constraints:** AMO-D024, AMO-D059, AMO-D070, AMO-D094
How is the topology **parameterised** per species? Do some species never enter deep dormancy, or never bloom? Can leaf and bloom ever be occupied at once? What routing governs entry into and exit from the Active family, and what durations does any of it have?
*Notes:* v0 recognises five broad phases (AMO-D059) and deliberately stops there. Real life-cycle facts are not Amorpho's to research and arrive only as approved input if a system needs them (AMO-D024, AMO-D025). Overlaps plant simulation depth (AMO-Q012) and what a rooted individual does over time (AMO-Q077).
*Refined 2026-09-21 ([17_LIFE_CYCLE_STATE_MACHINE_V0.md](17_LIFE_CYCLE_STATE_MACHINE_V0.md)):* the **base topology is resolved** — seven states in three families, with Bloom a sibling active state rather than a linear stage or an overlay, and premature retreat needing no separate state (AMO-D070, AMO-D071). What remains is everything species-shaped: routing, durations, whether dormancy is universal, whether concurrency is ever needed. The structure was chosen so each can be added without restructuring. No species' real cycle may be assumed, and no input format is designed (AMO-D024, AMO-Q076).
*Refined 2026-09-22 ([24_SAME_PHASE_LEAF_RECOVERY_V0.md](24_SAME_PHASE_LEAF_RECOVERY_V0.md)):* this question owns **replacement emergence** as a possible new Leaf manifestation during a disrupted active period, distinct from ordinary next-cycle emergence (AMO-D094). Open: whether the existing seven-state graph expresses it within Active Leaf or needs a routed emergence, species scope, when in the phase it remains possible, how old and new Leaf overlap, and how a reduced replacement form is determined. This is no guarantee of replacement. AMO-Q101 owns the trigger and required biological capacity; AMO-Q085/AMO-Q115 own access and signal during the handoff. Approved reality input must eventually determine species scope; none is imported here.

### AMO-Q101 — Life-cycle transition triggers
**Status:** OPEN · **Constraints:** AMO-D035, AMO-D037, AMO-D070
What actually causes a transition between life-cycle states? How do developmental progress, Environmental Fit, reserves, current condition, internal cycle timing and species biology combine, and with what weight?
*Notes:* v0 names the **input categories only** and defines no formula (AMO-D070). The ownership boundary is the constraint that matters: Environmental Fit may push toward continued activity, recovery, developmental progression or premature retreat, but **Fit does not become the life-cycle system** (AMO-D035–AMO-D037). Premature retreat is the same Senescence transition arriving early, so this question also governs how early is too early (AMO-Q087).
*Refined 2026-09-22 ([24_SAME_PHASE_LEAF_RECOVERY_V0.md](24_SAME_PHASE_LEAF_RECOVERY_V0.md)):* also owns **whether and when replacement emergence is triggered** instead of continued use of the old Leaf or premature retreat. Candidate influences include Tuber condition, reserves, timing, maturity, Fit and remaining opportunity; none is a rule or threshold. Replacement routing and species scope remain AMO-Q084.

### AMO-Q085 — Astral access windows across the life cycle
**Status:** OPEN · **Constraints:** AMO-D060, AMO-D063
Where exactly does the astral door close and reopen? Is there a transitional window after dormancy entry during which entry remains possible, and does accessibility return before emergence? What marks the boundary of deep dormancy, and what warning does the player get?
*Notes:* Only the extreme is decided: **deep dormancy is closed** (AMO-D060). The windows are a current design direction, not a rule, and if they exist they may create distinctive tuber and transition gameplay. Dormancy entry should normally give visible biological warning rather than a bare *unavailable* (AMO-D059) — what that looks like is part of this question.
*Refined 2026-09-21 ([17_LIFE_CYCLE_STATE_MACHINE_V0.md](17_LIFE_CYCLE_STATE_MACHINE_V0.md)):* the **shape** is now fixed — access is Open, Transitional or Closed, derived from state *and progress through it*, narrowing through Senescence and Early Dormancy to a closed floor at Deep Dormancy, then widening again through Pre-Emergence and Emergence (AMO-D070).
*Refined 2026-09-21 ([20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md](20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md)):* a second, independent curve now runs alongside access: the **Astral Signal**, which fades through senescence, goes silent in deep dormancy and returns in pre-emergence (AMO-D088). The two need not move together — an individual may be detectable but not enterable — so this question owns access and AMO-Q115 owns signal. What stays open is where within each transitional state the door actually closes and reopens. Also part of this question: transitions must be **legible enough to support decisions** — reallocating an Anchor, relocating an individual, timing a mission — rather than arriving as arbitrary lockouts (AMO-D073).
*Refined 2026-09-22 ([24_SAME_PHASE_LEAF_RECOVERY_V0.md](24_SAME_PHASE_LEAF_RECOVERY_V0.md)):* a replacement Leaf pathway also needs an access answer during its emergence and handoff from the old Leaf. No entry window or Warden transfer rule is inferred from ordinary next-cycle emergence; AMO-Q115 keeps Astral Signal and AMO-Q112 keeps Readiness.

### AMO-Q086 — Phase-specific abilities and damage
**Status:** OPEN · **Conceptual Leaf event-response handoff traced 2026-09-22** · **Constraints:** AMO-D056, AMO-D058, AMO-D074, AMO-D091
What does each playable phase actually do, and what integrity does it carry? Is there a leaf integrity, a bloom integrity, something else? How does damage to a temporary structure relate to persistent core vitality, and what does core compromise mean?
*Notes:* The architecture is reserved, not designed (AMO-D058): phase-specific integrity ends with its phase, core vitality persists. Must be answered coherently with combat consequences (AMO-Q026) and core damage (AMO-Q045). No formulas, magnitudes or stored-variable representation exists.
*Refined 2026-09-21 ([18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)):* the horizons are settled (AMO-D074) — a new manifestation never inherits the old one's structural damage, and no universal body-integrity meter exists. Still open: whether each phase needs a named integrity variable at all, and how much **in-phase repair** is possible (AMO-Q103).
*Refined 2026-09-21 ([18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)):* the crossing into persistent state is now bounded by the **Core-Impact Threshold** (AMO-D079, AMO-Q108), and the *gameplay* mapping — how integrity changes a playable Amorpho — is tracked separately as AMO-Q109. This question keeps the biological side: what integrity each phase carries, if any.
*Refined 2026-09-21 ([17_LIFE_CYCLE_STATE_MACHINE_V0.md](17_LIFE_CYCLE_STATE_MACHINE_V0.md)):* each state now has its own manifestation, so a per-state integrity has somewhere to attach (AMO-D070). Two further points: phase-specific damage **outlasts embodiment** — exiting and re-entering repairs nothing, because the damage belongs to the manifestation rather than the animation (AMO-D072) — and if transitional **tuber-form gameplay** ever exists it belongs to Early Dormancy or Pre-Emergence, never to deep dormancy (AMO-D060).
*Refined 2026-09-22 ([23_ACUTE_EVENT_TO_LEAF_IMPAIRMENT_V0.md](23_ACUTE_EVENT_TO_LEAF_IMPAIRMENT_V0.md)):* for a rooted Active Leaf, experienced acute exposure and individual susceptibility can produce a post-event manifestation state with **structural integrity** and **Leaf Functional Capacity** described separately. Same-phase recovery and immediate continuation are assessments, not mandated new stored variables. Exact susceptibility and structural-to-functional rules stay open here; AMO-Q103 owns in-phase repair, AMO-Q087/AMO-Q101 own retreat, AMO-Q109 owns combat mapping, and AMO-Q116 starts only when functional state feeds productive work. The trace defines no Bloom or dormant damage model.

### AMO-Q087 — Premature dormancy: triggers and costs
**Status:** OPEN · **Constraints:** AMO-D059, AMO-D056
What causes an individual to abandon its active phase early, and what does that cost — depleted reserves, a smaller resulting tuber, lost developmental progress, a reduced re-emergence?
*Notes:* Architecturally this is a **survivable failure with a lasting price**, distinct from both a minor setback and death — which is exactly the band the game most needs and has least of. No trigger or magnitude is defined.
*Refined 2026-09-22 ([21_PATHOLOGICAL_TUBER_IMPACT_V0.md](21_PATHOLOGICAL_TUBER_IMPACT_V0.md)):* premature retreat may be **protective** — abandoning a failing manifestation can be the reason Pathological Tuber Impact did *not* occur. It therefore never implies that it did, and this question covers both outcomes: a retreat that cost only opportunity and reserves, and one that still ended in persistent loss (AMO-D092).

### AMO-Q088 — Bloom: duration, abilities and trade-offs
**Status:** OPEN · **Constraints:** AMO-D015, AMO-D059
How long does Bloom last, what can a flowering individual do that others cannot, and what does it cost — reserve investment, discoverability, reproductive consequence, risk?
*Notes:* Decided: Bloom is rare, short and exceptional, a temporary superstate rather than a strictly better form (AMO-D059). Not decided: any of the content. It must not become "Leaf Form with better numbers", and it must not be universally optimal. Ties to flowering discoverability (AMO-Q015) and reproduction (AMO-Q079).
*Refined 2026-09-21 ([17_LIFE_CYCLE_STATE_MACHINE_V0.md](17_LIFE_CYCLE_STATE_MACHINE_V0.md)):* Bloom's **structural placement** is resolved — a sibling active state with its own manifestation, reached by parameterised routing (AMO-D071) — which is what lets it have a distinct kit and a distinct integrity without being a mandatory stage. Its content, cost, duration and post-Bloom routing all remain open.
*Refined 2026-09-21 ([18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)):* eligibility is now gated on **species-specific flowering maturity** (AMO-D078), and later Blooms may be larger and more developed as maturity grows. This question therefore also covers **manifestation scale** — how Bloom size relates to maturity, and whether Bloom-specific gameplay strength scales with it. Linear scaling is not assumed, and any scaling must not make Bloom strictly better (AMO-D059).
*Refined 2026-09-21 ([19_DEVELOPMENTAL_MATURITY_V0.md](19_DEVELOPMENTAL_MATURITY_V0.md)):* the threshold is now explicitly a **milestone on the Developmental Maturity axis**, not a separate quantity, and maturity keeps rising above it (AMO-D080). Any scaling rule is interpreted through the species profile (AMO-Q110), and none may produce a direct maturity-to-combat-power relationship (L15).

### AMO-Q089 — Astral Anchor: name, form, attachment and pairing
**Status:** OPEN · **Constraints:** AMO-D007, AMO-D061
What is an Anchor physically, how does it attach to an individual, and how does it pair with the human Warden artifact? Is attachment alone sufficient, or is a ritual required? Is "Astral Anchor" the final name?
*Notes:* "Astral Anchor" is working terminology. The artifact's own form and lore remain open (AMO-Q021). What is fixed is only that the Anchor is physical, reusable, and bound to the individual rather than to a pot or place (AMO-D061).

### AMO-Q090 — Anchor economy
**Status:** OPEN · **Constraints:** AMO-D061, AMO-D062
How many Anchors can a player have? How are they acquired — found, bought, crafted, granted? Can they be destroyed or lost? Do they differ in capability or grade?
*Notes:* Deliberately undecided, and consequential: Anchor supply is what turns roster composition into a real decision (AMO-D063). Too many and the constraint disappears; too few and the collection stops mattering. Only reuse and physical manipulation are accepted so far.
*Refined 2026-09-21 ([16_HUMAN_WARDEN_PROGRESSION_V0.md](16_HUMAN_WARDEN_PROGRESSION_V0.md)):* physical Anchor supply is now only **half** the constraint — **Astral Capacity** separately bounds how many active connections a human can sustain (AMO-D067). Two independent scarcity systems therefore exist, and this question covers the physical one. Whether they advance independently, and which usually binds, is open (AMO-Q095).

### AMO-Q091 — Anchor transfer, theft and rebinding
**Status:** OPEN · **Constraints:** AMO-D061, AMO-D062, AMO-D065
How does an Anchor change hands legitimately, and what happens when one is stolen along with its plant? Can a stolen Anchor be rebound to a new player, and under what conditions? Can an Anchor be stolen on its own?
*Notes:* Physical possession is **not** assumed to grant astral access (AMO-D065). This sits between theft rules (AMO-Q008) and ownership (AMO-Q093), and it must not become a way to bypass the human-hands rule (AMO-D062).
*Refined 2026-09-21 ([20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md](20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md)):* **explicitly still unresolved, and now more consequential.** Deep Dormancy silences the astral signal, so a dormant outdoor individual may be found, dug up, moved and its Anchor possessed with no live tracking to betray it (AMO-D088). Candidate models remain open: a Warden-specific Anchor a finder cannot use, a rebindable one, or conditional or difficult rebinding. Nothing is chosen.

### AMO-Q092 — The Astral Radar
**Status:** OPEN · **Constraints:** AMO-D061, AMO-D060
What does the player's astral interface actually expose — which individuals, what availability, what condition, what location precision? Does distance matter? Does deep dormancy weaken the signal or silence it entirely?
*Notes:* Fixed: it is a view of the player's own anchored connections, **not** a global botanical scanner, and not automatically a positioning system (AMO-D061). An anchored dormant individual may remain listed while unreachable, and its information may be deliberately minimal (AMO-D060). Interacts with the privacy constraint on locations (AMO-Q003).
*Refined 2026-09-21 ([16_HUMAN_WARDEN_PROGRESSION_V0.md](16_HUMAN_WARDEN_PROGRESSION_V0.md)):* greater **Astral Capacity** may mean more simultaneous connections shown, simply because more exist. It is explicitly **not** assumed to improve range, precision, positional information or biological sensing — those would be separate progression dimensions if they exist at all (AMO-D067, AMO-Q099).
*Refined 2026-09-21 ([17_LIFE_CYCLE_STATE_MACHINE_V0.md](17_LIFE_CYCLE_STATE_MACHINE_V0.md)):* the Radar may also need to express **life-cycle access status** — Open, Transitional or Closed — since an anchored individual can be connected but unreachable, and a narrowing window is exactly the kind of thing a player must see in time to act (AMO-D070, AMO-D073, AMO-Q085).
*Refined 2026-09-21 ([20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md](20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md)):* the Radar is a **resonance interface**, showing living astral connections whose information depends on **signal strength** — and during Deep Dormancy there is no signal at all, so an anchored individual simply disappears from it (AMO-D088). Strength, fidelity and timing are AMO-Q115.

### AMO-Q093 — Game ownership, release and custody
**Status:** OPEN · **Constraints:** AMO-D064, AMO-D065
What does ownership mean in game terms? Must every cultivated plant be owned? Does a released plant become ownerless immediately? What rights does a player have over offspring produced on their property, and how does custody by a friend or their greenhouse work?
*Notes:* Keep legal and social mechanics **separate** from astral mechanics (AMO-D065): astral access cannot change because an ownership field changed. Wild, unowned, unanchored life is the default state and must stay possible indefinitely (AMO-D064). Extends AMO-Q007 and relates to AMO-Q080.

### AMO-Q094 — Identity after severe core loss
**Status:** OPEN · **Constraints:** AMO-D011, AMO-D022, AMO-D058
If catastrophic core damage leaves a viable surviving fragment and it regenerates, is the result the **same persistent individual** or a **new clonal descendant** linked by provenance?
*Notes:* Both a gameplay and an identity-model question, and it now matters more than it first appears
*Refined 2026-09-21 ([19_DEVELOPMENTAL_MATURITY_V0.md](19_DEVELOPMENTAL_MATURITY_V0.md)):* the maturity model makes the two branches concrete. **If** continuity is accepted, maturity may collapse enormously while the individual lives, with a long rebuild ahead (AMO-D083). If the fragment is instead a new individual, it begins its own developmental history from scratch (AMO-D080). Either way nothing is permanent — but the two produce very different records, and that is the substance of the question.: identifiers are never reused (AMO-D011, AMO-D022), so the answer decides whether a lineage record can survive its own near-destruction — and whether a rare individual can ever truly be recovered. No botanical rule is encoded either way.
*Refined 2026-09-21 ([18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md)):* the surrounding model now sharpens this. Because living biological continuity never ended, fragment survival is **not** equivalent to death (AMO-D075), and regeneration is representable as an enormous developmental collapse that is nonetheless recoverable (AMO-D077). What stays open is identity itself — same individual, or new clonal descendant with provenance — which also determines **whether the original Astral Anchor remains valid** after fragmentation (AMO-D061, AMO-Q091).

## Establishment and long-term rooted life

These follow from AMO-D054: rooting may be strategic and long-term, and a rooted individual stays biologically active while the player is elsewhere.

### AMO-Q077 — What a rooted individual does over time
**Status:** OPEN · **Constraints:** AMO-D009, AMO-D054, AMO-D049
While rooted and unattended, what actually progresses — growth, size, structure, seasonal cycles, dormancy, flowering readiness, resource accumulation? How much of it is simulated when nobody is watching, and how much is derived on demand?
*Notes:* "Rooted does not mean inactive" is decided (AMO-D054); the content is not. Directly coupled to plant simulation depth (AMO-Q012), condition variables (AMO-Q073) and the simulation time step (AMO-Q074), and constrained by the cost of a persistent world full of developing individuals (AMO-Q068).

### AMO-Q078 — Seasonal routing and temporary bases
**Status:** OPEN · **Constraints:** AMO-D054, AMO-D046
How does a player plan around a location that is suitable only part of the year — travel there in a favourable window, use it as a base, and leave before conditions turn? What calendar, forecast and travel affordances does that require, and how is it kept from becoming a chore?
*Notes:* This is *operational rooting* made playable, and it is deliberate planning rather than an emergency. Depends on the time and season model (AMO-Q004), travel (AMO-Q002) and what the player can predict (AMO-Q044).

### AMO-Q079 — Flowering timing, pollination and reproductive opportunity
**Status:** OPEN · **Constraints:** AMO-D010, AMO-D015, AMO-D027, AMO-D054
What conditions make a rooted individual flower, and how do two individuals ever come to reproduce — flowering synchronisation, proximity, pollen movement, pollinators, scent dispersal? How much is natural and how much is player-directed?
*Notes:* Strategic establishment is what creates reproductive *opportunity*; this question is the mechanism that would use it. No pollination engine is designed (AMO-Q014 covers the pollinator abstraction and pollen distance). Hybridization policy is untouched and not negotiable here: approved pairs only, symmetric, and absence of approval never asserts biological impossibility (AMO-D027).

### AMO-Q080 — Player-created cultivation and population areas
**Status:** OPEN · **Constraints:** AMO-D010, AMO-D054, AMO-D045
If several players establish individuals in the same favourable region, what does that place become? How are access, use and protection of outdoor growing sites handled — owned land, shared infrastructure, a friend's greenhouse, or open habitat?
*Notes:* The emergent possibility is preserved; no ownership, land-rights or population mechanics follow (AMO-D054). Overlaps ownership (AMO-Q007), properties inside Earth geography (AMO-Q064), theft and anti-griefing (AMO-Q008) and spatial population representation (AMO-Q068). The provisional label *"Amorpho Farming"* is not a product term and no named subsystem exists.

### AMO-Q081 — Mission structure from biological geography
**Status:** OPEN · **Constraints:** AMO-D028, AMO-D054
Can objectives arise naturally from the combination of differing individual capabilities, differing environments, seasonal windows and one-body embodiment — for example needing a suitable individual routed into a region during a favourable season, or several positioned sequentially for use at different stages?
*Notes:* Recorded as a design possibility, explicitly **not** an accepted mission mechanic, and nothing may be hard-coded from the examples. Operations involving several individuals stay sequential, never simultaneous (AMO-D028). The attraction is that a small number of coherent rules would generate structure rather than scripting it (L37).

### AMO-Q082 — Availability of a rooted individual for later astral entry
**Status:** OPEN · **Constraints:** AMO-D028, AMO-D031, AMO-D050, AMO-D054
Under what conditions does an individual established far away remain available for future astral entry? Does distance, time, ownership, access or anything else besides biological condition affect it?
*Notes:* Biological condition already gates inhabitability (AMO-D031, AMO-D050). What is open is whether anything *else* does — transfer distance and eligibility (AMO-Q040) is the same question seen from the other end. If nothing else gates it, a distant established individual is permanently a body the player can step into, which is a large strategic fact worth deciding deliberately rather than by default.

### AMO-Q083 — Animated form and biological condition
**Status:** OPEN · **Constraints:** AMO-D030, AMO-D056, AMO-D084
Does being animated cost the individual anything biologically — reserves spent, stress added, vitality risked — and does condition change differently while inhabited than while rooted?
*Notes:* What is decided is that condition **persists across the transition**, because the rooted plant and the animated Amorpho are one individual (AMO-D030, AMO-D056): biological state does not vanish on animation. Whether animation is biologically free, costly, or even restorative is untouched. Closely tied to combat consequences (AMO-Q026) and to transformation cost generally (AMO-Q022); answering it would give the one-body law a biological price as well as a logistical one.
*Refined 2026-09-22 ([20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md](20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md), exercised in [22_BIOLOGICAL_YEAR_WALKTHROUGH_V0.md](22_BIOLOGICAL_YEAR_WALKTHROUGH_V0.md)):* the original ordinary-cost question is answered by AMO-D084: normal biology pauses while inhabited, and embodiment itself neither spends biological resources nor restores biological condition. The Warden's exit resumes rooted biology without resetting condition. This entry stays open only for any explicitly exceptional transfer or event consequence proposed later; ordinary animation must not be reopened as a biological drain.

## Earth representation

### AMO-Q063 — Local detail: authored versus procedural
**Status:** OPEN · **Constraints:** AMO-D045, AMO-D019
How is local detail produced — hand-authored places, procedural generation from geographic structure, or a mix that varies by importance? Which places deserve authored treatment?
*Notes:* Authoring the whole Earth is impossible; generating all of it risks a world with no memorable places. The answer probably differs between a species' origin region, a major city and an arbitrary field. Strongly coupled to AMO-Q001 and to production capacity (L19).

### AMO-Q064 — Properties and interiors inside Earth geography
**Status:** OPEN · **Constraints:** AMO-D045, AMO-D014
How do player-created properties, buildings, greenhouses and interiors sit inside real geography? Are they places in the world that others can reach, private spaces, or both? How is capacity and placement decided?
*Notes:* The principle is fixed — a house or greenhouse is a place *within* Earth, not a detached instance (AMO-D045) — so that outside conditions can reach inside (AMO-Q049). The representation is open. Overlaps ownership (AMO-Q007), property systems (AMO-Q032), theft (AMO-Q008) and the privacy requirement (AMO-Q003).

### AMO-Q065 — Nesting of local environments
**Status:** OPEN · **Constraints:** AMO-D035, AMO-D037, AMO-D045
How deep does environmental nesting go — world, city, property, building, room, pot, root zone — and where does it usefully stop? Does each level hold its own state, or is local state derived on demand from the level above plus modifiers?
*Notes:* The principle is that environmental state can exist at increasingly local scales, which is what lets a potted plant experience something different from the room and the street. Depth is a cost decision as much as a design one. Relates to AMO-Q005, AMO-Q049 and AMO-Q050.
*Refined 2026-09-21:* the contract is now fixed — every level produces the same five dimensions, so complexity can be inserted between levels without changing ownership (AMO-D046, AMO-D047). Open: how many levels actually exist, whether each holds state or derives it on demand from the level above plus modifiers, and where the cost stops being worth it.

### AMO-Q066 — How real geographic data could ever enter Amorpho
**Status:** OPEN · **Constraints:** AMO-D018, AMO-D024, AMO-D025, AMO-D045
If the game ever needs real geographic or climatic data, how would it arrive, and in what minimal form? Through the Reality Gate as approved input, as a one-time build-time asset, or not at all?
*Notes:* Nothing is imported now and nothing is chosen. Whatever the answer, the running game may not depend on an external service or live data source (AMO-D018), and only what the game demonstrably needs may cross (AMO-D025). Geography is not botanical research, so it may not belong to the same gate — that is part of the question.

### AMO-Q067 — World updates versus persistent player structures
**Status:** OPEN · **Constraints:** AMO-D009, AMO-D011, AMO-D045
When the World's geography or fidelity improves, what happens to player properties, plantings and populations already standing there? How are long-lived player structures protected across world changes?
*Notes:* Progressive fidelity (AMO-D045) guarantees this situation will arise. Persistent individuals with long histories (AMO-D011) are exactly what must not be lost to a map revision. Relates to AMO-Q007.

### AMO-Q068 — Spatial representation of populations
**Status:** OPEN · **Constraints:** AMO-D009, AMO-D010, AMO-D045
How are natural, cultivated and introduced populations represented in space — as individuals with locations, as population objects over an area, or at different resolutions depending on attention?
*Notes:* Finite populations (AMO-D010) and persistent individuals (AMO-D011) must survive whatever abstraction is chosen, including when nobody is looking. Relates to AMO-Q019, AMO-Q012 and AMO-Q053.

## Standard and VR gameplay

### AMO-Q056 — VR locomotion, comfort and posture
**Status:** OPEN · **Constraints:** AMO-D042
Teleport or smooth locomotion, or both? How is motion sickness handled? Is play room-scale, standing, seated, or all three?
*Notes:* Comfort options are not a nicety in a game meant to be inhabited for long sessions.

### AMO-Q057 — VR embodiment: human and non-human bodies
**Status:** OPEN · **Constraints:** AMO-D028, AMO-D029, AMO-D042
How is the player's body represented in VR — hands, full avatar, something else? And how is an Amorpho body embodied, given that it need not resemble a human at all?
*Notes:* The harder half is the non-human one: a plant body may have no arms, a different number of limbs, or a form with no human mapping. Relates to art direction (AMO-Q035).

### AMO-Q058 — VR interaction and interface
**Status:** OPEN · **Constraints:** AMO-D042, AMO-D043
How do inventory, menus and information work in VR without falling back on flat panels? How are pots, plants and world objects physically handled? What does the astral ritual feel like in VR?
*Notes:* This is where the "avoid concepts that fundamentally require a 2D UI" constraint (AMO-D043) is tested. A design that only works as a menu is a warning sign for both interfaces.

### AMO-Q059 — VR-native combat design
**Status:** OPEN · **Constraints:** AMO-D008, AMO-D042
What is VR combat actually made of? How much is physically performed? How are intentional techniques, readable rules and mastery preserved without rewarding flailing?
*Notes:* Must not assume unrestricted real-world physics, that any movement is a valid attack, or that human anatomy maps onto every Amorpho body. How fantastical moves are expressed physically is part of this. Needs prototypes (Phase 3).

### AMO-Q060 — Standard/VR parity, cross-play and matchmaking
**Status:** OPEN · **Constraints:** AMO-D008, AMO-D041, AMO-D042
Can Standard and VR players fight each other directly? Are both suited to ranked competition? Should matchmaking distinguish interface? Can combat rules stay identical while input disciplines differ, and how is physical attack speed normalised? How are exploits and physical fatigue handled?
*Notes:* Deliberately unanswered; it needs real testing, not an early decision. Note the tension with AMO-D041: one world and one progression do not automatically imply one competitive pool.

### AMO-Q061 — VR accessibility
**Status:** OPEN · **Constraints:** AMO-D042
How do players with different physical abilities, space constraints or tolerance for motion play in VR without being disadvantaged, competitively or otherwise?
*Notes:* Related to the control model generally (AMO-Q023). If VR is first-class, its accessibility cannot be an afterthought.

### AMO-Q062 — VR platforms and hardware
**Status:** OPEN · **Constraints:** AMO-D020, AMO-D043
Which VR platforms and hardware are targeted, and what are the minimum requirements?
*Notes:* No commitment exists to OpenXR details, Meta, SteamVR, Apple spatial frameworks, PlayStation VR, specific headsets, tracking hardware or middleware (AMO-D043). Part of target platforms (AMO-Q037) and an input to the engine decision (AMO-Q036).

---

## Suggested next to resolve

In rough order of value for the next phase:

1. **AMO-Q069** and **AMO-Q070** (value representation; aggregation and limiting factors) — now the highest-value pair. Version 0 fixed the boundary (AMO-D046–AMO-D049); these are the first two things a working evaluator needs, and both are best answered by walking worked examples through the contract rather than by argument.
2. **AMO-Q016** (changes in the approved species list) — needed before the second approved species export, not the first.
3. **AMO-Q013** and **AMO-Q012** (genetics, simulation depth) — shape the individual-plant model and the Evolutionator's core.
4. **AMO-Q042** and **AMO-Q051** (inhabitability; the three tolerance concepts) — turn the embodiment laws into something a prototype can be built against.
5. **AMO-Q025** and **AMO-Q026** (cultivation's effect on combat; loss) — decide whether the two layers reinforce each other.
6. **AMO-Q027** (roster scale) — decides whether the combat layer is producible at all.
7. **AMO-Q001** and **AMO-Q004** (world scale, time) — decide the cost of everything else.

The Earth-representation questions (AMO-Q063–AMO-Q068) mostly wait on AMO-Q001, which waits on evidence rather than argument. That the world *is* Earth is settled (AMO-D045); *how* it is represented is a technology-shaped question for Phase 2.

The VR questions (AMO-Q056–AMO-Q062) are deliberately **not** near the top. They are recorded so that architecture can account for them (AMO-D043); answering them needs prototypes, which belong to Phase 3.
