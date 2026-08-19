# Develop-Builder

Develop-Builder is a GitHub Template Repository for a **general project-definition, critical-design, development-governance, and continuity kernel**.

Canonical template and development authority: **`Local`**.

## Core principle

> Use the shortest correct path with sufficient project definition, sufficient evidence, sufficient current context, and sufficient proof.

The starter does not prescribe a programming language, framework, runtime, database, provider system, source-tree layout, release model, production workflow, or project-specialist inventory.

Its job is to help an AI-assisted project:

- determine what is actually worth building;
- challenge unsupported or disproportionate methods instead of defaulting to agreement;
- preserve durable project truth before implementation;
- create only development procedures/owners that real responsibilities require;
- continue across sessions without turning the repository into a documentation archive.

## Repository distribution contract

```text
canonical/default branch = Local
GitHub template mode     = enabled
```

`Local` is the only current template/development authority.

A retained branch such as `main` may remain by repository-owner decision, but it is non-authoritative: it is not a fallback, release/compatibility mirror, second current source, or synchronization target. It may diverge from `Local` without creating a parity repair task.

## Use as a starter

Create a new repository through GitHub's Template mechanism using current `Local`. Do not clone Develop-Builder history or use a retained non-authoritative branch as an alternate bootstrap source.

Canonical pre-development path:

```text
GitHub Template Repository
→ current Local source
→ new project repository
→ project-definition
→ Foundation + Documentation Readiness
→ AGENTS specialist-necessity gate
   ├─ no plausible recurring specialist need → zero project specialists
   └─ plausible/ambiguous need or existing specialist review → project-skill-planner
→ CONTEXT + only earned Knowledge navigation
→ one next-action
→ DEVELOPMENT READY
```

Normal product Developing does **not** begin merely because the repository has a name, an architecture was suggested, or a framework was selected.

## Core workflow capabilities

### Project Definition

`.agents/skills/project-definition/SKILL.md` is the critical semantic front door for new/materially undefined project meaning.

It recovers current evidence, separates facts/decisions/proposals/unknowns, challenges weak direction, guides the user through only material decisions, and persists accepted truth in Foundation.

### Project Skill Planning

`.agents/skills/project-skill-planner/SKILL.md` exists for cases where reusable specialized semantic judgment is plausibly needed or an existing specialist set needs review.

It is **not a mandatory bootstrap step**. `No project specialist required` is a normal result, and simple projects should skip the planner when the need is obviously absent.

### Non-trivial Developing

`.agents/skills/development-brief/SKILL.md` is the front door for non-trivial implementation after the affected Project Definition is ready. It defines the bounded implementation contract, owner set, acceptance criteria, proof budget, and zero/one matching already-earned project specialist.

## Documentation model

`docs/README.md` is the canonical documentation-system and Documentation Readiness owner.

```text
Foundation
→ durable project/product truth

Knowledge
→ current development navigation/context

CONTEXT
→ compact stable cross-session orientation

Skill
→ reusable AI judgment/procedure

Source
→ actual implementation behavior
```

A simple project may legitimately need only Overview + Requirements and zero project specialists. Additional structure is earned by real responsibility, not template aesthetics.

## One current source

Each responsibility has one current canonical owner. Update the current owner directly; do not accumulate `v2`, `_old`, `_new`, `_legacy`, backup, parallel service/state, duplicate docs, or compatibility layers merely to preserve ordinary history. Git history owns ordinary historical versions.

## Navigation

- human/template entry and distribution → `README.md`
- work routing, cross-cutting invariants, skill budget → `AGENTS.md`
- GitHub execution/history/CI/security → `GITHUB_RULES.md`
- stable cross-session orientation → `CONTEXT.md`
- documentation architecture/readiness → `docs/README.md`
- critical Project Definition → `.agents/skills/project-definition/SKILL.md`
- project-specialist planning when triggered → `.agents/skills/project-skill-planner/SKILL.md`
- non-trivial Developing → `.agents/skills/development-brief/SKILL.md`
- project definition scaffolds/current durable project truth → `docs/foundation/`
- active continuation → `docs/knowledge/next-action.md`

## Evidence boundary

Repository/source inspection proves repository/source claims. Change-prone external premises require current authoritative evidence when material. Runtime/device/visual/audio/model/target-machine/human-acceptance claims require matching execution or inspection.

Current continuation is intentionally not duplicated here; use `docs/knowledge/next-action.md`.
