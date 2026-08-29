# LC-0007 — Repository Agent Onboarding & Source-of-Truth Integrity

## Source

EntityLens Foundation workflow and external-agent onboarding issue observed during project execution.

## Status

candidate — pending review/generalization

## Observation

An external AI agent may incorrectly conclude that a project repository is empty or lacks documentation even when authoritative files exist on the repository's main branch. This can happen because of repository metadata/index lag, incomplete discovery, missing README/navigation, insufficient onboarding instructions, or use of a limited GitHub access path.

## Proposed General Rule

A project following Bootstrap MUST provide an explicit Agent Onboarding / Repository Integrity layer that lets any authorized agent determine:

1. repository identity;
2. current branch / canonical branch;
3. project status and SDLC stage;
4. Source of Truth locations;
5. Foundation status;
6. required reading order;
7. project governance rules;
8. current next-step / gate;
9. whether coding is authorized.

Agents MUST verify authoritative repository contents before concluding that a project is empty or that required knowledge does not exist.

## Minimum Onboarding Artifacts

A Bootstrap-based project should have, as applicable:

- README.md — repository-level orientation;
- AGENT-ONBOARDING.md — explicit agent entry point;
- project state / status file;
- Foundation document after Foundation Gate;
- clear documentation hierarchy;
- Source-of-Truth declaration;
- SDLC gate/status declaration.

## Verification Principle

Repository metadata such as reported size, search index state, or README discoverability MUST NOT by itself be treated as proof that the repository contains no authoritative content.

Agents should verify through direct repository contents access when possible and should distinguish:

- repository metadata;
- repository index/search visibility;
- actual repository contents.

## Bootstrap Implication

This pattern should become a Bootstrap requirement in the next appropriate version so that projects are agent-readable and resilient to differences between AI tools, GitHub indexes, repository metadata, and connector capabilities.

## Generalization

The reusable principle is broader than EntityLens:

> Every Bootstrap project MUST be self-describing enough for an authorized external agent to reconstruct the project's current SDLC context from repository contents without relying on prior Chat history.

## Governance

This is a learning candidate, not canonical Bootstrap policy. Promote only after review and generalization.
