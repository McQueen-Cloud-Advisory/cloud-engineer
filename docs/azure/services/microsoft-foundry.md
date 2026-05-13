# Microsoft Foundry

## Purpose

Microsoft Foundry, through Azure AI Foundry, provides a platform surface for building, evaluating, and operating AI applications on Azure.

## What Problem It Solves

It gives teams a managed environment for organizing model access, safety, evaluation, and application workflows in one platform context.

## When to Use It

- Use it when building AI workloads that need more than a single model endpoint.
- Use it when teams need a clearer platform for AI evaluation, management, and integration.
- Use it when AI work needs to fit into Azure governance and operational patterns.

## When Not to Use It

- Do not treat the platform as a substitute for defining retrieval, safety, and application boundaries.
- Do not expand tool choice faster than the team can operate and evaluate it.

## Cloud Engineering Considerations

### Identity and Access

Review who can create projects, use models, and manage associated data or search resources.

### Networking

Plan how the AI platform interacts with search, storage, application runtimes, and governance controls.

### Security

Use the platform as part of a wider AI safety and governance approach rather than as a stand-alone control.

### Observability

Track usage, evaluation results, latency, and integration failures as part of the workload lifecycle.

### Cost

Model usage and connected platform services can increase cost quickly during experimentation.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Azure AI Foundry documentation](https://learn.microsoft.com/en-us/azure/ai-foundry/)
- [What is Azure AI Foundry](https://learn.microsoft.com/en-us/azure/ai-foundry/what-is-azure-ai-foundry)
