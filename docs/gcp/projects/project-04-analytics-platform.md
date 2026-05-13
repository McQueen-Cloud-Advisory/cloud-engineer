# Project 04: Analytics Platform on Google Cloud

## Purpose

Build a small analytics platform so you practice ingestion, object storage organization, analytical querying, and monitoring on Google Cloud.

## Architecture

```text
Sources or scheduled ingestion
-> Pub/Sub or batch load
-> Cloud Storage raw zone
-> BigQuery curated analytics layer
-> Cloud Monitoring
```

## Services Used

- [Pub/Sub](../services/pubsub.md)
- [Cloud Storage](../services/cloud-storage.md)
- [BigQuery](../services/bigquery.md)
- [Cloud Monitoring](../services/cloud-monitoring.md)
- [Cloud Functions](../services/cloud-functions.md)

## What You Will Build

- A raw and curated data flow.
- A queryable analytics layer in BigQuery.
- Monitoring for ingestion and analytical workload health.

## Skills Practiced

- Analytics data flow design
- Object storage organization
- Data loading and query patterns
- Operational monitoring

## Implementation Notes

Keep the dataset and transformation flow small. Focus on how data moves from source to raw storage to curated analytics rather than trying to build a full enterprise platform.

## Security Considerations

Review who can access raw versus curated data, how service accounts move data, and how sensitive fields are handled.

## Cost Considerations

Storage, query scans, and repeated ingestion can increase cost if the dataset or schedule grows without controls.

## How to Extend This Project

- Add data quality checks.
- Add partitioning and lifecycle rules.
- Add a dashboard or scheduled analytical report.

## Portfolio Value

This project shows that you can move beyond application hosting and explain an end-to-end analytics workload with storage, transformation, and query concerns.

## Official References

- [BigQuery documentation](https://cloud.google.com/bigquery/docs)
- [Cloud Storage documentation](https://cloud.google.com/storage/docs)
- [Pub/Sub documentation](https://cloud.google.com/pubsub/docs)
- [Cloud Monitoring documentation](https://cloud.google.com/monitoring/docs)
