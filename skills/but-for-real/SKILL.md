---
name: but-for-real
description: Use when the user wants to run a rigorous second-pass review before finalizing meaningful deliverables or workspace changes, including code/config edits, automations, workflow changes, strategic deliverables, important writing, research synthesis, and recommendations.
metadata:
  short-description: Run an adversarial final quality gate
---


# But For Real

## Use This For

- Code, script, config, adapter, automation, or workflow changes
- Strategic deliverables, recommendations, research synthesis, and important written content
- Any task where a wrong answer would create rework, embarrassment, misleading analysis, broken process, or lost trust

Stay lightweight for quick lookups, simple formatting, low-stakes rewrites, and direct answers.

## Core Philosophy

Assume the first pass is elegantly broken. Do not declare victory until the work has survived a second pass against the most likely failure modes.

In an AI-native operating system, this skill is the critic layer in the coordination loop. Its job is to protect judgment, truth, and trust when generation is cheap. It should catch weak assumptions, stale facts, brittle routing, over-automation, voice drift, and recommendations that sound clean but do not survive contact with the actual workflow.

## Mandatory Second Pass

Before finalizing, silently review the work through these lenses:

1. **Assumption Check**
   - What did you assume without proof?
   - Which assumption would break the output if wrong?
   - For code or workflow changes, identify the exact line, branch, dependency, or trigger most likely to fail.

2. **User Intent Check**
   - Re-read the user's prompt and recent context.
   - If the user is asking to "try again" or fix prior work, identify the underlying failure, not just the visible symptom.
   - Confirm the output solves the real ask, not the easiest adjacent task.

3. **Execution Trace Check**
   - Dry-run the path from input to output.
   - Check boundary conditions: empty inputs, missing context, stale facts, conflicting instructions, permissions, async timing, null values, unsupported file types, or ambiguous recipients.
   - For coordinated workflows, confirm the right memory, resources, and connected apps were considered before output.

4. **Quality Bar Check**
   - For writing: cut filler, sharpen the lead, remove generic phrasing, and confirm the voice matches the context.
   - For research or analysis: separate known facts from inference, check date sensitivity, and name what remains unverified.
   - For recommendations: test whether the logic would still hold if the most convenient supporting fact were removed.
   - For code or systems work: verify with tests, validation scripts, dry-runs, or targeted inspection whenever feasible.
   - For automations or agentic workflows: confirm the approval boundary is clear and the system is not taking external or durable action when a draft or recommendation is the safer default.

## Final Response Requirement

When the task changes files, creates reusable workflow assets, or produces an important deliverable, end with:

```markdown
### Verification Proof
- **The Risk:** What could have been wrong, weak, incomplete, misleading, or brittle.
- **The Proof:** What you checked and why the final output holds up.
- **The Limit:** Only include if something important remains unverified.
```

Keep the proof brief. It is a receipt, not a second memo.


## Continuous Improvement

- Before materially changing this skill, test it manually on 2-3 realistic prompts.
- Use `evals.md` as the pass/fail self-check after meaningful runs or edits.
- Use a separate clean-context reviewer agent for evals when available; send failed checks back for revision until they pass or a blocker is clear.
- Add one-sentence learnings to `memory.md` when feedback should improve future uses and does not belong in the pass/fail evals.
