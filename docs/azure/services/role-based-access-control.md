# Azure Role-Based Access Control

## Purpose

Azure RBAC controls which identities can perform actions on Azure resources.

## What Problem It Solves

It gives teams a way to scope access by role, resource group, subscription, or individual resource instead of relying on broad administrator permissions.

## When to Use It

- Use it to assign least-privilege access to people and workloads.
- Use it to separate deployment, operations, and runtime responsibilities.
- Use it to control access to Azure resources in a repeatable way.

## When Not to Use It

- Do not grant owner-level access by default when narrower roles are sufficient.
- Do not treat role assignment as a one-time task with no ongoing review.

## Cloud Engineering Considerations

### Identity and Access

Review scope, inheritance, and role definition carefully before assigning access.

### Networking

RBAC is not a network boundary, so it should work alongside network controls rather than replace them.

### Security

Least privilege, periodic access review, and separation of duties matter as much as the role definitions themselves.

### Observability

Track role changes and authorization failures so access problems are visible quickly.

### Cost

RBAC does not add meaningful direct cost, but poor access control can contribute to accidental spend and operational risk.

## Related Projects

- [Project 01: Static Site](../projects/project-01-static-site.md)
- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Static Site](../patterns/static-site.md)
- [Serverless API](../patterns/serverless-api.md)
- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Azure RBAC documentation](https://learn.microsoft.com/en-us/azure/role-based-access-control/)
- [Azure RBAC overview](https://learn.microsoft.com/en-us/azure/role-based-access-control/overview)
