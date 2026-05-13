# Microsoft Entra ID

## Purpose

Microsoft Entra ID provides identity management for users, groups, applications, and federated access in Azure.

## What Problem It Solves

It gives teams a central identity system for access control, application authentication, and tenant-level governance.

## When to Use It

- Use it for human identity, application registration, and authentication flows.
- Use it when Azure services and applications need centralized identity control.
- Use it as the foundation for workload and user access design across Azure.

## When Not to Use It

- Do not treat identity as only a sign-in problem.
- Do not rely on overly broad tenant-wide privileges when scoped roles or app access are possible.

## Cloud Engineering Considerations

### Identity and Access

Design user, group, and application identities deliberately and review how they map to Azure roles and runtime access.

### Networking

Identity is a control-plane layer, but network restrictions and application exposure still affect how identities are used.

### Security

Use conditional access, MFA, and strong application registration practices wherever they apply.

### Observability

Review sign-in, directory, and application authentication behavior as part of security operations.

### Cost

Licensing tiers can matter depending on governance, conditional access, and identity protection needs.

## Related Projects

- [Project 01: Static Site](../projects/project-01-static-site.md)
- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Static Site](../patterns/static-site.md)
- [Serverless API](../patterns/serverless-api.md)

## Official References

- [Microsoft Entra ID documentation](https://learn.microsoft.com/en-us/entra/fundamentals/)
- [What is Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/fundamentals/whatis)
