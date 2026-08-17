# Knowledge Loop PO Reporting Invariant v1.0

## Origin
Generalized from Bootstrap LC-0003 Knowledge Loop PO Reporting.

## Canonical Principle
Knowledge Loop processing and PO-facing reporting are separate concerns. After applicable Knowledge Loop processing completes, the runtime MUST provide concise durable PO-facing visibility regardless of execution-control mode.

## Required Visibility
The report should cover discoveries, candidate capture, AiNote intake, review/generalization status, Bootstrap impact, and unresolved decisions when applicable.

## Boundary
Execution mode may govern approval and execution interaction, but MUST NOT suppress post-loop visibility. Concrete report format and storage are implementation-specific.

## Promotion Status
Canonical generalized knowledge in AiNote. Bootstrap impact requires a separate governed promotion decision.
