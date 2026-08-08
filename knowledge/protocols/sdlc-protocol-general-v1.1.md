# SDLC Protocol General

## Master Principles & Governance Rules

## Version 1.1

---

# 1. Purpose & Definition

SDLC Protocol General is the central methodology and governance framework for AI-native software development.

It defines:

- Software development principles
- SDLC lifecycle governance
- Documentation standards
- Specification standards
- AI-assisted development workflows
- Agent collaboration rules
- Knowledge management principles
- Architecture decision processes
- Quality validation rules

SDLC Protocol General is a methodology and protocol, not a product, website, SaaS platform, or commercial service.

---

# 2. Core Scope

The scope of SDLC Protocol General is defining standards and processes for building software systems.

It applies to:

- Product development
- AI-assisted software engineering
- Human-AI collaboration workflows
- Documentation-driven development
- Agent-based development processes

It does not define:

- Specific products
- Business models
- Customer platforms
- Commercial services

Each product must maintain its own project-specific knowledge and decisions.

---

# 3. Software Development Philosophy

## Documentation First

No implementation starts before sufficient documentation exists.

Required flow:

```text
Vision
  ↓
Requirements
  ↓
Architecture
  ↓
Specification
  ↓
Task Definition
  ↓
Implementation
  ↓
Review
```

---

## Specification First

Every feature must be clearly specified before implementation.

Each feature specification should define:

- Purpose
- User Value
- Scope
- Requirements
- Constraints
- Acceptance Criteria

---

## Architecture First

Architecture decisions must be defined before implementation.

Important decisions require:

- Documentation
- Evaluation
- Trade-off analysis
- Decision record

---

## Single Source of Truth

Approved documentation is the source of truth.

Implementation must follow approved documents.

If implementation conflicts with approved architecture or specification:

The approved documentation has priority until formally changed.

---

## MVP First

Build the smallest valuable version first.

Avoid:

- Over-engineering
- Premature optimization
- Unnecessary complexity

Future expansion should be enabled by architecture but not implemented prematurely.

---

# 4. SDLC Lifecycle Definition

Standard lifecycle:

```text
Vision
  ↓
Product Definition
  ↓
PRD
  ↓
SRS
  ↓
Architecture Design
  ↓
Database Design
  ↓
API Design
  ↓
UX/UI Design
  ↓
Knowledge Base Setup
  ↓
Feature Specification
  ↓
Task Definition
  ↓
Implementation
  ↓
Testing
  ↓
Deployment
  ↓
Monitoring
  ↓
Knowledge Evolution
```

---

# 5. AI Agent Collaboration Principle

AI Agents are assistants and engineering partners, not independent decision makers.

AI should:

- Analyze
- Suggest
- Compare options
- Generate documentation
- Generate implementation
- Execute approved tasks

AI should not:

- Change architecture silently
- Expand scope without approval
- Introduce undocumented decisions
- Ignore project standards

---

# 6. Documentation Governance

Every document must have:

- Clear purpose
- Defined owner
- Correct lifecycle position
- Required structure
- Version control

Rules:

- Avoid incomplete document accumulation
- Complete → Review → Approve → Continue
- Quality is more important than document quantity

---

# 7. SDLC Compliance Validation

All AI-generated documents must pass SDLC validation.

Validation includes:

## Structure Validation

Check:

- Correct document type
- Required sections exist
- Standard format followed

## Content Validation

Check:

- Requirements completeness
- Decision clarity
- Constraints
- Acceptance criteria

## Process Validation

Check:

- Correct SDLC stage
- Required dependencies exist
- Previous documents are available

## Quality Validation

Check:

- Product alignment
- Architecture consistency
- UX consistency
- Business alignment

---

# 8. Human Approval Model

(نسخه کامل بخش Human Approval که تایید کردیم در این قسمت قرار می‌گیرد)

---

# 9. Knowledge Management Principle

Project knowledge is a long-term product asset.

Knowledge includes:

- Product decisions
- Architecture decisions
- Business rules
- Design patterns
- Technical evaluations
- Lessons learned

Knowledge lifecycle:

```text
Experience
  ↓
Documentation
  ↓
Review
  ↓
Approved Knowledge
  ↓
Reuse
```

---

# 10. AI-Native Development Principle

Software should be designed from the beginning for:

- AI Assistants
- AI Agents
- Local LLMs
- RAG Systems
- Intelligent automation

AI capability should not be added as an afterthought.

---

# 11. Event-Driven Ready Principle

Projects should identify important business events.

Examples:

- UserRegistered
- ProfileCompleted
- PaymentCompleted
- SubscriptionActivated
- NotificationRequested
- DataUpdated

Benefits:

- Loose coupling
- Automation
- Background processing
- Integration readiness
- Auditability

---

# 12. Architecture Decision Governance

Technology and architecture choices should follow:

```text
Analyze
  ↓
Compare
  ↓
Document
  ↓
Review
  ↓
Decide
  ↓
Adopt / Adapt / Reject
```

---

# 13. Reusable Knowledge & Pattern Evolution

Repeated solutions should become reusable patterns.

Process:

```text
Project Experience
  ↓
Pattern Candidate
  ↓
Review
  ↓
Approved Pattern
  ↓
Reuse
```

---

# 14. Workspace Principle

Each project workspace should contain:

- Documentation
- Architecture
- Tasks
- Standards
- Code
- Knowledge

AI tools should use the project workspace as the primary context.

---

# 15. Final Goal

Build software that is:

- AI Native
- Spec Driven
- Knowledge Centered
- Secure
- Scalable
- Maintainable
- Observable
- Self Hostable
- Future Proof

Designed for:

- Human users
- Developers
- AI Agents
- Local LLMs
- Future intelligent systems

---

**End of Document — Version 1.1**
