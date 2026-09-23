# 41 — Bloom Embodiment, Core Security and Destruction Value, v0

**Status:** conceptual architecture pass using owner-supplied domain direction. It establishes what a Bloom manifestation implies about the hidden persistent core, and how that differs from a Leaf. It defines no Bloom move, statistic, combat role, duration, Programmed Draw rate, Tuber size, loot value, rarity, capture economics, ownership rule or reproduction mechanic, and it asserts no real-world flowering biology.

> **A Leaf may conceal whether there is much left to save. A Bloom reveals that substantial persistent biology had to exist for the manifestation to exist at all — capability, not condition.**

## 1. Purpose

[37](37_MANIFESTATION_DESTRUCTION_TUBER_CORE_VIABILITY_AND_PHYSICAL_DROP_V0.md) established that destroying a manifestation exposes the actual persistent core, and AMO-D134 established that a manifestation's **appearance** reports its own history rather than the core's. Bloom introduces an asymmetry those rules did not cover: a Bloom exists **only because** the persistent individual had already reached substantial biological capability. Its existence is therefore informative in a way no amount of looking at a Leaf can be.

This pass says what that information is, what it is not, and why it gives Bloom a distinct strategic identity before a single Bloom-specific combat mechanic is designed.

## 2. Bloom is not a Leaf with a flower on it

> **Leaf and Bloom are manifestations of the same persistent individual, but Bloom arises from a different biological condition of that individual.**

Bloom is already a rare, exceptional active state rather than Leaf form with better numbers (AMO-D059, AMO-D071), and it is already gated: an individual must have reached its **species-specific flowering-maturity threshold**, which *enables* rather than guarantees Bloom, with actual Bloom further depending on condition, reserves, routing, environment and species biology (AMO-D078). This pass adds no new prerequisite. It draws the consequence:

```text
A BLOOM EXISTS
   → the persistent Tuber had enough biological capability to fund this manifestation
```

That is Amorpho game biology, not a botanical claim, and no numerical or real-world flowering threshold is introduced (AMO-D024). A Tuber barely able to persist after paying for a Leaf does not produce an expensive Bloom as though its persistent condition were irrelevant — the existing maturity, condition and routing requirements stay meaningful, with no threshold defined here (AMO-Q107).

## 3. Bloom as a lower-bound signal about the core

> **A fully developed Bloom is evidence that the persistent individual possessed substantial biological capacity when that Bloom was produced.**

It is a **lower-bound signal**, a biological inference, and real information. It is **not** a core readout. A Bloom does not reveal present Tuber mass, Current Biological Condition, current reserves, prior Pathological Tuber Impact, how much Programmed Draw has already occurred, whether the core has been directly injured, exact post-destruction salvageability, or any future reproductive outcome.

This does not contradict AMO-D134; it sharpens it:

> **Surface wear does not reveal core state, but manifestation *type* may itself carry biological information.**

The observer is not reading scars. The observer is reasoning from a fact about what had to be true for this body to exist. And **Bloom's own appearance still resolves nothing**: a pristine, damaged or scarred Bloom is not a proportional readout, and *bigger or prettier Bloom → bigger Tuber* is explicitly rejected. The signal is in existence, not cosmetics (AMO-Q110).

## 4. Leaf versus Bloom, as information

| | What an observer can infer |
|---|---|
| **Leaf Amorpho** | very little. It may have been inhabited immediately after costly emergence, before any meaningful rooted Productive Return, after a long productive rooted phase, after environmental damage, or after many fights — so it may conceal a robust core, a weak one, or one with nothing viable left. Freshness is a clue, never proof (AMO-D134, AMO-D136). |
| **Bloom Amorpho** | that the persistent individual reached Bloom-producing biological capability. Current core state remains hidden. |

Both cases preserve information asymmetry; they differ in where the floor sits. Two Blooms may still conceal very different internal states — one from a strong Tuber with moderate draw and good current condition, another that met the requirement while carrying heavy prior stress or pathology and has since spent substantially. Both are Blooms, and the observer knows only the historical lower bound.

Seeing a Bloom in the world is therefore a genuine **information event**: something real has been learned about that individual, without exact figures and without any interface designed to announce it. The player can obviously tell a Bloom from a Leaf, so the inference emerges from the visible form itself — no icon, indicator or scan is added (AMO-Q111).

## 5. Bloom embodiment carries the same core

Nothing about the physical ontology changes for Bloom (AMO-D129, AMO-D132):

- the persistent **Tuber travels physically inside** the inhabited Bloom as its central core, and is not left behind;
- the **Astral Anchor** travels with the core, unchanged, with no special Bloom binding;
- embodied movement moves the persistent individual;
- the Bloom body is the body **around** the core, and there is no separate Bloom projection or copy (AMO-D120, AMO-D134).

Damage that reaches the Bloom body is **real biological Bloom damage** through the ordinary layering — protection → manifestation body → persistent core — and is not automatic Tuber injury (AMO-D121, AMO-D122, L58). Bloom-specific mature damage and recovery are **not** designed here: the Leaf recovery architecture is deliberately Leaf-scoped, and Bloom's own response remains open ([40](40_ROOTED_MATURE_LEAF_RECOVERY_CEILING_AND_COMPENSATORY_REMODELING_V0.md), AMO-Q086, AMO-Q088).

## 6. Programmed Draw erodes the inference without erasing it

Bloom production and maintenance are costly: **Programmed Tuber Draw** is normal biological spending for a legitimate process, not pathology, and it may continue while the Bloom does — pausing only while the individual is inhabited, like the rest of its biology (AMO-D087, AMO-D084).

> **Bloom existence proves prior biological capability, not unlimited current reserves.**

So two things must be held apart:

| | Asks |
|---|---|
| **Bloom capability evidence** | did this individual successfully fund a Bloom manifestation? — a historical fact, permanently true once it happened |
| **Current core salvageability** | if this Bloom were destroyed now, could the exposed Tuber continue as a viable persistent individual? — present biology (AMO-D131) |

The first **informs** the second and never determines it. Prior stress, pathology, accumulated draw, damage and deteriorating condition all sit between them, and the exposed core after destruction is the **current** core, not the pre-Bloom one. Bloom does not make the individual's history disappear: maturity, lineage, condition, prior cycles and any pathology all persist, and destroying a Bloom refunds none of what producing it cost (AMO-D137).

**v0 direction, stated cautiously:** a normal Bloom Amorpho should *usually* imply a substantial, rescue-relevant core. It is deliberately **not** made an unconditional law, because severe direct core injury, extraordinary depletion, pathology or other exceptional biology may leave less — or nothing worth recovering. What is canonical is the asymmetry: **Bloom substantially raises confidence that meaningful core value exists, without guaranteeing it.**

## 7. Combat and destruction

Bloom fights do **not** default to destruction. The ordinary resolution families remain fully authoritative: a Bloom Warden may surrender, escape, withdraw consciously, or see the objective resolve, all before any body is lost ([36](36_COMBAT_RESOLUTION_SURRENDER_ESCAPE_AND_WITHDRAWAL_V0.md), AMO-D124–AMO-D127). A valuable core removes none of those exits, and **no stronger surrender penalty or special Bloom rule is introduced** — doc 36's preservation logic simply becomes more obviously worth using.

If a Bloom body is destroyed, the existing architecture applies without amendment (AMO-D130, AMO-D118):

```text
BLOOM BODY DESTROYED → embodiment ends
   → the actual current core is exposed at that physical location
   → Tuber Core Viability is evaluated from actual persistent state
   ├── viable → living, immobile, non-playable Tuber + its Anchor remain on site
   └── non-viable → the persistent individual is lost; the Anchor may remain alone
```

**No Bloom loot rule exists.** Nothing teleports, nothing is generated, and nothing is awarded automatically to whoever won: what lies there is *the actual persistent Tuber that was inside the Bloom*, and its significance is biological continuity rather than a drop table. A strong signal is also not a guarantee of an intact remainder — destruction may involve direct core injury or catastrophic damage, and **direct Tuber harm remains its own extreme pathway** that this information rule never overrides (AMO-D090). Whoever reaches the remains first may take **physical custody**, which is not ownership, the Warden bond or astral authorisation (AMO-D065, L43).

## 8. Incentives on both sides

The same fact cuts both ways, and the architecture only preserves the tension:

- **The Warden** who embodies a Bloom knowingly carries a persistent core whose existence already signals substantial biological investment into travel, exploration and conflict. That value is no longer safely rooted somewhere. Bloom embodiment is therefore a high-value deployment decision — not universally more dangerous, but differently exposed.
- **An opponent** may reasonably reason that destroying this manifestation is more likely to expose a biologically significant Tuber than destroying an apparently fresh early Leaf. No reward, drop probability, aggression rule or AI utility follows, and nothing says hostile actors attack Blooms.

Risks genuinely invert rather than rank:

| | Fresh early Leaf | Bloom |
|---|---|---|
| **Body** | possibly excellent, minimally worn | a specialized, exceptional manifestation |
| **Core evidence** | weak; may be deeply depleted (AMO-D136) | substantial prior capability indicated |
| **If destroyed** | may leave no living Tuber at all | more likely to leave something worth recovering |
| **Owner exposure** | extreme total-loss risk, low capture value for an enemy | stronger survival prospects, higher expected capture or rescue value |

Neither is simply safer, neither is optimal, and no strategy is ranked. A Bloom Warden may also knowingly escalate to destruction and risk the body, the exposed core and possible loss of custody — there is no forced surrender and no morality system (AMO-D127).

Bloom is therefore already strategically distinct **before** move design: through its persistent biological prerequisite, the core information it carries, the stakes of its destruction and the value it exposes. Combat differentiation need not rest solely on kits and archetypes (AMO-Q088, AMO-Q109).

## 9. What Bloom is not, in this architecture

Bloom is **not** an active Leaf: it does not perform Active Leaf Productive Return, and its Programmed Draw is expenditure rather than contribution ([39](39_ACTIVE_LEAF_PRODUCTIVE_RETURN_AND_PERSISTENT_TUBER_BENEFIT_V0.md), AMO-D135, AMO-D087). Any future reproductive return is its own architecture and is not designed here.

Bloom is also **not a maturity readout**. Bloom capability depends on the existing maturity architecture, but no Developmental Maturity value is exposed through a Bloom's presence or appearance (AMO-D080, L47, AMO-Q111). And no species ranking is implied: nothing here says that species which bloom larger have better fighters, better cores or rarer remains (AMO-D024, AMO-Q110).

## 10. Worked contrasts

**A — fresh early Leaf.** A Leaf reaches Full Deployment and the Warden inhabits it immediately; the core remains deeply depleted from construction. An opponent sees a pristine Leaf fighter and may *suspect* poor core security without knowing. The manifestation is destroyed: possibly no viable Tuber remains, and the Anchor may lie there alone.

**B — worn productive Leaf.** The same construction, but the Leaf spends meaningful rooted active life and the core becomes robust while the body accumulates environmental wear. The Warden inhabits it later. An opponent sees a damaged Leaf and can infer very little. Destruction exposes a robust Tuber.

**C — Bloom.** The individual reaches the biological capability Bloom requires; the Bloom develops and fully deploys; the Warden inhabits it. An opponent observes the Bloom form and knows a substantial persistent core had to exist for this manifestation to be possible, while its exact current state stays hidden. Combat escalates to body destruction, the actual Tuber is exposed, and its viability follows actual biology rather than any Bloom rule.

**D — Bloom after substantial draw.** The capability was real and the Bloom exists, but normal Programmed Draw has since cost persistent resources. The observer still knows the capability occurred and still cannot know current reserves. Destruction exposes the **current** core, not the pre-Bloom one. **This is why Bloom is information, not knowledge.**

**E — withdrawing to protect the core.** A Bloom Amorpho enters conflict, protection begins to fail, and the Bloom body takes real biological damage. The Warden recognises that continued escalation risks exposing a valuable persistent core, and withdraws consciously. The encounter may be lost; the Bloom and the individual survive. **No special rule was needed** (AMO-D125, AMO-D126).

## 11. Deferred Bloom mechanics and acceptance

AMO-Q088 owns Bloom's content — capabilities, costs, duration and combat role — and AMO-Q107 the eligibility inputs and repeated-Bloom timing, including how much persistent capability Bloom actually requires. AMO-Q086 owns Bloom-specific damage and any recovery response; AMO-Q104 the viability criterion; AMO-Q117 direct Tuber susceptibility and the exposed core; AMO-Q106 and AMO-Q110 maturity representation and species interpretation; AMO-Q111 what a player perceives; AMO-Q079 reproduction; AMO-Q008, AMO-Q091 and AMO-Q093 capture, custody and ownership; AMO-Q109 combat mapping. No new question was required.

| Check | Result |
|---|---|
| Leaf uncertainty | A battered Leaf supports no reliable inference about core viability (AMO-D134). |
| Bloom signal | Bloom existence is evidence of substantial prior persistent capability (AMO-D142). |
| No perfect knowledge | It reveals no present mass, condition, reserves, pathology or salvageability. |
| Programmed Draw | Capability evidence survives as a historical fact while current reserves may have changed (AMO-D087). |
| Same physical core | Tuber and Anchor travel inside the Bloom exactly as inside a Leaf (AMO-D143). |
| Destruction | Exposes the actual current core through the existing architecture (AMO-D130). |
| No loot generation | Nothing special is spawned because the manifestation was a Bloom. |
| No guarantee | Bloom implies neither a pristine nor an invulnerable core (AMO-D144). |
| Tactical asymmetry | A fresh early Leaf and a Bloom carry different expected core-risk profiles. |
| Ordinary exits | Surrender, escape, withdrawal and objective resolution all remain available. |
| Custody | Recovering exposed remains is custody, never ownership (AMO-D065). |

**Result:** the flower is the one part of this architecture that talks. It cannot say how much is left, what has been spent, or whether anything could be saved today — but it says that this individual had already become substantial enough to make it, and that is more than a Leaf has ever been able to tell anyone.
