# Decision Ledger

This ledger records Amorpho's accepted product and architecture decisions. Its purpose is to make drift visible: if the project starts behaving differently from what is written here, either the work is wrong or a decision needs to be formally changed.

## How to use this ledger

- **IDs are permanent.** `AMO-D###` numbers are never reused or renumbered.
- **Never delete a decision.** To change a decision's substance, add a new decision and mark the old one `SUPERSEDED by AMO-D###`, with a short note on what changed and why. Anyone reading old documents, commits or data must still be able to understand what was true at the time.
- **Clarifications** that do not change a decision's substance (terminology, cross-references, filling in a detail the decision had left open) may be made in place, with a dated *Revised* note.
- **Statuses:** `ACCEPTED` (in force), `SUPERSEDED` (replaced; kept for history). Undecided matters do not belong here — they live in [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md). When an open question is resolved, record the outcome here and point the question to it.
- **Origin** says where a decision came from: *Founding brief* or *Foundation closure brief* (set by the project owner), or *Foundation session, derived* (a conservative consequence worked out while laying the foundation).
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

**Foundation closure (2026-09-18):** before the initial commit, the botanical input architecture was simplified. AMO-D016 and AMO-D023 were superseded; AMO-D024–AMO-D027 were added; AMO-D021 and AMO-D022 were confirmed. Terminology and cross-references in other entries were updated to match; entries whose wording changed beyond that carry a *Revised* note.

---

## AMO-D001 — Product name is Amorpho

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** The product, the repository and all product-facing material are named **Amorpho**. It is never called "TM Amorpho", "TM Amorpho Game", "Trederus Maximus Amorpho" or similar. Within the game, "an Amorpho" also names a plant awakened as a fighter.
- **Rationale:** Amorpho needs its own identity. Group affiliation is background, not branding.
- **Consequences:** Package names, headings, file names and documentation use "Amorpho". The Trederus Maximus affiliation appears only as one quiet sentence in an About section.

## AMO-D002 — Amorpho is an independent repository and system

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** Amorpho is self-contained. It has no code, build, data or service dependencies on any other system, including other Trederus Maximus projects such as Imperbio or TM Botanics.
- **Rationale:** The game must be able to exist, be built and be run entirely on its own, for as long as it lives.
- **Consequences:** Anything Amorpho needs, it owns. Knowledge from outside arrives only as approved input files through the Reality Gate (AMO-D017).

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

## AMO-D013 — Environmental suitability, not country locks

- **Status:** ACCEPTED · **Date:** 2026-09-18 · **Origin:** Founding brief
- **Decision:** Where a species can grow is determined by environmental suitability (for example temperature, seasonality, rainfall, moisture, dry season, light, drainage), not by political borders or native-country membership.
- **Rationale:** It allows meaningful movement of plants around the world and ties outcomes to understandable causes.
- **Consequences:** Locations carry environmental properties; species carry tolerance/suitability profiles. The exact variables and resolution are deliberately unspecified (AMO-Q005). Environmental facts enter approved input only after the environment model is designed (AMO-D025).

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
- **Decision:** The running game, its tools and its data never query, call or reference external knowledge systems (including Imperbio, TM Botanics or any other Trederus Maximus system), botanical websites or databases, external APIs or live data sources. Approved input files never name or identify their source.
- **Rationale:** Sources are relevant to the external research process, not to the game. Independence preserves Amorpho's ability to exist on its own.
- **Consequences:** No imports from external repositories, shared runtime packages, database links, callbacks, synchronisation jobs or environment variables pointing at research systems. Once an approved import is accepted, nothing in Amorpho needs continued access to the external master-data system.
- **Revised:** 2026-09-18, foundation closure — consequences restated for the file-based input; substance unchanged.

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
