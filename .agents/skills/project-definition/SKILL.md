---
name: project-definition
description: Mandatory critical semantic front door for creating or materially redefining a project before normal Developing. Recover sufficiently complete current evidence, distinguish facts/approved decisions/derived implications/AI proposals/unknowns, challenge unsupported or disproportionate user methods, preserve negative requirements, keep material evidence traceable, form the smallest coherent project model, disclose material AI proposals honestly, and reconcile approved meaning into Foundation. Do not implement product behavior or create project specialists.
---

# Project Definition

Turn a user's intent and available evidence into the **smallest coherent, evidence-grounded Project Definition worth developing for the user's actual goal**.

This skill is not a form filler and not a yes-man. Root `AGENTS.md` owns top-level routing, `docs/README.md` owns documentation architecture/readiness, and `GITHUB_RULES.md` owns GitHub execution. Durable approved project meaning belongs in `docs/foundation/`; this skill owns the reusable judgment used to form that meaning.

## Entry boundary

Use this skill when:

- bootstrapping a new project from the starter;
- materially redefining project purpose/scope/outputs;
- adding a materially new domain whose product meaning is not yet owned;
- Developing discovers that required product flow, boundary, source authority, quality, architecture, risk, feasibility, or acceptance meaning is undefined.

Do not use it for routine implementation of already-defined behavior, bounded Maintenance where wider definition cannot change the fix, normal domain execution with an existing contract, or project-specialist selection/creation.

## Truth before agreement

The objective is not to maximize user approval. The objective is the best responsible current definition supported by evidence and explicit decisions.

- Challenge unsupported assumptions and unnecessary complexity.
- Redirect/reject a proposed method when evidence shows it is contradictory, infeasible, unsafe, or materially disproportionate to the actual goal.
- Preserve the user's intended outcome where possible even when redirecting the method.
- Do not hide uncertainty, cost, risk, missing capability, or weak evidence to make a proposal sound attractive.

A respectful `REJECT` or `BLOCKED` result is valid.

### User-owned goals vs external claims

A personal, creative, learning, experimental, internal, or preference-driven goal does **not** need market proof merely to be legitimate. Do not invent an external problem/business case the user did not claim.

External evidence becomes mandatory when project direction materially relies on an external factual claim such as market/business viability, cost/supply, platform/library/provider capability, performance/resource feasibility, regulation/compliance, security/privacy properties, compatibility/interoperability, or another unstable/niche premise.

Critique method, scope, assumptions, and feasibility relative to the user's real goal. Do not reject a harmless user-owned goal solely because it lacks external commercial justification.

## Evidence classes

Keep these meanings distinct:

```text
SOURCE-BACKED
→ established by current authoritative evidence

APPROVED
→ current explicit user/project-owner decision

DERIVED
→ necessary implication from current evidence; no material option selected

PROPOSAL
→ AI selected one material direction among plausible options

UNKNOWN
→ current evidence insufficient for a responsible conclusion
```

Never present `DERIVED` or `PROPOSAL` as source-backed fact. Polished references, old implementations, generated output, example repositories, or common patterns remain evidence/method input unless current authority adopts their meaning.

## Evidence recovery and sufficiency

Recover discoverable facts before asking the user to repeat them or decide them.

Read by **material relevance**, not quantity. Potential authority may include current user/project-owner instruction, supplied authoritative documents/data, current repository/Foundation/source, approved specifications/references, external standards/contracts, and current official/primary documentation for material external technical claims.

### Source-coverage rule

Before declaring a material project direction grounded:

```text
identify known potentially authoritative sources for current scope
→ inspect each to the depth that can change current decisions
→ distinguish inspected vs unavailable/unread material authority
→ do not treat partial coverage as complete evidence
```

Targeted inspection is valid when the current boundary is targeted. A full-source read is not required when unseen portions cannot reasonably change the current decision. If a known uninspected/unavailable source could materially change scope, feasibility, requirement meaning, or acceptance, keep the affected claim `UNKNOWN` or explicitly blocked.

### Provenance rule

When a material `SOURCE-BACKED` claim changes project scope, feasibility, requirement, risk, compatibility, or acceptance, preserve enough source identity in the appropriate current Foundation owner to re-open/revalidate the basis later.

Use the smallest useful provenance, for example:

```text
repository path / commit / revision
source title / document section
official URL / standard identifier
version / platform / model when material
verification/access date when the fact is change-prone
```

Do not create a source inventory for a few simple references. If source intake/reconciliation itself becomes a distinct durable responsibility, use the `docs/README.md` Foundation Expansion Gate.

### Freshness rule

Foundation records accepted project meaning; it is **not perpetual proof that an external fact remains unchanged**.

For change-prone external claims, record enough version/date/source context to know what was verified. When later project work materially depends on that factual premise and staleness is plausible, revalidate the current authoritative source rather than treating an old verification as permanent truth.

Do not repeatedly re-research stable facts for ceremony.

## Recover the real goal

Separate:

```text
intended outcome
user preference
suggested method/architecture/tool
known constraint
existing implementation/history
external factual claim
negative requirement / explicit removal
material unknown
```

A user-suggested technology, architecture, provider, workflow, or feature set is not automatically a requirement.

### Negative requirements are first-class

Treat statements such as these as material when their scope is material:

```text
remove
no longer use
do not use
must not
only
replaced by
out of scope
```

Do not silently reintroduce removed/excluded behavior through “best practice”, backward compatibility, an old source path, or a generated design suggestion. Do not broaden a negative requirement beyond the scope actually stated.

Ask:

1. What outcome does the user actually want?
2. Who/what is the primary consumer?
3. What observable output/deliverable satisfies it?
4. Which constraints/exclusions are real and current?
5. Which proposed parts are requirements versus methods?
6. Which external claims require evidence or revalidation?
7. What is the simplest complete direction that satisfies the goal?

## Critical direction verdict

Use one verdict when useful:

```text
FOLLOW   → goal and proposed direction are grounded/proportionate
REFINE   → fundamentally sound; material details/boundaries need correction
REDIRECT → goal valid; proposed method/scope materially inferior/disproportionate
REJECT   → direction conflicts with evidence/requirements or has no responsible justification
BLOCKED  → no responsible direction can be formed without missing material authority/evidence
```

Do not use arbitrary scores or maturity percentages.

When redirecting/rejecting, state the valid goal being preserved, exact unsupported/contradictory part, evidence/reasoning boundary, smallest better direction when one exists, and what remains `UNKNOWN`.

## Resolution ladder

For each material gap/conflict:

```text
1. Current authority resolves it
   → recover.

2. One necessary result follows from evidence
   → DERIVED completion.

3. AI must choose among plausible material options
   → one concrete PROPOSAL best fitting current goal/constraints/evidence.

4. Options remain close but a responsible default exists
   → choose one PROPOSAL; mention alternatives only when they materially help review.

5. Current direction is materially wrong/disproportionate
   → REDIRECT or REJECT; provide the better supported direction when possible.

6. No responsible conclusion/proposal can be formed
   → BLOCKED / focused user or external decision.
```

`BLOCKED` is a last resort, not a substitute for reasoning.

## Critical completeness pass

After evidence recovery, inspect only applicable concerns:

| Concern | Must be sufficiently clear when material |
|---|---|
| User goal / intended value | actual intended outcome; external value claims only when claimed/material |
| Deliverable | canonical output/result and success boundary |
| Scope / exclusions | included work, explicit non-goals, removals, forbidden adjacent behavior |
| Source authority | evidence/decisions allowed to establish project truth and material provenance |
| Product/domain boundaries | semantic areas that must not silently repair/own each other |
| Flow/lifecycle | stages, transitions, eligibility, failure/retry/handoff |
| Feasibility | required capability/runtime/platform/dependency plausible from current evidence |
| Complexity | proposed architecture/features proportional to current need |
| Data/security/privacy | material ownership, sensitivity, destructive/authorization boundaries |
| Quality | dimensions materially determining acceptance |
| External contracts | public API/protocol/file format/deployed-client obligations |
| Acceptance/proof | evidence required to claim intended outcome works |
| Operational clarity | implementers should not need to invent material project behavior |

Do not add a concern merely because mature projects often have it.

## Complexity and feasibility challenge

For each material architecture, feature family, dependency, provider, compatibility layer, state authority, workflow, or service ask:

```text
required by current goal?
backed by current evidence/constraint when fact-dependent?
what simpler complete alternative exists?
what new failure/maintenance/proof cost appears?
would removing it change accepted outcome?
```

If removal does not harm the accepted outcome, it is not automatically part of the project. “Best practice”, “scalability”, “enterprise-ready”, “future-proof”, and popularity are not standalone requirements.

## Build and reconcile the Project Definition

Persist current approved meaning into:

```text
docs/foundation/01-project-overview.md
docs/foundation/02-product-requirements.md
+ only additional durable owners earned through docs/README.md
```

Use the Foundation Expansion Gate rather than inventing a document structure.

When one recovered/approved decision affects several Foundation owners:

```text
identify all affected current owners
→ update them coherently in the same logical definition change
→ remove/replace superseded conflicting meaning
→ leave no pending old/new alternatives
```

Cross-Foundation contradiction is a readiness defect. Do not “solve” it with a compatibility note or duplicate source.

Do not create parallel `PROJECT-BRIEF.md`, `PROJECT-PLAN.md`, research-summary, approval file, or per-session design artifact.

## Proposal disclosure and user authority

Material AI-selected `PROPOSAL` must be disclosed before promotion to approved truth. Prefer one coherent recommendation rather than asking the user to decide every small detail.

A user decision is required when the remaining choice materially changes product outcome/scope, user behavior, consequential architecture/runtime/data ownership, privacy/security/destructive behavior, compatibility/release obligation, acceptance boundary, or another high-impact user-owned project fact.

When the user approves/corrects a proposal, reconcile all affected Foundation owners. Do not preserve rejected/pending alternatives beside the current decision.

## Documentation Readiness handoff

After the project model is coherent:

```text
Foundation current truth
→ Foundation Expansion Gate
→ Documentation Readiness review
```

If readiness fails, fix only the missing material responsibility/contract/evidence basis. If it passes, hand off to `project-skill-planner` to determine whether project specialists are actually needed before initial development routing is finalized.

## Hard anti-slop rules

Do not:

- agree with unsupported assumptions merely to be helpful;
- convert AI recommendations into fake facts;
- invent external claims without evidence;
- treat partial source coverage as complete;
- lose material provenance when a source-backed fact becomes Foundation truth;
- treat old external verification as permanently current;
- fabricate a business problem for a personal/creative project;
- ignore/remove negative requirements because a familiar architecture usually includes the feature;
- add architecture/features because they sound professional;
- create multiple alternatives when one responsible recommendation is enough;
- turn every unknown into a user question;
- hide a bad root direction under implementation detail;
- create extra project docs outside canonical owners;
- preserve rejected/superseded proposals as legacy current state;
- use prototype/mock/static proof as evidence for claims it did not exercise;
- continue brainstorming after current definition/readiness is satisfied.

## Completion

A Project Definition pass ends when:

- known material authority has been inspected to sufficient depth for current scope;
- material source-backed claims are traceable enough to revalidate when needed;
- material unsupported assumptions are challenged;
- negative/removal requirements are preserved;
- the direction has a responsible verdict;
- applicable project meaning is complete enough for current scope;
- material AI proposals are approved/corrected or an exact blocker remains;
- all affected Foundation owners are coherent and contain the current accepted truth;
- Documentation Readiness is truthfully classified.

Then hand off to `project-skill-planner` only when readiness passes; otherwise report the exact remaining definition blocker and STOP.
