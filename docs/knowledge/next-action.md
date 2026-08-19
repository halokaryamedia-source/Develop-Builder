# Next Action

## Current Status

```text
PRESET_V1_FROZEN_AND_GITHUB_PARITY_HARDENED
CORE_BOOTSTRAP_COMPLETE
CROSS_DOMAIN_ROUTING_AUDIT_COMPLETE
COMPLEXITY_PRUNING_AUDIT_COMPLETE
GITHUB_CORE_RULES_PARITY_COMPLETE
GITHUB_CONDITIONAL_SURFACES_RESTORED
PRE_WRITE_TRANSACTION_GATE_ADDED
AUTOMATED_TEMPLATE_VERIFIER_NOT_REQUIRED
PROMOTED_GOVERNANCE_NOT_ADDED
```

Working authority: **`Local`**.

Develop-Builder Core Bootstrap **v1** remains the accepted baseline. A post-freeze Maintenance audit found that the final pruning had removed several GitHub safety rules that are generic across BuildIT, TranslateIT, and PRD-Creator. Those rules have now been restored inside the existing `GITHUB_RULES.md` owner rather than by adding files, skills, workflows, or routing layers.

The hardened GitHub contract now preserves:

- PIN / READ MINIMUM / DIAGNOSE / TOOL FIT / WRITE COHERENTLY / VERIFY MINIMUM / STOP;
- a pre-write transaction gate that forbids scratch/temporary repository mutations;
- atomic multi-file preparation without moving the working ref until the logical result is ready;
- meaningful logical commit/history discipline and default efficiency budgets;
- retry and ambiguous-mutation handling;
- special-file/LFS/binary/symlink/submodule handling;
- PR/branch-protection/ruleset/review/merge-queue authority;
- GitHub Actions least-privilege and untrusted-input security boundaries;
- secret incident handling and release/deployment approval authority;
- proof boundaries that do not inflate hosted/static evidence into target/runtime/human acceptance.

These conditional surfaces apply only when the current task touches them, so they do not add routine ceremony to simple Direct Bounded work.

## Active Boundary

There is **no active kernel-development milestone** after this Maintenance correction.

Reopen the kernel only for reproduced evidence of:

- a routing/continuity/ownership defect;
- a task made unnecessarily complex by the preset;
- underdevelopment that skips a material contract/safety/proof requirement;
- GitHub behavior not correctly handled by the current core/conditional rules;
- repeated template drift that makes automation simpler than manual review;
- a demonstrated simplification that reduces current complexity without losing required responsibility.

Do not add promoted governance, specialists, workflows, runtime/domain architecture, or extra safety ceremony without such evidence.

## Proof Boundary

The current kernel has been statically compared against the shared operating patterns of BuildIT, TranslateIT, and PRD-Creator.

For GitHub behavior, the parity review covers the general reusable invariants represented across those repositories: authority pinning, minimum reading, first-wrong-owner diagnosis, tool fit, transaction/write discipline, history quality, minimum proof, STOP, API ambiguity, special files, PR/protection surfaces, Actions security, secrets, and release/deployment constraints.

This is repository/source policy proof. It does not prove behavior of a future project-specific runtime or user environment.

## Next Step

**Use Develop-Builder v1 as the bootstrap source for the next real project. Reopen only the exact affected Maintenance/Plan boundary when real use produces evidence of a kernel defect or a simpler complete rule; otherwise make no kernel change.**
