# 47 — Deep Dormancy Duration and Active-Phase Reactivation Boundary, v0

**Status:** qualitative lifecycle-architecture pass using owner-supplied design direction. It defines the opposite half of [46](46_DORMANCY_COMMITMENT_BOUNDARY_V0.md): once the persistent Tuber is dormant, what decides how long dormancy lasts and when a new active phase may begin. It adds **no new life-cycle state**. It defines no duration, minimum or maximum, temperature or light trigger, species dormancy fact, hormone, sprouting physiology, timer, indicator or input field, and it researches no botany.

> **The World can invite a new cycle; only the Tuber can become ready to begin it.**

## 1. Purpose

Doc 46 fixed how an active phase ends: `ACTIVE LEAF → Dormancy Approach → Dormancy Commitment → Senescence → Tuber-only → Early Dormancy → Deep Dormancy`. Nothing yet said how dormancy ends. This pass answers:

> Once the persistent Tuber is in Deep Dormancy, what determines how long that dormancy continues and when a new active phase may begin?

The owner direction is the answer's spine: **the individual Tuber owns the duration of its dormancy and whether it is biologically ready to resume**, species lifecycle strategy shapes that behaviour, and actual environmental conditions influence whether emergence is appropriate. It must not become a fixed sleep timer, and it must not become *good weather → automatic sprouting*.

## 2. Deep Dormancy is biological life, not frozen time

Two things can look alike from outside — an individual that is not growing — and are different in kind:

| | **Embodiment pause** | **Deep Dormancy** |
|---|---|---|
| What happens | the Warden inhabits a manifestation | the persistent Tuber lives through a dormant lifecycle state |
| Individual biology | **suspended** (AMO-D084, AMO-D136, AMO-D157) | **running** — dormant biology, not active growth |
| World Time | continues | continues |
| The two clocks | diverge | **move together** |
| Playable / astral | inhabited | non-playable, **Astrally Silent**, door closed (AMO-D060, AMO-D088) |

> **Deep Dormancy is biological life, not frozen time** (AMO-D158).

The dormant Tuber exists through World Time and may progress within its dormancy biology toward future reactivation. It is not a frozen record waiting for a timer to expire, and it is not a pause like embodiment: [42](42_WORLD_TIME_SEASONAL_OPPORTUNITY_AND_EMBODIMENT_V0.md)'s two clocks diverge only while an individual is inhabited, and during dormancy they run side by side. No rate of dormant progression is defined.

**Dormancy is not a cooldown.** It is not a fighter cooldown, respawn timer, punishment or availability lock. Any gameplay downtime emerges from biology (AMO-D073, L45).

**Intrinsic Reactivation Readiness is not Astral Readiness.** Astral Readiness is magical state restored by rooted biological life, and a successful dormant period may restore it ([20](20_BIOLOGY_MAGIC_BOUNDARY_AND_ASTRAL_READINESS_V0.md), AMO-D086). Reactivation Readiness (§4) is the dormant individual's biological readiness to begin a new active phase. They share a word and nothing else.

## 3. Species strategy and individual state

> **Dormancy duration belongs to the individual.** It is determined by the biology of the individual Tuber, within the tendencies of its species lifecycle strategy and its actual environmental history.

Never `Species X sleeps N days`. As with doc 46, the architecture must let future approved input represent strategies that differ in whether substantial dormancy is normally required, how persistent dormancy tends to be, how readily active growth resumes, how responsive dormancy is to environment, whether long uninterrupted active growth is possible, and whether prolonged inactivity is biologically normal or undesirable ([42](42_WORLD_TIME_SEASONAL_OPPORTUNITY_AND_EMBODIMENT_V0.md) §7, AMO-D147). These are design dimensions only; no real species is assigned (AMO-D024).

The individual then lives the actual dormancy, shaped by its current Tuber condition, Productive Return from the prior phase, depletion, persistent harm, Developmental Maturity, previous dormancy and active-phase history, environmental history and future biological factors. No weighting is defined.

> **Species shapes the rhythm; the individual lives the actual dormancy.**

Hence three kinds of variation are all legitimate and none is a bug: the **same individual** need not sleep the same way every cycle; **individuals of the same species** need not share a schedule; and **species strategies** may produce long, short, condition-responsive or little dormancy.

- **Strongly seasonal strategies** may require or strongly favour a meaningful dormancy before the next active phase — an integral strength or constraint of that lifecycle.
- **Extended-growth strategies** may enter dormancy rarely, resume readily, and stay active for very long periods under suitable conditions. They may also be **poorly suited to prolonged forced inactivity**; that is design space for future curated biology, with no penalty canonized here.

**Fairness does not require equal dormancy.** Some strategies trade uptime for concentrated growth, others offer extended availability under different constraints, and no artificial cooldown balances them (AMO-D147).

## 4. Intrinsic Reactivation Readiness

> **Intrinsic Reactivation Readiness** is whether the dormant individual has biologically reached a point at which beginning a new active phase is again possible.

It belongs to the persistent individual. It is a concept, not a meter, and needs no formal field.

**It is not elapsed World time.** Dormancy happens through time, so time is relevant; `enough days passed → ready` is nonetheless rejected, because the individual's actual biology and history decide.

**It is not reserve strength.** A robust, well-provisioned Tuber may still be internally dormant; reserve amount is not the dormancy timer (§11, trace D).

**It is not something the Warden can order.** No command makes an internally unready Tuber leave Deep Dormancy. Deep Dormancy keeps Astral Silence and the closed door, so the Warden cannot enter the Tuber to force movement or growth, and direct player intent is never biological readiness (AMO-D060, AMO-D099, AMO-D097).

## 5. External Emergence Suitability

> **External Emergence Suitability** is whether the current local environment provides conditions in which beginning the next active manifestation is biologically appropriate.

The **World** owns the environmental facts and the **Amorpho** owns how this individual responds, through the existing World and Fit architecture with no new variable ([12](12_ENVIRONMENT_AND_FIT_MODEL_V0.md), AMO-D035–AMO-D037, AMO-D046). It is the dormant-side counterpart of External Productive Opportunity ([45](45_REMAINING_PRODUCTIVE_OPPORTUNITY_QUALITATIVE_COMPOSITION_V0.md)) and, like it, states conditions rather than permissions.

> **Intrinsic Reactivation Readiness ≠ External Emergence Suitability.** A Tuber may be internally ready while the environment is poor, and the environment may be excellent while the Tuber is still internally dormant.

**Environment influences dormancy without replacing the lifecycle.** Future biology may let conditions influence dormancy maintenance, the development of readiness, whether emergence stays suppressed and whether resumption is supported. No mechanism is defined. Dormancy is therefore not environment-independent, and not environment-owned.

## 6. A new active phase requires permission and feasibility

Two conditions give **permission**:

```
INTRINSIC REACTIVATION READINESS     (the individual's lifecycle)
            AND
EXTERNAL EMERGENCE SUITABILITY       (World, evaluated for this individual)
```

and a third gives **feasibility**:

```
            AND
BIOLOGICAL FEASIBILITY               (can the persistent state actually fund a manifestation?)
            ▼
next Emergence may proceed
```

`AND` is conceptual conjunction, never a formula (AMO-D159, AMO-D160).

- **A suitable environment cannot force an unready Tuber awake.** Excellent greenhouse or warm-climate conditions plus a Tuber that still requires dormancy: dormancy continues. *Perfect environment = forced sprouting* is rejected.
- **An internally ready Tuber need not emerge into unsuitable conditions.** It may remain dormant while waiting for a more appropriate opportunity, subject to future biology. How long is not defined, and **waiting is not pathology**.
- **Readiness is not the same as having enough capacity to fund a new manifestation.** A Tuber may be ready to become active again and still lack the persistent capacity or condition to build a viable manifestation. *Ready* is not *capable*.

Feasibility reuses what already exists rather than adding a test: biology bounds what the individual can do (AMO-D097), the Tuber funds construction (AMO-D095), and current capacity, condition and reserves constrain a new attempt (AMO-Q101). **Feasibility is not success**: a committed Emergence may still fail, and failure does not trap the lifecycle (AMO-D108).

> **Suitable conditions open the door; the Tuber must still be biologically ready, and able, to walk through it.**

## 7. Dormancy duration is emergent, not scheduled

Dormancy lasts until permission and feasibility align — and that alignment emerges from species strategy, individual state and history, and actual environmental context. Rejected: a fixed annual cooldown, a global winter sleep timer, the same duration for every individual, a hidden mandatory duration, days asleep, percentage complete, an annual wake date.

Consequences:

- **Poor conditions can prolong dormancy** for an internally ready Tuber. Not pathology by itself, and no maximum delay is defined.
- **A depleted but intact Tuber can still be dormant.** Dormancy does not require full reserves; whether the individual later becomes able to fund Emergence depends on its actual biology. No threshold exists.
- **A strong Tuber can remain dormant** because its lifecycle is not ready, which is what proves reserves are not the timer.

## 8. Reactivation Commitment

The topology already has the path. This pass names the boundary on it and adds no state ([17](17_LIFE_CYCLE_STATE_MACHINE_V0.md) §4):

```
DEEP DORMANCY ─────────── Intrinsic Reactivation Readiness may develop here; a ready
     │                     Tuber still waiting for suitable conditions stays here
     ▼  REACTIVATION COMMITMENT — readiness + suitability + feasibility align
PRE-EMERGENCE ─────────── the individual is leaving dormancy
     ▼
EMERGENCE ─────────────── Tuber-funded construction; existing architecture (29, 30, 31)
     ▼
ACTIVE LEAF (or BLOOM)
```

> **Reactivation Commitment** is the point at which the dormant Tuber has biologically committed to initiating the next manifestation cycle.

It is a **transition condition**, the meaning of the existing Deep Dormancy → Pre-Emergence edge, and it is the counterpart of Dormancy Commitment:

| | **Dormancy Commitment** ([46](46_DORMANCY_COMMITMENT_BOUNDARY_V0.md)) | **Reactivation Commitment** |
|---|---|---|
| Means | this active phase is ending | a new active phase is beginning |
| Edge | Active Leaf → Senescence | Deep Dormancy → Pre-Emergence |
| Owned by | the individual's lifecycle | the individual's lifecycle |
| Weather alone | cannot cause or undo it | cannot cause it |

Symmetry stops at ownership; the mechanics need not mirror each other. In particular, v0 defines **no return path** from Pre-Emergence back to Deep Dormancy: whether one exists, and what conditions turning hostile during Pre-Emergence do, stays with AMO-Q101 and AMO-Q084, while a failing Emergence uses the existing failure architecture (AMO-D108, AMO-D112).

**Reactivation is autonomous biology**, not an AI personality decision: when readiness, suitability and feasibility align sufficiently, the Tuber may commit (AMO-D097, AMO-D098). Nothing waits for the Warden, and no `WAITING_FOR_PLAYER` state exists ([17](17_LIFE_CYCLE_STATE_MACHINE_V0.md) §8).

**Construction rules take over.** Once committed, the Tuber funds a manifestation through Emergence exactly as [29](29_REPLACEMENT_EMERGENCE_TO_ASTRAL_READINESS_V0.md), [30](30_EMERGENCE_INVESTMENT_AND_FULL_DEPLOYMENT_ACCOUNTING_BOUNDARY_V0.md) and [31](31_DAMAGED_EMERGENCE_TO_IMPERFECT_DEPLOYMENT_V0.md) describe (AMO-D106, AMO-D109). **Reactivation costs actual Tuber capacity**; dormancy generates no free Leaf. When and how astral access reopens through Pre-Emergence is unchanged and stays AMO-Q085.

**Shallow and absent dormancy.** A strategy that never enters Deep Dormancy uses a dormant-family path that stays shallow ([17](17_LIFE_CYCLE_STATE_MACHINE_V0.md) §14, AMO-Q084), and one in continuous active growth may not need reactivation at all. The same ownership — readiness belongs to the individual, suitability to the World — applies wherever the dormant family is left.

## 9. Geography and controlled environments

A Human or another physical actor may transport a dormant Tuber, place it in a controlled environment, alter its local conditions or prepare for future growth. None of those actions is designed here, and a carried Tuber remains biologically simulated, neither harmed nor in stasis by being carried (AMO-D093, AMO-Q117). Moving it is physical custody, never ownership or astral authority (AMO-D065).

All of them change **External Emergence Suitability**, which may make later reactivation more or less appropriate. None changes intrinsic dormancy history.

- **Hemisphere travel does not instantly wake the plant.** Moving a dormant Tuber into *summer* is not instant emergence.
- **A greenhouse does not instantly wake the plant.** An ideal controlled environment modifies suitability; it cannot manufacture readiness.

> **Relocation and infrastructure change the World the Tuber will wake into, not whether it is ready to wake** (L65).

## 10. Persistent condition and pathology

**New Emergence begins only from the actual persistent state the Tuber carried through dormancy** ([44](44_FULL_BIOLOGICAL_YEAR_PERSISTENT_STATE_INTEGRATION_TRACE_V1.md) step 18, AMO-D095). No reset occurs at reactivation.

- **Dormancy does not automatically refill persistent capacity.** *Time asleep → full Tuber* is rejected. What dormancy does to capacity, maintenance, repair and condition remains AMO-Q102 with AMO-Q073; this pass defines only continuation and exit.
- **Dormancy does not erase persistent harm.** Pathology carries across dormancy unless genuine persistent repair occurs (AMO-D149, AMO-D150).
- **A harmed or depleted Tuber may stay dormant through a favourable season**: excellent conditions plus a lifecycle that would otherwise permit reactivation plus a Tuber too compromised to fund Emergence gives no successful new manifestation yet. Repair is not solved here (AMO-Q102, AMO-Q105).

## 11. Roster implications

A collection is not *fighters available* and *fighters on cooldown*. Different persistent individuals may at once be actively rooted, embodied, approaching dormancy, in Senescence, in Deep Dormancy, internally nearing reactivation, or emerging — and each condition comes from biology ([17](17_LIFE_CYCLE_STATE_MACHINE_V0.md) §11).

So planning emerges naturally: which individuals are likely to stay unavailable, where dormant Tubers are kept, when another individual's active phase may begin, and which regions or infrastructure support reactivation. No interface, forecast or party system is designed.

**No exact wake-up date.** Rejected: *3 days until emergence*, a countdown, a dormancy percentage, a calendar alarm presented as biological truth. A Warden may know species tendencies, the individual's history, its environment and its prior cycles without knowing the instant of emergence; cultivation can be **observational rather than timer-driven**. Any future qualitative cue stays with AMO-Q119 and AMO-Q085. What the Warden can infer — and how the signal's return in Pre-Emergence may be recognised by a long-attuned Warden without any channel through Astral Silence — is specified in [50](50_WARDEN_BIOLOGICAL_INFORMATION_AND_ROSTER_JUDGEMENT_MODEL_V0.md) (AMO-D164, AMO-D167).

## 12. Worked traces

**A — internally unready, excellent environment.** The Tuber enters Deep Dormancy. Conditions later become excellent. It remains intrinsically unready, no Emergence begins, and dormancy continues.

**B — ready, environment unsuitable.** The Tuber progresses through dormancy and readiness develops. Conditions stay unsuitable and it remains dormant. Conditions later improve, and Emergence may become biologically available.

**C — all align.** The Tuber becomes ready, the environment is suitable, and its persistent condition can fund a manifestation. Reactivation Commitment occurs, and Tuber-funded construction takes over.

**D — strong Tuber, still not ready.** Robust and well provisioned, in an excellent environment, with dormancy biology incomplete. No Emergence occurs. **Reserve strength is not wake-up permission.**

**E — ready but unable to fund.** Readiness exists and the environment is suitable, but the persistent Tuber is too compromised or depleted to fund a viable manifestation. New Emergence cannot proceed yet. Persistent recovery remains outside this pass.

**F — same species, different individuals.** Two individuals share a lifecycle strategy and had different seasons and conditions. Both go dormant. Their actual dormancy and readiness differ.

**G — extended-growth strategy.** An individual whose strategy involves minimal or rare Deep Dormancy, with suitable conditions available, resumes active biology relatively readily under future curated rules. No long dormancy is imposed for fairness.

**H — strongly seasonal strategy.** A strong active phase ends in Dormancy Commitment; Deep Dormancy is biologically meaningful and a suitable environment alone cannot eliminate it. Later, readiness and suitable conditions together permit a new cycle.

## 13. Acceptance and consistency audit

| Test | Result |
|---|---|
| **A — excellent environment, not ready** | Remains dormant. |
| **B — ready, bad environment** | May remain dormant. |
| **C — ready + suitable + feasible** | New Emergence may begin. |
| **D — strong core, not ready** | No forced Emergence. |
| **E — ready, insufficient capacity** | Readiness creates no manifestation. |
| **F — greenhouse** | Modifies suitability; cannot manufacture readiness. |
| **G — relocation** | Changes environment, not dormancy history. |
| **H — same species** | Individuals can wake at different times. |
| **I — species diversity** | Long, short and minimal dormancy strategies remain possible. |
| **J — no reset** | The new phase begins from actual persistent state. |

| Distinction | Holds |
|---|---|
| Deep Dormancy ≠ embodiment pause; duration ≠ fixed timer | §2, §7 |
| Reactivation Readiness ≠ Emergence Suitability ≠ reserves ≠ Astral Readiness | §2, §4, §5 |
| Readiness ≠ guaranteed feasible Emergence; feasibility ≠ success | §6 |
| Good environment ≠ forced wake-up; travel ≠ dormancy reset; greenhouse ≠ override | §6, §9 |
| New Emergence ≠ persistent-state reset; species strategy ≠ individual schedule | §3, §10 |

## 14. Deferred quantitative lifecycle model

AMO-Q101 keeps the exact readiness representation, environmental cue weighting, individual-history weighting, the reactivation feasibility test, timing, and any Pre-Emergence return path. AMO-Q084 keeps species parameterization of dormancy and reactivation, shallow and absent dormancy paths, and any cost of prolonged inactivity to extended-growth strategies. AMO-Q102 and AMO-Q073 keep dormancy maintenance biology and what dormancy does to capacity, condition and persistent harm; AMO-Q105 any repair layer. AMO-Q085 keeps astral access through Pre-Emergence; AMO-Q119 player knowledge and cues; AMO-Q117 dormant Tuber storage and transport. No new question was required.

**Result:** a dormant Tuber is a living plant on its own schedule. The World decides what it would wake into, the Warden can change where that is, and only the Tuber — when it is ready, and able to pay for it — decides to begin again.
