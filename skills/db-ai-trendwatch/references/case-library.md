# Case Library (golden + failure cases)

## Golden cases (what good signals look like)

### Case 1: Snowflake Cortex AI Functions
- Evidence: Official docs list region availability and warn that preview features are not suitable for production workloads.
- Why it matters: Docs provide clear availability and status, enabling accurate readiness assessment.
- Do: Treat doc-level GA/preview status and region lists as primary evidence.
- Do not: Assume universal availability without checking regions.
- Sources:
  - Snowflake Cortex AI Functions docs (availability + preview guidance): https://docs.snowflake.com/en/user-guide/snowflake-cortex/llm-functions

### Case 2: Databricks Assistant in Unity Catalog (Sample Data Exploration)
- Evidence: Databricks blog announces the experience and labels it Public Preview.
- Why it matters: UI-integrated AI features signal deep product investment, but preview status still implies rollout risk.
- Do: Track the path from preview to GA via release notes and docs.
- Do not: Treat preview features as production-ready adoption signals.
- Sources:
  - Databricks blog (Public Preview announcement): https://www.databricks.com/blog/explore-data-instantly-databricks-assistant-unity-catalog

### Case 3: Microsoft Fabric Copilot SKU expansion
- Evidence: Fabric blog states Copilot and AI capabilities are available for all paid SKUs (F2 and above) with rollout timing.
- Why it matters: Expanding availability to lower SKUs is a strong adoption signal, but timing and rollout still matter.
- Do: Confirm SKU gating and rollout schedule before drawing adoption conclusions.
- Do not: Assume immediate access for all customers on announcement day.
- Sources:
  - Fabric blog (FabCon 2025 recap): https://www.microsoft.com/en-us/microsoft-fabric/blog/2025/04/03/fabcon-2025-recap-what-happened-on-day-one-and-what-you-can-still-catch/

### Case 4: BigQuery Gemini feature updates in release notes
- Evidence: BigQuery release notes list Gemini-related features with explicit preview status and dates.
- Why it matters: Release notes provide a reliable timeline and status for feature maturity.
- Do: Use release notes as the primary source for GA/preview timeline tracking.
- Do not: Rely solely on marketing announcements to infer maturity.
- Sources:
  - BigQuery release notes (Gemini features): https://cloud.google.com/bigquery/docs/release-notes

## Failure patterns (what goes wrong)

### Failure 1: Treating preview as GA
- Example evidence: Snowflake docs explicitly warn that preview features are not for production; Databricks blog calls features Public Preview.
- Fix: Always label preview in outputs and wait for GA in release notes before calling it production-ready.

### Failure 2: Ignoring region/SKU gating
- Example evidence: Snowflake docs list select regions; Fabric blog notes SKU tiers and rollout.
- Fix: Always record region/SKU constraints and rollouts in the evidence log.

### Failure 3: Using announcements without doc validation
- Example evidence: BigQuery release notes show preview/GA timelines that announcements can omit.
- Fix: Require doc or release-note confirmation before elevating a claim.
