# 36 — Combat Resolution, Surrender, Escape and Conscious Withdrawal, v0

**Status:** conceptual combat-resolution pass using owner-supplied design direction. It establishes how an Amorpho encounter normally ends. It defines no HP value, KO mechanic, frame data, move, input, escape window, pursuit rule, armour or shield figure, matchmaking, ranking, conflict reward or penalty, and it designs no Human-versus-Amorpho combat.

> **A fight ends when the conflict resolves, not when a body fails. Winning need not destroy the opponent; losing need not cost the manifestation.**

## 1. Purpose

[35](35_COMBAT_PROTECTION_MANIFESTATION_BODY_DAMAGE_AND_BIOLOGICAL_PERSISTENCE_V0.md) established that the Warden fights through the actual biological manifestation, that protection decides what reaches it, and that body-reaching damage is real and persistent (AMO-D120–AMO-D123). That makes one question unavoidable: **how does an encounter normally end?**

The conventional answer — *deplete a meter, produce a knockout, end the fight* — is explicitly **not** this game's foundation. When the fighter's body is a living individual the player has cultivated, a resolution model that requires consuming a body to zero would make every ordinary fight an act of destruction. Amorpho resolves encounters through decisions and conflict outcomes instead.

## 2. Conflict resolution, not mandatory bodily destruction

> **An Amorpho fight is a conflict under escalating risk, not inherently a contest to destroy the opponent's manifestation.**

An encounter may end while both manifestations still exist, both remain biologically viable, and both remain capable of continuing. It ends because the **conflict** reached a resolution.

Two consequences follow immediately:

- **There is no universal knockout requirement.** No rule says an encounter continues until one body can no longer move. Some form of conventional incapacitation may still exist later where it is useful; it is not the foundational resolution rule.
- **Combat capability is not a death countdown.** A future combat meter may answer whether this Amorpho can keep participating effectively; it does not measure how close a living manifestation is to biological death, and resolution is not structurally tied to consuming the body (AMO-D121).

## 3. Four resolution families

These are conceptual families, not controls, states or an exhaustive list. They are kept **semantically distinct** and must not collapse into one generic “quit fight”:

| Family | What the side doing it is choosing | What it is not |
|---|---|---|
| **Surrender / Yield** | accepting defeat and the opponent's immediate conflict outcome | not a request to be spared further attack as a favour |
| **Escape / Flee** | preserving autonomy and position by physically disengaging and leaving | not a menu button labelled *lose* |
| **Conscious Withdrawal** | judging that further biological or strategic cost is no longer worth the conflict, and ending participation | not a failure state, and not conditional on being beaten |
| **Objective Resolution** | nothing — the conflict's goal was achieved or became impossible, so continuing is pointless | not a draw declared by a timer |

Surrender **concedes**; escape **leaves**; withdrawal **disengages by judgement**; objective resolution **ends the reason to fight**. Their eventual conflict consequences may differ — conceding an objective, abandoning a location, or accepting whatever context imposes — and none of those consequences is defined here.

## 4. Winning and losing, redefined

> **A player may win because the opponent yields, withdraws, flees, loses the objective, or can no longer justify continuing.** No knockout is required.

> **A player may lose an encounter while the manifestation remains alive, viable and usable later.** Losing a fight is not losing a body.

Because destruction is not the win condition, objective-shaped conflict becomes natural: holding a location, protecting something, reaching somewhere, denying access, buying time, taking control. No mission type, arena or contest format is designed here (AMO-Q028).

## 5. The encounter's end is not the embodiment's end

**Combat participation and embodiment state are separate.** An encounter ending — by surrender, withdrawal, escape or objective resolution — does not by itself return the Warden to the human body or root the plant:

- a Warden who surrenders or withdraws may remain embodied afterwards;
- a surrendered Amorpho is not thereby immobilised, and may later move away if the context permits;
- escape *requires* continued embodiment while it happens, and afterwards the player may travel on, seek safety or root.

Rooting remains the ordinary way embodiment ends, and it remains a decision rather than a consequence of losing (AMO-D032, [09](09_EMBODIMENT_AND_ASTRAL_TRANSFER.md)). Whether any future combat-state failure forces exit is a separate question and stays open (AMO-Q113). Terminal loss of the manifestation ends embodiment for the reason already established — there is no body left (AMO-D118, L57).

## 6. Conscious Withdrawal

A Warden may leave while still combat-capable, still protected, still tactically ahead. The reason is not weakness but arithmetic the game never performs for the player:

> The expected additional biological risk is no longer worth this conflict.

**Withdrawal does not require Functional Collapse**, and it does not require combat-state exhaustion. Shields failing, armour compromised and the first real injuries reaching the Leaf are already sufficient grounds; so is a valuable individual and a trivial objective. In system terms this is management of a living body, not cowardice, and nothing in the architecture may treat it as a failure state.

What the decision weighs — the objective's value, current biological condition, protection state, how much this particular individual matters, which other Amorphos exist, appetite for risk, the wider strategic position — is left to the player. **There is no single universal optimal stopping point**, no utility calculation, and no score that pronounces the choice irrational. A player may withdraw early precisely because this individual is rare or valued, and another may use a currently less important manifestation aggressively; the architecture never labels an individual expendable.

The opposite choice is equally legitimate. A Warden may knowingly continue after protection fails and injuries accumulate. There is no morality meter, no forced surrender, and no system that protects players from their own risk decisions.

## 7. Escalation: fighting to manifestation destruction

> **Fighting until a manifestation is biologically destroyed is possible, but it is not the ordinary resolution model.** It is escalation beyond normal combat, chosen by refusing the exits.

Terminology matters here. Destroying a Leaf or Bloom is **not** killing the individual: the Tuber persists, and the lifecycle may continue through Replacement, consolidation, dormancy or a later cycle (AMO-D115, AMO-D118, [33](33_MATURE_LEAF_FUNCTIONAL_COLLAPSE_BOUNDARY_V0.md), [34](34_EMBODIMENT_ACROSS_TERMINAL_MANIFESTATION_COLLAPSE_V0.md)). This document therefore uses **fight to manifestation destruction** rather than “fight to the death”. A conflict that genuinely threatened the persistent individual would be a far more extreme category, and none is designed or authorised here.

Because the manifestation is cultivated and persistent, continuing past the exits means risking something the player may care about. That is intentional, and it is the product's emotional question:

> Is this victory worth risking this manifestation?

No emotional value is quantified. Related emergent possibilities are recorded without design: an opponent may be able to read failing protection, visible injury and a refusal to withdraw as escalation and intent, and persistent refusal may come to matter socially or strategically. No information model, interface cue or reputation system follows (AMO-Q028, AMO-Q109).

## 8. What future mechanics owe these families

Product requirements, not mechanics. Each pins down a failure mode rather than a value:

| Requirement | Failure mode it prevents |
|---|---|
| **Surrender must be a credible preservation strategy** | if yielding costs nearly as much as losing the manifestation, players rationally fight to destruction |
| **Surrender must not be free** | if it costs nothing in the conflict, risk is escaped trivially whenever it rises |
| **Surrender normally ends hostile continuation within the encounter** | a surrender the opponent may simply ignore is not surrender |
| **Escape must be neither guaranteed nor impossible** | instant flight is not gameplay; impossible flight forces every fight toward destruction |
| **Meaningful exits must exist before biological destruction** | without them, persistent body damage becomes an unavoidable tax rather than an accepted risk |

**Escape carries agency.** It is a contested outcome rather than a passive defeat command: future designs may require creating distance, breaking pursuit, reaching an exit, using movement, terrain or abilities, and the opponent may pursue, intercept or prevent disengagement. Nothing about how is decided (AMO-Q023, AMO-Q026, AMO-Q028).

**Non-consensual continuation is a separate future problem.** Actors who ignore surrender, non-player threats that do not recognise it, and whatever rules constrain hostile behaviour between players belong to later work (AMO-Q008, AMO-Q028). Ordinary Warden-versus-Warden combat is expected to have a surrender concept that means something.

Some contexts may later permit simple mutual disengagement while others require creating space, crossing a boundary or conceding an objective. Withdrawal is therefore **context-dependent**, and no context taxonomy is created here.

## 9. Encounter scale and conflict scale

> **Resolving an encounter does not necessarily resolve the conflict.**

A Warden may lose or leave one fight while the dispute persists, the objective stays contested, the opponent remains in the world and another confrontation stays possible. In a persistent world that distinction is structural, not flavour (AMO-D009).

So losing one encounter does not erase the Warden's agency in the larger conflict. Continuation may later come through another Amorpho, relocation, allies, equipment, the Human, or simply another time and place — none of it designed here. What is fixed is the shape:

```text
ENCOUNTER               one fight, resolved by yield, escape, withdrawal or objective
   ↓  does not settle
CONFLICT                the dispute, which may continue by other means
```

**Conflict identity belongs partly to the Warden; the body belongs to the chosen Amorpho.** The same opponent may face one Warden through several manifestations over time, which allows rivalries that outlive any single body and distinguishes Amorpho from a fixed-character fighter. No social, rivalry or history system is designed (AMO-Q120, AMO-Q028).

Sequential embodiment makes this work without breaking anything: Amorpho A withdraws, survives, and the Warden may later return using Amorpho B. **One Consciousness still holds** — there is no tag-team switching inside an encounter, no simultaneous bodies, and changing Amorpho requires whatever embodiment and world process exists, with no transition timing decided (AMO-D028, AMO-D101, L22, AMO-Q040).

## 10. Biological continuity between encounters

Nothing resets. Two Wardens who fight again later bring whatever biological history survived: scars, reduced Structural Integrity or Functional Capacity, altered protection, a different manifestation entirely. There is no rematch that restores both bodies to pristine condition, and the only way a body is genuinely fresh is that it is genuinely new — a later manifestation built by the same persistent individual (AMO-D074, AMO-D113, AMO-D120).

A withdrawn, damaged Leaf may root, stabilize and regain useful function, and may be embodied again if the gates permit, so **withdrawal is not automatically retirement for the season** ([24](24_SAME_PHASE_LEAF_RECOVERY_V0.md), AMO-Q103). Equally, a Warden may decide a manifestation has done enough, root it, protect its remaining biological season and wait for a future one. Both are valid; neither is scheduled by the game.

Roster depth therefore distributes combat exposure — one individual fights and is rested, another is used later — and the reason to rotate stays biological rather than an availability clock (AMO-D123, [35](35_COMBAT_PROTECTION_MANIFESTATION_BODY_DAMAGE_AND_BIOLOGICAL_PERSISTENCE_V0.md) §12). No artificial fighter lockout is required, and none is created.

## 11. The Human Warden is a deferred domain

The owner has identified a future direction in which the Human may physically encounter Amorphos, need protection, carry a separate condition model and participate in conflicts directly. **None of it is designed here**, and it requires its own dedicated pass (AMO-Q130).

Two guard-rails apply meanwhile. There is **no automatic Human substitution**: an Amorpho losing an encounter does not make the Human appear and continue the fight. Human involvement is a separate action in a separate context, subject to One Consciousness and to physical location — the human body is somewhere specific and no teleportation is implied (AMO-D028, AMO-D029, L23).

## 12. Worked traces

**A — surrender preserves the manifestation.** Protection fails and the first real injuries reach the Leaf. The objective is already effectively lost. The Warden yields; the opponent's conflict outcome stands, the encounter ends, and the manifestation survives scarred and viable. Whatever the conflict cost — objective, position, possession — is context, not biology, and none of it is defined here.

**B — contested escape.** The Warden chooses to disengage rather than concede. Escape is played out rather than declared: the opponent may pursue and try to prevent it. If it succeeds, the Warden is still embodied, still free, and may travel on, seek better conditions or root. If it fails, the encounter continues and the risk continues with it. No mechanic is specified.

**C — conscious withdrawal while ahead.** A rare, long-cultivated individual is tactically winning, but a shield is gone and the objective is minor. The Warden stops participating and leaves with a nearly intact manifestation, losing nothing biologically important and gaining nothing from the conflict. **No system calls this a loss.**

**D — objective resolution.** The fight existed to hold a location until something else completed. It completes. Continuing has no purpose, so the encounter ends with both manifestations intact and no yield from either side.

**E — escalation to manifestation destruction.** The Warden refuses surrender, withdrawal and escape. Effects keep reaching the body, damage accumulates with recovery suspended, and the Leaf crosses into committed terminal decline and eventually ceases to exist; embodiment ends with it ([33](33_MATURE_LEAF_FUNCTIONAL_COLLAPSE_BOUNDARY_V0.md), [34](34_EMBODIMENT_ACROSS_TERMINAL_MANIFESTATION_COLLAPSE_V0.md), AMO-D118, AMO-D123). The Tuber remains alive unless separately harmed. This was an accepted risk, not a punishment, and not the death of the individual.

**F — the conflict continues.** After trace A the dispute is unresolved. Later, the same Warden returns using a different individual, or the same individual's later manifestation, and meets the same opponent again. Both arrive with their actual biological history. The rivalry belongs to the Wardens; the bodies are whichever manifestations exist then.

## 13. Deferred mechanics and acceptance

AMO-Q026 owns the combat side: how an encounter is represented, what surrender, escape, withdrawal and objective resolution actually require of the player, combat-state semantics, any incapacitation concept, and what determines that an effect reaches or destroys a body. AMO-Q028 owns where and against whom combat happens, including pursuit, contest of escape, and hostile behaviour between players; AMO-Q008 owns the anti-griefing side of ignored surrender. AMO-Q023 owns controls; AMO-Q109 owns protection architecture and how condition changes a playable Amorpho; AMO-Q113 owns forced exit; AMO-Q103 owns post-withdrawal recovery; AMO-Q120 may record encounter history; AMO-Q130 owns Human physical conflict. One new question was required (AMO-Q130); no conflict reward, penalty or balance figure is defined.

| Check | Result |
|---|---|
| No mandatory KO | An encounter may end with both manifestations intact and capable (AMO-D124). |
| Winning | Yield, escape, withdrawal or objective resolution are all wins for the other side; incapacitation is not required. |
| Losing | A player may lose while the manifestation stays alive, viable and usable later. |
| Four families | Surrender, escape, withdrawal and objective resolution stay semantically distinct (AMO-D125). |
| Encounter ≠ embodiment | Ending a fight does not force de-embodiment or rooting (AMO-D126). |
| Withdrawal timing | Neither Functional Collapse nor an empty meter is a precondition. |
| Escalation | Fighting to manifestation destruction is permitted and exceptional, never the default (AMO-D127). |
| Terminology | Manifestation destruction is not death of the persistent individual. |
| Conflict scale | Resolving an encounter need not resolve the conflict; Warden agency survives a lost fight (AMO-D128). |
| Continuity | No rematch reset; bodies carry their history, and only a new manifestation is fresh. |
| One Consciousness | Sequential embodiment only; no in-encounter switching. |
| Human | Deferred entirely, with no automatic substitution and no teleportation (AMO-Q130). |

**Result:** ordinary Amorpho combat ends the way conflicts end — someone yields, someone leaves, someone decides the price is too high, or the point of fighting disappears. Destruction of a living manifestation sits beyond those exits, reachable only by choosing to pass them, and even then it costs a body rather than an individual.
