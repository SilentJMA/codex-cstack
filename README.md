# cstack

`cstack` is a Codex workflow skill pack inspired by [gstack](https://github.com/garrytan/gstack).

It gives Codex explicit modes so you can switch between product thinking, technical planning, review rigor, release execution, QA, and retros.

## Skills

- `plan-product-review`
- `plan-eng-review`
- `review`
- `ship`
- `qa`
- `retro`

## Install

```bash
mkdir -p "$CODEX_HOME/skills"
git clone https://github.com/SilentJMA/codex-cstack.git "$CODEX_HOME/skills/cstack"
cd "$CODEX_HOME/skills/cstack"
./setup
```

The `setup` script creates convenience symlinks in `$CODEX_HOME/skills` so you can trigger skills directly by name.

## Usage examples

- `Use $plan-product-review for this feature request.`
- `Run $plan-eng-review and give me architecture + test matrix.`
- `Do a $review and list findings by severity.`
- `Use $ship mode and verify merge readiness.`
- `Run $qa in quick mode for this fix.`
- `Create a $retro for this delivery.`

## Repository layout

- `SKILL.md`: top-level meta skill and routing guidance
- `setup`: symlink helper for sub-skills
- `<skill-name>/SKILL.md`: each mode-specific skill prompt

## Inspiration

This project is inspired by `gstack`'s workflow concept and adapted for Codex skill triggering.

## License

MIT
