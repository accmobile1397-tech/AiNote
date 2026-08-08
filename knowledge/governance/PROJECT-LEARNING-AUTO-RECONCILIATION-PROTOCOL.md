# Project Learning → AiNote → Bootstrap Auto-Reconciliation Protocol
## Version 1.0

## Purpose

Create a standing workflow so project discoveries do not require the PO to repeatedly ask an Agent to review AiNote, update context, or reconcile Bootstrap.

## Default Behavior

During project execution, whenever the PO provides a new observation, preference, pattern, correction, architectural insight, workflow improvement, failure lesson, or reusable rule, the active Agent must automatically evaluate whether it has knowledge value.

The PO does not need to say: "check AiNote".

## Evaluation

For each meaningful new input, the Agent evaluates:

1. Is this project-specific only?
2. Is it a reusable engineering/product/AI/SDLC pattern?
3. Does it refine, contradict, extend, or duplicate existing AiNote knowledge?
4. Is there evidence from the current project?
5. Should it become an AiNote candidate?
6. Could it affect Agentic-SDLC-Project-Bootstrap?

## Outcomes

### No Knowledge Candidate
If the information is only transient/project-specific, keep it in project memory and do not pollute AiNote.

### Candidate
Create/update an AiNote Learning Candidate with source, context, evidence, proposed generalization, limitations, and affected knowledge areas.

### Canonical Update Candidate
If the discovery is a strong reusable pattern, route it through AiNote review/generalization before treating it as canonical.

## Automatic Reconciliation

When a candidate is accepted or materially changes canonical knowledge:

```text
Project Observation
→ Knowledge Evaluation
→ AiNote Candidate
→ AiNote Review / Generalization
→ Canonical Knowledge Update
→ Bootstrap Reconciliation
→ Bootstrap Update Proposal
→ Bootstrap Validation
→ Bootstrap Update (when required)
```

## Bootstrap Update Rule

The Agent must automatically determine whether the new AiNote knowledge affects Bootstrap. It must not directly change Bootstrap merely because a project observation exists.

A Bootstrap update is required when the new canonical knowledge changes a reusable protocol, pattern, skill contract, validation rule, artifact model, gate, or project bootstrap behavior.

## Reporting

When the PO gives a potentially reusable insight, the Agent should briefly report:

- Knowledge candidate: Yes / No
- Reason
- AiNote action: None / Candidate / Updated
- Bootstrap impact: None / Review / Update required
- Evidence/reference

The PO should not have to initiate these checks manually.

## Context Refresh

After an approved canonical knowledge change, the Agent should refresh its working context from the updated AiNote/Bootstrap artifacts before continuing work. Chat memory is not the authoritative mechanism.

## Agent-Agnostic Rule

This protocol applies regardless of whether the active participant is ChatGPT, Claude, Cursor, another AI Agent, or a human-assisted workflow. The repository knowledge and persisted records are authoritative.

## Safety Rule

Automatic does not mean silent. Material knowledge changes and Bootstrap updates must leave durable records and pass the applicable review/approval gates.

**Status:** Canonical governance protocol
