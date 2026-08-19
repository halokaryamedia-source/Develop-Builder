---
name: development-brief
description: Mandatory front door for non-trivial Developing after sufficient Project Definition exists. Recover current continuity, verify the affected durable contract is defined, ground the real goal, separate outcome from suggested method, identify the smallest coherent owner set, define 2-5 falsifiable acceptance criteria and a proportional proof budget, then use at most one useful specialist. Do not use for Direct Bounded work or normal existing-system/domain execution when wider context cannot materially change the decision.
---

# Development Brief

Turn a non-trivial development request into the **smallest grounded final development contract** without skipping project-definition prerequisites or adding ceremony/source generations.

Root `AGENTS.md` owns task class, bootstrap/readiness routing, current-source finalization, continuity, source/claim ownership, local-rule inheritance, skill budget, and STOP behavior. `docs/README.md` owns documentation architecture and Project Definition readiness. Root `GITHUB_RULES.md` owns GitHub execution/history/CI/safety.

## Entry boundary

Use only for **non-trivial Developing**.

Do not invoke merely because code/files exist. Direct Bounded work and bounded Maintenance stay on their shorter route when wider stable context cannot materially change solution/proof.

Do not invoke for normal production, authoring, or domain execution when an existing system/procedure is simply being used without changing system behavior.

## Mandatory Developing continuity

Before implementation:

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ this development-brief
→ nearest relevant AGENTS.md when one exists and matters
→ smallest relevant foundation/source/caller/contract evidence
```

If continuity and current source disagree, reconcile stale continuity vs stale implementation before proceeding.

## Development contract

Establish only fields that can change the decision:

```text
Goal
Actual requirement / foundation owner
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

Treat frameworks, screenshots, samples, old branches/source, reference projects, and technical suggestions as evidence/method proposals unless current requirements adopt them.

Recover discoverable repository facts before asking the user. If a high-impact decision remains unresolved, return to Plan instead of inventing it.

If the request is normal existing-system/domain execution, route to the matching domain owner/procedure.

### 2. Project Definition Gate

Before implementing non-trivial product/system behavior, verify that the affected project contract is sufficiently defined.

Use `docs/README.md` as the canonical readiness rule. Check only the smallest applicable set:

- purpose/consumer and deliverable are known;
- relevant input/source authority is sufficient;
- scope/non-goals are current;
- affected observable requirements are owned;
- any material product/domain flow is defined;
- any domain boundary that changes ownership/correctness is owned;
- architecture/data/security/interface decisions required **before this implementation** are resolved or explicitly blocking;
- material quality rules are owned;
- acceptance/proof for the changed claims is defined;
- Foundation Expansion Gate has been applied to the affected responsibility.

If a required contract is missing:

```text
DO NOT IMPLEMENT THE UNDEFINED BEHAVIOR
→ return to Plan / Project Definition
→ recover or decide the missing contract
→ update the current foundation owner
→ re-check readiness
```

Do not create documents just to pass the gate. A missing document is a problem only when a missing **responsibility/contract** can change implementation or acceptance.

A bounded discovery/prototype may precede readiness only when it is the minimum evidence needed to resolve a material unknown. It does not silently become product implementation; its result returns to the correct foundation owner first.

### 3. Development necessity gate

```text
current behavior already satisfies goal
→ No change required

requirement materially unresolved
→ Plan / Project Definition

suggested method unsupported/disproportionate
→ Redirect / Refine

grounded non-trivial system change required
→ Develop
```

Do not create a patch merely to create output.

### 4. Find the smallest coherent owner set

Find the current semantic owner plus callers/contracts/tests that can materially affect correctness.

The invariant is **one canonical owner per responsibility**, not one owner per task.

A complete change may require:

```text
contract
+ implementation
+ regression assertion
```

Inspect relevant existing regression assertions/invariants before writing when they constrain the change.

When replacing an owner/path, identify what becomes obsolete before implementation so the final patch does not leave old/new generations behind.

### 5. Define minimum complete final scope

Define explicit in/out scope where adjacent systems are easy to confuse.

Choose 2–5 falsifiable acceptance criteria describing required observable outcomes.

Choose the cheapest proof capable of falsifying each changed claim.

The scope describes the **final current state**, not staged accumulation of old + new + compatibility unless a current external contract requires coexistence.

### 6. Hard anti-AI-slop / complexity gate

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

- version-suffixed owner generations;
- old/new/legacy/backup copies;
- parallel old/new runtime or state authorities;
- compatibility aliases/fallback bridges without current external obligation;
- preserving superseded behavior “just in case”;
- speculative framework/scalability layers;
- per-task reports or decision layers created because work feels important;
- temporary structures promoted to permanent source without live responsibility;
- broad fallback/retry used to hide unknown root cause.

Git history is sufficient for ordinary historical preservation and rollback.

### 7. Select at most one useful specialist

Normal non-trivial Developing budget:

```text
development-brief
+
zero or one project specialist
```

Select by recurring semantic responsibility, not programming language/framework/library name.

Domain execution uses an already-earned project production/authoring procedure; this skill does not invent one.

### 8. Implement the final source and prove it

- fix the first wrong owner;
- preserve valid behavior outside scope;
- implement the smallest complete final solution;
- update required callers/contracts/tests coherently;
- remove superseded current source/path/state when safe;
- do not keep old/new generations for convenience;
- follow `GITHUB_RULES.md` for atomicity/history/tool fit;
- run only proof relevant to changed claims.

### 9. Final gate

Before completion verify:

- goal and expected output achieved;
- Acceptance POV satisfied;
- acceptance criteria supported by proof actually obtained;
- scope remained bounded;
- each responsibility has one current canonical owner;
- affected Project Definition remains current;
- superseded current source/path/state is removed when no external contract requires it;
- no speculative layer, duplicate state, ceremonial test/report, fake success, or unrelated cleanup was introduced.

If implementation is complete but required target/human proof is unavailable, report `Perlu pemeriksaan`, not `Selesai`.

Update `next-action.md` only when active status, boundary, blocker, proof requirement, or next meaningful action changed.

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

Do not dump the internal contract by default. Normal domain execution should deliver requested output rather than repository-development ceremony.
