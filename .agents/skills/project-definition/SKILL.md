---
name: project-definition
description: Critical semantic front door for creating or materially redefining a project before normal Developing. Recover sufficiently complete current evidence, distinguish source-backed facts/approved decisions/derived implications/AI proposals/unknowns, challenge unsupported or disproportionate methods, guide the user through only material decisions, preserve negative requirements and provenance, and reconcile approved meaning into Foundation. Do not implement product behavior or create project specialists.
---

# Project Definition

Turn user intent and available evidence into the **smallest coherent, evidence-grounded Project Definition worth developing for the user's actual goal**.

This skill is not a form filler and not a yes-man. `AGENTS.md` owns routing, `docs/README.md` owns documentation/readiness, and `GITHUB_RULES.md` owns GitHub execution. Durable approved project meaning belongs in Foundation; this skill owns the reusable critical judgment used to form that meaning.

## Entry boundary

Use this skill for:

- bootstrap of a new project;
- material redefinition of purpose/scope/output;
- a materially new domain whose project meaning is undefined;
- Developing that discovers undefined product flow, boundary, source authority, feasibility, quality, architecture, risk, or acceptance meaning.

Do not use it for routine implementation of already-defined behavior, bounded Maintenance where wider definition cannot change the fix, normal domain execution with an existing contract, or project-specialist creation.

## Truth before agreement

The objective is the best responsible current definition supported by evidence and explicit decisions—not maximum user agreement.

- Challenge unsupported assumptions and unnecessary complexity.
- Redirect/reject a proposed method when evidence shows contradiction, infeasibility, unsafe consequences, or material disproportionality to the actual goal.
- Preserve the user's intended outcome where possible even when redirecting the method.
- Do not hide uncertainty, cost, risk, missing capability, or weak evidence to make a direction sound attractive.

A respectful `REJECT` or `BLOCKED` result is valid.

A personal, creative, learning, experimental, internal, or preference-driven goal does **not** need market proof merely to be legitimate. Do not invent a business problem the user did not claim.

External evidence is required when the project materially relies on an external factual premise such as market/business viability, cost/supply, platform/library/provider capability, performance/resource feasibility, regulation/compliance, security/privacy properties, compatibility/interoperability, or another unstable/niche fact.

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

Never present `DERIVED` or `PROPOSAL` as source-backed fact. References, old implementations, generated output, example repositories, and common patterns are evidence/method inputs unless current authority adopts their meaning.

## Evidence recovery and sufficiency

Recover discoverable facts before asking the user to repeat or decide them. Read by **material relevance**, not quantity.

Potential authority may include current user/project-owner instruction, supplied documents/data, current repository/Foundation/source, approved specifications/references, external standards/contracts, and current official/primary documentation for material external claims.

### Source coverage

```text
identify known potentially authoritative sources for current scope
→ inspect each only to the depth that can change current decisions
→ distinguish inspected vs unread/unavailable material authority
→ never present partial coverage as complete evidence
```

A full-source read is unnecessary when unseen portions cannot reasonably change the current decision. If a known unread/unavailable source could materially change scope, feasibility, requirement meaning, risk, or acceptance, keep the affected claim `UNKNOWN` or blocked.

### Provenance and freshness

When a material `SOURCE-BACKED` premise changes scope, feasibility, requirement, risk, compatibility, or acceptance, retain the smallest useful source identity in the affected Foundation owner so it can be reopened/revalidated later.

For change-prone facts, keep enough version/date/source context to know what was verified. Revalidate later only when current work materially depends on the premise and staleness is plausible; do not repeatedly research stable facts for ceremony.

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

Negative statements such as `remove`, `no longer use`, `do not use`, `must not`, `only`, `replaced by`, and `out of scope` are first-class when material. Do not silently reintroduce them from old source, reference architecture, framework convention, or compatibility instinct; do not broaden them beyond their actual scope.

## User-guidance interaction contract

Guide the user toward a strong project definition without turning the interaction into an interview checklist.

Default conversational flow:

```text
1. recover what is already knowable
2. form the current project model and best supported direction
3. expose only material interpretation, tradeoff, PROPOSAL, or UNKNOWN
4. ask the smallest grouped high-impact question set only when a responsible recommendation cannot settle it
5. accept natural-language approval/correction; no special approval syntax or form required
6. reconcile every affected Foundation owner
7. continue until Documentation Readiness passes or one exact material blocker remains
```

Rules:

- Recommend before asking. Do not ask the user to choose implementation details the agent can own responsibly.
- Do not ask one question at a time when several tightly related unresolved high-impact decisions can be presented together clearly.
- Do not dump every internal concern, evidence class, or checklist item into the conversation.
- For low-impact details with a responsible default, choose the default and keep moving.
- For a material AI `PROPOSAL`, state it plainly as a recommendation with the reason/evidence boundary; do not silently promote it to approved truth.
- Natural-language responses such as “yes”, “use that”, corrections, or revised constraints are sufficient approval/correction when their referent is clear.
- If the user rejects the recommendation, re-evaluate against the actual goal/evidence; do not defend a prior proposal merely because it was generated earlier.
- `BLOCKED` is reserved for cases where no responsible direction can be formed without missing material authority/evidence or a genuine user-owned decision.

A useful user-facing Project Definition pass should feel like **critical guidance**, not questionnaire completion.

## Critical direction verdict

Use one verdict when it helps communicate a material direction:

```text
FOLLOW   → goal and direction are grounded/proportionate
REFINE   → fundamentally sound; material details/boundaries need correction
REDIRECT → goal valid; proposed method/scope materially inferior/disproportionate
REJECT   → direction conflicts with evidence/requirements or has no responsible justification
BLOCKED  → no responsible direction can be formed without missing material authority/evidence
```

Do not use arbitrary scores or maturity percentages.

When redirecting/rejecting, identify the valid goal being preserved, the unsupported/contradictory part, the evidence/reasoning boundary, the smallest better direction when one exists, and what remains `UNKNOWN`.

## Resolution ladder

For each material gap/conflict:

```text
current authority resolves it
→ recover

one necessary result follows
→ DERIVED

AI must choose among plausible material options
→ one best-supported PROPOSAL

responsible default exists
→ choose one PROPOSAL; mention alternatives only when they materially help review

current direction is materially wrong
→ REDIRECT / REJECT with better supported direction when possible

no responsible conclusion/proposal exists
→ BLOCKED / focused decision
```

`BLOCKED` is a last resort, not a substitute for reasoning.

## Critical completeness pass

Inspect only concerns that can materially change current scope or acceptance:

- actual user goal/intended value;
- canonical deliverable and success boundary;
- scope, non-goals, removals, forbidden adjacent behavior;
- source authority and material provenance;
- product/domain boundaries;
- material flow/lifecycle/handoff;
- feasibility of required capability/runtime/platform/dependency;
- proportionality of proposed architecture/features;
- material data/security/privacy obligations;
- quality dimensions controlling acceptance;
- external compatibility/contracts;
- acceptance/proof boundary;
- enough operational clarity that implementers do not invent material project behavior.

Do not add a concern merely because mature projects often have it.

## Complexity and feasibility challenge

For each material architecture, feature family, dependency, provider, compatibility layer, state authority, workflow, or service ask:

```text
required by current goal?
backed by evidence/constraint when fact-dependent?
what simpler complete alternative exists?
what failure/maintenance/proof cost does it add?
would removing it change the accepted outcome?
```

“Best practice”, “scalability”, “enterprise-ready”, “future-proof”, and popularity are not standalone requirements.

## Build and reconcile Foundation

Persist approved current meaning into:

```text
docs/foundation/01-project-overview.md
docs/foundation/02-product-requirements.md
+ only additional owners earned through docs/README.md
```

Use the Foundation Expansion Gate rather than inventing documentation structure.

When one decision affects several Foundation owners, update all affected owners coherently in the same logical definition change, replace superseded conflicting meaning, and leave no old/new alternatives. Cross-Foundation contradiction is a readiness defect.

Do not create parallel project-brief/plan/research-summary/approval/session artifacts merely to store reasoning.

## Documentation Readiness handoff

After current Foundation meaning is coherent:

```text
Foundation current truth
→ docs/README.md Documentation Readiness
→ return to AGENTS.md routing
```

If readiness fails, fix only the missing material responsibility/contract/evidence basis.

If readiness passes, **do not automatically invoke `project-skill-planner`**. `AGENTS.md` owns the specialist-necessity gate: simple projects may proceed with zero project specialists; load the planner only when specialist need is plausible/ambiguous or an existing specialist set needs review.

## Completion

A Project Definition pass ends when:

- material authority has been inspected deeply enough for current scope;
- material source-backed premises are traceable enough to revalidate when needed;
- unsupported assumptions and disproportionate direction have been challenged;
- negative/removal requirements are preserved;
- the current direction has a responsible verdict;
- applicable project meaning is complete enough for current scope;
- material AI proposals are approved/corrected or one exact blocker remains;
- all affected Foundation owners are coherent and current;
- Documentation Readiness is truthfully classified.

Then return to `AGENTS.md` routing or report the exact blocker and STOP.
