# Guardrails for Amazon Bedrock

## Purpose

Guardrails for Amazon Bedrock helps teams apply policy controls around model interactions and outputs.

## What Problem It Solves

It gives AI applications a managed way to reduce unsafe or non-compliant outputs before they reach end users or downstream systems.

## When to Use It

- Use it when an AI workload needs content filtering or response policy checks.
- Use it when governance requirements need to be visible in the application design.
- Use it when different AI experiences need different levels of restriction or review.

## When Not to Use It

- Do not assume a guardrail replaces application-level validation or human review where required.
- Do not wait until late testing to define what acceptable model behavior looks like.

## Cloud Engineering Considerations

### Identity and Access

Control who can configure guardrails and which applications are allowed to use them.

### Networking

Guardrails fit into the application path where prompts and outputs are exchanged, so plan the request path end to end.

### Security

Use guardrails as one layer in a broader safety model that also includes prompt design, retrieval control, and output handling.

### Observability

Track when guardrails are triggered so application teams can review false positives, false negatives, and risky inputs.

### Cost

Guardrails add part of the total AI request path cost, so monitor how often they are applied and where they deliver value.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Guardrails for Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/latest/userguide/guardrails.html)
- [Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/)
