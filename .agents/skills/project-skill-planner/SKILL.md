---
name: project-skill-planner
description: Core capability-planning skill used after Documentation Readiness for a new project or materially new domain. Determine which reusable semantic project specialists are actually needed, distinguish skills from tools/technology/module rules, accept zero specialists as valid, create only justified minimal SKILL.md owners, and remove/fold specialists whose responsibility disappears. Do not implement product behavior or invent specialists from technology names.
---

# Project Skill Planner

Determine the **minimum justified reusable project-specialist set** required to develop the current approved Project Definition.

This skill does not reward a project for having more specialists. A valid result is:

```text
No project specialist required.
Use development-brief alone.
```

Root `AGENTS.md` owns work-mode and per-task skill budget. `project-definition` owns project meaning. `docs/README.md` owns documentation architecture. `development-brief` owns non-trivial Developing. This skill owns the reusable judgment for **whether project-specific semantic specialists need to exist at all**.

## Entry boundary

Use this skill:

- after initial Project Definition passes Documentation Readiness;
- when a materially new project/domain becomes defined and may introduce a recurring semantic development boundary;
- when repeated work shows the existing project-specialist set no longer maps cleanly to current responsibilities;
- when a specialist appears obsolete and may need to be removed/folded.

Do not run it for every development task.

Do not use it to:

- define product requirements;
- choose ordinary implementation details;
- create generic technology experts;
- create test/research/profiling/anti-slop skills merely because those techniques are useful;
- replace nearest `AGENTS.md`, source contracts, official documentation, or normal technical tools.

## Core skill vs project specialist

Core starter skills are workflow/kernel responsibilities:

```text
project-definition
project-skill-planner
development-brief
```

They do not consume the one-project-specialist budget for a bounded Developing task.

A **project specialist** is different:

> reusable semantic judgment/procedure for a recurring project responsibility whose development decisions cannot be represented sufficiently by root policy + Foundation + nearest source/module rules + `development-brief` alone.

“Recurring” may be proven either by observed repeated work **or by current approved Project Definition showing that the same semantic judgment will be required across multiple distinct development slices**. Do not require historical repetition when the approved project structure already proves the recurrence.

Examples may include desktop runtime/state integration, visual UI composition, local AI runtime, physical audio routing, release packaging, modelling judgment, or another project-specific semantic boundary.

The example name is irrelevant unless the responsibility exists in the current project.

## Input authority

Use the smallest current evidence needed:

```text
approved Foundation / Project Definition
→ current domain boundaries / flow / quality / acceptance owners
→ current source/implementation ownership if the project already exists
→ existing project specialist skills, if any
→ current navigation only when ownership is ambiguous
```

Do not derive specialist needs from repository folder names or dependency lists alone.

## Semantic responsibility discovery

Identify recurring development responsibilities implied by the approved Project Definition.

For each candidate responsibility ask:

1. What exact semantic/acceptance boundary recurs or is explicitly required to recur by current project scope?
2. What decisions require specialized reusable judgment?
3. Which current owner would still own the problem if the implementation language/framework changed?
4. Can `development-brief` + Foundation + nearest `AGENTS.md`/source contract already handle it safely?
5. Is this actually a technology/tool concern rather than a semantic project responsibility?
6. Is the responsibility one-off, or will current approved scope require the same judgment across multiple development slices?

Do not route by filenames such as `.py`, `.rs`, `.ts`, `.svelte`, `.json`, or by named libraries/providers.

## Specialist creation gate

Create a new project specialist only when the current evidence supports the material conditions below:

```text
a real current semantic responsibility exists
+ observed work or approved scope proves recurring use across multiple development slices
+ it has distinct judgment / acceptance rules
+ generic development-brief is insufficient by itself
+ nearest project/module rules do not already own the reusable procedure
+ responsibility remains meaningful if implementation technology changes
+ a persistent skill reduces repeated reasoning/error/coordination
+ boundary can be stated clearly enough to prevent overlap
+ a current approved project consumer/use exists
+ no existing specialist already owns it
```

If these conditions are not met:

```text
DO NOT CREATE A SKILL
```

Importance, file count, code complexity, team size, or impressive technology names do not satisfy the gate by themselves.

Do not infer recurrence from vague future possibilities. It must follow from current approved project scope or observed work.

## Selection verdict

For each candidate use one result:

```text
NO SKILL
→ root/development-brief/module rules are sufficient

USE EXISTING
→ current specialist already owns the boundary

CREATE
→ distinct recurring semantic responsibility passes the creation gate

REFINE / MERGE
→ current specialist boundary is wrong/overlapping and should be corrected in place

REMOVE / FOLD
→ no live distinct responsibility remains

BLOCKED
→ responsibility cannot be classified responsibly from current project definition/ownership evidence
```

Do not create another skill to avoid resolving overlap between current owners.

## Distinguish skill from tool/helper

The following are **not automatically project specialists**:

- programming languages/frameworks;
- linters/type checkers/formatters;
- testing frameworks;
- browser automation;
- profilers/benchmarks;
- current official documentation helpers;
- research/search tools;
- migration utilities;
- build/package managers;
- anti-slop/reviewer personas;
- generic “architect”, “researcher”, “tester”, or “code quality” roles.

Use this rule:

```text
recurring semantic project judgment
→ possible specialist

technical utility / current documentation / execution aid
→ tool/helper

project fact / requirement
→ Foundation

current owner/navigation context
→ Knowledge when earned

module/package procedure
→ nearest AGENTS/source owner
```

## One bounded task still uses at most one project specialist

The project may legitimately have several specialists available across different responsibilities.

But normal non-trivial Developing remains:

```text
development-brief
+
zero or one matching project specialist
```

If a requested slice genuinely spans two independent specialist acceptance boundaries, split/reframe the work rather than stacking specialists automatically.

## Candidate analysis

Before authoring a skill, define internally:

```text
Semantic responsibility
Current approved consumers / development slices
Activation trigger
Do-not-use boundary
Why development-brief/module rules are insufficient
Canonical project inputs/owners
Reusable judgments/procedure
Acceptance POV
Proof boundary
Likely source/module handoff
Overlap check against existing specialists
Removal/fold condition
```

Do not create a persistent skill-plan, matrix, registry, or report merely to store this analysis.

## Skill authoring contract

For a candidate that passes `CREATE`, author the smallest useful:

```text
.agents/skills/<semantic-responsibility>/SKILL.md
```

A project-specialist skill should normally contain:

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

It must not duplicate detailed product requirements from Foundation or exact source/file routing that belongs in current source/Knowledge/nearest `AGENTS.md`.

Prefer semantic names such as:

```text
desktop-runtime-development
windows-audio-runtime-development
release-packaging-development
```

when those responsibilities are real.

Reject names like:

```text
python-expert
rust-expert
frontend-expert
testing-expert
researcher
anti-slop-reviewer
```

unless a truly distinct semantic responsibility—not the technology label—can be stated and justified.

## Routing registration

After specialist creation, register only the minimum current routing needed so an agent can select it correctly.

Preferred order:

```text
root / nearest AGENTS.md
→ enough routing while selection remains obvious

multiple earned specialists + repeated selection ambiguity
→ Knowledge may earn a compact skill activation/navigation map through docs/README.md Knowledge Navigation Gate
```

Do not pre-create a skill registry, skill map, activation matrix, or `docs/knowledge/skills/` folder during bootstrap merely because specialists might exist.

## Existing specialist review

When current specialists exist, check for:

- duplicate or overlapping semantic ownership;
- technology-based rather than responsibility-based boundaries;
- skills that merely restate Foundation or `development-brief`;
- specialists with no recurring current consumer;
- one specialist trying to own several independent acceptance boundaries;
- stale routing after the project changed.

Correct the current skill in place when possible.

Do not create `new-<skill>`, `legacy-<skill>`, versioned skills, compatibility wrappers, or replacement copies.

## Pruning

A specialist is not permanent merely because it was once useful.

If its distinct responsibility disappears or folds into another current owner:

```text
remove/fold specialist
→ update minimum routing/navigation
→ do not retain deprecated/legacy copy
→ Git history owns retired history
```

If the responsibility remains but scope changes, update the current skill directly.

## User interaction

Skill architecture is normally an implementation/governance responsibility of the agent, not a questionnaire for the user.

Ask the user only when specialist boundaries depend on an unresolved **product/domain decision** that the Project Definition did not settle. In that case, return to `project-definition` / Plan instead of guessing project meaning inside skill planning.

Do not ask the user to choose between technology-named specialist files.

## Hard anti-slop rules

Do not:

- reward complex projects with more skills by default;
- make a skill for every subsystem/folder/language;
- create placeholder skills for future work;
- create specialist skills from one difficult task;
- infer future recurrence from vague architecture speculation;
- create overlapping semantic skills and solve selection with a router;
- create a skill map before selection is genuinely ambiguous;
- treat tools/research/testing as extra specialist personas;
- copy Foundation requirements into skill files;
- put current implementation maps into skills;
- preserve obsolete skills as legacy/deprecated current source;
- run testing merely to justify a skill whose responsibility is not semantically established.

## Completion

Skill planning is complete when:

- current recurring semantic development responsibilities have been identified to sufficient depth from approved scope and/or observed work;
- every current project specialist has one distinct justified responsibility;
- zero unnecessary candidate specialists remain;
- any justified new skills are authored minimally;
- obsolete/overlapping specialist owners are corrected or removed when in scope;
- routing remains the smallest sufficient mechanism;
- no project-management/skill-registry layer was created without need.

Then return control to bootstrap/Project Definition lifecycle so `CONTEXT.md`, any earned Knowledge navigation, and `next-action.md` can reflect the final current development capability landscape. STOP.
