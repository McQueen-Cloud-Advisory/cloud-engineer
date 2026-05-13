# Azure Functions

## Purpose

Azure Functions runs event-driven application code without requiring server management.

## What Problem It Solves

It gives teams a managed compute option for APIs, automation, and background tasks without provisioning application hosts.

## When to Use It

- Use it for serverless APIs and scheduled background jobs.
- Use it when the workload fits an event-driven execution model.
- Use it to connect Azure events and triggers to custom application logic.

## When Not to Use It

- Do not use it when the workload needs runtime characteristics that do not fit the Functions model.
- Do not assume serverless removes the need for deployment and observability discipline.

## Cloud Engineering Considerations

### Identity and Access

Prefer managed identities for downstream access and keep function app permissions narrow.

### Networking

Review how functions reach storage, databases, APIs, and any private resources they depend on.

### Security

Protect configuration, validate trigger input, and keep secrets out of code and deployment artifacts.

### Observability

Use Application Insights and Monitor so invocation failures, performance, and dependency issues are visible quickly.

### Cost

Execution time, trigger volume, and supporting service usage determine cost.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)

## Related Patterns

- [Serverless API](../patterns/serverless-api.md)
- [Scheduled Job](../patterns/scheduled-job.md)

## Official References

- [Azure Functions documentation](https://learn.microsoft.com/en-us/azure/azure-functions/)
- [Azure Functions overview](https://learn.microsoft.com/en-us/azure/azure-functions/functions-overview)
