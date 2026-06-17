# But For Real Evals

Use these pass/fail checks after manual tests, meaningful skill edits, or important outputs. Prefer a separate clean-context reviewer agent when available. If any check fails, revise the output or skill and run the checks again.

1. **Trigger Fit:** Pass if this skill is used only for requests matching: Use when the user wants to run a rigorous second-pass review before finalizing meaningful deliverables or workspace changes, including code/config edits, automations, workflow changes, strategic deliverables, important writing, research synthesis, and recommendations.; fail if another local skill owns the workflow more directly.
2. **Required Context:** Pass if the run loads relevant memory, resources, and connected-app context named in `SKILL.md`; fail if it skips discoverable context or asks the user for what available context can answer.
3. **Output Shape:** Pass if the deliverable follows the sections, artifact type, and cadence defined in `SKILL.md`; fail if it becomes a generic memo, recap, or loose notes.
4. **Decision Value:** Pass if the output gives the user a concrete recommendation, decision, draft, artifact update, or next action; fail if it only summarizes.
5. **Voice / Judgment:** Pass if the language is concise, specific, and aligned with the user's context; fail if it sounds like a corporate memo or generic assistant prose.
6. **Specificity:** Pass if names, dates, companies, artifacts, obligations, signals, or examples are specific where the skill requires them; fail if placeholders or vague claims survive.
7. **Boundary Control:** Pass if draft-only work, workspace edits, external actions, and durable workflow changes are clearly separated; fail if the skill crosses an approval boundary.
8. **Failure Modes:** Pass if the output names missing context, stale facts, conflicts, or unsupported assumptions; fail if it smooths over uncertainty.
9. **No Slop / No Duplication:** Pass if the output avoids duplicate instructions, stale context, filler, and unnecessary verbosity; fail if cleanup would remove obvious noise.
10. **Learning Capture:** Pass if reusable feedback is added to `memory.md` only when useful; fail if memory duplicates eval checks or stores one-off noise.
