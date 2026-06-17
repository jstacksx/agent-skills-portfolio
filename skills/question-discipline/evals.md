# Question Discipline Evals

Use these pass/fail checks after manual tests, meaningful skill edits, or important question-strategy outputs. Prefer a separate clean-context reviewer agent when available. If any check fails, revise the output or skill and run the checks again.

1. **Trigger Fit:** Pass if the skill is used for asking better questions, finding an eigenquestion, pressure-testing a question list, meeting/interview question design, or discovery question improvement; fail if another local skill owns the workflow more directly.
2. **Required Context:** Pass if the run loads any relevant memory, resource, or connected-app context; fail if it asks the user for discoverable background.
3. **Decision Target:** Pass if the output names the decision, diagnosis, meeting outcome, or next action the questions are meant to unlock; fail if it starts with generic question lists.
4. **Eigenquestion Quality:** Pass if the eigenquestion would materially change downstream decisions; fail if it is broad, obvious, or merely interesting.
5. **Ranking Logic:** Pass if questions are ordered by decision leverage; fail if they are ordered by chronology, curiosity, or generic discovery flow.
6. **Cut Discipline:** Pass if low-leverage, vague, duplicative, or discoverable questions are removed or flagged; fail if the output adds more questions without pruning.
7. **Specificity:** Pass if each question exposes constraints, tradeoffs, objections, timing, ownership, decision criteria, or risk; fail if questions invite vague answers.
8. **Voice Fit:** Pass if questions are direct, commercially sharp, and low-filler; fail if they sound like a consultant checklist or generic assistant script.
9. **Operating Move:** Pass if the output tells the user what to ask first and what answer would change the plan; fail if it only provides a list.
10. **Boundary Control:** Pass if the skill produces draft questions and strategy only unless the user explicitly asks for storage, sending, or workflow changes; fail if it crosses an approval boundary.
