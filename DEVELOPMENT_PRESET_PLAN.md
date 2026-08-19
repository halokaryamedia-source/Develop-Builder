# Develop-Builder — Implementation Handoff

Status: **Phase 1 Core Bootstrap implemented**  
Working authority: **`Local`**

This file is a temporary implementation handoff for Develop-Builder itself. It is **not** a second governance/continuation authority and is not copied into instantiated projects. Durable rules now live in the Core Bootstrap owners; active continuation lives only in `docs/knowledge/next-action.md`. Detailed planning rationale remains available in Git history.

## Architecture outcome

The reference audit of BuildIT, TranslateIT, and PRD-Creator resolved the general preset around one primary principle:

> **Use the shortest correct path with sufficient context and sufficient proof.**

Anti-overdevelopment means proportional complexity, not minimal file/line count. Simple bounded work must stay direct; materially uncertain, risky, cross-owner, or hard-to-prove work must escalate only as far as necessary.

AI-slop is rejected when an element does not materially change a necessary decision, prevent a realistic error, satisfy a real requirement, reduce current total complexity, or prove a required claim.

## Phase 1 baseline

The Core Bootstrap is intentionally limited to nine persistent files:

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

Promoted governance such as detailed routing maps, ownership indexes, automated governance verification, decision/backlog/review systems, experiments, workspace continuity, additional specialists, product CI/release workflows, and runtime/source architecture remains absent until a demonstrated responsibility earns it.

## Frozen design decisions

- Direct Bounded Path is a short route inside Developing/Maintenance, not another work mode.
- Direct work never bypasses exact repo/ref, root safety, material contracts, affected callers, or required proof.
- Non-trivial escalation is based on material uncertainty/impact/risk/coordination/proof difficulty, not code/file/line count.
- The invariant is one canonical owner per responsibility; one coherent task may touch the smallest necessary owner set.
- Ordinary additions use a simple need/location/form check; only high-cost durable architecture receives an extended justification gate.
- Abstraction must provide a required capability or reduce total current complexity after its own costs are counted.
- Optional structures must be removable again when their responsibility disappears.
- Template verification and instantiated-project verification are different proof surfaces; the pristine template shape must not become a permanent constraint on mature projects.

## Remaining implementation phases

```text
Phase 2 — decide whether Develop-Builder template verification is currently justified
Phase 3 — direct-path/escalation assumption audit across materially different project contexts
Phase 4 — complexity/pruning audit
Phase 5 — freeze preset v1 and retire/reduce temporary implementation planning state
```

Do not infer active work from this list. `docs/knowledge/next-action.md` is the only active continuation owner.
