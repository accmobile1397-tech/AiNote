# AI Native Project Operating Memory (POM)
## Version 2.0 — Agent-Agnostic Project Memory

**Status:** Canonical successor to POM v1.1

## 1. Purpose

POM is the durable operating-memory architecture of an AI-native project. It allows any Human, ChatGPT, Claude/Cloud, Cursor, Coding Agent, Documentation Agent, QA Agent, or future tool to resume work from the Repository without relying on prior conversation history.

> **Project Memory must outlive every Agent, Model, Tool, IDE, and Conversation.**

## 2. Core Principle

**Project Should Remember — Agents Should Execute.**

Agent-owned memory is temporary. Project-owned memory is authoritative and persistent.

## 3. POM Is Not Documentation

POM governs knowledge, state, decisions, execution, learning, approvals, and continuity. Documentation expresses the project's product and engineering knowledge. They are complementary.

## 4. Architecture

```text
Project Operating Memory
├── Knowledge Layer
├── Project State Layer (PSL)
├── Decision Layer
├── Execution Layer
├── Approval Layer
├── Traceability Layer
└── Learning Layer
```

## 5. Knowledge Layer

Contains or indexes authoritative project knowledge:
- Foundation / Anchor Documents
- Product Definition
- Domain Knowledge
- Requirements
- Architecture
- UX/UI System
- API and Data Contracts
- Security / SEO / Operations knowledge
- Feature Specifications

## 6. Project State Layer

Machine-readable state must exist from day one.

Minimum state:
```yaml
project_phase:
project_milestone:
current_task:
current_objective:
documentation_state:
developer_readiness:
workflow_mode: gated | autonomous
completed_work: []
current_work: []
pending_work: []
blockers: []
next_actions: []
```

State must be updated after every meaningful execution boundary.

## 7. Decision Layer

Persist Product, Architecture, Technology, UX, Security, Business, and Workflow decisions. Every important decision records context, options, evaluation, decision, consequences, owner, date, and status.

## 8. Execution Layer

Persist Tasks, Task Specifications, Execution Reports, Reviews, Test Results, Evidence, Releases, and Deployment records.

## 9. Approval Layer

Persist PO/Human approvals as project state, not chat-only events.

Approval must identify:
- What was approved
- Version/commit or artifact reference
- Approver
- Date
- Scope of approval
- Conditions, if any

## 10. Traceability Layer

Maintain links across:
```text
Vision
→ Requirement
→ Domain/Architecture Decision
→ Specification
→ Feature
→ Task
→ Code
→ Test
→ Evidence
→ Review
→ Approval
```

## 11. Agent Entry / Recovery

A new Agent must first read the project entrypoint, state, workflow, knowledge map, current task, relevant decisions, and relevant authoritative documents.

It must be able to answer from the Repository:
- What is this project?
- Where are we?
- What is approved?
- What is incomplete?
- What is the current task?
- What is the next action?
- Which documents are authoritative?
- What constraints apply?

## 12. Handoff Rule

Agent handoff occurs through Repository state and artifacts. Chat history is optional context, never the required context.

## 13. Task Lifecycle

```text
READ
→ UNDERSTAND
→ CHECK SPECIFICATION
→ EXECUTE
→ VALIDATE
→ REPORT
→ UPDATE STATE
→ UPDATE KNOWLEDGE/TRACEABILITY
→ CONTINUE
```

## 14. Documentation Automation State

POM must distinguish at least:
- Discovery
- Foundation Gate
- Autonomous Documentation
- Documentation Validation
- Developer Ready
- Feature Development
- Project Complete

## 15. Developer Workflow State

The project stores the PO-selected execution mode:
- `gated`: next task starts after approval
- `autonomous`: approved task queue may continue automatically

The PO may switch modes during execution without losing state or traceability.

## 16. Agent Replacement Test

A POM implementation passes when a new Agent can continue the current work without asking the Human to reconstruct prior project history.

## 17. Final Rule

> **No critical context lives only in an Agent. If the project needs it to continue, persist it in the Project Repository.**

**End — POM v2.0**
