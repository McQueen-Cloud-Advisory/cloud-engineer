# Analytics Platform on Google Cloud

## Purpose

This pattern explains how to build a first-pass analytics platform on Google Cloud using managed storage, messaging, and analytical query services.

## Pattern Summary

A small analytics platform on Google Cloud often combines Cloud Storage as a landing zone with BigQuery as the analytical destination. Pub/Sub and a serverless processing layer can be used to move data into the right shape as it enters the platform.

This pattern matters because analytics systems need more than one storage choice. They require data movement, curation, access control, and operational visibility across the full pipeline.

## Common Use Cases

- Reporting pipelines
- Batch or event-driven analytics ingestion
- Portfolio analytics projects

## Reference Architecture

```text
Data source
-> Pub/Sub or batch load
-> Cloud Storage raw zone
-> BigQuery curated layer
-> Monitoring
```

## Provider Services

- Cloud Storage
- Pub/Sub
- Cloud Functions or Cloud Run
- BigQuery
- Cloud Monitoring

## Design Considerations

### Security

Separate access to raw and curated data where appropriate and review how service accounts move data through the pipeline.

### Reliability

Treat ingestion and transformation as production workloads with alerts, retries, and data-quality review.

### Observability

Track ingestion success, storage growth, and analytical freshness so issues surface before users notice them.

### Cost

Storage growth, repeated data movement, and query volume are the main cost areas to monitor.

### Deployment

Add layers incrementally so the data flow stays explainable and maintainable.

## Related Projects

- [Project 04: Analytics Platform](../projects/project-04-analytics-platform.md)

## Official References

- [BigQuery documentation](https://cloud.google.com/bigquery/docs)
- [Cloud Storage documentation](https://cloud.google.com/storage/docs)
- [Pub/Sub documentation](https://cloud.google.com/pubsub/docs)
