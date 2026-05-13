# Azure Data Factory

## Purpose

Azure Data Factory orchestrates data movement and transformation workflows across systems.

## What Problem It Solves

It gives teams a managed way to build repeatable ingestion and pipeline flows without creating every orchestration step from scratch.

## When to Use It

- Use it for scheduled ingestion and movement of data between systems.
- Use it when analytics or integration workflows need pipeline orchestration.
- Use it when the team needs a managed control plane for recurring data movement tasks.

## When Not to Use It

- Do not use it for simple tasks that are better handled by a lighter runtime.
- Do not build pipelines without clear ownership of data quality and failure handling.

## Cloud Engineering Considerations

### Identity and Access

Use managed identities and scoped data-source permissions so pipelines only access approved systems.

### Networking

Review self-hosted versus managed connectivity, private endpoints, and cross-system data paths.

### Security

Protect source credentials, review sensitive data movement, and make sure pipeline permissions are tightly scoped.

### Observability

Track pipeline runs, failures, latency, and data freshness so ingestion problems are visible quickly.

### Cost

Pipeline activity, movement volume, integration runtimes, and frequency all influence cost.

## Related Projects

- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)
- [Project 04: Analytics Platform](../projects/project-04-analytics-platform.md)

## Related Patterns

- [Scheduled Job](../patterns/scheduled-job.md)
- [Analytics Platform](../patterns/analytics-platform.md)

## Official References

- [Azure Data Factory documentation](https://learn.microsoft.com/en-us/azure/data-factory/)
- [Introduction to Azure Data Factory](https://learn.microsoft.com/en-us/azure/data-factory/introduction)
