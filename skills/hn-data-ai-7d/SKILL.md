---
name: hn-data-ai-7d
description: Analyze Hacker News threads from the last 7 days about data and AI in databases (SQL/NoSQL engines, analytics stores, vector/embedding search, RAG pipelines, ML-in-DB). Use when asked to summarize, rank, or report on recent HN discussions about database+AI topics, or to extract insights from HN comment threads.
---

# HN Data + AI 7D

## Overview
Analyze the most recent 7 days of HN discussion in the data+AI database space and produce a ranked, insight-driven report based on thread activity and comment content.

## Workflow

1. Confirm scope and ranking
   - Default to data+AI database topics only.
   - If ranking is not specified, default to most-discussed (by comment count) and report top 10.
   - Ask for keyword tweaks only if the user suggests additions or exclusions.

2. Build the HNRSS RSS query
   - Prefer RSS because JSONfeed is often blocked.
   - Use the user-provided URL if given; otherwise use a template like:
     https://hnrss.org/newest?q=database+OR+postgres+OR+postgresql+OR+sqlite+OR+duckdb+OR+clickhouse+OR+snowflake+OR+bigquery+OR+mongodb+OR+redis+OR+vector+OR+rag+OR+embedding&count=100&search_attrs=title,url&link=comments
   - Always include link=comments so item links go to HN discussion pages.

3. Fetch and filter
   - Use web.run to fetch the RSS feed.
   - Filter items to the last 7 days using UTC and cite the exact date window (include absolute dates).
   - Drop items that are not clearly data+AI database related.

4. Rank by discussion
   - For each candidate item, open the HN comments page and extract the comment count ("X comments").
   - If comment count is missing, mark it as unknown and rank lower.

5. Summarize thread insights
   - Read the top threads and capture the main arguments, tradeoffs, benchmarks, adoption signals, and open questions.
   - Keep the focus on data+AI implications (systems design, performance, costs, governance, reliability, MLOps/RAG impact).

## Output format

- Time window (UTC) and methodology
- Top threads table: title, HN link, date, comment count, topic tag
- Key insights: 5-10 bullets derived from the most-discussed threads
- Optional: noteworthy dissenting views or unresolved debates

## Guardrails

- Always use web.run for freshness; do not rely on memory.
- If the feed URL is not accessible, ask the user for the RSS URL in their message.
- Stay within data+AI domains only; exclude unrelated HN topics.

## Access methods tried (and fallbacks)

- HNRSS RSS (preferred): works when reachable; JSONfeed is often blocked or 400.
- Algolia API: often blocked/400 in this environment; avoid unless the user insists.
- hackernewsrss.com feed: sometimes accessible, but less reliable than HNRSS.
- HN frontpage daily snapshots (fallback): use `https://news.ycombinator.com/front?day=YYYY-MM-DD` for each day in the 7-day window, then open each item’s comments page to get counts and discussion.

## Best practices

- Use the last 7 full UTC days and always cite the exact date range.
- Prefer HNRSS RSS; only fall back to HN daily snapshots when RSS is blocked.
- De-duplicate by canonical HN item URL; if the same story appears multiple days, keep the most active thread.
- Rank by comment count; if missing, mark unknown and de-prioritize.
- Keep the scope strictly data+AI database topics; exclude unrelated posts.
- Emphasize insights: extract tradeoffs, adoption signals, performance/cost claims, and open questions from top threads.
