# GitHub Rules

Canonical GitHub execution policy for this repository and reusable starter kernel.

Root `AGENTS.md` owns task class, routing, continuity, semantic scope, current-source finalization, and architecture-addition judgment. This file owns GitHub/ref/write/history/CI/API/security mechanics. Nearer repository rules may narrow local behavior but must not weaken integrity, proof, history, security, single-source ownership, or STOP boundaries.

For normal repository work apply **Core Rules 1–7**. Read a **Conditional GitHub Surface** only when the current task touches it; PR, release, Actions, LFS, or deployment rules are not extra boot requirements for a bounded text edit.

```text
PIN
→ READ MINIMUM
→ DIAGNOSE
→ TOOL FIT
→ WRITE COHERENTLY
→ VERIFY MINIMUM
→ STOP
```

# Core Rules

## 1. PIN — exact current authority

Before a material GitHub mutation, know the repository, intended ref, current HEAD/state, requested scope, and whether the target is writable.

- `Local` is the working/development authority.
- Never silently use the repository default or another branch when the task targets `Local`.
- Every supported write explicitly targets the intended ref when the active tool supports it.
- Direct branch/file fetch is current-state authority; search is discovery only.
- Re-check HEAD only when concurrent movement is plausible or immediately before an overwrite-sensitive coordinated ref update.
- Replacement/deletion uses the current blob/content SHA from the exact target ref. On stale state, refetch once and rebuild the intended final state; never guess or substitute another identifier type.
- Protected, production, release, archived, or read-only refs are not mutation targets unless repository policy or explicit user instruction authorizes that exact action.
- Current source plus relevant proof owns actual behavior. If continuation prose materially conflicts with current source/state, reconcile the stale owner before continuing.

A Direct Bounded Path still pins repo/ref and inherits these safety rules.

## 2. READ MINIMUM — only evidence that can change the decision

After any continuity required by `AGENTS.md`:

```text
owner/source reads   1–3 by default
history reads        0 by default
broad scans          0 by default
```

- Open more only for a concrete unresolved question.
- Read callers/contracts/tests when they can change blast radius, ownership, or acceptance.
- Do not broad-read history, old reports, generated artifacts, adjacent owners, all specialists, or dependency trees merely to feel safer.
- Partial, truncated, paginated, or capped output is incomplete evidence, not proof of absence.
- Continue pagination or narrow a query only when unseen data can materially change the decision.
- A missing result may mean missing, inaccessible, stale ref, or unindexed. Verify the exact repository/ref/access once before concluding absence; do not guess alternate branches or paths.
- Old commits/branches/files are historical evidence only. Do not promote them into current source unless the current task explicitly requires bounded recovery/reconciliation.

## 3. DIAGNOSE — fix the first wrong owner

Before writing, establish actual vs expected behavior and identify the first responsibility that is wrong.

```text
intended behavior / policy wrong
→ foundation / semantic requirement owner

requirement correct + implementation wrong
→ implementation owner

implementation correct + regression assertion stale
→ test owner

implementation/test correct + CI routing wrong
→ workflow / repository policy

implementation/routing correct + required runtime/toolchain unavailable
→ environment / capability boundary

requested proof missing despite otherwise complete implementation
→ proof boundary remains incomplete

derived/generated output wrong
→ upstream canonical source / generator

continuation stale + current source correct
→ continuation owner

historical failure not reproduced or currently required
→ no active change
```

- Do not fix the easiest file merely because it is writable.
- Do not widen Maintenance into redesign.
- Do not perform unrelated cleanup, refactors, compatibility work, dependency upgrades, documentation synchronization, or framework creation unless they block current acceptance.
- CI failure is evidence to diagnose, not permission to mutate unrelated product code.
- Historical TODOs/audits/failures are not active work unless reproduced or explicitly promoted by current intent.
- Do not create old/new parallel paths merely because replacement feels risky; identify the real current contract and make the minimum complete final change.
- `No change required` is valid.

## 4. TOOL FIT — match repository semantics to the operation

Use the simplest mutation channel that preserves correctness and history quality.

```text
exact current branch/file state
→ direct GitHub fetch

one small bounded UTF-8 file
+ one logical delivery
+ complete current file known
→ contents-style file mutation

coherent multi-file delivery
/ commit atomicity matters
/ large file or precise patch
/ coordinated refactor
/ binary, Git LFS, or special file
→ atomic git/tree/commit capability or suitable local git workspace

CI diagnosis
→ failing run → job/step → exact relevant log

runtime/device/visual/audio/model/target claim
→ actual matching capability
```

Contents-style mutation is authored-state mutation, not a scratch/probe/preflight mechanism. Never create temporary/test files on `Local` to discover tool behavior, and do not use per-file mutation when it would turn one logical delivery into commit spam.

When low-level atomic Git capability is genuinely required and available:

```text
pinned HEAD + base tree
→ create required blobs
→ create one candidate tree from the base tree
→ keep working ref unchanged during preparation
→ re-check HEAD when concurrent movement is plausible
→ create one commit with current pinned HEAD as parent
→ fast-forward intended ref once
```

Unreferenced candidate blobs/trees/commits are acceptable preflight objects because they do not move the working ref. They are not repository history until deliberately referenced.

Hard stops:

- Never full-replace a file from partial context.
- Never split a whole-file replacement API into chunks as if it were append/patch semantics.
- Keep blob/content SHA, tree SHA, commit SHA, tag/ref, workflow-run ID, artifact ID, and job ID distinct.
- Low-level blob/tree/commit/ref operations are not the default editor; reserve them for genuine atomic-delivery semantics.
- Never use force-push, history rewrite, destructive reset, or ref manipulation as a workaround for stale state, connector limits, CI failure, commit spam, or messy history.
- Permission, policy, safety, or capability denial ends that operation unless materially new evidence changes the condition.
- Do not change repository structure merely to make a connector/tool easier to use.
- If the active channel cannot perform the change safely or preserve required history quality, use or report the suitable channel instead of forcing completion.

## 5. WRITE COHERENTLY — one logical final result

Before the **first working-ref mutation**, pass this transaction gate:

```text
repo / intended ref / current HEAD pinned
scope + smallest coherent owner set ready
complete intended file contents / patch state ready
superseded current paths identified
mutation channel matches delivery shape
no scratch / temporary repository path required
expected proof known

any NO
→ DO NOT MUTATE YET
```

Prepare the complete logical result before committing when practical.

- One intentional write per file is the default, but one write does not mean one commit per file.
- Same-file and overlapping mutations are serial, never parallel.
- Reuse successful mutation responses and returned identifiers as current state; do not immediately refetch for reassurance unless concurrency or proof requires it.
- For coordinated atomic work, keep the working ref unchanged while candidate blobs/tree are prepared. If HEAD moves materially before the ref update, rebuild from current state rather than layering a stale result on top.
- A logical delivery may touch several files when they form the smallest coherent owner set.
- Update README/CONTEXT/continuation/proof metadata only when their owned state actually changes.
- Preserve lockfiles, runtime/version files, dependency constraints, pins, and action references unless their drift is the first wrong owner or the task explicitly requires a change.
- Generated/derived artifacts follow their canonical source/generator; do not patch generated output to hide an upstream defect.
- New files, workflows, abstractions, compatibility layers, fixtures, reports, branches, PRs, issues, comments, labels, releases, and other persistent side effects default to zero unless current scope proves a real need.
- Architecture/governance additions are justified by `AGENTS.md` / `development-brief`; this file governs safe repository execution after that decision.

### Single-source replacement rule

When replacing current behavior or policy:

```text
canonical owner updated
+ required callers/contracts/tests updated
+ obsolete current path/state removed when safe
= one logical delivery
```

Do not leave `_old`, `_new`, `_legacy`, `v2`, backup copies, duplicate config/state, alternate service paths, or compatibility aliases merely to make the change feel reversible. Git history is the normal rollback/history mechanism.

A retained compatibility/migration path requires a named current external contract. Without that contract, remove the superseded path in the same coherent delivery when safe.

### Commit discipline — history must remain meaningful

A commit is a **categorized logical delivery**, not a save point, reasoning checkpoint, tool call, scratch experiment, CI trigger, proof marker, or artificial version boundary.

Default delivery:

```text
prepare complete logical change
→ cheapest relevant pre-commit proof available
→ review intended final diff/state
→ one categorized logical commit
→ one push/ref update
→ only relevant CI
→ STOP
```

Commit gate:

```text
one coherent outcome?
primary category clear?
intended file set complete?
superseded current paths handled?
message explains repository outcome?
reviewable / revertable as one unit?

any NO
→ DO NOT COMMIT YET
```

Default message:

```text
<type>(<optional-scope>): <concise logical outcome>
```

Categories:

```text
feat      new capability
fix       wrong behavior or regression
docs      documentation/policy-only outcome
refactor  internal restructuring without intended behavior change
test      regression-contract-only outcome
ci        workflow/routing outcome
build     dependency/toolchain outcome
release   explicit release/publish state
chore     bounded maintenance only when no clearer category fits
```

- A fix may include its tests/supporting docs when they prove/document the same outcome.
- Split commits only for genuinely independent logical deliveries that can be reviewed/reverted separately.
- Do not split by file, directory, technical layer, tool call, work order, discovery order, or “old vs new” generation.
- More than one commit for one requested task requires a concrete logical boundary.
- Avoid vague history such as `update`, `changes`, `fix again`, `sync`, `final`, `try`, `rerun`, `proof`, `noop`, `v2`, or `misc`.
- Do not create checkpoint/cleanup commits to compensate for avoidable intermediate repository mutations.
- Never rewrite published/shared history merely for aesthetics without explicit authority.
- When the active tool would create commit spam for one coherent result, use a known-safe atomic channel or report the required channel.

## 6. VERIFY MINIMUM — validation follows the claim

Validation is evidence, not ceremony.

- Run the cheapest check that can falsify the changed claim.
- Targeted proof is the default during iteration and for Direct Bounded work.
- Use broader/full verification only when changed executable/public contracts can realistically affect that broader surface and the final gate adds material evidence.
- When CI is relevant, prefer the relevant gate on the final logical state; intermediate runs are not final proof.
- Only completed successful execution is PASS. Queued, running, pending, cancelled, skipped, neutral, or superseded states are not PASS.
- A superseded run need not be waited on when a newer relevant run replaces it.
- Do not rerun unchanged checks or chase unrelated verifiers merely for reassurance/green status.
- On failure, inspect the exact failing run/job/step and relevant error before editing.
- Do not weaken, delete, bypass, or broaden a valid test/workflow merely to obtain green; change it only when evidence shows the verifier itself is the first wrong owner.
- Same-cause retry budget: maximum **2**, and a second attempt requires materially new evidence.
- Permission/capability denial retry budget: **0** unless the condition changes.
- Regression tests protect material, realistically recurring invariants—not every typo, cosmetic wording change, or temporary state.
- Do not use exact natural-language prose as a test contract unless the exact string itself is machine-required.
- Source/hosted proof establishes only what it actually exercises. It never silently becomes runtime/device/visual/audio/model/target-machine/human acceptance.

## 7. STOP — completion is terminal

When requested outcome, acceptance boundary, and minimum relevant proof are satisfied, stop.

Do not automatically:

- audit another layer;
- synchronize unrelated docs;
- run another verifier;
- create proof-of-proof;
- fix adjacent non-blocking issues;
- create branches/PRs/issues/comments/releases for ceremony;
- reopen historical TODOs/audits;
- create a new version/generation of a solved owner;
- start the next milestone;
- continue because more tooling is available.

## Default efficiency budget

```text
owner/source reads        1–3 after required continuity boot
history reads             0 by default
broad scans               0
new files                 0 unless required
new workflows             0 unless required
new abstractions          0 unless required
versioned replacement     0 unless external contract requires it
legacy/parallel owners    0
intentional writes/file   1 by default
logical commits/task      1 by default
uncategorized commits     0
intermediate commits      0
CI-trigger commits        0
proof-only commits        0
scratch/temporary commits 0
push/ref updates/task     1 by default
relevant CI               0–1 per affected proof surface
same-cause retry          <= 2
capability-denial retry   0
adjacent cleanup          0
high-impact mutations     0 unless explicitly authorized
```

Exceed a budget only when concrete current evidence requires it.

# Conditional GitHub Surfaces

Apply only when the current task touches that surface. These sections do not add steps to unrelated bounded work.

## API failures, pagination, rate limits, and ambiguous mutations

```text
401        authentication problem
403        permission / policy / rate-limit investigation
404        missing OR inaccessible / stale target
409        conflict / stale state → refetch relevant state
422        invalid request / policy failure → fix request before retry
429        rate limited → respect server retry/reset guidance
5xx/timeout after mutation → outcome may be UNKNOWN; inspect current state first
```

- Do not create request storms or parallel mutation bursts.
- Respect retry/rate-limit signals instead of repeatedly probing.
- If a mutating request has an unknown outcome, refetch the exact target state first. Retry only after confirming the intended mutation is absent; this prevents duplicate files, branches, issues, comments, releases, or writes.
- A 404 is not proof that the target never existed; repository/ref/access may be wrong or unavailable.

## Special files, Git LFS, binaries, symlinks, submodules, and generated artifacts

Before treating repository content as ordinary UTF-8 text, distinguish regular files from symlinks, submodules, Git LFS pointers, generated artifacts, binaries, and files outside practical tool limits.

- Never hand-edit an LFS pointer as though it were the large-file content.
- Do not rewrite a symlink, submodule, or binary through plain-text replacement unless that representation is explicitly the intended source.
- Generated/derived artifacts follow their canonical source; fix source and regenerate unless repository policy explicitly defines the artifact as authored source.

## Pull requests, branch protection, rulesets, reviews, and merge queues

When a task involves a PR or merge/high-impact branch decision:

- Refresh current PR head SHA, base, mergeability, required reviews/CODEOWNERS state, required checks, and relevant deployment/environment gates before acting.
- A new commit can stale prior approvals/check assumptions; do not act from an old PR snapshot.
- Required human review, CODEOWNERS approval, branch protection, repository rulesets, signed-commit requirements, linear-history rules, merge queues, and deployment gates are authority—not errors to bypass.
- If merge-queue CI routing is wrong, fix the workflow event/routing contract rather than avoiding the queue.
- Force-push/history rewrite, branch/tag deletion, PR merge/close, release publication/deletion, environment bypass, repository settings/permission/rules changes, and similar externally visible mutations require explicit task authority and an exact current target.
- Perform only the requested high-impact mutation; do not add repository-object cleanup or ceremony.

## GitHub Actions and hosted proof

GitHub Actions is verification/deployment infrastructure, not a remote/background development engine.

- Automatic workflows run only on intended branches/events/paths whose checks can actually falsify the relevant claims.
- Documentation/routing/planning/status changes do not justify a full executable product suite unless a check explicitly owns them.
- Correctly skipped irrelevant workflows are not missing proof; do not manufacture unrelated changes to trigger them.
- A required but skipped/missing check is CI/ruleset routing, not permission to change unrelated product code.
- Prefer fail-fast when downstream checks are meaningless after an upstream failure.
- Cancel/supersede older runs when their results are no longer useful.
- Verification workflows are read-only by default and must not commit/push back to the working branch unless an explicitly designed repository contract requires that behavior.
- Publishing/release bundling is explicit release work, not a default side effect of development pushes.
- Do not create temporary/one-use workflows merely because the active channel lacks another capability.
- Do not rerun an unchanged failed workflow merely to seek green.
- Understand event and credential semantics before relying on workflow chaining.
- Use least-privilege workflow/token permissions. Do not widen permissions, expose protected data, or switch credentials merely to make CI pass.
- Preserve repository-declared action/runtime versions unless version drift is the actual issue. For new third-party actions, prefer trusted sources and immutable/pinned revisions where practical; never move to `latest`, `main`, or `master` as a convenience fix.
- Treat issue/PR titles and bodies, branch names, labels, commit messages, workflow inputs, and other event-derived strings as untrusted input. Validate before privileged shell/script use.
- `pull_request_target` and equivalent privileged base-context workflows are security boundaries. Never execute untrusted PR code with secrets/write tokens or other privileged context without a separately reviewed safe design.
- Fork contributions may intentionally lack protected credentials; do not weaken repository policy merely to make fork CI green.
- Never route untrusted PR code to a privileged or persistent self-hosted runner merely to gain missing capabilities.
- Hosted proof proves only what the hosted runner actually executes; it does not become target-device/runtime/user-environment acceptance automatically.

## Sensitive data, releases, and deployment environments

- Never commit, paste, echo, or move secrets such as API keys, access tokens, passwords, private keys, authorization headers, `.env` credentials, or sensitive user data into source, workflows, issues, PRs, comments, logs, or documentation.
- If protected data is discovered, do not reproduce its value. Report only the affected location/type and treat the exposure as a security issue.
- Redaction/masking in logs is not permission to intentionally print a secret.
- Security/privacy/data-loss/destructive/release operations require authorization and evidence proportional to risk; a small diff is not automatically low risk.
- Environment/release/deployment approval gates are authoritative constraints, not ordinary CI failures. Do not bypass required reviewers/protection for convenience.
