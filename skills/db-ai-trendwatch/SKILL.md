---
name: db-ai-trendwatch
description: Monitor and analyze AI support trends in the database industry. Use when asked to track, summarize, or compare AI capabilities (copilots, NL2SQL, vector search, RAG, multimodal retrieval, full-text search, graph/knowledge graph support, ML-in-database, governance AI) across sources such as Databricks, Snowflake, Microsoft Fabric/Azure, Google/BigQuery, Airbnb, Pinterest, IDC, Gartner, Bloomberg, ACM, VLDB, Medium, and cloud/data leader blogs or updates.
---

# DB AI Trendwatch

## Overview
Track and analyze signals of AI capability support in databases and data platforms. Produce concise briefs, competitor snapshots, or deep dives grounded in primary sources (docs, release notes, pricing) with explicit GA/preview status and availability constraints.

## Workflow

### 1) Scope and output
- Ask for time range (default: last 30 days), geography, and target segments (warehouse, lakehouse, vector DB, query engines, governance).
- Use the default watchlist in `references/watchlist.md`, then ask the user to add/remove companies or people.
- Confirm the deliverable format: weekly brief, competitor matrix, or deep dive.

### 2) Build a source map
- Use `references/source-map.md`.
- For each item in `references/watchlist.md`, collect primary docs, release notes, and engineering blogs.
- Prioritize: product docs and release notes > pricing/entitlements > engineering blogs > analyst reports > media > social.
- For each company, capture: docs, release notes, pricing pages, roadmap/preview notes, and public GitHub release tags (if any).

### 3) Collect signals
- Use web browsing for up-to-date information.
- Log each signal with: date, source, feature, status (GA/preview), region/SKU constraints, and evidence link.
- Use `references/query-playbook.md` for targeted queries.

### 4) Validate and classify
- Use `references/evidence-matrix.md` to classify strength.
- Require at least two independent confirmations for GA/adoption claims.
- If only a blog/PR exists, mark as announcement and note missing evidence.

### 5) Analyze impact
- Map each signal to the AI capability taxonomy (copilot, NL2SQL, vector search, RAG, multimodal retrieval, full-text search, graph/knowledge graph, model serving, governance).
- Assess adoption readiness (availability, pricing, constraints) and strategic impact (moat, differentiation, switching cost).

### 6) Produce the output
- Use `references/output-templates.md`.
- Always include: what changed, why it matters, who is ahead/behind, risks, and a watch list.

## Calibration with real cases
- Read `references/case-library.md` to align on strong vs weak signals and common failure modes.
- When a new signal resembles a case, reuse the evaluation pattern and language.

## Guardrails (do / do not)
- Do check GA/preview, region/SKU constraints, and pricing.
- Do triangulate with docs or release notes.
- Do separate announcement noise from measurable adoption signals.
- Do not treat preview as GA.
- Do not assume availability is global or immediate.
- Do not rely on a single marketing blog for conclusions.

## Evidence log format
Use this minimal table for each update:

| Date | Source | Company | Feature | Status | Availability | Evidence |
|------|--------|---------|---------|--------|--------------|----------|

## When to ask the user
- Missing scope, target companies, or output format.
- The default watchlist is not desired or needs prioritization by region/segment.
- Paywalled sources (IDC, Gartner, Bloomberg) are required but access is unclear.
