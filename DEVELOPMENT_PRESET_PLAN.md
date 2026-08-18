# Develop-Builder — General Development Preset Plan

Status: **PLAN ONLY — NOT IMPLEMENTED**  
Working authority: **`Local`**  
Reference repositories: **BuildIT / TranslateIT / PRD-Creator (`Local`)**

## 1. Purpose

Develop-Builder will become the **general bootstrap preset used before developing a new project/system**.

The goal is not to copy one existing repository's product structure. The goal is to preserve the same **development operating model 1:1 at the semantic level**, then adapt only the domain-specific owners, proof surfaces, production/runtime structure, and specialists required by the new context.

The preset must prevent a new repository from starting as an unstructured code dump, while also avoiding speculative architecture, empty framework layers, duplicate documentation owners, and generic AI-generated ceremony.

## 2. What the three reference repositories prove

BuildIT, TranslateIT, and PRD-Creator differ materially in product domain, runtime, production flow, source layout, validation, workspace needs, and specialist skills.

They nevertheless share one development kernel:

```text
PIN CURRENT AUTHORITY
→ SELECT WORK MODE
→ RECOVER MINIMUM SUFFICIENT CONTEXT
→ FIND THE FIRST WRONG / RESPONSIBLE OWNER
→ GROUND GOAL VS SUGGESTED METHOD
→ DEFINE MINIMUM COMPLETE SCOPE
→ IMPLEMENT THROUGH ONE CANONICAL OWNER
→ VERIFY ONLY THE CLAIM THAT CHANGED
→ UPDATE ONLY CHANGED CANONICAL STATE
→ EXACTLY ONE NEXT STEP
→ STOP
```

This kernel is the part Develop-Builder must preserve.

## 3. Core invariants that must be 1:1

### 3.1 Branch and authority discipline

Every instantiated repository must explicitly define its working authority.

Default preset policy:

```text
Local = current working/development authority
other branches = historical/recovery/release authority only when explicitly defined
no silent fallback to repository default branch
```

Branch policy must be explicit in both agent routing and GitHub execution rules.

### 3.2 Work mode must be selected before editing

The baseline modes are:

```text
Context Recovery
Plan
Developing
Maintenance
```

A domain may add another real mode such as `Production Execution`, but only when the product actually has a repeatable production workflow distinct from developing the system itself.

No silent transition between modes.

### 3.3 Read-only observation remains read-only

Requests such as:

```text
amati
inspect
understand
study
audit
recover context
```

must recover the smallest current authority needed, report the result, then stop.

Observation must not automatically execute `next-action`, run CI, edit repository state, activate experiments, or promote old TODO/backlog/history into active work.

### 3.4 Cross-session continuity is mandatory

Non-trivial Developing must survive a new chat/session without asking the user to reconstruct prior work.

Canonical bootstrap:

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ development-brief
→ smallest relevant owner/source
```

If continuity prose disagrees with current source/state, inspect the exact current owner and reconcile the stale record before continuing.

### 3.5 One canonical owner per responsibility

The preset must enforce ownership separation:

```text
routing / work mode          → AGENTS.md
GitHub execution             → GITHUB_RULES.md
stable orientation           → CONTEXT.md
durable product policy       → docs/foundation/
active continuation          → docs/knowledge/next-action.md
responsibility/source map    → one ownership map
non-trivial development gate → development-brief
actual behavior              → current source + relevant proof
```

Do not create parallel roadmap, status, session-memory, review-state, plan, TODO, ownership, or routing systems that duplicate an existing owner.

### 3.6 Development Brief is the mandatory Developing front door

Every non-trivial Developing task must first establish the smallest grounded development contract.

Required semantic fields, only when material:

```text
Goal
Suggested method / observed reference (if any)
Actual requirement
Input authority
Expected output
Build POV
Acceptance POV
In scope / Out of scope
Acceptance criteria: 2–5
Proof budget
Open high-impact decisions
Execution channel only when it changes implementation/proof
```

Rules:

- user-suggested method is not automatically the requirement;
- inspect current behavior before deciding development is required;
- `No change required` is valid;
- ask the user only for genuinely unresolved high-impact decisions that repository/source recovery cannot resolve;
- use at most one specialist in a bounded Developing slice unless the task is explicitly reframed.

### 3.7 Minimum complete solution

Every persistent addition must earn its place.

A file, dependency, abstraction, workflow, config, compatibility layer, fallback, cache, state store, specialist, or persistent side effect is allowed only when it maps to:

- current goal;
- acceptance criterion;
- required interface/contract;
- proved root cause;
- or required proof.

Default counts for speculative additions are zero.

### 3.8 Proof must match the claim

The template must preserve the distinction between:

```text
repository/source/static proof
hosted CI proof
local/runtime proof
device/hardware proof
visual/human acceptance
production/user-environment proof
```

A cheaper proof may be used when it can falsify the changed claim. It must never be described as proving a stronger surface that did not run.

### 3.9 GitHub work follows the same seven-stage discipline

Canonical GitHub kernel:

```text
PIN
→ READ MINIMUM
→ DIAGNOSE
→ TOOL FIT
→ WRITE ONCE
→ VERIFY MINIMUM
→ STOP
```

Commit history represents logical outcomes, not reasoning checkpoints, CI triggers, tool calls, or save points.

### 3.10 Completion is terminal

When current scope and required proof are satisfied, stop.

Do not automatically continue into adjacent cleanup, another audit, another verifier, another historical TODO, the next milestone, or another framework layer.

## 4. Mandatory baseline repository preset

The initial Develop-Builder implementation should create only the following **general kernel**.

```text
/
├─ README.md
├─ AGENTS.md
├─ GITHUB_RULES.md
├─ CONTEXT.md
├─ .agents/
│  └─ skills/
│     └─ development-brief/
│        └─ SKILL.md
├─ docs/
│  ├─ foundation/
│  │  ├─ 01-project-overview.md
│  │  └─ 02-product-requirements.md
│  └─ knowledge/
│     ├─ work-routing.md
│     ├─ ownership.md
│     └─ next-action.md
├─ tools/
│  └─ verify_repository.py
└─ .github/
   └─ workflows/
      └─ repository-verify.yml
```

This is a semantic preset, not a requirement that every future repository keep every filename forever. A context may rename/extend an owner when a clearer domain-specific representation is justified, but the responsibility itself must remain singular and explicit.

## 5. Responsibilities of the baseline files

### `README.md`

Human-facing orientation only:

- what the project is;
- current high-level status;
- development authority;
- major product/runtime/production roots once known;
- navigation to canonical owners;
- proof boundary at a useful high level.

README must not become the detailed routing owner or active session log.

### `AGENTS.md`

Canonical work-routing owner:

- branch authority;
- smallest sufficient boot;
- Context Recovery / Plan / Developing / Maintenance boundaries;
- optional product-specific work mode when justified;
- source precedence;
- canonical state owners;
- skill budget;
- execution/proof boundary;
- STOP behavior.

### `GITHUB_RULES.md`

Canonical repository-execution owner:

- PIN;
- READ MINIMUM;
- DIAGNOSE;
- TOOL FIT;
- WRITE ONCE;
- VERIFY MINIMUM;
- STOP;
- commit/history discipline;
- API failure behavior;
- pagination/partial evidence;
- CI and hosted-proof boundaries;
- special files/binaries/generated artifacts;
- PR/branch-protection/release/security conditional surfaces;
- retry budgets and destructive-operation boundaries.

Domain rules may narrow this policy, never weaken it.

### `CONTEXT.md`

Stable orientation only:

- product/system purpose;
- stable terminology;
- approved major architecture/boundaries;
- repository shape;
- stable evidence boundary;
- navigation to detailed owners.

Active continuation and temporary milestones do not belong here.

### `docs/foundation/01-project-overview.md`

Durable project/product intent and scope boundary.

It answers what is being built and for whom, without becoming implementation history.

### `docs/foundation/02-product-requirements.md`

Durable current requirements and non-goals.

It owns intended behavior/policy, not actual implementation status.

Additional foundation files are created only when a real durable responsibility appears.

### `docs/knowledge/work-routing.md`

Detailed routing reference used only when the route needs more explanation than root `AGENTS.md`.

It must not become a duplicate top-level routing authority.

### `docs/knowledge/ownership.md`

Responsibility → canonical current owner map.

It contains ownership/navigation, not active milestone/status tracking.

A project may later rename this to a more precise domain term such as `source-ownership.md` or `implementation-map.md` when justified.

### `docs/knowledge/next-action.md`

Single active continuation owner.

Minimum required shape:

```text
## Current Status
## Active Boundary
## Proof Boundary        # only when material
## Blocker               # only when material
## Next Step             # exactly one
```

It must not become a backlog or multi-quarter roadmap.

### `.agents/skills/development-brief/SKILL.md`

General non-trivial Developing front door.

It stays semantic and small. It routes to at most one project specialist after ownership is understood.

### `tools/verify_repository.py`

Static governance verifier for the preset.

The generic verifier should check only reusable repository invariants, for example:

- required kernel owners exist;
- `Local` authority is explicit;
- work modes remain present;
- `development-brief` remains the Developing front door;
- exactly one `## Next Step` exists;
- ownership map does not become a status owner;
- duplicate/retired routing owners are absent when recorded;
- relative governance links resolve;
- governance files stay within reasonable size budgets;
- temporary one-use verification workflows are absent;
- repository verification remains read-only.

It must not contain BuildIT, TranslateIT, PRD-Creator, Minecraft, Windows audio, PRD, model, UI, or other domain assertions.

### `.github/workflows/repository-verify.yml`

Read-only, path-scoped static governance verification.

Default behavior:

```text
push to Local on governance-path changes
pull request to explicitly supported refs
manual dispatch
read-only contents permission
concurrency cancel-in-progress
run tools/verify_repository.py
```

The generic workflow proves repository/governance contracts only. Product/runtime verification is added separately when the new project proves a need.

## 6. What must NOT be included in the base preset

The following are **not** universal and must default to absent:

```text
specialist skills beyond development-brief
runtime/application source folders
workspace/active or archive systems
Experimental/
backlog system
decision log / decision directory
review archive
validation report
local-acceptance runbook
release workflow
product-specific CI
browser/UI/audio/model/device test layers
compatibility framework
fallback/router/provider framework
generic registry/profile system
production kit/package hierarchy
```

They may be added only when the new context demonstrates a durable owner that cannot be represented correctly by the baseline kernel.

## 7. Domain adaptation contract

When Develop-Builder is used to start a new repository, adaptation should happen in this order.

### Step A — Define project truth

Fill:

- project name and purpose;
- intended users/consumers;
- approved scope and explicit non-goals;
- current development authority;
- execution environment only when material;
- first proof boundary.

### Step B — Define semantic ownership

Identify actual responsibilities before choosing folders, frameworks, languages, or specialist names.

Examples of semantic owner questions:

```text
Who owns application/session truth?
Who owns data/state persistence?
Who owns generation/production semantics?
Who owns UI presentation?
Who owns external/device/runtime integration?
Who owns release/distribution?
Who determines acceptance?
```

Only responsibilities that currently exist receive owners.

### Step C — Freeze the first foundation

Write the minimum stable overview + requirements needed to prevent wrong implementation.

Unknowns remain unknown. Do not invent complete architecture merely because development is about to start.

### Step D — Define first continuation

`next-action.md` records the first real bounded development objective and one next step.

### Step E — Add specialists only after responsibility is stable

A specialist exists only when repeated semantic procedure is valuable enough that `development-brief` alone is insufficient.

Specialist selection is by responsibility, never by language/framework name alone.

### Step F — Add product verification only after product surfaces exist

Repository governance verification is baseline.

Runtime/build/UI/device/model/release verification is created when there is an actual changed claim to protect.

## 8. Implementation phases for Develop-Builder

### Phase 0 — Reference audit and plan freeze

**Status: current phase.**

- compare BuildIT / TranslateIT / PRD-Creator on `Local`;
- isolate invariant operating model from domain structure;
- define baseline vs optional surfaces;
- freeze this plan;
- no preset implementation yet.

### Phase 1 — Core governance kernel

Create domain-neutral:

```text
AGENTS.md
GITHUB_RULES.md
CONTEXT.md
README.md
```

Acceptance focus: authority, work modes, source precedence, canonical ownership, minimum-read discipline, evidence boundaries, STOP.

### Phase 2 — Foundation + continuity kernel

Create:

```text
docs/foundation/01-project-overview.md
docs/foundation/02-product-requirements.md
docs/knowledge/work-routing.md
docs/knowledge/ownership.md
docs/knowledge/next-action.md
```

Files must contain useful bootstrap contracts/instructions, not fake product facts.

### Phase 3 — Development front door

Create:

```text
.agents/skills/development-brief/SKILL.md
```

It must preserve the shared development contract and remain domain-neutral.

Do **not** create placeholder specialists.

### Phase 4 — Static governance verification

Create:

```text
tools/verify_repository.py
.github/workflows/repository-verify.yml
```

The gate validates only baseline repository invariants and must be read-only.

### Phase 5 — Bootstrap usability audit

Simulate at least three materially different hypothetical repository types against the preset, for example:

```text
desktop/runtime application
content/production system
creative/tooling/plugin system
```

The audit should prove the kernel is reusable without leaking assumptions from any reference repository.

Do not add architecture to make the simulation richer. Use the simulation only to find invalid generic assumptions.

### Phase 6 — Freeze preset v1

When the kernel passes its own governance verification and usability audit:

- mark preset baseline version;
- update `next-action.md` to the next real Develop-Builder objective or stable idle state;
- stop.

## 9. Acceptance criteria for preset v1

Preset v1 is acceptable only when all of the following are true:

1. **Semantic parity:** the core Developing lifecycle matches the reference repositories: continuity recovery → development-brief → smallest canonical owner → 2–5 criteria/proof budget → minimum complete implementation → minimum honest proof → one next step → STOP.
2. **Domain neutrality:** no BuildIT, TranslateIT, PRD-Creator, Minecraft, Blockbench, translation, Windows audio, PRD, Voice, renderer, or other reference-product assumption is required by the generic kernel.
3. **Anti-overdevelopment:** optional surfaces are absent by default and the preset explicitly requires proof before creating new skills, frameworks, workflows, state owners, compatibility layers, or persistent systems.
4. **Cross-session recoverability:** a fresh agent can recover current project authority and active continuation from the canonical bootstrap without relying on chat history.
5. **Mechanical drift protection:** the generic repository verifier detects missing core owners, duplicate routing/state patterns covered by the preset, malformed active continuation, unsafe repository-verification workflow behavior, and broken governance links.

## 10. Protected non-goals

This project is **not** intended to become:

- a universal application framework;
- a monorepo starter with every possible stack;
- a collection of pre-made language/framework specialists;
- an autonomous roadmap generator;
- an automatic branch/PR/release manager;
- an exhaustive documentation system;
- a mandatory migration target for existing repositories;
- a mechanism that forces every project to use the same runtime architecture.

The preset standardizes **how development is reasoned, owned, continued, changed, verified, and stopped**. It does not standardize what every product must be.

## 11. Next Step

**After this plan is accepted, implement Phases 1–4 as one coherent domain-neutral preset delivery on `Local`, then run Phase 5 as a bounded usability audit before declaring preset v1.**
