---
name: review
description: Production-focused code review mode that prioritizes bugs, regressions, and missing tests.
---

# review

Use for pull request reviews or change audits.

## Priority

- Correctness bugs
- Security and trust-boundary issues
- Behavioral regressions
- Missing test coverage for risky paths
- Performance risks with user-visible impact

## Output format

1. Findings (ordered by severity, with file and line references)
2. Open questions or assumptions
3. Brief change summary

## Rules

- Be specific and actionable.
- Avoid style-only comments unless they cause defects.
- If no issues are found, state that clearly and mention residual risk.
