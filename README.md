# cstack

[![Codex Skills](https://img.shields.io/badge/Codex-skills-0A0A0A?style=flat-square)](https://github.com/SilentJMA/codex-cstack)
[![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Linux%20%7C%20Windows-1F6FEB?style=flat-square)](https://github.com/SilentJMA/codex-cstack)
[![License](https://img.shields.io/badge/license-MIT-16A34A?style=flat-square)](./LICENSE)

**cstack turns Codex from one generic assistant into a set of explicit delivery modes.**

Inspired by [gstack](https://github.com/garrytan/gstack), this pack gives you clear workflow gears for planning, engineering design, review, release, QA, and retrospectives.

## Why cstack

Without explicit modes, requests blur together:

- product planning gets mixed with implementation details
- review quality varies by prompt quality
- shipping can drift into open-ended discussion

With cstack, you pick the right mode for the phase and get more consistent output quality.

## Modes

| Skill | Mode | What it does |
|---|---|---|
| `plan-product-review` | Product strategy | Reframes the request around user outcomes and sharp v1 scope. |
| `plan-eng-review` | Technical design | Produces architecture, edge cases, risks, and test matrix before coding. |
| `review` | Production reviewer | Prioritizes bugs, regressions, trust boundaries, and missing tests. |
| `ship` | Release execution | Checks merge readiness, validation status, and remaining blockers. |
| `qa` | Validation lead | Runs quick/standard/full test scopes with evidence and confidence level. |
| `retro` | Continuous improvement | Captures wins, pain points, and concrete next-cycle improvements. |

## Example Flow

```text
You: Use $plan-product-review for this feature idea.
Codex: Clarifies user job, defines v1, surfaces product risks.

You: Now run $plan-eng-review.
Codex: Architecture + failure modes + test plan + execution order.

You: Implement.

You: Run $review on current changes.
Codex: Lists high-risk findings first with concrete file references.

You: Apply fixes.

You: Use $ship.
Codex: Reports ship-readiness, checks run, and any blockers.

You: Run $qa quick.
Codex: Smoke coverage + evidence + confidence recommendation.

You: Run $retro.
Codex: What worked, what hurt, and what to improve next.
```

## Installation

### macOS

```bash
mkdir -p "$CODEX_HOME/skills"
git clone https://github.com/SilentJMA/codex-cstack.git "$CODEX_HOME/skills/cstack"
cd "$CODEX_HOME/skills/cstack"
chmod +x setup
./setup
```

### Linux

```bash
mkdir -p "$CODEX_HOME/skills"
git clone https://github.com/SilentJMA/codex-cstack.git "$CODEX_HOME/skills/cstack"
cd "$CODEX_HOME/skills/cstack"
chmod +x setup
./setup
```

### Windows (PowerShell)

```powershell
$skills = Join-Path $env:CODEX_HOME "skills"
New-Item -ItemType Directory -Force -Path $skills | Out-Null
git clone https://github.com/SilentJMA/codex-cstack.git (Join-Path $skills "cstack")
wsl bash -lc 'cd "$CODEX_HOME/skills/cstack" && chmod +x setup && ./setup'
```

### Windows (Git Bash / WSL)

```bash
mkdir -p "$CODEX_HOME/skills"
git clone https://github.com/SilentJMA/codex-cstack.git "$CODEX_HOME/skills/cstack"
cd "$CODEX_HOME/skills/cstack"
chmod +x setup
./setup
```

Notes:

- WSL is recommended on Windows for best compatibility.
- If symlinks fail, enable Windows Developer Mode or run terminal as Administrator.

## AGENTS.md Default Snippet

If your project uses `AGENTS.md`, add this:

```md
Use cstack skills by default for structured software delivery work.

Planning:
- $plan-product-review first
- then $plan-eng-review

Review:
- $review by default

Shipping:
- $ship by default
```

This keeps behavior consistent across contributors and sessions.

## Usage Prompts

- `Use $plan-product-review for this request before coding.`
- `Run $plan-eng-review and include architecture plus test matrix.`
- `Do a $review and list findings by severity.`
- `Use $ship and tell me if this branch is merge-ready.`
- `Run $qa in standard mode for this feature.`
- `Create a $retro for this delivery.`

## Repository Layout

- `AGENTS.md`: default routing guidance for planning/review/shipping
- `SKILL.md`: meta skill with selection guide
- `setup`: symlink helper for sub-skills
- `<skill>/SKILL.md`: mode-specific instructions

## Inspiration

cstack is inspired by gstack's explicit workflow model and adapted for Codex-native skill triggering.

## License

[MIT](./LICENSE)
