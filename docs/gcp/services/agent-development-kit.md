# Agent Development Kit

## Purpose

The Agent Development Kit page covers Google Cloud-adjacent tooling for building custom agent behavior that still needs a clear runtime, identity, and evaluation model.

## What Problem It Solves

It helps teams think about the application layer of agent development instead of treating managed platform features as the entire solution.

## When to Use It

- Use it when a custom agent workflow needs more control than a narrow managed configuration provides.
- Use it when the team needs to reason about tools, prompts, evaluation, and runtime behavior together.
- Use it when agent logic must fit into a larger Google Cloud deployment and operations model.

## When Not to Use It

- Do not adopt custom agent tooling before validating that the use case needs it.
- Do not separate agent code from the identity, safety, and observability concerns of the surrounding system.

## Cloud Engineering Considerations

### Identity and Access

Review which service accounts can reach models, tools, and data sources used by the agent workflow.

### Networking

Plan how the agent runtime communicates with models, retrieval systems, and application backends.

### Security

Custom agent behavior increases the surface area for prompt injection, unsafe tool use, and data leakage, so controls need to be explicit.

### Observability

Track tool usage, step failures, latency, and end-user outcomes as part of the application lifecycle.

### Cost

Custom agent flows can increase model and infrastructure usage, so monitor the whole request path.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Agent Engine overview](https://docs.cloud.google.com/vertex-ai/generative-ai/docs/agent-engine/overview)
- [Vertex AI generative AI overview](https://cloud.google.com/vertex-ai/generative-ai/docs/overview)
