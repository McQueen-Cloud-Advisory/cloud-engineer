# Managed Identities

## Purpose

Managed identities give Azure workloads a platform-managed identity for accessing other Azure resources.

## What Problem It Solves

They remove the need to store credentials for many service-to-service interactions inside Azure.

## When to Use It

- Use them for runtime access from Functions, Container Apps, and other Azure services.
- Use them when a workload needs Azure resource access without embedded secrets.
- Use them to simplify secret management and reduce credential sprawl.

## When Not to Use It

- Do not grant a managed identity broader access than the workload needs.
- Do not assume identity design is complete until RBAC assignments are reviewed end to end.

## Cloud Engineering Considerations

### Identity and Access

Treat managed identities as first-class workload identities and review every role assignment they receive.

### Networking

Managed identities are not a network control, so review how the workload still reaches the target service.

### Security

They reduce secret exposure, but authorization scope still determines blast radius.

### Observability

Track access failures and permission changes as part of normal platform operations.

### Cost

Managed identities are primarily a security and operational benefit rather than a direct cost driver.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Serverless API](../patterns/serverless-api.md)
- [Scheduled Job](../patterns/scheduled-job.md)
- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Managed identities documentation](https://learn.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/overview)
- [Managed identities overview](https://learn.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/overview)
