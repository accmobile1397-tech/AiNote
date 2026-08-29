# EntityLens.ir — Project Knowledge Candidate

**Status:** Idea Candidate / Discovery
**Source:** New project ideation session
**Date:** 2026-08-29

## Core Idea

EntityLens.ir is an Entity Intelligence platform/service/API. Given the name of a person or company, AI researches public web and social sources and produces a structured, evidence-backed intelligence profile containing relevant text, images, video, brand information, contact information, existing website content, social presence, and related public information.

## Primary Ecosystem Use Cases

### AiWebSiteBuilder.ir

When a customer requests a website and identifies themselves or their company, EntityLens should first help understand:
- who the customer/entity is;
- what the company/person does;
- existing website and digital presence;
- existing content and tone of voice;
- brand identity, logo, colors, imagery and visual style;
- public social presence;
- contact and business information;
- customer preferences and desired website direction.

The resulting Entity Intelligence Package can then be consumed by the website-generation workflow so generated sample/content data is close to reality rather than generic placeholder data.

### AiDrivenBusiness.ir

When a consulting customer identifies themselves or their company, EntityLens can prepare a documented intelligence dossier from public sources. The dossier can support business-transformation consulting and provide source/evidence references for facts used during the consultation.

## Product Form

EntityLens may initially operate as a service/API behind ecosystem products and may later become an independent user-facing product.

## Initial UX Hypothesis

- Main page is accessible after login.
- A primary search/input box accepts a person or company name.
- User clicks Search.
- AI performs research across the web and supported social sources.
- Results are generated in categorized sections.
- Results may include text, images, video and other relevant public media.
- Results retain source/evidence information and should not fabricate facts.

## API Hypothesis

EntityLens should expose the resulting Entity Intelligence through an API so AiWebSiteBuilder.ir, AiDrivenBusiness.ir and future products can consume the same researched entity knowledge instead of repeating research independently.

## Architectural/Product Principle Candidate

Research should produce a reusable Entity Knowledge Asset with evidence. Different consuming products can apply different lenses to the same entity:
- Website Lens
- Business Transformation Lens
- future product-specific lenses

## Important Discovery Constraints

- Public information must not be treated as unrestricted information.
- Sensitive/private information and unsupported inference must be excluded or governed explicitly.
- Source, retrieval context, confidence and verification status should be preserved where applicable.
- Social/web collection mechanisms must respect applicable access restrictions and terms.

## Relationship to Bootstrap

This is a project-level knowledge candidate discovered during the EntityLens project ideation. It is not yet a finalized PRD, architecture, or technical specification. During the project, new reusable lessons should be captured in the project repository and later submitted through the Knowledge Loop for review/generalization. Approved generalized knowledge may be used in a future Bootstrap upgrade.

## Next Discovery Topics

1. Entity definition and identity resolution.
2. Primary users and user journeys.
3. Core use cases and MVP boundary.
4. Supported source classes and evidence model.
5. Output/entity intelligence schema.
6. Customer-intent model.
7. Privacy, compliance and source-access boundaries.
8. API contract hypothesis.
