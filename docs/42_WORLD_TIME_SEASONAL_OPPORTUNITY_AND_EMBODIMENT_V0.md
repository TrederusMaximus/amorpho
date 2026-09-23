# 42 — World Time, Seasonal Opportunity and Embodiment, v0

**Status:** correction and closure pass using owner-supplied design direction. It resolves an ambiguity [39](39_ACTIVE_LEAF_PRODUCTIVE_RETURN_AND_PERSISTENT_TUBER_BENEFIT_V0.md) deliberately left open, and adds the lifecycle boundary that closure requires. It defines no calendar, season, day count, growing period, rate, species lifecycle fact, hemisphere rule, travel mechanic, greenhouse hardware or lighting system, and it researches no phenology.

> **Embodiment freezes the plant, not the planet. The World offers opportunity; species biology shapes the strategy; the individual determines whether it can use it.**

## 1. Purpose

AMO-D136 established that ordinary Productive Return is suspended while an individual is inhabited, and left one thing open: what happens to *external* seasonal opportunity meanwhile. The owner's rule closes it — **suitable seasonal opportunity can pass while the Warden remains embodied** — and that closure immediately raises a second question, since a mobile Amorpho could otherwise chase favourable seasons indefinitely. So this pass also fixes where environmental opportunity ends and biological permission begins.

## 2. Two clocks

| | Owns | Behaviour during embodiment |
|---|---|---|
| **World Time** | day and night, weather, seasonal change, changing local conditions and local suitability (AMO-D009, AMO-D046) | **continues** |
| **Individual Biological Progression** | growth, rooted recovery, Active Leaf Productive Return, ordinary senescence, Programmed Tuber Draw, lifecycle progression | **may be suspended** (AMO-D084, AMO-D117, AMO-D136) |

They are not the same clock, and neither is derived from the other.

> **Embodiment freezes ordinary biological progression of the inhabited individual, not the World around it.**

There is no global time stop. While the Warden stays embodied, local weather, temperature regime, light availability and the season itself may all move on, and local rooted suitability may improve or deteriorate — described through the existing environment and Fit architecture, with no new dimension introduced.

## 3. Opportunity can pass unused

> **Remaining Productive Opportunity is not frozen merely because the individual's biology is frozen.**

If useful rooted conditions pass while the Warden remains embodied, that opportunity may simply be **lost**. Missed opportunity is not stored time waiting to be spent later, and it is never repaid: a Warden who spends a whole favourable period embodied and then roots into unsuitable late conditions does not receive the productivity that never happened (AMO-D137, L61).

Three things therefore follow, and each rejects a tempting shortcut:

- **elapsed World time is not Productive Return** — only actual rooted biological work produces it;
- **elapsed World time is not biological maturity** — a paused individual gains no development from however much world history elapses (AMO-D081, L47);
- **elapsed World time does not strengthen the core** — an individual inhabited straight after Full Deployment may stay near its post-construction depletion indefinitely, however long the world moves around it (AMO-D131, AMO-D136).

**Lost opportunity is a cost, not damage.** A long embodiment may produce no productive return, no Tuber rebuilding, no rehabilitation and a missed season without any pathology, direct Tuber injury or automatic deterioration (AMO-D092, AMO-D138). That distinction matters directly downstream (AMO-Q118).

And it needs no enforcement. AMO-D117 stands: embodiment remains open-ended, with **no forced exit, maximum duration, decay timer, hidden punishment or cooldown**. The pressure to return to rooted life is simply that the world keeps moving while biology does not — the game never says *you must root now*.

Missed opportunity is also **historically real**: the individual genuinely spent that period embodied rather than productively rooted, and nothing rewrites that. An observer still cannot read it off the body — appearance reports the manifestation's history, not how much opportunity was spent (AMO-D134).

## 4. Environmental opportunity is not lifecycle permission

Closure creates a loophole to close: if opportunity is local and the Amorpho is mobile, a Warden might chase favourable conditions forever. The architecture answers that with ownership rather than with a rule against travel.

> **Suitable World conditions do not automatically mean an individual is biologically prepared to continue active growth.**

The World may supply suitable temperature, light, moisture and protection. Whether the individual can *use* them belongs to the Amorpho. This is the existing boundary applied to a new case: Environmental Fit may push toward continued activity, recovery or retreat but **never becomes the life-cycle system**, and there is no `force_bloom` or `prevent_dormancy` flag anywhere (AMO-D035–AMO-D037, AMO-D046, [17](17_LIFE_CYCLE_STATE_MACHINE_V0.md) §9).

**Intrinsic Lifecycle Drive** is the working name for the individual's biologically owned tendency or requirement to continue active growth, move toward dormancy, remain dormant, or resume active growth. It is qualitative, needs no formal field, and adds no state to the seven-state topology; its triggers and timing remain open (AMO-Q101, AMO-Q084). The rule it carries is an ownership rule: **the World does not decide the individual's lifecycle program; the Amorpho does.**

Two things must both hold for useful rooted active growth:

| | Asks | Owned by |
|---|---|---|
| **External Productive Opportunity** | does this place and time provide suitable conditions? | World, evaluated through Environmental Fit |
| **Biological Growth Availability** | can this individual currently use those conditions for active growth? | the Amorpho's lifecycle state |

Only where both align can useful rooted work occur. No formula combines them, and **Remaining Productive Opportunity should eventually reflect both** — what remains reachable in the World, and what remains available in this individual's own lifecycle — without collapsing into one season timer (AMO-Q116).

Environment is not irrelevant, either: future biology may let environmental cues influence whether active growth continues, when dormancy pressure develops and when a transition begins. **Environment can influence the lifecycle; it is not sovereign over it.**

## 5. Relocation changes the World, not the plant

> **Relocation can change environmental opportunity; it cannot by itself reset the individual's intrinsic lifecycle.**

An embodied Amorpho physically carries its own core (AMO-D129), so travel genuinely moves the individual to real conditions elsewhere — and travel alone accrues nothing: relocation rebuilds no Tuber, because benefit arrives only if the Warden eventually roots, biology resumes, and actual conditions support useful work (AMO-D136).

Nothing resets at a border, latitude or hemisphere. The individual carries its Tuber state, productive history, damage, lifecycle state, prior opportunity use and current drive across any distance; only the World around it changes. Explicitly rejected: *northern season ends → travel south → the plant is treated as newly beginning the same active phase.*

So the durable formulation is:

> **A Warden can chase suitable weather, but cannot necessarily outrun dormancy.**

- **Still active-capable** with declining local opportunity → relocation may expose the individual to genuinely new opportunity, and that is entirely legitimate.
- **Already committed to its dormancy transition** → moving to another favourable climate does not restore active growth; dormancy proceeds on the individual's biology. If the lifecycle architecture later names a commitment boundary, it is reused rather than duplicated; no trigger or timing is defined here.

No hemisphere shortcut exists in either direction: *south = always suitable* and *winter = globally impossible* are both rejected, because Fit remains local and real (AMO-D045, AMO-D046). Likewise no `Winter State → Productive Return disabled` rule — **season follows place, not game permission**.

Reaching a suitable destination late may also be worth little, since lifecycle context, manifestation condition and future World conditions all still constrain what can be achieved. Nothing here is quantified.

## 6. Controlled environments

A greenhouse or building modifies **local World conditions** — temperature, humidity, exposure, protection and whatever else future infrastructure genuinely changes — and is evaluated by the ordinary mechanism, never by a special rule (AMO-D014, AMO-D046, AMO-Q049).

> **A greenhouse does not automatically create perfect year-round Productive Opportunity, and it does not override biology.**

Limitations that the structure does not actually modify remain limitations — low available seasonal light, for instance, unless future infrastructure really changes it, and no lighting system is designed here. And **controlled suitability plus an individual whose biology requires dormancy does not equal forced active growth**: infrastructure modifies the World, not the Amorpho. Its value therefore emerges from **World modification × individual biology** rather than from any universal greenhouse effect.

## 7. Species strategy, individual state

> **Species biology constrains and shapes the lifecycle strategy available to an individual; the current lifecycle state belongs to the individual Amorpho.**

Species-level biology may influence whether prolonged active growth is possible at all, whether a substantial dormancy period is normally required, how growth is distributed through active periods, how sensitive the lifecycle is to extended unsuitable conditions, and how readily activity resumes after dormancy. The individual nonetheless carries its actual current active or dormant state, its previous active history, condition, Tuber state, environmental history and manifestation history. **Lifecycle is never a species-only lookup**, and two individuals of the same species may differ in what is happening now (AMO-D011, AMO-D058).

The architecture must be able to express meaningfully different strategies. As **design space only** — no real species is assigned to any of them here, and none may be inferred (AMO-D024, AMO-D053, AMO-Q076, AMO-Q110):

| Illustrative strategy | May emphasise | Plausible trade-off |
|---|---|---|
| **Burst-seasonal** | a concentrated favourable active window, exploited strongly, followed by a meaningful dormancy period | high concentrated opportunity against longer unavoidable inactivity |
| **Extended-growth** | long active periods, ready return to activity, less dependence on a long annual dormancy | temporal flexibility against less concentrated gain, and poor suitability to long forced dormancy or strongly seasonal places |

Crude equivalences are rejected: *seasonal = fast*, *tropical = slow*, *tropical = always grows*, *subtropical = must sleep every winter*. What is canonical is only that the simulation must support strategies in which **growth tempo, active-period length and dormancy requirement trade off differently**, without that relationship being universally inverse and without any numbers.

**Dormancy is not merely lost gameplay time.** Where biology genuinely requires it, it may be part of a successful strategy — active burst, persistent gain, dormancy, renewal — and it may carry real strengths rather than being pure disadvantage. Conversely an extended-growth individual may be poorly suited to long forced dormancy or to strongly seasonal environments. Consequences remain future modelling.

Hence the product direction:

> **Fairness comes from trade-offs, not equal uptime.** Amorpho does not balance species by making every individual equally available for active growth all year, and no compensating penalty is invented to even them out.

Two boundaries stay intact. **Relocation's value is itself lifecycle-dependent** — invaluable to one strategy, futile for an individual that has committed to dormancy — so no universal travel bonus exists. And **no species permission rules**: nothing says *species X grows only in region Y*; strategy combines with actual local Fit, so a species may thrive far from its native region where real conditions and its own lifecycle permit (AMO-D013, L9).

Repeated relocation is acclimation and expression, never inheritance: an individual cannot rewrite its species lifecycle strategy by being moved, and generational change remains the **Evolutionator's** (AMO-D012, [10](10_WORLD_AMORPHO_EVOLUTIONATOR.md)). Exact species lifecycle facts remain external, arriving only as approved input if the game demonstrably needs them, with **no data column added here** (AMO-D024, AMO-D025).

## 8. Recovery and Productive Return under two clocks

Rehabilitation runs only once rooted, so an embodied damaged Leaf recovers nothing while the season moves on ([40](40_ROOTED_MATURE_LEAF_RECOVERY_CEILING_AND_COMPENSATORY_REMODELING_V0.md), AMO-D139). That can produce a **high Recovery Ceiling beside shrinking Remaining Productive Opportunity** — the two remain independent axes (AMO-D141).

So a late rehabilitation may be genuinely successful and seasonally disappointing at the same time: the Leaf stabilizes and regains real function, and little useful opportunity remains to spend it in. Both statements are true, and neither cancels the other.

Terminal embodiment obeys the same rule: a committed terminal Leaf may be held indefinitely with its own terminal progression paused, while seasons, conditions and rescue prospects change around it (AMO-D117). No penalty is added for that; it is simply the same world clock.

## 9. Strategic consequences

The deployment question is now two questions at once:

> How much combat damage will I risk — and how much of the World's available biological opportunity will I spend embodied rather than rooted?

Early embodiment may offer an excellent body, poor core security and a large opportunity cost if prolonged. Later embodiment may offer a stronger core, more manifestation wear and less local opportunity remaining. Relocation may change the equation, while a greenhouse may extend it, and the individual's own lifecycle strategy decides how much either helps. **No option is universally optimal**, and no decision formula is defined.

## 10. Worked traces

**A — the missed season.** A Leaf reaches Full Deployment early in a favourable period; the Warden inhabits it immediately while the Tuber is still near post-construction depletion. Productive Return pauses. The Warden stays embodied a long time; the World season advances and local rooted suitability declines. On rooting, biology resumes with only limited local opportunity left. The Tuber may finish the season weak **without ever having suffered pathology**.

**B — legitimate seasonal chase.** The individual remains biologically capable of active growth while local opportunity declines. The Warden relocates, finds genuinely suitable conditions, has not entered a committed dormancy transition, and roots. Active growth and Productive Return may continue. **Allowed.**

**C — chase refused by biology.** The same relocation, but the individual has approached or entered its intrinsic dormancy transition. The destination's conditions are suitable; the individual's biology nonetheless requires the transition, and travel does not reset the lifecycle. Dormancy proceeds. **No anti-exploit penalty was needed.**

**D — extended-growth individual.** An individual whose biology permits long activity meets deteriorating local conditions, is relocated to genuinely suitable conditions and rooted, and continues active growth. Its advantage comes from continuity rather than concentrated gain — and if instead it faced a long period with no suitable environment reachable, growth would simply stop, with consequences left to future modelling.

**E — greenhouse limits.** A controlled environment improves local conditions considerably. For an individual still active-capable, that may extend real opportunity. For one whose biology requires dormancy, it does not cancel that requirement, however good the enclosure.

**F — late rehabilitation.** A damaged Leaf is held embodied too long; the local season advances. On rooting it stabilizes and recovers function well, yet little useful seasonal opportunity remains. **The recovery succeeded; the season did not.**

**G — no geographic reset.** An individual is carried across a hemisphere. Its Tuber state, productive history, damage, lifecycle state and prior opportunity use are all unchanged. Only the World around it is different.

## 11. Deferred model and acceptance

AMO-Q004 and AMO-Q074 own world time scale, granularity and how quickly suitability changes; AMO-Q074 no longer owns *whether* World time matters during a biological pause. AMO-Q116 owns the quantitative productivity model and the representation of both opportunity constraints; AMO-Q103 recovery extent and rates; AMO-Q101 and AMO-Q084 lifecycle triggers, any commitment boundary and species scope; AMO-Q049 controlled-environment fidelity and cost; AMO-Q110 and AMO-Q076 species interpretation and any future lifecycle input; AMO-Q118 the persistent-loss boundary; AMO-Q052 generational change. No new question was required.

| Check | Result |
|---|---|
| Long embodiment | Individual biology pauses while the World season advances (AMO-D136). |
| Missed season | Opportunity that passes unused may be gone (AMO-D145). |
| No biological aging | Elapsed World time grants a paused individual no maturity. |
| No banking | Missed productivity is never paid back later. |
| Relocation | May create genuinely new opportunity while biology still permits growth (AMO-D146). |
| No hemisphere shortcut | Suitability is always the actual local environment. |
| Committed dormancy | Travel cannot reset it; no artificial penalty is added. |
| Greenhouse | May extend opportunity; never makes conditions ideal or overrides biology. |
| Recovery | Rehabilitation waits for rooting while opportunity may shrink; the axes stay independent. |
| Core security | Early long embodiment may leave the core depleted however much time passes. |
| No pathology shortcut | Missed opportunity is a cost, not injury (AMO-D138). |
| Species and individual | Species shapes the strategy; the individual owns the current state (AMO-D147). |
| Fairness | Different strategies, not equal uptime; no compensating penalties. |
| No research | No real species assigned to any lifecycle strategy. |

**Result:** the Warden can stop the plant's clock and cannot stop the world's. Holding an Amorpho embodied spends something real — the season it is not using — and moving it somewhere better buys only what its own biology is still able to accept.
