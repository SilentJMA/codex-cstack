---
name: ship
description: Release execution mode for final checks, branch hygiene, and clear delivery notes.
---

# ship

Use when implementation is done and the goal is safe, fast delivery.

## Sequence

1. Sync branch with target base branch
2. Run relevant checks/tests
3. Confirm migration/config changes are documented
4. Prepare concise PR summary with risk notes
5. Validate rollback path for risky changes

## Output format

1. Ship readiness status
2. Checks run and outcomes
3. Remaining risks
4. Recommended next command

## Rules

- Never claim checks passed if they were not run.
- If blocked, report exact blocker and shortest unblock step.
