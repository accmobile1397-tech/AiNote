# AiNote Knowledge Organization

## Purpose

AiNote is a knowledge-capture repository for useful observations, patterns, and insights extracted from websites, products, projects, and research.

AiNote is **not** the source of truth for any individual product. It records what was learned; target projects decide what to build.

## Core Principle

> Capture broadly, classify explicitly, generalize carefully, and promote only after review.

A note may be generic, domain-specific, or product-specific. Specificity is part of the knowledge record, not a reason to exclude the note.

## Knowledge Scope

Every new knowledge item should identify its scope:

- `generic` — broadly reusable across products/domains.
- `domain` — reusable within a business or technical domain, such as employment, e-commerce, construction, or Computer Science.
- `product` — specific to one named product/project, such as ComputerJobs or AIMentor.
- `source-specific` — an observation that is useful as evidence but should not yet be generalized.

A source-specific observation may later become generic, domain, or product knowledge after comparison and review.

## Source and Target Separation

The repository should distinguish:

- **Source** — where the observation was learned (website, product, paper, project, etc.).
- **Scope** — how broadly the observation is believed to apply.
- **Domain** — the subject area, when applicable.
- **Potential targets** — projects that may benefit from the knowledge.
- **Status** — observation/candidate/reviewed/pattern/canonical, according to the repository governance model.

A potential target does **not** mean the target project has adopted the idea.

## Classification Rule for New Research

When a user asks to inspect a website/product and save useful findings to AiNote, the agent must:

1. Inspect the source and collect useful observations.
2. Separate facts/observations from interpretation and recommendations.
3. Identify the applicable scope for each finding.
4. Identify the domain when the finding is not generic.
5. Identify potential target projects only when justified by the finding.
6. Avoid forcing all findings into one category merely because they came from one source.
7. Store each finding in the appropriate knowledge area and/or learning-candidate area using the existing repository conventions.
8. Preserve source attribution so the finding can be rechecked.
9. Mark unvalidated generalizations as candidates rather than canonical knowledge.
10. Never silently turn a research finding into a project requirement or implementation decision.

## Example

A review of a job platform might produce:

| Finding | Scope | Domain | Potential target |
|---|---|---|---|
| Password reset UX pattern | generic | authentication | many projects |
| Structured job taxonomy | domain | employment / Computer Science | ComputerJobs |
| AI career-gap workflow | domain | career development | ComputerJobs, AIMentor |
| A specific ComputerJobs screen decision | product | ComputerJobs | ComputerJobs only |

The fact that all four came from the same website does not make them the same kind of knowledge.

## Placement Guidance

Use the existing repository taxonomy rather than creating a new top-level folder for every source website.

- General reusable observations/patterns belong in the appropriate general knowledge area when sufficiently reviewed.
- Unreviewed reusable insights belong under `knowledge/governance/learning-candidates/`.
- Domain knowledge should be grouped by domain rather than by source website.
- Product-specific knowledge should be grouped by the relevant product/project.
- Source/research evidence should retain its origin and links where appropriate.

The exact directory for a new item must be selected by inspecting the current AiNote tree and existing conventions before writing.

## Preservation / Migration Rule

When this organization model is introduced, existing knowledge must be preserved. Do not delete or rewrite historical notes merely to make the tree look cleaner.

Where an old item clearly belongs in a new category, prefer a minimal metadata/classification update or an additive index/reference. Preserve the original content and provenance.

## Governance

AiNote follows a promotion pipeline:

```text
External Source
    ↓
Observation / Note
    ↓
Classification
    ↓
Learning Candidate
    ↓
Review / Generalization
    ↓
Reusable Pattern / Canonical Knowledge
```

Project repositories remain the source of truth for project-specific decisions.

## Agent Rule

If the user says:

> "Review [website] and save the useful new points to AiNote"

the agent must infer and record **scope + domain + potential target(s) + source**, and must not assume that every finding belongs to the same project or domain.

If classification is uncertain, preserve the finding as source-specific or candidate knowledge rather than guessing a broader scope.
