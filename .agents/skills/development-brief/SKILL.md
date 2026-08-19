---
name: development-brief
description: Mandatory front door for non-trivial Developing. Recover sufficient current context, ground the real goal, separate outcome from suggested method, identify the smallest coherent owner set, define 2-5 falsifiable acceptance criteria and a proportional proof budget, then use at most one useful specialist. Do not use for Direct Bounded work or normal existing-system/domain execution when wider context cannot materially change the decision.
---

# Development Brief

Turn a non-trivial development request into the **smallest grounded development contract that preserves correctness without adding ceremony**.

Root `AGENTS.md` owns task class, Direct vs non-trivial routing, existing-system/domain-execution boundary, continuity, source/claim ownership, skill budget, and STOP behavior. Root `GITHUB_RULES.md` owns GitHub execution/history/CI/safety. Do not duplicate those rules here.

## Entry boundary

Use this skill only for **non-trivial Developing**.

Do not invoke it merely because code/files are involved. Direct Bounded work and bounded Maintenance should stay on their shorter route when wider stable context cannot materially change the solution or proof.

Do not invoke it for normal production, authoring, or domain execution when an existing system/procedure is simply being used to create or revise its intended output without changing system behavior.

Use this skill when material uncertainty, impact, risk, ownership coordination, migration, new persistent authority/material dependency boundary, difficult rollback, or target/human acceptance can change the implementation or acceptance.

## Sufficient continuity

Before implementation, recover only the current context that can materially change the decision:

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md when active continuation matters
→ this development-brief
→ smallest relevant owner/caller/contract evidence
```

In the same bounded task/session, already verified context may be reused unless relevant repository state could have changed.

If `next-action.md` materially disagrees with current source/state:

```text
inspect exact current owner
→ identify stale continuity vs stale implementation
→ reconcile stale owner
→ continue from actual truth
```

## Development contract

Establish only fields that can change the decision:

```text
Goal
Actual requirement
Suggested method / observed reference (if material)
Input authority
Expected output
Build POV / responsible owner set
Acceptance POV
Interface constraints (if material)
In scope / Out of scope
Acceptance criteria: 2–5
Proof budget
Open high-impact decisions
Execution channel only when it constrains implementation/proof
```

This is an internal contract. Do not create a per-task plan/report file merely to store it.

## Procedure

### 1. Ground the goal

Separate current fact, approved decision, proposal/method, historical evidence, derived artifact, and unknown.

Treat frameworks, screenshots, samples, old branches/source, reference projects, and technical suggestions as evidence/method proposals unless the current requirement explicitly adopts them.

Recover discoverable repository facts before asking the user. If a high-impact product/architecture/privacy/data/release/acceptance decision remains unresolved, return to Plan instead of inventing it.

If the request is actually normal existing-system/domain execution, leave Developing and route to the matching domain owner/procedure instead of forcing this contract.

### 2. Development necessity gate

```text
normal existing-system/domain execution
→ matching domain owner/procedure

current behavior already satisfies goal
→ No change required

requirement materially unresolved
→ Plan / Context Recovery

suggested method unsupported/disproportionate
→ Redirect / Refine

grounded non-trivial system change required
→ Develop
```

Do not create a patch merely to create output.

### 3. Find the smallest coherent owner set

Find the current semantic owner plus the callers/contracts/tests that can materially affect correctness.

The invariant is **one canonical owner per responsibility**, not one owner per task.

A complete change may require, for example:

```text
contract
+ implementation
+ regression assertion
```

Do not create a second service/store/controller/config/authority when the existing owner can represent the responsibility correctly.

### 4. Define minimum complete scope

Define explicit in/out scope where adjacent systems are easy to confuse.

Choose 2–5 falsifiable acceptance criteria. Criteria should describe required observable outcomes rather than incidental implementation detail unless that detail is itself required.

Choose the cheapest proof capable of falsifying each changed claim.

### 5. Complexity guard

Before adding a high-cost persistent layer—new service/runtime/state authority/provider/router/registry/compatibility/fallback/cache/queue/material dependency boundary/workflow/specialist/governance owner—establish:

```text
current demonstrated need
why the existing/direct solution is insufficient
current consumer
unique required capability or net complexity reduction
new failure/maintenance cost
whether an equally correct smaller solution exists
```

If an equally correct smaller solution exists, use it.

Do not add architecture for “best practice”, “clean architecture”, future scalability, or possible future use alone.

### 6. Select at most one useful specialist

Normal non-trivial Developing budget:

```text
development-brief
+
zero or one project specialist
```

Select by recurring semantic responsibility, not programming language/framework name. If no specialist adds material procedure, use none.

If a second independent problem appears, close/reframe the current boundary rather than stacking scopes/specialists.

Domain execution uses the project-defined production/authoring procedure or specialist budget instead; this skill does not invent that routing.

### 7. Implement and prove

- fix the first wrong owner;
- preserve valid behavior outside scope;
- make the smallest complete coherent change;
- do not hide unknown root causes with arbitrary retry/delay/fallback;
- follow `GITHUB_RULES.md` for atomicity/history/tool fit;
- run only proof relevant to the changed claims.

### 8. Final gate

Before completion verify:

- goal and expected output achieved;
- Acceptance POV satisfied;
- acceptance criteria supported by proof actually obtained;
- scope remained bounded;
- each responsibility still has one canonical owner;
- no speculative layer, duplicate state, ceremonial test/report, fake success, or unrelated cleanup was introduced.

If implementation is complete but required target/human proof is unavailable, report `Perlu pemeriksaan`, not `Selesai`.

Update `next-action.md` only when active status, boundary, blocker, proof requirement, or next meaningful action actually changed.

Then STOP.