# 12 — Environment and Environmental Fit, Model v0

**Status:** specification, version 0. This is the first usable environmental model for the accepted architecture. It is a **boundary contract**, not a biological simulation: it fixes what the World provides, what an Amorpho provides, what Fit evaluates and what Fit returns. It defines no numbers, units, formulas, tick rates or species values, and it contains no botanical facts. Where something is undecided it points to [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).

> Earth says where. World says what conditions exist there now. The Amorpho says what it needs. Environmental Fit says what happens. The Evolutionator determines what persists across generations.

## 1. What v0 is, and is not

v0 is deliberately small. It must be understandable in one sitting, testable later, extensible, capable of **positive as well as negative** outcomes, usable indoors and outdoors, usable across seasons and weather, and independent of any species, country or engine.

**v0 is intended to answer:** what the World provides · what the Amorpho provides · what Fit evaluates · what Fit returns.

**v0 does not finalise:** real species tolerance values · simulation equations · physiological realism · greenhouse mechanics · pot mechanics · acclimation · evolution · weather generation.

It is not an attempt to model plant physiology. It is the minimum viable environmental abstraction from which those things can later grow without the boundary moving.

## 2. The boundary this model serves

| Layer | Owns | Answers |
|---|---|---|
| **Earth** | real geographic foundation (AMO-D045) | *Where is this happening?* |
| **World** | environmental truth (AMO-D035) | *What conditions exist here, now?* |
| **Amorpho** | biological requirements, tolerances, traits, current state (AMO-D036) | *What does this individual need and tolerate?* |
| **Environmental Fit** | nothing — it evaluates (AMO-D037) | *What biological trajectory results from this individual existing in these conditions?* |
| **Evolutionator** | inheritance, variation, generational change (AMO-D038) | *What persists across generations?* |

Earth geography is **not** itself the biological environment model. Earth locates; the World describes. See [10_WORLD_AMORPHO_EVOLUTIONATOR.md](10_WORLD_AMORPHO_EVOLUTIONATOR.md).

## 3. World Environment Vector v0

The World produces five environmental dimensions. They are **neutral facts**, never judgements:

| Dimension | What it represents |
|---|---|
| **Temperature** | the thermal condition experienced locally |
| **Water availability** | usable moisture available to the plant and its root system |
| **Light availability** | light available to the individual at its local site |
| **Air moisture / humidity** | atmospheric moisture, kept separate from root-zone water |
| **Exposure / protection** | how exposed the individual is to environmental forces, versus sheltered by its setting |

No World value is ever labelled *good*, *bad*, *suitable*, *unsuitable*, *tropical* or *species-compatible*. Those are interpretations, and interpretation is Fit's job (AMO-D035, AMO-D047).

**Water availability is not rainfall.** `rainfall ≠ root-zone water availability`. Future World modelling may derive availability from rainfall, irrigation, substrate, drainage, container state and evaporation — none of which is modelled now. The dimension deliberately names the thing the plant actually experiences, so that the mechanisms can be added later without changing what Fit consumes.

**Light availability is not a light source.** It may later be derived from time of day, cloud, shade, canopy, buildings, greenhouses or artificial light. v0 models none of those sources.

**Air moisture is separate from water availability** because they are biologically different. A humid place with dry substrate and a dry place with saturated substrate are not the same situation, and a model that merges them cannot express either.

**Exposure / protection is provisional, and is a different *kind* of thing from the other four.** The other dimensions describe conditions an individual continuously experiences; this one describes **vulnerability to environmental forces and events** — wind, storms, weather extremes, and whatever an events system eventually adds. It is not a fifth comfort axis.

It carries a real risk: a vague universal score can quietly absorb every future variable and become meaningless, and a dimension without a clear job attracts one. The worked scenarios confirmed the concern rather than dispelling it — across a failing, a stable and a flourishing case it never once decided an outcome, because all three are sustained-condition cases and it has nothing to modify in them ([13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md) §6).

It is therefore retained but **unproven rather than validated**. Its real test comes only when acute events exist (AMO-Q020), and it may decompose then (AMO-Q069).

No units, scales or normalisation are chosen. Standard physical units are a likely eventual representation for some dimensions; that is a note, not a decision (AMO-Q069).

## 4. What v0 leaves out, and why

Deliberately deferred: soil chemistry · pH · nutrients · altitude as a direct biological variable · wind as its own detailed vector · atmospheric pressure · detailed rainfall history · pathogen load · pest populations · pollinator availability · exact drainage mechanics · detailed substrate chemistry.

Several of these matter in reality and several will matter in the game. None belongs in v0 merely because it exists.

> Add environmental dimensions when gameplay or biological modelling demonstrates a need.

This is the environmental form of AMO-D025 — import and model only what is demonstrably needed — applied to design data rather than to approved input.

## 5. Local Environment State

The World produces a **Local Environment State** for a specific place, time and local context:

```
LocalEnvironment(place, time, context)
```

Context matters: at one geographic position there may be different environments outside, inside a house, inside a greenhouse, under shade, inside a protected structure, or in a particular pot and root zone.

No nesting mechanics are implemented. The principle is that **World conditions are progressively modified into local conditions**, and that whatever does the modifying produces the same five dimensions, so Fit never learns about buildings (AMO-D046).

## 6. Geography is not environment

The hierarchy already recorded in [02_WORLD_MODEL.md](02_WORLD_MODEL.md) locates things. This one produces conditions:

```
EARTH GEOGRAPHY
      ▼
regional / local World conditions
      ▼
weather + season + time
      ▼
local modifiers
      ▼
building / greenhouse / shelter
      ▼
container / substrate / root zone
      ▼
LOCAL ENVIRONMENT STATE
```

Not every level need exist in v0 — most do not. The hierarchy exists so future complexity can be inserted **between** levels without changing who owns what (AMO-Q065).

## 7. Time is fundamental

Environment is never a permanent property of a place. The model is `Environment(place, time)`, not `Environment(place)` (AMO-D046).

The same location may move between excellent, good, adequate, stressful and critical conditions over time, through season, weather, time of day, player-controlled environment, or future environmental events. A place that is favourable in one season may be dangerous in another, and that is the point.

### Instantaneous environment versus exposure history

Effects may eventually depend both on conditions **now** and on how long the individual has experienced them:

| | Meaning |
|---|---|
| **Instantaneous environment** | current conditions |
| **Exposure history** | accumulated recent experience of those conditions |

This matters because `brief cold ≠ prolonged cold` and `one dry interval ≠ sustained drought`.

No exposure mathematics is defined. v0 only reserves the distinction so an exposure model can be added later without redefining the boundary (AMO-Q072).

## 8. Amorpho Response Profile v0

For each dimension the Amorpho side eventually provides a biological response profile. v0 prefers **zones** over a single ideal number:

| Zone | Meaning |
|---|---|
| **Preferred range** | conditions under which the individual can thrive |
| **Tolerable range** | outside preferred, still biologically manageable |
| **Critical boundary** | beyond which severe stress or damage may develop |

**No numeric values exist, and none may be invented** (L4, AMO-D025, AMO-D036). No real *Amorphophallus* tolerance has entered Amorpho, and none may be guessed here or anywhere else.

Nor does every dimension necessarily need exactly three hard ranges forever; a later implementation may use continuous response curves. What v0 fixes is only that the profile can distinguish **thriving** from **surviving** from **failing** (AMO-D048).

### Three contributing layers

The profile an individual actually responds with is layered:

```
SPECIES BASELINE      reality-grounded characteristics of the species
        +
INDIVIDUAL TRAITS     heritable or otherwise persistent individual variation
        +
CURRENT CONDITION     health, accumulated stress, recovery state,
                      developmental condition, later acclimation
        ▼
EFFECTIVE RESPONSE PROFILE
```

No genetics and no acclimation are implemented here; the Evolutionator owns the first (AMO-D038) and acclimation remains open (AMO-Q012). v0 establishes the layering so that individual variation and condition have somewhere to live from the start, rather than being retrofitted onto a species-only model.

## 9. Environmental Fit v0 — output contract

Fit consumes a Local Environment State and an effective response profile, and produces the smallest set of outputs downstream systems need (AMO-D049):

| | Output | Purpose |
|---|---|---|
| **A** | **Fit by dimension** | how well each dimension matches this individual — temperature fit, water fit, light fit, humidity fit, exposure fit |
| **B** | **Biological direction** | conceptually *improving*, *stable* or *deteriorating*; may later become continuous |
| **C** | **Stress pressure** | how strongly conditions push the individual toward biological stress |
| **D** | **Growth / recovery opportunity** | how strongly conditions support positive development or recovery |
| **E** | **Critical constraint indicators** | which dimensions, if any, are currently severe limiting factors |

No numeric ranges, scales or formulas are defined. Nothing further is added unless a downstream system demonstrates a need.

**Why per-dimension information is preserved.** Collapsing everything into one score immediately would make it impossible for any later system — gameplay, UI, a player's own reasoning — to say *why* a plant is struggling. Output A keeps that available; output B keeps the aggregate that downstream systems actually act on. Both are required.

**How the outputs are meant to be read** (clarified 2026-09-21 from the worked scenarios in [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md)):

- **B is the *condition* trajectory, and must be read together with D.** B alone cannot distinguish an individual that is thriving at its healthy baseline from one merely persisting in a mediocre place — both report *stable*. The pair does distinguish them: stable with modest opportunity is persistence; stable with high opportunity is flourishing. A consumer that reads B in isolation will flatten exactly the distinction L38 protects.
- **C is a pressure, not an accumulated total.** Stress pressure describes how hard conditions are pushing *now*; what has built up over time lives in the individual's condition (§13). Conflating them would make a brief severe episode indistinguishable from a long mild one (AMO-Q072).
- **D is gated by limiting factors, not only by the aggregate.** Favourable warmth and light produce no growth opportunity in an individual with no usable water: the resources cannot be spent. Output E therefore constrains D as well as B (AMO-Q070).
- **A is *independent* dimension fit, and must be read together with E.** It answers how each dimension compares with the profile *on its own*, which by construction cannot show anything that exists only in a combination. Two dimensions may each read *tolerable* while their interaction is severe. A is a diagnostic decomposition, never a complete explanation.
- **E names constraints, which may be a dimension or an interaction.** A severe limiting factor is not always a single dimension: a temperature × water interaction can be the binding constraint while neither dimension is individually critical. E may name such a pair (AMO-D055).

**None of the five outputs is self-sufficient.** They are five views of one evaluation, and every rule above is an instance of the same thing — B read with D, A read with E, D gated by E. A consumer acting on one output in isolation will misread the situation.

## 10. The Fit continuum

The internal model is preferred **continuous**. Qualitative tiers remain useful for documentation, UI, debugging and player feedback:

| Label | Conceptual trajectory |
|---|---|
| **Excellent** | strong positive biological trajectory |
| **Favourable** | healthy growth and stability |
| **Adequate** | stable equilibrium, normal survival |
| **Marginal** | limited performance, slowly accumulating stress |
| **Poor** | active deterioration |
| **Severe** | rapid deterioration |
| **Critical** | immediate risk of major damage or death |

These are **not mandatory internal states**, and nothing may lock an implementation to seven enumerated values. An evaluator may work in continuous values and expose categories outward. Whether the internal model ends up continuous, tiered or both is open (AMO-Q069).

## 11. Surviving is not thriving

> Absence of stress is not the maximum positive outcome.

The model must distinguish **not dying** from **stable survival** from **healthy growth** from **highly favourable development** (L38, AMO-D049).

Excellent Fit may produce recovery, stronger growth, better development, resource accumulation, improved health and improved reproductive readiness. A perfect environment must be genuinely valuable — not merely the absence of punishment. A model in which the best possible outcome is "nothing bad happened" has failed this requirement, and would quietly turn the whole environmental system back into a penalty mechanic (AMO-D033).

**Recovery is not the top of the model.** The positive side of Fit has at least two distinct uses (AMO-D054):

1. **restoring** condition — returning a stressed individual toward its healthy baseline;
2. **supporting continued life and development** once recovery is complete — growth, size, structure, seasonal cycles, and eventual readiness for flowering and reproduction through systems that do not exist yet. Concretely, it has two sinks that do not saturate at "healthy": **reserves** and **developmental state** (AMO-D056, AMO-D057).

These must not be conflated. An individual that has finished recovering has not exhausted what a good environment can do for it; output D does not fall to zero when condition returns to baseline, it changes what it is spent on. This is what makes **strategic establishment** worth doing rather than merely safe (AMO-D054, [09_EMBODIMENT_AND_ASTRAL_TRANSFER.md](09_EMBODIMENT_AND_ASTRAL_TRANSFER.md)).

## 12. Limiting factors and interactions

**Limiting factors are a requirement, not an optimisation.** Naive averaging must not let catastrophic failure in one dimension disappear behind excellent values elsewhere:

```
temperature excellent · water catastrophic · light excellent · humidity excellent
                    ↛  overall: good
```

A plant with no usable water does not care how good the light is. Fit must eventually support limiting-factor behaviour, and output E exists to surface it. The aggregation rule is not defined here (AMO-Q070).

**Interactions are real, and their ownership is settled** (AMO-D055). Two dimensions that are each individually tolerable can jointly produce a materially worse outcome — demonstrated in [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md) §17. What v0 does not yet do is *represent* them; the dimensions are treated independently for now, and the mathematics remains open (AMO-Q071).

Where an interaction belongs is decided by one question:

> Could the World compute this interaction **without knowing what organism is present**?

| | Mechanism | Owner |
|---|---|---|
| **World-side** | one environmental condition physically changes another — heat increases evaporation, so root-zone water falls | **World**: it produces a different Local Environment State, and Fit simply evaluates the resulting values |
| **Fit-side** | the *combination* changes this individual's biological response while the World values stay exactly as they are | **Environmental Fit**: it is part of the biology (AMO-D036) |

> Does the environment change itself, or does the organism respond differently to the same environment?

**Avoiding double-counting.** Because both describe the same physical world from different sides, the same relationship can be applied twice — once in a World value already lowered by evaporation, and again in a Fit rule that penalises "hot and dry". The governing rule is *World computes environmental causation; Fit computes biological consequence*, enforced by two disciplines: every Fit-side interaction must be justifiable **with World values held fixed**, and **Fit must not compensate for a thin World**. A missing World process is a reason to extend World, not to approximate it inside Fit (AMO-D055).

## 13. Condition changes over time

Fit acts on the individual over time:

```
Condition(t + Δt) = Condition(t) + effects of Fit during Δt
```

This is a shape, not an equation. No equation, tick rate or simulation frequency is defined (AMO-Q074).

What it supports is the full range: slow recovery, gradual stress, rapid collapse and long-term healthy growth.

Fit changes **biological condition**. It never changes identity or genetics (AMO-D012, AMO-D039). Which condition variables actually exist — health, stress load, development state, stored resources, or a different set — is open, and should be settled by what the Fit boundary genuinely requires rather than by physiological ambition (AMO-Q073).

The condition variables are specified in [14_CURRENT_BIOLOGICAL_CONDITION_V0.md](14_CURRENT_BIOLOGICAL_CONDITION_V0.md): **vitality**, **stress load** and **reserves**, with **developmental state** as a separate axis beside them (AMO-D056, AMO-D057).

Written with time made explicit, the loop is:

```
CONDITION(t) + DEVELOPMENTAL STATE(t) + traits + species baseline
        →  effective response profile
        +  LOCAL ENVIRONMENT(t)
        →  FIT over Δt
        →  CONDITION(t + Δt)
```

**Condition sits on both sides of Fit, deliberately.** It is one of the three layers forming the effective response profile (§8) *and* it is what Fit modifies over time. That feedback is intended, not an inconsistency: a weakened individual tolerates less, so the same environment presses harder on it, so it weakens faster — and the same loop run forward is why recovery firms up as it proceeds. It is also why two individuals of identical species and traits can meet the same conditions and have entirely different outcomes, and therefore why no fixed rescue timer could ever be correct (AMO-D034). Read across time — condition at `t`, effects over `Δt`, condition at `t + Δt` — it is a feedback loop, not a circular definition.

## 14. Rooting, rescue windows and inhabitability

### Rooting is environmentally neutral as an action, and often deliberate

Rooting adds no automatic penalty, stress rate or countdown (AMO-D033). Once rooted:

```
LOCAL WORLD ENVIRONMENT + AMORPHO RESPONSE PROFILE
                 ▼
         ENVIRONMENTAL FIT
                 ▼
       BIOLOGICAL TRAJECTORY        (positive, neutral or negative)
```

> **Rooting does not start a countdown. It starts an environmental relationship.**

That relationship may well be the point of the journey. Rooting is not primarily an emergency mechanic: a player may travel specifically in order to establish an individual somewhere favourable, and in a good environment it may then live, grow and develop there indefinitely while the player is elsewhere (AMO-D054).

### The rescue window is an emergent consequence

There is no separate rescue-timer system anywhere in Amorpho (AMO-D034). A rescue window exists only when Fit is negative, condition is deteriorating, and the individual remains inhabitable for some part of that decline:

```
poor Fit → accumulated stress → condition declines
        → inhabitability threshold crossed
        → astral re-entry no longer possible
        → physical rescue becomes necessary
```

If Fit is stable or positive there may be **no rescue window at all**, and the individual may stay inhabitable indefinitely. See [09_EMBODIMENT_AND_ASTRAL_TRANSFER.md](09_EMBODIMENT_AND_ASTRAL_TRANSFER.md).

### Inhabitability is downstream of biology

Neither the World nor geography may set `inhabitable = false` directly (AMO-D050):

```
World environment + Amorpho → Fit → current biological condition → inhabitability
```

This is what lets one location affect different species differently, different individuals differently, and the same individual differently over time. A place is never inherently un-inhabitable; a plant's condition is. Where the threshold sits, and how it relates to health, remains open (AMO-Q042).

## 15. Controlled environments, pots and root zones

A greenhouse never says `this Amorpho is safe`. It changes the local environment — temperature, humidity, water availability, light, exposure — and the individual then undergoes the **same** Fit evaluation (AMO-D035). The same applies to houses, rooms, protected growing spaces and future climate-controlled facilities. This is why no special-case rule such as `greenhouse makes tropical plant valid` is ever needed (AMO-Q049).

A pot is eventually a highly local growing environment rather than only an inventory item: root volume, water state, drainage, substrate and root-zone temperature may all matter. Pot size is already an established gameplay concept (AMO-D014). **v0 adds none of these dimensions.** It records that container and root-zone modelling will later extend the Local Environment State, entering at the lowest level of the hierarchy in §6 (AMO-Q050).

## 16. Two evaluation contexts

Rooted survival and animated traversal must not be confused (AMO-D032, AMO-Q051):

| Context | Status |
|---|---|
| **Rooted biological Fit** | the model specified in this document |
| **Animated environmental response** | a future model using the same World Environment plus animated-state protections and modifiers |

An inhabited Amorpho may eventually use clothing, armour or environmental equipment that modifies the effective environment its animated body experiences. When it roots, that protection does not become plant protection. The animated model is **not** defined here; v0 only reserves the second context so it cannot later be bolted onto the rooted one.

## 17. The Evolutionator stays downstream

Fit may influence survival, growth, health, reproductive readiness and reproductive success. Over generations those effects create selection.

Fit does **not** rewrite genetic traits, decide adaptations, or know any geographic evolutionary goal (AMO-D038, AMO-D039):

```
World → environment · Amorpho → biological response · Fit → performance
                    Evolutionator → inheritance and variation across offspring
```

Selection emerges from differential performance. Nothing commands it.

## 18. Positive Fit is strategic opportunity

Because Fit ranges into the positive, players should eventually be able to discover or create locations that are unusually favourable for particular Amorphos. That can motivate outdoor establishment, property acquisition, greenhouse investment, social cooperation, regional specialisation, breeding projects and long-term lineages.

None of those systems is designed here. What v0 records is that a good environment is an **opportunity to pursue**, not merely a punishment avoided — which is what makes the cultivation layer worth playing rather than worth surviving.

## 19. Conditions, not permissions

The World never prevents a player from taking an Amorpho somewhere unsuitable (L39, AMO-D051).

> The World does not say *"you cannot bring this Amorpho here."* It says *"these are the conditions here."*

The player decides whether the risk is acceptable, and the consequences emerge through Fit. A model that blocks movement would replace a judgement with a rule, and would destroy exactly the decisions the environmental system exists to create.

### Simulation truth versus player knowledge

These are separate, and v0 keeps them separate:

| | |
|---|---|
| **Simulation truth** | what conditions and Fit actually are |
| **Player knowledge** | what the player knows or can predict |

Players may eventually have forecasts, sensors, cultivation knowledge, equipment, warnings or uncertain predictions. No UI or information model is decided (AMO-Q044).

In particular, nothing assumes the player is shown an exact figure such as `12 minutes 43 seconds until non-inhabitable`. The simulation may produce a trajectory without exposing certainty about it. How much is revealed is an unresolved gameplay decision that matters for risk and exploration.

## 20. Deterministic core, explicit randomness

Given identical World state and identical Amorpho state, Fit itself produces the same result (AMO-D052).

Randomness belongs to systems where it means something — weather, individual biological variation, stochastic events, pests, future disease, other World events — and those sit **upstream** of Fit, in the state it evaluates. Arbitrary rolls hidden inside the evaluator would make outcomes unexplainable to players and untestable for the project, while adding nothing that upstream randomness cannot express.

This is a conservative v0 position, not a claim that biology is deterministic (AMO-Q075).

## 21. Extension points

Each of these can be added later **without moving the boundary**:

| Extension | Enters at |
|---|---|
| more environmental dimensions | World Environment Vector (§3) |
| decomposing exposure / protection | World Environment Vector (§3) |
| rainfall, irrigation, drainage, evaporation | derivation of water availability (§3) |
| light sources: sun angle, cloud, canopy, artificial | derivation of light availability (§3) |
| buildings, greenhouses, climate control | local modifiers (§6, §15) |
| containers, substrate, root zones | lowest hierarchy level (§6, §15) |
| exposure-history and accumulation models | between environment and Fit (§7) |
| response curves replacing zones | Amorpho response profile (§8) |
| acclimation | current-condition layer (§8) |
| aggregation rules and limiting-factor behaviour | Fit internals (§12) |
| factor interactions | Fit internals (§12) |
| condition variables and their dynamics | condition over time (§13) |
| animated-state environmental response | second evaluation context (§16) |
| approved species response data | Reality Gate, after this model exists (AMO-D053) |

## 22. The smallest spike that would validate v0

**Not to be built now.** Recorded so the eventual Phase 2/3 experiment stays small (see [07_INCUBATION_ROADMAP.md](07_INCUBATION_ROADMAP.md)).

The three cases have already been walked through on paper in [13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md](13_ENVIRONMENT_FIT_WORKED_SCENARIOS_V0.md), which is what a spike would have to reproduce.

It needs only: one abstract location · one Local Environment State · one abstract Amorpho profile · one current condition · time progression · Fit evaluation — and it should demonstrate three cases:

1. **deterioration** — negative Fit drives condition down, eventually past inhabitability;
2. **equilibrium** — adequate Fit holds condition stable indefinitely;
3. **improvement / recovery** — excellent Fit raises a damaged individual back up.

No real species, no graphics, no world map, no engine. If those three cases cannot be produced from this contract, v0 is wrong and should be revised through the ledger rather than worked around.

## 23. Open questions

Value representation, units and continuous-versus-tiered (AMO-Q069) · Fit aggregation and limiting factors (AMO-Q070) · factor interactions (AMO-Q071) · exposure history (AMO-Q072) · current-condition variables (AMO-Q073) · simulation time step (AMO-Q074) · where randomness lives (AMO-Q075) · approved input for response profiles (AMO-Q076).

Related earlier questions: the environmental model generally (AMO-Q005), plant simulation depth and acclimation (AMO-Q012), inhabitability threshold (AMO-Q042), prognosis and forecasting (AMO-Q044), recovery and core damage (AMO-Q045), controlled environments (AMO-Q049), substrate and root zone (AMO-Q050), the three tolerance concepts (AMO-Q051), environmental nesting (AMO-Q065). See [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).
