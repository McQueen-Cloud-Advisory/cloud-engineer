# AWS App Runner

## Purpose

AWS App Runner runs containerized or source-based web applications behind a managed application platform.

## What Problem It Solves

It gives teams a simpler path to deploy containerized web services without managing a full orchestrator.

## When to Use It

- Use it for HTTP applications that fit a managed container platform model.
- Use it when you want more packaging control than a function platform provides without running Kubernetes.
- Use it for internal tools or application fronts that can be deployed from source or container images.

## When Not to Use It

- Do not use it if the workload needs deep container orchestration features that App Runner does not expose.
- Do not assume container hosting removes the need for secret management, observability, and scaling review.

## Cloud Engineering Considerations

### Identity and Access

Separate deployment roles, runtime roles, and registry access so the application only gets the permissions it needs.

### Networking

Review ingress exposure and how the service reaches databases, APIs, or private AWS resources.

### Security

Keep images current, protect runtime secrets, and review public endpoint exposure deliberately.

### Observability

Monitor request behavior, deployment status, and container logs so application health stays visible.

### Cost

Runtime hours and scaling behavior determine cost, so idle services and oversized configurations matter.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [AWS App Runner documentation](https://docs.aws.amazon.com/apprunner/)
- [App Runner developer guide](https://docs.aws.amazon.com/apprunner/latest/dg/what-is-apprunner.html)
