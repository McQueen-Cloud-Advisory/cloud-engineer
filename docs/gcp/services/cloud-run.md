# Cloud Run

## Purpose

Cloud Run runs containerized applications on a managed platform designed for web services and event-driven workloads.

## What Problem It Solves

It gives teams a serverless container platform with more packaging control than a function runtime.

## When to Use It

- Use it for containerized APIs and application front ends.
- Use it when the workload needs an HTTP service or managed container runtime.
- Use it when you want container packaging without operating a cluster.

## When Not to Use It

- Do not use it if the workload requires an orchestration model beyond what Cloud Run exposes.
- Do not assume container hosting removes the need for secret handling, scaling review, or monitoring.

## Cloud Engineering Considerations

### Identity and Access

Use service accounts for runtime access and separate deployment permissions from runtime permissions.

### Networking

Review public versus internal services, ingress settings, and how the service reaches data or model backends.

### Security

Keep images current, restrict runtime privileges, and review public endpoint exposure deliberately.

### Observability

Monitor request latency, scaling behavior, container logs, and downstream dependencies.

### Cost

Runtime resource choices, request volume, and scale behavior drive cost.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Serverless API](../patterns/serverless-api.md)
- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Cloud Run documentation](https://cloud.google.com/run/docs)
- [What is Cloud Run](https://cloud.google.com/run/docs/overview/what-is-cloud-run)
