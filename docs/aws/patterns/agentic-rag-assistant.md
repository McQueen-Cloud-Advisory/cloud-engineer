# Agentic RAG Assistant on AWS

## Purpose

This pattern explains how to build an AI assistant on AWS that combines model access, retrieval, guardrails, and optionally agent orchestration.

## Pattern Summary

An agentic RAG assistant pattern uses a managed model layer, a retrieval layer over approved content, and a front-end application or API that mediates user requests. On AWS, Amazon Bedrock, Knowledge Bases for Amazon Bedrock, Guardrails, and optionally Agents for Amazon Bedrock form the core managed building blocks.

This pattern matters because AI assistants are not only prompt flows. They are full application systems with security boundaries, data governance, observability requirements, and cost controls. Cloud engineers need to understand those layers before treating the assistant as production-ready.

## Common Use Cases

- Internal knowledge assistants
- Guided support tools
- Retrieval-backed Q&A applications

## Reference Architecture

```text
User
-> App Runner or API Gateway
-> Amazon Bedrock or Bedrock Agents
-> Knowledge Bases for Amazon Bedrock
-> Guardrails
-> Monitoring and logging
```

## Provider Services

- Amazon Bedrock
- Agents for Amazon Bedrock
- Knowledge Bases for Amazon Bedrock
- Guardrails for Amazon Bedrock
- AWS App Runner
- AWS Secrets Manager
- Amazon CloudWatch

## Design Considerations

### Security

Review prompt injection, source content trust, tool permissions, and user access boundaries as part of the architecture.

### Reliability

Design for degraded behavior when retrieval fails, the model is unavailable, or an agent tool call does not complete as expected.

### Observability

Track prompt volume, retrieval quality, tool behavior, latency, and user-facing outcomes rather than only raw model responses.

### Cost

Model usage, retrieval, orchestration, and runtime hosting can all grow quickly, so usage visibility is essential.

### Deployment

Start with a narrow corpus and a small application surface, then expand only after the logging, safety, and access model are clear.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Official References

- [Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/)
- [Knowledge Bases for Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html)
- [Guardrails for Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/latest/userguide/guardrails.html)
