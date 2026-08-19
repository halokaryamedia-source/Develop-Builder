# Develop-Builder Context

Stable orientation for Develop-Builder on branch `Local`.

This file owns durable project facts only. Active continuation belongs in `docs/knowledge/next-action.md`; task routing belongs in `AGENTS.md`; GitHub execution discipline belongs in `GITHUB_RULES.md`.

## Product

Develop-Builder is a general bootstrap preset for starting and developing projects with AI-assisted repository work.

Its purpose is to preserve a disciplined development operating model while keeping the route to a correct result as direct as the real problem allows.

Primary principle:

```text
shortest correct path
+ sufficient context
+ sufficient proof
```

The preset is intentionally domain-neutral. It does not choose a programming language, framework, runtime, source architecture, database, provider model, release strategy, production workflow, or specialist inventory for the project using it.

## Stable operating model

For repository/system work, Develop-Builder distinguishes:

```text
Context Recovery
Plan
Developing
Maintenance
```

Developing may use either a Direct Bounded Path or the non-trivial `development-brief` path. Escalation is based on material uncertainty, impact, risk, blast radius, ownership coordination, and proof difficulty—not code/file count.

Normal **existing-system/domain execution** is a separate semantic boundary: creating or revising the normal output of an already-defined system does not become system Developing merely because files/artifacts are created. A project may formalize a named production/authoring mode only when a real repeatable workflow earns it.

The repository preserves **one canonical owner per responsibility**, while one coherent task may legitimately touch the smallest necessary set of owners.

## Core Bootstrap

The day-zero preset contains nine persistent files:

```text
README.md
AGENTS.md
GITHUB_RULES.md
CONTEXT.md
.gitignore
.agents/skills/development-brief/SKILL.md
docs/foundation/01-project-overview.md
docs/foundation/02-product-requirements.md
docs/knowledge/next-action.md
```

These own human orientation, AI routing, GitHub execution, stable memory, hygiene, non-trivial Developing procedure, durable project intent, durable requirements, and active continuation.

## Earned growth

The following are not baseline requirements and appear only after a real project responsibility proves need:

- detailed work-routing documents;
- ownership/source maps;
- decision logs/backlogs/review archives;
- repository-governance automation;
- experiments;
- workspace active/archive systems;
- additional specialist skills;
- product-specific production/authoring procedures;
- product-specific CI/release workflows;
- runtime/source architecture.

Mature structure is allowed to shrink again when a responsibility disappears.

## Anti-overdevelopment

Anti-overdevelopment means proportional complexity, not minimal line/file count.

A simple bounded correction should remain direct. Normal use of an existing system should go directly through its domain owner/procedure. A risky or cross-owner system change may require more coordination and proof. An abstraction is justified only when it uniquely supplies a current required capability or reduces total current complexity rather than moving it.

## AI-slop boundary

Do not add generic filler, duplicate state, speculative architecture, fabricated unknowns, ceremonial tests/reports, placeholder specialists, or robustness layers that hide an unknown root cause.

## Evidence boundary

Repository/static proof establishes only repository/static claims. Hosted execution establishes only the behavior it actually ran. Runtime/device/visual/audio/model/target-machine/human acceptance requires matching evidence.

## Navigation

- work routing → `AGENTS.md`
- GitHub execution → `GITHUB_RULES.md`
- project intent → `docs/foundation/01-project-overview.md`
- product/system requirements → `docs/foundation/02-product-requirements.md`
- active continuation → `docs/knowledge/next-action.md`
- non-trivial Developing → `.agents/skills/development-brief/SKILL.md`