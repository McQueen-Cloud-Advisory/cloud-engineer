# AWS Identity and Access Management (IAM)

## Purpose

IAM defines who or what can act in an AWS account and what those identities are allowed to do.

## What Problem It Solves

It gives teams a way to separate human access, workload access, and privileged administration instead of relying on shared credentials.

## When to Use It

- Use it to create least-privilege roles for workloads and automation.
- Use it to control developer and administrator access with policies and federation.
- Use it to define trust relationships between AWS services and your application roles.

## When Not to Use It

- Do not rely on long-lived access keys for workloads when roles are available.
- Do not use broad administrator permissions as a substitute for clear access design.

## Cloud Engineering Considerations

### Identity and Access

Use roles, federation, and scoped policies. Review trust policies as carefully as permission policies.

### Networking

IAM is a control-plane service, but account boundaries, VPC endpoints, and condition keys still influence access design.

### Security

Enable MFA for human access, remove unused credentials, and prefer short-lived credentials for workloads.

### Observability

Review CloudTrail events, access analyzer findings, and authorization failures regularly.

### Cost

IAM itself is not a major direct cost driver, but weak permissions can lead to accidental spend elsewhere.

## Related Projects

- [Project 01: Static Site](../projects/project-01-static-site.md)
- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Static Site](../patterns/static-site.md)
- [Serverless API](../patterns/serverless-api.md)

## Official References

- [AWS IAM documentation](https://docs.aws.amazon.com/iam/)
- [IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
