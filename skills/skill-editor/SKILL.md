---
name: skill-editor
description: Use when the user wants to create, audit, clean up, refactor, or improve agent skills, including trigger descriptions, evals.md, memory.md, AI slop removal, duplicate or stale instructions, and future skill standards.
metadata:
  short-description: Clean and improve agent skills
---


# Skill Editor

Use this skill to keep local agent skills sharp, triggerable, and low-slop. The goal is not to make every skill tiny. The goal is to make each skill easy to trigger, easy to evaluate, and useful without dragging stale or generic instructions into context.

## Use This For

- Creating or improving an agent skill.
- Auditing an existing skill for trigger quality, duplicate instructions, stale context, vague rules, and unnecessary verbosity.
- Adding or improving `evals.md` and `memory.md`.
- Removing AI slop such as em dashes, generic hooks, filler transitions, formulaic contrast phrasing, and performative professionalism.

## Required Standard

Every local skill folder should include:

- `SKILL.md` with YAML frontmatter containing `name` and a `description` that starts with explicit `Use when the user wants to...` trigger language.
- `evals.md` with 10 pass/fail checks tailored to the skill's common failure modes.
- `memory.md` with reverse-chronological one-sentence learnings from past uses.
- A `SKILL.md` reference to both `evals.md` and `memory.md` under a continuous improvement section.

## Cleanup Workflow

1. Read the target `SKILL.md`, `evals.md`, and `memory.md` if they exist.
2. Check whether the description is specific enough to trigger automatically from natural-language requests.
3. Remove duplicate instructions, stale context, vague rules, and generic assistant phrasing.
4. Preserve hard-earned domain judgment, approval boundaries, source requirements, and user-specific voice rules.
5. Tighten the skill body around what the assistant should do, what context to load, how to produce the output, and how to verify the result.
6. Update `evals.md` only when a recurring failure can be checked pass/fail.
7. Update `memory.md` only when real feedback from prior use should change future behavior.

## Eval Loop

- Test materially changed skills on 2-3 realistic prompts before treating the edit as done.
- Use a separate clean-context reviewer agent when available to grade against `evals.md`.
- If any eval fails, revise and rerun until all checks pass or the blocker is explicit.
- Keep the user as final reviewer for judgment-heavy outputs, especially voice, positioning, and strategic recommendations.

## Output

When auditing a skill, return:

- Trigger fixes
- Instruction cleanup
- Missing eval or memory coverage
- AI slop removed
- Recommended edits or the files changed

## Continuous Improvement

- Before materially changing this skill, test it manually on 2-3 realistic prompts.
- Use `evals.md` as the pass/fail self-check after meaningful runs or edits.
- Use a separate clean-context reviewer agent for evals when available; send failed checks back for revision until they pass or a blocker is clear.
- Add one-sentence learnings to `memory.md` when feedback should improve future uses and does not belong in the pass/fail evals.
