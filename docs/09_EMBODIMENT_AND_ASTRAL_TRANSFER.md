# 09 — Embodiment and Astral Transfer

**Status:** conceptual. This document fixes the embodiment model: who the player is, where their body is, how they come to control an Amorpho, and what happens when they stop. It deliberately does not settle lore, thresholds, timings or mechanics. Where something is undecided it points to [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).

> One consciousness. One inhabited body.

## 1. What transformation actually is

[04_TRANSFORMATION_AND_COMBAT.md](04_TRANSFORMATION_AND_COMBAT.md) established **transformation** as the bridge between the two gameplay layers (AMO-D007). This document says what the bridge is made of.

Transformation is **astral transfer**: the player's consciousness leaves their human body and inhabits one eligible *Amorphophallus* individual, which becomes an active, animated Amorpho. The human does not physically become a plant, and the plant does not become a new creature.

"Transformation" remains the umbrella term for the bridge. "Astral transfer" is the mechanism. The two are not competing concepts, and no document should treat them as separate systems.

## 2. One consciousness, one inhabited body

The player has **one** persistent human body. They may eventually own many plants. At any moment, their consciousness inhabits exactly one body (AMO-D028).

If a player owns a hundred Amorphos:

- one human body exists;
- a hundred plant individuals exist;
- at most one of those plants is currently inhabited;
- every other plant is simply a plant, living in the world under its own conditions.

A collection is therefore **not a remotely controllable army**. Collection size creates options, logistics and strategic choices; it never creates simultaneous direct control. Anything that would let a player act through several plants at once — squad commands, remote orders, automated defence by uninhabited plants — contradicts this law and needs a new decision, not a quiet feature.

## 3. Two bodies, both persistent

The human body and the plant body are separate persistent physical entities (AMO-D029). Astral transfer changes which one the player's consciousness occupies; it removes neither from the world.

```
HUMAN BODY + PLAYER CONSCIOUSNESS
                 │
                 │  astral transfer
                 ▼
HUMAN BODY REMAINS        +        CONSCIOUSNESS INHABITS PLANT
(unattended, in the world)         (plant becomes an active Amorpho)
```

The model to avoid is *"the human disappears and an unrelated fighter appears"*. Nothing may be built on that assumption.

## 4. One individual, two states

A plant and its animated Amorpho form are the **same persistent individual** in two states (AMO-D030):

```
PERSISTENT PLANT INDIVIDUAL
├── ROOTED PLANT STATE
└── INHABITED / ANIMATED AMORPHO STATE
```

Identity, provenance, lineage, ownership, history, genetics and individual variation belong to the individual and cross the boundary with it. They are not copied into a separate fighter object, and they are not suspended while the individual is animated.

This is why the concept works at all: the plant you raised is the fighter you play (L16). An architecture that instantiates an unrelated combat entity and reconciles it afterwards has already lost the point.

## 5. Where the transfer happens

The current strong design direction is that the human performs astral transfer from a **protected physical context**, with a dedicated ritual room inside the player's home as the leading concept:

1. the player enters the location as the human;
2. the transfer is initiated;
3. the player selects an eligible Amorpho from their collection;
4. the human body enters an unattended, trance-like state;
5. the player's consciousness enters the chosen plant.

The lore is **not decided**. An amulet, a belt, another artifact, the room alone, or a combination of place and object are all still candidates (AMO-Q021, AMO-Q039). What *is* decided is the consequence:

> The human body physically remains somewhere while the player inhabits an Amorpho.

That location therefore matters, whatever the fiction turns out to be.

## 6. The unattended human body

The world continues around the human body while it is unattended. This is a deliberate source of future gameplay pressure: events may occur that create a reason to return.

Nothing beyond that is decided. Whether other players can reach or harm an unattended human, whether homes can be entered, what protections exist, what anti-griefing rules apply, and what happens if a transfer is interrupted are all open (AMO-Q041). The durable principle is only:

> Astral embodiment does not remove the human body from persistent world reality.

## 7. Alive is not the same as inhabitable

Astral entry requires sufficient biological stability (AMO-D031). A plant can be alive and still be impossible to inhabit.

| Condition | Astral entry |
|---|---|
| healthy, stable | inhabitable |
| moderately stressed | possibly inhabitable, depending on rules not yet written |
| severely stressed, critical | alive, but no longer inhabitable |
| dead | unavailable |

State names, granularity and thresholds are open, including whether inhabitability is a binary gate or a continuous quality (AMO-Q042). The law is the separation of the two concepts, not the table.

Inhabitability is always derived from the individual's **biological condition**, never set by the World or by geography (AMO-D050). A place is not inherently un-inhabitable; a plant's condition is. This is what lets the same location affect different species, different individuals, and the same individual at different times, differently.

## 8. Astral exit and rooting

Leaving an inhabited Amorpho returns the individual to its biological plant state (AMO-D032). That requires rooting, or another biologically appropriate transition the game may later define.

The ideal case is a safe cultivation environment — its own pot, another suitable pot, suitable substrate, a greenhouse bed, suitable outdoor soil, or other controlled cultivation infrastructure. What actually counts as a valid rooting site is open (AMO-Q043).

> Astral exit returns fantasy to biological reality.

The moment the player leaves, the individual is once again governed by its real relationship with its surroundings — evaluated as Environmental Fit ([10_WORLD_AMORPHO_EVOLUTIONATOR.md](10_WORLD_AMORPHO_EVOLUTIONATOR.md)).

## 9. Rooting is not inherently harmful

This is easy to get wrong, so it is stated as a law (AMO-D033). Rooting does **not** start a decline timer. Rooting **exposes the individual to Environmental Fit**, and the resulting trajectory may be strongly negative, mildly negative, neutral, positive or strongly positive.

A rooted Amorpho in an excellent environment may stay healthy and inhabitable indefinitely. It may also recover, grow, develop, improve in condition, accumulate resources or become reproductively successful.

> **Rooting does not start a countdown. It starts an environmental relationship.**

How that relationship is evaluated is specified in [12_ENVIRONMENT_AND_FIT_MODEL_V0.md](12_ENVIRONMENT_AND_FIT_MODEL_V0.md).

### Rooting may be the destination, not the end of the journey

The most important thing to get right about rooting is that it is **not primarily an emergency mechanic** (AMO-D054).

> Rooting is not merely how an Amorpho stops travelling. Rooting may be the reason for travelling there.

A player may deliberately inhabit an Amorpho and move it across the world precisely in order to establish that individual somewhere chosen. The journey and the rooting site then form one strategic operation, and the rooting is its goal.

At least three player intentions sit behind the same underlying act. They describe purposes, not necessarily runtime states:

| | **Emergency rooting** | **Operational rooting** | **Strategic establishment** |
|---|---|---|---|
| Why | the player must leave the Amorpho somewhere less than ideal | the player stations the individual somewhere it may be useful later | the player deliberately establishes it somewhere biologically suitable for long-term life |
| Horizon | as short as possible | limited, often seasonal | indefinite |
| Concern | survival and rescue | access, staging, readiness, waiting for favourable conditions | healthy growth, development, flowering, reproduction, propagation, lineage |
| Follow-up | rescue, retrieval, or re-entry while still possible | later re-entry and use | cultivation, and whatever the biological systems eventually allow |

All three are the same act. Only the intention and the environment differ.

### Long-term rooted life

In an appropriate environment a rooted individual may simply live there. Depending on the biological systems that eventually exist, it may remain healthy, remain astrally inhabitable, grow, increase in size, develop, enter seasonal cycles, flower, reproduce, produce offspring and participate in a local population.

Excellent Environmental Fit therefore has to support more than recovery. Recovery is not the top of the model — **thriving and living there** is (L38, AMO-D054). See [12_ENVIRONMENT_AND_FIT_MODEL_V0.md](12_ENVIRONMENT_AND_FIT_MODEL_V0.md).

### Rooted does not mean inactive

An individual can be outside the player's control and still be biologically active. While rooted, future systems may continue to process growth, seasonal development, flowering, pollination, reproduction, health, environmental stress, recovery, interaction with local populations and selection pressure.

The player's consciousness does not need to be present for biological life to continue. This follows directly from the world persisting independently of players (AMO-D009), and it is what makes a collection spatially and temporally strategic rather than a set of parked objects.

What a rooted individual actually does over time, and whether it stays reachable and re-enterable, are open (AMO-Q077, AMO-Q082).

### Geography becomes strategic

Because Fit ranges into the positive, some places are genuinely better for some individuals. That can eventually motivate locating good habitat, transporting individuals to it, establishing distant populations, acquiring suitable property, using a friend's land or greenhouse, staging seasonally, and protecting valuable growing locations.

A location may also be suitable only for part of the year, which makes deliberate **seasonal routing** possible: travel and operate during a favourable window, use the location as a temporary base, and move the individual on before conditions turn dangerous. That is planning, not an emergency (AMO-Q078).

None of these systems is designed here. The implication recorded is only that Environmental Fit makes geography strategically meaningful.

### Sequential, never simultaneous

Because only one body can be inhabited at a time (AMO-D028), operations involving several Amorphos remain **sequential**. A player might inhabit A, establish it at one place, return to the human body, later inhabit B, establish it elsewhere, and use the resulting spatial arrangement for something later.

Persistent rooting is what makes that arrangement meaningful, and the one-body law is what makes it cost something. Transfer range, and how the player regains access to each body, are not decided here (AMO-Q040, AMO-Q081, AMO-Q082).

## 10. No universal rescue timer

Emergency rooting may create a limited rescue window, but there is no fixed one (AMO-D034). Duration emerges from the World environment, the individual's biological requirements and current condition, possibly acclimation, life stage, individual variation, and whatever else the eventual model includes.

A mildly unsuitable place might allow a long recovery period. A catastrophically unsuitable one might produce rapid decline. A suitable place might produce no deadline at all, and an excellent one may improve the plant.

No numerical thresholds are defined here, and none should be invented elsewhere. There is no rescue-timer system anywhere in Amorpho: a window exists only while a negative trajectory is running and the individual is still inhabitable, and a stable or positive trajectory produces no window at all (AMO-D049, AMO-D050).

## 11. The astral re-entry window

After emergency rooting in a poor environment, the individual may at first remain stable enough for astral re-entry. The player can then return, animate it again, and move it toward safety personally.

If deterioration continues, the individual may cross the inhabitability threshold:

```
ASTRAL RESCUE POSSIBLE
        │  biological condition declines
        ▼
ASTRAL ENTRY LOCKED
        │
        ▼
PHYSICAL RESCUE REQUIRED
```

The plant may still be alive. But the player must now reach it as the human, or use some other rescue route the game may later provide. Exact timings and re-entry rules are open (AMO-Q042, AMO-Q044).

## 12. The human must stay necessary

The astral system must not make the Human / World layer obsolete. There must be situations that only the human can resolve: physical retrieval, transport, repotting, treatment, relocation, controlled cultivation, and other human actions the game later defines (AMO-Q046).

> Human and Amorpho are complementary bodies.

The human is not the weak mode and the Amorpho is not the strong mode. Each body enables a different kind of agency, and a design in which one is simply better than the other has failed this principle.

## 13. Multiple Amorphos create real conflicts

Because only one body can be inhabited, simultaneous threats become genuine decisions. If Amorpho A is threatened in one place and Amorpho B in another, both remain persistent individuals and the player cannot directly control both. They must weigh:

- which Amorpho to inhabit;
- which problem is more urgent;
- which plant has the longer environmental stability window;
- whether the human can reach one;
- whether another player can help;
- whether infrastructure exists nearby;
- whether one must be left at risk.

This should **emerge from the simulation**, not from a scripted choice screen (L37).

## 14. Amorpho-to-Amorpho rescue is an open possibility

A situation may arise in which the human body is far away, Amorpho A is deteriorating, and Amorpho B is healthy and much closer. The player might then inhabit B, travel to A, and assist it physically — protecting, carrying, relocating, moving it into better substrate, or transporting it toward a greenhouse.

Whether any of this is possible, and under what limitations, is **not decided** (AMO-Q047):

> Can an inhabited Amorpho rescue, carry, protect, transport or relocate another rooted Amorpho?

It is recorded here because it follows naturally from the rest of the model, not because it is approved.

## 15. Reciprocal protection

Protection runs both ways. The human may protect plants through cultivation, transport, treatment, infrastructure, rescue and environmental control. An inhabited Amorpho may eventually protect the human, other plants, property or other entities through abilities available in animated form.

No combat or security rules are specified here. The principle is reciprocity.

## 16. Distributed safe locations

A player's own home need not be the only safe place to root. Other owned properties, owned greenhouses, suitable outdoor habitat, trusted friends' greenhouses, shared infrastructure and other future cultivation locations may all qualify.

A player operating in a cold region might come to rely on a friend's heated greenhouse as a safe rooting point. That makes cultivation infrastructure **social and strategic**, not merely personal.

No permission or access system is designed here (AMO-Q040, AMO-Q046).

## 17. Equipment

An inhabited Amorpho may eventually use equipment: combat gear, expedition gear, environmental protection, and other things the game later defines. Environmental gear may temporarily extend the conditions under which the animated Amorpho can operate — cold, rain, heat or mechanical protection, conceptually.

No actual items are designed here.

### Equipment does not rewrite biology

Equipment protects the **animated** body. It does not change the rooted plant's biological requirements.

> Animated traversal capability and rooted survival capability are different things.

An Amorpho might traverse a cold region with suitable equipment. That says nothing about whether the rooted plant could survive there.

### Rooting ends animated-state protection

Current design direction: when an inhabited Amorpho roots and returns to plant form, worn animated-state equipment stops providing environmental protection. It may fall beside the plant, remain at the rooting site, or otherwise cease functioning as worn protection. Exact inventory behaviour, ownership and retrieval are open (AMO-Q048).

The durable law is:

> Equipment that protects the animated body does not automatically protect the rooted plant.

Which produces the question a player should genuinely have to ask:

> I can travel here — but can I safely *stop being* Amorpho here?

## 18. Three distinct environmental capabilities

These must never collapse into a single `can live here / cannot live here` flag (AMO-Q051):

| Capability | Question |
|---|---|
| **Traversal tolerance** | Where can an inhabited, animated Amorpho temporarily operate, possibly with equipment? |
| **Rooting tolerance** | Where can the individual survive after returning to rooted form? |
| **Long-term suitability** | Where can the rooted individual genuinely remain healthy, grow, develop, recover, reproduce and persist? |

All three are evaluated through the same Environmental Fit boundary; they differ in what is being asked of the individual and for how long. See [10_WORLD_AMORPHO_EVOLUTIONATOR.md](10_WORLD_AMORPHO_EVOLUTIONATOR.md).

## 19. The embodiment model in one picture

```
HUMAN
player consciousness in the human body
   │
   │  astral transfer
   ▼
AMORPHO
human body remains physically in the world
consciousness inhabits one eligible plant
that plant becomes animated
   │
   │  rooting / astral exit
   ▼
ROOTED PLANT
consciousness returns to the human
the plant remains in the world
   │
   ▼
Environmental Fit continues to act on the plant
```

The player's active consciousness occupies exactly one body at a time.

## 20. Deliberately not decided

The lore of the transfer (amulet, belt, ritual room, several artifacts, or a combination), how the magic originated, why only some humans can perform it, whether transfer distance is limited, whether plants owned by others can be inhabited, and whether an Amorpho can be lent are all open (AMO-Q021, AMO-Q039, AMO-Q040). The ritual-room model is a strong direction, not a decision.

## 21. Open questions

Astral transfer lore (AMO-Q039), eligibility and permission (AMO-Q040), the unattended human body (AMO-Q041), inhabitability and re-entry (AMO-Q042), rooting sites (AMO-Q043), environmental prognosis (AMO-Q044), critical condition and death (AMO-Q045), physical rescue (AMO-Q046), Amorpho-to-Amorpho rescue (AMO-Q047), equipment on rooting (AMO-Q048), and the three tolerance concepts (AMO-Q051). Earlier related questions: the artifact (AMO-Q021), transformation rules (AMO-Q022), cultivation's effect on combat (AMO-Q025), loss and recovery (AMO-Q026). See [06_OPEN_QUESTIONS.md](06_OPEN_QUESTIONS.md).
