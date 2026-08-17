# Agent Workflow Dispatch Capability Pattern v1.0

## Origin
Generalized from Bootstrap LC-0003 Workflow Dispatch Agent Tooling Gap.

## Canonical Principle
Routine CI workflow execution SHOULD be available as an Agent capability rather than requiring a permanent manual PO action.

## Governance Requirements
The capability MUST be Agent-agnostic, preserve explicit governance and approval gates, fail closed on authorization or execution uncertainty, and produce durable evidence that survives Agent replacement.

## Boundary
The reusable knowledge is the capability/governance invariant. Specific GitHub APIs, MCP servers, GitHub Apps, credentials, and tool implementations are implementation choices and are not canonical here.

## Promotion Status
Canonical generalized knowledge in AiNote. Bootstrap impact requires a separate governed promotion decision.
