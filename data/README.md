# data/

Amorpho's own data. Everything here is language-neutral (CSV and Markdown) and owned by Amorpho alone.

## Layout

```
data/
├── input/     Approved reality input: accepted approved export files (CSV)
└── canon/     Internal representation derived from input (not defined yet)
```

## Data layers

Amorpho separates data into three conceptual layers (AMO-D021; see [`docs/08_CONCEPTUAL_ARCHITECTURE.md`](../docs/08_CONCEPTUAL_ARCHITECTURE.md#2-data-layers)):

| Layer | Location | Status |
|---|---|---|
| 1. Approved Reality Input | [`input/`](input/README.md), later derived into [`canon/`](canon/README.md) | species file is header only; no hybrid pairs |
| 2. Game Design Data (combat, abilities, balancing, transformation, progression) | not created yet | nothing to store yet |
| 3. Persistent World State (individual plants, ownership, lineages, trades, history) | not created yet | nothing to store yet |

Directories for design data and world state are created when there is real content for them, not before.

## Rules for everything in this directory

1. **No fabricated facts.** No invented species, no invented hybrid pairs, no unverified biological data, and no placeholder data that looks real.
2. **Reality enters only as approved input.** Real-world facts arrive as approved export files through the Reality Gate. Amorpho does not research them (AMO-D024).
3. **Only what the game needs.** No mirrored master data, third-party text, images or tables (AMO-D025).
4. **No external coupling.** No fields, files or scripts that name, query or depend on an external system.
5. **Stable identities.** Species IDs (`AMO-SP-000001` form) are permanent and never reused; scientific names are mutable metadata (AMO-D022).
