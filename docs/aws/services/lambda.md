# AWS Lambda

## Purpose

AWS Lambda runs event-driven code without requiring you to manage servers directly.

## What Problem It Solves

It gives teams a way to deploy small application and automation components quickly without taking on host lifecycle management.

## When to Use It

- Use it for event-driven APIs, background processing, and scheduled workloads.
- Use it when the runtime limits and execution model match the workload.
- Use it to connect AWS events to application logic with minimal platform setup.

## When Not to Use It

- Do not use it for workloads that need long-running sessions or specialized runtime control.
- Do not assume serverless removes the need for deployment, observability, or failure handling design.

## Cloud Engineering Considerations

### Identity and Access

Give each function its own execution role and review every permission the function uses downstream.

### Networking

If the function uses VPC resources, understand the networking impact on connectivity, cold starts, and downstream service access.

### Security

Protect environment configuration, validate event input, and avoid embedding secrets directly in code or configuration.

### Observability

Use structured logs, metrics, and alarms so invocation failures and latency shifts are visible quickly.

### Cost

Invocation count, duration, and supporting services determine cost, so noisy triggers and inefficient code matter.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)

## Related Patterns

- [Serverless API](../patterns/serverless-api.md)
- [Scheduled Job](../patterns/scheduled-job.md)

## Official References

- [AWS Lambda documentation](https://docs.aws.amazon.com/lambda/)
- [Lambda developer guide](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)
