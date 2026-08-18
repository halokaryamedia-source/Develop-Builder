# Develop-Builder — General Development Preset Plan

Status: **PLAN ONLY — NOT IMPLEMENTED**  
Working authority: **`Local`**  
Plan maturity: **revised specification candidate — requires final critique before freeze**  
Reference repositories: **BuildIT / TranslateIT / PRD-Creator (`Local`)**

> This file is the implementation plan for **Develop-Builder itself**. It is not a permanent second governance authority and must not automatically be copied into instantiated projects. After preset v1 is implemented and accepted, durable rules belong in their canonical owners; this plan should be reduced or retired and Git history should retain implementation rationale.

---

## 1. Objective

Develop-Builder will provide the **smallest development operating kernel that makes non-trivial project development safe and resumable without making simple work complicated**.

The preset standardizes:

- current authority;
- work-mode selection;
- cross-session continuity;
- requirement vs suggested-method separation;
- semantic ownership;
- direct vs escalated work paths;
- minimum complete implementation;
- evidence proportional to the claim;
- continuation and STOP behavior.

It does **not** standardize product architecture, programming language, framework, runtime, release model, folder structure, database, provider system, production workflow, or specialist inventory.

The primary success condition is:

> **Use the shortest correct path with sufficient context and sufficient proof.**

A project should become more structured only when real product complexity earns that structure.

---

## 2. Correct definitions

### 2.1 Anti-overdevelopment

Anti-overdevelopment does **not** mean “few files”, “few characters”, or “touch only one owner”.

It means:

> **The complexity of the solution and the process must be proportional to the real problem, uncertainty, risk, blast radius, and proof requirement.**

A simple task must remain simple. A risky task may legitimately require more owners, proof, and coordination.

Overdevelopment includes:

- routing a local obvious correction through unnecessary planning layers;
- introducing abstractions that do not reduce total current complexity;
- adding workflows, skills, services, state owners, adapters, fallbacks, or documents before a real responsibility exists;
- broad-reading or broad-testing unrelated surfaces;
- requiring multiple handoffs for work one direct owner can complete safely;
- turning an easy user action or developer workflow into multi-step setup without demonstrated need;
- expanding scope merely because nearby opportunities are visible.

Anti-overdevelopment must never become underdevelopment. Required contracts, affected owners, tests, safety checks, or target proof must not be skipped merely to minimize step count.

### 2.2 AI-slop

AI-slop is output with low decision/implementation value despite looking complete or professional.

Typical forms:

- generic professional filler;
- duplicate documentation/state;
- speculative architecture;
- fabricated completeness where unknowns are invented;
- ceremonial plans, tests, reviews, or reports;
- generic robustness layers that hide unknown root causes;
- placeholder specialists or framework layers;
- abstractions that move complexity without reducing it;
- audits that invent improvements because they assume every audit must produce changes.

The controlling test is:

```text
Does this element materially:
1. change a necessary decision; or
2. prevent a realistic error; or
3. satisfy a real requirement; or
4. reduce total current complexity; or
5. prove a claim that must actually be proven?

If none apply → remove it.
```

---

## 3. Reusable kernel proven by the three reference repositories

The three mature repositories differ in domain and repository shape, but share this reasoning lifecycle:

```text
PIN CURRENT AUTHORITY
→ IDENTIFY REAL TASK CLASS
→ RECOVER ONLY THE CONTEXT THAT CAN CHANGE THE DECISION
→ FIND THE RESPONSIBLE / FIRST WRONG OWNER
→ SEPARATE GOAL FROM SUGGESTED METHOD
→ DECIDE WHETHER A CHANGE IS NEEDED
→ CHOOSE DIRECT OR ESCALATED PATH
→ MAKE THE SMALLEST COMPLETE COHERENT CHANGE
→ VERIFY ONLY THE CLAIMS THAT CHANGED
→ UPDATE ONLY CANONICAL STATE THAT ACTUALLY CHANGED
→ RECORD ONE NEXT STEP WHEN CONTINUATION CHANGED
→ STOP
```

The important lesson is **not** that every task must traverse every governance file.

The reference repositories deliberately contain fast paths:

- bounded Maintenance can start at the exact defect when wider context cannot change the decision;
- ordinary production/authoring work can bypass repository-development machinery;
- specialists are loaded only when they add material semantic procedure;
- broad repository/history reading is not a default safety ritual.

Develop-Builder must preserve that behavior.

---

## 4. Work modes and path selection

The base semantic modes remain:

| Mode | Use when | Default path |
|---|---|---|
| **Context Recovery** | inspect / amati / understand current truth | read-only recovery → report → STOP |
| **Plan** | material method/architecture/product decision unresolved | recover relevant authority → resolve decision → NO IMPLEMENTATION → STOP |
| **Developing** | approved behavior/system capability must be created or materially changed | Direct Bounded Path **or** Non-trivial Developing Path |
| **Maintenance** | concrete defect, regression, stale rule, bounded cleanup | Direct Bounded Path by default; escalate only if diagnosis exposes a material unresolved decision |

A project may add a domain mode such as `Production Execution` only after a real repeatable workflow exists that is semantically different from changing the system itself.

### 4.1 No silent transitions

```text
Context Recovery finds a next step
≠ permission to execute it

Plan reaches a decision
≠ permission to implement unless the user also requested implementation

Maintenance reveals unresolved architecture/product behavior
→ leave Maintenance → Plan

Direct path reveals cross-owner/high-risk uncertainty
→ escalate → Non-trivial Developing
```

---

## 5. Direct Bounded Path — first-class anti-overdevelopment mechanism

A bounded task should use the direct path when **all** material conditions below are true:

```text
1. requested outcome is clear;
2. current owner / first wrong owner is obvious or cheaply discoverable;
3. no unresolved product/architecture/data/security decision exists;
4. no new durable state authority, runtime, compatibility system, dependency boundary, or generic abstraction is required;
5. blast radius is local and understandable;
6. rollback/recovery is straightforward;
7. the relevant proof is obvious and targeted.
```

Route:

```text
current request
→ exact owner / exact defect
→ smallest complete correction
→ targeted proof
→ update canonical continuation only if it changed
→ STOP
```

Examples expected to remain direct:

```text
rename one UI label
fix one known condition
correct one stale route/document pointer
repair one deterministic parser edge case with an obvious owner
remove one obsolete duplicate that has no remaining consumer
```

The direct path is **not a separate work mode**. It is a short execution path inside Developing/Maintenance when the task is already sufficiently grounded.

### Direct-path failure condition

If the preset makes a trivial correction require foundation review, development-brief, ownership map, broad CI, multiple documentation updates, or multiple specialists when those cannot change correctness, **the preset has failed anti-overdevelopment**.

---

## 6. Operational definition of non-trivial Developing

Use the full Developing path when at least one **material** escalation condition exists, for example:

- desired product/system behavior is being newly defined or materially changed;
- responsibility/ownership is unclear or crosses meaningful subsystem boundaries;
- a new persistent state authority/service/runtime/integration is required;
- a new dependency materially changes runtime, distribution, security, or compatibility;
- migration/backward-compatibility/data-conversion behavior is involved;
- security, privacy, user-data ownership, destructive behavior, or release boundary is affected;
- blast radius is large or rollback is difficult;
- several callers/contracts must stay coherent;
- target/runtime/hardware/human acceptance materially affects whether the solution is valid;
- the root cause is not yet grounded;
- the suggested method may materially change architecture or acceptance.

Full route:

```text
AGENTS.md
→ GitHub Core Rules when material
→ CONTEXT.md
→ next-action.md when continuation matters
→ development-brief
→ smallest relevant owner/caller/contract set
→ zero/one useful specialist
→ coherent implementation
→ minimum honest proof
→ state reconciliation
→ STOP
```

`Non-trivial` is determined by uncertainty/impact/risk/coordination, **not by whether code is involved or by line count**.

---

## 7. Complexity calibration

Before choosing the path, assess only dimensions that can change the approach:

```text
uncertainty
semantic/product impact
blast radius
reversibility
security/privacy/data risk
coordination across contracts/owners
proof difficulty / target-environment dependence
```

Do not create a scoring bureaucracy. These are qualitative escalation signals.

### Rule

```text
low uncertainty + low impact + local blast radius + obvious proof
→ direct

material uncertainty / cross-owner impact / high risk / hard proof
→ escalate only as far as necessary
```

The goal is neither “always simple” nor “always rigorous”. It is **proportionate rigor**.

---

## 8. Smallest coherent owner set — not “one owner per task”

The correct invariant is:

> **One canonical owner per responsibility.**

A single logical change may legitimately affect several owners when all are necessary to keep one outcome coherent.

Example:

```text
existing contract
+ implementation
+ regression assertion
```

may be the smallest complete owner set for one fix.

Therefore the implementation rule is:

> **Change the smallest coherent owner set required for the outcome; never create duplicate authority for one responsibility.**

Do not force a one-file/one-owner solution if doing so creates workaround logic, stale contracts, unprotected regressions, or manual synchronization debt.

---

## 9. Core Bootstrap vs Earned/Promoted Governance

The previous plan incorrectly treated the mature-repository shape as a mandatory day-zero shape. v1 must distinguish what a new repository needs immediately from what should appear only after complexity earns it.

### 9.1 Core Bootstrap — required before non-trivial development

```text
/
├─ README.md
├─ AGENTS.md
├─ GITHUB_RULES.md
├─ CONTEXT.md
├─ .gitignore
├─ .agents/
│  └─ skills/
│     └─ development-brief/
│        └─ SKILL.md
└─ docs/
   ├─ foundation/
   │  ├─ 01-project-overview.md
   │  └─ 02-product-requirements.md
   └─ knowledge/
      └─ next-action.md
```

**Core Bootstrap count: 9 persistent files.**

Each has a unique unavoidable responsibility:

| Owner | Unique responsibility |
|---|---|
| `README.md` | human orientation / entrypoint |
| `AGENTS.md` | AI task-class + routing authority |
| `GITHUB_RULES.md` | GitHub execution/history/CI/safety policy |
| `CONTEXT.md` | stable cross-session project orientation |
| `.gitignore` | minimum repository hygiene |
| `01-project-overview.md` | durable product intent/scope/non-goals |
| `02-product-requirements.md` | durable intended behavior/constraints |
| `next-action.md` | active continuation / one next step |
| `development-brief/SKILL.md` | non-trivial Developing front door |

### 9.2 Promoted Governance — absent until earned

These are useful in mature repositories but are **not universal day-zero requirements**:

```text
docs/knowledge/work-routing.md
docs/knowledge/ownership.md or source-ownership/implementation-map
repository governance verifier
repository governance CI workflow
decision log
backlog
review archive
validation report
local acceptance runbook
Experimental/
workspace active/archive system
additional specialist skills
product-specific CI/release workflows
```

Promotion examples:

- create `work-routing.md` only when `AGENTS.md` would otherwise become dense or product/domain modes need a detailed routing reference;
- create an ownership map only when direct source ownership is no longer obvious enough for efficient navigation;
- create repository governance automation only after stable governance invariants exist and drift risk justifies automated enforcement;
- create workspace continuity only when user/project artifacts require continuity separate from repository-development continuity.

Absence is valid architecture, not unfinished work.

---

## 10. Canonical content boundaries for Core Bootstrap

### `README.md`

Human-facing orientation only. Do not maintain detailed current status, roadmap, work modes, or copied requirements here.

### `AGENTS.md`

Own:

- authority/ref boot;
- work-mode selection;
- direct vs non-trivial route;
- smallest sufficient context rule;
- source/claim routing;
- coherent owner-set discipline;
- skill budget;
- evidence boundary;
- STOP behavior.

It must explicitly state that simple bounded work should not enter the full Developing machinery when wider context cannot change the decision.

### `GITHUB_RULES.md`

Own the common execution kernel:

```text
PIN
→ READ MINIMUM
→ DIAGNOSE
→ TOOL FIT
→ WRITE COHERENTLY
→ VERIFY MINIMUM
→ STOP
```

Rules must support both a one-file bounded change and a coherent multi-file atomic delivery. “Write once” must mean intentional logical delivery, not forcing one file or one mutation path.

### `CONTEXT.md`

Stable facts only. No active next step, temporary blocker, task diary, proof transcript, or speculative future architecture.

### `01-project-overview.md`

Own the durable purpose, primary consumer, scope, explicit non-goals, known constraints, success boundary, and high-impact unknowns. Unknown remains unknown.

### `02-product-requirements.md`

Own observable current requirements and constraints. Do not require heavy IDs/taxonomy for small projects. Add structure only when cross-reference complexity makes it useful.

### `next-action.md`

Compact continuation only:

```text
## Current Status
## Active Boundary
## Proof Boundary   # only when material
## Blocker          # only when real
## Next Step        # exactly one
```

Do not use it as backlog, roadmap, or historical timeline.

### `development-brief/SKILL.md`

Use only for **non-trivial Developing**. Required contract fields are conditional: include only fields that can change the decision.

Core logic:

```text
ground goal
→ inspect current behavior/owner
→ decide whether change is needed
→ define smallest coherent scope
→ 2–5 falsifiable criteria when complexity warrants them
→ proof budget
→ zero/one useful specialist
→ implement
→ final gate
→ STOP
```

A trivial correction must not be escalated simply to satisfy this skill.

---

## 11. Simplified creation policy

The previous eight-question gate for every persistent addition was itself too procedural.

### 11.1 Normal addition gate

For ordinary source/test/document additions, ask only:

```text
1. Is it needed for the current accepted outcome?
2. Is this the correct existing responsibility/owner location?
3. Is this the simplest complete form?
```

If yes, create it. No extra ceremony.

### 11.2 High-cost architectural addition gate

Use the extended gate only for additions that create durable complexity, such as:

```text
new state authority
new service/runtime/worker
provider/router/registry
compatibility/fallback layer
persistent cache/queue/event bus
new dependency boundary
new specialist skill
new CI/release/experiment system
new governance/state owner
```

Required questions:

```text
1. What current responsibility or demonstrated problem requires it?
2. Why can the existing direct path/owner not satisfy the requirement cleanly?
3. What current consumer needs this now?
4. What complexity does it remove or what required capability does it uniquely add?
5. What new failure/maintenance/synchronization cost does it introduce?
6. Is there a smaller current solution with equal acceptance?
```

If there is an equally correct smaller solution, use it.

“Best practice”, “clean architecture”, “future scalability”, “might need later”, and “another repository has it” are not sufficient reasons.

---

## 12. Net Simplification Test

An abstraction is justified only when it improves the **total current system**, not merely local code appearance.

Before adding an abstraction, ask whether it measurably reduces one or more current burdens:

- repeated logic;
- caller knowledge;
- coupling;
- duplicated state/authority;
- change coordination;
- failure handling complexity;
- user/developer setup steps;
- repeated semantic judgment.

Then account for costs it adds:

- additional indirection;
- new files/modules/interfaces;
- new synchronization/registration;
- new failure modes;
- debugging hops;
- maintenance obligations.

If complexity is merely moved or renamed rather than reduced, **do not add the abstraction**.

---

## 13. Proof calibration

Validation is evidence, not ceremony.

Use the cheapest proof that can falsify the changed claim.

```text
source/static claim
→ targeted source/static proof

build/contract claim
→ relevant build/test

runtime/UI/device/model claim
→ actual matching runtime/target capability

visual/audio/content acceptance
→ responsible human or matching acceptance capability
```

A small task may require one focused check. A high-risk one-line security change may require more proof than a 100-line internal refactor.

Do not use broad/full CI merely because it exists. Use broad verification only when the changed public/executable contract can realistically affect the broader surface.

Never upgrade source/CI proof into runtime/target/human acceptance.

---

## 14. Context economy without context loss

Mandatory continuity exists to prevent wrong work, not to create repeated I/O ceremony.

Rules:

- a fresh session/non-trivial Developing task recovers stable context and active continuation;
- within the same bounded task/session, already verified context may be reused unless relevant repository state could have changed;
- bounded Maintenance/direct work may skip stable-context files when they cannot change the decision;
- history, old reports, reviews, all skills, and broad source scans remain on-demand evidence only.

The correct target is **minimum sufficient context**, not “always re-read everything” and not “read as little as possible regardless of risk”.

---

## 15. Retirement and pruning

Anti-overdevelopment applies to removal as well as creation.

```text
hard to add without need
+
easy to remove when the need disappears
```

When a persistent layer no longer owns a live responsibility:

- remove or fold it into the remaining canonical owner when safe;
- remove stale routing to it;
- do not retain it merely as compatibility/history;
- keep historical rationale in Git history or a justified durable decision owner.

A mature repository should be allowed to become simpler again.

---

## 16. Verification architecture — template vs instantiated project

The previous plan incorrectly mixed two different proof surfaces.

### 16.1 Develop-Builder template verification

This is verification for **Develop-Builder itself** and may check:

- Core Bootstrap package completeness;
- reference-domain neutrality of the generic template;
- no duplicate template owner definitions;
- direct-path and non-trivial-path contracts exist;
- template links/invariants are coherent;
- promoted surfaces are not accidentally bundled as mandatory project output.

A template verifier/workflow may be implemented in Develop-Builder if it is the simplest reliable way to protect the template.

### 16.2 Instantiated project verification

An instantiated project must **not automatically inherit a verifier that assumes**:

- exactly one skill forever;
- generic neutrality terminology;
- fixed reference-product forbidden words;
- a permanent exact bootstrap file count.

Project governance verification is added/promoted only when stable project invariants and drift risk justify it.

If promoted, it verifies that project’s actual current governance — not the pristine template shape.

---

## 17. Bootstrap Adaptation

When using Develop-Builder for a new project, populate only facts required to begin correctly:

```text
project name/purpose
primary user/consumer
current scope/non-goals
working authority
known material constraints
initial proof boundary
first real development objective
```

Candidate Core Bootstrap owners are updated **only when their owned state actually changes**. Do not force a write to every bootstrap file merely because adaptation is occurring.

Do not invent during bootstrap:

- final architecture;
- complete source tree;
- specialist inventory;
- database/API/release systems;
- compatibility matrix;
- test matrix for nonexistent surfaces;
- future roadmap.

Bootstrap makes development safe; it does not pretend the product is already fully designed.

---

## 18. Reduced adversarial acceptance suite

The old 15-scenario set was too repetitive. v1 needs a smaller high-signal suite.

### A. Read-only remains read-only

`Amati repo dan pahami next step` → recover/report → do not execute.

### B. Simple work stays simple

One label rename or one obvious local conditional fix → exact owner → edit → targeted check → STOP. Full development machinery must not be required unless a material hidden dependency appears.

### C. Unresolved architecture escalates

A task requiring new persistent authority/integration with unresolved product behavior → Plan or non-trivial Developing, not direct invention.

### D. Suggested method can be redirected

User proposes framework/provider/architecture → preserve goal, evaluate method, FOLLOW / REFINE / REDIRECT.

### E. Stale continuation reconciles

`next-action` conflicts with current source → inspect current owner → reconcile stale state → continue from actual truth.

### F. Coherent cross-owner change remains coherent

A fix requires contract + implementation + regression proof → touch the smallest coherent set; do not force a one-owner workaround.

### G. Proof does not inflate

Hosted/source proof without actual runtime/target/human validation → stronger claim remains unverified.

### H. Optional architecture is rejected without current need

“Add scalable provider/router/specialists/workspace/CI for later” → reject unless current responsibility passes the high-cost addition gate.

---

## 19. Preset v1 acceptance criteria

Preset v1 may be frozen only when all pass.

### A. Shortest Correct Path

The system explicitly prefers the simplest route that still satisfies correctness, safety, continuity, and proof.

### B. Simple Work Stays Simple

Bounded obvious changes can bypass full Developing ceremony and complete through direct owner + targeted proof.

### C. Proportionate Escalation

Uncertainty, risk, blast radius, cross-owner impact, and proof difficulty escalate process only as far as needed.

### D. Complete, Not Minimalistic

The system does not omit necessary owners/contracts/tests merely to reduce file or step count.

### E. Domain Neutrality

Core Bootstrap imposes no reference product, runtime, framework, language, release, or storage architecture.

### F. Cross-session Recoverability

A fresh session can recover stable project truth and active continuation without relying on chat history.

### G. Ownership Integrity

Each responsibility has one canonical owner while a coherent task may affect the smallest necessary owner set.

### H. Net Simplification

New abstraction/persistent architecture must reduce current total complexity or uniquely satisfy a demonstrated capability.

### I. Proof Honesty

Evidence strength cannot exceed the environment/claim actually exercised.

### J. Growth and Pruning

Optional structures appear only when earned and can be removed when their responsibility disappears.

### K. No AI-slop

No duplicate status/ownership/routing, generic filler systems, fabricated unknowns, ceremonial reports/tests, or placeholder specialists are required by the baseline.

---

## 20. Implementation sequence after final plan acceptance

### Phase 0 — Final critique and freeze

Current phase after this revision.

- re-audit Core Bootstrap 9-file responsibility set;
- challenge Direct Bounded Path vs non-trivial threshold with real examples;
- verify no underdevelopment hole was introduced;
- verify promoted governance is truly optional;
- perform one final anti-slop/anti-overdevelopment critique;
- only then freeze specification.

### Phase 1 — Implement Core Bootstrap

Create/adapt the nine core files only.

No promoted governance or domain/runtime structure.

### Phase 2 — Implement Develop-Builder template validation only if justified

Choose the smallest reliable template verification mechanism. It must verify the template itself, not impose pristine-template invariants on future projects.

### Phase 3 — Direct-path / escalation audit

Exercise the reduced adversarial suite and at least three different project contexts:

```text
local application/runtime
content/production system
creative/tooling/plugin system
```

Do not build sample applications. Test assumptions only.

### Phase 4 — Complexity/pruning audit

Ask:

```text
Can any core owner be removed without losing a unique day-zero responsibility?
Does any rule create an unnecessary decision hop?
Can simple work remain direct?
Can legitimately complex work still become complete?
Does any abstraction/gate merely move complexity?
Is any promoted surface accidentally required?
Can obsolete layers be retired cleanly?
```

### Phase 5 — Freeze preset v1

After all gates pass:

- record v1 in the real canonical owner(s);
- set one real next step or stable idle continuation;
- reduce/retire this implementation plan so it does not become a second authority;
- STOP.

---

## 21. Protected non-goals

Develop-Builder v1 is not:

- a universal application/framework starter;
- a universal folder tree;
- a monorepo architecture;
- an autonomous project manager;
- a roadmap generator;
- a coding-style framework;
- a prebuilt frontend/backend/database/provider architecture;
- a library of placeholder specialists;
- an automatic release/PR/branch system;
- an exhaustive documentation framework;
- a generic test framework;
- a migration requirement for mature repositories.

It is a **development governance and continuity kernel whose main job is to keep the path to a correct result as direct as the real problem allows**.

---

## 22. Next Step

**Perform one final hard critique of this revised specification against BuildIT, TranslateIT, and PRD-Creator, concentrating on the 9-file Core Bootstrap, Direct Bounded Path, non-trivial escalation threshold, and risk of underdevelopment. Do not implement the preset until that critique passes.**
