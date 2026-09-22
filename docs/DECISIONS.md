# Decision Ledger

This ledger records Amorpho's accepted product and architecture decisions. Its purpose is to make drift visible: if the project starts behaving differently from what is written here, either the work is wrong or a decision needs to be formally changed.

## How to use this ledger

- **IDs are permanent.** `AMO-D###` numbers are never reused or renumbered.
- **Never delete a decision.** To change a decision's substance, add a new decision and mark the old one `SUPERSEDED by AMO-D###`, with a short note on what changed and why. Anyone reading old documents, commits or data must still be able to understand what was true at the time.
- **Clarifications** that do not change a decision's substance (terminology, cross-references, filling in a detail the decision had left open) may be made in place, with a dated *Revised* note.
- **Statuses:** `ACCEPTED` (in force), `SUPERSEDED` (replaced; kept for history). Undecided matters do not belong here — they live in [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md). When an open question is resolved, record the outcome here and point the question to it.
- **Origin** says where a decision came from: *Founding brief*, *Foundation closure brief*, *Embodiment and systems brief*, *World foundation brief*, *Environment v0 brief*, *Strategic rooting brief*, *Interaction boundary brief*, *Condition v0 brief*, *Life cycle and anchors brief*, *Warden progression brief*, *State machine brief*, *Harm and maturity brief*, *Manifestation boundary brief*, *Maturity v0 brief*, *Biology-magic boundary brief* or *Pathological impact brief* (set by the project owner), or *…, derived* (a conservative consequence worked out in that session).
- Keep entries short. Longer reasoning belongs in the design documents.

## Index

| ID | Title | Status |
|---|---|---|
| AMO-D001 | Product name is Amorpho | ACCEPTED |
| AMO-D002 | Amorpho is an independent repository and system | ACCEPTED |
| AMO-D003 | Fun comes first; entertainment is the product | ACCEPTED |
| AMO-D004 | Real species define the base species set | ACCEPTED |
| AMO-D005 | No invented species | ACCEPTED |
| AMO-D006 | Combat is designed for play, not as botanical simulation | ACCEPTED |
| AMO-D007 | Two gameplay layers, bridged by the same individual plant | ACCEPTED |
| AMO-D008 | Combat is real-time and skill-based, with fighting-game rounds | ACCEPTED |
| AMO-D009 | The world persists independently of players | ACCEPTED |
| AMO-D010 | Plant populations are finite; no spawning on demand | ACCEPTED |
| AMO-D011 | Plants are persistent individuals with provenance | ACCEPTED |
| AMO-D012 | Individuals acclimate; genetic change happens across generations | ACCEPTED |
| AMO-D013 | Environmental suitability, not country locks | ACCEPTED |
| AMO-D014 | Cultivation context is a risk/reward choice | ACCEPTED |
| AMO-D015 | Flowering increases discoverability | ACCEPTED |
| AMO-D016 | Hybrid compatibility is evidence-gated (directional) | SUPERSEDED by AMO-D027 |
| AMO-D017 | External reality enters only through a one-way Reality Gate | ACCEPTED |
| AMO-D018 | No runtime dependency on external systems | ACCEPTED |
| AMO-D019 | Slow, continuous incubation | ACCEPTED |
| AMO-D020 | No premature engine lock-in | ACCEPTED |
| AMO-D021 | Three data layers: approved reality input, game design data, persistent world state | ACCEPTED |
| AMO-D022 | Stable identifiers; permanent opaque `AMO-SP-` species IDs | ACCEPTED |
| AMO-D023 | Reality update package format, version 1 (JSON) | SUPERSEDED by AMO-D026 |
| AMO-D024 | Botanical research and master data stay outside Amorpho | ACCEPTED |
| AMO-D025 | Import only what the game demonstrably needs | ACCEPTED |
| AMO-D026 | Approved reality input is a simple file; CSV while sufficient | ACCEPTED |
| AMO-D027 | Hybrid compatibility is a symmetric approved species pair | ACCEPTED |
| AMO-D028 | One consciousness, one inhabited body | ACCEPTED |
| AMO-D029 | Human body and Amorpho are separate persistent entities | ACCEPTED |
| AMO-D030 | Plant state and animated state are one persistent individual | ACCEPTED |
| AMO-D031 | Astral entry requires sufficient biological stability | ACCEPTED |
| AMO-D032 | Astral exit returns the individual to rooted plant state | ACCEPTED |
| AMO-D033 | Rooting is not inherently harmful; Environmental Fit decides | ACCEPTED |
| AMO-D034 | Rescue windows are environmentally derived, never fixed | ACCEPTED |
| AMO-D035 | The World owns environmental truth | ACCEPTED |
| AMO-D036 | The Amorpho owns biological requirements, traits and condition | ACCEPTED |
| AMO-D037 | Environmental Fit is derived from World × Amorpho | ACCEPTED |
| AMO-D038 | The Evolutionator owns inheritance, variation and generational change | ACCEPTED |
| AMO-D039 | Individual acclimation is distinct from generational evolution | ACCEPTED |
| AMO-D040 | Environmental and player-driven selection both shape lineages | ACCEPTED |
| AMO-D041 | Standard and VR Gameplay are first-class interfaces to one game | ACCEPTED |
| AMO-D042 | VR is optional, never secondary | ACCEPTED |
| AMO-D043 | Account for VR early; defer VR production cost | ACCEPTED |
| AMO-D044 | No shared cross-project VR platform; prove first, extract later | ACCEPTED |
| AMO-D045 | Amorpho's World is Earth | ACCEPTED |
| AMO-D046 | World environment is local and time-dependent | ACCEPTED |
| AMO-D047 | Environment Vector v0: five neutral dimensions | ACCEPTED |
| AMO-D048 | Amorpho response profile v0: zones, three contributing layers | ACCEPTED |
| AMO-D049 | Environmental Fit v0 output contract | ACCEPTED |
| AMO-D050 | Inhabitability is downstream of biological condition | ACCEPTED |
| AMO-D051 | Environment describes conditions, not permissions | ACCEPTED |
| AMO-D052 | Fit is deterministic for identical state; randomness is upstream | ACCEPTED |
| AMO-D053 | The design model precedes importing real environmental data | ACCEPTED |
| AMO-D054 | Rooting may be strategic and long-term | ACCEPTED |
| AMO-D055 | World owns environmental interactions; Fit owns biological ones | ACCEPTED |
| AMO-D056 | Current Biological Condition v0: vitality, stress load, reserves | ACCEPTED |
| AMO-D057 | Developmental State is a separate axis from condition | ACCEPTED |
| AMO-D058 | The individual persists; its biological manifestation changes | ACCEPTED |
| AMO-D059 | Life-cycle phases v0 | ACCEPTED |
| AMO-D060 | Deep Dormancy closes the astral door and hides the individual | ACCEPTED |
| AMO-D061 | Astral Anchors are physical, reusable objects on individuals | ACCEPTED |
| AMO-D062 | Only the human may attach, remove or move an Anchor | ACCEPTED |
| AMO-D063 | Astral entry requires three independent gates | ACCEPTED |
| AMO-D064 | Biological life is independent of anchoring; new individuals begin unbound | ACCEPTED |
| AMO-D065 | Existence, ownership, custody, anchoring and availability are separate | ACCEPTED |
| AMO-D066 | Human/Warden progression is a distinct, slower domain | ACCEPTED |
| AMO-D067 | Astral Capacity is human capability, distinct from Anchor supply | ACCEPTED |
| AMO-D068 | Additional Astral Capacity becomes progressively harder | ACCEPTED |
| AMO-D069 | Human progression expands capability without overriding rules | ACCEPTED |
| AMO-D070 | Life-cycle state machine v0: three families, seven states | ACCEPTED |
| AMO-D071 | Bloom is a sibling active state, not a stage or an overlay | ACCEPTED |
| AMO-D072 | Rooting, astral exit and dormancy are three separate things | ACCEPTED |
| AMO-D073 | Availability follows biological state; no roster timer | ACCEPTED |
| AMO-D074 | Three harm horizons; manifestations do not inherit damage | ACCEPTED |
| AMO-D075 | All damage recovers while alive; only death is terminal | ACCEPTED |
| AMO-D076 | Vitality is stored persistent state; no second core variable | ACCEPTED |
| AMO-D077 | Developmental Maturity is a separate persistent dimension | ACCEPTED |
| AMO-D078 | Bloom requires species-specific flowering maturity | ACCEPTED |
| AMO-D079 | Manifestation damage reaches the core only past a threshold | ACCEPTED |
| AMO-D080 | Developmental Maturity v0: one slow, species-relative axis | ACCEPTED |
| AMO-D081 | Maturity grows from persistent biological surplus | ACCEPTED |
| AMO-D082 | Regression requires persistent loss; lost opportunity is not regression | ACCEPTED |
| AMO-D083 | Healing and regrowth are separate processes | ACCEPTED |
| AMO-D084 | Magic runs the fighter; biology is suspended during embodiment | ACCEPTED |
| AMO-D085 | Embodiment is open-ended; the Human trance is metabolically stable | ACCEPTED |
| AMO-D086 | Astral Readiness: magical state restored by rooted biological life | ACCEPTED |
| AMO-D087 | Tuber is canonical; Programmed Draw is not Pathological Impact | ACCEPTED |
| AMO-D088 | Astral Signal is distinct from inhabitability; dormancy silences it | ACCEPTED |
| AMO-D089 | Tuber gameplay deferred; Leaf and Bloom are the playable forms | ACCEPTED |
| AMO-D090 | Pathological Tuber Impact: direct and indirect, acute and cumulative | ACCEPTED |
| AMO-D091 | Persistent consequence follows function and opportunity, not appearance | ACCEPTED |
| AMO-D092 | Pathology is actual persistent loss, not depletion or lost growth | ACCEPTED |
| AMO-D093 | Excavated Tubers remain biologically simulated | ACCEPTED |
| AMO-D094 | Mature Leaf recovery preserves; replacement is a new manifestation | ACCEPTED |
| AMO-D095 | The persistent Tuber funds temporary manifestations | ACCEPTED |
| AMO-D096 | Replacement is capacity-limited intra-cycle salvage | ACCEPTED |
| AMO-D097 | Biology bounds routing choices; unattended plants route autonomously | ACCEPTED |

**Foundation closure (2026-09-18):** before the initial commit, the botanical input architecture was simplified. AMO-D016 and AMO-D023 were superseded; AMO-D024–AMO-D027 were added; AMO-D021 and AMO-D022 were confirmed. Terminology and cross-references in other entries were updated to match; entries whose wording changed beyond that carry a *Revised* note.

**Embodiment and systems pass (2026-09-20):** the first post-foundation design pass added AMO-D028–AMO-D044, covering the embodiment model (astral transfer), the World / Amorpho / Evolutionator ownership split with Environmental Fit as the derived bridge, and Standard and VR Gameplay as two first-class interfaces. Nothing was superseded. AMO-D007, AMO-D012 and AMO-D013 were extended rather than replaced; they carry *Revised* notes pointing at the extensions.

**World foundation (2026-09-21):** AMO-D045 fixed the World as a coherent representation of the real Earth, shared by the Human and Amorpho layers, with progressive fidelity and no technology commitment. Nothing was superseded; AMO-D009 carries a *Revised* note pointing at it.

**Environment and Fit v0 (2026-09-21):** AMO-D046–AMO-D053 gave the accepted architecture its first usable environmental model — a five-dimension World vector, a zoned Amorpho response profile, and a Fit output contract that preserves per-dimension information alongside an aggregate trajectory. It is a boundary contract, not a biological simulation: no values, units, formulas or tick rates are fixed. Nothing was superseded; AMO-D013, AMO-D031 and AMO-D037 carry *Revised* notes pointing at it. The specification is [12_ENVIRONMENT_AND_FIT_MODEL_V0.md](12_ENVIRONMENT_AND_FIT_MODEL_V0.md).

**Strategic rooting (2026-09-21):** AMO-D054 established that rooting is not primarily an emergency mechanic — a suitable rooted environment can support indefinite healthy life, growth and eventual reproduction, and rooting may be the reason for a journey rather than its end. Nothing was superseded; AMO-D033 carries a *Revised* note pointing at it.

**Interaction boundary (2026-09-21):** AMO-D055 settled where cross-dimensional interactions live, tested against a worked scenario in which two individually tolerable dimensions jointly change the outcome. Nothing was superseded; AMO-D035 and AMO-D049 carry *Revised* notes pointing at it.

**Current condition v0 (2026-09-21):** AMO-D056 and AMO-D057 gave the persistent individual its biological memory — three condition variables and a separate developmental axis — tested against the four existing worked scenarios rather than new ones. Nothing was superseded; AMO-D048 carries a *Revised* note pointing at them. The specification is [14_CURRENT_BIOLOGICAL_CONDITION_V0.md](14_CURRENT_BIOLOGICAL_CONDITION_V0.md).

**Life cycle and anchors (2026-09-21):** AMO-D058–AMO-D065 added the biological life cycle as a gameplay axis, the physical Astral Anchor, and the separation of existence, ownership, custody, anchoring and availability. Nothing was superseded; AMO-D015, AMO-D031 and AMO-D057 carry *Revised* notes pointing at them. The specification is [15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md).

**Warden progression (2026-09-21):** AMO-D066–AMO-D069 established the human's own progression domain and its first dimension, Astral Capacity. No curve, value, requirement or timing rule was chosen. Nothing was superseded; AMO-D061 and AMO-D063 carry *Revised* notes pointing at them. The specification is [16_HUMAN_WARDEN_PROGRESSION_V0.md](16_HUMAN_WARDEN_PROGRESSION_V0.md).

**Life-cycle state machine (2026-09-21):** AMO-D070–AMO-D073 gave the life cycle its topology, resolved Bloom's structural placement, separated rooting from astral exit from dormancy, and fixed availability to biological state. Nothing was superseded; AMO-D032, AMO-D059 and AMO-D063 carry *Revised* notes pointing at them. The specification is [17_LIFE_CYCLE_STATE_MACHINE_V0.md](17_LIFE_CYCLE_STATE_MACHINE_V0.md).

**Harm, recovery and Bloom maturity (2026-09-21):** AMO-D074–AMO-D078 resolved the policy half of AMO-Q045 and added the developmental gate on Bloom. The project's earlier working assumption that some harm might be permanent is **withdrawn**: while an individual lives, all biological damage is recoverable, and only death is terminal. AMO-D056's caveat about vitality being derivable is superseded by AMO-D076, which keeps the same conclusion for a stronger reason. Nothing else was superseded; AMO-D033, AMO-D056, AMO-D057 and AMO-D059 carry *Revised* notes. The specification is [18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md).

**Manifestation-to-core boundary (2026-09-21):** AMO-D079 added the missing boundary inside AMO-D074's horizons — manifestation damage affects the current body first, and reaches persistent state only when its biological consequences are deep enough. Nothing was superseded; AMO-D074 and AMO-D077 carry *Revised* notes.

**Developmental Maturity v0 (2026-09-21):** AMO-D080–AMO-D083 specified the persistent developmental axis — what it is, how it grows, how it regresses, and why healing it is not the same as regrowing it. Nothing was superseded; AMO-D077 and AMO-D078 carry *Revised* notes. The specification is [19_DEVELOPMENTAL_MATURITY_V0.md](19_DEVELOPMENTAL_MATURITY_V0.md).

**Biology ↔ magic boundary (2026-09-21):** AMO-D084–AMO-D089 separated the magically inhabited fighter from the biological plant, made embodiment open-ended, introduced Astral Readiness, fixed Tuber terminology, and separated the Warden's astral signal from inhabitability. Nothing was superseded; AMO-D061, AMO-D074 and AMO-D079 carry *Revised* notes. AMO-Q108 is **not** addressed. The specification is [20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md](20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md).

**Pathological Tuber Impact (2026-09-22):** AMO-D090–AMO-D093 answered AMO-Q108 at the conceptual level — what pathology is, its two pathways, why visible damage is not the verdict, and the outcome-based diagnostic that separates loss from spending and from lost opportunity. Nothing was superseded; AMO-D079 carries a *Revised* note. The specification is [21_PATHOLOGICAL_TUBER_IMPACT_V0.md](21_PATHOLOGICAL_TUBER_IMPACT_V0.md).

---

## AMO-D001 — Product name is Amorpho

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** The product, the repository and all product-facing material are named **Amorpho**. It is never called "TM Amorpho", "TM Amorpho Game", "Trederus Maximus Amorpho" or similar. Within the game, "an Amorpho" also names a plant awakened as a fighter.
- **Rationale:** Amorpho needs its own identity. Group affiliation is background, not branding.
- **Consequences:** Package names, headings, file names and documentation use "Amorpho". The Trederus Maximus affiliation appears only as one quiet sentence in an About section.

## AMO-D002 — Amorpho is an independent repository and system

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** Amorpho is self-contained. It has no code, build, data or service dependencies on any other system, including other Trederus Maximus projects such as Imperblio or TM Botanics.
- **Rationale:** The game must be able to exist, be built and be run entirely on its own, for as long as it lives.
- **Consequences:** Anything Amorpho needs, it owns. Knowledge from outside arrives only as approved input files through the Reality Gate (AMO-D017).
- **Revised:** 2026-09-21 — a sibling project's name was misspelled "Imperbio" at foundation and is corrected in place to **Imperblio**. Spelling only; substance unchanged, and the project remains a named example of something Amorpho does not depend on.

## AMO-D003 — Fun comes first; entertainment is the product

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** When fun and realism conflict, fun wins. Botanical realism grounds the world but must not suffocate gameplay. Amorpho is not educational software; any learning is incidental.
- **Rationale:** A player with no interest in botany must be able to love Amorpho purely as a game.
- **Consequences:** Realism is used where it creates interesting play (scarcity, risk, history, identity) and abstracted where it does not. Reality still constrains *which* species exist and *which* species pairs may hybridize (AMO-D004, AMO-D027); "fun first" is never a licence to fabricate facts.

## AMO-D004 — Real species define the base species set

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** The known, scientifically recognised species of the genus *Amorphophallus* form Amorpho's base species set. A real species defines the identity and visual foundation of the corresponding Amorpho character. Newly recognised real species may be added later through the Reality Gate.
- **Rationale:** Reality provides the cast; the game provides the fantasy. The genus's real range of forms gives the game an unusual, grounded roster.
- **Consequences:** The species list is approved reality input ([`data/input/amorphophallus_species.csv`](../data/input/amorphophallus_species.csv)), not a design choice. Which species are recognised is decided by the external research process (AMO-D024). The list currently contains no species. How the game handles later changes to the list (removals, merges, splits, infraspecific taxa) is open (AMO-Q016).
- **Revised:** 2026-09-18, foundation closure — consequences updated to the file-based input (AMO-D026); substance unchanged.

## AMO-D005 — No invented species

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** Amorpho never invents fictional *Amorphophallus* species, whether for roster size, gameplay convenience or placeholder content presented as real.
- **Rationale:** Species come from reality. Diversity in the game comes from individuals, variation, lineages and approved hybrids.
- **Consequences:** Illustrations and test fixtures use clearly fictional placeholders and never appear in approved input.

## AMO-D006 — Combat is designed for play, not as botanical simulation

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** A species' combat design is driven by balance, mastery and fun. A large real plant is not automatically a stronger fighter; a botanical trait is not automatically a combat mechanic.
- **Rationale:** A fighting game lives or dies on balance and feel. Real traits are inspiration, not specification.
- **Consequences:** Combat design is Game Design Data (AMO-D021) and never has to be justified botanically.

## AMO-D007 — Two gameplay layers, bridged by the same individual plant

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** Amorpho has a **Human / World layer** (the player as a human in a persistent world: exploring, acquiring, cultivating, propagating, trading) and an **Amorpho / Combat layer** (skill-based fighting). A single magical artifact per player lets a suitable plant be temporarily awakened as an Amorpho. The plant that fights is the same persistent individual that lives in a pot, greenhouse or landscape.
- **Rationale:** The bond between the plant a player has raised and the fighter they master is the core of the concept.
- **Consequences:** Both layers operate on the same individual-plant identity. The artifact's form, name and origin, and the exact transformation rules, are open (AMO-Q021, AMO-Q022).
- **Revised:** 2026-09-20, embodiment and systems pass — the bridge is **astral transfer**: the player's consciousness leaves a persistent human body and inhabits one eligible individual (AMO-D028, AMO-D029, AMO-D030). "Transformation" remains the umbrella term; substance unchanged, and the artifact's form stays open.

## AMO-D008 — Combat is real-time and skill-based, with fighting-game rounds

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** Combat is eventually a fully developed real-time fighting game: movement, positioning, timing, blocking, attacks, counters, learnable moves, combinations, input sequences and multiple rounds. "Rounds" means fighting-game rounds, not turn selection.
- **Rationale:** Players must be able to become significantly better with the same Amorpho through practice.
- **Consequences:** Player skill remains a central determinant of combat outcomes. Whatever influence cultivation has on combat (AMO-Q025) must not replace skill.

## AMO-D009 — The world persists independently of players

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** The world, its cities and its geography exist independently of any individual player. Without player intervention, natural *Amorphophallus* populations continue to exist and develop in their natural regions. Players act inside the world and can change its history; they are not its centre.
- **Rationale:** A world with its own continuity is what gives plants and events real history.
- **Consequences:** World state must be persistent and must evolve without player input. Scale, time model and topology are open (AMO-Q001, AMO-Q004, AMO-Q006).
- **Revised:** 2026-09-21, world foundation — the world that persists is specifically a coherent representation of the real **Earth**, shared by the Human and Amorpho layers (AMO-D045). Substance unchanged; scale and fidelity remain open.
- **Revised:** 2026-09-21, environment v0 — this is AMO-D009's entry; see also AMO-D046, which makes the persisting world's environment local and time-dependent rather than a fixed property of a place.

## AMO-D010 — Plant populations are finite; no spawning on demand

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** The world begins with finite natural populations and cultivated stocks. Plants never appear simply because someone needs one. They spread through propagation, seed production, trade, collection, human transport, deliberate cultivation and, where appropriate, natural establishment.
- **Rationale:** Scarcity and history make individual plants matter.
- **Consequences:** Every plant in the world has an origin traceable to the initial world state or to reproduction. How initial populations are seeded, and how newly approved species enter a live world, is open (AMO-Q019, AMO-Q033).

## AMO-D011 — Plants are persistent individuals with provenance

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** Each plant is a persistent individual that can carry provenance: species, unique identity, origin, founder population, known parentage, generation, lineage, owners, locations, propagation history, notable events, phenotype and relevant combat history.
- **Rationale:** An individual plant may matter because of its real history in the world.
- **Consequences:** The simulation may know more than any player sees; exposure of provenance in the UI is a separate design question.

## AMO-D012 — Individuals acclimate; genetic change happens across generations

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** Moving an individual plant does not change its genetics. An individual may acclimate and express different growth. Genetic change emerges across generations and populations through reproduction, variation and selection. Species, individual, genotype, phenotype, lineage, environment and acquired history are kept conceptually separate.
- **Rationale:** This keeps the model coherent and leaves room for a playable inheritance system and for recognisable player- or location-created lineages.
- **Consequences:** Data models must not merge these concepts. The genetic abstraction itself is open (AMO-Q013).
- **Revised:** 2026-09-20, embodiment and systems pass — inheritance, variation and generational change are owned by the **Evolutionator** (AMO-D038), and the acclimation/evolution distinction is restated as AMO-D039. Substance unchanged.

## AMO-D013 — Environmental suitability, not country locks

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** Where a species can grow is determined by environmental suitability (for example temperature, seasonality, rainfall, moisture, dry season, light, drainage), not by political borders or native-country membership.
- **Rationale:** It allows meaningful movement of plants around the world and ties outcomes to understandable causes.
- **Consequences:** Locations carry environmental properties; species carry tolerance/suitability profiles. The exact variables and resolution are deliberately unspecified (AMO-Q005). Environmental facts enter approved input only after the environment model is designed (AMO-D025).
- **Revised:** 2026-09-20, embodiment and systems pass — the ownership boundary is made explicit (AMO-D035, AMO-D036) and *suitability* is renamed **Environmental Fit**, derived from World × Amorpho (AMO-D037). Substance unchanged.
- **Revised:** 2026-09-21, environment v0 — the first concrete model is specified: a five-dimension World vector, a zoned response profile and a Fit output contract (AMO-D047–AMO-D049, [12_ENVIRONMENT_AND_FIT_MODEL_V0.md](12_ENVIRONMENT_AND_FIT_MODEL_V0.md)). Substance unchanged; values, units and formulas remain undefined.

## AMO-D014 — Cultivation context is a risk/reward choice

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** Pots, homes, greenhouses and outdoor planting are distinct cultivation contexts with different trade-offs. Pot size constrains development, so species identity does not determine achieved size. Homes give control and relative safety but are not perfect safe zones. Greenhouses give stronger control and capacity. Outdoor planting in a suitable climate can give better development and natural pollination, at the cost of exposure to weather, pests, discovery, theft and unintended pollination.
- **Rationale:** The risk/reward relationship between protected and exposed cultivation is a core part of world gameplay.
- **Consequences:** No cultivation context may be strictly best. Specific systems (property, greenhouses) are open (AMO-Q032).

## AMO-D015 — Flowering increases discoverability

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** A flowering plant becomes easier for others to find, because of its scent. A flowering, valuable outdoor plant is therefore at greater risk.
- **Rationale:** It turns a striking real characteristic of the genus into a natural risk/reward mechanic.
- **Consequences:** The implementation (radius, reports, clues, approximate signals) is deliberately open (AMO-Q015).
- **Revised:** 2026-09-21, life cycle — discoverability now varies by life-cycle phase: **Bloom** carries a strong signature, while a deeply dormant unexposed tuber is normally undiscoverable without prior location knowledge (AMO-D060). Substance unchanged.

## AMO-D016 — Hybrid compatibility is evidence-gated (directional)

- **Status:** SUPERSEDED by AMO-D027 (2026-09-18, foundation closure) · **Date:** 2026-09-18 · **Origin:** Founding brief (directionality derived in the foundation session)
- **Decision (historical):** A cross between two species is allowed in the game only if canon contains a record allowing it, and records enter canon only through the Reality Gate with verified real-world evidence. Unknown means unknown, and unknown is treated as not allowed. Compatibility is recorded per direction (seed parent × pollen parent); evidence for one direction does not imply the reciprocal cross.
- **Why superseded:** Directionality and evidence are scientific detail that belongs to the external research process. For gameplay, Amorpho needs only the approved result for a species pair, which is symmetric. The core rule — no invented compatibility; not approved means no hybridization — carries over into AMO-D027.

## AMO-D017 — External reality enters only through a one-way Reality Gate

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** Real-world knowledge enters Amorpho only through the Reality Gate: a single, explicit, strictly inbound boundary. Approved export files are supplied from outside the repository, validated, and accepted into `data/input/`. Once accepted, the information is Amorpho's own data, and the game works only from it.
- **Rationale:** Reality must be able to correct and extend the game without making the game depend on where knowledge came from.
- **Consequences:** Nothing flows outward through the gate. Game design data does not pass through the gate. See [05_REALITY_GATE.md](05_REALITY_GATE.md) and AMO-D026.
- **Revised:** 2026-09-18, foundation closure — the mechanism changed from update packages to approved input files (AMO-D026); the one-way principle is unchanged.

## AMO-D018 — No runtime dependency on external systems

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** The running game, its tools and its data never query, call or reference external knowledge systems (including Imperblio, TM Botanics or any other Trederus Maximus system), botanical websites or databases, external APIs or live data sources. Approved input files never name or identify their source.
- **Rationale:** Sources are relevant to the external research process, not to the game. Independence preserves Amorpho's ability to exist on its own.
- **Consequences:** No imports from external repositories, shared runtime packages, database links, callbacks, synchronisation jobs or environment variables pointing at research systems. Once an approved import is accepted, nothing in Amorpho needs continued access to the external master-data system.
- **Revised:** 2026-09-18, foundation closure — consequences restated for the file-based input; substance unchanged.
- **Revised:** 2026-09-21 — "Imperbio" corrected in place to **Imperblio**. Spelling only; substance unchanged.

## AMO-D019 — Slow, continuous incubation

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** Amorpho develops as a low-pressure, continuously evolving project. *Always moving, never rushed.* *Build irreversible knowledge now; defer expensive production until capacity catches up.* The roadmap is organised by maturity phases, not dates.
- **Rationale:** Other projects have higher priority today; capacity (AI agents, tooling, generative media, funding, people) is expected to grow. Good decisions must survive until then.
- **Consequences:** Prefer small, durable steps. No speculative infrastructure, microservices, networking stacks or empty boilerplate. See [07_INCUBATION_ROADMAP.md](07_INCUBATION_ROADMAP.md).

## AMO-D020 — No premature engine lock-in

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** No game engine, framework, programming language or runtime stack is chosen until there is concrete evidence for the choice.
- **Rationale:** An early engine choice would constrain world scale, combat networking and pipeline decisions before they are understood.
- **Consequences:** Engine selection is evidence-driven, using the criteria in [08_CONCEPTUAL_ARCHITECTURE.md](08_CONCEPTUAL_ARCHITECTURE.md#engine-and-technology-decision-criteria). Tracked as AMO-Q036.
- **Revised:** 2026-09-18, foundation closure — "programming language" made explicit; substance unchanged.

## AMO-D021 — Three data layers: approved reality input, game design data, persistent world state

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Foundation session, derived from AMO-D004, AMO-D006, AMO-D017; confirmed by the project owner at foundation closure
- **Decision:** Amorpho data is separated into three conceptual layers:
  1. **Approved Reality Input** — the minimal real-world information approved for use by Amorpho: species identities and approved scientific names, approved hybrid-compatible pairs, and later selected environmental facts once the game needs them. It changes only through the Reality Gate.
  2. **Game Design Data** — information Amorpho creates for gameplay: combat characteristics, abilities, animations, balancing, transformation behaviour, progression, and the visual and gameplay interpretation of species. It may reference species IDs but can never add species or compatible pairs.
  3. **Persistent World State** — what exists or happens inside a running world: individual plants, ownership, location, parentage, player-created lineages, houses, pots, greenhouses, populations, trades, combat history.
- **Terminology:** Within Layer 1, the *approved input* is the externally supplied file as accepted into `data/input/`; the *internal representation* — also called **canon** — is whatever form the implementation later derives from it. "Canon" never means the external master list, and never includes design data or world state.
- **Rationale:** It makes "species come from reality; individuals and lineages come from the game world" enforceable, and keeps game design free from botanical justification.
- **Consequences:** References point from world state to design data and approved input, and from design data to approved input — never the other way. See [08_CONCEPTUAL_ARCHITECTURE.md](08_CONCEPTUAL_ARCHITECTURE.md).
- **Revised:** 2026-09-18, foundation closure — layer names and the meaning of "canon" clarified; substance unchanged.

## AMO-D022 — Stable identifiers; permanent opaque `AMO-SP-` species IDs

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Foundation session, derived from AMO-D011, AMO-D017; confirmed, and species ID format set, by the project owner at foundation closure
- **Decision:** Species and world entities (such as individual plants) have identifiers that never change and are never reused. Each species has a permanent, opaque Amorpho species ID of the form `AMO-SP-` followed by six digits, for example `AMO-SP-000001`. A species ID never encodes the scientific name, never changes because taxonomy changes, remains valid if the accepted name or botanical interpretation changes, is never reused, and is independent of every external research source or system. The species ID is the game's long-term identity for a species; the scientific name is mutable metadata attached to it.
- **Rationale:** Savegames, individual plants, genealogies, lineages, ownership, world history, combat history and long-running persistent worlds must all survive name changes.
- **Consequences:** Scientific names are never used as permanent keys. No species IDs have been assigned yet; they arrive with the first approved species export. The ID format for individual plants and other world entities is not yet decided. Resolves AMO-Q017.
- **Revised:** 2026-09-18, foundation closure — species ID format fixed (previously open as AMO-Q017).

## AMO-D023 — Reality update package format, version 1 (JSON)

- **Status:** SUPERSEDED by AMO-D026 (2026-09-18, foundation closure) · **Date:** 2026-09-18 · **Origin:** Foundation session, derived from AMO-D016, AMO-D017, AMO-D018
- **Decision (historical):** Reality update packages are JSON documents validated by a JSON Schema (draft 2020-12) at `data/reality-gate/schema/reality-update.schema.json`. Format version 1 separates package metadata, target canon version, approval, evidence references and change records, and supports `add` and `amend` for `species` and directed `hybrid_compatibility`.
- **Why superseded:** The format mainly encoded evidence references, approval workflow and change operations that belong to the external research process (AMO-D024). A plain approved file plus version control covers everything Amorpho needs. The schema, example and package directory were removed before the initial commit.

## AMO-D024 — Botanical research and master data stay outside Amorpho

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Foundation closure brief
- **Decision:** Amorpho does not research botany. Detailed research about *Amorphophallus* — taxonomy, synonyms, descriptions, literature, distributions, morphology, hybrid evidence, cultivation knowledge — happens outside this repository, where a comprehensive master list is maintained. Amorpho is not a botanical master database, taxonomy research system, literature database, paper archive, taxonomic dispute-resolution system, evidence-management platform or mirror of external databases. It does not know who maintains the master list or which sources were consulted.
- **Rationale:** Master knowledge is not the same thing as game input. Keeping research outside keeps the game independent and simple.
- **Consequences:** No external botanical organisation, database or publication is an architectural source for Amorpho. Amorpho trusts approved input and does not adjudicate names or evidence. Agents do not perform botanical research in this repository unless a task explicitly requires external investigation.

## AMO-D025 — Import only what the game demonstrably needs

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Foundation closure brief
- **Decision:** Only botanical facts with a demonstrated game requirement cross into Amorpho. The external master dataset is never mirrored. A field is added to approved input only after the game system that needs it has been designed — for example, environmental facts only after the environment model exists. Amorpho does not copy third-party prose, website text, photographs, illustrations, external tables, database dumps or editorial descriptions; approved input is Amorpho's own minimal, curated factual representation.
- **Rationale:** It minimises licensing exposure, data duplication, external dependencies, scientific complexity, migration burden and coupling between research and game architecture.
- **Consequences:** The initial species input has two columns. Authorship, external IDs, references, distributions, morphology, climate, combat and visual data are not imported. No external website or research service needs to remain operational for Amorpho to work. This is an engineering principle, not legal advice; source-specific licensing logic does not belong in Amorpho.

## AMO-D026 — Approved reality input is a simple file; CSV while sufficient

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Foundation closure brief · **Supersedes:** AMO-D023
- **Decision:** The Reality Gate is: an approved export file supplied from outside the repository → validation against the documented input contract → acceptance by committing it to `data/input/` → whatever internal representation the eventual implementation needs. CSV is the preferred format while requirements remain simple. The first input is `data/input/amorphophallus_species.csv` with the columns `species_id,scientific_name`. No external APIs, live synchronisation, HTTP requests, database integrations, message queues, research-source adapters or evidence storage are introduced without demonstrated need.
- **Rationale:** A snapshot file under version control is a reviewable, versioned, auditable inbound boundary with no technology commitment.
- **Consequences:** Validation rules are documented in [`data/input/README.md`](../data/input/README.md), not encoded in a schema; no validation tool or language is chosen (AMO-Q038). Git history is the record of accepted imports; no extra import metadata is kept for now. The internal representation is not decided (no SQL, database, JSON runtime files or engine resources are chosen). Once an import is accepted, the running game does not depend on the external master-data system.

## AMO-D027 — Hybrid compatibility is a symmetric approved species pair

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Foundation closure brief · **Supersedes:** AMO-D016
- **Decision:** For gameplay, hybrid compatibility is a relationship between two species: `A + B` is either an **approved compatible pair** or **not approved as compatible**. It is symmetric: `A ↔ B`. A pair is approved only when the external research process has established that the two species can hybridize and the pair is supplied in approved input. Directional and evidential detail stays outside Amorpho. Absence of approval means "not currently approved as compatible", never "proven incompatible"; in the game, an unapproved pair cannot hybridize. Each pair is stored once, lower species ID first. An exception to symmetry would need a future explicit decision.
- **Rationale:** The game needs the final, approved answer, not the evidence behind it. A symmetric pair is the simplest representation that serves gameplay.
- **Consequences:** Hybrid pairs are never invented. No compatibility data exists yet; the future input file is documented in [`data/input/README.md`](../data/input/README.md) but not created. Deliberate and accidental hybridization in the world is possible only for approved pairs. Which individual plant acted as seed parent in a world event is world-state history (parentage), not compatibility data.

## AMO-D028 — One consciousness, one inhabited body

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** The player has one persistent human body and may own many plants, but their consciousness inhabits exactly one body at a time. Transformation is **astral transfer**: the player's consciousness leaves the human body and inhabits one eligible individual, which becomes an active Amorpho. A player who owns a hundred plants has one human body, a hundred plant individuals, and at most one of them inhabited.
- **Rationale:** Collection size should create options, logistics and strategic choices — not simultaneous direct control. The interesting decisions come from being able to be in only one place.
- **Consequences:** A collection is never a remotely controllable army. Simultaneous control of several Amorphos, remote orders and autonomous defence by uninhabited plants are excluded and would require a new decision. Multiple simultaneous threats become genuine dilemmas (AMO-Q047). See [09_EMBODIMENT_AND_ASTRAL_TRANSFER.md](09_EMBODIMENT_AND_ASTRAL_TRANSFER.md).

## AMO-D029 — Human body and Amorpho are separate persistent entities

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** The human does not physically transform into a plant. During astral transfer the human body remains physically present in the persistent world, in an unattended, trance-like state, while the plant individual remains a persistent physical individual that is now animated. Astral embodiment does not remove the human body from world reality.
- **Rationale:** Keeping both bodies real is what makes the human layer continue to matter and gives the location of the human body meaning.
- **Consequences:** The model "human disappears, unrelated fighter appears" is excluded. Where the transfer happens matters; a protected ritual location is the leading concept but the lore is open (AMO-Q021, AMO-Q039). What may happen to an unattended human body, and the anti-griefing implications, are open (AMO-Q041).

## AMO-D030 — Plant state and animated state are one persistent individual

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** The rooted plant and its animated Amorpho form are two states of the **same** persistent individual. Identity, provenance, lineage, ownership, history, genetics and individual variation belong to that individual and remain attached across the state change.
- **Rationale:** "The plant you raised is the fighter you play" (L16) is only true if it is literally the same individual.
- **Consequences:** The individual is never duplicated into an unrelated plant object and fighter object to be reconciled afterwards. The combat layer still receives a narrow view of the individual rather than the whole world simulation (AMO-D021, AMO-Q025); a view is not a second entity. Extends AMO-D007.

## AMO-D031 — Astral entry requires sufficient biological stability

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** `alive` and `inhabitable` are different concepts. A target individual must be healthy, stable and biologically functional enough for astral entry. A plant may be alive, but too stressed to be inhabited.
- **Rationale:** It makes biological condition matter to the fantasy layer, and it creates the transition where astral rescue stops being possible and physical rescue becomes necessary.
- **Consequences:** Deterioration can lock astral entry while the plant still lives (AMO-D034, AMO-Q042). State names, granularity, thresholds, whether inhabitability is binary or continuous, and re-entry rules are deliberately undecided; no numbers are defined anywhere.
- **Revised:** 2026-09-21, environment v0 — the evaluation path is fixed: inhabitability is computed from biological condition, never set by the World or by geography (AMO-D050). Substance unchanged; the threshold itself remains open.
- **Revised:** 2026-09-21, life cycle — biological stability is now one of **three** independent gates, alongside an Astral Anchor and life-cycle accessibility (AMO-D063). Deep dormancy closes entry regardless of how healthy the individual is (AMO-D060). Substance unchanged.

## AMO-D032 — Astral exit returns the individual to rooted plant state

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** Leaving an inhabited Amorpho returns the individual to its biological plant state, which requires rooting or another biologically appropriate transition the game may later define. From that moment the individual is again governed by its actual relationship with its environment.
- **Rationale:** *Astral exit returns fantasy to biological reality.* The fantasy layer is temporary; the biological layer is the persistent one.
- **Consequences:** Where a player can safely stop being an Amorpho becomes a real strategic question, distinct from where they can travel (AMO-D033, AMO-Q051). What counts as a valid rooting site is open (AMO-Q043). Equipment that protects the animated body does not automatically protect the rooted plant (AMO-Q048).
- **Revised:** 2026-09-21, state machine — rooting is separated explicitly from **dormancy** and from phase transition: a rooted individual may be in any phase, and astral exit does not change the life-cycle state (AMO-D072). Substance unchanged.

## AMO-D033 — Rooting is not inherently harmful; Environmental Fit decides

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** Rooting does not cause deterioration. Rooting **exposes** the individual to Environmental Fit, and the resulting trajectory may be strongly negative, mildly negative, neutral, positive or strongly positive. A rooted Amorpho in an excellent environment may remain healthy and inhabitable indefinitely, and may recover, grow, develop, improve in condition, accumulate resources or become reproductively successful.
- **Rationale:** If rooting always harmed the plant, the whole environmental system would collapse into a penalty timer and location would stop mattering.
- **Consequences:** Rooting has at least two strategic meanings — **emergency rooting** (leaving the Amorpho somewhere suboptimal and hoping it stays recoverable) and **strategic rooting** (deliberately establishing it somewhere favourable). Environmental Fit must never be treated as a synonym for stress. Nothing may model rooting as automatic decline.
- **Revised:** 2026-09-21, harm and maturity — a poor rooting decision now has a graded severity ladder beneath it, from stress through manifestation damage, premature retreat, core crisis and fragment survival to death; **only the last is permanent** (AMO-D074, AMO-D075). Substance unchanged.
- **Revised:** 2026-09-21, strategic rooting — a third intention is recognised (**operational rooting**), and the emphasis is corrected: rooting is not primarily an emergency mechanic and may be the destination of a journey rather than its end (AMO-D054). Substance unchanged.

## AMO-D034 — Rescue windows are environmentally derived, never fixed

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** There is no universal rescue timer. Where emergency rooting creates a limited window, its duration emerges from the World environment, the individual's biological requirements and current condition, and possibly acclimation, life stage, individual variation and other factors the eventual model includes. A mildly unsuitable place may allow substantial recovery time; a catastrophic one may produce rapid decline; a suitable one may produce no deadline at all.
- **Rationale:** An emergent window makes location, species and condition genuinely meaningful; a fixed timer would make them decorative.
- **Consequences:** No countdown constant exists anywhere in the design. How much prognosis a player can see, and how certain it is, is open (AMO-Q044). Once condition crosses the inhabitability threshold, astral rescue ends and physical rescue is required (AMO-D031, AMO-Q046).

## AMO-D035 — The World owns environmental truth

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** The World owns environmental state and answers only *what conditions exist here, now?* It may eventually describe location, season, time, temperature, humidity, rainfall, weather, light, substrate, soil, drainage, exposure, shelter, microclimate and other variables. The World does not know whether conditions are good or bad for a particular individual.
- **Rationale:** Separating description from judgement is what allows the environmental model and the biological model to grow independently.
- **Consequences:** Rules of the form `species X allowed here` or `species Y forbidden here` must never appear in World logic — the ownership form of L9 and AMO-D013. Buildings and greenhouses modify local conditions rather than granting exemptions (AMO-Q049). The variable list stays open (AMO-Q005).
- **Revised:** 2026-09-21, interaction boundary — the World also owns interactions *between* environmental conditions where the mechanism is physical and organism-independent, such as heat driving evaporation; interactions that change an organism's response belong to Fit (AMO-D055). Substance unchanged.

## AMO-D036 — The Amorpho owns biological requirements, traits and condition

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** The Amorpho side owns what an individual is and needs, answering *what does this individual need, prefer and tolerate?* This may eventually include preferred ranges, tolerance ranges, critical limits, health, developmental state, dormancy, acclimation, individual variation and inherited traits. The Amorpho knows itself; it does not know countries.
- **Rationale:** Biology belongs to the organism, not to the map.
- **Consequences:** Simplistic encodings such as `Thailand = good` or `Russia = bad` are excluded from the plant model. No real values exist or may be invented: botanical facts arrive only as approved input once the model that needs them is designed (L4, AMO-D025). Place names are World labels, never plant mechanics.

## AMO-D037 — Environmental Fit is derived from World × Amorpho

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** The effect of an environment on an individual is derived from the interaction of World environmental state and Amorpho requirements and condition. Environmental Fit evaluates; it is not a third owner of truth and holds no environmental or biological model of its own. Its results feed stability, stress, recovery, growth, development, reproductive performance and, across generations, selection pressure.
- **Rationale:** A derived bridge keeps both sides free to become more sophisticated without a shared hidden model in the middle.
- **Consequences:** Environmental Fit is not a synonym for stress; deterioration, equilibrium, stability, recovery, growth and improvement are all possible outcomes (AMO-D033). **Terminology:** Environmental Fit is the refined name for the concept [02_WORLD_MODEL.md](02_WORLD_MODEL.md) introduced as *suitability*; *effective environment* is unchanged and remains the World-side input to it. Extends AMO-D013.
- **Revised:** 2026-09-21, environment v0 — the output contract is specified (AMO-D049): per-dimension fit, biological direction, stress pressure, growth/recovery opportunity and critical constraint indicators. Substance unchanged.

## AMO-D038 — The Evolutionator owns inheritance, variation and generational change

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** A third independent long-term simulation domain, the **Evolutionator**, owns inheritance, heritable variation, recombination where appropriate, future mutation and variation mechanisms, transmission of traits through reproduction, generational change and population-level change over time. It answers *how are traits transmitted and changed across reproduction and generations?* It owns neither environmental conditions nor individual requirements, and it does not decide that a population should become adapted to a named place.
- **Rationale:** Inheritance, environment and biology change at different rates and should be improvable independently over the project's lifetime.
- **Consequences:** The Evolutionator needs no country names, continents, climatic-zone labels, borders or region names; logic such as `if location == Russia → increase cold resistance` violates the architecture. Adaptation emerges from variation, Environmental Fit, differential success and inheritance. World, Amorpho and Evolutionator meet through explicit boundaries, never shared hidden assumptions. The genetic abstraction remains open (AMO-Q013, AMO-Q052).

## AMO-D039 — Individual acclimation is distinct from generational evolution

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** Changes within one individual's lifetime — acclimation, developmental response, health and condition changes, resource accumulation, different phenotypic expression, recovery, stress response — are not evolution. A plant does not become genetically cold-adapted because it spent a long time somewhere cold. Evolutionary change occurs across reproduction and generations, when heritable variation meets differential success repeatedly.
- **Rationale:** Conflating the two would make the whole generational system meaningless and would quietly turn acclimation into a stat upgrade.
- **Consequences:** Individual improvement under a favourable environment (recovery, healthier growth, better development, improved reproductive condition) is Environmental Fit acting on one plant; shifting trait distributions is the Evolutionator. Both must be documented and modelled separately. Extends AMO-D012 to the Evolutionator boundary.

## AMO-D040 — Environmental and player-driven selection both shape lineages

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** Selection pressure may come from the World and from players simultaneously. The World creates it without knowing anything about evolution, simply by producing conditions under which some heritable variants perform better. Players may create it deliberately by choosing which individuals reproduce. A cultivated lineage may therefore reflect both what the player selected and what the World allowed to thrive. Evolutionary change is emergent: there is no generic `EVOLVE` action that upgrades a species once enough experience accumulates.
- **Rationale:** Emergent, systemic change produces more meaningful long-term history than stage evolution, and it lets players influence outcomes without commanding them.
- **Consequences:** No selectable trait list is defined and no breeding algorithm is designed (AMO-Q052, AMO-Q054). Distinctive game-world lineages within a real species are expected and are never new species (L3, AMO-D005). Divergence limits and the interaction with hybridization are open (AMO-Q053, AMO-Q055).

## AMO-D041 — Standard and VR Gameplay are first-class interfaces to one game

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** Standard Gameplay and VR Gameplay are two first-class entry points into the same Amorpho game — not separate games, persistent worlds, accounts or progression systems. A player who has played only in Standard Gameplay for years and later obtains VR hardware enters the same world as the same character, with the same plants, houses, greenhouses, ownership and history.
- **Rationale:** The persistent world and the player's accumulated history are the product. An interface is a way to inhabit them, not a second product.
- **Consequences:** No "Amorpho VR" as a separate title, world or save. The embodiment model (AMO-D028) already separates *who the player is* from *which body they occupy*, which this builds on. The technical architecture is deliberately unresolved; no classes, APIs or code follow from this decision.

## AMO-D042 — VR is optional, never secondary

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** Amorpho is neither a VR-only game, nor a conventional game with a VR novelty mode, nor a VR game with a reduced non-VR fallback. A player on conventional hardware must be able to experience the complete game — world exploration, collection, ownership, cultivation, propagation, trading, property, greenhouses, astral transfer, embodiment, combat, progression, social systems and persistent-world participation — and a VR player must eventually be able to remain in VR for the complete meaningful experience, across both the Human / World and Amorpho layers.
- **Rationale:** Either interface being a compromise would make one group of players second-class in a world they share.
- **Consequences:** Standard combat is not reduced because VR exists (AMO-D008). VR is not combat-only, sightseeing-only or a collection viewer. VR-native combat is a deliberately designed discipline, not a remapped gamepad (AMO-Q059), and competitive parity between the interfaces is an open problem requiring prototypes (AMO-Q060).

## AMO-D043 — Account for VR early; defer VR production cost

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** VR influences architecture from the beginning but does not trigger production work now. Amorpho avoids unnecessary flat-screen-only architectural assumptions, avoids core gameplay concepts that fundamentally require a 2D UI, preserves semantic separation between gameplay meaning and physical input, and considers embodiment and physical scale when designing world interactions. It does **not** build VR hands, tracked bodies, VR locomotion, motion controllers, hand tracking, VR avatars, VR combat, headset-specific rendering or XR menus, and it commits to no VR hardware, SDK or middleware.
- **Rationale:** *Account for VR early. Pay for VR production when the project is ready.* The risk to avoid is years of decisions that make full VR prohibitively expensive to add; the opposite risk is paying for VR production before the game exists.
- **Consequences:** Core rules should express gameplay intent rather than hard-coding one physical input method — but no intent API is defined and no abstraction is built for its own sake. VR joins the engine decision criteria (AMO-Q036, AMO-D020). Platform and hardware choices stay open (AMO-Q062). This is a constraint on design, not a licence to build.

## AMO-D044 — No shared cross-project VR platform; prove first, extract later

- **Status:** ACCEPTED · **Date:** 2026-09-20 · **Origin:** Embodiment and systems brief
- **Decision:** Amorpho creates no shared Trederus Maximus VR framework and introduces no dependency to or from any sibling project, and no cross-repository infrastructure. If Amorpho and, later, another project demonstrate through repeated real use that certain interaction primitives are genuinely generic, they may eventually be extracted deliberately. The path is project-specific implementation → repeated real use → proven generic behaviour → deliberate extraction → optional shared technology; never shared framework first.
- **Rationale:** *Prove first. Extract later.* A framework designed before two real users exist would force both into abstractions neither needs, and would breach Amorpho's independence.
- **Consequences:** Reuse potential for other projects is context only, never architecture (AMO-D002, AMO-D018). Interaction primitives such as grab, hold, inspect, place, point, select, open, navigate, manipulate and interact are illustrative examples, not a planned library. See [11_STANDARD_AND_VR_GAMEPLAY.md](11_STANDARD_AND_VR_GAMEPLAY.md).

## AMO-D045 — Amorpho's World is Earth

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** World foundation brief
- **Decision:** The long-term Amorpho World is a coherent representation of the real Earth. Real continents, countries, regions and cities form the geographic foundation for both Human and Amorpho gameplay, including the real areas associated with real *Amorphophallus* species. Fidelity may increase progressively over the project's lifetime and does not imply one-to-one representation of every road, building, street or tree.
- **Rationale:** Human life, travel, cultivation, native species geography, climate, introduced populations and social infrastructure all need one shared coherent geographic world. A fictional substitute for Thailand, Indonesia, Africa, India, Australia, Europe or Russia would cost the game the meaning that real provenance and real journeys give a plant.
- **Consequences:**
  - No fictional world map is substituted for Earth, and no invented stand-in for a real region.
  - Human and Amorpho gameplay occupy the **same** Earth — not a civilisation map and a separate habitat map. Cities and natural environments coexist, and the world must remain believable to live in *and* biologically meaningful (AMO-D009).
  - Native geography and Environmental Fit stay separate concepts. Where a species originates is not where it may live: `native country = allowed` and `non-native country = forbidden` remain excluded (L9, AMO-D013, AMO-D035–AMO-D037).
  - Local spaces — properties, buildings, greenhouses, beds, pots — have a place *inside* Earth geography rather than being detached instances, so outside conditions can reach them (AMO-Q064, AMO-Q065).
  - Players may change distribution over time: collection, transport, cultivation, propagation and outdoor establishment can create introduced populations far from a species' origin (AMO-D010).
  - World detail may grow progressively without invalidating the higher-level geographic structure.
  - **No map technology, data source, streaming architecture or world-instance model is selected by this decision** (AMO-D020, AMO-Q001, AMO-Q066). It authorises no global map, GIS ingestion, imagery, procedural cities, terrain generation, navigation or weather service.
  - Real Earth geography never implies anything about a player's real residential address; that separation stands (AMO-Q003).
  - No geographic facts enter approved input now. If species origin data is ever needed, it arrives through the Reality Gate once a game system requires it (AMO-D025, AMO-Q019).

## AMO-D046 — World environment is local and time-dependent

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Environment v0 brief
- **Decision:** The World produces a **Local Environment State** for a specific place, time and local context — conceptually `LocalEnvironment(place, time, context)`. Environment is never a permanent property of a place. World conditions are progressively modified into local conditions by season, weather, time of day, buildings, shelter and eventually containers, and the result always presents the same environmental dimensions.
- **Rationale:** Season, weather and controlled environments are where most of the interesting variation lives. A place-only model could not express any of it, and a context-free model would force every building and pot to become a special case.
- **Consequences:** The same geographic position may carry different environments outside, in a house, in a greenhouse, under shade or in a root zone. Because modifiers produce the same dimensions, Environmental Fit never learns about buildings (AMO-D035). No nesting mechanics, resolution or update frequency are defined (AMO-Q065, AMO-Q074). Geography locates; the World describes (AMO-D045).

## AMO-D047 — Environment Vector v0: five neutral dimensions

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Environment v0 brief
- **Decision:** Version 0 of the World Environment Vector has five dimensions: **temperature**, **water availability**, **light availability**, **air moisture / humidity**, and **exposure / protection**. They are neutral World facts and are never labelled good, bad, suitable, unsuitable, tropical or species-compatible. Water availability means usable moisture at the root system, not rainfall. Air moisture is kept separate from water availability because they are biologically different. Exposure / protection is an explicitly provisional coarse abstraction expected to decompose later.
- **Rationale:** Five dimensions are enough to produce meaningful, explicable outcomes indoors and outdoors, across seasons, for any species — and few enough to understand and test. Naming what the plant experiences, rather than the mechanisms that produce it, lets rainfall, irrigation, drainage, canopy and artificial light be added later without changing what Fit consumes.
- **Consequences:** Deferred until gameplay demonstrates a need: soil chemistry, pH, nutrients, altitude as a direct variable, wind as its own vector, atmospheric pressure, rainfall history, pathogen load, pests, pollinators, drainage mechanics and substrate chemistry. No units, scales or normalisation are chosen (AMO-Q069). No species values exist, and none may be invented (L4, AMO-D025, AMO-D036). This applies AMO-D025's discipline to design data: *add environmental dimensions when gameplay or biological modelling demonstrates a need.*

## AMO-D048 — Amorpho response profile v0: zones, three contributing layers

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Environment v0 brief
- **Decision:** For each environmental dimension, the Amorpho side eventually provides a biological response profile expressed as zones rather than a single ideal value: a **preferred range** (can thrive), a **tolerable range** (outside preferred, still manageable) and a **critical boundary** (beyond which severe stress or damage may develop). The effective profile an individual responds with is layered from **species baseline** + **individual traits** + **current condition**.
- **Rationale:** Zones are the smallest structure that distinguishes thriving from surviving from failing, which is the distinction the whole model exists to make (L38). Layering means individual variation and condition have somewhere to live from the start instead of being retrofitted onto a species-only model.
- **Consequences:** No numeric values exist, and none may be guessed (L4). Not every dimension necessarily needs exactly three hard ranges forever; a later implementation may use continuous response curves (AMO-Q069). Genetics remain the Evolutionator's (AMO-D038) and acclimation remains open (AMO-Q012). Which current-condition variables exist is open (AMO-Q073). Species profile data enters only through the Reality Gate, and only after the model needing it exists (AMO-D053).
- **Revised:** 2026-09-21, condition v0 — the layering gains a fourth contributor: **developmental state**, beside current condition (AMO-D057), and the condition layer is specified as vitality, stress load and reserves (AMO-D056). Condition degrades the profile; development changes which sensitivities apply. Substance unchanged.

## AMO-D049 — Environmental Fit v0 output contract

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Environment v0 brief
- **Decision:** Environmental Fit v0 consumes a Local Environment State and an effective response profile and produces: **(A)** fit by dimension; **(B)** biological direction — conceptually improving, stable or deteriorating; **(C)** stress pressure; **(D)** growth / recovery opportunity; **(E)** critical constraint indicators. Per-dimension information is preserved alongside the aggregate. Fit must eventually support **limiting-factor** behaviour: catastrophic failure in one dimension may not disappear behind excellent values elsewhere.
- **Rationale:** The aggregate is what downstream systems act on; the per-dimension detail is what makes it possible to ever explain *why* a plant is struggling. Naive averaging would let a plant with no water be rated "good" because the light is excellent.
- **Consequences:** Outputs D and C together make positive, neutral and negative trajectories first-class, so Fit is never a synonym for stress (AMO-D037, AMO-D033). No numeric ranges, scales or aggregation formulas are defined (AMO-Q070). Dimensions are treated independently in v0, but the architecture may not assume they stay independent forever (AMO-Q071). Nothing further is added to the contract without a demonstrated downstream need.
- **Revised:** 2026-09-21, interaction boundary — output **A** is *independent* dimension fit and is read together with **E**, which names constraints that may be a dimension **or an interaction between dimensions** (AMO-D055). No output was added or removed; substance unchanged.

## AMO-D050 — Inhabitability is downstream of biological condition

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Environment v0 brief
- **Decision:** Neither the World nor geography may set `inhabitable = false` directly. Inhabitability is evaluated from the individual's current biological condition, which is itself produced by Fit acting over time: *World environment + Amorpho → Fit → condition → inhabitability*.
- **Rationale:** It is what lets one location affect different species differently, different individuals differently, and the same individual differently over time. A place is never inherently un-inhabitable; a plant's condition is.
- **Consequences:** No location, region or climate may carry an inhabitability flag. The rescue window is emergent, not a system: it exists only while a negative trajectory is running and the individual is still inhabitable (AMO-D031, AMO-D034). Where the threshold sits and how it relates to health remains open (AMO-Q042).

## AMO-D051 — Environment describes conditions, not permissions

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Environment v0 brief
- **Decision:** The World never prevents a player from taking an Amorpho into an unsuitable environment. It states the conditions; the player decides whether the risk is acceptable; the consequences emerge through Fit.
- **Rationale:** Blocking movement would replace a judgement with a rule and destroy exactly the decisions the environmental system exists to create. It is also the agency form of L9: the map is not a permission list.
- **Consequences:** No travel, planting or rooting action is gated on environmental suitability. Simulation truth and player knowledge stay separate: the player may have forecasts, sensors, knowledge or warnings, and how much certainty is exposed is open (AMO-Q044). In particular nothing assumes the player sees an exact countdown to non-inhabitability.

## AMO-D052 — Fit is deterministic for identical state; randomness is upstream

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Environment v0 brief, derived
- **Decision:** Given identical World state and identical Amorpho state, Environmental Fit itself produces the same result. Randomness belongs to the systems where it carries meaning — weather, individual biological variation, stochastic events, pests, future disease and other World events — which sit upstream of Fit, in the state it evaluates.
- **Rationale:** Hidden rolls inside the evaluator would make outcomes unexplainable to players and untestable for the project, while adding nothing that upstream randomness cannot express. Determinism here also makes the validating spike meaningful.
- **Consequences:** Variation between two apparently similar plants comes from genuinely different state — individual traits, condition, exposure history — not from a die roll inside Fit. This is a conservative v0 position about the *evaluator*, not a claim that biology is deterministic; whether it should hold as the model matures is open (AMO-Q075).

## AMO-D053 — The design model precedes importing real environmental data

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Environment v0 brief
- **Decision:** The game-side environmental model is designed first; approved real-world environmental facts are imported only afterwards, and only in the minimal form the finished model demonstrably needs. No environmental field enters approved input before the system that consumes it exists.
- **Rationale:** Importing first would let the shape of someone else's data decide the shape of the game's model, which is the coupling the Reality Gate exists to prevent.
- **Consequences:** `data/input/amorphophallus_species.csv` remains `species_id,scientific_name` with no environmental columns. This is AMO-D025 applied to the environment model, and it makes v0 the precondition for ever extending the input contract. What minimal approved input a species response profile would need is an open question, not a design (AMO-Q076, AMO-D024).

## AMO-D054 — Rooting may be strategic and long-term

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Strategic rooting brief
- **Decision:** Rooting is **not primarily an emergency or recovery mechanic**. A suitable rooted environment can support indefinite healthy life, growth, development and eventual reproduction. Rooting may be the *reason* for a journey rather than the end of one: a player may deliberately inhabit an individual and move it across the world in order to establish it somewhere chosen. At least three player intentions sit behind the same act — **emergency rooting** (leaving it somewhere less than ideal, concerned with survival and rescue), **operational rooting** (stationing it somewhere it may be useful later, often seasonally), and **strategic establishment** (settling it somewhere biologically suitable for long-term life). These describe purposes, not required runtime states.
- **Rationale:** A model in which rooting is mainly something that goes wrong would waste the entire positive half of Environmental Fit and would make a collection a set of parked objects rather than a spatial strategy. If excellent conditions can only restore a plant to "unharmed", there is no reason to seek them out.
- **Consequences:**
  - The positive side of Fit must support at least two distinct uses: **restoring** condition, and **supporting continued development** once recovery is complete (L38, AMO-D049). Recovery is not the top of the model.
  - **Rooted does not mean inactive.** Growth, seasonal development, flowering, pollination, reproduction, health, stress, recovery, interaction with local populations and selection pressure may all continue while the player is elsewhere — which follows from the world persisting independently of players (AMO-D009).
  - Geography becomes strategically meaningful: habitat is worth finding, reaching, acquiring and protecting, and a location suitable only part of the year makes deliberate **seasonal routing** possible (AMO-Q078).
  - Operations involving several individuals stay **sequential**, never simultaneous; the one-body law is what gives spatial arrangement its cost (AMO-D028, AMO-Q081).
  - Long-term rooted populations are the bridge to the Evolutionator: they supply the conditions under which selection can operate, without the Environment creating traits or the Evolutionator reading place names (AMO-D038, AMO-D040).
  - No mission mechanic, farming subsystem, pollination engine, land-rights system or population model is authorised by this decision. The provisional term *"Amorpho Farming"* is **not** a product term and no named subsystem is created (AMO-Q080).
  - Hybridization policy is untouched: only approved compatible species pairs, symmetric, with absence of approval never asserting biological impossibility (AMO-D027).

## AMO-D055 — World owns environmental interactions; Fit owns biological ones

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Interaction boundary brief, tested
- **Decision:** Environmental dimensions may interact, and the two kinds of interaction have different owners.
  - A **World-side interaction** is one environmental condition physically changing another — heat increasing evaporation so root-zone water availability falls. The World resolves it into the Local Environment State, and Environmental Fit simply evaluates the resulting values.
  - A **Fit-side interaction** is a combination changing an individual's biological response while the World values stay exactly as they are — a temperature and a water availability that are each tolerable alone producing real deficit together, because this individual's water demand rises with temperature.

  The discriminating question is: **could the World compute this interaction without knowing what organism is present?** If yes, it belongs to World; if no, to Fit. Equivalently: *does the environment change itself, or does the organism respond differently to the same environment?*
- **Rationale:** Demonstrated rather than assumed. In [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md) §17, raising temperature within its tolerable zone while holding water availability *identical* produced a materially worse trajectory — an outcome expressible only as a Fit-side interaction. Putting such interactions in World would force the World to know which organism is standing somewhere before it could report conditions, and to report different conditions for two plants in the same place, which AMO-D035 forbids.
- **Consequences:**
  - **Double-counting is a real hazard** and the one-line rule — *World computes environmental causation; Fit computes biological consequence* — does not by itself catch it, because a Fit term over temperature and water looks identical whether it encodes biology or silently re-encodes evaporation. Two disciplines apply: every Fit-side interaction must be justifiable **with World values held fixed**; and **Fit must not compensate for a thin World** — a missing World process is a reason to extend World, not to approximate it inside Fit.
  - **Output A is independent dimension fit** and cannot express combinations; it is read together with E. **Output E names constraints, which may be a dimension or an interaction**, so a critical constraint can arise from an interaction while no single dimension is critical (AMO-D049).
  - No new environment dimension and no new Fit output follow. An interaction is a relationship *between* existing dimensions, not a new fact about the world.
  - Representation is **not** decided: interaction terms, response surfaces, conditional curves, modifiers and nonlinear aggregation all remain candidates, as do how many interactions are worth modelling, how they are sourced and how they are explained to players (AMO-Q071).

## AMO-D056 — Current Biological Condition v0: vitality, stress load, reserves

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Condition v0 brief, tested
- **Decision:** Every persistent individual carries a **Current Biological Condition** of three variables, as live world state belonging to the individual:
  - **Vitality** — present biological soundness and viability. Carries compromise in a form a recoverable buffer cannot, and is what survival and inhabitability hang on.
  - **Stress Load** — accumulated burden from adverse conditions. **History, not damage.** It gives the individual memory of exposure *duration*, and it carries the accumulation half of exposure history so no separate store is needed at this depth (AMO-Q072).
  - **Reserves** — abstract internal capacity that buffers adverse periods, funds recovery, and receives positive Fit once recovery is complete.

  Condition is read at `t` and written at `t + Δt`: **a feedback loop across time, not a circular definition.** It is one of the layers forming the effective response profile *and* the thing Fit modifies, and both roles are intended.
- **Rationale:** Tested rather than assumed, against the four worked scenarios in [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md). A single `health` scalar **fails Scenario C**: once it saturates at healthy, favourable Fit has nothing left to act on and output D must fall to zero, which the spec forbids (L38). Each retained variable does work no other does — remove stress load and Scenario A loses its delayed onset and therefore its rescue window; remove reserves and Scenario C phase 2 and differential resilience at equal health both collapse. Stress load and reserves are not mirror images: reserves are also spent on growth, so under excellent Fit reserves may fall while stress is zero.
- **Consequences:**
  - **Inhabitability is derived from condition, never stored** (AMO-D050) — principally from vitality, plausibly also stress load; the rule and threshold stay open (AMO-Q042). This is what makes `alive ≠ inhabitable` work.
  - The path `viable → deteriorating → critical → non-viable` is preserved without death being designed (AMO-Q045).
  - Deliberately excluded: hydration, carbohydrate state, membrane or organ damage, metabolic pools, hormone state, nutrient status, separate injury tracking. Reserves in particular must not become a general-purpose meter for unmodelled systems.
  - Condition is **never inherited**: a stressed parent does not produce genetically stressed offspring (AMO-D038, AMO-D039, L32). It is world state, never approved input, and no condition field is added to the species CSV (AMO-D021, AMO-D053).
  - Condition **persists across rooted ↔ animated**, since it is one individual (AMO-D030); whether animation costs reserves or adds stress is open (AMO-Q083). Whether combat touches condition is left possible and undecided (AMO-Q026).
  - **Vitality is the variable most likely to prove derivable.** If no harm is ever permanent it could in principle be recomputed from stress and reserves. It is stored because irreversible damage, if introduced, cannot be carried by a derived summary — and the test that settles it is AMO-Q045.
- **Revised:** 2026-09-21, harm and maturity — the caveat above is **superseded by AMO-D076**, which keeps vitality as stored state for a stronger reason: two individuals with identical stress and reserves may still differ in remaining core compromise, so no function of the other two can distinguish them. The argument no longer depends on permanence, and AMO-D075 withdraws the assumption that any harm is permanent. The three variables are unchanged.
  - Dynamics, rates, thresholds and the profile-modifying function are not defined (AMO-Q073, AMO-Q074).

## AMO-D057 — Developmental State is a separate axis from condition

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Condition v0 brief, tested
- **Decision:** **Developmental State** — what biological phase an individual is in — sits *beside* Current Biological Condition, not inside it. An individual therefore carries persistent identity, inherited traits, current condition and developmental state as four distinct kinds of state, all of which feed the effective response profile.
- **Rationale:** Three arguments, of which the third is decisive. They are **orthogonal** — healthy and dormant, healthy and growing, stressed and growing are all coherent. Condition is **evaluative** and development is not: a seedling is not in worse condition than a mature plant, so folding development into condition would make "more developed" read as "better" and let a large unhealthy plant score well — the confusion L38 exists to prevent. And they **shape the response profile differently**: condition degrades it uniformly, while development changes *which* sensitivities apply at all, since a dormant individual differs from an actively growing one in kind rather than degree. Categorical and degradational influences do not belong in one variable.
- **Consequences:** The developmental **state machine is deferred** — dormant, active growth, flowering, reproductive and any other phases are not designed, and no species' life-cycle facts are assumed or imported (AMO-D024, AMO-Q012). Positive Fit has two sinks after recovery completes: reserves and development (AMO-D054). Whether death is a vitality threshold, a terminal developmental state, or both, is open (AMO-Q045). Recorded as L40.
- **Revised:** 2026-09-21, life cycle — developmental state gains v0 content (five phases, AMO-D059) and becomes gameplay-relevant: it determines which body is expressed and whether the phase permits astral entry (AMO-D063). Substance unchanged.
- **Revised:** 2026-09-21, harm and maturity — a further persistent dimension sits beside condition and developmental state: **Developmental Maturity**, how far the individual has developed across repeated cycles (AMO-D077). Substance unchanged.

## AMO-D058 — The individual persists; its biological manifestation changes

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Life cycle and anchors brief
- **Decision:** A persistent individual is not identical to its current visible plant structure. The same individual may exist at different times as a rooted tuber, an actively growing leaf-form plant, a flowering individual, or something transitional, while identity, lineage, genotype, provenance, ownership and history stay attached to the individual throughout. **Each phase is never a new individual.**
- **Rationale:** It is the same principle that already makes an Amorpho the plant rather than a separate creature (AMO-D030), extended along time instead of across the embodiment boundary. Without it, a plant that loses its leaf and grows another would be two plants, and lineage records could not survive an ordinary season.
- **Consequences:** **Damage to a temporary manifestation and damage to the persistent core have different consequence horizons.** Leaf damage may persist for the rest of a phase without being permanent for the individual; when the phase ends, its temporary structure and whatever damage it carried cease to exist, while core state remains. This reserves a future split between **phase-specific integrity** and **persistent core vitality** (AMO-D056) without designing either (AMO-Q086). It also makes identity after catastrophic core loss a real question rather than an edge case (AMO-Q094). Extends AMO-D011 and AMO-D030.

## AMO-D059 — Life-cycle phases v0

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Life cycle and anchors brief
- **Decision:** Five broad life-cycle phases are recognised: **Tuber / Dormant**, **Emergence / Sprouting**, **Leaf**, **Bloom / Flowering**, and **Senescence / Dormancy entry**. Developmental State determines which is currently expressed. **Bloom is a rare, short, exceptional phase** — a temporary superstate offering capabilities unavailable in other forms, not Leaf Form with better numbers, and not automatically superior.
- **Rationale:** These are the phases gameplay already needs to distinguish: different playable bodies, different availability, different risk. Recognising them is what makes seasonal roster availability and Bloom's strategic value expressible at all.
- **Consequences:** This is **not a finished state machine**: sequencing, overlap, duration, species variation, and whether leaf and bloom can coexist are all open, and no species' real life cycle is assumed or imported (AMO-D024, AMO-Q084). Bloom's abilities, duration and trade-offs are undesigned (AMO-Q088), as are premature dormancy triggers and costs (AMO-Q087). **Dormancy entry should normally give visible biological warning** before availability closes — a player should not simply be told *unavailable* (AMO-Q085). Gives AMO-D057's developmental axis its first content.
- **Revised:** 2026-09-21, harm and maturity — Bloom additionally requires **species-specific flowering maturity**, so a healthy individual is not automatically Bloom-capable, and Bloom is repeatable and may become more developed with maturity (AMO-D078). Substance unchanged.
- **Revised:** 2026-09-21, state machine — the five phases become seven states in three families, with Bloom a **sibling active state** rather than a linear stage (AMO-D070, AMO-D071). Substance unchanged.

## AMO-D060 — Deep Dormancy closes the astral door and hides the individual

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Life cycle and anchors brief
- **Decision:** A **deeply dormant tuber is not astrally inhabitable**, even when an Anchor is physically present and the relationship is recorded. This is biological unavailability, not loss of ownership or of the Anchor. A deeply dormant, unexposed tuber is also **normally extremely difficult or impossible for others to discover** unless its physical location is already known — no leaf, no flower, no scent signature, no movement.
- **Rationale:** The two halves are one deliberate trade-off: dormancy buys safety with unavailability. It also gives the world a state in which a valuable individual is genuinely protected without any protection mechanic, and in which only the human layer can act.
- **Consequences:** Concealment is **not magical invisibility** — someone who knows the exact site, pot or greenhouse bed can still find it physically. What may not exist is a generic world signal revealing dormant tubers. An anchored dormant individual may remain listed as connected while being unreachable, and information during dormancy may be deliberately minimal (AMO-Q092). Whether the whole tuber phase is equally closed is open: transitional windows after dormancy entry and before emergence remain a design direction, not a rule (AMO-Q085). Extends AMO-D015 and AMO-D031.

## AMO-D061 — Astral Anchors are physical, reusable objects on individuals

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Life cycle and anchors brief
- **Decision:** An **Astral Anchor** is a physical, reusable magical object attached to an individual Amorpho, providing the physical side of the astral access path. It is associated with the **persistent individual**, not with the pot, property, greenhouse or location: if the plant is repotted, moved, animated or rooted elsewhere, the Anchor stays with it until physically removed. Removing it ends normal astral access through it and changes nothing biological — lineage, genotype, condition, developmental state and world history all remain, and the plant simply continues living unbound.
- **Rationale:** Making the access path a physical object rather than a bookkeeping field is what forces the human layer to participate in roster decisions, and what lets release, theft and trade be real world events.
- **Consequences:** Anchor count becomes a strategic constraint, so a limited supply makes the player choose which individuals are astrally reachable. Anchors are **not roster slots** and may not behave as invisible entries reassigned from a menu, though an interface may later assist. The **Astral Radar is a view of the player's own anchored connections, not a global botanical scanner** (AMO-Q092).
- **Revised:** 2026-09-21, biology-magic boundary — the Anchor is explicitly **not a tracker**: attachment guarantees neither an active astral signal nor location information, and Deep Dormancy silences the signal entirely (AMO-D088). Substance unchanged. Nothing about the economy is decided — starting count, maximum, rarity, price, crafting, acquisition, destructibility, grades, independent theft (AMO-Q090, AMO-Q091). Name, physical form, attachment method and any pairing ritual with the Warden artifact are open (AMO-Q021, AMO-Q089).
- **Revised:** 2026-09-21, Warden progression — physical Anchor supply is only one of two constraints; **Astral Capacity**, a human capability, separately bounds how many active Anchor relationships can be sustained (AMO-D067). Substance unchanged.

## AMO-D062 — Only the human may attach, remove or move an Anchor

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Life cycle and anchors brief
- **Decision:** Only the human player can physically attach, remove, transfer or reconfigure Astral Anchors. An inhabited Amorpho cannot remove its own Anchor, move it to another individual, reconfigure the anchored roster, or attach Anchors remotely, and no other Amorpho may do so on the player's behalf.
- **Rationale:** *The soul may travel; the Anchor must move by human hands.* Changing which individuals are playable must cost human-world action, or the astral layer quietly replaces the human layer it is supposed to complement (L23, AMO-D029).
- **Consequences:** Reallocating an Anchor requires physically reaching both individuals, which makes geography and travel part of roster management (AMO-Q002). Only the human can collect unbound plants, redistribute a limited supply, perform future pairing, and physically manage dormant individuals. Recorded as L42.

## AMO-D063 — Astral entry requires three independent gates

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Life cycle and anchors brief
- **Decision:** Normal astral entry requires all three of: an **Astral Anchor** (a physical access path), **life-cycle accessibility** (the current phase permits entry), and **biological inhabitability** (the individual is well enough). Each can block independently, and they are genuinely orthogonal.
- **Rationale:** They fail for different reasons and are restored by different actions — an Anchor by human travel, a phase by time and season, condition by care and environment. Merging any two would hide which one is actually stopping the player.
- **Consequences:** An active healthy unanchored plant has no path; an anchored dormant one has a path but a closed phase; an anchored active critically stressed one is blocked by condition alone (AMO-D031, AMO-D050). The playable roster is therefore an **emergent subset** of the collection, and owning many individuals does not produce many playable characters — the one-body law then allows only one to be inhabited at a time anyway (AMO-D028).
- **Revised:** 2026-09-21, Warden progression — **Astral Capacity** sits upstream of these gates, bounding how many active Anchor relationships can exist at once (AMO-D067). It is not a fourth gate; it constrains the supply feeding the first. Substance unchanged.
- **Revised:** 2026-09-21, state machine — the life-cycle gate is supplied by the state machine's access status, which is Open, Transitional or Closed and varies across transitional phases (AMO-D070, AMO-D073). Substance unchanged.

## AMO-D064 — Biological life is independent of anchoring; new individuals begin unbound

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Life cycle and anchors brief
- **Decision:** An individual needs no Anchor to exist. Unanchored plants grow, enter dormancy, emerge, flower, reproduce, die, establish populations and participate in evolution exactly as anchored ones do. Wild populations begin biologically persistent, unanchored, unowned and without a human warden, and that must remain possible indefinitely. **Every newly created biological individual begins without an Anchor** — seedlings, germinated seeds, vegetative offspring, bulbils, other clonal propagation and hybrids alike. Parent ownership and anchoring never propagate to offspring.
- **Rationale:** Anchoring is a human fantasy-control layer laid over a biological world that does not need it. If offspring inherited anchoring, a collection would compound into a roster by itself and the world would gradually become the property of whoever got there first.
- **Consequences:** Anchors are **never** required for reproduction or population persistence; population and evolutionary processes operate on biological individuals (AMO-D038, AMO-D040). The game never assumes every plant belongs to a player. Release is a clean path from playable character to unbound living individual with nothing deleted. Rooted unanchored life continues developing unattended (AMO-D009, AMO-D054).

## AMO-D065 — Existence, ownership, custody, anchoring and availability are separate

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Life cycle and anchors brief
- **Decision:** Five axes are kept distinct and may disagree: the **biological individual** (it exists), **ownership** (who, if anyone, is recognised as owner), **physical custody** (who controls the plant or its location), **astral anchoring** (whose system is physically connected), and **astral availability** (whether conditions permit entry). They must never be reduced to a single `owner_id`.
- **Rationale:** They already diverge in ordinary cases — a wild plant exists with none of the others; a stolen anchored plant separates custody from ownership; a dormant anchored plant separates anchoring from availability. A single field could not express any of these.
- **Consequences:** **Ownership is not availability** (L43): a player may own an individual that cannot be played, and may physically hold an unowned, unbound plant that is not playable at all. Theft may take the plant, the Anchor or both, and physical possession is **not** assumed to grant astral access — rebinding rules are open (AMO-Q091, AMO-Q008). Trade must involve the physical Anchor: *astral access cannot change merely because an ownership field changed* (AMO-Q093). Legal and social mechanics stay separate from astral mechanics. World state holds all five (AMO-D021).

## AMO-D066 — Human/Warden progression is a distinct, slower domain

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Warden progression brief
- **Decision:** The human character progresses along a long-term magical and astral development path that is **separate** from Amorpho biological progression. Amorphos advance through growth, development, life-cycle phases, cultivation, reproduction, selection, lineages and generations; the human advances through magical capability. Human advancement should be substantially **slower and harder** than ordinary change in the Amorpho ecosystem, and should **resist trivial grind acceleration** — it must not collapse into *repeat an activity → farm experience → unlock quickly*.
- **Rationale:** The living world is meant to feel busy and largely outside the player's control. Against that, human development should feel fundamental rather than farmed. It also makes the human the **continuity character**: individual plants grow, reproduce, die, are traded and released, while the human persists through all of it — plausibly the slowest and most persistent progression a player ever builds.
- **Consequences:** Two deliberately different pacing speeds coexist, which may become defining for Amorpho. **No player-facing term is fixed** — *Warden Progression*, *Astral Development* and *Astral Capacity* are working concepts (AMO-Q100) — and **conventional levelling is not assumed**: levels, ranks, stages, milestones or another representation are all still possible (AMO-Q096). What actually advances a Warden is undecided, as is whether world time or real elapsed time constrains it, in either direction (AMO-Q097). Because this progression is meant to be the slowest thing a player builds, casually destroying it is architecturally discouraged; any loss or regression needs its own explicit decision (AMO-Q098).

## AMO-D067 — Astral Capacity is human capability, distinct from Anchor supply

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Warden progression brief
- **Decision:** **Astral Capacity** is the human character's ability to sustain multiple active astral connections at once. It is distinct from **physical Anchor supply**, which is how many reusable Anchor objects the human possesses (AMO-D061). A player may hold more physical Anchors than their capacity lets them sustain simultaneously; acquiring another Anchor object does not by itself widen what the human can hold open. Capacity sits **upstream of the three gates**, bounding how many active Anchor relationships can exist, rather than adding a fourth gate to entry (AMO-D063).
- **Rationale:** Splitting the constraint gives two independent scarcity systems — *do I physically have enough Anchors?* and *can I sustain this many connections?* — one belonging to the world and one to the character. It is also what keeps a large collection from converting into a large roster.
- **Consequences:** Capacity is deliberately **narrow**: it means capacity and nothing else. It does **not** limit how many plants a player may own, cultivate, trade, breed, maintain or establish (AMO-D065), and it does not affect wild populations or offspring, which remain unbound regardless (AMO-D064). On the Astral Radar it may mean more simultaneous connections shown, since there are more of them — but **not** better range, precision, positional information or biological sensing (AMO-Q092). Which of the two scarcities usually binds is undecided, as are starting value and any maximum (AMO-Q090, AMO-Q095).

## AMO-D068 — Additional Astral Capacity becomes progressively harder

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Warden progression brief
- **Decision:** Increasing simultaneous Astral Capacity becomes **progressively more difficult**. Specifically excluded is any simple linear rule of the form `level N = N Anchors`. Gaining one more point of capacity must read as a deep magical development of the character, especially at higher capacity — never as `+1 inventory slot`.
- **Rationale:** A linear slot progression would make capacity feel like storage and would let a determined player convert routine activity into simultaneous reach. An accelerating cost keeps each increase significant and makes very high capacity a genuine marker of long player history.
- **Consequences:** **No curve, value or requirement is defined** (AMO-Q095). Whatever presentation eventually exists should reinforce the weight of the advancement, but no ceremony, ritual or interface is designed here (AMO-Q100). Very high capacity may reasonably be uncommon; rarity, maximum, prestige and competitive implications are all undecided.

## AMO-D069 — Human progression expands capability without overriding rules

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Warden progression brief
- **Decision:** Human progression expands what the human **can do**; it never overrides biological or physical access rules. A highly developed Warden still cannot enter a deeply dormant individual, one too biologically compromised for entry, or a dead one; cannot move an Anchor without physically travelling to it; cannot locate plants, convert ownership into access, resolve custody or remove geographic strategy. Human development is also **not** assumed to make any Amorpho stronger, faster or more damaging.
- **Rationale:** Progression that dissolved world constraints would quietly delete the human layer's reason to exist — the very layer it is supposed to develop. *The soul may travel; the Anchor must move by human hands* holds at every level of advancement (L42, AMO-D062).
- **Consequences:** Deep Dormancy, biological inhabitability and the missing-Anchor case all remain absolute regardless of capacity (AMO-D060, AMO-D031, AMO-D050). Whether human development touches combat at all is open and constrained by skill remaining central to outcomes (L15, AMO-Q025). **Astral Capacity is the only confirmed dimension of human progression.** Astral perception, transfer stability, richer Anchor information, ritual capability and sensitivity to life-cycle transitions are recorded as possibilities only — none is accepted, and no skill tree exists (AMO-Q099).

## AMO-D070 — Life-cycle state machine v0: three families, seven states

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** State machine brief
- **Decision:** The life cycle of a persistent individual is modelled as **seven states in three families**: a **Dormant** family (Early Dormancy · Deep Dormancy · Pre-Emergence), an **Active** family (Active Leaf · Bloom), and the transitions between them (**Emergence** in, **Senescence** out). Astral accessibility is **Open**, **Transitional** or **Closed**, and is derived from the state *and progress through it* rather than stamped on each state — steady states hold one value, transitional states change value across their own span. Access narrows on the way down, widens on the way up, and has a genuinely closed floor at Deep Dormancy (AMO-D060).
- **Rationale:** This is the smallest topology that carries everything the accepted architecture already needs — closed dormancy, reopening access, an exceptional bloom, a survivable early retreat, and roster availability that changes on its own. Families group states that behave alike for access and manifestation without adding a layer of mechanics.
- **Consequences:** **Premature retreat needs no separate state**: Senescence is entered either on the ordinary course of a cycle or early under pressure, and the difference is carried by condition, reserves and development rather than by the graph (AMO-D056, AMO-Q087). A "successful season" flag would duplicate what condition already records. **Phase-specific damage outlasts embodiment** — leaving and re-entering does not repair a damaged leaf, because the damage belongs to the manifestation, not the animation (AMO-D058). Identity is never keyed to the current manifestation. The machine is deliberately **parameterisable**: durations, routing, triggers and species variation are all open, and no species' real cycle is assumed (AMO-D024, AMO-Q084, AMO-Q085, AMO-Q101).

## AMO-D071 — Bloom is a sibling active state, not a stage or an overlay

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** State machine brief, evaluated
- **Decision:** **Bloom and Active Leaf are peer states inside the Active family.** Entry into that family, movement between its states, and exit from it are **parameterised** rather than fixed. Bloom is astrally playable, subject to the ordinary gates.
- **Rationale:** Two alternatives were considered and rejected. As a **linear stage** (`Leaf → Bloom → Senescence`) it would force every individual through Bloom every cycle, contradicting its rarity (AMO-D059), and would hard-code a leaf-then-bloom ordering that cannot be assumed for all species. As an **overlay on Leaf** it could not express an individual that blooms without an active leaf, since the overlay would have nothing to attach to, and it would muddle manifestation — a bloom structure is its own temporary body, not a modifier on another. Sibling states avoid both.
- **Consequences:** An individual may bloom or never bloom; may enter the active family *as* Bloom without a leaf first; and post-Bloom routing stays open — back to another active state, or on to Senescence (AMO-Q084). A species that never blooms simply never enters the state, needing no special case. Bloom keeps its own manifestation, so a bloom-specific integrity and kit can attach later (AMO-Q086, AMO-Q088). v0 does **not** assume Leaf and Bloom can be occupied simultaneously, but because they are siblings a future model needing concurrency can express it without restructuring. The machine exposes `individual is in reproductive Bloom` so discoverability, pollination and reproduction can react without any of them being designed (AMO-Q015, AMO-Q079).

## AMO-D072 — Rooting, astral exit and dormancy are three separate things

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** State machine brief
- **Decision:** **Rooted** means the individual exists in plant state rather than animated, and is compatible with **every** life-cycle phase — a rooted Active Leaf and a rooted Bloom are ordinary. **Astral exit** ends animation and does **not** cause a phase transition: an inhabited leaf that roots is still in Active Leaf. **Dormancy** is a life-cycle phase. Conversely, inhabitation animates the current manifestation **without changing the underlying state**.
- **Rationale:** All three were at risk of collapsing into "the plant stopped doing something", which would make the model incoherent — most damagingly by implying that leaving an Amorpho puts it to sleep, or that a blooming plant cannot be left rooted.
- **Consequences:** A blooming individual can be rooted and left blooming; a leaf-phase individual can be entered and exited repeatedly within one phase. Phase-specific damage persists across those exits and re-entries (AMO-D070). Whether animation itself costs the individual anything biologically remains open (AMO-Q083). Extends AMO-D032.

## AMO-D073 — Availability follows biological state; no roster timer

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** State machine brief
- **Decision:** The playable roster changes because individuals **move through life-cycle phases**, never because availability is scheduled. There is no seasonal roster timer, rotation, or availability event anywhere in Amorpho. Life-cycle state supplies the **middle of the three gates** and is not a fourth one (AMO-D063).
- **Rationale:** A schedule would be a second, competing source of truth about availability, and it would sever the connection between what a player did with their plants and what they can play — which is the connection the whole cultivation layer exists to create.
- **Consequences:** Hemisphere and geographic strategy stay **emergent**: nothing encodes *northern = dormant*, and a distributed collection can have different individuals available at the same global moment (AMO-D045, AMO-D046). Human Astral Capacity cannot force a phase open (AMO-D069, L44), and an Anchor persists through every phase change until a human removes it (AMO-D061, AMO-D062). Because availability is what players plan around, transitions should normally be **legible enough to support decisions** rather than arriving as arbitrary lockouts (AMO-Q085). Recorded as L45.

## AMO-D074 — Three harm horizons; manifestations do not inherit damage

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Harm and maturity brief
- **Decision:** Biological harm is classified by **horizon**, not by severity alone:
  - **Temporary manifestation damage** — structural harm to the currently expressed body (leaf integrity, bloom structure), bounded by that manifestation;
  - **Persistent core damage** — harm to what carries the individual across phases, recorded in **vitality**, spanning astral exit, senescence, dormancy, new emergence and the end of a bloom;
  - **Reversible burden** — stress load and depleted reserves, which are not structural damage and recover substantially faster.

  A later manifestation **does not inherit** the previous one's structural damage: a new leaf or a new bloom begins structurally fresh.
- **Rationale:** A damaged leaf is not a damaged core, a stressed individual is not a damaged one, and a depleted individual is not a compromised one. Without the split, any single "damage" number would have to be either too forgiving for a ruined core or too punishing for a torn leaf.
- **Consequences:** Seasonal structural renewal happens **without erasing biological history** — the individual carries reserves, stress, vitality and developmental maturity into the next cycle even though the structure is new. **Recovery of the individual is not repair of the manifestation**: a physically damaged leaf does not become whole because conditions improved, and how much in-phase repair is possible is open (AMO-Q103). Damaged seasons are **graded, never binary** — moderate damage may still allow a completed phase, some reserve gain and some maturity gain (AMO-D070). Phase-specific integrity stays per-manifestation; no universal body-integrity meter is created (AMO-Q086).
- **Revised:** 2026-09-21, biology-magic boundary — **Tuber** is the canonical term for the persistent core structure, and a further distinction applies: **Programmed Tuber Draw** (normal biological spending, e.g. Bloom) is not harm, unlike Pathological Tuber Impact (AMO-D087). Wording here is left as written; substance unchanged.
- **Revised:** 2026-09-21, manifestation boundary — the crossing between horizons A and B is specified as the **Core-Impact Threshold** (AMO-D079): manifestation damage affects the current body first and reaches persistent state only when its biological consequences are deep enough. Substance unchanged.

## AMO-D075 — All damage recovers while alive; only death is terminal

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Harm and maturity brief
- **Decision:** **If the biological individual survives, all forms of biological damage are ultimately recoverable.** Harm classes differ in severity, depth, cost, recovery duration, how many life cycles are needed, how much favourable growth is required, and what capability is lost meanwhile — never in *recoverable versus permanent*. **Death is the only normal permanently terminal biological outcome**; it is not dormancy, senescence, a phase transition, or severe stress by itself. A dead individual does not recover, and no routine resurrection exists.
- **Rationale:** Irreversible injury to a persistent individual a player may have cultivated for years turns a bad season into a permanent grievance, and the architecture already produces consequences severe enough without it — lost seasons, developmental regression, lost Bloom eligibility, multi-cycle recovery. Seriousness comes from **recovery depth and duration**, not from loss that never heals.
- **Consequences:** This **withdraws** the project's earlier working assumption that some harm might be permanent, and the wording in earlier documents has been corrected accordingly. Core damage remains among the most serious setbacks available; it may persist through dormancy and into a new emergence, close astral entry, and require long-term establishment across multiple cycles (AMO-D054). Death **does not erase history**: provenance, lineage, offspring and world history all remain (AMO-D011); no memorial system is designed. The exact death condition is open (AMO-Q104), as is treatment (AMO-Q105). Recorded as L46.

## AMO-D076 — Vitality is stored persistent state; no second core variable

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Harm and maturity brief · **Supersedes the caveat in** AMO-D056
- **Decision:** **Vitality** is the current long-horizon biological integrity and viability of the persistent individual, and it is **stored persistent state**, not derived. It is distinct from phase integrity, stress load, reserves, developmental maturity, size, age and genotype. No second stored variable such as `Core Integrity` is added: **core damage** is the causal event, **vitality** is the persistent state outcome.
- **Rationale:** AMO-D056 kept vitality on the reasoning that a derived summary could not carry irreversible damage. That reasoning is withdrawn with AMO-D075 — but the conclusion holds for a better reason. Two individuals may have identical stress and identical reserves and still differ in remaining core compromise, recovery need and proximity to losing inhabitability. **No function of stress and reserves can distinguish them**, because both have already recovered. The argument no longer depends on permanence at all. A separate core-integrity meter would move in lockstep with vitality and is the redundancy the condition model already rejects.
- **Consequences:** **Dormancy does not reset vitality** — life-cycle transition never erases persistent condition, and a compromised individual may stay compromised straight through dormancy into the next emergence. Whether dormancy ever *assists* recovery is open (AMO-Q102). Severe vitality reduction may make an individual alive but not inhabitable, with access returning as vitality recovers (AMO-D050, AMO-Q042). **Playable recovery precedes full restoration**: astral access may return long before former size and maturity do, which keeps a severe setback from becoming indefinite exclusion from play. Resolves the open caveat in AMO-D056 and the stored-state half of AMO-Q073.

## AMO-D077 — Developmental Maturity is a separate persistent dimension

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Harm and maturity brief
- **Decision:** **Developmental Maturity** — how far an individual has developed across repeated life cycles — is a persistent dimension distinct from life-cycle state, current condition and vitality. It **can grow** through sustained favourable conditions across successful cycles, and it **can regress** after severe stress, premature retreat, major core damage or extreme reserve loss. The name is a working one.
- **Rationale:** The three existing axes cannot express it. Life-cycle state says which phase is happening, vitality says how intact the individual is, condition says how it is doing right now — none of them says how large and developed it has become over years. Without it, repeated successful cultivation would have nothing to accumulate into, and a failed season would have nothing meaningful to cost.
- **Consequences:** **It is not experience points.** Maturity is biological development emerging from successful life cycles, favourable growth and condition — not a combat currency earned by activity. It gives premature retreat its real price: the individual survives while losing substantial progress, and the next manifestation may begin smaller, less capable and further from flowering (AMO-Q087). Regression is meaningful **without being permanent** — maturity can be rebuilt (AMO-D075). Representation, growth and regression rules are all open (AMO-Q106).
- **Revised:** 2026-09-21, manifestation boundary — maturity does **not** regress merely because a manifestation is damaged; regression requires crossing the Core-Impact Threshold (AMO-D079). Substance unchanged.
- **Revised:** 2026-09-21, maturity v0 — specified as one continuous, species-relative axis, with growth, regression and rebuilding rules (AMO-D080–AMO-D083). Substance unchanged.

## AMO-D078 — Bloom requires species-specific flowering maturity

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Harm and maturity brief
- **Decision:** A biologically healthy individual is **not automatically Bloom-capable**. Bloom requires developmental maturity at or above a **species-specific flowering-maturity threshold**. Reaching it **enables** Bloom; it does not guarantee it — actual Bloom may further depend on condition, reserves, life-cycle routing, environment and species biology. Eligibility can be **lost** if maturity regresses below the threshold and **regained** when it is rebuilt. **First Bloom is not maximum Bloom**: maturity continues growing beyond the minimum, Bloom is **repeatable** in later cycles where species biology permits, and later Bloom manifestations may be larger and more developed.
- **Rationale:** *Bloom is reached through biological maturity, not unlocked by player points.* It is a central product distinction: the player creates the conditions, and the living individual reaches the state. It also gives long-term successful cultivation its largest reward, and makes a setback that delays or shrinks a future Bloom a genuine loss even though nothing is permanent.
- **Consequences:** **No threshold is defined, researched or assumed**, and no universal threshold exists — species may differ in flowering requirements, developmental scale and tendency (AMO-D024). If the game later needs those facts they arrive as approved input once the consuming model exists; **nothing is added to the species CSV** (AMO-D025, AMO-D053, AMO-Q076). Roughly annual recurrence is possible where future data supports it but is **not** assumed universal, and no interval is defined (AMO-Q107). Bloom manifestation scaling is not defined and linear scaling is not assumed (AMO-Q088). Everything else about Bloom is unchanged — short, exceptional, highly discoverable, reproductively significant, never "Leaf with better stats" (AMO-D059, AMO-D071).
- **Revised:** 2026-09-21, maturity v0 — the flowering threshold is now explicitly a **milestone on the Developmental Maturity axis**, not a separate quantity, and maturity is species-relative so a threshold is only meaningful through the species profile (AMO-D080). Substance unchanged. Bloom manifestation damage is temporary, exactly parallel to the leaf (AMO-D074). Recorded as L47.

## AMO-D079 — Manifestation damage reaches the core only past a threshold

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Manifestation boundary brief
- **Decision:** Temporary manifestation damage **affects the current manifestation first**. It propagates into persistent state — reserves, developmental maturity, vitality, premature senescence — only once its biological consequences become deep enough. That boundary is the **Core-Impact Threshold**: a conceptual boundary, deliberately not a number.
  - **Below it:** the leaf or bloom stays damaged and the inhabited Amorpho may be substantially impaired, yet the manifestation may still complete its active period, persistent growth continues broadly unaffected, **developmental maturity need not regress**, and the next manifestation emerges structurally whole.
  - **Above it:** persistent consequences begin — reserve depletion, inadequate growth, maturity regression, premature senescence, a reduced next cycle, vitality compromise — all still recoverable while the individual lives (AMO-D075).
- **Rationale:** Without this boundary, AMO-D074's horizons touch but never say *when* one becomes the other, and the natural default would be that any structural damage bleeds straight into persistent state. That would make every torn leaf cost years of development, and it would collapse the graded outcomes the harm model exists to produce. It also protects the design directly before developmental maturity is specified: `leaf integrity loss` and `maturity loss` are different events (AMO-Q106).
- **Consequences:** **A difficult season can impair the current fighter without costing long-term biological progress**, and a damaged fighter this season may return fully functional next season having lost nothing durable. Leaf damage therefore does not automatically imply premature retreat, maturity loss, core damage or a failed season. **Visible damage does not determine the crossing by itself** — condition, reserves, Environmental Fit, developmental context, duration of impairment and eventual species biology all bear on it, so a proportion of structure lost is never a biological verdict (AMO-Q108). The same boundary applies to **Bloom**: a damaged Bloom may lose its capabilities and its reproductive opportunity without reducing maturity or vitality, so losing a Bloom is not losing the eligibility to bloom again (AMO-D078). How phase integrity alters a playable Amorpho's capabilities is a **combat-design question deliberately left downstream** (AMO-Q109, AMO-Q026). No threshold, mapping or formula is defined.
- **Revised:** 2026-09-21, biology-magic boundary — the persistent side is now called the **Tuber**, and what crosses into it is **Pathological Tuber Impact** as distinct from Programmed Tuber Draw (AMO-D087). Substance unchanged; the threshold remains AMO-Q108.
- **Revised:** 2026-09-22, pathological impact — the **Core-Impact Threshold remains conceptual shorthand and was never a number**; crossing may result from direct severe exposure, cumulative deficit, repeated insufficient recovery, developmental context or timing, and is judged by whether persistent loss actually occurred. Reserve depletion, missed growth and premature senescence alone do not prove the crossing (AMO-D090–AMO-D092). Substance unchanged.

## AMO-D080 — Developmental Maturity v0: one slow, species-relative axis

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Maturity v0 brief
- **Decision:** **Developmental Maturity** is the individual's accumulated long-term biological development of its persistent organism across life cycles. It is represented as **one persistent, conceptually continuous developmental quantity per individual** — no numeric range, no levels, no stages. It persists across leaf replacement, bloom ending, senescence, dormancy, new emergence and astral entry and exit, and it is **species-relative**: a maturity value has biological meaning only interpreted through the species, never compared directly across species.
- **Rationale:** No existing axis can express that two individuals of the same species may both be healthy, unstressed and in the same phase while one has developed vastly further. Continuity is what lets a good season be worth a little, a setback be worth a little or a great deal, a species threshold sit anywhere on the axis, and manifestation scale vary smoothly rather than in tiers.
- **Consequences:** Maturity is **not** life-cycle state, vitality, stress load, reserves, age or experience. *Age may correlate with maturity; it never defines it*, and chronological age is not a substitute. **It is not XP** — it never increases because a fight was won, a quest completed or points spent (AMO-D077, L47). It is also **not equated with any single physical measure** — height, span, diameter or mass may later be *derived* per species, which is what stops one universal physical metric from failing across very different species. The species development profile interprets it into manifestation scale, Bloom eligibility and Bloom scale; no schema is defined and the species CSV is untouched (AMO-D053, AMO-Q076, AMO-Q110). Internal representation, rates and presentation remain open (AMO-Q106, AMO-Q111). Gives AMO-D077 its v0 content.

## AMO-D081 — Maturity grows from persistent biological surplus

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Maturity v0 brief
- **Decision:** Maturity increases when the individual achieves **persistent net biological growth** — plausibly from favourable Environmental Fit, adequate reserves, healthy active phases and productive cycles. **Environmental Fit never awards maturity directly.** The chain is `Fit → biological opportunity → condition, reserves and growth processes → persistent development → maturity`. Growth need not wait for season boundaries; maturity may accrue during a healthy active phase.
- **Rationale:** *Positive biological surplus may become persistent development.* The wrong shape — `excellent Fit → +5 maturity` — would turn Fit into an experience dispenser and break the ownership boundary the entire environmental model rests on (AMO-D035–AMO-D037). Keeping development a *conversion* of sustained biological success preserves it.
- **Consequences:** **Reserves are a plausible bridge** between favourable conditions and persistent development, but nothing defines `spend X reserves → gain Y maturity`; the rule is only that persistent development requires biological capacity. No formula, rate, magnitude or update frequency is defined (AMO-Q106, AMO-Q074). Because development is biological rather than attention-driven, a rooted, uninhabited, even unbound individual keeps developing (AMO-D009, AMO-D064).

## AMO-D082 — Regression requires persistent loss; lost opportunity is not regression

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Maturity v0 brief
- **Decision:** Maturity regresses **only** when the persistent individual loses meaningful long-term biological development — which requires **Core Impact**, not temporary manifestation impairment (AMO-D079). Severity is continuous, from negligible to catastrophic collapse. **Lost opportunity is distinct from regression**: a season in which expected growth simply did not happen leaves maturity approximately unchanged, and is costly through the growth that never occurred plus spent reserves and accumulated stress.
- **Rationale:** Treating every bad season as regression would make the model punitive and would erase the difference between a disappointment and a disaster. A regression rule that reads proportionally off a damaged-structure percentage is wrong by construction: it would make every torn leaf cost years of development.
- **Consequences:** Below the Core-Impact Threshold a leaf or bloom may be visibly damaged and the inhabited Amorpho substantially impaired while maturity does not regress and may still increase (AMO-D079). **Premature retreat does not automatically regress maturity** — some retreats merely stop growth and cost reserves (AMO-Q087). Regression is a biological event, never punishment points, a debuff duration or reduced player progress. This decision deliberately treats **"Core Impact occurred" as an abstract trigger**; *when* harm crosses that boundary belongs to AMO-Q108 and is not settled here.

## AMO-D083 — Healing and regrowth are separate processes

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Maturity v0 brief
- **Decision:** Vitality recovery does **not** restore lost maturity. An individual may recover to full vitality while remaining developmentally far smaller than it was, and must rebuild maturity through successful growth, favourable long-term conditions and biological redevelopment — which may take far longer than stress recovery. Lost maturity is nonetheless **fully rebuildable while the individual lives**: no former developmental level is permanently out of reach.
- **Rationale:** *Healing restores integrity; growth restores development.* Vitality answers *is this organism sound?* and maturity answers *how far has it developed?* — so an individual can be severely damaged yet still large, or biologically recovered yet developmentally reduced. Collapsing them into one number would make a catastrophe either trivially undone by healing or permanently disfiguring, and the model wants neither.
- **Consequences:** Maturity never returns because a timer expired. A severely regressed individual may eventually rebuild, regain its former flowering maturity and exceed its previous development — the cost is time and successful biological life, which is exactly what strategic establishment provides (AMO-D054, AMO-D075). In the fragment case, **if** identity continuity is later accepted, maturity may collapse enormously while the individual lives; if the fragment is ruled a new individual it begins its own developmental history instead. Identity stays unresolved (AMO-Q094). Recorded as L48.

## AMO-D084 — Magic runs the fighter; biology is suspended during embodiment

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Biology-magic boundary brief
- **Decision:** Once astrally inhabited, an Amorpho operates as a **magical gameplay manifestation** with its own movement, combat state, capabilities and environmental tolerances. The biological individual provides the **starting template** — which manifestation is available (Leaf or Bloom), its phase-specific structural condition, its capability ceiling, which phase-specific abilities exist. From entry, that individual's **normal biological simulation is suspended**: no growth, no productive development, no maturity gain, no reproduction, no life-cycle progression, no Programmed Tuber Draw, no biological recovery. **Astral embodiment does not consume ordinary biological resources** — combat duration, distance travelled, ordinary attacks and time embodied do not by default draw down Tuber mass or reserves.
- **Rationale:** *Magic suspends biology; it does not consume it.* If fighting ate Tuber mass, every fight would be a developmental setback, the harm model's carefully separated horizons would collapse (AMO-D074), and players would be punished biologically for playing the game. Suspension also keeps both systems individually understandable, which is what the whole two-layer concept depends on.
- **Consequences:** Magical state — combat durability, stamina, status effects, phase-specific skills, combat resources, **Astral Readiness** — is its own stack and is **not** a view of leaf integrity, Tuber vitality, reserves, stress load or developmental maturity. The full stack is not designed (AMO-Q109, AMO-Q112). Biology resumes on rooting (AMO-D072). Recorded as L49.

## AMO-D085 — Embodiment is open-ended; the Human trance is metabolically stable

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Biology-magic boundary brief
- **Decision:** **Astral embodiment has no intrinsic maximum duration.** No universal *Astral Time Remaining* exists and none may be added; a player may remain embodied for hours, days or far longer. The limiter is **opportunity cost**. Correspondingly, the human body enters a deep trance with suspended metabolism: ordinary hunger, thirst and degeneration must not create a hidden embodiment timer, and normal aging during trance must not meaningfully force a return.
- **Rationale:** An arbitrary clock would be a constant where the design already has a better limiter: suspended biology on the inhabited individual, a Human unavailable for everything only humans can do, other Amorphos still living and changing, and a world that continues (AMO-D009). That cost scales with how much a player has to lose, which a constant cannot. And a metabolic timer would simply be the arbitrary clock wearing a biological disguise.
- **Consequences:** The unattended human body remains physically present and **may still be threatened** by hostile actors or world events (AMO-D029, AMO-Q041) — but **threat and metabolism stay separate**: a reason to return must be something that happened, not a bar quietly emptying. Long embodiment also means the player cannot physically move Anchors, which is a real strategic cost (AMO-D062).

## AMO-D086 — Astral Readiness: magical state restored by rooted biological life

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Biology-magic boundary brief
- **Decision:** **Astral Readiness** is a persistent magical state of an anchored individual: how ready it is to sustain effective magical embodiment. It belongs to the magical access layer and is **not** vitality, stress load, reserves, developmental maturity, leaf integrity or bloom integrity. **Astral exit does not reset it** — leaving an exhausted Amorpho and immediately re-entering leaves it exhausted. Fighting and magical exertion may deplete it. It is fundamentally restored by **returning the individual to rooted biological life**, and recovery may be substantially **time-compressed** relative to biological growth. A successful **Deep Dormancy** period restores it to full before the next active window, while dormancy itself stays uninhabitable.
- **Rationale:** *Leaving does not heal; living does.* An `exit → restore → re-enter` loop would erase every cost the magical layer has, so closing it is the point. Making rooted life the recovery path gives rooting a major purpose beyond stopping, and ties the magical loop directly to Environmental Fit and strategic establishment (AMO-D054). Time compression is a deliberate Fun First abstraction: biological reality legitimises the mechanism without dictating the pace (L1).
- **Consequences:** **Not every rooting site recharges well** — excellent Fit supports strong recovery, poor Fit slow or ineffective recovery, while pathological biological consequences may develop separately (AMO-Q108). **Bloom recovery has a biological price**: rooting a Bloom regenerates readiness while resuming its Programmed Tuber Draw, so repeated re-entry is limited **biologically rather than by a charge counter** (AMO-D087). Embodiment pauses that draw, so a very long Bloom embodiment is allowed and **no artificial Bloom timer may be added**. Future **magical healing** may restore combat state but must never restore leaf structure, Tuber vitality, maturity or biological reserves (L48). Representation, depletion, recovery rates, KO behaviour and how far magical healing reaches readiness are all open (AMO-Q112, AMO-Q113, AMO-Q114). Recorded as L50.

## AMO-D087 — Tuber is canonical; Programmed Draw is not Pathological Impact

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Biology-magic boundary brief
- **Decision:** **Tuber** is the canonical term for the persistent underground storage and core structure; *core* remains descriptive, and architecture wording prefers Tuber development, Tuber recovery, Tuber impact and Tuber draw. Two kinds of expenditure are distinguished: **Programmed Tuber Draw**, normal biological spending for a legitimate process — **Bloom** being the primary example — and **Pathological Tuber Impact**, harmful persistent loss from adverse circumstances. **Programmed Draw is not injury.**
- **Rationale:** Without the split, flowering would read as self-harm, and any system reacting to "Tuber resources went down" would treat a plant doing exactly what it is supposed to do as a plant in trouble. Both recover while the individual lives (AMO-D075); they differ in whether development was *spent* or *lost*.
- **Consequences:** *Leaf rebuilds; Bloom spends.* The leaf phase is the primary constructive opportunity — healthy leaf, good Fit and time support productive activity, reserves and Tuber growth (AMO-D081) — so an individual that blooms every possible cycle without good leaf seasons is spending a balance it is not replenishing. Earlier decisions written in terms of "core" are **not rewritten**; ledger history stays readable and affected entries carry *Revised* notes (AMO-D074, AMO-D079). No amounts, thresholds or species values are defined. **Pathological Tuber Impact thresholds are not settled here** and remain AMO-Q108.

## AMO-D088 — Astral Signal is distinct from inhabitability; dormancy silences it

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Biology-magic boundary brief
- **Decision:** **Astral Signal** — is this anchored individual currently *detectable* by its Warden — is independent of **Astral Inhabitability** — can the Warden *enter* it now. An Anchor may remain physically attached throughout the life cycle and guarantees **neither** an active signal, **nor** location information, **nor** entry: *the Anchor is a bridge, not a tracker.* The signal **fades progressively through Senescence**, may persist faintly in Early Dormancy, is **absent in Deep Dormancy — Astral Silence** — and **returns in Pre-Emergence, potentially before inhabitability does**.
- **Rationale:** The senescence fade turns dormancy from a surprise lockout into something a player can plan around — retrieve the individual, reallocate its Anchor, or knowingly accept losing track of it. Silence then makes physical location knowledge genuinely matter, which is the kind of consequence the world otherwise lacks.
- **Consequences:** **An Amorpho can become genuinely lost.** If an outdoor dormant Tuber's location is unknown, the Warden may be unable to find it, and **the world provides no quest marker** because someone once anchored it. **Last known location is historic player knowledge, not a live signal**: if the plant is physically moved during Astral Silence, the Warden does not automatically know. This creates real emergent risk — a silent dormant individual may be found, dug up, moved and its Anchor possessed — and a matching recovery, where a returning Pre-Emergence signal reveals the Amorpho somewhere unexpected. Whether a found Anchor can be used, rebound or broken from its Warden is **explicitly unresolved** (AMO-Q091). Distinct from AMO-D060, which concerns *other people* discovering a dormant tuber; this concerns the owner's own connection going quiet. Signal strength may affect location fidelity; no ranges or interface are defined (AMO-Q092, AMO-Q115).

## AMO-D089 — Tuber gameplay deferred; Leaf and Bloom are the playable forms

- **Status:** ACCEPTED · **Date:** 2026-09-21 · **Origin:** Biology-magic boundary brief
- **Decision:** For v0 the astrally playable forms are **Leaf** and **Bloom**. Deep Dormant Tuber is not inhabitable and there is no Tuber fighter gameplay. Transitional tuber or pre-emergence gameplay remains a future possibility and is not developed now.
- **Rationale:** Deliberate scope discipline. Two well-understood playable forms are enough to build and test the whole biology-to-fighter loop, and a third would multiply the open questions before either of the first two exists.
- **Consequences:** Dormancy loses **no** importance: transport, relocation, trade, repotting, digging, safe seasonal handling, Anchor management and strategic placement all happen in the Human layer while an individual is dormant (AMO-D062, L23). Transitional states also matter without any fighting in them, because that is where the **astral signal** changes (AMO-D088). If transitional tuber gameplay is ever added it belongs to the access windows, never to deep dormancy (AMO-D060, AMO-Q086).

## AMO-D090 — Pathological Tuber Impact: direct and indirect, acute and cumulative

- **Status:** ACCEPTED · **Date:** 2026-09-22 · **Origin:** Pathological impact brief
- **Decision:** **Pathological Tuber Impact** is harmful biological consequence that reaches the persistent Tuber as actual loss of integrity or accumulated development, with possible effects on stored capacity and future potential. It reaches the Tuber by two pathways:
  - **Direct** — the Tuber itself is exposed to harmful conditions or physical compromise, which may occur **whether or not a leaf is present** and bypasses productivity entirely;
  - **Indirect** — insufficient work by the active manifestation eventually causes actual persistent loss; reduced productivity or missed growth alone does not qualify.

  Both may be **acute** (a single severe event) or **cumulative** (persistent poor Fit, insufficient productivity, repeated incomplete recovery, prolonged unsuitable unrooted conditions).
- **Rationale:** The two routes behave differently and must not be merged: direct harm need not spend reserves first, and insufficient productivity need not directly compromise Tuber tissue. Allowing cumulative routes matters because otherwise a slow grinding deficit would be free, which is the wrong answer — *a slow grinding biological deficit may become serious without any single catastrophic moment.*
- **Consequences:** It stays distinct from leaf integrity loss, bloom integrity loss, stress load, temporary reserve use, lost growth opportunity and **Programmed Tuber Draw** (AMO-D087). No harm mechanisms, thresholds, tolerances, event lists or durations are defined (AMO-D024, AMO-Q117). Resolves the conceptual half of AMO-Q108.

## AMO-D091 — Persistent consequence follows function and opportunity, not appearance

- **Status:** ACCEPTED · **Date:** 2026-09-22 · **Origin:** Pathological impact brief
- **Decision:** **No percentage of visible structure lost may directly determine persistent Tuber loss** — no fixed mapping from Leaf damage to whether or how much persistent loss occurs. Visible structural damage is one input among several. Persistent outcome depends on **Leaf Functional Capacity** (how much useful biological work the current manifestation can still perform, which is *not* identical to leaf integrity), **Remaining Productive Opportunity** (how much useful active-phase opportunity remains before the manifestation naturally ends), Environmental Fit, current condition and reserves. Both terms are working terminology.
- **Rationale:** *Leaf damage is judged by lost function and lost opportunity, not by appearance alone.* The same visible damage early and late in an active phase can produce opposite persistent outcomes. Early damage may be compensated while opportunity remains, or prolonged lost function may accumulate; late damage may follow enough successful work, or leave too little time to recover earlier deficits. A percentage rule cannot express these cases.
- **Consequences:** **Gameplay impairment and persistent biological loss are separate questions** — a fighter may be badly impaired for a season while the plant finishes the year in good shape. **Environment after the damage participates**: a damaged leaf in excellent conditions may still do meaningful work. **Compensation is possible but not guaranteed**, and is not a catch-up bonus; the reverse does not hold, because good late conditions cannot recreate productive time already gone. Remaining Productive Opportunity is **biological opportunity, not a UI countdown**, and must not be modelled as a visible timer. No formula is defined (AMO-Q116). Recorded as L51.

## AMO-D092 — Pathology is actual persistent loss, not depletion or lost growth

- **Status:** ACCEPTED · **Date:** 2026-09-22 · **Origin:** Pathological impact brief
- **Decision:** **Pathological Tuber Impact has occurred when the persistent Tuber has actually lost biological integrity or accumulated development because of harmful circumstances.** Its persistent outputs are **vitality reduction**, **developmental maturity regression**, or both, in no fixed proportion. Not qualifying on their own: **reserve consumption** (a buffer being used for its purpose), **stress load** (however high — it recovers), and **lost expected growth** (*lost opportunity is not regression*). Apart from normal Programmed Tuber Draw, a productive phase may leave the individual gaining, approximately maintaining, or suffering actual persistent loss; only that harmful loss is pathology.
- **Rationale:** An outcome-based diagnostic settles ambiguous cases without accounting math. A named *Tuber Balance* concept was evaluated and **deliberately not adopted**: a blooming individual's balance is negative **by design**, so `balance negative → pathology` is wrong and the term invites exactly that inference; qualifying it as *balance net of Programmed Draw* becomes the arithmetic the concept was meant to avoid. The useful distinction survives as qualitative productive-phase outcomes, without treating Bloom's expected spending as harm.
- **Consequences:** **Severity is continuous** once the boundary is crossed — tiny regression through near-total developmental collapse — and all of it recovers while the individual lives (AMO-D075). **Current condition modifies susceptibility**, so an already compromised individual crosses sooner; no function is defined (AMO-Q118). **Reserves buffer but are not a shield meter**, and direct severe harm may bypass depletion entirely. **Premature senescence may be protective** — abandoning a failing manifestation can be the reason pathology did *not* occur, so it never implies that it did (AMO-Q087). **Dormancy does not automatically restore vitality or maturity**; that Deep Dormancy fully restores Astral Readiness is magical state and must not be read as biological recovery (AMO-D086). Failed productivity tends to cost development while direct harm tends to compromise integrity — a tendency, never a mapping.

## AMO-D093 — Excavated Tubers remain biologically simulated

- **Status:** ACCEPTED · **Date:** 2026-09-22 · **Origin:** Pathological impact brief
- **Decision:** Being unrooted is **not automatically harmful**, and it is **not stasis**: *a biological Tuber does not become timeless because a Human is carrying it.* An excavated Tuber remains a biological individual whose local environment continues to matter, and prolonged unsuitable conditions may eventually cause actual persistent loss. An individual ready to emerge or actively transitioning may be harmed if excavated and its biological demands continue unmet.
- **Rationale:** Treating a dug-up plant as an inventory icon outside world simulation would quietly exempt the most physically dangerous thing a player routinely does to an individual, and would contradict the world persisting independently of attention (AMO-D009).
- **Consequences:** Creates real Human-layer responsibility — excavating at appropriate times, providing appropriate transport conditions, replanting, choosing suitable locations, avoiding prolonged unsuitable exposure — with **no logistics interface, transport equipment, storage mechanics, timings or tolerances defined** (L23, AMO-D062, AMO-Q117). Abstraction and time compression for transported individuals remain open (AMO-Q074).

## AMO-D094 — Mature Leaf recovery preserves; replacement is a new manifestation

- **Status:** ACCEPTED · **Date:** 2026-09-22 · **Origin:** Same-phase Leaf recovery brief, owner-supplied biological input
- **Decision:** Once a Leaf has fully emerged and expanded, same-phase recovery may stabilize damaged structure and restore useful function, but **missing mature architecture does not regrow into a pristine original Leaf**. If the current Leaf cannot adequately continue, the persistent Tuber may instead initiate **replacement emergence**: a distinct new Leaf manifestation of the same individual. Replacement is possible, never guaranteed, and does not restore elapsed productive opportunity or reset persistent biological history.
- **Rationale:** Treating recovery as generic regeneration erases manifestation damage. Treating a replacement as repair of the old Leaf erases the distinction between one persistent individual and its temporary structures. A scarred but useful Leaf and a structurally fresh replacement with inherited biological history must both be expressible (AMO-D058, AMO-D074, AMO-D091).
- **Consequences:** Stabilization, compensation and functional improvement need not restore visual structure. Replacement spends biological resources and time; it may be reduced in scale without a size rule, while the old Leaf declines or is abandoned. This does not promise a replacement in every species or circumstance. AMO-D075's eventual recovery of a **living individual** does not require its **current mature Leaf** to regrow. AMO-Q103 keeps same-Leaf recovery mechanics; AMO-Q084 owns replacement lifecycle routing and species scope, AMO-Q101 its triggers, and AMO-Q085/AMO-Q115 its unresolved astral access and signal. No threshold, cost, duration, overlap or magical transfer rule is set ([24_SAME_PHASE_LEAF_RECOVERY_V0.md](24_SAME_PHASE_LEAF_RECOVERY_V0.md)).

## AMO-D095 — The persistent Tuber funds temporary manifestations

- **Status:** ACCEPTED · **Date:** 2026-09-22 · **Origin:** Tuber-funded routing brief
- **Decision:** The **Tuber is the primary persistent biological body of the individual**. It funds the emergence and establishment of temporary Leaf and Bloom manifestations from its current biological capacity. A Leaf can later contribute productive biological work toward the Tuber's future condition and development. The current Tuber state constrains the biological scale and capability of what it can produce or sustain.
- **Rationale:** A manifestation cannot be treated as the primary individual or as a free seasonal body independent of the persistent organism. The Tuber-to-Leaf investment and Leaf-to-Tuber productive return are distinct directions, not a single balance score.
- **Consequences:** Identity, inherited traits, lineage, condition, reserves, Developmental Maturity and persistent history stay with the Tuber-based individual across manifestations (AMO-D058, AMO-D080, AMO-D087). A stronger individual may support a more substantial Leaf, but manifestation size never maps directly to combat power (L5, AMO-Q109). Representation, species interpretation and accounting remain open (AMO-Q106, AMO-Q110, AMO-Q116). No new universal capacity variable is created ([25_TUBER_FUNDED_MANIFESTATION_AND_REPLACEMENT_ROUTING_V0.md](25_TUBER_FUNDED_MANIFESTATION_AND_REPLACEMENT_ROUTING_V0.md)).

## AMO-D096 — Replacement is capacity-limited intra-cycle salvage

- **Status:** ACCEPTED · **Date:** 2026-09-22 · **Origin:** Tuber-funded routing brief
- **Decision:** Repeated visible microdamage remains with the **current mature Leaf** while useful function and viability remain. When that Leaf can no longer adequately fulfill its biological role for the remaining active period, a **functional-collapse routing point** opens. Replacement Emergence may then salvage future opportunity **only if the Tuber can fund it**. It costs persistent biological capacity and emergence time, does not recover elapsed opportunity, and is not automatically chosen or endlessly repeatable. It is normal biological investment, not Pathological Tuber Impact by mere expenditure.
- **Rationale:** Scar count is not function, and a free replacement would erase damage. A costly replacement late in an active period can be a poor strategy even when biologically possible; an inadequate Tuber may be unable to replace at all (AMO-D091, AMO-D092, AMO-D094).
- **Consequences:** The smallest conceptual topology reuses **Emergence** in a replacement context: `Active Leaf → Emergence (replacement) → Active Leaf`, within the same broader active period and without dormancy or individual reset. The alternative early retreat enters ordinary **Senescence** (AMO-D070). Replacement is generally expected to be reduced relative to the primary Leaf, a game-system direction awaiting species scope and size derivation (AMO-Q084, AMO-Q110), with no ratio or cost specified. The old/new Leaf overlap, exact eligibility, repeated-replacement possibility and astral windows remain open (AMO-Q084, AMO-Q101, AMO-Q085). No combat mapping is decided ([25_TUBER_FUNDED_MANIFESTATION_AND_REPLACEMENT_ROUTING_V0.md](25_TUBER_FUNDED_MANIFESTATION_AND_REPLACEMENT_ROUTING_V0.md)).

## AMO-D097 — Biology bounds routing choices; unattended plants route autonomously

- **Status:** ACCEPTED · **Date:** 2026-09-22 · **Origin:** Tuber-funded routing brief
- **Decision:** At a Leaf routing point, **biological eligibility is evaluated before strategy**. Agency, where available, may influence selection only among biologically possible routes; ownership or Warden desire cannot create a replacement the Tuber cannot fund. When agency is absent, the Amorpho's biological life-cycle system must still select an available route autonomously as the persistent World advances, rather than pause for a player decision.
- **Rationale:** The World continues while the player is elsewhere or offline (AMO-D009, L7). Mandatory player input would make an unattended plant biologically timeless at exactly the moment its condition matters. Conversely, an unconstrained player command would make biological capacity meaningless.
- **Consequences:** Replacement eligibility is distinct from choosing replacement; a strong Tuber may conserve capacity through retreat, while a weak one may have no replacement option. AMO-Q101 owns biological eligibility and autonomous selection policy; AMO-Q119 owns when player agency is available, how a choice reaches the plant and what the player can know. Astral embodiment does not create biological capacity or advance replacement while normal biology is suspended (AMO-D084). No control interface, remote command, forecast or autonomous algorithm is chosen ([25_TUBER_FUNDED_MANIFESTATION_AND_REPLACEMENT_ROUTING_V0.md](25_TUBER_FUNDED_MANIFESTATION_AND_REPLACEMENT_ROUTING_V0.md)).
