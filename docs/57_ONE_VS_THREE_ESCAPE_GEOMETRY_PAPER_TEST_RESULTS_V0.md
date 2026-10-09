# 57 — One-versus-Three Escape Geometry: Paper Test Results, v0

**Status:** evidence record. The tabletop test designed in [56](56_ONE_VS_THREE_ESCAPE_GEOMETRY_PAPER_PROTOTYPE_V0.md) was **run manually by the project owner** with physical tokens and recorded here on 2026-10-06. This document reports what happened; it adds no decision, law or mechanic, and it does not redesign combat. **The Cultivation ↔ Embodiment transition test ([52](52_CULTIVATION_EMBODIMENT_TRANSITION_TEST_PAPER_PROTOTYPE_V0.md)) has not been run, and the central product hypothesis remains untested.**

> **The geometry hypothesis gained useful support; final anti-dogpile safety remains unproven.**

## 1. Purpose

To record honestly what the one-versus-three board test showed about the premise behind AMO-D174–AMO-D176 and L74 — that embodied geometry can give an outnumbered defender real chances without any anti-gank bonus while coordinated numbers stay genuinely dangerous — and to export what the test could **not** decide as requirements for future Movement and Defence design.

## 2. Method

**Material.** One Defender token (D), three Attacker tokens (A1–A3), a fourth Attacker token (A4) for the reinforcement thought test, hand-drawn positions and exits, a drawn Rock and GAP for terrain runs, and a separate board with no terrain for the open-ground run. Manual movement and qualitative reasoning only. No statistics, health, dice, formulas, speeds, ranges or timing values. Photographs were taken during the run and are not stored in the repository.

**Roles.** The owner played the Defender. The assistant, as facilitator, applied the intended attacker behaviour for each scenario — greedy pursuit, coordinated role-keeping, protecting, ignoring or rotating.

**Board as run.** Abstract locations C (centre), W, N, E and exits EXIT-N, EXIT-E and EXIT-S; **W had no exit**; Rock and GAP were present in the terrain runs. These are paper instruments, not game-world topology: nothing here implies Amorpho combat uses zones, tiles, exits as portals, a single Rock/GAP layout or board adjacency.

**Deviations from the doc 56 design, stated openly.**

- **Board.** The run used a simpler layout than doc 56 §5, with the attackers starting at W, N and E rather than the designed positions.
- **Scenario numbering.** The run's Scenarios 3, 4 and 5 were *protect the exposed member*, *ignore the exposed member* and *rotation/handoff*. Doc 56 numbered isolation, ignore and protect as 3, 4 and 5, and had no rotation scenario. This record follows the run's numbering.
- **Instruments.** The run did **not** resolve outcomes with doc 56's instrument rules (pinning, Shove, Cover, the escape condition). It used qualitative reasoning and **stopped whenever an outcome would have required a combat or movement mechanic that does not exist**. Doc 56's required instrument-sensitivity runs were therefore not performed; they would have tested instruments the run did not rely on.

**The stopping discipline is part of the evidence.** Each place the test stopped marks a boundary where a future mechanic, not geometry, decides the outcome.

## 3. Evidence standard

Labels: **SUPPORTED** · **PARTIALLY SUPPORTED** · **UNRESOLVED** · **NOT SEPARATELY RE-RUN** · **NEW REQUIREMENT EXPOSED**. *Unresolved* is never read as *probably works*, and no combat outcome is inferred from token proximity where missing Movement, Defence or Pursuit rules would decide it.

The test is evidence about spatial architecture, group coordination, local isolation, reinforcement arrival and information boundaries. It does **not** validate real-time feel or fun, balance, attacks, defence timing, protection, movement speed, pursuit, interception, body obstruction during active attack, camera, controls, latency or networking, or player behaviour at scale.

## 4. Scenario 1 — poor coordination

**Start.** D at C; A1 at W, A2 at N, A3 at E; Rock and GAP present; exits N, E and S.

**Defender's opening — deliberately counterintuitive:** attack A1 at W, moving *away* from every exit. The owner's reasoning: W was the least expected direction because it had no exit; attacking there might pull the N and E attackers off their useful positions; that could create options around the Rock later; the aim was to manipulate the attackers' geometry before choosing a route.

**Observed.**

1. D attacked A1 at W.
2. A2 and A3, pursuing greedily, abandoned their N and E coverage and moved toward D.
3. The attackers clustered.
4. D moved south, intending to use the Rock to create congestion and later escape east.
5. The attackers' actual route around the Rock differed from what D had expected.
6. D recognised the planned eastern route had become dangerous.
7. D adapted rather than following the original plan.
8. D reversed toward EXIT-S.
9. D reached EXIT-S while the attackers remained concentrated on the less useful side of the developing geometry.
10. The scenario ended in a successful escape.

**Not claimed:** stealth or line of sight. During play the owner briefly described the change of direction as perhaps less noticeable behind the Rock; the test explicitly declined to invent stealth, line-of-sight blocking or perception rules. **The escape followed from the attackers' positional concentration and the Defender's adaptation to the resulting geometry.**

**Result: SUPPORTED** — poor coordination created exploitable spatial redundancy; escape occurred without defeating any attacker.

**Findings.** Poor coordination can make attackers abandon useful exit coverage. Several attackers can become spatially redundant rather than acting as independent perfect pressure. Defender decision quality mattered: the first plan failed and adaptation produced the escape. Terrain changed the problem and did not guarantee the Defender's success. **This does not show that poor coordination always permits escape.**

## 5. Scenario 2 — coordinated enclosure

**Start.** Reset to the same position. D repeated the **same opening** for comparability: attack A1 at W.

**Observed.** A2 stayed at N and A3 stayed at E; neither abandoned exit coverage, so the lure failed. D changed strategy: disengaged from the initial pressure, moved south around and behind the Rock, and tried to draw A1 into being the only southern pursuer. The group answered: A2 held N, A3 held E, A1 followed D south to deny the southern exit. D chose to run for EXIT-S.

**Stopped at:** *can A1 catch, intercept or pin D before contact is broken?* No legitimate answer exists, because it depends on relative movement, acceleration, pursuit, interception, displacement, break-contact rules, possibly body morphology and possibly pressure during pursuit.

**Result: UNRESOLVED AT PURSUIT BOUNDARY.** Neither side is declared the winner.

**Findings.** **Coordinated enclosure was materially stronger than poor coordination**: the opening that broke Scenario 1 did not move A2 or A3 here. And **D turned the global one-versus-three geometry into a local one-versus-one pursuit problem.** Global multi-attacker pressure was reduced; successful break of contact was not shown.

## 6. Scenario 3 — protecting an exposed member

**Start.** Rewound to D pressuring A1 at W, A2 at N, A3 at E.

**Assumed for test purpose:** A1 had been pressured enough that continuing alone carried credible biological risk. No value, percentage or threshold was used.

**Observed.** The coordinated group chose to protect A1: A2 left N and moved toward A1 and D; A3 stayed at E. **Threatening one individual attacker forced the group to trade enclosure for member protection**, and EXIT-N became unoccupied.

**Stopped at:** once A2 reached the local fight, the owner wanted to arrange positions so the weakened A1 stood between D and the fresher A2 — A1 as a temporary physical obstruction — while D moved south. Whether that is possible needs rules for simultaneous pressure from several attackers, relative body positioning and orientation, obstruction, attack timing, defence, displacement, one opponent screening another, bodies denying attack angles, and repositioning under pressure from two directions.

**Result: PARTIALLY SUPPORTED** — the group-reaction trade-off appeared; the escape outcome is **unresolved at the multi-threat combat boundary**.

**New requirement exposed.** Multi-attacker combat should be **capable of producing relative positions in which one opponent temporarily obstructs or limits another's effective pressure.** This is a requirement to investigate, not a rule: nothing says an enemy body always blocks its ally, and no screening rule, collision formula or support radius is implied.

**An open exit was not automatically usable.** When EXIT-N emptied, D did not take it: two nearby attackers, their positions, the current threat and likely pursuit made a nominally open exit a poor practical choice. **A route being open is not the same as escape being available** — evidence against any combat model in which an unoccupied route immediately becomes a successful exit. No rule is defined.

## 7. Scenario 4 — ignoring an exposed member

**Start.** Rewound: D attacks A1 at W; A2 holds N; A3 holds E. The group deliberately chose to keep exit coverage and not help A1.

**Assumed for test purpose:** because the scenario exists to test the **cost of abandonment**, the local pressure was treated as succeeding far enough to produce the intended consequence: A1 was treated as broken — no longer able to oppose meaningfully in this encounter. **This does not claim future combat would let D destroy A1;** that was not tested.

**Tested proposition:** if a group refuses to protect a genuinely exposed member, does it keep its enclosure for free? **Observed answer: no.** The group kept N and E coverage, and A1 carried the individual consequence. With A1 out of effective opposition, D was separated from the remaining N and E attackers and moved toward S, where the Rock and the distance made the southern route look favourable. The final pursuit was not resolved.

**Result: SUPPORTED AS A TRADE-OFF** — ignoring an exposed member preserved coverage but left that member to bear the individual biological consequence. Escape afterwards: **strongly positioned, unresolved at the pursuit boundary.**

**Scenarios 3 and 4 together** showed the dilemma:

| | Benefit | Cost |
|---|---|---|
| **Protect A1** | preserves A1, reducing its immediate risk | another attacker leaves useful coverage; enclosure weakens; local congestion rises; an exit may become less controlled |
| **Ignore A1** | N and E coverage stays intact | A1 carries the individual biological risk |

This supports *group pressure is collective; biological consequences remain individual* (AMO-D176 revised). It does **not** show the trade-off is balanced, that it prevents griefing by itself, or that either response is always best.

## 8. Scenario 5 — rotation and handoff

**Start.** D pressures the already weakened A1 at W; A2 begins at N; A3 at E.

**Intended coordinated rotation:** A2 leaves N, reaches the fight and takes over pressure on D; A1 disengages, moves toward N and restores coverage if the handoff succeeds.

**Observed.** **Rotation cannot be treated as instantaneous or free.** A2 must physically leave N and arrive; A1 must physically disengage; there is a **handoff period**.

**Defender's decision at the handoff:** not to turn defensive, but to put maximum pressure on the weakened A1 and try to break that body before the rotation completes. The owner's reasoning: a clean handoff would preserve A1 and restore N, so the vulnerable transition is the Defender's best opportunity, and letting it pass would restore the group's structure too cheaply.

**Stopped at:** whether D succeeds — which depends on undefined rules for A2 interrupting D, A2 covering A1's disengagement, D keeping pressure on A1, simultaneous attacks, body blocking, defence, movement, disengagement, target switching, protection and local priority under several threats.

**Result: SUPPORTED STRUCTURALLY** — rotation creates a physical handoff; the outcome is **unresolved at the handoff-combat boundary**.

## 9. Scenario 6 — open terrain

**Start.** A separate clean board: D at C; A1 at W, A2 at N, A3 at E; exits N, E and S; no Rock, no GAP, no terrain. Attackers coordinated.

**Defender's decision:** move straight for EXIT-S — W guards no exit, N and E are occupied, S is open, and without terrain there is nothing to manipulate first; the question becomes speed and pursuit.

**Stopped at once at:** can D use movement to leave before any attacker intercepts? No legitimate answer exists.

**Result: UNRESOLVED** — movement and pursuit dominate open terrain.

**Finding.** With an obstacle, terrain created route choice, congestion, local isolation, different pursuit paths, repositioning and chances to manipulate relative positions. **In open terrain the problem collapsed almost immediately into movement, pursuit and interception.** Neither *open terrain favours the defender* nor *open terrain favours attackers* was shown. **The geometry-only prototype cannot resolve open-terrain escape without a movement and pursuit model.**

## 10. Scenario 7 — terrain contrast

**Result: NOT SEPARATELY RE-RUN** — the owner judged the contrast already shown by Scenarios 1–6. No replay is reported.

**Qualitative conclusion from the runs that were played:** **terrain changes the tactical problem for both sides; it is not a defender buff.** The Rock sometimes helped D — separating pursuers, redirecting their paths, creating congestion, enabling isolation attempts, breaking direct spatial relationships — and also constrained D, making EXIT-S less directly reachable, limiting D's own movement and creating possible interception points depending on route. *Geography matters because it changes available relationships, not because it favours one side.*

## 11. Reinforcement thought test

A fourth token, A4, was introduced. The owner identified at once that **A4 cannot fall from the sky or simply join the match**: it must arrive through World space — on the board, through an actual access point such as N, E or S, depending on where it came from (abstract exits, not game-world gateways). The test first considered A4 approaching from S.

**Before physical arrival A4 has no local geometry**: it cannot block D, complete the enclosure, protect another attacker, attack D, control the local exit or add pressure merely by being designated reinforcement.

**Direction and timing matter:** reinforcement strength depends on who is coming **and where and when they physically reach the conflict** — A4 from S, from N, from E, still far away, or arriving after the fight has already changed are different situations. No values.

**Result: SUPPORTED, WITH NEW INFORMATION-BOUNDARY FINDINGS** — reinforcement is a World arrival event, not a change in match population (AMO-D176).

## 12. Information and event-ordering findings

These are **NEW REQUIREMENTS EXPOSED**, not tested mechanics.

**Physical truth and participant knowledge separated during play.** The owner asked: when can D know A4 is approaching? Why would A4 know a conflict exists? Does A4 know A1–A3 are there, or where D is? Was A4 summoned, or arriving by coincidence? Does A4 know D's likely route, and does D know A4's? None was answered with omniscience. Three concepts are distinct:

| | |
|---|---|
| **Physical arrival** | where A4 actually is, and when it reaches the local conflict |
| **Conflict awareness** | whether A4 knows a conflict is happening at all |
| **Coordination knowledge** | whether A4 has enough current information to coordinate deliberately with A1–A3 |

And D's knowledge of A4 is separate from A4's actual approach.

**Reinforcement does not imply coordination.** An arriving fourth Amorpho is tactical reinforcement only if something actually causes it to know about, and support, the existing attackers — it may have been summoned, be independently aware, be arriving by coincidence or be misinformed. No communication or party system is designed.

**No automatic tactical omniscience.** An approaching ally or enemy must not give every participant perfect knowledge of the encounter. No minimap, party radar, team vision, shared markers, communication, voice, detection radius, alert or ping is designed, and **the Astral Anchor does not become an enemy or team radar**: its information stays within the bound Warden–individual relationship and the Astral Signal's existing limits (AMO-D088, AMO-D166).

**Near-simultaneous event order changed the encounter.** The owner demonstrated two variants at EXIT-S that differed only by a small amount of World time:

- **Variant A — D leaves first.** D escapes the original conflict through EXIT-S while A1–A3 are behind or just starting to pursue, emerges outside the earlier conflict space, and then meets the approaching A4 — possibly without either having known about the other. The original one-versus-three escape becomes **a new D-versus-A4 encounter outside the first one**, with A1–A3 possibly still behind. Not resolved.
- **Variant B — A4 enters first.** A4 reaches S slightly earlier and crosses into the ongoing conflict space, becoming a fourth participant inside the existing geometry before D can leave. D may no longer have a clear southern route; A4 may now see A1–A3 directly and infer more than in Variant A; A1–A3 may see A4 arrive. It is now one continuing conflict rather than two sequential contacts. Perfect information is not assumed even here: only actual perception or future communication could supply it.

> **Requirement exposed: near-simultaneous World events must resolve by their actual physical order, not by an abstract "reinforcement joins combat" event.** *D crosses the boundary, then A4 arrives* and *A4 crosses, then D reaches the boundary* can differ in geometry, information, available exits, encounter continuity and tactical meaning. No frame precision, tick order, networking or synchronization approach is implied.

**A rational decision can become bad only because information arrives later.** D chose EXIT-S because S looked open, N and E were held and A4 was unknown; after crossing, D found A4. That does not make the earlier choice irrational: **a Warden judges from available knowledge, not World omniscience** — the in-conflict counterpart of the biological truth-versus-knowledge split in [50](50_WARDEN_BIOLOGICAL_INFORMATION_AND_ROSTER_JUDGEMENT_MODEL_V0.md) (AMO-D164, AMO-D165). Tactical knowledge during conflict must obey the same separation. Ownership of the question is recorded as AMO-Q132.

## 13. Summary

| Scenario | Result | What was learned |
|---|---|---|
| **1 — poor coordination** | SUPPORTED — escape | Greedy pursuit produced spatial redundancy; adaptation after a failed first plan produced the escape |
| **2 — coordinated enclosure** | UNRESOLVED at pursuit boundary | Coordination was materially stronger; one-versus-three was reduced to local pursuit |
| **3 — protect exposed member** | PARTIALLY SUPPORTED | Threat to one attacker made the group weaken enclosure; an open exit was not automatically usable |
| **4 — ignore exposed member** | SUPPORTED as trade-off | Coverage was kept only by leaving A1 to bear the consequence |
| **5 — rotation and handoff** | SUPPORTED STRUCTURALLY; outcome unresolved | Rotation has a physical handoff window the defender can contest |
| **6 — open terrain** | UNRESOLVED | Movement and pursuit dominate without terrain |
| **7 — terrain contrast** | NOT SEPARATELY RE-RUN | Earlier runs showed terrain changes both sides' geometry |
| **Reinforcement** | SUPPORTED + new requirements | Physical arrival, awareness and coordination are separate; event order matters |

**What was observed, assumed and left open:**

| Observed | Assumed for test purpose | Unresolved |
|---|---|---|
| Scenario 1 escape | A1 could be pressured into credible biological risk (Scenarios 3–5) | pursuit outcome and interception |
| Coordination changed attacker behaviour | Scenario 4 treated A1 as effectively out of the encounter, to test the cost of abandonment | one-versus-two combat |
| Supporting A1 emptied N | | contest over the handoff |
| Ignoring A1 kept coverage and moved the risk onto A1 | | active body obstruction |
| Rotation created a handoff | | open-terrain escape |
| Open terrain hit pursuit uncertainty at once | | final anti-dogpile balance |
| Reinforcement had to arrive physically | | |
| Event order changed the situation | | |

## 14. Hypotheses and criteria

**Hypotheses (doc 56 §2):**

| | Hypothesis | Assessment |
|---|---|---|
| **A** | Three attackers meaningfully pressure one defender | **SUPPORTED QUALITATIVELY** — coordinated enclosure materially constrained D compared with poor coordination |
| **B** | Good coordination substantially stronger than poor | **SUPPORTED** — the same opening produced very different group behaviour |
| **C** | Geometry prevents perfect simultaneous pressure from all three | **PARTIALLY SUPPORTED** — congestion, role coverage and group-response trade-offs appeared; active multi-threat combat remains undefined |
| **D** | Defender can sometimes open an escape through positioning | **SUPPORTED** in the poor-coordination run; **PARTIALLY SUPPORTED** more generally |
| **E** | Defender can open a route by exposing or isolating one attacker | **PARTIALLY SUPPORTED** — the group-response trade-off appeared; whether isolation reliably becomes escape is unresolved |
| **F** | None of this guarantees escape | **SUPPORTED** — several runs stopped unresolved; no universal escape existed |
| **G** | No attacker count alone produces certain destruction | **NOT PROVEN; NO CONTRARY EVIDENCE IN THIS TEST** — the test showed mechanisms that can create counterplay, not that larger groups cannot force outcomes |

**Success criteria (doc 56 §15):** **A** three clearly more dangerous than one — SUPPORTED. **B** coordination strengthens containment — SUPPORTED. **C** poor coordination leaves exploitable mistakes — SUPPORTED. **D** defender decisions affect survival — SUPPORTED QUALITATIVELY. **E** isolation forces a group response — SUPPORTED STRUCTURALLY. **F** protecting a member weakens enclosure elsewhere — SUPPORTED. **G** ignoring a member carries individual consequence — SUPPORTED AS SCENARIO PREMISE AND STRUCTURAL TRADE-OFF; the actual combat consequence was not simulated. **H** escape without defeating attackers — SUPPORTED by Scenario 1. **I** escape not guaranteed — SUPPORTED. **J** no numerical anti-gank mechanic needed — SUPPORTED **for this prototype only**; it does not show final combat needs none.

**Failure criteria (doc 56 §16):** **A** deterministic containment regardless of decisions — NOT OBSERVED. **B** three add almost no pressure — NOT OBSERVED. **C** congestion never matters — NOT OBSERVED. **D** coordination does not matter — REJECTED BY OBSERVATION; it mattered strongly. **E** isolation creates no group decision — NOT OBSERVED; protect, ignore and rotate were distinct choices. **F** defender can always escape once choosing to — NOT SUPPORTED; several runs were unresolved. **G** defender can never escape once surrounded — REJECTED by Scenario 1, **under poor coordination only**. **H** opening only by defeating an attacker — NOT OBSERVED. **I** terrain decides everything — NOT OBSERVED. **J** hidden anti-gank bonus required — NOT OBSERVED; none was used.

## 15. Exported requirements for future combat design

Requirements, not answers. Each is recorded against its owner in the open-questions register.

- **Movement and pursuit** (AMO-Q028, AMO-Q027): how contact is broken; how pursuit keeps or loses contact; interception; acceleration and directional commitment, qualitatively; whether a fleeing body can be caught; whether pursuers can close space. **Open-terrain pursuit must contain real skill and counterplay**, reducible neither to *faster body = guaranteed escape* nor to *more pursuers = guaranteed interception*.
- **Multi-threat defence** (AMO-Q027, AMO-Q109, AMO-Q023): how two or more attackers apply pressure; whether they can attack simultaneously; how facing and orientation matter; whether one body can screen another; how the defender's attention is split.
- **Isolation** (AMO-Q027): combat must support meaningful local isolation if the principle is to survive.
- **Handoff and rotation** (AMO-Q027): whether one attacker can cover another's disengagement; whether the defender can punish the handoff; how costly rotation is in time and space; whether an injured attacker can rotate out under pressure; whether a covering attacker can interpose; how many threats can apply meaningful pressure at once.
- **Body geometry** (AMO-Q027): whether bodies obstruct movement and attack lines, and whether an opponent can be used as a temporary screen.
- **Routes** (AMO-Q028): an open route is not automatically an available escape.
- **Terrain** (AMO-Q028): must alter relationships for both sides, not act as a defender bonus.
- **Reinforcement** (AMO-Q028): must respect physical arrival, direction, timing and **event order**.
- **Information** (AMO-Q132): must separate World truth, current perception, known conflict state and coordination knowledge, with no automatic tactical omniscience and no Anchor radar.

## 16. What the test does not prove

It does not show that Amorpho combat works, is fun or is balanced; that real-time play behaves like a hand-moved board; that very large groups cannot guarantee destruction; that real-time combat will stay escapable; that coordination at scale will not dominate; or that griefing is solved (AMO-Q008). A board moved by hand is far kinder to deliberate positioning than real time will be.

> **The anti-dogpile geometry hypothesis remains plausible enough to continue into Movement and Defence design, but it is not validated as a complete multiplayer safety solution.**

## 17. The next boundary

The test repeatedly stopped at the same places — pursuit, interception, multi-threat defence, body obstruction, handoff and breaking contact. **Geometry has taken the question as far as it can; the next answers belong to movement, defence and protection interacting.** The broader transition test (doc 52) remains unrun, and the central hypothesis — *cultivation makes combat matter more, and combat makes cultivation matter more* — remains untested.

*Revised 2026-10-07:* the unresolved boundaries exported in §15 now have a qualitative owner in [58](58_MOVEMENT_DEFENCE_AND_PROTECTION_INTERACTION_V0.md). The evidence recorded above is unchanged, and doc 58 does not resolve any outcome this test left open.

*Revised 2026-10-09:* the pursuit boundary this test exposed (§5, §9) now has a dedicated disposable follow-up paper prototype in [59](59_BREAK_CONTACT_AND_PURSUIT_PAPER_PROTOTYPE_V0.md), designed and not yet run. The evidence recorded above is unchanged.
