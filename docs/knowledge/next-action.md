# Next Action

## Current Status

```text
TEMPLATE_QUALITY_STATICALLY_READY
```

Canonical authority: **`Local`**.

GitHub distribution remains ready:

```text
default_branch = Local
is_template     = true
```

The retained `main` branch remains intentionally non-authoritative and is not a blocker.

## Quality Remediation Completed

The Final Template Quality & Utility Audit findings have been resolved in the current canonical owners.

### 1. Core policy ownership consolidated

Detailed policy now has one clear owner:

```text
AGENTS.md
→ routing + cross-cutting invariants + specialist-necessity gate

docs/README.md
→ documentation architecture + Foundation/Knowledge + Documentation Readiness

project-definition
→ critical project-definition judgment + user-guidance interaction

project-skill-planner
→ specialist necessity/creation/pruning when triggered

development-brief
→ bounded non-trivial implementation contract/procedure

GITHUB_RULES.md
→ GitHub execution/history/CI/security
```

Other owners keep only the references/guards needed for routing rather than reproducing full policy.

### 2. `CONTEXT.md` compacted

`CONTEXT.md` now contains only stable template identity, repository authority/distribution facts, the short operating model, starter-source exception, owner navigation, and proof boundary.

It no longer duplicates detailed documentation, skill, anti-slop, or work-mode procedures.

### 3. Project Skill Planning made conditional

After Documentation Readiness:

```text
no plausible recurring specialized semantic judgment
→ zero project specialists
→ skip project-skill-planner

specialist need plausible/ambiguous
/ existing specialist set needs review
→ project-skill-planner
```

A simple project no longer pays planner ceremony merely because bootstrap completed.

### 4. Project Definition user-guidance flow added

`project-definition` now explicitly guides interaction as:

```text
recover what is knowable
→ form current model + best recommendation
→ expose only material proposal/unknown/tradeoff
→ ask the smallest grouped high-impact questions only when necessary
→ accept natural-language approval/correction
→ reconcile affected Foundation owners
→ continue until readiness or one exact blocker
```

The agent recommends rather than interrogates and does not ask the user to decide low-impact implementation choices it can own responsibly.

## Static Quality Re-read

The affected owner boundaries were re-read after remediation.

No material issue remains in the audited areas:

- routing vs detailed-procedure ownership;
- Foundation vs Knowledge separation;
- `CONTEXT.md` scope;
- specialist-planner activation;
- critical user-guidance behavior;
- non-trivial development handoff;
- distribution/default/template metadata;
- retained non-authoritative `main` policy.

No new skill, verifier, CI workflow, registry, sample project, architecture layer, or compatibility path is justified by this remediation.

## Proof Boundary

This status means **static template design/utility quality is ready** based on current source-policy inspection.

It does not claim real project-instantiation, runtime, device, visual, audio, model, or human-acceptance proof. Do not begin testing merely for reassurance.

## Active Boundary

There is no active Develop-Builder design/distribution/quality milestone.

## Next Step

**Keep Develop-Builder frozen at the current canonical owners. Reopen it only for a concrete template defect or when the repository owner explicitly selects a real project/bootstrap phase. Do not automatically test, mirror branches, add another audit layer, or create new hardening machinery.**
