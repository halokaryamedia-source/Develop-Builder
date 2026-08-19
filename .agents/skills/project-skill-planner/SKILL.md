---
name: project-skill-planner
description: Project-specialist planning capability used only when AGENTS specialist-necessity routing finds plausible or ambiguous recurring specialized semantic judgment, or when an existing specialist set needs overlap/sufficiency/pruning review. Determine the minimum justified reusable project-specialist set, distinguish skills from tools/technology/module rules, accept zero specialists as valid, create only justified minimal SKILL.md owners, and remove/fold obsolete specialists. Do not implement product behavior.
---

# Project Skill Planner

Determine the **minimum justified reusable project-specialist set** for the current approved Project Definition.

This skill is not a mandatory bootstrap ceremony. A valid outcome is:

```text
No project specialist required.
Use development-brief alone.
```

`AGENTS.md` owns whether this planner is invoked and the per-task skill budget. `project-definition` owns project meaning. `docs/README.md` owns documentation/readiness. `development-brief` owns non-trivial implementation.

## Activation boundary

Load this skill only when at least one current condition is true:

```text
approved project scope plausibly requires recurring specialized semantic judgment
that Foundation + development-brief + nearest AGENTS/source rules may not cover

OR specialist need is genuinely ambiguous

OR existing project specialists need overlap, sufficiency, routing, or pruning review
```

Do **not** load it merely because Documentation Readiness passed, a project has several technologies/folders, implementation looks difficult, or bootstrap is occurring.

If the need is obviously absent:

```text
zero project specialists
→ skip this skill
```

## What counts as a project specialist

A project specialist is:

> reusable semantic judgment/procedure for a recurring project responsibility whose development decisions cannot be represented sufficiently by Foundation + root/nearest rules + `development-brief` alone.

“Recurring” may be demonstrated by observed repeated work or by approved scope clearly requiring the same semantic judgment across several distinct development slices. Vague future possibility is not recurrence.

A responsibility should remain meaningful even if the implementation language/framework changes.

Examples may include desktop runtime/state integration, visual UI composition, local AI runtime, physical audio routing, release packaging, modelling judgment, or another project-specific semantic boundary—but only when that responsibility actually exists.

## Input authority

Use the smallest current evidence needed:

```text
approved Foundation / Project Definition
→ current domain boundaries / flow / quality / acceptance owners
→ current source ownership when the project already exists
→ existing project specialists, if any
→ current navigation only when ownership is ambiguous
```

Do not derive specialist needs from dependency lists, filenames, directories, or technology names alone.

## Specialist creation gate

Create a new project specialist only when current evidence supports the material conditions below:

```text
real current semantic responsibility
+ recurring use proven by observed work or approved scope
+ distinct reusable judgment / acceptance rules
+ development-brief alone is insufficient
+ nearest project/module rules do not already own the procedure
+ responsibility remains meaningful across implementation technology changes
+ persistent skill reduces repeated reasoning/error/coordination
+ boundary is clear enough to avoid overlap
+ current approved consumer/use exists
+ no existing specialist already owns it
```

If these conditions are not met:

```text
DO NOT CREATE A SKILL
```

Importance, code complexity, team size, file count, or impressive technology names do not satisfy the gate by themselves.

## Candidate classification

For each real candidate use one result:

```text
NO SKILL
→ Foundation/development-brief/module rules are sufficient

USE EXISTING
→ current specialist already owns the boundary

CREATE
→ distinct recurring semantic responsibility passes the gate

REFINE / MERGE
→ current specialist boundary is wrong or overlapping

REMOVE / FOLD
→ no live distinct responsibility remains

BLOCKED
→ responsibility cannot be classified responsibly from current project evidence
```

Do not create another specialist to avoid resolving overlap between existing owners.

## Skill vs tool/helper vs project owner

The following are not automatically project specialists:

- programming languages/frameworks/libraries;
- linters/type checkers/formatters;
- testing/browser automation/profiling/benchmark tools;
- official documentation helpers;
- research/search tools;
- build/package managers;
- migration utilities;
- generic “architect”, “researcher”, “tester”, “reviewer”, or “code quality” personas.

Use this separation:

```text
recurring semantic project judgment
→ possible project specialist

technical utility / execution aid / current external docs
→ tool/helper

project fact / requirement
→ Foundation

current navigation / owner map
→ Knowledge when earned

module/package procedure
→ nearest AGENTS/source owner
```

## One bounded Developing task still uses at most one project specialist

The project may have several specialists available across different responsibilities, but normal non-trivial Developing remains:

```text
development-brief
+
zero or one matching project specialist
```

If one request genuinely spans two independent specialist acceptance boundaries, split/reframe the work instead of stacking specialists automatically.

## Candidate analysis before authoring

For a candidate that may pass `CREATE`, establish internally:

```text
Semantic responsibility
Current approved consumers / development slices
Activation trigger
Do-not-use boundary
Why generic current owners are insufficient
Canonical project inputs/owners
Reusable judgments/procedure
Acceptance POV
Proof boundary
Implementation/module handoff
Overlap check
Removal/fold condition
```

Do not create a persistent skill plan, registry, matrix, or report to store this analysis.

## Skill authoring contract

A justified new project specialist uses the smallest useful:

```text
.agents/skills/<semantic-responsibility>/SKILL.md
```

It should normally contain:

```text
frontmatter name + precise activation description
Purpose / semantic responsibility
Use when
Do not use when
Authority / canonical inputs
Reusable judgment / procedure
Acceptance boundary
Proof boundary
Handoff to current implementation/module owners
STOP boundary
```

It must not duplicate product requirements from Foundation or current source/file routing from Knowledge/nearest `AGENTS.md`.

Prefer semantic names tied to actual responsibility. Reject technology/persona names such as `python-expert`, `rust-expert`, `frontend-expert`, `testing-expert`, `researcher`, or `anti-slop-reviewer` when the name is only a technology/role label.

## Routing registration

After creating/refining/removing specialists, register only enough current routing for correct selection.

```text
root / nearest AGENTS.md
→ sufficient while specialist selection is obvious

multiple earned specialists + repeated real selection ambiguity
→ Knowledge may earn a compact activation/navigation map via docs/README.md
```

Do not pre-create a skill registry, activation matrix, or `docs/knowledge/skills/` folder merely because specialists may exist.

## Existing specialist review and pruning

When current specialists exist, inspect for duplicate/overlapping semantic ownership, technology-based boundaries, skills that merely restate Foundation/development-brief, no recurring consumer, one skill owning several independent acceptance boundaries, or stale routing.

Correct the current skill in place when possible. Do not create `new-`, `legacy-`, versioned, deprecated, or compatibility wrapper skills.

If a distinct responsibility disappears:

```text
remove/fold specialist
→ update minimum routing/navigation
→ Git history retains retired history
```

## User interaction

Skill architecture is normally an agent governance decision, not a user questionnaire.

Ask the user only when specialist classification depends on an unresolved **project/domain decision**. In that case return to `project-definition` / Plan rather than guessing project meaning inside skill planning.

Do not ask the user to choose between technology-named specialist files.

## Completion

Skill planning is complete when:

- every current specialist has one distinct justified recurring responsibility;
- no unnecessary candidate specialists remain;
- justified new skills are minimal;
- obsolete/overlapping skills are corrected or removed when in scope;
- routing remains the smallest sufficient mechanism;
- no registry/project-management layer was added without need.

Return control to `AGENTS.md` routing so CONTEXT, earned Knowledge navigation, and `next-action.md` reflect the final current capability landscape. STOP.
