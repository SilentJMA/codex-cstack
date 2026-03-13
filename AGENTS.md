# AGENTS.md

Use `cstack` skills by default for structured software delivery work.

## Default Flow

- Planning requests:
  Use `$plan-product-review` first to validate user outcome and v1 scope.
  Then use `$plan-eng-review` to define architecture, risks, and test matrix.
- Review requests:
  Use `$review` by default.
  Prioritize correctness bugs, regressions, security/trust-boundary issues, and missing tests.
- Shipping requests:
  Use `$ship` by default.
  Verify readiness with checks, risk notes, and explicit blockers if not ready.

## Escalation Path

- If the user asks for validation evidence, run `$qa` after implementation.
- After completion, run `$retro` to capture improvements for the next cycle.

## Prompting Preference

- Keep outputs decision-oriented and concrete.
- Prefer one clear recommendation over many vague options.
