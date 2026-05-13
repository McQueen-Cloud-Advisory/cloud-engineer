# Foundry Agent Service

## Purpose

Foundry Agent Service provides a managed layer for building and operating agent-style AI workflows on Azure.

## What Problem It Solves

It reduces custom orchestration work when an Azure AI application needs tool use, retrieval, or multi-step behavior.

## When to Use It

- Use it when an AI workflow needs more than a single model prompt and response.
- Use it when Azure AI applications need a managed agent runtime path.
- Use it when tool invocation and multi-step reasoning must be part of the design.

## When Not to Use It

- Do not add agent orchestration before confirming the use case actually needs it.
- Do not rely on the agent layer alone for security, access control, or evaluation.

## Cloud Engineering Considerations

### Identity and Access

Review which identities can configure the agent and which tools or data sources the agent can reach.

### Networking

Plan how the agent runtime reaches models, search services, and application backends.

### Security

Treat tools, retrieved content, and prompts as part of the AI attack surface.

### Observability

Track tool calls, step failures, and user-facing outcomes, not just prompt latency.

### Cost

Agent workflows can drive additional model and tool usage, so monitor full request cost rather than only model calls.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Azure AI Foundry documentation](https://learn.microsoft.com/en-us/azure/ai-foundry/)
- [Azure AI Foundry overview](https://learn.microsoft.com/en-us/azure/ai-foundry/what-is-azure-ai-foundry)
