---
name: project-definition
description: Mandatory critical semantic front door for creating or materially redefining a project before normal Developing. Recover current evidence, separate facts/approved decisions/derived implications/AI proposals/unknowns, challenge unsupported or disproportionate user methods, form the smallest coherent project model, disclose material AI proposals honestly, and write approved current meaning into Foundation. Do not implement product behavior or create project specialists.
---

# Project Definition

Turn a user's intent and available evidence into the **smallest coherent, evidence-grounded Project Definition worth developing for the user's actual goal**.

This skill is not a form filler and not a yes-man. Its responsibility is independent project/product judgment before implementation.

Root `AGENTS.md` owns top-level routing, `docs/README.md` owns documentation architecture/readiness, and `GITHUB_RULES.md` owns GitHub execution. Durable approved project meaning belongs in `docs/foundation/`; this skill owns the reusable judgment used to form that meaning.

## Entry boundary

Use this skill when:

- bootstrapping a new project from the starter;
- materially redefining project purpose/scope/outputs;
- adding a materially new domain whose product meaning is not yet owned;
- Developing discovers that required product flow, boundary, source authority, quality, architecture, risk, or acceptance meaning is undefined.

Do not use it for:

- routine implementation of already-defined behavior;
- bounded Maintenance where wider product definition cannot change the fix;
- normal domain execution when the domain contract already exists;
- project-specialist selection/creation — that belongs to `project-skill-planner` after Documentation Readiness.

## Truth before agreement

The objective is not to maximize user approval. The objective is to help the user reach the best responsible current definition supported by evidence and explicit decisions.

- Challenge unsupported assumptions and unnecessary complexity.
- Reject a proposed **direction/method** when evidence shows it is contradictory, infeasible, unsafe, or materially disproportionate to the actual goal.
- Preserve the user's intended outcome where possible even when redirecting the method.
- Do not hide tradeoffs, uncertainty, cost, risk, missing capability, or weak evidence to make a proposal sound attractive.

A respectful `REJECT` or `BLOCKED` result is valid.

### User-owned goals vs external claims

A personal, creative, learning, experimental, internal, or preference-driven goal does **not** need market proof merely to be legitimate. The user's explicit desired outcome may itself be sufficient authority for why that project exists.

Do not invent an external “problem” or business case when the user did not claim one.

External evidence becomes mandatory when the proposed definition materially relies on an external factual claim, such as:

- market demand or business viability;
- pricing/cost/supply claims;
- platform/library/provider capability or support;
- performance/resource feasibility;
- regulation/compliance;
- security/privacy properties;
- compatibility/interoperability;
- another unstable/niche factual premise.

Critique the **method, scope, assumptions, and feasibility** relative to the user's real goal. Do not reject a harmless user-owned goal solely because it lacks external commercial justification.

## Evidence classes

Keep these meanings distinct internally:

```text
SOURCE-BACKED
→ established by current authoritative evidence

APPROVED
→ current explicit user/project-owner decision

DERIVED
→ necessary implication from current evidence; no material option was selected

PROPOSAL
→ AI selected one material direction among plausible options

UNKNOWN
→ current evidence is insufficient for a responsible conclusion
```

Never present `DERIVED` or `PROPOSAL` as source-backed fact.

A polished reference, old implementation, generated output, example repository, or common industry pattern is evidence/method input only unless current authority adopts its meaning.

## Evidence recovery

Before asking the user to repeat facts or make decisions, recover what can be established from current authoritative sources.

Read by **material relevance**, not by quantity.

Possible authority may include, when applicable:

- current explicit user/project-owner instruction;
- supplied authoritative documents/data;
- current repository/foundation/source;
- approved specifications/references;
- external standards/contracts;
- current official/primary documentation for material external technical claims.

If a claim depends on current external facts—support, compatibility, limits, pricing, regulation, library/runtime behavior, market data, or another unstable/niche fact—do not guess. Use current authoritative/primary evidence when available. If the environment cannot obtain sufficient evidence, mark the claim `UNKNOWN` or identify the exact external decision/evidence still required.

Do not perform broad research merely to make the project look well researched. Research only claims that can materially change project direction, feasibility, scope, risk, or acceptance.

## Recover the real goal

Separate:

```text
intended outcome
user preference
suggested method/architecture/tool
known constraint
existing implementation/history
external factual claim
material unknown
```

A user-suggested technology, architecture, provider, workflow, or feature set is not automatically a requirement.

Ask:

1. What outcome does the user actually want?
2. Who or what is the primary consumer?
3. What observable output/deliverable satisfies that outcome?
4. Which constraints are real and current?
5. Which proposed parts are requirements versus methods?
6. Which external claims require evidence?
7. What is the simplest complete direction that satisfies the goal?

## Critical direction verdict

Evaluate the current project **direction** using one verdict when useful:

```text
FOLLOW
→ goal and proposed direction are grounded and proportionate

REFINE
→ direction is fundamentally sound but material details/boundaries need correction

REDIRECT
→ goal is valid but the proposed method/scope is materially inferior or disproportionate

REJECT
→ current direction conflicts with evidence/requirements, is infeasible/unsafe, or has no responsible current justification relative to the accepted goal

BLOCKED
→ a responsible direction cannot be formed without missing material authority/evidence that the AI cannot safely supply
```

Do not use arbitrary scores or maturity percentages.

When redirecting/rejecting, state:

- the valid goal being preserved, if any;
- the exact unsupported/contradictory part;
- the evidence or reasoning boundary;
- the smallest better direction you recommend, when one can be formed;
- what remains `UNKNOWN`.

## Resolution ladder

For each material gap/conflict:

```text
1. Current authority resolves it
   → recover it.

2. One necessary result follows from evidence
   → DERIVED completion.

3. AI must choose among plausible material options
   → one concrete PROPOSAL that best fits current goal/constraints/evidence.

4. Options remain close but a responsible default can still be recommended
   → choose one PROPOSAL; mention an alternative only when it materially helps review.

5. Current direction is materially wrong/disproportionate
   → REDIRECT or REJECT; provide the better supported direction when possible.

6. No responsible conclusion/proposal can be formed
   → BLOCKED / focused user or external decision.
```

`BLOCKED` is a last resort, not a substitute for reasoning.

## Critical completeness pass

After source recovery, perform one integrated reasoning pass over **only applicable concerns**:

| Concern | Must be sufficiently clear when material |
|---|---|
| User goal / intended value | what outcome the user actually wants; external value claims only when claimed/material |
| Deliverable | canonical output/result and success boundary |
| Scope | included work, explicit non-goals, adjacent exclusions |
| Source authority | which evidence/decisions may establish project truth |
| Product/domain boundaries | semantic areas that must not silently repair/own each other |
| Flow/lifecycle | material stages, transitions, eligibility, failure/retry/handoff |
| Feasibility | required capability/runtime/platform/tool/dependency actually plausible from current evidence |
| Complexity | proposed architecture/features proportional to current need |
| Data/security/privacy | material ownership, sensitivity, destructive or authorization boundaries |
| Quality | dimensions that materially determine acceptance |
| External contracts | public API/protocol/file format/deployed-client compatibility obligations |
| Acceptance/proof | evidence required to claim the intended outcome works |
| Operational clarity | competent implementers should not be forced to invent material project behavior |

Do not add a concern just because mature projects often have it.

## Complexity and feasibility challenge

For every material proposed architecture, feature family, dependency, provider, compatibility layer, persistent state authority, workflow, or service ask:

```text
required by current goal?
backed by current evidence/constraint when fact-dependent?
what simpler complete alternative exists?
what new failure/maintenance/proof cost does it create?
would removing it change accepted outcome?
```

If removal does not harm the accepted outcome, it is not automatically part of the project.

Do not use “best practice”, “scalability”, “enterprise-ready”, “future-proof”, or popularity as standalone requirements.

## Build the Project Definition

Write approved/current meaning into the existing canonical Foundation owners:

```text
docs/foundation/01-project-overview.md
docs/foundation/02-product-requirements.md
+ only additional durable owners earned through docs/README.md
```

Use `docs/README.md` Foundation Expansion Gate rather than inventing a document structure.

The project definition should be complete enough that implementation does not need to choose material project behavior silently.

Do not create a parallel `PROJECT-BRIEF.md`, `PROJECT-PLAN.md`, `research-summary.md`, approval file, or per-session design artifact.

## Proposal disclosure and user authority

Material AI-selected `PROPOSAL` must be disclosed before it is promoted to approved project truth.

Do not ask the user to decide every small detail. Prefer one coherent recommendation.

A user decision is required when the remaining choice materially changes:

- project/product outcome or scope;
- user experience/behavior;
- architecture/runtime/data ownership with meaningful consequences;
- privacy/security/destructive behavior;
- compatibility/release obligation;
- acceptance boundary;
- another high-impact project fact owned by the user.

Present material proposals compactly as recommendations with reasons/evidence, not as a multi-page questionnaire.

When the user approves/corrects a proposal, update the affected Foundation owner. Do not preserve pending/old alternatives beside the current decision.

## Documentation Readiness handoff

After the project model is coherent:

```text
Foundation current truth
→ apply docs/README.md Foundation Expansion Gate
→ Documentation Readiness review
```

If Documentation Readiness fails, fix only the missing material responsibility/contract.

If it passes, hand off to `project-skill-planner` to determine whether any project specialists are actually needed before initial development routing is finalized.

This skill does not create project specialists.

## Hard anti-slop rules

Do not:

- agree with unsupported user assumptions merely to be helpful;
- convert AI recommendations into fake facts;
- invent market/technical/security/compatibility claims without evidence;
- fabricate a business problem for a personal/creative project;
- add architecture/features because they sound professional;
- create multiple alternatives when one responsible recommendation is enough;
- turn every unknown into a user question;
- hide a bad root direction under implementation detail;
- create extra project docs outside canonical owners;
- preserve rejected/superseded proposals as legacy current state;
- use prototype/mock/static proof as evidence for claims it did not exercise;
- continue brainstorming after the current definition/readiness boundary is satisfied.

## Completion

A Project Definition pass ends when:

- current authority/evidence has been recovered to sufficient depth;
- material unsupported assumptions are challenged;
- the project direction has a responsible verdict;
- applicable project meaning is complete enough for current scope;
- material AI proposals are approved/corrected or an exact blocker remains;
- current Foundation owners contain the accepted truth;
- Documentation Readiness is truthfully classified.

Then hand off to `project-skill-planner` only when readiness passes, otherwise report the exact remaining definition blocker and STOP.
