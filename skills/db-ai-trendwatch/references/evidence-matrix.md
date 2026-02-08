# Evidence Matrix

## Evidence levels

| Level | Label | Minimum evidence | Typical status | Weight |
|-------|-------|------------------|----------------|--------|
| A | Verified GA | Docs + release notes + pricing/entitlements + constraints stated | GA | High |
| B | Validated preview | Docs + limitations + explicit preview/beta label | Preview/Public Preview | Medium |
| C | Announcement only | Blog/PR only, no docs or release notes | Roadmap/Teaser | Low |

## Signal types to classify
- Product capability (copilot, NL2SQL, vector search, RAG, model serving, governance AI)
- Availability (GA/preview, region, SKU, rollout timeline)
- Economics (pricing, add-on charges, credits)
- Adoption (customer references, usage metrics)
- Performance (benchmarks, latency/cost claims)

## Validation checklist (use for A/B)
- Is there an official doc or release note?
- Is GA/preview status explicit?
- Are region/SKU constraints stated?
- Is pricing or entitlement stated?
- Is there at least one independent confirmation?

## Notes
- If any checklist item is missing, downgrade the level or mark as unknown.
- Do not promote to Level A without explicit GA and availability evidence.
