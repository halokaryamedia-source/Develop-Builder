# Documentation Architecture

This file is the canonical documentation-system owner for projects created from this starter.

Its job is not to make the repository look documented. Its job is to ensure the project has **enough durable truth to develop correctly**, while preventing duplicate, speculative, ceremonial, or versioned documentation.

## 1. Documentation principle

```text
real responsibility
→ one current owner

no current responsibility
→ no file
```

Documentation is created because a decision, contract, workflow, quality boundary, source authority, or acceptance rule must survive across tasks/sessions—not because a template feels incomplete without another document.

Git history owns ordinary historical versions. Current docs describe current truth.

## 2. Documentation layers

| Layer | Question it answers | Examples |
|---|---|---|
| root `README.md` | What is this project and where do humans start? | concise orientation/navigation |
| `CONTEXT.md` | What stable project/repository facts must a fresh session know? | stable summary + navigation |
| `docs/foundation/` | What durable product/project truth must remain correct? | scope, requirements, boundaries, workflow policy, quality standards |
| `docs/knowledge/` | What current repository navigation/operating memory is needed? | next action, ownership map, source authority, proof state, runbooks |
| `.agents/skills/` | What reusable AI judgment/procedure is needed repeatedly? | non-trivial Developing, earned domain specialist |
| implementation/source | What actually exists/behaves now? | code, assets, configs, tests, runtime source |

Do not use a lower-authority or derived layer to repair missing upstream meaning.

## 3. Project Definition lifecycle

A fresh project does not enter normal product Developing until its current project definition is sufficient.

```text
CURRENT USER INTENT
+ APPROVED DECISIONS
+ AUTHORITATIVE SOURCES
        ↓
SOURCE / REQUIREMENT RECOVERY
        ↓
01 PROJECT OVERVIEW
        ↓
02 PRODUCT REQUIREMENTS
        ↓
FOUNDATION EXPANSION GATE
        ↓
only required durable domain owners
        ↓
DOCUMENTATION READINESS REVIEW
        ↓
CONTEXT.md
stable projection/navigation
        ↓
next-action.md
one real next step / blocker
        ↓
PROJECT DEFINITION READY
        ↓
Developing / Domain Execution
```

`CONTEXT.md` is written/reconciled **after** foundation truth is established. It summarizes and navigates; it does not become a second requirements owner.

`next-action.md` is the final active-continuation result of Project Definition, not a substitute for Project Definition.

## 4. Mandatory project-definition owners

### `docs/foundation/01-project-overview.md`

Owns the durable answer to:

- what the project is;
- who/what consumes it;
- what problem/need it addresses;
- what outcomes/deliverables matter;
- what inputs/source authorities exist;
- what is in scope and explicitly out of scope;
- the high-level product/domain boundaries;
- material constraints;
- success boundary;
- high-impact unknowns.

Do not turn Overview into implementation architecture, task history, or a detailed requirements dump.

### `docs/foundation/02-product-requirements.md`

Owns the durable observable requirements needed to build and accept the product/system.

Depending on the project, it may own:

- product priorities;
- required inputs and source authority;
- expected outputs/deliverables;
- core behavior;
- simple product/user/operational flow;
- scope and exclusions;
- lifecycle/state rules;
- quality constraints;
- data/privacy/security rules;
- integration/interface constraints;
- failure/degradation/recovery behavior;
- persistence/storage rules;
- acceptance/proof requirements;
- current high-impact blocking decisions.

Keep a responsibility here when it remains part of the same product-requirement job. Split only when another durable owner is genuinely needed.

## 5. Foundation Expansion Gate

After Overview + Requirements, inspect the real project and ask:

> Is any durable responsibility important enough that keeping it only as a subsection would mix distinct jobs, hide acceptance rules, or make multiple project areas depend on an unclear contract?

Create an additional foundation owner **only** when the answer is yes.

| Responsibility | Create a dedicated owner when... | Keep inside Overview/Requirements when... | Typical name |
|---|---|---|---|
| Product/domain boundaries | multiple semantic domains have materially different ownership or forbidden cross-repair rules | one product boundary is simple and obvious | `product-boundaries.md` |
| Product/production workflow | multi-stage lifecycle/order materially controls correctness, handoff, or downstream eligibility | flow is short and safely described in Requirements | `product-flow.md` / `production-flow.md` |
| Source intake / source authority | correctness depends on recovering, classifying, reconciling, or normalizing multiple sources | input authority is simple | `source-intake.md` / `source-authority-policy.md` |
| System architecture | architecture decisions materially constrain implementation ownership, runtime boundaries, or acceptance | implementation architecture is not yet decided or is straightforward | `system-architecture.md` |
| Data/state/storage | state ownership, lifecycle, persistence, migration, or destructive behavior is materially complex | storage/state rules are small | `data-state.md` |
| External interface/integration | a public/external contract has independent semantics/compatibility/acceptance | interface details are local implementation detail | `interface-contract.md` |
| Security/privacy | security/privacy is a material cross-cutting contract with independent risk/acceptance | ordinary constraints fit Requirements | `security-privacy.md` |
| Domain craft/quality standard | a domain has recurring quality rules that several tasks/components must follow | a few quality bullets are enough | `<domain>-standard.md` |
| Validation/acceptance | validation has a distinct procedure/evidence model beyond requirement-level acceptance bullets | normal proof criteria are simple | `validation.md` |
| Handoff/delivery/release | downstream handoff or delivery has material independent requirements | output delivery is straightforward | `handoff-delivery.md` / `release-policy.md` |

The filename is secondary. The **responsibility** is what earns the owner.

### Reject a new foundation file when

- it merely makes the folder look complete;
- it repeats content already owned cleanly;
- it describes a possible future feature;
- it exists only because another repository has a similarly named file;
- it would contain mostly placeholders;
- it describes implementation detail that current source should own;
- it is a temporary plan/report rather than durable policy;
- the same consumer/change cadence is already served by an existing owner.

## 6. Split vs keep in the same owner

Keep information in an existing owner when:

```text
same semantic responsibility
+ same primary consumer
+ changes usually move together
+ one file remains understandable
```

Create a new owner when:

```text
distinct semantic responsibility
+ can change independently
+ has its own consumer/acceptance
+ multiple project areas depend on it
+ keeping it in the old owner would mix jobs or create hidden contracts
```

File length alone is not a reason to split. Importance alone is not a reason to split.

## 7. Knowledge growth gate

`docs/knowledge/next-action.md` is the only baseline knowledge owner.

Additional knowledge owners are created only when repository operation becomes materially clearer/safer with them.

| Knowledge owner | Create when... | Do not create when... |
|---|---|---|
| detailed `flow.md` / work-routing reference | root routing is correct but detailed current repository workflow is repeatedly needed | it would only restate `AGENTS.md` |
| `ownership.md` / `implementation-map.md` | finding current source/procedure owners is no longer obvious and repeated search causes error/cost | source ownership is still direct |
| `source-authority.md` | multiple source/state classes create recurring precedence ambiguity | one authority chain is obvious |
| decisions register/records | rationale must survive because the decision is durable, non-obvious, and likely to be revisited | the decision is trivial or current policy already explains enough |
| proof/validation state | repeated proof surfaces need a persistent current evidence boundary across sessions | proof is one-task/ephemeral |
| operations/runbook | a repeatable local/manual/production procedure is risky or easy to execute incorrectly | the procedure is one-off or obvious |
| skill inventory/activation map | multiple earned specialists make selection genuinely ambiguous | only one/few obvious skills exist |
| backlog/future-work owner | non-active future work must be retained separately from current continuation | Git issues/history/current next step are sufficient |
| review evidence index | review evidence has a real retained lifecycle and current-vs-historical distinction | reviews are ephemeral |

Never create all of these during bootstrap.

## 8. Project Definition Readiness Gate

Before **non-trivial product/system Developing** begins for a fresh project or materially new domain, verify the smallest applicable set:

- project purpose and primary consumer are known;
- expected outputs/deliverables are known;
- input/source authority is sufficient for the work;
- scope and explicit non-goals are current;
- observable requirements are current;
- any material product/domain flow is defined;
- any domain boundary that affects ownership/correctness has an owner;
- material architecture/data/security/interface decisions needed **before implementation** are resolved or explicitly blocking;
- quality rules that materially control output are owned;
- acceptance/proof requirements are defined;
- unresolved high-impact decisions are visible rather than invented;
- the Foundation Expansion Gate has been applied;
- `CONTEXT.md` reflects the resulting stable truth;
- `next-action.md` contains one real next step or exact blocker.

If a required item is missing:

```text
DO NOT IMPLEMENT THE UNDEFINED BEHAVIOR
→ return to Plan / Project Definition
→ recover or decide the missing contract
→ update the canonical foundation owner
→ re-check readiness
```

A bounded discovery/prototype may occur before readiness **only** when it is the minimum way to resolve a material unknown. It must not become product implementation by stealth. Its result returns to the correct foundation owner before normal Developing continues.

Direct Bounded Maintenance on an already understood local defect does not require replaying the full Project Definition gate when wider definition cannot change the fix.

## 9. Documentation anti-AI-slop — hard rules

### Do not

- create one document per feature by default;
- create empty/placeholder files for possible future needs;
- create version-suffixed replacement docs instead of updating the current owner;
- create `old`, `legacy`, `new`, backup, migration-copy, or parallel docs without a real external contract;
- duplicate Overview, Requirements, CONTEXT, README, routing, ownership, status, or next-step truth;
- copy the same contract into several files instead of linking to its owner;
- create per-task completion reports/worklogs;
- create decision records for trivial decisions;
- create an ownership map before ownership is materially difficult;
- create an architecture document before architecture is a material project decision;
- create a validation report before persistent proof-state ownership is needed;
- create a specialist because a technology/file type exists;
- retain obsolete docs merely because they once existed;
- interpret “professional documentation” as “more documentation.”

### Do

```text
use existing owner when responsibility fits
→ link instead of copy
→ split only for distinct durable responsibility
→ update current owner in place
→ merge/remove when responsibility disappears
→ let Git history preserve history
```

Every persistent document must materially do at least one of:

1. define a current requirement/decision/contract;
2. prevent a realistic recurring error;
3. establish an authority/ownership boundary;
4. define a workflow/quality/acceptance rule needed by current work;
5. reduce current navigation/coordination complexity;
6. preserve current state/proof that must survive sessions.

Otherwise, do not create it.

## 10. Foundation vs Knowledge vs Skill

```text
project/product fact or durable requirement
→ foundation / project owner

current repository navigation / operating memory
→ knowledge

reusable AI judgment/procedure
→ skill

actual implementation behavior
→ current source + matching proof
```

Skills must not become storage for project-specific facts.

A new specialist is justified only after a real recurring semantic responsibility exists and generic `development-brief` is insufficient. Technology names alone do not create specialists.

## 11. Three archetypes

These are examples of **decision outcomes**, not fixed file sets.

### Simple application

Often sufficient:

```text
01 Project Overview
02 Product Requirements
```

Do not create architecture/flow/validation documents unless the project actually needs independent owners.

### Domain-heavy authoring/tool

May legitimately earn:

```text
Overview
Requirements
domain workflow
one or more domain quality standards
validation policy
```

Only the standards materially needed by current scope are created.

### Multi-stage production system

May legitimately earn:

```text
product/domain boundaries
production flow
source intake/recovery
stage-specific durable contracts
validation/handoff policy
```

Do not force this structure onto a simple application.

## 12. Update and pruning rule

When current truth changes, update the current canonical owner.

When a responsibility disappears:

```text
remove or fold obsolete owner
→ update navigation
→ keep no current compatibility copy unless externally required
→ Git history retains retired rationale
```

Documentation quality is measured by **clarity of current authority and development readiness**, not document count.
