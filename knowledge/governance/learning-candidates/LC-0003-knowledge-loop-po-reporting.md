# LC-0003 — Knowledge Loop PO Reporting Must Be Mode-Independent

## Source Project
Agentic-SDLC-Project-Bootstrap

## Discovery
Knowledge Loop execution was correctly treated as an automatic agent obligation, but the PO-facing completion report had not been explicitly required outside PO-Guided execution.

## Generalizable Principle
Knowledge Loop reporting is independent of execution-control mode. After Knowledge Loop processing completes, the agent must provide a concise report to the PO in both AUTONOMOUS and PO_GUIDED modes.

## Why It Matters
The PO needs visibility into discoveries, candidate capture, AiNote intake, review/generalization status, Bootstrap impact, and unresolved decisions even when the PO has delegated task execution to autonomous mode.

## Resolution in Source Project
Added `docs/07-runtime-workflow/KNOWLEDGE-LOOP-PO-REPORTING-CONTRACT.md` and strengthened `KNOWLEDGE-LOOP-ENTRYPOINT.md` so reporting is an explicit execution obligation.

## Reusable Knowledge Candidate
Knowledge Loop processing and PO reporting are separate concerns. Execution-control mode governs task approval/execution interaction; it MUST NOT suppress post-loop visibility to the PO.

## Proposed Generalization
Any Agentic SDLC runtime implementing a Project → AiNote → Review/Generalize → Bootstrap loop should emit a concise durable PO-facing Knowledge Loop Report after applicable loop processing, regardless of whether the surrounding task execution is autonomous or PO-guided.

## Review Status
`pending review/generalization`

## Traceability
- Source Project: Agentic-SDLC-Project-Bootstrap
- Source Candidate: `knowledge/learning-candidates/LC-0003-knowledge-loop-po-reporting.md`
- Source Contract: `docs/07-runtime-workflow/KNOWLEDGE-LOOP-PO-REPORTING-CONTRACT.md`
- Route: Project → AiNote → Review/Generalize → Bootstrap

## Bootstrap Impact
Do not update Bootstrap directly from this intake. Review/generalize first, then create a Bootstrap candidate if the principle is accepted as reusable.
