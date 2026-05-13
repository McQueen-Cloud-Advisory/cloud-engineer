# Azure Cosmos DB

## Purpose

Azure Cosmos DB is a managed database service for globally distributed and application-focused data workloads.

## What Problem It Solves

It gives teams a managed way to store application data at scale without operating database servers directly.

## When to Use It

- Use it for application data that fits a managed document or NoSQL model.
- Use it when predictable scale and low-latency reads or writes matter.
- Use it when the data model and access paths are better suited to Cosmos DB than to a relational store.

## When Not to Use It

- Do not choose it before understanding the data model and access patterns.
- Do not assume it behaves like a relational database with the same design tradeoffs.

## Cloud Engineering Considerations

### Identity and Access

Use RBAC, managed identities, and scoped keys or tokens carefully so application access stays narrow.

### Networking

Review private endpoints and how application runtimes access the database across environments.

### Security

Protect sensitive data, review backup behavior, and make sure only the right services can access the account.

### Observability

Track request units, latency, and failure behavior against expected application usage patterns.

### Cost

Throughput configuration, storage, and inefficient access patterns all affect cost.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)

## Related Patterns

- [Serverless API](../patterns/serverless-api.md)

## Official References

- [Azure Cosmos DB documentation](https://learn.microsoft.com/en-us/azure/cosmos-db/)
- [Azure Cosmos DB overview](https://learn.microsoft.com/en-us/azure/cosmos-db/introduction)
