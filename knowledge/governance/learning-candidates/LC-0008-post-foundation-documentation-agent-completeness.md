# LC-0008 — Post-Foundation Documentation Agent Completeness

## Source

EntityLens project execution.

## Status

candidate — pending review/generalization

## Problem

After a project's Foundation Document is explicitly approved, the project owner expects any authorized Documentation Agent — including a different AI provider/model — to be able to enter the repository and continue the **complete documentation process required by the SDLC protocol** from the Foundation, without relying on the original Chat session or the original agent.

The previous project flow incorrectly treated the next step as a specific architecture task selected by the previous agent. This creates unnecessary agent coupling and can cause an agent to skip or invent SDLC stages.

## General Rule Candidate

Bootstrap MUST define a post-Foundation documentation handoff contract.

Once Foundation is approved:

1. Foundation becomes the authoritative baseline.
2. Any authorized Documentation Agent MUST be able to continue from the repository alone.
3. The agent MUST follow the project's defined SDLC documentation sequence.
4. The agent MUST determine the next required documentation artifact from the SDLC state and existing approved documents, not from prior Chat memory.
5. The agent MUST produce the complete documentation set required by the SDLC before coding is considered.
6. The agent MUST preserve traceability and human approval gates.
7. The workflow MUST be vendor/model independent.
8. A project MUST NOT require the original agent to continue documentation.

## Important Distinction

Foundation approval authorizes the Documentation phase; it does NOT mean the next document is always a particular architecture document. The next artifact must be determined by the project's SDLC protocol and current repository state.

## Required Project Contract

A Bootstrap project should expose enough repository-level information for a new Documentation Agent to determine:

- approved Foundation;
- current SDLC phase;
- current documentation state;
- required reading order;
- documentation sequence;
- approval gates;
- coding authorization status;
- Source of Truth;
- traceability requirements.

## Generalization

Reusable principle:

> After Foundation approval, documentation must become agent-portable: any authorized Documentation Agent can reconstruct the SDLC documentation state from the repository and continue through the complete documentation lifecycle without prior Chat context.

## Bootstrap Implication

Review this candidate for inclusion in the next Bootstrap version. The goal is to prevent agent-specific handoffs and premature selection of individual downstream architecture steps.
