# Azure Blob Storage

## Purpose

Azure Blob Storage is object storage for files, static assets, logs, datasets, and other unstructured data.

## What Problem It Solves

It gives cloud applications a durable storage layer for data that does not need relational query behavior or attached-disk semantics.

## When to Use It

- Use it for static site content and uploaded files.
- Use it as a landing zone for ingestion and analytics datasets.
- Use it for backups, logs, and lifecycle-managed object data.

## When Not to Use It

- Do not use it where a transactional application database is required.
- Do not expose storage publicly without an intentional public-content design.

## Cloud Engineering Considerations

### Identity and Access

Use RBAC, managed identities, and scoped storage access so applications only reach the containers they need.

### Networking

Review public versus private access, private endpoints, and data egress patterns.

### Security

Use encryption, lifecycle policies, and access restrictions that match the sensitivity of the stored content.

### Observability

Track storage growth, access patterns, and ingestion behavior as part of the wider system health picture.

### Cost

Capacity, operations, redundancy choice, and data transfer all affect cost.

## Related Projects

- [Project 01: Static Site](../projects/project-01-static-site.md)
- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)
- [Project 04: Analytics Platform](../projects/project-04-analytics-platform.md)

## Related Patterns

- [Static Site](../patterns/static-site.md)
- [Analytics Platform](../patterns/analytics-platform.md)

## Official References

- [Azure Blob Storage documentation](https://learn.microsoft.com/en-us/azure/storage/blobs/)
- [Introduction to Azure Blob Storage](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction)
