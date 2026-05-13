# Vertex AI Agent Builder

## Purpose

Vertex AI Agent Builder provides managed tools for building search, retrieval, and agent-style experiences on Google Cloud.

## What Problem It Solves

It reduces custom integration work when an AI application needs grounded retrieval or higher-level agent capabilities.

## When to Use It

- Use it for retrieval-backed assistant experiences.
- Use it when AI applications need managed search or agent building blocks.
- Use it when the team wants Google Cloud-managed tooling around agentic application flows.

## When Not to Use It

- Do not use it before the source content and retrieval goals are clear.
- Do not assume managed tooling removes the need for evaluation, access control, and safety review.

## Cloud Engineering Considerations

### Identity and Access

Review who can configure agent builder resources and which runtimes can query them.

### Networking

Plan how the application runtime reaches retrieval and agent services and how source content is made available.

### Security

Treat indexed content, retrieval responses, and agent interactions as part of the application attack surface.

### Observability

Monitor retrieval quality, latency, and application outcomes rather than only component availability.

### Cost

Search, retrieval, and connected model usage all contribute to total cost.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Agent Builder documentation](https://docs.cloud.google.com/agent-builder)
- [Agent Builder introduction](https://docs.cloud.google.com/generative-ai-app-builder/docs/introduction)
