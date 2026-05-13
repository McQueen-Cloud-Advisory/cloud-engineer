# Agentic RAG Assistant on Azure

## Purpose

This pattern explains how to build an AI assistant on Azure that combines model access, retrieval, safety controls, and optionally agent orchestration.

## Pattern Summary

An agentic RAG assistant on Azure typically combines an application runtime, a managed model service, a retrieval layer over approved content, and a safety layer for prompt and output review. Azure OpenAI, Azure AI Search, Content Safety, and the broader Azure AI Foundry platform are common building blocks for this pattern.

This pattern matters because modern AI workloads are operational systems. They need identity, governance, observability, cost control, and clear failure behavior in addition to model quality.

## Common Use Cases

- Internal knowledge assistants
- Retrieval-backed support tools
- Guided AI application experiences

## Reference Architecture

```text
User
-> Container Apps or API Management
-> Azure OpenAI and Foundry Agent Service
-> Azure AI Search
-> Content Safety
-> Monitoring and secrets
```

## Provider Services

- Azure Container Apps
- Azure API Management
- Azure OpenAI
- Foundry Agent Service
- Azure AI Search
- Azure AI Content Safety
- Azure Key Vault
- Managed Identities
- Application Insights

## Design Considerations

### Security

Review prompt injection, source content trust, runtime identity, and safety checks as part of the initial design.

### Reliability

Design clear fallback behavior when search, model, or agent steps fail or return low-quality results.

### Observability

Track prompt volume, retrieval quality, latency, and user-facing outcomes, not only backend component health.

### Cost

Model usage, search, safety checks, and runtime hosting can all compound quickly, so usage visibility is essential.

### Deployment

Start with a small corpus and narrow workflow before expanding the system surface.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Official References

- [Azure OpenAI documentation](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- [Azure AI Search documentation](https://learn.microsoft.com/en-us/azure/search/)
- [Azure AI Content Safety documentation](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/)
- [Azure AI Foundry documentation](https://learn.microsoft.com/en-us/azure/ai-foundry/)
