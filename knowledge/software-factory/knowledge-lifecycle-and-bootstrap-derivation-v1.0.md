# Knowledge Lifecycle & Bootstrap Derivation
## Version 1.0

**Status:** Canonical

## 1. Purpose

Define the governed relationship between AiNote, the Agentic-SDLC-Project-Bootstrap, and individual projects.

## 2. Core Model

```text
AiNote
Knowledge Laboratory
      ↓ review / generalize / approve
Agentic-SDLC-Project-Bootstrap
Executable Knowledge Baseline
      ↓ instantiate
Project
      ↓ learn / discover
AiNote
```

AiNote is upstream knowledge. Bootstrap is its curated executable interpretation. Projects are execution instances that generate new learning.

## 3. AiNote

AiNote may contain exploratory notes, discoveries, preferences, candidate patterns, experiments, lessons, canonical knowledge and historical versions. Not every item is a Bootstrap rule.

## 4. Bootstrap

Bootstrap contains only approved, generalized, reusable knowledge required to initialize and operate new projects, including protocols, skills, schemas, templates, validation rules, workflow rules and reusable patterns.

## 5. Project Learning

During and after a project, reusable lessons should be extracted into AiNote. The project itself remains the source of project-specific truth.

## 6. Promotion Pipeline

```text
Project Learning
→ AiNote
→ Generalize
→ Review
→ Canonical Knowledge
→ Bootstrap Proposal
→ Impact / Conflict Analysis
→ Approval
→ New Bootstrap Version
```

Direct Project → Bootstrap mutation is prohibited.

## 7. Knowledge States

```text
observed
→ candidate
→ reviewed
→ canonical
→ bootstrap-proposed
→ bootstrap-approved
```

Items may also remain `project-local` or become `deprecated`.

## 8. Generalization Gate

Before promoting knowledge to Bootstrap, verify:
- reusable across projects
- principle is understood
- not dependent on accidental project constraints
- improves quality, reliability, productivity or governance
- does not conflict with existing canonical knowledge
- can be expressed as a protocol, pattern, skill, template or validation rule

## 9. Versioning

Bootstrap is versioned. A project is associated with the Bootstrap version used to initialize it. New Bootstrap versions do not silently mutate existing projects.

## 10. Traceability

Significant Bootstrap rules should identify their AiNote source or an explicit architectural decision. Promotion should record reason, impact and approval.

## 11. Factory Learning Loop

```text
Knowledge
→ Bootstrap
→ Project
→ Software
→ Evidence
→ Learning
→ AiNote
→ Canonical Knowledge
→ Bootstrap
→ Next Project
```

## 12. Governing Principle

> **AiNote explores and accumulates. Bootstrap operationalizes. Projects execute and learn. AiNote receives the learning, and reviewed knowledge improves the next Bootstrap.**

**End — Knowledge Lifecycle & Bootstrap Derivation v1.0**
