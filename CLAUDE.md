# CLAUDE.md — Guidance for AI development agents

This file tells future Claude Code sessions (and any other development agent) how to work in this repository. Read it fully before changing anything. Then read [README.md](README.md), [docs/DECISIONS.md](docs/DECISIONS.md) and [docs/06_OPEN_QUESTIONS.md](docs/06_OPEN_QUESTIONS.md).

## What this repository is

**Amorpho** is a long-running game project: a persistent Earth-like world in which a human player collects, cultivates, propagates and trades individual plants of real *Amorphophallus* species, and can temporarily awaken one as an Amorpho for real-time, skill-based fighting.

**Maturity:** foundation plus the first systems pass. There is no game code, no engine, no programming language commitment and no species data. The approved species input is header only. The project is in Phase 1 — Systems Specification ([docs/07_INCUBATION_ROADMAP.md](docs/07_INCUBATION_ROADMAP.md)); the embodiment, simulation-domain and interface laws are settled (AMO-D028–AMO-D044), and the recommended next step is the environment and Environmental Fit model, version 0 (AMO-Q005).

## Non-negotiable rules

### Identity and independence
1. **The product name is Amorpho.** Never "TM Amorpho", "TM Amorpho Game", "Trederus Maximus Amorpho" or any prefixed variant — not in headings, package names, identifiers, file names or docs. The local checkout directory may carry a different name; do not propagate it. (AMO-D001)
2. **Keep the Trederus Maximus affiliation quiet.** It appears as one sentence in the README's About section. It is never a runtime or architecture concern.
3. **Amorpho is independent.** No runtime, build, code or data dependency on any other system — including Imperblio, TM Botanics, any other Trederus Maximus system, or any botanical website or database. No API clients, live data feeds, HTTP fetches, shared databases, shared runtime packages, callbacks, sync jobs, or environment variables pointing at research systems. (AMO-D002, AMO-D018)

### Reality and botany
4. **Amorpho does not research botany.** Detailed research about *Amorphophallus* happens outside this repository. Do not research taxonomy, browse botanical sources, or import botanical facts unless a task explicitly requires external investigation. Amorpho is not a botanical database, literature archive, evidence platform or mirror. (AMO-D024)
5. **Reality enters only as approved input.** Approved export files are supplied from outside the repository and accepted into `data/input/` through the Reality Gate — one way only. Amorpho trusts approved input; it does not adjudicate it or record where it came from. (AMO-D017, AMO-D026, [docs/05_REALITY_GATE.md](docs/05_REALITY_GATE.md))
6. **Import only what the game demonstrably needs.** Never mirror external master data. Never copy third-party prose, website text, photographs, illustrations, tables or database dumps. Add an input column only after the game system that needs it has been designed. (AMO-D025)
7. **Prefer simple CSV input while it is sufficient.** No schemas, APIs or interchange formats without demonstrated need. (AMO-D026)
8. **Never fabricate botanical facts.** If a fact did not arrive as approved input, it is unknown to Amorpho. This includes sizes, ranges, life cycles, climates, pollination and propagation behaviour.
9. **Never invent species** — not for roster size, variety, or examples presented as real. Real species define the base species set. (AMO-D004, AMO-D005)
10. **Species IDs are permanent; names are metadata.** Species are identified by opaque IDs of the form `AMO-SP-000001`, never derived from the name, never changed, never reused. Scientific names may change in later approved input; the ID stays. Never use a scientific name as a key. Never assign IDs yourself to real species. (AMO-D022)
11. **Hybrid compatibility is a symmetric, approved species pair.** `A + B` is approved or not approved; there is no direction. "Not approved" means no approved entry, not "proven incompatible". Never invent pairs. (AMO-D027)
12. **Keep the three data layers separate:** Approved Reality Input, Game Design Data, Persistent World State. Design data may reference species IDs but never adds species or pairs. (AMO-D021)

### The game
13. **Fun comes first.** Realism grounds the game; it never overrides fun, and fun never justifies fabricating facts. Amorpho is not educational software. (AMO-D003)
14. **Combat is skill-based, real-time fighting** with fighting-game rounds — not turn selection. Botany does not dictate combat mechanics. (AMO-D006, AMO-D008)
15. **The World is Earth.** A coherent representation of the real Earth — real continents, countries, regions and cities — shared by the Human and Amorpho layers. Never substitute a fictional map for a real region. Fidelity may grow progressively; this commits to no map technology, data source or streaming architecture, and authorises building none. (AMO-D045, [docs/02](docs/02_WORLD_MODEL.md))
16. **The individual persists; its body changes.** A tuber, a leaf-form plant and a flowering individual can be the same persistent individual. Structural damage to a temporary manifestation ends with it; actual persistent Tuber harm carries across phases in **vitality or developmental maturity**. **No harm is permanent while the individual lives** — classes differ in depth and recovery duration, never in recoverability; only death is terminal. **Bloom requires species-specific flowering maturity**, is repeatable, and is never unlocked with points. **Magic suspends biology; it does not consume it** — an inhabited Amorpho runs on magical state while its biology pauses, embodiment is open-ended, and **Astral Readiness** is restored by rooted life, never by leaving and re-entering. The **Anchor is a bridge, not a tracker**: Deep Dormancy silences the astral signal entirely. **Pathological Tuber Impact** is harmful persistent loss — direct or indirect, acute or cumulative — judged by whether loss actually occurred, never by a damage percentage; *Programmed Tuber Draw* (Bloom) is spending, not harm. **Developmental Maturity** is one continuous, species-relative axis of persistent development — not XP, not age, not condition; it grows from biological surplus and regresses only on Core Impact, and **healing does not restore it** (AMO-D080–AMO-D093, [docs/19](docs/19_DEVELOPMENTAL_MATURITY_V0.md), [docs/20](docs/20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md), [docs/21](docs/21_PATHOLOGICAL_TUBER_IMPACT_V0.md)). The topology is seven states in three families, with Bloom a **sibling active state** rather than a linear stage — and **rooted, astrally exited and dormant are three different things**. Availability follows biological state; there is no roster timer. (AMO-D058, AMO-D059, AMO-D070–AMO-D078, [docs/15](docs/15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md), [docs/17](docs/17_LIFE_CYCLE_STATE_MACHINE_V0.md), [docs/18](docs/18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md))
17. **Astral access has three gates, and only humans move Anchors.** Entry needs a physical **Astral Anchor**, an accessible life-cycle phase (deep dormancy closes the door) and a biologically inhabitable individual. Only the human player attaches, removes or moves an Anchor — never an Amorpho, never from a menu. Wild plants and every new individual begin **unbound**; ownership, custody, anchoring and availability are separate axes and never one field. (AMO-D060–AMO-D065)
18. **The human progresses separately, and slowly.** Human/Warden magical development is its own domain, much slower than biological change, and grind-resistant. Its only confirmed dimension is **Astral Capacity** — how many simultaneous astral connections the human can sustain, distinct from how many physical Anchors they hold. It never overrides dormancy, condition, missing Anchors or the human-hands rule, and does not make Amorphos stronger. No curve, value or timing rule is chosen. (AMO-D066–AMO-D069, [docs/16](docs/16_HUMAN_WARDEN_PROGRESSION_V0.md))
19. **One consciousness, one inhabited body.** Transformation is astral transfer: the player's consciousness leaves a persistent human body and inhabits **one** eligible individual at a time. The human body stays in the world; the plant and its animated form are one individual in two states. A collection is never an army. (AMO-D028, AMO-D029, AMO-D030, [docs/09](docs/09_EMBODIMENT_AND_ASTRAL_TRANSFER.md))
20. **Rooting is not a penalty.** It exposes the individual to Environmental Fit, whose outcomes range from death to genuine improvement. Never write a decline timer or a fixed rescue window. (AMO-D033, AMO-D034)
21. **Keep the three simulation domains separate.** The **World** owns environmental truth, the **Amorpho** owns biological requirements and condition, the **Evolutionator** owns inheritance and generational change; **Environmental Fit** is derived and owns nothing. No place names in the plant or the Evolutionator; no biology in the World. The first concrete model is [docs/12](docs/12_ENVIRONMENT_AND_FIT_MODEL_V0.md) — five neutral World dimensions, a zoned response profile, a Fit contract with positive as well as negative outcomes. Surviving is not thriving; the World states conditions, never permissions. (AMO-D035–AMO-D038, AMO-D046–AMO-D053)
22. **Standard and VR are both first-class.** Two interfaces, one persistent world and history. VR is optional, never secondary; account for it in architecture, but build no VR production systems and commit to no VR hardware or SDK. No shared cross-project VR framework — prove first, extract later. (AMO-D041–AMO-D044, [docs/11](docs/11_STANDARD_AND_VR_GAMEPLAY.md))

## How to work here

- **Continue; do not restart.** Build on the existing structure and accepted decisions. Do not redesign the foundation, rename the document set, or start parallel documents that duplicate existing ones.
- **Small durable steps.** Prefer one finished, well-recorded step over broad speculative implementation. *Always moving, never rushed.*
- **Build irreversible knowledge; defer expensive production.** Specifications, decisions and experiment findings are valuable now. Production infrastructure is not.
- **No speculative infrastructure.** No microservices, networking stacks, MMO backends, frameworks or empty boilerplate before a concrete step needs them.
- **No premature engine or language choice.** Do not select or lock in Unity, Unreal, Godot, Bevy, a web stack, a custom engine, a database or a programming language without concrete evidence. Use the criteria in [docs/08_CONCEPTUAL_ARCHITECTURE.md](docs/08_CONCEPTUAL_ARCHITECTURE.md#engine-and-technology-decision-criteria). (AMO-D020)
- **Avoid unnecessary dependencies.** Add one only when a concrete step requires it, and record why.
- **Prototypes are disposable; findings are not.** Write down what an experiment taught before moving on.
- **Document assumptions** where they are made.

## Decided versus open

Keep these strictly separate:

- **Decided:** [docs/DECISIONS.md](docs/DECISIONS.md) (the ledger) and [docs/01_DESIGN_PRINCIPLES.md](docs/01_DESIGN_PRINCIPLES.md) (the laws). Treat them as binding.
- **Open:** [docs/06_OPEN_QUESTIONS.md](docs/06_OPEN_QUESTIONS.md). Candidate options noted there are not decisions.

Never present an open question as settled, and never quietly "decide" something by writing it into a design document. If a step requires a decision:

1. make the smallest reasonable, conservative choice;
2. record it in `docs/DECISIONS.md` (new `AMO-D###`, with origin and rationale), or, if it is only a working assumption, state it explicitly where it is used;
3. update the related open question's status.

## Changing decisions and architecture

- A change to a major product or architectural rule requires a new entry in `docs/DECISIONS.md`.
- Never delete or renumber a decision or open question. Mark superseded decisions `SUPERSEDED by AMO-D###` and explain why. Clarifications that do not change substance may be made in place with a dated *Revised* note.
- **Preserve backwards understanding.** Someone reading an old commit, document or data file must still be able to tell what was true then.
- Changing an input file's columns is an architectural change: update `data/input/README.md` and record a decision.

## Data rules

- `data/input/` holds accepted approved exports only. Never hand-edit them to add or correct facts; corrections arrive as a new approved export. The contract and validation rules are in [data/input/README.md](data/input/README.md).
- An approved export that drops an existing species ID is not accepted automatically (AMO-Q016).
- `data/canon/` is reserved for the internal representation derived from input; it is not defined yet. Do not invent a format for it.
- Illustrations and test fixtures use clearly fictional placeholders and never enter `data/input/`.

## Writing style

- Clear technical English; precise rather than promotional.
- Do not claim Amorpho is "the first" or "unprecedented"; say what it aims to be.
- Other games may be mentioned only as clearly labelled conceptual reference points, sparingly.

## Before ending a session

- [ ] No "TM Amorpho"-style naming introduced.
- [ ] No external runtime, data or research-source dependency introduced.
- [ ] No invented species, hybrid pairs, species IDs or unverified botanical facts.
- [ ] Nothing imported beyond what the game demonstrably needs.
- [ ] Decisions and open questions updated if anything was decided or discovered.
- [ ] Internal links still resolve.
- [ ] The next small step is recorded (roadmap, open questions, or the session's report).

## Repository map

See [README.md](README.md#repository-map).
