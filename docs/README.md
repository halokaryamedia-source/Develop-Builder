# Documentation Architecture

This file is the canonical documentation-system and Documentation Readiness owner for projects created from this starter.

Its job is to ensure **enough durable truth, enough traceable evidence, and enough current navigation** to develop correctly—without speculative, duplicate, ceremonial, historical, or versioned documentation.

Critical project-definition judgment belongs to `.agents/skills/project-definition/SKILL.md`. Work-mode and specialist-necessity routing belongs to `AGENTS.md`. Specialist creation/pruning belongs to `.agents/skills/project-skill-planner/SKILL.md` when triggered.

## 1. Documentation principle

```text
real responsibility
→ one current owner

no current responsibility
→ no file
```

Git history owns ordinary historical versions. Current docs describe current truth.

A persistent document must materially define a current contract/decision, preserve a material evidence basis, prevent a realistic recurring error, establish authority/ownership, define a required workflow/quality/acceptance rule, or reduce current navigation complexity. Otherwise, do not create it.

## 2. Documentation layers

| Layer | Responsibility |
|---|---|
| root `README.md` | human/template entrypoint |
| `CONTEXT.md` | compact stable cross-session orientation |
| `docs/foundation/` | durable project/product definition and material evidence basis |
| `docs/knowledge/` | current development navigation/context |
| `.agents/skills/` | reusable AI judgment/procedure |
| implementation/source | actual current behavior |

```text
FOUNDATION
= what the project must remain or become

KNOWLEDGE
= how to find, understand, and resume what is being developed now
```

Knowledge is not a generic project-management archive. Historical rationale, completed reviews, inactive plans, meeting notes, and arbitrary backlog do not belong there merely because they may be useful someday.

Do not use a lower-authority or derived layer to repair missing upstream meaning.

## 3. Project-definition documentation lifecycle

```text
CURRENT USER INTENT
+ APPROVED DECISIONS
+ AUTHORITATIVE SOURCES
        ↓
project-definition
        ↓
01 PROJECT OVERVIEW
        ↓
02 PRODUCT REQUIREMENTS
        ↓
FOUNDATION EXPANSION GATE
        ↓
only earned durable Foundation owners
        ↓
EVIDENCE / COHERENCE READINESS
        ↓
DOCUMENTATION READINESS
        ↓
return to AGENTS specialist-necessity routing
        ↓
CONTEXT projection
        ↓
KNOWLEDGE NAVIGATION GATE when needed
        ↓
next-action
        ↓
DEVELOPMENT READY
```

Documentation Readiness does **not** imply that `project-skill-planner` must be loaded. After readiness, `AGENTS.md` decides whether specialist planning is unnecessary or actually triggered.

`CONTEXT.md` summarizes stable truth after the durable definition is coherent. `next-action.md` owns one active continuation point; neither replaces Foundation.

## 4. Mandatory Foundation owners

### `docs/foundation/01-project-overview.md`

Owns the durable high-level answer to:

- what the project is;
- who/what consumes it;
- the real problem/need or user-owned goal;
- intended outcomes/deliverables;
- source classes/decisions that may establish truth;
- current scope and explicit non-goals/removals;
- high-level product/domain boundaries;
- material constraints;
- success boundary;
- high-impact unknowns.

Do not turn Overview into implementation architecture, task history, or a detailed requirements dump.

### `docs/foundation/02-product-requirements.md`

Owns durable observable requirements needed to build and accept the current product/system, including material exclusions/removals.

Depending on the project it may contain priorities, inputs, outputs, core behavior, simple flow, lifecycle/state, quality, data/privacy/security, external interfaces, failure/recovery, persistence, acceptance/proof, and current blocking decisions.

Keep these together while they remain one product-requirement responsibility. Split only when another durable responsibility earns its own owner.

## 5. Evidence traceability and source coverage

Foundation is authoritative project meaning, but material **source-backed factual premises must remain traceable enough to audit or revalidate**.

### Source coverage

```text
known potentially authoritative sources for current scope identified
→ each inspected to the depth that can change current decisions
→ unread/unavailable material authority identified
→ partial coverage never presented as complete evidence
```

Targeted inspection is valid for a targeted boundary. Do not full-read unrelated material for ceremony.

If a known unread/unavailable source could materially change scope, feasibility, requirement meaning, risk, compatibility, or acceptance, the affected claim remains `UNKNOWN` or blocked.

### Provenance

When a material source-backed fact shapes Foundation, retain the smallest useful identity needed to reopen the basis later, such as repository path/revision, source title/section, official source/standard identifier, relevant version/platform/model, and verification date when change-prone.

Do not create a source inventory for a few direct references. If source intake/reconciliation becomes a distinct durable responsibility, use the Foundation Expansion Gate.

### Freshness

Foundation records accepted meaning; it is not perpetual proof that a change-prone external fact remains current. Revalidate unstable external premises only when later work materially depends on them and staleness is plausible.

### Negative requirements

Explicit `remove`, `no longer use`, `do not use`, `must not`, `only`, `replaced by`, and scoped exclusions are first-class project meaning. Do not silently reintroduce them from old source, references, framework convention, or compatibility instinct.

## 6. Foundation Expansion Gate

After Overview + Requirements ask:

> Would keeping this durable responsibility as a subsection mix distinct jobs, hide acceptance rules, or leave several project areas dependent on an unclear contract?

Create a dedicated Foundation owner only when yes.

| Responsibility | Dedicated owner is justified when... | Typical name |
|---|---|---|
| Product/domain boundaries | several semantic domains have materially different ownership or forbidden cross-repair rules | `product-boundaries.md` |
| Product/production workflow | multi-stage order materially controls correctness/handoff/eligibility | `product-flow.md` / `production-flow.md` |
| Source intake/authority | source recovery/classification/reconciliation is itself a durable contract | `source-intake.md` |
| System architecture | architecture decisions materially constrain runtime/ownership/acceptance | `system-architecture.md` |
| Data/state/storage | state lifecycle/persistence/migration/destructive behavior is materially complex | `data-state.md` |
| External interface | public/external contract has independent semantics/compatibility/acceptance | `interface-contract.md` |
| Security/privacy | cross-cutting security/privacy contract has independent risk/acceptance | `security-privacy.md` |
| Domain quality standard | recurring quality rules control several tasks/components | `<domain>-standard.md` |
| Validation/acceptance | validation has an independent procedure/evidence model | `validation.md` |
| Handoff/delivery/release | downstream handoff has material independent requirements | `handoff-delivery.md` |

Reject a new Foundation file when it only makes the folder look complete, repeats an existing owner, describes possible future work, contains placeholders, copies another repository's shape, stores temporary task state, or belongs in implementation/source.

### Split vs keep

Keep together when:

```text
same semantic responsibility
+ same primary consumer
+ changes usually move together
+ one owner remains understandable
```

Split when a distinct semantic responsibility changes independently, has its own consumer/acceptance, affects several areas, and would otherwise mix jobs or hide a contract.

File length or importance alone is not a reason to split.

## 7. Foundation coherence

One recovered/approved decision may affect several Foundation owners.

```text
identify every affected current owner
→ update coherently
→ remove superseded conflicting meaning
→ leave no old/new alternatives
```

Contradiction between current Foundation owners is a Documentation Readiness defect. Git history owns retired meaning.

## 8. Knowledge Navigation Gate

`docs/knowledge/next-action.md` is the only baseline Knowledge owner.

Add another Knowledge owner only when:

```text
current navigation/context problem exists
+ root/Foundation/source/next-action does not answer it cleanly
+ information must survive across sessions
+ new owner reduces repeated search, ambiguity, or resume error
```

Possible earned owners include implementation-flow maps, current ownership maps, source-precedence navigation, proof-surface navigation, risky repeatable runbooks, or a skill activation map when several earned specialists make selection genuinely ambiguous.

Decision/review/backlog files are not Knowledge merely because they contain information.

```text
active resume point
→ next-action.md

current development navigation/context
→ earned Knowledge owner

durable project meaning
→ Foundation

reusable procedure
→ Skill

actual behavior
→ source + proof

ordinary completed history
→ Git history / issues / PRs
```

Never pre-create the full Knowledge set during bootstrap and never broad-read all Knowledge owners during normal work.

## 9. Documentation Readiness Gate

Before non-trivial Developing for a fresh project or materially new domain, verify the smallest applicable set:

- purpose, primary consumer, and expected deliverable are known;
- source authority is sufficient and known material authority has been inspected deeply enough for current scope;
- material source-backed premises are traceable enough to reopen/revalidate;
- scope, non-goals, removals, and negative requirements are current;
- observable requirements are current;
- material flow and domain boundaries are owned when they affect correctness;
- architecture/data/security/interface decisions required **before implementation** are resolved or explicitly blocking;
- material quality rules and acceptance/proof requirements are owned;
- unresolved high-impact decisions remain visible rather than invented;
- affected Foundation owners are coherent;
- Foundation Expansion Gate has been applied.

If a required responsibility/evidence basis is missing:

```text
DO NOT IMPLEMENT THE UNDEFINED BEHAVIOR
→ project-definition / Plan
→ recover or decide missing meaning/evidence
→ update current Foundation owner(s)
→ re-check readiness
```

A bounded discovery/prototype before readiness is allowed only when it is the minimum evidence needed to resolve a material unknown; it must not become implementation by stealth.

Direct Bounded Maintenance on an already understood local defect does not replay the full gate when wider definition cannot change the fix.

## 10. Documentation anti-slop

Do not:

- create one document per feature by default;
- create empty/future placeholder files;
- create versioned/old/legacy/new/backup replacement docs;
- duplicate Overview, Requirements, CONTEXT, README, routing, ownership, status, or next-step truth;
- copy the same detailed contract into several owners instead of linking to its canonical owner;
- create per-task completion/worklog docs;
- create decision records for trivial decisions;
- create architecture/source-inventory/validation/ownership docs before their responsibility is real;
- create skill-planning reports/registries during bootstrap;
- turn Knowledge into a generic archive;
- preserve obsolete docs merely because they once existed.

Do:

```text
use current owner when responsibility fits
→ link/reference rather than duplicate detail
→ split only for distinct durable responsibility or real navigation need
→ update every affected current owner coherently
→ remove/fold when responsibility disappears
→ let Git history preserve history
```

## 11. Authority and pruning

- Foundation is not derived from Knowledge.
- Knowledge does not define product requirements.
- `CONTEXT.md` is a compact projection, not another policy/index dump.
- Skills do not store project-specific facts.
- Source owns actual behavior but does not silently redefine approved Foundation meaning.
- AI proposals become durable truth only after current authority approves/corrects them where material.
- Skill planning never repairs missing Project Definition inside a specialist file.

A simple project may legitimately need only Overview + Requirements and zero project specialists. Complex projects earn more structure only when real responsibilities require it.

When a documentation responsibility disappears, remove or fold its owner, update navigation, keep no current compatibility copy unless externally required, and let Git history retain retired rationale.

Documentation quality is measured by **clarity of current authority, evidence traceability, readiness, and navigation utility—not document count**.
