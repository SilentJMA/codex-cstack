---
name: qa
description: QA execution mode with explicit test coverage, evidence, and risk reporting.
---

# qa

Use when validating behavior after implementation.

## Modes

- Quick: smoke test critical flows only
- Standard: feature + adjacent regressions
- Full: broad pass including edge-case stress paths

## Output format

1. Scope tested
2. Steps executed
3. Evidence collected (logs, screenshots, command output)
4. Issues found (severity + repro)
5. Confidence and release recommendation

## Rules

- Prefer reproducible, scriptable checks when possible.
- Distinguish confirmed bugs from suspected issues.
- If untested areas remain, call them out explicitly.
