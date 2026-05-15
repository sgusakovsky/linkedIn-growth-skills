# LinkedIn Growth Skills

Modular agent skills for LinkedIn profile strategy, positioning, content, SSI improvement, competitor research, trend analysis, networking, and analytics review.

Use these skills when you want an agent to act as a LinkedIn strategist, analyst, editor, researcher, and growth operator. The system is intentionally human-in-the-loop: it proposes improvements and drafts, but it does not automate posting, mass messaging, fake engagement, or spam behavior.

## Available Skills

| Skill | Use When |
| --- | --- |
| [LinkedIn Growth Orchestrator](skills/linkedin-growth-orchestrator/) | Selecting the right pipeline of LinkedIn growth skills for a user goal. |
| [LinkedIn Profile Audit](skills/linkedin-profile-audit/) | Reviewing profile sections, keyword clarity, authority signals, and coherence. |
| [LinkedIn Positioning Strategy](skills/linkedin-positioning-strategy/) | Defining professional identity, niche, differentiation, and expertise clusters. |
| [LinkedIn Content Strategy](skills/linkedin-content-strategy/) | Building content pillars, cadence, audience strategy, and discussion strategy. |
| [LinkedIn Post Generator](skills/linkedin-post-generator/) | Drafting authentic, tone-aware LinkedIn posts from real user experience. |
| [LinkedIn Comment Generator](skills/linkedin-comment-generator/) | Drafting useful comments that add insight and develop relationships. |
| [LinkedIn Trend Research](skills/linkedin-trend-research/) | Finding sustainable authority opportunities and professional discussion gaps. |
| [LinkedIn Competitor Analysis](skills/linkedin-competitor-analysis/) | Comparing similar profiles and extracting non-copycat strategic patterns. |
| [LinkedIn Network Growth](skills/linkedin-network-growth/) | Improving connection quality, outreach strategy, and relationship development. |
| [LinkedIn SSI Optimizer](skills/linkedin-ssi-optimizer/) | Improving the four SSI pillars without treating SSI as the final goal. |
| [LinkedIn Analytics Review](skills/linkedin-analytics-review/) | Reviewing historical growth, engagement quality, experiments, and outcomes. |
| [LinkedIn Brand Modeling](skills/linkedin-brand-modeling/) | Modeling clarity, uniqueness, trust signals, and authority perception. |

## Recommended Entry Point

For most users, install all skills and invoke the orchestrator first. The orchestrator is the main entry point: it understands the request, checks shared context, chooses the relevant specialist skills, and aggregates the result.

```text
Use $linkedin-growth-orchestrator to help with my LinkedIn growth request: [describe the task].
```

Use a specialist skill directly only when the task is intentionally narrow.

## Install From GitHub

Repository URL:

```text
https://github.com/sgusakovsky/linkedIn-growth-skills
```

These commands require the current repository contents to be published to GitHub. If the remote repository has not been updated yet, install from a local clone instead.

### Using `ai-agent-skills`

Install every skill from this repository for Claude Code:

```bash
npx ai-agent-skills install https://github.com/sgusakovsky/linkedIn-growth-skills --agent claude
```

Install every skill from this repository for Codex:

```bash
npx ai-agent-skills install https://github.com/sgusakovsky/linkedIn-growth-skills --agent codex
```

Check what would be installed without changing local files:

```bash
npx ai-agent-skills install https://github.com/sgusakovsky/linkedIn-growth-skills --agent claude --dry-run
npx ai-agent-skills install https://github.com/sgusakovsky/linkedIn-growth-skills --agent codex --dry-run
```

Install only the orchestrator:

```bash
npx ai-agent-skills install https://github.com/sgusakovsky/linkedIn-growth-skills --skill linkedin-growth-orchestrator --agent codex
```

### Using `skills`

List available skills without installing:

```bash
npx skills add https://github.com/sgusakovsky/linkedIn-growth-skills --list
```

Install all skills for Codex:

```bash
npx skills add https://github.com/sgusakovsky/linkedIn-growth-skills --skill '*' --agent codex -y
```

Install all skills for every supported local agent:

```bash
npx skills add https://github.com/sgusakovsky/linkedIn-growth-skills --all
```

Install only the orchestrator for Codex:

```bash
npx skills add https://github.com/sgusakovsky/linkedIn-growth-skills --skill linkedin-growth-orchestrator --agent codex -y
```

## Install From A Local Clone

From an existing local clone of this repository:

```bash
npx ai-agent-skills install . --agent codex
npx skills add . --skill '*' --agent codex -y
```

Install one local skill:

```bash
npx ai-agent-skills install ./skills/linkedin-growth-orchestrator --agent codex
npx skills add . --skill linkedin-growth-orchestrator --agent codex -y
```

## Skill Prompt Examples

| Skill | Prompt |
| --- | --- |
| `linkedin-growth-orchestrator` | `Use $linkedin-growth-orchestrator to build a LinkedIn growth plan from my current profile, goals, audience, and analytics.` |
| `linkedin-growth-orchestrator` | `Use $linkedin-growth-orchestrator to improve my LinkedIn SSI while avoiding spam tactics and vanity-metric chasing.` |
| `linkedin-growth-orchestrator` | `Use $linkedin-growth-orchestrator to decide which LinkedIn skills should handle this request: I want more relevant inbound opportunities.` |
| `linkedin-profile-audit` | `Use $linkedin-profile-audit to audit my headline, About section, experience, Featured section, skills, and recommendations.` |
| `linkedin-profile-audit` | `Use $linkedin-profile-audit to identify clarity gaps, weak proof, keyword inconsistency, and missing authority signals in my profile.` |
| `linkedin-positioning-strategy` | `Use $linkedin-positioning-strategy to define a sharper professional identity and positioning statement from my profile and goals.` |
| `linkedin-positioning-strategy` | `Use $linkedin-positioning-strategy to compare several positioning options and explain their trade-offs.` |
| `linkedin-content-strategy` | `Use $linkedin-content-strategy to create content pillars, cadence, audience strategy, and experiments for the next 30 days.` |
| `linkedin-content-strategy` | `Use $linkedin-content-strategy to turn my positioning into a practical LinkedIn editorial plan without generic AI-style posts.` |
| `linkedin-post-generator` | `Use $linkedin-post-generator to draft three LinkedIn posts from these real notes while preserving my tone of voice.` |
| `linkedin-post-generator` | `Use $linkedin-post-generator to rewrite this draft so it sounds more specific, less generic, and still natural for LinkedIn.` |
| `linkedin-comment-generator` | `Use $linkedin-comment-generator to write useful comments for this post that add insight instead of shallow praise.` |
| `linkedin-comment-generator` | `Use $linkedin-comment-generator to draft relationship-building replies that sound human and do not feel automated.` |
| `linkedin-trend-research` | `Use $linkedin-trend-research to identify sustainable authority opportunities in my niche, not just viral topics.` |
| `linkedin-trend-research` | `Use $linkedin-trend-research to find overused topics, emerging themes, and under-discussed professional problems for my audience.` |
| `linkedin-competitor-analysis` | `Use $linkedin-competitor-analysis to compare these benchmark profiles and extract patterns without copying their positioning.` |
| `linkedin-competitor-analysis` | `Use $linkedin-competitor-analysis to find white space where my profile can become more distinct.` |
| `linkedin-network-growth` | `Use $linkedin-network-growth to recommend who I should connect with, how to approach them, and how to develop relationships responsibly.` |
| `linkedin-network-growth` | `Use $linkedin-network-growth to diagnose my network gaps and create a quality-first outreach strategy.` |
| `linkedin-ssi-optimizer` | `Use $linkedin-ssi-optimizer to analyze my four SSI pillars and recommend reputation-safe improvements.` |
| `linkedin-ssi-optimizer` | `Use $linkedin-ssi-optimizer to improve SSI as a supporting metric while keeping business and career outcomes primary.` |
| `linkedin-analytics-review` | `Use $linkedin-analytics-review to compare my recent LinkedIn analytics with the previous period and identify patterns.` |
| `linkedin-analytics-review` | `Use $linkedin-analytics-review to review profile views, search appearances, SSI changes, content performance, and experiment results.` |
| `linkedin-brand-modeling` | `Use $linkedin-brand-modeling to evaluate whether my profile feels clear, credible, differentiated, and human.` |
| `linkedin-brand-modeling` | `Use $linkedin-brand-modeling to identify where my profile risks sounding generic, interchangeable, or AI-generated.` |

## One-Skill Workflow

The simplest workflow is:

1. Install all skills.
2. Start every broad request with `$linkedin-growth-orchestrator`.
3. If no profile is known, the orchestrator asks for the LinkedIn profile URL first.
4. If a profile is already known, the orchestrator asks whether the current task should use that profile.
5. After the active profile is clear, give the orchestrator the available evidence: profile text, goals, audience, tone samples, analytics, SSI, competitors, or draft content.
6. The orchestrator selects the specialist pipeline, reads the relevant shared context, and aggregates the result.
7. The user reviews and approves any profile edits, posts, comments, or outreach.

## Profile Preflight Behavior

The orchestrator always resolves the active profile before profile-specific work:

| Situation | Behavior |
| --- | --- |
| No known profile | Ask for the LinkedIn profile URL before running specialist skills. |
| Known profile exists | Ask the user to confirm whether the task should use that profile. |
| User confirms known profile | Continue with the selected specialist pipeline. |
| User rejects known profile | Ask for the correct LinkedIn profile URL, then ask only for task-critical missing data. |
| New profile URL conflicts with stored context | Ask whether to use the new profile only for this task or replace the active profile. |

If LinkedIn content cannot be accessed from a URL alone, the orchestrator asks for profile text, screenshots, or exported details instead of inventing missing information.

For example:

```text
Use $linkedin-growth-orchestrator.

Goal: improve my LinkedIn visibility and inbound opportunities.
Evidence: here is my headline, About section, recent post analytics, target audience, and writing samples.
Constraints: no spam, no fake stories, no automated posting.
```

## System Design

The repository is split into:

- `skills/`: installable agent skills with narrow responsibilities.
- `core/`: reusable decision rules, schemas, evaluation criteria, and operating constraints.
- `shared-context/`: portable JSON context shapes for profile, audience, goals, positioning, analytics, tone, and SSI history.
- `personas/`: profession-sensitive strategy defaults that can be selected or blended.
- `templates/`: report and planning templates used by skills.
- `examples/`: sanitized examples showing expected output shape.

## Operating Boundaries

The skills are designed to:

- use user-provided evidence before making recommendations;
- separate verified facts from assumptions;
- avoid hardcoded personal data or profession-specific defaults;
- preserve authentic voice and domain specificity;
- evaluate long-term authority, trust, and outcomes, not only vanity metrics.

The skills must not:

- mass message, auto-post, or spam comment;
- clone competitor profiles;
- invent metrics, analytics, experience, or personal stories;
- optimize SSI at the expense of reputation or trust.
