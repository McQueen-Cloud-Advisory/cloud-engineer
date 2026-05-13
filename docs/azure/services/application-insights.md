# Application Insights

## Purpose

Application Insights collects application telemetry for Azure workloads, including requests, dependencies, failures, and performance data.

## What Problem It Solves

It helps teams understand runtime behavior and troubleshoot application issues beyond infrastructure-level metrics alone.

## When to Use It

- Use it to monitor application performance and failures.
- Use it when distributed request visibility matters for APIs or background jobs.
- Use it with Azure Monitor to build a stronger operational picture for cloud applications.

## When Not to Use It

- Do not assume default telemetry is enough for every workload.
- Do not capture sensitive data carelessly in traces or custom events.

## Cloud Engineering Considerations

### Identity and Access

Control who can view telemetry and who can change alerting or data retention settings.

### Networking

Review how telemetry is emitted from runtimes and whether network restrictions affect collection.

### Security

Treat logs and traces as potentially sensitive data and manage access and retention accordingly.

### Observability

Use Application Insights for request tracing, dependency visibility, error investigation, and alerting inputs.

### Cost

Telemetry volume, retention, and high-cardinality custom events can increase cost.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Serverless API](../patterns/serverless-api.md)
- [Scheduled Job](../patterns/scheduled-job.md)
- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Application Insights documentation](https://learn.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview)
- [Azure Monitor documentation](https://learn.microsoft.com/en-us/azure/azure-monitor/)
