# Azure AI Content Safety

## Purpose

Azure AI Content Safety helps evaluate prompts and outputs for unsafe or policy-sensitive content.

## What Problem It Solves

It adds a managed control layer for AI applications that need content review before inputs or outputs move further through the system.

## When to Use It

- Use it when AI applications need policy checks on prompts or responses.
- Use it when governance requirements need to be explicit in the application flow.
- Use it to reduce unsafe output risk in production-facing AI experiences.

## When Not to Use It

- Do not assume it replaces application-specific validation or human review.
- Do not add it without defining what acceptable and unacceptable content means for the workload.

## Cloud Engineering Considerations

### Identity and Access

Limit who can configure safety settings and which workloads can call the service.

### Networking

Plan where safety checks are applied in the request path and how the AI app reaches the service.

### Security

Use it as one control in a broader safety design that also includes prompt design, retrieval governance, and access control.

### Observability

Track safety events so teams can review false positives, false negatives, and recurring risky input patterns.

### Cost

Safety checks add cost to the AI path, so track where and how often they are being applied.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Azure AI Content Safety documentation](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/)
- [Azure AI Content Safety overview](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/overview)
