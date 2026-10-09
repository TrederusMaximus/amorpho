# 59 — Break Contact and Pursuit: Paper Prototype, v0

**Status:** test design — a disposable tabletop prototype of the Break Contact, Pursuit and Interception architecture named in [58](58_MOVEMENT_DEFENCE_AND_PROTECTION_INTERACTION_V0.md) §9–§10, exported from the unresolved pursuit boundary in [57](57_ONE_VS_THREE_ESCAPE_GEOMETRY_PAPER_TEST_RESULTS_V0.md) Scenarios 2 and 6. It adds no decision, law or combat mechanic, and nothing in it is canonical Movement. **It has not been run, and no result is known.** The broader Cultivation ↔ Embodiment transition test ([52](52_CULTIVATION_EMBODIMENT_TRANSITION_TEST_PAPER_PROTOTYPE_V0.md)) also remains unrun; completing this prototype does not validate that hypothesis.

> **Can Break Contact on open terrain become a meaningful spatial skill problem, rather than collapsing into "the faster body automatically wins"?**

## 1. Purpose and evidence basis

Doc 57 stopped at the same place twice. Scenario 2 reduced coordinated one-versus-three pressure to a local one-versus-one pursuit and could not decide whether the pursuer could catch or intercept the defender before contact broke. Scenario 6 found that without terrain, escape "collapsed almost immediately into movement, pursuit and interception." Doc 58 then gave that boundary a qualitative owner — **Break Contact** (enough separation or positional freedom that opponents no longer retain immediate effective control), **Pursuit** (physical effort to preserve or re-establish pressure on a disengaging target) and **Interception** (physically reaching or controlling where the target is trying to go, not merely where it is) — without defining a mechanic (AMO-D178). This document designs the cheapest test of whether those distinctions produce useful spatial behaviour, or whether open-terrain pursuit reduces to one scalar movement comparison.

The test should explore whether starting position, direction, route choice, pursuit commitment, interception, prediction, change of direction and multiple pursuers can matter independently of raw movement-speed comparison.

Preserved from doc 58: *Break Contact must be possible, and must not be trivial* (§9). *Pursuit follows; Interception moves to where the target is trying to go* (§10). *Speed alone decides neither escape nor catch* (§10, AMO-D178).

## 2. Hypotheses

Each must stay falsifiable; a run that contradicts one is evidence, not a mistake in the test.

| | Hypothesis |
|---|---|
| **H1** | Direct pursuit alone is heavily dependent on relative movement capability. |
| **H2** | Interception can create pressure that direct pursuit cannot. |
| **H3** | Interception creates commitment risk when the prediction is wrong. |
| **H4** | Route changes can matter without guaranteeing escape. |
| **H5** | Starting position and angle can materially affect pursuit. |
| **H6** | Two Pursuers create stronger containment than one. |
| **H7** | Two Pursuers still require coordination and role allocation. |
| **H8** | Break Contact can sometimes emerge on open terrain without terrain assistance. |
| **H9** | Break Contact is not reliably achievable merely by choosing to flee. |
| **H10** | Open-terrain pursuit contains meaningful judgement beyond pure movement advantage. |

## 3. Scope and non-goals

This prototype isolates **movement and spatial decision** from everything doc 58 deliberately left open. It decides none of: final locomotion speed, sprinting, acceleration, turn rate, body-specific mobility, stamina, endurance attrition, attack range, attack animation, collision implementation, root/stun or other crowd control, dodge mechanics, controls, camera, VR locomotion, controls mapping, or networking. It contains **no attacks, shoves, stuns, grabs, projectiles, damage or Protection** — the test isolates whether movement geometry alone is sufficient before asking whether offensive pressure changes the answer (doc 58 §4, §6–§8). It introduces no vision-blocking, stealth or concealment; that stays AMO-Q132's, separately. If a run exposes that one of these excluded items is actually load-bearing, **record it as an exposed requirement against its existing owner** (AMO-Q027, AMO-Q028, AMO-Q023, AMO-Q109) rather than solving it here.

## 4. Prototype-only instruments

> **PROTOTYPE-ONLY TEST INSTRUMENTS — NOT CANONICAL COMBAT MECHANICS.** Nothing here enters DECISIONS.md or describes a future control, speed, distance or contact radius. Their only job is to let paper tokens move so geometry can be observed.

**I1 — Movement allowance.** One movement step is one constant physical movement allowance per token per beat — one card length, one drawn segment, one consistent ruler span. The real-world distance is irrelevant; only the *ratio* between D's and P's allowance in a given run matters (§6). Movement allowance is abstract: do not name it walking, running, sprinting or dashing, and do not derive it from species size — *large species = slow, small species = fast* is rejected here exactly as it is in doc 58 §14 and AMO-D162.

**I2 — Test beat.** Both sides state or secretly mark movement intent, reveal, move using the current allowance, observe the resulting geometry, repeat. A beat is not a combat turn and implies no future turn structure; §6 varies the reveal order deliberately.

**I3 — Direct Pursuit.** P moves toward D's current or most recently known position. Models *follow the target*; no homing, no guaranteed closing.

**I4 — Interception Attempt.** P moves toward the route or space P believes D is trying to reach, not toward D's current position. A correct Interception Attempt and an incorrect one must be able to produce visibly different geometry — Interception is a prediction with real downside, not automatically superior pursuit (doc 58 §10).

**I5 — Route change.** D may continue its route, cut toward another exit, or reverse where physically plausible, with no invulnerability while doing so; a route change may cost forward progress, reduce separation, or expose a new intercept line, through token geometry alone. No turn radius is defined.

**I6 — Break Contact stand-in.** Record Break Contact when D reaches an escape boundary with no Pursuer in a position the facilitator treats as immediate control. If a more useful representation emerges during play, use it and label it TEST-ONLY; do not convert any version into a distance, time or radius. **The boundary represents sufficient separation, not a magical game-world line** — the final World may have no visible escape border at all.

**I7 — Contact-maintained stand-in.** Record contact-maintained by one simple visual condition fixed before the run — touching markers, or being within one movement-allowance of each other — and record whether the chosen definition drives the outcome (§6).

**Meta-test.** One purpose of this prototype is to discover whether a formal contact threshold is even needed. If token movement stays legible without one, prefer that; if every result becomes ambiguous without one, record: *future combat needs a concrete operational definition of immediate pressure/contact* — without inventing that definition here.

## 5. Open-terrain test field

```text
                       P
                       D

                  open field


   L-ROUTE        FORWARD ROUTE        R-ROUTE
```

The exact drawing may differ; what must hold: D has several plausible departure directions, P begins close enough that pursuit matters, and nothing on the field creates artificial congestion for either side. No Rock, no GAP, no walls, no terrain bonus. A single exit would collapse the test into "who moves faster in a straight line"; at least three credible directions (a more direct route and routes to either side) let pursuit, interception, prediction and route switching stay distinguishable (doc 58 §12).

**Scenario 6 and 7 (§7.6–7.7)** vary P's starting position or the number of credible exits against this same field; they do not change its shape. **§7.17's optional terrain comparison** is the only run that adds an obstacle, and only after the open-terrain scenarios are complete.

## 6. Movement-capability and choice-order sensitivity

Two axes vary independently across the recommended runs (§9), and neither is ever converted into a canonical value or a percentage.

**Movement-capability variant.**

| Variant | Allowance |
|---|---|
| **EQUAL** | D and P receive the same prototype movement allowance. |
| **DEFENDER-ADVANTAGED** | D receives a modestly greater allowance than P. |
| **PURSUER-ADVANTAGED** | P receives a modestly greater allowance than D. |

**Choice-order variant.**

| Variant | Procedure |
|---|---|
| **SIMULTANEOUS** | Both sides secretly mark intended movement, reveal together, then move. |
| **DEFENDER-FIRST** | D moves, then P reacts and moves. |
| **PURSUER-FIRST** | P commits and moves, then D reacts and moves. |

Real-time combat has no clean turn sequence, so a conclusion that only holds under one order is a turn-order artifact, not evidence about Break Contact itself (doc 58 §2). For every scenario in §7, ask:

| Question | Label if the answer is yes |
|---|---|
| Would the outcome change merely because one side had modestly more movement allowance? | `RAW-MOVEMENT SENSITIVE` |
| Does Defender-first vs simultaneous vs Pursuer-first movement change the conclusion? | `ORDER SENSITIVE` |
| Does the outcome depend entirely on how this prototype defines contact? | `CONTACT-DEFINITION SENSITIVE` |
| Did either side make an actual decision, or did the result follow automatically from allowance? | `PROTOTYPE-ARTIFACT DOMINATED` if no decision was made |

None of these labels is a verdict on the final combat model; each marks a dependency the next design pass must handle deliberately, not ignore.

Also vary **starting separation** (close pursuit and a visibly larger initial gap, no measured distance) and **starting angle** (§7.6) across the core scenarios: if Break Contact becomes trivial merely because D began one step farther away, or trivial merely because of relative orientation, record that as a sensitivity finding, not as a balance conclusion.

## 7. Scenarios

No attacks, damage, Protection or crowd control appear in any scenario; movement only.

### 7.1 Scenario 1 — Straight pursuit

D ahead, P behind, one obvious forward route, open terrain. Run under all three movement-capability variants (§6). **Question:** can direct pursuit alone close, hold or lose the initial separation? This scenario is not expected to be tactically rich — it exists to expose, honestly, how much raw capability decides the outcome before anything else is tested. If the three runs reduce to *equal → separation unchanged; D faster → D leaves; P faster → P closes*, record that plainly: it would mean straight open-field pursuit alone contains almost no decision, which is exactly the justification for testing route choice and interception next (H1).

### 7.2 Scenario 2 — Defender route choice

D is given several plausible escape directions; P uses Direct Pursuit only; no interception yet. **Observe:** does route angle affect separation; does P merely reproduce D's path; can D gain anything from changing direction against pure following?

### 7.3 Scenario 3 — Pursuit versus Interception

The central scenario. Same field and start, run twice: **(A)** P uses Direct Pursuit; **(B)** P uses an Interception Attempt against the route P believes D will take. Then run a **wrong-interception** pass: let D choose a different route than P predicted, and observe whether the failed Interception Attempt leaves P worse positioned than Direct Pursuit would have. **Questions:** can correct interception meaningfully threaten D; can incorrect interception create a larger escape opportunity than Direct Pursuit allowed; does this produce an actual decision rather than a speed check (H2, H3)?

### 7.4 Scenario 4 — Defender route change / feint

P commits to an Interception Attempt; D initially moves as if choosing one route, then redirects — the facilitator simply changes D's token direction, with no feint skill defined. **Observe:** can D punish premature Pursuer commitment; does the redirect cost D enough that interception still retains value; does P retain a reasonable response once committed?

### 7.5 Scenario 5 — Late interception

Repeat Scenario 4 with P deliberately waiting longer before committing to an Interception Attempt. **Compare:** does an earlier commitment deny the route more strongly but risk more if wrong, while a later commitment has more information but less space left to cut the route? Do not canonize this trade-off; only test whether it appears (H3, H4).

### 7.6 Scenario 6 — Starting-angle sensitivity

Vary P's starting position relative to D — directly behind, slightly left, slightly right, somewhat ahead but off-route where plausible — holding everything else fixed. **Question:** does initial angle meaningfully alter which pursuit or interception options are available, testing doc 58's claim that starting position matters (H5)?

### 7.7 Scenario 7 — One Pursuer against two exits

Simplify the field to two credible escape directions. **Question:** can one P deny both without committing to either? If P can cover both with no spatial commitment, record that as a problem (AMO-D178 rejects a hard lock); if committing to one opens the other, record that too.

### 7.8 Scenario 8 — Two Pursuers, movement only

Add P2: D versus P1+P2 on open terrain, movement only, no attacks. **Questions:** do two Pursuers meaningfully reduce D's route options; can they split responsibility; does this create more pressure than one Pursuer; can D still exploit poor coordination between them (H6, H7)?

### 7.9 Scenario 9 — Coordinated roles

P1 uses Direct Pursuit; P2 attempts Interception. **Observe:** is this materially stronger than both merely following D; does P2's commitment open another route; can D redirect to force re-coordination?

### 7.10 Scenario 10 — Poor coordination

P1 and P2 both use Direct Pursuit on D independently. **Observe:** do they become spatially redundant, converging on the same line; does D gain more route freedom than against Scenario 9's coordinated pair — connecting back to doc 57 Scenario 1's finding that greedy pursuit can produce exploitable redundancy?

### 7.11 Scenario 11 — Split-route denial

P1 denies the left route, P2 the right; D considers a central route or a late switch. **Question:** can two Pursuers create meaningful enclosure on open terrain without a magical hard lock, with no attacks, no crowd control and no hidden defender bonus?

### 7.12 Scenario 12 — Pursuer overcommitment

One P commits strongly to an Interception route; D redirects. **Observe:** does P lose useful relative position; can D exploit the commitment; can P recover without inventing a new mechanic? This tests that *Pursuit carries commitment* (doc 58 §10, AMO-D178).

### 7.13 Scenario 13 — Defender overcommitment

D commits strongly to one route; P intercepts correctly. **Observe:** does P gain a meaningful spatial advantage; does D still have options; does correct prediction matter? This is the counterweight to Scenario 12, so the test is not biased toward the Defender succeeding.

### 7.14 Scenario 14 — Break Contact and reacquisition (thought test only)

If D reaches the prototype's Break Contact stand-in (I6), run one thought test, with no new mechanic: can P later reacquire D simply by remaining nearby? The purpose is only to preserve *Break Contact ≠ teleportation ≠ permanent immunity* (doc 58 §9). After Break Contact, D remains exactly where D physically moved and P remains exactly where P physically moved — no arena reset — and a later encounter stays possible if the bodies happen to meet again. No detection mechanic is built.

### 7.15 Scenario 15 — Stake versus Pursuit

Add one abstract original conflict stake behind P, with no values (doc 54's access stake). D begins an escape attempt. P must choose: pursue D, or remain to secure the original stake. **Question:** does Pursuit naturally cost the Pursuer their previous position or objective, connecting doc 54's withdrawal cost to doc 58's pursuit commitment? No missions are designed.

### 7.16 Scenario 16 — Group allocation

With P1 and P2: P1 pursues; P2 may help intercept, remain with the original stake, or cover another route. **Question:** does group pressure require actual allocation rather than omnipresence? No combat, no reward system. Either Warden's objective may change mid-scenario — D from escaping to exploiting an overcommitted P, P from pursuing to returning to the stake — from the emerging geometry alone, with no scripted phase.

### 7.17 Optional final terrain comparison

After the open-terrain scenarios are complete, add **one** simple obstacle and repeat one pursuit scenario (Scenario 3 is the natural choice). **Purpose:** compare movement-decision structure on open ground with terrain-altered structure. Do not re-run the full doc 56 board test.

## 8. Facilitator log

For every run, record in words, not scores:

| Field | |
|---|---|
| Scenario | |
| Movement-capability condition | EQUAL / DEFENDER-ADVANTAGED / PURSUER-ADVANTAGED |
| Choice-order condition | SIMULTANEOUS / DEFENDER-FIRST / PURSUER-FIRST |
| Starting relationship | separation and angle, in words |
| D's decision | |
| P's / P1's / P2's decision | |
| Break Contact occurred? | yes / no / unresolved |
| Did interception matter? | |
| Did raw movement capability dominate? | |
| Did order matter? | |
| Did the contact definition matter? | |
| One-sentence reason for the outcome | |
| Unresolved question exposed | |

No numeric score is recorded anywhere in this log.

**Result labels**, for use once runs exist, not before: **SUPPORTED** · **PARTIALLY SUPPORTED** · **UNRESOLVED** · **RAW-MOVEMENT SENSITIVE** · **ORDER SENSITIVE** · **CONTACT-DEFINITION SENSITIVE** · **PROTOTYPE-ARTIFACT DOMINATED**.

## 9. Recommended run matrix

Enough to learn from in one sitting; not every scenario needs every sensitivity pass.

1. Straight pursuit — equal.
2. Straight pursuit — Defender advantage.
3. Straight pursuit — Pursuer advantage.
4. Pursuit vs Interception (correct).
5. Pursuit vs Interception (wrong prediction).
6. Defender route change.
7. One Pursuer — alternate starting angle.
8. Two Pursuers — poor coordination.
9. Two Pursuers — coordinated pursue + intercept.
10. Two Pursuers — split-route denial.
11. Key simultaneous-choice sensitivity pass (repeat one of the above under all three choice-order variants).
12. Optional terrain comparison.

**Designed for a short manual tabletop session.** No exact duration is promised.

## 10. Success criteria

| | Criterion |
|---|---|
| **A** | Direct pursuit reveals clearly how much raw movement capability matters — tactical richness is not required for success here. |
| **B** | Interception differs meaningfully from direct pursuit. |
| **C** | Correct interception can create pressure. |
| **D** | Incorrect interception can create an escape opportunity. |
| **E** | Defender route choice can matter. |
| **F** | Pursuer commitment can matter. |
| **G** | Break Contact can occur in at least some plausible configurations. |
| **H** | Break Contact is not automatic whenever D chooses to flee. |
| **I** | Two Pursuers create materially more pressure than one. |
| **J** | Two Pursuers still require actual role or route decisions. |
| **K** | No explicit anti-gank bonus is required to let D have options. |
| **L** | Open terrain contains at least some meaningful spatial decision beyond pure speed comparison — **the most important criterion of all**. |

## 11. Failure criteria

| | Failure |
|---|---|
| **A** | All one-versus-one pursuit outcomes reduce entirely to *faster token wins*. |
| **B** | Interception is always strictly superior to pursuit with no downside. |
| **C** | Interception never matters. |
| **D** | D can always escape simply by changing direction. |
| **E** | D can never escape unless D has greater raw movement allowance. |
| **F** | One P can perfectly control every escape route without spatial commitment. |
| **G** | Two Ps create deterministic capture regardless of D's decisions. |
| **H** | Two Ps add almost no pressure compared with one. |
| **I** | Results depend almost entirely on arbitrary paper turn order. |
| **J** | Results depend almost entirely on an arbitrary contact radius. |
| **K** | The prototype requires hidden Defender assistance to produce any escape. |
| **L** | The only way to create interesting pursuit is to add terrain — if this occurs, record it; do not patch the test to avoid it. |

## 12. Interpretation limits

**The prototype does not need to "pass."** If the evidence shows that open-terrain Break Contact cannot become interesting without explicit acceleration, facing, attack pressure or another mechanic, that is a valuable result — the next prototype can then introduce the minimum missing dimension deliberately, rather than this one inventing it under pressure to succeed.

**Most important falsifier.** If open-terrain pursuit remains nothing more than raw relative movement allowance despite route choice, interception and commitment, then doc 58's qualitative architecture is insufficient to produce the intended gameplay by itself. This must be treated as a valid result.

**Second major falsifier.** If two Pursuers can cover every route with certainty simply by existing, record: *multi-pursuer open-terrain containment may require additional mechanics or constraints.* Do not invent those mechanics during the results pass.

**Third major falsifier.** If one Defender can always redirect and escape because Pursuers must commit, record: *Interception is too weak under this test's representation.* Again, do not patch immediately.

Even if every success criterion holds, the most this test supports is: **the qualitative architecture of doc 58 appears plausible enough to justify designing concrete Movement and Pursuit mechanics around it.** It does not show Amorpho combat is solved, fun or balanced, and a hand-moved board is kinder to deliberate positioning than real time will be.

## 13. Exported requirements and consistency

Whatever the outcome, this design already implies requirements for later work. None is a mechanic; each belongs to its existing owner:

- **Movement and pursuit** (AMO-Q028, AMO-Q027): concrete Break Contact conditions, how pursuit keeps or loses contact, interception, acceleration and directional commitment — qualitatively — and whether open-terrain pursuit can contain real skill without reducing to *faster body = guaranteed escape* or *more pursuers = guaranteed interception*.
- **Controls** (AMO-Q023): remain untouched; this test exercises intent-level movement only.
- **Conflict information** (AMO-Q132): remains separate; this test assumes no omniscience between D and P and introduces no detection, stealth or concealment mechanic.
- **Protection and offence** (AMO-Q109, AMO-Q027): whatever this prototype cannot resolve through movement alone is a candidate for the next, separate prototype — not for this one to absorb.

**Consistency audit** — distinctions this document must not blur:

| |
|---|
| prototype movement allowance ≠ game speed |
| test beat ≠ combat turn |
| escape boundary ≠ World portal |
| prototype contact ≠ canonical engagement radius |
| interception test ≠ final interception mechanic |
| Break Contact test ≠ validated Break Contact system |
| movement advantage ≠ species trait |
| two Pursuers ≠ automatic capture |
| route change ≠ automatic escape |
| designed prototype ≠ run prototype |

**Result:** this document designs the test; it does not run it. The owner runs it manually afterwards and records findings in a dated results document, as doc 57 did for doc 56. **The Cultivation ↔ Embodiment transition test (doc 52) remains unrun, and the central product hypothesis stays untested regardless of this prototype's outcome.**
