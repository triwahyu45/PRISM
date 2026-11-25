---
name: karpathy-coding-discipline
description: Behavioral engineering guidelines derived from Andrej Karpathy's LLM coding principles (Think Before Coding, Simplicity First, Surgical Changes, Goal-Driven Execution). Use on non-trivial coding, refactoring, debugging, or architecture tasks to prevent over-engineering and silent assumptions.
---

# Karpathy Coding Discipline

High-precision behavioral rules that eliminate silent assumptions, speculative over-engineering, and collateral edits during coding tasks.

---

## 1. Think Before Coding

**Don't assume. Don't hide confusion. Surface tradeoffs.**

- State assumptions explicitly before writing code.
- If multiple valid interpretations exist, present them concisely instead of guessing silently.
- If a simpler approach exists, propose it first and push back on unnecessary complexity.
- If requirements are ambiguous, stop and ask rather than inventing behavior.

---

## 2. Simplicity First

**Minimum code that solves the problem. Nothing speculative.**

- Write zero features beyond what was asked.
- Avoid single-use abstractions, premature factories, or unrequested configurability.
- Skip error handling for impossible internal scenarios; validate only at real external boundaries.
- If 200 lines can be written cleanly in 50, rewrite it to 50.

---

## 3. Surgical Changes

**Touch only what you must. Clean up only your own mess.**

- Do not "improve" or reformat adjacent working code unrelated to the task.
- Match the repository's existing conventions even if you prefer another style.
- Remove unused imports, variables, or helpers **only** when your own edit orphaned them; flag pre-existing dead code instead of deleting it unasked.
- Every changed line in the diff should trace directly to the user's request.

---

## 4. Goal-Driven Execution

**Define verifiable success criteria, then loop until proven.**

- Convert vague goals into concrete checks:
  - *"Add validation"* -> write tests for invalid inputs and make them pass.
  - *"Fix the bug"* -> write a failing reproduction test, fix root cause, verify pass.
  - *"Refactor X"* -> run existing test suite before and after with zero regressions.
