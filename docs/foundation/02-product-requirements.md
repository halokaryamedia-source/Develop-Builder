# Product Requirements

These are the durable requirements of the Develop-Builder general preset. They describe intended behavior, not implementation progress.

## Authority and continuity

- The active working/development authority must be explicit; this repository uses `Local`.
- The system must not silently fall back to another branch or repository default.
- Stable project orientation must be recoverable from repository state without relying on chat history.
- Active continuation must have one canonical owner and one meaningful next step.
- Context Recovery and non-trivial Developing must recover `CONTEXT.md` + `docs/knowledge/next-action.md` before choosing current work.
- If continuation prose conflicts with current source/state, the exact current owner must be inspected and stale state reconciled before continuing.

## Work classification

The baseline must distinguish:

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

A fresh project created from Develop-Builder must have an explicit bounded bootstrap route before normal development.

Bootstrap must establish only:

- project name/purpose;
- primary user/consumer;
- current scope and explicit non-goals;
- working branch/ref authority;
- known material constraints;
- initial proof boundary;
- first real development objective.

The bootstrap should adapt existing project-specific owners first:

```text
README.md
CONTEXT.md
docs/foundation/01-project-overview.md
docs/foundation/02-product-requirements.md
docs/knowledge/next-action.md
```

Root routing/GitHub/development-brief rules remain generic unless the instantiated project proves a real authority/routing/procedure difference.

Bootstrap must not invent final architecture, source trees, database/API/release systems, compatibility matrices, specialist inventories, test matrices for nonexistent surfaces, or future roadmaps.

Bootstrap must remove or replace Develop-Builder-specific project identity, preset audit/status state, and old preset continuation from the instantiated project's current truth. Generic governance semantics may remain; preset-specific project facts may not masquerade as new-project facts.

Bootstrap is accepted only when:

```text
new project identity is consistent across current project owners
stable context describes the new project
foundation describes current approved intent and requirements
next-action contains only the new project's current continuation
exactly one real Next Step exists
unknowns remain explicit rather than fabricated
```

Bootstrap completion does not itself authorize implementation unless the user also requested it.

### Existing-system / Domain Execution boundary

Normal use of an existing system to create or revise its intended domain output must not be classified as system Developing merely because files or artifacts are created.

When a valid domain owner/procedure already exists and no system behavior is changing, work should route directly to that owner/procedure and its matching acceptance boundary.

The baseline must not pre-create a universal `Production Execution`, `Asset Authoring`, or equivalent mode. A project may formalize a named domain mode only when a real repeatable workflow exists and the additional route reduces current coordination complexity.

If domain execution exposes a defect or requires changing how the system works, the defect/change must route to Maintenance or Developing instead of being hidden inside production/authoring work.

## Plan discipline

Plan must recover repository/source facts before asking the user to repeat or decide discoverable information.

Ask the user only when a remaining unresolved choice materially changes product behavior, architecture, privacy/security/data ownership, compatibility, release/destructive boundary, or acceptance.

Plan transitions must be explicit:

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

A simple task must be able to remain simple when the requested outcome, owner, blast radius, rollback, and proof are sufficiently clear.

The direct path must:

- inherit exact repo/ref and root safety rules;
- go to the exact owner/defect;
- inspect nearest caller/contract/test only when they can change impact or acceptance;
- make the smallest complete correction;
- use targeted proof;
- update continuation only if it changed;
- stop when complete.

The direct path must not be forced through foundation review, `development-brief`, broad CI, specialist loading, or extra documentation when those cannot materially change correctness or proof.

The direct path must also never skip a material contract, safety boundary, affected caller, or required proof.

A small/local dependency use does not automatically make work non-trivial. Escalation is required when a **material dependency boundary** can change runtime, distribution, security, compatibility, ownership, rollback, or acceptance.

## Non-trivial Developing

The full Developing path is required when material uncertainty, semantic impact, risk, blast radius, ownership coordination, migration, new persistent authority, material dependency boundary, hard rollback, or target/human acceptance can change the solution.

Non-trivial Developing must:

- recover `CONTEXT.md` + `docs/knowledge/next-action.md`;
- use `development-brief`;
- separate requested outcome from suggested method/reference;
- establish the smallest coherent owner/caller/contract set;
- inspect relevant existing regression/invariant assertions when they can constrain correctness;
- define 2–5 falsifiable acceptance criteria;
- select a proof budget proportional to the claim;
- use zero or one useful project specialist by default;
- implement one coherent result;
- reconcile only canonical state that changed;
- stop when the acceptance boundary is satisfied.

`Non-trivial` must not be inferred from code presence, line count, file count, or impressive terminology alone.

## Local rule inheritance

A mature project may add a nearer `AGENTS.md` only when a durable package/domain responsibility requires distinct local routing or rules.

- Root `AGENTS.md` remains repository-wide authority.
- The nearest applicable `AGENTS.md` may narrow local behavior but must not silently weaken root branch/ref safety, proof honesty, ownership integrity, or STOP boundaries.
- The agent should read the nearest local `AGENTS.md` only when it can materially change the affected task.
- Directory existence alone is not justification for another `AGENTS.md`.

## Ownership and conflict resolution

- Each durable responsibility must have one canonical owner.
- One logical task may affect several owners when they are all required for one complete outcome.
- The system must prefer the smallest coherent owner set, not force one-file/one-owner solutions.
- Generated/derived output must not outrank or be manually patched to hide defects in its canonical source/generator.

Conflicts must be interpreted by claim type instead of resolved with one global ranking:

```text
current user decision vs durable policy
→ reconcile current policy

durable policy vs current source
→ distinguish desired behavior from implementation state
→ determine which owner is stale/wrong

next-action vs current source/state
→ distinguish stale continuation from stale implementation
→ reconcile stale owner

historical evidence vs current owner
→ current owner wins unless history is explicitly revalidated/promoted

generated artifact vs canonical source
→ fix canonical source/generator

material conflict cannot be recovered responsibly
→ UNKNOWN
→ Plan / focused user decision
```

The agent must not silently choose between contradictory current authorities merely to continue.

## Requirement vs method

- User intent and approved product decisions define the outcome.
- Suggested frameworks, samples, screenshots, old branches, reference repositories, and technical methods are evidence/method proposals unless explicitly required.
- The agent must be able to FOLLOW, REFINE, REDIRECT, or stop for a real unresolved decision.
- `No change required` is a valid successful result.

## Anti-overdevelopment

The solution/process complexity must be proportional to the real problem, uncertainty, risk, blast radius, reversibility, coordination, and proof requirement.

For ordinary additions, the decision should normally reduce to:

```text
needed for the current accepted outcome?
correct existing responsibility/location?
simplest complete form?
```

High-cost durable architecture—new state authority, runtime/service, provider/router/registry, compatibility/fallback layer, persistent queue/cache, material dependency boundary, specialist, CI/release/experiment system, or new governance owner—requires demonstrated current need.

A high-cost addition is justified only when the existing direct solution cannot satisfy the current requirement cleanly and the addition uniquely provides required capability or reduces total current complexity after its own failure/maintenance costs are counted.

“Best practice”, “clean architecture”, “future scalability”, “might need later”, and “another repository has it” are not sufficient requirements.

## Anti-AI-slop

The baseline must not require:

- generic professional filler;
- duplicate status/routing/ownership systems;
- speculative architecture;
- fabricated unknown product facts;
- ceremonial plans/reports/reviews/tests;
- placeholder specialists;
- generic robustness layers that hide unknown root causes;
- abstraction that only moves complexity to another layer;
- audits that invent work because they assume every audit must produce changes.

A persistent element should materially change a necessary decision, prevent a realistic error, satisfy a real requirement, reduce current total complexity, or prove a required claim. Otherwise it should be removed.

## Evidence

- Validation must be selected by the claim, not by ceremony.
- The cheapest evidence capable of falsifying the changed claim is preferred.
- Broader verification is justified only when the changed executable/public contract can realistically affect that broader surface.
- Repository/static evidence does not prove runtime/device/visual/audio/model/target-machine/human acceptance.
- A small high-risk change may require more proof than a larger low-risk internal change.

## Growth and pruning

The day-zero Core Bootstrap is intentionally small.

Detailed routing references, ownership maps, decision logs, backlogs, reviews, governance automation, experiments, workspace continuity, specialist skills, domain-specific production/authoring routes, product CI/release workflows, and runtime/source architecture are added only when a real current responsibility earns them.

When a persistent layer no longer owns a live responsibility, it should be removed or folded into the remaining canonical owner when safe. Historical rationale belongs in Git history or a justified durable decision owner, not in dead compatibility structure.

## Completion

Completion is terminal.

When the requested outcome and required proof are satisfied, the system must not automatically continue into adjacent cleanup, another audit, another verifier, historical TODOs, or the next milestone.
