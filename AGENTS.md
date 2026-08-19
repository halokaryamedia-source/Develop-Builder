# Agent Routing

This repository is a general project-definition and development kernel. Current repository/project sources are authority for repository state; chat history is supporting context only.

## Authority

- `Local` is the canonical template and working/development authority.
- Never silently fall back to another branch, including a retained non-authoritative `main`.
- Material GitHub execution follows `GITHUB_RULES.md`.
- Documentation architecture and Documentation Readiness follow `docs/README.md`.
- Detailed Project Definition judgment lives in `.agents/skills/project-definition/SKILL.md`.
- Project-specialist necessity/creation/pruning lives in `.agents/skills/project-skill-planner/SKILL.md` when that capability is actually triggered.
- Non-trivial Developing uses `.agents/skills/development-brief/SKILL.md`.

## Cross-cutting invariants

Use the **smallest sufficient path**. Efficiency must not remove context, authority, safety, or proof that can change correctness.

Each responsibility has one current canonical owner:

```text
change needed
→ find current owner
→ update it in place
→ update only required dependents
→ remove superseded current path/state when safe
→ obtain only matching proof
→ STOP
```

Git history owns ordinary history. Do not create versioned/legacy/backup/current duplicates, parallel authorities, compatibility/fallback paths, or permanent task/status/report owners merely to avoid replacing current truth cleanly. A compatibility/migration boundary requires a concrete current external contract.

Unknown remains unknown. User intent owns intended outcome and high-impact user decisions; user-suggested methods are proposals until current authority adopts them. Evidence owns factual claims. `No change required` is valid.

A nearer `AGENTS.md` may exist only for a real local/package responsibility. It may narrow local behavior but must not weaken branch safety, evidence honesty, current-source finalization, ownership integrity, or STOP boundaries.

# Task routing

## Bootstrap Instantiation

Use a clean GitHub Template Repository snapshot from current `Local`; do not carry Develop-Builder project history into the new project.

```text
project-definition
→ current Foundation through docs/README.md
→ Documentation Readiness
→ specialist-necessity gate
→ README.md + CONTEXT.md projection
→ Knowledge Navigation Gate only when current navigation needs it
→ one next-action
→ DEVELOPMENT READY
→ report
→ STOP
```

### Specialist-necessity gate

After Documentation Readiness, do **not** load `project-skill-planner` by default.

```text
approved scope/current source shows no plausible recurring specialized semantic judgment
beyond Foundation + development-brief + nearest AGENTS/source rules
→ zero project specialists
→ skip project-skill-planner

specialist need is plausible or ambiguous
/ existing project specialists need overlap, sufficiency, or pruning review
→ project-skill-planner
```

Technology names, folders, tools, difficult one-off tasks, or a desire to look mature do not trigger the planner.

Bootstrap normally rewrites project-specific `README.md`, `CONTEXT.md`, Overview, Requirements, and `next-action.md`; it retains the generic kernel owners unless the instantiated project has a real routing/procedure difference. Do not create empty future docs, placeholder specialists, speculative architecture, or parallel starter identity.

Bootstrap does not automatically begin implementation unless the user also requested it and all affected pre-development gates pass.

## Project Definition

Use `project-definition` for a new project, material redefinition, materially new undefined domain, or when Developing discovers undefined project meaning.

```text
current intent + authority + evidence
→ project-definition
→ accepted Foundation truth
→ Documentation Readiness
→ return to this routing
```

Project Definition may edit durable project definition. It does not implement undefined behavior. A bounded discovery/prototype before readiness is allowed only when it is the minimum evidence needed to resolve a material unknown and its result returns to the appropriate Foundation owner.

## Context Recovery

For read-only `amati`, inspect, understand, audit, study, or context recovery:

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ smallest current owner/navigation source needed
→ report
→ STOP
```

Do not broad-read all Knowledge/skills, edit, run CI, execute the recorded next step, or promote historical TODOs merely because they were discovered.

## Plan

Use Plan when a material product, architecture, ownership, risk, feasibility, or acceptance decision remains unresolved.

```text
recover current authority/evidence
→ separate outcome from suggested method
→ resolve or recommend what can be resolved responsibly
→ expose only remaining material decision
```

Recover discoverable facts before asking the user. Plan-only requests do not silently become Developing. Undefined project meaning routes to `project-definition`.

## Existing-system / Domain Execution

Using an existing system/procedure to produce its normal output is not automatically Developing.

```text
current request + current domain state
→ matching earned domain owner/procedure
→ matching acceptance
→ STOP
```

If required domain meaning/workflow/quality/acceptance is undefined, return to `project-definition`; do not improvise it inside production work.

## Developing

### Direct Bounded Path

Use when the requested outcome is already defined, the current/first-wrong owner is obvious or cheaply discoverable, wider stable context cannot change the solution, no material unresolved decision/new authority boundary exists, blast radius is local, and targeted proof is obvious.

```text
pin repo/ref
→ exact owner/defect
→ smallest complete correction
→ required caller/contract/assertion only when needed
→ remove superseded current path/state when safe
→ targeted proof
→ update continuation only if meaningfully changed
→ STOP
```

Direct means less ceremony, not less correctness.

### Non-trivial Developing

Use when uncertainty, semantic impact, blast radius, ownership coordination, migration, persistent authority, dependency change, hard rollback, or acceptance risk can materially change the implementation.

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ development-brief
→ smallest affected Foundation/navigation/source/caller/contract set
→ zero/one already-earned matching project specialist
→ coherent implementation
→ matching proof
→ reconcile changed current owners
→ STOP
```

`development-brief` owns the detailed implementation procedure. If its affected Project Definition check fails, leave implementation and return to `project-definition` / Plan.

Do not invoke `project-skill-planner` routinely inside development tasks. If work reveals a plausible new recurring semantic specialist need, finish/reframe the current bounded responsibility and route that capability question through the specialist-necessity gate.

## Maintenance

A concrete defect, regression, stale rule, or behavior-preserving cleanup uses the Direct Bounded Path by default when wider project definition cannot change the fix. If diagnosis exposes a material undefined decision, return to Plan / Project Definition.

# Claim ownership

Use the nearest current authority:

- task intent/new explicit project decision → current user instruction;
- GitHub/ref/write/history/CI/security → `GITHUB_RULES.md`;
- documentation structure/readiness → `docs/README.md`;
- critical project-definition procedure → `project-definition`;
- specialist necessity/creation/pruning → `project-skill-planner`;
- work mode/routing/per-task skill budget → applicable `AGENTS.md`;
- stable orientation → `CONTEXT.md`;
- durable project/product meaning → `docs/foundation/`;
- current development navigation/context → earned `docs/knowledge/` owner;
- active continuation → `docs/knowledge/next-action.md`;
- actual behavior → current source + relevant proof;
- generated output → upstream canonical source/generator;
- ordinary history → Git history/issues/PRs unless current work explicitly requires bounded recovery.

If current owners conflict, reconcile the wrong/stale current owner; do not create another compatibility/legacy path. Material conflict that cannot be resolved responsibly remains `UNKNOWN` and routes to Plan / Project Definition.

# Persistent-owner gate

Before adding any persistent file/module/layer/authority ask:

```text
what distinct live responsibility needs an owner?
why can the current owner not represent it cleanly?
who consumes it now?
what realistic error/decision/acceptance/navigation problem does it solve?
```

Documentation uses `docs/README.md`; project specialists use `project-skill-planner`. If the addition does not materially earn an owner, do not create it.

# Skill budget

```text
Project Definition
→ project-definition
→ zero project specialists

Bootstrap after Documentation Readiness
→ specialist-necessity gate
→ zero specialists OR project-skill-planner when triggered

Direct Bounded Path
→ zero project specialists by default

Non-trivial Developing
→ development-brief + zero/one already-earned project specialist

Maintenance
→ zero/one project specialist only when diagnosed semantic responsibility needs it

Plan / Context Recovery
→ zero project specialists by default
```

Tools, research, testing, profiling, languages, frameworks, and libraries do not become project specialists merely because they are used.

# Evidence and completion

Use the cheapest evidence capable of falsifying the changed claim. Current unstable external facts require current authoritative evidence when material; source/static/hosted proof establishes only what it actually exercises.

When current scope and required proof are satisfied: **STOP**. Do not automatically continue into adjacent cleanup, another audit, another verifier, unnecessary testing, historical TODOs, branch synchronization, another version/generation, or the next milestone.
