# 53 — Rooted Cultivation Decision Space, v0

**Status:** qualitative gameplay-design pass using owner-supplied design direction, including an addendum on **controlled versus open-world cultivation** and **infrastructure automation**. It answers the gap the paper transition test exposed ([52](52_CULTIVATION_EMBODIMENT_TRANSITION_TEST_PAPER_PROTOTYPE_V0.md) §17). It defines no watering, soil, fertiliser, pot size, treatment, inventory, tool, crafting, care meter, timer, construction, upgrade tree, energy, lighting value, horticultural fact, species fact, interface or code.

> **The Warden tends the conditions; the plant does the growing.**

## 1. Purpose

Rooted biology is specified in depth; what the Warden *does* while an individual is rooted was not. Without an answer, cultivation risks becoming passive waiting, a recovery cooldown, background simulation, or preparation for the next fight — exactly failure criteria A and F of doc 52. This pass answers:

> What does the player actually do when an Amorpho individual is rooted?

Enough that rooted life matters in itself; that the Warden can improve or worsen future outcomes; that observation, timing and preparation matter; that mistakes matter without twitch play; and that everything stays tied to the World and to Plant Autonomy.

## 2. Cultivation is environmental stewardship

> **Rooted cultivation is the Warden's management of an individual's surrounding conditions, exposure, protection and future options, while the plant's internal biology remains autonomous** (AMO-D170).

**The Warden manages the habitat; the plant manages its life.** The Warden can influence *where*, *under what conditions*, *with what protection*, *with what infrastructure* and *with what timing* an individual lives. The Warden never directly commands growth, Productive Return, recovery, Dormancy Commitment, reactivation, maturity, Bloom, manifestation construction or internal routing.

## 3. The Plant Autonomy boundary

The plant decides biologically among viable paths (AMO-D097, AMO-D098). Astral leverage, where it exists, is its own explicit channel ([26](26_PLANT_AUTONOMY_ASTRAL_LEVERAGE_AND_ROUTING_V0.md)); rooted cultivation is never *player chooses biological outcome*. The foundational loop:

```
WARDEN CHANGES CONDITIONS
        ▼
WORLD / LOCAL ENVIRONMENT CHANGES        World owns conditions (AMO-D035)
        ▼
ENVIRONMENTAL FIT CHANGES                derived, owns nothing (AMO-D037)
        ▼
PLANT BIOLOGY RESPONDS AUTONOMOUSLY      Amorpho owns its response (AMO-D036)
```

So there is no *increase growth*, *heal Leaf*, *gain reserves* or *delay dormancy* command — only changes to conditions that influence those outcomes.

## 4. Placement

> *Where should this individual be rooted?*

Scales include an outdoor site, a protected outdoor site, a house or interior, a greenhouse, another property, another region, and future controlled environments. No map or travel system is designed (AMO-Q002). Placement changes Fit, exposure, risk, Remaining Productive Opportunity, protection and accessibility — and it is **strategic, not one-time**: a site may stop being right, and changing it may mean Human transport, embodiment and relocation, another Amorpho carrying an exposed Tuber, or future logistics.

**No universally best location** (AMO-D014, L10):

| | May offer | May cost |
|---|---|---|
| **Outdoor** | strong natural opportunity, space, natural exposure | weather, pests, discovery, theft, uncontrolled pollination, physical risk |
| **House** | control, security, accessibility | space, light, local conditions, manifestation scale |
| **Greenhouse** | environmental modification, protection, infrastructure | never erases World constraints or lifecycle biology (§13) |

No bonuses are defined.

## 5. Environmental modification

The Warden may modify local World conditions — exposure, moisture availability, temperature, light, humidity, shelter, airflow, the rooting environment — within the dimensions the World and Fit already own ([12](12_ENVIRONMENT_AND_FIT_MODEL_V0.md)). No hardware or real horticultural practice is specified.

**It never forces an outcome.** Better conditions → better Fit → biology *may* perform better if its lifecycle and state permit. A perfect greenhouse is not a forced active phase ([42](42_WORLD_TIME_SEASONAL_OPPORTUNITY_AND_EMBODIMENT_V0.md), [46](46_DORMANCY_COMMITMENT_BOUNDARY_V0.md), [47](47_DEEP_DORMANCY_DURATION_AND_ACTIVE_PHASE_REACTIVATION_BOUNDARY_V0.md)).

## 6. Protection

**Protection decisions exist outside combat.** Rooted individuals face severe environment, physical disturbance, pests, discovery, theft and future hazards, and the Warden decides how much effort to invest against them. No pest or security system is designed (AMO-Q020, AMO-Q008).

**Rooted protection is not embodied protection.** Worn combat protection does not protect a rooted plant ([09](09_EMBODIMENT_AND_ASTRAL_TRANSFER.md) §17, AMO-Q048). Rooted protection comes from location, infrastructure, environmental management and physical security.

## 7. Observation

> **Attention produces information.**

Spending attention on an individual can reveal or sharpen judgement about visible condition, damage, recovery, lifecycle position, response to the environment, upcoming transitions, unusual behaviour and whether to intervene. A long-attuned Warden combines what is seen with history, Anchor feedback and species tendency ([50](50_WARDEN_BIOLOGICAL_INFORMATION_AND_ROSTER_JUDGEMENT_MODEL_V0.md)). Observation is a decision, never a minigame, and never telemetry: *know enough to judge, not enough to calculate* (L71).

## 8. Timing

Timing is central: when to leave a Leaf rooted, when to embody it, when to stop and return it, when to relocate, when **not** to disturb a productive window, when a recovery period is worth protecting, and when to let a normal lifecycle transition proceed rather than intervene. No calendar is involved; the timing is biological.

Timing carries opportunity cost — a threat during a highly productive window asks whether to keep cultivating or interrupt it ([48](48_ROSTER_TIMING_AND_ONE_CONSCIOUSNESS_BIOLOGICAL_OPPORTUNITY_TRACE_V0.md), [49](49_COMBAT_PILLARS_AND_BIOLOGICAL_ROSTER_STRATEGY_V0.md)). **Cultivation includes choosing when not to use the fighter.**

## 9. Rehabilitation

After damage the decision is:

> *Do I give this individual a real opportunity to rehabilitate, or expose it again?*

The Warden creates favourable circumstances; the Leaf performs Structural Stabilization, Compensatory Remodeling and Functional Recovery itself ([40](40_ROOTED_MATURE_LEAF_RECOVERY_CEILING_AND_COMPENSATORY_REMODELING_V0.md)). **There is no heal button.** Treatment of persistent harm remains a separate future layer (AMO-Q105).

## 10. Risk and non-intervention

**Risk acceptance is a cultivation decision.** Outdoor rooting may offer excellent opportunity at greater world risk; an indoor site may be safer and less productive. No optimum exists.

**Doing nothing can be correct.** When conditions are already excellent, when intervention would disturb productive biology, when dormancy should proceed, when recovery needs time, the right action may be none — and that is an **informed decision**, not an absence of gameplay. *Choosing not to disturb a well-placed individual is legitimate cultivation.*

**Not a chore simulation.** Rejected: repeated watering clicks, mandatory daily maintenance, cleaning, timer collection, maintenance streaks, decay because the player did not log in, and dozens of identical micro-actions. The persistent World may create consequences; gameplay is not built as obligation. The question is *what does this individual need from its environment right now?* — never *which chores are due?* — so there is **no canonical checklist**: different situations call for different subsets of these families.

**Calm, not empty.** Combat is intense, reactive and high in immediate risk; cultivation is observational, strategic, patient and lower in tempo. **Lower tempo is not lower agency.** Cultivation rewards planning, observation, biological understanding, patience, environmental judgement and anticipation; combat rewards execution, timing, spacing, defence and risk judgement. Both are mastery.

## 11. Preparation for embodiment

Checking condition, judging whether the body is worth risking, preparing protection, choosing timing and planning where to root afterwards are cultivation too — **one function of cultivation, not its purpose**.

**Cultivation matters even if the individual never fights.** It shapes Productive Return, persistent Tuber state, maturity, Core security, Bloom possibility, the future lifecycle and later lineage. It is not maintaining fighter inventory.

**Consequences arrive later and stay biological.** A rooted decision may change future manifestation condition, Core security, return, recovery, deployment cost, the future combat body and later lifecycle, with no instant score. Wrong placement means poor conditions → poor Fit → biological consequence, never an arbitrary debuff. **Good decisions do not guarantee good outcomes**: world events happen and biology stays uncertain. The Warden manages risk; they do not control reality.

## 12. Spatial and World integration

**Human agency is physical.** Cultivation is performed through the Human and World layer. While embodied elsewhere the Warden cannot remotely alter a rooted plant's environment unless future infrastructure explicitly allows it, and early cultivation may require the Human to visit the plant or greenhouse in person to water, check, adjust, move or inspect — **environmental care may cost real Warden time and presence** (AMO-D028, L23). That is a genuine opportunity cost against being embodied elsewhere.

**Absence does not pause biology.** If the Warden leaves, the plant keeps living (AMO-D009). Cultivation manages a persistent organism, not an active screen. Others — other humans, friends, future services, shared infrastructure — may physically influence rooted conditions; no delegation is designed (AMO-Q046, AMO-Q080).

**Cultivation and combat geography are one World.** Because the Tuber stays where it is rooted, placement decides where the next embodiment starts, how far objectives are, what exposure and environment are available:

```
WARDEN ROOTS INDIVIDUAL AT LOCATION A
        ▼
THREAT APPEARS AT LOCATION B
        ▼
EMBODIED AMORPHO TRAVELS  (the core travels with it)
        ▼
ENCOUNTER
        ▼
WARDEN CHOOSES WHERE TO ROOT AFTERWARDS
```

Placement shapes later combat logistics, and combat movement changes later cultivation state (AMO-D161, AMO-D129). Both directions are legitimate trade-offs: rooting somewhere biologically worse because it is strategically important, better protected or closer to future conflict; or choosing an excellent growing site that is remote, hard to reach, less secure or far from home. *Where the Warden roots today changes the biological and strategic possibilities of tomorrow.*

**Investment in places.** Cultivation includes improving locations — a greenhouse, a protected rooting site, a secure home site, future infrastructure — and others' protected sites may become part of a network of strategic biological locations. No base-building, property or permission system is designed (AMO-Q080, AMO-Q007).

## 13. Controlled and open-world cultivation

Two broad contexts sit at opposite ends of a control spectrum. Neither is superior (AMO-D171, L10).

### Controlled cultivation

> **A greenhouse is infrastructure that lets the Warden modify and stabilize selected local World conditions around rooted individuals.**

It does not rewrite biology, cancel dormancy, guarantee Productive Return, create universal perfect conditions or remove every constraint; the existing World and Fit architecture evaluates it by the ordinary mechanism (AMO-D035, AMO-Q049). *A greenhouse is controlled opportunity, not guaranteed growth.*

**Automation changes Warden workload, not biological rules.** Long-term progression space includes automatic irrigation, environmental monitoring, ventilation, temperature control, supplemental lighting, shading and physical protection — examples only, no upgrade tree. Automatic irrigation is not a growth bonus: **infrastructure maintains a desired World condition without the Warden performing the corresponding physical intervention every time**; climate or light automation changes local conditions or their stability, never biological truth.

The direction of progression:

- **early** — the Warden must often be present in person to maintain selected conditions, and in doing so learns place, environment and need;
- **developed** — some repeated maintenance is automated;
- **advanced** — less routine presence; attention shifts to judgement, exceptional intervention, strategic placement, biology and major environmental change.

No stage is quantified. Automation **reduces repetitive work and does not automate judgement**: even an advanced site may need monitoring, strategic change, repair and adaptation, and environmental shifts, infrastructure limits, equipment failure, lifecycle change and unusual condition remain possible. *Automation removes chores before it removes judgement.* This is the anti-chore principle given a progression path, and it is **operational capability, not a stat**: better infrastructure frees the Warden for decisions, exploration, embodiment and exceptions.

**Infrastructure value is relational.** Because Fit and lifecycle belong to the individual, one setup may be excellent for one individual and mediocre for another; there is no universal greenhouse quality score. Its value comes from what conditions it can create, which individuals can use them, where it is, and how much direct work it saves.

**Lifecycle stays sovereign.** Automatic irrigation, heating, lighting or climate control is never *force active growth*: automation does not cancel a committed dormancy or wake an unready Tuber. Infrastructure acts on the **External Productive Opportunity** component only — preserving suitable conditions longer, creating them where outdoors cannot, protecting rehabilitation, supporting extended-growth strategies — and never manufactures Biological Growth Availability (AMO-D153, AMO-D156, AMO-D159).

### Open-world rooting

Rooted in an open natural environment, **the individual experiences the actual local World**, and the Warden does not own that environment. Conditions may be excellent through part of the year and deteriorate later.

> **A good rooting site is time-dependent.** Outdoors can be excellent now and dangerous later.

A site may be suitable in one season, stressful later and unable to support the individual in another period — a direct consequence of World Time and Fit (AMO-D046, AMO-D145), with no static site-quality score and no lethal threshold defined. The Warden manages outdoor risk mainly through **location and timing**: where and when to root, when to remove or relocate, limited protection where allowed, and watching conditions change. *The Warden cannot command the weather.*

### Moving between them

```
GREENHOUSE → EMBODY → TRAVEL → ROOT OUTDOORS
OUTDOOR SITE → EMBODY → RETURN TO CONTROLLED SITE
```

One continuous individual throughout; no teleport (AMO-D129). And not every move needs embodiment: depending on lifecycle and body state, the Human may physically transport a Tuber, a potted or rootable individual, or other valid forms (AMO-D093, AMO-Q046, AMO-Q117). *The same individual can move between greenhouse, home and open Earth without changing what it is* (AMO-D168).

## 14. Lifecycle variation

The same decision families weigh differently by lifecycle:

- **seasonal individual** — the timing of its rooted productive window may dominate;
- **extended-growth individual** — maintaining long-term suitable conditions may matter more, and controlled sites may extend its opportunity;
- **Bloom-capable or blooming individual** — substantial core value, Programmed Draw and future reproductive decisions; no flowering care is designed (AMO-Q079);
- **Tuber-only or dormant individual** — storage location, protection, transport, environmental context and placement for future reactivation; no storage mechanics (AMO-Q117).

**Dormancy creates no busywork.** Strategic placement, protection and observation can be enough; quiet periods are preserved.

**Attachment and Attunement grow from continuity, not from actions.** Caring for the same individual across growth, damage, recovery, dormancy and new manifestations builds significance; there is no affection meter, and **a cultivation action is never Attunement XP** — it is meaningful shared history that deepens understanding (AMO-D167). Better knowledge improves decisions without making them certain; there is no optimal-care algorithm (AMO-D164).

## 15. The minimal rooted decision loop

Domain logic, not an interface loop:

```
OBSERVE
  ▼
UNDERSTAND THE INDIVIDUAL AND ITS WORLD
  ▼
DECIDE WHETHER INTERVENTION IS NEEDED
  ├── no  → let biology continue
  └── yes → change location · environment · protection · infrastructure · timing · preparation
  ▼
WORLD CONDITIONS CHANGE → FIT CHANGES → THE PLANT RESPONDS ON ITS OWN
  ▼
OBSERVE AGAIN, LATER
```

## 16. Transition-test integration

Doc 52's Card 1 is rewritten from this decision space so that it holds **genuine competing reasons** and none is trivially best: leave X undisturbed in good but exposed conditions; protect it against a foreseeable risk at the cost of attention; change its site or local environment, gaining one thing and giving up another; observe closely for better evidence without changing anything; prepare for a likely embodiment. The test still asks whether those choices created investment — **care is not assumed to produce attachment**, and the test remains falsifiable ([52](52_CULTIVATION_EMBODIMENT_TRANSITION_TEST_PAPER_PROTOTYPE_V0.md) §4).

## 17. Acceptance and consistency audit

| Test | Result |
|---|---|
| **A** — meaningful choices without combat | §4–§11 |
| **B** — through World and Fit, never biological commands | §3 |
| **C** — non-intervention can be correct | §10 |
| **D** — placement has trade-offs | §4, §13 |
| **E** — protection outside combat | §6 |
| **F** — observation has information value | §7 |
| **G** — timing matters | §8 |
| **H** — rehabilitation enabled, not performed | §9 |
| **I** — rooting is not a cooldown | §10, §11 |
| **J** — rooting location shapes combat geography | §12 |
| **K** — value without combat | §11 |
| **L** — no chore system | §10, §13 |
| **M** — Card 1 has competing choices | §16 |
| **Automation** | changes workload, never biology; removes chores before judgement |
| **Outdoors** | time-dependent, World-owned, managed by location and timing |

| Distinction | Holds |
|---|---|
| Cultivation ≠ direct biological control; care ≠ healing button | §2, §3, §9 |
| Environmental modification ≠ guaranteed outcome; greenhouse ≠ forced growth | §5, §13 |
| Rooting ≠ cooldown; non-intervention can be active judgement | §10 |
| Observation ≠ telemetry | §7 |
| Plant Autonomy sovereign; World and Fit mediate Warden action | §3 |
| Combat and cultivation geography are one World | §12 |

## 18. Deferred concrete care

AMO-Q012 keeps the concrete individual cultivation model: care interactions, physical handling, propagation and Tuber division. AMO-Q105 keeps treatment, pathology-specific care and persistent repair — general cultivation does **not** depend on it. AMO-Q049 keeps controlled environments: greenhouse construction and upgrading, automation, utilities and resources, supplemental lighting, irrigation, climate control, infrastructure failure and maintenance. AMO-Q043 keeps valid rooting sites; AMO-Q080 outdoor site management and shared sites; AMO-Q046 physical Human care, rescue and transport; AMO-Q117 dormant storage; AMO-Q020 pests; AMO-Q008 theft. No new question was required.

**Result:** the Warden chooses where an individual lives, what shelters it, what changes around it, when to look, when to act, when to take it into danger and when to leave it alone — and the plant, given those conditions, lives its own life. Calm gameplay, real decisions.
