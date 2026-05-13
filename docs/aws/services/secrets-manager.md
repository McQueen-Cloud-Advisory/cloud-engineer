# AWS Secrets Manager

## Purpose

AWS Secrets Manager stores and rotates sensitive application values such as API keys, tokens, and connection details.

## What Problem It Solves

It keeps secrets out of code, deployment manifests, and ad hoc configuration files while giving applications a managed retrieval path.

## When to Use It

- Use it for API credentials, database secrets, and other sensitive runtime configuration.
- Use it when applications need controlled secret retrieval at runtime.
- Use it when rotation or lifecycle management should be part of the platform design.

## When Not to Use It

- Do not hard-code secrets into functions, containers, or repositories.
- Do not grant broad secret read access to workloads that only need one or two values.

## Cloud Engineering Considerations

### Identity and Access

Grant workloads access to the smallest set of secrets possible and separate operator access from runtime access.

### Networking

Review how workloads retrieve secrets and whether private connectivity or network controls are required.

### Security

Treat secret naming, rotation, and access logging as part of the security design, not just storage details.

### Observability

Monitor secret retrieval failures and unusual access patterns so credential issues are visible quickly.

### Cost

Stored secrets and API usage add cost, so remove unused secrets and avoid unnecessary retrieval loops.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Serverless API](../patterns/serverless-api.md)
- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [AWS Secrets Manager documentation](https://docs.aws.amazon.com/secretsmanager/)
- [Secrets Manager user guide](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html)
