# Working in this repo

This repo holds the method's Contract and runs the method on itself, lightly.

- Checks command: `bin/check`. Run it before you say done; CI runs exactly it. A check that could not run is a gap to name, never a pass.
- Contract location: `method-contract.md` is both this repo's product and its Contract; its obligations are the ids `AG-n`, `CN-n`, `BD-n`, `CK-n`, `RV-n`, `MG-n`, `RC-n`, `LN-n`. Ids are never reused; a retired id keeps its heading.
- Labels: `fix:` only for a defect in a text an implementation already took by tag; everything else `refine:`.
- Merge rule: a change to `method-contract.md` is a pull request, presented, merged on the user's explicit word; no grant. The two records (`method-contract-evidence.md`, `method-contract-adoption.md`) are the keeper's bookkeeping of decisions already made: the keeper commits them directly to main, each commit carrying the ruling's date and the user's words, and `bin/check` runs on every push (the user, 2026-11-07).
- Design location: `docs/design/<branch>.md` when a change's shape is a decision the user reserved.
- Attribution: none required.
- Evidence and adoption records change with the Contract when a change touches what they describe; the ledger they cite lives in the keeper's workspace, not here.
