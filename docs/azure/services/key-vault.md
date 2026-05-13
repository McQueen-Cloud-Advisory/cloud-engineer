# Azure Key Vault

## Purpose

Azure Key Vault stores secrets, keys, and certificates for Azure applications and automation.

## What Problem It Solves

It keeps sensitive values out of code and configuration while giving applications a managed retrieval path.

## When to Use It

- Use it for application secrets, credentials, and certificates.
- Use it when workloads need controlled secret retrieval at runtime.
- Use it to support separation between operators, deployments, and runtime access.

## When Not to Use It

- Do not hard-code secrets into applications or pipelines.
- Do not grant vault-wide access to workloads that only need a small subset of secrets.

## Cloud Engineering Considerations

### Identity and Access

Use RBAC or access policies deliberately and prefer managed identities for runtime secret access.

### Networking

Review private endpoints and how workloads reach the vault across environments.

### Security

Treat secret naming, rotation, and access logging as part of the security design, not just storage details.

### Observability

Track access failures and unusual access patterns so credential problems surface quickly.

### Cost

Operation volume and premium features can increase cost, so remove unused secrets and avoid noisy access patterns.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Serverless API](../patterns/serverless-api.md)
- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Azure Key Vault documentation](https://learn.microsoft.com/en-us/azure/key-vault/)
- [Azure Key Vault overview](https://learn.microsoft.com/en-us/azure/key-vault/general/overview)
