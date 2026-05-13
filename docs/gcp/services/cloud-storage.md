# Cloud Storage

## Purpose

Cloud Storage is Google Cloud object storage for files, static assets, datasets, logs, and other unstructured data.

## What Problem It Solves

It gives teams durable storage for data that does not need a relational or attached-disk access model.

## When to Use It

- Use it for static site assets and file storage.
- Use it as a landing zone for ingestion and analytics datasets.
- Use it for backups, logs, and lifecycle-managed object data.

## When Not to Use It

- Do not use it where a low-latency transactional database is required.
- Do not expose buckets publicly unless that access pattern is intentionally designed.

## Cloud Engineering Considerations

### Identity and Access

Use IAM and service accounts so workloads and users only access the buckets and objects they need.

### Networking

Review public endpoints, private access paths, and data egress behavior when storage participates in a wider system.

### Security

Use encryption, lifecycle rules, and narrow access controls that match the sensitivity of the stored data.

### Observability

Track storage growth, access behavior, and ingestion activity as part of normal operations.

### Cost

Storage class choice, operations, retention, and egress all affect cost.

## Related Projects

- [Project 01: Static Site](../projects/project-01-static-site.md)
- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)
- [Project 04: Analytics Platform](../projects/project-04-analytics-platform.md)

## Related Patterns

- [Static Site](../patterns/static-site.md)
- [Analytics Platform](../patterns/analytics-platform.md)

## Official References

- [Cloud Storage documentation](https://cloud.google.com/storage/docs)
- [Cloud Storage introduction](https://cloud.google.com/storage/docs/introduction)
