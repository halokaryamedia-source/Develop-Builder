# Develop-Builder Context

Stable orientation for the Develop-Builder starter source on branch `Local`.

This file owns stable starter/repository facts only. Documentation architecture belongs in `docs/README.md`; active continuation belongs in `docs/knowledge/next-action.md`; task routing belongs in `AGENTS.md`; GitHub execution discipline belongs in `GITHUB_RULES.md`.

## Purpose

Develop-Builder is a general starter for AI-assisted project definition and repository development.

Primary principle:

```text
shortest correct path
+ sufficient project definition
+ sufficient context
+ sufficient proof
```

The starter is domain-neutral. It does not choose a language, framework, runtime, source architecture, database, provider model, release strategy, production workflow, or specialist inventory for the project using it.

## Documentation model

A project created from the starter must not jump from repository naming directly into product Developing.

Canonical bootstrap sequence:

```text
source / intent recovery
→ Project Overview
→ Product Requirements
→ Foundation Expansion Gate
→ Documentation Readiness review
→ CONTEXT projection
→ one current next-action
→ normal Developing / Domain Execution
```

`docs/README.md` owns this documentation lifecycle and the rules for creating or rejecting additional durable docs.

## Starter-source exception

In the Develop-Builder source repository:

- `docs/foundation/01-project-overview.md` and `02-product-requirements.md` are **reusable project-definition scaffolds**, not Develop-Builder product policy;
- `docs/README.md`, `AGENTS.md`, `GITHUB_RULES.md`, and `development-brief` are reusable kernel owners;
- this `CONTEXT.md`, root `README.md`, and `next-action.md` describe the starter source itself.

When instantiated into a real project, the project-specific owners are rewritten with current project truth.

## Current-source model

Each durable responsibility has one current owner.

- No artificial owner generations or legacy/current duplicates.
- Git history owns ordinary history.
- Compatibility/migration exists only for a real current external contract.
- When a responsibility disappears, unnecessary current structure is removed or folded into the remaining owner.

## Work model

Repository/system work distinguishes:

```text
Context Recovery
Plan
Developing
Maintenance
```

Project Definition is a bounded **pre-development phase**, not another permanent work mode. Normal existing-system/domain execution is also distinct from changing the system itself.

Non-trivial Developing uses `development-brief`; Direct Bounded work remains shorter when wider context cannot change correctness.

## Core starter owners

```text
README.md
AGENTS.md
GITHUB_RULES.md
CONTEXT.md
.gitignore
.agents/skills/development-brief/SKILL.md
docs/README.md
docs/foundation/01-project-overview.md
docs/foundation/02-product-requirements.md
docs/knowledge/next-action.md
```

Additional foundation or knowledge owners are earned by real project responsibilities. File count is not a target; complete ownership without duplication is the target.

## Anti-overdevelopment and AI-slop boundary

Do not confuse simplicity with missing project definition.

A simple project may need only Overview + Requirements before Developing. A domain-heavy or multi-stage project may genuinely need workflow, boundary, quality-standard, source-intake, validation, or other durable owners before implementation.

Do not add those documents speculatively. Do not omit them when their responsibility materially controls implementation or acceptance.

## Evidence boundary

Repository/static proof establishes only repository/static claims. Runtime/device/visual/audio/model/target-machine/human acceptance requires matching evidence.

## Navigation

- bootstrap / work routing → `AGENTS.md`
- GitHub execution → `GITHUB_RULES.md`
- documentation architecture → `docs/README.md`
- project overview → `docs/foundation/01-project-overview.md`
- project requirements → `docs/foundation/02-product-requirements.md`
- active continuation → `docs/knowledge/next-action.md`
- non-trivial Developing → `.agents/skills/development-brief/SKILL.md`
