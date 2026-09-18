# 07 — Incubation Roadmap

> The game may grow very slowly — but from now on, it never stops growing.

**Current phase:** Phase 0 is complete; the next work belongs to Phase 1 — Systems Specification.

This roadmap is organised by **maturity**, not by dates. No calendar is promised. A phase ends when its exit criteria are met, however long that takes. Phases may overlap: a technical spike can run during specification, and a micro-prototype can motivate a spike.

## Working rules for incubation

- **Always moving, never rushed.** Every session should leave the project a little further along, even if only by one resolved question or one verified record.
- **Build irreversible knowledge now; defer expensive production.** Decisions, verified data, validated experiments and clear specifications last. Production art, content and infrastructure wait until requirements are known and capacity exists.
- **Small, answerable steps.** Each step should answer a specific question or add specific durable knowledge.
- **Experiments are disposable; their findings are not.** Prototype code may be thrown away. What it taught must be written down (in the relevant design document, the decision ledger or the open-question register).
- **No speculative infrastructure.** No servers, networking stacks, microservices or frameworks before an experiment needs them.

---

## Phase 0 — Foundation (complete)

Identity, vision, design laws, decision ledger, open-question register, conceptual architecture, and the approved-input contract for the Reality Gate (species CSV, header only).

**Exit criteria:** a new developer or AI agent can understand what Amorpho is, what is decided, what is open and where to continue — without asking the founders.

## Phase 1 — Systems Specification

Turn concepts into precise, small specifications — on paper, not in engine code.

Typical work:
- accepting the first approved species export, once it is supplied from outside the repository;
- the game's handling of later changes to the approved species list (AMO-Q016);
- the individual-plant model: identity, provenance, genotype/phenotype split (AMO-Q012, AMO-Q013);
- an environment and suitability model, version 0 (AMO-Q005);
- the transformation contract: what an individual plant hands to the combat layer (AMO-Q022, AMO-Q025);
- combat design pillars and a roster strategy (AMO-Q027).

**Exit criteria:** the core models are specified well enough that a prototype can be built against them without inventing their rules along the way.

## Phase 2 — Technical Spikes

Short, throwaway experiments that answer technical questions with evidence.

Candidate spikes:
- automated validation of approved input, if manual checking becomes a burden (AMO-Q038);
- persistence of individuals and provenance over long simulated time;
- fighting-game feel and latency requirements;
- evaluating engine candidates against the criteria in [08_CONCEPTUAL_ARCHITECTURE.md](08_CONCEPTUAL_ARCHITECTURE.md#engine-and-technology-decision-criteria).

**Exit criteria:** enough evidence to make the engine and technology decision (AMO-Q036) deliberately.

## Phase 3 — Micro-Prototypes

Tiny, focused, playable experiments that test whether ideas are **fun**. Each tests one thing.

Candidates (not all are needed, and none needs to be built immediately):
- one persistent plant through its lifecycle;
- one minimal climate-suitability simulation: the same species in two places;
- one small human-space prototype: a room, a pot, a plant;
- one plant → Amorpho transformation;
- a two-character fighting prototype;
- **the transition test:** moving between cultivation and combat with the same plant — the central hypothesis ([04_TRANSFORMATION_AND_COMBAT.md](04_TRANSFORMATION_AND_COMBAT.md#7-the-central-hypothesis-to-test)).

**Exit criteria:** the central hypothesis is either supported, or the concept has been deliberately adjusted through the decision ledger.

## Phase 4 — Vertical Slice

One small, complete, polished piece of the game: a limited region, a small set of real species, one cultivation loop, one transformation, real fights.

**Exit criteria:** people who do not care about plants enjoy it.

## Phase 5 — Early Persistent World

A persistent world, small in scope, with finite populations, trade, propagation and the first real player history.

## Phase 6 — Expanded Content

More regions, more species, lineages emerging over time, deeper economy, broader combat roster.

## Phase 7 — Production Scale

The full game, built by a team with the tools and capacity that the earlier phases waited for.

Phases 5–7 are described only in outline on purpose; they will be specified when the project gets there.

---

## Near-term candidate steps

Small, high-value steps suitable for a single session. Pick one; finish it; record what was learned.

1. Accept the first approved species export into `data/input/amorphophallus_species.csv` — only once it has been supplied from outside the repository — validating it against [`data/input/README.md`](../data/input/README.md).
2. Answer AMO-Q016: how the game treats species that leave, merge or split in a later approved export.
3. Draft the individual-plant model specification (identity, provenance, genotype/phenotype split).
4. Draft an environment and suitability model, version 0, on paper — and only then decide which environmental facts approved input must carry.
5. Write a one-page combat pillars and roster-strategy note (AMO-Q027).
6. Sketch the transition test as a paper prototype before any code.

## Engine decision

No engine has been chosen (AMO-D020). The questions an engine decision must answer are listed in [08_CONCEPTUAL_ARCHITECTURE.md](08_CONCEPTUAL_ARCHITECTURE.md#engine-and-technology-decision-criteria). The decision belongs at the end of Phase 2, based on evidence.
