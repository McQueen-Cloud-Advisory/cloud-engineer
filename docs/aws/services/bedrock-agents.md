# Agents for Amazon Bedrock

## Purpose

Agents for Amazon Bedrock orchestrates model reasoning, tools, and multi-step execution inside a managed AWS service.

## What Problem It Solves

It reduces custom orchestration work when an AI application needs to call tools, retrieve knowledge, and manage intermediate steps.

## When to Use It

- Use it when the application needs tool use or multi-step agent behavior.
- Use it when you want a managed orchestration layer around Bedrock models.
- Use it when integrating retrieval and tool execution into a user-facing workflow.

## When Not to Use It

- Do not add agent orchestration before validating that the task actually needs it.
- Do not rely on the agent framework alone for security, tool permissions, or output review.

## Cloud Engineering Considerations

### Identity and Access

Limit which tools and data sources the agent can call and review those permissions explicitly.

### Networking

Plan how the agent reaches downstream tools and whether those services require controlled network paths.

### Security

Treat tool invocation and retrieved context as part of the attack surface, especially for prompt injection and data exposure.

### Observability

Track agent failures, tool call behavior, and outcome quality, not just raw model latency.

### Cost

Agent orchestration can increase overall model and retrieval usage, so observe multi-step execution cost.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Agents for Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/latest/userguide/agents.html)
- [Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/)
