# 04 — Transformation and Combat

**Status:** conceptual. The principles here are accepted; almost every concrete rule is open. Nothing in this document chooses a control scheme, camera, engine or netcode.

## 1. Plants are plants

*Amorphophallus* plants in Amorpho are normally plants. They live, grow, flower, reproduce and die according to the world simulation. They do not walk around, and they are not creatures in disguise.

## 2. The mechanism

Awakening requires a magical mechanism that is not yet settled. A single artifact — an amulet, a belt — was the founding concept; a dedicated ritual room inside the player's home is now the leading one, and a combination of place and object remains possible. Its name, origin story and role in the fiction are open (AMO-Q021, AMO-Q039). "The artifact" is a placeholder term for whatever this turns out to be.

## 3. Transformation is astral transfer

Transformation is the bridge between the two gameplay layers, and its mechanism is **astral transfer**: the player's consciousness leaves their human body and inhabits one eligible individual, which becomes an active Amorpho (AMO-D028, AMO-D029).

```
Human / World layer                          Amorpho / Combat layer
─────────────────────                        ──────────────────────
human body  ──────────▶ remains in the world, unattended
     +
consciousness ─────────────astral transfer──▶ inhabits one individual,
                                              which becomes an active fighter
individual plant in a pot,  ◀──rooting───────
greenhouse or landscape
```

Accepted:

- The Amorpho **is** the individual plant, temporarily animated — not a separate creature, copy or summon (L16, AMO-D030).
- The human body does **not** transform, vanish or leave the world; it stays somewhere, and that somewhere matters (AMO-D029).
- Only **one** body is inhabited at a time, however many plants a player owns (AMO-D028).
- Only a plant that is biologically stable enough can be inhabited — alive is not the same as inhabitable (AMO-D031).
- Awakening is **temporary**, and it ends by rooting, which returns the individual to plant state and to its real relationship with its environment (AMO-D032).
- The animated fighter uses the **actual** biological manifestation as its body, so protection decides what reaches it and an effect that does reach it is real biological damage that persists after embodiment (AMO-D120, AMO-D122, L58). **Combat state is not biological condition:** the two are distinct but coupled domains with no proportional mapping (AMO-D121). See [35](35_COMBAT_PROTECTION_MANIFESTATION_BODY_DAMAGE_AND_BIOLOGICAL_PERSISTENCE_V0.md).

The full model is in [09_EMBODIMENT_AND_ASTRAL_TRANSFER.md](09_EMBODIMENT_AND_ASTRAL_TRANSFER.md), including rooting, rescue and equipment.

Open (AMO-Q022): what else makes a plant suitable (age, life-cycle stage, size, bond, species); how long awakening lasts; and what it costs. That it *can* have consequences for the plant afterwards is now settled — damage reaching the body is biological and persists (AMO-D120) — while the combat mechanics that produce it are not. Finer questions are tracked as AMO-Q039–AMO-Q043.

## 4. From species to fighter

A real species defines the **identity and visual foundation** of an Amorpho character. Its combat design is authored game design, driven by balance, mastery and fun (AMO-D006):

- A large real plant is not automatically a stronger fighter.
- A botanical trait is not automatically a combat mechanic.
- Real characteristics are welcome as **inspiration** — for silhouette, animation, move themes, personality, humour — but never as specification.

Combat design belongs to Game Design Data (Layer 2). It references species by their permanent `AMO-SP-` IDs and never needs botanical justification (AMO-D021).

Individuals of the same species may differ in appearance through variation and history. Whether individual differences also affect combat is part of AMO-Q025.

An individual also has more than one **body** over its life. Leaf form and Bloom form are different biological manifestations of the same persistent individual, and Bloom is intended as a rare, short superstate with capabilities unavailable otherwise — not the same fighter with better numbers (AMO-D058, AMO-D059). Phase-specific abilities and the relationship between damage to a temporary structure and damage to the persistent core are open (AMO-Q086). See [15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md](15_LIFE_CYCLE_ASTRAL_ANCHORS_AND_AVAILABILITY.md).

## 5. Combat pillars

Combat is intended to become a fully developed, real-time, skill-based fighting game (AMO-D008):

- real-time movement and positioning;
- timing;
- blocking;
- attacks and counters;
- learnable moves;
- combinations and input sequences;
- individual character mastery;
- multiple **fighting-game rounds** per match.

"Rounds" means fighting-game rounds. It does **not** mean selecting actions in turns.

**How an encounter ends is not a knockout rule.** An Amorpho fight is a conflict under escalating risk: it normally resolves through surrender, escape, conscious withdrawal or objective resolution, and may end with both manifestations intact and still capable. Winning need not destroy the opponent, losing need not cost the manifestation, and ending a fight does not end the embodiment. Fighting on until a living manifestation is destroyed is escalation the player may choose, never the assumed model ([36](36_COMBAT_RESOLUTION_SURRENDER_ESCAPE_AND_WITHDRAWAL_V0.md), AMO-D124–AMO-D128, L59).

These pillars describe **Standard Gameplay** combat, which is never reduced because VR exists. VR combat is intended to become a genuinely VR-native discipline rather than a remapped gamepad, with its own answers to skill, mastery and balance — and how the two relate competitively is an open problem (AMO-D042, AMO-Q059, AMO-Q060). See [11_STANDARD_AND_VR_GAMEPLAY.md](11_STANDARD_AND_VR_GAMEPLAY.md).

## 6. Mastery

A player must be able to become significantly better with the same Amorpho through practice. This is the defining property of the combat layer (L15).

Consequently, whatever influence cultivation, size, health or lineage has on combat (AMO-Q025) must not replace skill as a central determinant of outcomes. A well-cultivated plant may matter; a well-practised player must matter.

The same applies to the human's own magical development. A more advanced Warden is **not** assumed to make any Amorpho stronger, faster or more damaging — human progression expands what the human can do, and its only confirmed dimension is how many astral connections they can sustain (AMO-D067, AMO-D069). Whether it touches combat at all is open (AMO-Q025, AMO-Q099). See [16_HUMAN_WARDEN_PROGRESSION_V0.md](16_HUMAN_WARDEN_PROGRESSION_V0.md).

## 7. The central hypothesis to test

The concept depends on one untested hypothesis:

> Moving between calm, long-term cultivation and intense, short-term fighting — with the same individual plant — is fun, and each layer makes the other more meaningful.

It could fail in several ways: the transition may feel jarring; players may refuse to risk plants they have raised for years; combat may make cultivation feel like a stat grind; or cultivation may make combat feel secondary. This hypothesis should be tested early with deliberately small prototypes (see [07_INCUBATION_ROADMAP.md](07_INCUBATION_ROADMAP.md)).

## 8. The roster challenge

The real genus provides the cast, and its species count is expected to be large. Giving every species a fully bespoke fighter is a significant content problem. How distinct fighters are produced at that scale — bespoke kits, shared archetypes with species-specific identity, staged roster growth, or something else — is open (AMO-Q027). Any answer must respect AMO-D004 and AMO-D005: the roster is never padded with invented species, and never pruned by pretending real species do not exist.

## 9. Open questions

Artifact (AMO-Q021), transformation rules (AMO-Q022), control model (AMO-Q023), camera and perspective (AMO-Q024), cultivation's effect on combat (AMO-Q025), death, loss and recovery (AMO-Q026), roster scale (AMO-Q027), where and against whom combat happens (AMO-Q028), and Human Warden physical conflict (AMO-Q130). From this pass: astral transfer lore (AMO-Q039), inhabitability and re-entry (AMO-Q042), VR-native combat (AMO-Q059) and Standard/VR parity (AMO-Q060). See [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).
