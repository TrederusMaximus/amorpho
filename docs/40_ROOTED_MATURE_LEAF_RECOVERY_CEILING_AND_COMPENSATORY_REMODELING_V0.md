# 40 — Rooted Mature Leaf Recovery Ceiling and Compensatory Remodeling, v0

**Status:** qualitative biological-design pass using owner-supplied domain direction. It specifies how a damaged mature Leaf rehabilitates during rooted life and what bounds that rehabilitation. It defines no percentage, rate, formula, threshold, ceiling value, vascular physiology, species-specific response, combat statistic, shader or implementation, and it asserts no real botanical mechanism.

> **A mature Leaf cannot rebuild what it lost, but it can reorganize what remains and recover far more function than its scars suggest.**

## 1. Purpose and scope

[24](24_SAME_PHASE_LEAF_RECOVERY_V0.md) established that same-phase recovery means stabilization and compensation rather than regrowth (AMO-D094). This pass gives that its architecture and separates seven ideas that had been travelling together: **Structural Stabilization**, **Scarring**, **Compensatory Remodeling**, **Functional Recovery**, **Recovery Ceiling**, current **Leaf Functional Capacity**, and **Remaining Productive Opportunity**.

It applies to any **fully deployed mature Leaf**, however it came to be damaged — healthy and later injured, [imperfectly deployed](32_IMPERFECTLY_DEPLOYED_MATURE_LEAF_STABILIZATION_OR_DECLINE_V0.md) and already compromised, harmed by environment, pests or mechanical events, or damaged while embodied in combat ([35](35_COMBAT_PROTECTION_MANIFESTATION_BODY_DAMAGE_AND_BIOLOGICAL_PERSISTENCE_V0.md)). **Damage origin changes nothing here**: one mature recovery architecture serves all of them, and no combat-specific healing subsystem exists.

Bloom is **out of scope**. The no-reset principle plainly applies to it, but Bloom-specific recovery deserves its own design if it is ever needed (AMO-Q088).

## 2. Rehabilitation needs biology to be running

Ordinary recovery is one of the processes suspended while the individual is inhabited (AMO-D084, AMO-D123). So:

```text
body damage while embodied  → damage persists; stabilization and remodeling do not progress
   ↓  Warden exits, individual roots
rooted biological life      → stabilization, scarring, compensation and Functional Recovery may proceed
```

Rehabilitation therefore waits for rooting while **World time does not wait**: local conditions and seasonal opportunity may already have changed during the embodiment ([42](42_WORLD_TIME_SEASONAL_OPPORTUNITY_AND_EMBODIMENT_V0.md), AMO-D145, L64).

**Rooting is not healing.** It re-enables the processes; it does not perform them. What actually happens then depends on current Leaf condition, how much viable architecture survived, Environmental Fit, persistent biological condition and remaining biological opportunity — with no rate and no guarantee (AMO-D033, L27).

## 3. Lost architecture stays lost

If mature architecture is physically gone, it does not reappear: a broken-off mature part is not reconstructed, and same-phase recovery never rewinds the Leaf to its pre-damage form (AMO-D094).

> **Mature recovery preserves and reorganizes surviving architecture; it does not reconstruct lost mature architecture.**

Magic changes nothing about this. Embodiment does not heal, astral exit and re-entry repair nothing, and magical healing may support the fighter without rebuilding mature structure (AMO-D072, AMO-D086, L48, L49, L50).

## 4. Structural Stabilization

> **Structural Stabilization** is the process by which surviving damaged architecture becomes mechanically and biologically stable enough to persist rather than continuing to fail.

Conceptually it may include damaged areas becoming secured, the progression of a break being arrested, surviving connections being protected, and scarred interfaces becoming stable. No botanical mechanism is specified.

Stabilization is valuable **before** any function returns, because it can prevent further structural deterioration — and therefore prevent further loss of what could still be recovered (§7).

## 5. Scarring

A mature Leaf may carry permanent visible consequences of damage. Scars remain part of the manifestation, persist through rooted life and through any later embodiment, and survive recovery itself (AMO-D134).

> **Scarred does not mean nonfunctional**, and scars are not achievements. A scarred Leaf may function very well, function poorly, or be close to Collapse; current biology decides, never the scar count, and no scar confers any bonus (L51).

## 6. Compensatory Remodeling

> **Compensatory Remodeling** is the mature Leaf's biological reorganization of surviving structures so that the remaining architecture can carry more useful function than it could immediately after the damage.

It is **not** regrowth of missing architecture, restoration of original geometry, or magical healing. It is **better use of what remains**:

> Recovery may change how effectively surviving architecture works without restoring the architecture that was lost.

Surviving regions may come to carry a greater share of the Leaf's total useful work than they did before the damage. That is described in game-biological terms — compensatory reinforcement, remodeling, functional rerouting — and **no real physiological mechanism is claimed or researched** (AMO-D024).

**Compensation has limits.** It never makes a damaged Leaf function better than its undamaged architecture could have, and damage confers no biological advantage. The Leaf becomes effective *relative to what remains*.

*Presentation extension point, not canon:* compensated tissue may later be made visually legible — stronger-looking surviving veining, thickened or reinforced transitions, more vigorous remaining functional regions — and distinguishable from fresh injury, from terminal yellowing and from pristine structure. No appearance, rendering or interface behaviour is defined (AMO-Q111).

## 7. Functional Recovery and the Recovery Ceiling

Functional Capacity may fall sharply at the moment of serious damage and then recover substantially once rehabilitation runs: stabilization stops further loss, and remodeling improves what surviving structure can do.

> **Severe visible damage does not imply permanently equally severe functional loss.**

Two further separations carry the architecture:

| | Describes |
|---|---|
| **Structural Integrity** | the surviving physical architecture and its condition |
| **Leaf Functional Capacity** | how much useful biological work the Leaf can currently perform |
| **Recovery Ceiling** | the highest mature Functional Capacity this particular Leaf could still plausibly regain from its surviving architecture and condition during this phase |

Neither is derived from the others, and **current function is not recoverable function**: a freshly damaged Leaf may show low current capacity and a substantially higher ceiling, and rehabilitation is what moves the first toward the second. That distinction is what makes an early withdrawal decision meaningful rather than sentimental (§9).

**Damage can permanently lower the ceiling.** Because lost architecture is not rebuilt, some potential is simply gone for this manifestation. The reduction is **not proportional to visible damage**: compensation may let surviving structure support disproportionately useful function, while a small but strategically placed loss may cost a great deal. No damage-to-ceiling mapping exists.

**v0 direction on the ceiling's own movement:** rehabilitation moves current function toward what surviving biology can still support; it does **not** restore ceiling already lost merely through time. Whether any biological process can ever raise a reduced ceiling within the same phase is left open (AMO-Q103).

**A ceiling belongs to its manifestation only.** When the Leaf ends, its ceiling ends with it: a later manifestation is newly constructed architecture and does not inherit the old one's missing structure, while persistent Tuber consequences carry forward on their own terms (AMO-D074, AMO-D113).

## 8. Appearance, and fresh versus compensated damage

Three things stay distinct: **appearance**, **current Functional Capacity** and **Recovery Ceiling**. A Leaf may be visually heavily scarred, mechanically stable and functionally strong, all at once (L51, AMO-D134).

This produces a distinction the domain model should be able to express even if an interface later hides it:

| | May show |
|---|---|
| **Fresh injury** | instability, severe impairment, low current capacity, recovery potential not yet realized |
| **Old stabilized, compensated injury** | equally dramatic scars, stable structure, substantially recovered capacity |

Identical visible missing architecture can therefore support very different current function. No formal state, field or player inspection mechanic is created.

## 9. Environmental Fit, withdrawal and overuse

**Fit decides how much of the remaining potential is realized.** Favourable rooted conditions can support stabilization, compensation and functional recovery; poor conditions may slow or prevent useful rehabilitation, allow continued decline, and push toward Functional Collapse ([12](12_ENVIRONMENT_AND_FIT_MODEL_V0.md), [33](33_MATURE_LEAF_FUNCTIONAL_COLLAPSE_BOUNDARY_V0.md)). But:

> **Excellent conditions help the Leaf realize what remains recoverable; they cannot recreate mature architecture that no longer exists.** Good environment is not a pristine reset.

The combat consequence is the sharpest one in this pass. A further body-reaching effect may lower current capacity, destabilize structure, destroy surviving architecture **and lower the remaining ceiling**. So continuing a fight can cost more than tonight's performance:

> A Warden may withdraw not because the Amorpho can no longer fight, but because further damage could permanently reduce what this Leaf will ever be able to recover to.

That links Conscious Withdrawal directly to biology ([36](36_COMBAT_RESOLUTION_SURRENDER_ESCAPE_AND_WITHDRAWAL_V0.md), AMO-D125). The mirror case is **overuse**: staying embodied through repeated encounters suspends rehabilitation throughout while damage accumulates, so both current function and the attainable ceiling may fall before any recovery is ever attempted (AMO-D123, AMO-D136). No interface, warning or readout is designed; the Warden may also have no precise knowledge of the ceiling, and the decision is made under uncertainty (AMO-D134).

## 10. Productive Return and remaining opportunity

Once rooted and biologically active, recovered function feeds the existing accounting: current Functional Capacity, Fit, condition and Remaining Productive Opportunity together support **Active Leaf Productive Return** ([39](39_ACTIVE_LEAF_PRODUCTIVE_RETURN_AND_PERSISTENT_TUBER_BENEFIT_V0.md), AMO-D135). Recovery matters because it can restore some of the Leaf's ability to work for the Tuber.

**Recovery restores future capability, not past opportunity.** Productive opportunity that passed while the Leaf was embodied, damaged or rehabilitating is not returned (AMO-D137, L61).

**Recovery potential and remaining opportunity are independent axes**, and all four combinations are legitimate:

| | High remaining opportunity | Low remaining opportunity |
|---|---|---|
| **High recovery potential** | the most valuable rehabilitation case | biology recovers well with little useful season left to spend it in |
| **Low recovery potential** | much season remains but function may not return sufficiently | replacement or retreat may become more attractive downstream (AMO-Q101) |

No decision matrix, weighting or optimum follows. Late rehabilitation is not automatically pointless either: it may stabilize the manifestation, protect the individual from worse consequences, contribute some remaining return and allow a safer transition. How much is AMO-Q116's, and the interaction between a paused individual and external world time remains where AMO-D136 left it (AMO-Q004, AMO-Q074).

Two domains also stay unmerged: a Leaf may recover enough function to be biologically valuable while the Warden still declines to risk it in combat again, and any future combat-state recovery is separate from biological rehabilitation (AMO-D121). A biologically imperfect Leaf is not thereby tactically weak; that mapping remains open (AMO-Q109).

## 11. The Collapse boundary

Before **Collapse Commitment**, rehabilitation may avert loss entirely: serious damage does **not** imply inevitable Collapse, and a significantly damaged Leaf may stabilize, regain function and never cross the boundary (AMO-D114).

At and after Commitment, the current Leaf's fate is irreversible and good conditions no longer return it to viable active status (AMO-D115). **Recovery Ceiling for continued active-Leaf viability therefore stops mattering once commitment is crossed**, and no terminal recovery exists. If commitment happened while embodied, terminal progression stays paused for as long as the embodiment continues and resumes when rooted life does — which reopens nothing (AMO-D117, [34](34_EMBODIMENT_ACROSS_TERMINAL_MANIFESTATION_COLLAPSE_V0.md)).

Recovery failure may instead contribute downstream: damage, weak stabilization, low capacity, lost opportunity and insufficient return can end in a harmful persistent outcome — but where that boundary lies is **AMO-Q118's**, and this pass stops before it (AMO-D138). Severe Leaf damage is not automatically Pathological Tuber Impact, and successful rehabilitation is one of the things that can keep it from becoming so (AMO-D092).

Persistent Tuber condition may influence how well a Leaf can stabilize and recover, without owning the damage: immediate mature damage stays Leaf-owned and no second Tuber debit is created (AMO-D111, L55). Whether rehabilitation itself carries a biological demand is **left open rather than denied** (AMO-Q103), and no healing currency — repair points, regeneration energy, recovery charges, a medicine meter — may be introduced.

## 12. Canonical flow

```text
MATURE LEAF
   ↓ damage, from any origin
SURVIVING ARCHITECTURE
   → current Structural Integrity · current Functional Capacity · recovery potential
   ↓ Warden exits; rooted biology resumes
STRUCTURAL STABILIZATION + SCARRING + COMPENSATORY REMODELING
   ↓ under Environmental Fit and condition, over biological time
FUNCTIONAL RECOVERY
   ↓
CURRENT FUNCTION APPROACHES A REDUCED RECOVERY CEILING
   ↓
PRODUCTIVE RETURN MAY RESUME, bounded by remaining opportunity
   ↓
remaining seasonal outcome
```

No box is a quantity and no arrow implies a rate.

## 13. Worked traces

**A — severe combat damage, strong rehabilitation.** A mature Leaf in good condition is inhabited and takes serious body-reaching damage; meaningful mature architecture is permanently lost, and the Leaf stays above Functional Collapse. The Warden withdraws consciously, relocates to a favourable place and roots. Biology resumes: structure stabilizes, scars form and remain, compensatory remodeling develops, and Functional Capacity recovers substantially. The Leaf is still visibly heavily damaged and again performs useful biological work — with a Recovery Ceiling below its undamaged potential. **Flagship outcome.**

**B — the same-looking Leaf, poor rehabilitation.** Similar visible damage, but rooted under poor Fit. Stabilization is insufficient, functional recovery stays limited, decline continues, and Functional Collapse later becomes possible. **Appearance did not determine the outcome; conditions and biology did.**

**C — moderate damage, near-ceiling function.** Some architecture is lost, rehabilitation begins promptly, stabilization succeeds and compensation is effective. Current function recovers close to what remains attainable, the Leaf stays scarred, and Productive Return remains substantial.

**D — high potential, little opportunity.** A damaged Leaf could recover substantially, but roots very late in its useful seasonal opportunity. Functional Recovery genuinely occurs and little productive opportunity remains to use it. **Biological rehabilitation was real; seasonal value was bounded by opportunity** (AMO-D137).

**E — repeated combat before recovery.** Body damage occurs and the Warden does not root. Rehabilitation stays suspended while further encounters add damage; current capacity falls further and recoverable architecture is destroyed, so the remaining ceiling falls too. The Warden eventually roots and rehabilitation proceeds — to a lower attainable outcome than was available earlier. **This is the cost of overuse.**

**F — the scarred veteran, re-embodied.** A previously damaged Leaf was rooted, stabilized and compensated, and significant function returned. Later the gates permit re-entry and the same Leaf is inhabited again: scars and structural losses are all still there, and its functional state reflects successful rehabilitation rather than a pristine reset. **There is no fresh body between fights** (AMO-D134, L61).

**G — damage crosses Collapse Commitment.** A badly damaged Leaf initially retains theoretical recovery potential, but further deterioration removes any viable active-role trajectory. Commitment occurs, recovery no longer offers a way back to active viability, and the terminal architecture takes over ([33](33_MATURE_LEAF_FUNCTIONAL_COLLAPSE_BOUNDARY_V0.md), [34](34_EMBODIMENT_ACROSS_TERMINAL_MANIFESTATION_COLLAPSE_V0.md)).

## 14. Deferred quantitative biology and acceptance

AMO-Q103 owns recovery extent and rates, how the ceiling is represented, how damage changes it, whether anything can raise it within a phase, any biological demand rehabilitation makes, and how stabilization, scarring and remodeling are represented. AMO-Q086 owns the structural-to-functional relationship. AMO-Q111 owns what a player perceives, including any visual distinction between fresh, compensated and terminal states. AMO-Q116 owns productive integration; AMO-Q118 the persistent-loss boundary; AMO-Q104 viability; AMO-Q101 and AMO-Q084 routing; AMO-Q109 combat mapping; AMO-Q088 Bloom. Species interpretation requires approved input, not research (AMO-D024). No new question was required.

| Check | Result |
|---|---|
| Lost architecture | Never simply regrows during this phase (AMO-D094, AMO-D139). |
| Stabilization | Surviving damaged structure can become stable, which itself protects remaining potential. |
| Scarring | Permanent for this manifestation; no functional verdict and no bonus (L51). |
| Functional Recovery | A scarred Leaf can regain substantial useful function (AMO-D140). |
| Ceiling | Bounded by surviving architecture; damage can permanently lower it, non-proportionally (AMO-D141). |
| Current versus ceiling | Freshly damaged means low current function with a possibly much higher ceiling. |
| Repeated damage | Can lower both current function and remaining recoverable function. |
| Good Fit | Realizes remaining potential; never recreates lost architecture. |
| Poor Fit | Potential may go unrealized and decline may continue. |
| Productive Return | Recovered function can support future return, never past opportunity (AMO-D137). |
| Opportunity | Recovery can succeed biologically and still be seasonally worth little. |
| Collapse | Before Commitment recovery may avert it; after Commitment there is no way back. |
| Same body | A re-embodied Leaf carries its scars, stabilized areas and actual function. |
| Appearance | Heavily scarred may be mechanically stable and functionally strong. |

**Result:** rehabilitation in Amorpho is reorganization, not repair. A Leaf that loses part of itself keeps the loss, stabilizes what survived, learns to work with less, and can come back biologically powerful while looking permanently marked — up to a ceiling that every further injury lowers, and never past the one it has left.
