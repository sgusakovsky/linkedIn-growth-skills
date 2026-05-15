# Profile Preflight

Use this preflight before executing any LinkedIn growth task through the orchestrator.

## Scenario A: No Known Profile

If shared context does not contain a usable `profile.profileUrl` and the user did not provide a profile URL in the current request:

1. Stop before running specialist skills.
2. Ask the user for their LinkedIn profile URL.
3. Ask only for task-critical missing data after the URL is provided.
4. Do not assume profession, industry, goals, audience, geography, language, or tone.

Minimum first question:

```text
Please send the LinkedIn profile URL I should work with.
```

If the request cannot be handled from URL alone, ask concise follow-up questions for the missing evidence, such as:

- primary goal;
- target audience;
- current profile text or screenshots if the agent cannot access the page;
- SSI or analytics values;
- writing samples;
- competitors or benchmark profiles.

## Scenario B: Known Profile Exists

If shared context contains a usable `profile.profileUrl` or the current conversation already has profile data:

1. Stop before running specialist skills.
2. Ask the user to confirm whether the task should use that profile.
3. Include the known URL or profile identifier in the confirmation question.
4. If the user confirms, continue with the selected pipeline.
5. If the user says no or provides another profile, switch to Scenario A for the new profile and request missing data.

Confirmation question:

```text
I have an existing LinkedIn profile in context: [profile URL or identifier]. Should I use this profile for the current task?
```

## Scenario C: User Provided A New Profile In The Request

If the user provides a profile URL in the current request:

1. Treat it as the active profile for this task.
2. If it conflicts with stored context, state the conflict and ask whether to replace or use the new profile for this task only.
3. Continue only after the active profile is clear.

## Missing Data Rule

Ask for missing data only when it materially affects the requested outcome. Do not block simple tasks with a full onboarding form.

Examples:

- Profile audit needs profile text, screenshots, or accessible profile evidence.
- SSI optimization needs current SSI or pillar scores if the user wants SSI-specific diagnosis.
- Analytics review needs baseline and current period metrics.
- Post generation needs topic notes and, for higher confidence, writing samples.
- Competitor analysis needs competitor or benchmark profiles.
