# CLAUDE.md

## Universal Execution Rules

### Think Before Coding
- State assumptions explicitly before implementing.
- If multiple interpretations exist, present all options. Do not pick silently.
- If a simpler approach exists, say so. Push back when warranted.
- If something is unclear, stop. Name what is confusing. Ask.

### Simplicity First
- Minimum code that solves the problem. Nothing speculative.
- No features beyond what was asked.
- No abstractions for single-use code.
- No "flexibility" or "configurability" that was not requested.
- No error handling for impossible scenarios.
- If you write 200 lines and it could be 50, rewrite it.

### Surgical Changes
- Touch only what the prompt requires.
- Do not "improve" adjacent code, comments, or formatting.
- Do not refactor things that are not broken.
- Match existing style, even if you would do it differently.
- If your changes create orphaned imports/variables/functions, remove them.
- If you notice unrelated dead code, mention it. Do not delete it.
- Every changed line must trace directly to the prompt.

### Goal-Driven Execution
- Transform every task into verifiable goals with success criteria.
- For multi-step tasks, state a brief plan with verification checks.
- Loop until success criteria are met. Do not stop at "should work."

## Workflow Rules
- All prompts originate from Claude Chat. Execute exactly what is prompted.
- Every task must end with: git add -A && git commit -m "<descriptive message>" && git push
- Do not refactor code that was not part of the prompt.
- Do not rename files, restructure directories, or update dependencies unless explicitly asked.
- If a prompt is ambiguous, stop and ask. Do not guess.
- If a task will break existing functionality, say so before proceeding.
- No placeholder solutions. No "TODO" comments. No "good enough for now." Build the real thing.

## Code Style
- No console.log left behind unless explicitly part of the feature.
- No commented-out code in commits.
- Commit messages must be specific. Not "fix bug" or "update file." Describe what changed and why.

---
