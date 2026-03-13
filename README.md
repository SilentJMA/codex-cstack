# cstack

[![Codex Skills](https://img.shields.io/badge/Codex-skills-0A0A0A?style=flat-square)](https://github.com/SilentJMA/codex-cstack)
[![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Linux%20%7C%20Windows-1F6FEB?style=flat-square)](https://github.com/SilentJMA/codex-cstack)
[![License](https://img.shields.io/badge/license-MIT-16A34A?style=flat-square)](./LICENSE)

`cstack` is a Codex workflow skill pack inspired by [gstack](https://github.com/garrytan/gstack).

It gives Codex explicit modes so you can switch between product thinking, technical planning, review rigor, release execution, QA, and retrospectives.

## Included Skills

- `plan-product-review`
- `plan-eng-review`
- `review`
- `ship`
- `qa`
- `retro`

## Quick Start

1. Clone this repo into your Codex skills directory.
2. Run `setup` once.
3. Trigger skills by name in your prompts.

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

### Windows (Git Bash / WSL direct)

```bash
mkdir -p "$CODEX_HOME/skills"
git clone https://github.com/SilentJMA/codex-cstack.git "$CODEX_HOME/skills/cstack"
cd "$CODEX_HOME/skills/cstack"
chmod +x setup
./setup
```

Notes:

- On Windows, WSL is recommended for best compatibility with the `setup` script.
- If symlink creation is restricted, enable Developer Mode or run the terminal with elevated permissions.

## Usage Examples

- `Use $plan-product-review for this feature request.`
- `Run $plan-eng-review and give me architecture + test matrix.`
- `Do a $review and list findings by severity.`
- `Use $ship mode and verify merge readiness.`
- `Run $qa in quick mode for this fix.`
- `Create a $retro for this delivery.`

## Repository Layout

- `SKILL.md`: top-level meta skill and routing guidance
- `setup`: symlink helper for sub-skills
- `<skill-name>/SKILL.md`: each mode-specific skill prompt

## Inspiration

This project adapts the workflow concept from [gstack](https://github.com/garrytan/gstack) for Codex skill triggering.

## License

[MIT](./LICENSE)
