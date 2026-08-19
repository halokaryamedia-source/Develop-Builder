# Product Requirements

These are the durable requirements of the general development starter. They describe intended behavior, not implementation progress.

## Authority and continuity

- The active working/development authority must be explicit; this repository uses `Local`.
- The system must not silently fall back to another branch or repository default.
- Stable project orientation must be recoverable from repository state without relying on chat history.
- Active continuation must have one canonical owner and one meaningful next step.
- Context Recovery and non-trivial Developing must recover `CONTEXT.md` + `docs/knowledge/next-action.md` before choosing current work.
- If continuation prose conflicts with current source/state, inspect the exact current owner and reconcile stale continuity vs stale implementation before continuing.

## Single current source — mandatory anti-AI-slop rule

Each durable responsibility has one current canonical owner.

Evolution must update that owner rather than create generations around it.

By default, the starter and projects created from it must not create or preserve:

- `v1`, `v2`, `v3`, or similar governance/implementation generations;
- `_new`, `_old`, `_legacy`, `_backup`, `final2`, duplicate replacement files/folders;
- parallel services/controllers/configs/state stores for the same responsibility;
- old/new runtime paths retained “just in case”;
- compatibility aliases, migration bridges, fallback layers, feature flags, adapters, or deprecated copies used only to avoid replacing current source;
- duplicate plan/status/TODO/completion/review/session-memory systems;
- temporary repository structures that remain because cleanup was deferred.

The normal finalization rule is:

```text
identify canonical owner
→ implement final current behavior in that owner
→ update required callers/contracts/tests
→ remove superseded current path/state when safe
→ prove final behavior
→ STOP
```

Git history preserves ordinary history. Current source must not preserve obsolete structures solely as historical evidence.

A compatibility or migration boundary is allowed only when a concrete **current external contract** requires it, such as persisted user data, deployed clients, a supported public API/protocol, or an explicitly supported file/schema format. It must remain minimal and must not create a second product/runtime authority.

Real externally defined product/API/schema versions are allowed only when versioning is part of the actual product contract. AI development evolution itself is never sufficient reason to create versioned owners.

## Work classification

The baseline distinguishes:

```text
Context Recovery
Plan
Developing
Maintenance
```

- Context Recovery is read-only unless the user also requests implementation/change.
- Plan resolves material decisions without silently implementing them.
- Maintenance begins from a concrete defect/first wrong owner when wider context cannot change the decision.
- Developing supports both a Direct Bounded Path and a non-trivial escalated path.

### Bootstrap Instantiation

A fresh project created from the starter uses a clean snapshot of the **current tree**, not the starter's Git history.

Before normal development:

```text
new empty repository
→ establish `Local` as working authority unless explicitly replaced by project policy
→ copy current starter tree
→ replace project-specific starter state with real project truth
→ one coherent first project commit
```

Bootstrap establishes only:

- project name/purpose;
- primary user/consumer;
- current scope and explicit non-goals;
- working branch/ref authority;
- known material constraints;
- initial proof boundary;
- first real development objective.

Project-specific owners to adapt first:

```text
README.md
CONTEXT.md
docs/foundation/01-project-overview.md
docs/foundation/02-product-requirements.md
docs/knowledge/next-action.md
```

Root routing/GitHub/development-brief rules remain identity-neutral generic owners unless the project proves a real routing/authority/procedure difference.

Bootstrap must not invent final architecture, source trees, database/API/release systems, compatibility matrices, specialist inventories, test matrices for nonexistent surfaces, or future roadmaps.

Bootstrap must not preserve starter-specific identity/status beside the new project state. Replace it; do not create a versioned or legacy copy.

Bootstrap is accepted only when:

```text
new project identity is consistent across project-specific owners
stable context describes the new project
foundation describes current approved intent and requirements
next-action contains only current project continuation
exactly one real Next Step exists
no duplicate/versioned/legacy current owner exists
unknowns remain explicit
```

Bootstrap completion does not itself authorize implementation unless the user also requested it.

### Existing-system / Domain Execution

Normal use of an existing system to create or revise its intended domain output is not system Developing merely because files/artifacts are created.

When a valid domain owner/procedure exists and no system behavior is changing, work routes directly to that owner/procedure and matching acceptance boundary.

The starter must not pre-create universal Production/Asset/Content modes. A project formalizes a named domain route only when a real repeated workflow exists and the route reduces current coordination complexity.

If domain execution exposes a defect or requires changing how the system works, route the change to Maintenance or Developing.

## Plan discipline

Plan must recover repository/source facts before asking the user to repeat or decide discoverable information.

Ask only when a remaining unresolved choice materially changes product behavior, architecture, privacy/security/data ownership, compatibility, release/destructive boundary, or acceptance.

```text
plan-only request
→ report plan
→ STOP

explicit plan + implementation request
+ no remaining material user decision
→ state transition
→ Developing

material user decision still required
→ STOP and ask
```

Plan must not silently become Developing.

## Direct Bounded Path

A simple task must stay simple when outcome, owner, blast radius, rollback, and proof are sufficiently clear.

The direct path must:

- inherit exact repo/ref and root safety rules;
- go to the exact owner/defect;
- inspect nearest caller/contract/test only when they can change impact or acceptance;
- make the smallest complete correction;
- remove superseded stale/current paths created by the same correction when safe;
- use targeted proof;
- update continuation only if it changed;
- stop when complete.

The direct path must not be forced through foundation review, `development-brief`, broad CI, specialist loading, or extra documentation when those cannot materially change correctness or proof.

A small/local dependency use does not automatically make work non-trivial. Escalate only when a **material dependency boundary** can change runtime, distribution, security, compatibility, ownership, rollback, or acceptance.

## Non-trivial Developing

Use the full Developing path when material uncertainty, semantic impact, risk, blast radius, ownership coordination, migration, new persistent authority, material dependency boundary, hard rollback, or target/human acceptance can change the solution.

Non-trivial Developing must:

- recover `CONTEXT.md` + `docs/knowledge/next-action.md`;
- use `development-brief`;
- separate requested outcome from suggested method/reference;
- establish the smallest coherent owner/caller/contract set;
- inspect relevant existing regression/invariant assertions when they can constrain correctness;
- define 2–5 falsifiable acceptance criteria;
- select a proof budget proportional to the claim;
- use zero or one useful project specialist by default;
- implement one coherent final result;
- remove superseded current paths/state when safe instead of retaining artificial generations;
- reconcile only canonical state that changed;
- stop when the acceptance boundary is satisfied.

`Non-trivial` must not be inferred from code presence, line count, file count, or impressive terminology.

## Local rule inheritance

A mature project may add a nearer `AGENTS.md` only when a durable package/domain responsibility requires distinct local routing/rules.

- Root `AGENTS.md` remains repository-wide authority.
- The nearest applicable `AGENTS.md` may narrow local behavior but must not weaken root branch/ref safety, current-source finalization, proof honesty, ownership integrity, or STOP boundaries.
- Read the nearest local `AGENTS.md` only when it can materially change the task.
- Directory existence alone is not justification for another `AGENTS.md`.

## Ownership and conflict resolution

- Each durable responsibility has one canonical owner.
- One logical task may affect several owners when all are required for one complete outcome.
- Prefer the smallest coherent owner set; do not force one-file solutions.
- Generated/derived output does not outrank or repair its canonical source/generator.

```text
current user decision vs durable policy
→ reconcile current policy

durable policy vs current source
→ desired behavior vs implementation state
→ determine which current owner is stale/wrong

next-action vs current source/state
→ stale continuation vs stale implementation
→ reconcile stale owner

historical evidence vs current owner
→ current owner wins unless history is explicitly revalidated

generated artifact vs canonical source
→ fix canonical source/generator

material current conflict cannot be recovered responsibly
→ UNKNOWN
→ Plan / focused user decision
```

Never create a compatibility/legacy path merely to avoid resolving a current conflict.

## Requirement vs method

- User intent and approved product decisions define the outcome.
- Frameworks, samples, screenshots, old branches/source, reference repositories, and technical methods are evidence/method proposals unless explicitly required.
- The agent must be able to FOLLOW, REFINE, REDIRECT, or stop for a real unresolved decision.
- `No change required` is valid.

## Root-cause and edit discipline

Before a non-trivial behavior edit establish:

1. what happens now;
2. who owns it;
3. why it is wrong/incomplete;
4. why the proposed final change addresses that cause;
5. what proof can falsify the result.

Before creating any persistent owner/file/module/layer, establish why the existing canonical owner cannot represent the responsibility and why the addition is required now.

Do not hide unknown causes with blind retry, arbitrary delay, broad fallback, compatibility aliases, duplicate state, parallel services/runtimes, or generic frameworks.

## Anti-overdevelopment

Solution/process complexity must be proportional to the real problem, uncertainty, risk, blast radius, reversibility, coordination, and proof requirement.

For ordinary additions:

```text
needed for current accepted outcome?
correct existing responsibility/location?
simplest complete final form?
```

High-cost durable architecture—new state authority, runtime/service, provider/router/registry, compatibility/fallback layer, persistent queue/cache, material dependency boundary, specialist, CI/release/experiment system, or new governance owner—requires demonstrated current need.

“Best practice”, “clean architecture”, “future scalability”, “might need later”, “keep old just in case”, and “another repository has it” are not sufficient requirements.

## Anti-AI-slop

The starter must reject:

- generic professional filler;
- duplicate status/routing/ownership systems;
- speculative architecture;
- fabricated unknown product facts;
- ceremonial plans/reports/reviews/tests;
- placeholder specialists;
- generic robustness layers that hide unknown root causes;
- abstraction that only moves complexity;
- audits that invent work because every audit is assumed to require changes;
- versioned rewrites used instead of replacing canonical source;
- legacy/old/new copies kept without a current external obligation;
- compatibility/fallback paths that exist only because AI is afraid to remove the superseded path;
- temporary structures, experiments, or migrations promoted to permanent source without a real owner/contract;
- repeated “hardening” passes that add rules without reproduced evidence.

A persistent element must materially change a necessary decision, prevent a realistic error, satisfy a real requirement, reduce total current complexity, or prove a required claim. Otherwise remove it.

## Evidence

- Validation is selected by the claim, not ceremony.
- Prefer the cheapest evidence capable of falsifying the changed claim.
- Broader verification is justified only when the changed executable/public contract can realistically affect the broader surface.
- Repository/static evidence does not prove runtime/device/visual/audio/model/target-machine/human acceptance.
- A small high-risk change may require more proof than a larger low-risk internal change.

## Growth and pruning

The Core Bootstrap is intentionally small.

Detailed routing references, ownership maps, decision logs, backlogs, reviews, governance automation, experiments, workspace continuity, specialist skills, domain-specific production routes, product CI/release workflows, and runtime/source architecture are added only when a real current responsibility earns them.

When a persistent layer no longer owns a live responsibility, remove it or fold it into the remaining canonical owner when safe. Do not rename it `legacy`, version it, or keep a compatibility copy just to avoid deletion. Git history preserves retired rationale.

## Completion

Completion is terminal.

When the requested outcome and required proof are satisfied, do not automatically continue into adjacent cleanup, another audit, another verifier, historical TODOs, another “version”, or the next milestone.
