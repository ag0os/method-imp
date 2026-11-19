# The method's Contract

Word count: 5,585.

Agreed by the user 2026-11-05 (the seven questions and the defaults put to them). Revision 4, 2026-11-05, on the user's ruling of the same day: "the method should stand on its own, shouldn't be bounded to any repo or implementation below it." This is the method, implementation agnostic: what any implementation must do, never how. LN-4 is how it changes. Revision 5, 2026-11-19, adds two things on the user's rulings of that day: a failing test first for each new feature obligation (CN-4) and the proof that a check can fail before it is relied on (CK-3).

## Standing (the user's dated rulings that shape the method)

- **Precedence, 2026-11-05.** The Contract outranks every implementation, as a floor: an implementation may add to an obligation, never contradict or weaken one. Additions (a hook that runs while the agent works, a showcase line, a grant's extra condition) are not conflicts.
- **Repos set values, and depart only by a dated exception, 2026-11-05.** Paths, tools, thresholds, budgets and cadences are the repo's, in its agent instructions and CI. A departure from an obligation is an exception the user ruled, recorded in the repo with date and reason, and pointed to from the adoption record.
- **Rule 24, 2026-11-05** (guardrails while the agent works) stays not adopted until a hook finds something the checks before done would not; such hooks remain an implementation's addition.
- **Every grant excludes changes to its own gate, 2026-11-05** (MG-2). The guarded-inputs half was ruled for every repo on 2026-10-17; the grant-merge half the user ruled 2026-10-17.
- **Rule 7, 2026-11-05** ("Human understanding goes to the new stuff") is adopted as AG-2's source. **Rule 14** is narrowed: a design artifact where the user reserved scope or shape, or asks for one (AG-5), not for every feature.
- **Defaults accepted, 2026-11-05.** Ids as drafted, never reused. The word "Contract" (below). Batching the user's decisions stays a habit, measured by RC-1's wait, not an obligation. Labels for advisories follow rule 9 until the case recurs. "A measured value in a committed floor changes only with a measurement" is a proposal for the repo layer, not an obligation.
- **Words.** "Contract" means product obligations: this file's sense for the method, and each repo's for its software. A framework's own contracts, what it asks of the code that plugs into it, are "protocol". "Inhale" and "exhale" are the breath's two halves (rule 12), and a "mutant" is a mutated copy of the code that a test must kill (rules 26 and 28). "The method's record" is the running record of what the method gives and what it costs, kept by the method's keeper; LN-1 feeds it and LN-4 starts from it.
- **Reserved decisions and reserved questions.** A reserved decision is one the user named in the agreement as theirs to make before the work is spent (AG-1), including how deep they want to look (AG-2). A reserved question is a One Question whose answer would settle a reserved decision; an assumption the user would rule on if it failed joins the reserved decisions when found (AG-3). The two phrases name one thing. Everything not reserved is the agent's to decide and propose (AG-6) (the user, 2026-11-06).

## What this is

The user, 2026-11-04: "we need to have a contract-like thing for our Impatient method. That way if you need to write another module, if you need to implement on a different code base or whatever, we have an implementation-agnostic version of it." And what the method is for: to "enhance the initial human understanding and the agent-human collaboration that ends up being the contract."

Rule 13 says why the Contract exists: the system metaphor "lived in people's heads (Naur, 1985: a program's real value is the theory in its programmers' heads)"; in IMP it is written down. This file is that for the method itself: what any implementation must do (a coordinator, a session with no coordinator, a CI job, a person by hand), never how.

**Membership test.** Would building the method in another harness, another repo or by hand invalidate the statement? Then it is implementation and stays out. Values a repo sets (paths, tools, thresholds, budgets, cadences) are not obligations.

**No names.** The Contract names no implementation, repo or tool, nor the place its keeper works. What it learned from them is in the evidence record, `method-contract-evidence.md`; how each implementation meets it, and where it does not yet, is in the adoption record, `method-contract-adoption.md`. Both are kept by the method's keeper beside this file, and nothing in this file changes when an implementation, a repo or the keeper's home changes.

**Binds.** Every implementation, unless an obligation says the repo or the method's keeper.

**Proof kinds.** *Record*: something left behind that a reader can check. *Check*: something a machine can run. *Question*: something asked of the user, with the answer recorded. *Refusal*: something not done, checkable from what was done.

**Source marks.** "Rule n" is Obie Fernandez's rule as the site showed it on 2026-11-04. "Ours" marks what we add or bend, with the user's dated decision.

**Ids.** Revision 1's ids are kept; merged ones are retired, each retired heading saying where it went. Numbers are never reused.

## 1. Human understanding and the agreement (AG)

These decide where the user's attention goes and what they come away understanding. They are first because that is what the user asked the method for.

### AG-1 The agreement comes first, and it is the user's

Before work is spent, the user and the agent agree, in a record both can read: the outcome, the scope, the constraints, acceptance criteria, the period, the decisions the user reserves, the permissions agents need to prepare and present the work, and the change's size and blast radius. A bug or a chore agrees in one line: the outcome, and for a bug the missing obligation. A story that cannot be stated is not ready, and the work does not start.

**Reason.** The user, 2026-10-16: "Have the human desire in the direction, bring on most of the ideas or brainstorm with an agent to take away some ideas to implement and then the method should take care of it, most of the implementation until it's in production."

Source: rule 1 ("understand and document what you're going to build before you commit to delivering it"). Ours: reserved decisions and permissions (the user, 2026-10-09, human involvement); size and blast radius (the user, 2026-10-16).

Proof: record. A feature's agreement, dated before its first build commit, names each item, "none" being a value. A bug or chore has its line.

### AG-2 The user chooses where their understanding goes

The agreement records where the user wants to take part: the decisions they reserve, and whether they want to see the obligations, a design or a prototype before the work is spent. The implementation asks; it does not choose the depth for them, and it spends their attention where they chose and nowhere else. A bug or chore defaults to nothing reserved and needs no question.

**Reason.** Rule 7: "Human understanding goes to the new stuff." The user, 2026-11-04 (paraphrased): the level of abstraction is the user's to choose per task; deep understanding costs effort and is spent only where it is needed.

Source: rule 7. Ours: the choice is the user's, per task, through reserved decisions (the user, 2026-10-09, human involvement).

Proof: question. A feature's agreement holds the user's answer to "which decisions do you reserve, and do you want to see the obligations before the build?"

### AG-3 The One Question, answered from evidence; spikes when unclear

Before building a feature, ask what we still need to learn. Answer from evidence against the revision the build starts from: the code and, where data matters, authorized representative records, read only, in a safe environment. Record the evidence and the assumptions left; one the user would rule on if it failed joins the reserved decisions. When the answer is unclear, run several spikes, in parallel where the means allow, and compare them; a spike on a question the user reserved goes in front of the user. Spike and prototype code is thrown away. A chore asks nothing; a bug asks only why the fence stands.

**Reason.** Before the build is the cheapest place to change direction, and the answer is what the user's understanding of the change is built from.

Source: rule 5 (the question); rule 16 (name your hypotheses and assumptions); rules 15 and 18 (parallel spikes, deleted; in front of the customer). Ours: evidence first, the base revision and safe environment, assumptions joining the reserved decisions, and only reserved questions going to the user (rule 18 sends every spike) (the user, 2026-11-06).

Proof: record. A feature's record holds the question, the evidence with its revision, and the remaining assumptions, or "nothing to learn" with why. No spike or prototype commit is an ancestor of the merged change.

### AG-4 Retired 2026-11-04, merged into AG-3.

### AG-5 Design talked through until both understand

Where the user reserved the scope or shape of a change, the agent works it out with them in an editable artifact, asking for options and taking rejections, until both understand what will be built, at the depth the user chose (AG-2). Then the build starts. The artifact becomes the design record. Where a screen is reserved, prototypes go in front of the user.

**Reason.** This is where the collaboration "ends up being the contract": the user shapes the obligations in something they can change, and leaves understanding them.

Source: rule 14 ("talk through the design and architecture decisions ... until we both understand what we're building"; "The artifact that helped you think becomes the design record"); rule 18. Ours: only where the user reserved scope or shape (rule 14 opens one for every feature; the user, 2026-11-05), and the depth is the user's (AG-2).

Proof: record. Each reserved scope or shape decision links its artifact, and its last state agrees with the obligations the build was given.

### AG-6 Inside the agreement, agents decide and propose

Within the agreement, agents own implementation and verification: they investigate, choose, resolve ordinary ambiguity, and may demonstrate an architectural change, each as a proposal the user settles when the change is presented. Work stops for the user only on a reserved decision, or on an act outside the branch (a deploy, a change to external data), which needs its own yes. A proposal never silently redefines the agreed outcome, marks itself accepted, or widens the agent's authority.

**Reason.** The user, 2026-10-09: the system "sets the goal, the Contract and the checks, not the steps inside the build". The user's turns, not agent minutes, are the cost.

Source: ours (the user, 2026-10-09, human involvement and vision).

Proof: refusal. Every stop for the user names a reserved decision or an outside act; an unreserved choice appears in the presented change as a proposal.

### AG-7 On M and L work, the builder says back what it understood

For a change sized M or L, whoever builds states, before any code: the outcome and done in its own words, the obligations it will build from, and its assumptions. Each difference from the agreement is ruled on before it matters.

**Reason.** A misunderstanding is cheapest before code, and a backbrief makes the agent's understanding readable to the human.

Source: ours (the user's rulings, 2026-10-15, shift review left).

Proof: record. The backbrief and its rulings are dated before the first code commit.

### AG-8 The result is presented so the user can judge it without reading code

Every change is presented with: a working preview or demonstration fit to it; what changed and why, with its consequential choices and every departure from the agreement and its reason; the Contract's changes and the decisions still open; and the checks, naming each that could not run.

**Reason.** The user, 2026-10-09 (vision): "The human decides and stays in control of what matters, without reading every line; agents do the typing and most of the checking."

Source: ours (the user, 2026-10-09); rule 18 is kin.

Proof: record. The presented change holds each part or says why it does not apply; "code read by the user" is recorded (RC-1).

## 2. The Contract (CN)

### CN-1 Each repo keeps its Contract as obligations with reasons

The repo holds its Contract: per component, obligations each with an id that names one obligation in the repo for its life, a statement, a reason, a kind (functional, or non-functional with its budget and how it is measured), and a proof (a named test, recorded evidence, or none, counted). An obligation states what any implementation must do: if reimplementing the component in another language would invalidate it, it is an implementation test and stays out. Decisions are pointed to, never repeated. Binds the repo.

**Reason.** The Contract is "the team's comprehensive description of what the software must do, in a form a team can collaborate on and maintain" (rule 13).

Source: rules 13 and 20 (functional and non-functional). The membership test: Obie's ZAR case study, not among the numbered rules. Ours: per component, the fields, decisions by pointer (the user, 2026-10-16).

Proof: check. A lint reports each obligation with no reason, a reused id, or a proof naming a missing test; a reviewer's finding of an implementation sentence in the Contract is a CN-1 failure.

### CN-2 Retired 2026-11-04, merged into CN-1.

### CN-3 Pin what the code does, and learn why each fence stands

Before changing code, pin what it does now and find out why each fence is there. A pin the change is meant to break is rewritten as the new obligation's test, never deleted.

**Reason.** A fence moved without knowing why is a regression waiting.

Source: rule 20. Ours: rewritten, not deleted (the user, 2026-11-06; practiced since 2026-10-09).

Proof: record. Pins exist before the changing commit and are green at the tip; a removed pin is matched by a rewritten test.

### CN-4 The Contract changes in the same change as the behavior, and each addition traces to the agreement

A change that adds or changes behavior updates the component's Contract in the same change; one with none says so, with its reason. A feature's obligations are written as the build goes, each under the id the agreement gave it; what the build discovers, and what review finds the Contract got wrong or left out, enter as statement and test in the same change, marked as discovered with the reason they entered. On the exhale the whole Contract is checked against the agreement and against the behavior the change leaves, and that read is not the builder's: a fresh reader compares the Contract's diff with the agreed ids and the discovered marks. An added obligation with neither is a finding, and the change does not merge until it is agreed, marked or removed. Where no second reader can be staffed, the gap is named and the change is presented, not merged under a grant.

For each new or strengthened feature obligation, before the behavior it newly requires is implemented, its test is recorded failing because that behavior is absent; after implementation, it is recorded passing. Where the behavior is already present, that fact is recorded instead, and no failure is manufactured. An obligation discovered after its implementation says that red first was not achieved; a later fault injection can show its test bites, never that the test came first.

**Reason.** Rule 20: "An agent that writes the Contract while it writes the code can end up describing whatever it built." The kill matrix proves a test bites; it does not say the behavior was ever asked for. The agreement's ids are the one reference that exists before the build, and the Contract's diff is small enough to be read against them on every change. A test seen failing before the behavior exists has shown, once, that it can tell the behavior's absence from its presence; the user, 2026-11-19, on a failing test first for new features: "I think we should follow that".

Source: rules 12, 20 and 26. Ours: the same change is required, "no obligation changed" is stated, review findings enter like bugs (the user, 2026-10-16); the trace to the agreement and the reader who did not build (the user, 2026-11-05); the failing test first for a new feature obligation, a bend of rule 20, which asks it only for existing code and, through rule 28, for bugs (the user, 2026-11-19).

Proof: check. A change touching code a Contract covers either changes that Contract or states that no obligation changed, with its reason; every obligation it adds carries an agreed id or a discovered mark with its reason; the exhale reader is named and is not the builder, or the gap is named. And record: each new or strengthened feature obligation has its test's failing run, dated before the behavior's implementation, and its passing run; or says the behavior was already present; or says red first was not achieved.

### CN-5 A production bug enters the Contract first

For a defect in code live in production: the missing obligation first; its test, red against the unfixed code; then the fix; then mutation on the fixed lines where it runs; then the full checks.

**Reason.** "When a bug is found, the Contract was missing something." The unfixed code is the mutant that matches the bug, so the red run is the proof the test kills it.

Source: rule 28, bent: Obie proves the kill and then fixes; we run red on the unfixed code because mutation tools abort on a red suite (the user, 2026-10-18).

Proof: record. The test is shown red on the unfixed code before the fix.

### CN-6 Changing an established obligation is the user's to accept

The agreement authorizes the obligation changes it clearly describes. Any other change to an established obligation or decision keeps the id, is dated, and is flagged in the presented change for the user's acceptance.

**Reason.** An obligation is what the user agreed the software does; an agent may not change the agreement while building to it.

Source: ours (the user, 2026-10-16).

Proof: record. A reworded statement carries its dated line and appears among the decisions for acceptance.

### CN-7 The Contract is met or not, and coverage is published, never invented

The Contract is reported as met or not met. What share of the system it covers is published. Each Contract also counts its obligations by proof (test, evidence, unproved); coverage nobody measured is "unknown", never a number.

**Reason.** A number the user trusts must come from a count.

Source: rule 29 (met or not; how much of the system the Contract covers). Ours: proof counts and "unknown" (the user, 2026-10-16).

Proof: record. Each Contract states its counts and the repo its covered share; a reported number with no count behind it fails.

### CN-8 The repo carries the method without a coordinator

What an agent needs to change code by the method is in the repo: where the Contract lives, the one checks command, the labels, the bug order. A fresh session with no coordinator, given a live bug, fixes it by CN-5 from the repo alone. Binds the repo.

**Reason.** Agents outside any implementation are reached by the repo and its CI, not by an implementation's tools.

Source: ours (the user, 2026-10-16, three layers).

Proof: check. The fresh-session test, once per repo after adoption and after any rewrite of its agent instructions, its result in the method's record.

## 3. Build and fold (BD)

### BD-1, BD-2 Retired 2026-11-04, merged into CN-4 and CK-4.

### BD-3 A test leaves only on mutation evidence

Tests are kept only when they catch something no other test catches. A test is deleted only when mutation evidence, from the code as it will merge, shows the rest catch everything it catches; one at a time, recomputed after each removal.

**Reason.** Every test must prove it is worth keeping, and so must every deletion.

Source: rule 26 (the kill matrix). Ours: deletion only on evidence, one at a time (the user, 2026-10-09).

Proof: refusal. Each deleted test names the mutation run that justified it.

### BD-4 Integrate continuously

No branch outlives the repo's integration limit, or the agreement's period when shorter, unless it waits on the user. A branch that waited is brought up to the current base before it moves, and a conflict resolved on the way is a proposal the presented change names.

**Reason.** Rule 23: "a branch goes stale in hours."

Source: rule 23. Ours: the repo's limit and the waiting exception (the user, 2026-11-06).

Proof: check. Branch age at merge against the repo's limit, and a rebase recorded on each waited branch.

## 4. Checks (CK)

### CK-1 One definition of done, for every agent and for CI

The project's checks run from one definition that any agent runs before saying done and CI runs on every change. A check run by hand and not by CI is a habit, not a gate. Binds the repo.

**Reason.** Rule 19: "The rules run in machines."

Source: rule 19. Ours: CI as the full gate (the user, 2026-10-16).

Proof: check. CI runs the same definition the repo gives its agents.

### CK-2 A check that could not run is a named gap, and code does not move for a tool

Every report of done and every presented change names each required check that could not run and each the project lacks. A gate that could not run blocks unless the project's definition of done says otherwise. A required check that fails on a cause the change did not add, one the main line would fail on too, is a named gap with its cause, not a block: the change is presented with it, and merges on the user's word, never under a grant. Where a framework puts code somewhere a check cannot reach, the gap is named; the code does not move for the tool's sake.

**Reason.** A clean exit is not evidence that a guardrail ran.

Source: ours (the user, 2026-10-09; 2026-10-20 for conventions; 2026-11-06 for a check red on an outside cause); rule 19's "convention over configuration" is kin.

Proof: record and refusal. The presented change lists checks not run and checks red on a cause it did not add, each with its cause; no such change merges under a grant; no change moves code only to bring it within a tool's reach.

### CK-3 Tests must bite: mutation against the merge base

The method needs mutation testing. A change passes when it adds no surviving mutant against its merge base: a full run where it fits the project's budget, otherwise a scoped run that says what it cannot see and is completed by another run. Added code the tool will not mutate needs an accepted reason. Each survivor is equivalent, with its reason, or a sentence the Contract lacks, written with its test. Where no tool runs, red tests are the fallback and the gap is named every time.

Before a check is relied on as proof of an obligation, it is recorded accepting a conforming case and rejecting a named violation of that obligation. Where the proof uses a stand-in for something real (a faked tool, a stubbed service, a recorder), the behavior at that boundary on which the conclusion depends is grounded in independent evidence from the real thing; otherwise the obligation is named unproved. The evidence is reused only while the check, the stand-in and the real thing it stands for are unchanged in what matters to it.

Binds every implementation and the repo.

**Reason.** The user, 2026-10-09: without mutation "there is no way to measure the real impact of a change on the codebase." A check that cannot fail, or that passes against a stand-in more lenient than the real thing, proves nothing it appears to prove; mutation changes the code under test, not the stand-in.

Source: rules 19 ("mutation gates") and 26. Ours: the merge base (the user, 2026-10-18), the budget rule (the user, 2026-11-04), the named fallback (the user, 2026-10-09); the check shown to reject a named violation, and the stand-in grounded in the real thing (the user, 2026-11-19).

Proof: check. The gate's output shows the merge-base comparison and zero new survivors, or the named gap. And record: for each check relied on as proof, the conforming case it accepted and the named violation it rejected; for each stand-in, the evidence from the real thing, or the obligation named unproved.

### CK-4 Breathe out: health judged against the merge base, in the same change

Before a change is done, dead code, needless complexity and undeclared copies are out, and a deliberate copy is declared with its reason. Health checks fail a change for a finding present at its tip and absent at its merge base, wherever it sits, and never for debt it did not add. Debt the change did not add is kept with a reason per entry and changes only with a reason; a change to what the checks read fails without a logged reason. Binds every implementation and the repo.

**Reason.** Rule 12: "Agents add complexity by default, and the exhale is where simplicity happens. Technical debt is not tolerated."

Source: rules 12 and 19. Ours: the merge-base rule (the user, 2026-10-17, every repo), floors (the user, 2026-10-16).

Proof: check. The checks run on both trees; a change to the record of inherited debt without a reason fails the change.

### CK-5 Retired 2026-11-04, merged into CK-2.

## 5. Review (RV)

### RV-1 Retired 2026-11-04, merged into AG-1 and RV-2.

### RV-2 Review depth follows blast radius

Blast radius is large when the change touches a migration that destroys data, authentication or permissions, or deploy configuration or secrets; otherwise it is judged from what the change can break and what reacts once it ships. Small: the checks and the presenter's own read. Large or foundational: two reviewers with different lenses or models who do not see each other's findings, then a synthesis that tries to refute each finding before it reaches the user; after a fix round, review again at that depth. A large review that cannot be staffed is a named gap, and the change is presented, not merged under a grant.

**Reason.** Rule 27: "Save human eyes for reviews guarding against catastrophic risks."

Source: rule 27 (blast radius; adversarial model review). Ours: the list of large kinds (the user, 2026-10-16 and 2026-10-19); two blind reviewers and a refuting synthesis (the user, 2026-11-06).

Proof: record. The presented change links each review and the synthesis; neither reviewer's input holds the other's findings.

### RV-3 Retired 2026-11-04, merged into CN-4.

## 6. Merge and grants (MG)

### MG-1 Every agent change reaches the codebase through a presented change

Every change an agent made reaches the main line through a presented change: a branch put before the user with its checks and the parts AG-8 names, and merged from there. Pairing, where the user drives one agent and merges in that session, keeps its own path.

**Reason.** The presented change is where the user judges (AG-8) and the checks hold. On a code host its usual form is the pull request; a repo with none presents a branch the same way.

Source: ours (the user, 2026-10-09, human involvement).

Proof: check. Every main-line commit since adoption arrives by a merged presented change, or is recorded as pairing.

### MG-2 Merge on the user's word or under a grant they wrote

A change merges only with the user's explicit permission for that change, or under a grant the user wrote naming what it covers, the checks it requires, and when it lapses. A grant covers small blast radius only, unless its text names the large kinds. Outside every grant: an open choice, a departure from the agreement, a check that could not run or that the project lacks unless the grant accepts the lack, and any change to what the grant's checks run or read. Green alone merges nothing.

**Reason.** The user, 2026-10-16: "we need to lean into adhering more into the 'if it's right, we merge' ... most of the time ... it's a waste of time waiting for me to approve the PRs." Grants are how green comes to merge itself as experience earns it. A change that weakens the check it is merged on must not merge on it (the user, 2026-10-17).

Source: rule 27, bent: green merges itself only under a grant (the user, 2026-10-09, 2026-10-16, 2026-10-19). Ours: the gate exclusion (the user, 2026-10-17; for every grant 2026-11-05).

Proof: check. Each merge matches a recorded yes for that change, or a grant whose every condition held at the merge.

### MG-3 Retired 2026-11-04, merged into MG-2.

### MG-4 A grant is asserted at each merge, and its state is kept true

Merging under a grant, the change names it and asserts that no reserved decision is pending and no reserved obligation changed; a false assertion ends the grant. A grant's start, lapses and withdrawal are recorded with date and cause; its lapse conditions are checked before each assertion, and a lapsed grant covers nothing.

**Reason.** A grant is a standing permission of the user's, honored only as written and only while it lives.

Source: ours (the user, 2026-10-16 and 2026-10-17).

Proof: record. Every grant merge carries the assertion; the grants record agrees with each grant's dates and conditions on any day it is read.

### MG-5 Honest labels

`fix:` only for a defect in code live in production, naming its obligation; everything else `refine:`.

**Reason.** Rule 9: throughput is measured, and only an honest label measures it.

Source: rule 9. Ours: a `fix:` names the obligation (the user, 2026-10-16, confirmed 2026-11-06).

Proof: check. A `fix:` change names an obligation id and the production defect.

## 7. The record (RC)

### RC-1 Four facts per change

For each change: whether the user read code, the reserved decisions they made, the wait from ready to their turn, and the outcome with escaped defects. Captured while the work happens, each marked verified, relayed or inferred.

**Reason.** The user, 2026-10-16: minutes and turn budgets are dropped; these four judge the user's time, and the wait is what a grant shrinks.

Source: ours (the user, 2026-10-16).

Proof: record. Each merged change's record holds the four facts with their marks.

### RC-2 The record is true now, and its evidence is kept

Raw evidence (red runs, mutation and gate output, reviews) is kept with the change's record. Every claim says whether it was verified, relayed or inferred. A decision is credited to the user only where the record shows them making it. The record shows each change's step, what it waits on, and its merge.

**Reason.** The user steers from the record, and evidence outside it is lost.

Source: ours (the user, 2026-10-09, the record's rule: verified, relayed or inferred).

Proof: check. A finished change has its record and raw logs beside it, and a sample checked against the main line's history and the work's own record agrees.

### RC-3 Retired 2026-11-04, merged into RC-2.

## 8. Learning the method (LN)

### LN-1 Every report says what the method gave and what got in the way

Each finished change's report says what the method gave and what got in the way, even when one is "nothing", and that goes to the method's record.

**Reason.** A practice stays only while it shows its worth, and that is learned task by task.

Source: ours (the user, 2026-10-09); rule 11 is kin.

Proof: record. The report has both.

### LN-2, LN-3 Retired 2026-11-04; the method's record carries them in its own header, and the simplicity rule is in LN-4.

### LN-4 A change to the method starts from the record, is decided by the user, and reaches every implementation

A change starts from the method's record: a cost that keeps showing up gets a simpler form that keeps the principle; a practice with no gain is proposed for dropping. It is grounded in the rule's reasoning on the site, checked by a fresh critic, and decided by the user. Then this Contract changes first, and each implementation is changed and proved against it; the ruling's line in the record names the implementations it reached. Binds the keeper.

**Reason.** The vision, agreed 2026-10-09: "As simple as the principles allow: a practice stays only while it shows its worth." Rulings made in one document have failed to reach the others.

Source: rule 11. Ours: the path (the user, 2026-11-05, precedence).

Proof: record. Each ruling's line in the record lists the implementations it reached, with dates.

## Not obliged today

- Rule 2 (call your shot weekly) and rule 10 (move attention around): not decided by the user.
- Rule 4 (the weekly showcase) and rule 8 (the morning brief): not adopted (the user's "not yet" of 2026-10-09); an implementation may write a showcase line as an addition.
- Rule 3 (every green merge is a release): a per-repo fact.
- Rule 17 (keep it regenerable): a target, not a requirement (the user, 2026-10-16); no implementation could fail a target.
- Rule 24 (guardrails fire on every change, while the agent works): not adopted until a hook finds what the checks before done would not (the user, 2026-11-05).
- Rules 6, 21, 22 and 25: nothing an implementation could fail.
