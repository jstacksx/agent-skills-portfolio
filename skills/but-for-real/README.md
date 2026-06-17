# But For Real

AI first drafts often sound done before they are true, useful, or safe to rely on.

This skill is the critic layer. It runs a blunt second pass before meaningful work ships.

## What It Does

- Checks unsupported assumptions.
- Re-reads the user's actual intent.
- Dry-runs the execution path.
- Tests the quality bar against likely failure modes.
- Produces a short verification proof when the work matters.

## Why I Built It

The cost of generation keeps falling. The cost of bad judgment has not.

This skill exists to catch the clean-sounding answer before it creates rework, embarrassment, or a broken workflow.

## Tools It Can Touch

- Local files and diffs.
- Test or validation commands when the work is technical.
- Source checks when facts are current, legal, financial, or otherwise date-sensitive.

## Files

- `SKILL.md` - agent instruction.
- `evals.md` - pass/fail quality checks.
- `memory.md` - public development notes.
- `examples/` - sample prompts.
