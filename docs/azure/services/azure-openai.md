# Azure OpenAI

## Purpose

Azure OpenAI provides managed access to OpenAI models within Azure platform controls.

## What Problem It Solves

It gives teams a model-serving path that can be integrated into Azure security, identity, and operational tooling.

## When to Use It

- Use it when an application needs foundation model access inside Azure.
- Use it for prompt-based features, assistants, or RAG applications that fit the Azure ecosystem.
- Use it when model usage needs to sit within broader Azure governance patterns.

## When Not to Use It

- Do not treat model access as the whole application architecture.
- Do not move sensitive prompts or data into production without clear governance and review.

## Cloud Engineering Considerations

### Identity and Access

Use Entra ID, managed identities, and scoped permissions so model access is limited to the right workloads and operators.

### Networking

Review how applications reach the model endpoint and how that endpoint fits into wider data and network controls.

### Security

Design for prompt safety, data classification, output review, and integration with content or policy controls.

### Observability

Track latency, failures, token usage, and application outcome quality together.

### Cost

Model and token usage can grow quickly during development and production traffic.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Azure OpenAI documentation](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- [Azure OpenAI overview](https://learn.microsoft.com/en-us/azure/ai-services/openai/overview)
