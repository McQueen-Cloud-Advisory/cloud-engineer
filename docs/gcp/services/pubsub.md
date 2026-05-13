# Pub/Sub

## Purpose

Pub/Sub is Google Cloud's managed messaging service for asynchronous event delivery between producers and consumers.

## What Problem It Solves

It helps decouple systems so one service can publish events without needing direct knowledge of every downstream consumer.

## When to Use It

- Use it for event-driven architectures and asynchronous processing.
- Use it when multiple consumers may need to react to the same event.
- Use it for ingestion pipelines and scheduled workloads that benefit from decoupling.

## When Not to Use It

- Do not use it without a plan for message acknowledgment, retries, and dead-letter handling.
- Do not publish noisy high-volume traffic without a clear consumer design.

## Cloud Engineering Considerations

### Identity and Access

Review which service accounts can publish and subscribe and keep topic or subscription access narrow.

### Networking

Plan how publishers and subscribers reach Pub/Sub and what cross-project or hybrid paths are involved.

### Security

Treat published data as part of the application surface and review who can read messages at each stage.

### Observability

Track backlog, acknowledgment failures, and subscriber health so delivery issues are visible.

### Cost

Message volume, retention, and downstream processing determine cost.

## Related Projects

- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)
- [Project 04: Analytics Platform](../projects/project-04-analytics-platform.md)

## Related Patterns

- [Scheduled Job](../patterns/scheduled-job.md)
- [Analytics Platform](../patterns/analytics-platform.md)

## Official References

- [Pub/Sub documentation](https://cloud.google.com/pubsub/docs)
- [Pub/Sub overview](https://cloud.google.com/pubsub/docs/overview)
