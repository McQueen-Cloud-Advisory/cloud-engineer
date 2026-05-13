# Microsoft Fabric

## Purpose

Microsoft Fabric provides an integrated analytics platform for data engineering, reporting, and broader analytical workflows.

## What Problem It Solves

It gives teams a more unified analytics layer when storage, transformation, and reporting need to work together.

## When to Use It

- Use it when analytics work spans ingestion, transformation, and reporting.
- Use it when a project needs a platform that can support broader analytics workflows over time.
- Use it when you want a more complete analytics surface than a single storage or pipeline service provides.

## When Not to Use It

- Do not adopt it before the basic data flow and reporting needs are clear.
- Do not treat platform breadth as a substitute for disciplined data modeling and governance.

## Cloud Engineering Considerations

### Identity and Access

Review workspace access, data access, and how identities map to the broader Azure estate.

### Networking

Understand where data originates, how it is ingested, and which services must reach Fabric workloads.

### Security

Plan for data governance, workspace access boundaries, and sensitive data exposure.

### Observability

Track pipeline, dataset, and reporting health as part of platform operations.

### Cost

Capacity and workload usage can become significant, so align the platform size to a realistic project scope.

## Related Projects

- [Project 04: Analytics Platform](../projects/project-04-analytics-platform.md)

## Related Patterns

- [Analytics Platform](../patterns/analytics-platform.md)

## Official References

- [Microsoft Fabric documentation](https://learn.microsoft.com/en-us/fabric/)
- [What is Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/get-started/microsoft-fabric-overview)
