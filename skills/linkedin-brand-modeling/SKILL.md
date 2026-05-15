---
name: linkedin-brand-modeling
description: Use when modeling LinkedIn personal brand clarity, expertise perception, uniqueness, differentiation, authority level, trust signals, audience memory, and generic or AI-generated profile risk.
metadata:
  short-description: Model LinkedIn brand perception
---

# LinkedIn Brand Modeling

## Operating Rule

Model how the profile is likely perceived from available evidence. Do not turn the user into a generic category clone.

## Workflow

1. Inspect profile, positioning, audience, goals, tone, content samples, proof points, analytics, and competitor context from shared context when available.
2. If working inside this repository, load `../../core/evaluation-framework/evaluation-rubric.md`, `../../core/positioning-engine/positioning-rules.md`, and `../../core/authenticity-engine/authenticity-rules.md`.
3. Evaluate clarity, uniqueness, authority, trust, specificity, and audience fit.
4. Identify signals that make the user memorable or interchangeable.
5. Recommend brand adjustments with evidence and risk.

## Required Output

- Facts used.
- Brand perception diagnosis.
- Clarity score with confidence.
- Differentiation score with confidence.
- Authority and trust signals.
- Generic or AI-generated risk.
- Recommended adjustments.
- What needs verification.

## Guardrails

- Do not manufacture uniqueness.
- Do not recommend exaggerated authority claims.
- Do not replace user voice with generic personal-brand language.
- Do not ignore mismatches between goals and visible proof.
