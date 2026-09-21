# 05 — The Reality Gate

**Status:** simplified at foundation closure (AMO-D026). The gate is a file-based inbound boundary with documented validation rules. No tooling exists. The approved species input contains no species yet.

> The game does not need to know where reality came from. It only needs the approved representation of the reality it actually uses.

## 1. The flow

```
  external curated master data        outside Amorpho — not Amorpho's concern
            │
            ▼
  approved export file                e.g. amorphophallus_species.csv
            │
            ▼   REALITY GATE: validate against the input contract, then accept
  data/input/                         accepted approved input, versioned in Git
            │
            ▼   derived by the future implementation (not decided)
  internal representation ("canon")
            │
            ▼
  game systems
```

Knowledge moves one way only. Nothing flows back through the gate: Amorpho does not report, sync or export through it (AMO-D017).

Once an approved import is accepted, the running game must not depend on continued access to the external master-data system, or to any website or service (AMO-D018).

## 2. Amorpho does not research botany

Detailed research about *Amorphophallus* happens outside this repository, where a comprehensive master list is built and maintained (AMO-D024). Amorpho is **not**:

- a scientific botanical master database;
- a taxonomy research system;
- a literature database or paper archive;
- a taxonomic dispute-resolution system;
- a botanical evidence-management platform;
- a mirror of external databases.

Amorpho does not know who maintains the master list, which organisations or databases were consulted, which papers were used, or where the evidence is stored. From Amorpho's perspective there is simply **an approved input file supplied from outside the repository**. That is the entire dependency boundary.

## 3. Master knowledge is not game input

The external master list may eventually contain taxonomy, synonyms, original descriptions, literature, distributions, environmental information, morphology, hybrid evidence, cultivation knowledge and more. Amorpho does **not** import it wholesale. Only the facts the game demonstrably needs cross the boundary (AMO-D025).

This keeps licensing exposure, data duplication, external dependencies, scientific complexity, migration burden and coupling between research and game architecture to a minimum.

| Game need | Input | Status |
|---|---|---|
| which species exist, and what they are currently called | `amorphophallus_species.csv` | contract defined; header only |
| which species pairs may hybridize | `amorphophallus_hybrid_compatibility.csv` | contract documented; file not created |
| environmental facts for Environmental Fit | — | deferred until the environment model is designed |

The exact file contracts and validation rules are in [`data/input/README.md`](../data/input/README.md).

## 4. What the gate is, and what it is not

The gate **is**: an approved file, a set of documented validation rules, and a Git commit that accepts the file into `data/input/`.

The gate is **not**: an external API, live synchronisation, HTTP requests, a database integration, a message queue, a remote dependency, a research-source adapter, evidence storage, or a place for external-system identifiers. None of these is introduced without a demonstrated need and a decision.

## 5. Accepting an approved export

1. Receive the approved export file from outside the repository.
2. Validate it against the rules in [`data/input/README.md`](../data/input/README.md).
3. Review the difference from the currently accepted file: new IDs, changed names, and anything missing.
4. Accept it by committing it to `data/input/`, in a commit whose message says what changed. Git history is the audit trail; no extra import metadata is kept for now.

If a file fails validation, it is not accepted. Fixing it is the job of the external process, which then supplies a corrected export.

## 6. Stable species identity and taxonomic change

Each species has a permanent, opaque Amorpho species ID of the form `AMO-SP-000001` (AMO-D022). The ID is the game's long-term identity for the species; the scientific name is mutable metadata attached to it.

A species may first be accepted as `AMO-SP-000042,Amorphophallus exampleensis` (a fictional illustration). If a later approved export changes the name, the identity is still `AMO-SP-000042`. This protects savegames, individual plant records, genealogies, lineages, ownership, world history, combat history and long-running persistent worlds.

Deciding whether a name is scientifically correct is not Amorpho's job; Amorpho trusts the approved input. What the *game* does when a species leaves the approved list, or when the external process later treats two species as one or one as two, is a game design question (AMO-Q016).

## 7. Hybrid compatibility

For gameplay, hybrid compatibility is a **symmetric species-pair relationship** (AMO-D027):

- `A + B` is either an **approved compatible pair** or **not approved as compatible**.
- Directional detail — which species was the seed parent, whether reciprocal crosses were documented, other evidence — stays in the external research process.
- Absence of approval means "Amorpho has no approved compatibility entry for this pair". It is **not** a claim of biological incompatibility. In the game, a pair that is not approved cannot hybridize.
- A pair is stored once, lower species ID first.
- Hybrid pairs are never invented. None exist yet.

## 8. Environmental data: design first, import second

Real environmental fit will matter (AMO-D013, AMO-D037), but the environment model is not designed yet (AMO-Q005). No fields for range, countries, latitude, altitude, climate, rainfall, humidity, temperature, dormancy, soil, drainage, pollinators, flowering, odour or growth size are defined. When the environment model exists, the input format is extended with exactly the subset it needs.

## 9. Third-party content and dependency principle

This is an engineering principle, not legal advice (AMO-D025):

- Amorpho minimises reliance on copied third-party botanical content. The approved export is Amorpho's own minimal, curated factual representation.
- Amorpho does not copy or depend on third-party prose, website text, photographs, illustrations, external tables, database dumps or protected editorial descriptions.
- No external botanical website or research service needs to remain operational for Amorpho to work.
- The external research process may consult whatever legitimate sources are appropriate. Source-specific licensing logic does not belong in Amorpho.

## 10. History

At foundation, the gate was first specified as a JSON "reality update package" format with evidence references, approval workflow and change operations (AMO-D023). Before anything was committed, it was superseded by the simpler file-based design above (AMO-D026). The evidence and approval concerns it encoded belong to the external research process.

## 11. Not built yet

- a validation tool (optional; AMO-Q038);
- the internal representation ([`data/canon/README.md`](../data/canon/README.md));
- the game's handling of species leaving the approved list, merges, splits and infraspecific taxa (AMO-Q016);
- how newly approved species appear in a live world (AMO-Q033).
