# DB AI Trend Brief (2026-02-08)

Scope: last 30 days (2026-01-09 to 2026-02-08), global. Paywalled IDC/Gartner/Bloomberg/WSJ/FT/The Information content excluded.

## Executive summary
- AI-ready platforms are concentrating on assistant + governance + data-residency controls (Snowflake Cortex Code + AI_COUNT_TOKENS; BigQuery conversational analytics + Gemini data-residency; Databricks Knowledge Assistant + MCP). 
  - Snowflake Cortex Code CLI GA: https://docs.snowflake.com/en/release-notes/2026/other/2026-02-02-cortex-code-cli
  - Snowflake AI_COUNT_TOKENS GA: https://docs.snowflake.com/en/release-notes/2026/other/2026-01-27-ai-count-tokens-function-ga.html
  - BigQuery release notes (Gemini + conversational analytics): https://cloud.google.com/bigquery/docs/release-notes
  - Databricks Jan 2026 release notes (Knowledge Assistant + MCP): https://docs.databricks.com/aws/en/release-notes/product/2026/january
- AI-native vendors are moving up-stack into built-in embedding/reranking and managed models (Zilliz) while vector search infra improves operational controls (Pinecone). 
  - Zilliz changelogs: https://docs.zilliz.com/docs/changelogs
  - Pinecone release notes 2026: https://docs.pinecone.io/release-notes/2026
- Full-text search stacks continue blending lexical + neural + vector, and graph DBs maintain rapid release cadence (OpenSearch hybrid search; Elastic DiskBBQ; Neo4j 2026.01.3). 
  - OpenSearch hybrid search: https://aws.amazon.com/about-aws/whats-new/2025/08/amazon-opensearch-serverless-ai-connectors-hybrid-search/
  - Elastic DiskBBQ: https://ir.elastic.co/news/news-details/2025/Elastic-Introduces-New-Vector-Storage-Format-DiskBBQ-for-More-Efficient-Vector-Search/default.aspx
  - Neo4j release notes: https://neo4j.com/release-notes/
- Pinterest provides two strong peer signals: a new CDC-based ingestion framework (AI-ready data freshness) and a multimodal AI pipeline (AI-native search). 
  - Pinterest CDC ingestion: https://medium.com/pinterest-engineering/next-generation-db-ingestion-at-pinterest-66844b7153b7
  - Pinterest PinLanding multimodal pipeline: https://medium.com/pinterest-engineering/pinlanding-turn-billions-of-products-into-instant-shopping-collections-with-multimodal-ai-3489320294e9

## Top signals (recent, high-confidence)
- Snowflake expanded AI-assistant tooling: Cortex Code CLI is GA and Cortex Code in Snowsight is in Preview; AI_COUNT_TOKENS is GA.
  - https://docs.snowflake.com/en/release-notes/2026/other/2026-02-02-cortex-code-cli
  - https://docs.snowflake.com/en/release-notes/2026/other/2026-02-02-cortex-code-snowsight
  - https://docs.snowflake.com/en/release-notes/2026/other/2026-01-27-ai-count-tokens-function-ga.html
- Databricks: Knowledge Assistant is GA in select regions, Managed MCP Servers are Public Preview, and GPT-5.1 Codex models are available via Mosaic AI Model Serving.
  - https://docs.databricks.com/aws/en/release-notes/product/2026/january
- BigQuery: conversational analysis is Preview; Gemini Cloud Assist features updated; Gemini in BigQuery supports US/EU data-jurisdiction processing; column-level data policies are GA.
  - https://cloud.google.com/bigquery/docs/release-notes
- Zilliz Cloud (Milvus 2.6.x) introduced model-based embedding/reranking functions (Public Preview), hosted models (Private Preview), semantic/lexical highlighters, and primary-key ANN search in January 2026.
  - https://docs.zilliz.com/docs/changelogs
- Qdrant Cloud Inference integrates embedding generation with vector search and supports multimodal (text+image) and hybrid search in a single API.
  - https://qdrant.tech/blog/qdrant-cloud-inference-launch/

## Last-30-days AI-ready signals (platforms)
- Databricks: Knowledge Assistant GA in select US regions; Managed MCP servers in Public Preview; GPT-5.1 Codex Max/Mini available via Model Serving.
  - https://docs.databricks.com/aws/en/release-notes/product/2026/january
- Snowflake: Cortex Code CLI GA; Cortex Code in Snowsight Preview; AI_COUNT_TOKENS GA (cost/usage governance).
  - https://docs.snowflake.com/en/release-notes/2026/other/2026-02-02-cortex-code-cli
  - https://docs.snowflake.com/en/release-notes/2026/other/2026-02-02-cortex-code-snowsight
  - https://docs.snowflake.com/en/release-notes/2026/other/2026-01-27-ai-count-tokens-function-ga.html
- BigQuery: Gemini in BigQuery data-residency (US/EU) announced; conversational analytics Preview; Gemini Cloud Assist for resource discovery and job history in Preview.
  - https://cloud.google.com/bigquery/docs/release-notes
- Microsoft Fabric: January "What’s New" highlights warehouse features (MERGE, result set caching), but no new Copilot entries on that page in this window.
  - https://learn.microsoft.com/en-us/fabric/fundamentals/whats-new

## AI-native breadth (multimodal + full-text + graph)
- Multimodal: BigQuery’s Gemini-based functions explicitly support multimodal inputs (text + multimodal), and Pinterest’s PinLanding pipeline uses multimodal LLMs to generate and validate shopping collections at scale.
  - https://cloud.google.com/bigquery/docs/release-notes
  - https://medium.com/pinterest-engineering/pinlanding-turn-billions-of-products-into-instant-shopping-collections-with-multimodal-ai-3489320294e9
- Full-text + hybrid: OpenSearch Serverless supports hybrid (lexical + neural + vector) search and AI connectors.
  - https://aws.amazon.com/about-aws/whats-new/2025/08/amazon-opensearch-serverless-ai-connectors-hybrid-search/
- Vector infra at scale: Elastic’s DiskBBQ improves vector search efficiency by reducing RAM dependence; Zilliz adds embedding/reranking functions and hosted models (preview), strengthening end-to-end retrieval pipelines.
  - https://ir.elastic.co/news/news-details/2025/Elastic-Introduces-New-Vector-Storage-Format-DiskBBQ-for-More-Efficient-Vector-Search/default.aspx
  - https://docs.zilliz.com/docs/changelogs
- Graph: Neo4j released 2026.01.3 in early Feb, signaling sustained graph-platform velocity (not necessarily AI-specific, but relevant for KG workloads).
  - https://neo4j.com/release-notes/

## Peer/Customer engineering signals (Pinterest)
- New CDC-based ingestion framework built on Debezium/TiCDC, Kafka, Flink, Spark, and Iceberg; delivers online-to-offline updates in minutes and supports row-level deletion.
  - https://medium.com/pinterest-engineering/next-generation-db-ingestion-at-pinterest-66844b7153b7
- PinLanding uses multimodal LLMs and an LLM-as-judge pipeline to build shopping collections; deployed at production scale with millions of landing pages and reported search-performance gains.
  - https://medium.com/pinterest-engineering/pinlanding-turn-billions-of-products-into-instant-shopping-collections-with-multimodal-ai-3489320294e9

## Interpretation (inference)
- AI-ready leaders are converging on a "trusted assistant layer" tied to governance/cost controls (AI_COUNT_TOKENS, data-residency, assistant/MCP integration), which is becoming a prerequisite for enterprise adoption.
- AI-native competition is shifting from pure vector storage to full retrieval stacks: embedded inference + reranking + hybrid retrieval + operational limits (Zilliz + Pinecone + OpenSearch).
- Multimodal is becoming a first-class search primitive, validated by BigQuery multimodal AI functions and Pinterest’s large-scale multimodal production pipeline.

## Risks and unknowns
- Many AI-native features remain Preview/Private Preview; availability and pricing may be constrained by region/SKU.
- Paywalled analyst and premium media sources are not included.
- Some AI-native breadth signals (OpenSearch hybrid, Elastic DiskBBQ) are not in the last 30 days but remain important baselines.

## Watch list (next 2-4 weeks)
- Preview to GA transitions: Databricks MCP servers, Snowflake Cortex Code in Snowsight, BigQuery conversational analytics, Zilliz hosted models.
- Multimodal retrieval maturity: track whether BigQuery multimodal AI functions progress beyond Preview and whether vector vendors expose multimodal pipelines as GA.
- Graph + KG: monitor Neo4j and graph vendors for AI-specific features (beyond maintenance releases).

## Evidence log (selected)
| Date | Source | Company | Feature | Status | Availability | Link |
|---|---|---|---|---|---|---|
| 2026-02-02 | Snowflake release notes | Snowflake | Cortex Code CLI | GA | GA | https://docs.snowflake.com/en/release-notes/2026/other/2026-02-02-cortex-code-cli |
| 2026-02-02 | Snowflake release notes | Snowflake | Cortex Code in Snowsight | Preview | Preview | https://docs.snowflake.com/en/release-notes/2026/other/2026-02-02-cortex-code-snowsight |
| 2026-01-27 | Databricks release notes | Databricks | Managed MCP Servers | Public Preview | Preview | https://docs.databricks.com/aws/en/release-notes/product/2026/january |
| 2026-01 | Zilliz Cloud release notes | Zilliz | Embedding/reranking + hosted models | Preview | Preview/Private | https://docs.zilliz.com/docs/changelogs |
| 2025-07-15 | Qdrant blog | Qdrant | Cloud Inference (multimodal + hybrid) | GA | Paid clusters | https://qdrant.tech/blog/qdrant-cloud-inference-launch/ |
| 2025-08-07 | AWS What’s New | OpenSearch | Hybrid + neural search, AI connectors | GA | Regional | https://aws.amazon.com/about-aws/whats-new/2025/08/amazon-opensearch-serverless-ai-connectors-hybrid-search/ |
| 2026-01-29 | MongoDB Search changelog | MongoDB | Search alerts/metrics | GA | Atlas | https://www.mongodb.com/docs/atlas/atlas-search/changelog/ |

