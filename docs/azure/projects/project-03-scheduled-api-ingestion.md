# Project 03: Scheduled API Ingestion on Azure

## Purpose

Build a scheduled ingestion workflow so you practice recurring data movement, secret handling, and operational visibility on Azure.

## Architecture

```text
Scheduled trigger
-> Azure Data Factory
-> External API or source system
-> Azure Blob Storage
-> Azure Monitor and Application Insights
```

## Services Used

- [Azure Data Factory](../services/data-factory.md)
- [Azure Blob Storage](../services/blob-storage.md)
- [Azure Key Vault](../services/key-vault.md)
- [Azure Monitor](../services/monitor.md)
- [Application Insights](../services/application-insights.md)

## What You Will Build

- A scheduled pipeline that pulls data from an external source.
- A storage landing zone for raw data.
- Monitoring for pipeline runs and failure visibility.

## Skills Practiced

- Pipeline orchestration
- External data integration
- Data landing zone design
- Operational alerting

## Implementation Notes

Use Data Factory for the first-pass orchestration and keep the pipeline narrow. The goal is to understand scheduling, secret handling, storage layout, and failure visibility.

## Security Considerations

Store external credentials in Key Vault, scope pipeline identities carefully, and review who can access the landing storage.

## Cost Considerations

Pipeline activity, storage growth, and monitoring retention are the main cost areas to watch.

## How to Extend This Project

- Add data validation checks.
- Add a transformation step after landing.
- Add freshness alerts for delayed or failed runs.

## Portfolio Value

This project demonstrates recurring integration work, operational monitoring, and the discipline needed for scheduled data movement in production-style environments.

## Official References

- [Azure Data Factory documentation](https://learn.microsoft.com/en-us/azure/data-factory/)
- [Azure Blob Storage documentation](https://learn.microsoft.com/en-us/azure/storage/blobs/)
- [Azure Key Vault documentation](https://learn.microsoft.com/en-us/azure/key-vault/)
