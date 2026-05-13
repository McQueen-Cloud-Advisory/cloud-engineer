# Amazon CloudWatch

## Purpose

Amazon CloudWatch collects metrics, logs, dashboards, and alarms for AWS workloads.

## What Problem It Solves

It gives teams a managed place to monitor system behavior, alert on problems, and review operational history.

## When to Use It

- Use it to collect runtime metrics and logs from AWS services.
- Use it to create alarms and dashboards for application and infrastructure behavior.
- Use it as a baseline observability layer across serverless, storage, and AI workloads.

## When Not to Use It

- Do not assume default metrics and logs are enough for production troubleshooting.
- Do not create alerts without clear ownership and response expectations.

## Cloud Engineering Considerations

### Identity and Access

Control who can read logs, manage alarms, and change dashboards or metric filters.

### Networking

Understand which services publish telemetry automatically and which need additional configuration or delivery paths.

### Security

Logs can contain sensitive data, so treat retention, access, and redaction as part of system design.

### Observability

Use CloudWatch to connect service health, error rates, latency, and operational alerts in one place.

### Cost

Log ingestion, retention, custom metrics, and dashboards all contribute to cost.

## Related Projects

- [Project 01: Static Site](../projects/project-01-static-site.md)
- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Serverless API](../patterns/serverless-api.md)
- [Scheduled Job](../patterns/scheduled-job.md)
- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Amazon CloudWatch documentation](https://docs.aws.amazon.com/cloudwatch/)
- [CloudWatch user guide](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html)
