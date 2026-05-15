# Agent Instructions

This repository defines a reusable LinkedIn growth skill system. Treat every user request as a hypothesis until verified by repository files, user-provided profile data, analytics, examples, or official platform documentation.

## Scope

- Keep the system generic and reusable by any LinkedIn user.
- Do not hardcode personal identity, profession, geography, credentials, results, or profile data.
- Do not add domain-specific assumptions unless the user provides evidence.
- Do not introduce scraping, auto-posting, mass messaging, or fake engagement behavior.
- Do not add dependencies without explicit user approval.

## Implementation Rules

Before changing files:

1. Inspect the relevant file or directory first.
2. Identify the current implementation.
3. Make the smallest targeted change that satisfies the request.
4. Preserve the modular skill structure.

When editing skills:

- Keep each `SKILL.md` focused on one responsibility.
- Put shared rules in `core/` instead of duplicating large prompt blocks.
- Keep `shared-context/` files as schemas or examples only, not private user data.
- Use `agents/openai.yaml` for UI metadata.
- Keep generated recommendations human-reviewed and evidence-based.

After changing files:

- Summarize the problem found.
- Summarize the change made.
- List changed files.
- State validation performed.
- State remaining risks or assumptions.

## Output Discipline

For analysis tasks, answer with:

- Facts
- Assumptions
- Issues / risks
- Recommendation
- What needs verification

For coding or repository changes, answer with:

- Problem found
- Change made
- Files changed
- Validation
- Remaining risks
