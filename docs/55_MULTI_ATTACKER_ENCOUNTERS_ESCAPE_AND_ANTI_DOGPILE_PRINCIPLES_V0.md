# 55 — Multi-Attacker Encounters, Escape and Anti-Dogpile Principles, v0

**Status:** qualitative combat-architecture pass using owner-supplied design direction. It extends [36](36_COMBAT_RESOLUTION_SURRENDER_ESCAPE_AND_WITHDRAWAL_V0.md), [49](49_COMBAT_PILLARS_AND_BIOLOGICAL_ROSTER_STRATEGY_V0.md) and [54](54_CONFLICT_STAKES_AND_COST_OF_WITHDRAWAL_V0.md) to one Warden facing several. *Revised 2026-10-06:* sharpened with the owner's clarification that **group pressure is collective while biological consequence stays individual** (§7, §8, trace F); the disposable geometric test of these principles is designed in [56](56_ONE_VS_THREE_ESCAPE_GEOMETRY_PAPER_PROTOTYPE_V0.md) and **has not been run**. It defines no player cap, damage scaling, anti-gank buff, health, crowd-control value, escape timer, invulnerability, matchmaking, safe zone, criminal or reputation system, faction, control, move, camera, interface or code.

> **Numbers create pressure, not certainty.**

## 1. Purpose

The owner wants Amorpho to hold genuinely dangerous asymmetric encounters — one Warden in a valuable Amorpho set upon by several Wardens in theirs — where the defender's objective is no longer *defeat everyone* but **break away with the living manifestation and its core**. Chaotic, physical, *fight your way out* situations should be possible.

The opposite failure must be ruled out: **numerical superiority automatically guaranteeing the destruction of a beloved persistent individual.** Outnumbered combat should be dangerous, should not be fair, and should not guarantee escape — and attendance alone must not become a deterministic way to delete a plant someone has raised for years.

## 2. Numerical superiority

> **Numerical superiority increases tactical pressure, not deterministic outcome** (AMO-D174).

More attackers matter: more threat directions, less space, stronger pursuit, more chances to intercept, higher biological risk. Three attackers are more dangerous than one. But *four attackers* does not inherently mean *manifestation destruction guaranteed*.

**Destruction requires sustained successful control.** To destroy a resisting manifestation, a group must generally keep contact, prevent escape, overcome protection, land real body-reaching damage and keep doing so against resistance. **Numbers help achieve that; they do not substitute for it.**

**No artificial equality either.** A lone Warden attacked by five prepared opponents is in serious danger, and that is acceptable. There is no automatic stat boost, damage immunity, per-attacker damage reduction, scaling armour, escape invulnerability, hidden comeback multiplier or numeric diminishing return. Counter-pressure comes from **geometry, skill, preparation, logistics, persistent cost and disengagement** — never from a defender buff.

## 3. Escape as a combat objective

When outnumbered, a Warden may rationally stop trying to beat everyone and make the objective **escape with the manifestation**. That is a legitimate objective, not a failure (AMO-D175).

> **Escape** is successfully creating enough physical and tactical separation that the opponents can no longer maintain the encounter or prevent departure.

It is not a menu command, instant disengagement, surrender or teleport (AMO-D125). Two things are distinguished:

- **attempting escape** — the Warden changes objective toward disengagement;
- **successful escape** — the encounter is actually broken.

Turning away is not escaping; attackers may pursue. No distance, duration or exact condition is defined.

> **An outnumbered Warden can win their immediate survival objective without defeating anyone.** Creating an opening, breaking contact and leaving with body and core intact is success.

**Escape can require fighting one's way out.** The owner's experiential direction — fighting *through* a crowd rather than conducting several formal duels at once, shoving through pressure, surviving contact, making a gap, keeping moving — is recorded as a possibility, not a style mandate or a presentation:

```
SURROUNDED, PRESSURED
  → survives exchanges
  → creates a local positional advantage
  → breaks part of the enclosure
  → gains a path
  → attackers pursue
  → creates enough separation
  → encounter ends by successful escape
```

**Escape is preservation of a persistent individual, not retreat from a match.** Body damage is real, so one-versus-many pressure can turn biologically dangerous quickly — protection degrading, body-reaching hits, a lowering Recovery Ceiling, Collapse, core exposure (AMO-D120, AMO-D141).

## 4. Enclosure and pursuit

**Preventing disengagement is active work.** The attackers' objective may become *stop the target leaving*: surround, intercept, pursue, deny routes, pressure protection, force the defender back into engagement. A target that wants to leave does not stay trapped automatically; attackers must keep up geometry, pursuit, interception and pressure. That gives skill to both sides. No move or crowd-control mechanic is designed.

**Pursuit is part of the encounter.** While attackers chase, positioning and body risk continue, and the chase runs through the persistent World with no arena boundary (AMO-D009).

**Neither rooting nor leaving the body is an escape.** Rooting removes mobility and returns the individual to biology where it stands; under pursuit it may be dangerous, and it is never a universal safety teleport (AMO-D032). Exiting embodiment returns the Warden to the human body and leaves the plant exactly where the Amorpho was (AMO-D129), so de-embodiment does not solve pursuit or capture. **Escape stays physical.** No rooting-under-combat rule is designed (AMO-Q043).

## 5. Spatial congestion

> **More bodies create congestion as well as power** (AMO-D176).

No numeric diminishing return is introduced; congestion is meant to **emerge from embodied space**. Several attackers may obstruct each other's approach, compete for useful angles, block routes, interfere with each other's positioning, expose one another to displacement and find coordinated timing harder. Combat must therefore **not** be architected so that each extra attacker is an independent damage stream with no spatial cost: position, angle, space, line of approach and obstruction all apply.

**Allies may interfere with each other** — movement, attack opportunities, pursuit lines, positioning — and an attacker does not automatically pass through an allied body. Full friendly fire and any collision system are not designed.

**Geography is a combat resource.** Narrow passages, obstacles, vegetation, elevation, built environment and open ground may all shape enclosure, approach, escape and pursuit. No terrain mechanic is designed.

## 6. Defender skill and geometry

> **Outnumbered survival is partly geometry management.**

Design direction for skill expression, with no technique defined: keeping one attacker between the defender and another, forcing attackers into poor angles, using narrow terrain, opening gaps by displacement, drawing pursuit into a line, buying moments of separation. Movement, positioning, defensive timing, target prioritisation, risk judgement and knowledge of terrain must keep real influence.

**Isolation is a first-class defender opportunity.** The defender need not defeat the group; they can target its **coherence**. Overcommitment, displacement, poor spacing, terrain, a pursuit error or the defender's own repositioning may leave one attacker locally cut off from the group's effective support:

```
GROUP COHERENCE
  → one attacker becomes locally isolated
  → the defender pressures that individual
  → that attacker must defend their own living manifestation
  → the allies choose whether and how to react
  → group geometry changes
  → an escape opening may appear
```

Isolation does **not** require knocking out, defeating or destroying the attacker. Forcing them defensive, wearing down their protection, making body risk credible, displacing them or making them pull back is enough if it **changes local control**. *An isolated attacker should have to care about their own living body again.*

Two opposite rejections hold together: *outnumbered = automatic loss*, and *high skill = guaranteed escape from any number*.

**Preparation is counter-pressure** — protection, mobility configuration, body condition, starting position, environment, known routes (Pillar 9, [49](49_COMBAT_PILLARS_AND_BIOLOGICAL_ROSTER_STRATEGY_V0.md)). No builds are designed.

**Requirements for later design**, recorded rather than solved:

- combat must not assume one locked target against one locked target, and must support several threats and rapid shifts of attention (AMO-Q023, AMO-Q027);
- defence must be able to account for threats from front, side, rear and several angles at once, rather than being built as if only one opponent exists;
- protection must be able to answer what happens when it is stressed from several directions or by repeated attacks (AMO-Q109);
- several attackers create **informational pressure** — directions, protection state, escape geometry, body condition, intent — and that is a future usability challenge, not a camera decision (AMO-Q024, AMO-Q044).

## 7. Group coordination

**Group play is not prohibited.** Groups may cooperate, plan, surround and pursue, and should gain real advantage from timing, positioning, pursuit coordination and control of escape routes — positive social skill, not raw numbers. **Good coordination materially increases danger.**

**Poor coordination creates openings.** Crowding, mistimed attacks, blocked routes and bad pursuit may let the target escape — the intended counterweight, with no defender bonus needed.

> **Group pressure is collective; biological consequences remain individual.**

A coordinated group produces enclosure, several threat directions, continuous pressure, pursuit and escape denial *together* — and every member contributes through **one actual living manifestation carrying one persistent core**. The group is not a shared health pool and absorbs nothing collectively; individual bodies do. Its advantages stay real and large — more angles, space control, pursuit coverage, rotating pressure, closing routes, dividing the defender's attention — and **three coordinated attackers are genuinely more dangerous than one**. The point is not symmetry.

**Commitment to the group can cost an attacker individual freedom.** Holding an angle, staying close enough to deny a route, pursuing hard, keeping formation, committing to an attack or occupying cramped space beside allies may leave less room to evade, position defensively, orient protection, keep a retreat route or stay flexible. That is not a penalty; it emerges from **position, commitment and geometry**.

**There is no group-status damage modifier.** Being part of a group never makes anyone take more damage, and there is no hidden swarm vulnerability. Damage still follows the one causal chain — incoming effect → protection and defence → residual effect → the actual body → real biological consequence (AMO-D122) — and any added danger comes from exposure, reduced freedom, isolation and hits that actually land.

**Individual risk can fracture collective pressure.** One attacker takes meaningful body damage; that Warden reassesses their own biological risk; they defend, withdraw or reposition; the enclosure weakens; the defender gains an opening. No morale meter, automatic group-break rule or scripted retreat: each attacking Warden makes their own judgement (AMO-D173).

**Attackers may need to protect one another** — covering an exposed member, rotating a damaged one away, holding space for another's retreat, giving up pursuit pressure to restore coherence. No formation is defined. *Maintaining collective advantage may require spending pressure to preserve individual bodies; if allies protect an exposed member, they may have to give up pressure somewhere else.* The swarm picture is inspiration only, with no zoological claim: **a group can be hard to disrupt as a whole while one badly positioned member is acutely vulnerable as an individual.**

**Local objectives shift with spatial state**, with no scripted phases: attackers begin by preventing escape and the defender by breaking the enclosure; once one attacker is exposed, the attackers' objective becomes restoring coherence or protecting that member, and the defender's becomes exploiting the opening.

The aim is not to prevent group play; it is to prevent **group size alone** from guaranteeing destruction.

## 8. Biological cost to attackers

> **Attackers risk their own living manifestations.**

Every attacker carries a real manifestation, a persistent core, Biological Deployment Cost, interrupted productive opportunity and body-damage risk (AMO-D161). Coordinated aggression is not biologically free. A long group pursuit means each attacker stays embodied, interrupts their own rooted biology, travels physically, exposes their own manifestation and carries their own core into danger (AMO-D136, AMO-D145) — so long hunts are naturally expensive, with no artificial pursuit tax.

Attackers therefore face their own decision: ***is this target still worth chasing?*** No pursuit meter.

**A larger group brings more pressure and more at risk.** More attackers can mean stronger control, more pursuit and more containment, and also more manifestations, more persistent cores, more interrupted opportunity and more individual history and Attunement inside a dangerous encounter. Nothing reduces that to a balancing formula.

## 9. Persistent World and logistics

**No instant dogpiling.** A Warden cannot simply *join the fight* from anywhere. Their embodied body must physically be at the location, able to reach the target and able to take part; there are no teleporting reinforcements by default (AMO-D028, AMO-D129).

> **Reinforcement is a World event, not a change in match population.** An arriving attacker arrived in the World, and the encounter evolves; numerical advantage stays grounded in logistics, not arena slots.

## 10. Destruction, custody and changing objectives

**Destruction opens a new conflict phase.** If attackers prevent escape and destroy the manifestation: a viable Tuber lies exposed where the body fell, the Warden is back in their human body elsewhere, and the attackers are physically beside the core ([37](37_MANIFESTATION_DESTRUCTION_TUBER_CORE_VIABILITY_AND_PHYSICAL_DROP_V0.md), AMO-D130). The conflict may shift from *destroy the body* to **custody or rescue of the exposed Tuber** — and custody still grants no ownership, binding or Attunement (AMO-D065, AMO-D169). Attackers may even prefer capture to destruction of the core; no targeting is designed.

**Objectives move with the World.** A defender may begin by protecting access or completing something, turn to preserving the manifestation under serious pressure, and after losing the body turn to recovering the Tuber. No scripted phases (AMO-D172, AMO-D173).

**Escape and the stake are separate outcomes.** A defender who escapes may save an irreplaceable individual and still lose the immediate stake — attackers gain the location, access or objective. *Successful biological escape can coexist with losing the encounter's stake*, and escape can be a strategic victory and a conflict defeat at once. Whether that was worth it is the player's judgement; there is no single results label ([54](54_CONFLICT_STAKES_AND_COST_OF_WITHDRAWAL_V0.md)).

**A defender can win with no one defeated.** The target escapes, the attackers remain intact, no one surrenders, nobody is knocked out and no body is destroyed: preservation and disengagement were achieved, and that is a valid resolution (AMO-D124).

## 11. The anti-dogpile boundary

> **Deterministic gang destruction is a product failure.** If the optimal group strategy becomes *bring enough bodies, surround the target, and destruction is certain regardless of the defender's skill, preparation, terrain or escape attempt*, persistent individuals become deletable by griefing, and attachment collapses (AMO-D174).

Two sharper forms of it: **each additional attacker must remain an individually punishable living participant, not another consequence-free damage source**, and **a group gains power through coordination, not immunity from consequence**.

That constraint weighs more in Amorpho than elsewhere: long Attunement and history make individuals personally irreplaceable (AMO-D169), so the destruction of a persistent body must be the result of meaningful World, conflict and combat play — never trivial numerical bullying.

**Hunts are still allowed.** A group deliberately hunting a particular Amorpho can be a powerful emergent story. The requirement is that **the hunt creates danger and drama, not guaranteed deletion by attendance count**. Persistent destruction remains possible.

**Combat alone may not be enough, and that is said honestly.** Attackers' biological costs discourage some reckless hunting; they are not assumed to solve deliberate griefing. Future World, social and governance layers — law, reputation, protected locations, social consequence, Warden governance, security — may be needed and are **not designed here** (AMO-Q008). **Safe regions are not assumed**: nothing is solved by declaring PvP disabled somewhere, and combat itself should stay viable under asymmetry.

## 12. Worked traces

**A — successful crowd escape.** One Warden is pressed by three attackers. Protection absorbs early attacks; the attackers try to enclose. The defender positions so that the attackers obstruct one another. One hit reaches the body. The defender abandons the original objective, makes an opening, breaks the enclosure, is pursued, and gains enough separation to escape. The manifestation survives; the attackers take the location and stake; the defender later roots and rehabilitates. **No one was knocked out.**

**B — failed escape.** The defender tries to leave; the attackers coordinate well and keep closing the lanes. Protection deteriorates, body damage accumulates, and the defender stays trapped until the manifestation is in serious biological danger. **The trace stops here**: what follows may still be surrender, a change in the attackers' objective, a later escape — or destruction.

**C — attackers overcommit.** A group chases one target for a long time. Every attacker stays embodied with their own biology interrupted; one takes body damage; the target escapes. The group now carries real persistent consequences despite its numbers. **Pursuit was not free.**

**D — destruction, then a contest for the core.** The group prevents escape and destroys the manifestation. A viable Tuber drops; the Warden is back in the human body; the attackers are at the site. Tuber custody is now the stake, and ownership and binding are unchanged. **The trace stops here.**

**E — a beloved individual targeted.** A Warden fighting with a long-attuned individual realises a coordinated group intends to destroy it. The objective becomes preservation; the Warden willingly abandons the original stake; survival matters because the relationship history does. No emotional stat is involved.

**F — breaking coherence.** Four attackers press one defender and hold most useful escape directions. One commits too deeply trying to close the last route. The defender repositions and briefly isolates that attacker, whose defensive freedom is now constrained, and lands a counter that puts their body at real risk. That attacker must put their own manifestation first; their allies shift spacing to support them; the enclosure opens; the defender breaks contact and escapes. The group kept its numerical superiority and still failed to destroy the target; one attacker carries persistent biological damage away; and the attackers may still have won the original stake. **No numerical modifier was involved.** This is intended procedure, not an observed result: whether geometry really allows it is what doc 56 tests.

## 13. Acceptance and consistency audit

| Test | Result |
|---|---|
| **A** — three attackers more dangerous than one | §2 |
| **B** — three attackers do not guarantee destruction | §2, §11 |
| **C** — escape rather than defeat can succeed | §3 |
| **D** — attackers must actively prevent disengagement | §4 |
| **E** — bodies complicate group coordination | §5 |
| **F** — poor coordination opens escape | §7 |
| **G** — good coordination materially increases danger | §7 |
| **H** — attackers carry biological and opportunity cost | §8 |
| **I** — reinforcements arrive physically | §9 |
| **J** — escape may concede the stake | §10 |
| **K** — destruction may turn into a custody contest | §10 |
| **L** — no stat-based anti-gank system | §2 |
| **M** — an attuned individual can be hunted without being trivially deletable | §11 |
| **N** — group pressure collective, consequence individual, no group damage modifier | §7 |
| **O** — isolation of one attacker can force the group to react | §6, §7, trace F |
| **P** — attackers may have to protect one another at a cost in pressure | §7 |

| Distinction | Holds |
|---|---|
| Outnumbered ≠ automatically destroyed | §2 |
| Escape ≠ surrender; escape attempt ≠ successful escape | §3 |
| Successful escape ≠ winning the stake | §10 |
| More attackers = more pressure, and more congestion and cost | §5, §8 |
| Group play stays possible; persistent destruction stays possible | §7, §11 |
| Attendance count ≠ guaranteed deletion | §11 |
| Group advantage ≠ group immunity; group support ≠ shared health | §7 |
| Individual exposure ≠ damage multiplier; isolation ≠ automatic kill | §6, §7 |

## 14. Deferred implementation

AMO-Q028 keeps escape contests, pursuit, enclosure and multi-party encounters in their contexts. AMO-Q027 keeps the combat structure that must support several threats, congestion and group interference. AMO-Q109 keeps protection and hit determination under multi-directional pressure. AMO-Q023 and AMO-Q024 keep controls, targeting and camera, which must not assume a one-on-one lock. AMO-Q008 keeps hostile behaviour, griefing and any future governance or protected-location layer. AMO-Q043 keeps rooting rules, including rooting under pressure. No new question was required.

*Revised 2026-10-07:* movement, Defence, Protection, Break Contact, pursuit, interception, Local Screening, Local Isolation and handoff interaction now have their qualitative owner in [58](58_MOVEMENT_DEFENCE_AND_PROTECTION_INTERACTION_V0.md) (AMO-D177, AMO-D178, AMO-D176 revised). The principles here are unchanged.

**Result:** being outnumbered in Amorpho should be frightening and survivable — a scramble through bodies and terrain toward open ground, with a living plant at stake on one side and real living plants spent on the other. Numbers decide how hard it is, never that it is already over.
