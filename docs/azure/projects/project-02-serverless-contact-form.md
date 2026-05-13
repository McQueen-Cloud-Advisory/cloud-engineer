# Project 02: Serverless Contact Form on Azure

## Purpose

Build a serverless contact form so you practice API exposure, function integration, application data storage, secrets handling, and telemetry.

## Architecture

```text
User request
-> Azure API Management
-> Azure Functions
-> Azure Cosmos DB
-> Azure Key Vault and Application Insights
```

## Services Used

- [Azure API Management](../services/api-management.md)
- [Azure Functions](../services/functions.md)
- [Azure Cosmos DB](../services/cosmos-db.md)
- [Azure Key Vault](../services/key-vault.md)
- [Application Insights](../services/application-insights.md)
- [Managed Identities](../services/managed-identities.md)

## What You Will Build

- An API endpoint for form submission.
- A function app that validates and stores submitted data.
- Operational telemetry for requests, failures, and dependencies.

## Skills Practiced

- Serverless API delivery
- Managed identity usage
- Application data modeling
- Operational telemetry

## Implementation Notes

Keep the API and data model small. Focus on validation, runtime identity, telemetry, and a deployment shape you can explain clearly.

## Security Considerations

Use managed identities where possible, keep secrets in Key Vault, and make sure backend access is scoped to the minimum required resources.

## Cost Considerations

This project is typically low cost at small scale, but request volume, Cosmos DB configuration, and logging can increase costs if left unchecked.

## How to Extend This Project

- Add authentication for an admin view.
- Add notifications or queue-based processing.
- Add spam controls or abuse monitoring.

## Portfolio Value

This project shows that you can connect an API front door, serverless compute, storage, identity, and observability into a coherent application path.

## Official References

- [Azure API Management documentation](https://learn.microsoft.com/en-us/azure/api-management/)
- [Azure Functions documentation](https://learn.microsoft.com/en-us/azure/azure-functions/)
- [Azure Cosmos DB documentation](https://learn.microsoft.com/en-us/azure/cosmos-db/)
- [Azure Key Vault documentation](https://learn.microsoft.com/en-us/azure/key-vault/)
