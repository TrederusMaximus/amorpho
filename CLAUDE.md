# CLAUDE.md — Guidance for AI development agents

This file tells future Claude Code sessions (and any other development agent) how to work in this repository. Read it fully before changing anything. Then read [README.md](README.md), [docs/DECISIONS.md](docs/DECISIONS.md) and [docs/06_OPEN_QUESTIONS.md](docs/06_OPEN_QUESTIONS.md).

## What this repository is

**Amorpho** is a long-running game project: a persistent Earth-like world in which a human player collects, cultivates, propagates and trades individual plants of real *Amorphophallus* species, and can temporarily awaken one as an Amorpho for real-time, skill-based fighting.

**Maturity:** foundation. There is no game code, no engine, no programming language commitment and no species data. The approved species input is header only. The project is entering Phase 1 — Systems Specification ([docs/07_INCUBATION_ROADMAP.md](docs/07_INCUBATION_ROADMAP.md)).

## Non-negotiable rules

### Identity and independence
1. **The product name is Amorpho.** Never "TM Amorpho", "TM Amorpho Game", "Trederus Maximus Amorpho" or any prefixed variant — not in headings, package names, identifiers, file names or docs. The local checkout directory may carry a different name; do not propagate it. (AMO-D001)
2. **Keep the Trederus Maximus affiliation quiet.** It appears as one sentence in the README's About section. It is never a runtime or architecture concern.
3. **Amorpho is independent.** No runtime, build, code or data dependency on any other system — including Imperbio, TM Botanics, any other Trederus Maximus system, or any botanical website or database. No API clients, live data feeds, HTTP fetches, shared databases, shared runtime packages, callbacks, sync jobs, or environment variables pointing at research systems. (AMO-D002, AMO-D018)

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
