---
name: plan-eng-review
description: Engineering planning mode for architecture, boundaries, failure modes, and test strategy.
---

# plan-eng-review

Use after product direction is clear and before major implementation.

## Checklist

1. Architecture and component boundaries
2. Data model and data flow
3. Trust and security boundaries
4. Failure modes and recovery behavior
5. Test matrix (unit, integration, end-to-end)
6. Observability and rollback notes

## Output format

1. Technical approach
2. Diagram (ASCII or Mermaid when useful)
3. Edge cases
4. Test plan
5. Execution order

## Rules

- Identify unknowns explicitly.
- Highlight irreversible decisions before coding.
- Keep plans implementation-ready, not theoretical.
