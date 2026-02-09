# HN Data + AI 7D Skill

Analyze Hacker News threads from the last 7 days about data + AI in the database
ecosystem (SQL/NoSQL engines, analytics stores, vector/embedding search, RAG
pipelines, ML-in-DB). Produces a ranked, insight-driven report based on thread
activity and comment content.

## Scope

- Focus strictly on data + AI database topics.
- Exclude unrelated HN posts.

## Access methods (in priority order)

1. HNRSS RSS (preferred).
2. HN frontpage daily snapshots: `https://news.ycombinator.com/front?day=YYYY-MM-DD`.

## Best practices

- Use the last 7 full UTC days and cite the exact date range.
- De-duplicate by canonical HN item URL; keep the most active thread.
- Rank by comment count; if missing, mark unknown and de-prioritize.
- Emphasize insights: tradeoffs, adoption signals, performance/cost claims, and
  open questions.

## Usage

1. Place this folder under `$CODEX_HOME/skills/hn-data-ai-7d`.
2. In Codex, invoke the skill by name and provide a workable HN URL for the
   7-day window if RSS access is blocked.

## License

MIT. See `LICENSE`.
