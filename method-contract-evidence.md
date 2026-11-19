# The method's Contract: evidence record

Kept by the method's keeper, this workspace. Never inside the Contract (`method-contract.md`, its "No names" rule).

**What this is.** Per obligation of the Contract, the ledger lines and the pilot work that support it or strain it. A rule learns from the pilots this way: the ledger (`imp-ledger.md`) records what each change gave and cost, by date and subject, verified or relayed; this file maps those lines to the obligation they bear on; LN-4 turns a cost that keeps showing up into a proposal, decided by the user, and the Contract changes first. A line marked *support* is the best ledger evidence that the obligation earns its place. A line marked *strain* is a cost the ledger holds against the obligation as written: a case it has no answer for, a pilot that could not meet it, or a proof that did not catch what the obligation exists to catch. "None yet" means no pilot line bears on it; the obligation stands on its source alone.

Every entry's first line is the Evidence line revision 3 carried, verbatim (the ledger date and subject, the pull request where there is one). Where revision 3 had none, the entry says so. Citations are by the ledger's date and subject; the rules snapshot the Contract's "Rule n" marks refer to is `work/in-progress/method-contract/imp-rules-2026-11-04.md`. Retired ids (AG-4, CN-2, BD-1, BD-2, CK-5, RV-1, RV-3, MG-3, RC-3, LN-2, LN-3) carry no evidence of their own; their lines went with the obligation that absorbed them.

Written 2026-11-05 for revision 4, from the ledger as of 2026-11-05 evening.

## 1. Human understanding and the agreement (AG)

### AG-1 The agreement comes first, and it is the user's
- Revision 3: ledger 2026-10-14 copy-refresh (decisions arriving mid-build cost five rounds).
- Support: 2026-10-14, the site pilot PR #24 copy-refresh (five rounds and four rebases as decisions arrived over 4 h; the landed wording reversed by #25 three hours after merge).
- Support: 2026-10-15, the app pilot PR #59 agency-admin-access (one process rework: the Contract rewrite incomplete across spec and plan, found by the scope review).

### AG-2 The user chooses where their understanding goes
- Revision 3: no Evidence line (the only obligation besides AG-5 without one).
- None yet from a pilot. The ruling's line: 2026-11-04, the take-home pilot, final outcome (the user's principle: choose your level of abstraction at will; deep understanding costs mental energy and is not always needed; "No rule from this", then rule 7 adopted as AG-2's source on 2026-11-05).

### AG-3 The One Question, answered from evidence; spikes when unclear
- Revision 3: ledger 2026-10-16 the app pilot #62 (the user chose between two shapes before any build).
- Support: 2026-10-15, the site pilot PR #26 launch-prep (three pre-existing defects found in the One Question pass, among them a public default admin password the seed printed).
- Support: 2026-10-17, the app pilot PR #67 ac015-budget (the One Question before the budget showed the cost was the counts, not the view, so the fix was a cheaper count, not a design rollback).
- Support: 2026-10-29, imp-feature skill, first run outside this workspace (step 2 found the fill score is two signals collapsed under a max, which changed the choices put to the user).

### AG-5 Design talked through until both understand
- Revision 3: no ledger line yet.
- None yet. Nearest: 2026-10-29, imp-feature skill, first run (parked at step 3 on three decisions of the user's, the design not yet worked through); 2026-11-04, the take-home pilot, final outcome (the mechanism the user could not explain had been built by an agent with no design talked through; the user withdrew the interview as out of scope the same day).

### AG-6 Inside the agreement, agents decide and propose
- Revision 3: ledger 2026-10-09 pilot 1 (44 agent minutes, about 9 h of wall clock in handoffs and his turns).
- Support: 2026-10-14, the site pilot PR #23 consulting-page (about 17 h from final ready to the user's push turn; turns, not agents, are the cost).
- Support: 2026-10-16, the app pilot PR #65 api-signup-close (a hole found while building #64 went through as its own small PR the same day).

### AG-7 On M and L work, the builder says back what it understood
- Revision 3: ledger 2026-10-17 the app pilot #70 (13 design points settled before code).
- Support: 2026-10-20, the site pilot PR #39 locale-urls (the backbrief caught a wrong design claim before code).
- Support: 2026-11-05, the app pilot PR #78 mutation-package (2) (the backbrief caught the clean-tree conflict between re-anchor and acceptance before code).
- Support: 2026-10-15, shift review left (on 37 re-briefed items, misread 0 primary, Contract gaps 18; the method's answer is the backbrief for M and L).
- Strain, relayed 2026-11-07 (cosmonauts factory-poc trial 2, 2026-10-21): a backbrief costs the coordinator turns, and a decision rule that counts turns penalizes the method's own alignment step; the method's measure is the user's wait (RC-1), not agent turns.

### AG-8 The result is presented so the user can judge it without reading code
- Revision 3: ledger 2026-10-14 the site pilot #23 (judged from summaries and the dev server, without code).
- Support: 2026-11-02, the app pilot PR #75 ruby-409 (approved from the plan and the summary; code read no).
- Support: 2026-10-18, the site pilot repo layer, final (#34 approved from the PR body).

## 2. The Contract (CN)

### CN-1 Each repo keeps its Contract as obligations with reasons
- Revision 3: ledger 2026-10-09 pilot 1 ("MR-n says X, code does Y").
- Support: 2026-10-15, the app pilot PR #60 contracts-convention (one file per component turned the first collision between two parallel lanes into an agreed order).
- Support: 2026-10-17, the Jev experiment (the membership question kept 98 of 102 human-accepted obligations and caught 7 of 9 implementation sentences at 0.5).
- Strain: 2026-10-09, pilot 1 (the membership test is judgment: CSS class names kept as Contract); 2026-10-17, the Jev experiment (asked of the sentence alone it caught 1 of 9; the membership test does not fit configuration components such as CI).
- Strain: 2026-10-19, the app pilot PR #74 honeybadger-rake-eager-load (the new Contract file lacks the standard's front matter).

### CN-3 Pin what the code does, and learn why each fence stands
- Revision 3: ledger 2026-10-09 pilot 1 (pinning found a bug already on main).
- Support: 2026-10-20, the site pilot PR #36 spanish-pr36 (a review of a PR the cycle did not build made its new tests fail when they should, before the production migration ran).

### CN-4 The Contract changes in the same change as the behavior, and each addition traces to the agreement
- Revision 5 (red first for a new feature obligation), 2026-11-19: the user's ruling, as a bend of rule 20 he chose for the discipline's own value. The record neither proves nor refutes it: eight pilot changes ran red first (ledger 2026-10-09 to 2026-10-20) with gains recorded (an existing 500 surfaced by a red case; a test that could pass vacuously avoided) and no cost isolated; no record shows a feature defect that red first would have caught and a conforming mutation gate plus an independent exhale read would not; later reviews still found weak tests after red-first runs, so a red run certifies the test once, not for good (critic of 2026-11-18, kept by the keeper).
- Revision 3: ledger 2026-10-09 pilot 1 cost (about ten places wrong or silent, completed by review); no pilot has yet shown this failure caught or missed (ledger 2026-11-05, watch).
- Support: 2026-10-09, pilot 1 (two false obligations caught by review, corrected).
- Strain: 2026-11-05, the method's Contract (draft, revision 3): nothing in the module, the skill or the contract tool compares a Contract's additions with the agreed id list, and the exhale read is the builder's own, so the failure rule 20 names has no catch today; no pilot has shown it caught or missed. Watch: does the second reader find anything; if not in the pilots, the check alone is the lighter form.
- Strain: 2026-10-13, pilot 2 (Contract docs conflict when two branches touch one obligation).
- Relayed 2026-11-07 (cosmonauts factory-poc trial 2, 2026-10-21): both round-2 reviewers flagged that a fix brief writing a new Contract sentence changes the plan the user agreed outside the agreement step. The obligation's answer: a sentence the build or a fix finds enters marked as discovered with its reason (CN-4), and a change to an established obligation is the user's to accept (CN-6); the concern is met by the marks, not by a new rule.

### CN-5 A production bug enters the Contract first
- Revision 3: ledger 2026-10-17 the site pilot #32 (a session with no coordinator followed it on a live bug).
- Support: 2026-10-09, pilot 1 (rule 28 worked as written on the build blocker: Contract first, red, then the fix).
- Support: 2026-10-19, the app pilot PR #74 honeybadger-rake-eager-load (a live production defect through rule 28: obligation first, red in three fresh-process proofs, then the fix).
- Support: 2026-10-20, the site pilot PR #38 client-ip-fix (rule 28 reproduced a live 500 red through the real stack before the fix).
- Support for the bend: 2026-10-18, rule 28's order against the tools (the convention's "prove the test kills the matching mutant, then fix" cannot run; mutation tools abort on a red suite).
- Strain: 2026-10-19, the app pilot PR #74 (the source is a `.rake` file outside mutation's scope, so three hand mutations stood in: a scope gap for every Rails repo with logic in tasks).

### CN-6 Changing an established obligation is the user's to accept
- Revision 3: ledger 2026-10-16 the app pilot #61 (four dated rewordings, ids kept).
- Support: 2026-10-16, the app pilot PR #64 agency-team-access (AC-002 reworded in place with a dated line); 2026-10-20, the site pilot PR #37 copy-admin (seven obligations reworded and flagged); 2026-10-20, the site pilot PR #39 locale-urls (13 dated rewordings).
- Strain: 2026-10-20, the site pilot PR #39 (the merged D-34 and D-35 credited the owner with rulings the records showed as the Shepherd's; amended the same evening when the user confirmed them as the user's own).

### CN-7 The Contract is met or not, and coverage is published, never invented
- Revision 3: ledger 2026-10-20, the contract tool's first runs.
- Support: 2026-10-20, the contract tool's first runs over the pilots' real files (coverage counted from the files' own marks for the first time; the migration gaps named by a tool rather than remembered).
- Strain: 2026-10-20, the contract tool's first runs (a ruling made from the convention's text alone would have failed the one canonical Contract file; the review caught it before the tool shipped).

### CN-8 The repo carries the method without a coordinator
- Revision 3: ledger 2026-10-18 the app pilot #72 (passed; the checks step held only once placed inside the bug steps).
- Support: 2026-10-17, the site pilot #32 and the no-Shepherd bug test (a plain session with no Shepherd prompt followed AGENTS.md on a live 500 in about 3 minutes).
- Strain: 2026-10-18, the app pilot PR #72 ("before you say done, run bin/ci" did not hold for a Sonnet session when it sat outside the bug steps; one sample each, model or placement not separated); 2026-10-17, the site pilot #32 (the stranger session added the attribution footer the repo forbids, since AGENTS.md did not carry that rule).

## 3. Build and fold (BD)

### BD-3 A test leaves only on mutation evidence
- Revision 3: ledger 2026-10-09 pilot 1 cost (six tests deleted with no mutants measured; restored).
- Support: 2026-10-09, pilot 1 mutation and run 4 (every old kill was also a Contract kill; the old tests retired on evidence, totals verified).

### BD-4 Integrate continuously
- Revision 3: ledger 2026-10-20 the site pilot #37 (checks after a rebase caught a conflict that stacking hid).
- Support: 2026-10-14, the site pilot PR #24 copy-refresh (four rebases as decisions arrived; the nav test race found by the system run the builder's sandbox skipped).
- Strain: 2026-11-02, the app pilot PR #75 ruby-409 (plan ready 10-30 evening to approval 11-02, a weekend: a branch that waits on the user is the obligation's own exception, and the wait is RC-1's fact, not BD-4's failure).

## 4. Checks (CK)

### CK-1 One definition of done, for every agent and for CI
- Revision 3: ledger 2026-10-13 prerequisites (the method's checks lived outside CI).
- Support: 2026-10-17, the site pilot PR #28 ci-gate (an adversarial reviewer found real holes three rounds running; local runs hid a fresh-runner bundle failure only GitHub caught).
- Support: 2026-11-04, the desktop pilot, step 1 (one checks command where there was none and a type check CI never ran).

### CK-2 A check that could not run is a named gap, and code does not move for a tool
- Revision 3: ledger 2026-10-13 Phase 1 AC4 (a clean exit with no guardrail behind it).
- Support: 2026-10-15, the app pilot PR #59 (mutation unavailable at build time named; a hand revert of 8 lines stood in and caught 2 tests passing for the wrong reason).
- Strain: 2026-10-21, the site pilot PR #40, the hooks' first run (floors and exhale logged COULD-NOT-RUN inside the session and did not block; the Stop gate checked only tests and lint on changed files).
- Strain: 2026-10-18, the site pilot repo layer, final (selection completeness left open: code moved behind a delegate into an unlisted class is not mutated).

### CK-3 Tests must bite: mutation against the merge base
- Revision 5 (a check shown to fail; a stand-in grounded in the real thing), 2026-11-19: the user's ruling, from three records. Pilot 1, 2026-11-12: a named proof that could not fail (an always-green recorder), and a weekly run that crashed on main because its end-to-end test used a faked command line tool that printed an empty list where the real one prints nothing (escaped 2026-11-09, fixed 2026-11-13, proved by the scheduled run of 2026-11-16). The factory pilot, 2026-11-17 and 2026-11-18: a request the real backend refuses and a silent login, green against stubs that accepted anything, and a blind restart counted as success, each found only by a reviewer breaking the code on purpose. Three mechanisms, not one: a check that cannot go red, a stand-in more lenient than the real thing, a wrong success criterion (critic of 2026-11-18).
- Revision 3: ledger 2026-10-09 pilot 1 mutation (33 survivors named 7 missing sentences).
- Support: 2026-10-09, pilot 1 run 4 (after the 7 gap sentences the Contract killed every non-equivalent mutant); 2026-10-18, the site pilot repo layer, final (the merge-base mutation gate closes the old floor's credit window and fails closed on a subject leaving mutation).
- Support: 2026-11-05, the app pilot PR #78 mutation-package (2) (the weekly full run exists: 6,131 mutants, score 72.4%; a committed accepted list of 1,664 entries).
- Strain: 2026-11-04, the budget rule's first contact with CI (the 48 s local full run was a 14-job run; the CI gate step takes 10m20s at 4 jobs, over the proposed ten-minute budget before any change; a budget is measured on CI at the job count CI uses, never locally).
- Strain: 2026-11-04, the desktop pilot, step 1 (Stryker has no merge-base survivor comparison, so without a script diffing survivors at base and tip the mutation gate is a habit on a Stryker repo; a runtime-error mutant is left out of its score).
- Strain: 2026-11-05, the app pilot PR #78 (the tooling's own 34 survivors and 31 uncovered mutants entered the accepted list untriaged under the agreement instead of being routed before merge; the project's value for this change, where the method's rule would route them).
- Strain: 2026-10-09 and 2026-10-16, the `.ordered` survivor (same mutant shape, opposite verdicts, equivalent on task 1 and a gap on consulting-page: equivalence can depend on the environment).
- Strain: 2026-10-18, the app pilot PR #72 (mutation as a threshold of 80 on changed files, a deliberate difference from the checks table with its reason in the PR; the adoption record carries it as a dated interim exception).
- Relayed 2026-11-11 (the user's direction on the app pilot's survivors, via the master): an equivalence is a run proof checked by a second reviewer from the other model family before it reaches the user, and a narrow survivor class may be ruled once by the user. Weighed: additions over "equivalent, with its reason", allowed by the floor; a class ruling supplies the reason per entry when each entry names the class; the app pilot's values until a second repo needs them, watched.

### CK-4 Breathe out: health judged against the merge base, in the same change
- Revision 3: ledger 2026-10-17 the app pilot health floors (two false results under the changed-scope wording).
- Support: 2026-10-17, the app pilot PR #70 health-floors (a reviewer's proof produced the merge-base rule; review found two CI-only breaks no local gate could show).
- Ruled 2026-11-06 (the method's, into CK-2: a required check red on a cause the change did not add is a named gap, presented, merged on the user's word, never under a grant). Was strain: 2026-11-05, the app pilot PR #78 (same note): a required scan went red on an outside event, Rails advisories published that day against a version present on main and production, unrelated to the PR; the same case stands on the site pilot (main red on new advisories). The rule has no standing answer for a required check that fails on a cause the change did not add and the merge base would show if rerun; the checks table's tip-against-merge-base reads at the base's old run. A decision for the user: the method's or each repo's.
- Strain: 2026-10-17, the app pilot PR #69 carlos-doc-answers (a docs-only PR waited about 11.5 h on the user's turns and on an unrelated red gate).

## 5. Review (RV)

### RV-2 Review depth follows blast radius
- Revision 3: ledger 2026-10-21 the site pilot #40 (a cross-family review found three gaps a green gate hid).
- Support: 2026-11-05, the app pilot PR #78 (the cross-family review found six real holes the builder's checks passed, two of which would have cost a 45 min rerun or emptied the list); 2026-10-20, the site pilot PR #37 (the cross-family review found a silent change to existing data); 2026-10-19, Troupe PR 17 (two blind reviews plus a refuting synthesis).
- Strain: 2026-10-17, the app pilot PR #70 (one reviewer per round, no cross-family review, Codex rationed: a named gap on an L, foundational change); 2026-10-18, the site pilot repo layer, final (Opus reviewers stood in for cross-family; the last fix read without a fourth review).

## 6. Merge and grants (MG)

### MG-1 Every agent change reaches the codebase through a presented change
- Revision 3: ledger 2026-10-15 the app pilot baseline (232 of 234 commits went straight to main, which deploys).
- Support: every the app pilot PR line from 2026-10-15 on (#59 onward, each merged from a presented change).
- Strain: 2026-10-20, the site pilot PR #36 spanish-pr36 (built outside the cycle by the user's cloud session and merged on the user's word: the pairing path, with the merged commit carrying an agent as author, which nobody flagged).

### MG-2 Merge on the user's word or under a grant they wrote
- Revision 3: ledger 2026-10-17 the site pilot #32 (the first merge under G1, no turn of his).
- Support: 2026-10-18, the site pilot repo layer, final (#34 was outside G1 for touching the gate's own files and merged on the user's approval; G1 merged a production fix with no turn of the user's); 2026-10-20, the site pilot PR #39 (outside G1 because of an owned `config/mutant.yml` line).
- Strain: 2026-11-05, the app pilot PR #78 (same note): the wait from ready to the user's turn was about 26 h 27 m, almost all on the merge decision after a required check went red on an outside event the change did not add; the user merged on it ahead of the fix. Under MG-2 as written such a check is "a check that could not run", outside every grant, so no grant could have merged it; whether that is the method's answer or each repo's is the same open decision as under CK-4.
- Strain: 2026-10-17, the app pilot PR #71 css-parser-33 (a lockfile-only advisory fix waited 6.5 h on the user's turn, the case a grant would remove once floors and a rollback path exist).

### MG-4 A grant is asserted at each merge, and its state is kept true
- Revision 3: ledger 2026-11-04 (G1's record said in force after it lapsed; the repo had honored the lapse).
- Support: 2026-11-04, the mutation budget rule (G1 found lapsed by date since 10-31 while the record said in force; the site pilot's #44 and #45 were presented with "merge grant G1 ended 2026-10-31" in the body).
- Strain: the same line: the keeper's record was stale four days; the obligation's proof ("the grants record agrees ... on any day it is read") failed on the keeper, not on the repo.

### MG-5 Honest labels
- Revision 3: ledger 2026-10-15 pilot 2 closed (`fix:` on a defect that never reached the live URL).
- Support: 2026-10-17, the site pilot #32 (the stranger session titled the PR `fix:` and named the obligation); 2026-10-17, the Jev experiment (shape 6 of 7 from one line of context).
- Strain: 2026-11-02, the app pilot PR #75 ruby-409 (titled `fix:` with no production defect behind it, advisories and a version bump; either advisories count as defects for the label or it should have been `refine:`; the app pilot's call, the method's if it recurs). The Standing default of 2026-11-05: labels for advisories follow rule 9 until the case recurs.

## 7. The record (RC)

### RC-1 Four facts per change
- Revision 3: ledger 2026-10-16 the site pilot notes (minutes cannot be known after the fact).
- Support: 2026-10-17, the site pilot PR #28 ci-gate (the first note on the four facts); 2026-11-02, the app pilot PR #75 (current template, four facts in section 9); 2026-11-05, the app pilot PR #78 (code read no; three reserved decisions; the wait timed).
- Strain: 2026-10-16, the app pilot PR #64 and 2026-10-17, the app pilot #68 and #71 (waits "of minutes, not timestamped"; code read "inferred there"); 2026-10-20, the site pilot PR #39 (two of the user's rulings were approved in chat and never journaled, found the same evening).

### RC-2 The record is true now, and its evidence is kept
- Revision 3: ledger 2026-10-16 the site pilot notes (raw logs only in temporary space; two notes still "not landed" after merge).
- Support: 2026-10-20, Troupe PR 19 (two record rules in the check named ten record gaps on their first run over the two pilots); 2026-11-02, the app pilot PR #75 (five raw logs beside the note; review caught an honest-record error: a floor file's reference edited without a re-run).
- Strain: 2026-10-20, the site pilot PR #37 (the re-check's 17 of 18 is reported only, because its logs went to a cleanup glob); 2026-10-20, the site pilot PR #39 (D-34 and D-35 credited the owner with rulings the records showed as the Shepherd's); 2026-10-19, the app pilot PR #74 (the note written to the old form because the repo's pointer named a stale copy of the template).

## 8. Learning the method (LN)

### LN-1 Every report says what the method gave and what got in the way
- Revision 3: every line of the ledger.
- Support: every ledger line since 2026-10-09 carries a Gives and a Costs part.
- Strain: 2026-11-04, the method's Contract, design-notes section 2 (no report of the module's or the skill's asks for it: fails in both; the accepted gap is in the adoption record).

### LN-4 A change to the method starts from the record, is decided by the user, and reaches every implementation
- Revision 3: ledger 2026-10-19 Troupe PR 17 (a ruling had not reached the module's Checks row).
- Support: 2026-11-05, Troupe PR #27 mutation-budget (the budget rule agreed 11-04 reached the module's step 6 and its check guide the next day; 13 pinned tests moved).
- Support: 2026-11-05, the method's Contract agreed (the method now has a statement a second implementation can be checked against; `method.md` found drifted in six places and retired).
- Strain: 2026-10-19, Troupe PR 17 (the shapes' Checks row still carried pre-10-17 wording: a ruling made in one doc did not reach the module on its own); 2026-11-04, the mutation budget rule (the reversal of a dated ruling must reach the module, G2 and both pilots, where rulings have been lost before); 2026-10-29, imp-feature skill into Troupe (the references claim generation at install while the convention lives in this workspace).
- Strain: 2026-11-05, the method's Contract agreed (the change path gains one hop, Contract first then each implementation, accepted only with `method.md` retired); 2026-11-05, Troupe PR #27 (the module sits at exactly its 2,200-word budget, so the next rule must cut words).
