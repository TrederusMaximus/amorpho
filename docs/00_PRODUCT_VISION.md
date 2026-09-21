# 00 — Product Vision

> Reality provides the cast. The game provides the fantasy.

## The game in one paragraph

In Amorpho, the player lives as a human in a persistent world modelled on Earth. They travel, explore, discover and acquire real *Amorphophallus* plants — each one a persistent individual with its own origin and history — and they cultivate, propagate and trade them in pots, homes, greenhouses and gardens. Through a magical mechanism, the player's consciousness can leave their human body and inhabit a suitable plant, which becomes an **Amorpho**: a fighter they control in real-time, skill-based combat. The plant they raised is the fighter they learn to master.

The human body remains in the world while this happens, and the player can inhabit only one body at a time. Both of those facts do a great deal of work: they keep the human layer necessary, and they make a large collection a source of choices rather than an army. See [09_EMBODIMENT_AND_ASTRAL_TRANSFER.md](09_EMBODIMENT_AND_ASTRAL_TRANSFER.md).

## What Amorpho aims to be

Amorpho aims to become its own genre: a combination of ideas that are familiar individually but are brought together here in a distinct way.

- a **persistent world** that continues without the player;
- **exploration** as a human character;
- **collecting** living plants that are real species;
- **ownership, cultivation, propagation and trade**;
- **persistent individual plants** with provenance and lineage;
- **the real Earth** as the shared geographic foundation for both layers (AMO-D045);
- a **fantasy astral embodiment** layer;
- direct, **skill-based fighting**;
- **generational change** in plants that players breed, select and move around the world;
- potentially very deep, **long-term player-created biological and economic history**;
- playable **either on conventional hardware or in VR**, as the same game.

The goal is not to be a better version of an existing game, but to make this particular combination feel like a coherent whole.

## Product pillars

1. **A real cast.** The species are the real species of the genus. Their bizarre, sometimes enormous, often foul-smelling forms give Amorpho an unusual roster without inventing anything.
2. **Every plant is an individual.** Plants are not interchangeable items. A plant's history — where it came from, who owned it, what it produced — can make it matter.
3. **A world with its own continuity.** Populations exist and develop whether or not anyone is watching. Players change history; they are not its centre.
4. **Risk is where the interesting decisions are.** Protected cultivation is safer; exposed cultivation can be better. A flowering plant announces itself.
5. **Mastery.** Combat rewards practice. A player can become significantly better with the same Amorpho over time.
6. **The bond between layers.** The same individual plant spans the calm, long-term world of cultivation and the intense, short-term world of fighting.
7. **One consciousness, one body.** The player has one human body and inhabits at most one plant at a time. Owning many Amorphos creates logistics and hard choices, never simultaneous control (AMO-D028).
8. **Environment is an interaction, not a verdict.** The world says what conditions exist; a plant knows what it needs; what happens between them can harm, stabilise or genuinely improve the plant (AMO-D035–AMO-D037).
9. **Change across generations.** Inheritance, variation and selection — environmental and player-driven — can make distinctive lineages emerge within real species over long spans of play (AMO-D038, AMO-D040).
10. **Two ways in, one world.** Standard and VR gameplay are both first-class entrances to the same persistent game. VR is optional, never secondary (AMO-D041, AMO-D042).

## Who it is for

A player with no botanical interest must be able to love Amorpho purely because it is an excellent game. Players who do care about the plants should find that the game respects reality where it matters. Education may happen incidentally, because the underlying things are real — but entertainment is the product (AMO-D003).

Amorpho may ultimately create a humorous, memorable connection to the fact that these strange organisms actually exist.

## What Amorpho is not

- **Not a clone** of any existing game, even where individual ideas are familiar.
- **Not educational software.** It never lectures.
- **Not a botanical simulator.** Botany grounds the world; it does not dictate mechanics (AMO-D006).
- **Not a botanical database or research system.** Botanical research happens outside Amorpho. Amorpho holds only the minimal approved real-world facts the game needs (AMO-D024, AMO-D025).
- **Not dependent on anything else.** Amorpho stands alone (AMO-D002).

## Conceptual reference points

These are shorthand for individual ideas only, never templates:

- *creature-collecting games* (for example Pokémon) — collecting, owning and bonding with distinct creatures;
- *competitive fighting games* (for example Street Fighter) — rounds, input-driven moves, frame-level timing, character mastery;
- *open-world games* (for example GTA) — an inhabitable world with cities, travel and consequences.

Amorpho differs from each in ways that matter: its creatures are real species and persistent individuals rather than catalogue entries; its fighters are raised through cultivation rather than captured; its world has scarcity and history rather than respawning content.

## Tone

Undecided (AMO-Q034). The subject invites humour — the plants' appearance, their names and their smell — and the concept includes genuine wonder at strange real organisms. How these balance is an open design question.

## Glossary

| Term | Meaning |
|---|---|
| **Amorpho** | The game. |
| **an Amorpho** | An individual plant temporarily inhabited by the player's consciousness and animated as a fighter. The same individual, in a different state — not a separate creature. Plural form not yet fixed. |
| **the artifact** | The magical object that has been the leading concept for enabling astral transfer. Placeholder name; whether an object is involved at all, alongside or instead of a ritual location, is open (AMO-Q021, AMO-Q039). |
| **astral transfer** | The mechanism of transformation: the player's consciousness leaves the human body and inhabits one eligible individual plant. |
| **inhabited** | Of an individual: currently animated by the player's consciousness. At most one individual is inhabited at a time (AMO-D028). |
| **inhabitable** | Of an individual: biologically stable enough for astral entry. Not the same as alive (AMO-D031). |
| **rooting** | The act by which an inhabited Amorpho returns to rooted plant state, ending astral embodiment. |
| **emergency rooting** | Rooting somewhere suboptimal because the player has to, hoping the individual stays recoverable. |
| **strategic rooting** | Rooting somewhere favourable on purpose, because the location benefits the individual. |
| **species** | A real *Amorphophallus* species, as listed in approved input. |
| **species ID** | A species' permanent, opaque Amorpho identity, e.g. `AMO-SP-000001`. The scientific name is mutable metadata attached to it. |
| **individual** | One persistent plant in the world, with its own identity and history. |
| **lineage** | A line of descent traced through reproduction across generations. |
| **approved reality input** | Layer 1: the minimal real-world facts approved for use by Amorpho, supplied as files from outside the repository. See [05_REALITY_GATE.md](05_REALITY_GATE.md). |
| **approved export** | A file of approved real-world facts prepared outside Amorpho, for Amorpho to accept. |
| **Reality Gate** | The one-way inbound boundary: an approved export is validated and accepted into `data/input/`. |
| **canon** | The internal representation the implementation derives from approved input. Never the external master list. |
| **approved compatible pair** | Two species approved, symmetrically, as able to hybridize in the game. Absence of approval is not proof of incompatibility. |
| **game design data** | Layer 2: information Amorpho creates for gameplay (combat, abilities, balancing, progression). Not reality-derived. |
| **persistent world state** | Layer 3: what exists or happens in a running world: individuals, lineages, ownership, locations, trades, history. |
| **cultivation context** | Where and how a plant is kept: pot, home, greenhouse or outdoors. |
| **effective environment** | The local conditions an individual actually experiences, after cultivation context and care have modified the location environment. A World-side concept. |
| **Environmental Fit** | What happens when an effective environment meets a particular individual's requirements and condition. Derived from World × Amorpho, never a source of truth of its own (AMO-D037). Formerly called *suitability*. |
| **traversal tolerance** | Where an inhabited, animated Amorpho can temporarily operate, possibly with equipment. |
| **rooting tolerance** | Where an individual can survive after returning to rooted form. Not the same as traversal tolerance (AMO-D032). |
| **long-term suitability** | Where a rooted individual can genuinely remain healthy, grow, develop, recover, reproduce and persist. |
| **World** | The simulation domain that owns environmental truth: *what conditions exist here, now?* (AMO-D035) Its geography is the real Earth (AMO-D045). |
| **Amorpho** (domain) | The simulation domain that owns biological traits, requirements and individual condition: *what does this individual need?* (AMO-D036) |
| **Evolutionator** | The simulation domain that owns inheritance, variation and generational change: *how are traits transmitted and changed across generations?* (AMO-D038) |
| **Standard Gameplay** | Playing Amorpho on conventional hardware: gamepad, keyboard and mouse, a conventional display. |
| **VR Gameplay** | Playing the same Amorpho, in the same world with the same history, through VR embodiment. Optional, never secondary (AMO-D042). |
