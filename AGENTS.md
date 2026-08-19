# Agent Routing

This repository uses a general development kernel. Current repository/project sources are authority for repository state; chat history is supporting context only.

## Branch and safety authority

- `Local` is the working/development authority.
- Never silently fall back to another branch or repository default.
- Material GitHub execution follows `GITHUB_RULES.md`.
- Choose the **smallest sufficient path**. Efficiency must not remove context, contracts, safety, or proof that can change correctness.

## Current-source finalization — hard anti-AI-slop invariant

Current work has one current source per responsibility.

```text
change needed
→ find canonical owner
→ update that owner in place
→ update callers/contracts/tests that must change with it
→ remove superseded current path/state when safe
→ prove the final state
→ STOP
```

Do **not** solve evolution by accumulating alternatives.

Forbidden by default:

- `v1` / `v2` / `v3` governance or implementation generations;
- `_new`, `_old`, `_legacy`, `_backup`, `final2`, replacement-copy files/folders;
- duplicate services/controllers/configs/state stores for the same responsibility;
- parallel old/new runtime paths kept “just in case”;
- compatibility aliases, fallback bridges, adapters, migration layers, feature flags, or deprecated copies created only to avoid replacing the current source cleanly;
- permanent TODO/plan/status/completion/review files that duplicate a current owner;
- “temporary” repository structures that become persistent because cleanup was deferred;
- preserving obsolete source merely because it once existed.

Git history owns ordinary history. Do not keep historical code/docs alive inside current source just to preserve history.

A compatibility or migration boundary is allowed only when a **current external contract** proves it is required: persisted user data, a supported public API/protocol, deployed clients, an explicitly supported file/schema format, or another concrete compatibility obligation. Even then:

```text
name the external contract
→ keep the compatibility boundary minimal
→ define its owner and removal condition when removable
→ do not create a second product/runtime authority
```

Real externally defined API/schema/product versions are allowed when the product contract itself requires versioning. AI workflow evolution is not a reason to version canonical owners.

If the existing owner can be corrected directly, direct replacement is the default.

## Rule inheritance

Root `AGENTS.md` owns repository-wide invariants and task routing. A project may later add a nearer `AGENTS.md` only for a real package/domain responsibility.

When work is inside a subtree with a nearer `AGENTS.md`:

```text
root AGENTS.md
→ nearest relevant AGENTS.md
→ exact owner/source
```

- Read a nearer `AGENTS.md` only when its local rules can materially change the task.
- A nearer rule may narrow local/domain behavior; it must not weaken root branch/ref safety, current-source finalization, proof honesty, ownership integrity, or STOP boundaries.
- For local behavior, the nearest compatible rule applies.
- Directory existence alone is not a reason to create another `AGENTS.md`.

## Task class first

### Bootstrap Instantiation

Use this route when starting a new project from the starter before normal project development begins.

Use a **clean snapshot of the current starter tree in a new repository**. Do not carry the starter's Git history into the new project's history.

Establish `Local` as the working authority before normal project writes, unless the user explicitly requires another working-ref policy. If another policy is required, adapt the root branch rules as one coherent bootstrap decision before development begins.

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

Adapt only project-specific owners whose state must change:

```text
README.md
CONTEXT.md
docs/foundation/01-project-overview.md
docs/foundation/02-product-requirements.md
docs/knowledge/next-action.md
```

`AGENTS.md`, `GITHUB_RULES.md`, and `development-brief` are identity-neutral kernel owners. Change them during bootstrap only when the project has a real routing/authority/procedure difference.

Bootstrap rules:

- unknown project facts remain unknown;
- do not invent final architecture, source tree, database/API/release design, specialist inventory, compatibility matrix, future roadmap, or tests for nonexistent surfaces;
- remove/replace starter-specific project identity, audit/status state, and old continuation from current project truth;
- never create versioned starter generations or preserve old starter state beside the new project state;
- do not copy starter Git history/status as project requirements;
- finish with exactly one real project `Next Step`.

Bootstrap acceptance:

```text
project identity is the new project
stable context describes the new project
foundation describes current approved intent/requirements
next-action describes only current project continuation
generic kernel contains no project-specific starter leakage
no duplicate/legacy/versioned owner exists
unknowns remain explicit
```

After those conditions are true: report the bootstrap result and STOP. Bootstrap does not automatically start the first development objective unless the user also requested implementation.

### Context Recovery

For read-only `amati`, inspect, understand, audit, study, or context recovery:

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ smallest owner needed to explain current state
→ report
→ STOP
```

`CONTEXT.md` and `docs/knowledge/next-action.md` are mandatory continuity for Context Recovery. Do not edit, run CI, execute the recorded next step, or promote old TODO/history merely because it was discovered.

### Plan

Use when a material product, architecture, ownership, risk, or acceptance decision remains unresolved.

```text
recover current authority
→ recover repository/source facts that can answer the question
→ inspect smallest evidence that can change the decision
→ separate goal from suggested method
→ resolve/present only the remaining material decision
```

Before asking the user, recover facts current owners/source can answer. Ask only when an unresolved choice materially changes product behavior, architecture, privacy/security/data ownership, compatibility, release/destructive boundary, or acceptance.

Plan transition:

- Plan-only request → NO IMPLEMENTATION → report → STOP.
- Explicit plan + implementation request → if no material user decision remains, state the transition and continue into the appropriate Developing path.
- Material user decision still required → STOP and ask; do not invent it.

Plan must never silently become Developing.

### Existing-system / Domain Execution

Using an existing system to create or revise its normal domain output is **not automatically Developing** merely because files/artifacts are created.

```text
current request + current project/domain state
→ matching domain owner/procedure
→ produce/revise requested output
→ matching domain acceptance
→ STOP
```

Do not invoke `development-brief` when repository/system behavior is unchanged. A named Production/Authoring mode or specialist appears only when a real repeated workflow earns it.

If normal execution exposes a defect or requires changing how the system works, route that defect/change to Maintenance or Developing.

### Developing

#### Direct Bounded Path

Use when all material conditions are true:

- requested outcome is clear;
- first-wrong/current owner is obvious or cheaply discoverable;
- wider stable context cannot materially change the solution;
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
→ remove superseded current path/state when safe
→ targeted proof
→ update continuation only if it changed
→ STOP
```

Direct means fewer unnecessary decision hops, not less correctness or safety.

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
→ coherent final implementation
→ minimum honest proof
→ reconcile changed canonical state
→ STOP
```

`CONTEXT.md` and `next-action.md` are mandatory continuity here. `Non-trivial` is determined by impact/uncertainty/risk/coordination, not code/file/line count.

### Maintenance

A concrete defect, regression, stale rule, or behavior-preserving cleanup should use the Direct Bounded Path by default when wider context cannot change the decision.

```text
exact defect
→ first wrong owner
→ smallest safe correction
→ remove superseded stale path/state
→ targeted proof
→ STOP
```

If diagnosis exposes an unresolved product/architecture decision, return to Plan.

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
- historical rationale → Git history unless a justified current decision owner exists.

Conflict handling:

```text
current user decision vs foundation
→ reconcile current durable policy

foundation vs current source
→ desired behavior vs implementation state
→ identify which current owner is wrong/stale

next-action vs current source/state
→ stale continuity vs stale implementation
→ reconcile stale owner
→ continue from actual current state

generated artifact vs canonical source
→ fix canonical source/generator

historical evidence/TODO/audit vs current owner
→ current owner wins unless history is explicitly revalidated

material current conflict cannot be resolved responsibly
→ UNKNOWN
→ Plan / focused user decision
```

Never create a compatibility/legacy path merely to avoid reconciling conflicting current owners.

## Requirement and method discipline

The user owns intended outcome and high-impact product decisions. The agent owns repository discovery, owner discovery, implementation detail/method quality, scope discipline, and evidence quality.

Treat frameworks, samples, screenshots, old branches/source, reports, and technical suggestions as evidence/method proposals unless current requirements explicitly adopt them.

Evaluate a proposed method as:

```text
FOLLOW
REFINE
REDIRECT
STOP / DECISION REQUIRED
```

Redirect methods that create duplicate ownership/runtime, preserve obsolete paths without a current contract, repeat disproven work, inflate proof, or add disproportionate abstraction/compatibility/fallback.

`No change required` is valid.

## Root-cause and edit gate

Before a non-trivial behavior edit establish:

1. what happens now;
2. who owns it;
3. why it is wrong/incomplete;
4. why the proposed final change addresses that cause;
5. what proof can falsify the result.

Before creating any persistent file/module/owner/layer, establish why the current canonical owner cannot represent the responsibility and why the addition is required **now**.

Do not hide unknown causes with blind retry, arbitrary delay, broad fallback, compatibility aliases, duplicate state, parallel services, or generic frameworks.

If the same correction direction fails twice without materially new evidence, stop that direction and reassess.

## Minimum complete solution

Every material file, dependency, abstraction, config, compatibility boundary, cache, state, workflow, or persistent side effect must trace to the current goal, acceptance criterion, required contract, proved cause, or required proof.

The final solution replaces superseded current behavior rather than accumulating generations around it.

Do not add unrelated cleanup, speculative future architecture, duplicate owners, placeholder success, ceremonial tests, broad hardening, framework work, versioned rewrites, or “temporary” compatibility paths by default.

## Skill budget

- Direct Bounded Path → no specialist by default.
- Non-trivial Developing → mandatory `development-brief` + zero/one useful project specialist.
- Maintenance → zero/one specialist only when the diagnosed semantic boundary needs it.
- Plan / Context Recovery → no project specialist by default.
- Existing-system/domain execution → use only an already-earned project domain procedure/specialist when it adds material value.

Choose specialists by recurring semantic responsibility, not programming language/framework/library names.

## Evidence boundary

Use the cheapest proof capable of falsifying the changed claim.

Repository/static/hosted evidence proves only what it actually exercises. It does not prove runtime/device/visual/audio/model/target-machine/human acceptance without matching execution.

## Completion

When current scope and required proof are satisfied: STOP.

Do not automatically continue into adjacent cleanup, another audit, another verifier, another historical TODO, another versioned rewrite, or the next milestone.

For material work, final reporting may use:

```text
Status: Selesai | Perlu pemeriksaan | Terhenti
Hasil:
Bukti:
Batasan:
Next step:
```

Use exactly one meaningful next step when continuation actually changed. Do not create per-task completion reports/worklogs.
