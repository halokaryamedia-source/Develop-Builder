---
name: development-brief
description: Mandatory front door for non-trivial Developing. Recover current stable context and active continuation, ground the real goal, separate outcome from suggested method, identify the smallest coherent owner set, define 2-5 falsifiable acceptance criteria and a proportional proof budget, then use at most one useful specialist. Do not use for Direct Bounded work or normal existing-system/domain execution when wider context cannot materially change the decision.
---

# Development Brief

Turn a non-trivial development request into the **smallest grounded final development contract that preserves correctness without adding ceremony or source generations**.

Root `AGENTS.md` owns task class, routing, current-source finalization, existing-system/domain-execution boundary, continuity, source/claim ownership, local-rule inheritance, skill budget, and STOP behavior. Root `GITHUB_RULES.md` owns GitHub execution/history/CI/safety. Do not duplicate those owners here.

## Entry boundary

Use this skill only for **non-trivial Developing**.

Do not invoke it merely because code/files are involved. Direct Bounded work and bounded Maintenance stay on their shorter route when wider stable context cannot materially change the solution or proof.

Do not invoke it for normal production, authoring, or domain execution when an existing system/procedure is simply being used to create/revise intended output without changing system behavior.

Use this skill when material uncertainty, impact, risk, ownership coordination, migration, new persistent authority/material dependency boundary, difficult rollback, or target/human acceptance can change implementation or acceptance.

## Mandatory Developing continuity

Before implementation:

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ this development-brief
→ nearest relevant AGENTS.md when one exists and matters
→ smallest relevant owner/caller/contract evidence
```

`CONTEXT.md` and `next-action.md` are mandatory so a new session does not invent project boundaries, repeat completed work, or select arbitrary TODO/history as current scope.

In the same bounded task/session, already verified continuity may be reused unless relevant repository state could have changed.

If `next-action.md` disagrees materially with current source/state:

```text
inspect exact current owner
→ stale continuity vs stale implementation
→ reconcile stale owner
→ continue from actual current truth
```

Do not blindly replay a stale step or replace it with a nearby TODO/audit/history item.

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
Superseded current owner/path to remove (only when replacement is involved)
External compatibility obligation (only when real)
```

This is an internal contract. Do not create a per-task plan/report/version file merely to store it.

## Procedure

### 1. Ground the goal

Separate current fact, approved decision, proposal/method, historical evidence, derived artifact, and unknown.

Treat frameworks, screenshots, samples, old branches/source, reference projects, and technical suggestions as evidence/method proposals unless the current requirement explicitly adopts them.

Recover discoverable repository facts before asking the user. If a high-impact product/architecture/privacy/data/release/acceptance decision remains unresolved, return to Plan instead of inventing it.

If the request is normal existing-system/domain execution, leave Developing and route to the matching domain owner/procedure.

If current owners materially disagree, use root `AGENTS.md` conflict-resolution semantics. Do not create a compatibility layer merely to let contradictory owners coexist.

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

Find the current semantic owner plus callers/contracts/tests that can materially affect correctness.

The invariant is **one canonical owner per responsibility**, not one owner per task.

A complete change may require:

```text
contract
+ implementation
+ regression assertion
```

Inspect relevant existing regression assertions/invariants before writing when they can constrain the change; do not use intermediary commits/pushes as avoidable regression discovery.

Do not create a second service/store/controller/config/authority when the existing owner can represent the responsibility correctly.

When replacing an owner/path, identify what becomes obsolete **before** implementation so the final patch does not leave old/new generations behind.

### 4. Define minimum complete final scope

Define explicit in/out scope where adjacent systems are easy to confuse.

Choose 2–5 falsifiable acceptance criteria describing required observable outcomes rather than incidental implementation detail unless that detail is required.

Choose the cheapest proof capable of falsifying each changed claim.

The scope must describe the **final current state**, not a staged accumulation of `old + new + compatibility` unless a current external contract truly requires coexistence.

### 5. Hard anti-AI-slop / complexity gate

Before adding any persistent file, service, runtime, state authority, provider, router, registry, compatibility/fallback layer, cache, queue, material dependency boundary, workflow, specialist, governance owner, migration layer, feature flag, alias, or alternate path, establish:

```text
current demonstrated need
why the existing canonical owner cannot satisfy it
current consumer / external contract
unique required capability or net complexity reduction
new failure/maintenance cost
whether an equally correct direct replacement exists
```

If an equally correct direct replacement exists, use it.

Forbidden by default:

- versioned owner generations (`v2`, `v3`, etc.);
- `new`/`old`/`legacy`/backup copies;
- parallel old/new runtime or state authorities;
- compatibility aliases or fallback bridges without a current external obligation;
- preserving superseded behavior “just in case”;
- speculative framework/scalability layers;
- per-task reports, migration frameworks, decision layers, or specialists created because the change feels important;
- temporary structures promoted to permanent source without a live responsibility;
- broad fallback/retry used to hide an unknown root cause.

Git history is sufficient for ordinary historical preservation and rollback.

Every fallback/retry must handle a named expected condition or proved failure mode.

A real compatibility/migration boundary is permitted only when a current external contract requires it. Record the contract; keep the boundary minimal; do not create a second product/runtime authority.

### 6. Select at most one useful specialist

Normal non-trivial Developing budget:

```text
development-brief
+
zero or one project specialist
```

Select by recurring semantic responsibility, not programming language/framework/library name. If no specialist adds material procedure, use none.

If a second independent problem appears, finish/reframe the current boundary instead of stacking scopes/specialists.

Domain execution uses an already-earned project production/authoring procedure instead; this skill does not invent one.

### 7. Implement the final source and prove it

- fix the first wrong owner;
- preserve valid behavior outside scope;
- implement the smallest complete final solution;
- update required callers/contracts/tests coherently;
- remove superseded current source/path/state when safe;
- do not keep old/new generations for convenience;
- do not hide unknown root causes with arbitrary retry/delay/fallback;
- follow `GITHUB_RULES.md` for atomicity/history/tool fit;
- run only proof relevant to changed claims.

### 8. Final gate

Before completion verify:

- goal and expected output achieved;
- Acceptance POV satisfied;
- acceptance criteria supported by proof actually obtained;
- scope remained bounded;
- each responsibility has one current canonical owner;
- superseded current source/path/state from this change is removed when no external contract requires it;
- no `v2`/`legacy`/old/new/backup generation was introduced as an AI development technique;
- no placeholder/dry-run/mock/stale marker or fallback was promoted beyond the narrow claim it proves;
- no speculative layer, duplicate state, ceremonial test/report, fake success, temporary permanentization, or unrelated cleanup was introduced.

If implementation is complete but required target/human proof is unavailable, report `Perlu pemeriksaan`, not `Selesai`.

Update `next-action.md` only when active status, boundary, blocker, proof requirement, or next meaningful action actually changed.

Then STOP.

## User-facing brief

For non-trivial Developing, expose only enough meta-context to let the user steer material decisions. When useful:

```text
Tujuan:
Cara berpikir:
Hasil yang dituju:
Tidak diubah:
Cara memastikan benar:
```

- Do not dump the internal contract by default.
- Trivial/unambiguous corrections do not need this meta-brief.
- Normal domain execution should deliver requested output rather than repository-development ceremony.
- If a material decision needs user review, surface that decision directly instead of wrapping it in generic process language.
