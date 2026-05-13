# Azure Monitor

## Purpose

Azure Monitor is the main monitoring platform for collecting metrics, logs, dashboards, and alerts across Azure workloads.

## What Problem It Solves

It gives teams a central observability layer for understanding platform and application behavior.

## When to Use It

- Use it to monitor Azure resources and application health.
- Use it to define alerts, dashboards, and operational views.
- Use it as a shared observability layer across storage, compute, data, and AI workloads.

## When Not to Use It

- Do not rely only on default signals if the workload has important application-specific behaviors.
- Do not create alerts without clear response ownership.

## Cloud Engineering Considerations

### Identity and Access

Control who can read telemetry and who can configure alerting or retention settings.

### Networking

Review how telemetry is collected across isolated networks or private resources.

### Security

Treat monitoring data as sensitive operational data and control access accordingly.

### Observability

Use Azure Monitor for baselines, alerts, dashboards, and log analysis across the platform.

### Cost

Log ingestion, retention, and advanced observability features can add cost over time.

## Related Projects

- [Project 01: Static Site](../projects/project-01-static-site.md)
- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)
- [Project 04: Analytics Platform](../projects/project-04-analytics-platform.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Static Site](../patterns/static-site.md)
- [Scheduled Job](../patterns/scheduled-job.md)
- [Analytics Platform](../patterns/analytics-platform.md)
- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Azure Monitor documentation](https://learn.microsoft.com/en-us/azure/azure-monitor/)
- [Azure Monitor overview](https://learn.microsoft.com/en-us/azure/azure-monitor/overview)
