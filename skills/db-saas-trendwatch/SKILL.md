---
name: db-saas-trendwatch
description: Monitor and analyze trends in how SaaS products use databases (multi-tenant patterns, scaling, cost, reliability, migrations, analytics/search/AI) across SaaS vendors, cloud providers, and database ecosystems.
---

# DB SaaS Trendwatch

## Overview
Track and analyze signals about how SaaS products design, operate, and evolve their database stacks. Focus on architecture choices, scale, cost, reliability, and migration patterns. Produce concise briefs, pattern maps, or deep dives grounded in primary sources.

## Workflow

### 1) Scope and output
- Ask for time range (default: last 90 days), geography, SaaS segment (B2B/B2C, verticals), and product stage.
- Ask which database layers to focus on: OLTP, OLAP, search, vector, cache, streaming.
- Confirm output format: weekly brief, pattern map, competitor matrix, or deep dive case study.
- Use the default watchlist in `references/watchlist.md`, then ask the user to add/remove companies.

### 2) Case-first analysis (gold + failure cases)
- Collect 3-5 "gold" cases (best-in-class architecture or migrations) and 3-5 failure cases (incidents, cost blowups, scaling bottlenecks).
- Use primary sources: engineering blogs, postmortems, migration retrospectives, architecture talks.
- For each case, record: context, decision, outcome, what worked, what failed, and measurable impact.
- Summarize patterns as "do this / avoid this" with evidence.

### 3) Build a source map
- Use `references/source-map.md`.
- Prioritize: engineering blogs and docs > release notes > incident reports > conference talks > media/analyst.
- Capture for each company: architecture posts, reliability incidents, pricing/SLA changes, and migration writeups.

### 4) Collect signals
- Log signals with: date, source, company, capability, status, and evidence link.
- Signal types:
  - Tenancy model (shared, siloed, hybrid)
  - Sharding/partitioning strategy
  - Storage engine changes (row/column/LSM)
  - Search and vector support inside SaaS products
  - Data residency and compliance controls
  - Cost optimization (tiering, compression, reserved capacity)
  - Reliability (RPO/RTO, multi-region, failover)
  - Migration and consolidation events

### 5) Validate and classify
- Use `references/evidence-matrix.md` to classify strength.
- Require at least two independent confirmations for GA or production claims.
- If only a blog post exists, mark as announcement or anecdotal.

### 6) Analyze impact
- Map signals to the taxonomy in `references/taxonomy.md`.
- Highlight patterns across SaaS segments (SaaS verticals, consumer SaaS, infra SaaS).
- Compare cost/reliability tradeoffs and migration drivers.

### 7) Produce the output
- Use `references/output-templates.md`.
- Always include: what changed, why it matters, leaders/laggards, risks, and a watch list.

## Evidence log format
Use this minimal table for each update:

| Date | Source | Company | Capability | Status | Impact | Evidence |
|------|--------|---------|------------|--------|--------|----------|

## Guardrails (do / do not)
- Do separate product marketing from engineering reality.
- Do cite primary sources for architecture or reliability claims.
- Do flag paywalled sources as unavailable if access is missing.
- Do not treat rumor or hiring posts as confirmed architecture changes.
- Do not extrapolate a single incident into a global trend.

## When to ask the user
- Missing scope, target SaaS segments, or output format.
- The default watchlist is not desired or needs prioritization.
- Paywalled sources are required but access is unclear.
