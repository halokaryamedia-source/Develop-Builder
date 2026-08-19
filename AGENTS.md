# Agent Routing

This repository uses a general project-definition and development kernel. Current repository/project sources are authority for repository state; chat history is supporting context only.

## Branch and safety authority

- `Local` is the working/development authority.
- Never silently fall back to another branch or repository default.
- Material GitHub execution follows `GITHUB_RULES.md`.
- Documentation architecture and Project Definition readiness follow `docs/README.md`.
- Choose the **smallest sufficient path**. Efficiency must not remove project definition, context, contracts, safety, or proof that can change correctness.

## Documentation authority

Before creating, splitting, or deleting durable project documentation, use `docs/README.md`.

Canonical separation:

```text
project/product durable truth
→ docs/foundation/

current repository navigation + current development context
→ docs/knowledge/

stable cross-session projection
→ CONTEXT.md

reusable AI judgment/procedure
→ .agents/skills/

actual implementation behavior
→ current source + matching proof
```

`docs/knowledge/` is a navigation/current-development-context layer, **not a generic project-management archive**. Historical rationale, completed reviews, inactive plans, meeting notes, and arbitrary backlog do not belong there unless a distinct current-navigation responsibility requires them and no simpler current owner exists.

Do not invent a documentation structure from file-count aesthetics. A simple project may need only Overview + Requirements; a complex project must add the durable owners or current-navigation owners its real responsibilities require.

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

- version-suffixed governance/implementation owner generations;
- old/new/legacy/backup replacement copies;
- duplicate services/controllers/configs/state stores for the same responsibility;
- parallel old/new runtime paths kept “just in case”;
- compatibility aliases, fallback bridges, adapters, migration layers, feature flags, or deprecated copies created only to avoid replacing current source cleanly;
- permanent TODO/plan/status/completion/review files that duplicate a current owner;
- temporary repository structures that persist because cleanup was deferred;
- preserving obsolete source merely because it once existed.

Git history owns ordinary history.

A compatibility or migration boundary is allowed only when a **current external contract** proves coexistence is required: persisted user data, supported public API/protocol, deployed clients, explicitly supported file/schema format, or another concrete compatibility obligation. Keep it minimal and never create a second product/runtime authority.

## Rule inheritance

Root `AGENTS.md` owns repository-wide invariants and task routing. A project may add a nearer `AGENTS.md` only for a real package/domain responsibility.

```text
root AGENTS.md
→ nearest relevant AGENTS.md
→ exact owner/source
```

- Read a nearer `AGENTS.md` only when its local rules can materially change the task.
- A nearer rule may narrow local/domain behavior; it must not weaken branch/ref safety, documentation readiness, current-source finalization, proof honesty, ownership integrity, or STOP boundaries.
- Directory existence alone is not a reason to create another `AGENTS.md`.

# Task class first

## Bootstrap Instantiation

Use when starting a new project from the starter before normal project development begins.

Use a **clean snapshot of the current starter tree in a new repository**. Do not carry starter Git history into the new project's history.

Establish `Local` as working authority before normal project writes unless the user explicitly requires another policy. If another working-ref policy is required, adapt the root branch rules as one coherent bootstrap decision before development begins.

Then run Project Definition, not immediate product implementation:

```text
read docs/README.md
→ recover current user intent + approved decisions + authoritative sources
→ complete 01-project-overview.md
→ complete 02-product-requirements.md
→ apply Foundation Expansion Gate
→ create only earned durable foundation owners
→ Documentation Readiness review
→ derive/reconcile README.md + CONTEXT.md
→ write next-action.md with one real step or blocker
→ PROJECT DEFINITION READY
→ report → STOP
```

Project-specific owners normally rewritten during bootstrap:

```text
README.md
CONTEXT.md
docs/foundation/01-project-overview.md
docs/foundation/02-product-requirements.md
docs/knowledge/next-action.md
+ only foundation/knowledge owners earned by the real project
```

Generic kernel owners normally retained:

```text
AGENTS.md
GITHUB_RULES.md
docs/README.md
.agents/skills/development-brief/SKILL.md
```

Change generic kernel owners during bootstrap only when the new project has a real routing/authority/procedure difference.

Bootstrap rules:

- unknown project facts remain unknown;
- remove scaffold guidance from project-specific foundation owners before declaring readiness;
- do not invent architecture, source tree, database/API/release design, specialist inventory, compatibility matrix, roadmap, or test matrix merely to fill documentation;
- do not preserve starter identity/status beside the new project state;
- do not create empty future docs;
- Knowledge growth must pass the `docs/README.md` Knowledge Navigation Gate; do not create generic archive/project-management files during bootstrap;
- finish with exactly one real current `Next Step` or blocker.

Bootstrap does not automatically start the first implementation objective unless the user also requested implementation **and** Documentation Readiness passes.

## Project Definition — pre-development phase

Project Definition is a bounded pre-development phase, **not another permanent work mode**.

Use it when:

- bootstrapping a new project;
- a materially new product/domain is entering scope and lacks durable contracts;
- Developing discovers that required product flow, boundary, source authority, architecture, quality, or acceptance meaning is undefined.

Route:

```text
current intent + approved decisions + authoritative sources
→ recover what is already known
→ update Overview / Requirements
→ apply docs/README.md Foundation Expansion Gate
→ resolve only high-impact blockers
→ Documentation Readiness review
→ update CONTEXT only as a projection of stable truth
→ set one next-action
→ STOP or explicitly transition to Developing when already authorized
```

Project Definition may edit project documentation. It does **not** implement undefined product behavior.

A bounded discovery/prototype is allowed before readiness only when it is the minimum evidence needed to resolve a material unknown. It must return evidence to the correct foundation owner before normal implementation continues.

## Context Recovery

For read-only `amati`, inspect, understand, audit, study, or context recovery:

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ smallest current navigation/owner source needed to explain state
→ report
→ STOP
```

Do not broad-read every Knowledge owner. Open an earned Knowledge file only when it can materially change understanding of the active repository context.

Do not edit, run CI, execute the recorded next step, or promote old TODO/history merely because it was discovered.

## Plan

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
- Explicit plan + implementation request → if no material user decision remains, ensure affected Project Definition is sufficient, state the transition, then enter the appropriate Developing path.
- Material user decision still required → STOP and ask; do not invent it.

Plan must never silently become Developing.

## Existing-system / Domain Execution

Using an existing system to create or revise its normal domain output is **not automatically Developing** merely because files/artifacts are created.

```text
current request + current project/domain state
→ matching domain owner/procedure
→ produce/revise requested output
→ matching domain acceptance
→ STOP
```

A domain execution route/procedure must already have an earned current owner. If the required domain workflow/quality/acceptance contract does not exist and can materially change output, return to Project Definition instead of improvising it inside production work.

Do not invoke `development-brief` when repository/system behavior is unchanged.

## Developing

### Direct Bounded Path

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

Direct means fewer unnecessary decision hops, not less correctness or safety. It is not a bypass for undefined new product behavior.

### Non-trivial Developing

Escalate when uncertainty, semantic impact, blast radius, risk, ownership coordination, migration, new persistent authority, material dependency change, hard rollback, or target/human acceptance can materially change implementation or acceptance.

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ .agents/skills/development-brief/SKILL.md
→ Project Definition Gate for affected contract
→ nearest relevant AGENTS.md when one exists and matters
→ smallest relevant foundation / current Knowledge navigation / source / caller / contract set
→ zero/one useful specialist
→ coherent final implementation
→ minimum honest proof
→ reconcile changed canonical state
→ STOP
```

If the Project Definition Gate fails, leave implementation and return to Plan / Project Definition.

Open Knowledge only for current navigation/context needed to locate or understand the affected owners; Knowledge does not replace Foundation requirements or source inspection.

`Non-trivial` is determined by impact/uncertainty/risk/coordination, not code/file/line count.

## Maintenance

A concrete defect, regression, stale rule, or behavior-preserving cleanup should use the Direct Bounded Path by default when wider project definition cannot change the decision.

```text
exact defect
→ first wrong owner
→ smallest safe correction
→ remove superseded stale path/state
→ targeted proof
→ STOP
```

If diagnosis exposes an unresolved product/architecture decision, return to Plan / Project Definition.

# Claim ownership and conflict resolution

Use the nearest authoritative owner for each claim type:

- current task intent/new explicit product decision → current user instruction;
- GitHub/ref/write/history/CI/security discipline → `GITHUB_RULES.md`;
- documentation architecture / doc creation thresholds → `docs/README.md`;
- work mode/path/skill budget → root/nearest applicable `AGENTS.md`;
- stable project orientation → `CONTEXT.md`;
- durable product/project behavior/non-goals → `docs/foundation/`;
- current development navigation/context → earned `docs/knowledge/` owner;
- active continuation/status/boundary/blocker/one next step → `docs/knowledge/next-action.md`;
- actual behavior → current source + relevant proof;
- generated/derived output → upstream canonical source/generator;
- ordinary historical rationale/completed work → Git history/issues/PRs unless a current owner explicitly needs bounded context from it.

Conflict handling:

```text
current user decision vs foundation
→ reconcile current durable policy

foundation vs current source
→ desired behavior vs implementation state
→ identify which current owner is wrong/stale

knowledge navigation vs source
→ navigation may be stale
→ verify current source owner
→ update/remove stale navigation

next-action vs current source/state
→ stale continuation vs stale implementation
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

# Requirement and method discipline

The user owns intended outcome and high-impact product decisions. The agent owns repository discovery, owner discovery, implementation detail/method quality, scope discipline, and evidence quality.

Treat frameworks, samples, screenshots, old branches/source, reports, and technical suggestions as evidence/method proposals unless current requirements explicitly adopt them.

Evaluate a proposed method as:

```text
FOLLOW
REFINE
REDIRECT
STOP / DECISION REQUIRED
```

`No change required` is valid.

# Root-cause, documentation, and edit gates

Before a non-trivial behavior edit establish:

1. what happens now;
2. who owns it;
3. why it is wrong/incomplete;
4. why the proposed final change addresses that cause;
5. what proof can falsify the result.

Before creating any persistent file/module/owner/layer:

```text
what distinct live responsibility needs an owner?
why cannot an existing owner represent it cleanly?
who consumes it now?
what error/decision/acceptance/navigation problem does it solve?
```

For documentation specifically, follow `docs/README.md` Foundation Expansion Gate or Knowledge Navigation Gate as applicable.

Do not hide unknown causes with blind retry, arbitrary delay, broad fallback, compatibility aliases, duplicate state, parallel services, or generic frameworks.

If the same correction direction fails twice without materially new evidence, stop that direction and reassess.

# Minimum complete solution

Every material file, dependency, abstraction, config, compatibility boundary, cache, state, workflow, document, or persistent side effect must trace to the current goal, acceptance criterion, required contract, proved cause, required proof, or real current-navigation need.

The final solution replaces superseded current behavior rather than accumulating generations around it.

Do not add unrelated cleanup, speculative future architecture, duplicate owners, placeholder success, ceremonial tests, broad hardening, framework work, versioned rewrites, empty documentation scaffolds beyond the starter's two required Project Definition owners, generic Knowledge archives, or temporary compatibility paths by default.

# Skill budget

- Direct Bounded Path → no specialist by default.
- Non-trivial Developing → mandatory `development-brief` + zero/one useful project specialist.
- Maintenance → zero/one specialist only when the diagnosed semantic boundary needs it.
- Plan / Context Recovery / Project Definition → no specialist by default.
- Existing-system/domain execution → use only an already-earned project domain procedure/specialist when it adds material value.

Choose specialists by recurring semantic responsibility, not programming language/framework/library names.

Project facts/requirements belong in foundation/project owners, not skills.

# Evidence boundary

Use the cheapest proof capable of falsifying the changed claim.

Repository/static/hosted evidence proves only what it actually exercises. It does not prove runtime/device/visual/audio/model/target-machine/human acceptance without matching execution.

# Completion

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
