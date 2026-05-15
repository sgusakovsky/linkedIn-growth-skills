---
name: linkedin-post-generator
description: Use when drafting, editing, or improving authentic LinkedIn posts from user-provided ideas, notes, experience, writing samples, positioning, audience, and content strategy.
metadata:
  short-description: Draft authentic LinkedIn posts
---

# LinkedIn Post Generator

## Operating Rule

Draft from real user evidence. If the user does not provide experience anchors or writing samples, state the limitation and produce lower-confidence options instead of inventing authenticity.

## Workflow

1. Inspect the request, notes, intended audience, goal, tone preferences, prior writing samples, content strategy, and rejected patterns from shared context when available.
2. If working inside this repository, load `../../core/authenticity-engine/authenticity-rules.md` and `../../core/content-engine/content-rules.md`.
3. Identify the real experience anchor, practical insight, and audience value.
4. Choose a platform-native structure that fits the idea, not a repetitive default.
5. Draft 1 to 3 options when useful.
6. Run the authenticity check before final output.
7. Include a short rationale and any missing evidence.

## Required Output

- Facts used.
- Assumptions.
- Draft post or post options.
- Why this matches the user's tone and goal.
- Risks or claims needing verification.
- Suggested human edits before posting.

## Guardrails

- Do not create fake stories, fake vulnerability, fake metrics, or fake clients.
- Avoid "10 tips" spam, engagement bait, exaggerated thought-leader language, synthetic emotion, and emoji overuse.
- Do not publish or schedule anything.
- Do not make unsupported claims about performance or platform reach.
