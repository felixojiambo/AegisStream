# ADR 0001: Trunk-Based Development

## Status
Accepted

## Context
AegisStream is a multi-service monorepo (core-service, web, infra, docs).
We need a workflow that:
- keeps `main` always releasable,
- avoids long-running branches,
- reduces merge conflicts,
- enforces quality gates via CI,
- supports fast iteration and frequent integration.

## Decision
We will use **trunk-based development**:
- `main` is the single integration branch.
- All work is done in **short-lived branches**.
- Changes are merged through **Pull Requests** only.
- We use **Squash Merge** to keep a clean, linear history.

## Consequences
### Positive
- Frequent integration reduces drift and merge conflicts.
- `main` stays stable and deployable.
- Clear audit trail: each PR becomes one commit on `main`.
- CI gates enforce quality consistently.

### Trade-offs
- Requires discipline to keep branches short-lived.
- Larger features must be split into incremental PRs.
- CI reliability is critical (failing CI blocks merges).

### Operational Rules
- No direct pushes to `main`.
- At least 1 reviewer approval is required (more for sensitive areas later).
- CI must pass before merging.
