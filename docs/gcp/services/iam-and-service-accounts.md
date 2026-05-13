# IAM and Service Accounts

## Purpose

Google Cloud IAM and service accounts control who or what can access Google Cloud resources and what actions they can perform.

## What Problem It Solves

They provide a way to separate human access, workload access, and automation privileges without sharing credentials broadly.

## When to Use It

- Use IAM roles to scope user and group permissions.
- Use service accounts for workload identity and automation.
- Use them to enforce least privilege across projects and services.

## When Not to Use It

- Do not use broad project-wide permissions when narrower roles are enough.
- Do not rely on unmanaged service account keys when platform-managed identity paths are available.

## Cloud Engineering Considerations

### Identity and Access

Review IAM bindings, service account usage, and the difference between acting as a workload and administering the platform.

### Networking

Identity is separate from networking, but project structure, ingress, and cross-project access patterns still affect design.

### Security

Avoid unnecessary service account keys, review permission inheritance, and keep powerful roles tightly limited.

### Observability

Monitor access changes and authorization failures so permission issues surface quickly.

### Cost

IAM is not a major direct cost driver, but weak access controls can contribute to operational and spend risk elsewhere.

## Related Projects

- [Project 01: Static Site](../projects/project-01-static-site.md)
- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Static Site](../patterns/static-site.md)
- [Serverless API](../patterns/serverless-api.md)
- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Google Cloud IAM overview](https://cloud.google.com/iam/docs/overview)
- [Service accounts overview](https://cloud.google.com/iam/docs/service-account-overview)
