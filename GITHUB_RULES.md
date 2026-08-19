# GitHub Rules — Develop-Builder

Canonical GitHub execution policy for this repository and the generic preset baseline.

Root `AGENTS.md` owns task class, direct/escalated routing, continuity, semantic scope, and architecture-addition judgment. This file owns GitHub/ref/write/history/CI/security mechanics. Domain rules may narrow these rules but must not weaken integrity, proof, or STOP boundaries.

For normal material GitHub work:

```text
PIN
→ READ MINIMUM
→ DIAGNOSE
→ TOOL FIT
→ WRITE COHERENTLY
→ VERIFY MINIMUM
→ STOP
```

## 1. PIN — exact current authority

Before a material mutation, know the repository, intended ref, current state, requested scope, and whether the target is writable.

- `Local` is the working/development authority.
- Never silently use the repository default or another branch when the task targets `Local`.
- Direct file/branch state is current-state authority; search is discovery.
- Re-check HEAD only when concurrent movement is plausible or before an overwrite-sensitive coordinated write.
- Replacement/deletion must use current state from the intended ref.
- Protected/release/archived/read-only refs are not mutation targets unless explicitly authorized.

A Direct Bounded Path still pins repo/ref and inherits these safety rules.

## 2. READ MINIMUM — only evidence that can change the decision

After any task-class continuity required by `AGENTS.md`:

```text
owner/source reads   smallest sufficient set
history reads        0 by default
broad scans          0 by default
```

- Read callers/contracts/tests when they can change blast radius or acceptance.
- Do not broad-read history, old reports, generated artifacts, all specialists, or dependency trees merely to feel safer.
- Partial, truncated, paginated, or capped output is incomplete evidence, not proof of absence.
- Continue reading only when unseen data can materially change the decision.
- A missing result may mean missing, inaccessible, stale ref, or unindexed; verify the exact intended source once before concluding absence.

## 3. DIAGNOSE — first wrong owner

Before writing, establish actual vs expected behavior and the first responsibility that is wrong.

```text
intended behavior/policy wrong
→ foundation / semantic requirement owner

requirement correct + implementation wrong
→ implementation owner

implementation correct + regression assertion stale
→ test owner

source/test correct + CI routing wrong
→ workflow/repository policy

derived/generated output wrong
→ upstream canonical source/generator

continuation stale + source correct
→ continuation owner

historical failure not reproduced/currently required
→ no active change
```

Do not fix the easiest file. Do not widen Maintenance into redesign. `No change required` is valid.

## 4. TOOL FIT — match the operation

Use the simplest mutation channel that preserves correctness and history quality.

```text
exact current file/branch state
→ direct GitHub fetch

one small bounded UTF-8 file
+ one logical delivery
→ contents-style file mutation

coherent multi-file delivery
/ atomicity matters
/ coordinated refactor
/ binary or special file
→ atomic git/tree/commit capability or suitable local git workspace

CI diagnosis
→ failing run/job/step → exact relevant log

runtime/device/visual/target claim
→ actual matching capability
```

Do not split one coherent multi-file result into commit spam merely because a per-file API is convenient.

Never full-replace a file from partial context. Keep blob/content SHA, tree SHA, commit SHA, ref, run ID, job ID, and artifact ID distinct.

Never use force-push, destructive reset, history rewrite, or ref manipulation as a workaround for stale state, connector limits, CI failure, or messy history.

## 5. WRITE COHERENTLY — one logical result

Prepare the intended result before committing when practical.

- A logical delivery may touch multiple files when they form the smallest coherent owner set.
- Same-file/overlapping mutations are serial.
- Reuse successful mutation responses as current state unless concurrency/proof requires refetch.
- Update README/CONTEXT/continuation only when their owned state actually changed.
- Generated artifacts follow their canonical source/generator; do not patch generated output to hide an upstream defect.
- New persistent side effects default to zero unless current scope proves need.
- Whether a new architecture/governance layer is justified is decided by `AGENTS.md` / `development-brief`; this file only governs how an approved repository change is executed safely.

### Commit discipline

A commit is a logical repository outcome, not a save point, reasoning checkpoint, CI trigger, or proof marker.

Default message:

```text
<type>(<optional-scope>): <concise outcome>
```

Useful categories:

```text
feat     new capability
fix      wrong behavior/regression
docs     docs/policy-only outcome
refactor internal structure, no intended behavior change
test     regression-contract-only outcome
ci       workflow/routing
build    dependency/toolchain
release  explicit release state
chore    bounded maintenance when no clearer category fits
```

Split commits only for genuinely independent outcomes that can be reviewed/reverted separately. Do not split by file, directory, frontend/backend layer, tool call, or discovery order.

## 6. VERIFY MINIMUM — validation follows the claim

Validation is evidence, not ceremony.

- Run the cheapest check that can falsify the changed claim.
- Targeted proof is the default for Direct Bounded work.
- Broader verification is justified only when the changed executable/public contract can realistically affect the broader surface.
- Only completed successful execution proves the surface it actually ran.
- Do not rerun unchanged checks for reassurance.
- On failure, inspect the exact failing surface before editing.
- Do not weaken valid tests/workflows to get green.
- Same-cause retry: maximum two attempts; a second attempt requires materially new evidence.
- Permission/capability denial retry: zero unless the condition changes.
- Source/hosted proof never silently becomes runtime/device/visual/model/target-machine/human proof.

## 7. STOP — completion is terminal

When requested outcome, scope, and required proof are satisfied, stop.

Do not automatically:

- audit another layer;
- synchronize unrelated docs;
- run another verifier;
- fix adjacent non-blocking issues;
- create branches/PRs/issues/comments/releases for ceremony;
- reopen historical TODOs;
- start the next milestone.

## Sensitive and high-impact operations

Security/privacy/data-loss/destructive/release operations require evidence and authorization proportional to risk. A change being small in lines does not make it low risk.

Never expose secrets, credentials, private keys, tokens, or sensitive user data in commits, logs, issues, or generated evidence.