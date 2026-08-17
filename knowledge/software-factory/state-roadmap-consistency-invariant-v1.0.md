# State/Roadmap Consistency Invariant v1.0

## Origin
Generalized from Bootstrap LC-0002.

## Canonical Principle
A governed SDLC transition MUST NOT be reported successful unless canonical machine-readable State and Roadmap are mutually consistent and the consistency validation passes.

## Reusable Value
This invariant protects fresh-agent resume, handoff, milestone detection, and autonomous execution from durable repository drift.

## Boundary
The invariant is reusable; the concrete transition engine, schema, validator, and roadmap representation are project-specific.

## Promotion Status
Canonical generalized knowledge in AiNote. Bootstrap impact requires a separate governed promotion decision.
