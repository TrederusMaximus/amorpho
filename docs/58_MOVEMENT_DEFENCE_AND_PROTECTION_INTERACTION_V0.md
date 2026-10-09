# 58 — Movement, Defence and Protection Interaction, v0

**Status:** qualitative combat-architecture pass using owner-supplied design direction. It is the first specification of how an embodied Amorpho moves, defends and survives inside active conflict, and it takes ownership of the boundaries the one-versus-three board test stopped at ([57](57_ONE_VS_THREE_ESCAPE_GEOMETRY_PAPER_TEST_RESULTS_V0.md) §15, §17). It defines the **interaction architecture** later mechanics must satisfy. It defines no move, attack, combo, frame data, timing window, control, camera, lock-on, animation, physics, collision volume, speed, range, distance, damage or Protection value, stamina, crowd control, hitbox, UI, networking model, engine, technology, PvP governance or species fact. **The Cultivation ↔ Embodiment transition test ([52](52_CULTIVATION_EMBODIMENT_TRANSITION_TEST_PAPER_PROTOTYPE_V0.md)) has not been run, and the central product hypothesis remains untested.**

> **A Warden survives by controlling space, reacting to threats, using Protection intelligently and deciding when biological risk is no longer worth the objective.**

## 1. Purpose and evidence basis

Docs [35](35_COMBAT_PROTECTION_MANIFESTATION_BODY_DAMAGE_AND_BIOLOGICAL_PERSISTENCE_V0.md), [36](36_COMBAT_RESOLUTION_SURRENDER_ESCAPE_AND_WITHDRAWAL_V0.md), [49](49_COMBAT_PILLARS_AND_BIOLOGICAL_ROSTER_STRATEGY_V0.md) and [55](55_MULTI_ATTACKER_ENCOUNTERS_ESCAPE_AND_ANTI_DOGPILE_PRINCIPLES_V0.md) fixed what combat is *for* and what it may not become. Doc 57 then ran into the same missing layer in nearly every scenario: pursuit, interception, breaking contact, repositioning under pressure, several attackers pressing at once, bodies obstructing movement and attack relationships, covering or punishing a handoff, and Protection stressed from several directions. This document gives those questions a qualitative owner.

**Doc 57 is evidence, not canon.** It established that poor coordination can create exploitable spatial redundancy; that coordinated attackers are materially harder to escape; that threatening one attacker can force a group-level reaction, where protecting the exposed member weakens enclosure and ignoring it externalises risk onto that individual; that rotation creates a physical handoff window; that open terrain collapses at once into movement and pursuit; that terrain changes the problem for both sides; that reinforcements must physically arrive; that arrival, awareness and coordination are separate; and that near-simultaneous event order can produce different encounters.

It did **not** establish movement speed, attack reach, dodge or block timing, exact interception, Break Contact distance, whether one body always blocks another, how much simultaneous pressure several attackers can create, exact Protection behaviour or final anti-dogpile balance. The board's instruments — zones, exits, Rock, GAP, pinning, Shove, Cover — are **not** combat rules and are not imported here.

Preserved throughout: *one consciousness, one inhabited body* (L22), *Protection may stop the blow; a body that is struck cannot ignore it* (L58), and *numbers create pressure, not certainty* (L74).

## 2. Physical embodied movement

**The combat body is the biological manifestation.** Nothing here creates a separate combat avatar, astral duplicate, fighter copy or combat-only body (AMO-D120). The embodied Leaf or Bloom is the actual manifestation, carrying the persistent Tuber core and its Astral Anchor (AMO-D129, AMO-D132, AMO-D143).

> **Embodied movement changes the actual physical position of the persistent individual in the World.**

There is no arena-copy position and no automatic return to a pre-fight coordinate. Where the Warden moves the Amorpho is where the individual goes; if the Warden later exits, the plant roots where the body actually stands (AMO-D032, Pillar 3 of [49](49_COMBAT_PILLARS_AND_BIOLOGICAL_ROSTER_STRATEGY_V0.md)). Combat geography is real geography — consistent with [37](37_MANIFESTATION_DESTRUCTION_TUBER_CORE_VIABILITY_AND_PHYSICAL_DROP_V0.md), [42](42_WORLD_TIME_SEASONAL_OPPORTUNITY_AND_EMBODIMENT_V0.md), [49](49_COMBAT_PILLARS_AND_BIOLOGICAL_ROSTER_STRATEGY_V0.md), [51](51_PERSISTENT_INDIVIDUAL_PLANT_MODEL_V0.md) and [55](55_MULTI_ATTACKER_ENCOUNTERS_ESCAPE_AND_ANTI_DOGPILE_PRINCIPLES_V0.md). This restates AMO-D129 for the combat context; it adds no new rule.

**Engagement is relational, not an arena state.** There is no `IN_COMBAT` bubble that governs physical reality. Combat is occurring because bodies are close enough to threaten, contest movement, pursue, block routes or defend objectives. The World stays continuous, and an encounter may move through roads, structures, vegetation, open ground and transitions between local spaces. No zone boundary is defined.

**No target-lock ontology.** The architecture does not assume one attacker, one defender and one locked target. It must support several nearby threats, changing threat directions, target switching, moving without facing only one opponent, and one attacker becoming locally more important than another. No camera behaviour or lock-on control is chosen (AMO-Q023, AMO-Q024).

**Agency under pressure.** The future system must leave meaningful decisions available: reposition, change angle, increase separation, move toward terrain, move away from enclosure, move around one body to affect another's access, abandon an objective, begin an escape attempt.

> **Pressure may constrain movement without removing movement as meaningful play.**

## 3. Position and Threat Geometry

> **Where bodies stand relative to one another matters independently of damage.**

Position may affect who can reach whom, who blocks whom, available routes, defensive options, escape paths, support between allies and pursuit geometry. **Position is not a stat bonus**: there is no flanking percentage, formation bonus or terrain modifier.

**Bodies occupy physical space.** Embodied bodies are not intangible damage sources ([55](55_MULTI_ATTACKER_ENCOUNTERS_ESCAPE_AND_ANTI_DOGPILE_PRINCIPLES_V0.md) §5, AMO-D176). Physical bodies — enemies, allies, the defender — and terrain can interfere with movement through the space they occupy. Several attackers cannot occupy the same optimal position with no spatial consequence. No collision capsule, body radius or push force is defined.

**Body obstruction and body shielding are different claims.**

| | Meaning | Status here |
|---|---|---|
| **Body obstruction** | one body makes a route or spatial relationship harder for another body | part of the architecture |
| **Body shielding** | one body physically prevents an attack reaching another | **not canonised** — depends on future attack and Protection geometry |

Nothing says one enemy always blocks attacks from another. What is required is weaker and durable: **relative body position must be capable of affecting effective pressure.**

### Threat Geometry

> **Threat Geometry** is which bodies can meaningfully threaten which spaces and bodies, given their current physical relationships.

It is the conceptual owner for approach, angle, obstruction, enclosure, support and pressure on escape routes. It is **not** a visible grid, numerical threat radius, UI overlay or stored stat; it is a way of describing what the World's actual positions currently allow.

**Threat Geometry is dynamic.** It changes when the defender moves, an attacker moves, terrain intervenes, an attacker retreats, a body is displaced, a reinforcement arrives, a participant is injured in a way that changes what its body can do, or the conflict objective changes. There are no static formation bonuses.

**Enclosure is emergent.** No `ENCLOSED` status exists merely because three attackers do.

> **Enclosure** exists when the attackers' actual spatial control leaves the defender without a practical uncontested departure route.

Whether that holds depends on bodies, terrain, movement, support and current threat relationships. No formula.

## 4. Multi-threat spatial interaction

**Several attackers remain more dangerous.** Two attackers should normally create more pressure than one, and three coordinated attackers more than two: more angles, more pursuit possibilities, less safe movement space, less defensive freedom, more chance of Protection being challenged, higher biological risk. **Numerical superiority matters strongly** (AMO-D174).

**But simultaneous pressure needs spatial legitimacy.** Additional attackers are never abstract independent damage streams. For an attacker to apply meaningful immediate pressure, their actual position must support it.

> **Simultaneous pressure is constrained by geometry.**

No maximum attacker count, slot around a target or attack cooldown is defined.

**Movement and offence are interdependent.** Applying offensive pressure requires spatial commitment, and movement can create or remove offensive opportunity. This holds for future reach, projectile, emitted or other non-contact effects too: no universal melee assumption is made, and every hostile effect must still obey position, line or area relationships, Protection and World causality. No attack is designed (AMO-Q027).

**Offensive commitment can reduce defensive freedom.** To press, an attacker may commit position, attention, movement direction, proximity and body exposure.

> **Offensive pressure is not completely separable from personal defensive risk.**

No recovery frames or stamina. This is qualitative commitment only, and it is how *group pressure is collective; biological consequences remain individual* (AMO-D176 revised) becomes physical: an attacker helping hold enclosure, pursuit, route denial or immediate pressure may thereby reduce their own ability to retreat, evade, reposition or protect themselves — through actual commitment and geometry, never a group debuff.

## 5. Local Screening and Local Isolation

### Local Screening

> A body is **locally screening** a threat when its physical position limits that threat's immediate ability to apply pressure cleanly.

Causes may include body occupancy, a constrained route, attack angle, terrain and positioning. Local Screening is **contextual, not guaranteed, not immunity and not a status effect**, and carries no numerical bonus.

**An opponent may sometimes become part of the geometry that limits another opponent.** An outnumbered defender may try to place one attacker between themselves and another, force attackers into one approach lane, make one attacker reposition around another, or open temporary separation from part of the group — the direction doc 57 Scenario 3 stopped at. No technique is defined. The durable requirement:

> **Multi-attacker combat must permit positional relationships that reduce how perfectly several attackers can pressure the same body at once.**

### Local Isolation

> An attacker is **locally isolated** when the current spatial relationship prevents allies from immediately applying effective support without changing their own positions or responsibilities.

Isolation is contextual and temporary and is **not a debuff**. It creates **opportunity, not automatic victory**: the defender may apply more focused pressure, force a group reaction or create an escape opening, and combat still decides what happens.

**The group-protection dilemma** observed in doc 57 Scenarios 3–5 is preserved as a three-way structure, with no option automatically optimal:

| Response | Keeps | Accepts |
|---|---|---|
| **Ignore** the exposed member | coverage elsewhere | that member's individual biological risk |
| **Reinforce** the exposed member | that member's safety | weaker coverage elsewhere |
| **Rotate / hand off** | both, if it succeeds | a vulnerable physical transition |

## 6. Active Defence

> **Active Defence** is a Warden's immediate combat action intended to prevent, redirect, reduce or control a hostile effect before it reaches the vulnerable biological body.

Design-space examples only, none canonised: guarding, deflection, parrying, bracing, redirection, evasive repositioning.

**Active Defence is skill expression.** It depends on future player execution and judgement — reading threats, positioning, timing, deciding what to protect — and never becomes a Defence stat that rolls automatically. No probability model, no automatic perfect guard, no timing window is defined (L15, AMO-D163).

**Spatial avoidance.** *A threat that does not reach the manifestation body cannot biologically damage it.* Movement may prevent contact by changing position, angle, distance or line of approach. Avoidance stays **physical**: no dodge roll, invulnerability frames or immunity window is assumed. **Movement does not grant invulnerability by default** — a body that remains inside a valid hostile effect is not saved by the fact that it was moving. Future evasion mechanics must stay spatial and causal.

**Defence cannot assume one direction.** Threats may come from front, side, rear, changing directions and several opponents. No directional control is designed, but an architecture in which **one successful guard action automatically answers all simultaneous directions is rejected**, unless a future specific Protection capability explicitly justifies it.

**Defensive freedom is spatial.** A Warden may defend well from a good position and badly from a bad one: terrain behind may prevent retreat, one attacker may limit rotation, another may hold the escape path, a body may block lateral movement. No Defence percentage.

## 7. Protection

**Active Defence and Protection are distinct.**

| | What it is |
|---|---|
| **Active Defence** | what the Warden **does** in the moment |
| **Protection** | a physical, magical or designed protective layer or capability that intercepts hostile effect before it damages the body |

**Terminology, reconciled.** Docs 35 and 49 and AMO-D122 use *protection* broadly for everything standing between a hostile effect and the body, listing skilful blocking, parrying, evasion and positioning alongside shields, wards and armour; doc 35 §5's diagram already separated a *defensive response* step from *Protection interception*. From this document on, that whole intercepting boundary is the **protection boundary**, decomposed as **spatial avoidance → Active Defence → Protection**, and *Protection* by itself names the protective layer or capability. Nothing that was protective stops being protective; the layer's architectural role is unchanged. Recorded as a clarification on AMO-D122 and in AMO-D177.

**Protection does not replace Defence.**

> **Protection makes mistakes and risk more survivable; it does not eliminate the need to move, defend and disengage.**

*Best armour, therefore ignore positioning* is a failure.

**Protection is not biological HP.** Protection, body integrity and Core Viability are never one bar (AMO-D121, AMO-D151, L58). Protection can be compromised while the manifestation is biologically intact; the manifestation can be injured after Protection fails; the core can remain viable despite manifestation damage.

**Coverage must be comprehensible.** Protection is assumed neither omnidirectional nor directional. Instead:

> **Every future Protection mechanism must have a comprehensible relationship between what it covers and where hostile effect comes from.**

Future Protection may be local, directional, body-wide or situational; no equipment is designed. It must support **several threats stressing different parts or directions of protection**: one attacker from one direction and three attackers from different directions need not be equivalent situations. No degradation model or shield meter is defined (AMO-Q109).

**Protection makes stakes usable, not trivial.** If every mistake immediately ruins a living Leaf, combat is irrational; if Protection makes body risk negligible, biological stakes are cosmetic. Protection must eventually support the middle — **enough forgiveness for active combat, while body-reaching failure stays meaningful** — the two opposite requirements of [35](35_COMBAT_PROTECTION_MANIFESTATION_BODY_DAMAGE_AND_BIOLOGICAL_PERSISTENCE_V0.md) §5.

**No mandatory gear escalation.** Higher-tier gear must not automatically invalidate lower-tier players; equipment and economy balance are outside scope. A future trade-off between protective coverage, mobility, weight, commitment and exposure is left open — *heavy armour = slow* is not canonised.

## 8. The interaction order, and the body

A hostile action never jumps straight from attack input to biological damage. The causal architecture:

```text
THREAT / HOSTILE EFFECT
  ↓
SPATIAL AVOIDANCE / POSITION       does the effect reach the body's space at all?
  ↓
ACTIVE DEFENCE                     does the Warden's action redirect, reduce or control it?
  ↓
PROTECTION                         does a protective layer intercept some, all or none?
  ↓
RESIDUAL EFFECT
  ↓
BIOLOGICAL MANIFESTATION BODY
  ↓
REAL MANIFESTATION CONSEQUENCE     existing mature pathway (docs 23, 24, 33, 35, 40)
```

This is a **causal architecture, not a mandatory sequence**: not every attack passes through every layer, and different future attacks may interact with the layers differently. No universal move assumption follows. It refines, and does not replace, the protection boundary of [35](35_COMBAT_PROTECTION_MANIFESTATION_BODY_DAMAGE_AND_BIOLOGICAL_PERSISTENCE_V0.md) §5: incoming effect → Protection intercepts some, all or none → residual → body. **Protection cannot retroactively erase a body hit.**

**Body hit means real body hit.** If hostile effect reaches the manifestation body, real biological state changes now (AMO-D120). There is no combat-only damage copy, and the body that roots afterwards is the body that was struck.

**No HP-to-biology mapping.** Combat capability, Protection state, manifestation condition and Core state are related and distinct (AMO-D121). There is no *100 combat HP = healthy Leaf*. A body can keep fighting while biologically damaged, withdraw before Collapse, and keep scars after combat.

**Function changes through the actual body.** No generic *injured = −20% speed*. If body damage affects a biologically or physically relevant function — mobility, stability, reach, structural use — later combat capability may change **because the actual body changed**. Mappings remain AMO-Q109. The same holds for movement: a damaged manifestation may later move differently only where actual damage affects relevant structure or function.

**Damage does not end embodiment.** Body damage, even serious damage, does not equal surrender, withdrawal, Functional Collapse or manifestation destruction (AMO-D124, AMO-D126). The Warden keeps judgement while the body remains inhabitable.

**Collapse stays biological.** Functional Collapse and Collapse Commitment ([33](33_MATURE_LEAF_FUNCTIONAL_COLLAPSE_BOUNDARY_V0.md)) are not knockdown, stagger, stun or incapacitation. Any future combat-control effect needs separate design.

**Escalation stays interpretable:**

```text
PROTECTION STILL EFFECTIVE       → body risk lower
PROTECTION COMPROMISED/BYPASSED  → body risk rises
BODY STRUCK                      → persistent biological consequence
```

That creates the question *is continuing worth another body hit?* with no numeric risk meter — Pillar 2 and Pillar 6 of [49](49_COMBAT_PILLARS_AND_BIOLOGICAL_ROSTER_STRATEGY_V0.md), now with a place in the interaction order.

**Biological Deployment Cost continues during combat.** It is not only a pre-fight choice (AMO-D161): new body damage, Protection loss, changing stakes and deteriorating position all bear on *is continuing still worth it?*, and the Warden keeps re-evaluating, with no automated recommendation.

**No passive armour math.** Position, timing, judgement and Protection stay separate contributors; there is **no single Defence score** and **no single Mobility scalar** that resolves spatial combat. Movement may later have quantitative properties, but player decisions, geography, direction, commitment and relationships between bodies must remain meaningful.

## 9. Break Contact and Escape

> **Break Contact** occurs when the defender has created enough physical separation or positional freedom that opponents no longer retain immediate effective control over continued engagement.

No meter, seconds, tiles, timer or icon. It sharpens the spatial half of Escape as defined in AMO-D175.

**Four things, kept apart:**

| | |
|---|---|
| **Escape Objective** | the Warden's intention: *leave this encounter* |
| **Escape Attempt** | the active process of trying to create separation |
| **Break Contact** | the spatial result that ends immediate forced interaction |
| **Post-Escape Movement** | the Warden continuing physically through the World — no teleport |

**Escape is not a button.** Choosing to escape does not produce Break Contact; it must be created through movement and combat relationships (AMO-D125, AMO-D175).

**Break Contact must be possible.** A sufficiently good situation must sometimes let a defender actually leave. An architecture in which, once contacted, combat can end only by surrender or body failure is rejected — it would invalidate the Escape resolution family ([36](36_COMBAT_RESOLUTION_SURRENDER_ESCAPE_AND_WITHDRAWAL_V0.md) §8).

**Break Contact must not be trivial.** *Turn away → instant escape* is equally rejected. Attackers must have meaningful ways to pursue, intercept, preserve contact and deny routes.

**Open is not escapable.**

| | |
|---|---|
| **Geometrically open route** | no body currently occupies it |
| **Practically escapable route** | the defender can plausibly reach and use it without opponents retaining effective control |

An unoccupied exit is not automatically usable while local combat geometry still makes reaching it unsafe — doc 57 Scenario 3's observation. No exact test is defined.

**Break Contact and the stake are separate.** A defender may Break Contact and preserve the manifestation while losing the location, access or custody opportunity or abandoning the objective. That is intended (AMO-D172, AMO-D175).

**Withdrawal, Escape and Surrender stay distinct.** *Conscious Withdrawal* concedes the stake and may be followed by disengagement and physical departure; *Escape* is the contested act of getting away without necessarily accepting the opponent's claim; neither is one command (AMO-D125). *Surrender* is not a movement mechanic: a yielded Warden may still stand in the same place, and ordinary opponents should generally stop hostile continuation under existing architecture; enforcement stays AMO-Q008. **No universal knockout**: winning is not destroying a body, and Movement, Defence and Protection must support objective resolution, surrender, escape and withdrawal without requiring biological failure (AMO-D124, L59).

## 10. Pursuit and Interception

> **Pursuit** is continued physical effort to preserve or re-establish effective pressure on a target attempting to disengage.

It requires actual movement, route choice and continued commitment. It is not target lock, teleport or automatic follow.

> **Interception** occurs when an opponent physically reaches or controls a relevant route or space in time to prevent a clean Break Contact.

It requires actual World position — no remote interception, no menu response.

**They differ:** pursuit *follows* the escaping target; interception *moves to where the target is trying to go*. The distinction matters for groups, terrain, reinforcements and route coverage. No predictive AI is designed.

**Pursuit carries commitment.** A pursuer leaves its previous position, may abandon an objective, may lose formation support, may expose its own body, stays embodied and keeps paying biological opportunity cost (AMO-D136, AMO-D176). No pursuit resource exists; this follows from World continuity.

**Pursuit can fail** — a poor route, intervening terrain, separation created by the defender, a change of direction, pressure on the pursuer, interference from the defender's allies, or an objective that becomes more important. No speed check.

**Speed alone decides neither.** *Higher movement stat = automatic escape* and *higher movement stat = automatic catch* are both rejected. Movement capability may matter strongly, but pursuit also depends on starting position, route, acceleration and commitment, terrain, interception, body condition, pressure and decision quality. No formula (doc 57 Scenario 6).

**No infinite kiting.** Outnumbered combat is not solved by making flight always optimal: attackers need future means to pressure, intercept, pursue and control routes. Balance is future design and testing.

## 11. Handoff and rotation

> A **Combat Handoff** occurs when one attacker attempts to assume pressure or spatial responsibility from another attacker who is trying to disengage or reposition.

**A handoff requires physical transition.** Roles do not teleport between attackers: A2 must move into a useful position, A1 must physically disengage, and the group must survive the transition (doc 57 Scenario 5).

**A handoff can be contested.** The defender must have a meaningful opportunity to exploit a poorly executed handoff — keep pressure on the weakened attacker, reposition around the arriving one, or escape through temporarily weakened coverage. Success is not guaranteed. No move is designed.

**Covering another attacker is permitted and costs space.** A2 may occupy threatening space, screen A1, force the defender defensive, and make room for A1 to disengage — physical support, with no `Cover` move. A supporting body is **somewhere** doing that support and cannot simultaneously keep every previous positional responsibility: group advantage without free omnipresence.

**Rotation may restore enclosure later**, if the handoff succeeds — A1 moving to another angle, route or safer position — but restoration takes actual movement and World time. No instant formation reset.

**Objectives shift mid-encounter on both sides.** A defender may go from protecting an objective to escaping, or from escaping to pressing an isolated attacker and back. A group may go from preventing escape to protecting an exposed member, to restoring enclosure, to pursuit. These emerge from World state; there are no scripted phases and no AI state machine is designed.

## 12. Terrain and open terrain

**Terrain changes the problem for both sides.** It alters paths, relative positions, congestion, interception possibilities, pursuit options and escape choices, and it can help or hurt either side. Terrain is not *defender +20%* (doc 57 §10).

**Open terrain needs genuine gameplay.** Doc 57 Scenario 6 showed that without terrain, escape collapses at once into pursuit. Future Movement must therefore support meaningful skill even where no obstacle exists — possible qualitative contributors include angle change, commitment, acceleration, directional choice, pursuit prediction, spacing and pressure. No mechanic is chosen.

**No guaranteed open-terrain outcome.** Open terrain must not always favour the faster or fleeing body, and must not be automatic death because several attackers can fan out. That remains a future balance and mechanics problem.

## 13. Reinforcements and the information boundary

**Reinforcement contributes only after physical arrival.** Movement architecture must allow arrival from a direction, at a time, into existing geometry. There is no *join combat* event (AMO-D176). Before arrival a reinforcement adds no local Threat Geometry.

**Physical event order changes the encounter.** *The defender crosses a local boundary before A4 arrives* is not the same encounter as *A4 arrives before the defender crosses* (doc 57 §12). Movement must respect actual physical event ordering. These are domain semantics; no networking, tick ordering or synchronization approach is implied (AMO-Q123, AMO-Q132).

**Movement does not imply awareness.** A4's approach does not automatically reveal A4 to the defender, and the defender's position does not automatically reveal itself to A4. Movement and Defence must not rely on omniscient awareness.

**Threats must be perceptible enough to play fairly.** A product requirement, with no UI: *a player must have a reasonable way to perceive threats they are expected to react to, subject to legitimate occlusion, surprise and information limits* — otherwise Active Defence becomes arbitrary. **Hidden threats remain possible** — through occlusion, surprise, lack of communication or arrival from elsewhere — but surprising outcomes must stay causally grounded (AMO-D165).

**The Astral Anchor is not combat radar.** Its feedback concerns the bound individual's biological and astral relationship; it provides no enemy positions, reinforcement alerts, ally positions or attack-direction warnings (AMO-D088, AMO-D166, L71).

**Protection confidence.** Warden knowledge should permit qualitative judgements such as *Protection is still reliable*, *one side is compromised*, *another body hit is plausible*; no telemetry is required here (AMO-Q044, AMO-Q109, AMO-Q132).

**AMO-Q132 is not resolved here.** This document only avoids assumptions that would pre-decide perception range, team sharing, ally communication, detection or tactical overlays.

**Readability and causal fairness.** A player must be able to learn from failure: *"I was hit because A2 had a clean angle while I focused A1"* is useful; *"I randomly lost biological condition because three enemies were nearby"* is unacceptable. A player may lose because opponents coordinated better, they were surrounded, Protection failed, they chose the wrong route or they overcommitted — **never because group count silently increased hidden damage** (AMO-D165, AMO-D174).

## 14. Standard and VR semantic requirements

The interactions here are **intent-level**: reposition, defend against a threat from a direction, press, disengage, pursue, intercept, cover. They must eventually be expressible through standard screen, controller and keyboard input and through VR interaction (AMO-D041, AMO-D104). No control, gesture or locomotion scheme is designed (AMO-Q023, AMO-Q059).

**VR gains no mandatory physical-performance advantage** merely because a player can gesture faster or more precisely; platform implementation must preserve shared game truth and fairness (L54, AMO-Q060). **No athletic requirement**: the Warden's combat skill belongs to game interaction, not to real-world dodging speed, striking ability or extreme motion. Accessibility design is deferred.

**Movement capability may differ by body** — locomotion, turning, reach, movement form, body shape — but only by deliberate design. Taxonomy, rarity, origin, cultivation difficulty and real plant size never determine combat role, power or movement archetype; *large species = slow, small species = fast* is not a rule (AMO-D162, L70).

## 15. Worked traces

All traces are qualitative and stop before any value or mechanic would decide them.

**A — single-attacker escape attempt.** D judges the objective no longer worth further body risk and moves toward a plausible route. A1 pursues. D changes position to create separation; A1 tries to intercept or keep pressure. **The outcome depends on concrete movement mechanics that do not yet exist.** If Break Contact occurs, D physically leaves through the World, and the stake consequence persists.

**B — two-direction pressure.** A1 presses from one direction while A2 occupies another useful approach. D cannot treat them as one threat and repositions to reduce their simultaneous access. A1 and A2 must reposition if they want to keep the pressure. Protection and body risk depend on what hostile effects actually reach D.

**C — screening.** D, pressed by A1 and A2, moves so that A1 stands in A2's clean route. A2's immediate pressure becomes less direct; A2 may reposition around A1. D may use that interval to move or disengage. **Nothing guarantees A1 blocks every attack.**

**D — handoff.** A1 is damaged and exposed. A2 leaves its route coverage to help and moves into a useful pressure position. D chooses whether to exploit the transition now, escape elsewhere, or switch target. A1 attempts to disengage. **The outcome is a future mechanic.**

**E — Protection and body hit.** A hostile effect reaches D; movement failed to avoid it; Active Defence controls only part of it; Protection intercepts part of the rest; a residual reaches the Leaf. Real Leaf damage occurs. D remains embodied and reassesses whether continued conflict is worth further biological risk. No HP was involved.

**F — open terrain** (doc 57 Scenario 6). D identifies the open southern route and moves toward it. The attackers decide whether to pursue or intercept. **Without concrete Movement and Pursuit mechanics, the outcome cannot be determined.** This document defines the interaction questions; it does not pretend to solve numerical chase balance.

**G — arriving reinforcement** (doc 57 §11–§12). A4 physically approaches from elsewhere and, until it arrives, contributes no local geometry. Depending on actual event order, D may leave before A4 enters, or A4 may enter before D leaves. Awareness stays separate from arrival. Threat Geometry changes only when physical presence actually changes.

### Summary diagrams

**Interaction loop** — not a UI or turn order:

```text
PERCEIVE RELEVANT THREAT
  ↓
ASSESS POSITION / OBJECTIVE / BODY RISK
  ↓
MOVE / DEFEND / PRESS / DISENGAGE
  ↓
THREAT GEOMETRY CHANGES
  ↓
PROTECTION MAY INTERCEPT HOSTILE EFFECT
  ↓
BODY MAY BE REACHED → BIOLOGICAL CONSEQUENCE IF HIT
  ↓
WARDEN REASSESSES
  ↓
CONTINUE / WITHDRAW / ESCAPE / SURRENDER / OBJECTIVE RESOLVES
```

**Defence layering** — different future attacks may interact differently:

```text
HOSTILE EFFECT
  ↓
CAN POSITION / MOVEMENT PREVENT CONTACT?
  ↓ if no
CAN ACTIVE DEFENCE REDIRECT / CONTROL IT?
  ↓ if no, or only partly
DOES PROTECTION INTERCEPT IT?
  ↓ residual
BIOLOGICAL MANIFESTATION BODY → REAL CONSEQUENCE
```

**Pursuit** — no timer:

```text
ESCAPE INTENT
  ↓
DEFENDER CREATES MOVEMENT ADVANTAGE / ROUTE
  ↓
ATTACKERS CHOOSE: pursue · intercept · hold the original stake · protect an ally
  ↓
GEOMETRY EVOLVES
  ↓
BREAK CONTACT   or   CONTACT / PRESSURE MAINTAINED
```

**Handoff** — no result predetermined:

```text
A1 UNDER SERIOUS PRESSURE
  ↓
A2 LEAVES PRIOR RESPONSIBILITY
  ↓
A2 MOVES INTO SUPPORTING POSITION
  ↓
HANDOFF WINDOW
  ├── defender exploits the transition
  └── group stabilises
  ↓
A1 disengages / repositions, if successful
```

## 16. Deferred concrete combat mechanics, and what this pass excludes

**Excluded by design** — every item belongs to later work:

- **Attacks:** buttons, combos, attack types, specials, ultimates, frame data, hit stun, combo scaling (AMO-Q027).
- **Moves:** Light/Heavy Attack, Dodge, Roll, Block, Parry, Dash, Shove — none is canonical (AMO-Q027).
- **Controls and camera:** key or stick mapping, dodge button, lock-on, camera mode, VR locomotion (AMO-Q023, AMO-Q024, AMO-Q059).
- **Numbers:** speeds, acceleration, turn radius, sprint duration, chase radius, melee range, attack radius, engagement distance, Break Contact distance, armour points, shield value, percentage reduction, recharge time.
- **Resources:** stamina, energy, endurance, dodge resource, sprint meter.
- **Crowd control:** stuns, roots, knockbacks, grabs, grapples, immobilisation; only generic displacement, route control and pressure are used here.
- **Hidden anti-gank mechanics:** damage scaling by attacker count, defender buffs, group debuffs, outnumbered immunity, automatic escape advantage (AMO-D174). If outnumbered counterplay works, it must come from movement, geometry, Defence, Protection, decision quality and attacker costs. **No hard lock either**: enough attackers never produce an inescapable lock by rule, and the defender never gains escape immunity (L74).
- **PvP governance:** safe zones, penalties, bounties, policing, reputation, clans, guild wars (AMO-Q008).
- **Networking:** ticks, rollback, latency compensation, reconciliation (AMO-Q123).
- **Combat UI:** directional indicators, health bars, threat arrows, radar, lock markers (AMO-Q044, AMO-Q132).

**Owners.** AMO-Q027 keeps attacks, concrete movement actions, abilities, interaction timing, matchups, skill ownership and body morphology. AMO-Q028 keeps concrete Break Contact conditions, movement rules, escape contests and pursuit mechanics. AMO-Q109 keeps Protection coverage, durability, directional behaviour, repair, equipment types and simultaneous-effect handling, and how damage changes a playable body. AMO-Q023 keeps controls. AMO-Q132 keeps conflict information. AMO-Q008 keeps governance. No new question was required.

**Product feeling.** The target is that preserving a living body feels like it requires skilful movement and Defence — not watching a health bar drain — and that **escape feels earned because space was created**, not selected from a menu. Desired mastery includes avoiding unnecessary body hits, using space, reading several threats, knowing when to disengage, preserving Protection and choosing biological risk deliberately (AMO-D163). An outnumbered Warden may show skill by reducing simultaneous pressure, creating Local Screening, isolating one participant, forcing a group rotation, changing routes and escaping — **with no promise that skill defeats arbitrary numbers**.

## 17. Requirements for the next prototype

This specification makes the following **designable and testable**, and claims none of them is solved: Break Contact; pursuit; interception; defence against two directions; Local Screening; handoff; Protection under several pressures. A prototype that tests them needs a concrete, disposable movement and pursuit instrument — explicitly non-canonical, as doc 56's were — because doc 57 showed geometry alone cannot decide them, and a hand-moved board is kinder to deliberate positioning than real time will be.

**Break Contact and Pursuit has a dedicated disposable paper prototype in [59](59_BREAK_CONTACT_AND_PURSUIT_PAPER_PROTOTYPE_V0.md)**, designed and not yet run. It does not extend or alter this document's qualitative definitions of Break Contact, Pursuit, Interception or handoff.

### Acceptance

| Test | Holds |
|---|---|
| **A** — moving the embodied Amorpho moves the real individual | §2 |
| **B** — no arena copy exists | §2 |
| **C** — the Tuber remains physically inside the body | §2 |
| **D** — post-fight rooting happens where the body actually is | §2 |
| **E** — avoiding a hit is distinct from Protection absorbing it | §6, §7, §8 |
| **F** — Protection is distinct from body health | §7 |
| **G** — a body-reaching effect creates real biological consequence | §8 |
| **H** — no passive Defence stat replaces skill and position | §6, §8 |
| **I** — two attackers can create more pressure than one | §4 |
| **J** — their pressure depends on actual geometry | §3, §4 |
| **K** — one opponent may sometimes reduce another's clean pressure through positioning | §5 |
| **L** — this is not automatic shielding | §3, §5 |
| **M** — several attackers cannot occupy identical perfect space without consequence | §3 |
| **N** — Escape is not a menu action | §9 |
| **O** — Break Contact is physical | §9 |
| **P** — Pursuit requires movement | §10 |
| **Q** — Interception differs from Pursuit | §10 |
| **R** — an open route is not automatically an Escape | §9 |
| **S** — Escape is neither guaranteed nor impossible | §9, §10 |
| **T** — A2 cannot instantly replace A1 | §11 |
| **U** — A2 must physically arrive in a useful support position | §11 |
| **V** — A1 must physically disengage | §11 |
| **W** — the defender may contest the transition | §11 |
| **X** — no handoff outcome is predetermined | §11, §15 |
| **Y** — terrain can help either side | §12 |
| **Z** — open terrain still needs meaningful Movement and Pursuit play | §12 |
| **AA** — terrain is not a stat modifier | §12 |
| **AB** — reinforcement has no local pressure before physical arrival | §13 |
| **AC** — arrival direction and timing matter | §13 |
| **AD** — event order matters | §13 |
| **AE** — physical presence does not grant perfect knowledge | §13 |
| **AF** — the Anchor is not tactical radar | §13 |

### Consistency

| Distinction | Holds |
|---|---|
| Movement ≠ teleportation; engagement ≠ arena lock | §2 |
| Position ≠ numeric buff | §3 |
| Active Defence ≠ Protection; Protection ≠ biological HP | §7 |
| Body hit = real body consequence | §8 |
| Break Contact ≠ button; Escape Attempt ≠ successful Escape | §9 |
| Open route ≠ guaranteed Escape | §9 |
| Pursuit ≠ automatic following; Interception ≠ teleportation | §10 |
| Isolation ≠ automatic kill | §5 |
| Handoff ≠ instant role swap | §11 |
| More attackers ≠ consequence-free independent damage streams — **but more attackers still increase pressure** | §4 |

**Decisions.** AMO-D177 (layered defence before the body; Active Defence distinct from Protection) and AMO-D178 (engagement, Break Contact, Pursuit, Interception and handoff are physical and relational). AMO-D122 and AMO-D176 carry dated clarifications. **No law was added**: L58 already says that Protection may stop the blow and the struck body cannot ignore it, and L74 that numbers create pressure and that escape is won through the World rather than a button.

**Result:** the geometry test gave enough evidence to design this interaction layer, not enough to claim final combat balance. The embodied Amorpho moves as a real body in the real World; position matters before damage; defence begins before the body is touched; several attackers are more dangerous only through positions they can physically hold; escape must be created. **The broader Cultivation ↔ Embodiment hypothesis remains untested until doc 52 is run with human testers.**
