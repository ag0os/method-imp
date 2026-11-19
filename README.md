# The method's Contract

The implementation-agnostic statement of the software method this flock runs: Impatient Programming (IMP, Obie Fernandez) as we adopt and bend it. Public since 2026-11-19; the pilots it learned from are named by kind, not by repo.

Three texts, one owner (the method's keeper):

- `method-contract.md`: the Contract. What any implementation of the method must do, never how. It names no implementation, repo, tool or workspace. It is the floor: an implementation may add to an obligation, never contradict or weaken one.
- `method-contract-evidence.md`: the evidence record. Per obligation, what the pilots showed, by date and subject. How a rule learns.
- `method-contract-adoption.md`: the adoption record. Precedence, where the Contract lives, each implementation's proof list and accepted gaps, each repo's dated exceptions, grants.

How an implementation takes it: by a tag. A module, a skill, a CI job or a person by hand cites the tag it implements and keeps a proof list against it. A deviation is a diff against that tag, visible here, never silent.

How it changes: by the Contract's own LN-4. A change starts from the ledger (kept in the keeper's workspace), is decided by the user, lands here as a presented change, and reaches every implementation as a dated update to its proof list. `fix:` only for a defect in a text an implementation already took; everything else `refine:`.

Checks: `bin/check` (ids unique and never reused; every active obligation has a statement, a reason, a source and a proof; the Contract names no implementation; no em or en dashes; the word count line is true). CI runs the same command.
