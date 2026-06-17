# Meeting Coach Evals

Use these pass/fail checks after manual tests, meaningful skill edits, or important coaching outputs. Prefer a separate clean-context reviewer agent when available. If any check fails, revise the output or skill and run the checks again.

1. **Trigger Fit:** Pass if the skill is used for meeting transcript review, communication coaching, concision, persuasion, questioning, summarization, or decision-driving feedback; fail if another local skill owns the request more directly.
2. **Speaker Identity:** Pass if the user's speaker label is confirmed before analysis; fail if the output guesses which speaker is the user.
3. **Input Handling:** Pass if pasted transcripts are analyzed directly and referenced meetings are retrieved or clarified; fail if the skill asks for context a connector or transcript can provide.
4. **Evidence:** Pass if every substantive critique ties to a transcript moment, timestamp, speaker turn, quote, or paraphrase; fail if feedback is generic.
5. **Blunt Usefulness:** Pass if the tone is direct, executive-level, and practical; fail if it becomes soft encouragement, theatrical harshness, or corporate coaching speak.
6. **Behavior Change:** Pass if recommendations focus on actions the user can apply in the next meeting; fail if they are abstract traits or broad self-improvement advice.
7. **Communication Lens:** Pass if the review covers relevant clarity, concision, persuasion, question quality, summarization, decision-driving, and executive presence; fail if it only summarizes content.
8. **Better Phrasing:** Pass if rewrites are specific, compressed, and sound like something the user could actually say; fail if they are generic, verbose, or out of voice.
9. **Decision Orientation:** Pass if missed chances to align, summarize, assign ownership, ask for timing, or push for a decision are identified when present; fail if decision-driving moments are ignored.
10. **Approval Boundary:** Pass if the skill creates coaching output only unless the user explicitly asks for storage, tracking, drafts, or workflow changes; fail if it updates memory or external tools without approval.
