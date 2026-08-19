---
name: development-brief
description: Mandatory front door for non-trivial Developing after the affected Project Definition is ready. Recover current continuity, ground the real goal, identify the smallest coherent owner set, define 2-5 falsifiable acceptance criteria and a proportional proof budget, then use zero or one already-earned matching project specialist. Do not create project specialists or redefine product meaning inside implementation.
---

# Development Brief

Turn a non-trivial development request into the **smallest grounded implementation contract**.

`AGENTS.md` owns routing, current-source/complexity invariants, and per-task skill budget. `docs/README.md` owns Documentation Readiness. `project-definition` owns project meaning. `project-skill-planner` owns specialist creation/pruning when triggered. `GITHUB_RULES.md` owns GitHub execution.

## Entry boundary

Use only for **non-trivial Developing**.

Do not invoke merely because code/files exist. Direct Bounded work and bounded Maintenance stay on their shorter route when wider context cannot change the decision. Normal production/authoring/domain execution with an existing procedure is not Developing.

Do not create a new project specialist here.

## Mandatory continuity

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ this development-brief
→ smallest affected Foundation/navigation/source/caller/contract set
→ zero/one already-earned matching project specialist when useful
```

If continuity and current source disagree, reconcile the stale current owner before proceeding. Knowledge is navigation/current context, not a substitute for Foundation requirements or direct source inspection.

## Internal development contract

Establish only fields that can change implementation or acceptance:

```text
Goal
Actual requirement / Foundation owner
Suggested method/reference when material
Input authority / material evidence basis
Expected output
Build POV / responsible owner set
Acceptance POV
Interface constraints when material
In scope / Out of scope
Acceptance criteria: 2–5
Proof budget
Open high-impact decisions
Execution channel only when it constrains proof/implementation
Superseded current owner/path when replacement is involved
External compatibility obligation only when real
Matching existing project specialist only when useful
```

Do not create a per-task file merely to store this contract.

## Procedure

### 1. Ground the request

Separate the intended outcome from suggested method/reference/history. Recover discoverable repository facts before asking the user.

If project/product meaning is materially unresolved, return to `project-definition` / Plan. If the request is normal existing-system/domain execution, use the matching domain procedure instead.

### 2. Check the affected Project Definition

Use `docs/README.md` as the canonical Documentation Readiness owner. Do **not** reproduce its full checklist here.

For the affected responsibility only, verify that:

- the current requirement/owner is defined enough to implement without inventing product meaning;
- material exclusions/removals are not being silently reversed;
- affected Foundation owners are coherent;
- any material source-backed premise is traceable enough to reopen/revalidate.

If the affected definition/evidence basis is insufficient:

```text
DO NOT IMPLEMENT
→ project-definition / Plan
→ repair current Foundation meaning/evidence
→ return when ready
```

### 3. Revalidate only material unstable external premises

When implementation materially depends on a change-prone external fact and staleness is plausible, revalidate the smallest current authoritative/primary source needed.

Do not re-research unrelated or stable claims for reassurance. If current evidence cannot be obtained and the claim affects correctness/acceptance, preserve `UNKNOWN` / `Perlu pemeriksaan`.

### 4. Decide whether development is needed

```text
current behavior already satisfies goal
→ No change required

project meaning unresolved
→ project-definition / Plan

suggested method unsupported/disproportionate
→ Redirect / Refine

grounded non-trivial system change required
→ Develop
```

Do not create a patch merely to produce activity.

### 5. Find the smallest coherent owner set

Find the current semantic owner plus only callers/contracts/assertions that can materially affect correctness.

A complete change may require:

```text
current contract
+ implementation
+ regression assertion when it protects a realistic recurring invariant
```

Identify superseded current path/state before writing so the final result does not retain old/new generations.

### 6. Define final scope and proof

Set explicit in/out scope where adjacent systems are easy to confuse.

Choose 2–5 falsifiable acceptance criteria and the cheapest evidence capable of falsifying each changed claim.

The scope describes the **final current state**, not staged coexistence of old + new unless a concrete current external contract requires it.

### 7. Apply root complexity/current-source invariants

Use the persistent-owner and current-source rules in `AGENTS.md` rather than duplicating another anti-slop checklist here.

Every new persistent owner/layer/dependency/state/compatibility path must have a real current responsibility and consumer. If an equally correct direct replacement exists, prefer it.

Select at most one already-earned project specialist. If none adds material semantic judgment, use none. If work reveals a plausible new recurring specialist need, do not create it ad hoc; finish/reframe the current boundary and return that question to `AGENTS.md` specialist-necessity routing.

### 8. Implement and prove

- fix the first wrong current owner;
- preserve valid behavior outside scope;
- implement the smallest complete final solution;
- update required Foundation/contracts/callers/assertions coherently;
- remove superseded current source/path/state when safe;
- follow `GITHUB_RULES.md` for atomicity/history/tool fit;
- obtain only proof relevant to changed claims.

If implementation would change project meaning rather than implement it, return to `project-definition`; do not silently mutate intent from source code.

### 9. Final gate

Before completion verify:

- goal and expected output are achieved;
- Acceptance POV and 2–5 criteria are supported by evidence actually obtained;
- scope remained bounded;
- one current owner remains for each changed responsibility;
- affected Project Definition is still coherent/current;
- material unstable external premises used by the change are current enough for the claim;
- superseded current state is removed when no external contract requires it;
- no unrelated cleanup, duplicate authority, fake success, or proof inflation was introduced.

If implementation is complete but required target/human/current-external proof is unavailable, report `Perlu pemeriksaan`, not `Selesai`.

Update `next-action.md` only when active status, boundary, blocker, proof requirement, or next meaningful action changed. Then STOP.

## User-facing brief

For non-trivial Developing, expose only enough meta-context for the user to steer material decisions. When useful:

```text
Tujuan:
Cara berpikir:
Hasil yang dituju:
Tidak diubah:
Cara memastikan benar:
```

Do not dump the internal contract by default. Normal domain execution should deliver the requested output rather than development ceremony.
