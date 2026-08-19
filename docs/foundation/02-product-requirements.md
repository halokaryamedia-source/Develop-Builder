# Product Requirements

> **Starter scaffold:** during Project Definition, replace this guidance with current observable requirements. Remove sections that do not apply. If one section grows into a distinct durable responsibility, use the Foundation Expansion Gate in `../README.md` instead of letting this file become a mixed owner.

## Product Priority

State the priorities that decide tradeoffs.

Example form:

```text
required outcome / correctness
> optional feature breadth
```

Use project-specific priorities only.

## Required Inputs and Source Authority

Define what inputs are required for the product/system to operate or for work to begin.

State which current sources/decisions are authoritative where ambiguity is material.

For any material requirement that depends on a source-backed external fact, retain enough source basis to re-open/revalidate the premise later. Do not treat an old external verification as permanent proof when the fact is change-prone.

## Expected Outputs / Deliverables

Define observable outputs and required deliverable qualities.

Distinguish canonical source/output from generated/derived artifacts when applicable.

## Core Behavior

Define what the system/product **must**, **must not**, and where useful **should** do.

Use requirement IDs only when cross-reference complexity benefits from them. Do not create numbering ceremony for a small project.

### Negative requirements are first-class

Preserve material removals, exclusions, replacements, `only`, and `must not` rules. Existing source, historical features, reference architectures, or compatibility instincts do not silently restore behavior current authority removed.

Do not broaden a negative requirement beyond its stated scope.

## Product / User / Operational Flow

If the flow is short and belongs to the same requirements responsibility, define it here.

If a multi-stage flow materially controls stage eligibility, ownership, downstream handoff, or acceptance, create a dedicated flow policy through the Foundation Expansion Gate and keep only the high-level reference here.

## Scope and Exclusions

State required scope plus material exclusions.

Existing source, historical plans, examples, or old features do not remain current scope unless current project authority includes them.

## Lifecycle / State

Use only when states/transitions materially affect behavior.

Example only when real:

```text
Ready → Running → Completed
```

Do not invent state machines for simple request/response behavior.

## Quality Requirements

Define only quality dimensions that materially control acceptance, such as visual fidelity/readability, correctness/completeness, latency/performance, reliability/recovery, editability when it is an observable need, or content/craft quality.

When a domain has recurring quality rules used across several tasks/owners, create a dedicated `<domain>-standard.md` instead of burying a second job here.

## Data / Privacy / Security

Use when material.

Define current data ownership, sensitivity, retention, destructive behavior, authorization, or privacy/security constraints.

If this becomes a substantial cross-cutting contract, split it through the Foundation Expansion Gate.

## Interfaces / Integrations

Use when material.

Define external/public contracts that constrain behavior, compatibility, ownership, or acceptance.

When compatibility/support depends on a change-prone external platform/library/provider fact, reference the current evidence basis and revalidate later when material work relies on it and staleness is plausible.

Local internal implementation details belong in source unless a durable architecture/interface contract is actually needed.

## Failure / Degradation / Recovery

Define required failure behavior only where correctness or user safety depends on it.

Do not add speculative fallback paths. A fallback must handle a named expected condition and must not hide an unknown root cause.

## Persistence / Storage

Use when material.

Define what must persist, what is temporary, and which owner controls stored state.

Do not invent persistence simply because many applications have it.

## Acceptance / Proof Requirements

Define what evidence can establish material product claims.

Examples:

```text
source/static contract → source/static proof
build behavior          → relevant build/test
runtime/device behavior → matching runtime/device proof
visual/audio/content    → matching inspection/human acceptance
external current fact   → current authoritative/primary evidence
```

Do not upgrade one evidence class into another.

## Blocking Decisions / High-impact Unknowns

List only unresolved choices/facts that must be decided or verified before affected behavior can be implemented responsibly.

If none remain, say so briefly or remove this section.

## Related Foundation Owners

Link only additional durable owners created by the Foundation Expansion Gate.

Do not list files that do not exist.
