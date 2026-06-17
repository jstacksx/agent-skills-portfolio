---
name: html-slides
description: Use when the user wants to create, draft, revise, QA, or systematize single-file HTML slide decks, presentation decks, executive slides, advisory pitch decks, corporate update decks, or web-based presentations.
metadata:
  short-description: Build polished single-file HTML decks
---


# HTML Slides

Use this skill to turn sparse outlines, raw notes, documents, or company context into practical, responsive, single-file HTML presentations. The default output is a native HTML deck, not a PDF or screenshot wrapper.

## Intake

Before generating code, identify:

- Mode: A file/template profile, B scratch/minimalist, or C web-derived brand discovery.
- Target slide count.
- Audience and tone.
- Source material: outline, document, URL, company, template, or existing profile.
- Density: infer by context unless the user specifies. Default to reading-first for corp dev, advisory, interview, board, buyer-facing, and async review decks; default to speaker-led for live talks, content repurposing, and presentation coaching.
- Style lock: whether the user has already provided a template, brand system, or explicit visual direction.

Ask only for missing details that materially affect the deck. If the mode is obvious from the request, proceed and state the assumption.

## Mode Selection

- **Mode A: Template profile.** Use when the user provides a PPTX/template or names an existing profile. Load the relevant profile from `references/` when available. Do not re-parse the PPTX unless a new template is provided or the user asks to refresh the profile.
- **Mode B: Scratch.** Use when no template or brand URL is provided. Default to Executive Editorial: restrained, high-polish, strong hierarchy, distinctive but credible typography, and layouts such as cover, agenda, two-column, stat grid, bento grid, comparison, timeline, chart, and conclusion.
- **Mode C: Web-derived.** Use when the user provides a company URL and wants the deck to match that company. Browse the homepage or brand page, inspect CSS/DOM for colors and type stacks, then create a temporary brand profile in the working output folder before generating the deck.

## Frontend Slides Integration

This skill incorporates selected assets and workflow patterns from `zarazhangrui/frontend-slides`, stored in `references/frontend-slides/`. Use them as a reference library inside this existing `html-slides` workflow; do not create a separate top-level `frontend-slides` skill.

Load these assets when building or materially revising a deck:

- `references/frontend-slides/viewport-base.css` for fixed-stage viewport behavior.
- `references/frontend-slides/html-template.md` for single-file deck architecture and navigation patterns.
- `references/frontend-slides/STYLE_PRESETS.md` for safe visual systems.
- `references/frontend-slides/animation-patterns.md` for restrained motion choices.
- `references/frontend-slides/bold-template-pack/selection-index.json` for optional bold template candidates.

Generate three real title-slide style previews before the full deck when the user has not locked a style. The previews must look like first slides from the actual deck, not diagnostic cards. Use the user's content, title, company, date, or genuine framing language. Never render internal labels such as "preview," "style option," "template," "generated," file paths, mode names, source notes, or workflow instructions inside the slide.

Preview mix:

- One Executive Editorial or safe preset option.
- One restrained bold template candidate when appropriate.
- One wildcard option, either a second template or a custom visual thesis tailored to the deck.

For conservative or high-stakes decks, keep all three options executive-ready. Bold means visually memorable, not loud. If the user names a style, template, or brand direction, skip broad discovery and use that direction unless it conflicts with readability or audience fit.

If a bold template is selected, read the selected template's `design.md` only after the choice. Do not load every template's full design file up front.

## Required Workflow

1. Classify mode and load the right profile or source context.
2. Retrieve and parse source material. For PPTX inputs, use `scripts/extract_pptx_dna.py` or existing PPTX tooling when profile creation is needed.
3. Use web augmentation only when current facts, company context, metrics, or missing claims matter.
4. Infer density by context unless specified. Use reading-first for async/executive artifacts and speaker-led for live talks or content repurposing.
5. If style is not locked, generate three real title-slide previews and ask the user to choose or mix. If style is locked, document the chosen direction and proceed.
6. Generate a standalone native HTML file. Prefer inline CSS/JS, native tables, SVG charts, and small custom chart renderers so the deck works as a single local file. Use CDN libraries only when the user explicitly wants them.
7. Run the executive readiness gate and slide audit checklist before visual QA.
8. Run a visual QA loop with browser screenshots. Check every slide for scrollbars, clipping, low contrast, awkward wraps, repeated layouts, and fixed-stage scaling at desktop plus phone viewport.
9. Fix the HTML and re-run QA until the deck passes.

## Output Tiers

- **Native HTML Deck:** Default. Build each slide as editable HTML with native text, tables, cards, SVG diagrams/charts, CSS motion, and keyboard navigation.
- **Hybrid Deck:** Use native HTML for the deck and selected embedded images only where reconstruction is inefficient, such as screenshots, logos, maps, or product UI.
- **Reference Wrapper:** Fast fidelity fallback. Embed rendered PDF/PPTX pages as images only when the user asks for literal preservation or speed. Label this explicitly as a wrapper, not the main skill output.

## Layout Rules

- Every deck uses a fixed 1920×1080 slide stage scaled uniformly to the viewport. It may letterbox or pillarbox, but slide content must not reflow by device.
- Every slide must fit exactly inside the fixed 16:9 stage and the visible browser viewport.
- No vertical or horizontal scrollbars. Overflow is a failure.
- Include the full contents of `references/frontend-slides/viewport-base.css` or an equivalent fixed-stage implementation in each generated deck.
- Use `.active` / `.visible` style visibility, opacity, and pointer-event controls for slide switching. Do not use `display: none` / `display: block` as the primary slide-switching mechanism.
- Never use the same layout blueprint more than two slides in a row.
- Choose layouts from the content: stats need scorecards or stat grids; sequence needs timeline/process; decision work needs matrix/scorecard; narrative needs text split or divider.
- If content density threatens overflow, reduce type size, tighten hierarchy, split the slide, or summarize. Do not let content clip.
- Keep text blocks scannable. Use strong headers, concise body copy, and visible hierarchy.
- For reusable archetypes, load `references/layout-blueprints.md`.

## Visual Standards

Default taste is Executive Editorial for executive-facing work: polished, restrained, specific, and commercially credible. Avoid generic AI aesthetics: purple gradients on white, predictable dashboard cards, overused fonts, decorative filler, vague iconography, or layouts that look like a template demo.

Use distinctive design choices only when they sharpen the audience outcome. For corp dev, board, interview, advisory, and buyer-facing work, the deck should feel confident and expensive, not playful. For LinkedIn/content/talk decks, use more expressive pacing and visual contrast while preserving the user's voice: specific, direct, and compressed.

## Executive Readiness Gate

Use this gate for CEO, board, IC, investor, or executive presentations.

- Never expose implementation metadata inside the deck: no "Mode A", "native HTML", "rebuild", "template", "generated", "source", "under the hood", or tool/process labels.
- Section divider numbers must map to agenda sections, not slide numbers. Use the folio for slide numbers only.
- Every subtitle must be specific and decision-useful. Remove clever filler, meta commentary, or vague framing.
- Native HTML rebuilds must improve the source deck's argument, not dilute it with decorative layouts.
- Metrics must have labels and context: `$275M` becomes "base-case enterprise value"; multiples must say revenue, EBITDA, ARR, etc.
- If a slide has obvious whitespace, use it to increase hierarchy, add decision-useful context, or simplify the layout. Do not leave it looking underbuilt.
- Remove duplicative recommendation or conclusion slides unless they add a new decision, condition, owner, or next action.

## Slide Audit Checklist

Before final delivery, check:

- Audience and context fit the stated forum.
- Agenda and section divider numbering are correct.
- Titles and subtitles are useful, not filler.
- No implementation language appears in visible content.
- Each important metric has context.
- Layouts fit the content and look executive-ready.
- No slide clips, scrolls, or hides content at normal presentation viewport.
- No repeated layout runs more than twice.
- Recommendation slides are not duplicative.

## QA Helpers

- Use `scripts/qa_html_deck.mjs` to detect viewport overflow and capture screenshots from a local HTML deck.
- If the local shell cannot launch a browser, use the available browser/screenshot tool for the same checks and record the limitation.
- Use `scripts/extract_pptx_dna.py` to summarize theme colors, layout names, slide text, and media counts from a PPTX template.

## Output

Return:

- The local HTML file path.
- A short summary of the mode, profile, and layout system used.
- Verification notes covering screenshot/overflow QA and any remaining limits.

If the user asks for PPTX export, treat that as a separate output step; this skill defaults to HTML decks.


## Continuous Improvement

- Before materially changing this skill, test it manually on 2-3 realistic prompts.
- Use `evals.md` as the pass/fail self-check after meaningful runs or edits.
- Use a separate clean-context reviewer agent for evals when available; send failed checks back for revision until they pass or a blocker is clear.
- Add one-sentence learnings to `memory.md` when feedback should improve future uses and does not belong in the pass/fail evals.
