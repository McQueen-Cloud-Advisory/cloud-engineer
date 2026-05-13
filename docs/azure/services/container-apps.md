# Azure Container Apps

## Purpose

Azure Container Apps runs containerized applications on a managed platform designed for modern web services and event-driven apps.

## What Problem It Solves

It gives teams a simpler way to run containers without managing a full orchestrator while still supporting HTTP and background workloads.

## When to Use It

- Use it for containerized APIs and application fronts.
- Use it when a workload needs more packaging control than a function platform provides.
- Use it for managed container hosting that integrates with Azure identity and monitoring services.

## When Not to Use It

- Do not use it when the workload requires deep orchestrator-level control that the service does not expose.
- Do not assume container hosting removes the need for secret, image, and scaling review.

## Cloud Engineering Considerations

### Identity and Access

Separate deployment permissions from runtime permissions and prefer managed identities for downstream access.

### Networking

Review ingress exposure, internal versus external apps, and how the app reaches data or model services.

### Security

Keep images current, restrict secrets, and review public exposure deliberately.

### Observability

Monitor requests, revisions, scaling behavior, and container logs as part of normal operations.

### Cost

Runtime resource choices and scale-out behavior drive cost.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Azure Container Apps documentation](https://learn.microsoft.com/en-us/azure/container-apps/)
- [Azure Container Apps overview](https://learn.microsoft.com/en-us/azure/container-apps/overview)
