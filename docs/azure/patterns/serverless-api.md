# Serverless API on Azure

## Purpose

This pattern explains how to build a managed API path on Azure using a gateway, serverless compute, and supporting platform services.

## Pattern Summary

A serverless API pattern on Azure often uses API Management as the front door and Azure Functions as the compute layer. Data, secrets, and telemetry are handled by supporting services such as Cosmos DB, Key Vault, Application Insights, and Azure Monitor.

This pattern matters because it shows how cloud engineers connect identity, request handling, runtime logic, monitoring, and data storage into a coherent application path without managing servers directly.

## Common Use Cases

- Forms and lightweight application backends
- Internal APIs
- Event-driven service endpoints

## Reference Architecture

```text
Client
-> Azure API Management
-> Azure Functions
-> Data store and secrets
-> Monitoring and telemetry
```

## Provider Services

- Azure API Management
- Azure Functions
- Azure Cosmos DB
- Azure Key Vault
- Managed Identities
- Application Insights

## Design Considerations

### Security

Validate inputs, restrict API exposure, and use managed identities and least-privilege roles for downstream access.

### Reliability

Design for retries, clear failure handling, and predictable dependency behavior so the API remains understandable under load or error conditions.

### Observability

Correlate request telemetry, function execution, and dependency calls so issues can be traced end to end.

### Cost

Requests, function execution, data store settings, and telemetry volume are the main cost drivers.

### Deployment

Deploy the gateway, function app, identities, and configuration together so environments stay aligned.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)

## Official References

- [Azure API Management documentation](https://learn.microsoft.com/en-us/azure/api-management/)
- [Azure Functions documentation](https://learn.microsoft.com/en-us/azure/azure-functions/)
- [Azure Cosmos DB documentation](https://learn.microsoft.com/en-us/azure/cosmos-db/)
