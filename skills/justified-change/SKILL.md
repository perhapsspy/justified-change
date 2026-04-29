---
name: justified-change
description: Use for non-trivial code changes to keep implementation, bug fixes, refactors, and review edits proportional to the goal, justified by constraints, and verified without speculative scope
license: MIT
metadata:
  author: perhapsspy@gmail.com
  version: '0.1'
  source_repository: https://github.com/perhapsspy/justified-change
---

# Skill: Justified Change

## Purpose

Keep code changes proportional to the requested goal, justified by evidence or constraints, and verifiable.

The purpose is not to make every change as small as possible.
Do the work required to satisfy the goal, including direct follow-up updates, but keep the scope explainable.

## Use / Do Not Use

- Use before non-trivial implementation, bug fix, refactor, or code review edits.
- Use when the change could expand into speculative work, broad cleanup, or unnecessary rewrites.
- Use when necessary follow-up changes could be missed by making the edit too narrow.
- Use when ambiguity affects implementation choices.
- Do not use for trivial typo fixes or obvious one-line edits where the review cost is higher than the risk.
- Do not use as a replacement for project-specific build, test, style, or repository instructions.

## Operating Flow

For a non-trivial change, keep this frame small but explicit:

1. State the goal and observable success criteria.
2. Identify the direct impact area: implementation, call sites, types, tests, documentation, and configuration that must change together.
3. Name any implementation-affecting assumptions or questions.
4. Edit only what the goal, success criteria, or direct impact area justifies.
5. Verify at the smallest level that still protects the behavior.
6. Report the scope rationale and verification result briefly.

Do not turn this into a long ritual for routine work. The frame should clarify the change, not become the work.

## Core Rules

1. **Fix Goal and Success Criteria**

- State the change goal in one sentence.
- Define success criteria before editing.
- Prefer observable success criteria: reproduced failure, passing test, type/lint check, behavior check, or explicit requirement satisfied.
- Include direct follow-up changes required to satisfy the goal.
- Do not skip necessary call-site, type, test, documentation, or configuration updates when they are directly affected.

2. **Justify Scope**

- Set the scope to what is sufficient and proportional for the goal, not to the fewest possible edits.
- Every major change should be explainable by the user request, success criteria, or existing code constraints.
- Keep direct impact areas in scope.
- Treat a surface as directly affected when leaving it unchanged would break the requested behavior, type/check, documentation/configuration contract, or meaningful verification.
- Nearby inconsistency, old naming, or general cleanup opportunity is not enough to include a surface.
- Keep unrelated cleanup, polish, and improvements out of the change.
- Mention unrelated cleanup opportunities separately instead of applying them.

3. **Surface Assumptions**

- State implementation-affecting assumptions before changing code.
- If ambiguity affects public API, architecture, data loss, security, dependencies, cost, or migration path, ask before changing code.
- For minor local ambiguity, state a reasonable assumption and continue.
- In non-interactive runs, choose a reversible assumption and report it in the result.

4. **Limit Speculative Work**

- Do not add features, options, parameters, configuration, dependencies, or abstractions only because they may be useful later.
- Do not perform unrelated refactors, formatting changes, comment rewrites, or naming changes.
- Remove pre-existing dead code only when it is directly connected to the current goal or blocks verification.
- Clean up imports, variables, functions, or files made unused by the current change.

5. **Verify Appropriately**

- Match verification to the risk and nature of the change.
- For bug fixes, prefer a failing reproduction or characterization check before the fix.
- For refactors, verify behavior that should remain stable before and after the change.
- For feature changes, verify success, failure, and relevant boundary cases.
- If verification cannot be run, state why and name the next useful check.

## Anti-Patterns

- Omitting necessary call-site, type, or test updates to make the change look smaller.
- Cleaning up broader files or modules beyond the requested goal.
- Adding future-proof options, parameters, configuration, dependencies, or abstractions.
- Reorganizing structure or renaming things without a direct reason.
- Folding pre-existing dead-code cleanup into an unrelated change.
- Ending with “seems fixed” without a verification basis.
- Changing multiple possible causes at once without narrowing the failure.
- Leaving a diff whose major changes cannot be explained.

## Final Check

- Is the goal clear?
- Are the success criteria clear enough to evaluate the change?
- Were necessary direct follow-up changes included?
- Can every major change be explained by the goal, success criteria, or existing code constraints?
- Were unrelated cleanup and improvements kept separate?
- Were speculative features, options, configuration, dependencies, or abstractions avoided?
- Was verification matched to the change, or was the reason for deferring it stated?

## Completion Evidence

Use only when useful:

- `Goal:` change goal
- `Success Criteria:` observable success criteria
- `Scope Rationale:` why the touched scope is necessary and proportional
- `Assumptions:` implementation-affecting assumptions
- `Verification:` checks run, failed, skipped, or deferred with reason
- `Deferred:` related cleanup or follow-up work not mixed into this change
