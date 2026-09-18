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
