# Agent Routing

Develop-Builder is a general development preset. Current repository/project sources are authority for repository state; chat history is supporting context only.

## Branch and safety authority

- `Local` is the working/development authority.
- Never silently fall back to another branch or repository default.
- Material GitHub execution follows `GITHUB_RULES.md`.
- Choose the **smallest sufficient path**. Efficiency must not remove context, contracts, safety, or proof that can change correctness.

## Task class first

### Context Recovery

For read-only `amati`, inspect, understand, audit, study, or context recovery:

```text
AGENTS.md
→ GitHub Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md when active continuation matters
→ smallest owner needed to explain current state
→ report
→ STOP
```

Do not edit, run CI, execute a recorded next step, or promote old TODO/history merely because they were discovered.

### Plan

Use when a material product, architecture, ownership, risk, or acceptance decision remains unresolved.

```text
recover relevant authority
→ inspect smallest evidence that can change the decision
→ separate goal from suggested method
→ resolve/present the material decision
→ NO IMPLEMENTATION
→ STOP
```

Plan must not silently become Developing.

### Developing

Developing has two execution paths.

#### Direct Bounded Path

Use when all material conditions are true:

- requested outcome is clear;
- current/first-wrong owner is obvious or cheaply discoverable;
- wider stable context cannot materially change the solution, or the relevant invariant is already known;
- no unresolved product/architecture/data/security decision exists;
- no new durable authority/runtime/compatibility/dependency boundary/generic abstraction is required;
- blast radius is local and understandable;
- rollback is straightforward;
- targeted proof is obvious.

```text
pin repo/ref + inherit root safety rules
→ exact owner / exact defect
→ nearest caller/contract/test only when needed
→ smallest complete correction
→ targeted proof
→ update continuation only if it changed
→ STOP
```

Direct means fewer unnecessary decision hops, **not** less correctness or safety. It may skip `CONTEXT.md`, `next-action.md`, `development-brief`, broad tests, or specialist loading only when those surfaces cannot materially change the decision or proof.

#### Non-trivial Developing

Escalate when uncertainty, semantic impact, blast radius, risk, ownership coordination, migration, new persistent authority, material dependency change, hard rollback, or target/human acceptance can materially change implementation or acceptance.

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md when continuation matters
→ .agents/skills/development-brief/SKILL.md
→ smallest relevant owner/caller/contract set
→ zero/one useful specialist
→ coherent implementation
→ minimum honest proof
→ reconcile changed canonical state
→ STOP
```

`Non-trivial` is determined by impact/uncertainty/risk/coordination, not by code presence, file count, or line count.

### Maintenance

A concrete defect, regression, stale rule, or bounded cleanup should use the Direct Bounded Path by default when wider context cannot change the decision.

```text
exact defect
→ first wrong owner
→ smallest safe correction
→ targeted proof
→ STOP
```

If diagnosis exposes an unresolved product/architecture decision, leave Maintenance and return to Plan.

## Claim ownership

Use the nearest authoritative owner for the claim:

- current task intent/new explicit decision → current user instruction;
- GitHub/ref/write/history/CI/security discipline → `GITHUB_RULES.md`;
- work mode/path/skill budget → `AGENTS.md`;
- stable project orientation → `CONTEXT.md`;
- durable intended behavior/non-goals → `docs/foundation/`;
- active continuation/status/boundary/blocker/one next step → `docs/knowledge/next-action.md`;
- actual behavior → current source + relevant proof;
- generated/derived output → upstream canonical source/generator;
- historical rationale → Git history unless a later justified decision owner exists.

If `next-action.md` disagrees materially with current source/state, inspect the exact current owner, reconcile stale continuity vs stale implementation, then continue from actual truth.

## Requirement and method discipline

The user owns intended outcome and high-impact product decisions. The agent owns repository discovery, owner discovery, implementation method quality, scope discipline, and evidence quality.

A suggested framework, sample, screenshot, reference repository, old branch, or technical method is not automatically the requirement. Evaluate a proposed method as:

```text
FOLLOW
REFINE
REDIRECT
STOP / DECISION REQUIRED
```

`No change required` is valid.

## Smallest coherent owner set

The invariant is **one canonical owner per responsibility**, not one owner per task.

A coherent change may legitimately require contract + implementation + regression assertion. Touch the smallest owner set needed for a complete outcome. Do not force one-file solutions that create workaround logic, stale contracts, duplicate authority, or synchronization debt.

## Anti-overdevelopment and anti-slop

Prefer the simplest complete route that preserves correctness.

Do not add a service, runtime, state authority, router, registry, provider layer, compatibility/fallback system, cache, queue, workflow, specialist, document owner, or abstraction merely for “best practice”, “clean architecture”, or future possibility.

For ordinary additions ask only:

```text
needed now?
correct existing responsibility?
simplest complete form?
```

For high-cost architectural additions, require a demonstrated current need and evidence that the new layer uniquely adds required capability or reduces total current complexity.

Do not broad-read, broad-test, create ceremonial reports, invent unknown requirements, or expand scope because adjacent opportunities are visible.

## Skill budget

- Direct Bounded Path → no specialist by default.
- Non-trivial Developing → mandatory `development-brief` + zero/one useful project specialist.
- Maintenance → zero/one specialist only when the diagnosed semantic boundary needs it.
- Plan / Context Recovery → no project specialist by default.

A specialist is selected by recurring semantic responsibility, not programming language/framework name.

## Evidence boundary

Use the cheapest proof capable of falsifying the changed claim.

Repository/static evidence does not prove runtime/device/visual/model/target-machine/human acceptance. A one-line high-risk change may require more proof than a large low-risk internal refactor.

## Completion

When current scope and required proof are satisfied: STOP.

Do not automatically continue into adjacent cleanup, another audit, another verifier, another historical TODO, or the next milestone.

For material work, final reporting may use:

```text
Status: Selesai | Perlu pemeriksaan | Terhenti
Hasil:
Bukti:
Batasan:
Next step:
```

Use one meaningful next step only when continuation actually changed.
