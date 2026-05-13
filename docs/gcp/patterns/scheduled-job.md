# Scheduled Job on Google Cloud

## Purpose

This pattern explains how to run recurring workloads on Google Cloud using managed scheduling and event delivery services.

## Pattern Summary

A scheduled job pattern on Google Cloud commonly uses Cloud Scheduler to publish to Pub/Sub and a downstream runtime such as Cloud Functions to do the work. That creates a managed recurring pipeline without operating a dedicated scheduler host.

This pattern matters because recurring workloads need more than a cron expression. They need secret handling, retry strategy, landing storage, and monitoring if they are going to run reliably over time.

## Common Use Cases

- Scheduled ingestion
- Maintenance tasks
- Recurring synchronization jobs

## Reference Architecture

```text
Schedule
-> Cloud Scheduler
-> Pub/Sub
-> Cloud Functions
-> Storage or downstream API
-> Monitoring
```

## Provider Services

- Cloud Scheduler
- Pub/Sub
- Cloud Functions
- Cloud Storage
- Secret Manager
- Cloud Monitoring

## Design Considerations

### Security

Protect external credentials, keep service account access narrow, and review who can modify the schedule or subscriptions.

### Reliability

Design for safe retries, visible failures, and idempotent processing so recurring jobs do not silently drift.

### Observability

Track scheduled runs, queue backlog, processing failures, and data freshness together.

### Cost

The base schedule is inexpensive, but repeated processing, storage, and telemetry can add up over time.

### Deployment

Treat the scheduler, messaging, runtime, and monitoring definitions as one deployable system.

## Related Projects

- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)

## Official References

- [Cloud Scheduler documentation](https://cloud.google.com/scheduler/docs)
- [Pub/Sub documentation](https://cloud.google.com/pubsub/docs)
- [Cloud Functions documentation](https://cloud.google.com/functions/docs)
