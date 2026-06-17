# Skill Editor

Local skills decay unless someone maintains them.

Trigger language gets vague. Instructions duplicate. Evals test the wrong thing. Generic AI phrasing creeps in.

This skill audits and improves other skills so an agent system stays useful as it grows.

## What It Does

- Checks whether the trigger description is specific enough.
- Removes stale, duplicated, or generic instructions.
- Preserves hard-earned workflow judgment.
- Tightens the skill around inputs, process, output, and verification.
- Updates evals only when a real failure mode can be tested.

## Why I Built It

Once skills become a real operating layer, skill maintenance becomes its own workflow.

This is the meta-skill: the agent that keeps the other agents sharp.

## Tools It Can Touch

- `SKILL.md`
- `evals.md`
- `memory.md`
- Local skill folders and examples

## Files

- `SKILL.md` - agent instruction.
- `evals.md` - pass/fail quality checks.
- `memory.md` - public development notes.
- `examples/` - sample prompts.
