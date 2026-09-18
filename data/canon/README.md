# data/canon/ — Internal representation (not defined yet)

In Amorpho, **canon** means the *internal representation* of approved reality input: whatever form the eventual game implementation derives from the accepted files in [`../input/`](../input/README.md). It is Layer 1 (AMO-D021) in derived form. It never means the external master list, and it never includes game design data or world state.

## Current state

**Empty, by design.** The internal representation has not been decided. No database, SQL, SQLite, JSON runtime files, binary assets or engine-specific resources have been chosen (AMO-D020, AMO-D026). Where the representation will live is decided together with the implementation. This README exists to keep the distinction visible until then.

Until an implementation exists, the accepted files in `data/input/` are the complete statement of approved reality in Amorpho.

## Rules for the future representation

- It is derived from `data/input/` only. It is never edited by hand to add or correct facts.
- It contains nothing that the accepted input does not contain.
- Species are keyed by their permanent `AMO-SP-` IDs, never by scientific name (AMO-D022).
- Once built, it needs no access to any external system (AMO-D018).
