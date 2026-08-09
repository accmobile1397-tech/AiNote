# LC-0002 — State/Roadmap Sync Enforcement Gap

## Source
Agent discovery during Agentic-SDLC-Project-Bootstrap M7 runtime workflow implementation and integrated review.

## Status
`candidate — pending review/generalization`

## Observation
State/Roadmap synchronization had been specified as a governance policy, but it was not initially enforced through a single transition mechanism. This allowed repository drift between canonical `.project/state.yaml` and `ROADMAP.md`.

## Evidence
- Project candidate: `knowledge/learning-candidates/LC-0002-state-roadmap-sync-enforcement-gap.md`
- Project artifact: `docs/07-runtime-workflow/M7-TRANSITION-ENGINE.md`
- Project validator: `tests/validators/m7-state-roadmap-consistency-validator.sh`
- Project CI: `.github/workflows/m7-runtime-workflow-validation.yml`
- CI Run: `31308615483` — successful
- Integrated review: `docs/07-runtime-workflow/M7-INTEGRATED-REVIEW.md`

## Proposed Generalization
State/Roadmap synchronization MUST be an enforced invariant of the transition mechanism, not a post-transition maintenance step. A transition MUST NOT be reported successful unless canonical State and Roadmap are mutually consistent and the consistency check passes.

## Reusable Value
A repository-state-driven Agentic SDLC requires deterministic fresh-agent resume, handoff, milestone detection, and autonomous execution safety. Drift between state and roadmap undermines those guarantees.

## Limitations
The exact synchronization implementation may vary by repository and roadmap representation. The invariant is the reusable knowledge; the concrete validator/implementation is project-specific.

## Potential Bootstrap Impact
Likely affects reusable transition rules, state/roadmap validation, runtime workflow contracts, and future bootstrap project behavior. Bootstrap mutation MUST wait for AiNote review/generalization and explicit governed approval.

## Review Questions
1. Does this generalize beyond the current project?
2. Is it already represented elsewhere in AiNote?
3. Should it be merged into an existing runtime/state/traceability pattern?
4. What Bootstrap contracts or validators should be updated if accepted?

## Traceability
Project → AiNote → Review/Generalize → Bootstrap
