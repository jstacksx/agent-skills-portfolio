---
name: question-discipline
description: Use when the user wants to ask better questions, find the eigenquestion, pressure-test a question list, decide what to ask in a meeting or interview, improve discovery questions, or design questions that sharpen a decision.
metadata:
  short-description: Find the highest-leverage question
---

# Question Discipline

Use this skill when the question itself is the work. The goal is to help the user ask fewer, sharper questions that reveal the real constraint, decision standard, tradeoff, owner, timing, or next move.

## Context To Load

- Load any relevant memory, resources, or connected-app context when the question depends on a specific deal, interview, meeting, company, thread, or document.
- Do not ask the user for background that can be found in available context.
- For written questions the user will send or ask live, use any available voice or style guidance.

## Workflow

1. **Name the decision**
   - State what the questions are meant to unlock: a decision, diagnosis, strategy, meeting outcome, interview signal, or next action.
   - If the real decision is buried, say so and infer the strongest useful version.

2. **Find the eigenquestion**
   - List the candidate question themes.
   - Identify the one question that would change the most downstream decisions if answered.
   - If two dimensions are needed, use the two-question constraint and explain the map they create.

3. **Rank for leverage**
   - Keep questions that change recommendation, scope, sequencing, owner, timing, or risk.
   - Cut questions that are merely interesting, vague, answerable from available context, or likely to produce generic answers.

4. **Write questions in Jann's voice**
   - Make each question direct, specific, and commercially sharp.
   - Avoid throat-clearing, performative curiosity, consultant language, and multi-part sprawl.
   - For live meetings, make questions easy to say out loud.

5. **Give the operating move**
   - Tell the user what to ask first, what to hold for later, and what answer pattern would change the plan.

## Default Output

Use this structure unless the user asks for another format:

```markdown
**Eigenquestion**
[One question.]

**Why This Unlocks the Work**
[One to three lines on the decisions it drives.]

**Ranked Questions**
1. [Highest-leverage question.]
2. [Next question.]
3. [Next question.]

**Cut**
- [Question or topic to skip, with a short reason.]

**Sharper Ask**
[The clean version the user can use live or in writing.]
```

## Use-Case Notes

- **Founder / advisory calls:** Prioritize questions that reveal founder goals, real alternatives, urgency, buyer fit, process readiness, and what must be true for a transaction or partnership to be worth pursuing.
- **Corp Dev interviews:** Prioritize questions that reveal the company's strategic constraint, operating cadence, executive decision standard, build/buy/partner posture, and where the role can create leverage.
- **Decision memos:** Prioritize questions that test the load-bearing assumption, the opposing case, the missing proof, and the execution owner.
- **Meeting prep:** Prioritize questions that create alignment, surface objections, force specificity, or turn discussion into an owner, action, timing, or decision.

## Quality Check

Before finalizing, confirm:

- The eigenquestion would materially change downstream decisions.
- The ranked questions are not answerable from loaded context.
- The list is shorter and sharper than the user's starting set.
- Each question has a clear decision purpose.
- The language sounds specific and usable, not like a generic discovery script.

## Approval Boundary

This skill produces question strategy and draft questions only. Do not send messages, update trackers, store coaching results, or make durable workflow changes unless the user explicitly asks.

## Continuous Improvement

- Before materially changing this skill, test it manually on 2-3 realistic prompts.
- Use `evals.md` as the pass/fail self-check after meaningful runs or edits.
- Use a separate clean-context reviewer agent for evals when available; send failed checks back for revision until they pass or a blocker is clear.
- Add one-sentence learnings to `memory.md` when feedback should improve future uses and does not belong in the pass/fail evals.
