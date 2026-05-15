# Memory Schema

The memory layer stores historical state so recommendations can improve over time. It must not be treated as verified truth unless the source and date are known.

## Store

- profile snapshots;
- positioning decisions;
- previous posts and comments;
- rejected strategies;
- content experiments;
- engagement history;
- SSI history;
- network activity summaries;
- competitor and trend observations;
- user feedback on drafts.

## Required Fields

Each memory item should include:

- `id`: stable identifier;
- `type`: profile_snapshot, post, comment, recommendation, experiment, analytics, ssi, network, competitor, trend, feedback;
- `date`: ISO date when captured or created;
- `source`: user_provided, linkedin_export, manual_note, analytics_report, agent_inference;
- `confidence`: high, medium, low;
- `content`: structured payload or text;
- `decision`: accepted, rejected, pending, informational;
- `notes`: optional explanation.

## Rules

- Never overwrite historical records without preserving prior state.
- Mark inferred items as inference.
- Do not store private credentials or session tokens.
- Do not turn memory into an automation queue.
- Use rejected strategies to avoid repeating advice.
