# Analytics Platform on Azure

## Purpose

This pattern explains how to organize a first-pass analytics platform on Azure using storage, orchestration, and reporting services.

## Pattern Summary

A small analytics platform on Azure commonly starts with Blob Storage as a landing zone, Data Factory as an orchestration layer, and a reporting or analytical surface such as Microsoft Fabric. The key design concern is not just the tool choice but the movement of data from raw inputs into a curated analytical shape.

This pattern matters because analytics systems require attention to data organization, permissions, freshness, and monitoring. They are not only storage projects.

## Common Use Cases

- Data ingestion and reporting
- Operational analytics
- Foundational analytics portfolio projects

## Reference Architecture

```text
Data source
-> Azure Data Factory
-> Azure Blob Storage raw zone
-> Curated analytics layer
-> Monitoring and reporting
```

## Provider Services

- Azure Blob Storage
- Azure Data Factory
- Microsoft Fabric
- Azure Monitor

## Design Considerations

### Security

Separate access to raw and curated data where needed and review how identities move through the ingestion and analytics path.

### Reliability

Treat data movement and transformation as production workloads with alerting, retry, and quality checks.

### Observability

Track ingestion success, storage growth, and reporting freshness so problems surface before they affect users.

### Cost

Storage, orchestration, and analytical platform capacity are the main cost areas to keep intentionally scoped.

### Deployment

Build the platform incrementally so the data flow stays explainable and easy to operate.

## Related Projects

- [Project 04: Analytics Platform](../projects/project-04-analytics-platform.md)

## Official References

- [Azure Blob Storage documentation](https://learn.microsoft.com/en-us/azure/storage/blobs/)
- [Azure Data Factory documentation](https://learn.microsoft.com/en-us/azure/data-factory/)
- [Microsoft Fabric documentation](https://learn.microsoft.com/en-us/fabric/)
