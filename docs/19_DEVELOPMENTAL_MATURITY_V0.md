# 19 — Developmental Maturity, v0

**Status:** specification, version 0. This document defines what Developmental Maturity is, how it grows, how it regresses, and how species biology interprets it. It defines no representation, no rates, no formulas, no thresholds and no species facts.

It completes the persistent-individual model alongside [14_CURRENT_BIOLOGICAL_CONDITION_V0.md](14_CURRENT_BIOLOGICAL_CONDITION_V0.md), [17_LIFE_CYCLE_STATE_MACHINE_V0.md](17_LIFE_CYCLE_STATE_MACHINE_V0.md) and [18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md).

> Condition says how the individual is doing. Life-cycle state says what phase it is in. Developmental Maturity says how far the persistent individual has developed.
> Healing restores integrity; growth restores development.

## 1. What it is

**Developmental Maturity is the individual's accumulated long-term biological development of its persistent organism across life cycles** (AMO-D080).

It exists to express something none of the other axes can: that two individuals of the same species may both be healthy, unstressed and in the same phase, and yet one has developed vastly further than the other.

It persists across leaf replacement, bloom ending, senescence, dormancy, new emergence, and astral entry and exit. It belongs to the **persistent individual** (AMO-D058).

## 2. What it is not

| | Answers | Maturity is not this because |
|---|---|---|
| **Life-cycle state** | *what phase is happening now?* | two individuals can both be in Active Leaf with wildly different maturity, and a deeply dormant individual may be highly mature (AMO-D057, AMO-D070) |
| **Vitality** | *how biologically intact is it?* | a large developed individual recovering from core damage has **high maturity, low vitality**; a small healthy one has **low maturity, full vitality** |
| **Stress load** | *what burden has accumulated?* | stress is reversible history over days and seasons; maturity is structural progress over years |
| **Reserves** | *what capacity is available now?* | a mature individual may temporarily run low on reserves; a small one may be relatively well provisioned |
| **Age** | *how long has it lived?* | time under poor conditions buys little development. **Age may correlate with maturity; it never defines it** — and chronological age is not a substitute for it |
| **Experience points** | *what has the player done?* | see §3 |

### It is emphatically not XP

> Developmental Maturity is biological development, not experience (AMO-D077, L47).

It must never increase because the player won a fight, completed a quest, earned account progress or spent points. Combat and missions may eventually change a plant's *circumstances* — where it is, what happens to it — but nothing awards biological maturity by fiat.

Maturity emerges from the biological life of the individual, which is also why it keeps accruing while the player is elsewhere (§10).

## 3. Representation: one slow continuous axis

v0 takes **one persistent, conceptually continuous developmental quantity per individual** (AMO-D080).

No numeric representation is chosen — not `0–100`, not levels, not stages. What matters is **continuity**, because four things depend on it:

- gradual growth, so a good season can be worth a little;
- gradual regression, so a setback can be worth a little or a great deal (§7);
- species-specific flowering thresholds sitting anywhere on the axis (§9);
- manifestation scaling that varies smoothly rather than in tiers (§9).

A player-facing interface may later show bands, categories or visual cues. The underlying concept must not require discrete levels to work (AMO-Q106, AMO-Q111).

## 4. Maturity is species-relative

A maturity value is **not** directly comparable between species (AMO-D080). It only has biological meaning interpreted through the species:

```
INDIVIDUAL DEVELOPMENTAL MATURITY  +  SPECIES DEVELOPMENT PROFILE
                        ▼
                biological expression
```

Possible future outputs include manifestation scale, Bloom eligibility, Bloom scale and development potential. No species profile schema is defined, and the species CSV is untouched (AMO-D053, AMO-Q076, AMO-Q110).

> Maturity is an individual developmental coordinate interpreted through species biology.

Nothing may ever assert a universal claim such as `maturity 80 means large` across species. Nor is maturity equated with any single physical measure — height, leaf span, tuber diameter or mass. Those may later be *derived* per species; maturity is the durable coordinate underneath, which is what stops one universal physical metric from failing across very different species (AMO-Q110).

## 5. How maturity grows

Maturity increases when the individual achieves **persistent net biological growth** (AMO-D081) — plausibly from favourable Environmental Fit, adequate reserves, healthy active phases, successful cultivation and productive cycles.

> Positive biological surplus may become persistent development.

No formula, rate or magnitude is defined (AMO-Q106).

### Environmental Fit never awards maturity directly

This is an ownership rule, not a stylistic preference. The wrong shape is `excellent Fit → +5 maturity`. The right shape is a chain (AMO-D081, AMO-D037):

```
ENVIRONMENTAL FIT      → biological opportunity and pressure
        ▼
CONDITION / RESERVES / growth processes
        ▼
persistent biological development
        ▼
DEVELOPMENTAL MATURITY increases
```

Fit describes what the environment offers; development processes convert sustained success into persistent growth. Short-circuiting the chain would make Fit an experience dispenser and break the boundary the whole environmental model rests on (AMO-D035–AMO-D037).

**Reserves are a plausible bridge** between favourable conditions and persistent development — but nothing defines `spend X reserves → gain Y maturity`. The rule is only that persistent development requires biological capacity, and reserves may be one relevant input (AMO-Q106).

### Growth need not wait for season boundaries

An individual may accumulate persistent development *during* a healthy active phase. A season-end or dormancy transition may be a convenient point to settle the books, but nothing requires it to be the only moment maturity can change. Update frequency is undefined (AMO-Q074, AMO-Q106).

### The long-term loop

```
healthy emergence → productive active period → sufficient reserves and favourable Fit
    → successful senescence → next cycle begins at higher maturity
```

## 6. How maturity regresses

Maturity regresses only when the persistent individual **loses meaningful long-term biological development** (AMO-D082). That requires **Core Impact**, not merely temporary manifestation impairment.

### Manifestation damage alone does not cost maturity

Below the Core-Impact Threshold, the leaf or bloom may be visibly damaged and the inhabited Amorpho substantially impaired, while biological productivity stays sufficient, persistent growth continues and **maturity does not regress** — and may still increase (AMO-D079).

**Nothing may map structural damage proportionally into maturity loss.** A regression rule that reads off a damaged-structure percentage is wrong by construction, because it would make every torn leaf cost years of development.

### Regression is a biological event, not a penalty

> Regression means the persistent organism is now developmentally smaller or less advanced than it was.

It is not punishment points, a debuff duration, reduced player progress or reduced magical capability. It has real future biological consequences — smaller manifestations, lost Bloom eligibility, a longer road back.

### Severity is continuous

A setback may cost negligible persistent development, modest regression, major regression, or catastrophic collapse. These are not runtime bands; the axis is continuous and so is the loss (AMO-D080).

### Premature retreat does not automatically regress maturity

Premature senescence may mean little or no expected growth, reserve expenditure and missed development — **without any persistent loss at all**. Some retreats merely stop growth and cost reserves. Regression still requires persistent biological loss (AMO-D082, AMO-Q087).

## 7. Lost opportunity is not regression

The distinction the whole regression rule depends on:

| | **Lost opportunity** | **Regression** |
|---|---|---|
| What happened | expected growth did not occur | persistent development actually decreased |
| Maturity | stays approximately where it was | falls |
| Feels like | a wasted year | a setback of years |

A bad season can be genuinely costly while maturity is unchanged — the cost is the growth that never happened, plus spent reserves and accumulated stress. Treating every bad season as regression would make the model punitive and would erase the difference between a disappointment and a disaster (AMO-D082).

## 8. Healing and regrowth are separate processes

Severe Core Impact may reduce **both** vitality and maturity, and they are different consequences:

| | Represents |
|---|---|
| **Vitality** | integrity and viability — *is this organism sound?* |
| **Maturity** | developmental scale and progress — *how far has it developed?* |

So an individual may be severely damaged but still large and developed; biologically recovered but developmentally reduced; or both compromised. These must never collapse into one number (AMO-D083).

### Vitality recovery does not restore maturity

> **Healing restores integrity; growth restores development** (L48, AMO-D083).

```
large mature individual → severe core damage → survives
    → vitality eventually fully recovers
    → persistent development remains much lower
    → further successful cycles are required to rebuild maturity
```

A fully healed individual can still be a fraction of what it was. This is the sharpest consequence in the harm model, and it is why a catastrophe costs *time* rather than costing the plant.

### Maturity is rebuilt biologically, and fully

Because all damage recovers while the individual lives (AMO-D075), lost maturity can be rebuilt — but **not because a timer expired**. It returns only through successful growth, favourable long-term conditions and biological redevelopment, which may take far longer than stress recovery (AMO-D083).

> While the individual survives, no former developmental level is permanently out of reach.

A severely regressed individual may eventually rebuild, regain its former flowering maturity, and exceed its previous development. The cost is time and successful biological life — which is precisely what strategic establishment provides (AMO-D054).

## 9. Maturity and Bloom

### The flowering threshold sits on this axis

Species may later supply a **flowering maturity threshold**. Bloom eligibility requires `developmental maturity ≥ that threshold` (AMO-D078). No value, format or species data is defined, and nothing is added to the species CSV (AMO-D053).

Crossing it is **biological, not a player unlock**: no skill point, no experience, no purchase. The individual's own development created the capability (L47).

Crossing it also **does not force Bloom** — eligibility may still depend on reserves, condition, life-cycle routing, environment and species biology. Maturity is necessary where it applies, never sufficient (AMO-Q107).

### Regression can remove eligibility, temporarily

An individual that falls below the threshold **loses** Bloom eligibility until maturity is rebuilt (AMO-D078, AMO-D082). Real long-term consequence, no permanent loss.

### The threshold is a milestone, not a maximum

First Bloom does not cap development. An individual keeps becoming larger, more mature and more developed across later successful cycles, so:

```
flowering threshold  =  a milestone on the maturity axis
                     ≠  the top of it
```

Later Blooms may therefore become larger, more developed and more visually impressive as maturity grows beyond the minimum. No scaling rule, linear relationship or combat bonus is defined (AMO-Q088).

### Compounding value

```
successful cycle → maturity gain → flowering threshold → first Bloom
    → further successful cycles → higher maturity → increasingly developed manifestations
```

This is intended, and it is the largest long-horizon reward cultivation offers.

### Maturity is not only about flowering

Higher maturity may later influence leaf manifestation scale, tuber and core scale, and other phases. The species profile interprets it; no effects are defined (AMO-Q110).

## 10. What maturity does *not* determine

### Not combat power

A biologically larger or more mature Amorpho is **not** automatically stronger in every fight, a higher tier, or unbeatable by a smaller individual. **No `maturity → attack power` rule exists or may be created.**

Maturity may influence physical manifestation and, through that, future phase-specific gameplay — but combat balance remains its own design problem, subject to skill staying central to outcomes (L1, L15, AMO-D006, AMO-D008, AMO-Q109).

Maturity is valuable without combat superiority: biological scale, Bloom eligibility, Bloom expression, long-term reproductive potential, individual history, collection value and strategic cultivation are all reasons to care. None of those requires it to win fights.

### Not affected by the human control layer

Astral Anchors have **no effect whatsoever** on maturity. Attaching one, removing one, trading the plant or releasing it leaves maturity untouched, because maturity belongs to the biological individual and anchoring is a human layer laid over it (AMO-D061, AMO-D064).

### Not dependent on the player being present

A rooted, uninhabited, even unbound individual may grow, regress, cross its flowering threshold, Bloom and reproduce. Development belongs to persistent biological simulation, not to attention (AMO-D009, AMO-D054).

The converse also holds: **an inhabited individual does not develop.** While astrally embodied its biological simulation is suspended, so no maturity accrues through growth (AMO-D084, [20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md](20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md)). Long embodiment therefore costs development the individual would otherwise have made — one of the opportunity costs that replaces a duration timer (AMO-D085).

### Not inherited

Maturity belongs to **one individual**; the Evolutionator works across generations on inherited traits (AMO-D038, AMO-D039). A mature parent does not produce developmentally mature offspring.

> Every new biological individual begins its own developmental history.

Parent maturity is never copied. Inherited traits may later influence how *readily* an offspring develops — that is the Evolutionator's business, not a transfer of accumulated development. No starting maturity is defined (AMO-Q106). **Do not confuse ontogeny with evolution.**

## 11. The boundary with AMO-Q108

These two questions are adjacent and were at risk of circling each other. The split is explicit:

| | Owns |
|---|---|
| **AMO-Q106** — this document | what maturity *is*, and what gain or loss *means* once persistent growth or loss has occurred |
| **AMO-Q108** | *when* biological harm crosses deeply enough into the persistent core to cause that loss |

This specification therefore uses **"Core Impact occurred"** as an abstract trigger and deliberately does not solve for it. Nothing here should be read as defining the Core-Impact Threshold (AMO-D079).

## 12. Worked cases

Non-numeric, species-neutral, no real biology.

| Case | What happens |
|---|---|
| **A — healthy growth** | productive active phase; stress low; reserves support development; **maturity increases** |
| **B — damage below Core Impact** | leaf visibly damaged and the playable form impaired; threshold not crossed; season still productive enough; **maturity does not regress and may still increase** |
| **C — poor season, no persistent loss** | premature retreat; expected growth lost; reserves lower; no persistent structural loss; **maturity approximately unchanged** — lost opportunity, not regression |
| **D — severe Core Impact** | persistent development lost; vitality compromised; **maturity regresses**; vitality later recovers faster than maturity is rebuilt |
| **E — Bloom maturity** | repeated successful cycles cross the species flowering threshold; Bloom becomes possible but not guaranteed; growth continues above it; later Blooms may be more developed |
| **F — catastrophic fragment survival** *(conditional)* | **if** identity continuity is later accepted (AMO-Q094), maturity may collapse enormously while the individual remains alive, with a long rebuild ahead. If the fragment is instead ruled a new individual, it begins its own developmental history under §10. Identity is unresolved today. |

## 13. Open questions

Internal representation, update mechanics, and rates of gain and regression (AMO-Q106) · species interpretation, manifestation scale and physical-size mapping (AMO-Q110) · player-facing presentation (AMO-Q111) · the Core-Impact Threshold (AMO-Q108) · Bloom eligibility inputs and timing (AMO-Q107) · Bloom manifestation scaling (AMO-Q088) · approved input for species thresholds (AMO-Q076) · fragment identity (AMO-Q094) · phase-specific gameplay impairment (AMO-Q109) · reproduction (AMO-Q079).
