# Secret Manager

## Purpose

Secret Manager stores sensitive values such as API keys, tokens, and credentials for Google Cloud workloads.

## What Problem It Solves

It keeps secrets out of code and configuration files while giving runtimes a managed retrieval path.

## When to Use It

- Use it for application secrets and integration credentials.
- Use it when workloads need runtime access to sensitive configuration.
- Use it to reduce credential sprawl across projects and services.

## When Not to Use It

- Do not hard-code secrets into applications or deployment configuration.
- Do not grant broad secret access to workloads that only need one or two values.

## Cloud Engineering Considerations

### Identity and Access

Use IAM and service accounts so each workload can only read the secrets it actually needs.

### Networking

Review how workloads retrieve secrets and whether private service access or network restrictions affect that path.

### Security

Treat secret lifecycle, rotation, and access logging as part of the security design.

### Observability

Track secret access failures and unusual access patterns so credential issues are visible quickly.

### Cost

Stored versions and access operations add cost, so clean up unused secrets and avoid noisy access loops.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Serverless API](../patterns/serverless-api.md)
- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Secret Manager documentation](https://cloud.google.com/secret-manager/docs)
- [Secret Manager overview](https://cloud.google.com/secret-manager/docs/overview)
