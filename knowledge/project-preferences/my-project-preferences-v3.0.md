# My Project Preferences
## Version 3.0 — Specification-Driven AI-Native Project Standard

**Status:** Canonical successor to v2.1

## 1. Product Owner Working Style

Preferred approach:
- Guided intelligence during discovery and major decisions
- Step-by-step explanation when learning is useful
- Autonomous execution after explicit approval gates
- Clear options, trade-offs and recommendations
- Human remains Product Owner and decision authority

## 2. Core Product Principles

- Vision First
- Business Model First
- User Value First
- User-Centric First
- Scalability-aware
- AI First / AI Native
- Knowledge Base First
- Specification First

## 3. Core Development Principles

- Documentation First
- Specification First
- Architecture First
- SDLC First
- Source of Truth First
- Traceability First
- Agent-Agnostic Execution
- Modular Architecture First
- API First
- Domain-oriented design
- Event-driven ready
- Open standards
- Avoid unnecessary vendor lock-in
- MVP First

## 4. Project Memory Principle

Project Repository is the durable memory. POM and Project State Layer must exist from the beginning. No critical context may live only in ChatGPT, Claude, Cursor or another Agent.

## 5. Standard Project Bootstrap

After Discovery/Q&A, the initial Human approval package is:
1. PROJECT_CONTEXT
2. VISION
3. PRODUCT_DEFINITION
4. DOMAIN_MODEL
5. REQUIREMENTS_BASELINE
6. ARCHITECTURE_BASELINE

After approval, documentation may continue automatically according to the Documentation Skill.

## 6. Documentation Principle

The project is not expected to contain a fixed number of documents. The Documentation System creates the documents required by project complexity, dependencies and traceability.

Every important document has purpose, lifecycle position, dependencies, owner, status, version and references.

## 7. Specification Standard

Feature specifications should define as applicable:
- Purpose
- Actors
- User value
- Scope / out of scope
- Functional requirements
- Business rules
- Inputs / outputs
- States
- Errors
- Permissions
- Dependencies
- API contracts
- Data contracts
- UI/UX contracts
- AI behavior
- Non-functional requirements
- Acceptance criteria
- Test expectations

Coding must not start when material ambiguity remains.

## 8. Architecture Preferences

Default:
- Modular monolith first
- Clear module boundaries
- API-first
- Domain-oriented organization
- Infrastructure abstraction
- External-service abstraction

Microservices are an evolution option, not the default.

## 9. Web Technology Defaults

For applicable new web applications:
- Next.js
- React
- TypeScript
- Tailwind CSS
- shadcn/ui
- Node.js / TypeScript backend
- Prisma where ORM is appropriate
- Relational database by default
- Docker / container deployment
- Linux / VPS or Cloud
- GitHub / Git / CI/CD

Technology remains a project decision; defaults do not override requirements.

## 10. AI Architecture

Prefer:
```text
Application
→ AI Capability
→ AI Gateway / Provider Abstraction
→ Model Provider
```

Support where relevant:
- Provider abstraction
- Model abstraction
- Fallback
- Retry / timeout
- Usage tracking
- Cost tracking
- Observability
- Local LLM readiness

LLM and Embedding are separate capabilities.

## 11. RAG / Knowledge

RAG is introduced only when required by product needs. Embedding lifecycle, versioning and re-indexing must be explicitly managed when RAG exists.

## 12. Frontend / UI Preferences

UI is a first-class engineering output.

Default web UX preferences:
- Mobile-first
- Responsive mobile/tablet/desktop
- RTL for Persian projects
- Persian-first where applicable
- Jalali calendar where applicable
- Vazirmatn preferred for Persian projects
- Accessibility
- Performance
- SEO
- Design System
- Reusable components
- Consistent interaction patterns

Coding Developer should be capable of producing polished forms, cards, dashboards, charts, tables, filters, navigation, landing pages, settings, wizards and all common application UI patterns from specification.

Every meaningful screen should account for loading, empty, error, success and permission states where applicable.

## 13. API / Data

Contracts must be explicit and documented. Include request, response, validation, authentication, authorization, errors and rate limits where relevant.

## 14. Agent Collaboration

Any Agent must:
- Read the project entrypoint
- Read current state
- Identify authoritative sources
- Stay within task scope
- Never silently invent missing requirements
- Record meaningful decisions
- Validate its work
- Update state and traceability

## 15. Developer Workflow

```text
Feature
→ Specification
→ Task Breakdown
→ Implementation
→ Test
→ Evidence
→ Review
→ PO Approval
```

At the start of feature execution, Coding Developer asks PO whether task execution is Gated or Autonomous. PO may switch mode during execution.

## 16. Human Approval

Human approval is required for foundation baseline and other project-defined strategic/product/architecture gates. Approval is persisted in Repository state.

## 17. Quality

Validation must cover documentation completeness, consistency, traceability, testability, security, UX/UI quality and implementation evidence.

## 18. Final Principle

> **Build project understanding first, persist it in the project, validate its specifications, and let replaceable Agents execute against that durable source of truth.**

**End — My Project Preferences v3.0**
