# Agentic RAG Assistant on Google Cloud

## Purpose

This pattern explains how to build an AI assistant on Google Cloud that combines model access, retrieval, safety controls, and optionally custom agent logic.

## Pattern Summary

An agentic RAG assistant on Google Cloud typically combines an application runtime such as Cloud Run, model access through Vertex AI, retrieval or agent capabilities through Agent Builder, and safety controls such as Model Armor. Supporting services for identity, secrets, and monitoring are part of the architecture, not side details.

This pattern matters because AI applications are operational systems. They need identity, observability, cost visibility, data governance, and clear failure behavior in addition to model quality.

## Common Use Cases

- Internal knowledge assistants
- Retrieval-backed support tools
- Guided AI application workflows

## Reference Architecture

```text
User
-> Cloud Run
-> Vertex AI and Agent Builder
-> Retrieval and safety layers
-> Secrets and monitoring
```

## Provider Services

- Cloud Run
- Vertex AI
- Vertex AI Agent Builder
- Agent Development Kit
- Model Garden
- Model Armor
- Secret Manager
- Cloud Monitoring

## Design Considerations

### Security

Review prompt injection, source data trust, runtime identity, and safety controls as part of the initial design.

### Reliability

Define how the system should behave when retrieval fails, models time out, or an agent step produces poor results.

### Observability

Track request volume, retrieval quality, latency, and user-facing outcomes across the full request path.

### Cost

Model usage, retrieval, safety checks, and runtime hosting can all compound quickly, so cost visibility is essential.

### Deployment

Start with a narrow corpus and simple workflow before expanding the surface area of the assistant.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Official References

- [Vertex AI documentation](https://cloud.google.com/vertex-ai/docs)
- [Agent Builder documentation](https://docs.cloud.google.com/agent-builder)
- [Model Armor overview](https://cloud.google.com/security/products/model-armor)
