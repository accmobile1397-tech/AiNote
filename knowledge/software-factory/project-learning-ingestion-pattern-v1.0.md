# Project Learning Ingestion Pattern
## Version 1.0

**Status:** Canonical

## Purpose

Define how reusable knowledge discovered during project execution is returned to AiNote without contaminating the global knowledge base with project-specific assumptions.

## Lifecycle

```text
Project Execution
→ Observation / Lesson
→ Candidate Learning
→ AiNote
→ Generalization
→ Review
→ Canonical Knowledge
→ Bootstrap Candidate
```

## Capture Categories

Capture reusable lessons such as:
- SDLC process improvements
- documentation patterns
- architecture patterns
- agent collaboration patterns
- validation rules
- UI/UX patterns
- coding patterns
- testing patterns
- DevOps/security/SEO patterns
- failure modes and mitigations

## Do Not Promote Automatically

Do not promote:
- project-specific business rules
- accidental implementation details
- one-off workarounds
- vendor-specific choices without general value
- domain-specific assumptions

## Promotion Test

Ask:
1. Would this help another project?
2. What is the generalized principle?
3. Under what conditions is it valid?
4. What evidence supports it?
5. Does it conflict with existing knowledge?
6. Should it change Bootstrap?

## Post-Project Review

Every completed project should perform a knowledge extraction pass and place candidate reusable learning into AiNote. This review is part of project completion, not an optional afterthought.

## Governing Rule

> **Projects contribute learning to AiNote; only reviewed and generalized knowledge may influence the Bootstrap.**

**End — Project Learning Ingestion Pattern v1.0**
