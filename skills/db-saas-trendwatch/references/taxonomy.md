# SaaS Database Trend Taxonomy

Use this taxonomy to classify signals and compare SaaS vendors.

## Architecture and tenancy
- Tenancy model: shared, siloed, hybrid
- Isolation: schema-per-tenant, database-per-tenant, row-level
- Sharding/partitioning: key-based, tenant-based, geo-based
- Consistency model: strong vs eventual

## Workload and data layers
- OLTP store (primary)
- OLAP/warehouse (analytics)
- Search (full-text)
- Vector search / semantic retrieval
- Cache (redis/memcached)
- Streaming / CDC

## Storage and performance
- Storage engine: row, column, LSM, hybrid
- Indexing strategy: secondary, inverted, vector
- Query acceleration: materialized views, pre-aggregation
- Latency and tail behavior

## Reliability and availability
- Multi-region architecture
- RPO/RTO targets
- Failover automation
- Backup/restore cadence and verification

## Security and compliance
- Data residency and sovereign regions
- Encryption at rest/in transit
- Audit logging and access controls
- Compliance: SOC2, HIPAA, PCI, GDPR

## Cost and efficiency
- Storage tiering and lifecycle
- Compression and columnarization
- Reserved capacity vs on-demand
- Cost attribution by tenant

## Migration and lifecycle
- Database migrations and replatforming
- Version upgrades and compatibility
- Schema evolution strategy
