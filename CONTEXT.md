# Develop-Builder Context

Stable orientation for the Develop-Builder starter source on canonical branch `Local`.

This file is intentionally compact. Detailed routing belongs in `AGENTS.md`; GitHub execution in `GITHUB_RULES.md`; documentation/readiness in `docs/README.md`; active continuation in `docs/knowledge/next-action.md`; reusable procedures in `.agents/skills/`.

## Purpose

Develop-Builder is a domain-neutral GitHub Template Repository for AI-assisted project definition and repository development.

Primary principle:

```text
shortest correct path
+ sufficient evidence-backed project definition
+ sufficient current context
+ sufficient proof
```

It does not preselect a language, framework, runtime, database, source architecture, provider, release model, production workflow, or project-specialist inventory.

## Repository authority and distribution

```text
canonical/default branch = Local
GitHub template mode     = enabled
```

`Local` is the single current template/development authority. A retained `main` may remain by repository-owner decision, but it is non-authoritative: agents do not fall back to it, it is not a compatibility/release mirror, it needs no recurring synchronization, and divergence from `Local` is not a repair task by itself.

New projects are created from the GitHub Template mechanism using current `Local`; they do not inherit Develop-Builder project history.

## Stable operating model

```text
user intent + authoritative evidence
→ project-definition when project meaning is new/materially undefined
→ Foundation + Documentation Readiness
→ AGENTS specialist-necessity routing
→ zero specialists OR project-skill-planner when actually triggered
→ CONTEXT + only earned Knowledge navigation
→ one next-action
→ development-brief for non-trivial Developing
```

Simple projects are allowed to remain simple. Additional Foundation, Knowledge, local AGENTS, project-specialist, source, or proof owners exist only when a real responsibility earns them.

## Starter-source exception

In this source repository:

- `docs/foundation/01-project-overview.md` and `02-product-requirements.md` are reusable scaffolds, not Develop-Builder product policy;
- `AGENTS.md`, `GITHUB_RULES.md`, `docs/README.md`, and the three core workflow skills are reusable kernel owners;
- root `README.md`, this file, and `docs/knowledge/next-action.md` describe the starter repository itself.

An instantiated project rewrites project-specific owners with its own current truth.

## Canonical owner navigation

- human/template entry and distribution contract → `README.md`
- work routing, cross-cutting invariants, skill budget → `AGENTS.md`
- GitHub/ref/write/history/CI/security → `GITHUB_RULES.md`
- documentation architecture/readiness → `docs/README.md`
- critical project definition → `.agents/skills/project-definition/SKILL.md`
- specialist planning when triggered → `.agents/skills/project-skill-planner/SKILL.md`
- non-trivial Developing → `.agents/skills/development-brief/SKILL.md`
- project definition scaffolds/current Foundation → `docs/foundation/`
- active continuation → `docs/knowledge/next-action.md`
- actual behavior → current source + matching proof

## Proof boundary

Repository/static evidence proves repository/static claims only. External change-prone facts and runtime/device/visual/audio/model/human-acceptance claims require matching current evidence when material.
