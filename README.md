# Develop-Builder

Develop-Builder is the source starter for a **general project-definition, development-governance, and continuity kernel**.

Development authority: **`Local`**.

## Core principle

> Use the shortest correct path with sufficient project definition, sufficient context, and sufficient proof.

The starter does not prescribe a programming language, framework, runtime, database, release model, provider system, or source-tree layout. It provides the operating structure needed to define a project before implementation, develop it without losing context, and grow documentation only when a real responsibility earns an owner.

## One current source

Each responsibility has one current canonical owner.

When a requirement, rule, workflow, or implementation changes:

```text
find current owner
→ update it in place
→ update required dependents
→ remove superseded current path/state when safe
→ prove the final state
→ STOP
```

Git history owns ordinary history. Do not preserve obsolete current source as versioned generations, legacy copies, parallel owners, or compatibility paths merely to avoid replacing it cleanly.

A compatibility or migration boundary exists only when a current external contract genuinely requires coexistence.

## Use as a starter

Use a **clean snapshot of the current starter tree** in a new repository. Do not carry Develop-Builder Git history into the new project's history.

```text
current starter tree
→ new empty repository
→ establish `Local` as working authority
→ read `docs/README.md`
→ Bootstrap Instantiation + Project Definition
→ Documentation Readiness gate
→ one coherent first project commit
```

Normal product Developing does **not** begin merely because the repository has a name and two short documents. The project must first define the durable truth required for the work it is about to perform.

## Documentation entrypoint

`docs/README.md` is the canonical documentation-system owner. It explains:

- what must be defined before Developing;
- what belongs in `docs/foundation/` vs `docs/knowledge/`;
- when Overview + Requirements are sufficient;
- when another durable domain document is required;
- when a new document would be AI-slop and must not be created;
- the Project Definition / Documentation Readiness gate.

## Navigation

- project bootstrap, work routing, source finalization → `AGENTS.md`
- GitHub execution/history/safety → `GITHUB_RULES.md`
- documentation architecture / pre-development readiness → `docs/README.md`
- stable project orientation after definition → `CONTEXT.md`
- project overview scaffold/current owner → `docs/foundation/01-project-overview.md`
- product requirements scaffold/current owner → `docs/foundation/02-product-requirements.md`
- active continuation → `docs/knowledge/next-action.md`
- non-trivial Developing front door → `.agents/skills/development-brief/SKILL.md`

## Evidence boundary

Repository/source inspection proves repository/source claims. Hosted execution proves only what it actually runs. Runtime, device, visual, audio, model, target-machine, and human-acceptance claims require matching evidence.

Current continuation is intentionally not duplicated here; use `docs/knowledge/next-action.md`.
