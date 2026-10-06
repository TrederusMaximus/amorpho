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

[33_MATURE_LEAF_FUNCTIONAL_COLLAPSE_BOUNDARY_V0.md](33_MATURE_LEAF_FUNCTIONAL_COLLAPSE_BOUNDARY_V0.md) defines the routing seam: a mature Leaf serves until it can no longer meaningfully serve as the active manifestation, judged from current capability rather than appearance, decline or output (AMO-D114, L56). Crossing it commits the loss of that Leaf — visibly legible as a terminal period when gradual, immediate when catastrophic — after which the manifestation ends and the Tuber is the remaining living form (AMO-D115). A doomed Leaf may still be temporarily inhabitable (AMO-D116). The exact criterion, confirmation behaviour, terminal duration and astral cutoff remain open (AMO-Q084, AMO-Q101, AMO-Q103, AMO-Q112, AMO-Q113).

[34_EMBODIMENT_ACROSS_TERMINAL_MANIFESTATION_COLLAPSE_V0.md](34_EMBODIMENT_ACROSS_TERMINAL_MANIFESTATION_COLLAPSE_V0.md) traces the Warden across that boundary. Collapse Commitment ends no embodiment; a doomed manifestation may still be used, and continuous embodiment suspends its terminal progression indefinitely by design, priced in One Consciousness and deferred biology rather than in any timer (AMO-D117). When the manifestation ends, embodiment ends and the consciousness returns to the human body (AMO-D118, L57). The mapping from astral-state damage to biological persistence is explicitly left undecided (AMO-D119, AMO-Q026).

[35_COMBAT_PROTECTION_MANIFESTATION_BODY_DAMAGE_AND_BIOLOGICAL_PERSISTENCE_V0.md](35_COMBAT_PROTECTION_MANIFESTATION_BODY_DAMAGE_AND_BIOLOGICAL_PERSISTENCE_V0.md) resolves that mapping. The animated Amorpho's body is the actual manifestation, so protection decides what reaches it, an effect that reaches it is real biological damage that persists after embodiment, and combat state remains a separate coupled domain with no proportional translation (AMO-D120–AMO-D122, L58, superseding AMO-D119). Suspension of ordinary progression is not invulnerability, so damage accumulates across long embodiments and explicit destruction can end a manifestation whose senescence is paused (AMO-D123). Combat mechanics, protection architecture and combat-state semantics remain open (AMO-Q026, AMO-Q109).

[36_COMBAT_RESOLUTION_SURRENDER_ESCAPE_AND_WITHDRAWAL_V0.md](36_COMBAT_RESOLUTION_SURRENDER_ESCAPE_AND_WITHDRAWAL_V0.md) settles how an encounter ends. A fight is a conflict under escalating risk that normally resolves through surrender, escape, conscious withdrawal or objective resolution, with no universal knockout requirement; winning need not destroy the opponent, losing need not cost the manifestation, and ending a fight does not end the embodiment (AMO-D124–AMO-D126, L59). Fighting to manifestation destruction is permitted escalation rather than the default, and a resolved encounter need not resolve the conflict (AMO-D127, AMO-D128). Combat mechanics, pursuit, conflict consequences and Human Warden conflict remain open (AMO-Q026, AMO-Q028, AMO-Q130).

[37_MANIFESTATION_DESTRUCTION_TUBER_CORE_VIABILITY_AND_PHYSICAL_DROP_V0.md](37_MANIFESTATION_DESTRUCTION_TUBER_CORE_VIABILITY_AND_PHYSICAL_DROP_V0.md) follows the escalated case and fixes the physical ontology behind it. The persistent Tuber travels inside the embodied Amorpho as its central core, so movement moves the individual and complete destruction of the body exposes whatever core the season has actually produced, where it fell — non-playable, immobile, and nothing respawning or awarded to a winner (AMO-D129, AMO-D130, L60). Survival depends on **Tuber Core Viability**: a viable core means the individual outlives its body, and no viable core means the individual is lost (AMO-D131). The Astral Anchor travels with the core and may remain when the plant does not (AMO-D132). Embodiment eligibility stays separate from deployment risk (AMO-D133), and one manifestation body spans rooted and inhabited modes while its appearance records its own history rather than the core's (AMO-D134). Viability criteria, productivity, rescue, custody and Anchor rebinding remain open (AMO-Q104, AMO-Q116, AMO-Q117, AMO-Q046, AMO-Q091, AMO-Q093).

[38_END_TO_END_COMBAT_ENCOUNTER_AND_BIOLOGICAL_CONTINUITY_TRACE_V0.md](38_END_TO_END_COMBAT_ENCOUNTER_AND_BIOLOGICAL_CONTINUITY_TRACE_V0.md) is the **integration trace for that whole chain, and it passes**. One individual runs from rooted life through embodiment, an intercepted effect, a body-reaching effect, a risk decision under uncertainty, Conscious Withdrawal, relocation, rooting, mature recovery and the rest of its season — and through contrast branches into Functional Collapse, terminal embodiment and manifestation destruction with either a viable or a non-viable core. **No new decision or law was required.** Audits for double accounting, mode copies, hidden knockout assumptions and state resets came back clean. Two clarifications were recorded: combat reaches the individual only as death via a non-viable core, never as permanent injury (AMO-D075, AMO-D131), and a Tuber has two transport modes with two different rules (AMO-D084 embodied versus AMO-D093 carried). Everything downstream now waits on seasonal accounting (AMO-Q116).

[39_ACTIVE_LEAF_PRODUCTIVE_RETURN_AND_PERSISTENT_TUBER_BENEFIT_V0.md](39_ACTIVE_LEAF_PRODUCTIVE_RETURN_AND_PERSISTENT_TUBER_BENEFIT_V0.md) supplies that accounting qualitatively. **Active Leaf Productive Return** is biological work performed during rooted active life; Functional Capacity is a non-linear input rather than the return itself, and return depends jointly on capacity, Environmental Fit, condition, actual rooted time and Remaining Productive Opportunity (AMO-D135). Embodiment suspends it, which is why an early-inhabited fighter can become battle-worn with a core that never rebuilt (AMO-D136). Realized return is never erased by later loss — a lost Leaf forfeits its future work, not its past (AMO-D137, L61) — and insufficient return is not pathology, with the persistent-loss boundary handed to AMO-Q118 (AMO-D138). AMO-Q116 stays open for everything quantitative.

[40_ROOTED_MATURE_LEAF_RECOVERY_CEILING_AND_COMPENSATORY_REMODELING_V0.md](40_ROOTED_MATURE_LEAF_RECOVERY_CEILING_AND_COMPENSATORY_REMODELING_V0.md) specifies what rehabilitation actually is. A damaged mature Leaf stabilizes, scars and **compensatorily remodels** surviving structure so it carries more useful function, without reconstructing anything lost (AMO-D139, L62). Functional recovery can therefore be substantial while the scars stay permanent (AMO-D140), bounded by a qualitative **Recovery Ceiling** that further damage can permanently lower and no environment can lift (AMO-D141). Recovery potential and remaining opportunity stay independent axes. Extent, rates, ceiling representation and any cost of rehabilitation remain open (AMO-Q103, AMO-Q086, AMO-Q116).

[41_BLOOM_EMBODIMENT_CORE_SECURITY_AND_DESTRUCTION_VALUE_V0.md](41_BLOOM_EMBODIMENT_CORE_SECURITY_AND_DESTRUCTION_VALUE_V0.md) turns Bloom into an information asymmetry rather than a flower skin. A Bloom exists only where the persistent individual had already become capable of producing one, so its presence is evidence of substantial biology — a lower bound, never a readout of present condition (AMO-D142, L63). Bloom embodiment carries the same Tuber and Anchor, and destruction exposes the actual current core with no Bloom loot rule (AMO-D143). Programmed Draw means capability evidence is historical, so confidence rises without any guarantee (AMO-D144). Bloom's capabilities, costs, damage response and reproductive return remain open (AMO-Q088, AMO-Q107, AMO-Q086, AMO-Q079).

[42_WORLD_TIME_SEASONAL_OPPORTUNITY_AND_EMBODIMENT_V0.md](42_WORLD_TIME_SEASONAL_OPPORTUNITY_AND_EMBODIMENT_V0.md) closes an ambiguity the productive-return pass left open, and adds the boundary that closure required. **Embodiment freezes the plant, not the planet**: the World's seasons advance while an inhabited individual's biology is paused, so suitable opportunity can pass unused and is never banked, and elapsed world time grants no return, no maturity and no stronger core (AMO-D145, AMO-D136 revised, L64). Because a mobile Amorpho could otherwise chase seasons forever, environmental suitability and intrinsic lifecycle permission are separated: relocation and greenhouses change conditions, never a lifecycle, and **a Warden can chase suitable weather but cannot outrun dormancy** (AMO-D146, L65). Species biology shapes which lifecycle strategies exist while the individual owns its current state, and fairness comes from trade-offs rather than equal uptime (AMO-D147). Lifecycle triggers, commitment boundary, species facts and quantitative opportunity remain open (AMO-Q101, AMO-Q084, AMO-Q110, AMO-Q116).

[43_ORDINARY_DEPLETION_TO_PERSISTENT_HARM_BOUNDARY_V0.md](43_ORDINARY_DEPLETION_TO_PERSISTENT_HARM_BOUNDARY_V0.md) resolves the qualitative core of AMO-Q118. **Ordinary depletion** is defined positively, and legitimate expenditure — construction, Replacement, Bloom's Programmed Draw — together with insufficient return and missed opportunity is depletion rather than injury, however severe (AMO-D148, L66). **Persistent harm** requires actual degradation of enduring structure, capability or condition; crossing changes what happened rather than a value, cumulative strain crosses only where persistence degrades, and no new manifestation, dormancy or elapsed time resets it (AMO-D149). Replenishment and repair stay separate processes (AMO-D150), and Core Viability is a separate dimension from pathology (AMO-D151). **Detailed persistent pathology — causes, diagnosis, treatment, repair — is a deliberately lower-priority future layer beside the core loop, owned by AMO-Q105**; only the boundary was needed now. Quantitative criteria remain AMO-Q118.

[44_FULL_BIOLOGICAL_YEAR_PERSISTENT_STATE_INTEGRATION_TRACE_V1.md](44_FULL_BIOLOGICAL_YEAR_PERSISTENT_STATE_INTEGRATION_TRACE_V1.md) is the **full-cycle integration trace, and it passes**. One individual runs from a viable dormant Tuber through construction, post-construction depletion, rooted productive work, improving core viability, embodiment with real missed opportunity, mature damage, rehabilitation to a scarred but strongly functional Leaf, renewed return, ordinary retirement, dormancy and a fresh next manifestation — ending **viable and meaningfully provisioned with no pathology anywhere**. **No new decision, law or question was required.** Audits for double accounting and hidden scalar health came back clean, and the trace names what a later quantitative model must not break: temporary and persistent state stay split, cost/loss/harm stay three different things, and nothing in the cycle is a reset. Doc 22 remains the foundational walkthrough.

[45_REMAINING_PRODUCTIVE_OPPORTUNITY_QUALITATIVE_COMPOSITION_V0.md](45_REMAINING_PRODUCTIVE_OPPORTUNITY_QUALITATIVE_COMPOSITION_V0.md) gives that frontier its first qualitative representation. **Remaining Productive Opportunity** is derived future possibility — not stored value, elapsed time or a countdown — and no single scalar may own it (AMO-D152). Useful opportunity exists only where **External Productive Opportunity** (World, reachable), **Biological Growth Availability** (the individual's lifecycle) and **Manifestation Productive Usability** (the current Leaf) overlap, as conjunction rather than a formula (AMO-D153, L67). Rehabilitation, Replacement and relocation each restore only their own component and never opportunity already passed (AMO-D154). Roster choice gains a biological dimension: **choosing an Amorpho to inhabit also means choosing whose opportunity to interrupt**. Everything quantitative, reachability and presentation remain AMO-Q116.

[46_DORMANCY_COMMITMENT_BOUNDARY_V0.md](46_DORMANCY_COMMITMENT_BOUNDARY_V0.md) draws the boundary doc 45 leaned on, with **no new state**. **Dormancy Approach** is a still-active condition within Active Leaf, where environment may still matter; **Dormancy Commitment** is what the Active Leaf → Senescence edge means, belongs to the individual's lifecycle, closes Biological Growth Availability for the phase and is irreversible by weather, relocation, rooting, embodiment or greenhouses (AMO-D155, L68). Environment influences before commitment and cannot reset after; commitment is history-sensitive, and dormancy is a strategy rather than a failure, with no universal annual cycle and no anti-exploit rule (AMO-D156). Embodiment pauses lifecycle progression on both sides: world time alone cannot push a paused individual across, and a committed one stays committed (AMO-D157). **Collapse ends a Leaf; Dormancy Commitment ends a phase.** Triggers, timing, species parameterization and player cues remain open (AMO-Q101, AMO-Q084, AMO-Q119).

[47_DEEP_DORMANCY_DURATION_AND_ACTIVE_PHASE_REACTIVATION_BOUNDARY_V0.md](47_DEEP_DORMANCY_DURATION_AND_ACTIVE_PHASE_REACTIVATION_BOUNDARY_V0.md) supplies the opposite half, again with **no new state**. **Deep Dormancy is biological life, not frozen time**: dormant biology runs with World Time, unlike embodiment's pause, and dormancy duration belongs to the individual within its species strategy — emergent, never a timer or cooldown (AMO-D158). **Intrinsic Reactivation Readiness** and **External Emergence Suitability** are separate and both required: a suitable environment cannot wake an unready Tuber, and a ready one need not emerge into unsuitable conditions (AMO-D159, L69). Readiness is not feasibility, so **Reactivation Commitment** — the meaning of the Deep Dormancy → Pre-Emergence edge — also needs a Tuber able to fund a manifestation, and the new cycle begins from exactly the persistent state carried through dormancy (AMO-D160). Readiness representation, timing, species parameterization and dormancy maintenance remain open (AMO-Q101, AMO-Q084, AMO-Q102).

[48_ROSTER_TIMING_AND_ONE_CONSCIOUSNESS_BIOLOGICAL_OPPORTUNITY_TRACE_V0.md](48_ROSTER_TIMING_AND_ONE_CONSCIOUSNESS_BIOLOGICAL_OPPORTUNITY_TRACE_V0.md) is the **roster-timing integration check, and it passes**. One Warden, a seasonal individual in a short valuable window, an extended-growth individual and a dormant one nearing reactivation meet one threat: the choice between the first two is a choice between **different biological timing costs**, the dormant one matters while unplayable and emerges only through biology, unselected plants keep living, and the roster afterwards has changed persistently. **No decision, law, cooldown, energy, mandatory rest or equal-uptime rule was needed**; One Consciousness turns biological timing into roster strategy. It also showed that choosing a body chooses where that body will be when its biology resumes, and that a seasonal individual becomes cheap to use once its own window has closed. Two leaning points were recorded against existing owners: body-to-body presence transfer (AMO-Q040) and what the Warden can know about lifecycle position and readiness (AMO-Q044). What the trace could not supply is the other side of the scale — why one body would be better in a given fight.

[49_COMBAT_PILLARS_AND_BIOLOGICAL_ROSTER_STRATEGY_V0.md](49_COMBAT_PILLARS_AND_BIOLOGICAL_ROSTER_STRATEGY_V0.md) supplies that other side qualitatively and resolves the design-space half of AMO-Q027. **Biological Deployment Cost** and **Combat Suitability** are separate axes, and the roster decision is the tension between what a body costs to risk and what it is worth risking for (AMO-D161, L70). Combat identity comes from skill, preparation and deliberate design, never from botanical size, rarity or taxonomy (AMO-D162). Skill includes preserving the living body: protection is preservation rather than extra health, and disengagement is mastery (AMO-D163). Eleven pillars name the space concrete combat must satisfy; moves, resources, protection mechanics, controls and fighter production at scale remain open (AMO-Q027, AMO-Q026, AMO-Q109, AMO-Q023).

[50_WARDEN_BIOLOGICAL_INFORMATION_AND_ROSTER_JUDGEMENT_MODEL_V0.md](50_WARDEN_BIOLOGICAL_INFORMATION_AND_ROSTER_JUDGEMENT_MODEL_V0.md) removes the omniscience assumption and resolves the qualitative core of AMO-Q044. **Biological truth and Warden knowledge are separate**: the Warden judges from observation, individual history, species tendency and environmental context rather than readouts — enough to judge, not to calculate — and no system recommends a body (AMO-D164, L71). Uncertainty must stay causally grounded: a reasonable judgement may be wrong, an arbitrary outcome may not (AMO-D165). The **Astral Anchor** becomes an awareness channel as well as an access path, carrying qualitative feedback bounded by the Astral Signal and silent in Deep Dormancy (AMO-D166), and **Astral Attunement** lets one Warden read one long-known individual more finely without ever reading it exactly (AMO-D167, AMO-Q131). Owner knowledge may exceed an opponent's. Presentation remains open (AMO-Q044, AMO-Q115).

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

1. **Draft the individual-plant model specification, qualitatively** — doc 50 makes individual history a primary knowledge source and Attunement follows the persistent individual, yet the persistent individual's state is spread across docs 03 and 14–50. Consolidate, as an inventory of concepts rather than a schema, what one persistent individual carries — identity, provenance, genotype/phenotype split, persistent biological dimensions, lifecycle position and history, manifestation history, Anchor binding and Attunement relationships — and what is temporary to a manifestation, recording which history categories persist (AMO-Q120, AMO-Q012). No fields, formats or storage.
2. Accept the first approved species export into `data/input/amorphophallus_species.csv` — only once it has been supplied from outside the repository — validating it against [`data/input/README.md`](../data/input/README.md).
3. Answer AMO-Q016: how the game treats species that leave, merge or split in a later approved export.
4. Sketch the transition test as a paper prototype before any code.
5. Sketch a broader emergent scenario on paper — two *threatened* Amorphos, one body, different environments — building on the roster-timing trace in [48](48_ROSTER_TIMING_AND_ONE_CONSCIOUSNESS_BIOLOGICAL_OPPORTUNITY_TRACE_V0.md), to check that the laws really do generate the dilemma without scripting it (L37).

## Engine decision

No engine has been chosen (AMO-D020). The questions an engine decision must answer are listed in [08_CONCEPTUAL_ARCHITECTURE.md](08_CONCEPTUAL_ARCHITECTURE.md#engine-and-technology-decision-criteria). The decision belongs at the end of Phase 2, based on evidence.
