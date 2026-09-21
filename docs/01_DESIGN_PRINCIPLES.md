# 01 — Design Principles

These are Amorpho's design laws. They are durable: work that breaks one of them is wrong unless the law is formally changed through a new entry in [DECISIONS.md](DECISIONS.md).

Each law has a short explanation and a **smell** — a sign that work is drifting away from it.

Laws are not the same as designs. A law says what must stay true; it does not say how a system is implemented. Most implementation questions are still open ([06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md)).

---

## Product laws

### L1 — Fun comes first.
When fun and realism conflict, fun wins. Realism is used where it creates interesting play and abstracted where it does not. *(AMO-D003)*
**Smell:** a mechanic that is accurate but tedious, justified only by "that is how it works in reality".

### L2 — Reality provides the cast; the game provides the fantasy.
Which species exist, and which of them can hybridize, comes from reality. Everything the plants *do* as Amorpho — moves, powers, personality — is the game's invention. *(AMO-D004, AMO-D006)*
**Smell:** a fantasy feature presented as a botanical fact, or a botanical fact overridden for convenience.

### L3 — Species come from reality; individuals and lineages come from the game world.
The species list is fixed by reality. The enormous diversity of the game comes from individuals, variation, lineages and approved hybrids. *(AMO-D004, AMO-D005, AMO-D012)*
**Smell:** a proposal to add a "new species" to give players more variety.

### L4 — Unknown means unknown.
Botanical facts that have not arrived as approved input through the Reality Gate do not exist for the game. This applies especially to species and hybrid compatibility, and equally to AI-generated "facts". A missing approval is not a negative fact: an unapproved pair is "not approved", not "incompatible". *(AMO-D017, AMO-D027)*
**Smell:** "it is probably compatible", "this species likely prefers…", or plausible-looking data that did not come from approved input.

### L5 — Botany grounds the game; it does not dictate mechanics.
A large real plant is not automatically a stronger fighter. A botanical trait is not automatically a combat mechanic. Real traits are inspiration. *(AMO-D006)*
**Smell:** combat numbers derived directly from real measurements.

### L6 — Entertainment is the product; learning is a side effect.
Amorpho never lectures. If players learn something about real plants, it is because the plants are real, not because the game is teaching. *(AMO-D003)*
**Smell:** text walls, quizzes, or mechanics that exist to convey information rather than to be played.

## World laws

### L7 — The world does not revolve around the player.
The world, its cities and its natural populations exist and develop independently of any player. Players are actors in the world and can change its history. *(AMO-D009)*
**Smell:** world content that only exists or changes when a player looks at it, in ways the player can notice.

### L8 — Nothing comes from nothing.
Every plant exists because of the initial world state or because of reproduction. Plants never spawn because someone needs one. *(AMO-D010)*
**Smell:** a quest reward, shop or event that creates plants from thin air.

### L9 — Suitability, not borders.
A species grows where the environment suits it, not where a map says it belongs. *(AMO-D013)*
**Smell:** logic of the form "species X is allowed in country Y".

### L10 — Every advantage has an exposure.
Protected cultivation is safer but constrained; exposed cultivation can be better but is riskier. No cultivation context is strictly best. *(AMO-D014)*
**Smell:** a location, building or item that removes all risk without a real cost.

### L11 — A flowering plant announces itself.
Flowering makes a plant easier for others to find. The most spectacular moment of a plant's life is also its most exposed. *(AMO-D015)*
**Smell:** a way to flower outdoors with no discoverability consequence.

## Plant laws

### L12 — Every plant is an individual.
Plants have persistent identity and history. Identity is never reused. *(AMO-D011, AMO-D022)*
**Smell:** plants modelled as stackable, interchangeable inventory items.

### L13 — Moving a plant changes its expression, not its genes.
Individuals acclimate. Genetic change happens across generations, through reproduction, variation and selection. *(AMO-D012)*
**Smell:** an individual's genotype being modified by relocation, care or combat.

### L14 — The simulation may know more than the player sees.
The world can track provenance, genetics and history in full, while the UI shows only what serves play. Knowing and showing are separate decisions. *(AMO-D011)*
**Smell:** simulation depth being cut because "the player would not see it", or UI clutter because "the data exists".

## Combat laws

### L15 — Skill is the core of combat.
Combat is real-time and skill-based. Practice must make a player significantly better with the same Amorpho. *(AMO-D008)*
**Smell:** a combat outcome that is decided mainly by stats, collection size or time spent cultivating.

### L16 — The plant you raised is the fighter you play.
An Amorpho is not a separate creature; it is a specific individual plant, temporarily awakened. *(AMO-D007)*
**Smell:** combat characters that exist independently of individual plants in the world.

## Project laws

### L17 — Amorpho stands alone.
No runtime, build or data dependency on any external system. Reality enters only through the one-way Reality Gate. *(AMO-D002, AMO-D017, AMO-D018)*
**Smell:** an API client, a live data feed, or a field naming an external system.

### L18 — Always moving, never rushed.
The project may grow slowly, but it never stops growing. *(AMO-D019)*
**Smell:** either a large speculative build-out, or a long pause waiting for "enough capacity".

### L19 — Build irreversible knowledge now; defer expensive production.
Decisions, verified data and validated experiments last. Art, content and infrastructure can wait until capacity catches up. *(AMO-D019)*
**Smell:** effort spent on production assets or infrastructure whose requirements are not yet known.

### L20 — Continue; do not restart.
Build on accepted decisions. Change them deliberately, through the decision ledger, instead of redesigning the foundation each session.
**Smell:** a new document or structure that silently duplicates or contradicts an existing one.

### L21 — Amorpho uses reality; it does not research it.
Botanical research happens outside this repository. Amorpho receives approved files and imports only what the game demonstrably needs. *(AMO-D024, AMO-D025)*
**Smell:** a column added "because the master list has it", stored citations or source comparisons, copied third-party text or images, or a script that fetches botanical data.

## Embodiment laws

### L22 — One consciousness, one inhabited body.
The player has one persistent human body and may own many plants, but inhabits exactly one body at a time. A collection creates options, logistics and strategic choices — never simultaneous direct control. *(AMO-D028)*
**Smell:** squad commands, remote orders, or uninhabited plants acting on the player's behalf.

### L23 — Human and plant are separate persistent bodies.
The human does not physically become a plant. During astral transfer the human body remains in the world, unattended, and the plant remains a persistent individual that is now animated. *(AMO-D029)*
**Smell:** "the human disappears and a fighter appears", or a design in which the human body has no location while an Amorpho is active.

### L24 — The plant and the Amorpho are one individual in two states.
Identity, provenance, lineage, ownership, history, genetics and variation belong to the individual and cross the state change with it. *(AMO-D030)*
**Smell:** a fighter object created alongside a plant object and reconciled afterwards.

### L25 — Astral entry requires biological stability.
`alive` and `inhabitable` are different. A plant can be alive and too stressed to inhabit. *(AMO-D031)*
**Smell:** a design that treats "not dead" as "available".

### L26 — Astral exit returns fantasy to biological reality.
Leaving an Amorpho returns the individual to rooted plant state, where its real relationship with its environment resumes. *(AMO-D032)*
**Smell:** an Amorpho that can be parked indefinitely in animated form, or a rooting act with no environmental consequence at all.

### L27 — Rooting is not inherently harmful; Environmental Fit determines the trajectory.
Rooting exposes an individual to its environment. The result may be deterioration, equilibrium, stability, recovery, growth or improvement. Rescue windows emerge from conditions; there is no universal timer. *(AMO-D033, AMO-D034)*
**Smell:** a countdown that starts when a plant roots, or any fixed survival constant.

## Simulation ownership laws

### L28 — The World owns environmental truth.
The World answers *what conditions exist here, now?* and nothing more. It does not know whether those conditions suit any particular individual. *(AMO-D035)*
**Smell:** `species X allowed here` inside World logic — the ownership form of L9.

### L29 — The Amorpho owns its own biology.
The individual answers *what do I need, prefer and tolerate?* It knows itself; it does not know countries. *(AMO-D036)*
**Smell:** `Thailand = good`, `Russia = bad`, or any place name inside the plant model.

### L30 — Environmental Fit is derived, never a third source of truth.
Fit evaluates the interaction of World and Amorpho. It stores no environment and no biology of its own, and it is not a synonym for stress. *(AMO-D037)*
**Smell:** a fit system that accumulates its own climate model, or one whose only output is damage.

### L31 — The Evolutionator owns inheritance, variation and generational change.
Trait transmission across reproduction belongs to its own domain, which needs no geography. Adaptation emerges from variation, differential success and inheritance. *(AMO-D038)*
**Smell:** `if region == … then grant tolerance`, or an evolution system reading place names.

### L32 — Acclimation is not evolution.
An individual may change within its lifetime; that is not genetic change. Populations shift only across generations. *(AMO-D012, AMO-D039)*
**Smell:** a plant becoming genetically adapted because it lived somewhere long enough.

### L33 — Selection is emergent, and comes from both the World and players.
Environmental and player-driven selection may act at once, producing distinctive lineages within a real species. There is no `EVOLVE` action that upgrades a species. *(AMO-D040)*
**Smell:** stage evolution, an experience bar that unlocks a better form, or a lineage promoted to a new species.

## Interface laws

### L34 — Standard and VR are first-class entrances to the same game.
Two interfaces, one persistent world, one character, one history, one progression. VR is optional, but never secondary, and Standard is never a fallback. *(AMO-D041, AMO-D042)*
**Smell:** "Amorpho VR" as a separate mode, world or save; or any core activity that requires one interface.

### L35 — Account for VR early; pay for VR production later.
Avoid flat-screen-only assumptions and express gameplay intent rather than one physical input — but build no VR production systems and commit to no VR hardware yet. *(AMO-D043)*
**Smell:** either a core rule written as `button X = action`, or VR hands and locomotion being built before the game exists.

## Further project laws

### L36 — Prove first; extract later.
Shared infrastructure is extracted from repeated real use, never designed in advance for projects that do not exist yet. *(AMO-D044)*
**Smell:** a shared framework created before two real consumers have proven the need.

### L37 — Prefer systems that generate situations over scripted special cases.
A small number of coherent rules should produce many meaningful situations. *(AMO-D028, AMO-D033, AMO-D040)*
**Smell:** an illustrative example turned into a hard-coded feature, or a scripted choice screen standing in for a simulated dilemma.

## Environmental laws

### L38 — Surviving is not thriving.
Absence of stress is not the best possible outcome. The model must distinguish not dying, stable survival, healthy growth and highly favourable development — and an excellent environment must be worth seeking, not merely a punishment avoided. *(AMO-D049, AMO-D033)*
**Smell:** a design whose best case is "nothing bad happened", or a fit score that only ever subtracts.

### L39 — Environment describes conditions, not permissions.
The World states what conditions exist; it never forbids a player from going somewhere or rooting there. Consequences emerge through Environmental Fit. *(AMO-D051)*
**Smell:** a travel, planting or rooting action blocked because a location is "unsuitable" — the agency form of L9's smell.

### L40 — Condition is how it is doing; development is what phase it is in.
They are separate axes of an individual's biological state. A seedling is not in worse condition than a mature plant, and a large plant is not in better condition for being large. *(AMO-D056, AMO-D057)*
**Smell:** a single score that rises with growth, or a model in which "more developed" reads as "healthier" — the same collapse L38 guards from the other side.

## Life-cycle and access laws

### L41 — The individual persists; the biological body changes.
A tuber, a leaf-form plant and a flowering individual can all be the same persistent individual. Identity, lineage and history belong to the individual, never to the current structure — so damage to a temporary manifestation and damage to the persistent core have different horizons. *(AMO-D058, AMO-D059)*
**Smell:** a phase modelled as a new entity, a lineage record that cannot survive a season, or leaf damage treated as permanent harm.

### L42 — The soul may travel; the Anchor must move by human hands.
Only the human can attach, remove or move an Astral Anchor. Changing which individuals are playable always costs human-world action. *(AMO-D062, AMO-D061)*
**Smell:** reassigning an Anchor from a menu, an Amorpho managing its own access, or Anchors behaving as invisible roster slots.

### L43 — Ownership is not availability.
Existence, ownership, custody, anchoring and astral availability are five separate axes that may disagree. Owning an individual does not make it playable; holding one does not make it yours. *(AMO-D063, AMO-D064, AMO-D065)*
**Smell:** a single `owner_id` standing in for all five, or a roster derived straight from the collection.

### L44 — Astral capacity belongs to the human; biological availability belongs to the Amorpho.
How many connections a player can sustain is a property of the human character. Whether a given individual can be entered is a property of that individual and its phase. Neither side may answer the other's question. *(AMO-D067, AMO-D069)*
**Smell:** human advancement that opens a dormant plant, or a plant's condition that changes how many others a player can hold open.

