# 20 — The Biology ↔ Magic Boundary and Astral Readiness, v0

**Status:** specification, version 0. This document draws the line between the real biological plant and the magically inhabited fighter, and defines the persistent magical state that sits on the magic side of it. It defines no combat stats, no rates, no thresholds, no healing rules and no species facts.

It builds on [09_EMBODIMENT_AND_ASTRAL_TRANSFER.md](09_EMBODIMENT_AND_ASTRAL_TRANSFER.md), [17_LIFE_CYCLE_STATE_MACHINE_V0.md](17_LIFE_CYCLE_STATE_MACHINE_V0.md), [18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md](18_PHASE_DAMAGE_CORE_RECOVERY_AND_BLOOM_MATURITY_V0.md) and [19_DEVELOPMENTAL_MATURITY_V0.md](19_DEVELOPMENTAL_MATURITY_V0.md).

> Biology determines the available magical form. Magic runs the fighter.
> Magic suspends biology; it does not consume it.
> Leaving does not heal; living does.

## 1. Terminology: the Tuber

**Tuber** is the canonical term for the persistent underground storage and core structure of an individual (AMO-D087). *Core* remains useful descriptively — *the tuber is the persistent biological core of the Amorpho* — but architecture wording prefers **Tuber development**, **Tuber recovery**, **Tuber impact** and **Tuber draw**.

Earlier decisions written in terms of "core" are **not** rewritten; ledger history stays readable, and the affected entries carry *Revised* notes instead (AMO-D074, AMO-D079).

## 2. Two kinds of Tuber expenditure

Not everything that reduces persistent Tuber resources is harm (AMO-D087):

| | **Programmed Tuber Draw** | **Pathological Tuber Impact** |
|---|---|---|
| What | normal biological expenditure for a legitimate biological process | harmful persistent loss caused by adverse circumstances |
| Example | **Bloom** | severe exposure, prolonged failed productivity, dehydration, inappropriate storage, physical damage — all illustrative |
| Is it injury? | **No.** The plant is spending what it accumulated | **Yes.** Development is lost rather than spent |
| Recoverable? | rebuilt through productive growth | rebuilt through productive growth (AMO-D075) |

Both reduce persistent resources, and both recover while the individual lives. Conflating them would make flowering read as self-harm, which it is not.

### Bloom uses Programmed Draw

```
mature Tuber → Bloom → Programmed Tuber Draw
    → reduced stored development and resources
    → later rebuilding through productive growth
```

Bloom therefore carries a real biological price without being damage. No amount is defined.

### Leaf rebuilds; Bloom spends

The Leaf phase is the primary constructive opportunity: a healthy leaf, good Environmental Fit and time support productive activity, which supports reserves, which supports Tuber growth and developmental maturity (AMO-D081). No formula is defined — only the direction.

> **Leaf rebuilds. Bloom spends.**

Which is why an individual that blooms every possible cycle without good leaf seasons between them is spending down a balance it is not replenishing.

The Leaf is itself funded by the persistent Tuber before it can perform that constructive work. A possible [same-cycle replacement](25_TUBER_FUNDED_MANIFESTATION_AND_REPLACEMENT_ROUTING_V0.md) is another biological investment, not a free reset or an automatic injury (AMO-D095, AMO-D096). This does not make Leaf emergence and Bloom cost identical.

## 3. The boundary

At the moment of astral entry, the individual stops being simulated as a plant and starts being run as a fighter (AMO-D084).

```
BIOLOGICAL INDIVIDUAL          →  determines what can be manifested, and its baseline
        │  astral entry
        ▼
MAGICAL MANIFESTATION          →  its own movement, combat state, capabilities, tolerances
        │  rooting / astral exit
        ▼
BIOLOGICAL INDIVIDUAL          →  biology resumes
```

### Biology determines the template

At entry, the biological individual may determine which manifestation is available (Leaf or Bloom), its phase-specific structural condition, its capability ceiling, which phase-specific abilities exist, and other future baseline properties.

> Biology determines what magical form can be manifested, and the baseline condition of that form.

No combat mapping is defined (AMO-Q109).

### Magical state is its own stack

Once inhabited, the Amorpho may eventually carry combat durability, stamina, magical status effects, phase-specific skills, combat resources and **Astral Readiness** (§5). These are **not** leaf integrity, Tuber vitality, reserves, stress load or developmental maturity. The full magical stack is not designed here.

## 4. Magic suspends biology; it does not consume it

While the player inhabits the Amorpho, that individual's **normal biological simulation is suspended** (AMO-D084): no biological growth, no productive development, no maturity gain, no reproduction, no life-cycle progression, no Programmed Tuber Draw, no biological recovery.

And critically, in the other direction (L49):

> Astral embodiment does not consume ordinary biological resources simply because the player is moving, fighting or remaining embodied.

Combat duration, distance travelled, ordinary attacks and time spent embodied do **not** by default draw down Tuber mass or biological reserves. The magical layer has its own costs, and they are paid in magical state.

This is what keeps both systems understandable. If fighting ate Tuber mass, every fight would be a developmental setback, the harm model's careful horizons would collapse, and players would be punished biologically for playing the game.

## 5. Open-ended embodiment

> **Astral embodiment has no intrinsic maximum duration** (AMO-D085).

There is no universal *Astral Time Remaining*, and none may be added. A player may remain embodied for hours, days or far longer if circumstances permit.

### The limiter is opportunity cost, not a clock

Prolonged embodiment is expensive because the rest of the world does not wait:

| | While you stay embodied |
|---|---|
| **The inhabited Amorpho** | biology suspended — no growth, no Tuber rebuilding, no Bloom progression, no reproduction |
| **The Human** | unavailable for everything only the human can do — including physically moving Anchors (AMO-D062) |
| **Other Amorphos** | keep living: growing, entering dormancy, blooming, becoming stressed, needing rescue, being stolen |
| **The World** | continues (AMO-D009) |

So the cost of a long embodiment is everything that happened elsewhere meanwhile — which scales naturally with how much a player has to lose, rather than with an arbitrary constant.

### The Human trance is metabolically stable

When the consciousness leaves, the human body enters a deep trance with suspended metabolism (AMO-D085). Ordinary hunger, thirst and degeneration must **not** create a hidden embodiment timer, and normal aging during trance must not meaningfully force a return.

The body remains physically present in the world and **may still be threatened** by hostile actors or world events (AMO-Q041) — but:

> Human biological maintenance must never become a disguised astral countdown.

Threat and metabolism stay separate. A reason to return should be something that *happened*, not a bar quietly emptying.

## 6. Astral Readiness

**Astral Readiness** is a persistent magical state of an anchored individual: **how ready it is to sustain effective magical embodiment** (AMO-D086).

It belongs to the magical access layer. It is **not** vitality, stress load, reserves, developmental maturity, leaf integrity or bloom integrity, and it must not be implemented as a view of any of them.

### Leaving does not heal

> **Astral exit does not reset Astral Readiness** (L50, AMO-D086).

Leave an exhausted Amorpho and immediately re-enter, and it is still exhausted. There is no `exit → instant restore → re-enter` loop, and closing that door is the point: an exploit there would erase every cost the magical layer has.

Fighting, magical exertion and extreme ability use may deplete readiness. No mapping, percentage, formula or KO threshold is defined (AMO-Q112, AMO-Q113).

### Magic heals the fighter; biology heals the plant

Future magical healing may restore combat durability, clear magical status effects and support short-term capability. It must **not** directly restore damaged leaf structure, Tuber vitality, developmental maturity or depleted biological reserves (AMO-D086, L48).

How much magical healing can restore *readiness* is deliberately open (AMO-Q114).

## 7. Rooted life restores readiness

The fundamental recovery path is biological:

```
fight / explore → readiness depleted → ROOT → biological life resumes
    → readiness regenerates → future astral entry
```

This gives rooting a major gameplay purpose beyond simply stopping (AMO-D054, AMO-D072).

**Recovery is time-compressed.** Biological reality legitimises the mechanism, but the game must not require literal biological recovery durations to make a fighter usable again. Readiness recovery may be substantially faster than biological growth — a deliberate Fun First abstraction (L1, AMO-D086). No duration is defined.

### Leaf-form recovery

A rooted leaf-phase individual resumes productive life, and readiness regenerates. Better conditions may support better recovery:

```
excellent Fit → strong recovery opportunity
adequate Fit  → usable recovery
poor Fit      → slow, limited or ineffective recovery
```

No categories are numeric, and pathological biological consequences may develop separately and simultaneously (AMO-Q108).

> Healthy rooted leaf life recharges magical readiness.

**Not every rooting site recharges well.** Where a player roots matters for readiness as well as for survival, which ties the magical loop directly to Environmental Fit and to strategic establishment.

### Bloom-form recovery, and its price

A rooted bloom-phase individual also regenerates readiness — but rooting resumes the **Programmed Tuber Draw** that embodiment had suspended:

```
astral Bloom use → readiness depleted → ROOT Bloom
    → readiness recovers  +  Tuber continues spending biological resources
```

So a Bloom can be re-entered repeatedly while it remains biologically present and the plant viable — and each rooted interval between uses consumes more of the biological opportunity. **The limit is biological, not a charge counter** (AMO-D086, AMO-D087). No fixed number of uses exists.

### Embodiment pauses the Bloom draw

Because biology is suspended (§4), inhabiting a Bloom pauses its Programmed Tuber Draw. A player could therefore remain in Bloom form for a very long time. **That is allowed**, and no artificial Bloom timer may be added to prevent it.

The same reasoning governs a manifestation whose loss is already committed: continuous embodiment suspends its terminal progression too, so a Warden may hold a doomed body indefinitely and postpone its biological end. **That is also allowed** (AMO-D117, [34](34_EMBODIMENT_ACROSS_TERMINAL_MANIFESTATION_COLLAPSE_V0.md)). Exiting resumes the trajectory from exactly the same state; re-entry pauses it again and reverses nothing (L50).

The cost is the usual one: Bloom progression paused, pollination and reproduction paused, the Human unavailable, the world moving on, and readiness draining with nothing restoring it.

### Deep Dormancy fully restores readiness

> A successful Deep Dormancy period restores Astral Readiness to full before the next active availability window (AMO-D086).

Deep Dormancy remains astrally uninhabitable, biologically resting and unusable as a fighter (AMO-D060). What it provides is that when the individual returns toward active life, its magical readiness starts fully restored. Where in the transition that becomes usable is open; **life-cycle accessibility still gates entry regardless** (AMO-D063, AMO-Q085).

## 8. Astral Signal and Astral Silence

Two things that look alike and are not (AMO-D088):

| | Question |
|---|---|
| **Astral Signal** | is this anchored individual currently *detectable* by its Warden? |
| **Astral Inhabitability** | can the Warden *enter* it now? |

They are independent, and during life-cycle transitions they come apart: an individual may be **detectable but not inhabitable**, or the reverse in principle.

### The Anchor is a bridge, not a tracker

An Anchor may stay physically attached through every phase, and attachment alone guarantees **neither** an active signal, **nor** location information, **nor** astral entry (AMO-D061, AMO-D088).

### Signal across the life cycle

| Phase | Signal |
|---|---|
| Active Leaf · Bloom | present |
| **Senescence** | **fades progressively** — biological warning, and a final window to locate or retrieve |
| Early Dormancy | possibly faint residual; location may still be inferred |
| **Deep Dormancy** | **none — Astral Silence** |
| Pre-Emergence | faint signal returns, strengthening as awakening proceeds |
| Emergence | present in the ordinary post-dormancy route; exact replacement handoff remains open |

Inhabitability may close **before or during** the signal fade, and may reopen **after** the signal returns. The exact sequence is open (AMO-Q085, AMO-Q115).

**Manifestation existence bounds inhabitability at both ends.** A mature manifestation whose loss is biologically committed may still be a usable body while it exists, and entering it changes none of that biology; when the manifestation itself ends, normal inhabitation of it ends with it, no shell remains playable, and the Warden's consciousness returns to the human body ([34](34_EMBODIMENT_ACROSS_TERMINAL_MANIFESTATION_COLLAPSE_V0.md), AMO-D115–AMO-D118, L57). Recoverability and inhabitability therefore stay separate dimensions, bounded only by whether the body exists.

Signal or visibility during **Manifestation Emergence** does not make a developing Leaf or Bloom normally inhabitable. Both use biological construction through an Emergence Sheath/path and deployment; **Full Deployment** is required before normal Leaf or Bloom entry may become possible ([29](29_REPLACEMENT_EMERGENCE_TO_ASTRAL_READINESS_V0.md), AMO-D106, AMO-D107). Astral Readiness and the other gates remain separate. A fully deployed manifestation is not automatically Astral Ready (AMO-Q085, AMO-Q112, AMO-Q115).

The senescence fade matters: it is what turns dormancy from a surprise lockout into something a player can plan around — retrieve the individual, reallocate its Anchor, or accept losing track of it.

### Deep Dormancy causes Astral Silence

During Deep Dormancy the Anchor may remain attached, the Warden relationship may persist and the individual is alive — and there is **no astral signal, no live location and no automatic tracking** (AMO-D088).

This is distinct from AMO-D060, which says a dormant tuber is hard for *other people* to discover. This is about the owner's own connection going quiet.

### An Amorpho can be genuinely lost

If an outdoor dormant Tuber's exact physical location is not known, the Warden may be genuinely unable to find it during Astral Silence. **This is intentional.** The world does not hand out a quest marker because a player once anchored something.

> Physical location knowledge matters.

**Last known location is not live tracking.** The game may later remember where a Warden last knew an individual to be; that is historic player knowledge, not a current signal. If the plant is physically moved during Astral Silence, the Warden should **not** automatically know.

This produces real emergent risk: a dormant outdoor individual may physically contain its Anchor while being astrally silent, and another player who finds it could dig it up, move it and possess the Anchor — with no live tracking to betray them. Whether a found Anchor can be used, rebound or broken away from its Warden is **explicitly unresolved** (AMO-Q091).

And a corresponding emergent recovery: a Warden loses an individual during Deep Dormancy, someone relocates it, months later Pre-Emergence begins and the signal returns — revealing that the Amorpho is now somewhere unexpected. Location fidelity is undecided (AMO-Q115).

### The Astral Window

When a manifestation ends — on the ordinary course of a cycle, or after a Leaf's functional collapse — the persistent Tuber may stay **astrally reachable** for a transitional biological period before Deep Dormancy silences it. That period is the **Astral Window** (AMO-D099).

Inside it a Warden may establish **direct astral presence** with the persistent individual, for one purpose: influence over a biologically available routing decision ([26_PLANT_AUTONOMY_ASTRAL_LEVERAGE_AND_ROUTING_V0.md](26_PLANT_AUTONOMY_ASTRAL_LEVERAGE_AND_ROUTING_V0.md)). That is not astral entry. The Tuber does not become a playable body — no locomotion, no combat, no exploration (AMO-D089, §9). Because nothing is animated, nothing runs on magical state and §4's suspension of biology does not apply: the individual's biology continues throughout, which is why the window can close while the Warden is present.

Three limits travel with it. **Deep Dormancy closes it**, and a route already taken is not rewritten afterwards. **Presence is singular** — it occupies the same one consciousness that full embodiment occupies, so no second individual can be attended at the same moment (AMO-D028, AMO-D101). A selected Replacement route hands off to biological Emergence; its developing Leaf remains non-playable. Only after Full Deployment may that new manifestation pass through the ordinary gates, including **Astral Readiness**; it is never an automatic continuation of window presence (AMO-D063, AMO-D086, AMO-D107).

Duration, exact boundaries, how presence is established and ended, and whether it costs readiness are open (AMO-Q085, AMO-Q112, AMO-Q119).

### The Radar is a resonance interface

The Astral Radar represents the Warden's **living astral connections**, and is not global map tracking, exact positioning or universal plant detection (AMO-D061, AMO-D088). What it can show may depend on signal strength, and signal strength may affect **location fidelity** — a strong active signal potentially giving better awareness, a weak transitional signal less, Deep Dormancy none. No ranges, accuracy or interface are defined (AMO-Q092, AMO-Q115).

## 9. The Tuber is not a playable form

The astrally playable manifestations are **Leaf** and **Bloom** after their biological construction and ordinary astral gates. The Tuber is never a playable locomotion or combat form, in Deep Dormancy, an Astral Window or Pre-Emergence (AMO-D089, AMO-D099, AMO-D107).

**Reachability does not loosen this.** A Tuber inside an Astral Window (§8) is reachable, not playable: the Warden may be present with the individual and still has no body to move, fight or explore with. *Astrally reachable* and *inhabitable* are different questions, and only the second produces an Amorpho (AMO-D099).

This is deliberate scope discipline, and it costs nothing: the dormant Tuber remains highly relevant to the **Human layer** — transport, relocation, trade, repotting, digging, safe seasonal handling, Anchor management and strategic placement all happen there (AMO-D062, L23).

Transitional states also matter without any fighting in them, because that is where the **signal** changes (§8): warning, a last window, silence, and return.

## 10. What this pass deliberately leaves open

**Pathological Tuber Impact was not settled here** — it is specified in [21_PATHOLOGICAL_TUBER_IMPACT_V0.md](21_PATHOLOGICAL_TUBER_IMPACT_V0.md) (AMO-D090–AMO-D093), which this document prepared the terminology for. Two things are prepared for it:

- the **terminology** separating Programmed Draw from Pathological Impact (§2);
- the observation that **the same leaf damage early and late in an active phase may have very different Tuber consequences**, because what matters is functional capacity, remaining productive opportunity, environment, time and condition — not a proportion of structure lost. No rule such as *"up to 20% leaf damage has no persistent consequence"* may be introduced (AMO-D079, AMO-Q108).

Also open: Astral Readiness representation, depletion and recovery (AMO-Q112) · KO and forced exit (AMO-Q113) · magical healing (AMO-Q114) · signal strength and location fidelity (AMO-Q115) · threats to the unattended human body (AMO-Q041) · Anchor rebinding after theft or trade (AMO-Q091).

## 11. The model against the required cases

| Case | How |
|---|---|
| fighting does not consume Tuber mass | magic suspends biology and pays its own costs (§4, L49) |
| inhabited plant does not grow | biological simulation suspended during embodiment (§4) |
| a player may stay embodied indefinitely | no intrinsic duration cap (§5) |
| doing so still costs | suspended biology, unavailable Human, a world that keeps moving (§5) |
| exit then re-entry does not heal | readiness persists across exit (§6, L50) |
| leaf rooting restores readiness | rooted productive life regenerates it, better under better Fit (§7) |
| bloom rooting restores readiness and spends | readiness recovers while Programmed Draw resumes (§7) |
| dormancy starts the next window restored | successful Deep Dormancy fully restores readiness (§7) |
| dormancy remains uninhabitable | life-cycle access still closed (§7, AMO-D060) |
| a dormant anchored Amorpho leaves the Radar | Astral Silence (§8) |
| an outdoor Amorpho can be genuinely lost | no signal, no marker, physical knowledge matters (§8) |
| its signal returns in Pre-Emergence | signal returns before inhabitability (§8) |
| the Anchor is not GPS | a bridge, not a tracker (§8) |
| transitional states matter without Tuber fighting | the signal changes there (§8, §9) |
| a reachable Tuber is still not a fighter | the Astral Window carries presence, not embodiment (§8, §9) |
| Programmed Draw ≠ Pathological Impact | spending versus losing (§2) |

## 12. Open questions

Astral Readiness representation, depletion and recovery (AMO-Q112) · KO and forced exit (AMO-Q113) · magical healing (AMO-Q114) · Astral Signal strength and location fidelity (AMO-Q115). Related: the Core-Impact Threshold and Pathological Tuber Impact (AMO-Q108), astral access windows (AMO-Q085), phase-specific gameplay (AMO-Q086, AMO-Q109), Bloom content and timing (AMO-Q088, AMO-Q107), Anchor rebinding (AMO-Q091), the Radar (AMO-Q092), the unattended human body (AMO-Q041), and astral presence at a routing point (AMO-Q119).
