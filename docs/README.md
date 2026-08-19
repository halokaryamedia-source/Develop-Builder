# Documentation Architecture

This file is the canonical documentation-system owner for projects created from this starter.

Its job is to ensure the project has **enough durable truth to develop correctly**, **enough traceable evidence to know why that truth is trusted**, and **enough current navigation/context to continue development safely**—without duplicate, speculative, ceremonial, historical, or versioned documentation.

Detailed critical project-definition judgment lives in `.agents/skills/project-definition/SKILL.md`. Project-specialist planning lives in `.agents/skills/project-skill-planner/SKILL.md`.

## 1. Documentation principle

```text
real responsibility
→ one current owner

no current responsibility
→ no file
```

Documentation exists because a decision, requirement, workflow, quality boundary, source authority, evidence basis, navigation need, or acceptance rule must survive across tasks/sessions—not because a template looks incomplete without another document.

Git history owns ordinary historical versions. Current docs describe current truth.

## 2. Documentation layers

| Layer | Question it answers |
|---|---|
| root `README.md` | What is this project and where do humans start? |
| `CONTEXT.md` | What stable project/repository facts must a fresh session know? |
| `docs/foundation/` | What durable project/product truth must remain correct, and what material evidence/authority supports factual premises? |
| `docs/knowledge/` | How does an AI/developer navigate and resume the project currently being developed? |
| `.agents/skills/` | What reusable AI judgment/procedure is needed repeatedly? |
| implementation/source | What actually exists/behaves now? |

### Foundation vs Knowledge

```text
FOUNDATION
= durable specification / definition
= what the project must remain or become

KNOWLEDGE
= navigation + current development context
= how to find, understand, and resume what is being developed now
```

`docs/knowledge/` is **not a generic project-management archive**. Historical rationale, old reviews, completed work, inactive plans, and arbitrary backlog do not belong there merely because they may be useful someday.

Do not use a lower-authority or derived layer to repair missing upstream meaning.

## 3. Pre-development lifecycle

A fresh project does not enter normal product Developing merely because repository bootstrap is complete.

```text
CURRENT USER INTENT
+ APPROVED DECISIONS
+ AUTHORITATIVE SOURCES
        ↓
project-definition
critical evidence recovery + direction judgment
        ↓
01 PROJECT OVERVIEW
        ↓
02 PRODUCT REQUIREMENTS
        ↓
FOUNDATION EXPANSION GATE
        ↓
only required durable domain owners
        ↓
EVIDENCE / COHERENCE READINESS
        ↓
DOCUMENTATION READINESS
        ↓
project-skill-planner
zero or more justified project specialists
        ↓
CONTEXT.md
stable projection/navigation
        ↓
KNOWLEDGE NAVIGATION GATE
only current navigation actually needed
        ↓
next-action.md
one real next step / blocker
        ↓
DEVELOPMENT READY
```

`project-definition` is the semantic procedure; it does not replace Foundation. Approved current meaning is persisted in Foundation.

`project-skill-planner` does not change project requirements and does not create documentation merely to describe skills.

`CONTEXT.md` is reconciled after durable project truth and required initial capability planning are established. It summarizes/navigates; it does not become a second requirements owner.

`next-action.md` is the final active-continuation result, not a substitute for Project Definition.

## 4. Mandatory project-definition owners

### `docs/foundation/01-project-overview.md`

Owns the durable answer to:

- what the project is;
- who/what consumes it;
- what problem/need it addresses;
- what outcomes/deliverables matter;
- what source classes/decisions may establish project truth;
- what is in scope and explicitly out of scope;
- high-level product/domain boundaries;
- material constraints;
- success boundary;
- high-impact unknowns.

Do not turn Overview into implementation architecture, task history, or a detailed requirements dump.

### `docs/foundation/02-product-requirements.md`

Owns durable observable requirements needed to build and accept the product/system, including material exclusions/removals.

Depending on the project, it may own priorities, required inputs, outputs, core behavior, simple flow, lifecycle/state, quality, data/privacy/security, interfaces, failure/recovery, persistence, acceptance/proof, and current blocking decisions.

Keep a responsibility here when it remains part of the same product-requirement job. Split only when another durable owner is genuinely needed.

## 5. Evidence traceability and source coverage

Foundation is authoritative project meaning, but **source-backed factual premises must remain traceable enough to audit/revalidate**.

### Source-coverage rule

Before treating a material project direction as grounded:

```text
known potentially authoritative sources for current scope identified
→ each inspected to the depth that can change current decisions
→ unavailable/unread material authority identified
→ partial coverage never presented as complete evidence
```

Targeted inspection is valid for a targeted boundary. A full-source read is unnecessary when unseen portions cannot reasonably change the decision.

If a known unread/unavailable source could materially change scope, feasibility, requirement meaning, risk, compatibility, or acceptance, the affected claim remains `UNKNOWN` or explicitly blocked.

### Provenance rule

When a material source-backed fact shapes Foundation, retain the **smallest useful source identity** in the affected Foundation owner, for example:

```text
repository path / commit / revision
source title / relevant section
official URL / standard identifier
version / platform / model when material
verification/access date when change-prone
```

Do not create a source inventory for a few simple references. If source intake/reconciliation itself becomes a distinct durable responsibility, use the Foundation Expansion Gate.

### Freshness rule

Foundation records accepted project meaning. It does **not** permanently prove that a change-prone external fact remains current.

For facts such as current platform/library/provider support, pricing, regulation, compatibility, limits, or another unstable premise:

- record enough version/date/source context to know what was verified when material;
- revalidate current authoritative evidence when later work materially depends on the premise and staleness is plausible;
- do not repeatedly re-research stable facts for ceremony.

### Negative-requirement rule

Explicit `remove`, `no longer use`, `do not use`, `must not`, `only`, `replaced by`, and scoped exclusions are first-class project meaning.

Do not reintroduce them because an old implementation, reference project, framework convention, or compatibility instinct contains them. Do not broaden a negative statement beyond its actual scope.

## 6. Foundation Expansion Gate

After Overview + Requirements, ask:

> Is any durable responsibility important enough that keeping it only as a subsection would mix distinct jobs, hide acceptance rules, or make multiple project areas depend on an unclear contract?

Create an additional Foundation owner **only** when yes.

| Responsibility | Dedicated owner is justified when... | Typical name |
|---|---|---|
| Product/domain boundaries | multiple semantic domains have materially different ownership or forbidden cross-repair rules | `product-boundaries.md` |
| Product/production workflow | multi-stage order materially controls correctness/handoff/eligibility | `product-flow.md` / `production-flow.md` |
| Source intake / authority | recovering/classifying/reconciling multiple sources is itself a durable contract | `source-intake.md` / `source-authority-policy.md` |
| System architecture | architecture decisions materially constrain ownership/runtime/acceptance | `system-architecture.md` |
| Data/state/storage | state ownership/lifecycle/persistence/migration/destructive behavior is materially complex | `data-state.md` |
| External interface | public/external contract has independent semantics/compatibility/acceptance | `interface-contract.md` |
| Security/privacy | cross-cutting security/privacy contract has independent risk/acceptance | `security-privacy.md` |
| Domain quality standard | recurring quality rules control several tasks/components | `<domain>-standard.md` |
| Validation/acceptance | validation has a distinct procedure/evidence model | `validation.md` |
| Handoff/delivery/release | downstream handoff/delivery has material independent requirements | `handoff-delivery.md` / `release-policy.md` |

Reject a new Foundation file when it merely makes the folder look complete, repeats an existing owner, describes possible future work, contains placeholders, copies another repo's shape, stores temporary task state, or belongs in implementation/source.

## 7. Split vs keep in the same owner

Keep information together when:

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
+ several project areas depend on it
+ keeping it together would mix jobs or hide contracts
```

File length or importance alone is not a reason to split.

## 8. Foundation coherence rule

One approved/recovered decision may affect several Foundation owners.

```text
identify every affected current Foundation owner
→ update them coherently
→ remove/replace superseded conflicting meaning
→ leave no pending old/new alternatives
```

A contradiction between current Foundation owners is a **Documentation Readiness defect**.

Do not preserve contradictory current meaning through compatibility notes, duplicate requirements, or “old/new” docs. Git history owns retired meaning.

## 9. Knowledge Navigation Gate

`docs/knowledge/next-action.md` is the only baseline Knowledge owner.

Knowledge grows only to make the **currently developing repository** easier and safer to navigate, understand, or resume.

Before adding a Knowledge owner require:

```text
current navigation/context problem exists
+ existing root/Foundation/source/next-action owner does not answer it cleanly
+ information must survive across tasks/sessions
+ new owner reduces repeated search, ambiguity, or resume error
```

Potential earned owners include current implementation-flow maps, ownership/implementation maps, current source-precedence navigation, proof-surface navigation, risky repeatable runbooks, or a skill activation map when multiple earned specialists make selection genuinely ambiguous.

Decision/review/backlog files are not Knowledge merely because they contain information. They require a live current-navigation responsibility.

### Knowledge separation

```text
active resume point
→ next-action.md

current development navigation / owner map / source map / implementation flow
→ earned Knowledge owner

durable project meaning
→ Foundation

reusable semantic procedure
→ Skill

actual behavior
→ source + proof

ordinary completed history / retired rationale
→ Git history / issues / PRs
```

Never create all possible Knowledge owners during bootstrap. Never broad-read all Knowledge owners during normal work.

## 10. Documentation Readiness Gate

Before **non-trivial product/system Developing** begins for a fresh project or materially new domain, verify the smallest applicable set:

- purpose and primary consumer are known;
- expected outputs/deliverables are known;
- relevant input/source authority is sufficient;
- known material authority has been inspected to sufficient depth for current scope;
- material source-backed premises are traceable enough to re-open/revalidate;
- scope, explicit non-goals, negative/removal requirements are current;
- observable requirements are current;
- any material product/domain flow is defined;
- any domain boundary affecting ownership/correctness has an owner;
- material architecture/data/security/interface decisions needed before implementation are resolved or explicitly blocking;
- quality rules materially controlling output are owned;
- acceptance/proof requirements are defined;
- unresolved high-impact decisions remain visible rather than invented;
- affected Foundation owners are mutually coherent;
- Foundation Expansion Gate has been applied.

If a required item is missing:

```text
DO NOT IMPLEMENT THE UNDEFINED BEHAVIOR
→ project-definition / Plan
→ recover or decide the missing contract/evidence basis
→ update canonical Foundation owner(s)
→ re-check readiness
```

A bounded discovery/prototype may occur before readiness **only** when it is the minimum way to resolve a material unknown. It must not become product implementation by stealth.

Documentation Readiness does not require project specialists. After it passes, `project-skill-planner` separately determines whether zero or more project specialists are justified.

Direct Bounded Maintenance on an already understood local defect does not replay the full gate when wider definition cannot change the fix.

## 11. Skill/document separation

```text
project/product fact or durable requirement
→ Foundation

current repository navigation + development context
→ Knowledge

compact stable cross-session projection
→ CONTEXT.md

reusable AI judgment/procedure
→ Skill

actual implementation behavior
→ source + matching proof
```

Core workflow skills are `project-definition`, `project-skill-planner`, and `development-brief`.

Project specialists are earned reusable semantic procedures governed by `project-skill-planner`. Skills must not become storage for project-specific facts, source inventories, or current implementation maps.

If multiple earned specialists later make selection genuinely ambiguous, Knowledge may earn a compact activation/navigation map. Do not pre-create one.

## 12. Documentation anti-AI-slop — hard rules

Do not:

- create one document per feature by default;
- create empty/placeholder files for possible future needs;
- create version-suffixed or old/legacy/new/backup replacement docs;
- duplicate Overview, Requirements, CONTEXT, README, routing, ownership, status, or next-step truth;
- copy the same contract into several files instead of linking to its owner;
- create per-task completion reports/worklogs;
- create decision records for trivial decisions;
- create an ownership map before ownership is materially difficult;
- create architecture/validation/source-inventory docs before their responsibility is real;
- create a specialist because a technology/file type exists;
- create skill-planning reports/registries during bootstrap;
- retain obsolete docs merely because they once existed;
- turn Knowledge into a generic archive;
- lose material evidence provenance while claiming a Foundation fact is source-backed;
- interpret “professional documentation” as “more documentation.”

Do:

```text
use existing owner when responsibility fits
→ link instead of copy
→ split only for distinct durable responsibility or real current-navigation need
→ update all affected current owners coherently
→ merge/remove when responsibility disappears
→ let Git history preserve history
```

Every persistent document must materially define a current contract/decision, prevent a realistic recurring error, establish authority/ownership, define a required workflow/quality/acceptance rule, reduce current navigation complexity, or preserve current state/evidence basis that must survive sessions. Otherwise, do not create it.

## 13. Authority rules

- Foundation is not derived from Knowledge.
- Knowledge does not define product requirements.
- `CONTEXT.md` summarizes/navigates stable truth and must not become a second Foundation or Knowledge dump.
- Skills must not store project-specific facts.
- Source owns actual implementation behavior but does not silently redefine Foundation meaning.
- AI proposals become durable truth only after current authority approves/corrects them where material.
- Foundation requirements backed by unstable external facts may require later factual revalidation; the old source reference does not become permanent proof.
- Skill planning never repairs missing Project Definition inside a specialist file.

## 14. Archetype rule

These are decision outcomes, not fixed file sets:

- a simple application may need only Overview + Requirements and zero project specialists;
- a domain-heavy tool may earn workflow/quality/validation owners and specialists only for recurring semantic judgment;
- a multi-stage production system may earn boundaries/flow/source-intake/stage/handoff owners.

Do not force complex structure onto simple projects or omit distinct responsibilities from complex projects.

## 15. Update and pruning

When current truth changes, update the current canonical owner. When a responsibility disappears:

```text
remove or fold obsolete owner
→ update navigation/routing
→ keep no compatibility copy unless externally required
→ Git history retains retired rationale
```

Documentation quality is measured by **clarity of current authority, traceable evidence basis, development readiness, and current development navigation**, not document count.
