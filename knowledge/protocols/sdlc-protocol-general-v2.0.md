# SDLC Protocol General
## Version 2.0 — Specification-Driven, Knowledge-Centered, Traceable, Agent-Agnostic

**Status:** Canonical successor to v1.1

## 1. Purpose

This protocol governs AI-native software development independent of any specific Agent, model, IDE, vendor, or conversation.

## 2. Core Principles

- Vision First
- Product / Business / User Value First
- Knowledge Before Execution
- Specification Before Implementation
- Architecture Before Coding
- Project Repository as durable Source of Truth
- Agent-Agnostic execution
- Human governance at explicit gates
- Traceability from intent to evidence
- MVP first without sacrificing sound foundations
- UI/UX as an engineering concern, not an afterthought

## 3. Durable Project Memory

Every project must initialize Project Operating Memory (POM) and Project State Layer (PSL) before substantive work. Critical context must be persisted in the Repository.

## 4. Discovery Before Documentation

Start with Human/PO discovery and structured Q&A. The Documentation Agent must establish:
- Project context
- Goals and constraints
- Users and actors
- Product intent
- Business model
- Domain understanding
- Major risks and assumptions

No autonomous documentation generation starts until the Human approves the understanding baseline.

## 5. Foundation Approval Gate

The default initial approval package is:
1. PROJECT_CONTEXT
2. VISION
3. PRODUCT_DEFINITION
4. DOMAIN_MODEL
5. REQUIREMENTS_BASELINE
6. ARCHITECTURE_BASELINE

After PO approval, documentation may proceed autonomously under the active Documentation Skill.

## 6. Documentation Lifecycle

```text
Discovery
→ Foundation Documents
→ PO Approval Gate
→ Autonomous Specification Development
→ Cross-Document Consistency Checks
→ Documentation Validation
→ Developer Readiness Gate
```

The number of documents is not fixed. Documents are produced when required by project complexity and traceability.

## 7. Documentation Skill

Every project must contain or reference a versioned Documentation Skill defining:
- Entry conditions
- Required inputs
- Document sequence
- Dependencies
- Validation rules
- State updates
- Handoff rules
- Resume behavior
- Stop conditions

The Skill is an execution protocol, not project memory.

## 8. Documentation Validator Gate

Before coding, an independent validator must verify:
- Required documents exist
- No critical ambiguity remains
- Requirements are complete enough to implement
- Architecture is consistent with requirements
- UI/UX contracts are sufficient
- API/Data/Security contracts exist where needed
- Tasks can be generated from specifications
- Task acceptance criteria are testable
- Traceability is complete
- Project is genuinely SDLC-driven
- Developer can execute without guessing

If validation fails, return to documentation rather than starting coding.

## 9. Specification Graph

The project must maintain traceability:
```text
Vision
→ Product Requirement
→ Domain / Architecture
→ Feature Specification
→ Task
→ Code
→ Test
→ Evidence
→ Review
→ PO Approval
```

## 10. Coding Developer Gate

Coding Developer may start only when Developer Readiness is PASS.

Coding Developer must:
- Read project entrypoint and state
- Read relevant specification and contracts
- Reuse existing UI/design components
- Never invent missing requirements silently
- Record deviations and decisions
- Produce tests and evidence
- Update project state and traceability

## 11. Feature Lifecycle

```text
Feature Request
→ Feature Specification
→ Task Breakdown
→ Task Execution
→ Validation
→ Evidence
→ Review
→ PO Approval
→ Next Task / Queue Continuation
```

## 12. Task Execution Modes

At the beginning of a feature, Coding Developer asks the PO whether execution should be:

**Gated:** each approved task unlocks the next task.

**Autonomous:** the approved task queue may continue automatically while respecting all safety, validation, and approval gates.

This mode is runtime-configurable. PO may switch between modes during execution.

## 13. Human Approval

Human/PO remains the authority for:
- Product intent
- Major scope changes
- Strategic decisions
- Foundation approval
- Major architecture changes
- Feature acceptance where required
- Workflow mode changes

Human approval must be persisted in project state.

## 14. Agent Handover

Any Agent may be replaced at any point. Handover occurs through:
- POM
- PSL
- Knowledge Map
- Current Task
- Specifications
- Decision Records
- Execution Reports
- Evidence

## 15. UI/UX Engineering Baseline

For applicable web projects:
- Mobile-first
- Responsive mobile/tablet/desktop
- RTL when required
- Persian-first when applicable
- Jalali calendar where applicable
- Accessible
- Performance-aware
- SEO-aware
- Design-system based
- Reusable components
- Loading, empty, error and success states

Coding Developer should be capable of implementing forms, cards, dashboards, charts, tables, navigation, landing pages, settings, wizards and other common UI patterns from specification and design-system rules.

## 16. Change Governance

If implementation reveals an incomplete or incorrect specification:
```text
Stop / Contain
→ Record Gap
→ Update Specification
→ Revalidate
→ Resume
```

Do not silently diverge from approved intent.

## 17. Final Goal

The protocol must allow:
- ChatGPT to start and continue work
- Claude/Cloud to resume it
- Cursor or another Coding Agent to implement it
- Human developers to take over
- Future Agents to continue

without losing project context or SDLC traceability.

> **Skills execute the protocol. The Project Repository remembers the project.**

**End — SDLC Protocol General v2.0**
