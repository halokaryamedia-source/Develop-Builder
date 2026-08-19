# Develop-Builder

Develop-Builder is the source starter for a **general project-definition, critical design, capability-planning, development-governance, and continuity kernel**.

Canonical template and development authority: **`Local`**.

## Core principle

> Use the shortest correct path with sufficient project definition, sufficient evidence, sufficient context, and sufficient proof.

The starter does not prescribe a programming language, framework, runtime, database, release model, provider system, or source-tree layout. It provides the operating structure needed to define **what is worth building**, challenge unsupported/disproportionate direction, determine what reusable development judgment is actually needed, and then develop the project without losing context.

## One current source

Each responsibility has one current canonical owner.

```text
find current owner
→ update it in place
→ update required dependents
→ remove superseded current path/state when safe
→ prove only the claims actually exercised
→ STOP
```

Git history owns ordinary history. Do not preserve obsolete current source as versioned generations, legacy copies, parallel owners, or compatibility paths merely to avoid replacing it cleanly.

## Repository distribution contract

The reusable starter has one canonical repository source:

```text
canonical branch      = Local
GitHub default branch = Local
GitHub template flag  = enabled
```

These repository settings are part of the template contract, not optional presentation settings.

Rules:

- `Local` is the only template/development authority.
- Never silently consume the repository default when it is not `Local`.
- `main` must not become a second current source, release mirror, fallback, or independent policy owner.
- Do not create a recurring `Local → main` synchronization workflow.
- After GitHub default branch is `Local`, remove `main` when no concrete current external contract requires it.
- If repository metadata does not satisfy `default_branch=Local` and `is_template=true`, template **distribution configuration is incomplete** even when source content itself is correct.

Repository settings/history must not be changed merely for aesthetics. The removal of a superseded branch happens only after the canonical default branch is established and the branch has no current external obligation.

## Canonical consumption path

Once the repository distribution contract is satisfied, create new projects through the GitHub template mechanism from the current `Local` source.

```text
GitHub template repository
→ current Local source
→ new project repository without Develop-Builder project history
→ establish/retain Local as project working authority
→ project-definition
→ Foundation + Documentation Readiness
→ project-skill-planner
→ CONTEXT + only earned Knowledge navigation
→ one next-action
→ DEVELOPMENT READY
```

Do not use cloning Develop-Builder history, copying an old branch, or falling back to `main` as alternate bootstrap paths.

Normal product Developing does **not** begin merely because the repository has a name or because the user proposed an architecture.

## Critical project design

`.agents/skills/project-definition/SKILL.md` is the critical semantic front door for new/materially redefined projects.

It must:

- recover current evidence before asking for discoverable facts;
- separate source-backed facts, approved decisions, necessary implications, AI proposals, and unknowns;
- challenge unsupported assumptions and disproportionate architecture/features;
- `FOLLOW`, `REFINE`, `REDIRECT`, `REJECT`, or `BLOCKED` honestly rather than defaulting to agreement;
- recommend the smallest responsible direction supported by current evidence;
- persist accepted project meaning in Foundation instead of creating parallel planning artifacts.

## Development capability planning

After Documentation Readiness, `.agents/skills/project-skill-planner/SKILL.md` determines whether the project needs any reusable project specialists.

`No project specialist required` is valid.

Project specialists are created only for distinct recurring semantic development responsibilities. They are not created from programming languages, frameworks, directories, testing tools, research techniques, or difficult one-off tasks.

## Documentation entrypoint

`docs/README.md` is the canonical documentation-system owner. It explains:

- what must be defined before Developing;
- what belongs in Foundation vs Knowledge vs CONTEXT vs Skill;
- when Overview + Requirements are sufficient;
- when another durable domain document is required;
- when another Knowledge navigation owner is required;
- when a new document would be AI-slop and must not be created;
- the Documentation Readiness gate.

## Core workflow skills

```text
project-definition
project-skill-planner
development-brief
```

These are reusable kernel procedures, not project-specific fact stores and not project specialists.

## Navigation

- project bootstrap, work routing, source finalization, skill budget → `AGENTS.md`
- GitHub execution/history/safety → `GITHUB_RULES.md`
- documentation architecture / pre-development readiness → `docs/README.md`
- critical Project Definition → `.agents/skills/project-definition/SKILL.md`
- project-specialist planning/creation → `.agents/skills/project-skill-planner/SKILL.md`
- stable project orientation + distribution contract → `CONTEXT.md`
- project overview scaffold/current owner → `docs/foundation/01-project-overview.md`
- product requirements scaffold/current owner → `docs/foundation/02-product-requirements.md`
- active continuation / distribution blocker → `docs/knowledge/next-action.md`
- non-trivial Developing front door → `.agents/skills/development-brief/SKILL.md`

## Evidence boundary

Repository/source inspection proves repository/source claims. Repository metadata must be inspected to claim template-distribution readiness. External feasibility/support/compatibility facts require current authoritative evidence when material. Hosted execution proves only what it actually runs. Runtime, device, visual, audio, model, target-machine, and human-acceptance claims require matching evidence.

Current continuation is intentionally not duplicated here; use `docs/knowledge/next-action.md`.
