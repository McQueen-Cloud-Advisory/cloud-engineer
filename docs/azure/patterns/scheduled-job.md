# Scheduled Job on Azure

## Purpose

This pattern explains how to run recurring workloads on Azure using managed scheduling and integration services.

## Pattern Summary

A scheduled job pattern on Azure often uses Data Factory or another managed trigger path to run a recurring ingestion or maintenance workload. The design centers on repeatability, controlled access to source systems, and clear failure visibility.

This pattern matters because recurring jobs often become operationally important even when they look simple at first. Scheduling, secret access, data landing, and monitoring all need to be explicit in the design.

## Common Use Cases

- Scheduled ingestion
- Batch maintenance tasks
- Recurring synchronization jobs

## Reference Architecture

```text
Schedule
-> Azure Data Factory
-> External source or internal system
-> Blob Storage or downstream processing
-> Monitoring
```

## Provider Services

- Azure Data Factory
- Azure Blob Storage
- Azure Key Vault
- Azure Monitor
- Application Insights

## Design Considerations

### Security

Protect source credentials, scope pipeline permissions carefully, and review who can operate the schedule and downstream data access.

### Reliability

Design for retry, idempotency, and visible failure states so recurring jobs do not silently drift out of compliance.

### Observability

Track pipeline success, latency, and data freshness rather than only trigger execution.

### Cost

Pipeline activity, storage growth, and retained telemetry are the main cost areas to monitor.

### Deployment

Treat schedule definitions and pipeline configuration as part of the deployable system rather than manual platform setup.

## Related Projects

- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)

## Official References

- [Azure Data Factory documentation](https://learn.microsoft.com/en-us/azure/data-factory/)
- [Azure Blob Storage documentation](https://learn.microsoft.com/en-us/azure/storage/blobs/)
