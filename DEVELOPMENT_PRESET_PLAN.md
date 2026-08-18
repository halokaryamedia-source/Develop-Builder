# Develop-Builder — General Development Preset Plan

Status: **PLAN ONLY — NOT IMPLEMENTED**  
Working authority: **`Local`**  
Plan maturity: **architecture/specification freeze candidate**  
Reference repositories: **BuildIT / TranslateIT / PRD-Creator (`Local`)**

> This file is the implementation plan for **Develop-Builder itself**. It is **not** a file that should automatically be copied into every instantiated project.

---

## 1. Objective

Develop-Builder will provide the **smallest general development operating preset that must exist before non-trivial project development begins**.

The preset standardizes **how development is understood, owned, continued, changed, verified, and stopped**. It does **not** standardize product architecture, programming language, framework, runtime, content workflow, release model, or domain-specific folder structure.

The target is semantic parity with the mature operating model demonstrated by BuildIT, TranslateIT, and PRD-Creator while removing product-specific assumptions and refusing structures that have not yet earned a real responsibility.

The preset must solve five recurring failure classes:

1. **context loss** — a new AI/session should not need the user to reconstruct prior work;
2. **authority drift** — old chat, old TODO, generated artifact, or default branch must not silently become current truth;
3. **AI-slop** — development must not create duplicate docs, generic frameworks, ceremonial layers, speculative abstractions, or fake proof;
4. **overdevelopment** — adjacent opportunities must not expand the requested boundary;
5. **proof inflation** — source/build/CI success must not be described as runtime, visual, hardware, target-machine, or human acceptance when that surface did not run.

Success means a fresh project can start with a disciplined development kernel **without inheriting irrelevant architecture from another project**.

---

## 2. What is actually common across the three reference repositories

BuildIT, TranslateIT, and PRD-Creator have different products and different mature repository shapes. Their reusable commonality is not their domain folders; it is their **operating kernel**:

```text
PIN CURRENT AUTHORITY
→ CLASSIFY THE WORK MODE
→ RECOVER MINIMUM SUFFICIENT CURRENT CONTEXT
→ IDENTIFY THE RESPONSIBLE / FIRST WRONG OWNER
→ SEPARATE GOAL FROM SUGGESTED METHOD
→ DECIDE WHETHER DEVELOPMENT IS NEEDED AT ALL
→ DEFINE THE MINIMUM COMPLETE CHANGE
→ DEFINE 2–5 FALSIFIABLE ACCEPTANCE CRITERIA
→ CHOOSE THE CHEAPEST PROOF THAT CAN FALSIFY THE CLAIM
→ CHANGE ONE CANONICAL OWNER
→ UPDATE ONLY STATE THAT ACTUALLY CHANGED
→ RECORD EXACTLY ONE NEXT STEP
→ STOP
```

This lifecycle is the **1:1 behavior** that Develop-Builder must preserve.

The following mature-repository surfaces are **not** automatically part of that kernel:

```text
product runtime folders
production kits
workspace/archive systems
experimental research areas
decision logs
review archives
backlogs
local acceptance runbooks
release systems
product-specific CI
specialist skills beyond development-brief
```

They appear only when the project proves they are needed.

---

## 3. Design doctrine

### 3.1 Minimum sufficient context, not minimum context

The preset must minimize reading **after** mandatory continuity has been recovered. It must never optimize token usage by skipping the context that prevents wrong work.

For non-trivial Developing:

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ development-brief
→ smallest relevant owner/source
```

After that bootstrap, additional reading is evidence-driven and bounded.

### 3.2 One information type → one canonical owner

Every persistent fact or rule has one current owner. Other files may link to it, but must not independently maintain the same state.

### 3.3 Desired behavior and actual behavior are different claims

```text
desired product/system behavior
→ foundation / current approved requirement owner

actual implemented behavior
→ current source + matching proof

active continuation
→ next-action.md

stable orientation
→ CONTEXT.md

historical rationale
→ Git history / explicit decision record when justified
```

No global “one file outranks everything” rule should be used for all claim types.

### 3.4 A proposed implementation is not automatically the requirement

User examples, screenshots, sample repositories, old source, technical suggestions, and fixtures are evidence or suggested methods unless the user explicitly makes the exact implementation a requirement.

The development process must first recover the underlying outcome.

### 3.5 `No change required` is a valid successful result

An AI must not create a patch merely because the user asked it to investigate or because a tool is available.

### 3.6 Completion is terminal

When the requested acceptance boundary is satisfied, the correct behavior is `STOP`, not “continue improving”.

---

## 4. Baseline work modes

The base preset owns four modes.

| Mode | Use when | Editing | Required behavior |
|---|---|---:|---|
| **Context Recovery** | inspect, amati, understand, audit current state | No | recover authority → smallest owner → report → STOP |
| **Plan** | goal known but method/architecture/scope remains materially unresolved | No product implementation | inspect evidence → resolve decision → plan → STOP |
| **Developing** | create/change approved product or repository behavior | Yes | continuity → development-brief → minimum complete change → proof → STOP |
| **Maintenance** | concrete bug, regression, stale rule, bounded cleanup | Yes | exact defect → first wrong owner → smallest repair → targeted proof → STOP |

A project may add a fifth domain mode such as `Production Execution` **only when a real repeatable production workflow exists that is semantically different from changing the system itself**.

### No silent transitions

Examples:

```text
Context Recovery → discovers next-action
≠ permission to execute next-action

Plan → produces architecture decision
≠ permission to implement it

Maintenance → reveals unresolved product choice
→ leave Maintenance and return to Plan
```

---

## 5. Canonical claim ownership model

The preset should teach the AI to route by **claim type**, not by filename or framework.

| Claim / responsibility | Canonical owner |
|---|---|
| task intent / new explicit user decision | current user instruction |
| GitHub/ref/write/commit/CI/security discipline | `GITHUB_RULES.md` |
| agent boot / work mode / routing / skill budget | `AGENTS.md` |
| stable project orientation / terminology / architecture boundary | `CONTEXT.md` |
| durable intended requirements / non-goals | `docs/foundation/` |
| active current status / boundary / blocker / one next step | `docs/knowledge/next-action.md` |
| responsibility → source/owner navigation | `docs/knowledge/ownership.md` |
| non-trivial development contract | `.agents/skills/development-brief/SKILL.md` |
| actual behavior | current implementation/source + relevant runtime/static proof |
| generated/derived output | upstream canonical source + generator |
| historical rationale | Git history; explicit decision owner only when the decision-recording gate is met |

This matrix is intentionally small. New canonical state types are not created until a real responsibility appears.

---

## 6. Mandatory baseline preset

The v1 baseline should contain only this kernel:

```text
/
├─ README.md
├─ AGENTS.md
├─ GITHUB_RULES.md
├─ CONTEXT.md
├─ .gitignore
│
├─ .agents/
│  └─ skills/
│     └─ development-brief/
│        └─ SKILL.md
│
├─ docs/
│  ├─ foundation/
│  │  ├─ 01-project-overview.md
│  │  └─ 02-product-requirements.md
│  │
│  └─ knowledge/
│     ├─ work-routing.md
│     ├─ ownership.md
│     └─ next-action.md
│
├─ tools/
│  └─ verify_repository.py
│
└─ .github/
   └─ workflows/
      └─ repository-verify.yml
```

**Baseline count: 13 persistent files.**

That count is a guardrail, not a target to inflate. A new project begins with these responsibilities and adds nothing else at governance level unless a creation gate is satisfied.

`LICENSE`, language/framework configs, source directories, test directories, release files, workspace systems, experimental areas, and product-specific workflows are **context-owned additions**, not general preset requirements.

---

## 7. Exact content contract of every baseline file

### 7.1 `README.md` — human orientation

**Function**

Give a human a fast explanation of what the project is and where current truth lives.

**Must contain**

- project name and one-paragraph purpose;
- development authority (`Local` by default until explicitly changed);
- high-level product/system boundary once known;
- high-level repository map once real source roots exist;
- links to `AGENTS.md`, `CONTEXT.md`, foundation, and `next-action.md`;
- concise evidence-boundary statement.

**Must not contain**

- detailed work-mode rules;
- duplicated current task status;
- session diary;
- roadmap/backlog;
- copied product requirements;
- full ownership matrix;
- detailed CI procedure.

**Anti-drift rule**

For live current status, README links to `next-action.md` instead of maintaining another mutable status narrative.

---

### 7.2 `AGENTS.md` — canonical AI work-routing owner

**Function**

Determine how an AI begins and routes every repository task.

**Must contain**

1. working branch/ref authority;
2. Context Recovery boot;
3. Plan boot;
4. Developing boot;
5. Maintenance boot;
6. no-silent-mode-transition rule;
7. canonical owner map summary;
8. claim/source precedence by responsibility;
9. first-wrong-owner discipline;
10. minimum-complete-solution rule;
11. specialist budget;
12. evidence/proof boundary;
13. user-facing final status format;
14. STOP rule.

**Required Developing route**

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ development-brief
→ smallest relevant owner/source
→ zero/one specialist if justified
```

**Must not contain**

- product requirement detail owned by foundation;
- GitHub API/commit mechanics owned by `GITHUB_RULES.md`;
- full source file inventory;
- task-specific plans;
- duplicated next step;
- framework-specific coding standards unless no nearer owner can exist.

---

### 7.3 `GITHUB_RULES.md` — canonical repository execution policy

**Function**

Keep GitHub work safe, atomic, minimal, reviewable, and honest.

**Core lifecycle**

```text
PIN
→ READ MINIMUM
→ DIAGNOSE
→ TOOL FIT
→ WRITE ONCE
→ VERIFY MINIMUM
→ STOP
```

**Core rules must own**

- exact repo/ref authority;
- no silent default-branch fallback;
- current-state fetch vs search distinction;
- minimum read budget;
- partial/truncated/paginated evidence handling;
- first-wrong-owner diagnosis;
- appropriate mutation/tool choice;
- one logical delivery discipline;
- commit classification/message discipline;
- generated artifact rules;
- CI claim boundaries;
- retry budgets;
- capability/permission denial behavior;
- destructive operation boundaries;
- sensitive data / release / PR surfaces as conditional sections;
- STOP behavior.

**Default discipline**

```text
new files/task              0 unless required
new workflows/task          0 unless required
new abstractions/task       0 unless required
history reads               0 by default
broad scans                 0 by default
logical commits/task        1 by default
push/ref updates/task       1 by default
same-cause retry            <= 2 with new evidence
capability-denial retry     0 without changed evidence
adjacent cleanup            0
```

**Must not become**

A generic Git tutorial or an exhaustive copy of GitHub documentation.

---

### 7.4 `CONTEXT.md` — stable project memory

**Function**

Allow a fresh session to understand the durable project shape without reading history.

**Must contain only stable facts**

- what the product/system is;
- stable terms;
- approved major boundary/architecture once decided;
- durable repository shape;
- stable execution/evidence limitations;
- navigation to detailed owners.

**Must not contain**

- active next step;
- temporary blocker;
- recent test run transcript;
- per-task status;
- speculative future architecture;
- historical narrative already owned by Git history.

**Update threshold**

Update only when a stable fact changes.

---

### 7.5 `.gitignore` — minimal repository hygiene

**Function**

Prevent universal/transient local artifacts from entering history.

**Baseline content must remain minimal** and cover only artifacts created by the baseline itself or universally unwanted OS/cache noise.

Project-specific ignores are added with the project stack; the preset must not ship a giant language/framework ignore catalog.

---

### 7.6 `docs/foundation/01-project-overview.md` — durable product intent

**Function**

Record what is being built before implementation detail begins driving the project.

**Required sections**

```text
Purpose
Primary user / consumer
Problem or job to be solved
In scope
Explicit non-goals
Material constraints already approved
Success boundary
Known high-impact unknowns
```

**Rules**

- unknown stays unknown;
- examples do not silently become requirements;
- implementation choices appear only if already approved and materially constraining;
- no status/history.

---

### 7.7 `docs/foundation/02-product-requirements.md` — durable intended behavior

**Function**

Own current requirements and non-goals independently from implementation status.

**Content model**

Requirements should be expressed as observable product/system obligations, constraints, or boundaries.

Use IDs only when cross-reference complexity makes them useful. Do not force ceremony such as hundreds of IDs for a small project.

**Must distinguish**

```text
required behavior
explicit non-goal
approved constraint
unknown / unresolved decision
```

**Must not contain**

- implementation progress;
- CI result logs;
- speculative fallback behavior;
- historical rejected ideas unless still materially needed to explain current policy.

Additional foundation files are created only when one durable responsibility becomes too large or semantically distinct to remain correct here.

---

### 7.8 `docs/knowledge/work-routing.md` — detailed routing reference

**Function**

Explain routing visually/compactly when `AGENTS.md` should remain concise.

**Authority boundary**

`AGENTS.md` remains canonical. `work-routing.md` may explain but must not introduce a conflicting work mode, owner, or rule.

**Expected content**

- Context Recovery route;
- Plan route;
- Developing route;
- Maintenance route;
- acceptance/proof result routing;
- optional product-specific route only after it exists.

**Must not become**

A second AGENTS file, roadmap, project flow unless the project specifically needs production-flow documentation.

---

### 7.9 `docs/knowledge/ownership.md` — semantic responsibility map

**Function**

Answer: “who currently owns this responsibility?” without broad repository searching.

**Shape**

```text
Responsibility → canonical owner/source
```

**Baseline entries**

- governance owners;
- foundation owner;
- active continuation owner;
- actual product/source owners only after those sources exist.

**Must not contain**

- current status column;
- completion percentage;
- roadmap priority;
- TODO list;
- duplicate next steps;
- every file in the repository.

A mature project may rename this file to `source-ownership.md`, `implementation-map.md`, or another precise name if its semantic responsibility truly changes. It remains one ownership system.

---

### 7.10 `docs/knowledge/next-action.md` — single active continuation owner

**Function**

Make current work resumable across chat/session boundaries.

**Required minimum shape**

```text
# Next Action

## Current Status
<compact factual state>

## Active Boundary
<what is currently in scope and explicitly not being advanced>

## Proof Boundary
<only if material>

## Blocker
<only if real>

## Next Step
<exactly one meaningful next action>
```

**Rules**

- exactly one `## Next Step`;
- no general backlog;
- no historical timeline;
- no duplicate durable requirements;
- no automatically promoted audit findings;
- update only when status, boundary, blocker, required proof, or the next meaningful action changes.

If current source contradicts `next-action.md`, current source is inspected and the stale owner is reconciled before work continues.

---

### 7.11 `.agents/skills/development-brief/SKILL.md` — mandatory non-trivial Developing front door

**Function**

Convert a development request into the smallest grounded contract before edits begin.

**Required contract fields — only when material**

```text
Goal
Suggested method / observed sample
Actual requirement
Input authority
Expected output
Build POV
Acceptance POV
Interface constraints
In scope / Out of scope
Acceptance criteria: 2–5
Proof budget
Open high-impact decisions
Execution channel when it changes implementation/proof
```

**Required procedure**

1. recover continuity;
2. separate fact / proposal / history / unknown;
3. inspect current owner before assuming a change is needed;
4. choose Build POV and Acceptance POV;
5. define minimum complete scope;
6. define 2–5 falsifiable acceptance criteria;
7. select cheapest falsifying proof;
8. use zero/one specialist;
9. implement one coherent change;
10. return to the same contract for final gate;
11. reconcile `next-action.md` only if continuation changed;
12. STOP.

**Hard rules**

- `No change required` is valid;
- no specialist merely because a language/framework appears;
- no second independent problem inside the same bounded slice;
- no fake success/fallback/placeholder promoted beyond what it proves.

---

### 7.12 `tools/verify_repository.py` — static governance contract verifier

**Function**

Mechanically protect reusable repository invariants. It does not prove the product.

**Must verify**

1. required baseline owners exist;
2. `Local` authority is explicit in governance owners;
3. four baseline work modes remain represented;
4. Developing routes through `development-brief`;
5. `next-action.md` contains exactly one `## Next Step`;
6. `ownership.md` does not become a status/TODO owner;
7. relative governance links resolve;
8. temporary/one-use workflow patterns are absent;
9. repository verification workflow is read-only;
10. governance files remain below anti-bloat size ceilings;
11. required baseline skill inventory remains exactly one skill until a project deliberately changes that invariant;
12. generic preset files contain no forbidden reference-product leakage.

**Must not verify**

- product behavior;
- runtime success;
- UI quality;
- model quality;
- device behavior;
- release success;
- human acceptance.

**Implementation constraint**

Use Python standard library only. No dependency/lockfile is justified for a governance verifier that can remain dependency-free.

---

### 7.13 `.github/workflows/repository-verify.yml` — read-only governance CI

**Function**

Run the governance verifier only when governance surfaces change.

**Required properties**

```text
push: Local + governance paths only
pull_request: only explicitly supported refs
workflow_dispatch
concurrency cancel-in-progress
permissions: contents: read
setup pinned supported Python
run: python tools/verify_repository.py
```

**Forbidden**

```text
contents: write
pull-request mutation
git push
release/deploy behavior
continue-on-error that hides failure
one-use temporary workflow behavior
product/runtime claims
```

Product-specific CI is a separate future proof surface.

---

## 8. Anti-AI-slop contract

The preset must explicitly reject the following patterns unless a current acceptance need proves them necessary.

### 8.1 Duplicate ownership

Forbidden examples:

```text
ROADMAP.md + next-action.md carrying the same active status
STATUS.md + README + CONTEXT all maintaining current milestone
flow.md + routing.md + AGENTS.md each defining work modes
multiple ownership maps
multiple config/state stores for the same responsibility
```

### 8.2 Ceremonial documentation

Do not create:

- per-task completion reports;
- daily worklogs;
- review-of-review files;
- generic architecture documents with no decision to preserve;
- empty placeholder directories;
- “future scalability” docs with no current requirement;
- copied checklists that are not used by a real gate.

### 8.3 Speculative abstraction

Do not introduce a service, manager, registry, router, provider layer, plugin system, generic adapter, compatibility framework, cache, queue, state machine, event bus, abstraction interface, or configuration layer merely because it could be useful later.

### 8.4 Fake robustness

Do not hide unknown failures behind:

- broad catch-and-ignore;
- arbitrary retry;
- arbitrary delay;
- silent fallback;
- alternate provider/runtime;
- compatibility aliases;
- placeholder success;
- dry-run success described as real execution.

### 8.5 Test ceremony

Tests exist to protect realistic invariants. Do not add tests that merely assert prose wording, file existence without semantic reason, implementation detail that is free to change, or “proof that the proof file exists”.

### 8.6 Context inflation

The AI should not broad-read the repository, Git history, old reports, all specialist files, or every dependency “to be safe”. Mandatory continuity is read first; everything else is question-driven.

### 8.7 Adjacent cleanup

Visible adjacent issues are not automatically part of the task. Record or mention them only when they block current acceptance or the user asks to include them.

---

## 9. Persistent-addition creation gate

Before creating **any new persistent file, directory, skill, workflow, abstraction, config, state owner, compatibility layer, fallback, cache, experiment, or dependency**, all applicable questions below must pass.

```text
1. Does a current responsibility actually exist?
2. Is it required by the current goal, acceptance criterion, interface, root cause, or proof?
3. Can an existing canonical owner represent it correctly without mixing incompatible responsibilities?
4. Does the addition have one clearly named owner?
5. Can we name the consumer that needs it now?
6. Can we describe when it is updated and when it is not?
7. Can we verify its usefulness with a falsifiable criterion?
8. Is there a smaller solution with fewer persistent surfaces?
```

If the answer to 1–3 or 8 fails: **do not create it**.

A persistent addition is not justified by:

```text
“best practice”
“future scalability”
“clean architecture”
“might need later”
“AI usually creates this”
“another repository has it”
```

---

## 10. Specialized creation gates

### 10.1 New specialist skill

Create only if:

- a recurring semantic responsibility exists;
- `development-brief` alone lacks material procedure;
- the specialist is selected by responsibility, not language/framework;
- its scope is non-overlapping with existing skills;
- repeated tasks would materially benefit from the encoded judgment.

Do not pre-create empty specialists.

### 10.2 New CI/workflow

Create only if:

- an actual executable/proof surface exists;
- there is a repeatable deterministic command or bounded procedure;
- the workflow proves a claim that repository verification cannot prove;
- path/event routing can be scoped appropriately;
- permissions are minimum-needed.

Never create a temporary workflow solely to obtain one proof run when a safer existing channel exists.

### 10.3 New decision log

Create only when decisions repeatedly need durable rationale that cannot be represented by current foundation + Git history, especially when:

- the choice is high-impact and likely to be reconsidered;
- alternatives/reasoning matter to future correctness;
- the decision spans multiple owners or migrations.

Small local decisions stay in the canonical owner and Git history.

### 10.4 New backlog

Create only when multiple deferred independent items genuinely need persistent prioritization. `next-action.md` is never allowed to become that backlog.

### 10.5 New experiment area

Create only when:

- a bounded unknown cannot be resolved safely inside the production owner;
- the experiment has a specific question;
- entry/exit criteria are written;
- experimental evidence cannot silently become production proof;
- promotion requires an explicit production change.

### 10.6 New fallback / compatibility layer

Create only for a named, expected, supported condition. Never use fallback as a substitute for diagnosing an unknown root cause.

### 10.7 New workspace/archive system

Create only when the product has persistent user/project artifacts whose continuity is separate from repository-development continuity.

---

## 11. Governance size and complexity budgets

These are anti-bloat ceilings for v1. A project may deliberately change a ceiling only when the affected responsibility genuinely outgrows it; exceeding a limit is not solved by splitting duplicated information into more files.

| Owner | v1 ceiling |
|---|---:|
| `README.md` | 6,000 chars |
| `AGENTS.md` | 10,000 chars |
| `GITHUB_RULES.md` | 20,000 chars |
| `CONTEXT.md` | 8,000 chars |
| `01-project-overview.md` | 8,000 chars |
| `02-product-requirements.md` | 12,000 chars |
| `work-routing.md` | 6,000 chars |
| `ownership.md` | 8,000 chars |
| `next-action.md` | 6,000 chars |
| `development-brief/SKILL.md` | 8,000 chars |

The verifier should fail clearly when a baseline governance owner crosses its ceiling.

A ceiling breach triggers **semantic compression/reconciliation first**, not automatic file proliferation.

---

## 12. First-wrong-owner diagnostic algorithm

Before editing, determine which owner is actually wrong.

```text
user changes intended behavior
→ foundation / current product policy owner

foundation is correct, implementation violates it
→ implementation owner

implementation is correct, regression test is stale
→ test owner

test/source are correct, CI routes or executes incorrectly
→ workflow/repository policy owner

derived/generated output is wrong
→ upstream canonical source or generator

next-action is stale but source is correct
→ continuity owner

historical issue cannot be reproduced and no current requirement supports it
→ NO ACTIVE CHANGE
```

The AI must not “fix the easiest file”.

---

## 13. Development-necessity gate

After grounding the request:

```text
current behavior already satisfies requirement
→ NO CHANGE REQUIRED

requirement materially unresolved
→ PLAN

concrete existing behavior is wrong
→ MAINTENANCE

approved behavior requires creation/change
→ DEVELOPING

requested method conflicts with requirement/evidence
→ REDIRECT METHOD, PRESERVE GOAL
```

This gate prevents automatic implementation output.

---

## 14. Acceptance and proof model

### 14.1 Acceptance criteria

Non-trivial Developing uses **2–5** criteria only.

Each criterion must be:

- tied to the requested outcome;
- observable/falsifiable;
- free from implementation detail unless the detail is itself required;
- capable of being supported by real proof.

### 14.2 Proof budget

Choose the cheapest evidence that can falsify each changed claim.

Generic proof classes:

```text
SOURCE VERIFIED
→ current repository/source/static contract proves the claim

HOSTED VERIFIED
→ CI/hosted environment actually executed the claim

TARGET VERIFIED
→ actual target/local/runtime/device environment executed the claim

HUMAN ACCEPTED
→ visual/audio/content/usability judgment was actually reviewed by the responsible human

UNKNOWN / REQUIRED PROOF MISSING
→ do not upgrade status
```

Labels are used only when materially useful; they are not mandatory decoration in every response.

### 14.3 Status rule

```text
all required implementation + proof complete
→ Selesai

implementation complete but required target/human proof unavailable
→ Perlu pemeriksaan

material blocker prevents safe completion
→ Terhenti
```

---

## 15. User-facing communication contract

For non-trivial Developing, a compact visible pre-edit brief may use:

```text
Tujuan:
Cara berpikir:
Hasil yang dituju:
Tidak diubah:
Cara memastikan benar:
```

Final material report:

```text
Status: Selesai | Perlu pemeriksaan | Terhenti
Hasil:
Bukti:
Batasan:
Next step:
```

Exactly one `Next step`.

Internal development-contract detail should not be dumped to the user unless it is needed for a material decision.

---

## 16. Project instantiation contract

Develop-Builder is a general source preset. Before the first real Developing task in a new project, perform a bounded **Bootstrap Adaptation**.

### Bootstrap Adaptation inputs

Recover or define only:

```text
project name
project purpose
primary user/consumer
current scope
explicit non-goals
working branch authority
known major constraints
initial proof boundary
first real development objective
```

### Bootstrap Adaptation writes

Adapt only:

```text
README.md
AGENTS.md          # project-specific branch/product mode only when needed
CONTEXT.md
01-project-overview.md
02-product-requirements.md
ownership.md
next-action.md
```

`GITHUB_RULES.md`, `development-brief`, repository verifier, and repository workflow remain generic unless the project proves a real reason to narrow/extend them.

### Bootstrap prohibition

Do **not** invent during bootstrap:

- final architecture;
- full source tree;
- specialist inventory;
- release design;
- database schema;
- API system;
- compatibility matrix;
- monitoring/telemetry;
- test matrix for nonexistent surfaces;
- future roadmap.

The bootstrap makes development safe; it does not pretend the whole product has already been designed.

---

## 17. Domain adaptation order

When a project starts growing, adapt in this sequence:

### A. Product truth

Define desired outcome and non-goals before technical shape.

### B. Semantic responsibilities

Ask who owns current truth for each real responsibility.

### C. Current implementation owners

Create/map source folders only for responsibilities that now exist.

### D. Specialist procedure

Add a specialist only after the semantic responsibility is stable and repeated.

### E. Product-specific proof

Add tests/workflows only when executable/product surfaces exist.

### F. Release/operations

Add only when deployment/distribution/operations becomes a current requirement.

This order prevents framework-first design.

---

## 18. What is explicitly absent from baseline v1

The following must be absent unless a creation gate later passes:

```text
additional .agents skills
Experimental/
workspace/active
workspace/archive or workspace/saved
reviews/
decisions/
backlog.md
validation-report.md
local-acceptance-runbook.md
release workflow
product CI
deployment workflow
source-code framework
runtime folders
database/storage layer
provider/router registry
feature-flag framework
compatibility layer
fallback runtime
telemetry/analytics
plugin architecture
general cache/queue/event bus
API gateway
monorepo package hierarchy
```

Absence is intentional architecture, not missing work.

---

## 19. Repository verifier specification

The v1 verifier should be small, deterministic, and dependency-free.

### Required checks

#### Structure

- 13 baseline files exist;
- exactly one canonical root `.agents/skills` directory exists;
- baseline skill set is exactly `{development-brief}`.

#### Authority

- `Local` is explicitly identified as working authority in `AGENTS.md` and `GITHUB_RULES.md`;
- no text suggests silent fallback to another branch.

#### Work modes

- Context Recovery, Plan, Developing, Maintenance are present;
- observation is explicitly read-only;
- Developing references `development-brief`;
- Plan is explicitly no implementation.

#### Continuity

- `next-action.md` has one `## Current Status`, one `## Active Boundary`, exactly one `## Next Step`;
- optional proof/blocker headings may appear at most once;
- next-action does not contain backlog/roadmap headings.

#### Ownership

- ownership file references core canonical owners;
- forbidden active-status columns/headings are absent.

#### Anti-bloat

- governance size ceilings pass;
- no second routing/status/ownership filenames from an explicit retired/forbidden baseline list;
- no placeholder specialist directory exists.

#### Link integrity

- relative Markdown links in active governance owners resolve.

#### Workflow safety

- `repository-verify.yml` uses read-only permissions;
- it runs on `Local` governance changes;
- it uses concurrency cancellation;
- no write, push, release, deploy, or `continue-on-error` bypass appears;
- no `temp-*` / one-use workflows are present.

#### Domain neutrality

The generic baseline governance/kernel must not contain reference-product assertions such as:

```text
BuildIT
TranslateIT
PRD-Creator
Blockbench
Minecraft
Windows audio
VoiceLab
PRD production
```

Develop-Builder's own implementation plan may mention references; instantiated kernel files may not leak them.

### Verifier non-goals

The verifier must not become a linter for writing style, architecture quality, or product behavior.

---

## 20. Adversarial usability scenarios

Preset v1 must be tested conceptually against these scenarios before freeze.

### Scenario 1 — Read-only observation

Request: “Amati repo dan pahami next step.”

Expected:

```text
recover context
→ report current state
→ do not execute next step
```

### Scenario 2 — User supplies a concrete method

Request: “Add X using framework/library Y.”

Expected:

```text
recover actual requirement
→ verify whether Y is necessary/suitable
→ FOLLOW / REFINE / REDIRECT
→ do not blindly encode suggested method
```

### Scenario 3 — Current behavior already works

Expected result: `No change required`, no ceremonial commit.

### Scenario 4 — Concrete regression

Expected: Maintenance begins from defect/first wrong owner, not full redesign.

### Scenario 5 — Stale next-action

Expected: current source inspected, stale continuation reconciled, no blind replay.

### Scenario 6 — Derived artifact is wrong

Expected: repair source/generator, not manually patch generated output.

### Scenario 7 — Hosted CI passes but target runtime was never run

Expected: target claim remains unverified; status cannot be inflated.

### Scenario 8 — AI notices adjacent cleanup

Expected: leave it out unless it blocks current acceptance.

### Scenario 9 — “Create a scalable provider/router framework for future integrations.”

Expected: reject/redirect unless current requirements prove multiple providers/routes.

### Scenario 10 — “Create specialists for frontend, backend, database, testing before coding.”

Expected: reject placeholder specialists; only `development-brief` remains.

### Scenario 11 — A second independent problem appears during Developing

Expected: finish/reframe current boundary before opening another specialist/scope.

### Scenario 12 — Product requires persistent user project packages

Expected: workspace system may now pass its creation gate; baseline itself was still correct to omit it.

### Scenario 13 — High-impact architecture choice cannot be recovered

Expected: return to Plan; do not invent a decision inside Developing.

### Scenario 14 — CI failure appears after unrelated docs change

Expected: diagnose exact failure; do not mutate product code merely to make CI green.

### Scenario 15 — User asks to “improve everything”

Expected: recover current product objective, bound acceptance, refuse undefined repo-wide refactor as default.

---

## 21. Cross-domain neutrality audit

Before v1 freeze, apply the kernel without adding fake architecture to three materially different hypothetical contexts:

```text
A. local desktop/runtime application
B. document/content production system
C. creative plugin/tooling system
```

For each context, verify:

- baseline governance adapts without deleting core responsibilities;
- product source structure can differ completely;
- no reference-domain terminology is required;
- optional mode/specialist/workspace/CI surfaces are added only if context proves need;
- fresh-session recovery works;
- a simple task does not require broad repository reading;
- no generic framework is forced.

This is an **assumption audit**, not a request to build three sample applications.

---

## 22. Implementation phases

### Phase 0 — Reference audit + specification freeze

**Current phase.**

Deliverable:

- this plan;
- exact baseline responsibility set;
- optional-surface gates;
- anti-slop contract;
- verifier contract;
- acceptance/adversarial scenarios.

No preset implementation yet.

### Phase 1 — Governance core

Create and ground:

```text
README.md
AGENTS.md
GITHUB_RULES.md
CONTEXT.md
.gitignore
```

Gate:

- responsibilities do not overlap;
- branch/routing/STOP behavior is explicit;
- no domain leakage;
- no fake project facts.

### Phase 2 — Foundation + continuity

Create:

```text
docs/foundation/01-project-overview.md
docs/foundation/02-product-requirements.md
docs/knowledge/work-routing.md
docs/knowledge/ownership.md
docs/knowledge/next-action.md
```

Gate:

- stable vs active information is separated;
- exactly one next step;
- work-routing explains but does not override AGENTS;
- ownership maps responsibilities only.

### Phase 3 — Development front door

Create:

```text
.agents/skills/development-brief/SKILL.md
```

Gate:

- non-trivial Developing always enters through it;
- 2–5 criteria + proof budget;
- development necessity gate;
- zero/one specialist rule;
- no placeholder specialist set.

### Phase 4 — Static governance verification

Create:

```text
tools/verify_repository.py
.github/workflows/repository-verify.yml
```

Gate:

- dependency-free verifier passes locally/hosted;
- workflow is read-only and path-scoped;
- verifier tests only repository-governance claims.

### Phase 5 — Adversarial + cross-domain audit

Run Sections 20–21 against the implemented preset.

Fix only assumptions that fail the baseline responsibility.

Do not add optional architecture to make hypothetical scenarios more complete.

### Phase 6 — Complexity audit

Before v1 freeze ask:

```text
Can any baseline file be removed without losing a unique required responsibility?
Can any two files be merged without mixing stable/active/execution responsibilities?
Does every line belong to its owner?
Does every automated check protect a real invariant?
Is any rule duplicated?
Is any optional system present without a current need?
```

Expected result is not “more complete”; expected result is the **smallest correct kernel**.

### Phase 7 — Freeze preset v1

Only after all gates pass:

- record preset version in README;
- set `next-action.md` to stable idle or the next real Develop-Builder objective;
- commit as one coherent logical delivery if tooling allows atomicity;
- stop.

---

## 23. Preset v1 acceptance criteria

Preset v1 is accepted only if all criteria below pass.

### A. Semantic parity

The Developing lifecycle preserves:

```text
continuity recovery
→ development-brief
→ requirement vs method separation
→ development necessity gate
→ one canonical owner
→ 2–5 acceptance criteria
→ proof budget
→ minimum complete change
→ honest status
→ one next step
→ STOP
```

### B. Domain neutrality

No reference product, runtime, language, framework, platform, model, content type, or release architecture is required by the kernel.

### C. Ownership singularity

Each baseline responsibility has exactly one canonical owner and no competing state system.

### D. Cross-session recoverability

A fresh AI can recover:

```text
what this project is
what branch/state is authoritative
what mode applies
where desired behavior lives
where actual behavior lives
what is currently active
what the one next step is
```

without relying on chat history.

### E. Anti-overdevelopment

The preset begins with one skill, one governance workflow, no product-specific architecture, and explicit gates for every optional persistent surface.

### F. Proof honesty

Repository/static/hosted/target/human proof boundaries are distinguishable and cannot silently upgrade.

### G. Mechanical drift protection

The generic verifier catches baseline owner loss, routing drift, continuity shape drift, governance bloat, link breakage, unsafe verification workflow behavior, and reference-domain leakage.

### H. Usability

A normal bounded development task can start after continuity with the smallest relevant owner; the preset does not require broad scanning or loading multiple specialists.

### I. Stop discipline

Completion, `No change required`, and `Perlu pemeriksaan` are all valid terminal outcomes. The system does not automatically continue to adjacent work.

---

## 24. Failure conditions — preset must not be frozen if any occur

Do not call the preset v1 if:

- more than one active status/next-step owner exists;
- `AGENTS.md` and `work-routing.md` disagree;
- a new project inherits reference-product terminology;
- baseline contains placeholder specialists;
- baseline contains generic runtime/source architecture;
- verifier requires unnecessary third-party dependencies;
- repository workflow can mutate the repo;
- a fresh session still needs chat history for current continuation;
- generated output can outrank its source;
- current-source vs stale-next-action reconciliation is undefined;
- proof classes are conflated;
- optional-surface creation gates are missing;
- governance size budgets are already exceeded;
- hypothetical context audit requires deleting core responsibilities rather than merely adapting domain owners.

---

## 25. Protected non-goals

Develop-Builder v1 is not:

- a universal application framework;
- a universal folder tree;
- a monorepo starter;
- a coding-style framework;
- an autonomous project manager;
- a roadmap generator;
- a prebuilt frontend/backend/database architecture;
- a library of language-specific AI specialists;
- an automatic release/PR/branch system;
- an exhaustive documentation framework;
- a generic test framework;
- a migration requirement for existing repositories;
- a replacement for product/domain judgment.

It is a **development governance and continuity kernel**.

---

## 26. Final implementation principle

The final preset should feel deliberately small.

A good result is not the preset with the most safeguards, files, skills, workflows, and abstractions. A good result is the smallest system that reliably prevents:

```text
wrong authority
lost context
wrong owner
method-before-requirement
scope expansion
duplicate state
fake robustness
proof inflation
stale continuation
endless improvement loops
```

Anything beyond that belongs to the project only after the project earns it.

---

## 27. Next Step

**After this specification is accepted, implement Phases 1–4 as the complete baseline kernel on `Local` without adding any optional surface, then run the adversarial/cross-domain/complexity audits in Phases 5–6 before declaring preset v1.**
