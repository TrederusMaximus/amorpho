# 27 — Platform and World Sovereignty v0

**Status:** product and conceptual architecture specification. This fixes durable boundaries, not a port, account system, network design, engine choice or release plan. Amorpho grows continuously, but it is never rushed.

> **Amorpho is the World. Platforms are gateways into it.**
>
> **One World. Many Ways In.**

## 1. Purpose and vocabulary

The **Amorpho World** is the canonical persistent game-domain reality: the Earth-based World, its inhabitants and their history. An **Amorpho client** is an application through which a player enters or interacts with that World. A **gateway** is a product metaphor for access through a device and its platform ecosystem; it does not name a technical service (AMO-D102).

One World means coherent canonical continuity, not one giant synchronous session. Future zones, instances, partitions, combat sessions and representation choices remain open (AMO-Q006). A home or story moment may feel private without becoming another canon. One World also does not require every player to see every other player.

## 2. World sovereignty

The Amorpho product, under Trederus Maximus, owns and governs canonical Amorpho-domain truth (AMO-D102). No device, storefront, platform account, vendor save or client defines the World. This product boundary creates no runtime or data dependency on another Trederus Maximus system (AMO-D002, AMO-D018).

Canonical truth includes Warden and Human character continuity; persistent Amorpho individuals, Tubers, manifestations, lineage and genealogy; ownership, houses, greenhouses, properties, populations and locations; biological state, progression, relationships, player-created and World history; and any persistent economy that later exists. This is a statement of responsibility, not a storage schema or computation location.

Earth remains one geographic foundation (AMO-D045). There is no mobile Earth, console Earth or VR Earth. A lower-power client may show a smaller or simpler local slice; it must not have a smaller canon, different plant identity or contradictory ownership and lineage.

## 3. One World, many entrances

The strategic target is broad access through Windows/PC, macOS where appropriate, iPhone/iPad, Android phones and tablets, Nintendo gaming hardware, PlayStation, Xbox, VR/XR devices and future relevant platforms where practical (AMO-D105). This is architectural intent, not approval, release order, simultaneous launch or a promise that every gateway will be available. Access can expand progressively without making an early client the owner of the World.

**Mobile is a genuine entrance into the game**, not intrinsically a plant viewer, notification utility or reduced side game. **Console is access to the same World**, not a ported universe. **VR remains optional and first-class**, with the same house, greenhouse, plants, Warden, relationships and history a Standard player already has (AMO-D041, AMO-D042). PC, handheld, touch, controller, keyboard and VR interfaces can differ substantially while preserving meaningful participation. No single interface is the definition of complete Amorpho.

The player-facing target is natural device switching: mobile in the morning, console or handheld later, PC in the evening, perhaps VR on another day. The World continues throughout. Hardware replacement, a new console generation, a client rewrite or loss of one platform gateway must not by itself replace a Warden or erase canonical history. Entitlement and migration details remain open.

## 4. Warden and platform identity

> **A Warden belongs to Amorpho, not to a device.**
>
> **Platform identity is not Warden identity.**

The long-term model is one Warden and Human character with one meaningful history across supported gateways (AMO-D103). Platform identities may later authenticate or provide access, but they are distinct from Amorpho identity. No platform profile is itself the Warden; no local or vendor cloud save is the sole canonical plant collection or World history. Linking, unlinking, recovery and session policy remain open. A platform entitlement may permit use of a client without defining who the Warden is; one Warden need not imply access rights on every storefront.

One Warden on several devices still has **one consciousness and one direct embodied presence** (AMO-D028, AMO-D101). Simultaneous devices cannot control the Human and several Amorphos at once. Spectator, status or secondary views are possible future questions, provided they grant no second controlling consciousness. The exact connection and login policy is open.

## 5. Client model and platform-independent truth

> **Clients are replaceable. The World persists.**
>
> **Platform changes the experience, not the truth.**

A client may render, interpret input, cache and perhaps locally calculate detail. It is not the authoritative World (AMO-D104). Canonical game outcomes, including biology, ownership and progression, must remain coherent across supported clients. Client hardware alone must not alter biological time, Environmental Fit, routing cost, Replacement, identity or history. A simpler local calculation may not create contradictory canonical outcomes; how coherence is achieved remains open.

Presentation may vary in resolution, frame rate, draw distance, vegetation, effects, asset detail, audio, UI layout and local density. **Visual fidelity may differ. Game truth must not.** Global canonical Earth does not require every client to hold or render the whole World simultaneously. Broad hardware support requires scalable fidelity from the start, without reducing core depth to the weakest device or treating a powerful PC or VR as the only complete experience (AMO-D105). Specific scaling mechanisms and minimum hardware are open.

Gameplay meaning remains separate from physical input:

```text
physical input → client interpretation → gameplay intent → Amorpho game rules
```

Keyboard keys, console buttons, touch gestures and VR motions are ways to express intent, not the rule's meaning. Standard Gameplay must remain viable with a controller, without assuming a mouse cursor, hover or desktop window. Touch can translate intent without shaping core rules. Each client may use a suitable UI; shared meaning does not require pixel-identical interfaces. Essential play must not be tied unnecessarily to one motor modality, screen size, control scheme or VR. Exact controls and accessibility design remain open (AMO-Q023, AMO-Q061).

## 6. Cross-progression and shared participation

Cross-progression and shared Warden history are first-class long-term targets (AMO-D105). The same player should continue the same meaningful existence when moving between supported clients. Shared-world participation across mobile, PC, console and VR is also a strategic target, but exact cross-play rules are unresolved. One World does not demand that every combat queue mix touch, controller, keyboard/mouse and physical VR combat. Fairness, input-aware matchmaking, performance, social systems and platform policies need later design and testing (AMO-Q060).

Combat may use a specialized technical representation in the future. Any result that becomes persistent history must rejoin the same canon. This chooses no combat session architecture. Private-feeling exploration, rituals, homes and narrative remain possible inside the persistent World.

## 7. Platform services and commercial access

Platform services belong across a boundary from Amorpho's domain rules: accounts, achievements/trophies, friends, invitations, rich presence, cloud-save facilities, parental controls, platform matchmaking, commerce and entitlements may be useful or required later. None may become a necessary definition of canonical biology, progression or Warden identity (AMO-D104). An achievement reflects Amorpho history; it does not create that history. A vendor cloud save may support local settings, caches or required client data; its loss must not itself delete canonical existence.

Storefronts can control commercial access on their platform without owning World truth. Purchases, subscriptions, DLC, regional access and cross-platform entitlement reconciliation are open. No optional vendor feature, sole vendor identity, vendor-controlled canonical database or storefront-dependent core simulation should become necessary for the World to exist. Future partnerships are access relationships, not an assumed transfer of product sovereignty. Platform APIs should receive only game-domain data an eventual integration actually needs; policy and legal design come later.

## 8. Persistent-world implications

The World exists and changes independently of an individual player (AMO-D009). Plants may grow, retreat, enter Dormancy or route autonomously while their Warden is elsewhere or offline (AMO-D097, AMO-D098). **Persistent biology requires persistent World continuity**; a closed client cannot be the sole source of that truth. This says nothing about where computation occurs.

Disconnected play is a major open question: **What can a client do while disconnected from the canonical persistent World without creating contradictory history?** Network loss must not produce divergent canonical plants, duplicated ownership or conflicting lineage. Local settings and caches may exist, but a traditional local “save slot” is an inadequate model for the canonical World. Offline scope, writes, synchronization and conflict handling are undecided.

Platform-account data and real residential addresses must not become public Warden or game-location identity by default. Earth geography and cross-platform identity increase the importance of the existing privacy question (AMO-Q003). Exact privacy, family-account and regional policies remain open.

## 9. Future technology and production constraints

Future engine evaluation must consider credible long-term support for desktop, iOS/Android, major console families and VR/XR; large 3D Earth-based spaces; scalable rendering; controller, touch, keyboard/mouse and VR input; cross-platform interaction; networking; certification/toolchain viability and long-term commercial maintenance. A technology that structurally closes major gateways is a significant negative or possible disqualifier (AMO-D105, AMO-Q036). No engine is selected here.

Conceptually, canonical World/domain truth, simulation, client experience, and rendering/input/platform services have distinct responsibilities. This is not a prescribed module or deployment diagram. World identity and history should reasonably outlive a rendering engine or client generation, without building premature abstractions. Future platform certification, including lifecycle, account, privacy, commerce, controller and network-loss requirements, becomes a first-class production constraint when implementation and release work reach it; no current vendor rule is encoded now.

## 10. Strategic and player-facing North Stars

**Strategic aspiration, not a forecast:** The long-term ambition is that a platform benefits from giving its users access to Amorpho, rather than Amorpho depending on that platform for its identity. Amorpho aims to become loved enough that access to its World is strategically valuable to a platform. No present platform demand, partnership or approval is claimed.

**Intended future product relationship, not a claim of present market power:**

> If Amorpho is unavailable on a platform, players are being denied access to a world in which they already live.

## 11. Open questions

The [question register](06_OPEN_QUESTIONS.md) keeps implementation and policy unresolved: Amorpho identity and platform linking/recovery (AMO-Q121); simultaneous sessions (AMO-Q122); offline actions, disconnected writes and conflict handling (AMO-Q123); entitlements and commerce boundaries (AMO-Q124); cross-platform participation, social systems and competitive fairness (AMO-Q125); client lifecycle, version skew, migration and gateway withdrawal (AMO-Q126); hardware floors, fidelity and accessibility (AMO-Q127); platform launch sequencing, certification and feature policy (AMO-Q128); and privacy, family and regional constraints (AMO-Q129). Existing AMO-Q006, AMO-Q036, AMO-Q037, AMO-Q060 and AMO-Q062 also remain open.

## 12. Explicit non-decisions

No engine, networking stack, server topology, cloud provider, simulation-hosting scheme, account or linking design, authentication, cross-save implementation, offline authority, commerce policy, SDK integration, release date, launch platform or platform approval is chosen. “Gateway” does not imply a Gateway service. One World does not imply a single networking session, shard rule, instance rule or battle architecture. Different client capabilities do not license different canonical truths.

## 13. Invariant checks

| Scenario | Required result |
|---|---|
| PC to mobile | The same Warden, plants and World history remain, even if the interface changes. |
| Old to new console generation | The client can be replaced without replacing canonical identity. |
| Lower-fidelity mobile view | Simpler graphics or local detail cannot change canonical biology or ownership. |
| Standard to VR after years | The same house, greenhouse, plants, relationships and history remain. |
| Vendor achievement or social service unavailable | Amorpho progression and biology continue independently. |
| Several devices connected | At most one directly controlled body or astral presence; passive secondary uses remain open. |
| A gateway unavailable or withdrawn | The World and Warden history still exist independently of that client. |
| A future platform appears | It may become another client without redefining World truth. |
| Entitlement on only one platform | Client access can differ while canonical Warden identity remains one. |
| Radically different graphics on two devices | Shared canonical history and game outcomes remain coherent. |
