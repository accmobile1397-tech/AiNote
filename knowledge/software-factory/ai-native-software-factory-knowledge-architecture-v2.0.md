# AI Native Software Factory Knowledge Architecture
## Version 2.0 — Project Memory + Specification + Agent-Agnostic Execution

**Status:** Canonical successor to v1.0

## 1. Purpose

Define how reusable knowledge becomes project knowledge, how project memory persists, how specifications are generated and validated, and how replaceable Agents execute software work.

## 2. Four-Layer Model

```text
General Knowledge Layer
        ↓
Project Bootstrap / Operating Contract
        ↓
Project Knowledge Layer
        ↓
Project Operating Memory + State
```

General Knowledge contains reusable protocols, preferences and patterns. Bootstrap contains execution contracts. Project Knowledge contains product-specific truth. POM/PSL contain current operational memory and state.

## 3. Factory Pipeline

```text
Idea
→ Discovery / Interview
→ Context Baseline
→ Foundation Documents
→ PO Approval
→ Autonomous Documentation
→ Documentation Validation
→ Developer Readiness
→ Feature Specification
→ Task Generation
→ Coding
→ Testing
→ Evidence
→ Review
→ PO Approval
→ Knowledge Evolution
```

## 4. Agent Independence

No phase may require a particular Agent. Agent identity, model, IDE and session are replaceable. Repository state and artifacts are the handoff mechanism.

## 5. Skills

Skills are versioned execution protocols. Typical project skills:
- Documentation Engineer
- Documentation Validator
- Coding Developer
- QA / Verification
- DevOps
- Security
- SEO

Skills must read project state and write back execution state.

## 6. Documentation Factory

Documentation is produced as a dependency-aware system rather than a pile of Markdown files. Each artifact declares purpose, lifecycle position, inputs, outputs, dependencies, owner, approval state and references.

## 7. Specification Graph

```text
Product Intent
→ Requirement
→ Domain
→ Architecture
→ Contract / Specification
→ Feature
→ Task
→ Code
→ Test
→ Evidence
→ Review
```

The graph is used for impact analysis and developer readiness.

## 8. Documentation Validator

The validator is an independent gate. It must detect missing documents, contradictions, unresolved ambiguities, broken dependencies, untestable acceptance criteria, missing task inputs and weak traceability.

## 9. Developer Readiness

A project becomes Developer-Ready only when a developer can implement the next Feature without guessing product intent, architecture, business rules, contracts or acceptance criteria.

## 10. Developer Factory

Coding Developer consumes approved specifications and produces code plus tests and evidence. It must not silently invent requirements.

## 11. PO-Controlled Execution

Two modes are supported:
- Gated task execution
- Autonomous task queue execution

The mode can change during runtime.

## 12. UI Engineering Capability

The factory treats UI/UX as a first-class engineering output. Project UI contracts may define layout, components, forms, cards, dashboards, charts, tables, landing pages, states and responsive behavior. Coding Agents should be capable of implementing these using the project's Design System. Persian projects default to RTL, mobile-first, Jalali-aware and accessibility-conscious behavior.

## 13. Learning Loop

```text
Execution
→ Evidence
→ Review
→ Lesson
→ Pattern Candidate
→ Review
→ Reusable Knowledge
```

## 14. Factory Success Test

The factory is successful when a project can be started by one Agent, continued by another, documented by a third and coded by a fourth without loss of context or traceability.

> **The Factory does not manufacture code first. It manufactures reliable project understanding and specifications, then turns them into verified software.**

**End — Knowledge Architecture v2.0**
