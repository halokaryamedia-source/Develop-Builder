# Agent Routing

Develop-Builder is a general development preset. Current repository/project sources are authority for repository state; chat history is supporting context only.

## Branch and safety authority

- `Local` is the working/development authority.
- Never silently fall back to another branch or repository default.
- Material GitHub execution follows `GITHUB_RULES.md`.
- Choose the **smallest sufficient path**. Efficiency must not remove context, contracts, safety, or proof that can change correctness.

## Rule inheritance

Root `AGENTS.md` owns repository-wide invariants and task routing. A project may later add a nearer `AGENTS.md` for a real package/domain responsibility.

When work is inside a subtree with a nearer `AGENTS.md`:

```text
root AGENTS.md
→ nearest relevant AGENTS.md
→ exact owner/source
```

- Read a nearer `AGENTS.md` only when its local rules can materially change the task.
- A nearer rule may narrow local/domain behavior; it must not silently weaken root branch/ref safety, proof honesty, ownership integrity, or STOP boundaries.
- For local behavior, the nearest applicable rule wins when it is compatible with root invariants.
- Do not create nested `AGENTS.md` files merely because directories exist; add one only when a durable local responsibility needs distinct routing/rules.

## Task class first

### Bootstrap Instantiation

Use this route when starting a **new project from the Develop-Builder preset** before normal project development begins.

Establish only current project truth:

```text
project name / purpose
primary user or consumer
current scope / explicit non-goals
working branch/ref authority
known material constraints
initial proof boundary
first real development objective
```

Then adapt only the existing owners whose project-specific state must change:

```text
README.md
CONTEXT.md
docs/foundation/01-project-overview.md
docs/foundation/02-product-requirements.md
docs/knowledge/next-action.md
```

`AGENTS.md`, `GITHUB_RULES.md`, and `development-brief` remain the generic kernel unless the new project has a **real** authority/routing/procedure difference that must be represented there.

Bootstrap rules:

- unknown project facts remain unknown;
- do not invent final architecture, source tree, database/API/release design, specialist inventory, compatibility matrix, future roadmap, or tests for nonexistent surfaces;
- remove/replace Develop-Builder-specific project identity, preset status, parity/audit state, and old continuation from the instantiated project's current truth;
- retain generic governance semantics only where they still apply;
- do not copy Develop-Builder Git history/status as project requirements;
- finish with exactly one real project `Next Step`.

Bootstrap acceptance:

```text
project identity is the new project, not Develop-Builder
stable context describes the new project
foundation describes current approved intent/requirements
next-action describes only the new project's active continuation
generic kernel has no leaked preset-specific project facts
unknowns remain explicit
```

After those conditions are true: report the bootstrap result and STOP. Bootstrap does not automatically start the first development objective unless the user also requested implementation.

### Context Recovery

For read-only `amati`, inspect, understand, audit, study, or context recovery:

```text
AGENTS.md
→ GitHub Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ smallest owner needed to explain current state
→ report
→ STOP
```

`CONTEXT.md` and `docs/knowledge/next-action.md` are mandatory continuity for Context Recovery so a fresh session does not invent current boundaries or promote arbitrary historical work.

Do not edit, run CI, execute a recorded next step, or promote old TODO/history merely because they were discovered.

### Plan

Use when a material product, architecture, ownership, risk, or acceptance decision remains unresolved.

```text
recover relevant current authority
→ recover repository/source facts that can answer the question
→ inspect smallest evidence that can change the decision
→ separate goal from suggested method
→ resolve/present only the remaining material decision
```

Before asking the user, recover facts that current repository owners/source can answer. Ask only when an unresolved choice materially changes product behavior, architecture, privacy/security/data ownership, compatibility, release boundary, destructive behavior, or acceptance.

Plan transition:

- **Plan-only request** → NO IMPLEMENTATION → report → STOP.
- **User explicitly requested planning + implementation** → when all material decisions are resolved without a new user choice, state the transition and continue into the appropriate Developing path.
- If a new material user decision is required → STOP and ask for that decision; do not invent it.

Plan must never silently become Developing.

### Existing-system / Domain Execution

Using an existing system to create or revise its normal domain output is **not automatically Developing** merely because files or artifacts are created.

When the project already has a valid domain owner/procedure and no system behavior is being changed:

```text
current request + current project/domain state
→ matching domain owner/procedure
→ produce/revise requested output
→ matching domain acceptance
→ STOP
```

Do not invoke `development-brief` for normal production/authoring/execution when repository/system behavior is unchanged.

A project may later formalize a named mode such as `Production Execution`, `Asset Authoring`, or another domain-specific route only when a real repeatable workflow earns it. The Core Bootstrap does not pre-create that mode or its specialists.

If normal execution reveals a defect or requires changing how the system works, route the defect/change to Maintenance or Developing as appropriate.

### Developing

Developing has two execution paths.

#### Direct Bounded Path

Use when all material conditions are true:

- requested outcome is clear;
- current/first-wrong owner is obvious or cheaply discoverable;
- wider stable context cannot materially change the solution, or the relevant invariant is already known;
- no unresolved product/architecture/data/security decision exists;
- no new durable authority/runtime/compatibility/material dependency boundary/generic abstraction is required;
- blast radius is local and understandable;
- rollback is straightforward;
- targeted proof is obvious.

```text
pin repo/ref + inherit root safety rules
→ exact owner / exact defect
→ nearest caller/contract/test only when needed
→ smallest complete correction
→ targeted proof
→ update continuation only if it changed
→ STOP
```

Direct means fewer unnecessary decision hops, **not** less correctness or safety. It may skip `CONTEXT.md`, `next-action.md`, `development-brief`, broad tests, or specialist loading only when those surfaces cannot materially change the decision or proof.

#### Non-trivial Developing

Escalate when uncertainty, semantic impact, blast radius, risk, ownership coordination, migration, new persistent authority, material dependency change, hard rollback, or target/human acceptance can materially change implementation or acceptance.

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ .agents/skills/development-brief/SKILL.md
→ nearest relevant AGENTS.md when one exists and matters
→ smallest relevant owner/caller/contract set
→ zero/one useful specialist
→ coherent implementation
→ minimum honest proof
→ reconcile changed canonical state
→ STOP
```

`CONTEXT.md` and `docs/knowledge/next-action.md` are mandatory continuity for non-trivial Developing. The Direct Bounded Path remains the exception for work whose wider continuity cannot materially change correctness or proof.

`Non-trivial` is determined by impact/uncertainty/risk/coordination, not by code presence, file count, or line count.

### Maintenance

A concrete defect, regression, stale rule, or bounded cleanup should use the Direct Bounded Path by default when wider context cannot change the decision.

```text
exact defect
→ first wrong owner
→ smallest safe correction
→ targeted proof
→ STOP
```

If diagnosis exposes an unresolved product/architecture decision, leave Maintenance and return to Plan.

## Claim ownership and conflict resolution

Use the nearest authoritative owner for each claim type:

- current task intent/new explicit product decision → current user instruction;
- GitHub/ref/write/history/CI/security discipline → `GITHUB_RULES.md`;
- work mode/path/skill budget → root/nearest applicable `AGENTS.md`;
- stable project orientation → `CONTEXT.md`;
- durable intended behavior/non-goals → `docs/foundation/`;
- active continuation/status/boundary/blocker/one next step → `docs/knowledge/next-action.md`;
- actual behavior → current source + relevant proof;
- generated/derived output → upstream canonical source/generator;
- historical rationale → Git history unless a later justified decision owner exists.

Interpret conflicts instead of blindly applying a global priority list:

```text
current user decision vs foundation
→ reconcile the current durable policy owner

foundation vs current source
→ distinguish desired behavior from implementation state
→ inspect whether source is wrong or policy became stale

next-action vs current source/state
→ identify stale continuity vs stale implementation
→ reconcile the stale owner
→ continue from actual current truth

generated/derived output vs canonical source
→ canonical source/generator owns the correction

historical evidence/TODO/audit vs current owner
→ current owner wins unless the historical item is explicitly revalidated/promoted

material owner conflict cannot be responsibly resolved from current evidence
→ UNKNOWN
→ Plan / focused user decision when truly necessary
```

Never silently choose between contradictory current authorities merely to keep moving.

## Requirement and method discipline

The user owns intended outcome and high-impact product decisions. The agent owns repository discovery, owner discovery, implementation method quality, scope discipline, and evidence quality.

A suggested framework, sample, screenshot, reference repository, old branch, or technical method is not automatically the requirement. Evaluate a proposed method as:

```text
FOLLOW
REFINE
REDIRECT
STOP / DECISION REQUIRED
```

`No change required` is valid.

## Smallest coherent owner set

The invariant is **one canonical owner per responsibility**, not one owner per task.

A coherent change may legitimately require contract + implementation + regression assertion. Touch the smallest owner set needed for a complete outcome. Do not force one-file solutions that create workaround logic, stale contracts, duplicate authority, or synchronization debt.

## Anti-overdevelopment and anti-slop

Prefer the simplest complete route that preserves correctness.

Do not add a service, runtime, state authority, router, registry, provider layer, compatibility/fallback system, cache, queue, workflow, specialist, document owner, or abstraction merely for “best practice”, “clean architecture”, or future possibility.

For ordinary additions ask only:

```text
needed now?
correct existing responsibility?
simplest complete form?
```

For high-cost architectural additions, require a demonstrated current need and evidence that the new layer uniquely adds required capability or reduces total current complexity.

Do not broad-read, broad-test, create ceremonial reports, invent unknown requirements, or expand scope because adjacent opportunities are visible.

## Skill budget

- Direct Bounded Path → no specialist by default.
- Non-trivial Developing → mandatory `development-brief` + zero/one useful project specialist.
- Maintenance → zero/one specialist only when the diagnosed semantic boundary needs it.
- Plan / Context Recovery → no project specialist by default.
- Existing-system/domain execution → use only the project-defined domain procedure/specialist if one already exists and adds material value; do not route through `development-brief` by default.

A specialist is selected by recurring semantic responsibility, not programming language/framework name.

## Evidence boundary

Use the cheapest proof capable of falsifying the changed claim.

Repository/static evidence does not prove runtime/device/visual/model/target-machine/human acceptance. A one-line high-risk change may require more proof than a large low-risk internal refactor.

## Completion

When current scope and required proof are satisfied: STOP.

Do not automatically continue into adjacent cleanup, another audit, another verifier, another historical TODO, or the next milestone.

For material work, final reporting may use:

```text
Status: Selesai | Perlu pemeriksaan | Terhenti
Hasil:
Bukti:
Batasan:
Next step:
```

Use one meaningful next step only when continuation actually changed.
