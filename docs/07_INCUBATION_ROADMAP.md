# 07 — Incubation Roadmap

> The game may grow very slowly — but from now on, it never stops growing.

**Current phase:** Phase 0 is complete. Phase 1 — Systems Specification — has begun. The first design pass (2026-09-20) settled the embodiment model, the World / Amorpho / Evolutionator ownership split and the Standard/VR interface principles; a following pass (2026-09-21) fixed the World as the real Earth (AMO-D045). All of it as laws and decisions rather than mechanics.

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
- inhabitability and the three tolerance concepts, now that Fit v0 exists (AMO-Q042, AMO-Q051);
- Fit internals: value representation, aggregation and limiting factors (AMO-Q069, AMO-Q070);
- the transformation contract: what an individual plant hands to the combat layer (AMO-Q022, AMO-Q025);
- combat design pillars and a roster strategy (AMO-Q027);
- an Evolutionator model, version 0: inheritance, variation, generation timing (AMO-Q013, AMO-Q052).

Done in this phase so far: Pathological Tuber Impact ([21](21_PATHOLOGICAL_TUBER_IMPACT_V0.md); AMO-D090–AMO-D093), the biology–magic boundary and Astral Readiness ([20](20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md); AMO-D084–AMO-D089), Developmental Maturity ([19](19_DEVELOPMENTAL_MATURITY_V0.md); AMO-D080–AMO-D083), harm horizons, the recovery law and Bloom maturity ([18](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md); AMO-D074–AMO-D078), the life-cycle state machine ([17](17_LIFE_CYCLE_STATE_MACHINE_V0.md); AMO-D070–AMO-D073), the human's own progression domain and Astral Capacity ([16](16_HUMAN_WARDEN_PROGRESSION_V0.md); AMO-D066–AMO-D069), the life-cycle, Astral Anchor and availability architecture ([15](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md); AMO-D058–AMO-D065), the individual's biological condition model ([14](14_CURRENT_BIOLOGICAL_CONDITION_V0.md); AMO-D056, AMO-D057), the environment model validated against four worked cases ([13](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md)), including the World/Fit interaction boundary (AMO-D055), the embodiment model, the three-domain ownership split and the Standard/VR principles ([09](09_EMBODIMENT_AND_ASTRAL_TRANSFER.md), [10](10_WORLD_AMORPHO_EVOLUTIONATOR.md), [11](11_STANDARD_AND_VR_GAMEPLAY.md); AMO-D028–AMO-D044), Earth as the World's geographic foundation ([02](02_WORLD_MODEL.md); AMO-D045), and the Environment and Environmental Fit model v0 ([12](12_ENVIRONMENT_AND_FIT_MODEL_V0.md); AMO-D046–AMO-D053).

The first complete qualitative integration trace is [22_BIOLOGICAL_YEAR_WALKTHROUGH_V0.md](22_BIOLOGICAL_YEAR_WALKTHROUGH_V0.md). It found no missing simulation owner and left productivity, direct Tuber susceptibility and the crossing into actual loss with AMO-Q116–AMO-Q118.

The first acute-event handoff is traced in [23_ACUTE_EVENT_TO_LEAF_IMPAIRMENT_V0.md](23_ACUTE_EVENT_TO_LEAF_IMPAIRMENT_V0.md): a World occurrence becomes local exposure, then a distinct structural and functional state of the current Leaf. Event representation and response rules remain open.

[24_SAME_PHASE_LEAF_RECOVERY_V0.md](24_SAME_PHASE_LEAF_RECOVERY_V0.md) traces mature-Leaf stabilization and functional recovery separately from possible replacement emergence. Recovery extent and replacement routing remain open; neither trace evaluates persistent Tuber outcome.

[25_TUBER_FUNDED_MANIFESTATION_AND_REPLACEMENT_ROUTING_V0.md](25_TUBER_FUNDED_MANIFESTATION_AND_REPLACEMENT_ROUTING_V0.md) adds the funded intra-cycle replacement loop and the eligibility-before-choice boundary. It leaves route triggers, autonomous policy and player agency availability open.

[26_PLANT_AUTONOMY_ASTRAL_LEVERAGE_AND_ROUTING_V0.md](26_PLANT_AUTONOMY_ASTRAL_LEVERAGE_AND_ROUTING_V0.md) answers who selects a route: biology bounds it, the individual's own autonomy prefers its continuation, and a Warden with direct astral presence may choose differently among feasible routes at full biological cost (AMO-D098–AMO-D101). It names the **Astral Window** without making the Tuber playable, and leaves the autonomous policy, presence mechanics and player knowledge open.

[27_PLATFORM_AND_WORLD_SOVEREIGNTY_V0.md](27_PLATFORM_AND_WORLD_SOVEREIGNTY_V0.md) establishes one canonical World, Warden continuity across gateways, and the client/platform boundary (AMO-D102–AMO-D105). It sets product and technology-selection requirements without selecting an implementation.

[28_ASTRAL_WINDOW_END_TO_END_TRACE_V0.md](28_ASTRAL_WINDOW_END_TO_END_TRACE_V0.md) tests Leaf collapse through autonomous Replacement, Warden override or agreement, an impossible override and a missed Window. It finds no missing invariant or need for a new decision or law; the replacement Signal/Readiness handoff stays open.

[29_REPLACEMENT_EMERGENCE_TO_ASTRAL_READINESS_V0.md](29_REPLACEMENT_EMERGENCE_TO_ASTRAL_READINESS_V0.md) establishes shared biological Emergence for Leaf and Bloom, a non-playable developing period, Full Deployment before normal inhabitation, and a route out of failed attempts (AMO-D106–AMO-D108). Exact damage, timing, access and Readiness remain open.

[30_EMERGENCE_INVESTMENT_AND_FULL_DEPLOYMENT_ACCOUNTING_BOUNDARY_V0.md](30_EMERGENCE_INVESTMENT_AND_FULL_DEPLOYMENT_ACCOUNTING_BOUNDARY_V0.md) fixes accumulating Tuber construction investment, the independence of visible damage and sunk cost, and Full Deployment as the handoff to mature manifestation performance and damage ownership (AMO-D109–AMO-D111, L55). Investment remains distinct from Pathological Tuber Impact.

[31_DAMAGED_EMERGENCE_TO_IMPERFECT_DEPLOYMENT_V0.md](31_DAMAGED_EMERGENCE_TO_IMPERFECT_DEPLOYMENT_V0.md) traces damaged construction through compensation, imperfect Full Deployment or failure. Full Deployment transfers the actual built state without healing it (AMO-D112–AMO-D113); developmental response and exact completion remain open.

[32_IMPERFECTLY_DEPLOYED_MATURE_LEAF_STABILIZATION_OR_DECLINE_V0.md](32_IMPERFECTLY_DEPLOYED_MATURE_LEAF_STABILIZATION_OR_DECLINE_V0.md) follows a Leaf that deployed already compromised through its first mature period: stabilization and functional recovery, a stable compromised equilibrium, or decline toward a later routing question. It needed no new decision or law — the mature domain inherits the actual constructed state and the Tuber is not charged twice (AMO-D094, AMO-D111, AMO-D113, L51, L55). Recovery extent, any attainable functional ceiling, the collapse criterion, productivity and playable consequences remain open (AMO-Q086, AMO-Q101, AMO-Q103, AMO-Q109, AMO-Q112, AMO-Q116, AMO-Q118).

**Exit criteria:** the core models are specified well enough that a prototype can be built against them without inventing their rules along the way.

## Phase 2 — Technical Spikes

Short, throwaway experiments that answer technical questions with evidence.

Candidate spikes:
- automated validation of approved input, if manual checking becomes a burden (AMO-Q038);
- **the Environment/Fit v0 validating spike** (its three cases are already walked on paper in [13](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md); a spike must reproduce them) — one abstract location, one environment state, one abstract profile, one condition, time progression, and three cases: deterioration, equilibrium, and improvement/recovery. No real species, no graphics, no map, no engine. If those three cases cannot be produced from the v0 contract, v0 is wrong and is revised through the ledger ([12](12_ENVIRONMENT_AND_FIT_MODEL_V0.md) §22);
- persistence of individuals and provenance over long simulated time;
- fighting-game feel and latency requirements;
- evaluating engine candidates against the criteria in [08_CONCEPTUAL_ARCHITECTURE.md](08_CONCEPTUAL_ARCHITECTURE.md#engine-and-technology-decision-criteria).

**Exit criteria:** enough evidence to make the engine and technology decision (AMO-Q036) deliberately.

## Phase 3 — Micro-Prototypes

Tiny, focused, playable experiments that test whether ideas are **fun**. Each tests one thing.

Candidates (not all are needed, and none needs to be built immediately):
- one persistent plant through its lifecycle;
- one minimal Environmental Fit simulation: the same species in two places;
- one small human-space prototype: a room, a pot, a plant;
- one plant → Amorpho transformation;
- a two-character fighting prototype;
- one rooting decision: the same Amorpho rooted in two different environments, to see whether the trajectory range reads as a real choice (AMO-D033);
- **the transition test:** moving between cultivation and combat with the same plant — the central hypothesis ([04_TRANSFORMATION_AND_COMBAT.md](04_TRANSFORMATION_AND_COMBAT.md#7-the-central-hypothesis-to-test)).

The VR questions (AMO-Q056–AMO-Q062) will eventually need prototypes of their own, and this is where they belong — not earlier. Recording them now is what AMO-D043 asks for; building them now is what it forbids.

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

### Future track — Platform Viability / Client Architecture

After core design and evidence-based technology selection, examine desktop, mobile, console and VR/XR reach, scalable fidelity, input translation, certification and continuity across client generations (AMO-Q036, AMO-Q037, AMO-Q126–AMO-Q128). This track has no date or launch order and authorises no port or platform integration now.

---

## Near-term candidate steps

Small, high-value steps suitable for a single session. Pick one; finish it; record what was learned.

1. **Define the shape of the mature Leaf functional-collapse boundary** — close the seam where [32](32_IMPERFECTLY_DEPLOYED_MATURE_LEAF_STABILIZATION_OR_DECLINE_V0.md) stops and [25](25_TUBER_FUNDED_MANIFESTATION_AND_REPLACEMENT_ROUTING_V0.md) begins: what distinguishes a merely imperfect or declining Leaf from one that can no longer serve, stated qualitatively and workable for a Leaf that began mature life impaired, with no threshold, rate or productivity model (AMO-Q101, AMO-Q103). Active-phase productivity integration (AMO-Q116) remains the larger step after it.
2. Accept the first approved species export into `data/input/amorphophallus_species.csv` — only once it has been supplied from outside the repository — validating it against [`data/input/README.md`](../data/input/README.md).
3. Answer AMO-Q016: how the game treats species that leave, merge or split in a later approved export.
4. Draft the individual-plant model specification (identity, provenance, genotype/phenotype split).
5. Write a one-page combat pillars and roster-strategy note (AMO-Q027).
6. Sketch the transition test as a paper prototype before any code.
7. Sketch one emergent scenario end to end on paper — two threatened Amorphos, one body, different environments — to check that the laws from this pass really do generate the dilemma without scripting it (L37).

## Engine decision

No engine has been chosen (AMO-D020). The questions an engine decision must answer are listed in [08_CONCEPTUAL_ARCHITECTURE.md](08_CONCEPTUAL_ARCHITECTURE.md#engine-and-technology-decision-criteria). The decision belongs at the end of Phase 2, based on evidence.
