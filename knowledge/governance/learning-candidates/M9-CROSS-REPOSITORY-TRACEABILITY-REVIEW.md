# M9 Cross-Repository Learning Traceability Review

source_project: Agentic-SDLC-M9-Representative-Project
knowledge_repository: AiNote
status: reviewed

## Finding

Learning Candidate numeric identifiers are not globally unique across repositories. At least two AiNote records use `LC-0003` for distinct learning topics, while the M9 source project uses `LC-0005` for Workflow Dispatch.

## Decision

Candidate identity MUST be traced by a stable source-project-qualified identity, not by the numeric suffix alone. A practical identity is `(source_project, candidate_id)` plus the canonical candidate filename/path.

## Boundary

This review does not rename existing candidates or mutate Bootstrap. Existing records remain valid when their source project and canonical path are explicit.

## Recommendation

Future Learning Candidate records should carry stable source metadata and an explicit source path. Cross-repository links should reference the qualified source identity rather than relying on a bare numeric candidate ID.

## Traceability

M9 Learning Candidates → AiNote intake → Cross-repository identity review → No Bootstrap Change
