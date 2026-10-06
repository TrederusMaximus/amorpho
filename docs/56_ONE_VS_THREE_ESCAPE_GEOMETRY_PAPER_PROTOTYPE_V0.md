# 56 — One-versus-Three Escape Geometry: Paper Prototype, v0

**Status:** test design — a disposable tabletop prototype of the spatial assumption behind AMO-D174–AMO-D176 and L74 ([55](55_MULTI_ATTACKER_ENCOUNTERS_ESCAPE_AND_ANTI_DOGPILE_PRINCIPLES_V0.md)). It adds no decision, law or rule, and nothing in it is a combat mechanic. **It has not been run, and no result is known.**

> **Does geometry alone let a lone defender sometimes break away from three — without making three attackers barely more dangerous than one?**

## 1. Purpose

Doc 55 rests on an untested premise: that embodied space — congestion, obstruction, enclosure, pursuit and the individual exposure of overcommitted attackers — can give an outnumbered defender real escape chances **without any anti-gank buff**, while coordinated numbers stay genuinely dangerous. This document designs the cheapest test that could show the premise is wrong.

The chain under test:

```
GROUP PRESSURE → OVERCOMMITMENT → INDIVIDUAL EXPOSURE → GROUP REACTION → ESCAPE OPENING
```

## 2. Hypotheses

- **A** — three attackers meaningfully pressure one defender.
- **B** — good attacker coordination is substantially stronger than poor coordination.
- **C** — physical geometry prevents all three attackers from applying perfect pressure at once.
- **D** — a defender can sometimes create an escape opening by positioning.
- **E** — a defender can sometimes create that opening by exposing or isolating one attacker.
- **F** — none of this guarantees escape.
- **G** — no attacker count alone produces certain containment.

**Not tested:** real-time feel, actual attacks, timing, movement speed, animation, camera, input, damage balance. **The test is built to be able to fail**, and failure is informative.

## 3. Scope and non-goals

No species, Amorpho attributes, stats, health, damage values or dice. No randomness: outcomes come from the players' decisions, and the facilitator deliberately sets up contrasting cases. One board, one Defender token, three Attacker tokens, one or two terrain features — coins on paper are enough.

## 4. Prototype-only instruments

> **PROTOTYPE-ONLY TEST INSTRUMENTS — NOT CANONICAL COMBAT MECHANICS.** Nothing in this section enters DECISIONS.md, describes future controls, or implies zones, tiles, turns, adjacency, capacity, zones of control, flanking or support radii exist in the game. Their only job is to make pieces move so that geometry can be observed.

Some instruments use small counts — how many bodies a zone holds — because a board cannot move otherwise. They are board properties, not stats.

**I1 — Zones.** The board is a handful of named zones joined by edges. A body occupies one zone. **Open** zones hold up to three bodies — so at most two attackers beside the defender; a **narrow** zone holds one body of any side; **blocked** terrain holds none. A full zone cannot be entered by anyone — allies included. *(Stands in for congestion and obstruction.)*

**I2 — Rounds.** Each round the Defender takes one action, then each Attacker takes one action in the order the attacking side chooses.

**I3 — Contact.** Bodies in the same zone are **in contact**. Attackers in a zone simply occupy it; the defender may still move into an attacker's zone if there is room, which puts them in contact.

**I4 — Pinned.** A defender in contact with **two** attackers cannot Reposition. *(Stands in for physical containment by bodies.)*

**I5 — Supported / isolated.** An attacker is **supported** when another attacker is in the same or an adjacent zone, and **isolated** otherwise. Being isolated changes nothing by itself; it only means no ally is placed to Cover (A5).

**I6 — Body-risk track.** Each body's state is one of: **Protected → Exposed → Body damage suffered → Seriously endangered.** These are facilitator declarations, not hit points. When any body reaches *Seriously endangered*, **stop the scenario and record it** — destruction is never played (doc 55 §12, trace B).

**I7 — Escape.** If the Defender **starts its action in an exit zone with no attacker in that zone**, it may Leave the board: escape succeeds. *(Stands in for "enough separation that no attacker keeps immediate containment".)*

**I8 — Enclosure.** The Defender is **enclosed** when every zone it could move into is full, blocked, or occupied by an attacker. Recorded, not scored.

**I9 — Stalemate.** If the same position recurs, stop and record a stalemate.

### Actions

| Action | Who | Effect |
|---|---|---|
| **Reposition** | any | move to an adjacent zone with room (not if pinned) |
| **Pressure** | any, on a body in the same zone | the target's body-risk track advances one step |
| **Shove** | any, on a body in the same zone | the target is pushed into an adjacent zone of the shover's choice that has room, **loses its next action** and is now at least *Exposed* |
| **Cover** | attacker, on an ally in the same zone | the ally's track does not advance from the next Pressure against it |
| **Hold** | any | stay; do nothing else |
| **Withdraw** | attacker | the attacker's Warden decides to stop; the token leaves by Repositioning away and takes no further part |

Shove is deliberately strong and Cover deliberately costly — covering spends an action that could have pressured or held. **Both are assumptions under test**; §14 requires sensitivity runs without them.

## 5. Board

```
                 EXIT-N
                   |
       NW -------- N -------- NE
       |           |           |
       W  -------- C -------- E -------- EXIT-E
       |           |           |
       SW        ROCKS        SE
       |        (blocked)
      GAP  (narrow)
       |
     EXIT-S
```

Edges are only the lines drawn. ROCKS is blocked; GAP is narrow; every other zone, exits included, is open. Three exits lie in different directions: one wide (EXIT-E, reached through E), one central (EXIT-N, through N), and one only through the narrow GAP (EXIT-S).

**Open-terrain variant (Scenario 6):** ROCKS becomes an open zone joined to C, SW and SE, and GAP becomes open.

**Stake.** The Defender begins at C, where it was contesting something — doc 54's access stake. Choosing to escape concedes it; record when the Defender makes that choice.

**Players.** Ideally two people: one plays the Defender, one plays all three Attackers. The facilitator rules on instruments and records. Attackers' Wardens may Withdraw when their own token takes body damage; the Attacker player must decide that as that Warden would.

## 6. Scenario 1 — poor coordination

**Setup.** Defender at C. Attackers at NW, NE and SW.
**Attacker policy (scripted, to model poor coordination):** each attacker on its action moves along the shortest path toward the Defender; if in contact, it Pressures. No holding of routes, no Cover, no thought about spacing.
**Observe:** Do attackers obstruct one another at full zones? Duplicate coverage? Does one overcommit into an isolated position? Can the Defender exploit it and reach an exit?

## 7. Scenario 2 — coordinated enclosure

**Setup.** Same start.
**Attacker policy:** played by a person told to keep spacing, cover different routes, avoid crowding, pin when possible, and Cover each other.
**Observe:** Is pressure clearly higher than in Scenario 1? Is escape substantially harder? Does coordination *feel* like skill? Is escape still conceivable? **Do not steer toward an escape.**

## 8. Scenario 3 — isolation counterplay

**Setup.** Defender at C. One attacker at N, one at E — two routes covered. The third attacker starts at SW and must commit into W to close the last open direction; when it arrives it is **isolated** (nobody in W, NW, C or SW).
**Defender's attempt:** move into W, Shove or Pressure that attacker, threaten its body.
**Then ask the Attacker player:** *what do you do?* — keep the enclosure and let that member suffer; break spacing to Cover or support it; rotate another attacker; or let a route open.
**Observe:** is there a genuine trade-off? **This is the central test of the swarm idea.**

## 9. Scenario 4 — the group ignores the exposed member

**Setup.** As Scenario 3 at the moment the third attacker is Exposed and in contact with the Defender.
**Attacker policy:** maintain pursuit and route coverage; nobody helps.
**Facilitator:** if the Defender's next Pressure lands, declare *Body damage suffered* on that attacker and ask its Warden whether they continue or Withdraw.
**Observe:** Is ignoring the member a real cost? Can the Defender exploit it without needing to "defeat" anyone? Does the group still keep its advantage?

## 10. Scenario 5 — the group protects the exposed member

**Setup.** The same moment.
**Attacker policy:** preserve the teammate — move an ally into W to Cover, or open spacing so it can retreat.
**Observe:** Does pressure on the Defender fall? Does a route open — EXIT-N through N, EXIT-E through E? Does the group's geometry reorganize in a meaningful way?

## 11. Scenario 6 — open terrain

**Setup.** Open-terrain variant; Defender at C; attackers start spread around it.
**Run** both the scripted poor policy and the coordinated policy.
**Observe:** Does geometry-based escape become too weak when terrain offers no help? **If escape only ever works through the narrow GAP, record that as a major limitation of the premise.**

## 12. Scenario 7 — terrain-assisted defender

**Setup.** Standard board; Defender begins at SW, near GAP.
**Observe:** Does the narrow GAP let the Defender limit simultaneous pressure — attackers forced into a line, one at a time? Can the Defender use it to reach EXIT-S? Does terrain become **too** powerful, deciding outcomes regardless of what anyone does?

## 13. Reinforcement thought test

Place a fourth token **off the board**, beyond one exit, and do not let it act until it has entered through that exit and moved zone by zone. Ask: *what must happen in World space before this attacker can contribute?* — and record whether its late arrival changes the picture. It never appears in a zone it did not travel to. Reinforcement is physical arrival (AMO-D176).

## 14. Observations to record

After **every** scenario, write down — in words, not scores:

- **The main question:** *what produced the outcome — numbers alone, or numbers plus geometry, coordination and decision quality?*
- **Coordination quality:** poor, competent or strong — and what physically differed: spacing, route coverage, overcommitment, support, pursuit discipline.
- **Defender decisions:** could the Defender meaningfully choose where to move, which attacker to pressure, when to give up the stake, which exit to aim for, when to exploit an exposed attacker? *If the Defender's choices did not matter, that is a failure.*
- **Isolation:** did threatening one exposed attacker force the group into a meaningful decision — support it and release pressure, or abandon it and accept its body damage? *If the group lost nothing by ignoring it, the swarm counter-dynamic may not be viable without more mechanism.*
- **Congestion:** did the attackers actually get in each other's way? *If three attackers could take perfect independent positions at no cost, the congestion premise is weak.*
- **Coordination:** was the coordinated group visibly more effective than the scripted one? *If not, the group-skill premise is weak.*
- **Escape:** was there at least one believable route by which a skilled Defender broke contact? *If never, AMO-D174 may need a further mechanism — record it; do not invent it here.*
- **Escape too easy:** could the Defender escape so reliably that three felt barely worse than one? *If yes, that fails too.*

**Instrument sensitivity — required.** Re-run Scenarios 2, 3 and 6 at least once each with one instrument changed: Shove without the lost action; pinning by a single attacker; and Cover removed. **If a conclusion flips when an instrument changes, record it as driven by the instrument, not as evidence about the architecture.**

Record verbatim what each player said they were trying to do.

## 15. Success criteria

- **A** — three attackers are clearly more dangerous than one.
- **B** — good coordination produces substantially stronger containment.
- **C** — poor coordination produces exploitable spatial mistakes.
- **D** — Defender decisions change survival chances.
- **E** — isolating one attacker can force a group-level response.
- **F** — protecting an exposed member can weaken enclosure elsewhere.
- **G** — ignoring an exposed member can carry a real individual biological consequence.
- **H** — escape can happen without defeating any attacker.
- **I** — escape is not guaranteed.
- **J** — no numerical anti-gank mechanic was needed.

## 16. Failure criteria

| | Failure |
|---|---|
| **A** | Three attackers produce certain containment whatever the Defender decides. |
| **B** | Three attackers add almost no pressure. |
| **C** | Congestion and obstruction never matter. |
| **D** | Coordination quality does not matter. |
| **E** | Isolating one attacker creates no meaningful group decision. |
| **F** | The Defender can always escape once it chooses to. |
| **G** | The Defender can never escape once surrounded. |
| **H** | The only way to open a route is to "defeat" an attacker. |
| **I** | Terrain decides the outcome regardless of anyone's positioning. |
| **J** | The test only works with a hidden anti-gank bonus. |

A and G are near-relatives on one side, B and F on the other; the premise needs the space between them.

## 17. Interpretation limits

Even if every success criterion holds, the most the test supports is:

> **The geometry hypothesis appears plausible enough to justify designing Movement, Defence and Protection around it.**

It does **not** show that Amorpho combat is solved, that it is fun, or that real-time play behaves like a turn-based board. If it fails, the conclusion is narrower than despair: *this particular geometric mechanism, as currently conceived, is insufficient* — recorded through AMO-Q027 and AMO-Q028 before any design reacts. A turn structure is far kinder to deliberate positioning than real time will be, and that bias must be kept in mind when reading any result.

## 18. Requirements exported to future Movement and Defence design

Whatever the result, the test design already implies requirements that later combat design must meet or consciously reject. None is a mechanic; each is recorded against its owner:

- the defender must be able to **reposition under pressure**, not only while free (AMO-Q027, AMO-Q023);
- attackers must **physically occupy and control useful space**, so that bodies can block routes and each other (AMO-Q027);
- defence and targeting **cannot assume one opponent** (AMO-Q023, AMO-Q024);
- protection may need some **directional** meaning under pressure from several sides (AMO-Q109);
- movement must allow a **local isolation** of one attacker to arise and be exploited (AMO-Q027);
- **pursuit must commit space** — chasing should cost position as well as gain it (AMO-Q028);
- some way to **break contact** that is neither instant nor impossible must exist, or Scenario 6's open-ground case cannot be survived (AMO-Q028, AMO-D175).

**In short:** a board, four coins and two people for an hour — enough to learn whether the outnumbered-escape idea has a spatial mechanism under it, or only a principle.
