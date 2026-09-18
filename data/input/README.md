# data/input/ — Approved reality input

This directory holds **approved export files** supplied from outside the repository and accepted through the Reality Gate ([`docs/05_REALITY_GATE.md`](../../docs/05_REALITY_GATE.md)). These files are Layer 1, Approved Reality Input (AMO-D021).

Amorpho trusts the content of an approved export. It does not research, verify or adjudicate botanical facts, and it does not know or record where they came from (AMO-D024).

## Files

| File | Status |
|---|---|
| [`amorphophallus_species.csv`](amorphophallus_species.csv) | contract defined; **header only — contains no species** |
| `amorphophallus_hybrid_compatibility.csv` | contract documented below; **not created** — no approved pairs exist |

## Rules for every input file

- UTF-8 without byte-order mark, LF line endings, comma-separated.
- The first line is exactly the header given below. No extra columns, blank lines or comment lines.
- Values containing a comma or a double quote are quoted as in RFC 4180.
- Each accepted file is a **complete snapshot**. A new approved export replaces the previously accepted file; version control history is the record of accepted imports.
- Never hand-edit a file to add or correct a fact. Corrections arrive as a new approved export.
- Files contain no external database IDs, citations, URLs, source names or research provenance (AMO-D025).

## `amorphophallus_species.csv`

```csv
species_id,scientific_name
```

| Column | Meaning | Rules |
|---|---|---|
| `species_id` | Permanent, opaque Amorpho species ID (AMO-D022) | exactly `AMO-SP-` followed by six digits, e.g. `AMO-SP-000001`; `AMO-SP-000000` is not used; unique within the file |
| `scientific_name` | The currently approved scientific name, as supplied by the approved export | not empty; no leading or trailing whitespace; no author citation; unique within the file |

Rows are ordered by `species_id` ascending.

When a new approved export replaces the accepted file:

- Every `species_id` in the accepted file must still be present. A missing ID is **not** accepted automatically: how the game handles a species that leaves the approved list is open (AMO-Q016).
- The `scientific_name` of an existing ID may change. The ID stays the same.
- New IDs may appear. An ID is never reused for a different species.
- The approved export supplies both columns. Allocating new IDs, and keeping each ID attached to the same species when its name changes, is the job of the process that prepares the export. Amorpho cannot check this, because it does not know taxonomy.

Deliberately **not** included: authorship, external database IDs, source references, citations, research provenance, distribution, morphology, climate, combat data and visual data. A column is added only when a game system demonstrably needs it (AMO-D025).

### Name changes keep the identity

Illustration only: `exampleensis` is a fictional placeholder, and `AMO-SP-000042` has not been assigned.

```text
AMO-SP-000042,Amorphophallus exampleensis        ← first accepted export
AMO-SP-000042,<a different approved name>         ← later accepted export
```

The permanent identity stays `AMO-SP-000042`. Savegames, individual plants, genealogies, lineages, ownership, world history and combat history all refer to the ID and are unaffected. Scientific names are never used as permanent keys.

## `amorphophallus_hybrid_compatibility.csv` (documented, not created)

```csv
species_a_id,species_b_id
```

- One row per **approved compatible pair**. Compatibility is symmetric for gameplay (AMO-D027), so each pair appears once.
- `species_a_id` is lower than `species_b_id`. IDs are zero-padded, so text order and numeric order agree.
- Both IDs must exist in the accepted species file. A species is never paired with itself. No duplicate rows.
- Rows are ordered by `species_a_id`, then `species_b_id`.
- **Absence of a pair means "not currently approved as compatible". It does not mean "proven incompatible".** The game does not allow hybridization for a pair that is not approved.

The file will be created when the first approved pairs are supplied.

## Validation

No validation tool or programming language has been chosen (AMO-Q038). The rules above can be checked by hand or with any tool. An automated validator can be added once imports make manual checking a burden.
