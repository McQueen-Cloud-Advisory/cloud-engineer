# AI and Agentic Workloads on Google Cloud

## Purpose

This page frames modern AI and agentic systems on Google Cloud as cloud engineering workloads with deployment, security, observability, and governance needs.

## What Problem It Solves

It helps teams connect model access, retrieval, agent behavior, runtime integration, and safety controls into one operating model.

## When to Use It

- Use it when planning how generative AI features fit into a Google Cloud architecture.
- Use it when a workload needs model access, retrieval, tools, or multi-step agent behavior.
- Use it when AI systems need to be treated like production cloud workloads rather than isolated experiments.

## When Not to Use It

- Do not start with agent orchestration if a narrow prompt workflow is enough.
- Do not treat AI as separate from identity, data access, secrets, and monitoring design.

## Cloud Engineering Considerations

### Identity and Access

Review which service accounts can call models, access source data, and operate supporting runtimes.

### Networking

Plan how model-serving paths, retrieval systems, and user-facing services connect, especially when private access matters.

### Security

Address prompt injection, data classification, output review, and AI safety controls before production rollout.

### Observability

Track latency, model failures, retrieval quality, and user-facing outcomes as one system.

### Cost

Model usage, retrieval, and runtime hosting can grow quickly, so usage visibility and budget controls matter.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Vertex AI generative AI overview](https://cloud.google.com/vertex-ai/generative-ai/docs/overview)
- [Vertex AI documentation](https://cloud.google.com/vertex-ai/docs/start/introduction-unified-platform)
