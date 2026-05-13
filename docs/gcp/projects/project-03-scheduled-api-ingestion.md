# Project 03: Scheduled API Ingestion on Google Cloud

## Purpose

Build a scheduled ingestion workflow so you practice recurring automation, messaging, secret handling, and landing data in storage.

## Architecture

```text
Cloud Scheduler
-> Pub/Sub
-> Cloud Functions
-> External API call
-> Cloud Storage
-> Cloud Monitoring
```

## Services Used

- Pub/Sub
- [Cloud Functions](../services/cloud-functions.md)
- [Cloud Storage](../services/cloud-storage.md)
- [Secret Manager](../services/secret-manager.md)
- [Cloud Monitoring](../services/cloud-monitoring.md)
- Cloud Scheduler

## What You Will Build

- A scheduled trigger path for ingestion.
- A function that pulls external data and stores results.
- Monitoring and failure visibility for the recurring job.

## Skills Practiced

- Scheduled automation
- Event-driven messaging
- External API integration
- Data landing zone design

## Implementation Notes

Use Cloud Scheduler with Pub/Sub to trigger the function and keep the data flow small. The goal is to understand recurring execution, permissions, secret handling, and operational visibility.

## Security Considerations

Store external credentials in Secret Manager, keep service account access narrow, and review who can trigger or modify the schedule.

## Cost Considerations

The base pattern is usually low cost, but repeated runs, storage growth, and telemetry volume can add up over time.

## How to Extend This Project

- Add retry or dead-letter handling.
- Add data quality checks before storage.
- Add a downstream transformation step into analytics.

## Portfolio Value

This project shows recurring integration work, event-driven design, and the operational thinking needed for scheduled jobs.

## Official References

- [Cloud Scheduler documentation](https://cloud.google.com/scheduler/docs)
- [Pub/Sub documentation](https://cloud.google.com/pubsub/docs)
- [Cloud Functions documentation](https://cloud.google.com/functions/docs)
- [Cloud Storage documentation](https://cloud.google.com/storage/docs)
