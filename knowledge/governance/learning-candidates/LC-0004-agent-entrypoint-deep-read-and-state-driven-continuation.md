# LC-0004 — Agent Entrypoint and State-Driven Continuation

## Source

Project learning candidate from `accmobile1397-tech/Agentic-SDLC-Project-Bootstrap`.

## Status

candidate — pending review/generalization

## Observation

During M9 Bootstrap Validation entry inspection, an agent initially stopped after failing to find a dedicated M9 execution artifact. Deeper inspection showed that this conclusion was incorrect: the canonical agent entrypoint, machine-readable project state, roadmap, approvals, active protocols/skills, and milestone artifacts together define the continuation point even when a milestone has no dedicated implementation artifact yet.

Bootstrap state explicitly identifies M9 as active, the validation gate, and the next action:

`inspect-m9-entrypoint-and-define-representative-bootstrap-validation-scope`

`AGENT_ENTRYPOINT.md` requires a new agent to read state, workflow, approvals, roadmap, active SDLC/skill documents, determine current phase/gate/pending work/next action, and continue from durable repository state rather than assumptions or chat history.

## Candidate Generalization

> Absence of a dedicated artifact for the current milestone is not evidence that the milestone lacks an executable next step. Before declaring work undefined or blocked, an agent must reconcile the canonical entrypoint, machine-readable state, roadmap, approvals, active protocols/skills, and milestone artifacts.

## Evidence

- Bootstrap `AGENT_ENTRYPOINT.md`
- Bootstrap `KNOWLEDGE-LOOP-ENTRYPOINT.md`
- Bootstrap `.project/state.yaml`
- Bootstrap `ROADMAP.md`
- Bootstrap `docs/00-foundation/BOOTSTRAP-ARCHITECTURE.md`
- Bootstrap state at M9 records `current_gate: validation`, `current_task: M9-ENTRY`, and the explicit next action `inspect-m9-entrypoint-and-define-representative-bootstrap-validation-scope`.

## Reusability Assessment

- Reusable beyond the source project: yes
- Process/agent-execution improvement: yes
- Project-specific business rule: no
- Vendor-specific: no
- Bootstrap impact: review required; no direct promotion

## Governance

This is an intake candidate, not canonical knowledge. It must be reviewed and generalized before becoming canonical knowledge or influencing Bootstrap.
