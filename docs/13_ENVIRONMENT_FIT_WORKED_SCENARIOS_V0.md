# 13 — Environmental Fit v0: Worked Scenarios

**Status:** validation exercise. This document stress-tests the contract in [12_ENVIRONMENT_AND_FIT_MODEL_V0.md](12_ENVIRONMENT_AND_FIT_MODEL_V0.md) against worked cases. That document governs; this one only tests it. Nothing here adds to the model.

**Part I (§1–§11)** tests the contract against a deteriorating, a stable and a recovering case. **Part II (§14–§22)** adds Scenario D, which tests cross-dimension interaction and the World/Fit ownership boundary (AMO-Q071, AMO-D055).

> ⚠️ **All values in this document are synthetic.** They are invented for a paper exercise. They are **not** biological measurements, **not** facts about any real *Amorphophallus* species, and **not** a proposed runtime representation. The individuals are generic test subjects — *Test Amorpho A*, *B*, *C*, *D* — and are deliberately not real species. No value here may ever be copied into `data/`, quoted as a tolerance, or treated as approved input (AMO-D024, AMO-D025, L4).

## 1. The testing scale

For this exercise only, each dimension uses an abstract **0.0 – 1.0** scale. For temperature, water availability, light availability and air moisture, `0.0` is the bottom of the modelled band and `1.0` the top. For exposure / protection, `0.0` is fully exposed and `1.0` fully sheltered.

This scale is a **paper tool**. It is not recorded as a decision, and value representation remains entirely open (AMO-Q069). It exists so the reasoning below can be explicit rather than hand-waved.

Fit by dimension is described in words — *favourable*, *shortfall*, *critical* — rather than scored, because the aggregation rule does not exist yet (AMO-Q070).

## 2. What this pass was asked to find out

> Does the v0 contract actually describe believable positive, neutral and negative cases without hidden assumptions?

Specifically: whether limiting factors work, whether current condition matters, whether rescue windows emerge rather than being invented, whether air moisture and water availability earn separate existence, whether water availability beats rainfall as the input, and whether exposure / protection survives contact with examples.

---

## 3. Scenario A — Deteriorating

*Test Amorpho A, rooted at fictional Site A-1 after an animated journey. Emergency rooting: the player had to stop here.*

### World environment (Site A-1, at this time)

| Dimension | Value | |
|---|---|---|
| Temperature | 0.58 | comfortable |
| Water availability | **0.07** | root zone effectively dry |
| Light availability | 0.72 | good |
| Air moisture | **0.74** | humid air |
| Exposure / protection | 0.62 | reasonably sheltered |

Note the pairing deliberately chosen here: **humid air over a dry root zone.**

### Response profile — Test Amorpho A

| Dimension | Preferred | Tolerable | Critical beyond |
|---|---|---|---|
| Temperature | 0.45 – 0.70 | 0.30 – 0.80 | < 0.18 or > 0.88 |
| Water availability | 0.45 – 0.75 | 0.25 – 0.85 | **< 0.15** or > 0.95 |
| Light availability | 0.50 – 0.85 | 0.30 – 0.95 | < 0.10 |
| Air moisture | 0.55 – 0.85 | 0.35 – 0.95 | < 0.20 |
| Exposure / protection | 0.50 – 1.00 | 0.30 – 1.00 | < 0.10 |

### Current condition before exposure

Healthy. The individual was animated, travelled, and rooted in good order: health high, stress load low, stored resources moderate. This matters enormously, and §3.9 shows why.

### Fit by dimension

| Dimension | Position | Fit |
|---|---|---|
| Temperature | inside preferred | favourable |
| **Water availability** | **0.07, below the 0.15 critical boundary** | **critical** |
| Light availability | inside preferred | favourable |
| Air moisture | inside preferred | favourable |
| Exposure / protection | inside preferred | favourable |

### Critical constraint

**Water availability, alone.** Four of five dimensions are favourable and one is past its critical boundary.

### Biological direction

**Deteriorating.**

### Stress pressure

High, and **concentrated rather than diffuse**. This is not an individual mildly uncomfortable on several fronts; it is one on which a single dimension has failed outright. The distinction matters for what a player should be told and for how fast the trajectory runs.

### Growth / recovery opportunity

**Effectively nil** — and the reason is the interesting part. Warmth, light and humidity are all favourable, but they cannot be *used*. A plant with no usable water cannot convert good light into growth.

This surfaced something the spec did not say explicitly: **output D is gated by limiting factors just as the aggregate is.** It is not the average of the favourable dimensions, and it is not independent of output E.

### Short-term trajectory if exposure continues

Stored resources deplete, stress load accumulates, health declines. The rate is set by how far below the critical boundary the value sits and by the individual's condition — not by any constant. No survival time is assigned here, and none exists in the model (AMO-D034).

### Inhabitability

Initially **yes**. Condition is good, and inhabitability is computed from condition, not from the place (AMO-D050). The site is hostile, but the plant standing in it is not yet compromised.

As condition declines it eventually crosses the inhabitability threshold, and astral rescue stops being possible while the plant is still alive. Physical rescue becomes the only route (AMO-D031). The **rescue window is exactly this interval** — it exists only because the trajectory is negative, and nothing generated it but the trajectory itself.

### 3.8 — Why simple averaging would be dangerous

Suppose each dimension were crudely scored and the results averaged. Giving *favourable* ≈ 0.85 and *critical* ≈ 0.05:

```
(0.85 + 0.05 + 0.85 + 0.85 + 0.85) / 5  =  0.69   →  reads as "favourable"
```

The individual is dying of thirst and the model says it is doing well. Four comfortable dimensions have hidden one fatal one.

This is the requirement in AMO-D049 demonstrated rather than asserted: aggregation must let a single critical dimension dominate. It does **not** tell us which rule to use — a minimum, a weighted minimum, a product, a soft floor and others all satisfy it (AMO-Q070).

### 3.9 — Why current condition cannot be ignored

Run the same Site A-1 against a second individual of identical species baseline and traits, but arriving **already stressed** — depleted resources, elevated stress load, reduced health.

Because current condition is one of the three layers forming the effective response profile (AMO-D048), the stressed individual's usable bands are narrower. Its effective critical boundary for water sits higher than 0.15, so the same environmental value of 0.07 sits *further* outside it. The result:

| | Healthy arrival | Stressed arrival |
|---|---|---|
| Fit: water | critical | critical, by a wider margin |
| Stress pressure | high | higher |
| Starting condition | good | already low |
| Inhabitable on arrival | yes | possibly not |
| Rescue window | exists, and is real | short, or already closed |

Same place. Same time. Same species. Two different stories.

This is precisely why no fixed rescue timer could ever be correct (AMO-D034), and it confirms that condition genuinely participates rather than decorating the model.

---

## 4. Scenario B — Stable equilibrium

*Test Amorpho B, in a pot in a room of a house in a temperate city, during the local dry season. Operational rooting: the player is keeping it here for now.*

### World environment (Site B-1, indoors, at this time)

| Dimension | Value | |
|---|---|---|
| Temperature | 0.40 | cool for this individual |
| Water availability | 0.52 | adequately moist substrate |
| Light availability | 0.33 | dim indoor position |
| Air moisture | 0.44 | dry indoor air |
| Exposure / protection | 0.72 | well sheltered |

The **outdoor** environment at this same geographic position would be harsher and drier. The building modified it into the values above — no special rule, just a local modifier producing the same five dimensions (AMO-D046, AMO-D035).

### Response profile — Test Amorpho B

| Dimension | Preferred | Tolerable | Critical beyond |
|---|---|---|---|
| Temperature | 0.45 – 0.72 | 0.32 – 0.82 | < 0.20 |
| Water availability | 0.40 – 0.70 | 0.22 – 0.82 | < 0.12 |
| Light availability | 0.45 – 0.80 | 0.25 – 0.92 | < 0.08 |
| Air moisture | 0.50 – 0.80 | 0.30 – 0.92 | < 0.15 |
| Exposure / protection | 0.45 – 1.00 | 0.25 – 1.00 | < 0.08 |

### Current condition

Healthy and unremarkable. No accumulated stress, no depletion, no recent disturbance.

### Fit by dimension

| Dimension | Position | Fit |
|---|---|---|
| Temperature | 0.40 — tolerable, below preferred | mild shortfall |
| Water availability | inside preferred | favourable |
| Light availability | 0.33 — tolerable, below preferred | mild shortfall |
| Air moisture | 0.44 — tolerable, just below preferred | slight shortfall |
| Exposure / protection | inside preferred | favourable |

### Critical constraint

**None.** Three dimensions sit in tolerable rather than preferred; none is past a critical boundary.

### Biological direction

**Stable.**

### Stress pressure

Low, **diffuse and chronic** — the opposite shape to Scenario A. Three small shortfalls, none individually threatening, which an otherwise healthy individual absorbs indefinitely.

### Growth / recovery opportunity

**Modest — neither zero nor maximal.** There is nothing to recover from, and the shortfalls, led by light, hold development well below what this individual is capable of. It persists. It does not flourish.

### Short-term trajectory

Essentially flat. Condition holds. Development continues slowly. Nothing is accumulating toward failure, and nothing is accumulating toward much else either.

### Inhabitability

Yes, and stably so. There is **no rescue window here at all**, because there is no negative trajectory to produce one. A plant can stay in a place like this indefinitely.

### 4.8 — Why "water availability" beats "rainfall"

Site B-1 is in a dry season. **Rainfall is effectively zero.** Water availability is 0.52, because the pot is watered indoors.

Had the dimension been named *rainfall*, this individual would read as being in severe drought while in fact being perfectly comfortable — and the model would have needed a special case for "but it is indoors and watered" to correct itself. Naming the thing the plant actually experiences removes that need entirely: irrigation, substrate, drainage and container state can all be added later as things that *produce* the value, with no change to what Fit consumes (AMO-D047).

The abstraction is validated.

### 4.9 — Stable is not thriving

Scenario B is the case L38 exists to protect. Nothing is wrong. The individual is healthy, safe and inhabitable, and a player checking on it would find no problem to solve.

It is also a poor place to raise anything. A player intending strategic establishment — growth, development, eventual reproduction — should look elsewhere, and the model must be able to tell them so without any dimension being in trouble. It can: the direction is stable but the growth / recovery opportunity is modest, and that pairing *is* the signal.

---

## 5. Scenario C — Recovery, then thriving

*Test Amorpho C, retrieved from a site much like A-1 and carried to fictional Site C-1. **Strategic establishment**: the player travelled here deliberately in order to put this individual here (AMO-D054).*

### World environment (Site C-1, at this time)

| Dimension | Value | |
|---|---|---|
| Temperature | 0.57 | comfortable |
| Water availability | 0.63 | good |
| Light availability | 0.69 | good |
| Air moisture | 0.71 | good |
| Exposure / protection | 0.80 | well sheltered |

### Response profile — Test Amorpho C

| Dimension | Preferred | Tolerable | Critical beyond |
|---|---|---|---|
| Temperature | 0.45 – 0.72 | 0.30 – 0.82 | < 0.18 |
| Water availability | 0.45 – 0.75 | 0.25 – 0.85 | < 0.15 |
| Light availability | 0.50 – 0.85 | 0.30 – 0.95 | < 0.10 |
| Air moisture | 0.55 – 0.85 | 0.35 – 0.95 | < 0.20 |
| Exposure / protection | 0.50 – 1.00 | 0.30 – 1.00 | < 0.10 |

Every World value sits inside the preferred band, several near its centre.

### Current condition on arrival

**Mildly stressed.** Health reduced, stress load elevated, stored resources depleted after the earlier episode. Not critical; not healthy.

### Fit by dimension

All five: **favourable**, with none near a boundary.

### Critical constraint

**None.**

### Biological direction

**Improving.**

### Stress pressure

Near zero. Conditions are not merely failing to impose stress — there is nothing here working against the individual at all.

### Growth / recovery opportunity

**High**, and this is where the two-phase behaviour matters.

**Phase 1 — restoring.** The opportunity is spent returning the individual toward its baseline: stress load falls, resources rebuild, health recovers. The feedback noted in §3.9 now runs *forward* — as condition improves, the effective bands widen, the same environment sits even more comfortably inside preferred, and recovery firms up before levelling off as there is less left to restore.

**Phase 2 — thriving.** Condition reaches healthy baseline. Recovery is complete — and the opportunity **does not fall to zero**. It changes what it is spent on: size, structure, seasonal development, and eventually readiness to flower and reproduce through systems that do not exist yet (AMO-D054, AMO-Q077, AMO-Q079).

This is the case the model most needed to prove, because it is the reason to seek good places out. An environment whose best offer was "you stop being damaged" would make strategic establishment pointless.

### Inhabitability

Yes throughout, and increasingly securely. There is no rescue window, and none should exist.

### 5.8 — The ambiguity this scenario exposed

In phase 2, condition is no longer climbing — it is at baseline and holding. Read naively, output **B** would then say *stable*, which is exactly what Scenario B says about a dim, cool room where nothing much happens.

Those two situations are not remotely the same, and collapsing them would destroy the distinction L38 exists to protect.

The contract already separates them, via output **D**:

| | Direction (B) | Opportunity (D) |
|---|---|---|
| Scenario B — persisting | stable | modest |
| Scenario C phase 2 — thriving | stable | high |

So no new output is needed. What *is* needed is for the spec to say plainly that **B describes the condition trajectory** and must be read together with D — otherwise a consumer reading B alone would treat a thriving mature plant and a barely-ticking-over one as equivalent. That clarification has been made in [12](12_ENVIRONMENT_AND_FIT_MODEL_V0.md) §9.

---

## 6. Exposure / protection assessment

The brief asked specifically whether this dimension survives contact with examples. Honestly: **it did not do any work in any of the three scenarios.**

| Scenario | Value | Did it change the outcome? |
|---|---|---|
| A | 0.62 | No. Favourable and irrelevant; water decided everything. |
| B | 0.72 | Partly — it carried "indoors is sheltered", but temperature already carried that. |
| C | 0.80 | No. Favourable and inert. |

It was never the constraint, never the explanation, and never distinguished two otherwise identical cases.

The reason is diagnostic rather than damning. All three scenarios are **sustained conditions** — states the individual continuously experiences. Exposure / protection is reaching toward something structurally different: **vulnerability to discrete events** that have not been modelled. A storm, a frost night, wind damage, an animal, a person finding the plant. Against a steady background it has nothing to modify.

That also explains its known risk of becoming a miscellaneous bucket: a dimension with no clear job attracts one.

### Assessment: **retain, clarify scope, keep explicitly provisional.**

- **Retain.** Three scenarios that fail to exercise something are weak grounds for deleting it, and the situations where it would matter are ones v0 deliberately does not model.
- **Clarify scope.** It describes *vulnerability to environmental forces and events*, not a continuously experienced condition like the other four. It is not simply a fifth comfort axis.
- **Keep provisional.** Its real test comes only when acute events exist (AMO-Q020). Until then it cannot be validated, and the honest position is that it is unproven rather than confirmed.

No decision is made and no dimension is removed; the evidence is recorded against AMO-Q069.

---

## 7. Air moisture versus water availability

The two scenarios were built to test this from opposite directions:

| | Air moisture | Water availability | Situation |
|---|---|---|---|
| **A** | 0.74 — comfortable | 0.07 — critical | humid air, dead-dry root zone |
| **B** | 0.44 — slight shortfall | 0.52 — favourable | dry air, comfortably moist root zone |

**Scenario A cannot be expressed at all by a merged dimension.** Any single "moisture" value would have to be either high — losing the fatal constraint entirely — or low, wrongly implying the air was also a problem. The individual dies of one while the other is fine, and that is the whole scenario.

Scenario B is the mirror case and is equally inexpressible merged.

The separation is **validated decisively** — more strongly than any other element of the vector.

---

## 8. Structural gaps revealed

Where the contract forced something into the wrong place, or left a term doing undefined work.

### 8.1 Condition is both an input to Fit and the thing Fit changes
Current condition forms part of the effective response profile (AMO-D048) **and** is what accumulates over time (§13 of the spec). That is a feedback loop, and it is desirable — it is what makes collapse accelerate in Scenario A and recovery firm up in Scenario C. But the spec never said so, and a reader could reasonably have assumed condition sat on only one side.
**Deferrable?** No — it is a language gap, not a model gap. **Clarified in [12](12_ENVIRONMENT_AND_FIT_MODEL_V0.md) §13.** No new question.

### 8.2 Output B was ambiguous between condition trajectory and overall trajectory
See §5.8. Resolved by definition, not by adding an output.
**Deferrable?** No. **Clarified in [12](12_ENVIRONMENT_AND_FIT_MODEL_V0.md) §9.** No new question.

### 8.3 Output D is gated by limiting factors, not only the aggregate
Scenario A has four favourable dimensions and zero usable opportunity. The spec presented E as protecting the aggregate; the exercise shows it must also protect D.
**Deferrable?** No. **Clarified in [12](12_ENVIRONMENT_AND_FIT_MODEL_V0.md) §9.** Feeds AMO-Q070.

### 8.4 Stress pressure needed to be a rate, not a total
Scenario A's trajectory only makes sense if C is a *pressure per unit time* and the accumulated total lives in condition. The spec did not distinguish them.
**Deferrable?** No. **Clarified in [12](12_ENVIRONMENT_AND_FIT_MODEL_V0.md) §9.** Feeds AMO-Q072.

### 8.5 Acute events have no home
Nothing in the vector expresses a discrete damaging occurrence. Exposure / protection gestures at it without being able to act on it (§6).
**Deferrable?** **Yes.** v0 is a model of sustained conditions and said so. Recorded against the existing pests, pathogens and weather-events question (AMO-Q020) rather than a new one, and against AMO-Q069.

### 8.6 Container volume could not be represented
In Scenario B, "healthy but developing slowly" could be caused by the dim light *or* by an undersized pot — and pot size is an established constraint on development (AMO-D014). The contract cannot currently tell those apart.
**Deferrable?** **Yes**, but it is the strongest candidate for the first extension. Recorded against AMO-Q050. **No sixth dimension is proposed**; it likely belongs in the root-zone layer of the local environment.

### 8.7 Root-zone temperature is not ambient temperature
A dry substrate in strong light can be far hotter than the air around it. Visible in Scenario A, though not needed to make it work, since water had already decided the outcome.
**Deferrable?** **Yes.** Recorded against AMO-Q050. No new dimension.

### 8.8 Nutrients were never needed
Across three scenarios spanning failure, equilibrium and flourishing, nutrient status never had to be smuggled anywhere. This is a **positive** finding: the deferral in AMO-D047 was correct, and nothing forced it back in.

---

## 9. What v0 already handles

Claimed only where a scenario actually demonstrated it.

| Capability | Where |
|---|---|
| A harmful environment producing genuine deterioration | A |
| Limiting-factor dominance, with the averaging failure shown concretely | A §3.8 |
| Current condition materially changing the outcome of identical conditions | A §3.9 |
| Rescue window emerging from trajectory, never from a timer | A |
| Inhabitability derived from condition, not from place | A, C |
| A stable environment that is honestly mediocre | B |
| Stable distinguished from thriving without any dimension being in trouble | B §4.9, C §5.8 |
| Controlled local environment modifying World state with no special rule | B |
| Water availability outperforming rainfall as the input | B §4.8 |
| Air moisture and water availability as genuinely independent | A + B §7 |
| Recovery from a stressed starting condition | C phase 1 |
| Continued development *after* recovery completes | C phase 2 |
| Rooting as a deliberate destination rather than an emergency | C |
| Deterioration, equilibrium and improvement all expressible in one contract | A, B, C |

## 10. What v0 does not yet solve

None of these are defects; each was deliberately deferred.

Value representation and units (AMO-Q069) · the aggregation formula (AMO-Q070) · interactions between dimensions — untested here, since no scenario needed two dimensions to combine (AMO-Q071) · exposure-history mathematics (AMO-Q072) · the actual set of condition variables, though the exercise showed **stress load**, **stored resources** and **health** all doing real work (AMO-Q073) · time step and rates (AMO-Q074) · where randomness lives — deliberately absent from all three scenarios (AMO-Q075) · acute events (AMO-Q020) · container and root zone (AMO-Q050) · acclimation (AMO-Q012) · irreversible damage (AMO-Q045) · any real species data (AMO-D053, AMO-Q076).

## 11. Verdict

**The five-dimension Environment Vector survived intact.** No dimension was removed, none was added, and nothing had to be smuggled into the wrong field to make the three cases work.

The contract produced deterioration, equilibrium and improvement without special cases, and the two elements most at risk of being wrong — the separation of air moisture from water availability, and the insistence on limiting factors — both proved necessary rather than merely defensible.

Four clarifications were folded back into the specification, all of them about naming what the model was already doing. One dimension, exposure / protection, remains unproven rather than validated.

The model was made to survive three examples before being made more complicated. It did.

---

# Part II — Scenario D: cross-dimension interaction

Added 2026-09-21 to test AMO-Q071, the one part of the v0 contract the first three scenarios left completely untested. The same warning applies to everything below: **all values are synthetic**, *Test Amorpho D* is a generic test subject and not a real species, and nothing here is importable.

## 14. What this scenario has to provoke

Scenarios A–C each had an outcome explicable from a single dimension. This one must produce a case where **two individually tolerable dimensions jointly change the biological outcome** — because if that can happen, treating dimensions independently is insufficient, and the model has to say where the interaction lives.

The architectural question is the real subject:

> If two World conditions interact biologically, does that interaction belong to World or to Environmental Fit?

## 15. Response profile — Test Amorpho D

| Dimension | Preferred | Tolerable | Critical beyond |
|---|---|---|---|
| Temperature | 0.40 – 0.62 | 0.25 – 0.78 | < 0.15 or > 0.88 |
| Water availability | 0.45 – 0.75 | 0.28 – 0.85 | < 0.16 |
| Light availability | 0.45 – 0.80 | 0.28 – 0.92 | < 0.10 |
| Air moisture | 0.50 – 0.82 | 0.32 – 0.92 | < 0.18 |
| Exposure / protection | 0.45 – 1.00 | 0.25 – 1.00 | < 0.08 |

## 16. Case D1 — moderate thermal condition

| Dimension | Value | Position | Independent fit |
|---|---|---|---|
| Temperature | 0.52 | inside preferred | favourable |
| **Water availability** | **0.33** | tolerable, below preferred | mild shortfall |
| Light availability | 0.60 | inside preferred | favourable |
| Air moisture | 0.62 | inside preferred | favourable |
| Exposure / protection | 0.70 | inside preferred | favourable |

**Critical constraint:** none. **Direction:** stable, very slightly negative. **Stress pressure:** low. **Opportunity:** modest — the water shortfall holds development back without threatening the individual.

A player finding this would see a plant that is a little dry and otherwise fine. That reading is correct.

## 17. Case D2 — higher thermal condition, water unchanged

| Dimension | Value | Position | Independent fit |
|---|---|---|---|
| **Temperature** | **0.74** | tolerable, below the 0.88 critical boundary | shortfall, not critical |
| **Water availability** | **0.33** | *unchanged*, tolerable | mild shortfall |
| Light availability | 0.60 | inside preferred | favourable |
| Air moisture | 0.62 | inside preferred | favourable |
| Exposure / protection | 0.70 | inside preferred | favourable |

**Only temperature changed, and it stayed inside its tolerable zone. No dimension is critical.**

### 17.1 The experimental control that makes this a clean test

Water availability reads **0.33 in both cases**, and this is deliberate. In D2 the World has already accounted for whatever evaporation the higher temperature causes — the site is being replenished, or the substrate holds water well enough — so 0.33 is the genuine, final root-zone value the individual experiences.

That control is the whole point. It removes the physical explanation, so anything left over must be biological.

### 17.2 The result

At 0.74, this individual's water demand is higher and its drought tolerance lower than at 0.52. The same 0.33 that was a manageable shortfall now leaves it in real deficit.

**Direction:** deteriorating. **Stress pressure:** moderate to high, and attributable to *neither dimension alone*. **Opportunity:** near nil. **Critical constraint:** the **temperature × water availability interaction** — even though neither dimension is individually critical.

Independent evaluation cannot produce this. Reading the five dimensions separately gives "one shortfall, one mild shortfall, three favourable" — which describes D1 about as well as D2, and describes the actual D2 outcome not at all.

**Interactions are therefore real and must be representable.** That much the scenario settles.

## 18. Where does the interaction belong?

Two different things could have produced a worse outcome at higher temperature, and separating them is the architectural finding.

### 18.1 The discriminating question

> Could the World compute this interaction **without knowing what organism is present**?

Applied to the two candidates:

| | Mechanism | Organism-dependent? | Owner |
|---|---|---|---|
| **Physical** | heat increases evaporation, so less water remains in the root zone | **No** — it happens to an empty pot | **World** |
| **Biological** | at higher temperature *this individual* needs more water and tolerates deficit less | **Yes** — another organism in the same conditions would respond differently | **Environmental Fit** |

The physical one changes **the environment**. The biological one changes **the response to the same environment**.

> Does the environment change itself, or does the organism respond differently to the same environment?

Scenario D was built to isolate the second: the World value did not move, and the outcome still got worse. That is only expressible as a Fit-side interaction.

### 18.2 World-side interactions

A World-side interaction produces a different Local Environment State. Heat raising evaporation and lowering water availability; a canopy lowering light; a building raising temperature and lowering exposure. Fit never sees the interaction at all — it sees the resulting values and evaluates them normally.

This is already how the model works (AMO-D046): every local modifier produces the same five dimensions, and Fit never learns about buildings. Evaporation is simply another modifier of that kind, whenever World grows enough to model it.

### 18.3 Fit-side interactions

A Fit-side interaction leaves the World values exactly as they are and changes what they *mean* for a particular individual. It is part of the biological response, so it belongs with the rest of the biology (AMO-D036) and is evaluated where biology meets conditions (AMO-D037).

Putting it in World would be a boundary violation with a concrete cost: the World would have to know which organism is standing there in order to report conditions, which is precisely what AMO-D035 forbids, and it would have to report different conditions for two plants in the same place.

### 18.4 The chain survives

```
EARTH / WORLD
      ▼  physical environmental processes  (World-side interactions)
FINAL LOCAL ENVIRONMENT STATE
      ▼
AMORPHO RESPONSE PROFILE
      ▼
ENVIRONMENTAL FIT
      ▼  biological cross-dimensional interactions  (Fit-side interactions)
CONDITION TRAJECTORY
```

Scenario D did not break it. Each interaction type has exactly one home, and the two are told apart by a question that can be asked of any candidate interaction.

## 19. Double-counting

The two interaction types describe the same physical world from different sides, so the same relationship can easily be applied twice.

Concretely: World lowers water availability from 0.40 to 0.33 because heat drove evaporation. Fit then *also* penalises the combination of high temperature and low water "because heat dries plants out". The heat's physical effect has now been counted once in the World value and again in the Fit rule, and the individual is punished twice for it.

The governing rule:

> **World computes environmental causation. Fit computes biological consequence.**

That formulation is correct but not, on its own, sufficient to catch the error — a Fit interaction term over temperature and water looks identical whether it encodes biology or silently re-encodes evaporation. Two working disciplines close the gap:

1. **Every Fit-side interaction must be justifiable with World values held fixed.** If the justification is "because the substrate dries out faster", it is describing a change in the World value and belongs in World. If it is "because this organism's water demand rises with temperature", the World value is unchanged and it belongs in Fit.
2. **Fit must not compensate for a thin World.** v0's World models no evaporation at all, which creates a standing temptation to approximate it inside Fit. That would be Fit quietly modelling physics, and it would become double-counting the moment World later gains the real mechanism. A missing World process is a reason to extend World, not to patch Fit.

## 20. What this means for the Fit outputs

### 20.1 Output A is *independent* dimension fit

In D2, output A reports temperature *tolerable* and water *tolerable*. Both are true. Neither explains the outcome.

Output A is a **diagnostic decomposition, not a complete explanation** — it answers "how does each dimension compare with the profile on its own", and by construction it cannot show anything that exists only in a combination. A consumer reading A alone would conclude that nothing is wrong.

No new output field is needed. What is needed is that A be *named* as independent fit, and that it be read with E — the same shape of rule as B-must-be-read-with-D from Scenario C §5.8.

### 20.2 Output E must be able to name an interaction

Output E was worded as "which **dimensions**, if any, are currently severe limiting factors". In D2 the severe limiting factor is not a dimension: it is the temperature × water pair.

Taken literally, E could not express the constraint that actually mattered. This is the one place Scenario D found the contract's wording genuinely too narrow.

The fix is a clarification rather than a new output: **E names constraints, and a constraint may be a single dimension or a named interaction between dimensions.** With that, §9's question is answered — yes, a critical constraint can arise from an interaction while no individual dimension is critical — and it stays answerable by the existing contract.

### 20.3 The outputs are a set, not five independent readings

Three separate clarifications have now each taken the form *"read X together with Y"*: B with D, A with E, and D gated by E. That is not a coincidence, and it is worth stating once in general rather than three times in particular: **no single Fit output is self-sufficient.** They are five views of one evaluation, and any consumer that acts on one in isolation will misread the situation.

## 21. Current condition under interaction

Applying D2 to an individual that arrives already stressed, rather than healthy:

Its effective bands are narrower (Scenario A §3.9), so temperature 0.74 may fall **outside** tolerable for it rather than inside, and the elevated water demand meets an individual with fewer stored resources. The interaction that is *significant stress* for a healthy individual becomes an *outright critical constraint* for a stressed one — possibly with the loss of inhabitability that D2 does not otherwise imply.

This is the established feedback loop (spec §13) operating through an interaction rather than a single dimension, which is what one would want. Condition remains relevant; nothing new is required to keep it so.

## 22. Assessment

| Question | Answer |
|---|---|
| **1. Does the five-dimension vector survive?** | **Yes, unchanged.** An interaction is a relationship *between* existing dimensions, not a new fact about the world, so no sixth dimension is implied — and none is proposed. |
| **2. Can interaction live cleanly inside Fit?** | **Yes.** Scenario D isolates a case expressible *only* as a Fit-side interaction, and the biology sits with the rest of the biology. |
| **3. Which interactions belong to World?** | Those that are **physical causation** — one environmental condition changing another, computable without knowing the organism. Heat driving evaporation is the canonical example. |
| **4. Is the boundary still clear?** | **Yes, and sharper.** The discriminating question (§18.1) can be applied to any candidate interaction and gives an unambiguous answer. |
| **5. Double-counting risk?** | **Real.** Named in §19, with two disciplines to prevent it. The one-line rule alone is not enough to catch it on inspection. |
| **6. Does Fit-by-dimension need clarification?** | **Yes.** Output A is independent fit and cannot express combinations; it must be read with E. |
| **7. Can a critical constraint arise from an interaction?** | **Yes**, once E is clarified to name constraints rather than only dimensions. This was the single genuinely too-narrow piece of wording. |
| **8. Does v0 require structural change?** | **No — clarification only.** Nothing was added, removed or restructured. |

### Verdict

The contract held. One scenario built specifically to break the independent-dimensions assumption did break it — as intended — and the model absorbed the result without gaining a field, a dimension or a formula.

The durable gain is a boundary that can be applied rather than merely stated: **the environment changing itself is World; the organism responding differently to the same environment is Fit** (AMO-D055). How interactions are represented, how many are worth modelling, how they are sourced and how they are explained to players all remain open (AMO-Q071).
