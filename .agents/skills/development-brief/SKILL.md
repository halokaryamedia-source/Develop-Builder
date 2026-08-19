---
name: development-brief
description: Mandatory front door for non-trivial Developing after sufficient Project Definition and initial capability planning exist. Recover current continuity, verify the affected durable contract and evidence basis are current enough, ground the real goal, identify the smallest coherent owner set, define 2-5 falsifiable acceptance criteria and a proportional proof budget, then use zero or one already-earned matching project specialist. Do not create new specialists inside a normal development task.
---

# Development Brief

Turn a non-trivial development request into the **smallest grounded final development contract** without skipping project-definition prerequisites, inventing project meaning, or adding unnecessary structure.

Root `AGENTS.md` owns task class/routing/per-task skill budget. `docs/README.md` owns documentation architecture/readiness. `project-definition` owns critical project-definition judgment. `project-skill-planner` owns creation/pruning of project specialists. Root `GITHUB_RULES.md` owns GitHub execution/history/CI/safety.

## Entry boundary

Use only for **non-trivial Developing**.

Do not invoke merely because code/files exist. Direct Bounded work and bounded Maintenance stay on their shorter route when wider stable context cannot materially change solution/proof.

Do not invoke for normal production/authoring/domain execution when an existing procedure is simply being used without changing system behavior.

Do not create a new project specialist here. Specialist necessity belongs to `project-skill-planner` outside the normal bounded implementation task.

## Mandatory Developing continuity

```text
AGENTS.md
→ GITHUB_RULES.md Core Rules when material
→ CONTEXT.md
→ docs/knowledge/next-action.md
→ this development-brief
→ nearest relevant AGENTS.md when one exists and matters
→ smallest relevant Foundation / current Knowledge navigation / source / caller / contract evidence
→ zero/one already-earned matching project specialist when useful
```

If continuity and current source disagree, reconcile stale continuity vs stale implementation before proceeding.

Knowledge is navigation/current development context only; do not use it as a substitute for Foundation requirements or direct source inspection.

## Development contract

Establish only fields that can change the decision:

```text
Goal
Actual requirement / Foundation owner
Suggested method / observed reference (if material)
Input authority / material evidence basis
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
Matching existing project specialist (only when useful)
```

This is an internal contract. Do not create a per-task plan/report/version file merely to store it.

## Procedure

### 1. Ground the goal

Separate current fact, approved decision, proposal/method, historical evidence, derived artifact, and unknown.

Treat frameworks, screenshots, samples, old branches/source, reference projects, and technical suggestions as evidence/method proposals unless current requirements adopt them.

Recover discoverable repository facts before asking the user. For material current external API/library/platform/support facts, use current authoritative/primary evidence when available rather than guessing.

If project meaning is materially unresolved, return to `project-definition` / Plan instead of inventing it. If the request is normal existing-system/domain execution, route to the matching domain owner/procedure.

### 2. Project Definition and evidence gate

Before implementing non-trivial product/system behavior, verify the affected contract is sufficiently defined and its material factual basis is usable.

Use `docs/README.md` as the canonical readiness rule. Check only the smallest applicable set:

- purpose/consumer and deliverable are known;
- relevant input/source authority is sufficient;
- scope/non-goals and material negative requirements are current;
- affected observable requirements are owned;
- any material product/domain flow is defined;
- any domain boundary changing ownership/correctness is owned;
- architecture/data/security/interface decisions required before this implementation are resolved or explicitly blocking;
- material quality rules are owned;
- acceptance/proof for changed claims is defined;
- Foundation Expansion Gate has been applied;
- affected Foundation owners are mutually coherent;
- material source-backed premises are traceable enough to re-open/revalidate.

If a required contract/evidence basis is missing:

```text
DO NOT IMPLEMENT THE UNDEFINED BEHAVIOR
→ project-definition / Plan
→ recover or decide missing contract/evidence
→ update current Foundation owner(s)
→ re-check readiness
```

Do not create documents merely to pass the gate. A missing document is a problem only when a missing responsibility/contract/evidence basis can change implementation or acceptance.

### 3. Freshness gate for external premises

Foundation may record a requirement that was shaped by an external factual premise, but that old verification is not permanent proof.

When current implementation materially depends on a change-prone fact—platform/library/provider support, compatibility, limits, regulation, pricing/cost, model/runtime behavior, or another unstable external premise—ask:

```text
is the recorded source/version/date exact enough?
is staleness plausible for this task?
would a changed fact alter implementation/acceptance?
```

If yes, revalidate the smallest current authoritative/primary source needed. If sufficiently current evidence cannot be obtained, preserve `UNKNOWN` / `Perlu pemeriksaan`; do not assume the old fact still holds.

Do **not** re-research unrelated or stable claims for reassurance.

### 4. Development necessity gate

```text
current behavior already satisfies goal
→ No change required

requirement materially unresolved
→ project-definition / Plan

suggested method unsupported/disproportionate
→ Redirect / Refine

grounded non-trivial system change required
→ Develop
```

Do not create a patch merely to create output.

### 5. Find the smallest coherent owner set

Find the current semantic owner plus callers/contracts/tests that can materially affect correctness.

The invariant is **one canonical owner per responsibility**, not one owner per task.

A complete change may require:

```text
Foundation/contract
+ implementation
+ regression assertion
```

Inspect relevant existing regression assertions/invariants before writing when they constrain the change.

When replacing an owner/path, identify what becomes obsolete before implementation so the final patch does not leave old/new generations behind.

### 6. Define minimum complete final scope

Define explicit in/out scope where adjacent systems are easy to confuse.

Choose 2–5 falsifiable acceptance criteria describing required observable outcomes. Choose the cheapest proof capable of falsifying each changed claim.

The scope describes the **final current state**, not staged accumulation of old + new + compatibility unless a current external contract requires coexistence.

### 7. Hard anti-AI-slop / complexity gate

Before adding any persistent file, service, runtime, state authority, provider, router, registry, compatibility/fallback layer, cache, queue, material dependency boundary, workflow, governance owner, migration layer, feature flag, alias, or alternate path, establish:

```text
current demonstrated need
why existing canonical owner cannot satisfy it
current consumer / external contract
unique required capability or net complexity reduction
new failure/maintenance cost
whether an equally correct direct replacement exists
```

If an equally correct direct replacement exists, use it.

Forbidden by default:

- version-suffixed owner generations;
- old/new/legacy/backup copies;
- parallel old/new runtime/state authorities;
- compatibility aliases/fallback bridges without current external obligation;
- preserving superseded behavior “just in case”;
- speculative framework/scalability layers;
- per-task reports/decision layers because work feels important;
- temporary structures promoted to permanent source without live responsibility;
- broad fallback/retry hiding unknown root cause.

Git history is sufficient for ordinary historical preservation and rollback.

### 8. Select at most one useful project specialist

Normal non-trivial Developing:

```text
development-brief
+
zero or one already-earned project specialist
```

Select by recurring semantic responsibility, not programming language/framework/library name.

If no existing specialist adds material judgment, use none. If a genuinely new recurring semantic responsibility is discovered, finish/reframe the bounded task and route specialist necessity to `project-skill-planner`; do not create it ad hoc here.

### 9. Implement and prove

- fix the first wrong owner;
- preserve valid behavior outside scope;
- implement the smallest complete final solution;
- update required Foundation/contracts/callers/tests coherently;
- remove superseded current source/path/state when safe;
- do not keep old/new generations for convenience;
- follow `GITHUB_RULES.md` for atomicity/history/tool fit;
- run only proof relevant to changed claims.

If implementation changes project meaning rather than merely implementing it, return to `project-definition`; do not silently mutate product intent from source code.

### 10. Final gate

Before completion verify:

- goal and expected output achieved;
- Acceptance POV satisfied;
- acceptance criteria supported by proof actually obtained;
- scope remained bounded;
- each responsibility has one current canonical owner;
- affected Project Definition remains coherent/current;
- source-backed external premises used by the change are current enough for the claim;
- superseded current source/path/state is removed when no external contract requires it;
- no speculative layer, duplicate state, ceremonial test/report, fake success, or unrelated cleanup was introduced.

If implementation is complete but required target/human/current-external proof is unavailable, report `Perlu pemeriksaan`, not `Selesai`.

Update `next-action.md` only when active status, boundary, blocker, proof requirement, or next meaningful action changed. Then STOP.

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
