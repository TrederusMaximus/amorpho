# 11 — Standard and VR Gameplay

**Status:** conceptual. This document establishes VR as a foundational product requirement and fixes the relationship between the two interfaces. It chooses no hardware, no SDK, no runtime and no input architecture, and it authorises no VR production work. Where something is undecided it points to [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).

> Standard Gameplay and VR Gameplay are two first-class entrances into the same Amorpho world.
> VR is optional, but never secondary.

The wider [platform sovereignty model](27_PLATFORM_AND_WORLD_SOVEREIGNTY_V0.md) treats both interfaces as gateways to the same canonical World alongside future PC, mobile and console clients. Platform identity is separate from Warden identity, and several connected devices never permit more than one direct embodied presence (AMO-D102, AMO-D103, AMO-D101).

## 1. What is being established

Amorpho is **not** a VR-only game. It is **not** a conventional game with a small VR novelty mode. It is **not** a VR game with a reduced non-VR fallback.

Standard Gameplay and VR Gameplay are two first-class entry points into the same game (AMO-D041, AMO-D042):

- a player must be able to experience Amorpho completely without ever owning VR hardware;
- a VR player must be able to experience Amorpho completely without repeatedly leaving VR for essential functionality.

## 2. Two entrances, one game

```
                SAME AMORPHO GAME
                        │
          gameplay and world truth
                        │
                  player intent
                  ╱           ╲
        STANDARD GAMEPLAY     VR GAMEPLAY
```

These are not separate games, persistent worlds, Amorpho identities or progression systems. They are two ways of inhabiting and controlling the same game. Biological truth is shared with them: protection, manifestation body damage and its persistence are canonical in both, so input and presentation may differ while what an effect does to a living manifestation may not ([35](35_COMBAT_PROTECTION_MANIFESTATION_BODY_DAMAGE_AND_BIOLOGICAL_PERSISTENCE_V0.md), AMO-D120, L54). A platform may still require its own distinct platform account; linking policy remains open (AMO-D103, AMO-Q121).

The technical architecture is deliberately unresolved. No classes, APIs or implementation code follow from this document.

## 3. Standard Gameplay must be complete

A player using conventional hardware — gamepad, keyboard and mouse, a conventional display — must be able to experience the full game. VR must not be required for any of:

world exploration · collection · plant ownership · cultivation · propagation · trading · property · greenhouses · astral transfer · Amorpho embodiment · combat · progression · social systems · persistent-world participation.

A player should be able to love and play Amorpho for years without ever using VR, and must never feel they are using a lesser version.

## 4. VR Gameplay must also be complete

A VR player should eventually be able to remain in VR for the complete meaningful experience. VR is not combat-only, not sightseeing-only, not a first-person camera, not a collection viewer and not a short special mode.

VR may eventually support the full Human / World layer — standing inside one's house, walking through owned spaces, entering a greenhouse, looking closely at plants, handling pots, manipulating world objects, interacting with other players, performing the astral ritual, experiencing the persistent world spatially — and the full Amorpho layer: inhabiting the Amorpho, movement, exploration, environmental interaction, equipment, combat, rooting, and returning to plant state.

None of this is implemented now. The requirement is recorded; the production cost is not incurred.

## 5. Same player, same world, same history

This is a major long-term product goal.

A player may spend ten years in Standard Gameplay and accumulate houses, greenhouses, plants, rare individuals, lineages, friends, property, history, combat experience and world relationships. When they later obtain VR hardware and enter Amorpho in VR, it is the same human character, the same plants, the same houses, the same greenhouses, the same world, the same ownership and the same persistent history.

The player does not begin *"Amorpho VR"* as a separate game. They enter the existing world through a different form of embodiment. Given the embodiment model in [09_EMBODIMENT_AND_ASTRAL_TRANSFER.md](09_EMBODIMENT_AND_ASTRAL_TRANSFER.md), this is a natural fit: the game already distinguishes *which body the player occupies* from *who the player is*.

## 6. Input should express intent

The technical input architecture is not designed here, and no intent API is defined. The architectural direction is only this: core game logic should not depend unnecessarily on one physical input method.

Foundational gameplay rules should not be written as `button X = action` when what the game actually means is closer to *the player expresses attack intent*, *the player attempts interaction*, or *the player initiates rooting*. Standard controls and VR controls may express the same gameplay meaning very differently.

This is not a licence to build abstractions for their own sake. It is enough separation that future VR does not require rewriting every core rule.

## 7. VR combat should be genuinely VR-native

The intention is not "VR controller button triggers the same animation as the gamepad". VR should eventually allow physical embodiment of fighting, with the player performing aspects of combat rather than only entering conventional inputs.

But nothing may assume unrestricted real-world physics, that every physical movement equals a valid attack, that flailing should be advantageous, that human anatomy matches every Amorpho body, or that Standard and VR controls will automatically be competitively equivalent.

VR combat must become a deliberately designed discipline, aiming at skill, mastery, meaningful physical action, intentional techniques, readable rules and balance (AMO-Q059). It requires prototypes.

## 8. Standard combat remains a full fighting game

Standard combat stays a deep, active fighting system: real-time movement, positioning, timing, attacks, defence, blocking, counters, abilities, combinations, input sequences, individual character mastery and fighting-game rounds (AMO-D008).

Standard combat is not reduced because VR exists. Each should be excellent on its own terms.

## 9. Parity is an open problem

How the two interfaces relate competitively is deliberately unanswered (AMO-Q060). Open: whether Standard and VR players can fight directly; whether both control styles suit ranked competition; whether matchmaking distinguishes interface type; whether combat rules can stay identical while input disciplines differ; how physical attack speed is normalised; how impossible or fantastical Amorpho moves are expressed in VR; how accessibility is maintained; how physical fatigue is handled; how exploits are prevented.

These need prototypes and real testing, not an early decision.

## 10. Account for VR early; pay for VR production later

This distinction is the practical point of the whole document (AMO-D043). The failure to avoid is a future in which Amorpho has been designed for years around assumptions that make full VR prohibitively expensive or impossible to add.

**From the beginning, therefore:**

- avoid unnecessary flat-screen-only architectural assumptions;
- avoid core gameplay concepts that fundamentally require a 2D UI;
- preserve semantic separation between gameplay meaning and physical input;
- consider embodiment when designing world interactions;
- consider physical scale and spatial interaction where relevant.

**But do not build VR production systems now.** Not VR hands, tracked bodies, VR locomotion, motion controllers, hand tracking, VR avatars, VR combat, headset-specific rendering or XR menus.

> Account for VR early. Pay for VR production when the project is ready.

## 11. No hardware or SDK commitment

No choice has been made, or may be made yet, regarding OpenXR implementation details, Meta SDK, SteamVR, Apple spatial frameworks, PlayStation VR technology, specific headsets, specific tracking hardware or VR middleware (AMO-D020, AMO-Q062). The design principle at this stage is platform-independent.

VR also joins the list of things the eventual engine decision must weigh (AMO-Q036); see the criteria in [08_CONCEPTUAL_ARCHITECTURE.md](08_CONCEPTUAL_ARCHITECTURE.md#engine-and-technology-decision-criteria).

## 12. No shared cross-project VR platform

Amorpho's future VR work may produce knowledge and technical primitives that could eventually benefit other Trederus Maximus projects. **Imperblio**, the Imperial Library, is one plausible future consumer: a spatial library experience — entering a library, moving through shelves, taking a book down, opening it, reading, inspecting works — would need similar interaction primitives.

That is **context, not architecture** (AMO-D044). Amorpho remains independent (AMO-D002, AMO-D018):

- no shared VR framework is created now;
- no dependency from Amorpho to any sibling project;
- no dependency from any sibling project into Amorpho;
- no cross-repository infrastructure.

If Amorpho and, later, another project prove that certain primitives are genuinely generic — grab, hold, inspect, place, point, select, open, navigate, manipulate, interact are only examples — they may eventually be extracted deliberately. No generic shared VR library exists or is planned.

The extraction path is:

```
project-specific implementation
        → repeated real use
        → proven generic behaviour
        → deliberate extraction
        → optional shared technology
```

and never:

```
shared framework first → projects forced into it
```

> Prove first. Extract later.

## 13. Open questions

VR locomotion, comfort and posture (AMO-Q056), VR embodiment of human and non-human bodies (AMO-Q057), VR interaction and interface (AMO-Q058), VR-native combat (AMO-Q059), Standard/VR parity, cross-play and matchmaking (AMO-Q060), VR accessibility (AMO-Q061), VR platforms and hardware (AMO-Q062). Related earlier questions: combat control model (AMO-Q023), camera and perspective (AMO-Q024), engine choice (AMO-Q036), target platforms (AMO-Q037). See [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).
