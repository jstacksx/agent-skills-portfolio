# Agent Skills Portfolio

AI-native operating skills built by Jann Lau.

This repo is a public library of reusable agent skills: structured instructions, evals, examples, and build notes for workflows where a general assistant needs sharper judgment.

The focus is operator leverage. Each skill turns a repeatable judgment pattern into something an AI agent can run, test, and improve.

## What's Inside

- `skills/` - individual skill folders with `SKILL.md`, `evals.md`, memory notes, examples, and public-facing docs.
- `skills.json` - structured metadata for a future portfolio site.
- `portfolio-site-prompt.md` - a prompt for Lovable, v0, or another site builder.

## First Batch

- `question-discipline` - finds the highest-leverage question in a decision, meeting, interview, or discovery process.
- `but-for-real` - runs an adversarial second-pass review before important work ships.
- `skill-editor` - audits and improves local agent skills.
- `html-slides` - builds polished single-file HTML decks for executive and advisory work.
- `meeting-coach` - reviews meeting transcripts and gives blunt, specific communication coaching.

## How To Use

Open a skill folder and read:

1. `README.md` for the public-facing explanation.
2. `SKILL.md` for the actual agent instruction.
3. `evals.md` for the pass/fail quality bar.
4. `examples/` for sample prompts.

## Design Principle

A useful agent skill should do three things:

- Encode judgment, not just steps.
- Name failure modes clearly enough to test.
- Stay close to a real workflow someone runs more than once.

## Portfolio Site

The repo is designed to become the backend for a simple portfolio site. Use `skills.json` as the content source and `portfolio-site-prompt.md` as the build brief.
