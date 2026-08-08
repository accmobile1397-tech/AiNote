# AI-Native Project Bootstrap & Agent-Independent Memory Pattern
## Version 2.0

**Status:** Canonical successor to v1.0

## Purpose

Define the reusable bootstrap pattern for starting projects whose documentation, state and execution can survive replacement of every Agent, model, IDE and conversation.

## Fundamental Model

```text
Bootstrap
→ Discovery
→ Foundation Gate
→ Autonomous Documentation
→ Documentation Validation
→ Developer Readiness
→ Feature Execution
→ Evidence / Review
→ Knowledge Evolution
```

## Core Rule

> **Project Repository / Knowledge Layer is durable memory. Skills are replaceable execution protocols. Agents are replaceable executors.**

## Bootstrap Requirements

Every new project receives:
- Agent entrypoint
- POM / Knowledge architecture
- Machine-readable project state
- Workflow configuration
- Master roadmap
- Decision record mechanism
- Documentation skill
- Documentation validator skill template
- Coding developer skill template
- Traceability rules

## Agent Entrypoint

Every Agent must begin by reading the project's entrypoint and then discovering current state, workflow, knowledge map, approvals, current task and relevant specifications.

## Initial Human Gate

After Discovery/Q&A, generate:
1. PROJECT_CONTEXT
2. VISION
3. PRODUCT_DEFINITION
4. DOMAIN_MODEL
5. REQUIREMENTS_BASELINE
6. ARCHITECTURE_BASELINE

Then obtain PO approval. After approval, the Documentation Skill may continue autonomously.

## Resume Rule

A new Agent must continue from Repository state, not reconstruct history from chat.

## Documentation Automation

The Documentation Skill must be able to:
- determine current documentation phase
- identify missing prerequisites
- generate the next required artifact
- validate consistency
- update state
- record decisions
- resume after interruption
- hand off to another Agent

## Documentation Validator

Must answer from the Repository:
- Is documentation complete enough for development?
- Are any required documents missing?
- Can features be decomposed into executable tasks?
- Can acceptance criteria be tested?
- Is the specification graph traceable?
- Is the process SDLC-compliant?
- Would a Coding Developer need to guess?

Only PASS creates Developer-Ready status.

## Coding Developer

Coding Developer must be Agent-Agnostic and consume project specifications rather than conversation context.

For every Feature:
```text
Read
→ Understand
→ Check Spec
→ Create/Review Tasks
→ Implement
→ Test
→ Evidence
→ Review
→ PO Approval
→ Continue
```

## Workflow Mode

At the first feature execution, ask PO:
- Gated: next task waits for approval
- Autonomous: approved queue continues automatically

PO may change mode at runtime. State and traceability must survive the switch.

## UI Capability

For web projects, Coding Developer is expected to implement high-quality UI from project specifications and design system, including forms, cards, dashboards, charts, tables, landing pages, navigation, settings, wizards and responsive states. Mobile-first, RTL/Persian, Jalali, accessibility and responsive behavior are project preferences where applicable.

## Continuity Test

The bootstrap passes only if a different Agent can enter the Repository and correctly identify:
- current phase
- current state
- approved knowledge
- active task
- missing work
- next action
- workflow mode
- relevant constraints

without prior chat.

**End — Pattern v2.0**
