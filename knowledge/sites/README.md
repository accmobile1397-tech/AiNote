# Site/Product Knowledge Spaces

This directory groups knowledge by the user's own sites/products.

Each site/product is a context boundary. Observations, research, candidates, validated knowledge, and product-specific decisions related to that site should remain discoverable together.

## Structure

```text
knowledge/sites/<site>/
├── README.md
├── observations/
├── research/
├── candidates/
├── knowledge/
└── decisions/
```

The lifecycle/status of a finding is separate from its site context. A finding may move from observation to candidate to reviewed knowledge without losing its source or site association.

## Classification

- `site/product` — belongs specifically to one of our own products/sites.
- `domain` — belongs to a broader domain and may be relevant to more than one of our sites; keep the source and potential targets in metadata.
- `generic` — broadly reusable across products; store in the generic/shared area while preserving provenance.
- `source-specific` — useful observation that has not yet been safely generalized.

A source website used for competitive research is evidence/source metadata, not automatically a site/product knowledge space.

## Rule

When a website is reviewed, the agent must classify each finding independently. Findings from one source may legitimately be distributed across multiple site/product spaces and the generic/shared area.
