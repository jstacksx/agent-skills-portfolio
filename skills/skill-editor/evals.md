# Skill Editor Evals

Use these pass/fail checks after manual tests, meaningful skill edits, or important outputs. Prefer a separate clean-context reviewer agent when available. If any check fails, revise the output or skill and run the checks again.

1. **Trigger Fit:** Pass if this is used for creating, auditing, cleaning, or improving agent skills; fail if the request is ordinary writing, coding, or workspace cleanup.
2. **Frontmatter Check:** Pass if the target skill has `name` and a description starting with `Use when the user wants to...`; fail if trigger language is missing, vague, or buried in the body.
3. **Trigger Specificity:** Pass if the description includes natural phrases the user would actually use; fail if it is too broad to route reliably.
4. **Companion Files:** Pass if the target skill has `evals.md` and `memory.md`; fail if either is missing or not referenced from `SKILL.md`.
5. **Eval Quality:** Pass if `evals.md` has 10 pass/fail checks tied to the skill's real failure modes; fail if the checks are generic scaffold hygiene.
6. **Memory Discipline:** Pass if `memory.md` stores only reverse-chronological one-sentence learnings from real use; fail if it duplicates evals, stores one-off noise, or invents learnings.
7. **Instruction Cleanup:** Pass if duplicate, stale, vague, and contradictory instructions are removed while preserving domain judgment; fail if cleanup deletes useful context or leaves obvious bloat.
8. **Anti-Slop Cleanup:** Pass if the skill removes or flags em dashes, generic hooks, filler transitions, performative professionalism, and formulaic contrast phrasing where they would degrade outputs; fail if those patterns remain in generated guidance.
9. **Approval Boundary:** Pass if the edited skill keeps draft-only, external-action, and durable-workflow boundaries clear; fail if cleanup weakens safeguards.
10. **Actionable Report:** Pass if the audit names concrete fixes or changed files; fail if it returns generic advice without implementation value.
