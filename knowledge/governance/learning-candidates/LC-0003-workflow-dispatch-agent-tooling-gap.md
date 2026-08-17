# LC-0003 — Workflow Dispatch Agent Tooling Gap

## Source Project
Agentic-SDLC-Project-Bootstrap

## Source Candidate
`knowledge/learning-candidates/LC-0003-workflow-dispatch-agent-tooling-gap.md`

## Discovery
The Bootstrap can define and validate GitHub Actions workflows and inspect existing runs, but connected Agent tooling initially lacked a direct workflow-dispatch operation.

## Candidate Principle
Routine CI execution SHOULD be an Agent capability rather than a permanent manual PO action. The capability MUST remain Agent-agnostic, preserve explicit governance/approval gates, and produce durable evidence that survives Agent replacement.

## Status
`intake_complete — pending review/generalization`

## Governance
This is an intake candidate, not canonical knowledge. Review/generalization is required before any Bootstrap mutation.

## Traceability
Project → AiNote → Review/Generalize → Bootstrap
