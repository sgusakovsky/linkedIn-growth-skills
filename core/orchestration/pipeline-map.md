# Orchestration Pipeline Map

Use this reference when a task spans more than one skill. Select the smallest pipeline that can answer the user request.

## Pipeline Rules

- Start with user intent, not the list of available skills.
- Treat `linkedin-growth-orchestrator` as the default entry point for broad or ambiguous requests.
- Run profile preflight before specialist execution: if no profile is known, ask for the LinkedIn profile URL; if a profile is already known, ask the user to confirm it is the right profile for the current task.
- Prefer existing shared context before asking for new input.
- Ask only for missing evidence that materially changes the recommendation.
- Do not run competitor, trend, analytics, or SSI work unless the user goal requires it.
- Load peer skill instructions when the orchestrator is handling a request on behalf of specialist skills.
- Aggregate outputs into one recommendation set with conflicts resolved explicitly.
- Keep the user in review control for profile edits, posts, comments, and outreach.

## Intent Routing

| User Intent | Primary Pipeline | Usually Skip |
| --- | --- | --- |
| Improve SSI | profile-audit, network-growth, ssi-optimizer, content-strategy | competitor-analysis unless benchmarking is requested |
| Rewrite profile | profile-audit, positioning-strategy, brand-modeling | trend-research unless niche direction is unclear |
| Build content plan | positioning-strategy, content-strategy, trend-research, brand-modeling | network-growth unless relationship goals are central |
| Draft post | post-generator, authenticity review from core, optional content-strategy | analytics-review unless performance history is provided |
| Draft comments | comment-generator, network-growth if relationship targeting matters | profile-audit |
| Analyze competitors | competitor-analysis, positioning-strategy, brand-modeling | post-generator |
| Review performance | analytics-review, content-strategy, ssi-optimizer if SSI data exists | competitor-analysis unless comparison is needed |
| Full growth review | profile-audit, positioning-strategy, brand-modeling, content-strategy, network-growth, ssi-optimizer, analytics-review, optional trend-research and competitor-analysis | post-generator and comment-generator unless drafting is requested |

## Output Contract

Every orchestrated result should include:

- verified facts used;
- assumptions made;
- selected pipeline;
- skipped skills and why;
- consolidated recommendation;
- next human review step;
- data needed for better confidence.
