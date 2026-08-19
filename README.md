# Develop-Builder

Develop-Builder is the source starter for a **general development governance and continuity kernel**. It exists to make project development safe and resumable without turning simple work into a complicated process.

Development authority: **`Local`**.

## Core principle

> Use the shortest correct path with sufficient context and sufficient proof.

The starter standardizes how work is routed, grounded, owned, continued, verified, and stopped. It does not prescribe product architecture, framework, runtime, database, release model, provider system, or source-tree layout.

## One current source

The current repository source is the only starter baseline.

Do not create or preserve artificial generations such as `v1`, `v2`, `new`, `legacy`, `old`, `final2`, compatibility copies, parallel owner files, or replacement folders merely to avoid updating the canonical source.

When a rule or implementation changes, update the canonical owner and remove the superseded current path/state when safe. Git history preserves history. A real externally defined product/API/schema version may exist only when the product contract itself requires that versioning; AI workflow evolution is not a reason to version current owners.

## Use as a starter

For a new project, use a **clean snapshot of the current starter tree**, not Develop-Builder Git history:

```text
current starter tree
→ new empty repository
→ establish `Local` as working authority
→ Bootstrap Instantiation in AGENTS.md
→ one coherent first project commit
```

Do not clone Develop-Builder history and treat it as project history.

Bootstrap is complete when README/CONTEXT/foundation/next-action describe the new project, no Develop-Builder project state leaks into current truth, generic kernel files remain identity-neutral, unknowns stay explicit, and exactly one real project next step exists.

## Navigation

- AI work routing, Bootstrap Instantiation, source finalization, and path selection → `AGENTS.md`
- GitHub execution/history/safety → `GITHUB_RULES.md`
- stable starter/project orientation → `CONTEXT.md`
- durable project intent → `docs/foundation/01-project-overview.md`
- durable intended behavior → `docs/foundation/02-product-requirements.md`
- active continuation → `docs/knowledge/next-action.md`
- non-trivial Developing front door → `.agents/skills/development-brief/SKILL.md`

## Evidence boundary

Repository/source inspection proves repository/source claims. Hosted execution proves only what it actually runs. Runtime, device, visual, audio, model, target-machine, and human-acceptance claims require matching evidence.

Current continuation is intentionally not duplicated here; use `docs/knowledge/next-action.md`.
