# HTML Slides Evals

Use these pass/fail checks after manual tests, meaningful skill edits, or important outputs. Prefer a separate clean-context reviewer agent when available. If any check fails, revise the output or skill and run the checks again.

1. **Trigger Fit:** Pass if this skill is used only for requests matching: Use when the user wants to create, draft, revise, QA, or systematize single-file HTML slide decks, presentation decks, executive slides, advisory pitch decks, corporate update decks, or web-based presentations.; fail if another local skill owns the workflow more directly.
2. **Required Context:** Pass if the run loads relevant memory, resources, and connected-app context named in `SKILL.md`; fail if it skips discoverable context or asks the user for what available context can answer.
3. **Style Discovery:** Pass if an unlocked deck gets three real title-slide visual previews using the deck's actual content; fail if previews are generic cards, expose process labels, or skip discovery without a locked style.
4. **Decision Value:** Pass if the output gives the user a concrete recommendation, decision, draft, artifact update, or next action; fail if it only summarizes.
5. **Voice and Anti-Slop:** Pass if the language matches the user's voice and avoids em dashes, generic hooks, filler transitions, fake polish, and formulaic contrast phrasing; fail if those patterns remain.
6. **Specificity:** Pass if names, dates, companies, artifacts, obligations, signals, or examples are specific where the skill requires them; fail if placeholders or vague claims survive.
7. **Boundary Control:** Pass if draft-only work, workspace edits, external actions, and durable workflow changes are clearly separated; fail if the skill crosses an approval boundary.
8. **Fixed-Stage QA:** Pass if every generated deck uses a fixed 1920×1080 stage scaled to desktop and phone viewports with no scrollbars, clipping, or overlap; fail if content reflows by device or uses fragile slide visibility controls.
9. **Visual Distinctiveness:** Pass if the deck avoids generic AI aesthetics and uses a deliberate Executive Editorial or context-specific visual system; fail if it relies on purple gradients, default fonts, repetitive cards, or decorative filler.
10. **Learning Capture:** Pass if reusable feedback is added to `memory.md` only when useful; fail if memory duplicates eval checks or stores one-off noise.
