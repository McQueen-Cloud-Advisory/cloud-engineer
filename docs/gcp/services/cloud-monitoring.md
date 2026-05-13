# Cloud Monitoring

## Purpose

Cloud Monitoring provides metrics, dashboards, alerts, and operational visibility for Google Cloud workloads.

## What Problem It Solves

It gives teams a central place to observe service health and respond to operational issues.

## When to Use It

- Use it for metrics, dashboards, and alerting across Google Cloud services.
- Use it as a baseline observability layer for storage, compute, data, and AI workloads.
- Use it to connect application and platform behavior during troubleshooting.

## When Not to Use It

- Do not rely only on default signals if the workload needs application-specific telemetry.
- Do not create alerts without clear response ownership and action thresholds.

## Cloud Engineering Considerations

### Identity and Access

Control who can view telemetry and who can configure dashboards or alerts.

### Networking

Review how telemetry is emitted from restricted or private workloads and how cross-project visibility is handled.

### Security

Treat monitoring data as sensitive operational information and control access accordingly.

### Observability

Use it for health indicators, dashboards, and alerts that tie together application and platform behavior.

### Cost

Telemetry volume, retention, and custom metrics can increase cost over time.

## Related Projects

- [Project 01: Static Site](../projects/project-01-static-site.md)
- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)
- [Project 04: Analytics Platform](../projects/project-04-analytics-platform.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Static Site](../patterns/static-site.md)
- [Serverless API](../patterns/serverless-api.md)
- [Scheduled Job](../patterns/scheduled-job.md)
- [Analytics Platform](../patterns/analytics-platform.md)
- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Cloud Monitoring documentation](https://cloud.google.com/monitoring/docs)
- [Cloud Monitoring overview](https://cloud.google.com/monitoring/docs/monitoring-overview)
