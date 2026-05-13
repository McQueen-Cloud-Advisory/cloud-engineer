# Model Armor

## Purpose

Model Armor helps apply safety and content controls around AI interactions on Google Cloud.

## What Problem It Solves

It provides a managed safety layer for prompts and outputs so AI applications can enforce policy before results reach users or downstream systems.

## When to Use It

- Use it when AI applications need prompt or response safety controls.
- Use it when policy enforcement should be explicit in the AI request path.
- Use it as part of a broader AI risk mitigation approach on Google Cloud.

## When Not to Use It

- Do not assume safety controls replace application-specific validation or human review.
- Do not wait until late testing to define acceptable model behavior.

## Cloud Engineering Considerations

### Identity and Access

Control who can configure safety behavior and which workloads can use it.

### Networking

Plan where safety checks sit in the request path and how application runtimes reach them.

### Security

Use it as one control in a broader design that also includes retrieval governance, prompt design, and access control.

### Observability

Track safety events so teams can review patterns, false positives, and risky inputs.

### Cost

Safety processing adds cost to the AI path, so monitor where and how often it is used.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Model Armor overview](https://cloud.google.com/security/products/model-armor)
- [Vertex AI generative AI overview](https://cloud.google.com/vertex-ai/generative-ai/docs/overview)
