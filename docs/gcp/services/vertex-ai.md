# Vertex AI

## Purpose

Vertex AI is Google Cloud's managed AI platform for model access, development, and deployment workflows.

## What Problem It Solves

It gives teams a managed platform for building AI applications without assembling every model and tooling component from scratch.

## When to Use It

- Use it when applications need model access inside Google Cloud.
- Use it for generative AI, evaluation, and broader ML platform workflows.
- Use it when AI workloads need to fit into Google Cloud governance and operations.

## When Not to Use It

- Do not treat model access as the whole architecture when retrieval, safety, or runtime concerns are still undefined.
- Do not expand platform usage faster than the team can evaluate and operate it safely.

## Cloud Engineering Considerations

### Identity and Access

Review which service accounts can access models, data, and surrounding AI platform resources.

### Networking

Plan how AI runtimes, retrieval layers, and application services connect to Vertex AI endpoints.

### Security

Address data classification, prompt safety, and output handling as part of the design, not after deployment.

### Observability

Track model usage, failures, latency, and outcome quality as part of the application lifecycle.

### Cost

Model usage and supporting AI platform features can increase cost quickly during experimentation and production.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Vertex AI documentation](https://cloud.google.com/vertex-ai/docs)
- [Vertex AI overview](https://cloud.google.com/vertex-ai/docs/start/introduction-unified-platform)
