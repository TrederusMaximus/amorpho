# 04 — Transformation and Combat

**Status:** conceptual. The principles here are accepted; almost every concrete rule is open. Nothing in this document chooses a control scheme, camera, engine or netcode.

## 1. Plants are plants

*Amorphophallus* plants in Amorpho are normally plants. They live, grow, flower, reproduce and die according to the world simulation. They do not walk around, and they are not creatures in disguise.

## 2. The artifact

Each player possesses **one** special magical artifact. It allows a suitable plant to be temporarily brought to life as an **Amorpho** (AMO-D007).

The artifact's physical form (possible concepts include an amulet or a belt), its name, its origin story and its role in the fiction are open (AMO-Q021). "The artifact" is a placeholder term.

## 3. Transformation

Transformation is the bridge between the two gameplay layers:

```
Human / World layer                      Amorpho / Combat layer
─────────────────────                    ──────────────────────
individual plant in a pot,   ──awaken──▶  the same individual,
greenhouse or landscape                   as an active fighter
                             ◀──return──
```

Accepted:

- The Amorpho **is** the individual plant, temporarily awakened — not a separate creature, copy or summon (L16).
- Only a **suitable** plant can be awakened.
- Awakening is **temporary**; the plant returns to being a plant.

Open (AMO-Q022): what makes a plant suitable (age, life-cycle stage, health, size, bond, species); how long awakening lasts; what it costs; where it can happen; and whether it has consequences for the plant afterwards.

## 4. From species to fighter

A real species defines the **identity and visual foundation** of an Amorpho character. Its combat design is authored game design, driven by balance, mastery and fun (AMO-D006):

- A large real plant is not automatically a stronger fighter.
- A botanical trait is not automatically a combat mechanic.
- Real characteristics are welcome as **inspiration** — for silhouette, animation, move themes, personality, humour — but never as specification.

Combat design belongs to Game Design Data (Layer 2). It references species by their permanent `AMO-SP-` IDs and never needs botanical justification (AMO-D021).

Individuals of the same species may differ in appearance through variation and history. Whether individual differences also affect combat is part of AMO-Q025.

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

## 6. Mastery

A player must be able to become significantly better with the same Amorpho through practice. This is the defining property of the combat layer (L15).

Consequently, whatever influence cultivation, size, health or lineage has on combat (AMO-Q025) must not replace skill as a central determinant of outcomes. A well-cultivated plant may matter; a well-practised player must matter.

## 7. The central hypothesis to test

The concept depends on one untested hypothesis:

> Moving between calm, long-term cultivation and intense, short-term fighting — with the same individual plant — is fun, and each layer makes the other more meaningful.

It could fail in several ways: the transition may feel jarring; players may refuse to risk plants they have raised for years; combat may make cultivation feel like a stat grind; or cultivation may make combat feel secondary. This hypothesis should be tested early with deliberately small prototypes (see [07_INCUBATION_ROADMAP.md](07_INCUBATION_ROADMAP.md)).

## 8. The roster challenge

The real genus provides the cast, and its species count is expected to be large. Giving every species a fully bespoke fighter is a significant content problem. How distinct fighters are produced at that scale — bespoke kits, shared archetypes with species-specific identity, staged roster growth, or something else — is open (AMO-Q027). Any answer must respect AMO-D004 and AMO-D005: the roster is never padded with invented species, and never pruned by pretending real species do not exist.

## 9. Open questions

Artifact (AMO-Q021), transformation rules (AMO-Q022), control model (AMO-Q023), camera and perspective (AMO-Q024), cultivation's effect on combat (AMO-Q025), death, loss and recovery (AMO-Q026), roster scale (AMO-Q027), and where and against whom combat happens (AMO-Q028). See [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).
