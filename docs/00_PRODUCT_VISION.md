# 00 — Product Vision

> Reality provides the cast. The game provides the fantasy.

## The game in one paragraph

In Amorpho, the player lives as a human in a persistent world modelled on Earth. They travel, explore, discover and acquire real *Amorphophallus* plants — each one a persistent individual with its own origin and history — and they cultivate, propagate and trade them in pots, homes, greenhouses and gardens. Through a single magical artifact, a player can temporarily awaken a suitable plant as an **Amorpho**: a fighter they control in real-time, skill-based combat. The plant they raised is the fighter they learn to master.

## What Amorpho aims to be

Amorpho aims to become its own genre: a combination of ideas that are familiar individually but are brought together here in a distinct way.

- a **persistent world** that continues without the player;
- **exploration** as a human character;
- **collecting** living plants that are real species;
- **ownership, cultivation, propagation and trade**;
- **persistent individual plants** with provenance and lineage;
- **real geography and climate** as grounding;
- a **fantasy transformation** layer;
- direct, **skill-based fighting**;
- potentially very deep, **long-term player-created biological and economic history**.

The goal is not to be a better version of an existing game, but to make this particular combination feel like a coherent whole.

## Product pillars

1. **A real cast.** The species are the real species of the genus. Their bizarre, sometimes enormous, often foul-smelling forms give Amorpho an unusual roster without inventing anything.
2. **Every plant is an individual.** Plants are not interchangeable items. A plant's history — where it came from, who owned it, what it produced — can make it matter.
3. **A world with its own continuity.** Populations exist and develop whether or not anyone is watching. Players change history; they are not its centre.
4. **Risk is where the interesting decisions are.** Protected cultivation is safer; exposed cultivation can be better. A flowering plant announces itself.
5. **Mastery.** Combat rewards practice. A player can become significantly better with the same Amorpho over time.
6. **The bond between layers.** The same individual plant spans the calm, long-term world of cultivation and the intense, short-term world of fighting.

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
| **an Amorpho** | A plant temporarily awakened as a fighter through the artifact. Plural form not yet fixed. |
| **the artifact** | The single magical object each player possesses that enables awakening. Placeholder name; form and origin are open (AMO-Q021). |
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
| **suitability** | How well a location's environment (possibly modified by cultivation context) fits a species' tolerances. |
