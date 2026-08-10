# Cursor Agent UI Development Tooling Pattern v1.0

## Status

Proposed reusable knowledge pattern.

## Purpose

Define a preferred Cursor Agent tooling stack for AI-native web application development, with particular emphasis on high-quality UI implementation, design fidelity, browser verification, and evidence-backed delivery.

## Core Pattern

Use Cursor Marketplace plugins as capability extensions around the development lifecycle rather than installing plugins indiscriminately.

Recommended UI-first chain:

```text
Figma / Design System
        ↓
Figma Plugin / MCP / Skills
        ↓
Cursor Agent
        ↓
shadcn/ui + project design system
        ↓
Next.js / React / Tailwind
        ↓
Browser verification
        ↓
Playwright and/or Subtext
        ↓
Visual evidence / regression evidence
        ↓
GitHub
```

## Preferred UI Stack

### 1. Figma — primary design source

Use the official Figma Cursor plugin for design-to-code and code-to-design workflows, Code Connect, design-system-aware implementation, and diagram generation.

Use Figma as the preferred source when a product has an explicit visual design system.

### 2. shadcn/ui — implementation component system

Use the official shadcn/ui Cursor plugin for component discovery, installation, fixing, debugging, styling, composition, registries, presets, and project-aware component work.

The project remains the source of truth for the actual component source code and project-specific design decisions.

### 3. Browser verification — mandatory for important UI

Do not consider a UI task complete merely because the code builds. Run the application and verify the rendered result in a browser.

Verify at minimum:

- responsive behavior
- layout and spacing
- typography
- RTL behavior where applicable
- interaction states
- navigation
- forms
- loading/error/empty states
- accessibility-critical behavior

### 4. Playwright — deterministic browser testing

Prefer Playwright for repeatable E2E and browser tests, especially for acceptance criteria and regression coverage.

### 5. Subtext — evidence and visual review candidate

Use Subtext when reviewer-facing evidence, visual regression, live browser exploration, or proof of changes is valuable. It can provide browser interaction and evidence-oriented workflows.

Subtext is complementary to Playwright rather than an automatic replacement for deterministic project tests.

## Recommended Plugin Policy

Install a plugin only when it provides a concrete capability required by the project or workflow.

Initial UI-focused recommendation:

1. Figma
2. shadcn/ui
3. Playwright or equivalent deterministic browser testing capability
4. Subtext when evidence/visual review is required
5. GitHub integration where existing GitHub connectivity does not already provide the required capability

Potential later additions:

- Sentry for production error investigation
- Datadog/Grafana or another observability integration for infrastructure/runtime operations
- Postman/API tooling for API lifecycle workflows
- OpenShip-specific integration for deployment operations

## Agent Workflow Rule

For UI work, prefer the following instruction pattern:

1. Read the relevant product/design specifications.
2. Inspect the existing design system and components.
3. Use the Figma source when available.
4. Reuse existing shadcn/project components before creating new primitives.
5. Implement the smallest coherent change.
6. Run the application.
7. Verify the result in a real browser.
8. Run relevant automated tests.
9. Capture evidence for important visual/UX changes.
10. Report changed files, verification performed, evidence, and remaining limitations.

## Mobile-First Cloud Agent Application

For remote work from mobile, a high-value workflow is:

```text
User on mobile
    ↓
Cursor Cloud Agent
    ↓
Read project/design context
    ↓
Implement UI
    ↓
Run application
    ↓
Browser verification
    ↓
Tests + evidence
    ↓
GitHub commit/PR
```

The goal is for the user to be able to request a complete UI task remotely without needing to open the local IDE for every iteration.

## Agent-Agnostic Principle

This pattern describes capabilities and workflow, not a permanent dependency on Cursor. Figma, component systems, browser automation, evidence capture, GitHub, and deployment integrations should remain replaceable abstractions where practical.

Cursor Marketplace is currently one implementation of this capability model.

## Architectural Implication for Agentic SDLC

The pattern should be treated as reusable development knowledge and may later be generalized into Agentic-SDLC-Platform capabilities. Cursor-specific details should remain adapters/integrations rather than becoming the core SDLC protocol.

## Decision Summary

**Preferred UI capability chain:** Figma → design-system-aware implementation → shadcn/ui → browser verification → Playwright/evidence → GitHub.

**Principle:** UI quality requires rendered verification, not code-only verification.

**Principle:** Marketplace plugins are capability adapters; project knowledge and the repository remain the source of truth.

## References

- Cursor Marketplace: https://cursor.com/marketplace
- Cursor Figma plugin: https://cursor.com/marketplace/figma
- Cursor shadcn/ui plugin: https://cursor.com/marketplace/shadcn
- Cursor Subtext plugin: https://cursor.com/marketplace/subtext
