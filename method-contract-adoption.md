# The method's Contract: adoption record

Kept by the method's keeper, this workspace. Never inside the Contract (`method-contract.md`, its "No names" rule).

**What this is.** How each implementation and each repo stands against the Contract, and the transition by which the Contract comes to bind them. The Contract says what any implementation must do; this file says who implements it today (Troupe's software module, `packages/software/`; the imp-feature skill for a plain session; each repo's own layer in its agent instructions and CI), what each has accepted as a gap, which repo has an exception the user ruled, which grants exist, and where the Contract's text lives. Everything here changes when an implementation, a repo or a workspace changes; nothing in the Contract does.

Written 2026-11-05 for revision 4. Sources: `design-notes.md` sections 2 and 3, `docs/grants.md`, `docs/grant-G1.md`, `docs/method.md`, the ledger.

## 1. Precedence (the user's ruling of 2026-11-05, in full)

Agreed by the user 2026-11-05 ("I agree on the contract recommendations"), on the five parts proposed in `design-notes.md` section 3.

1. **The Contract wins, as a floor.** An implementation may add to an obligation but never contradict or weaken one. Examples of additions: the module's hooks; the skill's showcase line; G1's cross-family review for size M. Such additions are allowed, not conflicts. This is how software Contracts already work: an implementation may do more than its obligations ask, never less.
2. **A repo sets values, and departs only by a dated exception.** Paths, tools, thresholds, budgets and cadences are the repo's, recorded in its agent instructions and CI. A repo that departs from an obligation does so through an exception the user ruled. The exception is recorded in the repo with its date and reason, and the method's record points to it (section 4 below). The app pilot #72 is the model: it set mutation as a threshold of 80 on changed files for now, a deliberate difference with its reason in the PR. Under the ruling that is an exception, not a violation.
3. **A transition, not a cutover.** Each implementation keeps a proof list: obligation id, where the implementation meets it, or the named gap. On the day the user agreed, each list started with that implementation's gaps from `design-notes.md` section 2, recorded as accepted gaps (section 3 below). The Contract binds an implementation obligation by obligation as each gap closes, or entirely from a date the user sets. Until then, the pilots run as they do today.
4. **The Contract lives where implementations can cite and test against it.** A Contract kept only in this private workspace cannot be pinned by Troupe's tests or shipped with the skill. The user chose option (a) of the two put to them: this workspace stays the source, as ruled on 2026-10-13 ("home of the IMP module ... owns the method"); a copy generated into Troupe at release is pinned by Troupe's tests and fails them when it drifts. Option (b), Troupe as the Contract's home with this workspace keeping the ledger, the eval and the why, was not chosen. See section 2 for the state of this part.
5. **The change path gets one hop longer, so the number of texts must not grow.** Under LN-4 a ruling changes the Contract first and then each implementation. The ledger shows rulings lost across hops (2026-10-19, 2026-11-04). This is acceptable only because `method.md` stopped being a fourth text to keep true (section 6).

**What changed with the agreement.** A ruling lands in the Contract first, then reaches each implementation as a dated update to its proof list. Forge's evals for the module gain a source: each obligation becomes a case. A third implementation has something to be built from and judged against. Three texts change: `method.md`'s "the module wins" sentence (retired to a pointer, done 2026-11-05); the skill's precedence line ("where AGENTS.md or the module says more, they win"), which now conflicts with part 1 and waits on the forge brief; the module's header, which moves Troupe's pinned tests. Section 3's gaps are forge's work list, as accepted gaps first. The forge brief is drafted (`forge-brief-draft.md`) and waits on the user's yes to send.

## 2. Where the Contract lives

**Ruled 2026-11-06, public since 2026-11-19.** The Contract lives in this repo, `ag0os/method-imp`, private until the user ruled it public on 2026-11-19 ("make it public", "cleaned first": the pilots named by kind, a fresh history; the earlier history is kept privately), the user's account, created on his word. Tag `v1.0` is the agreed text of 2026-11-05 with its marks dated 2026-11-06. An implementation takes the method by tag: it names the tag it implements and keeps a proof list against it (section 3); a deviation is a diff against that tag, never silent. No copy of the Contract exists anywhere: the keeper's workspace holds a pointer, and Troupe pins a tag instead of carrying a generated copy, which retires the 2026-11-05 morning ruling (a generated copy in Troupe checked for drift, as the one named exception to "no copies") before it was ever built. The skill's references are proved against the pinned tag the same way.

Tags are `v<major>.<minor>`: minor for additions and clarifications, major when what an implementation must do changes. Repos of the declared layer are named `<kind>-<name>` (`method-imp`, later `method-<other>`, `agent-<name>`, `workflow-<name>`, `tool-<name>`; the framework that executes them stays `troupe`).

The keeper's workspace keeps the ledger, the eval and the briefs; this repo keeps the Contract and the two records.

**History.** 2026-11-05 morning: the workspace the source, a generated copy in Troupe (superseded above). 2026-11-05 evening: marked provisional while the user weighed a repo. 2026-11-06: the repo.

## 3. The transition: proof lists and accepted gaps

Each implementation keeps a proof list: obligation id, where it meets it, or the named gap. The lists start with the accepted gaps of 2026-11-05, read by the designer from Troupe's `packages/software/` (MODULE.md and the four guides) and the skill (SKILL.md and its two references) against revision 2 on 2026-11-04, with revision 3's CN-4 row added 2026-11-05 (`design-notes.md` section 2). "Silent" means the text does not require it; an implementation that is silent may still meet it in practice, but nothing makes it. "Unknown" means the designer could not read the file that would settle it. Everything not in the table meets in both, or binds the repo or the keeper rather than an implementation (CN-1, CN-8, CK-1, LN-4).

| Obligation | Troupe module | imp-feature skill |
|---|---|---|
| AG-2 | partial: asks where the user takes part, not whether they want the obligations first | partial: asks the reserved decisions only |
| AG-5 | partial: an editable document for reserved scope or shape, with no "until both understand" | partial: same |
| AG-7 | meets | partial: no reader for the backbrief when the session builds alone |
| CN-1 (membership test) | silent | partial: only in a reference read when the repo has no convention |
| CN-4 (review findings) | meets | partial: adds a missing obligation, not a wrong one |
| CN-4 (trace to the agreement, revision 3) | partial: agreed ids listed, no check of the diff against them; the exhale read is the builder's | partial: same; step 5 is the session's own read |
| CN-5 | meets | out of scope (features only; the repo's agent instructions carry bugs) |
| CN-6 | meets | silent |
| CN-7 (system share) | meets | partial: proof counts only |
| BD-4 | meets | partial: no age limit |
| CK-2 (code does not move for a tool) | partial | partial |
| CK-3 | partial: no completeness check for added code (closed by Troupe PR #27, 2026-11-05, if the proof list confirms it) | partial: defers wholly to the repo |
| CK-4 (binds every implementation and the repo) | meets by the 2026-11-04 read (step 6, health against the repo's floors); the proof list should confirm, since that read listed CK-4 among the repo-bound | meets by the same read (runs the repo's checks as its gate does); same confirmation owed |
| RV-2 | meets | partial: no second review after a fix round |
| MG-2 (the grant's own gate) | partial: silent on it | partial: silent on it |
| MG-4 | partial: no lapse record required | partial: confirmed each run, nothing recorded |
| RC-1 | unknown (`eval-change.md` unread) | fails |
| RC-2 | unknown | fails |
| LN-1 | fails | fails |

Totals against revision 3 (the user's accepted gaps, 2026-11-05): 4 fail, 20 partial, 2 silent, 2 unknown, 1 out of scope, across the module and the skill. (Against revision 2 the partials were 18; revision 3's CN-4 trace row added one to each column.)

**Where the accepted gaps come from, and what closes them.** Fails and partials in RC-1, RC-2 and LN-1 close when the module's and the skill's reports carry the four facts, the raw evidence and the "gave and got in the way" line. AG-2 and AG-5 close when each asks whether the user wants the obligations first and works a reserved design through "until both understand". MG-2's and MG-4's partials close when each names the grant's own gate as excluded and records lapses. CN-4's trace row closes when the contract tool's diff reads the agreement's id list and the exhale read is staffed by someone who did not build (the forge brief's item). The module's two unknowns close when `eval-change.md` is read against RC-1 and RC-2. The skill's CN-5 is out of scope by design and stays so unless the user widens the skill.

**Revision 5, 2026-11-19.** Two additions open a gap in every implementation and every repo from the day they land: CN-4's failing test first for a new feature obligation (neither the module nor the skill asks for it; some pilot changes did it unasked) and CK-3's record that a check accepts a conforming case and rejects a named violation, with a stand-in grounded in the real thing (no implementation asks for it). Each proof list gains both rows as gaps until its text carries them.

**Binding dates.** None set. The Contract binds each implementation obligation by obligation as its gap closes, recorded in its proof list with the date; the user may instead set a date from which it binds entirely.

## 4. Repo exceptions (dated, with their reason)

An exception is a repo's departure from an obligation that the user ruled, recorded in the repo with date and reason and pointed to from here.

- **The app pilot, mutation threshold, interim.** the app pilot PR #72 (merged 2026-10-18, the user's reserved decision in that PR): mutation as a threshold of 80 on changed files for now, with the merge-base comparison later, a deliberate difference from the checks table (CK-3's zero new survivors against the merge base), 4 shards, `lib/` in scope. PR #77 named it an interim. The budget rule of 2026-11-04 and the weekly full run of PR #78 (2026-11-05: 6,131 mutants, an accepted list of 1,664 entries) are the app pilot's path out of it; the exception stands until the merge-base comparison lands and this line is dated closed.
- **The app pilot, the agreement's routing of survivors (PR #78, 2026-11-05; ruled the repo's own 2026-11-06, with a watch: a second change doing the same makes it the method's).** The tooling's own 34 survivors and 31 uncovered mutants entered the accepted list untriaged under the agreement instead of being routed before merge: the project's value for this one change, where CK-3 would route them. Recorded in the ledger; not a standing exception.
- **Ruled the method's, 2026-11-06, not an exception: a required check red on an outside cause (the app pilot #78 and the site pilot, 2026-11-05).** Now CK-2's sentence; the two pilots' cases below were its evidence. Each implementation's proof list gains CK-2 (outside cause) as a gap until its text carries it. Was: Both pilots have had a required scan go red on advisories published that day against a version already on main and production, unrelated to the change. CK-4 and MG-2 have no standing answer; the user merged on it ahead of the fix. Whether the answer is the method's (a rule in CK-4 or MG-2) or each repo's (an exception here) is the user's decision; until then each such merge is on the user's word.

- **The factory pilot, a stop that is neither a reserved decision nor an outside act (AG-6), 2026-11-18.** The user, 2026-11-18: "yes to manual reconciliation". The factory's first version stops for a person where recovery after an interrupted step cannot be proved, inside the branch included; AG-6 allows a stop for the user only on a reserved decision or an outside act. Recorded in that repo's `docs/method-adoption.md`, section "Dated AG-6 exception" (repo the factory pilot, pull request 6, merged 2026-11-19 as ca96a17). It authorizes no blind replay and no uncertain outside effect. Whether the Contract gains this kind of stop is open with the user (LN-4); the factory's runs are its evidence.
- **The factory pilot, changes to what the grant's checks run or read merge under its grant (MG-2), first phase, 2026-11-18.** The user, 2026-11-18: "We are in the early stage of Cosmonauts 2 So, at the beginning everything will be changing fast So yeah, yes to both for this first phase and then we can revisit the permissions". An exception to MG-2 and to the Standing ruling of 2026-11-05 that every grant excludes changes to its own gate. Recorded in the same file, section "Dated MG-2 exception". To be revisited with the user at the latest before the factory's first real run on a target repository. The same answer names the large kinds inside that grant, which is within MG-2 and no exception.

- **The desktop pilot, mutation by hand, interim (the user, 2026-11-06).** Its mutation tool has no merge-base survivor comparison, so CK-3's gate is run by hand on changed files and named as a gap on each pull request, until a base-and-tip script is proposed with its first feature. Recorded in the keeper's ledger on 2026-11-06; entered here 2026-11-19, when a read of the four repos found this record saying no exception existed.

No exception is recorded for the site pilot.

## 5. Grants

What a grant must be is the Contract's MG-2 and MG-4. The grants themselves and their state are in `docs/grants.md`, one line per grant, the grant's text linked, lapses and withdrawals written with date and cause, nothing deleted.

- **G1, the site pilot** (`docs/grant-G1.md`). Decided by the user 2026-10-17; started 2026-10-17 with CI as the full gate, protection and auto-merge; covered S and M, `refine:` and `fix:`, excluding data, auth, deploy, the gate's own files, code-owner paths and L. Lapsed 2026-10-31 by its own date; no escaped defect recorded. Found lapsed on 2026-11-04 while `grants.md` said in force (the repo had honored the lapse: its #44 and #45 of 11-02 were presented with "merge grant G1 ended 2026-10-31" in the body). G2 is the user's to write, carrying the mutation changes agreed on 2026-11-04 (condition 1's "every subject" becomes the budget rule; a re-anchor PR of accepted-list entries merges under the grant). G1's text still carries "Granted by: the user, on <date he confirms this text>" unfilled.
- **The app pilot.** No grant. Its grant waits for CI green on main (first fully green 2026-10-17) and a known rollback path, since a merge there deploys and branch protection is refused on its plan.
- **The factory pilot.** A grant since 2026-11-17, confirmed for the method's changes 2026-11-18. The user, 2026-11-17: "you can also merge. For now the factory project is just for us so if we mess up we don;t affect no one else"; 2026-11-18: "I don't want to approve every PR actually. merge on green". Covers every pull request of the factory's own changes, the large kinds named 2026-11-18; green as that workspace's charter states it; lapses on a condition, reopened before the repo goes public or anything depends on it. Its gate exclusion is lifted for the first phase by the dated exception in section 4. On 2026-11-19 the user accepted in words the checks the repo lacks on its first day (a complete mutation gate, a complete health gate, a branch age check), which MG-2 requires a grant to accept before a merge under it (relayed by that repo's coordinator).
- **The desktop pilot.** No grant; the repo went onto the method on 2026-11-04 (step 1) and its first Contract file waits on the first feature.

What G1 contributed to the Contract: MG-2's gate exclusion ("a PR that weakens the check it is merged on must not merge on it"), generalized to every grant by the user on 2026-11-05; MG-4's assertion and lapse conditions. G1's cross-family review for size M is an addition under precedence part 1, and the one text that ties review depth to size rather than blast radius.

## 6. `method.md`, retired to a pointer (2026-11-05)

`docs/method.md`, written 2026-10-09 after pilot 1, had drifted in six places by 2026-11-04 (the critic's finding 33 and the designer's Discoveries: cycle step 3 against the 10-16 narrowing, changed scope against merge base, G1's state, the module's path, two different "three layers", rule 28's order). On the user's agreement of 2026-11-05 it was retired to a pointer of a few lines: what IMP is, where the Contract is, how it runs today, where the ledger is, why. Its glossary line moved into the Contract's Standing ("Words"). Its "the module wins" sentence is gone; the Contract outranks the module as a floor. The old text is kept at `work/in-progress/method-contract/method-md-retired-2026-11-05.md`. The pointer still names Troupe's `packages/software/` as how the method runs today and the Contract as outranking the module and the skill; those are this record's facts, right where they are.

## 7. The implementations, named

- **Troupe's software module** (`packages/software/`: MODULE.md, the guides, the tools including the contract tool, the hooks). Its hooks are an addition under precedence part 1 and under the Standing's rule 24 ruling: armed and harmless on their first real run (the site pilot #40, 2026-10-21), not yet a finder. Its mutation step 6 carries the budget rule since Troupe PR #27 (2026-11-05). The module sits at its 2,200-word budget.
- **The imp-feature skill** (one source in Troupe since PR #25, 2026-10-29, installed into the Claude Code and Codex skills directories). Features only; bugs and chores are the repo's agent instructions. Its precedence line defers to AGENTS.md and the module and must change under part 1. Its showcase line is an addition. Its references claim generation at install; under part 4 they are generated from, or proved against, the Contract.
- **Two tools share the method's words.** exhale, the duplication tool the pilots' Rails repos run, keeps its declared copies and thresholds in a directory named `contract/`; that directory is exhale's word, not the IMP Contract, and the tool is not rule 12's exhale. mutant, the Ruby mutation tool the site pilot runs, and Mutineer on the app pilot, produce mutants in rule 28's sense; the tool name is not the method's word. The Contract's Words line keeps the method's words; this line keeps the tools.
- **The checks table's mechanism for CK-4.** The Contract's CK-4 obliges the what: debt the change did not add is kept with a reason per entry and changes only with a reason. The how on the pilots is `docs/checks-table.md` rules 2 to 4: a committed baseline per tool as the weekly snapshot, guarded floor inputs, a weekly full run that re-anchors with a reason. An implementation that runs the checks on both trees needs no snapshot file; one that keeps a baseline is adding.
- **Each repo's layer**: the site pilot (on the method since pilot 1, 2026-10-09; the repo layer final 2026-10-18), the app pilot (pilot three, baseline 2026-10-15; repo layer 2026-10-18), the desktop pilot (step 1 agreed 2026-11-04), the factory pilot (adopted 2026-11-19 by its pull request 6; its own record is `docs/method-adoption.md` in that repo), with the convention (`docs/contract-convention.md`), the checks table (`docs/checks-table.md`) and the grants (`docs/grants.md`) as the repo-level values the keeper maintains for them.

## 8. Dated 2026-11-06
The user dated the five "ours" marks revision 4 had left without a ruling: CN-3 (rewritten, not deleted), AG-3 (evidence first, the base revision and safe environment, assumptions joining the reserved decisions, only reserved questions to the user), BD-4 (the repo's limit and the waiting exception; the week stays a default in the repo layer, not the Contract), RV-2 (two blind reviewers and a refuting synthesis), all 2026-11-06; MG-5 (a fix names the obligation) confirmed as 2026-10-16. A glossary line for reserved decisions and reserved questions was added to the Contract's Standing the same day.

## 9. Ruled 2026-11-06
The two findings from the app pilot #78: a required check red on an outside cause is the method's (CK-2 amended, a named gap, merged on the user's word, never under a grant; the module and the skill gain the gap in their proof lists); a change's own survivors entering the accepted list untriaged under its agreement is the app pilot's own value, watched.
