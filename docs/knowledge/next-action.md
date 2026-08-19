# Next Action

## Current Status

```text
QUALITY_AUDIT_REMEDIATION_REQUIRED
```

Canonical authority: **`Local`**.

GitHub template distribution remains ready:

```text
default_branch = Local
is_template     = true
```

The repository-level distribution contract is not the active problem. The retained `main` branch remains non-authoritative and is not a blocker.

## Final Template Quality & Utility Audit

A full static quality/utility audit of the current template found **no critical architecture failure**, but found four material usability/maintainability issues that should be corrected before calling the template final-quality ready.

### 1. HIGH — Core policy duplication / drift risk

Detailed project-definition, skill-planning, evidence, anti-slop, and STOP rules are repeated across `AGENTS.md`, `docs/README.md`, core skills, and `development-brief` beyond what routing guards require.

Required direction:

```text
AGENTS.md
→ routing + cross-cutting invariants only

docs/README.md
→ documentation/readiness contract

project-definition
→ critical project-definition procedure

project-skill-planner
→ specialist necessity/creation/pruning procedure

development-brief
→ bounded non-trivial implementation procedure

GITHUB_RULES.md
→ GitHub execution discipline
```

Keep short references/guards where needed, but remove duplicated detailed policy that creates multi-owner synchronization obligations.

### 2. HIGH — `CONTEXT.md` is not compact enough

`CONTEXT.md` currently repeats distribution rules, skill responsibilities, documentation model, work modes, anti-slop rules, evidence rules, and navigation already owned elsewhere.

Required direction:

- keep stable project/template identity;
- keep current authority/distribution facts;
- keep only the smallest stable orientation and owner navigation;
- link to detailed owners instead of reproducing their rules.

### 3. HIGH — Project Skill Planning is mandatory even when obviously unnecessary

The current bootstrap sequence always invokes `project-skill-planner` after Documentation Readiness. This creates avoidable ceremony for simple projects even though `No project specialist required` is valid.

Required direction:

```text
Documentation Readiness
→ cheap specialist-necessity gate

no plausible recurring specialized semantic judgment
→ zero project specialists
→ do not load project-skill-planner

specialist need plausible / ambiguous / existing specialists need review
→ project-skill-planner
```

The planner remains a core capability, but invocation becomes evidence-triggered rather than universal ceremony.

### 4. MEDIUM — `project-definition` lacks an explicit user-guidance interaction contract

The critical reasoning model is strong, but the skill does not yet define a sufficiently explicit conversational path for guiding a user from a vague idea to approved Foundation without turning the process into a checklist/questionnaire.

Required direction:

```text
recover what is already knowable
→ form current project model + recommended direction
→ expose only material uncertainty/proposals
→ ask the smallest high-impact question set when genuinely needed
→ accept natural-language approval/correction
→ reconcile affected Foundation owners
→ continue until readiness or exact blocker
```

The agent should recommend rather than interrogate, and should not require confirmation for low-impact implementation choices it can own responsibly.

## Areas That Passed

No material correction is currently justified for:

- GitHub distribution/default/template settings;
- `GITHUB_RULES.md` core/conditional execution model;
- Foundation vs Knowledge semantic separation;
- Overview / Product Requirements scaffold coverage;
- evidence provenance/freshness/negative-requirement rules;
- project-specialist semantic creation criteria themselves;
- single current source / no legacy-generation policy;
- retained `main` branch policy.

## Proof Boundary

This is a **static product-quality / utility audit**. It does not claim runtime/template-instantiation proof and does not authorize testing merely for reassurance.

No new skill, verifier, CI workflow, registry, sample project, or architecture layer is justified by the findings.

## Next Step

**Perform one coherent quality-remediation pass focused on the four findings above: reduce duplicate detailed policy, compact `CONTEXT.md`, make specialist planning conditional for simple projects, and add a concise user-guidance/approval flow to `project-definition`. Do not add new capabilities or begin testing during this remediation.**
