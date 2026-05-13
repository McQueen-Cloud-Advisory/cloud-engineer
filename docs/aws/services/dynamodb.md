# Amazon DynamoDB

## Purpose

Amazon DynamoDB is a managed NoSQL database for high-scale, low-latency key-value and document workloads.

## What Problem It Solves

It provides a durable application data store when relational features are not required and predictable scale matters.

## When to Use It

- Use it for request-driven application state and metadata.
- Use it when access patterns are known and fit a key-value or document model.
- Use it when you need managed scaling and high availability without operating database servers.

## When Not to Use It

- Do not use it before you understand the access patterns and key design.
- Do not assume it is a drop-in replacement for relational querying and joins.

## Cloud Engineering Considerations

### Identity and Access

Limit read and write permissions to the specific tables and actions each workload needs.

### Networking

Review how application runtimes reach DynamoDB and whether private access patterns are required.

### Security

Protect sensitive attributes, enable encryption, and review access paths for data export or streams.

### Observability

Monitor throttling, latency, failed requests, and capacity behavior against expected access patterns.

### Cost

Read and write volume, storage, backups, and inefficient key design all affect cost.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)

## Related Patterns

- [Serverless API](../patterns/serverless-api.md)

## Official References

- [Amazon DynamoDB documentation](https://docs.aws.amazon.com/dynamodb/)
- [DynamoDB developer guide](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html)
